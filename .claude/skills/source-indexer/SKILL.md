---
name: source-indexer
description: Build /sources/<book>/index.md by walking each chapter .md file in the book directory and emitting a block with the chapter heading, subheadings with line ranges, and a `**Topics:**` keyword line. Optionally accepts one or more course slugs; when supplied, each course's /courses/<course>/index.md is passed as context to the per-chapter pass so course-relevant topics are not omitted from Topics. Concatenates the per-chapter blocks into one flat index.md per book. Use when a new book is added, when source files are edited, or to re-index against a course.
---

# Source Indexer

Builds one flat `/sources/<book>/index.md` per book. The index has one job: map topics from the courses to chapters of the book, and give explicit refs like `2.5.4` a line range to read.

## When to invoke

- New chapter files dropped into `/sources/<book>/`.
- "reindex sources" / "refresh `<book>`".
- Source files were edited (re-OCR, fixed headings).
- "index `<book>` against `<course>`" — passes the course index to each per-chapter pass.

## Inputs

- `<book-slug>` — required. Directory at `/sources/<book>/` with one `.md` file per chapter (PDF/HTML/TXT also acceptable; see "Non-MD sources" below).
- `<course-slug>` — optional, repeatable. When supplied, `/courses/<course>/index.md` is included as context in each per-chapter pass so the chapter's `**Topics:**` line reuses course-vocabulary terms wherever the chapter genuinely discusses them.

## Procedure

For each chapter file in `/sources/<book>/` (sorted by filename, excluding `index.md`), do **one pass**:

1. Read the chapter file.
2. If course slugs were supplied, also read each `/courses/<course>/index.md`.
3. Emit a chapter block:

   ```markdown
   ## Chapter <N> · <Name>
   *Source: <chapter-filename>*

   ### <ref> <Subheading> [<a>-<b>]
   ### <ref> <Subheading> [<a>-<b>]

   **Topics:** <comma-separated keywords>
   ```

   - **Chapter number and name** — from the H1 in the source (e.g. `# 5 Truth` → `Chapter 5 · Truth`); fall back to leading digits in the filename if no H1.
   - **Subheadings** — every H2 and H3 in the source. Compose the ref as `<chapter>.<local>`: if the source heading has a number, use it; otherwise number sections in source order. Recurse for sub-subheadings (`<chapter>.<local>.<sub>`).
   - **Line range `[<a>-<b>]`** — the heading's own line through the line before the next equal-or-higher-level heading (or EOF for the last one). Use `[pp. <a>-<b>]` for PDF.
   - **Topics line** — the philosophical concepts, theories, named figures, paradoxes, and arguments *actually discussed* in the chapter. Aim for 5–15 items, comma-separated, lowercase except for proper nouns and acronyms. When a course is supplied, prefer course terminology where it overlaps with the chapter's content; never add topics the chapter does not cover.

Concatenate every chapter block — separated by a blank line — into `/sources/<book>/index.md`, prefixed with frontmatter and the book H1:

```markdown
---
slug: <book-slug>
title: <Book Title>
author: <Author>
generated: <YYYY-MM-DD>
---

# <Book Title>
```

`title` and `author` come from any pre-existing `index.md` frontmatter, the source files, or the user. If unknown, ask.

## Non-MD sources

For PDF/HTML/TXT chapters without parseable headings, ask the user for the chapter's section TOC and explicit page or line ranges, then format identically (`[pp. <a>-<b>]` for PDF).

## Refresh

Refresh is the same procedure — every block is regenerated from the current source. Topics, subheadings, refs, and ranges all re-derive. **Nothing in the old `index.md` is preserved.** If the user previously ran `accept-canonical-chapters` to add `- Use <ref> for <topic>` bullets, those will be wiped on refresh; re-run `accept-canonical-chapters` afterward to re-add them.

## What this skill does NOT do

- Never edits source files in `/sources/<book>/`.
- Never edits `/courses/*/` files.
- Never writes `- Use <ref> for <topic>` bullets — that is `accept-canonical-chapters`.
- Never writes prose annotations, chapter narrative, book intros, or `**Usage:**` blocks.
- Never produces split-layout / per-chapter `index-ch<NN>.md` files.
- Never modifies `/sources/catalog.yaml` (no longer maintained by this skill).
