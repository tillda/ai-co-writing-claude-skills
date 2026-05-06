---
name: essay-canonical
description: Write canonical-book-derived study-note essays (C-essays) — one per chapter of the course's canonical book. The C-essay mirrors the chapter's own argumentation, stripped of filler, ≤950 words. A chapter usually presents two or more opposing positions (e.g. Hume vs. Feagin); that dialectic is the structural backbone, not an exam thesis. Use when the user asks for "canonical essays / C-essays / study notes for chapter N of <canonical book>", "write canonical essays for <course>", "write me canonical essays for chapters X, Y, Z in <course>", or names a course + chapter list and asks for canonical essays.
---

# Canonical-Book Essay Writer (C-essays)

Take a chapter (or a list of chapters) from the **course-canonical book** and write one C-essay per chapter. The C-essay reproduces the chapter's argumentation precisely, stripped of textbook filler — close to revision notes, but written as continuous prose.

C-essays are **not exam essays**. There is no exam question, no opinionated thesis-by-default, no theory-rejection structure imposed from outside. The structure is whatever the chapter itself sets: typically two or more opposing positions in dialectic, sometimes a single author's argument with objections-and-replies. The skill follows the chapter, not a template.

## Modes

Three invocation modes, all writing to disk **and** chat (one C-essay is short enough that chat output is fine).

- **Single chapter** — `"C-essay for intro-to-philosophy chapter 2"`, `"canonical essay for module 5 in <course>"`, `"write me a canonical essay for ch. 8 of intro-to-philosophy"`. One chapter, one file, full prose to chat.
- **Multi-chapter** — list of chapter numbers and/or module names: `"chapters 1, 3, 5"`, `"chapters: doubt, self, tragedy"`, `"chapters 1-4"` (range). Mixing allowed. Print one short status line per chapter to chat plus an aggregated summary at the end; do not print full prose for batch runs.
- **All chapters** — `"all canonical essays for <course>"`, `"do every C-essay for <course>"`. Process every chapter in the canonical book that has a corresponding course module. Same chat output as multi-chapter (status lines + summary).

If the course is not given, stop and ask which course. If a chapter token does not resolve (digit with no chapter, name with zero or multiple matches), stop and ask — do not silently skip.

## Process

### 1. Resolve the course and the canonical book

- Match the course slug case-insensitively against directories under `/courses/`. Zero or multiple matches → stop and ask.
- Read `/courses/<course>/index.md`. Locate the course-level `**Usage:**` block (placed after the H1 intro and any `**Essay scope:**` block, before the first `## <N>. <Module>` heading).
- Find the bullet that explicitly designates a book as **canonical for this course**. The user's convention is the suffix `— canonical for this course` (or "for this course; lead with it on every prompt", or any bullet whose first clause asserts canonical status). Examples:
  - `- *Reading Philosophy* (...) — canonical for this course; lead with it on every prompt.` ← canonical
  - `- Huemer *Knowledge, Reality, and Value* — authoritative but supplemental: never lead with it...` ← not canonical
- Resolve the named book to a slug: take the book title from the bullet, fuzzy-match against `books:` in the course frontmatter and against `title:` in `/sources/<slug>/index.md` for each candidate slug.
- **If the course has no `**Usage:**` block, no canonical bullet, or multiple canonical bullets**, stop with a one-line message: `<course> has no canonical book — C-essays not applicable.` (or `multiple canonical bullets — please pick one`). Do not guess.

### 2. Resolve the chapters

- Read the canonical book's `/sources/<slug>/index.md`. Note the layout (`chapter-indexes: split | inline` from frontmatter — fall back to scanning if absent).
- For each token in the user's chapter list:
  - **Digit token** (`2`, `10`) → that chapter number.
  - **Range** (`1-4`) → expand inclusively.
  - **Name token** (`doubt`, `tragedy`, `freedom`) → fuzzy-match against the course MD's `## <N>. <Name>` headings (preferred; the course is what the user thinks in) and against the canonical book's `## Chapter <N> · <Name>` headings as fallback.
  - `"all"` → every chapter in the canonical book that has a matching `## <N>. <Name>` heading in the course MD. Skip Chapter 0 unless it has a matching course module.
- Any unresolvable token → stop and ask. Do not skip.

### 3. Read the chapter content (substantive sections only)

For each resolved chapter `N`:

