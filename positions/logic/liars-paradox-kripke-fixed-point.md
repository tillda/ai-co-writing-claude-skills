---
course: logic
---

# Kripke's Fixed-Point Theory of Truth (better than Tarski, still wrong)

Kripke (*Outline of a Theory of Truth*, 1975) gives the most sophisticated formal treatment of the Liar on the table. He starts with a language *L* containing a partial truth predicate — defined on some sentences and undefined on others — and applies a monotonic "jump" operator: at each stage, declare more sentences true (or false) on the basis of what is already settled. The construction reaches a *fixed point* — a stage at which the truth predicate's extension is stable — and the Liar sentence ends up *ungrounded*: neither in the extension nor in the anti-extension. The truth predicate applies to itself, and the language can talk about its own truth, all without contradiction.

My verdict: Kripke is a clear improvement on Tarski's hierarchy, but he is still wrong, and for two reasons. He gives the wrong *philosophical* diagnosis (the Liar is content-defective, not truth-valueless), and his theory faces revenge. My own preferred treatment is the no-proposition view — see *Liar's Paradox*. This position is about Kripke specifically; for the broader claim about formal solutions and revenge, see *Liar's Paradox: Revenge*.

## The paradox in formal terms

Sentence L: *This sentence is false*.

1. If a sentence says that *a* is *F*, then the sentence is true if and only if *a* is *F*. (Premise — the T-schema.)
2. L says that L is false. (Premise.)
3. Therefore, L is true if and only if L is false. (From 1, 2.)
4. L is either true or false. (Premise — bivalence.)
5. Therefore, L is both true and false. (From 3, 4.)

Kripke's strategy targets (4) and (1) jointly: bivalence is replaced by a partial extension built up monotonically through the fixed-point construction, and the truth predicate is correspondingly partialised so that the schema (1) only applies where the predicate is defined. The Liar then sits outside both the extension and the anti-extension — *ungrounded*. My objection runs at premise (2): even granting the construction, the right diagnosis is that there is no proposition for L to *say* anything about, not that L expresses a proposition with a third semantic status.

## What Kripke gets right

There is a lot to like about the fixed-point construction:

1. **A language can contain its own truth predicate.** This is the headline result. Kripke shows it concretely: we do not need a hierarchy of metalanguages to talk about truth. There is a single, general truth predicate that applies across the language including to its own truth-ascriptions. That is the right verdict, and it answers the question "Can a language coherently contain its own truth predicate?" with a clear *yes*. Tarski had to deny this; Kripke restores it.

2. **The Liar is recognised as semantically defective.** Kripke's "ungrounded" sentences are sentences that never get assigned a truth-value through the iterative construction. This is in the right neighbourhood: it captures something genuine about how Liar sentences fail to engage with the recursive grounding of truth in the world. The construction makes vivid that the Liar's defect is not surface-grammatical — well-formed sentences can fail to ground.

3. **No ad hoc restriction on the truth predicate's syntax.** Unlike Tarski, the truth predicate is a single, general predicate; it just has a partial extension. This is theoretically much cleaner: the syntactic apparatus of the language is not crippled to avoid paradox.

4. **It accommodates the cross-orders intuition.** "Everything you said is true", said of a mixed batch, is intelligible in Kripke's framework because there is one truth predicate doing all the work. Tarski couldn't say this; Kripke can.

These are real virtues. Kripke is the right place to push back from, not Tarski.

## Where Kripke goes wrong

Two complaints — one philosophical, one technical.

**1. He gives the wrong diagnosis: truth-valueless rather than content-defective.**

Kripke classifies the Liar as "ungrounded" — not in the extension of "true", not in the extension of "false". The Liar sentence is treated as a perfectly meaningful sentence that happens to lack a truth-value. The diagnosis is: "L expresses a proposition; that proposition has no truth-value because the construction never assigns one."

My view: L doesn't *fail to be true or false*; it fails to express a proposition at all. The grammatical surface is well-formed; the content is empty. Treating L as a meaningful sentence with a truth-value gap concedes too much to the Liar — it grants the sentence semantic standing it does not have. The right diagnosis is non-formal: there is no proposition that is true iff false (the schema rules this out), and L purports to express such a proposition, so L expresses no proposition.

This is a substantive disagreement, not a verbal one. Kripke is committed to a third semantic status (ungrounded) that takes its place in the formal apparatus alongside true and false. The no-proposition view denies any third status: there are sentences that successfully express propositions (true or false), and there are sentences that fail to express propositions at all. The "ungrounded" category is a formal artefact of trying to give the Liar a place inside a logic, when what we should say is that the Liar has no place because there is no content for the schema to apply to.

