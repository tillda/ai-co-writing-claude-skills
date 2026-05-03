---
name: source-indexer
description: Scaffold or refresh per-book /sources/<book>/index.md files (and the top-level /sources/catalog.yaml). Scaffold mode generates a fresh MD index from a source's headings; refresh mode preserves all human-written prose and only updates derived line/page ranges. Use when adding new sources or after editing source files.
---

# Source Indexer

Builds and maintains the per-book index files that make subchapter-precise source resolution possible. The index is **markdown**: human-readable, prose-friendly, with structured data inline in headings and frontmatter.

Two layouts exist, both valid:

- **Inline layout** (default for small books) — single `index.md` carries everything: book metadata, chapter blocks, section headings with line ranges, prose.
- **Split layout** (default for ≥500-line indexes or ≥10 chapters with subsections) — short `index.md` carries book metadata + per-chapter topic annotations only; line ranges and structural detail live in per-chapter `index-ch<NN>.md` files.

The resolver always opens `index.md` first; whether it then opens a per-chapter file depends on layout. Reverse-mode (topic-only matching) reads only the short `index.md`. Forward-mode and post-match resolution read the matching per-chapter file when split.

## When to invoke

- "reindex sources"
- "scaffold an index for the new book I just added"
- "refresh Understanding Knowledge"
- After dropping a new chapter into `/sources/<book>/`
- After editing a source file (re-OCR, fixed headings, etc.)
- "split this index" — to migrate an inline-layout book to split layout

The skill never edits source files. It only writes:
- `/sources/<book>/index.md` (the per-book index)
- `/sources/<book>/index-ch<NN>.md` (per-chapter files, split layout only)
- `/sources/catalog.yaml` (the small generated catalog)

## Layout decision

At scaffold time, choose the layout based on the source.

**Use split layout** when at least one of:
- The would-be inline `index.md` would exceed ~500 lines.
- The book has ≥10 numbered chapters with subsections.
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

- Use 2.4 for Gettier's refutation
- Use 2.5.2 for reliabilism
- Use 2.5.3 for proper function
- Use 2.5.4 for sensitivity / tracking
- Use 2.5.5 for safety
- Use 2.5.6 for relevant alternatives
- Use 2.5.7 for defeasibility
- Use 2.6.2 for the Lockean theory of concepts
- Use 2.6.3 for the Wittgensteinian view of concepts

## Chapter 3 · ...
```

The short index has **no line ranges**. Line ranges live in per-chapter files. The short index is the always-read entry point — fast to scan, cheap to keep in context.

### Conventions (split layout, short index)

- **Frontmatter** carries book-level structured data plus `chapter-indexes: split`.
- **Chapter headings** are H2: `## Chapter <N> · <Name>`.
- **Chapter metadata line** is a single backtick-fenced inline-code line directly under the chapter heading: `` `cite: <key> · file: <relative-path> · format: md|pdf|html|txt` ``. Same fields as inline layout.
- **Chapter prose** (optional) — any free paragraphs between metadata line and `**Topics:**` or first bullet. Author-curated guidance: scope, summary, when to invoke.
- **`**Topics:**` line** (auto-generated, user-editable) — comma-separated keyword list for at-a-glance reverse-mode matching. Lowercased except for proper nouns.
- **Bullet list** of `- Use <ref> for <topic-phrase>` annotations. Each bullet binds a section ref (e.g. `2.5.2`) to a topic phrase. The resolver matches the topic phrase against the prompt; on a match, parses the ref and looks it up in the matching `index-ch<NN>.md`.
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
- **Section headings** are H3 / H4 / H5 with line ranges as before: `### <ref> <Name> [<a>-<b>]` (MD/TXT/HTML), `### <ref> <Name> [pp. <a>-<b>]` (PDF).
- **Section prose** lives here, not in the short index.
- The per-chapter file is structurally a single chapter slice of the old monolithic format.

### Three roles in a section heading

A section heading has three slots, each with a different job:

| Slot | Role | Stability | Owner |
|------|------|-----------|-------|
| `<ref>` (e.g. `2.3.4`) | **Identifier** — the match key | Stable across re-OCR | The book |
| `<Name>` | **Documentation** — for the human reader | Mostly stable; user may tweak | The user |
| `[<a>-<b>]` | **Derived range** — what to read | Volatile; recomputed every refresh | The indexer |

**The identifier is `<ref>`, not the bracket.** The indexer matches index entries to source headings by `<ref>` (`2.3.4`), then writes the freshly-derived range into `[<a>-<b>]`. The bracket is the indexer's only writable target on a heading line; everything else is preserved verbatim.

Use plain ASCII hyphen (`-`) inside the bracket, not en-dash, to keep grep/sed simple.

## Format — `index.md` (inline layout)

Identical to the split-layout short index *except*:
- Frontmatter carries `chapter-indexes: inline`.
- Each chapter block, after the `**Topics:**` line and bullets, also lists section headings inline (H3/H4/H5) with `[<a>-<b>]` ranges, followed by any per-section prose.
- No `index-ch<NN>.md` files exist for the book.

