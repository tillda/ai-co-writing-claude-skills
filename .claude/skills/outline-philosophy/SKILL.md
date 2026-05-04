---
name: outline-philosophy
description: Write argumentative outlines for analytic philosophy questions — the same theory-rejection structure as a full essay, but as semi-structured bullets (more than nouns, less than prose). Use when the user asks for an essay outline, plan, skeleton, or revision-style argument map.
---

# Philosophy Essay Outline Writer

Write a clear argumentative outline for an undergraduate analytic philosophy question. This is the **same argument the essay would make**, but compressed into semi-structured bullets — short clauses, not full sentences and not bare nouns. Useful as a revision aid or a blueprint for writing the full essay later.

This skill is the outline-only sibling of `essay-philosophy`. The source-resolution, position-matching, and theory-rejection logic is identical — only the output form changes.

## Before Writing

1. **Positions** — if the prompt names a course and `/positions/<course>/index.md` exists, read the index. Match each entry's `**Applicable to:**` keywords / module refs against the prompt topic / module. For matched positions, open the named position file for the body. Honour an optional `**Usage:**` line if present (it can redirect how the position is deployed — e.g. as an alternative theory after the canon, not as the conclusion).

2. **Resolve sources** — see the dedicated section below. Same three layers as essay-philosophy (prompt explicit refs; course MD `**Sources:**` and `**Readings:**`; book-index reverse mode). Read only the cited line/page ranges; never whole books.