**2. The theory faces revenge.**

This is the decisive technical complaint. Once Kripke has drawn the line between "true", "false", and "ungrounded", we can form a strengthened Liar that exploits the new category:

> L*: *L\* is not true (in any fixed point)*

— or equivalently, *L\* is false or ungrounded*. If L* is true, it is true at some fixed point, but then the construction makes it false or ungrounded — contradiction. If L* is false or ungrounded, then what L* says obtains, so L* is true after all.

Kripke's apparatus has no internal way to say "ungrounded" while remaining stable; the moment we ascend to a perspective from which the construction is described, revenge re-targets the new vocabulary. This is the standard revenge problem applied to the fixed-point theory specifically — see *Liar's Paradox: Revenge* for the systematic claim that this happens to all formal solutions.

The first complaint is independent of the second: even if we could repair the revenge problem (Field's recent work attempts this for Kripke-style theories), the philosophical diagnosis would still be wrong. And the second is independent of the first: even if Kripke's diagnosis were on the right lines, the theory would fail technically.

## "Does Kripke's fixed-point construction give a better treatment than Tarski's hierarchy?"

Yes — substantially better. Three points of comparison:

- **Single truth predicate.** Kripke has it; Tarski doesn't. This is the most important methodological win.
- **Self-applicability.** Kripke's truth predicate applies to its own ascriptions; Tarski's cannot. Kripke vindicates the natural-language fact that we do this routinely.
- **Cross-orders quantification.** Kripke handles "everything you said is true" naturally; Tarski needs ad hoc patches.

What Tarski has and Kripke doesn't: technical simplicity. The hierarchy is easier to formalise; Kripke's fixed-point construction is mathematically intricate (Kleene three-valued logic, monotonic jump operators, transfinite iteration). But that is a cost of doing the job properly, not a virtue of Tarski's.

So Kripke wins the comparison decisively. But "better than Tarski" is a low bar; it does not entail "right". My view: the right treatment of the Liar is non-formal, and Kripke's improvement on Tarski is an improvement *within* the formal-solution paradigm whose limits the no-proposition view exposes.

## Honest objections

1. **"You're being unfair to Kripke — the construction is intentionally restricted to a particular formal language, not a general theory of natural-language truth."** Granted, Kripke is more modest than the more ambitious dialetheist or paracomplete projects. But (a) the construction is presented as a model of how natural-language truth could work, and (b) the philosophical diagnosis (Liar = ungrounded) is meant to apply at the philosophical level too. The complaints target the philosophical reading; the formal construction itself is mathematically unimpeachable.

2. **"The 'wrong diagnosis' complaint is question-begging — you assume the no-proposition view to argue against ungroundedness."** Partly fair. The complaint is that the *natural reading* of the construction commits Kripke to a third semantic status, and that this is more theoretical machinery than the situation calls for. The no-proposition view is preferable on grounds of parsimony (no third status) and of fit with the schema (we already deny that there's a proposition true iff false). The argument is comparative, not deductive.

3. **"Field's later work plugs the revenge hole."** Field (*Saving Truth from Paradox*, 2008) attempts a fixed-point-style theory with a determinately-true operator that purports to escape revenge. Whether it succeeds is contested; many think it generates a revenge variant of its own. I leave this open: even granting that some Kripke-style theory eventually escapes revenge, the philosophical diagnosis (truth-valueless rather than content-defective) is the deeper problem.

4. **"The fixed-point construction has independent technical interest beyond the Liar."** True. Kripke-style fixed points are useful in semantics, knowledge representation, and the theory of partial functions. Nothing in this position objects to the formal apparatus as such; the objection is to its deployment as a *theory of truth*.

## Considered view

Kripke's fixed-point construction is the most successful formal treatment of the Liar to date. It correctly establishes that a language can contain its own truth predicate, and it correctly identifies that the Liar is semantically defective. But it gives the defect the wrong status (truth-valueless rather than content-defective) and faces revenge. The right response is to abandon the formal-solution paradigm and accept the no-proposition diagnosis — see *Liar's Paradox*.

The slogan: Kripke wins the formal arms race against Tarski, but the formal arms race is the wrong race. The Liar is a defect in proposition-expression, not a third semantic status to be modelled.

**Applicable to:** Kripke fixed-point theory of truth, Kripke's *Outline of a Theory of Truth*, fixed-point construction, ungrounded sentences, partial truth predicate, monotonic jump operator, Kleene three-valued logic, three-valued treatment of the Liar, "can a language coherently contain its own truth predicate", Kripke vs Tarski on truth, "does Kripke's fixed-point construction give a better treatment of the Liar than Tarski's hierarchy", *logic / 2. Truth*
