# Architecture Reference

Reference doc for the philosophy-essay system. CLAUDE.md is the operating manual loaded every turn; this file is consulted only when something there is unclear, or when authoring/maintaining structured files (positions, course MDs, book indexes).

---

## System overview

```
┌─────────────────────────────────────────────────────────────────┐
│                    PHILOSOPHY ESSAY SYSTEM                       │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  CONTEXT             LIBRARY                  SKILLS             │
│  ──────              ───────                  ──────             │
│  voice-dna.md        sources/catalog.yaml     essay-philosophy   │
│  icp.md              sources/<book>/index.md  source-indexer     │
│                      sources/<book>/          source-ingestor    │
│                        <chapter>.{md,pdf}     accept-canonical-  │
│                        index-ch<NN>.md           chapters        │
│                          (split layout only)  accept-canonical-  │
│                      courses/<course>/           positions       │
│                        index.md                                  │
│                      positions/<course>/                         │
│                        index.md                                  │
│                        <position-slug>.md                        │
│                                                                  │
│   WHO I am /         Library + curriculum     HOW to             │
│   serve              + my stances             produce            │
│                      (all topic-keyed)                           │
│                                                                  │
│  EXAM PROMPTS                                                    │
│  ────────────                                                    │
│  exam-prompts/<slug>.md   (the question + outline + sources)     │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

The three peer inputs to the resolver: **sources** (third-party library), **courses** (school-provided curriculum scope), **positions** (my stated stances). All keyed by topic; the exam prompt supplies the topic. Sources and positions are matched independently — a source annotation never points at a position.

---

## Context profiles

In `/context/`. Read the relevant ones before writing any essay.

### `voice-dna.md`
**Purpose**: My writing voice — philosopher-educator, intellectually direct, uses inclusive "we", grounds abstract arguments in concrete examples, weaves formal arguments with accessible explanations.
**When to read**: ALWAYS before writing.

### `icp.md`
**Purpose**: The **examiner**, not a commercial customer. UK undergraduate analytic philosophy programme. Lists what the examiner values (clarity, engagement, opinionated thesis early), what they penalise (advanced/obscure digressions, mere surveying, dry sustained prose), and the jargon they expect.
**When to read**: ALWAYS before writing.

(`business-profile.json` exists but is unused for this project. Ignore it.)

---

## Positions subsystem

```
/positions/
  <course-slug>/
    index.md                 # course-level intro + per-position catalog
    <position-slug>.md       # one file per position
    <position-slug>.md
    ...
```

**Per-position file** (`<slug>.md`) — frontmatter `course: <slug>`, an H1 with the position name, body prose, a trailing `**Applicable to:**` line listing trigger keywords and module refs, and an **optional** `**Usage:**` line giving a one-line hint on how to deploy the position when it matches.

**Index** (`index.md`) — frontmatter, course intro paragraph, then for each position a `## <Name>` heading, a `` `file: <slug>.md` `` pointer, and a denormalized `**Applicable to:**` line for fast scanning. Hand-maintained; no generator (yet). The `**Usage:**` hint is **not** denormalized — it lives only in the per-position file and is read once the position is opened.

**Matching is index-only.** Trigger matching scans `index.md` and never opens per-position files. The per-position `**Applicable to:**` line is the source of truth; the index copy exists so matching can happen with one read. A position file is opened only after its index entry matches the prompt — unmatched position files are never opened. The denormalization carries a small sync cost (keep the two `**Applicable to:**` lines in step when editing) in exchange for O(1)-file matching as the position library grows.

**Purpose**: My stated philosophical positions for one course. When the prompt is silent on direction, the matching position becomes the **conclusion** of the essay; the theory-rejection structure presents rival views honestly first and arrives at my position last. When the prompt directs a position, the prompt wins.

**Usage hint** (optional, per-position): a `**Usage:**` line in the position file overrides the default "matched position = conclusion" behaviour with a per-position instruction in plain English, e.g. "Present as an alternative theory after the analytical canon, not as the conclusion." Precedence: **prompt direction > position `**Usage:**` > default conclusion-role**. If the prompt sets a direction, the prompt wins regardless of what `**Usage:**` says. The hint applies only after the position has been matched via `**Applicable to:**`.

