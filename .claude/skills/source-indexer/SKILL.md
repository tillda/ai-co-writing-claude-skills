---
name: source-indexer
description: Scaffold or refresh per-book /sources/<book>/index.md files (and the top-level /sources/catalog.yaml). Scaffold mode generates a fresh MD index from a source's headings; refresh mode preserves all human-written prose and only updates derived line/page ranges. Use when adding new sources or after editing source files.
---

# Source Indexer

Builds and maintains the per-book `index.md` files that make subchapter-precise source resolution possible. The book index is **markdown**: human-readable, prose-friendly, with structured data inline in headings and frontmatter.

## When to invoke

- "reindex sources"
- "scaffold an index for the new book I just added"
- "refresh Understanding Knowledge"
- After dropping a new chapter into `/sources/<book>/`
- After editing a source file (re-OCR, fixed headings, etc.)

The skill never edits source files. It only writes:
- `/sources/<book>/index.md` (the per-book index)
- `/sources/catalog.yaml` (the small generated catalog)

## Format of `/sources/<book>/index.md`

```markdown
---
slug: understanding-knowledge
title: Understanding Knowledge
author: Michael Huemer
kind: book
tags: [epistemology]
generated: 2026-04-28
---

# Understanding Knowledge

<optional book-level prose intro>

## Chapter 2 · Induction
`cite: huemer-uk-ch02 · file: 02-induction.md · format: md`

**Summary.** Hume's problem of induction and Huemer's reply.

Use this chapter whenever the essay asks about Hume's problem or
the rationality of inductive inference.

### 2.1 The Problem [37-88]

### 2.3 Counterexamples [180-240]

#### 2.3.4 The Zebra and the Mule [221-240]

Canonical zebra/mule counterexample to reliabilism.

## Chapter 14 · Scientific Knowledge
`cite: huemer-uk-ch14 · file: 14-scientific-knowledge.pdf · format: pdf`

Default chapter for prompts about scientific realism vs anti-realism.

### 14.2 The No-Miracles Argument [pp. 309-318]

Concise version of the no-miracles argument.
```

### Conventions

- **Frontmatter** carries book-level structured data (`slug`, `title`, `author`, `kind`, `tags`, `generated`).
- **Chapter headings** are H2: `## Chapter <N> · <Name>`.
- **Chapter metadata line** is a single backtick-fenced inline-code line directly under the chapter heading: `` `cite: <key> · file: <relative-path> · format: md|pdf|html|txt` ``. Fields separated by ` · `.
- **Optional summary**: a paragraph starting with `**Summary.**` immediately after the metadata line.
- **Chapter notes**: any free prose paragraphs between the metadata/summary and the first H3.
- **Section headings** are H3 / H4 / H5: `### <ref> <Name> [<a>-<b>]` for MD/TXT/HTML, `### <ref> <Name> [pp. <a>-<b>]` for PDF.
- **Section notes**: any free prose between the section heading and the next section heading (of any level) or next chapter.

### Three roles in a section heading

A section heading has three slots, each with a different job:

| Slot | Role | Stability | Owner |
|------|------|-----------|-------|
| `<ref>` (e.g. `2.3.4`) | **Identifier** — the match key | Stable across re-OCR | The book |
| `<Name>` | **Documentation** — for the human reader | Mostly stable; user may tweak | The user |
| `[<a>-<b>]` | **Derived range** — what to read | Volatile; recomputed every refresh | The indexer |

**The identifier is `<ref>`, not the bracket.** The indexer matches index entries to source headings by `<ref>` (`2.3.4`), then writes the freshly-derived range into `[<a>-<b>]`. The bracket is the indexer's only writable target on a heading line; everything else is preserved verbatim.

Use plain ASCII hyphen (`-`) inside the bracket, not en-dash, to keep grep/sed simple.

### Books without numbered sections

Some books just have `## Introduction`, `## The Argument`, `## Conclusion` — no dotted numbers.

For those, the indexer assigns synthetic numeric prefixes at scaffold time:

```markdown
### 1 Introduction [10-45]
### 2 The Argument [46-180]
### 3 Replies [181-220]
### 4 Conclusion [221-240]
```

The number is arbitrary — just a stable handle. The indexer numbers sections in source order at scaffold time; refresh matches by number-then-name. If the user reorders or renames sections in the index, the synthetic numbers are still the match key — they survive renames.

If the user prefers no synthetic prefix (e.g. wants `### Introduction [10-45]`), refresh falls back to matching by heading text (case-insensitive, whitespace-normalised). This is brittle — editing the title in the index breaks the link. Numbers are recommended.

## Two modes

The skill picks the mode automatically per book.

### Scaffold mode — `/sources/<book>/index.md` does not exist

Used when a book is new to the library.

1. List all chapter files in `/sources/<book>/` (excluding `index.md` itself).
2. For each MD file, extract numbered headings via grep:
   ```bash
   grep -nE '^#{2,6}[[:space:]]+[0-9]+(\.[0-9]+)*([[:space:]]|$)' "$file"
   ```
   Output looks like:
   ```
   45:## 2.1 The Problem
   78:## 2.3 Counterexamples
   221:### 2.3.4 The Zebra and the Mule
   ```
   Parse each line: split on `:`, count the leading `#` characters for level, extract the dotted ref (first whitespace-separated token after the hashes), the rest is the name.
