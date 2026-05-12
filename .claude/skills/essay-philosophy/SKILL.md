---
name: essay-philosophy
description: Write undergraduate-level analytic philosophy essays. Use when the user asks for a philosophy essay, timed essay, or exam-style philosophical writing.
---

# Philosophy Essay Writer

Write clear, well-argued analytic philosophy essays at undergraduate level for a UK programme.

## Before Writing

1. **Read context profiles** — `/context/voice-dna.md` (match voice throughout) and `/context/icp.md` (what the examiner values and penalises).

2. **Match positions** — if the prompt names a course and `/positions/<course>/index.md` exists, read the index and match each entry's denormalized `**Applicable to:**` line against the prompt topic / module. For matched entries, open the named position file. While reading, note any `**Usage:**` line — a one-line hint about how to deploy the position (e.g. "present as an alternative theory after the analytical canon, not as the conclusion"). Honour it when planning structure.

3. **Resolve sources** — see the dedicated section below. Three layers (exam prompt, course MD, book index). Free text everywhere; only the cited line/page ranges enter context, never whole books.

4. **Direction precedence** (highest first):
   - **Outline or provided argumentation given?** Mirror it. This covers anything from a numbered ten-point outline to a rough prose narration of the arguments — any pre-laid-out content describing how the essay should be argued. Follow its structure and inferential moves closely, ideally argument-per-argument, while still applying voice DNA, referencing rules, and the rest of the conventions in this skill. See the dedicated subsection below.
   - **Opinion / position / specific argument in the prompt?** Argue in line with it (overrides any user position and any `**Usage:**` hint).
   - **Matched user position?** Argue that position as the conclusion **unless** the matched file's `**Usage:**` redirects (e.g. present as an alternative after the canon).
   - **No direction?** Argue the analytic-mainstream view.

### Mirroring provided argumentation

When the prompt supplies an outline or any laid-out argumentation (numbered outline, bulleted skeleton, rough narration, draft prose):

- **Treat the supplied content as the spine.** Each distinct argument, objection, or move in it gets a corresponding argument in the essay, in the same order, with the same dialectical role (premise, objection, reply, verdict). Do not silently drop, reorder, or merge moves; do not invent new branches not present in the source.
- **Match the outline's emphasis — depth tracks prominence.** The amount of essay-space an argument gets must mirror the amount of outline-space it gets. Two regimes:
  - **Detailed outline arguments → present closely in argument-shape, not in wording.** When the outline lays an argument out in detail (its own paragraph of prose, a full sub-tree of bullets with reasons and replies, or a numbered premise-by-premise statement), the essay treats it as a load-bearing argument: present it closely *in shape* — same dialectical role, same order of moves, same specific reasons given, same conclusion. Do not paraphrase into a higher-level summary; do not substitute a different argument for the same conclusion.
  - **Bullets at depth-3 / depth-4, or single items in a long list → keep brief, do not expand.** When an argument appears as a single bullet inside a longer list of siblings, or sits at the third or fourth level of nesting, it is a *mention*, not a load-bearing argument. One sentence in the essay is usually enough — sometimes a clause inside another sentence. Do not promote a depth-4 bullet into a full paragraph; do not invent a sub-dialectic of objections-and-replies the outline doesn't supply. If the outline lists ten such bullets under one parent, the essay groups or compresses them, it does not give each its own paragraph.
  - **The test:** roughly count the outline's words against the essay's words per argument. If the outline gave argument A four times the words of argument B, the essay should too — the proportion is the signal.
