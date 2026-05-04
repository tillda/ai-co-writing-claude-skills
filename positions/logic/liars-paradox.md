---
course: logic
---

# Liars Paradox

My solution to the liar paradox: liar sentence (L: This sentence is false) fails to express a proposition due to an inconsistency built into our language. As a result, premise 2 in the paradoxical reasoning – "L says that L is false" – is false.

Proposition S can be identified by their truth conditions. The liar sentence, "L: This sentence is false" L is supposed to express some (unique) proposition, and it is also intended to assert that that very proposition is false. This can't be satisfied - of course there is no such proposition. So L lacks any determinate meaning.

Why Tarski's hierarchy is not the right solution. Tarski rejects a general truth predicate and replaces it with a hierarchy: truth₁ for first-order sentences, truth₂ for second-order, and so on. The Liar then cannot be formulated, because it has no determinate order. But this view fails on several counts:

- **Other semantic words generate parallel paradoxes.** "Refer" gives us R: "the smallest natural number not referred to by this expression". "Ascribe" and "assert" give analogous puzzles. Tarski would have to deny general relations of referring, ascribing, and asserting — not just a general property of truth. Implausible.
- **We plainly use "true" across orders.** "Everything you just said is true", said of a mixed batch of first-order and second-order claims, is intelligible and correct. There clearly is something the truthₙ predicates have in common, and we evidently grasp the fully general notion.
- **The theory cannot state itself.** A theory that talks about the whole hierarchy of orders has no order itself, so no truth predicate applies to it. Tarski's solution cannot claim to be true on its own terms.
- **The truth_N patch is insufficient.** Quantifying over the n's gives us a predicate covering all ordered sentences, but Liar-style sentences would simply migrate to that level. The hierarchy never closes.

**Applicable to:** The Liar paradox, Tarski's hierarchy, semantic conception of truth, T-schema
