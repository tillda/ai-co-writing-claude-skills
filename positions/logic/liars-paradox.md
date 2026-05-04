---
course: logic
---

# Liar's Paradox

## The paradox in formal terms

Sentence L: *This sentence is false*.

1. If a sentence says that *a* is *F*, then the sentence is true if and only if *a* is *F*. (Premise — the T-schema.)
2. L says that L is false. (Premise.)
3. Therefore, L is true if and only if L is false. (From 1, 2.)
4. L is either true or false. (Premise — bivalence.)
5. Therefore, L is both true and false. (From 3, 4.)

The conclusion is contradictory: truth and falsity are incompatible by definition. Solutions divide on which premise to reject. Three-valued and paracomplete theories deny (4). Dialetheists accept (5) and deny the law of non-contradiction. Tarski and Kripke restrict (1), either by typing the truth predicate or by making it partial. My view rejects (2): there is no proposition for L to be about, so it is not the case that L *says* anything determinate.

## My view

My solution: the Liar sentence (L: *This sentence is false*) fails to express a proposition due to an inconsistency built into our language. So premise 2 in the paradoxical reasoning — "L says that L is false" — is false. There is no proposition for L to be about, hence nothing to be true or false.

A proposition is individuated by its truth conditions. The Liar sentence is supposed to express some unique proposition, and that very proposition is supposed to assert its own falsity. Such a proposition would have to be true iff false. There is no such proposition. So L lacks determinate content. The schema doesn't apply because there's no `<p>` to feed in. The paradox is a defect of the sentence, not of the truth predicate.

This is a *non-formal* solution. It diagnoses the Liar by pointing at a defect in the offered content, rather than restricting the truth predicate or the language. That distinction matters because all formal solutions face revenge — see below.

## Why Tarski's hierarchy is not the right solution

Tarski rejects a general truth predicate and replaces it with a hierarchy: truth₁ for first-order sentences, truth₂ for second-order, and so on. The Liar then cannot be formulated, because no determinate order can be assigned to it. But this view fails on several counts:

- **Other semantic words generate parallel paradoxes.** "Refer" gives us R: *the smallest natural number not referred to by this expression*. "Ascribe" and "assert" yield analogous puzzles. Tarski would have to deny general relations of referring, ascribing, and asserting — not just a general property of truth. Implausible.
- **We plainly use "true" across orders.** "Everything you just said is true", said of a mixed batch of first-order and second-order claims, is intelligible and correct. There clearly is something the truthₙ predicates have in common, and we evidently grasp the fully general notion.
- **The theory cannot state itself.** A theory that talks about the whole hierarchy of orders has no order itself, so no truth predicate applies to it. Tarski's solution cannot claim to be true on its own terms.
- **The truthₙ patch is insufficient.** Quantifying over the n's gives a predicate covering all ordered sentences, but Liar-style sentences would simply migrate to that level. The hierarchy never closes.

For a more sophisticated formal alternative — Kripke's fixed-point construction — and why it is better than Tarski but still not the right answer, see *Kripke's Fixed-Point Theory of Truth*.

## The revenge problem in brief

All formal solutions to the Liar face *revenge*: by introducing a new category to handle the original Liar (a third value, an undefined region, an ordinal level, a paraconsistent glut), they make available fresh vocabulary for a strengthened Liar — *this sentence is in the bad category, or false* — that re-runs the contradiction one level up. The pattern is so consistent across surveyed solutions that a general claim is plausible: any consistent theory of truth expressively rich enough to be interesting will face a revenge paradox. For the systematic version of this argument and the survey across solutions, see *Liar's Paradox: Revenge*.

The no-proposition view escapes revenge because it is not a formal solution. It does not introduce a new *category* of sentence; it offers a *diagnosis* of content-defect. There is no formal predicate "expresses no proposition" inside the theory for revenge to retarget. Revenge constructions like L*: *L\* expresses no proposition, or is false* receive the same diagnosis: their supposed content is incoherent for the same reason the original Liar's is, so they too fail to express a proposition. No new vocabulary is introduced, no new self-reference is enabled, no contradiction at a higher level. The defect is recognised wherever it occurs, without expanding the theory.

That is the structural advantage of stepping outside the formal-solution paradigm.

## Honest objections to the no-proposition view

1. **"You are just stipulating that there is no such proposition."** No: the proposition the Liar would have to express is one true iff false. The schema rules this out — being true and being false are exclusive, so no proposition can satisfy both conditions. The non-existence is a consequence of the meanings of "true" and "false", not a stipulation.

2. **"What about the Strengthened Liar, *this sentence is not true*?"** Same diagnosis. *This sentence is not true* purports to express a proposition that is true iff not true. No such proposition exists. The "not true" formulation, like the "false" formulation, is content-defective.

3. **"Doesn't this make you a sceptic about a host of self-referential sentences?"** Some, yes — those whose supposed content is incoherent. Many self-referential sentences (Quine sentences, Gödel sentences, ordinary "this sentence has five words") are perfectly meaningful because their supposed content is consistent. The no-proposition diagnosis applies only where the content would be incoherent.

4. **"This is suspiciously close to refusing to engage with the paradox."** It is a refusal — but a principled one. The schema independently rules out the proposition the Liar is supposed to express. The refusal is not "I won't play"; it is "there is nothing to play with". The Liar's apparent meaningfulness is grammatical, not propositional.

## Considered view

The Liar sentence does not express a proposition. The schema therefore does not apply to it; no contradiction arises. Tarski's hierarchical solution misdiagnoses the problem and is independently implausible. Kripke's fixed-point construction is a substantial improvement on Tarski but still gives the wrong diagnosis (truth-valueless rather than content-defective) and faces revenge — see *Kripke's Fixed-Point Theory of Truth*. All formal solutions face revenge of essentially the same shape; the no-proposition diagnosis avoids it because it is not a formal solution — see *Liar's Paradox: Revenge*.

The slogan: the Liar is not a logical problem; it is a linguistic mishap. Languages can have their own truth predicate. What they cannot have is sentences that successfully express incoherent propositions, because no such propositions exist.

**Applicable to:** the Liar paradox, Tarski's hierarchy, semantic conception of truth, T-schema, "can a language contain its own truth predicate", *logic / 2. Truth*