- **What "follow closely" means.** Whenever an instruction (in this skill, in the prompt, or in an outline) says to follow something *closely* — an outline, an argument, a sketched move — it means **follow the argumentative moves AND structural shape, not the words and sentences**. Two halves:
  - **Mirror the moves and the structure.** Same dialectical role, same order, same specific reasons. If the outline enumerates three objections, your essay enumerates three objections, signposted (`First, … / Second, … / Third, …`, `Objection 1: …`, narrative `##` sub-headings). The argumentative scaffolding is part of what is being followed; paraphrasing the outline does not mean dissolving its structure into a wall of prose. See Format → "Narrative structure markers".
  - **Original wording, original sentence structure, original examples.** Different prose, different sentence boundaries, your own wording throughout. Where the source uses a concrete example (thought experiment, counter-example, analogy), invent a similar one of your own — same role, similar logical structure, original surface. Verbatim re-use only when the example *is* the canonical case (Gettier, brain-in-a-vat, trolley) and rewriting loses the reference. The only verbatim allowance for non-canonical content is **formal logical premises** (see Writing Style: numbered premises and inline propositional formulations).
- **Translate, don't transcribe.** Rewrite in the user's voice (per `/context/voice-dna.md`), expand telegraphic notes into argued prose where the outline calls for depth, weave attribution into the inference, and apply the no-markdown / no-em-dash / no-positional-refs rules. The supplied text is a scaffold for *what* to argue, not a draft of *how* to phrase it. "Closely" is about argument shape, never about lexical copying — see the "follow closely" rule above.
- **Add only what the form demands.** A thesis sentence, a brief setup, transitions, and a conclusion that echoes the supplied verdict are fine. Background or extra theories not in the supplied content do not belong unless the supplied content gestures at them.
- **If the supplied content conflicts with a matched user position or a `**Usage:**` hint, the supplied content wins** — it sits above position-matching in the precedence list. Note the conflict in a one-line preface only if the user clearly didn't realise (e.g. the outline argues *against* a position they normally hold).
- **Sources still resolve normally.** Refs cited inside the outline are read; the three-layer source resolution still runs for unattributed moves. The mirroring constraint is on argument structure, not on what evidence backs each step.

## Format

- **Word count**: ~1000 words, **hard cap 1200**. Models overshoot — aim low and trim.
- **Thesis / opening statement**: stated clearly in the opening paragraph. When the provided sources (prompt refs, course-MD Sources/Readings, book-index canonical sections) contain a natural direction of argumentation or a clear conclusion, the opening paragraph must explicitly say what the essay is going to argue for — not just preview the topic. Land the thesis in one sentence: "I argue that …", "The view defended here is …", "This essay rejects … in favour of …". No wishy-washy "we shall see".
- **Structure**: introduction (with thesis) → body → conclusion. The conclusion paragraph **must match the opening**: it restates the same thesis as now established, names the rejected rivals briefly, and adds no new arguments. Opening and conclusion are bookends. If an outline or provided argumentation is given, mirror its structure instead (see "Mirroring provided argumentation" above).
- **Narrative structure markers**: break long stretches of prose with light visual rhythm — either short narrative `##` sub-headings (noun-phrase, e.g. `## The empiricist reply`, `## Two objections`) or inline labels at the start of paragraphs (`Objection 1: the criterion is too coarse. …`, `Objection 2: …`, `First reply: …`, `A second worry: …`). Use sparingly: roughly three to five markers per essay, not one per paragraph. Pure walls of text are forbidden; so is over-segmentation.
- **H1 title**: first line is a single `# <question>` H1, verbatim from the prompt's `# Question` body. One blank line, then prose.

## Output

The finished essay is written to disk **and** printed to chat.

**Path template**: `/courses/<course>/essays/<moduleId>-<moduleName-slug>/<questionSlug>.md`

- `<course>` — frontmatter `course:` (matches `/courses/<course>/`).
- `<moduleId>` and `<moduleName>` — looked up from the matching `## <N>. <Name>` heading in `/courses/<course>/index.md`. Slugify the name: lowercase, non-alphanumerics → `-`, collapse, trim. E.g. `Tragedy and the Tragic` → `tragedy-and-the-tragic`.
- `<questionSlug>` — frontmatter `slug:`; if absent, derive a 2–5 word slug from the question. **If the question's H1 (or the Q-file H1 it was derived from) starts with `Extra:` (case-insensitive), the slug must keep `extra-` as its leading token** — do not strip the `Extra:` qualifier when slugifying.

