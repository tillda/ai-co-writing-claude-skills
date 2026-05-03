---
name: prepare-course
description: Build or refresh `/courses/<slug>/index.md` from the course directory's syllabus document and exam-question bank. The course index is a topic-keyed lookup table the essay resolver matches against — topic bullets must be clean noun-phrase labels (matching keys), not sentences or descriptions. Use when adding a new course, when a syllabus PDF is dropped into `/courses/<slug>/`, or when the user says the existing course index is out of date or too verbose.
---

# Prepare Course

Builds the per-course `index.md` from raw course materials sitting in `/courses/<slug>/` — typically a study-guide PDF (the syllabus) and a markdown file of past exam questions. The course index is *not* a study guide for a human reader; it is a topic-keyed lookup table the resolver matches against an essay prompt to decide what sources and readings to load. Treat every line accordingly.

## When to invoke

- "prepare/build the &lt;course&gt; course index"
- "redo the &lt;course&gt; index from the syllabus"
- A syllabus PDF + exam-questions MD have just been dropped into `/courses/<slug>/`
- The user says "the index is too verbose / too sparse / out of date"
- After the user adds or revises an exam-questions file

The skill never edits the syllabus or the exam-questions file. It only writes `/courses/<slug>/index.md`.

## Inputs the skill discovers

In `/courses/<slug>/` the skill looks for:

- **Syllabus / study guide.** A PDF or MD that defines the chapter (= module) structure, gives canonical readings at the top of each chapter (if any), and supplies a master bibliography. Common names: `*Study Guide*.pdf`, `syllabus.md`, `<CODE> Study Guide.pdf`.
- **Exam questions file.** An MD file listing past exam questions, usually grouped by year. Common names: `*Exam Questions*.md`, `questions.md`, `past-papers.md`. May begin with a list of canonical modules — if so, prefer that list over inferring from the syllabus.
- **Existing `index.md`** — if present, refresh mode (see below).

If the directory has neither a syllabus nor an exam questions file, stop and ask. The skill cannot fabricate course structure.

## Output shape

```markdown
---
slug: <course-slug>
name: <Course Name (CODE)>
code: <CODE>
style: analytic | continental | mixed
books: [<book-slug>, ...]
---

# <Course Name (CODE)>

<one short paragraph of course-level orienting context: where the syllabus comes from, how to read the index, any course-wide scope/usage hints. No more than ~5 sentences.>

## 0. <Module name>

**Topics:**

- topic
- topic
- topic

**Sources:**

- canonical source 1
- canonical source 2

**Readings:**

- reading 1
- reading 2
```

That is the entire shape. There is **no prose paragraph between the H2 module heading and `**Topics:**`** — the topic list is the module description. If a cross-reference or scope note is genuinely needed, place it as a parenthetical inside a bullet, not as a leading paragraph.

`**Sources:**` and `**Readings:**` are optional per module. Omit the block entirely if empty (do not write an empty heading).

## Topic-bullet shape rules

A topic bullet is a **matching key** for the resolver. Not a sentence, not a question, not a syllabus blurb. Treat each bullet as a tag that an essay prompt might fuzzy-match.

### Required form

- **Noun phrase**, not sentence. ✅ `Truth as a property` / `Truth as predicate`. ❌ `When we say a statement is true, are we attributing the property of truth to it?`
- **Concise** — typically 2–5 words; single-word bullets OK for established philosophical terms (`Deflationism`, `Supervaluationism`, `Sorites`). Maximum ~7 words.
- **Lowercased** except for proper nouns and standard capitalised technical terms (`de re/de dicto`, `Russell's theory of descriptions`, `Frege's puzzle`, `LEM`).
- **Italicise** Latin and stylistic conventions where the philosophical literature does (`*de re*`, `*a priori*`).
- **No `—` followed by an explanation.** If you find yourself wanting to add an em-dash with a clause, you are describing rather than labelling. Split into a separate topic, or drop the elaboration.
- **No exam-year tags** in bullets by default. The exam questions file is the source of truth for "what's been asked"; duplicating it inside the index drifts.
- **No star-ratings** by default. If frequency-of-asking matters, the user can add stars manually after the fact.

### Naming conventions