This is the legacy format with the topics/bullets addition. Suitable for short books.

## Books without numbered sections

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

## Auto-topic extraction (scaffold mode)

For each chapter, walk all H3/H4/H5 source headings and detect candidate topics. The output is the chapter's `**Topics:**` line and bullet list in the short / inline index.

### Detection heuristics

A heading earns a bullet if any of these match its text:

1. **`-ism` / `-ist` words** (case-insensitive, ≥4 chars). Examples: reliabilism, foundationalism, coherentism, infinitism, scepticism, contextualism, expressivism, nihilism, fideism, disjunctivism, externalism, internalism, Bayesianism, Kantianism, empiricism, rationalism, positivism, dialetheism, deflationism, minimalism, supervaluationism, epistemicism, libertarianism, compatibilism, naturalism, intuitionism, evidentialism, dualism, monism, materialism, idealism, realism, anti-realism, behaviourism, functionalism, intentionalism, particularism, generalism.
2. **Eponymous adjectives** — capitalized word ending in `-ian`, `-ean`, `-onian`. Examples: Wittgensteinian, Lockean, Sellarsian, Bayesian, Kantian, Goodmanian, Cartesian, Aristotelian, Humean, Russellian, Fregean, Quinean, Tarskian, Davidsonian, Gricean, Berkeleyan, Putnamian, Kripkean, Moorean.
3. **Possessive philosopher names** — `\b[A-Z]\w+'s\b` (e.g. `Hume's`, `Quine's`, `Bayes'`, `Goodman's`, `Occam's`, `Anselm's`, `Donnellan's`, `Frege's`, `Russell's`, `Pascal's`).
4. **Named arguments / paradoxes / theories / theorems / principles / theses / hypotheses / views / problems / dilemmas / wagers / razors** — heading contains one of those nouns preceded by capitalized words. Examples: Brain-in-a-Vat Argument, Liar Paradox, Sorites, Open Question Argument, Sellarsian Dilemma, Newcomb's Problem, Sleeping Beauty, Doomsday Argument, Ontological Argument, Cosmological Argument, Argument from Design, Fine Tuning Argument, Argument from Disagreement, Categorical Imperative, Doctrine of Double Effect, Equivalence Schema, T-schema, KK Thesis, Closure Principle, Principle of Indifference, Principle of Sufficient Reason, Principle of Charity, Inference to the Best Explanation, Twin Earth, Trolley Problem.
5. **Standalone capitalized noun-phrase technical terms** — `Reliabilism`, `Falsifiability`, `Coherentism`, `Disjunctivism`, `Internalism`, `Externalism`, `Intuitionism`, etc. (overlaps with rule 1; either match suffices.)

### Stop list (skip these headings even if they contain a candidate)

`Introduction`, `Conclusion`, `Conclusions`, `Background`, `Overview`, `Summary`, `Notes`, `Questions`, `Further Reading`, `Reply`, `Rejoinder`, `Comment`, `Comments`, `Objections` (alone — `Objection 1` etc. are skipped too), `Examples`, `A Solution`, `Solutions`, `The Paradox`, `The Argument`, `The Theory`, `The Issue`, generic `Section <N>`, generic `Subsection <N>`. Match case-insensitively. If the heading is *only* a stop-list phrase, skip; if it contains a real topic plus a stop word, keep.

### Bullet generation

For each section heading that earned a topic match:

- Emit `- Use <ref> for <topic-phrase>`.
- `<topic-phrase>` is the heading name with normalisation:
  - Strip the leading `<ref>` and any leading numeric prefix.
  - Lowercase the first character if it's an article (`The`/`A`/`An`) followed by another word.
  - Otherwise preserve original casing (proper nouns survive).
  - Trim trailing punctuation.

Example transformations:

| Source heading | Bullet |
|---|---|
| `### 2.5.2 Reliabilism` | `- Use 2.5.2 for reliabilism` |
| `### 8.2.2 The Brain-in-a-Vat Argument` | `- Use 8.2.2 for the Brain-in-a-Vat Argument` |
| `### 10.4 Quine's Radical Empiricism` | `- Use 10.4 for Quine's radical empiricism` |
| `### 12.7 Inference to the Best Explanation` | `- Use 12.7 for inference to the best explanation` |
| `### 14.3.1 Occam's Razor and the Burden of Proof` | `- Use 14.3.1 for Occam's razor` |

### Topics line

Aggregate the detected keyword phrases per chapter into the `**Topics:**` line:

- Pull the matched lexical item (`reliabilism`, `Hume`, `Brain-in-a-Vat`, `Occam's razor`) from each bullet.
- Lowercase except for proper nouns and acronyms.
- Dedup, comma-separated, in source order.
- Skip if the chapter has no detected topics (no Topics line, no bullets).