The file has no frontmatter. First line is `# <question>`, blank line, then prose. Short narrative `##` sub-headings (noun-phrase) are permitted as structure markers, used sparingly (≈3–5 per essay); inline section labels (`Objection 1: …`) are an equally good alternative. No bullets, no fences, no numbered markdown lists — `##` plus paragraph breaks is the only structure.

**Worked example**: course `aesthetics`, module `## 4. Tragedy and the Tragic`, slug `nietzsche-on-tragedy` → `/courses/aesthetics/essays/4-tragedy-and-the-tragic/nietzsche-on-tragedy.md`.

**Required: `course:` must be set.** If the prompt has no `course:`, reply with one line saying so and stop. No draft, no clarifying question.

**Fallback**: course set but no module resolvable → save to `/courses/<course>/essays/_unfiled/<questionSlug>.md`.

**Existing file → overwrite.** Re-running the same prompt replaces the previous draft.

After saving, print the essay to chat. Final reply line reports `Saved to: <path>`.

## Referencing

This is a timed essay, not a research paper. Referencing is light, narrative, one-shot — write **as a student would from memory, without any materials at hand**.

- **Always informal, student-from-memory style.** Phrasings like "Smith writes in a book that...", "Horwich argues somewhere that...", "On Tarski's account...", "As Quine puts it...". Never write as if consulting a reference. No formal citations, no parentheticals, no footnotes, no bibliographies.
- **No academic-lineage chains.** Never "a view going back to Smith and developed by Jones and Barley...". A student writing from memory does not track scholarly genealogies. Attribute to one figure if needed, otherwise just present the view.
- **NEVER mention specific chapters, chapter numbers, section numbers, or page numbers.** Includes "ch. 14", "§3.5", "10.4.2", "(p. 221)", "in the third chapter", "early in the book", or any positional reference within a text. Section refs in the source index are for *you* to read the right passage — they never appear in prose.
- **Cite each source ONCE, narratively, at first use.** After that, engage with the idea without re-citing. Each named author from a provided source appears exactly once.
- **Mention philosophers** only when their view is actually being engaged with — no name-dropping.
- **Direct quotes** — quotation marks plus author name only (no chapter/section/page). Quoting is rarely necessary; paraphrase instead.

## Depth and Scope

- **Target level**: a sharp, enthusiastic undergraduate who grasps the main and most well-known arguments in analytic philosophy.
- **Opinionated positioning**: take a position and argue for it; do not neutrally survey.
- **Do NOT** dig into advanced academic opinions or obscure digressions an undergraduate wouldn't normally encounter — looks suspicious rather than impressive.
- **Non-standard arguments**: only when the question explicitly calls for them.

## Writing Style

- **Use voice DNA** from `/context/voice-dna.md` throughout.
- **Plain, simple language.** Write as a sharp student whose first language is not English: clear common words, no flourish, no rhetorical filler.
  - BAD: "The criterion is right in spirit" → GOOD: "The criterion is plausible"
  - BAD: "The standard objection runs" → GOOD: "The standard objection is"
  - BAD: "Two worries deserve naming" → GOOD: "There are two worries"
  - Avoid stylised verbs ("runs", "deserves naming", "cuts deeper", "looms large"), abstract nouns where a verb works ("offers a defence" → "defends"), and stacked qualifiers ("right in spirit", "broadly correct in outline"). When unsure, pick the simpler word.