- Use the **canonical philosophical term** the literature uses. Prefer `de re/de dicto` over `the distinction between de re and de dicto necessity`. Prefer `material conditional` over `'→' as the meaning of "if"`.
- **Eponymous attribution** is fine when it's the standard term: `Russell's theory of descriptions`, `Frege's puzzle`, `Lewis's counterpart theory`, `Kripke's necessary aposteriori`, `Quine on analyticity`, `Carroll's tortoise`.
- **Paradox / argument names** — keep as the literature has them: `Liar paradox`, `Sorites paradox`, `Tarski's T-schema`, `Adams thesis`, `Lewis bombshell`.
- **Cross-reference parentheticals are OK** when a topic genuinely lives in two modules: `- rigid designation (cross-reference Module 8)`. Keep them short.

### Granularity

A bullet should be specific enough to match a question, generic enough to match more than one phrasing.

- ✅ `Liar paradox` — matches "What is the Liar paradox?", "What does the Liar tell us about truth?", "Best solution to 'this sentence is false'".
- ❌ `Tarskian language-hierarchy as Liar response` — too specific; this is a *sub-topic of* `Liar paradox`. The essay-philosophy skill will pick up Tarskian responses when writing about the Liar.
- ❌ `Truth` — too generic; matches everything in the Truth module. Split into the actual themes (`deflationism`, `correspondence`, `Liar paradox`, `Tarski's T-schema`, `bivalence vs LEM`, `truth as property`).

When in doubt, ask: would an exam prompt actually phrase this? If the bullet sounds like an essay topic at the right grain, keep it. If it sounds like an essay paragraph, it's too narrow.

### One bullet per topic

- **Don't conjoin** with semicolons or "and". `- deflationism, redundancy theory, minimalism` should be three bullets, not one.
- **De-duplicate aggressively.** A topic that fits two modules belongs in the more natural one, with a parenthetical cross-reference from the other.

## Sources vs Readings

Use the same convention used elsewhere in this repo:

- **Sources** — the canonical backbone the essay-philosophy skill leads with. Bulletted list of texts the syllabus *names as required reading at the top of the chapter*. If the syllabus does not name a canonical source for a chapter, omit the `**Sources:**` block entirely — do not invent one. Also: a layperson-introductory book in the user's library may legitimately serve as a Source if the syllabus's bibliography references it as canonical for that chapter.
- **Readings** — deepening additions: each typically elaborates one branch of an argument. Drawn from the syllabus's master bibliography and from any sub-section reading lists. Aim for the items the syllabus explicitly cites in the chapter body, not every entry in the bibliography.

Each Source / Reading bullet is precise: **author, exact title, venue, year**. No "X on Y" placeholders. Expand abbreviations: write `(Stanford Encyclopedia of Philosophy)` not `(SEP)`. Use bullet lists, not prose.

## Module structure

Modules are H2s, numbered. Use `## <N>. <Name>` (with optional `## 0. Introduction`). The numbering follows the syllabus's chapter numbers. If the exam-questions file lists modules with explicit numbers, prefer that numbering.

Module names should match the syllabus chapter titles (close paraphrase OK). Do not invent modules; do not merge or split syllabus chapters unless the user explicitly asks.

## Process

### Phase 1 · Read inputs