The Topics line is a denormalised quick-scan companion to the bullets. Editing the bullets does not auto-update Topics — the user owns both after scaffold.

### Auto-extraction is scaffold-only

Refresh mode never re-runs auto-extraction. Once written, bullets and Topics are user-owned. To regenerate them for a chapter, the user explicitly asks ("regenerate auto-topics for ch 14") and the indexer overwrites that chapter's `**Topics:**` line and bullet list (only).

When refresh detects a new section in the source not present in any per-chapter file, it appends the new section heading to the chapter file — but it does NOT auto-add a bullet. The user adds bullets manually if wanted.

## Two modes (plus migration)

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
5. Decide layout (split vs inline) using the threshold rule.
6. Run auto-topic extraction per chapter.
7. Write files:
   - **Inline layout:** one `index.md` with frontmatter, the H1, an empty `**Usage:**` placeholder line right after the H1 intro paragraph (`**Usage:** _(unfilled — add a one-line policy describing how to deploy this book)_`), then per-chapter blocks (metadata line, optional empty prose, **Topics:** line, bullets, then section H3/H4/H5 with ranges).
   - **Split layout:** one short `index.md` (frontmatter, H1, empty `**Usage:**` placeholder, per-chapter blocks with metadata + Topics + bullets, no section listings) plus one `index-ch<NN>.md` per chapter (lightweight frontmatter, chapter H2 + metadata, section H3/H4/H5 with ranges).
   - Suggest a default `cite` per chapter (e.g. `huemer-uk-ch02`).
8. Regenerate `/sources/catalog.yaml`.

### Refresh mode — `/sources/<book>/index.md` already exists

Used when a book already has an index and the user wants to pick up changes.

1. Load the existing `index.md`. Read `chapter-indexes` from frontmatter (`split` or `inline`; default to `inline` if missing for back-compat).
2. Preserve all prose, including the book-level `**Usage:**` block. The only thing that gets updated is the range marker `[<a>-<b>]` in section headings, and possibly the chapter metadata line (`file:` if a file was renamed). If the existing index has no `**Usage:**` block (older book scaffolded before the slot existed), insert an empty placeholder in the right spot — but never overwrite an existing one.
3. **Inline layout:**
   - For each MD chapter, re-run the heading-extraction grep.
   - Match by section ref; replace the bracket range.
   - Append new sections present in source but missing from index, with empty prose, after the last existing section in the chapter.
   - Flag (warning) sections present in index but missing from source.
   - Never touch `**Topics:**`, bullets, chapter prose, section prose, summary, cite, frontmatter `tags`.
   - For non-MD chapters, leave page/line ranges untouched. Update only `file:` if renamed.
4. **Split layout:**
   - For each chapter listed in the short index, expect an `index-ch<NN>.md` file. Warn if missing; do not auto-create (user may have deleted intentionally — explicit migrate-to-inline path resolves this).
   - For each `index-ch<NN>.md`:
     - Re-derive ranges (same logic as inline).
     - Append new sections.
     - Sync the chapter metadata line (`file:` only) with the short index if needed.
   - Short index: never touch chapter prose, **Topics:**, or bullets.
5. Regenerate `/sources/catalog.yaml`.

### Migration mode

On user request: "split the understanding-knowledge index" / "merge the truth-horwich index back into one file".

**Inline → split:**

1. Read existing `index.md`.
2. For each `## Chapter <N> ·` block, extract the section listing + per-section prose into a fresh `index-ch<NN>.md` (with lightweight frontmatter).
3. Run auto-topic extraction on the chapter's section headings (the section headings are now in the new per-chapter file). Write `**Topics:**` line + bullets into the chapter block in the short index, **only if** the chapter does not already have them.
4. Preserve chapter prose verbatim in the short index.
5. Strip section headings (H3/H4/H5) and per-section prose from the short index.
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
- Body: walk lines tracking the current chapter (last `^## ` heading) and section (last `^#{3,6} ` heading). For each section heading, regex-replace the `\[(pp\. )?[0-9]+-[0-9]+\]` marker with the new range. Everything between section headings is prose to preserve verbatim.

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
- Never re-runs auto-topic extraction on refresh (only on scaffold or explicit request).
- Never modifies `/courses/*/index.md` (so it never touches a course's `**Books usage:**` block either).
- Never writes essays or modifies prompts.

## Implementation notes

- For MD heading extraction, use `grep -nE` (the regex above). It's a deterministic, fast, well-tested approach.
- For range update on refresh, prefer line-aware editing over a regex sweep of the whole file: walk lines, identify section headings, update only those.
- When parsing YAML frontmatter, accept loose formatting (lists may be inline `[a, b]` or block-style).
- Keep diffs small: don't reflow prose, don't reorder sections that are already present, don't normalize whitespace beyond what's necessary.
- For split layout, when reading a per-chapter file in isolation (e.g. forward-mode resolution), the resolver computes the path as `sources/<slug>/index-ch<NN>.md` from the chapter number — no lookup needed.