- **Sentence length: write long for the inferential tissue, then split.** Long sentences are good connective tissue — they trace an inference, weigh a view against an objection, tie a reply back to a prior claim. The fix for readability is *not* to write short sentences from the start; it is to write the long argumentative sentence and then split it on its connectives. Break on words like *but*, *because*, *and*, *so*, *yet* — the connective stays at the head of the new sentence, preserving the link. Example: "X holds A, but this fails because Y, and so the criterion collapses." → "X holds A. But this fails, because Y. And so the criterion collapses." The argument still reads as one inferential chain; each piece is short enough to follow.
  - Default to splitting wherever a coordinating conjunction joins two independent clauses, or where a `,` precedes a *because* / *so* / *but* clause.
  - Avoid runs of three or more sentences all under ~10 words unless the rhythm is doing real work.
  - Avoid the "X says, Y says, Z says" cadence: prefer "X holds A. But this fails, because…", "The natural reply, defended by Y, is that…" — attribution woven into the inference, not front-loaded.
  - Use colons and subordinate clauses freely when they make the inferential structure clearer. **No em-dashes and no semicolons** (see Forbidden formulations) — when tempted to join two clauses with either, split into two sentences instead.
- **Enumerative markers at paragraph starts.** Use "First, …", "Second, …", "Third, …" (and "Finally, …" for the closing item) at the head of paragraphs that introduce successive objections, considerations, or steps in an argument. They anchor the reader, signal the structure of the dialectic, and give the essay rhythm. Use them when the underlying structure is genuinely enumerated; don't sprinkle them as decoration.
- **Split long paragraphs.** A paragraph that runs past ~6–8 sentences usually contains two argumentative moves. Split it. One paragraph = one inferential move (a claim and its support, an objection and its reply, a verdict and its grounds) — then a paragraph break.
- **No markdown emphasis in prose.** No `**bold**`, no `*italic*`, no `_underscore_` emphasis anywhere in the body. The H1 title and the permitted narrative `##` sub-headings are the only markdown structure; everything else is plain prose. Emphasis is carried by word choice and sentence shape, not by formatting.
- **Weave formal arguments with accessible explanations** — do not sustain dry, purely formal academic prose. A formal argument (numbered premises, conclusion) should be followed or preceded by a clear explanation of what it shows and why it matters. **Premises in formal logical argumentation may be reproduced verbatim from the source**, in either form — displayed/numbered (e.g. `(1) S knows that S is not a brain in a vat. (2) …`) or inline propositional formulations (e.g. *Jones owns a Ford OR Brown is in Barcelona implies I know that …*). The propositional structure is load-bearing; rephrasing it can distort the argument. No quotation marks are needed for premises in this form. The surrounding commentary — motivation, what the argument shows, replies — stays in your own voice.
- **Show understanding of WHY** — not just what positions exist, but what supports them and what can be said against them.
- **Inclusive "we"** — reason alongside the examiner ("We can see that...", "Suppose we accept..."), not "you".

### Forbidden formulations

Never use any of the following in essay prose. They mark AI-style or generic-academic writing and immediately break voice. If a draft contains one, rewrite the sentence — do not just swap a synonym.

**Banned constructions:**
- **Triplets of the form "foo, bar and baz"** — never list three items joined by "and". Use two, or split into separate sentences, or restructure.
- **"Not only X, but also Y"** — restructure as two clauses or two sentences.
- **Em-dashes (—).** Replace with comma, colon, or full stop.
- **Semicolons (;).** Never used to connect sentence parts. **Always split into two sentences** — there are no exceptions, no "stylistic" uses, no "the clauses are tightly linked" carve-outs. If you find yourself reaching for a `;`, the second clause needs to start a new sentence (with a connective like *But*, *And*, *Because*, *So* at its head if the link must be preserved).
- **Markdown emphasis in prose (`**bold**`, `*italic*`, `_underscore_`).** Emphasis is carried by word choice and sentence shape, not by formatting. Only the H1 title and permitted narrative `##` sub-headings use markdown.

**Enumerated lists inside prose — `(i)`, `(ii)`, `(iii)`:**
- When using parenthetical Roman numerals to enumerate considerations, objections, or steps, **each item starts a new sentence AND a new paragraph**, with a **capital letter** at the start and a **full stop** at the end. The paragraph break before the next marker is what makes the enumeration readable on the page — never two markers inside the same paragraph.
- Example (correct):

  `(i) The criterion is too coarse.`

  `(ii) It collapses on the borderline cases.`

  `(iii) No principled fix is on offer.`

  Three sentences, three paragraphs.
