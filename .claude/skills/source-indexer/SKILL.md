---
name: source-indexer
description: Scaffold or refresh per-book /sources/<book>/index.md files (and the top-level /sources/catalog.yaml). Scaffold mode generates a fresh MD index from a source's headings, including a per-chapter `**Topics:**` keyword line for soft topic matching. Refresh mode preserves all human-written prose and only updates derived line/page ranges. Optionally accepts one or two course slugs; when given, the indexer reads those courses and biases Topics extraction toward course-vocabulary matches. The skill never emits authoritative `- Use <ref> for <topic>` bullets — those are produced exclusively by `accept-canonical-chapters`. Use when adding new sources or after editing source files.
---

# Source Indexer

Builds and maintains the per-book index files that make subchapter-precise source resolution possible. The index is **markdown**: human-readable, prose-friendly, with structured data inline in headings and frontmatter.

The indexer's output for reverse-mode matching is the per-chapter `**Topics:**` line — a soft surface that surfaces the chapter as a *candidate* when a prompt topic matches. The hard surface — `- Use <ref> for <topic>` bullets that bind a topic to a specific section as canonical — is produced only by the separate `accept-canonical-chapters` skill, and only with explicit user approval. The indexer preserves any such bullets it finds on refresh but never generates them.

Two layouts exist, both valid:

- **Inline layout** (default for small books) — single `index.md` carries everything: book metadata, chapter blocks, section headings with line ranges, prose.
- **Split layout** (default for ≥500-line indexes or ≥10 chapters with subsections) — short `index.md` carries book metadata + per-chapter topic annotations only; line ranges and structural detail live in per-chapter `index-ch<NN>.md` files.

The resolver always opens `index.md` first; whether it then opens a per-chapter file depends on layout. Reverse-mode (topic-only matching) reads only the short `index.md`. Forward-mode and post-match resolution read the matching per-chapter file when split.

## When to invoke

- "reindex sources"
- "scaffold an index for the new book I just added"
- "refresh Understanding Knowledge"
- "index Understanding Knowledge against the epistemology course" (course-aware Topics)
- "index Paradox Lost against logic and intro-to-philosophy" (two-course)
- After dropping a new chapter into `/sources/<book>/`
- After editing a source file (re-OCR, fixed headings, etc.)
- "split this index" — to migrate an inline-layout book to split layout

The skill never edits source files. It only writes:
- `/sources/<book>/index.md` (the per-book index)
- `/sources/<book>/index-ch<NN>.md` (per-chapter files, split layout only)
- `/sources/catalog.yaml` (the small generated catalog)

## Inputs

- `<book-slug>` — required. Either a book that already exists at `/sources/<book>/` (refresh) or a book directory just populated by `source-ingestor` (scaffold).
- `<course-slug>` — optional, 0–2 entries. When supplied, the indexer reads `/courses/<course>/index.md` and uses that course's vocabulary (module names, per-module `**Sources:**` and `**Readings:**` text, module prose) as soft context when generating Topics — biasing the wording toward course terminology where the chapter genuinely discusses overlapping material. Two slugs are accepted because a single book can occasionally span two courses (rare). More than two: ask the user to pick at most two — Topics with too many course filters becomes noisy.

A course argument applies only to **Topics** generation. It never causes the indexer to emit `- Use ...` bullets, and it never edits course-MD files.

## Layout decision

At scaffold time, choose the layout based on the source.

**Use split layout** when at least one of:
- The would-be inline `index.md` would exceed ~500 lines.
- The book has ≥10 chapters with subsections (any heading style).
- The user explicitly requests it.

**Use inline layout** otherwise. Small books (a few short chapters) read better as one file.

The chosen layout is recorded in the short index frontmatter as `chapter-indexes: split` or `chapter-indexes: inline`. Refresh mode reads this field to know which logic to apply.

A book can be migrated between layouts (split → inline or inline → split) on request — see "Migration mode" below.

## Format — short `index.md` (split layout)