- Open `/sources/<slug>/index-ch<NN>.md` (split layout, NN zero-padded) or use the inline layout's section list under the chapter block.
- The chapter's section list looks like `### N.M Title [a-b]` (line range) or `### N.M Title [pp. a-b]` (PDF page range).
- **Filter the sections**:
  - **Skip** pure-filler subsections — anything titled exactly *Notes*, *Final Task*, *Further Questions*, *Abstract*, or sub-numbered note sections (`N.M.1 Notes`, etc.).
  - **Skip** "Introduction to the Problem" subsections by default — they tend to be generic textbook scaffolding, not part of the chapter's argument. Read them only if they are the chapter's *only* substantive expository run (rare).
  - **Keep** "Introduction to <Author>" subsections — these set up the author's position.
  - **Keep** all author extracts and "Commentary on <Author>" subsections — these are the chapter's load-bearing content.
- Read each kept subsection's range with `Read(path, offset=start, limit=end-start+1)` for MD/TXT/HTML or `Read(path, pages: "<a>-<b>")` for PDF. **Read only the resolved ranges. Never read whole chapters or whole books.**
- Cache the course module's `**Topics:**` block (and any star ratings) for orientation — it tells you what the course considers important within the chapter.

### 4. Plan the C-essay

Identify, before writing:

- The chapter's **central question or problem** (one line).
- The chapter's **primary authors** and their positions.
- The **dialectic structure** — does the chapter present two opposing positions (the typical case), one author's argument with objections (sometimes), or several parallel sub-topics (e.g. Logic chapters covering several distinct devices)?
- Where the chapter **takes a side** vs. where it **leaves the dialectic open**. Mirror this — do not force a verdict the chapter does not deliver.

Default plan for the typical two-author dialectic chapter:

1. One short opening paragraph: the question / problem the chapter is about, who the authors are, and (one clause) what is at stake between them.
2. Position 1 — author named, view stated, the chapter's strongest formulation, the chapter's own objections (if any) recorded.
3. Position 2 — same shape; if it is a direct response to Position 1, present the contact points explicitly.
4. The chapter's own assessment, if it makes one. If the chapter leaves the question open, say so plainly.

Plan for a single-author chapter (rarer in *Reading Philosophy*; more common in monographic canonical books):

1. Question and author.
2. The argument, decomposed into steps as the chapter decomposes it.
3. Objections-and-replies the chapter records.
4. The chapter's verdict.

Plan for a parallel-topics chapter (e.g. several conditionals; several puzzles):

- One paragraph per parallel topic, in the chapter's order. No forced unifying thesis.

### 5. Write

- **Voice**: match `/context/voice-dna.md` — the C-essay still sounds like the user. Read voice-dna.md and icp.md once at the start of a batch and reuse.
- **Register**: study notes in continuous prose. Less rhetorical than an exam essay — fewer stylised verbs, fewer thesis-defending flourishes. Each sentence should advance the chapter's argumentation. No rhetorical "we can see that...", no "in my view" framing (this is not the user's view, it is the chapter's).
- **No filler tokens**: drop "It is worth noting that...", "The standard objection runs...", "Two worries deserve naming...". Same banlist as essay-philosophy plus stricter: anything that delays the dialectic is cut.
- **Density**: the C-essay should compress the chapter, not summarise it. Aim for the same arguments at higher information density per word.
- **Word count**: ≤950 hard cap, aim for ~800. Models overshoot — trim aggressively. Cut: chapter framing the canonical book itself does (textbook scaffolding has already been skipped at the read stage; do not reintroduce it), restatement, ornamental qualifiers, "as we shall see" / "as discussed above" cross-references.
- **Author attribution**: each named philosopher appears once at first mention, then engaged with by view. Same single-mention rule as essay-philosophy. **No chapter, section, or page numbers in prose** (same rule as essay-philosophy — section refs are for the reader of the index, not the reader of the C-essay).
- **No academic-lineage chains**: do not write "a view going back to Aristotle and developed by...". The chapter does not need that, and a study note especially does not.

### 6. Save

Path template:

`/courses/<course>/canonical-essays/<N>-<moduleName-slug>.md`

- `<N>` — the chapter number (matching the course module number; they correspond by design when a canonical book is set up).
- `<moduleName-slug>` — slugify the module name from `## <N>. <Name>` in the course MD (lowercase, non-alphanumerics → `-`, collapse, trim). Falls back to slugifying the canonical book's chapter title if the chapter has no matching course module (rare; usually means the course MD is out of date — note in chat, do not abort).
- One file per chapter. **No `<questionSlug>` subfolder**: a chapter is the unit, and there is no question.
- Existing file → **overwrite**. Re-running replaces the previous draft.

