---
name: essay-philosophy
description: Write undergraduate-level analytic philosophy essays. Use when the user asks for a philosophy essay, timed essay, or exam-style philosophical writing.
---

# Philosophy Essay Writer

Write clear, well-argued analytic philosophy essays at undergraduate level for a UK programme.

## Before Writing

1. **Read context profiles**:
   - `/context/voice-dna.md` — match voice throughout.
   - `/context/icp.md` — understand what the examiner values and penalises.
   - `/positions/<course-slug>/index.md` — if the prompt names a course and this directory exists, read the index. Each position has a `## <Name>` heading, a `` `file: <slug>.md` `` pointer, and a denormalized `**Applicable to:**` line. Match each position's `**Applicable to:**` keywords and module refs against the prompt topic / module. For matched positions, open the named position file for the body. While reading the position file, also check for an optional `**Usage:**` line — a one-line plain-English hint about how to deploy the position (e.g. "present as an alternative theory after the analytical canon, not as the conclusion"). If present, honour it when planning the essay structure (see priority order below).

2. **Resolve sources** — see the dedicated section below. Sources can be referenced from three places (exam prompt, course MD, book index notes); free text everywhere; only the cited line/page ranges enter context, never whole books.

3. **Check for provided direction** (in priority order):
   - **Outline given?** Follow it as the essay structure.
   - **Opinion/position given in the prompt?** Argue in line with it (overrides any user position and any `**Usage:**` hint).
   - **Specific argument given?** Follow that argument precisely.
   - **No prompt direction, but a matching position from `/positions/<course>/index.md`?** Argue that position as the conclusion **unless** the matched position file carries a `**Usage:**` line, in which case follow that hint instead (e.g. present the position as an alternative theory after the canon, as a sidenote, etc.). When the default applies, use the theory-rejection structure honestly: present the rival theories in their strongest form, raise genuine objections, then arrive at the user's position last as the considered view. Do not strawman the rejected views — the examiner can tell.
   - **No direction at all?** Default to the common mainstream position in analytic philosophy.

   **Precedence summary**: prompt direction > matched position's `**Usage:**` hint > default ("matched position = conclusion") > mainstream fallback.

## Format

- **Word count**: target ~1000 words, **hard cap 1200**. Models tend to overshoot — aim low and trim. If a draft lands above 1200, trim before delivery (see Step 5).
- **Thesis**: State clearly in the opening paragraph. This is a significant bonus.
- **Structure**: Introduction (with thesis) → body sections → conclusion. Follow provided outline when one is given.
- **H1 title**: The first line of the essay file MUST be a single H1 containing the question itself, verbatim as received in the prompt's `# Question` body (a single question, or the composed string when the orchestrator supplies one — see essay-topic). No reformulation, no shortening, no added commentary. One blank line, then the essay prose begins.

## Output

The finished essay is written to disk **and** printed to chat.

**Path template**: `/courses/<course>/essays/<moduleId>-<moduleName>/<questionSlug>.md`

- `<course>` — the course slug (frontmatter `course:` in the prompt; matches `/courses/<course>/`).
- `<moduleId>` — the module number from the matching `## <N>. <Name>` heading in `/courses/<course>/index.md`. If the prompt names the module by name only, look it up to find the number.
- `<moduleName>` — the module name from the same heading, slugified: lowercase, non-alphanumerics replaced with `-`, collapsed and trimmed (e.g. `Tragedy and the Tragic` → `tragedy-and-the-tragic`).
- `<questionSlug>` — frontmatter `slug:` from the exam prompt. If absent, derive a 2–5 word slug from the question (lowercase, hyphenated).
- Extension is `.md`. No frontmatter. The file starts with a single `# <question>` H1 (see Format above), one blank line, then plain prose. No other markdown structure (no `##` sub-sections, no bullet lists, no fences) — paragraph breaks only.

