---
name: essay-topic
description: Write philosophy essays from question-bank files at /courses/<course>/Q-<N>-<topic>.md in three modes — (a) batch mode: one essay per H1 in a single Q-file; (b) multi-module batch: batch mode looped across a list of modules given as numbers or names; (c) single-section mode: one essay for a named H1. Each H1 is the essay's topic and becomes the essay's H1 verbatim; the **Question(s):** block lists *specifics* — possible exam-question formulations of that topic, all of which the essay must explain. One essay per H1 covers every specific. Other content under the H1 becomes additional notes. Use when the user points at a Q-*.md file ("do the whole revision sheet"), names a list of modules ("write essays for topics: 1, 2, 3" or "topics: Essentialism, Truth"), or names a specific course + module + H1 ("write the essay in Logic course module Truth '# Tarski's T-Schema...'").
---

# Essays From a Q-File

Take a question-bank file at `/courses/<course-slug>/Q-<N>-<topic>.md`, parse the targeted H1 section(s) into synthesised exam prompts, and run the **essay-philosophy** flow once per section.

This skill is an orchestrator. The actual essay writing — voice, sources, structure, save path — is delegated to essay-philosophy. Read `/.claude/skills/essay-philosophy/SKILL.md` once at the start so its rules are loaded, then apply them to each section.

## Modes

Three invocation modes share all the per-section work below; they differ only in (a) how the Q-file(s) are identified, (b) how many sections are written, and (c) whether the essay text is printed to chat.

- **Batch mode** — user points at a Q-file directly (path or "do all the questions in `Q-2-Truth.md`"). Write **one essay per H1** that has a `**Question(s)**:` block. Disk-only output; chat gets a one-line status per section plus a summary.
- **Multi-module batch mode** — user names a course + a list of module tokens (digits, names, or a mix), e.g. *"write essays for topics: 1, 2, 3 in Logic"* or *"do topics Essentialism, Truth in Logic"* or *"topics: 1, Truth, 3"*. Resolve each token to a module number, then run **batch mode** on each module's Q-file in turn. Disk-only output; chat gets per-section status lines grouped by module plus an aggregated summary.
- **Single-section mode** — user names a course + module + H1, e.g. *"write the essay in Logic course module Truth '# Tarski's T-Schema and the concept of truth'"* or *"rewrite … "*. Write **one essay** for the named H1. Disk **and** chat output, matching essay-philosophy's default. "Write" and "rewrite" trigger the same flow — the canonical path is overwritten either way.

If the request is ambiguous (e.g. a Q-file path with no H1 quoted, but only one H1 in the file), default to batch mode and proceed. If a course + module is named with no H1, ask which H1. If a list of module tokens is given without a course, ask which course.

## Input format

```
# <Topic A>

**Question(s)**:
    <specific 1 — one way the exam might phrase the topic>
    <specific 2 — another phrasing>
    <specific 3 — yet another phrasing>

<optional free-text notes / instructions for this topic>

# <Topic B>

**Question(s)**:
    <specific 1>

# <Topic C>
...
```

- File path: `/courses/<course-slug>/Q-<N>-<topic>.md`. The parent directory is the course slug; the leading `Q-<N>-` of the filename is the module number.
- Each `# <heading>` starts a new section. **The H1 is the essay's topic** — what the essay is about (e.g. "Nozick's entitlement theory of justice"). It becomes the essay file's H1 verbatim. Sections end at the next `# ` or EOF.
- `**Question(s)**:` is followed by indented lines, one per line. Each line is a **specific** — a way the topic might be formulated as an exam question. Strip leading whitespace; drop blank lines. The essay is written about the H1 topic and **must explain anything raised across the specifics**, since any of them could be the actual exam wording. A topic like "Nozick's entitlement theory of justice" can take many forms ("What does Nozick mean by 'liberty upsets patterns'?", "Is his argument persuasive?", "Explain his conception of a *just* situation"); the essay needs to cover all of them.
- Anything else under an H1 (besides the Question(s) block) is **additional notes** — direction, scope, focus, what to address. Pass it forward to essay-philosophy as the `# Notes for the writer` body.

## Specifics handling

One H1 → exactly one essay, regardless of how many specifics are listed under **Question(s)**. The essay is about the H1 topic; each specific is a way the exam might phrase a question on that topic, and **the essay must explain anything raised across the specifics**.