```markdown
---
slug: understanding-knowledge
title: Understanding Knowledge
author: Michael Huemer
kind: book
tags: [epistemology]
generated: 2026-05-03
chapter-indexes: split
---

# Understanding Knowledge

<optional book-level prose intro>

**Usage:** <one-line policy on how to deploy this book by default — e.g. "Canonical reference; prefer over Readings where they overlap", "Lay introduction; reinforces but does not override academic positions", "Skip technical chapters 5-7 unless prompt demands depth". Leave the placeholder text in to signal "unfilled"; replace it when the policy is decided.>

## Chapter 2 · What is Knowledge?
`cite: huemer-uk-ch02 · file: 02-what-is-knowledge.md · format: md`

<optional chapter prose: notes, summary, scope guidance>

**Topics:** Gettier, reliabilism, proper function, sensitivity, tracking, safety, relevant alternatives, defeasibility, Lockean theory, Wittgenstein

## Chapter 3 · ...
```

`- Use <ref> for <topic>` bullets, when present, sit directly under the `**Topics:**` line. The indexer never emits them at scaffold time and never edits them on refresh — they're written and maintained by `accept-canonical-chapters`. A chapter block in a curated book typically looks like:

```markdown
## Chapter 2 · What is Knowledge?
`cite: huemer-uk-ch02 · file: 02-what-is-knowledge.md · format: md`

**Topics:** Gettier, reliabilism, proper function, sensitivity, tracking, safety, relevant alternatives, defeasibility, Lockean theory, Wittgenstein

- Use 2.4 for Gettier's refutation
- Use 2.5.2 for reliabilism
- Use 2.5.4 for sensitivity / tracking
```

The short index has **no line ranges**. Line ranges live in per-chapter files. The short index is the always-read entry point — fast to scan, cheap to keep in context.

### Conventions (split layout, short index)

- **Frontmatter** carries book-level structured data plus `chapter-indexes: split`.
- **Chapter headings** are H2: `## Chapter <N> · <Name>`.
- **Chapter metadata line** is a single backtick-fenced inline-code line directly under the chapter heading: `` `cite: <key> · file: <relative-path> · format: md|pdf|html|txt` ``. Same fields as inline layout.
- **Chapter prose** (optional) — any free paragraphs between metadata line and `**Topics:**` or first bullet. Author-curated guidance: scope, summary, when to invoke.
- **`**Topics:**` line** (auto-generated, user-editable) — comma-separated keyword list for at-a-glance reverse-mode matching. **Soft surface**: a topic match here surfaces the chapter as a candidate; the resolver does not auto-read on a Topics match alone. Lowercased except for proper nouns.
- **Bullet list** of `- Use <ref> for <topic-phrase>` annotations (optional; absent on a freshly-scaffolded book). Each bullet binds a section ref (e.g. `2.5.2`) to a topic phrase. **Hard surface**: a topic match here is authoritative; the resolver parses the ref and reads the section directly. Bullets are produced exclusively by `accept-canonical-chapters` via explicit user approval — the indexer never writes or modifies them, and only preserves them verbatim across refresh.
- **No section headings.** All H3/H4/H5 headings live in per-chapter files.
- **Per-chapter file pointer is implicit by convention:** `index-ch<NN>.md` where `<NN>` is the chapter number zero-padded to 2 digits (`index-ch02.md`, `index-ch14.md`). The chapter heading's `<N>` supplies the number. No explicit pointer field needed.

### Book-level `**Usage:**` block

A short hand-authored hint describing how the book should be deployed by default whenever the resolver loads it. Lives near the top of the index, after the H1 intro paragraph(s) and before the first `## Chapter`.

- **Scaffold writes a placeholder** — the indexer emits a single `**Usage:**` line with placeholder text (e.g. `**Usage:** _(unfilled — add a one-line policy describing how to deploy this book)_`). The block is always present so the structural slot exists; the user fills the text in.
- **Refresh never touches it** — once written, the line is user-owned. Refresh mode preserves it verbatim, exactly like chapter prose, **Topics:**, and bullets. There is no auto-regeneration mode for `**Usage:**`.
- **One line, prose** — no list, no nested formatting. Same shape as a single bullet from the course-level `**Books usage:**` block, minus the leading dash and book name.
- **Course override** — a `**Books usage:**` line in `/courses/<course>/index.md` that names the same book overrides this hint within that course. The book-level hint is the cross-course default. The indexer does not maintain or validate this relationship — it only writes the book-level slot.