The file has no frontmatter. First line is `# <Chapter title>` — use the canonical book's chapter title (e.g. `# Doubt`, `# Self`, `# Tragedy`), not a question, not a numbered prefix. One blank line, then prose.

### 7. Report

- **Single-chapter mode** — print full essay prose to chat, end with `Saved to: <path>`.
- **Multi-chapter / all-chapters mode** — one short status line per chapter:
  - `✓ <chapter title> → <path>` on success
  - `– <chapter title> (skipped: <reason>)` if skipped (e.g. no matching course module and the chapter title couldn't be resolved)
  - `✗ <chapter title> (failed: <reason>)` if write failed (don't abort the batch)

  End with a one-line summary: `Wrote N C-essays to /courses/<course>/canonical-essays/` (plus skipped/failed counts if any). Do not print full prose for batch runs.

## Format reminder

- First line `# <Chapter title>`, blank line, then prose.
- Plain paragraphs only. **No `##` sub-sections, no bullets, no numbered lists, no fences** — paragraph breaks only. (Same as essay-philosophy. Tempting to add headings for "study notes", but the prose-only convention keeps these readable as continuous text and consistent with the rest of the essay tree.)
- ≤950 words.

## Difference from essay-philosophy at a glance

| | essay-philosophy (P-essay) | essay-canonical (C-essay) |
|---|---|---|
| Source of topic | exam question or Q-file H1 | chapter of the course's canonical book |
| Structure | theory-rejection by default; outline if given | mirrors the chapter's own argumentation |
| Thesis | opinionated, stated up front | none — the chapter's verdict (if any) appears where the chapter places it |
| Conclusion | matched user position when prompt is silent; mainstream otherwise | the chapter's own conclusion or open dialectic |
| Voice | user voice, exam-essay register | user voice, study-note register |
| Word cap | 1200 | 950 |
| Path | `/courses/<c>/essays/<N>-<name>/<questionSlug>.md` | `/courses/<c>/canonical-essays/<N>-<name>.md` |
| H1 | the exam question | the chapter title |
| Position-matching | matches user positions, makes them Theory N | **does not** match positions — the C-essay reflects the book, not the user's stance |
| Source resolution | three-layer aggregation | restricted to the canonical book; no other sources |

## What NOT to do

- **Do not consult the user's positions.** C-essays mirror the book, not the user. Position-matching is a P-essay feature only.
- **Do not aggregate sources from other books in the course.** Only the canonical book is read. If the chapter mentions other authors that the canonical book itself summarises (e.g. Aristotle in the *Reading Philosophy* tragedy chapter), present them as the chapter presents them — do not open external sources.
- **Do not invent a thesis to give the C-essay an exam-essay shape.** If the chapter is genuinely a survey, the C-essay is a survey.
- **Do not read whole chapters at once.** Only the substantive subsection ranges, as in essay-philosophy.
- **Do not include section numbers, page numbers, or chapter cross-references in prose.**
- **Do not mention the canonical book by name in prose** (the C-essay's H1 + path identify the source; restating "in *Reading Philosophy* the authors..." is filler).
- **Do not strawman.** When a chapter presents two positions in genuine dialectic, both must be presented in their strongest form. The C-essay is not picking sides on the user's behalf.

## Quality checklist

Before reporting completion:

- [ ] One file per requested chapter at `/courses/<course>/canonical-essays/<N>-<moduleName-slug>.md`
- [ ] First line is `# <Chapter title>` (no question framing, no numbered prefix in the H1)
- [ ] Each C-essay is ≤950 words; aim was ~800
- [ ] Plain paragraphs only — no `##` sub-sections, no bullets, no fences
- [ ] Each named author from the chapter appears exactly once in attribution; thereafter engaged-with by view
- [ ] No chapter / section / page numbers in prose; no canonical-book name in prose
- [ ] Filler subsections (Notes, Final Task, Further Questions, Abstract) were skipped at the read stage and do not appear in the essay
- [ ] When the chapter presents opposing positions, both are in the C-essay in dialectic — not a one-sided summary
- [ ] When the chapter takes a verdict, the C-essay records it; when the chapter leaves the question open, the C-essay says so plainly
- [ ] No user-position content; no sources from books other than the canonical
- [ ] Multi-chapter runs: one status line per chapter, summary count at the end, no full prose in chat
