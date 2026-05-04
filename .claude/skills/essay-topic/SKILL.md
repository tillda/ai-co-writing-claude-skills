---
name: essay-topic
description: Write philosophy essays from a question-bank file at /courses/<course>/Q-<N>-<topic>.md — either one per H1 section in batch mode, or a single named H1 in single-section mode. Each H1 is the topic; the **Question(s):** block lists variants (one essay per H1, merging variants); any other content under the H1 is passed forward as additional notes. Use when the user points at a Q-*.md file and asks to write/answer all the questions ("do the whole revision sheet"), OR when the user asks to write/rewrite a specific essay identified by course + module name + H1 (e.g. "write the essay in Logic course module Truth '# Tarski's T-Schema...'").
---

# Essays From a Q-File

Take a question-bank file at `/courses/<course-slug>/Q-<N>-<topic>.md`, parse the targeted H1 section(s) into synthesised exam prompts, and run the **essay-philosophy** flow once per section.

This skill is an orchestrator. The actual essay writing — voice, sources, structure, save path — is delegated to essay-philosophy. Read `/.claude/skills/essay-philosophy/SKILL.md` once at the start so its rules are loaded, then apply them to each section.

## Modes

Two invocation modes share all the per-section work below; they differ only in (a) how the Q-file is identified, (b) how many sections are written, and (c) whether the essay text is printed to chat.

- **Batch mode** — user points at a Q-file directly (path or "do all the questions in `Q-2-Truth.md`"). Write **one essay per H1** that has a `**Question(s)**:` block. Disk-only output; chat gets a one-line status per section plus a summary.
- **Single-section mode** — user names a course + module + H1, e.g. *"write the essay in Logic course module Truth '# Tarski's T-Schema and the concept of truth'"* or *"rewrite … "*. Write **one essay** for the named H1. Disk **and** chat output, matching essay-philosophy's default. "Write" and "rewrite" trigger the same flow — the canonical path is overwritten either way.

If the request is ambiguous (e.g. a Q-file path with no H1 quoted, but only one H1 in the file), default to batch mode and proceed. If a course + module is named with no H1, ask which H1.

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

1. **Resolve the Q-file and target section(s).**

   **Batch mode** (Q-file path given directly):
   - Parse the file path: `/courses/<course>/Q-<N>-<topic>.md` → `course = <course>`, `module = <N>`.
   - Target sections = every H1 in the file with a `**Question(s)**:` block.

   **Single-section mode** (course + module name + H1 quoted):
   - Resolve the course slug: match the course name (e.g. "Logic") against directories under `/courses/` case-insensitively. One match → `course = <slug>`. Zero or multiple → stop and ask.
   - Resolve the module: read `/courses/<course>/index.md`, find the `## <N>. <Name>` heading whose `<Name>` matches the user-supplied module name (case-insensitive, allow trivial fuzziness — "Truth" matches "Truth" or "Truth and Falsity"). One match → `module = <N>`. Zero or multiple → stop and ask.
   - Locate the Q-file: glob `/courses/<course>/Q-<N>-*.md`. Exactly one file is expected.
   - Resolve the H1: parse all H1 headings in the Q-file. Match the user-supplied heading (with or without leading `#`, case-insensitive, fuzzy on whitespace and punctuation). Exactly one match required; otherwise stop and ask.
   - Target sections = the single matched H1.

   **Common to both modes:**
   - Read `/courses/<course>/index.md` once. Find the `## <N>. <Name>` heading. Capture `<Name>` for the output path.
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

   **Canonical-question rule** — this string becomes the essay's H1 verbatim (essay-philosophy's H1 rule), so construct it deliberately. **Every essay-topic H1 is prefixed with the Q-file H1 label, then ` — ` (space, em-dash U+2014, space), then the chosen variant text.** The Q-file H1 label gives the reader a short topical entry-point before the long exam-style question; without it the file opens straight into a paragraph-length sentence with no orientation.

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

6. **Report.**

   **Batch mode** — after each section, emit one short line in chat:
   - `✓ <heading> → <path>` on success
   - `– <heading> (skipped: <reason>)` if skipped
   - `✗ <heading> (failed: <reason>)` if a section couldn't be written (don't abort the batch — record and continue)

   **Do not print the full essay text in chat for a batch run.** The essays go to disk; the user opens them. End the reply with a summary line:

   `Wrote N essays to /courses/<course>/essays/<N>-<name-slug>/` (plus a count of skipped/failed if any).

   **Single-section mode** — fall through to essay-philosophy's default: write to disk, print the full essay to chat, end with `Saved to: <path>`. No batch-style status line, no summary count.

## Doing the batch efficiently

- Load shared context (voice, examiner, course index, positions index, source catalog, in-scope book indexes) **once at the top**. Reuse for every section.
- Resolve sources per-section — different topics need different ranges from the canonical book — but rely on the cached book-index reads.
- Write essays sequentially. Do not try to parallelise — each essay is ~1200 words, and they share enough loaded state that interleaving doesn't pay off.
- If the same source range appears across sections (e.g. multiple sections share a single chapter), read it once and reuse.

## Safety

- If the file has no H1 sections at all, stop and tell the user the file looks empty.
- If a section's heading exists but has no `**Question(s)**:` block, skip it (don't invent a question) — report in the summary (batch) or refuse with a one-line explanation (single-section).
- If the course directory or module number can't be resolved, abort and tell the user — don't silently fall back to `_unfiled/`.
- **Single-section mode resolution failures** (any of: course slug ambiguous, module name not found in course index, multiple Q-files matched the module, H1 not found in Q-file, multiple H1s fuzzy-matched) — stop and ask the user to disambiguate. Do not guess.
- If essay-philosophy would refuse a section's prompt (e.g. no `course:`), that's a bug in this skill's prompt construction — fix the synthesised prompt, don't paper over it.

## Quality checklist

Before reporting completion:

- [ ] One essay file written per targeted H1 section (every H1 with a Question(s) block in batch mode; the single named H1 in single-section mode)
- [ ] Each essay is at `/courses/<course>/essays/<moduleId>-<moduleName-slug>/<heading-slug>.md`
- [ ] Each essay individually passes the essay-philosophy quality checklist (voice, structure, length cap, no chapter/page refs, single-mention authors)
- [ ] Each essay's first line is a single `# <Q-file H1 text> — <variant>` H1 — Q-file label always prefixed, em-dash ` — ` separator (not hyphen, en-dash, or colon). Variant chosen per the rule: single → that variant; paraphrase → longest; materially different → shortest
- [ ] All variants under each H1 are folded into one essay; materially different angles each got a paragraph
- [ ] Free-text notes under each H1 were respected
- [ ] Chat output matches the mode: batch → status line per section + summary count, no essay prose; single-section → essay prose printed, ending with `Saved to: <path>`