- Never write `(i) the criterion is too coarse, (ii) it collapses on the borderline cases, …` — comma-joined lower-case lists are forbidden. Equally never write `(i) The criterion is too coarse. (ii) It collapses on the borderline cases.` as one paragraph — the paragraph break is mandatory.
- The same rule applies to other parenthetical enumerators (`(a)`, `(b)`, `(1)`, `(2)`).

**Banned grandstanding / throat-clearing phrases:**
- "study underscores the significance"
- "plays a pivotal role"
- "That being said,"
- "At its core,"
- "most striking"
- "immense", "crucialc", "vital"
- "To put it simply,"
- "This underscores the importance"
- Any of these: Delve/delving, leverage, foster, cultivate, maximize, navigate, enhance, transform, utilize, streamline, "It's worth noting," "in the realm of," "gain insights," "plays a pivotal role," "ensure," "at the intersection of," and "notable figures".
- Any close variant of these.

**Banned register:**
- **Hedging and softening** — "arguably", "perhaps", "it could be said that", "to some extent", "in a sense", "broadly speaking", "more or less", "somewhat". State the claim, or don't.
- **Generic-academic verbs** — "sheds light on", "bolsters", "underscores", "highlights" (in the sense of *makes salient*), "delves into", "explores", "navigates", "grapples with", "speaks to". Use a plain verb that says what actually happens.

The list is illustrative, not exhaustive. The underlying rule: prefer the plain word, the direct claim, the unfussy sentence. If a phrase sounds like it could appear in any essay on any topic, rewrite it.

## Essay Structure Guidelines

### Default Argumentative Structure

Analytic essays survey competing theories, refute them in turn, and arrive at the preferred position last. Default when no outline is given:

```
1. INTRODUCTION
   - State the question / topic
   - Declare the thesis clearly
   - Briefly preview the argumentative direction

2. BACKGROUND
   - Key definitions, distinctions, assumptions
   - Set up the problem precisely

3. THEORY 1 (rejected)
   - Present in strongest form
   - Objection 1 (counterexample, false assumption, etc.)
       → Possible reply (if any)
   - Objection 2
       → Possible reply (if any)
   - Assessment: refuted or seriously contested because of objection(s) X, Y

4. THEORY 2 (rejected)
   - same shape

   [... further theories as needed ...]

5. THEORY N (preferred — always last)
   - Prompt-provided position → that position.
   - Otherwise matched user position → that position UNLESS its `**Usage:**` redirects (in which case Theory N reverts to the analytic-mainstream view and the user's position is woven in per the hint).
   - Otherwise the analytic-mainstream view.
   - Present clearly
   - (Alleged) Objection 1
       → Reply that succeeds in favour of Theory N
   - (Alleged) Objection 2
       → Reply that succeeds in favour of Theory N

6. CONCLUSION (matches the opening)
   - Restate the thesis announced in the opening paragraph as now established.
   - Briefly name the rejected rivals and the decisive reason each fails.
   - Restate the reasons for accepting Theory N.
   - No new arguments. Opening and conclusion are bookends — the same claim, before and after the dialectic.
```

### When to Use This Structure

- **Best**: epistemology, logic, philosophy of language, modern metaethics, any topic with formal competing theories.
- **Less suited**: historical positions, historical ethics — usually need exposition + critical assessment instead.
- **Sometimes**: less formal topics with one theory — collapses to: present, raise objections, assess replies.

### Notes

