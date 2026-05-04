# 'Any justification of deduction is bound to be circular.' Discuss.

**Thesis**: The slogan is correct on the *bound to be circular* reading and false on the *viciously circular* reading. Every attempted suasive justification of basic deductive rules is rule-circular — Haack's parity arguments make this watertight. But the right moral is not scepticism about deduction: basic rules need no inferential justification, because they are self-evident from the meanings of the logical constants. The demand for a non-circular suasive proof is misplaced, not unmet.

## Background

- **deductive validity**: syntactic vs semantic — derivable by rules vs truth-preserving in all models (Haack 1976)
- the justification problem (syntactic side): show that the rules of a system are truth-preserving
- **rule-circular argument**: uses rule R in proving R's validity; conclusion not literally a premise
- **vicious circularity**: argument lacks the power to give rational support; persuades only those already convinced
- **suasive vs explanatory** (Dummett 1973): suasive aims to persuade; explanatory takes conclusion as already accepted, derives it from premises whose grounds are explanatory power
- target rule throughout: modus ponens (MPP), with modus morons (MM) — *from A⊃B and B, infer A* — as the test case

## Theory 1: Deduction needs no justification (rejected)

- the deflationary line (Strawson-style): "valid argument" *means* "truth-preserving"; no further question
- best-case formulation: it is analytic that valid arguments preserve truth, so demanding a justification is confused
- objection: this conflates the two definitions of validity (Haack 1976 §3)
  - syntactic validity = derivable by rules
  - semantic validity = truth-preserving in all interpretations
  - the question is whether the *syntactic* rules track *semantic* validity — that's a real question, not a verbal one
- objection: even granting analyticity for "valid", we still need to know which forms (MPP, not MM) deserve the title
  - reply: intuition tells us
  - that just relocates the problem and offers no defence against rivals
- refuted because: the move evades the question by exploiting an ambiguity in "valid"

## Theory 2: Non-circular justifications are available (rejected)

- claim: a careful argument can vindicate MPP without using MPP
- candidate (a): truth-table proof of MPP — if A and A⊃B are both true, the table forces B true (Haack 1976 §4a)
  - objection: the proof itself has the form *suppose C; if C then D; so D* — i.e. it uses MPP
  - parity blow: the same form vindicates MM by symmetric construction — *suppose D; if C then D; so C* — and MM is invalid
  - so the strategy proves too much
- candidate (b): Carroll's Tortoise / Thomson's appended-premise strategy — extra premises bridge the gap (Haack 1976 §4b)
  - reply: Thomson's diagnosis says the bridging premise is true-but-superfluous for MPP and false-but-needed for MM
  - this presupposes MPP is the valid one — exactly what was at issue
- candidate (c): MPP follows from the meaning of '⊃' (Haack 1976 §4c)
  - sub-proposal (i): meaning given by the rules themselves — then MPP and MM are equally vindicated by stipulation (Prior's *tonk* problem)
  - sub-proposal (ii): meaning given by the truth-table — collapses back to (a)
  - sub-proposal (iii): meaning given by English "if … then" — begs the question; whether 'B' follows from 'if A then B' and 'A' is the issue
- candidate (d): MPP justified by the validity of its instances (Haack 1976 §5)
  - shifts the problem from rule to instance; "I just see the conclusion follows" is a non-answer
  - claim about a single instance has implicit generality (no counter-example of that *form*) — circular
  - infinitely many instances → would need induction → too weak
- refuted because: every candidate either uses MPP, presupposes MPP's privilege over MM, or trades the problem for an inductive one

## Theory 3: Circularity is rule-circular, not vicious (Dummett, rejected)

- Dummett 1973: the standard charge of circularity assumes the justification must be *suasive*; but what we want is *explanation*, not persuasion
- in an explanatory argument, epistemic and logical direction can diverge: we already accept the conclusion (deduction is justified) and seek premises that explain why it is
- soundness and completeness proofs are the natural candidates
- best-case formulation: rule-circularity is benign in explanation because there is no one to persuade — only something to make intelligible
- objection (Haack 1982): the suasive/explanatory line is belief-relative
  - philosophers who *do* doubt deduction (sceptics, paraconsistent dialetheists) still need suasion
  - Dummett owes them an argument, not a description of the rest of us
- objection (Haack 1982): the move is indiscriminate — it would equally "explain" any universally accepted fallacy
  - imagine the gambler's fallacy were universally believed valid — Dummett's strategy would license a circular explanation of it
  - so the strategy cannot distinguish good rules from bad
- objection (Haack 1982): to discriminate MPP from MM within explanation, one must already know MPP is valid
  - "MPP-explains-MPP works because MPP is valid; MM-explains-MM fails because MM isn't" presupposes the very justification at stake
- objection: Dummett's induction/deduction asymmetry is empirically false — ordinary reasoners trust both equally
- refuted because: the explanatory move either smuggles in the justification it claims to dispense with, or licenses too much

## Theory N: The slogan is true but harmless — basic rules are self-evident (preferred)

- thesis-bearing claim: every suasive justification of basic deductive rules is bound to be rule-circular; this is correct but not damaging
- the demand for an inferential justification of MPP, LNC, LEM is misplaced — these rules are self-evident from the meanings of "if", "not", "or"
- to deny MPP is not to disagree about a logical fact; it is to misuse "if then"
- *not* a stipulationist tonk-style move: the rules in question are constrained by genuine semantic content, not by free convention
- this is why the modus morons parody fails on its own: MM is not a candidate self-evident rule — its rejection has the same status as MPP's acceptance, both delivered by what '⊃' means
- alleged objection: "self-evidence is just intuition relabelled, and intuitions disagree" (paraconsistent logicians, dialetheists)
  - reply: deviant logicians cannot reason about their own systems without classical logic — the meta-theory invariably uses LNC and MPP (Haack 1982 §I.c on the metalanguage point)
  - any apparent counter-example to LEM/LNC reduces to a sentence that fails to express a determinate proposition (Liar, vague borderline cases) — scope restriction, not content revision
- alleged objection: Haack 1976's symmetry conclusion — induction and deduction stand or fall together — leaves deduction looking shaky
  - reply: the symmetry is real but cuts the other way; induction is in better shape than tradition holds, because the demand for non-circular suasive justification is misplaced for *both*
- alleged objection: Dummett is right that we want some explanation
  - reply: agreed — but explanation isn't justification; conceding rule-circular *explanations* doesn't license the slogan that rule-circular *justifications* are fine
- stands because: the prompt is correct as it stands, but the conclusion it suggests (deduction is rationally insecure) doesn't follow; basic logic doesn't need a non-circular suasive argument to be in good standing

## Conclusion

- Theory 1 fails: "deduction is valid by definition" trades on syntactic/semantic equivocation
- Theory 2 fails: every candidate non-circular justification is either rule-circular or vindicates MM by parity
- Theory 3 fails: Dummett's explanatory rescue is belief-relative, indiscriminate, and presupposes what it set out to explain
- Theory N stands: the slogan is true on the literal reading and false on the vicious reading — basic rules don't need an inferential justification, so their resistance to one is no scandal