3. **Check for provided direction** (in priority order):
   - **Outline given in the prompt?** Follow that structure — but render it in outline form (this skill's output style), not as prose.
   - **Opinion / position in the prompt?** Make Theory N that view (overrides any user position and any `**Usage:**` hint).
   - **Specific argument given?** Follow it precisely.
   - **No prompt direction, but a matched position from `/positions/<course>/`?** Theory N is that position — unless the matched file's `**Usage:**` redirects it.
   - **No direction at all?** Theory N is the analytic-mainstream view.

   **Precedence**: prompt direction > matched position's `**Usage:**` > default ("matched position = conclusion") > mainstream fallback.

## Output Format

The outline is markdown. The first line is `# <question>` (verbatim from the prompt's `# Question` body), one blank line, then a `**Thesis**:` line, then sectioned bullets.

**Word count**: target ~300 words, **hard cap 1400**. Models tend to overshoot — aim low and trim. If a draft lands above 400, trim before delivery (see Step 5).

**Style for bullet content**: short clauses. Not bare noun-phrases ("Russell's view"), not full sentences with all the connective tissue ("Russell argues, in his famous 1905 paper, that..."). Aim for the middle: `Russell: descriptions are quantifier phrases, not referring expressions`. One clause per bullet. A bullet that needs more than two short clauses should usually become two bullets.

**Citations**: Cite only authors of attached PAPERS. General books (like "Introduction to ...") don't need citations because their content is  usually canonical.

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
- ...
- ...
  - ...
  - ...
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

### Notes on the skeleton

- **Theory-rejection is the default.** best for epistemology, logic, philosophy of language, modern metaethics. For historical-position or single-theory topics, collapse to: present the theory, raise the objection(s), assess.
- **Argue rivals honestly.** When Theory N is set by a user position, the rival theories must still be presented in their strongest form, with the genuine objections — strawmanning is as visible in an outline as in prose.
- **Not every theory needs the same depth.** A weaker rival can be one best-case bullet and a single decisive objection. The preferred theory deserves the most rows.
- **Verdicts can be partial; acceptance comes in degrees.** A rival does not have to be outright refuted — it can be partly right, and the closing verdict bullet should reflect that (e.g. `partly right: X holds, Y fails because...`). Theory N does not have to win cleanly either: it can stand because it has the **fewest or least decisive problems**, not because every objection has a knockdown reply. When this is the honest read, write the verdict bullet that way (`stands on balance: fewer/less decisive problems than rivals`) rather than forcing a clean win. The conclusion section then ties back accordingly — preferred-on-balance, not proven.
- **No filler.** If a theory has no real reply to an objection, omit the reply bullet. If there is no counter because the reply succeeds (preferred theory), say so in the verdict bullet.
- **Length target**: roughly 30–60 bullets total across all sections. A revision-density artefact, not a 200-bullet exhaustive map.

## Output Path

Same template as essays, but under `outlines/`:

`/courses/<course>/outlines/<moduleId>-<moduleName-slug>/<questionSlug>.md`

- `<course>` — frontmatter `course:` from the prompt.
- `<moduleId>` and `<moduleName>` — looked up from the matching `## <N>. <Name>` heading in `/courses/<course>/index.md`. Slugify the name: lowercase, non-alphanumerics → `-`, collapse, trim.
- `<questionSlug>` — frontmatter `slug:` from the prompt; if absent, derive a 2–5 word slug from the question.
- Extension `.md`. No frontmatter in the file.

**Required: `course:` must be set in the prompt.** If absent, reply with one line saying so and stop. No draft, no clarifying question.

**Fallback for missing module**: save to `/courses/<course>/outlines/_unfiled/<questionSlug>.md`.

**Existing file → overwrite.** Re-running the same prompt replaces the previous outline.

After saving, print the outline to chat and report `Saved to: <path>` on the final line.

## Source Resolution

Identical to essay-philosophy. Three layers, all merging:

1. **Exam prompt** — explicit free-text refs in the prompt (e.g. `(Huemer UK 10.4.2)`). Always resolved and read.
2. **Course MD per-module** — `/courses/<course>/index.md`:
   - `**Sources:**` — canonical backbone, always loaded. If a module has none, fall back to the canonical analytic position from general knowledge (no fabrication of quotes, page refs, or specific arguments).
   - `**Readings:**` — deepening additions, loaded when present, each typically becoming one rejected-theory or supporting branch in the outline. If unresolvable but the named author is canonical, invoke their standard view from general knowledge — never fabricate.
3. **Book index reverse mode** — `/sources/<book>/index.md`. Two surfaces:
   - `- Source <ref> for <topic>` bullets are **hard**: a topic match means read the section's range as canonical evidence.
   - `**Topics:**` bullets are **soft**: a match flags the chapter as a candidate. For a topic-only prompt, propose to the user with layer-of-origin labelled before reading.

### Resolution algorithm

1. Read `/sources/catalog.yaml`. If course is set, read `/courses/<course>/index.md` and identify in-scope books (frontmatter `books:` plus optional `**Books:**` override under the named module). Note any `**Essay scope:**` and `**Usage:**` blocks.
2. For each free-text ref, tokenise → identify author, book, section. Open the book's `index.md` (or `index-ch<NN>.md` for split-layout books — see CLAUDE.md). Find the section heading whose ref matches; read the trailing range marker (`[<a>-<b>]` for line ranges, `[pp. <a>-<b>]` for PDF page ranges).
3. Read only that range: `Read(path, offset=start, limit=end-start+1)` for MD/TXT/HTML; `Read(path, pages: "<start>-<end>")` for PDF. Never read whole books.
4. If multiple candidates match, ask before reading.
5. Cache resolved content for the session keyed by the original ref string. Cache per-book index reads too.
6. If a ref is unresolvable, note it in a one-line preface before writing — don't silently drop it.

### Topic-only prompts

If the prompt names a topic without a source, aggregate candidates:
- Layer 1: explicit refs (none).
- Layer 2: matching module's `**Sources:**` + `**Readings:**`.
- Layer 3: in-scope books' `Source` bullets (hard) and `**Topics:**` bullets (soft).

Deduplicate, propose to the user with each candidate's layer-of-origin and surface (Source / Reading / Topics-only / book-prose), confirm, then read.

### What NOT to do

- Never read a whole book or whole chapter when a section was named.
- Never load a book's `index.md` if the book is out-of-scope and not explicitly cited.
- Never invent a citation key or section number that the index doesn't have.
- Never fabricate a quote, page number, or specific argument when falling back to general knowledge.

## Depth and Scope

- **Target level**: a sharp undergraduate who knows the main and most well-known arguments.
- **Opinionated**: take a position; an outline that just lists views without ranking them is not what this skill produces.
- **Avoid obscurities** — no advanced or unusual positions unless the prompt explicitly calls for them.

## Process

```
STEP 1: UNDERSTAND THE TASK
  □ Parse the question
  □ Note any provided outline / position / argument
  □ Identify course + module from the prompt frontmatter

STEP 2: RESOLVE POSITIONS AND SOURCES
  □ If course is set, read /positions/<course>/index.md and match
    **Applicable to:** triggers; open matched position files
  □ Read /sources/catalog.yaml
  □ Read /courses/<course>/index.md; note **Essay scope:** and **Usage:**;
    load matching module's **Sources:** + **Readings:**
  □ Apply layer-3 reverse-mode (book-index Source bullets hard, Topics soft)
  □ For topic-only prompts, propose candidates and confirm
  □ Resolve refs → read only the resolved ranges

STEP 3: PLAN THE ARGUMENT
  □ Thesis (provided / matched position / mainstream default)
  □ Theories to reject and order
  □ For each: the strongest formulation, the decisive objection(s),
    any defenders' replies, and why the replies fail
  □ For Theory N: the alleged objections and the conclusive replies

STEP 4: WRITE THE OUTLINE
  □ First line: # <question> verbatim from the prompt
  □ Blank line, then **Thesis**: line
  □ Background section (terse)
  □ One section per theory (rejected ones first, preferred last)
  □ Conclusion section (one bullet per theory)
  □ Bullets are short clauses — not nouns, not sentences
  □ Cite sources at first use within each block, refs allowed
    (e.g. (Huemer UK 10.4.2))

STEP 5: CHECK
  □ Thesis stated up front
  □ Rivals presented honestly (not strawmanned)
  □ Decisive objection on every rejected theory
  □ Conclusive reply on every alleged objection to Theory N
  □ Resolved-source content actually used (not just cited)
  □ No source loaded that wasn't referenced
  □ Roughly 30–60 bullets total (revision density, not exhaustive)
  □ Bullets read as short clauses, not bare nouns or full sentences

STEP 6: SAVE & DELIVER
  □ Construct path: /courses/<course>/outlines/<moduleId>-<moduleName-slug>/<questionSlug>.md
  □ Look up moduleId + moduleName from /courses/<course>/index.md
  □ Overwrite if a file exists
  □ If no course in prompt: reply with one line ("This skill requires
    `course:` in the prompt frontmatter."), stop
  □ If no module resolvable: save under .../outlines/_unfiled/<questionSlug>.md
  □ Print the outline to chat
  □ Final reply line: Saved to: <path>
```

## Quality Checklist

- [ ] First line is `# <question>` verbatim, then blank line
- [ ] `**Thesis**:` line stated up front
- [ ] Background section is terse (definitions, distinctions, assumptions)
- [ ] One section per theory; rejected theories first, preferred last
- [ ] Each rejected theory presents the claim, the best-case formulation, at least one objection (with reply + counter where defenders have a reply), and a closing verdict bullet
- [ ] Preferred theory presents the claim, why it works, alleged objections with conclusive replies, and a closing verdict bullet
- [ ] Conclusion section has one bullet per theory tying back to thesis
- [ ] Bullets are short clauses — not bare nouns, not full prose sentences
- [ ] Source refs included where relevant (e.g. `(Huemer UK 10.4.2)`); cited once per theory block
- [ ] Resolved-source content actually used, not just cited
- [ ] No source loaded that wasn't referenced
- [ ] Rival theories argued honestly; no strawmanning
- [ ] No advanced or obscure material unless the prompt asked for it
- [ ] Roughly 30–60 bullets total
- [ ] Saved to `/courses/<course>/outlines/<moduleId>-<moduleName-slug>/<questionSlug>.md` (or fallback), printed to chat, final reply line reports `Saved to: <path>`