## Format — per-chapter `index-ch<NN>.md` (split layout)

```markdown
---
slug: understanding-knowledge
chapter: 2
generated: 2026-05-03
---

## Chapter 2 · What is Knowledge?
`cite: huemer-uk-ch02 · file: 02-what-is-knowledge.md · format: md`

<optional chapter prose, mirroring or extending the short-index prose>

### 2.1 The Project of Analyzing "Knowledge" [39-59]

### 2.2 The Traditional Analysis [60-94]

### 2.3 About "Justification" [95-128]

#### 2.3.1 The General Concept of Justification [97-104]

<optional per-section prose>

#### 2.3.2 Epistemic vs. Non-Epistemic Reasons [105-114]

...
```

### Conventions (split layout, per-chapter file)

- **Lightweight frontmatter** — `slug` (parent book), `chapter` (number), `generated` (date). No need to repeat `title`, `author`, `kind`, `tags` — those live in the short index.
- **Chapter heading** is H2 (matches the short index for consistency). The metadata line is duplicated from the short index; the indexer keeps both in sync on refresh.
- **Section headings** are H3 / H4 / H5 with composed `<chapter>.<local>` ref + name + line range: `### <chapter>.<local> <Name> [<a>-<b>]` (MD/TXT/HTML), `### <chapter>.<local> <Name> [pp. <a>-<b>]` (PDF). The leading `<chapter>.` is always present in the index, even when the source heading didn't carry a number — see "Heading conventions in source files" above.
- **Section prose** lives here, not in the short index.
- The per-chapter file is structurally a single chapter slice of the old monolithic format.

#### Example — same chapter, different source styles

Source `## 2.5 Reliabilism` (prefixed) → index `### 2.5 Reliabilism [128-201]`.
Source `## 5 Reliabilism` (local, in chapter 2) → index `### 2.5 Reliabilism [128-201]`.
Source `## Reliabilism` (unnumbered, fifth section under chapter 2 H1) → index `### 2.5 Reliabilism [128-201]`.

All three render identically in the index. The match key changes per style (full ref / tail-after-chapter / heading name) but downstream resolution is uniform.

### Three roles in a section heading

A section heading has three slots, each with a different job:

| Slot | Role | Stability | Owner |
|------|------|-----------|-------|
| `<ref>` (e.g. `2.3.4`) | **Identifier** — the match key (for `prefixed` and `local` styles) | Stable across re-OCR | The book |
| `<Name>` | **Documentation** for `prefixed`/`local`; **identifier** for `unnumbered` | Mostly stable; user may tweak | The user |
| `[<a>-<b>]` | **Derived range** — what to read | Volatile; recomputed every refresh | The indexer |

**For `prefixed` and `local` styles, the identifier is `<ref>`.** The indexer matches index entries to source headings by `<ref>` (composed `<chapter>.<local>` on the index side), then writes the freshly-derived range into `[<a>-<b>]`.

**For `unnumbered` books, the identifier is the normalised heading name** (case-insensitive, whitespace-collapsed). The leading number in the index ref is cosmetic — synthesised from source order and re-derived on every refresh. Renaming a section in source updates the name in the index; reordering sections updates the cosmetic numbers; either way Topics, prose, and any attached metadata follow the section by name.

Use plain ASCII hyphen (`-`) inside the bracket, not en-dash, to keep grep/sed simple.

## Format — `index.md` (inline layout)

Identical to the split-layout short index *except*:
- Frontmatter carries `chapter-indexes: inline`.
- Each chapter block, after the `**Topics:**` line (and any `Use` bullets, when present), also lists section headings inline (H3/H4/H5) with `[<a>-<b>]` ranges, followed by any per-section prose.
- No `index-ch<NN>.md` files exist for the book.

Suitable for short books.

## Heading conventions in source files

