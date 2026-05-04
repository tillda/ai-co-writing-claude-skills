---
course: logic
---

# Liar's Paradox: Revenge and the Limits of Formal Solutions

Revenge is the general phenomenon whereby a formal solution to the Liar paradox, by introducing a new category to handle the original Liar, opens itself up to a strengthened Liar that targets the new category. The pattern is so consistent across solutions that the slogan in the title of Beall's edited volume is widely accepted: *any consistent theory of truth that is expressively rich enough to be interesting will face a revenge paradox*.

I think the slogan is right — for *formal* solutions. Any solution that introduces new semantic vocabulary to classify the Liar will face a revenge variant in that vocabulary. The way out is non-formal: my own preferred treatment of the Liar (see *Liar's Paradox*) holds that the Liar sentence fails to express a proposition at all. That is not a category for revenge to retarget; it is a philosophical diagnosis of content-defect, and content-defects do not have the level-structure that revenge exploits.

## The paradox in formal terms

Sentence L: *This sentence is false*.

1. If a sentence says that *a* is *F*, then the sentence is true if and only if *a* is *F*. (Premise — the T-schema.)
2. L says that L is false. (Premise.)
3. Therefore, L is true if and only if L is false. (From 1, 2.)
4. L is either true or false. (Premise — bivalence.)
5. Therefore, L is both true and false. (From 3, 4.)

Most formal solutions reject (4): bivalence is broken by a third value, an undefined region, an ordinal level, or a paraconsistent glut. The new category enriches the language, and the strengthened Liar exploits that enrichment by referring to its own membership in the new category. That is the structural source of revenge, and the topic of this position. (Solutions that instead restrict (1) — Tarski's hierarchy — face a different revenge route, via quantification over the levels of the truth predicate.)

## What is revenge?

A revenge paradox is a strengthened Liar that targets the resources a proposed solution uses. The pattern:

1. A theorist proposes that the Liar belongs to category C (a third value, an undefined region, an ordinal level, a paraconsistent glut, an indeterminacy zone).
2. We ascend to a perspective from which we can talk about C.
3. We construct L_C: *L_C is in C, or false (not true)*.
4. The same paradox arises one level up.

The key move is step 3: by being articulable in the theory's own vocabulary, the new category is available for fresh self-reference, and the original paradoxical structure (a sentence whose content forces it to be true iff not true) replays in the new setting.

## Survey of solutions and their revenge variants

- **Tarski's hierarchy.** Solution: each language *L_n* has its own truth predicate truth_n; no language contains its own truth predicate. Revenge: quantify over all levels — "this sentence is not true at any level". Either the level-quantifying language has a truth predicate (then the Liar reappears) or it doesn't (then the theory cannot state itself).

- **Kripke's fixed-point theory.** Solution: the Liar is *ungrounded* — neither true nor false in any fixed point. Revenge: *this sentence is not true (in any fixed point)*. If true, the construction would assign truth, but then it says it is not — contradiction. If untrue, it is true after all.

- **Three-valued / paracomplete theories** (Soames, early Field). Solution: the Liar takes a third value (gap, undefined, neither). Revenge: *this sentence is gappy or false*. The strengthened Liar plays the same trick using the new value.

- **Paraconsistent / dialetheic theories** (Priest, LP). Solution: the Liar is both true and false (a "glut"). Revenge: *this sentence is false-only, not also true*. If true-only, then it says it isn't, contradicting itself; if false-only, then it really is false-only as it says, which is being-true; if both, then it isn't false-only, contradicting itself. The dialetheist's apparatus has no coherent place for it.

- **Field's recent paracomplete theory** (*Saving Truth from Paradox*, 2008). Solution: a sophisticated determinately-true operator that purports to handle revenge by being itself non-classical at higher levels. Some critics think a revenge variant for "determinately determinately... true" still arises; the debate is technical and ongoing. Even if Field eventually escapes, the cost is enormous expressive complexity.

- **Contextualist theories** (Glanzberg, Simmons). Solution: the Liar's truth-value is context-relative; in different contexts it gets different values. Revenge: a sentence that asserts of itself that it is untrue in *every* context. The revenge re-targets the contextualist's quantification over contexts.

The pattern is not accidental. Each new formal apparatus introduces a vocabulary in which the paradoxical sentence can be redescribed, and self-reference plus the schema is enough to force contradiction in the new vocabulary.

## Why is revenge so resilient?

The structural reason: paradox arises from self-reference plus the equivalence schema. Any new category sufficient to *mark* the paradoxical sentences is, by being expressively available in the theory, *also* available for new self-reference. So:

- If the theory talks about the new category at all (and it must, to state the solution), the category appears in the language.
- If the category appears in the language, sentences can refer to themselves as belonging to it.
- A sentence that refers to itself as being in the bad category, plus the schema, generates the same contradiction one level up.

This is not a contingent fact about particular solutions; it is a structural feature of how formal solutions interact with self-reference. The only way to block it is to deny the schema (a high cost) or to deny the legitimacy of the strengthened Liar's self-reference (which requires either ad hoc syntactic restrictions or a non-formal diagnosis).

## Why the no-proposition view escapes

The no-proposition view does not introduce a new *category* of sentence. It introduces a *defect*: failure to express a proposition. The difference is structural:

1. **No new formal vocabulary.** "Expresses a proposition" is not a formal predicate inside a theory of truth; it is a philosophical observation about what propositions there are. We do not have a formal predicate "expresses no proposition" that the theory commits to applying determinately to all sentences.

2. **The diagnosis applies uniformly.** When someone constructs a strengthened revenge sentence — say L**: *L\*\* expresses no proposition, or is false* — the same diagnosis applies: L** also fails to express a proposition. Why? Because its supposed content, like the original Liar's, would be a proposition true iff false (or true iff "fails to express a proposition", which collapses into the same incoherence given that we have already denied that the failed expression has a truth-value). And there is no such proposition.

3. **No category for revenge to retarget.** Revenge needs a *category* to retarget. There is no formal category here — only a philosophical claim about which sentences successfully express propositions. The claim is applied case-by-case based on whether the supposed content is incoherent. There is no "ungrounded" or "gappy" or "level-restricted" tag inside the theory that can be quantified over and re-used.

The point is that the no-proposition view is *not in the same business* as formal solutions. Formal solutions try to model the Liar inside a logic. The no-proposition view says the Liar is not a logical puzzle at all; it is a linguistic defect. Defects don't have level-structure.

## The "expressively rich enough to be interesting" caveat

The slogan I'm endorsing is qualified: revenge afflicts theories that are *expressively rich enough to be interesting*. There is a way to escape revenge: build a theory so expressively impoverished that it cannot articulate its own solution. (Tarski's untyped hierarchy, in a sense, attempted this — but couldn't state itself.) Such theories escape revenge by escaping interest.

A theory of truth worth having must be able to say things like "the Liar is in category C" — which is just to say it must have the resources to talk about its own classifications. Any such theory has the expressive vocabulary that revenge exploits. So the dilemma is real: expressive richness vs. revenge-immunity.

The no-proposition view sits outside this dilemma because it doesn't have categories at all. It has a *diagnosis* that applies wherever the conditions for proposition-expression fail. Diagnoses don't have the expressive structure that revenge needs.

## Honest objections

1. **"Isn't 'expresses no proposition' itself a category — just an unformalised one?"** Yes and no. It is a category in the loose sense (a way of classifying sentences), but not in the sense relevant to revenge (a formal predicate inside the theory of truth). What revenge exploits is the formal status of categories within a logic — their availability for self-reference inside the system. A philosophical diagnosis applied at the meta-level by a competent speaker is not formal in this sense; the speaker can apply it to any sentence, including revenge constructions, without thereby committing the *theory of truth* to a determinate formal extension for "expresses no proposition".

2. **"This sounds like cheating — you escape revenge by refusing to play the game."** Yes — that is exactly the dialectical point. Formal solutions try to play the game (model the Liar inside a logic); the no-proposition view refuses to play. The question is whether refusing is principled or evasive. I think it is principled because the schema independently rules out the proposition the Liar is supposed to express. The refusal is not "I won't engage"; it is "there is nothing to engage with". The Liar's apparent meaningfulness is grammatical, not propositional.

3. **"Some sophisticated formal solutions claim to escape revenge."** Field's project is the leading example. The technical debate is ongoing. Two responses. First, even if some such solution succeeds, the *general* pattern across the surveyed solutions remains striking. Second, the no-proposition view escapes revenge for a different reason than Field's apparatus tries to: not by clever formal machinery, but by being non-formal. Both responses can be true at once; they are not in competition.

4. **"You owe a story about *why* the no-proposition diagnosis is the right one for the original Liar."** Granted — that is the work done in the *Liar's Paradox* position. This position is only about why formal solutions face revenge and why a non-formal solution avoids it. The two positions complement each other: the *Liar's Paradox* position gives the positive diagnosis; this one explains why formal alternatives fail.

## Considered view

Yes, all formal solutions to the Liar face revenge — at least, every formal solution proposed so far does, and the structural reason makes it likely no formal solution can fully escape. The slogan that any consistent expressively-rich theory of truth faces revenge is essentially correct. The way out is to abandon the formal-solution paradigm and recognise that the Liar sentence is content-defective: there is no proposition it could express, and so the schema does not apply to it.

The slogan: revenge is the right problem for formal solutions and a non-problem for the no-proposition view. If you must fix the Liar inside a logic, expect revenge. If you can step outside the logic and say what the Liar tries and fails to do, the problem dissolves.

**Applicable to:** revenge paradox, revenge problem, strengthened Liar, expressive completeness, limits of formal solutions to the Liar, "any consistent theory of truth that is expressively rich enough to be interesting will face a revenge paradox", "do all formal solutions to the Liar paradox face revenge versions", expressive richness vs paradox-immunity, Field on revenge, Beall on revenge, *logic / 2. Truth*