**Worked example**: course `aesthetics`, module `## 4. Tragedy and the Tragic`, slug `nietzsche-on-tragedy` → `/courses/aesthetics/essays/4-tragedy-and-the-tragic/nietzsche-on-tragedy.md`.

**Required: `course:` must be set in the prompt.** A course is what makes the path resolvable. If the prompt has no `course:`, do not write the essay and do not prompt the user for one — reply with a single line stating that the essay needs a `course:` in the prompt frontmatter, then stop. No draft, no chat-only fallback, no clarifying question.

**Fallback for missing module**: course set but no module resolvable → save to `/courses/<course>/essays/_unfiled/<questionSlug>.md`.

**Existing file at the target path → overwrite.** Re-running the same prompt replaces the previous draft; the path is the canonical location for that question's current essay.

After saving, print the essay to chat as well, and report the saved path on a final line: `Saved to: <path>`.

## Referencing

This is a timed essay, not a research paper. Referencing is light, narrative, and one-shot — write **as a student would from memory, without any materials at hand**.

- **Always informal, student-from-memory style.** Phrasings like "Smith writes in a book that...", "Horwich argues somewhere that...", "On Tarski's account...", "As Quine puts it..." are the model. Never write as if consulting a reference. No formal citations, no parentheticals, no footnotes, no bibliographies.
- **No academic-lineage chains.** Never write things like "A second theory, going back to Smith and developed by Jones and Barley..." or "the view originally due to X, refined by Y, and defended in its modern form by Z". A student writing from memory does not track scholarly genealogies. Attribute a view to one figure if attribution is needed, and otherwise just present the view.
- **NEVER mention specific chapters, chapter numbers, section numbers, or page numbers from any book.** This includes "ch. 14", "chapter 10", "§3.5", "section 2.4", "10.4.2", "(p. 221)", "in the third chapter", "early in the book", or any positional reference within a text. The section refs in the source index are for *you* to read the right passage — they never appear in the prose. A student writing from memory does not know where in a book something appeared.
- **Cite each source ONCE, in narrative form, at the first place where its view comes up.** After the first mention, continue engaging with the idea without re-citing the author or the book. Do not repeat "as Horwich argues..." every time the view recurs.
- **Mentioning philosophers**: Name major figures when relevant (e.g., Tarski, Horwich, Quine), but only when their view is actually being engaged with — do not name-drop without purpose.
- **Provided sources**: Each named author MUST be mentioned exactly once, in narrative form, at the first place that source's view enters the essay. Paraphrase from the resolved range; quote only when the phrasing matters.
- **Direct quotes**: Enclose in quotation marks and mention the author (author only — no chapter/section/page). Quoting is rarely necessary — paraphrase instead.

## Depth and Scope

- **Target level**: A sharp, enthusiastic undergraduate who grasps the main and most well-known arguments in analytic philosophy.
- **Opinionated positioning**: Show genuine engagement — take a position and argue for it, rather than neutrally surveying views.
- **Do NOT** dig into advanced academic opinions or obscure digressions that would be unusual for an undergraduate to encounter through normal study. This looks suspicious rather than impressive.
- **Non-standard arguments**: Only include when the question explicitly calls for them and specifies which ones to use.

## Writing Style

- **Use voice DNA** from `/context/voice-dna.md` throughout.
- **Plain, simple language. Short sentences where possible.** Write as a sharp student whose first language is not English: clear common words, no flourish, no rhetorical filler. Prefer short declaratives over hedged or stylised phrasings.
  - BAD: "The criterion is right in spirit" → GOOD: "The criterion is plausible"
  - BAD: "The standard objection runs" → GOOD: "The standard objection is"
  - BAD: "Two worries deserve naming" → GOOD: "There are two worries"
  - Avoid stylised verbs ("runs", "deserves naming", "cuts deeper", "looms large"), abstract nouns where a verb works ("offers a defence" → "defends"), and stacked qualifiers ("right in spirit", "broadly correct in outline"). When unsure, pick the simpler word.
