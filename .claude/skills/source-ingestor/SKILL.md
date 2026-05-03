---
name: source-ingestor
description: File a raw source from /sources/_inbox/ (PDF/HTML/TXT/MD) into /sources/<book>/, optionally converting to MD. Then invokes source-indexer to scaffold or refresh the book's index.md. Curated metadata (cite, summary, notes) is added later by editing index.md directly.
---

# Source Ingestor

Takes raw material the user dropped into `/sources/_inbox/` and files it into the bibliographic library at `/sources/<book>/`. The skill is deliberately minimal — it gathers only the identifying metadata needed to file the source, then hands off to `source-indexer` for everything else.

## When to invoke

- "ingest the PDF I just dropped in inbox"
- "add this chapter to the library"
- After dropping a file into `/sources/_inbox/`

## Inputs accepted

- `.md` — already in canonical-ish form; kept as MD.
- `.pdf` — kept as-is by default; conversion to MD is optional.
- `.html`, `.txt` — kept as-is by default; conversion to MD is optional.

## Process

1. **Identify the file**: list `/sources/_inbox/`. If the user named one specific file, work on that; otherwise process them one at a time.

2. **Read enough to identify the chapter**: Read the file (PDFs are supported by the Read tool; pass `pages` for long PDFs).

3. **Gather minimal metadata** via AskUserQuestion. Pre-fill from any obvious frontmatter or PDF metadata. Required:
   - Book title (e.g. "Understanding Knowledge")
   - Book slug (e.g. "understanding-knowledge")
   - Author (e.g. "Michael Huemer")
   - Chapter number (e.g. "2")
   - Chapter name (e.g. "Induction")

   Do NOT gather `cite`, `summary`, or `notes` here. Those are added later by editing the book's `index.md` directly — that's the curation step, separate from ingest.

4. **Decide on conversion** (only for non-MD inputs):
   - **Convert to MD** (recommended for chapters that will be cited often, since line-range precision is sharper than page-range): produce a `.md` file with the chapter body and minimal frontmatter (`book`, `number`, `name`). Make sure section headings in the body start with the section ref (e.g. `## 2.1 The Problem`, `### 2.3.4 Zebra and Mule`) so the indexer's grep can pick them up. Place at `/sources/<book-slug>/<NN>-<chapter-slug>.md`. Move the inbox original to `_inbox/_processed/`.
   - **Keep as-is**: move the file to `/sources/<book-slug>/<NN>-<chapter-slug>.<ext>`. The indexer will collect the TOC + page/line ranges at scaffold time and store them in the book's `index.md`.

   Default: keep-as-is for PDFs (conversion is overhead the user said they want only when worth it). Ask if not sure.

5. **Choose the chapter filename**: `<NN>-<slug>.<ext>` where `<NN>` is the zero-padded chapter number and `<slug>` is a kebab-case version of the chapter name. Example: `02-induction.md`, `14-scientific-knowledge.pdf`.

6. **Create the book directory if it doesn't exist**: `/sources/<book-slug>/`.

7. **Move/write the file** into the book directory.

8. **Invoke `source-indexer`** for the affected book. If the book is new, the indexer runs in scaffold mode and creates `/sources/<book-slug>/index.md`; otherwise refresh mode picks up the new chapter.

9. **Report**: name the new file, the book directory it landed in, and the indexer mode that ran. Remind the user of three optional next steps:
   - Hand-edit `index.md` to fill in `cite`, the book-level `**Usage:**` policy, chapter-level notes, and per-section notes (just open it and write prose under the headings).
   - Run `accept-canonical-chapters <book>` (optionally with a course slug) to propose authoritative `- Use <ref> for <topic>` marks via the approval loop.
   - Run `accept-canonical-positions <book> <course>` to propose new or strengthened user positions for that course.

## What this skill does NOT do

- Never writes `cite`, `summary`, or `notes` values — those are curated by the user in `index.md`.
- Never deletes inbox originals. Move them to `_inbox/_processed/` so the user can re-OCR or revert if needed.
- Never modifies existing source files in `/sources/<book>/`.
- Never touches `/courses/*/index.md`.

## Implementation notes

- For batch ingest of multiple inbox files, process one at a time — the metadata questions are per-chapter.
- If a book directory and filename collision occurs (e.g. user re-OCR'd ch. 2), ask the user whether to overwrite or rename before proceeding.
- After ingestion, curation is split across two skills: `accept-canonical-chapters` (authoritative `- Use ...` marks in the book index, optionally with course-MD updates) and `accept-canonical-positions` (the user's stated stances per course). Both are approval-loop based and never auto-apply.