- **Paraphrase specifics** (same probe reworded): one comprehensive treatment of the topic addresses them all. No special structuring needed.
- **Materially different specifics** (e.g. one asks "what does X mean?", another asks "is X right?", another asks about a specific sub-claim of X): allocate distinct paragraphs or sub-sections in the body so every specific is explained — none silently dropped. Flag this explicitly in `# Notes for the writer` so the essay writer knows to allocate paragraphs.
- **Never write multiple essays for the same H1.**

Use judgment to decide whether two specifics are paraphrases or materially different — if they would produce overlapping body paragraphs, they're paraphrases; if they'd produce non-overlapping content, they're materially different.

## Process

1. **Resolve the Q-file(s) and target section(s).**

   **Batch mode** (Q-file path given directly):
   - Parse the file path: `/courses/<course>/Q-<N>-<topic>.md` → `course = <course>`, `module = <N>`.
   - Target sections = every H1 in the file with a `**Question(s)**:` block.

   **Multi-module batch mode** (course + list of module tokens):
   - Resolve the course slug as in single-section mode (match against directories under `/courses/`, case-insensitive). Zero or multiple matches → stop and ask. If no course is given at all → stop and ask which course.
   - Read `/courses/<course>/index.md` once.
   - For each token in the list (split on comma or semicolon, trim whitespace):
     - **Digit token** → use directly as module number `N`.
     - **Name token** → fuzzy-match against `## <N>. <Name>` headings in the course index (case-insensitive, allow trivial fuzziness — same matcher as single-section mode). Exactly one match required.
   - Mixed lists (`1, Truth, 3`) are allowed.
   - For each resolved `N`, glob `/courses/<course>/Q-<N>-*.md`. Exactly one file expected per module.
   - Target sections = every H1 with a `**Question(s)**:` block across **all** resolved Q-files, processed Q-file by Q-file (in the order the user gave the tokens).
   - **Any unresolvable token** (digit with no Q-file, name with zero or multiple matches, multiple Q-files for one N) → stop and ask. Don't silently skip and don't proceed with a partial list.

   **Single-section mode** (course + module name + H1 quoted):
   - Resolve the course slug: match the course name (e.g. "Logic") against directories under `/courses/` case-insensitively. One match → `course = <slug>`. Zero or multiple → stop and ask.
   - Resolve the module: read `/courses/<course>/index.md`, find the `## <N>. <Name>` heading whose `<Name>` matches the user-supplied module name (case-insensitive, allow trivial fuzziness — "Truth" matches "Truth" or "Truth and Falsity"). One match → `module = <N>`. Zero or multiple → stop and ask.
   - Locate the Q-file: glob `/courses/<course>/Q-<N>-*.md`. Exactly one file is expected.
   - Resolve the H1: parse all H1 headings in the Q-file. Match the user-supplied heading (with or without leading `#`, case-insensitive, fuzzy on whitespace and punctuation). Exactly one match required; otherwise stop and ask.
   - Target sections = the single matched H1.

   **Common to all modes:**
   - Read `/courses/<course>/index.md` once. For each module N being processed, find the `## <N>. <Name>` heading and capture `<Name>` for the output path.
   - If a path doesn't match the expected shape, or a module number isn't found in the course index, **stop and ask the user** — don't guess and don't fall back to `_unfiled/`.

2. **Load shared context once.**
   - Read `/.claude/skills/essay-philosophy/SKILL.md` (the rules to apply per section).
   - Read `/context/voice-dna.md` and `/context/icp.md`.
   - Read `/positions/<course>/index.md` if the directory exists.
   - Read `/sources/catalog.yaml` and the in-scope books' `index.md` files (per the course's `books:` frontmatter).
   - Cache these for the whole batch — do not re-read them per section.

