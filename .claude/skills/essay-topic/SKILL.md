---
name: qfile-essays
description: Walk a question-bank file at /courses/<course>/Q-<N>-<topic>.md and write one philosophy essay per H1 section by running essay-philosophy once per section. Each H1 is the topic; the **Question(s)**: block lists variants (one essay per H1, merging variants); any other content under the H1 is passed forward as additional notes. Use when the user points at a Q-*.md file and asks to write essays for all the questions, batch-answer a question file, or "do the whole revision sheet".
---

# Batch Essays From a Q-File

Take a question-bank file at `/courses/<course-slug>/Q-<N>-<topic>.md`, parse each H1 section into one synthesised exam prompt, and run the **essay-philosophy** flow once per section.

This skill is an orchestrator. The actual essay writing — voice, sources, structure, save path — is delegated to essay-philosophy. Read `/.claude/skills/essay-philosophy/SKILL.md` once at the start of a batch so its rules are loaded, then apply them to each section.

## Input format

```
# <Topic A>

**Question(s)**:
    <variant 1>
    <variant 2>
    <variant 3>

<optional free-text notes / instructions for this topic>

# <Topic B>

**Question(s)**:
    <variant 1>

# <Topic C>
...
```

- File path: `/courses/<course-slug>/Q-<N>-<topic>.md`. The parent directory is the course slug; the leading `Q-<N>-` of the filename is the module number.
- Each `# <heading>` starts a new section. Sections end at the next `# ` or EOF.
- `**Question(s)**:` is followed by indented variant lines (one per line). Strip leading whitespace; drop blank lines.
- Anything else under an H1 (besides the Question(s) block) is **additional notes** — direction, scope, focus, what to address. Pass it forward to essay-philosophy as the `# Notes for the writer` body.

## Variant handling

One H1 → exactly one essay, regardless of how many variants are listed.

- **Paraphrase variants** (same question reworded): pick the most explicit/longest phrasing as the canonical question. Write one essay that addresses it. The other variants are absorbed silently — they don't change the structure.
- **Materially different variants** (e.g. one asks "what is X?", another asks "is X right?", another asks about a specific sub-claim): write one essay that **covers all the angles raised across variants**, typically by giving each distinct angle its own paragraph or sub-section in the body. Flag this explicitly in `# Notes for the writer` so the essay writer knows to allocate paragraphs.
- **Never write multiple essays for the same H1.**

Use judgment to decide whether two variants are paraphrases or materially different — if they would produce overlapping body paragraphs, they're paraphrases; if they'd produce non-overlapping content, they're materially different.

## Process

1. **Resolve metadata.**
   - Parse the file path: `/courses/<course>/Q-<N>-<topic>.md` → `course = <course>`, `module = <N>`.
   - Read `/courses/<course>/index.md` once. Find the `## <N>. <Name>` heading. Capture `<Name>`.
   - If the path doesn't match the expected shape, or the module number isn't found in the course index, **stop and ask the user** — don't guess and don't fall back to `_unfiled/`.

2. **Load shared context once.**
   - Read `/.claude/skills/essay-philosophy/SKILL.md` (the rules to apply per section).
   - Read `/context/voice-dna.md` and `/context/icp.md`.
   - Read `/positions/<course>/index.md` if the directory exists.
   - Read `/sources/catalog.yaml` and the in-scope books' `index.md` files (per the course's `books:` frontmatter).
   - Cache these for the whole batch — do not re-read them per section.

3. **Parse the file into sections.**
   - Split on top-level `# ` (H1) headings. Each section yields `{ heading, variants[], notes }`.
   - `variants[]` = lines under `**Question(s)**:`, leading whitespace stripped, blank lines dropped.
   - `notes` = any other prose under the H1 that isn't part of the Question(s) block.
   - If a section has no Question(s) block, skip it and remember to mention it in the final summary.

