---
name: curate-source
description: After a book is ingested into /sources/, walk it against the user's positions for a course (in /context/positions-<course>.md) and the course's module topics, and propose three things: (1) updates to the user's positions, (2) authoritative back-reference annotations to add under section headings in /sources/<book>/index.md — these prescribe the required line of argument when matched at essay time (layer-3 / reverse-mode), (3) course-MD updates (`books:` scope, per-module `**Sources:**` lists). Produces a structured plan the user iterates on, then applies the approved items only on explicit signal.
---

# Curate Source

Bridges an ingested book into the writing system. Ingestion (source-ingestor + source-indexer) leaves a book filed and structurally indexed, but the *judgement* layer — which of the user's positions to update, which sections to back-reference, which modules to scope it into — is curation, and that's what this skill proposes.

Both outputs are **authoritative**, not advisory:
- A **position** in `/context/positions-<course>.md` is the user's stated stance for the course; when an essay prompt is silent on direction, the matched position is the conclusion the essay must argue toward.
- A **back-reference annotation** under a section heading in `/sources/<book>/index.md` prescribes the line of argument when the resolver matches it at essay time. It is not a "passage worth citing" hint — it is a binding directive, written in the user's voice, that commits the essay to a particular argumentative course.

The skill never auto-applies. It surveys, proposes a plan, iterates with the user, and executes only on explicit approval — because every accepted item commits the user to an argumentative line that future essays will follow.

## When to invoke

- "curate <book> against the <course> course"
- After source-ingestor finishes, when the user wants to integrate the book's content
- "update my <course> positions based on <book>"
- "back-reference <book> to <course> topics"
- "match <book> with my <course> positions"

## Inputs

Required:
- **book**: slug of an ingested book (e.g. `paradox-lost`). Must exist as `/sources/<book>/index.md`.
- **course**: slug of a course (e.g. `logic`). Must exist as `/courses/<course>/index.md`.

Optional:
- **chapters**: chapter numbers to focus on (e.g. `[1, 2, 3]`). Default: all chapters in the book.
- **topics**: topics or position names to focus on (e.g. `["liar", "vagueness"]`). Default: all positions + all module topics.

If the book is large or the course has many modules, prefer narrowing `chapters` or `topics` over producing a sprawling plan.

### Curate one course per run

Books often span multiple courses (a general philosophy text might cover epistemology, ethics, metaphysics, free will, etc.). Curating against more than one course in a single run conflates separate position files, separate module structures, and separate argumentative directions, producing a sprawling plan that's hard to iterate on.

The skill therefore curates **exactly one course per run** and detects ambiguity up front:

- If `course` is unambiguous (only one plausible match), proceed.
- If `course` is missing or the book plausibly spans several courses, **stop and ask** which course to curate against now, before any survey work. Show the candidate courses with the book's apparent overlap (e.g. "Ch. 6–8 fit *epistemology*, Ch. 13–17 fit *intro-to-philosophy*"). The user picks one. The others are deferred to separate runs.

Detection heuristics for cross-course relevance — apply before Phase 1:
- Book frontmatter `tags` overlap with multiple courses' frontmatter `tags` or module names.
- Multiple chapter titles in the book's `index.md` align with module topics in different courses.
- The book is already listed in multiple courses' `books:` scope.

If any of these triggers fire and `course` was not supplied (or was supplied but other courses also clearly match), pause and ask. Do not silently scope to the named course when a single chapter spans elsewhere — surface the cross-course coverage to the user briefly so they can decide whether the deferred course needs its own run later.

## Process

### Phase 1 · Survey

1. Read `/sources/<book>/index.md` — frontmatter (tags), chapter list, any existing prose under chapter/section headings (prior annotations).
2. Read `/courses/<course>/index.md` — module list, frontmatter `books:`, per-module `**Sources:**` and `**School Readings:**`, any module-level prose.
3. Read `/context/positions-<course>.md` if it exists — for each position: name, body, `**Applicable to:**` triggers.
4. If `chapters` or `topics` was given, narrow accordingly.
5. Read in-scope chapters at section granularity using line ranges from the book's `index.md` (`offset` + `limit` for MD/TXT/HTML; `pages` for PDF). Never read whole books or whole chapters when section-level reading suffices.

### Phase 2 · Match

For each in-scope chapter/section, classify against three buckets:

- **The user's existing positions** — does the passage strengthen, refine, or supply objections to a position the user has stated for this course?
- **Module topics without a stated position** — does the passage fit a course-module topic where the user has not yet stated a position (candidate for a *new* user position)?
- **Out of scope** — neither.

For each existing position, identify candidate book passages. For each module without coverage, identify candidate passages. Track unmatched passages as "considered, no action".

Do not propose new positions casually — every accepted position becomes an authoritative stance the user is committing to. A new position is appropriate only when (a) the book offers a developed argument on the topic, (b) the topic appears in a course module, (c) no existing position triggers on that topic, and (d) the user is likely to actually defend the position in essays. If the proposed position would be a single sentence or just "I agree with X", prefer to fold it into an existing position or skip it.

### Phase 3 · Build the plan

Produce a structured markdown plan in chat with five sections (A–E). Use stable item IDs (A.1, B.2, C.5, etc.) so the user can refer to them when iterating.