Source files come in three styles. The indexer detects the style per chapter at scaffold (and re-detects on refresh — no stored signal), and **always emits composed `<chapter>.<local>` refs in the index** regardless of style. Citations like `Grayling PL 5.2` resolve cleanly in every case.

| Style | Example source heading | Index heading |
|---|---|---|
| `prefixed` | `## 2.5 Reliabilism` | `### 2.5 Reliabilism [<a>-<b>]` |
| `local` | `## 2 The Argument` (in chapter 5) | `### 5.2 The Argument [<a>-<b>]` |
| `unnumbered` | `## Introduction` (in chapter 5, in source order = 1) | `### 5.1 Introduction [<a>-<b>]` |

For `unnumbered`, the leading number is **synthesised from source order** — first section under the chapter heading is `<chapter>.1`, second is `<chapter>.2`, etc. The number is cosmetic; the **stable identifier is the heading name** (case-insensitive, whitespace-collapsed). Renaming a section in source updates the index name. Reordering sections re-derives the numbers. Either way the bracket range and any attached metadata follow the section by name.

For `local` and `prefixed`, the **stable identifier is the ref** — index `5.2` matches source bare `2` (local) or source `5.2` (prefixed) directly.

The detection algorithm is in scaffold step 2 below.

## Topics extraction (scaffold mode)

For each chapter, the indexer emits a single `**Topics:**` line — a comma-separated keyword list. The skill is run by Claude, so Topics extraction is done by *reading the chapter and deciding what it discusses*, not by regex matching. This handles every heading convention naturally and produces better topics than any keyword heuristic.

### Procedure (per chapter, at scaffold time)

1. Read the chapter source file in full. For very large chapters (≳1500 lines), read all section headings plus the first ~30 lines under each section — enough to recognise what's discussed without loading the whole body.
2. If one or two `<course-slug>` arguments were supplied, read `/courses/<course>/index.md` and keep the course's module names, `**Sources:**` and `**Readings:**` entries available as soft context.
3. Generate one `**Topics:**` line: a comma-separated list of the philosophical concepts, positions, theories, arguments, paradoxes, principles, and named figures *actually discussed* in the chapter. Aim for 5–15 items. Use the chapter's own terminology where it has a settled name (e.g. *reliabilism*, *Brain-in-a-Vat argument*, *Occam's razor*); compress where the chapter is verbose.
4. **Course bias.** When a course slug is supplied and a topic the chapter discusses also appears as a course module name or in `**Sources:**` / `**Readings:**`, prefer the course's wording so reverse-mode matches line up. The course bias never *adds* topics the chapter doesn't actually discuss — it only chooses between equivalent phrasings.
5. **Skip the line entirely** if the chapter has no philosophical content (preface, acknowledgements, pure historical front-matter).
6. Lowercase each keyword except for proper nouns and acronyms.

### What the indexer does NOT generate

- **No `- Use <ref> for <topic>` bullets, ever.** Those are the exclusive output of `accept-canonical-chapters` and represent a deliberate user judgement that a specific section is the canonical text for a topic. The indexer cannot make that judgement and does not try.
- **No prose annotations under section headings.** Section-level prose is fully user-owned.

### Topics is scaffold-only

Refresh mode never re-runs Topics extraction. Once written, the `**Topics:**` line is user-owned (whether the user kept the scaffolded version, edited it, or replaced it). To regenerate Topics for a chapter — perhaps because a course has been added to scope — the user explicitly asks ("regenerate topics for ch 14 against the epistemology course") and the indexer reads that one chapter, regenerates only its `**Topics:**` line, and leaves everything else (chapter prose, `Use` bullets, section headings, ranges) intact.

Existing `- Use <ref> for <topic>` bullets are preserved verbatim through every refresh — same handling as chapter prose, frontmatter `tags`, and the book-level `**Usage:**` block. When refresh detects a new section in the source not present in any per-chapter file, it appends the new section heading to the chapter file but never adds a Use bullet for it.

## Two modes (plus migration)

The skill picks the mode automatically per book.

### Scaffold mode — `/sources/<book>/index.md` does not exist

Used when a book is new to the library.