**Architecture note**: Sources, courses, and positions are three **peer** inputs to the resolver. The exam prompt's topic is the meeting ground — sources and positions are matched against it independently. Source-index annotations (in `/sources/<book>/index.md`) describe **topics** the section is good for; they must not point at named position files.

---

## Sources subsystem

The sources subsystem is what makes precise citation possible without loading whole books.

### Directory layout

```
/sources/
  catalog.yaml                # generated; lists books → per-book index paths
  _inbox/                     # drop zone for unprocessed PDFs/HTML/TXT
  <book-slug>/
    index.md                  # the per-book index (markdown)
    index-ch<NN>.md           # per-chapter index files (split layout only)
    <NN>-<chapter>.md         # raw OCR (or converted) — never hand-edited
    <NN>-<chapter>.pdf        # PDFs allowed alongside MD
/courses/
  <course>/
    index.md                  # hand-authored; per-course scope and module guidance
```

### Index and course-spec format

Both `<book>/index.md` and `courses/<course>/index.md` are **markdown** with YAML frontmatter. Edit them as prose; structure is implicit in headings.

**`<book>/index.md`** comes in two layouts; `chapter-indexes: split | inline` in the frontmatter says which. Both carry: book metadata in frontmatter; an optional book-level prose intro under the H1; an optional `**Usage:**` block (see below) right after the intro; one `## Chapter <N> · <Name>` per chapter with an inline metadata line `` `cite: <key> · file: <path> · format: md|pdf|html|txt` `` directly under the heading; optional chapter prose; an indexer-generated `**Topics:**` bulleted list (one topic per `- ` line); and zero or more curator-approved `- Use <ref> for <topic>` bullets binding specific section refs to topics. The two surfaces have different force — see Layer 3 below.

**`**Usage:**`** (book-level, optional) — a one-line policy describing how this book should be deployed by default whenever it's loaded. Lives near the top of `<book>/index.md`, after the H1 intro paragraph and before the first `## Chapter`. Examples: *"Canonical reference for this topic; prefer over Readings where they overlap"*, *"Lay introduction; reinforces academic positions but never overrides them"*, *"Skip technical chapters 5-7 unless the prompt demands depth"*. The hint is hand-authored — the indexer scaffolds an empty placeholder and never overwrites it. A course's `**Books usage:**` line for the same book overrides this hint inside that course; outside any course context, the book-level hint applies as-is.

- **Inline layout** (small books) — after the `**Topics:**` block (and any `Use` bullets, when present), each chapter block also contains `### <ref> <Name> [<a>-<b>]` per section (use `[pp. <a>-<b>]` for PDF) with optional per-section prose. One file holds everything.
- **Split layout** (≥500-line index, or ≥10 chapters with subsections) — section headings and line ranges are extracted into per-chapter `index-ch<NN>.md` files (`<NN>` zero-padded). The short `index.md` carries only chapter blocks (metadata, prose, Topics, optional `Use` bullets — no section listings). Each `index-ch<NN>.md` has lightweight frontmatter (`slug`, `chapter`, `generated`), the chapter H2 + metadata line, and the section listing with line ranges. The per-chapter file path is implicit by convention: `sources/<slug>/index-ch<NN>.md` from the chapter number.

Reverse-mode (topic-only) is **two-tier**:

- **`**Topics:**` is the soft surface.** A topic match flags the chapter as a candidate. The resolver does not auto-read on a Topics-only match — without a section ref the chapter is too coarse a target. Topics matches enter the candidate list shown to the user for confirmation.
- **`- Use <ref> for <topic>` is the hard surface.** A topic match is authoritative: parse `<ref>`, open the corresponding `index-ch<NN>.md` (split) or read the inline section heading (inline) for the line range, and read the section directly as canonical evidence.

Forward-mode (explicit `<ref>` in prompt): same range lookup, but the topic match is skipped.

A section heading has three roles:
- **`<ref>` (e.g. `2.3.4`) is the identifier** — the indexer matches index entries to source headings by this. It's stable across re-OCR.
- **`<Name>` is documentation** for you. You can edit it freely; refresh won't break.
- **`[<a>-<b>]` is derived** — the indexer's only writable target on a heading line. It gets recomputed every refresh.