3. Compute ranges per section:
   - Sort headings by line number.
   - Each section runs from its own heading line through the line before the next equal-or-higher-level heading.
   - The last section runs to EOF (use `wc -l "$file"` for the line count).
4. For each non-MD file (PDF/HTML/TXT):
   - For PDFs, attempt to extract bookmarks first; if found, use those.
   - Otherwise ask the user (via AskUserQuestion) for the chapter's TOC and explicit page/line ranges.
5. Write `/sources/<book>/index.md`:
   - Frontmatter with book-level fields (some empty as placeholders).
   - One H2 per chapter, with the inline metadata line.
   - Suggest a default `cite` per chapter (e.g. `huemer-uk-ch02`); leave `summary` blank.
   - Empty prose under the chapter heading (the user fills in `notes`).
   - One H3/H4/H5 per section with the range marker; empty prose under each (the user adds per-section `note` if wanted).
6. Regenerate `/sources/catalog.yaml`.

### Refresh mode — `/sources/<book>/index.md` already exists

Used when a book already has an index and the user wants to pick up changes.

1. Load the existing `index.md`. Preserve all prose. The only thing that gets updated is the range marker `[<a>-<b>]` (or `[pp. <a>-<b>]`) in section headings, and possibly the chapter metadata line (`file:` if a file was renamed).
2. **For each MD chapter:**
   - Re-run the heading-extraction grep on the source file.
   - For each section heading in the index, find the matching source heading by **section ref** (`2.3.4`) — not by name. The user may have edited the index's section name to something more descriptive; that's fine, the ref is the match key. Replace the `[a-b]` marker with the freshly-derived range.
   - For unnumbered books (synthetic-prefix mode), match by the synthetic number first; fall back to heading text only if numbers are absent in the index.
   - For each section heading present in the source but missing from the index, append a new section entry inside that chapter's H2 block, with empty prose. Place it after the last existing section in that chapter.
   - For each section heading present in the index but missing from the source, **leave it alone** but flag a warning ("section 14.5 in index has no matching heading in source"). The user resolves explicitly.
3. **For each non-MD chapter:** leave page/line ranges untouched (not re-derivable). Only update `file:` if the actual filename changed.
4. **Never touch:** chapter notes, section notes, summary, cite, frontmatter `tags`, or any prose the user wrote.
5. Regenerate `/sources/catalog.yaml`.

## Parsing trick for MD index round-trip

When refreshing, parse the existing index.md line by line and treat it as a sequence of segments:
- Frontmatter (between `---` markers): preserve `slug`, `title`, `author`, `kind`, `tags`. Update `generated` to today.
- Body: walk lines tracking the current chapter (last `^## ` heading) and section (last `^#{3,6} ` heading). For each section heading, regex-replace the `\[(pp\. )?[0-9]+-[0-9]+\]` marker with the new range. Everything between section headings is prose to preserve verbatim.

In code:
```bash
# Pseudocode for the range update inside one heading line
sed -E 's/\[(pp\. )?[0-9]+-[0-9]+\]/[\1<NEW_START>-<NEW_END>]/'
```

For the cite/file line under a chapter heading: it's identifiable by being a single-line inline-code paragraph starting with `` ` `` containing `cite:` and `file:`. Update only `file:` if needed; leave `cite:` and `format:` alone.

## Catalog regeneration

After per-book work, regenerate `/sources/catalog.yaml`:

- Walk `/sources/*/index.md`.
- For each, parse the frontmatter and copy: `slug`, `title`, `author`, `kind`, `tags`.
- Pull a `summary:` field if a `**Summary.**` paragraph exists at the top of the body (book-level).
- Add `index: sources/<slug>/index.md`.
- Sort by `slug` for stable diffs.

`catalog.yaml` stays YAML — it's purely generated, no human curation expected.

## Validation

Run after every invocation:

- Every section heading has a parseable range marker.
- `cite` keys are unique across the whole library (only flag when both filled in; empty placeholders are OK).
- Every `file:` referenced exists on disk under `/sources/<book>/`.
- For each `/courses/*/index.md`:
  - Every book listed under frontmatter `books:` exists in `catalog.yaml`.
  - Every entry under any module's `**Sources:**` list resolves through the fuzzy resolver (warn for unresolved).

## Run summary format

Print at the end of every run. Keep it short and scannable:

```
Indexed: 2 books, 12 chapters, 47 sections.
- understanding-knowledge: 8 chapters, 31 sections (refreshed; 2 new sections in ch. 11)
- paradox-lost: 4 chapters, 16 sections (scaffolded)
Catalog: 2 books listed.
Validation: OK.
Warnings: ch. 14 in understanding-knowledge lists "14.5" with no matching heading in source.
```

## What this skill does NOT do

- Never edits source files (`.md`, `.pdf`, etc.).
- Never deletes or modifies user prose in `index.md`.
- Never modifies `/courses/*/index.md`.
- Never writes essays or modifies prompts.

## Implementation notes

- For MD heading extraction, use `grep -nE` (the regex above). It's a deterministic, fast, well-tested approach.
- For range update on refresh, prefer line-aware editing over a regex sweep of the whole file: walk lines, identify section headings, update only those.
- When parsing YAML frontmatter, accept loose formatting (lists may be inline `[a, b]` or block-style).
- Keep diffs small: don't reflow prose, don't reorder sections that are already present, don't normalize whitespace beyond what's necessary.