- **Provided outline or argumentation overrides this default.** When the prompt supplies any laid-out content — from a numbered outline down to a rough narration of the arguments — mirror its structure and inferential moves closely (argument-per-argument where possible). The default applies only when no such content is given. Voice DNA, referencing, and other conventions still apply.
- **Argue rivals honestly.** When Theory N comes from a user position, the rivals must still be presented in their strongest form with genuine objections. Strawmanning a rejected view to make the user's position look easy is the fastest way to lose marks — the examiner profile penalises it.
- **Mirror a loaded position's concreteness.** Position files are written as clear, specific claims with stripped-down reasons. When Theory N comes from a matched position, argue *that* claim in *that* register — do not abstract upward into a more general thesis, soften the verdict, or add flourish the position itself avoids. The closer the prompt sits to the position's stated topic, the tighter the match: land the position's own claim, not a more academic-sounding cousin of it.
- **Not every theory needs the same depth.** A weaker theory can be dispatched briefly; the preferred theory deserves the most careful treatment.
- **Verdicts can be partial.** A rival can be partly right (some claims survive, others fail) — the assessment should say so. Theory N can stand because it is the **least problematic** — fewer or less decisive objections than rivals — not because every objection has a knockdown reply. When that's the honest read, frame the conclusion as preferred-on-balance, not proven; pretending to a clean victory where the dialectic doesn't deliver one looks like strawmanning.
- **Concrete examples from ordinary life** illuminate abstract points where possible.

## Source Resolution

Sources come from three layers. **Layers merge — they do not override.**

1. **Exam prompt (must-read)** — explicit free-text refs in the prompt or chat (e.g. `(Huemer UK 10.4.2)`). Always resolved and read.
2. **Course MD per-module** — `/courses/<course>/index.md` carries:
   - `**Sources:**` — canonical backbone (well-structured texts presenting the canonical arguments). **Always loaded; lead with these.** **If a module lists no Sources, fall back to the canonical analytic position from general knowledge — standard interpretation only, never fabricated quotes, page numbers, or specific arguments.**
   - `**Readings:**` — specific deepening additions on top of the canonical answer. Each Reading typically elaborates an argument that Sources cover in short form. **Loaded when present**; each becomes one branch of argumentation. **If a Reading is unresolvable (book not in `/sources/`) but the named author's position is canonical, invoke their standard view from general knowledge — never hallucinate quotes, page numbers, or specific arguments. When in doubt, omit.**
3. **Book index reverse mode** — `/sources/<book>/index.md`. Two surfaces:
   - `- Source <ref> for <topic>` bullets are **hard**: a topic match means parse `<ref>` and read the section's range as canonical evidence.
   - `**Topics:**` bullets are **soft**: a match flags the chapter as a candidate. Surface to the user with layer-of-origin labelled before reading.

### Format reminders

- **`/sources/catalog.yaml`** is generated; lists books → `index: sources/<slug>/index.md`.
- **`/sources/<book>/index.md`**: frontmatter (`slug`, `title`, `author`, `kind`, `tags`); `## Chapter <N> · <Name>` per chapter with an inline-code metadata line (`cite`, `file`, `format`); `### <ref> <Name> [<a>-<b>]` per section (use `[pp. <a>-<b>]` for PDF). Split-layout books keep section headings in `index-ch<NN>.md`.
- **`/courses/<course>/index.md`**: frontmatter (`slug`, `name`, `style`, `books: [...]`); `## <N>. <Module Name>` per module (numbered 1-10, optional `## 0. Introduction`); optional `**Sources:**`, `**Readings:**`, `**Books:** [override]`. Prompts may reference modules by number or name.

### Resolution algorithm

1. Read `/sources/catalog.yaml` once. If `course:` set, read `/courses/<course>/index.md` and identify in-scope books (frontmatter `books:` plus optional `**Books:**` override under the named module).
2. For each free-text ref: tokenise (author / book / section). Author matches `author` field case-insensitively (surname sufficient). Book matches `title` and `slug` fuzzy ("UK" → "Understanding Knowledge"). Section: most specific dotted number wins (`2.3.4` > `2.3` > `2`); else "ch. N".
3. Open the matched book's `index.md` (or `index-ch<NN>.md` for split layout). Find the section heading whose ref matches; read the trailing range marker. If the requested ref is more specific than the index records, fall back to the closest enclosing heading.
4. **Read only that range**: `Read(path, offset=start, limit=end-start+1)` for MD/TXT/HTML; `Read(path, pages: "<a>-<b>")` for PDF. Never read whole books.
5. Multiple candidates → ask before reading. Cache per session by ref string; cache index reads too.

