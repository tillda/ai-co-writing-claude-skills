---
name: accept-canonical-positions
description: Walk an ingested book against an existing course's modules and the user's positions for that course (in /positions/<course>/), and propose two things via an approval loop: (1) strengthening or refining existing positions with new passages, and (2) new positions for course-module topics where the user has not yet stated a stance. Applies approved items only on explicit signal. Never edits the book index, course MD, or source files.
---

# Accept Canonical Positions

Bridges an ingested book into the user's stated philosophical stances for a course. Positions are authoritative — when an essay prompt is silent on direction, the matched position becomes the conclusion the essay must argue toward — so committing to one is a real argumentative commitment, not a casual annotation.

This skill proposes position changes; the user approves; the skill applies. Nothing else.

## When to invoke

- "accept canonical positions in `<book>` for the `<course>` course"
- "update my `<course>` positions based on `<book>`"
- "match `<book>` with my `<course>` positions"
- After `accept-canonical-chapters` has finished, when the user is ready to also commit positions

## Inputs

Required:
- **book**: slug of an ingested book (e.g. `paradox-lost`). Must exist as `/sources/<book>/index.md`.
- **course**: slug of a course (e.g. `logic`). Must exist as `/courses/<course>/index.md`. Exactly one course per run — positions are course-scoped, and proposing across multiple courses in one run conflates separate position files and separate argumentative directions.

Optional:
- **chapters**: chapter numbers to focus on (e.g. `[1, 2, 3]`). Default: all chapters.
- **topics**: topics or position names to focus on (e.g. `["liar", "vagueness"]`). Default: all positions + all module topics.

If the book is large or the course has many modules, prefer narrowing `chapters` or `topics` over producing a sprawling plan.

### One course per run

If the book plausibly spans several courses *and* `course` is missing, **stop and ask** which course to curate against now, before any survey work. Show the candidate courses with the book's apparent overlap (e.g. "Ch. 6–8 fit *epistemology*, Ch. 13–17 fit *intro-to-philosophy*"). The user picks one. The others are deferred to separate runs.

Detection heuristics — apply before Phase 1:
- Book frontmatter `tags` overlap with multiple courses' frontmatter `tags` or module names.
- Multiple chapter titles in the book's `index.md` align with module topics in different courses.
- The book is already listed in multiple courses' `books:` scope.

If any trigger fires and `course` was supplied but other courses also clearly match, surface the cross-course coverage to the user briefly so they can decide whether the deferred course needs its own run later.

## Process

### Phase 1 · Survey

1. Read `/sources/<book>/index.md`:
   - Frontmatter (slug, tags).
   - Chapter list with metadata lines.
   - Per-chapter `**Topics:**` lines and `- Use <ref> for <topic>` bullets — these are the candidate topic surface. Use bullets are particularly informative: they tell you which sections the user has already committed to as canonical.
2. Read `/courses/<course>/index.md`: module list (numbered), per-module `**Sources:**` and `**Readings:**`, any module-level prose, frontmatter `books:`, optional `**Essay scope:**` and `**Books usage:**` blocks (read for context; never edit).
3. Read `/positions/<course>/index.md` if it exists: the catalog of existing positions and their `**Applicable to:**` triggers (denormalized in the index). For each candidate position, open the named position file (`/positions/<course>/<slug>.md`) for the body. If the directory does not exist yet, treat the course as having no stated positions.
4. If `chapters` or `topics` was given, narrow accordingly.
5. Read in-scope chapters at section granularity using line ranges from the book's `index.md` (or `index-ch<NN>.md` for split layout). Prioritise sections that already carry `Use` bullets — those are the user's flagged-as-canonical passages. Never read whole books or whole chapters when section-level reading suffices.

### Phase 2 · Match

For each in-scope chapter/section, classify against three buckets:

- **The user's existing positions** — does the passage strengthen, refine, or supply objections to a position the user has stated for this course? Frame the change as a diff: what specifically gets added (new evidence, new objection, sharpening a clause), what gets softened, what stays.
- **Module topics without a stated position** — does the passage fit a course-module topic where the user has *no* stated position? Candidate for a new position.
- **Out of scope** — neither.

**Do not propose new positions casually.** Every accepted position becomes an authoritative stance the user is committing to. A new position is appropriate only when:
1. The book offers a developed argument on the topic (not just a passing mention).
2. The topic appears in a course module.
3. No existing position triggers on the topic.
4. The user is likely to actually defend the position in essays.

If the proposed position would be a single sentence or just "I agree with X", prefer to fold it into an existing position or skip it.

### Phase 3 · Build the plan

Produce a structured markdown plan in chat with three sections (A, B, C). Use stable item IDs.