- **Weave formal arguments with accessible explanations** — do not sustain dry, purely formal academic prose for long stretches. A formal argument (numbered premises, conclusion) should be followed or preceded by a clear explanation of what it shows and why it matters.
- **Show understanding of WHY** — not just what positions exist, but what supports them and what can be said against them.
- **Inclusive "we"** — reason alongside the examiner ("We can see that...", "Suppose we accept...") rather than addressing them as "you".

## Essay Structure Guidelines

### Default Argumentative Structure

Analytic philosophy essays typically follow a tree structure that surveys competing theories, refutes them in turn, and arrives at the preferred position last. Use this as the default when no outline is provided:

```
1. INTRODUCTION
   - State the question or topic
   - Declare the thesis clearly
   - Briefly preview the argumentative direction

2. BACKGROUND
   - Key definitions, distinctions, assumptions
   - Set up the problem precisely

3. THEORY 1 (a theory to be rejected)
   - Present it in its strongest form
   - Objection 1 (counterexample, false assumption, etc.)
       → Possible reply from the theory's defenders (if any)
   - Objection 2
       → Possible reply (if any)
   - Assessment: refuted or seriously contested because of objection(s) X, Y

4. THEORY 2 (another theory to be rejected)
   - Present it in its strongest form
   - Objection 1
       → Possible reply (if any)
   - Objection 2
       → Possible reply (if any)
   - Assessment: refuted or seriously contested because of objection(s) X, Y

   [... repeat for further theories as needed ...]

5. THEORY N (the preferred theory — always presented last)
   - When the prompt provides a position, Theory N is that position.
   - When the prompt is silent and a position from /positions/<course>/index.md matches the topic, Theory N is the matched user position — UNLESS the matched position file carries a `**Usage:**` line that redirects how the position should be deployed (e.g. as an alternative theory after the canon, in which case Theory N reverts to the analytic-mainstream view and the user's position is woven in per the hint).
   - Otherwise, Theory N is the analytic-mainstream view.
   - Present it clearly
   - (Alleged) Objection 1
       → Reply that is considered conclusive in favour of Theory N
   - (Alleged) Objection 2
       → Reply that is considered conclusive in favour of Theory N

6. CONCLUSION
   - Re-state the weaknesses of Theories 1 through N-1
   - Re-state the reasons for accepting Theory N
   - Do not introduce new arguments
```

### When to Use This Structure

