---
name: essay-philosophy
description: Write undergraduate-level analytic philosophy essays. Use when the user asks for a philosophy essay, timed essay, or exam-style philosophical writing.
---

# Philosophy Essay Writer

Write clear, well-argued analytic philosophy essays at undergraduate level for a UK programme.

## Before Writing

1. **Read context profiles**:
   - `/context/voice-dna.json` — match voice throughout
   - `/context/icp.json` — understand what the examiner values and penalises

2. **Check for provided sources** — if the user attaches or points to a document, read it. The author MUST be mentioned in the essay.

3. **Check for provided direction**:
   - **Outline given?** Follow it as the essay structure.
   - **Opinion/position given?** Argue in line with it.
   - **Specific argument given?** Follow that argument precisely.
   - **No direction?** Default to the common mainstream position in analytic philosophy.

## Format

- **Word count**: ~1200 words (unless specified otherwise)
- **Thesis**: State clearly in the opening paragraph. This is a significant bonus.
- **Structure**: Introduction (with thesis) → body sections → conclusion. Follow provided outline when one is given.

## Referencing

This is a timed essay context — no full formal referencing required.

- **Mentioning philosophers**: Name major figures when relevant (e.g., Tarski, Horwich, Quine), but only when their view is actually being engaged with — do not name-drop without purpose.
- **Provided sources**: If the essay draws on a document the user provided, the author MUST be mentioned.
- **Direct quotes**: Enclose in quotation marks and mention the author. But direct quoting is rarely necessary — paraphrase instead.
- **Format**: Informal in-text mentions are sufficient (e.g., "As Horwich argues, ..." or "On Tarski's account, ...").

## Depth and Scope

- **Target level**: A sharp, enthusiastic undergraduate who grasps the main and most well-known arguments in analytic philosophy.
- **Opinionated positioning**: Show genuine engagement — take a position and argue for it, rather than neutrally surveying views.
- **Do NOT** dig into advanced academic opinions or obscure digressions that would be unusual for an undergraduate to encounter through normal study. This looks suspicious rather than impressive.
- **Non-standard arguments**: Only include when the question explicitly calls for them and specifies which ones to use.

## Writing Style

- **Use voice DNA** from `/context/voice-dna.json` throughout.
- **Weave formal arguments with accessible explanations** — do not sustain dry, purely formal academic prose for long stretches. A formal argument (numbered premises, conclusion) should be followed or preceded by a clear explanation of what it shows and why it matters.
- **Show understanding of WHY** — not just what positions exist, but what supports them and what can be said against them.
- **Inclusive "we"** — reason alongside the examiner ("We can see that...", "Suppose we accept...") rather than addressing them as "you".

## Essay Structure Guidelines

### Default Argumentative Structure

Analytic philosophy essays typically follow a tree structure that surveys competing theories, refutes them in turn, and arrives at the preferred position last. Use this as the default when no outline is provided:

```
1. INTRODUCTION
   - State the question or topic
   - Declare the thesis clearly
   - Briefly preview the argumentative direction

2. BACKGROUND
   - Key definitions, distinctions, assumptions
   - Set up the problem precisely

3. THEORY 1 (a theory to be rejected)
   - Present it in its strongest form
   - Objection 1 (counterexample, false assumption, etc.)
       → Possible reply from the theory's defenders (if any)
   - Objection 2
       → Possible reply (if any)
   - Assessment: refuted or seriously contested because of objection(s) X, Y

4. THEORY 2 (another theory to be rejected)
   - Present it in its strongest form
   - Objection 1
       → Possible reply (if any)
   - Objection 2
       → Possible reply (if any)
   - Assessment: refuted or seriously contested because of objection(s) X, Y

   [... repeat for further theories as needed ...]

5. THEORY N (the preferred theory — always presented last)
   - Present it clearly
   - (Alleged) Objection 1
       → Reply that is considered conclusive in favour of Theory N
   - (Alleged) Objection 2
       → Reply that is considered conclusive in favour of Theory N

6. CONCLUSION
   - Re-state the weaknesses of Theories 1 through N-1
   - Re-state the reasons for accepting Theory N
   - Do not introduce new arguments
```

### When to Use This Structure

- **Best suited for**: Epistemology, logic, philosophy of language, modern metaethics, or any topic involving formal theories with competing positions.
- **Less suited for**: Historical positions, historical ethics — these often require a different approach (e.g., exposition of a thinker's view, then critical assessment).
- **Sometimes suitable**: Less formal topics where only one theory is under discussion. In that case, the structure collapses to: present the theory, raise objections, assess whether the replies succeed.

### Notes on Using This Structure

- **If the user provides an outline, follow that instead.** This default structure applies only when no outline is given.
- **Not every theory needs the same depth.** A weaker theory can be dispatched briefly; the preferred theory deserves the most careful treatment.
- **Use concrete examples from ordinary life** to illuminate abstract points where possible.

## Process

```
STEP 1: UNDERSTAND THE TASK
  □ What is the question asking?
  □ Is there a provided outline? → follow it
  □ Is there a provided position/theory? → argue in line with it
  □ Is there a provided source document? → read it, note the author

STEP 2: LOAD CONTEXT
  □ Read /context/voice-dna.json
  □ Read /context/icp.json

STEP 3: PLAN THE ARGUMENT
  □ Identify the thesis (provided or mainstream default)
  □ Identify which theories to reject and in what order
  □ For each rejected theory: what are the decisive objections?
  □ For the preferred theory: what are the alleged objections, and why do the replies succeed?
  □ Map to provided outline, or use the default argumentative structure (rejected theories first, preferred theory last)

STEP 4: WRITE
  □ Open with clear thesis
  □ Argue through the body — reasons, not just descriptions
  □ Weave formal arguments with explanations
  □ Mention relevant philosophers naturally
  □ Close with a conclusion that ties back to the thesis

STEP 5: CHECK
  □ ~1200 words?
  □ Thesis stated at the beginning?
  □ Arguments supported with reasons, not just asserted?
  □ No suspicious advanced material?
  □ Provided source author mentioned?
  □ Voice DNA matched?
  □ Not too dry for sustained stretches?
  □ Follows provided outline (if any)?
```

## Quality Checklist

Before delivering:

- [ ] Thesis is clearly stated in the opening paragraph
- [ ] Essay addresses the question directly — not a related-but-different topic
- [ ] Arguments are supported with reasons, not just asserted
- [ ] Strongest objection is raised and addressed
- [ ] Depth is appropriate — sharp undergraduate, not postgraduate
- [ ] No advanced or obscure material unless the question explicitly calls for it
- [ ] Formal arguments are explained, not left as dry notation
- [ ] Voice matches voice DNA
- [ ] Authors of provided sources are mentioned
- [ ] ~1200 words
- [ ] Follows provided outline if one was given
