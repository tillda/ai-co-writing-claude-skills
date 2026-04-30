---
name: essay-philosophy
description: Write undergraduate-level analytic philosophy essays. Use when the user asks for a philosophy essay, timed essay, or exam-style philosophical writing.
---

# Philosophy Essay Writer

Write clear, well-argued analytic philosophy essays at undergraduate level for a UK programme.

## Before Writing

1. **Read context profiles**:
   - `/context/voice-dna.json` — match voice throughout.
   - `/context/icp.json` — understand what the examiner values and penalises.
   - `/context/positions-<course-slug>.md` — if the prompt names a course and this file exists, read it. Match each position's `**Applicable to:**` keywords and module refs against the prompt topic / module. Note any matches.

2. **Resolve sources** — see the dedicated section below. Sources can be referenced from three places (exam prompt, course MD, book index notes); free text everywhere; only the cited line/page ranges enter context, never whole books.

3. **Check for provided direction** (in priority order):
   - **Outline given?** Follow it as the essay structure.
   - **Opinion/position given in the prompt?** Argue in line with it (overrides any user position).
   - **Specific argument given?** Follow that argument precisely.
   - **No prompt direction, but a matching position from `/context/positions-<course>.md`?** Argue that position as the conclusion. Use the theory-rejection structure honestly: present the rival theories in their strongest form, raise genuine objections, then arrive at the user's position last as the considered view. Do not strawman the rejected views — the examiner can tell.
   - **No direction at all?** Default to the common mainstream position in analytic philosophy.

## Format

- **Word count**: ~1200 words (unless specified otherwise)
- **Thesis**: State clearly in the opening paragraph. This is a significant bonus.
- **Structure**: Introduction (with thesis) → body sections → conclusion. Follow provided outline when one is given.

## Referencing

This is a timed essay context — no full formal referencing required.

- **Mentioning philosophers**: Name major figures when relevant (e.g., Tarski, Horwich, Quine), but only when their view is actually being engaged with — do not name-drop without purpose.
- **Provided sources**: Each named author MUST be mentioned at least once.
   - General sources: name the author in the introduction or first body section.
   - Per-bullet sources: name the author in the section that uses that source.
   - Multiple sources for one bullet: name each author at first use.
   - Paraphrase from the resolved range; quote only when the phrasing matters.
- **Direct quotes**: Enclose in quotation marks and mention the author. But direct quoting is rarely necessary — paraphrase instead.
- **Format**: Informal in-text mentions are sufficient (e.g., "As Horwich argues, ..." or "On Tarski's account, ...").

## Depth and Scope

- **Target level**: A sharp, enthusiastic undergraduate who grasps the main and most well-known arguments in analytic philosophy.
- **Opinionated positioning**: Show genuine engagement — take a position and argue for it, rather than neutrally surveying views.
- **Do NOT** dig into advanced academic opinions or obscure digressions that would be unusual for an undergraduate to encounter through normal study. This looks suspicious rather than impressive.
- **Non-standard arguments**: Only include when the question explicitly calls for them and specifies which ones to use.

## Writing Style

- **Use voice DNA** from `/context/voice-dna.json` throughout.
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
   - When the prompt is silent and a position from /context/positions-<course>.md matches the topic, Theory N is the matched user position.
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
- **Argue rivals honestly.** When the conclusion (Theory N) is set by a user position from `/context/positions-<course>.md`, the rival theories must still be presented in their strongest form with the genuine objections. Strawmanning a rejected view to make the user's position look easy is the fastest way to lose marks — the examiner profile penalises it.
- **Not every theory needs the same depth.** A weaker theory can be dispatched briefly; the preferred theory deserves the most careful treatment.
- **Use concrete examples from ordinary life** to illuminate abstract points where possible.

## Source Resolution

Sources can come from three layers. **Layers merge — they do not override.** Layer 1 always reads, layer 2 Sources always merge, layer 2 School Readings merge selectively, layer 3 surfaces additional candidates from in-scope books.