The `**Topics:**` block is generated by `source-indexer` at scaffold time from the source headings — `-isms`, named theories, eponymous adjectives (`Wittgensteinian`, `Bayesian`), possessive philosopher names (`Hume's`, `Quine's`), and named arguments / paradoxes / principles. Each topic is emitted as its own `- ` bullet under the `**Topics:**` label. The indexer optionally accepts one or two course slugs; when supplied, it also matches the book against those courses' module vocabulary (module names, `**Sources:**`, `**Readings:**`) and emits course-relevant terms as additional Topics. Refresh never re-runs Topics extraction; once written, the Topics block is user-owned (ask explicitly to regenerate one chapter's Topics).

The `- Use <ref> for <topic>` bullets are *never* indexer output. They are produced exclusively by `accept-canonical-chapters` after explicit user approval — every bullet is a deliberate claim that the named section is the canonical text for the topic, and the resolver's hard-surface read depends on that being true. The indexer preserves any bullets it finds verbatim across refresh but never creates, modifies, or removes them.

For books without numbered sections (`## Introduction`, `## The Argument` etc.), the indexer assigns synthetic numeric prefixes at scaffold time (`### 1 Introduction [10-45]`, `### 2 The Argument [46-180]`) so there's still a stable identifier to match by.

**`courses/<course>/index.md`** carries: course metadata in frontmatter (`slug`, `name`, `style`, `books: [...]`); optionally an `**Essay scope:**` block at the very top of the file describing course-wide sourcing policy (see below); optionally a `**Books usage:**` block immediately after it with per-book deployment hints scoped to this course (see below); one `## <N>. <Module Name>` per module (numbered 1-10 typically, with optional `## 0. Introduction` for preamble material); module guidance as free prose; optionally `**Sources:**` and/or `**Readings:**` bullet lists with free-text refs; optional `**Books:** [...]` line to override the course-level book scope for that module.

**`**Essay scope:**`** (course-level, optional) — a course-specific policy directive that **always binds the essay-philosophy skill**. Read it before writing. Common shapes: *textbook-bound* (stay strictly within the course's canonical readings unless the prompt explicitly invites going outside — typical for tightly-textbooked introductory courses), *open* (follow the canonical book's own references into external authors as needed — typical when exam questions cluster around named external philosophers). When this block is present and the prompt does not override it, defer to it: do not pull in outside authors merely because they would strengthen the argument.

**`**Books usage:**`** (course-level, optional) — a bullet list of per-book deployment hints scoped to this course. Each bullet names a book (italicised title or slug, with optional author in parens) followed by an em-dash and a one-line hint. Example:

```markdown
**Books usage:**
- *Understanding Knowledge* (Huemer) — canonical for this course; prefer over Longworth where they overlap
- *Problems of Philosophy* (Russell) — historical framing only; skip the technical chapters
```

These overrides apply only inside this course. They take precedence over the same book's own `**Usage:**` block in `/sources/<book>/index.md`. The resolver reads both whenever it loads a book and uses the course-level hint when present, otherwise the book-level hint. Hints are guidance, not gates — they shape what gets cited and how an author's authority is framed, but never override the prompt or licence fabrication.

The two bullet lists serve different purposes:

- **`**Sources:**`** — the **canonical backbone** for the module. Well-structured texts that present the canonical arguments. When listed, they're the primary thing the essay leans on. **Always loaded.** If a module has no `**Sources:**` at all, the essay falls back to the canonical analytic position from the relevant field invoked from general knowledge — the standard interpretation only, never fabricated quotes, page numbers, or specific arguments.
- **`**Readings:**`** — **specific deepening additions** layered on top of the canonical answer. Each Reading typically elaborates a particular argument that Sources cover only in short form. When present, each becomes one branch of argumentation in the essay. **Loaded when present.** Some Readings may not yet be ingested into `/sources/`; in that case, if the named author's position is canonical/well-known philosophy, it is acceptable to invoke that position from general knowledge — but never hallucinate quotes, page numbers, specific arguments, or invented positions. When in doubt, leave the unresolved Reading out rather than risk fabrication.

