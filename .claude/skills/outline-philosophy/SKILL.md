---
name: outline-philosophy
description: Write argumentative outlines for analytic philosophy questions — the same theory-rejection structure as a full essay, but as semi-structured bullets (more than nouns, less than prose). Use when the user asks for an essay outline, plan, skeleton, or revision-style argument map.
---

# Philosophy Essay Outline Writer

Write a clear argumentative outline for an undergraduate analytic philosophy question. This is the **same argument the essay would make**, compressed into semi-structured bullets — short clauses, not full sentences and not bare nouns. Useful as a revision aid or a blueprint for the full essay later.

This skill is the outline-only sibling of `essay-philosophy`. Source resolution, position matching, and theory-rejection logic are identical — only the output form changes.

## Before Writing

1. **Match positions** — if the prompt names a course and `/positions/<course>/index.md` exists, read the index. Match each entry's `**Applicable to:**` line against the prompt topic / module. For matched entries, open the position file. Honour any `**Usage:**` line (it can redirect how the position is deployed — e.g. as an alternative theory after the canon, not the conclusion).

2. **Resolve sources** — see Source Resolution below. Same three layers as essay-philosophy. Read only the cited line/page ranges; never whole books.

3. **Direction precedence** (highest first):
   - **Outline in the prompt?** Follow it — but render as outline-form bullets (this skill's style), not prose.
   - **Opinion / position / specific argument in the prompt?** Theory N is that view (overrides any user position and `**Usage:**` hint).
   - **Matched user position?** Theory N is that position — unless its `**Usage:**` redirects.
   - **No direction?** Theory N is the analytic-mainstream view.

## Output Format

The outline is markdown. First line is `# <question>` (verbatim from the prompt), one blank line, then a `**Thesis**:` line, then sectioned bullets.

**Word count**: target ~300 words, **hard cap 1400**. Aim low and trim.

**Style for bullet content**: short clauses. Not bare nouns ("Russell's view"), not full sentences with all the connective tissue ("Russell argues, in his famous 1905 paper, that..."). Aim for the middle: `Russell: descriptions are quantifier phrases, not referring expressions`. One clause per bullet. A bullet that needs more than two short clauses should usually become two bullets.

**Citations**: cite only authors of attached PAPERS. General books (like introductions) don't need citations — content is canonical.

### Skeleton

```markdown
# <question>

**Thesis**: <one-sentence position to be defended>

## Background
- <key term>: <one-line definition>
- <key distinction>: <stated>
- <relevant assumption>: <stated, if any>

## Theory 1: <name> (rejected)
- <view in one clause>
- <strongest formulation, 1–2 short clauses> (cite if from a source)
- <objection in one clause>
  - <best defence>
  - <why the reply fails>
- <objection>
  - <defence>
  - <why it fails>
- refuted because <decisive reason>

## Theory 2: <name> (rejected)
- ...

[... further rejected theories as needed ...]

## Theory N: <name> (preferred)
- <view>
- <main support, 1–3 short clauses; cite sources>
- <objection>
  - <conclusive defence in favour of Theory N>
- <objection>
  - <conclusive defence>
- stands because <reason tying back to thesis>

## Conclusion
- Theory 1 fails: <one-line summary>
- Theory 2 fails: <one-line summary>
- Theory N stands: <one-line summary tying to thesis>
```

### Notes

- **Theory-rejection is the default.** Best for epistemology, logic, philosophy of language, modern metaethics. For historical-position or single-theory topics, collapse to: present the theory, raise objection(s), assess.
- **Argue rivals honestly.** When Theory N is set by a user position, rivals must still be presented in their strongest form with genuine objections — strawmanning is as visible in an outline as in prose.
- **Not every theory needs the same depth.** A weaker rival can be one best-case bullet and a single decisive objection. The preferred theory deserves the most rows.
- **Verdicts can be partial.** A rival can be partly right; verdict bullet says so (`partly right: X holds, Y fails because...`). Theory N can stand on balance — fewest or least decisive problems, not a clean win (`stands on balance: fewer/less decisive problems than rivals`). Conclusion section ties back accordingly — preferred-on-balance, not proven.
- **No filler.** If a theory has no real reply to an objection, omit the reply bullet. If a reply succeeds (preferred theory), say so in the verdict.
- **Length target**: 30–60 bullets total. Revision-density, not exhaustive.

## Output Path

Same template as essays, but under `outlines/`:

`/courses/<course>/outlines/<moduleId>-<moduleName-slug>/<questionSlug>.md`

- `<course>` — frontmatter `course:`.
- `<moduleId>` and `<moduleName>` — looked up from `## <N>. <Name>` in `/courses/<course>/index.md`. Slugify the name.
- `<questionSlug>` — frontmatter `slug:`; if absent, derive a 2–5 word slug.

**Required: `course:` must be set.** If absent, reply with one line and stop.

**Fallback**: course set but no module resolvable → `/courses/<course>/outlines/_unfiled/<questionSlug>.md`.

**Existing file → overwrite.** Print to chat. Final reply line `Saved to: <path>`.

## Source Resolution

Identical to essay-philosophy. Three layers, all merging:

1. **Exam prompt** — explicit free-text refs (e.g. `(Huemer UK 10.4.2)`). Always resolved and read.
2. **Course MD per-module** — `/courses/<course>/index.md`:
   - `**Sources:**` — canonical backbone, always loaded. If a module has none, fall back to canonical analytic position from general knowledge (no fabrication of quotes, page refs, or specific arguments).
   - `**Readings:**` — deepening additions, loaded when present; each typically becomes one rejected-theory or supporting branch. If unresolvable but the author is canonical, invoke their standard view (no fabrication).
3. **Book index reverse mode** — `/sources/<book>/index.md`:
   - `- Source <ref> for <topic>` bullets are **hard**: read the section's range as canonical evidence.
   - `**Topics:**` bullets are **soft**: a match flags the chapter as a candidate. For topic-only prompts, propose to the user with layer-of-origin labelled before reading.

### Algorithm

1. Read `/sources/catalog.yaml`. If course set, read `/courses/<course>/index.md`; note `**Essay scope:**` and `**Usage:**`; identify in-scope books (frontmatter `books:` + optional `**Books:**` override).
2. For each free-text ref: tokenise → author / book / section. Open the book's `index.md` (or `index-ch<NN>.md` for split-layout books — see CLAUDE.md). Find the matching section heading and trailing range marker (`[<a>-<b>]` lines, `[pp. <a>-<b>]` PDF).
3. **Read only that range**: `Read(path, offset=start, limit=end-start+1)` MD/TXT/HTML; `Read(path, pages: "<a>-<b>")` PDF. Never whole books.
4. Multiple candidates → ask before reading. Cache by ref string.
5. If a ref is unresolvable, note in a one-line preface — don't silently drop.

### Topic-only prompts

Aggregate Layer 2 (Sources + Readings) and Layer 3 (Source-bullets hard, Topics-bullets soft); deduplicate; propose to the user with each candidate's layer-of-origin and surface; confirm; read.

### What NOT to do

- Never read a whole book / chapter when a section was named.
- Never load an out-of-scope book's index.
- Never invent a citation key or section number that the index doesn't have.
- Never fabricate quotes, page numbers, or specific arguments.

## Depth and Scope

- **Target level**: a sharp undergraduate who knows the main and most well-known arguments.
- **Opinionated**: take a position. An outline that just lists views without ranking them is not what this skill produces.
- **Avoid obscurities** — no advanced or unusual positions unless the prompt explicitly calls for them.

## Process

1. **Understand**: parse question; note any provided outline / position / argument; identify course + module from frontmatter.
2. **Resolve**: if course set, read positions index + match triggers + open matched files; read catalog + course index + scope/usage blocks; aggregate three source layers; propose candidates if topic-only; resolve refs and read ranges; note unresolved refs in a one-line preface.
3. **Plan**: thesis (provided / matched position / mainstream); theories to reject and order; for each rejected theory: strongest formulation, decisive objection(s), defenders' replies, why they fail; for Theory N: alleged objections, conclusive replies.
4. **Write**: first line `# <question>`, blank line, `**Thesis**:` line, Background, one section per theory (rejected first, preferred last), Conclusion. Bullets are short clauses.
5. **Save & deliver**: construct path; if no `course:`, reply with one line and stop; if no module, save under `_unfiled/`; overwrite if exists; print to chat; final reply line `Saved to: <path>`.
