---
name: essay-canonical
description: Write canonical-book-derived study-note essays (C-essays) — one per author block of the course's canonical book. The C-essay mirrors the chapter's own argumentation, stripped of filler, ≤950 words. A chapter that contains two or more philosophical positions structurally separated as distinct subchapter blocks (each with its own Intro / extracts / Commentary) is treated as containing two or more distinct topics, and yields one C-essay per block. A chapter with a single position or with parallel sub-topics yields one C-essay. Use when the user asks for "canonical essays / C-essays / study notes for chapter N of <canonical book>", "write canonical essays for <course>", "write me canonical essays for chapters X, Y, Z in <course>", or names a course + chapter list and asks for canonical essays.
---

# Canonical-Book Essay Writer (C-essays)

One C-essay per **topic** in a chapter of the course-canonical book. Topic = author block (Intro to Author + extracts + Commentary). 2+ structurally separated blocks → one C-essay per block. 1 block or parallel sub-topics → one C-essay for the chapter. C-essay reproduces the block's argument, no textbook scaffolding.

Not exam essays. No thesis-by-default, no theory-rejection, no template. Follow the chapter.

## Modes

All write to disk and chat.

- **Single chapter** (`"C-essay for <course> ch. 2"`) — full prose to chat.
- **Multi-chapter** (list / range, mix digits and names) — status lines + summary; no full prose.
- **All chapters** (`"all C-essays for <course>"`) — every chapter with a matching course module. Same output as multi-chapter.

Course missing → ask. Chapter token unresolvable → ask. Never silently skip.

## Process

### 1. Resolve course and canonical book

- Course slug → case-insensitive match in `/courses/`. Zero/multiple → ask.
- Read `/courses/<course>/index.md`. Find course-level `**Usage:**` block (after H1 + `**Essay scope:**`, before first `## <N>.`).
- Find the bullet asserting canonical status (suffix `— canonical for this course` or equivalent first-clause assertion). Resolve title to slug via `books:` frontmatter and `title:` in `/sources/<slug>/index.md`.
- No `**Usage:**` / no canonical bullet → stop: `<course> has no canonical book — C-essays not applicable.` Multiple canonical bullets → stop: `multiple canonical bullets — please pick one.` Don't guess.

### 2. Resolve chapters

Read `/sources/<slug>/index.md`; note `chapter-indexes: split | inline`.

Per token:
- Digit → chapter N.
- Range `1-4` → expand inclusively.
- Name → fuzzy-match course MD `## <N>. <Name>` first, canonical book `## Chapter <N> · <Name>` as fallback.
- `"all"` → every chapter with a matching course module. Skip Chapter 0 unless matched.

Unresolvable → stop and ask.

### 3. Read substantive sections only

Per chapter N:

- Open `/sources/<slug>/index-ch<NN>.md` (split, NN zero-padded) or use inline section list.
- Sections look like `### N.M Title [a-b]` (lines) or `[pp. a-b]` (PDF).
- **Skip**: *Notes*, *Final Task*, *Further Questions*, *Abstract*, sub-numbered note sections.
- **Skip**: "Introduction to the Problem" — generic scaffolding. Read only if the chapter has no other expository run.
- **Keep**: "Introduction to <Author>", all extracts, "Commentary on <Author>".
- Read each kept range with `Read(path, offset, limit)` (MD/TXT/HTML) or `Read(path, pages: "<a>-<b>")` (PDF). **Ranges only — never whole chapters or books.**
- Cache the course module's `**Topics:**` block for orientation.

### 4. Detect structural split

Author block = contiguous run:

- `### N.M Introduction to <Author>` (or `<Position>`)
- 1+ extract subsections
- `### N.M Commentary on <Author>` (sub-numbered commentary OK)

Count blocks:

- **2+ separated** (contiguous, not interleaved) → one C-essay per block. Default for *Reading Philosophy*.
- **1** (single-author) → one C-essay for the chapter.
- **0 clear blocks** (parallel topics) → one C-essay for the chapter.