The leading number is the **module identifier** (stable across renames); the name after it is documentation for the human reader. Prompts reference modules by either number ("module 3") or name ("module: Tragedy") — the resolver matches whichever is supplied.

### Three layers of source guidance (full)

When a prompt names sources, or names only a topic, look in three places. **All free text everywhere** — the same fuzzy resolver parses "Huemer Understanding Knowledge 2.3.4" wherever it appears.

**Layers merge, they do not override.** Layer 1 always reads. Layer 2 Sources always load (or trigger the canonical-knowledge fallback when the module has none). Layer 2 Readings always load when present (and become argumentation branches in the essay). Layer 3 surfaces additional candidates from in-scope books.

1. **Exam prompt (must-read)** — explicit refs in the prompt MD or chat. **Always resolved and read.** Non-negotiable.
2. **Course MD** — `/courses/<course>/index.md` carries two distinct lists per module:
   - `**Sources:**` — the canonical backbone. **Always loaded.** Lead with these; they present the canonical arguments. **If the module lists no Sources at all, fall back to the canonical analytic answer from the relevant field invoked from general knowledge — the standard interpretation only, never fabricated quotes, page numbers, or specific arguments.**
   - `**Readings:**` — specific deepening additions. **Loaded when present.** Each typically elaborates an argument that Sources cover in short form, and becomes one branch of argumentation in the essay. **If a Reading cannot be resolved (book not in `/sources/`) but the author's position is well-known canonical philosophy, it is acceptable to invoke that position from general knowledge — but never hallucinate quotes, page numbers, specific arguments, or invented positions.** When in doubt, leave the unresolved Reading out rather than risk fabrication.
3. **Book index** ("reverse mode") — `/sources/<book>/index.md` carries per-chapter `**Topics:**` bulleted lists (indexer-generated; soft surface) and zero or more `- Use <ref> for <topic>` bullets (curator-approved; hard surface). **Topic-matched, two-tier:**
   - A `**Topics:**` match flags the chapter as a candidate and surfaces it to the user for confirmation. The resolver does not auto-read on a Topics-only hit.
   - A `- Use <ref> for <topic>` match is authoritative: parse `<ref>` and read the section (range from inline section heading or per-chapter file).
   Both surfaces describe **topics**, not positions: they must not point at named position files. Positions are matched separately via their own `**Applicable to:**` triggers under `/positions/<course>/`. Topic is the meeting ground; sources and positions are peer inputs to the resolver.

For topic-only or under-specified prompts, aggregate candidates from layer 2 (Sources first, then Readings) and layer 3, propose to me with the layer of origin labelled, then resolve.

**Usage hints overlay the layers.** Independent of which layer surfaced a book, two optional hints shape how the book gets deployed once loaded:

- **Book-level `**Usage:**`** — a one-line default in `/sources/<book>/index.md`. Travels with the book.
- **Course-level `**Books usage:**`** — per-book overrides in `/courses/<course>/index.md`. Scoped to that course only.

Precedence: **course `**Books usage:**` (per-book line) > book `**Usage:**` > no hint**. Hints are interpretive guidance — they steer what to cite and how strongly to lean on the author — but they never override the prompt and never licence fabrication.

---

## Common requests (worked examples)

### Essay from an exam prompt MD
```
User: "Write an essay using exam-prompts/induction.md"
You:
1. Read /context/voice-dna.md, /context/icp.md
2. Read /exam-prompts/induction.md
3. Parse course/module/outline/source refs
4. Read /positions/<course>/index.md (if directory exists); match
   **Applicable to:** triggers against prompt topic; open matched
   position file(s) for the body
5. Read /sources/catalog.yaml + relevant /courses/<course>/index.md
6. Resolve and read only cited section ranges (three layers merge:
   prompt refs + course **Sources:** + book-index reverse mode)
7. Plan via essay-philosophy framework (matched position = conclusion
   when prompt is silent on direction)
8. Print ~1200-word essay to chat
```