1. **Exam prompt (must-read)** — explicit free-text refs in the prompt MD or chat (e.g. `(Huemer UK 10.4.2)`). **Always resolved and read.**
2. **Course MD, per-module** — `/courses/<course>/index.md` carries two distinct lists:
   - `**Sources:**` — what the user has indicated they will use. **Always merged with layer 1.** Resolve every entry as a candidate.
   - `**School Readings:**` — school-suggested bibliography. Loaded only if (a) the prompt names them explicitly, or (b) layers 1 + Sources don't cover the topic and a School Reading clearly fits. **If a School Reading is unresolvable (book not in `/sources/`) but the named author's position is canonical/well-known philosophy, it is acceptable to invoke the standard interpretation of their view from general knowledge — but never hallucinate quotes, page numbers, specific arguments, or invented positions.** When in doubt, omit the unresolved School Reading rather than risk fabrication.
3. **Book index notes** — chapter-level prose and per-section prose in each in-scope book's `/sources/<book>/index.md` (reverse-mode "use for X" annotations). Topic-matched: when the annotation hits the prompt topic, the passage is pulled in.

### Format reminders

- **`/sources/catalog.yaml`** is YAML, generated, lists books → `index: sources/<slug>/index.md`.
- **`/sources/<book>/index.md`** is markdown:
  - Frontmatter: `slug`, `title`, `author`, `kind`, `tags`.
  - `## Chapter <N> · <Name>` per chapter, followed by an inline-code metadata line `` `cite: <key> · file: <relative-path> · format: md|pdf|html|txt` ``, then prose for chapter notes.
  - `### <ref> <Name> [<a>-<b>]` per section (use `[pp. <a>-<b>]` for PDF), followed by optional prose for the section note.
- **`/courses/<course>/index.md`** is markdown:
  - Frontmatter: `slug`, `name`, `style`, `books: [...]`.
  - `## <N>. <Module Name>` per module (numbered 1-10, with optional `## 0. Introduction` for preamble), followed by prose for module notes, optionally `**Sources:**` and/or `**School Readings:**` bullet lists, optional `**Books:** [override]`.
  - **Sources** = user-indicated working set; always merged with prompt refs.
  - **School Readings** = school-suggested bibliography; loaded only on explicit reference or as fallback; canonical-author fallback allowed when unresolved (no fabrication).
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
- Layer 2 School Readings: read the matching module's `**School Readings:**` list. Surface only the entries that clearly fit the topic; the rest are background bibliography. For School Readings that do not resolve to any ingested book, skip the lookup but note the named author — if their canonical position is genuinely well-known and clearly relevant, the author and view may be invoked from general knowledge in the essay (no fabrication of quotes, page refs, or specific arguments).
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
  □ Read /context/voice-dna.json
  □ Read /context/icp.json

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

STEP 5: CHECK
  □ ~1200 words?
  □ Thesis stated at the beginning?
  □ Arguments supported with reasons, not just asserted?
  □ No suspicious advanced material?
  □ Every named source's author mentioned in its section?
  □ Resolved-source content actually used (paraphrased), not just cited?
  □ No source loaded that wasn't referenced?
  □ Voice DNA matched?
  □ Not too dry for sustained stretches?
  □ Follows provided outline (if any)?
```

## Quality Checklist

Before delivering:

- [ ] Thesis is clearly stated in the opening paragraph
- [ ] Essay addresses the question directly — not a related-but-different topic
- [ ] Arguments are supported with reasons, not just asserted
- [ ] Strongest objection is raised and addressed
- [ ] Depth is appropriate — sharp undergraduate, not postgraduate
- [ ] No advanced or obscure material unless the question explicitly calls for it
- [ ] Formal arguments are explained, not left as dry notation
- [ ] Voice matches voice DNA
- [ ] Authors of provided sources are mentioned in the relevant section
- [ ] Resolved-source content was actually used (paraphrased), not just cited
- [ ] No source was loaded that wasn't referenced
- [ ] ~1200 words
- [ ] Follows provided outline if one was given
