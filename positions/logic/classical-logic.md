---
course: logic
---

# Classical Logic

I am committed to laws of classical logic: law of non-contradiction, the law of excluded middle, and bivalence are self-evident, near-trivial truths. They reflect the meanings of "and", "or", "not", and "true" — anyone who denies them has misunderstood those words.

The argumentative path:

- **LNC follows from the meaning of negation.** ¬A holds in all and only the situations where A fails. There is no overlap, by definition. A contradiction (A ∧ ¬A) entails two incompatible propositions and is therefore necessarily false.
- **LEM follows by reductio.** Suppose neither A nor ¬A holds. Then it is not the case that A and it is not the case that ¬A — i.e. ¬A ∧ ¬¬A. That is itself a contradiction. So either A or ¬A must hold.
- **Bivalence follows from LEM plus the meanings of "true" and "false".** If a sentence asserts that p, it is true if p and false if ¬p; LEM gives us that one or the other obtains. So any proposition-expressing sentence is true or false.
- **Deviant logics (paraconsistent, three-valued, degree-of-truth) misdiagnose the problem.** Even reasoning about a deviant system requires classical logic to draw out its consequences. And any apparent counterexample to LEM/LNC can be rebuilt with a strengthened operator (Huemer's "not!", defined to exclude both gaps and gluts), reviving the original paradox without using the disputed concept of negation.

Crucial qualification: bivalence and LEM apply only to **proposition-expressing sentences**. A sentence that fails to express a proposition — the Liar, vague sentences in their borderline range — is no counterexample. This is how I can keep classical logic intact while still saying the Liar sentence and "B is a heap" (for borderline B) are neither true nor false. Restricting the *scope* of these laws is a different operation from revising their *content*.

In detail: see Michael Huemer's *Paradox Lost*, Introduction §1.3 and Chapter 3 §3.5.7. For an intro-level statement of the same arguments, see Huemer's *Knowledge, Reality, and Value* §§5.2.1-5.2.2 — including the closing caveat at §5.2.2 that LEM/LNC apply only to proposition-expressing sentences ("All blugs are torf" is no counterexample to LEM), which is the canonical statement of the scope-restriction move.

**Applicable to:** classical logic, deviant logics, paraconsistent logic, three-valued logic, dialetheism, law of non-contradiction, law of excluded middle, bivalence, *logic / 1. What is Logic?*, *logic / 2. Truth*, *logic / 7. Vagueness*