```
## Plan: curate <book> ↔ <course>

### Survey
- Book: <title> by <author>; <N> chapters in scope
- Course: <name>; <N> modules
- Positions file: <found / not found>; <N> existing positions

### A. Position updates (the user's existing positions)

A.1 <Position Name> — strengthen with <book ch/§ refs>
    Change: <one-paragraph diff or summary; what's added, what's softened>
    Rationale: <which passages support this>

### B. New positions proposed (commit the user to a new stance)

B.1 <Draft Position Name> (covers module <N> · <topic>)
    Body draft:
        <2–4 sentences capturing the position>
    Applicable to: <trigger list>
    Rationale: <why this gap; which passages back it>

### C. Book index back-references (directive — prescribe the line of argument)

C.1 §<ref> <heading> — <annotation prose>

### D. Course MD updates

D.1 Add `<book-slug>` to /courses/<course>/index.md frontmatter `books:`
D.2 Module <N>: add `<source ref>` to **Sources:**

### E. Considered, no action

E.1 §<ref> — <reason for skipping>

---

Reply with:
- "execute" / "go" / "apply" → apply all items
- "accept A, C; drop B; revise D.2" → partial accept
- specific edits ("in A.1, soften the X claim"; "add an item under C for §3.6") → revise the plan
- "stop" → exit without applying
```

If the plan would be very long (>20 items), summarise sections D and E and offer to expand them on request.

### Phase 4 · Iterate

Stay in proposal mode. After each user reply:

- **Execute signal** ("execute", "go", "apply", "do it") → move to Phase 5 with the currently approved set.
- **Modification** ("drop A.2", "rewrite B.1 as ...", "add an item for §3.6") → update the plan, re-print only the changed items unless the change is structural.
- **Question** ("what does §2.5 actually say about X?") → answer from the source, leave the plan unchanged, re-prompt.
- **Stop signal** ("stop", "cancel", "leave it") → exit without applying.

Never apply changes without an explicit execute signal. Silence or off-topic replies hold the plan; they do not approve it.

### Phase 5 · Execute

Apply the approved items in this order:

1. **Positions file** (`/context/positions-<course>.md`)
   - For position updates: edit the existing position's body and `**Applicable to:**` line.
   - For new positions: append at the end of the file using the standard structure (heading, body, argumentative path bullets if appropriate, `**Applicable to:**` line).
   - If the file does not exist and B has approved items, create it with course frontmatter (`---\ncourse: <slug>\ngenerated: <today>\n---`) and the standard intro paragraph from existing positions files.

2. **Book index** (`/sources/<book>/index.md`)
   - Insert each approved annotation as a paragraph between the section heading line and the next heading.
   - If a section already has prose, propose a *refinement* rather than appending — do not stack annotations.
   - Never modify the structural skeleton (heading text, range markers, frontmatter). For range refresh, run source-indexer.

3. **Course MD** (`/courses/<course>/index.md`)
   - For `books:` additions: append the new slug to the frontmatter list if not already present.
   - For `**Sources:**` additions: append a new bullet at the end of the relevant module's `**Sources:**` list. Use the user's free-text reference style (e.g. "Huemer *Paradox Lost* ch. 3").

After execution, report:
- Files changed (paths)
- Items applied per section (counts)
- Items deferred or dropped (counts, with brief reasons)
- **Other courses to consider** — if cross-course overlap was detected at input time, list the deferred courses by slug with one-line summaries of the chapters that fit them, so the user can run the skill again per course without re-discovering the overlap.

## What this skill does NOT do

- Never ingests new sources (that's source-ingestor).
- Never edits source MD/PDF/HTML files in `/sources/<book>/<chapter>.*`.
- Never modifies the structural skeleton of `/sources/<book>/index.md` (headings, range markers, frontmatter) — only inserts prose under existing headings.
- Never writes essays (that's essay-philosophy).
- Never applies any item without explicit user approval.
- Never spans multiple courses or multiple books in one run — scope is the named (book, course) pair.

## Implementation notes

- For section-level matching, use the section ref (`3.5.7`) as the identifier. Heading text can be lightly rewritten by the user; refs are stable.
- Read sparingly: use `index.md` line ranges to load only relevant sections.
- Frame position updates as diffs ("strengthen X by adding Y", "soften the Z claim") rather than full rewrites — the user can see what's actually changing.
- Annotations are directive: when the resolver matches them at essay time, the essay must follow the line of argument they prescribe. Write in the user's voice with exam-language keywords (the strings the resolver fuzzy-matches), and state the argumentative course plainly. Bad: "interesting discussion of vagueness". Good: "Use for *positions-<course>.md / Sorites Paradox* — argue Huemer's moderate nihilism: vague sentences fail to express propositions; classical logic preserved by restricting scope. Reject supervaluationism (T-schema), epistemicism (no fact fixes the cutoff), deviant logic."
- If a section in the book index already carries prose, treat existing prose as authoritative; propose refinement only.
- The plan lives in chat, not on disk. If the user wants to defer for a session, they can ask for the plan to be saved to a temp file.
- When proposing additions to a course's `**Sources:**` list, prefer the per-module list whose topic the passage matches; do not blanket-add the book to every module.