1. List all chapter files in `/sources/<book>/` (excluding `index.md` itself).
2. **For each MD file, detect the heading convention and extract sections.**

   Pull all heading lines with `grep -nE '^#{1,6}[[:space:]]+' "$file"`. From those:

   - **Chapter number** — parse from the H1 line (e.g. `# 5 Truth: ...` → `5`) or from the filename (`05-...md` → `5`). The chapter number is needed for ref composition.
   - **End-matter stop list** — drop trailing blocks whose heading text matches `Notes`, `References`, `Bibliography`, or `Index` (case-insensitive, exact match) before picking the section level. A single trailing `## Notes` shouldn't fool the detector.
   - **Section level** — among the remaining headings, pick the smallest `#`-count that occurs ≥2 times. If only one heading appears below H1, use its level. Sub-section levels are one deeper, and so on.
   - **Style detection** at the section level:
     - `prefixed` — every section line matches `/^#+ \d+(\.\d+)+ /` (dotted ref, e.g. `## 2.5 ...`).
     - `local` — every section line matches `/^#+ \d+ /` with no dotted tail (e.g. `## 2 ...` restarting per chapter).
     - `unnumbered` — anything else (e.g. `## Introduction`, `## Three Distinctions`).
   - **Compose refs.** Always emit `<chapter>.<local>` in the index regardless of style:
     - `prefixed`: pass the dotted ref through verbatim.
     - `local`: prepend chapter number → source `## 2 Foo` in chapter 5 becomes index `### 5.2 Foo`.
     - `unnumbered`: number sections in source order (1, 2, 3, …) and prepend chapter → first section in chapter 5 becomes index `### 5.1 ...`. The leading number is cosmetic; the heading name is the stable identifier.
   - **Strip the leading number from the heading text** when composing the index entry. Source `## 2 The Argument` produces index `### 5.2 The Argument` (not `### 5.2 2 The Argument`).
   - **Sub-sections** at the next level deeper follow the same rule recursively. For unnumbered books, synthesise `5.1.1`, `5.1.2`, etc. from source order.
3. Compute ranges per section:
   - Sort headings by line number.
   - Each section runs from its own heading line through the line before the next equal-or-higher-level heading.
   - The last section runs to EOF (use `wc -l "$file"` for the line count).
4. For each non-MD file (PDF/HTML/TXT):
   - For PDFs, attempt to extract bookmarks first; if found, use those.
   - Otherwise ask the user (via AskUserQuestion) for the chapter's TOC and explicit page/line ranges.
5. Decide layout (split vs inline) using the threshold rule.
6. If one or two `<course-slug>` arguments were supplied, read each `/courses/<course>/index.md` so its module names + `**Sources:**` / `**Readings:**` are in context for Topics generation.
7. Generate `**Topics:**` per chapter by *reading the chapter* (with course MD in context if supplied) — see "Topics extraction" above.
8. Write files:
   - **Inline layout:** one `index.md` with frontmatter, the H1, an empty `**Usage:**` placeholder line right after the H1 intro paragraph (`**Usage:** _(unfilled — add a one-line policy describing how to deploy this book)_`), then per-chapter blocks (metadata line, optional empty prose, **Topics:** line, then composed-ref section headings with ranges). **No `- Use ...` bullets are emitted.**
   - **Split layout:** one short `index.md` (frontmatter, H1, empty `**Usage:**` placeholder, per-chapter blocks with metadata + Topics, no section listings, no Use bullets) plus one `index-ch<NN>.md` per chapter (lightweight frontmatter, chapter H2 + metadata, composed-ref section headings with ranges).
   - Suggest a default `cite` per chapter (e.g. `huemer-uk-ch02`).
9. Regenerate `/sources/catalog.yaml`.
10. Print the run summary (see below). If the user wants to add canonical `Use` marks for the new book, point them to `accept-canonical-chapters`.

### Refresh mode — `/sources/<book>/index.md` already exists

Used when a book already has an index and the user wants to pick up changes.