### Essay from a topic only
```
User: "Write an essay on the Liar paradox" (and mentions a course/module)
You:
1. Load context (voice-dna, icp)
2. Read /positions/<course>/index.md; match topic against
   **Applicable to:** triggers; open matched position file(s)
3. Read catalog + course YAML
4. Aggregate three source layers; propose candidate sources to me; confirm
5. Resolve and read confirmed ranges
6. Plan and write (matched position = conclusion if prompt is silent)
```

### Adding a new source
```
User: drops PDF in /sources/_inbox/, "ingest this"
You:
1. Invoke source-ingestor
2. Gather minimal metadata (book, slug, author, chapter number/name)
3. File into /sources/<book-slug>/
4. Invoke source-indexer (scaffold mode for new books, refresh otherwise);
   optionally pass a course slug to bias Topics extraction toward that
   course's module vocabulary
5. Remind me of the optional curation steps:
   - Hand-edit index.md to fill cite, **Usage:**, chapter/section prose
   - Run accept-canonical-chapters <book> [<course>] to add `Use` marks
     (and, with a course, course-MD updates)
   - Run accept-canonical-positions <book> <course> to update positions
```

### Refreshing the index after editing notes
```
User: "I added some notes to the Understanding Knowledge index, refresh it"
You:
1. Invoke source-indexer
2. Refresh mode: re-derive line ranges in section headings;
   preserve all my prose verbatim
3. Regenerate catalog.yaml; validate; report
```

---

## File operations

### Reading
```
"Read /context/voice-dna.md"
"Show me sources/understanding-knowledge/index.md"
"What's in /exam-prompts/?"
```

### Saving (only when I ask)
```
"Save the essay to /drafts/induction.md"
```

---

## Troubleshooting

### Output sounds generic
- Verify voice-dna.md is populated (it is, as of latest update).
- Confirm you actually read it before writing.

### Wrong audience tone
- icp.md describes the **examiner**, not a customer. Re-read.

### A source ref didn't resolve
- Run source-indexer (the index may be stale).
- Check the author/book name — is it spelled the way the catalog has it?
- If the chapter exists but the section doesn't, the section number in the source heading and the index heading don't match. The number is the identifier — fix whichever is wrong.

### `[a-b]` is wrong after re-OCR
- Run source-indexer in refresh mode. It re-derives the bracket range from the current source headings, matched by section number, and leaves your prose alone.

### A source that should have been suggested wasn't
- The book may not be in scope for the named course/module. Check the `books:` field in `/courses/<course>/index.md` frontmatter (or `**Books:**` under the module). To add it for a course, run `accept-canonical-chapters <book> <course>` and approve the bucket-B course-MD updates.
- The chapter's `**Topics:**` block may not list the topic you expected — only a soft match would have fired anyway. Either rerun `source-indexer` against the relevant course slug to widen Topics, or hand-edit the block (add a new `- <topic>` bullet).
- For an authoritative auto-read, the chapter needs a `- Use <ref> for <topic>` bullet matching the prompt's topic. Run `accept-canonical-chapters <book>` (optionally with a course) to propose one through the approval loop. Hand-editing the bullet is also fine — the indexer preserves any it finds. For split-layout books, line ranges live in `index-ch<NN>.md`; the bullet only needs the `<ref>`.

### Subchapter content was wrong (read more than the section)
- The heading numbering in the source body may not start with the section ref. Either fix the heading or hand-edit the `[a-b]` marker in the matching section heading inside the book's `index.md`.

---

## Quick reference

### Paths
```
Context:       /context/voice-dna.md, /context/icp.md
Positions:     /positions/<course>/index.md
               /positions/<course>/<slug>.md
Sources:       /sources/catalog.yaml
               /sources/<book>/index.md
               /sources/<book>/index-ch<NN>.md   (split layout only)
               /courses/<course>/index.md
Inbox:         /sources/_inbox/
Skills:        /.claude/skills/<skill>/SKILL.md
Exam prompts:  /exam-prompts/
Drafts:        /drafts/             (only when explicitly saving)
Voice samples: /setup/voice-samples/ (input for voice-dna-creator)
```

### Key commands
```
"What books are in the library?"           → reads catalog.yaml
"What's the index say about UK ch. 10?"   → reads understanding-knowledge/index.md
"What modules are in the epistemology course?" → reads courses/epistemology/index.md
```