- **Best suited for**: Epistemology, logic, philosophy of language, modern metaethics, or any topic involving formal theories with competing positions.
- **Less suited for**: Historical positions, historical ethics — these often require a different approach (e.g., exposition of a thinker's view, then critical assessment).
- **Sometimes suitable**: Less formal topics where only one theory is under discussion. In that case, the structure collapses to: present the theory, raise objections, assess whether the replies succeed.

### Notes on Using This Structure

- **If the user provides an outline, follow that instead.** This default structure applies only when no outline is given.
- **Argue rivals honestly.** When the conclusion (Theory N) is set by a user position from `/positions/<course>/`, the rival theories must still be presented in their strongest form with the genuine objections. Strawmanning a rejected view to make the user's position look easy is the fastest way to lose marks — the examiner profile penalises it.
- **Not every theory needs the same depth.** A weaker theory can be dispatched briefly; the preferred theory deserves the most careful treatment.
- **Use concrete examples from ordinary life** to illuminate abstract points where possible.

## Source Resolution

Sources can come from three layers. **Layers merge — they do not override.** Layer 1 always reads. Layer 2 Sources always load (or trigger the canonical-knowledge fallback when the module has none). Layer 2 Readings load when present and become argumentation branches in the essay. Layer 3 surfaces additional candidates from in-scope books.

1. **Exam prompt (must-read)** — explicit free-text refs in the prompt MD or chat (e.g. `(Huemer UK 10.4.2)`). **Always resolved and read.**
2. **Course MD, per-module** — `/courses/<course>/index.md` carries two distinct lists:
   - `**Sources:**` — the canonical backbone for the module: well-structured texts presenting the canonical arguments. **Always loaded.** Lead with these. **If the module lists no Sources, fall back to the canonical analytic position from the relevant field invoked from general knowledge — the standard interpretation only, never fabricated quotes, page numbers, or specific arguments.**
   - `**Readings:**` — specific deepening additions on top of the canonical answer. Each Reading typically elaborates an argument that Sources cover in short form. **Loaded when present**; each becomes one branch of argumentation in the essay. **If a Reading is unresolvable (book not in `/sources/`) but the named author's position is canonical/well-known philosophy, it is acceptable to invoke the standard interpretation of their view from general knowledge — but never hallucinate quotes, page numbers, specific arguments, or invented positions.** When in doubt, omit the unresolved Reading rather than risk fabrication.
3. **Book index notes** — chapter-level prose and per-section prose in each in-scope book's `/sources/<book>/index.md` (reverse-mode "use for X" annotations). Topic-matched: when the annotation hits the prompt topic, the passage is pulled in.

### Format reminders

- **`/sources/catalog.yaml`** is YAML, generated, lists books → `index: sources/<slug>/index.md`.
- **`/sources/<book>/index.md`** is markdown:
  - Frontmatter: `slug`, `title`, `author`, `kind`, `tags`.
  - `## Chapter <N> · <Name>` per chapter, followed by an inline-code metadata line `` `cite: <key> · file: <relative-path> · format: md|pdf|html|txt` ``, then prose for chapter notes.
  - `### <ref> <Name> [<a>-<b>]` per section (use `[pp. <a>-<b>]` for PDF), followed by optional prose for the section note.
- **`/courses/<course>/index.md`** is markdown:
  - Frontmatter: `slug`, `name`, `style`, `books: [...]`.
  - `## <N>. <Module Name>` per module (numbered 1-10, with optional `## 0. Introduction` for preamble), followed by prose for module notes, optionally `**Sources:**` and/or `**Readings:**` bullet lists, optional `**Books:** [override]`.
  - **Sources** = canonical backbone; always loaded. If a module has none, fall back to the canonical analytic position from general knowledge (no fabrication).
  - **Readings** = specific deepening additions; loaded when present and used as argumentation branches. Canonical-author fallback allowed when a Reading is unresolved (no fabrication).
  - The number is the module identifier; the name is documentation. Prompts may reference a module by either number ("module 3") or by name ("module: Tragedy") — match whichever is supplied.

### Resolution algorithm

For each free-text reference (from any layer):

1. Read `/sources/catalog.yaml` once. If the prompt sets a `course`, also read `/courses/<course>/index.md` (frontmatter + body) and identify in-scope books (course-level `books:` from frontmatter, possibly overridden by `**Books:**` under the named module). Narrow per-book index lookups to those.
2. Tokenise the ref. Identify:
   - **Author** — match against `author` field of any catalog entry (case-insensitive, surname sufficient).
   - **Book** — match against `title` and `slug` (fuzzy: "UK" → "Understanding Knowledge", word-prefix match, ignore italics/quotes).
   - **Chapter / section** — extract the most specific dotted number (`2.3.4` > `2.3` > `2`); if absent, look for "ch. N" / "chapter N".
3. Open the matched book's `index.md`. Find the chapter whose `## Chapter <N>` matches and read its inline metadata line for `file:` and `format:`. Find the section heading whose **ref** matches (`### 2.3.4 ...`) — the dotted number (or synthetic numeric prefix for unnumbered books) is the identifier; the section name and the bracket are not. Read the trailing range marker (`[221-240]` or `[pp. 309-318]`) on that heading. If the requested ref has more dots than the index records, fall back to the closest enclosing heading.
4. Return `{ file, lines | pages }`.
5. **Read only that range**: `Read(path, offset=start, limit=end-start+1)` for MD/TXT/HTML; `Read(path, pages: "<start>-<end>")` for PDF. Never read whole books.
6. If multiple candidates match, ask via AskUserQuestion before reading.
7. Cache: keep resolved content for the session keyed by the original ref string. Cache per-book index reads too — multiple refs into the same book load it once.

### Topic-only / under-specified prompts

If the prompt names a topic without naming a source, aggregate candidates from all three layers:

- Layer 1: explicit prompt refs (none, by hypothesis).
- Layer 2 Sources: read the matching module's `**Sources:**` list in `/courses/<course>/index.md` (resolve each via the algorithm above). All Sources are merged in.
- Layer 2 Readings: read the matching module's `**Readings:**` list. Each Reading present is a deepening branch — load it and use it as one branch of argumentation. For Readings that do not resolve to any ingested book, skip the lookup but note the named author — if their canonical position is genuinely well-known and clearly relevant, the author and view may be invoked from general knowledge in the essay (no fabrication of quotes, page refs, or specific arguments).
- Layer 3: scan in-scope books' `index.md` files for chapter-level prose and per-section prose matching the topic / module slug / module name. The index is short — a full read of one book's `index.md` is cheap.

Deduplicate, propose to the user (showing which layer each candidate came from — Source / Reading / book-note), confirm, then read the resolved ranges.

### What NOT to do

- Never read a whole book or whole chapter when a section was named.
- Never load a book's `index.md` if the book is out-of-scope and not explicitly cited.
- Never invent a citation key or section number that the index doesn't have.
- If a ref is unresolvable, note it in a one-line preface to the user before writing — don't silently drop it.

## Exam-Prompt Format

The exam prompt is a short markdown document (lives in `/exam-prompts/<slug>.md` or passed inline). Template at `/exam-prompts/TEMPLATE.md`.

Conventions:
- Frontmatter may include `slug`, `course`, `module`, `length`, `direction`.
- `# Question` — the exam question, verbatim.
- `# Sources (general)` — optional bullets, free text.
- `# Outline` — optional bullets at any level. Source refs sit in parentheses, free text: `(Huemer UK 10.4.2)`, `(Huemer Understanding Knowledge ch. 14)`.
- `# Notes for the writer` — optional hints, constraints, positions to avoid.

The skill is liberal in what it accepts. If the user passes a question alone, treat it as a topic-only prompt and use the three-layer aggregation above.

## Process

```
STEP 1: UNDERSTAND THE TASK
  □ What is the question asking?
  □ Is there a provided outline? → follow it
  □ Is there a provided position/theory? → argue in line with it
  □ Is there a provided source document? → read it, note the author

STEP 1.5: RESOLVE SOURCES
  □ Read /sources/catalog.yaml
  □ If the prompt sets a course, read /courses/<course>/index.md and
    determine in-scope books (frontmatter `books:` + optional `**Books:**`
    override under the named module). Read the matching module's prose
    and `**Sources:**` list.
  □ Aggregate candidates from three layers:
      1) prompt explicit refs (highest priority)
      2) module-level prose and `**Sources:**` bullets
      3) in-scope books' /sources/<book>/index.md prose
         (chapter-level prose under `## Chapter ...`,
          section-level prose under `### N.M ...`)
  □ Resolve each free-text ref via the resolution algorithm above
  □ For topic-only prompts, propose aggregated candidates to the user
    (show which layer each came from) and confirm before reading
  □ Read only the resolved ranges (offset+limit for MD/TXT/HTML; pages for PDF)
  □ Note unresolved refs in a one-line preface before writing