1. Load the existing `index.md`. Read `chapter-indexes` from frontmatter (`split` or `inline`; default to `inline` if missing).
2. Preserve all prose, including the book-level `**Usage:**` block, every `**Topics:**` line, and every `- Use <ref> for <topic>` bullet. The only thing that gets updated is the range marker `[<a>-<b>]` in section headings, and possibly the chapter metadata line (`file:` if a file was renamed). If the existing index has no `**Usage:**` block (older book scaffolded before the slot existed), insert an empty placeholder in the right spot — but never overwrite an existing one.
3. **Inline layout:**
   - For each MD chapter, re-run the detection algorithm (scaffold step 2) on the source to recover the convention (`prefixed` / `local` / `unnumbered`) — no stored signal.
   - **Match index entries to source headings by convention:**
     - `prefixed`: match by full ref string (index `5.2.1` ↔ source `## 5.2.1 ...`).
     - `local`: strip the chapter prefix from the index ref, match against source bare local ref (index `5.2` ↔ source `## 2 ...`).
     - `unnumbered`: match by **normalised heading name** (case-insensitive, whitespace-collapsed). The leading number in the index is cosmetic and re-derives from source order on every refresh — so reordering source sections updates the cosmetic numbers, while Topics, prose, and any attached metadata follow the section by name.
   - Replace the bracket range. For `unnumbered`, also rewrite the cosmetic ref prefix when source order has changed.
   - Append new sections present in source but missing from index, with empty prose, after the last existing section in the chapter. Never auto-add a `Use` bullet for a new section — `accept-canonical-chapters` does that.
   - Flag (warning) sections present in index but missing from source.
   - Never touch `**Topics:**`, `Use` bullets, chapter prose, section prose, summary, cite, frontmatter `tags`.
   - For non-MD chapters, leave page/line ranges untouched. Update only `file:` if renamed.
4. **Split layout:**
   - For each chapter listed in the short index, expect an `index-ch<NN>.md` file. Warn if missing; do not auto-create (user may have deleted intentionally — explicit migrate-to-inline path resolves this).
   - For each `index-ch<NN>.md`:
     - Re-detect the convention from source and re-derive ranges + match entries (same per-style logic as inline).
     - Append new sections (no `Use` bullet auto-add).
     - Sync the chapter metadata line (`file:` only) with the short index if needed.
   - Short index: never touch chapter prose, `**Topics:**`, or `Use` bullets.
5. Course argument(s) on refresh — accepted but a no-op for Topics by default. The user must explicitly request "regenerate topics for ch <N> against <course>" for that single chapter's `**Topics:**` line to be overwritten.
6. Regenerate `/sources/catalog.yaml`.

### Migration mode

On user request: "split the understanding-knowledge index" / "merge the truth-horwich index back into one file".

**Inline → split:**

1. Read existing `index.md`.
2. For each `## Chapter <N> ·` block, extract the section listing + per-section prose into a fresh `index-ch<NN>.md` (with lightweight frontmatter).
3. If the chapter has no existing `**Topics:**` line, generate one by reading the chapter source (same procedure as scaffold). Existing `**Topics:**` lines and existing `- Use ...` bullets are preserved verbatim. Never auto-generate Use bullets here.
4. Preserve chapter prose verbatim in the short index.
5. Strip section headings (the section level — typically H3/H4/H5) and per-section prose from the short index.
6. Update frontmatter: `chapter-indexes: split`.
7. Regenerate catalog.

**Split → inline:**

1. Read short `index.md` and all `index-ch<NN>.md` files.
2. Splice each per-chapter file's section listings back under its chapter block in the short index.
3. Update frontmatter: `chapter-indexes: inline`.
4. Delete the per-chapter files (only after the merged file is written and verified).
5. Regenerate catalog.

Migration preserves all prose, all topics, all bullets. Only structural arrangement changes.

## Parsing trick for MD index round-trip