4. **For each section, build a synthesised exam prompt** in essay-philosophy's expected shape:

   ```markdown
   ---
   slug: <slugify(heading)>
   course: <course>
   module: <N>
   ---

   # Question

   <canonical question — see rule below>

   # Notes for the writer

   <free-text notes from the section>
   <one-line variant-handling note if multiple distinct angles need their own paragraphs>
   ```

   **Canonical-question rule** — this string becomes the essay's H1 verbatim (essay-philosophy's H1 rule), so construct it deliberately. **Every qfile-essays H1 is prefixed with the Q-file H1 label, then ` — ` (space, em-dash U+2014, space), then the chosen variant text.** The Q-file H1 label gives the reader a short topical entry-point before the long exam-style question; without it the file opens straight into a paragraph-length sentence with no orientation.

   The shape is always: `<Q-file H1 text> — <chosen variant>`. The choice of variant depends on the section:

   - **Single variant**: use that variant. The H1 will be `# <Q-file H1 text> — <variant>`.
   - **Paraphrase variants** (same question reworded): use the longest / most explicit variant. The H1 will be `# <Q-file H1 text> — <longest variant>`.
   - **Materially different variants** (multiple distinct angles under one Q-file H1, i.e. a *grouped* section): use the **shortest** variant verbatim (measured by character count; on a tie, take the earliest in the list). The H1 will be `# <Q-file H1 text> — <shortest variant>`. Follow this with a bulleted list of the remaining distinct angles to cover in the question body (not the H1).

   Separator: always the em-dash ` — ` (with one space before and one after). Do not substitute a hyphen `-`, en-dash `–`, or colon `:`. If the Q-file label ends with terminal punctuation (`?`, `.`), keep it as-is — the em-dash still follows: e.g. `# Why does it matter? — <full question>`.

   Other rules:
   - `slugify(heading)` matches essay-philosophy's question-slug rule: lowercase, non-alphanumerics → `-`, collapse repeated dashes, trim.
   - Omit `# Notes for the writer` entirely if the section had no notes and only one variant (or only paraphrase variants).

5. **Run essay-philosophy on the synthesised prompt.** Apply its full flow per section: resolve sources for that topic, plan argument, write the essay, run its quality checklist, save to disk at the canonical path:

   `/courses/<course>/essays/<N>-<name-slug>/<heading-slug>.md`

   Where `<name-slug>` is the slugified module name from step 1.

6. **Report.** After each section, emit one short line in chat:
   - `✓ <heading> → <path>` on success
   - `– <heading> (skipped: <reason>)` if skipped
   - `✗ <heading> (failed: <reason>)` if a section couldn't be written (don't abort the batch — record and continue)

   **Do not print the full essay text in chat for a batch run.** The essays go to disk; the user opens them. End the reply with a summary line:

   `Wrote N essays to /courses/<course>/essays/<N>-<name-slug>/` (plus a count of skipped/failed if any).

## Doing the batch efficiently

- Load shared context (voice, examiner, course index, positions index, source catalog, in-scope book indexes) **once at the top**. Reuse for every section.
- Resolve sources per-section — different topics need different ranges from the canonical book — but rely on the cached book-index reads.
- Write essays sequentially. Do not try to parallelise — each essay is ~1200 words, and they share enough loaded state that interleaving doesn't pay off.
- If the same source range appears across sections (e.g. multiple sections share a single chapter), read it once and reuse.

## Safety

- If the file has no H1 sections at all, stop and tell the user the file looks empty.
- If a section's heading exists but has no `**Question(s)**:` block, skip it (don't invent a question) and report it in the summary.
- If the course directory or module number can't be resolved, abort the whole batch and tell the user — don't silently fall back to `_unfiled/`.
- If essay-philosophy would refuse a section's prompt (e.g. no `course:`), that's a bug in this skill's prompt construction — fix the synthesised prompt, don't paper over it.

## Quality checklist

Before reporting completion:

- [ ] One essay file written per H1 section that had a Question(s) block
- [ ] Each essay is at `/courses/<course>/essays/<moduleId>-<moduleName-slug>/<heading-slug>.md`
- [ ] Each essay individually passes the essay-philosophy quality checklist (voice, structure, length cap, no chapter/page refs, single-mention authors)
- [ ] Each essay's first line is a single `# <Q-file H1 text> — <variant>` H1 — Q-file label always prefixed, em-dash ` — ` separator (not hyphen, en-dash, or colon). Variant chosen per the rule: single → that variant; paraphrase → longest; materially different → shortest
- [ ] All variants under each H1 are folded into one essay; materially different angles each got a paragraph
- [ ] Free-text notes under each H1 were respected
- [ ] Final chat reply lists each saved file with a status mark and ends with a count summary
- [ ] No full essay prose printed to chat (disk only for batch mode)
