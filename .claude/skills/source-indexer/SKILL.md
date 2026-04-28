---
name: source-indexer
description: Scaffold or refresh per-book /sources/<book>/index.yaml files (and the top-level /sources/catalog.yaml). Scaffold mode generates a fresh index from a source's TOC/headings; refresh mode preserves all human-edited fields and only updates derived line/page ranges. Use when adding new sources or after editing source files.
---

# Source Indexer

Builds and maintains the per-book index files that make subchapter-precise source resolution possible.

## When to invoke

- "reindex sources"
- "scaffold an index for the new book I just added"
- "refresh Understanding Knowledge"
- After dropping a new chapter into `/sources/<book>/`
- After editing a source file (re-OCR, fixed headings, etc.)

The skill never edits source files. It only writes `/sources/<book>/index.yaml` and `/sources/catalog.yaml`.

## Two modes

The skill picks the mode automatically per book.

### Scaffold mode — `/sources/<book>/index.yaml` does not exist

Used when a book is new to the library.

1. List all chapter files in `/sources/<book>/` (excluding `index.yaml` itself).
2. For each MD file:
   - Read optional frontmatter. Useful fields if present: `book`, `number`, `name`, `toc:`.
   - Walk the body looking for headings whose text starts with a section number (e.g. `## 2.1 The Problem`, `### 2.3.4 The Zebra and the Mule`).
   - Build a `toc:` from headings (or from frontmatter's `toc:` block if it's complete).
   - Compute line ranges: each section runs from its heading line through the line before the next equal-or-higher-level heading (or EOF).
3. For each non-MD file (PDF/HTML/TXT):
   - For PDFs, attempt to extract bookmarks using the Read tool.
   - Otherwise ask the user (via AskUserQuestion) for the chapter's TOC and explicit page/line ranges.
4. Write `/sources/<book>/index.yaml`. Required keys:
   - Book-level: `version`, `generated`, `slug`, `title`, `author`, `kind`, `tags`, `chapters`.
   - Per chapter: `number`, `name`, `cite` (suggested default like `<author>-<book-initials>-ch<NN>`), `summary` (empty placeholder), `format`, `file`, `notes` (empty placeholder), `toc`.
   - Per `toc` entry: `ref`, `name`, `lines: [a, b]` or `pages: [a, b]`, optional `note` (empty placeholder), optional `children`.
5. Append a comment in the header noting that placeholder fields (`summary`, `notes`, per-entry `note`) are for the user to fill in.
6. Regenerate `/sources/catalog.yaml` (see "Catalog regeneration" below).

### Refresh mode — `/sources/<book>/index.yaml` already exists

Used when a book already has an index and the user wants to pick up changes.

1. Load the existing `index.yaml` into memory. Preserve every field unless explicitly listed below as derived.
2. **Derived fields, regenerated each refresh:**
   - For MD chapters: `lines: [a, b]` on every `toc` entry — re-derive from current headings. Exception: if the entry has an explicit pre-existing `lines` value AND the user has marked the entry as overridden (any human edit besides line numbers indicates ownership), preserve the explicit range.
   - `file` paths if files were renamed (best-effort match by `number` or filename pattern).
3. **Preserved fields, never touched:** `cite`, `summary`, `notes`, `note`, `tags`, any other key the user added. Page ranges on PDF/HTML/TXT entries are also preserved (not re-derivable).
4. **New TOC entries:** if the source body now has section headings the index doesn't list, add new `toc` entries with empty `note:`. Place them in source order.
5. **Missing TOC entries:** if the index lists a section ref the source no longer has a heading for, do NOT delete. Flag with a one-line warning in the run summary; the user resolves explicitly.
6. Regenerate `/sources/catalog.yaml`.

## Catalog regeneration

After per-book work, regenerate `/sources/catalog.yaml`:

- Walk `/sources/*/index.yaml`.
- For each, copy the book-level fields: `slug`, `title`, `author`, `kind`, `tags`, `summary`.
- Add `index: sources/<slug>/index.yaml`.
- Sort by `slug` for stable diffs.

## Validation

Run after every invocation:

- Every `toc` entry has a resolvable range (`lines` for MD/TXT/HTML, `pages` for PDF).
- `cite` keys are unique across the whole library (only flag when both filled in; empty placeholders are OK).
- Every `file` path referenced exists on disk.
- For each `/sources/courses/*.yaml`:
   - Every book listed under `books:` exists in `catalog.yaml`.
   - Every free-text entry under any module's `sources:` resolves through the fuzzy resolver (if not, print a warning naming the module and the unresolved string).

## Run summary format

Print at the end of every run. Keep it short and scannable:

```
Indexed: 2 books, 12 chapters, 47 sections.
- understanding-knowledge: 8 chapters, 31 sections (refreshed; 2 new sections in ch. 11)
- paradox-lost: 4 chapters, 16 sections (scaffolded)
Catalog: 2 books listed.
Validation: OK.
Warnings: ch. 14 lists section "14.5" with no matching heading in the source.
```

## What this skill does NOT do

- Never edits source files (`.md`, `.pdf`, etc.).
- Never deletes user-added fields from `index.yaml`.
- Never modifies `/sources/courses/*.yaml`.
- Never writes essays or modifies prompts.

## Implementation notes

- Implement directly with Read and Write tools — no external script.
- Read each source MD with line numbers (default Read output) so heading line numbers are exact.
- For PDFs without bookmarks, prefer asking the user once at scaffold time over guessing page ranges.
- When parsing YAML, preserve key order where reasonable so diffs stay readable.
