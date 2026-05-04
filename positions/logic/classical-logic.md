---
course: logic
---

# Classical Logic

I am committed to laws of classical logic: law of non-contradiction, the law of excluded middle, and bivalence are self-evident, near-trivial truths. They reflect the meanings of "and", "or", "not", and "true" — anyone who denies them has misunderstood those words.

The argumentative path:

- **LNC follows from the meaning of negation.** ¬A holds in all and only the situations where A fails. There is no overlap, by definition. A contradiction (A ∧ ¬A) entails two incompatible propositions and is therefore necessarily false.
- **LEM follows by reductio.** Suppose neither A nor ¬A holds. Then it is not the case that A and it is not the case that ¬A — i.e. ¬A ∧ ¬¬A. That is itself a contradiction. So either A or ¬A must hold.
- **Bivalence follows from LEM plus the meanings of "true" and "false".** If a sentence asserts that p, it is true if p and false if ¬p; LEM gives us that one or the other obtains. So any proposition-expressing sentence is true or false.
- **Deviant logics (paraconsistent, three-valued, degree-of-truth) misdiagnose the problem.** Even reasoning about a deviant system requires classical logic to draw out its consequences.
- **The "nox" maneuver closes the escape route.** Define a strengthened operator: **nox A** means A is definitely not true — neither true, nor in any "gap" or "glut" middle state the deviant logician posits. For any L offered as a counterexample to LEM, consider L ∨ nox L. Denying it gives nox L ∧ nox nox L, a contradiction by the meaning of nox. So either the deviant logician accepts LEM-for-nox (and the paradox returns one level up), or they cannot state their own position — saying "L is neither true nor false" already requires an operator at least as strong as nox. Deviant logics don't avoid LEM/LNC; they hide them behind a weaker operator and rediscover them the moment they say anything precise.

Crucial qualification: bivalence and LEM apply only to **proposition-expressing sentences**. A sentence that fails to express a proposition — the Liar, vague sentences in their borderline range — is no counterexample. This is how I can keep classical logic intact while still saying the Liar sentence and "B is a heap" (for borderline B) are neither true nor false. Restricting the *scope* of these laws is a different operation from revising their *content*.

**Applicable to:** classical logic, deviant logics, paraconsistent logic, three-valued logic, dialetheism, law of non-contradiction, law of excluded middle, bivalence, *logic / 1. What is Logic?*, *logic / 2. Truth*, *logic / 7. Vagueness*