### Topic-only / under-specified prompts

Aggregate candidates from all three layers — Layer 2 Sources first (always loaded), then Layer 2 Readings, then Layer 3 (Source-bullets hard, Topics-bullets soft, plus chapter prose). Deduplicate, propose to the user with each candidate's layer-of-origin labelled, confirm before reading.

### What NOT to do

- Never read a whole book or whole chapter when a section was named.
- Never load a book's `index.md` if the book is out-of-scope and not explicitly cited.
- Never invent a citation key or section number that the index doesn't have.
- Never fabricate a quote, page number, or specific argument when falling back to general knowledge.
- If a ref is unresolvable, note it in a one-line preface before writing — don't silently drop it.

## Exam-Prompt Format

The prompt is a short markdown document (in `/exam-prompts/<slug>.md` or inline). Template at `/exam-prompts/TEMPLATE.md`.

- Frontmatter: `slug`, `course`, `module`, `length`, `direction`.
- `# Question` — verbatim.
- `# Sources (general)` — optional bullets, free text.
- `# Outline` — optional. Bullets at any level, *or* a rough prose narration of the arguments — anything that lays out how the essay should be argued. Whatever form it takes, it triggers the mirror-the-argumentation rule. Refs in parentheses: `(Huemer UK 10.4.2)`.
- `# Notes for the writer` — optional hints, constraints, positions to avoid.

The skill is liberal in what it accepts. A bare question is treated as a topic-only prompt and uses the three-layer aggregation.

## Process

1. **Understand**: parse question; note any provided outline / position / argument / sources.
2. **Resolve**: read voice + icp; if course set, read positions index and course index; aggregate three source layers; resolve refs; propose candidates if topic-only; read only resolved ranges; note unresolved refs in a one-line preface.
3. **Plan**: identify thesis, theories to reject and order, decisive objections per rejected theory, alleged objections + replies for Theory N. If an outline or laid-out argumentation is provided, plan instead to mirror its moves argument-per-argument (per "Mirroring provided argumentation"); otherwise map to the default structure.
4. **Write**: follow Format, Referencing, Writing Style, Essay Structure Guidelines.
5. **Trim**: count words. If > 1200, cut redundant restatement, over-explained background, and any objection/reply that doesn't change the verdict. Never cut the thesis, the decisive objection on each rejected theory, or the conclusion. Re-count.
6. **Rhythm, structure, and intertwining pass**: scan the essay for failure modes. (a) Any *padding* sentence (rhetorical flourish, restatement, throat-clearing) — cut or merge into adjacent argument. (b) Any run of three or more consecutive short sentences in the "X says A. Y says B. X is wrong." cadence — rewrite to weave attribution into the argument. (c) Any sentence joining two independent clauses with *but*, *because*, *and*, *so*, *yet* that could be split at the connective without breaking the inference — split it (the connective stays at the head of the new sentence). (d) Any paragraph past ~6–8 sentences that contains two argumentative moves — split it. (e) Any semicolon — split into two sentences. (f) Any parenthetical enumeration (`(i)`/`(ii)`/`(iii)`, `(a)`/`(b)`, `(1)`/`(2)`) joined by commas, lower-case continuations, or sharing a paragraph with another marker — rewrite as one sentence and one paragraph per item, each starting with a capital letter and ending with a full stop, with a paragraph break before the next marker. Also check: opening states the thesis explicitly; conclusion bookends it; the essay carries three to five narrative `##` sub-headings or inline "Objection 1: …" / "First, …" markers (not zero, not one per paragraph); no markdown bold or italic anywhere in prose. The test is whether the essay reads as someone *arguing* with visible structure, not as a wall of text.
7. **Save & deliver**: construct path; if no `course:`, reply with one line and stop; if no module, save under `_unfiled/`; overwrite if exists; print to chat; final reply line `Saved to: <path>`.