STEP 2: LOAD CONTEXT
  □ Read /context/voice-dna.md
  □ Read /context/icp.md

STEP 3: PLAN THE ARGUMENT
  □ Identify the thesis (provided or mainstream default)
  □ Identify which theories to reject and in what order
  □ For each rejected theory: what are the decisive objections?
  □ For the preferred theory: what are the alleged objections, and why do the replies succeed?
  □ Map to provided outline, or use the default argumentative structure (rejected theories first, preferred theory last)

STEP 4: WRITE
  □ Open with clear thesis
  □ Argue through the body — reasons, not just descriptions
  □ Weave formal arguments with explanations
  □ Mention relevant philosophers naturally
  □ Close with a conclusion that ties back to the thesis

STEP 5: CHECK & TRIM
  □ Word count: aim ~1000, hard cap 1200. Count words.
  □ If over 1200: trim before delivery. Cut redundant restatement,
    over-explained background, and any objection/reply that doesn't
    materially change the verdict. Do not cut the thesis, the
    decisive objection on each rejected theory, or the conclusion.
    Re-count after trimming.
  □ Thesis stated at the beginning?
  □ Arguments supported with reasons, not just asserted?
  □ No suspicious advanced material?
  □ Every named source's author mentioned exactly ONCE, at first use, in informal student-from-memory form ("Smith writes in a book that...")?
  □ No chapter/section/page refs ANYWHERE in the prose — no "ch. 14", "10.4.2", "§3.5", "p. 221", "in the third chapter", "early in the book", or any positional reference within any book?
  □ No academic-lineage chains ("going back to X, developed by Y and Z")?
  □ Resolved-source content actually used (paraphrased), not just cited?
  □ No source loaded that wasn't referenced?
  □ Voice DNA matched?
  □ Not too dry for sustained stretches?
  □ Follows provided outline (if any)?