```
## Plan: accept canonical positions in <book> ↔ <course>

### Survey
- Book: <title> by <author>; <N> chapters in scope
- Course: <name>; <N> modules
- Positions file: <found / not found>; <N> existing positions

### A. Position updates (the user's existing positions)

A.1 <Position Name> — strengthen with <book ch/§ refs>
    Change: <one-paragraph diff: what's added, what's softened, what stays>
    Rationale: <which passages support this; quote 1-2 keywords/phrases>

A.2 <Position Name> — add objection-handling on <topic>
    ...

### B. New positions proposed (commit the user to a new stance)

B.1 <Draft Position Name> (covers module <N> · <topic>)
    Body draft:
        <2–4 sentences capturing the position>
    Applicable to: <trigger keywords/phrases>
    Rationale: <why this gap matters; which passages back it>

### C. Considered, no action

C.1 §<ref> — <reason for skipping>: e.g. "passing mention only", "topic not in any course module", "covered by existing position A.1"

---

Reply with:
- "execute" / "go" / "apply" → apply all items
- "accept A; drop B.1; revise A.2" → partial accept
- specific edits ("in B.1, soften the X claim"; "add an item under A for §3.6") → revise the plan
- "stop" → exit without applying
```

If the plan would be very long (>20 items), summarise section C and offer to expand on request.

### Phase 4 · Iterate

Stay in proposal mode. After each user reply:

- **Execute signal** ("execute", "go", "apply", "do it") → move to Phase 5 with the currently approved set.
- **Modification** ("drop A.2", "rewrite B.1 as ...", "add an item for §3.6") → update the plan, re-print only the changed items unless the change is structural.
- **Question** ("what does §3.6 actually say about X?") → answer from the source (read only the section's range), leave the plan unchanged, re-prompt.
- **Stop signal** ("stop", "cancel", "leave it") → exit without applying.

Never apply changes without an explicit execute signal. Silence or off-topic replies hold the plan; they do not approve it.

### Phase 5 · Execute

Apply the approved items in this order:

1. **Position updates** (A items)
   - Edit the existing position file (`/positions/<course>/<slug>.md`): apply the body diff, update the trailing `**Applicable to:**` line if the proposal added triggers. Frame edits as targeted insertions or replacements; do not reflow paragraphs that aren't changing.
   - Update the denormalized `**Applicable to:**` line under that position's heading in `/positions/<course>/index.md` to match.

2. **New positions** (B items)
   - For each: write a new file `/positions/<course>/<slug>.md` (slug = kebab-case of the position name; drop parenthetical disambiguators) with:
     - Frontmatter: `course: <slug>`.
     - H1: the position name.
     - Body: the approved draft prose.
     - Trailing `**Applicable to:**` line: the approved trigger list.
     - Optional `**Usage:**` line: only if the user explicitly approved one (the default conclusion-role behaviour applies otherwise).
   - Append a new entry under `/positions/<course>/index.md`: a `## <Name>` heading, a `` `file: <slug>.md` `` line, and the denormalized `**Applicable to:**` line.

3. **Bootstrap if needed**
   - If `/positions/<course>/` does not exist and B has approved items, create it. Seed `index.md` with frontmatter `course: <slug>`, the standard intro paragraph (theory-rejection guidance — match the prose used in other positions indexes for consistency), then append per-position entries.

After execution, report:
- Files changed (paths)
- Items applied per section (counts)
- Items deferred or dropped (counts, with brief reasons)
- **Other courses to consider** — if cross-course overlap was detected at input time, list the deferred courses by slug with one-line summaries of the chapters that fit them.

## What this skill does NOT do

- Never edits `/sources/<book>/index.md` or `/sources/<book>/index-ch<NN>.md` — that's `accept-canonical-chapters` (Use marks) or `source-indexer` (structure / Topics).
- Never edits source files (`/sources/<book>/<chapter>.*`).
- Never edits `/courses/<course>/index.md` — that's `accept-canonical-chapters` (when a course is supplied) or hand-editing.
- Never writes essays.
- Never applies any item without explicit user approval.
- Never spans multiple courses in one run.

## Implementation notes

- Use the section ref (e.g. `3.5.7`) as the stable identifier when citing book passages in rationales — heading text drifts, refs don't.
- Frame position updates as diffs ("strengthen X by adding Y", "soften the Z claim") rather than full rewrites — the user can see what's actually changing.
- Read sparingly: load only the section ranges you need to argue the case.
- New positions are theory-rejection-shaped: the position is *defensible* against rivals, not just sympathetic to one author. The body should signal which rivals the position rejects and on what grounds, even in a 2–4 sentence draft.
- Sections already flagged with `Use` bullets in the book index are particularly strong evidence for position updates — they're the user's curated canonical passages.
- Match prose style to the existing positions in `/positions/<course>/` — read one or two before drafting B items so the voice is consistent.
- The plan lives in chat. If the user wants to defer for a session, they can ask for the plan to be saved to a temp file.
