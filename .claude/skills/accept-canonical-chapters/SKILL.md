---
name: accept-canonical-chapters
description: Walk an ingested book against its `**Topics:**` blocks (and optionally a course's module vocabulary), propose `- Source <ref> for <topic>` bullets that mark specific sections as the canonical text for a topic, and — when a course is supplied — also propose course-MD updates (`books:` scope, per-module `**Sources:**`). Iterates as a structured plan with the user; applies approved items only on explicit signal. Never emits free-prose annotations, never edits positions, never edits source files.
---

# Accept Canonical Chapters

Turns an indexed book into a curated one. The indexer's `**Topics:**` blocks are a *soft* surface — they say "this chapter mentions X." This skill produces the *hard* surface: `- Source <ref> for <topic>` bullets that authoritatively bind a topic to a specific section, telling the resolver to read that range as canonical evidence whenever the topic matches the prompt.

`Source` marks are load-bearing — a match steers the essay's argumentation toward a specific passage as canonical — so they should be earned, not heuristically generated. This skill is the only path to creating them, and only ever after explicit user approval.

When invoked with a course slug, the skill also proposes the course-MD updates that naturally accompany "this book is canonical for topic X in this course": adding the book to the course's `books:` scope and appending per-module `**Sources:**` entries.

## When to invoke

- "accept canonical chapters in `<book>`"
- "add canonical Source marks to `<book>`"
- "accept canonical chapters in `<book>` against `<course>`" (with course-MD updates)
- After `source-ingestor` and `source-indexer` finish on a new book, when the user wants to commit canonical-status claims
- "back-reference `<book>` for the `<course>` course" (course-aware mode)

## Inputs

Required:
- **book**: slug of an ingested book (e.g. `paradox-lost`). Must exist as `/sources/<book>/index.md`.

Optional:
- **course**: slug of a course (e.g. `logic`). Must exist as `/courses/<course>/index.md`. When supplied, the plan also includes course-MD update proposals (the skill's bucket B). Without a course, only Use-mark proposals are produced (bucket A only).
- **chapters**: chapter numbers to focus on (e.g. `[1, 2, 3]`). Default: all chapters.
- **topics**: topics to focus on (e.g. `["liar", "vagueness"]`). Default: every topic appearing in any in-scope chapter's `**Topics:**` block.

If the book is large, prefer narrowing `chapters` or `topics` over producing a sprawling plan.

### One course per run

Books often span multiple courses. Adding `Source` marks is book-level (a `Source` bullet is not course-scoped), but course-MD updates are course-scoped, and proposing them across multiple courses in one run conflates separate decisions.

When `course` is supplied, **curate against exactly one course per run**. Detect ambiguity up front:

- If the book's frontmatter `tags`, chapter titles, or existing `books:` membership clearly span multiple courses *and* the user has supplied no course, run in book-only mode (bucket A only) and surface the course overlap in the run summary so the user can re-run per course.
- If the user supplied a course but the book also clearly fits another, proceed with the named course but list the deferred ones in the summary.

Detection heuristics — apply before Phase 1:
- Book frontmatter `tags` overlap with multiple courses' frontmatter `tags` or module names.
- Multiple chapter titles in the book's `index.md` align with module topics in different courses.
- The book is already listed in multiple courses' `books:` scope.

## Process

### Phase 1 · Survey

1. Read `/sources/<book>/index.md`:
   - Frontmatter (slug, tags, layout).
   - Chapter list with metadata lines (file, format).
   - Per-chapter `**Topics:**` blocks (the candidate vocabulary — bulleted list under the `**Topics:**` label).
   - Existing `- Source <ref> for <topic>` bullets — never propose duplicates of these.
2. For split-layout books, read each in-scope chapter's `index-ch<NN>.md` to get section headings with line ranges.
3. If `<course>` was supplied, read `/courses/<course>/index.md`: module list (numbered), each module's `**Sources:**` and `**Readings:**`, current frontmatter `books:`. Note any module's existing `**Books:**` override.
4. If `chapters` or `topics` was given, narrow the candidate set accordingly.
5. **Read in-scope sections at line-range granularity** using the indexer's section-heading ranges (`offset` + `limit` for MD/TXT/HTML; `pages` for PDF). Never read whole books or whole chapters when section-level reading suffices.

### Phase 2 · Match

For each in-scope section, ask: **is this section the canonical text for any topic appearing in the chapter's `**Topics:**` block (or, if course given, in any module's vocabulary)?**

Canonical means more than "discusses X" — the section should be (a) a developed argument or definitive treatment, (b) the strongest section in the chapter for that topic (one section per topic per chapter is the typical pattern, occasionally two), and (c) something the user would actually want the resolver to auto-read whenever a prompt mentions the topic.

Track candidates as `(chapter, section ref, topic phrase, rationale)` tuples. A section may be canonical for more than one topic; emit one bullet per `(ref, topic)`. Skip a section if it merely mentions a topic in passing or recapitulates a position covered better elsewhere — log it under bucket C with a one-line reason.

For course-MD proposals (bucket B), separately decide: does the book belong in the course's `books:` scope at all? Do any of the canonical sections fit a specific module's `**Sources:**` list? Use the existing free-text reference style (e.g. "Huemer *Paradox Lost* ch. 3").

### Phase 3 · Build the plan

Produce a structured markdown plan in chat with two or three sections (A, optionally B, and C). Use stable item IDs (A.1, B.2, C.5, etc.) so the user can refer to them when iterating.

```
## Plan: accept canonical chapters in <book>[ ↔ <course>]

### Survey
- Book: <title> by <author>; <N> chapters in scope, <M> existing Source bullets
- Course (if supplied): <name>; <N> modules
- Topics in scope: <comma list> (drawn from per-chapter Topics blocks)

### A. Canonical-chapter Source marks

A.1 Chapter <N> · <Name> — add bullet:
    `- Source <ref> for <topic-phrase>`
    Rationale: <one-paragraph: which passage in §<ref> backs the canonical claim, why this section over neighbours>

A.2 Chapter <N> · <Name> — add bullet:
    ...

### B. Course MD updates  (omitted if no <course>)

B.1 Add `<book-slug>` to /courses/<course>/index.md frontmatter `books:`
B.2 Module <M> · <Module Name>: append `<free-text ref>` to **Sources:**
    Rationale: <which canonical sections back this addition>

### C. Considered, no action

C.1 §<ref> <heading> — <one-line reason>: e.g. "passing mention only", "covered better by §<other-ref>", "topic not in any chapter's Topics block"

---

Reply with:
- "execute" / "go" / "apply" → apply all items
- "accept A, B; drop C; revise A.2" → partial accept
- specific edits ("in A.1, change topic phrase to 'Sorites'"; "add a bullet under A for §3.6") → revise the plan
- "stop" → exit without applying
```

If the plan would be very long (>20 items), summarise section C and offer to expand on request.

### Phase 4 · Iterate

Stay in proposal mode. After each user reply:

- **Execute signal** ("execute", "go", "apply", "do it") → move to Phase 5 with the currently approved set.
- **Modification** ("drop A.2", "rewrite A.1 as ...", "add an item for §3.6") → update the plan, re-print only the changed items unless the change is structural.
- **Question** ("what does §3.6 actually say about X?") → answer from the source (read only the section's range), leave the plan unchanged, re-prompt.
- **Stop signal** ("stop", "cancel", "leave it") → exit without applying.

Never apply changes without an explicit execute signal.

### Phase 5 · Execute

Apply the approved items in this order:

1. **Book index** (`/sources/<book>/index.md`)
   - For each approved A item: insert the bullet under the matching `## Chapter <N> · <Name>` block, after the entire `**Topics:**` block (the label plus all its `- <topic>` bullets). If the chapter already has Source bullets, append in section-ref order. Never duplicate an existing `(ref, topic-phrase)` pair (case-insensitive on the topic phrase).
   - Never modify chapter headings, metadata lines, frontmatter, prose, the `**Topics:**` block (label or its bullets), section headings, or range markers. Source marks are the only writable target.

2. **Course MD** (`/courses/<course>/index.md`) — only if `<course>` was supplied
   - For B items adding the book to `books:`: edit the frontmatter list. Append the slug if not already present. Preserve list style (inline `[a, b]` or block).
   - For B items appending to `**Sources:**`: locate the matching `## <M>. <Module Name>` block; append a new bullet at the end of that module's `**Sources:**` list. If the module has no `**Sources:**` block at all, add one. Use the user's free-text reference style (e.g. "Huemer *Paradox Lost* ch. 3").
   - Never touch other modules, `**Readings:**`, `**Essay scope:**`, `**Usage:**`, or module prose.

After execution, report:
- Files changed (paths)
- Items applied per section (counts)
- Items deferred or dropped (counts, with brief reasons)
- **Other courses to consider** — if cross-course overlap was detected at input time, list the deferred courses by slug with one-line summaries of the chapters that fit them.

## What this skill does NOT do

- Never ingests new sources (that's `source-ingestor`).
- Never re-derives section ranges or modifies the structural skeleton of the book index (that's `source-indexer`).
- Never edits source files (`/sources/<book>/<chapter>.*`).
- Never writes prose annotations under section headings (Source bullets are the only authoritative annotation surface).
- Never edits `**Topics:**` blocks (that's the indexer's surface).
- Never edits `/positions/*/` (that's `accept-canonical-positions`).
- Never writes essays.
- Never applies any item without explicit user approval.
- Never spans multiple courses in one run.

## Implementation notes

- Use the section ref (e.g. `3.5.7`) as the stable identifier when matching candidates to existing bullets and when writing new ones — heading text can drift, refs cannot.
- Read sparingly: use `index.md` (or `index-ch<NN>.md`) line ranges to load only relevant sections.
- A section being canonical for a topic does NOT mean other sections can't also discuss it. The bar is "the resolver should auto-read this when the topic matches" — typically one or two sections per topic per book.
- Topic-phrase casing: lowercase except for proper nouns (`Hume`, `Bayes`, `Wittgenstein`, `T-schema`) and acronyms. Match the casing already used in the chapter's `**Topics:**` block where possible.
- If a candidate topic doesn't appear in any chapter's `**Topics:**` block and no course is supplied, do not propose it — the indexer's Topics block is the gate. With a course supplied, course-vocabulary terms can override this gate (the user can later regenerate Topics for the chapter via the indexer).
- The plan lives in chat. If the user wants to defer for a session, they can ask for the plan to be saved to a temp file.
- When proposing course-MD `**Sources:**` additions, prefer the per-module list whose topic the section actually matches; do not blanket-add the book to every module.