3. **Parse the file into sections.**
   - Split on top-level `# ` (H1) headings. Each section yields `{ heading, specifics[], notes }`.
   - `specifics[]` = lines under `**Question(s)**:`, leading whitespace stripped, blank lines dropped.
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

   <Q-file H1 text>

   # Specifics

   The exam may pose this topic in any of the following forms. The essay must explain anything raised across them:

   - <specific 1, verbatim>
   - <specific 2, verbatim>
   - <specific 3, verbatim>
   ...

   # Notes for the writer

   <free-text notes from the section, if any>
   <one-line specifics-handling note if the specifics are materially different and each needs its own paragraph>
   ```

   **Topic-as-question rule** — the body of `# Question` is the **Q-file H1 text verbatim**. This becomes the essay's H1 verbatim (per essay-philosophy's H1 rule). Do **not** append a chosen specific, do **not** insert an em-dash, do **not** reformulate the topic as a sentence. The H1 names what the essay is about; the specifics live in their own section.

   Examples:
   - Q-file `# Nozick's entitlement theory of justice` → essay H1 `# Nozick's entitlement theory of justice`.
   - Q-file `# Williams on need vs merit and the irrationality of wealth-based distribution` → essay H1 `# Williams on need vs merit and the irrationality of wealth-based distribution`.

   **Specifics rule** — always include `# Specifics` whenever the section has at least one entry under `**Question(s)**`, even if there is only one. List every specific verbatim as a bullet, in the order they appear in the Q-file. The leader sentence (`The exam may pose this topic in any of the following forms…`) is fixed — it tells essay-philosophy that each bullet is an exam-question candidate the essay must address, not a reading note.

   For materially different specifics (the *grouped* case), add a one-line note in `# Notes for the writer` reminding the writer to allocate distinct paragraphs or sub-sections so each specific is explained — none silently dropped.

   Other rules:
   - `slugify(heading)` matches essay-philosophy's question-slug rule: lowercase, non-alphanumerics → `-`, collapse repeated dashes, trim. **If the heading starts with `Extra:` (case-insensitive), the slug must keep `extra-` as its leading token** — slugify the full heading including the `Extra:` prefix, do not strip it.
   - Omit `# Notes for the writer` entirely only if the section had no free-text notes **and** the specifics are all paraphrases of one another (no distinct-paragraph reminder needed).

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

   **Multi-module batch mode** — same per-section status lines as batch mode, but group them under a `## Module <N>: <Name>` header per Q-file (in the order the modules were resolved). Don't abort the run if one module fails entirely — record and continue to the next module. End with an aggregated summary line:

   `Wrote N essays across M modules in /courses/<course>/essays/` (plus skipped/failed counts if any).

   **Single-section mode** — fall through to essay-philosophy's default: write to disk, print the full essay to chat, end with `Saved to: <path>`. No batch-style status line, no summary count.

## Doing the batch efficiently

- Load shared context (voice, examiner, course index, positions index, source catalog, in-scope book indexes) **once at the top**. Reuse for every section.
- Resolve sources per-section — different topics need different ranges from the canonical book — but rely on the cached book-index reads.
- Write essays sequentially. Do not try to parallelise — each essay is ~1200 words, and they share enough loaded state that interleaving doesn't pay off.
- If the same source range appears across sections (e.g. multiple sections share a single chapter), read it once and reuse.

## Safety

- If the file has no H1 sections at all, stop and tell the user the file looks empty.
- If a section's heading exists but has no `**Question(s)**:` block, skip it (don't invent a question) — report in the summary (batch / multi-module batch) or refuse with a one-line explanation (single-section).
- If the course directory or module number can't be resolved, abort and tell the user — don't silently fall back to `_unfiled/`.
- **Single-section mode resolution failures** (any of: course slug ambiguous, module name not found in course index, multiple Q-files matched the module, H1 not found in Q-file, multiple H1s fuzzy-matched) — stop and ask the user to disambiguate. Do not guess.
- **Multi-module batch mode resolution failures** (any of: no course given, course slug ambiguous, a digit token has no matching Q-file, a name token has zero or multiple matches in the course index, multiple Q-files matched a single N) — stop and ask the user. Do not proceed with a partial list and do not silently skip unresolvable tokens.
- If essay-philosophy would refuse a section's prompt (e.g. no `course:`), that's a bug in this skill's prompt construction — fix the synthesised prompt, don't paper over it.

## Quality checklist

Before reporting completion:

- [ ] One essay file written per targeted H1 section (every H1 with a Question(s) block in batch / multi-module batch; the single named H1 in single-section mode)
- [ ] Each essay is at `/courses/<course>/essays/<moduleId>-<moduleName-slug>/<heading-slug>.md`
- [ ] Each essay individually passes the essay-philosophy quality checklist (voice, structure, length cap, no chapter/page refs, single-mention authors)
- [ ] Each essay's first line is a single `# <Q-file H1 text>` H1 — the topic, verbatim from the Q-file, with no em-dash, no specific appended, no reformulation
- [ ] Every specific listed under `**Question(s)**` for the H1 is explained somewhere in the essay; materially different specifics each got their own paragraph or sub-section
- [ ] Free-text notes under each H1 were respected
- [ ] Multi-module batch: every token in the user's list resolved to a module before any writing began; status lines grouped by module; aggregated summary at the end
- [ ] Chat output matches the mode: batch / multi-module batch → status line per section + summary count, no essay prose; single-section → essay prose printed, ending with `Saved to: <path>`
