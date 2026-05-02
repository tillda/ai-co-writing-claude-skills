---
course: logic
generated: 2026-04-28
---

# Philosophical Positions — Logic (PY1070)

These are my stated leanings on questions in this course. When the prompt is silent on direction, default to these positions as the **conclusion** of the essay. Use the theory-rejection structure honestly: present rival theories in their strongest form, raise the genuine objections to them, then arrive at the position below as the considered view. Do not strawman the rejected positions — the examiner can tell.

When the prompt directs a specific position or argument, follow the prompt; these defaults apply only when the prompt is silent.

## Classical Logic

I am committed to classical logic. The law of non-contradiction, the law of excluded middle, and bivalence are self-evident, near-trivial truths. They reflect the meanings of "and", "or", "not", and "true" — anyone who denies them has misunderstood those words.

The argumentative path:

- **LNC follows from the meaning of negation.** ¬A holds in all and only the situations where A fails. There is no overlap, by definition. A contradiction (A ∧ ¬A) entails two incompatible propositions and is therefore necessarily false.
- **LEM follows by reductio.** Suppose neither A nor ¬A holds. Then it is not the case that A and it is not the case that ¬A — i.e. ¬A ∧ ¬¬A. That is itself a contradiction. So either A or ¬A must hold.
- **Bivalence follows from LEM plus the meanings of "true" and "false".** If a sentence asserts that p, it is true if p and false if ¬p; LEM gives us that one or the other obtains. So any proposition-expressing sentence is true or false.
- **Deviant logics (paraconsistent, three-valued, degree-of-truth) misdiagnose the problem.** Even reasoning about a deviant system requires classical logic to draw out its consequences. And any apparent counterexample to LEM/LNC can be rebuilt with a strengthened operator (Huemer's "not!", defined to exclude both gaps and gluts), reviving the original paradox without using the disputed concept of negation.

Crucial qualification: bivalence and LEM apply only to **proposition-expressing sentences**. A sentence that fails to express a proposition — the Liar, vague sentences in their borderline range — is no counterexample. This is how I can keep classical logic intact while still saying the Liar sentence and "B is a heap" (for borderline B) are neither true nor false. Restricting the *scope* of these laws is a different operation from revising their *content*.

In detail: see Michael Huemer's *Paradox Lost*, Introduction §1.3 and Chapter 3 §3.5.7.

**Applicable to:** classical logic, deviant logics, paraconsistent logic, three-valued logic, dialetheism, law of non-contradiction, law of excluded middle, bivalence, justification of deduction, justification of specific logical laws, *logic / 1. What is Logic?*, *logic / 2. Truth*, *logic / 7. Vagueness*, *logic / 9. The Justification of Deduction*

## Truth Minimalism (Horwich)

I favour Horwich's minimalism about truth:
- truth predicate is governed by the equivalence schema — `<p> is true iff p` . 
- <p> is true if is the case that p and <p> is false if it is not the case that p. Because that is what the predicates true and false mean.
- Truth is not a property in any robust metaphysical sense; the predicate's role is logical (it lets us generalise, e.g. "Everything Plato said is true").

The argumentative path:

- **Correspondence** founders on the obscurity of the "fact" relation. We have no informative account of what makes a sentence correspond to a fact that doesn't itself appeal to truth. 
- **Coherence** faces the fairy-tale objection: a maximally coherent set of beliefs can still be false. Coherence is at best a fallible test for truth, not its nature.
- **Pragmatism** conflates truth with utility; useful falsehoods (and useless truths) are real.
- **Minimalism** explains all the deflationary data (T-schema biconditionals, the generalising role) without metaphysical excess. 

**Applicable to:** truth, T-schema, deflationism, disquotationalism, redundancy theory, "is truth a property", correspondence theory of truth, coherence theory of truth, pragmatist theory of truth, the Liar paradox, *logic / 2. Truth*

## Liars Paradox

My solution to the liar paradox: liar sentence (L: This sentence is false) fails to express a proposition due to an inconsistency built into our language. As a result, premise 2 in the paradoxical reasoning – “L says that L is false” – is false.

Proposition S can be identified by their truth conditions. The liar sentence, "L: This sentence is false" L is supposed to express some (unique) proposition, and it is also intended to assert that that very proposition is false. This can't be satisfied - of course there is no such proposition. So L lacks any determinate meaning.

Why Tarski's hierarchy is not the right solution. Tarski rejects a general truth predicate and replaces it with a hierarchy: truth₁ for first-order sentences, truth₂ for second-order, and so on. The Liar then cannot be formulated, because it has no determinate order. But this view fails on several counts:

- **Other semantic words generate parallel paradoxes.** "Refer" gives us R: "the smallest natural number not referred to by this expression". "Ascribe" and "assert" give analogous puzzles. Tarski would have to deny general relations of referring, ascribing, and asserting — not just a general property of truth. Implausible.
- **We plainly use "true" across orders.** "Everything you just said is true", said of a mixed batch of first-order and second-order claims, is intelligible and correct. There clearly is something the truthₙ predicates have in common, and we evidently grasp the fully general notion.
- **The theory cannot state itself.** A theory that talks about the whole hierarchy of orders has no order itself, so no truth predicate applies to it. Tarski's solution cannot claim to be true on its own terms.
- **The truth_N patch is insufficient.** Quantifying over the n's gives us a predicate covering all ordered sentences, but Liar-style sentences would simply migrate to that level. The hierarchy never closes.

In detail: see Michael Huemer's *Paradox Lost*, Chapter 2 — esp. §2.5 (against Tarski) and §2.6 (the inconsistent-language solution).

**Applicable to:** The Liar paradox, Tarski's hierarchy, semantic conception of truth, T-schema


## Supervaluationism

I do not like Supervaluationism because of it’s need to reject the T-schema. 

The T-schema says that, in general, if a sentence asserts p, then the sentence is true if and only if p (in symbols: T\langle p\rangle \leftrightarrow p). The supervaluationist holds that, if B is a borderline case of a heap, then “B is a heap” is not true, and “B is not a heap” is not true. Given the T-schema (and given that “B is a heap” asserts that B is a heap and “B is not a heap” asserts that B is not a heap), this implies that B is not a heap, and it is not the case that B is not a heap. But that is an explicit contradiction, a statement of the form “p and not-p”. To avoid this, the supervaluationist would have to reject the T-schema. 

The T-schema, however, is a fundamental principle about the meaning of “true” in English. We should therefore reject supervaluationism rather than reject the T-schema.

Further problems with supervaluationism:

- **A disjunction comes out true with no true disjunct.** “B is a heap or B is not a heap” is supertrue (true on every precisification), yet neither disjunct is supertrue. That is a strange thing to say a disjunction is. We thought disjunction-truth just meant at-least-one-disjunct-truth.
- **Vagueness merely relocates.** Replacing one vague boundary (between true and false) with two (between true / neither / false) is hardly progress. Second-order vagueness reproduces the puzzle one level up.
- **The theory is self-undermining.** On any acceptable precisification, “heap” is precise — that is what precisification means. So “'heap' is precise” is supertrue, hence true on the theory. But supervaluationists themselves think “heap” is vague. The theory judges its own central claim false.
- **It requires deviant logic** (rejection of bivalence), which I independently reject (see *Classical Logic* above).

In detail: see Michael Huemer's *Paradox Lost*, Chapter 3 §3.3.

**Applicable to:** The Sorites paradox, Supervaluationism, vagueness, borderline cases, excluded middle under vagueness

## Sorites Paradox

My solution follows Huemer's "moderate nihilism": vague sentences fail to express propositions. The underlying reality is that mental states have continuous **satisfaction profiles** — they fit the world to a degree, not in a binary "satisfied / unsatisfied" way. Imputing a propositional content to such a state is loose talk; the proposition is at best an approximation. The sorites is what happens when we try to force a continuous fit into the discrete categories of true and false.

The argumentative path:

- **Vague sentences cannot express precise propositions** (else they would not be vague). They cannot express vague propositions either: vagueness is purely semantic, so there are no vague properties, vague objects, or vague propositions. Hence vague sentences express no proposition at all.
- **The sorites premises lack truth-values strictly speaking.** "If n grains are a heap, then n − 1 are a heap" and "1,000,000 grains are a heap" both fail to express propositions. Modus ponens preserves strict truth, but there is no strict truth here to preserve. The argument's absurd conclusion is therefore unsurprising — it is no genuine modus ponens chain.
- **Classical logic is preserved.** Logic applies only to proposition-expressing sentences. LEM and bivalence are not threatened by sentences that fail to express propositions — just as "Blug or not blug" is no counterexample to LEM.
- **Ordinary use of "true" is loose.** "There is a heap of sand in the yard" is "truthy" — close enough to expressing a true proposition for practical purposes. We use this loose sense ubiquitously without confusion. The sorites trick exploits the gap: it applies the logical rules valid for strict truth to mere approximations, and the approximation breaks down under iteration.
- **Why I reject the rivals.** Embracing the conclusion (no heaps, or every quantity a heap) is absurd. Epistemicism (a precise hidden cutoff) cannot explain what would *make* a particular cutoff correct, given that meaning is fixed by usage and our usage settles no such cutoff. Supervaluationism fails for the reasons given above. Deviant logic is the wrong move.

In detail: see Michael Huemer's *Paradox Lost*, Chapter 3 — esp. §3.5 (the moderate nihilist solution) and §3.5.11 (strict truth vs. truthiness).

**Applicable to:** The Sorites paradox, vagueness, borderline cases, propositional content, degrees of truth, epistemicism