1. List `/courses/<slug>/`. Identify the syllabus file and the exam-questions file (if both exist).
2. If the syllabus is a PDF, read it page-by-page (use the PDF tool's `pages` parameter; do not load the whole PDF blindly). Pull: chapter titles + numbers, sub-section headings, any "Reading"/"Readings" header at the top of each chapter, the master bibliography (usually at the end of the introduction).
3. If the syllabus is markdown, read it directly.
4. Read the exam-questions file end-to-end. Note any explicit module list at the top — if present, that is the canonical module structure.
5. If `/courses/<slug>/index.md` already exists, read it for frontmatter (`books:`, `style:`) and any user-authored prose to preserve.

### Phase 2 · Determine module structure

- Modules = the syllabus's chapters, plus a Module 0 for the syllabus's introductory chapter if it covers material the user wants captured (validity, monotonicity, etc.).
- If the exam-questions file declares an explicit module list and it diverges from the syllabus, surface the divergence to the user before proceeding. Default to the exam-questions list when both are consistent.

### Phase 3 · Identify canonical sources per module

For each chapter in the syllabus:

- Look at the very top of the chapter for a `Reading` or `Readings` header. The items listed there are canonical; they go into `**Sources:**`.
- Sub-section `Readings` headers (within a chapter) feed into `**Readings:**`, not `**Sources:**`.
- The master bibliography supplies further `**Readings:**` items — but only those the chapter body actually cites or that clearly bear on the chapter's topics.
- If no canonical Reading is listed at the top of a chapter, omit the `**Sources:**` block. A layperson-introductory companion book (if the user has one) may be promoted to `**Sources:**` only when the syllabus's bibliography explicitly recommends it as a chapter-level reference.

### Phase 4 · Cluster exam questions to modules

For every question in the exam-questions file:

1. Identify the topic(s) the question probes (often more than one — a question on possible worlds may also touch *de re/de dicto*).
2. Place each topic under its natural module.
3. Some questions clearly belong to a sister course (epistemology, philosophy of science, perception). Skip those rather than forcing them into a logic-style module.

The output of this phase is a per-module set of topic candidates drawn from the question bank.

### Phase 5 · Synthesise topic bullets

For each module:

- Combine: (a) topics inferred from the syllabus's section headings, (b) topics extracted from the exam-questions clustering.
- Reduce each candidate to its **clean label** per the topic-bullet shape rules above.
- De-duplicate. Order from most central to most peripheral (intuitive reading order; no formal rank).
- Aim for completeness: every distinct theme that has been asked about in the question bank should appear as some bullet in some module.

### Phase 6 · Write the index

Compose the file using the output shape above. Hard rules:

- No prose paragraph between the H2 module heading and `**Topics:**`.
- Topic bullets follow the shape rules strictly.
- Sources and Readings blocks are precise and bulleted (never inline prose).
- Frontmatter `books:` is preserved from any existing index, or asked from the user if missing.

### Phase 7 · Validate

Before finishing, scan the produced file:

- Every module H2 is numbered and ordered.
- Every `**Topics:**` block is a non-empty unordered list.
- No topic bullet contains an em-dash followed by a sentence-length clause.
- No topic bullet ends with a question mark or a period (indicating a sentence).
- Every Source/Reading bullet has author + title at minimum.
- No `(SEP)` or other abbreviated venue names.
- The file ends without trailing whitespace.

Report at the end: number of modules, total topics, any modules where the question bank suggests topics not yet captured.

## Refresh mode

If `/courses/<slug>/index.md` already exists:

- **Preserve** the user's frontmatter (`books:`, `style:`), the H1 intro paragraph, any `**Essay scope:**` or `**Usage:**` blocks at the top.
- **Refresh** topic lists per the latest syllabus + exam-questions content.
- Leave hand-written `**Sources:**` / `**Readings:**` lists untouched unless the user explicitly asks for them to be regenerated. The user often curates these.
- If the existing index has prose paragraphs under module headings (the legacy verbose format), drop them — that is part of the cleanup the skill exists to do — but show the user a brief diff so nothing material is lost.

## What this skill does NOT do

- Never edits the syllabus PDF or the exam-questions file.
- Never writes positions, essays, or notes into `/positions/` or elsewhere.
- Never adds books to `/sources/` or modifies `/sources/catalog.yaml` (that is `source-ingestor` / `source-indexer`).
- Never invents modules, topics, sources, or readings that the input materials do not support. When in doubt, ask the user.
- Never adds star ratings, exam-year tags, or "use this module for…" prose to topic bullets unless the user explicitly asks.

## Worked example (excerpt)

Bad (verbose, sentence-shaped, year-tagged):

```markdown
## 2. Truth

The Liar paradox, Tarski's T-schema, deflationism, correspondence... Use for any prompt mentioning 'true', the property of truth, the redundancy theory, the Liar...

**Topics:**

- ★★★ Deflationism — disquotationalism (Tarski's schema as exhausting the notion), minimalism (Horwich), the redundancy theory (Ramsey); whether 'true' has a valuable expressive role without standing for any property; whether this can be justified (2022 + many supplementary)
- ★★★ Truth as a property — when we say a statement is true, are we attributing the property of truth to it; if 'true' does not pick out a property in any robust sense, what role does the predicate play (2022 + many supplementary)
```

Good (clean, label-shaped):

```markdown
## 2. Truth

**Topics:**

- truth as property
- truth as predicate
- deflationism
- disquotationalism
- minimalism
- redundancy theory
- correspondence
- Liar paradox
- Tarski's T-schema
- bivalence vs LEM
- pragmatism, coherence, identity theories
- Frege on truth as the goal of logic
- factivity of knowledge (cross-reference epistemology)
```