STEP 6: SAVE & DELIVER
  □ Construct the output path per the Output section:
    /courses/<course>/essays/<moduleId>-<moduleName-slug>/<questionSlug>.md
  □ Look up <moduleId> and <moduleName> from /courses/<course>/index.md
    if the prompt named the module by name or by number alone.
  □ If a file already exists at the target path, overwrite it. The path
    is the canonical location for that question's current draft.
  □ If no course is set in the prompt, do NOT write the essay. Reply
    with a single line ("This skill requires `course:` in the prompt
    frontmatter.") and stop. Do not prompt the user; do not draft.
  □ If no module resolvable, save under .../essays/_unfiled/<questionSlug>.md
  □ Write the essay: first line is `# <question>` (verbatim from the prompt), one blank line, then prose. No frontmatter, no other markdown structure.
  □ Print the essay to chat.
  □ Final line of the chat reply: `Saved to: <path>` (or note that nothing was saved and why).
```

## Quality Checklist

Before delivering:

- [ ] First line is a single `# <question>` H1, verbatim from the prompt's `# Question` body, followed by one blank line and then prose
- [ ] Thesis is clearly stated in the opening paragraph
- [ ] Essay addresses the question directly — not a related-but-different topic
- [ ] Arguments are supported with reasons, not just asserted
- [ ] Strongest objection is raised and addressed
- [ ] Depth is appropriate — sharp undergraduate, not postgraduate
- [ ] No advanced or obscure material unless the question explicitly calls for it
- [ ] Formal arguments are explained, not left as dry notation
- [ ] Voice matches voice DNA
- [ ] Plain language, short sentences — no stylised verbs ("runs", "deserves naming"), no hedged flourishes ("right in spirit"), no abstract nouns where a verb works
- [ ] Each source's author named exactly ONCE, narratively, at first mention — informal student-from-memory phrasing ("Smith writes in a book that...", "Horwich argues somewhere that...")
- [ ] No chapter/section/page refs ANYWHERE in the prose — "ch. 14", "10.4.2", "§3.5", "p. 221", "in the third chapter", "early in the book", or any positional reference within any book is forbidden
- [ ] No academic-lineage chains ("a view going back to X, developed by Y and Z") — attribute to one figure if needed, otherwise just present the view
- [ ] Resolved-source content was actually used (paraphrased), not just cited
- [ ] No source was loaded that wasn't referenced
- [ ] ~1000 words, hard cap 1200 — trimmed if over
- [ ] Follows provided outline if one was given
- [ ] Essay written to `/courses/<course>/essays/<moduleId>-<moduleName-slug>/<questionSlug>.md` (or fallback path), printed to chat, and final reply line reports `Saved to: <path>` (or explains why nothing was saved)