Cross-references between blocks (one's commentary attacks the other) don't disqualify the split — each per-block essay restates the rival briefly where engaged.

### 5. Plan

Identify upfront: chapter's central question (one line, shared across split essays); per block, author + the position the chapter attributes; where the chapter takes a side vs. leaves open. Mirror — don't force a verdict the chapter doesn't deliver.

**Per-block (split):**
1. Short opener: chapter's question, framed for this author.
2. The position, decomposed as the chapter decomposes it (intro + extracts + commentary). Multiple threads (Williams's three threads, Locke's stages) structure the body.
3. Objections recorded against this author, including from the rival block where the chapter records them. Restate rival in 1–2 sentences only — enough to make the objection intelligible. Rival's full case lives in rival's own file.
4. Chapter's verdict on this author, or "open" plainly stated.

**Single-author (non-split):** question + author → argument decomposed → objections-and-replies → verdict.

**Parallel-topics (non-split):** one paragraph per topic, chapter's order. No forced unifying thesis.

### 6. Write

- **Voice**: `/context/voice-dna.md`. Read voice-dna.md and icp.md once per batch.
- **Register**: study notes in continuous prose. Less rhetorical than P-essay. Every sentence advances the chapter's argument. No "we can see that…", no "in my view" (it's the chapter's view, not the user's).
- **No filler**: drop "It is worth noting that…", "The standard objection runs…", "Two worries deserve naming…". Anything that delays the dialectic is cut. Same banlist as essay-philosophy plus stricter.
- **Density**: compress, don't summarise. Same arguments at higher info-density per word.
- **Word count**: ≤950 hard, ~800 target. Trim aggressively — models overshoot. Cut: textbook framing (already skipped at read stage; don't reintroduce), restatement, ornamental qualifiers, "as we shall see" / "as discussed above". Splitting ≠ budget increase; each per-block file ≤950 on its own.
- **Author attribution**: each philosopher named once at first mention, thereafter engaged-with by view. **No chapter / section / page numbers in prose.**
- **No academic-lineage chains** ("a view going back to Aristotle and developed by…").
- **Cross-block restatement (split only)**: 1–2 sentences max where commentary engages the rival.

### 7. Save

Path templates (book-keyed; multiple courses sharing a canonical book share this tree):

- **Non-split**: `/courses/<course>/essays/C-<bookSlug>/<moduleNumber>-<topicSlug>.md`
- **Split**: `/courses/<course>/essays/C-<bookSlug>/<moduleNumber>-<authorSlug>.md`

- `<bookSlug>` — canonical book's `/sources/` dir name (e.g. `reading-philosophy`). Tree mirrors with `C-` prefix: `/essays/C-reading-philosophy/`.
- `<moduleNumber>` — chapter number = course module number. No padding; write `1`, `2`, `10`.
- `<topicSlug>` (non-split) — slugify module name from `## <N>. <Name>` in course MD. Falls back to canonical book's chapter title if no matching module (note in chat, don't abort). E.g. `1-doubt.md`, `2-self.md`.
- `<authorSlug>` (split) — author surname slugified (`williams`, `nozick`, `descartes`, `moore`, `locke`, `hume`, `feagin`). Same surname clash → first-name initial prefix (`b-williams`). Module name **not** in split filenames. E.g. `6-williams.md`, `6-nozick.md`.
- One file per topic. No `<questionSlug>` subfolder. Existing → overwrite. Create `/essays/C-<bookSlug>/` if absent.

H1 (no frontmatter, blank line, prose):

- **Non-split**: `# <Chapter title>` (e.g. `# Doubt`, `# Self`, `# Tragedy`).
- **Split**: `# <Chapter title>: <Author>` (e.g. `# Equality: Williams`, `# Doubt: Descartes`).

Plain paragraphs only — no `##`, no bullets, no numbered lists, no fences.

### 8. Report

- **Single chapter, non-split** — full prose, end `Saved to: <path>`.
- **Single chapter, split** — full prose per block separated by H1s; one `Saved to:` per file.
- **Multi / all** — status lines, no full prose:
  - `✓ <chapter title>: <author> → <path>` (split)
  - `✓ <chapter title> → <path>` (non-split)
  - `– <chapter title> (skipped: <reason>)`
  - `✗ <chapter title> (failed: <reason>)` (don't abort batch)

  Summary: `Wrote N C-essays to /essays/C-<bookSlug>/` (+ skipped/failed counts if any).

## vs. essay-philosophy (P-essays)

| | P-essay | C-essay |
|---|---|---|
| Topic source | exam question / Q-file H1 | chapter of canonical book |
| Structure | theory-rejection / given outline | mirrors chapter |
| Thesis | opinionated, up front | none — chapter's verdict if any |
| Conclusion | matched position or mainstream | chapter's verdict or open |
| Voice | user, exam register | user, study-note register |
| Word cap | 1200 | 950 |
| Path | `/courses/<c>/essays/<N>-<name>/<questionSlug>.md` | `/essays/C-<bookSlug>/<N>-<topicSlug>.md` or `<N>-<authorSlug>.md` |
| H1 | exam question | chapter title (± `: <Author>`) |
| Files / chapter | one per question | one per chapter or one per author block |
| Positions | matched as Theory N | not consulted |
| Sources | three-layer aggregation | canonical book only |

## Don'ts

- No user positions. Position-matching is P-essay only.
- No other-book sources. Other authors mentioned by the canonical book → present as the canonical book presents them; don't open externals.
- No invented thesis. Survey chapter → survey C-essay.
- No whole-chapter reads. Subsection ranges only.
- No section / page / chapter numbers in prose. No canonical-book name in prose.
- No strawman. Both sides at strongest where the chapter holds dialectic.

## Quality checklist

- [ ] Split detected (2+ contiguous Intro/extracts/Commentary)? If yes → one file per block at `<N>-<authorSlug>.md`. If no → one file at `<N>-<topicSlug>.md`.
- [ ] H1 correct: `# <Chapter title>` (non-split) or `# <Chapter title>: <Author>` (split). No question framing, no number prefix.
- [ ] ≤950 words per file. Splitting doesn't raise cap.
- [ ] Plain paragraphs only — no `##`, bullets, fences.
- [ ] Each named philosopher attributed once; thereafter engaged-with by view.
- [ ] No chapter / section / page numbers in prose; no canonical-book name in prose.
- [ ] Filler subsections (Notes, Final Task, Further Questions, Abstract) skipped at read stage.
- [ ] Non-split: opposing positions in dialectic. Split: each file presents its author primarily; rival restated 1–2 sentences max where engaged.
- [ ] Verdict where the chapter delivers one; "open" plainly stated where it doesn't.
- [ ] No user-position content. No non-canonical sources.
- [ ] Multi-chapter: status lines per file, summary count, no full prose in chat.