When refreshing, parse the index files line by line and treat as a sequence of segments:
- Frontmatter (between `---` markers): preserve everything; update `generated` to today.
- Body: walk lines tracking the current chapter (last `^## ` heading) and section (last heading at the index's section level — typically H3, but the section level is whatever the indexer emitted at scaffold and stays consistent within a book). For each section heading, regex-replace the `\[(pp\. )?[0-9]+-[0-9]+\]` marker with the new range. Everything between section headings is prose to preserve verbatim.

For `unnumbered` books, the cosmetic leading number in the index ref may also need rewriting if source order changed; the heading name is the match key.

In code:
```bash
# Pseudocode for the range update inside one heading line
sed -E 's/\[(pp\. )?[0-9]+-[0-9]+\]/[\1<NEW_START>-<NEW_END>]/'
```

For the cite/file line under a chapter heading: it's identifiable by being a single-line inline-code paragraph starting with `` ` `` containing `cite:` and `file:`. Update only `file:` if needed; leave `cite:` and `format:` alone.

## Catalog regeneration

After per-book work, regenerate `/sources/catalog.yaml`:

- Walk `/sources/*/index.md`. (Per-chapter files are not separately catalogued — one entry per book.)
- For each, parse the frontmatter and copy: `slug`, `title`, `author`, `kind`, `tags`.
- Pull a `summary:` field if a `**Summary.**` paragraph exists at the top of the body (book-level).
- Add `index: sources/<slug>/index.md`.
- Sort by `slug` for stable diffs.

`catalog.yaml` stays YAML — purely generated.

## Validation

Run after every invocation:

- Every section heading (in inline `index.md` or any `index-ch<NN>.md`) has a parseable range marker.
- `cite` keys are unique across the whole library (only flag when both filled in; empty placeholders are OK).
- Every `file:` referenced exists on disk under `/sources/<book>/`.
- For split-layout books: every chapter listed in the short index has a corresponding `index-ch<NN>.md`. Warn if missing or orphaned.
- For each `/courses/*/index.md`:
  - Every book listed under frontmatter `books:` exists in `catalog.yaml`.
  - Every entry under any module's `**Sources:**` list resolves through the fuzzy resolver (warn for unresolved).

## Run summary format

Print at the end of every run. Keep it short and scannable:

```
Indexed: 2 books, 12 chapters, 47 sections.
- understanding-knowledge: 19 chapters, 161 sections (refreshed; 2 new sections in ch. 11) [split]
- paradox-lost: 11 chapters, 94 sections (scaffolded) [inline]
Catalog: 2 books listed.
Validation: OK.
Warnings: ch. 14 in understanding-knowledge lists "14.5" with no matching heading in source.
```

## What this skill does NOT do

- Never edits source files (`.md`, `.pdf`, etc.).
- Never deletes or modifies user prose in any index file.
- Never overwrites the book-level `**Usage:**` block on refresh — only inserts an empty placeholder if missing entirely.
- Never re-runs Topics extraction on refresh (only on scaffold or explicit per-chapter regenerate request).
- **Never emits or modifies `- Use <ref> for <topic>` bullets** — those are the exclusive output of `accept-canonical-chapters`. The indexer preserves any it finds, but creating, removing, or rewriting them is out of scope.
- Never writes prose annotations under section headings.
- Never modifies `/courses/*/index.md` (so it never touches a course's `**Books usage:**` block, `**Sources:**` lists, or `books:` field — even when invoked with course arguments). Course arguments are read-only inputs to Topics extraction.
- Never modifies `/positions/*/`.
- Never writes essays or modifies prompts.

## Implementation notes

- For MD heading extraction, pull all heading lines first with `grep -nE '^#{1,6}[[:space:]]+'`, then apply the per-style detection logic in scaffold step 2 to decide which level is the section level and which style is in use. Don't pre-filter to numbered headings — that excludes `unnumbered` books.
- For range update on refresh, prefer line-aware editing over a regex sweep of the whole file: walk lines, identify section headings (at the index's section level), update only those.
- For `unnumbered`-style books on refresh, always re-derive the cosmetic local number from current source order before computing matches; the heading name is the stable match key.
- When parsing YAML frontmatter, accept loose formatting (lists may be inline `[a, b]` or block-style).
- Keep diffs small: don't reflow prose, don't reorder sections that are already present, don't normalize whitespace beyond what's necessary.
- For split layout, when reading a per-chapter file in isolation (e.g. forward-mode resolution), the resolver computes the path as `sources/<slug>/index-ch<NN>.md` from the chapter number — no lookup needed.
