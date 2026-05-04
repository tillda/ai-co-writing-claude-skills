# 'Any justification of deduction is bound to be circular.'

**Thesis**: The claim is true on the *suasive* reading and harmless on the *explanatory* reading; a non-circular persuasive justification of deduction is impossible, but rule-circular use of deduction in an explanatory project is not vicious — and in any case the demand presupposes that deductive laws must be reached by inference, which we should reject.

## Background
- *Justification* (in this debate): show that a basic rule like MP is truth-preserving. Two readings — *suasive* (persuade someone who doubts) vs *explanatory* (account for what we already accept).
- *Deductive validity*: syntactic (derivable by the system's rules) and semantic (no model with true premisses and false conclusion).
- *Vicious vs rule-circular*: vicious = the conclusion appears as a premiss; rule-circular = the rule under scrutiny is *used* in the proof.
- Background asymmetry the question presupposes: induction is shaky, deduction is firm.

## Theory 1: simple deductive justification of MP (rejected)
- Claim: MP is justified by a deductive argument from the truth-table for `⊃`.
- Best-case (Haack 1976 §1.4.1): "Suppose A and A⊃B; by the truth-table, B follows; so B." Looks like a clean meta-level proof.
- Objection: the meta-step is itself an instance of MP — same form as the rule it claims to support.
  - Reply: but the truth-table is not an inference, just a definition.
  - Counter: reading off "if A=T and A⊃B=T then B=T" *is* the inference; you cannot extract the conclusion without using MP.
- Objection — Carroll's tortoise (Carroll 1895; Haack 1976 §1.4.2): turn the rule into a premiss `A ⊃ ((A⊃B) ⊃ B)` and the same gap reopens, ad indefinitum.
  - Reply: take MP as a primitive rule, not a premiss.
  - Counter: that just renames the circle — the rule is now used without justification.
- Refuted because every candidate either uses MP in the proof or generates Haack's regress of premises and rules.

## Theory 2: justification by the validity of instances (rejected)
- Claim: MP is justified because each of its instances is valid; we just *see* that the premisses force the conclusion (Haack 1976 §1.5).
- Objection: shifts the problem from schema to instance without solving it — "we just see it" is not a justification.
- Objection: validity of an instance already involves generality (no argument of *that form* with true premisses and false conclusion); appeal to instances is therefore parasitic on the schema.
- Objection: a schema has infinitely many instances, so any proof from them would be inductive — and would yield only "usually truth-preserving", which is too weak (Haack's second horn).
- Refuted because the move is either inductive-and-too-weak or covertly relies on the schema it was meant to vindicate.

## Theory 3: rule-circularity is not vicious — Dummett's escape (rejected)
- Claim (Dummett 1973): three levels of justification — (i) deriving inside a system, (ii) justifying a rule via soundness proofs, (iii) explaining how deduction is possible. At level (ii–iii) the project is *explanatory*, not *suasive*; rule-circularity is acceptable.
- Best-case: in a suasive argument the epistemic direction must run with logical consequence, so circularity is fatal; in an explanation, the conclusion is already accepted and the deductive proof of soundness merely displays the connection.
- Objection (Haack 1982 §I.b — gambler's-fallacy parity): the move would equally "explain" any universally believed rule, including invalid ones; modus morons could be vindicated by an argument that uses modus morons.
  - Reply: but MP is valid and modus morons is not.
  - Counter: that asymmetry is precisely what the justification was meant to deliver. Dummett helps himself to it.
- Objection (Haack 1982 §I.c): soundness/completeness proofs are *necessary but not sufficient* — there are too many sound systems (classical, relevance, intuitionist), and the metalanguage's own logic may exceed the object language's (Gödel-style worry).
  - Reply: pluralism is fine; pick the system that fits the practice.
  - Counter: "fits the practice" is not justification, and revisability undermines the appeal to entrenched practice as a starting point.
- Refuted because rule-circularity dodges the suasive horn but leaves the explanatory project unable to rule out an exactly parallel "explanation" of an invalid rule.

## Concession: induction and deduction stand or fall together (Haack 1976 §1.6)
- Pessimistic gloss: deduction is no firmer than induction.
- Optimistic gloss: induction is no shakier than deduction.
- Either way the asymmetry presumption driving the original claim is wrong. So even if "any justification of deduction is bound to be circular" stands, it is not the special scandal it sounds like.

## Theory 4: Phenomenal Conservatism — supplementary, not replacement (preferred)
- Claim: if it intellectually seems to S that MP preserves truth, S thereby has prima facie (defeasible) justification for believing it. The seeming is foundational, not a step in an inference.
- Why it works: Haack's dilemma and Carroll's regress both presuppose that deductive laws must be reached *by inference*. PC denies that presupposition; the regress never starts because there is no first inferential step demanded.
- Defeasibility, honestly: naive comprehension once seemed obvious and turned out false — so PC does not claim infallibility, only that the seeming is the terminus of warrant absent defeaters.
- Objection: this just renames "intuition" and gives up on justification.
  - Reply: PC treats rational seemings on a par with perceptual ones; we accept perceptual seemings as foundational without inferential backing, so consistency requires the same for rational ones.
- Objection: PC is epistemology, not logic — it has no business in a Logic-course answer.
  - Reply: agreed it is supplementary; the canonical logical answer (semantic / proof-theoretic justification) remains the main line. PC explains *why* the absence of a non-circular suasive justification is not a defect.
- Stands because it dissolves rather than satisfies the demand: there is no inferential justification on offer, and none is needed.

## Conclusion
- Theory 1 fails: every concrete deductive justification of MP either uses MP or kicks off Carroll's regress.
- Theory 2 fails: validity-by-instances is either inductive-and-too-weak or parasitic on the schema.
- Theory 3 fails: Dummett's suasive/explanatory split would equally vindicate invalid rules; soundness proofs are necessary but not sufficient.
- Concession: deduction and induction stand or fall together; the asymmetry presumed by the question is wrong.
- Theory 4 stands: the rational seeming that MP preserves truth is itself foundational warrant; the demand for a non-circular inferential justification is not met but dissolved. So the claim is correct only on its narrow suasive reading, and harmless once we have the right epistemology of basic logical seemings.
