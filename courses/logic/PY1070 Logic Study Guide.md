
UNIVERSITY  
OF LONDON

Undergraduate study in  
Philosophy

Logic
M. Sainsbury

PY1070

© University of London 2012

The University of London asserts copyright over all material in this subject guide except where otherwise indicated. All rights reserved. No part of this work may be reproduced in any form, or by any means, without permission in writing from the publisher. We make every effort to contact copyright holders. If you think we have inadvertently used your copyright material, please let us know.

# Contents

| <b>Introduction</b>                                                                | 1  |
|------------------------------------------------------------------------------------|----|
| 1. What is logic?                                                                  | 1  |
| 2. Why is logic important?                                                         | 1  |
| 3. Getting started                                                                 | 2  |
| Readings                                                                           | 2  |
| <b>What is logic? The varieties of logic, Logical languages, Logical constants</b> | 6  |
| 1.1 Introduction                                                                   | 6  |
| 1.2 Formal logic versus philosophical logic; logical form                          | 6  |
| 1.3 The language of classical logic                                                | 7  |
| 1.4 Models and proofs                                                              | 9  |
| 1.5 What is a logical constant?                                                    | 10 |
| <b>Truth</b>                                                                       | 12 |
| 2.1 Introduction                                                                   | 12 |
| 2.2 The paradox of the Liar                                                        | 12 |
| 2.3 Deflationism                                                                   | 13 |
| 2.4 Correspondence                                                                 | 15 |
| 2.5 Pragmatism, coherence, identity                                                | 16 |
| 2.6 Bivalence and excluded middle                                                  | 16 |
| <b>Modality</b>                                                                    | 18 |
| 3.1 Boxes and diamonds                                                             | 18 |
| 3.2 Counterpart theory                                                             | 20 |
| <b>Conditionals</b>                                                                | 22 |
| 4.1 'if' and '→'                                                                   | 22 |
| 4.2 Conditionals and probabilities                                                 | 23 |
| 4.3 Subjunctive and counterfactual conditionals                                    | 24 |
| <b>Reference – names and descriptions</b>                                          | 26 |
| Introduction                                                                       | 26 |
| 5.1 Russell's theory of descriptions                                               | 26 |
| 5.2 Proper names: Millian versus descriptive theories                              | 28 |
| 5.3 Existence and ontology                                                         | 30 |
| 5.4 Reference and the <i>de re/de dicto</i> distinction                            | 31 |
| <b>Non-extensional language</b>                                                    | 32 |
| <b>Vagueness</b>                                                                   | 34 |
| <b>Essentialism</b>                                                                | 37 |
| 8.1 Necessary, <i>apriori</i> , analytic                                           | 37 |
| 8.2 Kripke's counterexamples to the coincidence                                    | 38 |
| 8.3 Quine's arguments against essentialism                                         | 39 |
| <b>The justification of deduction</b>                                              | 41 |
| <b>Feedback to Activities</b>                                                      | 43 |

# Introduction

## 1. What is logic?

Logic is the study of reasoning. It attempts to give a general answer to the question: what makes the difference between good reasoning and bad? It's a normative subject, dealing not with how we in fact reason, but how we should reason.

If all rich people are happy and John is rich, it follows that John is happy. If the potatoes have been boiling for 20 minutes, it's reasonable to infer that they are cooked. These examples suggest different kinds of reasoning. The reasoning about John is **deductively valid** ('valid', for short), marked by the fact that if the reasons given are true (that all rich people are happy, and that John is rich) they **guarantee** the truth of the conclusion (that John is happy). Deductive logic is the systematic study of deductive validity. Its official topic is 'arguments', using this word in a technical sense:

**An argument is a sequence of sentences.**  
**The last sentence in the sequence is called the conclusion. The remainder (if any) are called the premises.**

We have considered two arguments. The one about John has two premises, 'All rich people are happy' and 'John is rich'; its conclusion is 'John is happy'. The one about the potatoes has one premise, 'The potatoes have been boiling for 20 minutes'; its conclusion is 'They are cooked'.

This second argument is not deductively valid: it's possible that we have some maverick super-hard potatoes, or that the water is boiling at a lower temperature than usual. Even so, the reasoning is of value, as we all know from experience. We can call it **inductively strong**: in very many circumstances, the fact that the potatoes have been boiling for 20 minutes makes it rational to believe that they are cooked, even if it doesn't conclusively establish this.

The contrast between validity and inductive strength is marked by the following feature.

Deductive validity is **monotonic**: no matter how many premises are added to the premises of a deductively valid argument, the resulting argument is deductively valid. Inductive validity is **non-monotonic**.

To illustrate: suppose we add some extraneous material to the argument about John, yielding the following argument (using 'P1' and so on to number the premises, and 'C' to mark the conclusion):

(P1) All rich people are happy.  
(P2) John is rich.  
(P3) Being a lawyer is a bad way to get rich.  
(C) John is happy.

The argument with the extra premise is still valid: the premises guarantee that John is happy. This holds for any way the original argument might be supplemented.

By contrast, inductive strength is non-monotonic. The following argument is inductively weak:

(P1) The potatoes have been boiling for 20 minutes.  
(P2) We are at 16,000 feet.  
(P3) At 16,000 feet, water boils at around 190°F.  
(P4) Cooking time approximately doubles for every 10°F below 212°F.  
(C) The potatoes are cooked.

This subject guide relates just to deductive logic: 'logic', for short.

## 2. Why is logic important?

Logic has been a highly influential discipline, affecting mathematics, computing, artificial intelligence, linguistics, information theory, neuroscience and philosophy. Part of the explanation for this is that human societies have depended from the earliest times on information, and logic concerns the extraction of information. Given some data, what follows? What information is hidden or implicit in the data?

Corresponding to the distinction between deductive logic and inductive logic, there are other approaches to information extraction, notably those that can be subsumed under the heading of statistics, in the broadest sense. In these other approaches, the notion of **evidence** is crucial, and, as in the example about boiling potatoes, evidence falls short of entailing that for which it is evidence: good evidence for a conclusion doesn't provide a logical guarantee of its truth.

We all want to think logically rather than illogically. It's arguable that the capacity for logical thinking is a prerequisite for rationality. That's one reason to study logic.

In trying to characterise validity, we have to generalise. There are too many arguments to consider one-by-one. Generalising involves finding patterns in sentences, and this has consequences that lead in various interesting directions:

- One source of patterning is the 'logical constants' or 'logical connectives' contained in sentences. In English these are words like 'and', 'or' and 'not'. Understanding how these expressions work had immediate applications in computing. For example, the function of the ubiquitous NAND gate can be seen as a combination of the function of 'not' and that of 'and' (hence its name). It was logicians who first studied these notions (going back at least to the Middle Ages).
- The central role of pattern connects logic with algebra. The name to conjure with in this connection is **George Boole** (mid-nineteenth century).
- Work on how to pattern sentences led to a deeper understanding of how sentences themselves function. Examples:
  - Theorists became sensitive to certain kinds of ambiguity and devised tools for disambiguating.
  - **Bertrand Russell** said that 'is' is ambiguous between expressing identity ('The murderer **is** none other than Geoffrey Jones'), expressing predication ('Obama **is** a national leader') and expressing existence ('God **is**').
  - 'These students have a laptop' is (arguably) ambiguous between claiming that they share ownership of a laptop and claiming that each owns one.
- Expressions that seemed to be of the same kind were said to be of different kinds. We might initially classify proper names like 'Obama' with definite descriptions like 'the president of the USA'. We would then make no distinction between the contributions to validity of a sentence like 'Obama spoke this evening' and 'The president of the USA spoke this evening'. However, this similarity has been debated (see 'Russell's theory of descriptions', Chapter 4).

The best sorts of arguments, set in somewhat academic contexts, constitute 'proofs'. Logicians lay claim to special authority on the question of what constitutes a proof. This notion has had significant impact in mathematics (for example, in Gödel's incompleteness theorems) and in computing (in the conception of an **algorithm** and in adequacy proofs for programming languages).

### 3. Getting started

A 45-minute BBC **radio programme**, in which Melvyn Bragg talks to A.C. Grayling, Peter Millican and Rosanne Keefe, provides a gentle and largely historical introduction to this subject. It would be quite useful to know some elementary formal logic. You could consult such books as **Guttenplan (1997)**, **Hodges (2005) Priest (2000)** or **Sider (2010)**. (These are very different kinds of books. The reading list below

contains a few comments on some of the entries.) This guide does not presuppose prior knowledge.

You will find that web searches using problematic terms (for example 'free logic') will be very rewarding. The usual cautions are in order. For example, 'model' is a technical term in logic, but an unqualified search using that word leads to distracting results. Instead search under 'model logic philosophy'.

In this guide, definitions or claims that are especially important are highlighted in red text.

In many of the chapters there are Activities to guide your reflections. Feedback to selected Activities may be found at the end of this guide.

Some of the readings that appear in the list of readings that follows are available through the Student Portal, either:

1. articles from different journals, which can be found in the Online Library (for the most part in JSTOR), marked \*
2. single chapters of books, which have been made available on the VLE, marked \*\*

Other readings are available online. Public internet resources are accessed by clicking links (shown in the standard way selected by your text viewer, and typically changing colour after they've been clicked).

Most books recommended in the guide are widely available for purchase from online booksellers.

The resources marked with asterisks are sufficient to give you a reasonable understanding of the subject.

One of the most important reasons to study philosophy is to learn how to form and defend views of your own. A view of your own does not have to be a view no one has ever held before. In Logic, new views are hard to come by. A view counts as your own if you believe it and are willing to defend it. In thinking about logic, you will have to decide which views to make your own.

Especially in the early stages, it can be hard to decide which of two opposing theories is correct. Even so, you may be able to make lesser decisions: does this argument decisively establish or refute this theory? Could an objection be avoided by some modification of the theory? Can one not distinguish at least two versions of a given doctrine? Asking and answering these questions is essential, if studying philosophy is to be worthwhile.

### Readings

- Adams, E. W. 'Subjunctive and indicative conditionals', *Foundations of Language* 6 (1970), pp.89–94.
- Aristotle *On Interpretation*, 9. This is where to find Aristotle's account of the future sea-battle. Available online.

Ayer, A.J. *Language, Truth and Logic*. (London: Victor Gollancz Ltd., 1936). Classic logical positivist text, with a brief discussion of ethics. Too far from the topic of this guide to be more than possible subsidiary reading.

Batchelor, R. 'Topic-Neutrality', *Mind* 120 (2011), pp.1–9. A rather austere account of topic neutrality. Available online.

Beall, J.C. and M. Glanzberg 'Liar Paradox', *The Stanford Encyclopedia of Philosophy* (Spring 2011 edition), Edward N. Zalta (ed.), <http://plato.stanford.edu/archives/spr2011/entries/liar-paradox/>.

\* Boghossian, P. 'The transparency of mental content revisited', *Philosophical Studies* online (DOI 10.1007/s11098-010-9611-3)

Blackburn, S. and K. Simmons (eds) *Truth*. (Oxford: Oxford University Press, 1999) [ISBN 9780198752509]. A good collection of papers on the topic, mostly reprints.

\* Carroll, Lewis 'What the Tortoise Said to Achilles', *Mind* 4 (1895), pp.278–80.

Davidson, D. 'Action and reaction', *Inquiry* 13 (1970), pp.140–48. Davidson defends his notion of logical form.

\* Davidson, D. 'Truth and meaning', *Synthese* 7 (1967). Reprinted in his *Essays on Truth and Interpretation* (Oxford: Oxford University Press, 1984) [ISBN 0141186046], pp.17–36.

\* Donnellan, K. 'Reference and definite descriptions', *Philosophical Review* 77 (1966), pp.203–15. Source for the distinction between referential and attributive descriptions.

\* Dummett, M. 'Truth', *Proceedings of the Aristotelian Society* 59 (1959), pp.141–62. Classic paper on the topic.

\*\* Dummett, M. 'The Justification of Deduction', *Proceedings of the British Academy* (1973). Reprinted in his *Truth and Other Enigmas* (Cambridge, MA: Harvard University Press, 1978) [ISBN 0674910753] pp.290–318. Rather tricky discussion of this important issue.

\* Edgington, D. 'On conditionals', *Mind* 104 (1995), pp.235–329. Classic survey article. It's long and complicated – but clear. This is what I would focus on if I was planning to answer a question on conditionals.

\*\* Edgington, D. 'Vagueness by degrees' in Keefe, R. and P. Smith (eds) *Vagueness: A Reader* (Cambridge, Mass: MIT Press, 1997) [ISBN 0262611457], pp.294–316. Nice, and original, account of a degree-theoretic conception of vagueness.

Edgington, D. 'Conditionals', *The Stanford Encyclopedia of Philosophy* (Winter 2008 edition), Edward N. Zalta (ed.), <http://plato.stanford.edu/archives/win2008/entries/conditionals/>. A shorter, but still excellent, survey.

\*\* Evans, G. 'Semantic structure and logical form' in Evans, G. and J. H. McDowell (eds) *Truth and Meaning: Essays in Semantics* (Oxford: Clarendon Press, 1976) [ISBN 019825007X]. Reprinted in Evans's *Collected Papers* (Oxford: Oxford University Press, 1985), pp.49–75.

\*\* Evans, G. *The Varieties of Reference*. (Oxford: Clarendon Press, 1982) [ISBN 0198246862]. Classic book on a range of topics. For this paper, the most important chapters are those on Frege (1), Russell (2) and Existential statements (10). ('Existential statements' is available on the VLE)

Forbes, G. 'Intensional Transitive Verbs', *The Stanford Encyclopedia of Philosophy* (Spring 2010 edition), Edward N. Zalta (ed.), <http://plato.stanford.edu/archives/spr2010/entries/>

intensional-trans-verbs/. Nice survey of constructions like 'She wants a sweater'. Likely to be too technical and detailed for this paper.

\*\* Frege, G. 'On sense and meaning' in B. McGuinness (ed.) *Collected Papers on Mathematics, Logic and Philosophy* (Oxford: Basil Blackwell, 1984; first published 1892) [ISBN 0631127283], pp.157–77. Classic paper, in which the sense/reference contrast is introduced. Essential reading.

Garson, J. 'Modal Logic', *The Stanford Encyclopedia of Philosophy* (Winter 2009 edition), Edward N. Zalta (ed.), <http://plato.stanford.edu/archives/win2009/entries/logic-modal/#QuaModLog>. Much more detail here than you really need, but a useful source if you plan to answer a question on modality.

Glanzberg, M. 'Truth', *The Stanford Encyclopedia of Philosophy* (Spring 2009 edition), Edward N. Zalta (ed.), <http://plato.stanford.edu/archives/spr2009/entries/truth/>. Good overview – recommended if you are planning to answer on this topic.

Goodman, N. *Fact, Fiction and Forecast* (Indianapolis: Bobbs-Merrill, 1953). An early account of the approach to justification now called that of reflective equilibrium. Only a couple of pages relate to the justification of deduction.

\*\* Grice, H.P. 'Logic and conversation' in Cole, P. and J. L. Morgan (eds) *Syntax and Semantics, Vol. 3: Speech Acts*. (New York: Academic Press, 1975) [ISBN 0127854231], pp.41–58.

\* Grice, H.P. and P.F. Strawson 'In defense of a dogma', *Philosophical Review* 65 (1956), pp.41–58. A criticism of Quine's attacks on the notion of analyticity.

Guttenplan, S. *The Languages of Logic. An Introduction to Formal Logic*. (Oxford: Blackwell, 1997) second edition [ISBN 155786988X]. Probably the most student-friendly introduction to formal logic available, informed by pedagogical originality and a sensitivity to philosophical questions.

\* Haack, S. 'Dummett's Justification of Deduction', *Mind* 91 (1982), pp.216–39. Easier to read than Dummett himself, and with some lines of criticism.

Hodges, W. *Logic*. (London: Penguin, 2005) second edition [ISBN 0141003146]. A very popular introduction to formal logic. Competes directly with Guttenplan. You can compare samples on Amazon and see which you prefer.

Holt, J. 'Whose idea is it anyway?': *Lingua Franca* (1997). Available online.

Horwich, P. *Truth*. (Oxford: Basil Blackwell, 1990) [ISBN 0631173161]. Very clearly presented deflationist or minimalist account. The most important part is reprinted in Horwich (1999).

Horwich, P. 'The minimalist conception of truth' in Blackburn, S. and K. Simmons (eds) *Truth*. (Oxford: Oxford University Press, 1999) [ISBN 9780198752509], pp.239–63. An excerpt from his book *Truth*.

Hume, D. *A Treatise of Human Nature*. (London: 1739–40). Available online.

\* Jackson, F. 'On assertion and indicative conditionals', *Philosophical Review* 88 (4) (1979), pp.565–89. An attempt to defend the view that English conditionals are truth functional.

James, W. *Pragmatism: A New Name for Some Old Ways of Thinking*. (Indianapolis; Cambridge: Hackett Publishing, 1981; first published 1907) [ISBN 0915145049].

Kant, I. *Critique of Pure Reason*. Translated and edited by P. Guyer and A. Wood (Cambridge: Cambridge University Press, 1997; first published 1781) [ISBN 0521657296].

Keefe, R. *Theories of Vagueness*. (Cambridge: Cambridge University Press, 2000) [ISBN 0521650674]. Very clear overview. Discussion of supervaluation is especially well done.

Kripke, S. 'A Completeness Theorem in Modal Logic', *Journal of Symbolic Logic* 24 (1) (1959), pp.1–14. This and his 1963 and 1975 publications are listed for historical reasons. I doubt students preparing for this paper will find them useful.

Kripke, S. 'Semantic Considerations on Modal Logic', *Acta Philosophica Fennica* 16 (1963), pp.83–94.

\* Kripke, S. 'Outline of a theory of truth', *Journal of Philosophy* 72 (1975), pp.690–716.

Kripke, S. 'Speaker's Reference and Semantic Reference', *Midwest Studies in Philosophy* 2 (1977), pp.255–76. This is a very rich paper, and well worth reading if you are taking the topic of reference seriously.

Kripke, S. *Naming and Necessity*. (Cambridge, MA: Harvard University Press, 1980) [ISBN 0674598466]. Lovely book, already a classic. Transcript of lectures, so informally presented, and everyone finds it a joy to read.

Lewis, C.I. *Alternative Systems of Logic*, *Monist* 42 (1932), pp.481–507.

\* Lewis, D. 'Counterpart theory and quantified modal logic', *The Journal of Philosophy* 65 (1968), pp.113–26.

Lewis, D. *Counterfactuals*. (Oxford: Basil Blackwell, 1973). Probably the best source of Lewis's account of counterfactual conditionals.

\* Lewis, D. 'Probabilities of conditionals and conditional probabilities', *Philosophical Review* 85 (1976), pp.297–315.

\* Lewis, D. 'Counterfactual dependence and time's arrow', *Noûs* 13 (1979), pp.455–76.

Lewis, D. *On the Plurality of Worlds*. (Oxford: Basil Blackwell, 1986) [ISBN 0631224963]. Very detailed discussion of the metaphysics of modality.

\*Macfarlane, J. 'Future Contingents and Relative Truth', *The Philosophical Quarterly* 53 (2003), pp.321–36. Important suggestion for how we should respond to the sea-battle.

Martin, R.L. (ed.) *Recent Essays on Truth and the Liar Paradox*. (Oxford: Oxford University Press, 1984) [ISBN 0198247125]. Quite old, but not out of date! A collection of essays on the Liar paradox, with helpful editorial introduction.

Melia, J. *Modality*. (Durham: Acumen, 2003) [ISBN 0198247125].

Mill, J.S. *System of Logic*. (London: Parker, 1843). Available online. Only a few pages are relevant: search for 'Dartmouth' in an electronic version of the work and you will find them.

\*\* Montague, R. 'English as a formal language'. Reprinted in R.H. Thomason (ed.) *Formal Philosophy*. (New Haven: Yale University Press, 1974; first published 1970) [ISBN 0300024126], pp.188–221. I don't suggest you read this, but it's historically important, as the title suggests: it undermines the conception of logical forms as sentences in the language of first order logic.

Neale, S. *Descriptions*. (Cambridge, Mass; London: MIT Press, 1990) [ISBN 0262640317]. Very nice clear defence of Russellian treatment of definite descriptions, with a good historical survey.

Neale, S. 'On a milestone of empiricism' in Orenstein, A. and P. Kotatko (eds) *Knowledge, Language and Logic*. (Dordrecht: Kluwer, 2000) [ISBN 140200253X], pp.237–346.

Plantinga, A. *The Nature of Necessity*. (Oxford: Oxford University Press, 1974) [ISBN 0198244142].

\* Priest, G. 'Contradiction, belief and rationality', *Proceedings of the Aristotelian Society* 86 (1986), pp.99–116.

Priest, G. *In Contradiction*. (Dordrecht: Nijhof, 1987) [ISBN 9024736307].

Priest, G. *Logic. A Very Short Introduction*. (Oxford: Oxford University Press, 2000) [ISBN 0192893203].

Priest, G. and F. Berto 'Dialetheism', *The Stanford Encyclopedia of Philosophy* (Summer 2010 edition), Edward N. Zalta (ed.), <http://plato.stanford.edu/archives/sum2010/entries/dialetheism/> Best source for paraconsistent logic and dialetheism.

Proops, I. 'Russell on Substitutivity and the Abandonment of Propositions', *The Philosophical Review* 120 (2011), pp.151–205. Careful account of Russell on George IV.

\* Quine, W. van O. 'Two dogmas of empiricism', *The Philosophical Review* 60 (1951), pp.20–43. Classic source of attack on analyticity.

\*\* Quine, W. van O. 'Three grades of modal involvement' in W. van O. Quine *The Ways of Paradox*. (New York: Random House, 1966). Classic source of attack on essentialism.

Quine, W. van O. *Word and Object*. (New York: Technology Press of MIT and John Wiley and Sons Inc., 1960). Brings together many of Quine's ideas, including hostility to both analyticity and essentialism.

\* Quinton, A. 'The a priori and the analytic', *Proceedings of the Aristotelian Society* 64 (1963), pp.31–54. Defence of a thesis of equivalence, subsequently attacked by Kripke.

\*\* Ramsey, F.P. 'Facts and propositions' in G. Pitcher (ed.) *Truth*. (Englewood Cliffs, NJ: Prentice Hall, 1964; first published 1927), pp.16–17.

Robertson, T. 'Essential vs. Accidental Properties', *The Stanford Encyclopedia of Philosophy* (Fall 2008 edition), Edward N. Zalta (ed.), <http://plato.stanford.edu/archives/fall2008/entries/essential-accidental/>

Rodriguez-Pereyra, G. 'Truthmakers', *Philosophy Compass* 1 (2006), pp.186–200.

Rumfitt, I. 'Meaning and possibilities: the semantic justification of logical laws', inaugural lecture at Birkbeck College, 2008. Available online.

\* Russell, B. 'On denoting', *Mind* 14 (1905), pp.479–93. Classic source of the theory of descriptions.

\* Russell, B. 'Mathematical logic as based on the theory of types', *American Journal of Mathematics* 30 (1908), pp.222–62.

Russell, B. *Problems of Philosophy*. (Oxford: Oxford University Press, 1959; first published 1912). Chapter 5 is what you need for the contrast between names and descriptions, and Russell's account of acquaintance. (Available online at Project Gutenberg.)

Russell, B. *Introduction to Mathematical Philosophy*. (London: George Allen and Unwin, 1919).

## Introduction

Sainsbury, R.M. *Logical Forms: An Introduction to Philosophical Logic*. (Oxford; Cambridge, Mass: Blackwell Publishers, 1991; second edition 2001) [ISBN 0631177787]. A somewhat pedantic presentation of how formal logic can be applied to English. Also includes a more general discussion of logical form and the logical constants.

Sainsbury, R.M. 'Russell on names and communication' in Irvine, A. and G. Wedeking (eds) *Russell and Analytic Philosophy* (Toronto: University of Toronto Press, 1993) [ISBN 0802028756], pp.3–21.

Sainsbury, R.M. *Reference Without Referents*. (Oxford: Oxford University Press, 2005) [ISBN 9780199241804].

\*\* Sainsbury, R.M. 'Philosophical logic' in D. Moran (ed.) *The Routledge Companion to Twentieth Century Philosophy* (Abingdon: Routledge, 2008) [ISBN 9780415299367], pp.347–81. This is an introduction to philosophical logic, focusing on the notion of logical form.

Sainsbury, R.M. *Paradoxes*. (Cambridge; New York: Cambridge University Press, 2009) third edition [ISBN 9780521720793]. Intended for a non-specialist audience. Has a chapter on the Liar and one on dialetheism.

Sider, T. *Logic for Philosophy*. (New York: Oxford University Press, 2010) [ISBN 9780199575589]. This is very well done, but contains a lot more than you need to know for this paper.

\* Soames, S. 'The modal argument: wide scope and rigidified descriptions', *Noûs* 32 (1998), pp.1–22. Kripke showed that proper names have a different modal profile from some definite descriptions in some contexts. But suppose we consider wide-scope descriptions? Or descriptions that are made rigid? Soames says that there will still be problems.

Stalnaker, R. 'Indicative conditionals', *Philosophia* 5 (1975), pp.269–86.

\* Strawson, P. 'On Referring', *Mind* 59 (1950), pp.269–86. Classic rejoinder to Russell. Claims that ordinary language has no exact logic, which has proved quite exciting!

\* Strawson, P. 'Truth', *Supplementary Proceedings of the Aristotelian Society* 24 (1950), pp.129–56.

\* Tarski, A. 'The semantic conception of truth: and the foundations of semantics', *Philosophy and Phenomenological Research* 4 (1944), pp.341–76.

\* Tennant, N. 'Rule-Circularity and the Justification of Deduction', *Philosophical Quarterly* 55 (2005), pp.625–48.

Wright, C. *Truth and Objectivity*. (Cambridge, Mass: Harvard University Press, 1992) [ISBN 0674910877].

# What is logic? The varieties of logic, Logical languages, Logical constants

## 1.1 Introduction

Logic is the study of reasoning. Reasoning is expressed in arguments, and logic aims to characterise what it takes for an argument to be valid. An initial intuitive characterisation of validity is as follows:

**An argument is valid if and only if, necessarily, if all the premises are true so is the conclusion.**

To achieve generality, logic identifies patterns or **forms** of argument. An early attempt was Aristotle's syllogistic, according to which there are **four basic kinds** of sentence. A syllogism is an argument with two premises and a conclusion. Syllogistic arguments can be exhaustively classified according to the form of each premise and the conclusion. Here is a traditional example of a valid syllogistic argument form (code-named bArbArA to remind you that all the premises take the form 'All so-and-sos are such-and-such'):

(P1) **All Fs are Gs**  
(P2) **All Gs are Hs**  
(C) **All Fs are Hs.**

The letters 'F' and 'G' are supposed to mark blanks. We don't have a real argument, but only the form of an argument. We obtain a real argument by replacing the letters with words, while retaining the same pattern, for example:

(P1) All doctors are human beings  
(P2) All human beings are rational animals  
(C) All doctors are rational animals.

To preserve the pattern, it's important to replace a letter on each of its occurrences by the same English expression.

### Activity 1.1

Give an example of an argument which is invalid because it fails to observe this restriction.

Syllogistic logic is rather limited. For one thing, all its arguments have to have two premises, whereas there are good arguments with many more premises, or with just one premise or even none. Syllogistic logic also has trouble doing justice to the logical powers of words like 'and', 'or' and 'if', now thought of as at the heart of logic.

## Activity 1.2

Give an example of an argument with just one premise or with none.

The most salient formal logic nowadays is so-called 'classical logic' or 'first-order logic with identity' or 'predicate logic'. It is possible to draw distinctions, but for the most part these expressions are used interchangeably. Classical logic is formal because it deals with the forms that sentences – called formulae – can take, and thus enables a classification of arguments according to their form.

## 1.2 Formal logic versus philosophical logic; logical form

In the syllabus for this subject, this paper is about **philosophical logic**, which includes questions like the following:

- How, if at all, can one justify deduction?
- What is a logical constant?
- Can truth be defined?
- Is 'if' ambiguous?
- If 'Father Christmas does not exist' is true, does it not follow that there is something that doesn't exist?
- What is logical form?

Some of these topics are best approached if you have a background, however sketchy, in **formal logic**. Formal logic is a branch of mathematics, in which the three main objects of study are abstract entities: formal **languages**, **models** for these languages, and **proofs** within the languages. All these notions (explained in more detail in the next section) are defined with complete precision, and there is no room for two opinions about whether, for example, something is or is not a formula of a logical language, or whether some set-theoretic structure is a model of some formulae, or whether some series of formulae constitute a proof.

To take a central example: the intuitive or informal definition of validity given in section 1.1 of this chapter invokes a notion of necessity. Informally, the validity of an argument is not being defined in terms of whether the premises or conclusion are or are not true, but in terms of some kind of necessary connection whereby, if the premises were true, this would guarantee the truth of the conclusion. It's not unreasonable to find this notion of

necessary connection rather murky. In formal logic, validity is defined without appeal to necessity, simply in terms of models, which are themselves precisely defined (see section 1.4 of this chapter). The informal approach and the formal logical approach share some subject matters, but treat them in different ways.

### Activity 1.3

Give an example of an invalid argument with true premises and true conclusion.

A very specific connection between formal and informal logic occurs in the notion of **logical form**. As a first approximation, the (classical) logical form of a sentence of English is its translation into the language of (classical) formal logic. The idea is that by so translating, you can better understand the logical and semantic properties of the English sentence. Whether this methodology can be justified is a substantive question in philosophical logic. It's a question that essentially involves comparisons between informal notions (those expressed in ordinary English) and formal ones (those expressed in the formal language of a formal logic).

Philosophical logic, or informal logic, is a branch of philosophy concerned with reflection on the nature of reasoning and its place in our thought. One issue before its tribunal is the relevance of formal logic to this project. The development of formal logics dates back to the late nineteenth century (Frege was a major innovator, along with Venn, Boole, Peano and Russell), since when philosophical logic has not been able to ignore formal logic, which promises finally to provide the precision needed to make woolly philosophical questions answerable. Whether formal logic lives up to this promise, what its methodology is, how it can be justified: these are philosophical questions, not mathematical ones, and are open to dispute.

Although it is these philosophical questions on which you will be examined, it is useful to know some formal logic. Otherwise, the notion of logical form, central to many questions in philosophical logic, will be opaque. If you have some background in formal logic, you can now skip to section 1.5 of this chapter. If the first paragraph of section 1.5 makes no sense, you need to return to this point and read the sections that immediately follow: sections 1.3 and 1.4. If you have a rooted dislike of all things formal, you might be best off omitting, or skipping lightly over, the remainder of this chapter and Chapters 3 and 4. The other chapters make little allusion to formal matters.

## 1.3 The language of classical logic

When people speak of 'logic' or 'formal logic' without qualification, they often have in mind classical first-order logic (sometimes called first-order logic with identity, or

the predicate calculus). The three components of any logic are a language, an account of models for the language, and an account of proofs in the language. In this section I briefly describe **the language of classical logic**. It contains the following primitive elements:

*sentence letters*:  $p, q, r, \dots$  etc.

*sentence connectives*:  $\&, \lor, \to, \neg$  (with roughly the same meaning as 'and', 'or', 'if' and 'not')

*individual constants*:  $a, b, c, \dots$  etc. (corresponding to proper names like 'Fido' or 'London')

*a predicate constant*: = (identity, or being the same as)

*predicate letters*:  $F, G, H, \dots$  etc. (some corresponding to predicates like 'walks', that take one noun phrase to form a sentence – e.g. 'Fido walks'; some corresponding to transitive verbs, like 'loves', that take two noun phrases to make a sentence – e.g. 'John loves Mary'; some corresponding to phrases like 'is a man' and 'is happy')

*variables*:  $x, y, z, \dots$  etc. (functioning the way pronouns sometimes do, as the 'she' in 'If a girl is well-read, she is fun to talk to')

*quantifiers*:  $\forall, \exists$  (with roughly the meaning of 'all' and 'some')

Formulae of the language are formed by arranging these primitive elements in certain permissible ways, which can be precisely defined. Rather than providing the definition, here are some examples of formulae of classical logic (in the left column) and (in the middle column) one or more English sentences that (it is customary to hold) could be formalised by the formula in the left column. The rightmost column lists some common variant symbols.

| $p$                     | Fido barks                                                                 | $\psi$          |
|-------------------------|----------------------------------------------------------------------------|-----------------|
| $\neg p$                | Fido doesn't bark                                                          | $\neg p$        |
| $p \& q$                | Fido barks and Mary is sad                                                 | $p \land q$     |
| $p \to q$               | If Fido barks, Mary is sad<br>If Britain is a monarchy, then<br>Fido barks | $p \to q$       |
| $Fa$                    | Fido barks                                                                 |                 |
| $Gb$                    | Mary is sad                                                                |                 |
| $a=b$                   | Fido is Mary                                                               |                 |
| $\forall x Fx$          | Everything barks<br>For all $x$ , $x$ barks                                | $(\forall)(Fx)$ |
| $\exists x Fx$          | Something barks<br>There is an $x$ such that $x$ barks                     |                 |
| $\forall x (Fx \to Gx)$ | All dogs are happy<br>For all $x$ , if $x$ is a dog, $x$ is happy          |                 |

| $\forall x(Fx \to \exists y(Gy \& Hxy))$    | Every dog has a bone<br>For all $x$ , if $x$ is a dog, there is something, $y$ , such that $y$ is a bone and $x$ has $y$ . |  |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|--|
| $\exists x \exists y(Fx \& Fy \& \neg x=y)$ | There are at least two dogs<br>There is a dog, $x$ , and a dog, $y$ , and $x$ is distinct from $y$                         |  |

### Activity 1.4

This all seems like mumbo-jumbo to me. What should I do?

*Feedback to this Activity can be found on p.43*

**The language of sentential (sometimes called propositional) logic** is a sub-language of the language of classical logic. Its formulae are composed just of sentence letters and sentence connectives. This language does not admit any significant structure below the level of a complete sentence: it contains no quantifiers or predicate letters. For example, it cannot discern anything more in common between 'Mary dances' and 'John runs' than it can between 'Mary dances' and 'There are more than 94 million miles between the earth and the sun'. Sentential logic is a good place to start because it is relatively straightforward. Later we'll single it out for attention, since it enables a very simple account of the role played by **models** in logic.

If we are to use classical logic to help give a general characterisation of the validity of arguments expressed in ordinary English, we need to match formulae of classical logic with English sentences. This enterprise is sometimes called 'finding the **logical form**' of the English sentences, and it turns out to give rise to surprising results. To some, the process seems like a panacea, enabling a better theoretical understanding of what ordinary English sentences really mean; to others it seems like taking a chainsaw to the delicate and complex structures of English.'

*For something close to the panacea view, see Davidson (1970, p.144). For the chainsaw view, see Evans (1982, p.56). Montague (1970, p.188) rejects the debate as I have characterised it: 'I reject the contention that an important theoretical difference exists between formal and natural languages.'*

Classical logic is what is likely to spring to the mind of a philosopher when she hears the word 'logic', but there are many other logics. There are two dimensions of variation from classical orthodoxy: there are logics which expand the language of classical logic and there are logics which have the same language, but which define validity differently.

Three examples of language-expanding logics are second-order logic, set-theory and quantified modal logic. In **second-order logic**, there are quantifiers which bind predicate letters like 'F' and 'G', so there are formulae like:

 $\forall F \exists x(Fx)$ .

### Activity 1.5

What does this formula say? Is it valid?

*Feedback to this Activity can be found on p.43.*

These 'second-order' quantifiers are thought of as ranging over whatever one thinks predicates refer to: properties, perhaps, or sets. There is also a more direct way to move from first-order logic to a logic well adapted to **set-theory**. Two additions are required:

1. An expression for set-membership:

 $\in$  (epsilon):  $x \in y$  abbreviates ' $x$  is a member of  $y$ '.

1. Some way of specifying sets. You can just list their members, marking the list by curly brackets. For example, the set of prime natural numbers less than 10 is: {1, 2, 3, 5, 7}.

Alternatively, you can describe a set using 'set-builder' notation, which is the only practicable approach for sets with many members. The set just given in the list fashion can be described in the set-builder style thus:

 $\{x: x$  is a prime natural number less than 10),  
read 'the set of things,  $x$ , such that  $x$  is a natural number less than 10'. This notation enables us to describe a set whose members cannot all be listed, for example:

 $\{x: x$  is a natural number).

Given these additions, we can define the standard set-theoretic notions, union, intersection, complement and so on, drawing on the resources of classical logic.

### Activity 1.6

If you are familiar with set-theoretic union, show how it can be defined in classical logic supplemented with the notation just specified.

*Feedback to this Activity can be found on p.43.*

An extension of first-order logic that has come to play an increasingly important role in philosophical logic is **quantified modal logic** (QML). This adds the symbol  $\square$  (box), understood to express necessity. The first-order formula  $\forall x(x=x)$  is valid; it can be read: for All  $x$ ,  $x$  is identical to  $x$ . In QML,  $\square$  is to be understood in such a way that a formula like the following will also be valid:

 $\square \forall x(x=x)$ ,

read: necessarily, for all  $x$ ,  $x$  is identical to  $x$  (or: necessarily,  $x$  is self-identical). See **Chapter 3** below.

Variations on first-order logic may take the form not of additional notation (like adding  $\in$  or  $\square$ ) but of an altered understanding of the existing notation. Two examples are paraconsistent logic and free logic.

**Paraconsistent logic** has the same language (the same symbols and formation rules) as classical logic but rejects the validity of the following argument (which is classically valid):

p, not-p; therefore q (for any sentence q whatsoever).

This form of argument was known to medieval logicians as '*Ex Contraditione Quodlibet*' (from a contradiction, infer what you like), and is now more commonly called 'Explosion'. One reason for being interested in logics that do not validate Explosion is that you might wish a database that contained something inconsistent not thereby to contain every sentence whatsoever – it would be nice if the inconsistency could remain localised.<sup>2</sup>

<sup>2</sup>A database is a body of data closed under a relation R: if something in the database is R-related to something, then that too is in the database. (For very trivial databases, R is the identity relation.) If R is classical entailment (i.e. the classical relation of validity), a database containing an inconsistent pair of sentences contains every sentence.

**Free logic** also shares the language of classical logic. It comes in various forms, united by their rejection of the validity of this classically valid argument form:

... a ...; therefore  $\exists x$  (... x ...).

Here the premise is any sentence containing the individual constant 'a', and the conclusion is the result of performing existential quantification with respect to this constant. Often, reasoning of this kind seems plainly correct, as in this argument:

Fido barks; therefore  $\exists x$  (x barks).

Here 'Fido' replaces 'a' and 'barks' replaces the dots. But there are cases in which the pattern raises doubts, for example:

Pegasus does not exist; therefore  $\exists x$  (x does not exist).

Here 'Pegasus' replaces 'a', and 'does not exist' replaces the dots. You might well not wish this to be valid, since the premise is true yet the conclusion seems to say something unacceptable: that there exists something that does not exist. This suggests a motivation for preferring a logic, like free logic, that does not deliver this result.

## 1.4 Models and proofs

In the last section, we merely presented the language of classical logic, a system of symbols, with only cursory remarks about how the symbols should be understood. One important feature of logic is the development of two related notions: **model** and **proof**.

A **model** for a language is a mathematical structure that offers an **interpretation** of the language. Intuitively, an interpretation should assign a meaning to every formula in the language. The concept of meaning, however, is

not very clear, and logicians have no need to appeal to it. Instead, an interpretation can be thought of as something that supplies each formula with a condition under which it is true in a given model. This provides the resources for a precise specification of validity for arguments expressed in the language. The standard definition in terms of models is:

an argument is (model-theoretically) **valid iff**<sup>3</sup>  
every model in which all the premises are true  
is a model in which the conclusion is true.

<sup>3</sup>'iff' is the abbreviation for 'if and only if'.

Compared with the earlier definition of validity, this replaces the notion of necessity by quantification over all models. Given that the notion of **truth in a model** can be precisely defined, we now have a more precise definition of validity.

### Activity 1.7

Using the notion of model-theoretic validity, show that Explosion (see previous section) is classically valid.

We speak of sentences as true or false. In model theory, the plan is to assign entities to reflect various important 'semantic' properties, properties closely related to meaning. Having the truth value true, symbolised T, reflects being true; having the truth value false, symbolised  $\perp$ , reflects being false.

A classical model for a sentential language (that part of the language of classical logic involving just sentence letters and sentence connectives) is an assignment of one or other of the two truth values, T or  $\perp$ , to each sentence letter. Truth values for complex formulae (those containing something other than just a single sentence letter) are computed according to rules, one rule for each sentence connective, with the requirement that every formula gets assigned just one truth value. Using 'M' for any model for a sentential language, and 'f1', 'f2', etc. for arbitrary formulae of the language, the rules are:

& M assigns T to f1 & f2 iff M assigns T to f1' and T to f2'.

v: M assigns T to f1 v f2 iff M either assigns T to f1' or assigns T to f2'.

→: M assigns T to f1 → f2 iff M either assigns  $\perp$  to f1' or assigns T to f2'.

→: M assigns T to → f1 iff M assigns  $\perp$  to f1'.

### Activity 1.8

Would it have been equally good to say: if M assigns T to 'f1' it assigns T to 'f2'? This connects with the discussion of conditionals in Chapter 3.

The result is that **truth in a model** has been defined for every model and every formula of a sentential language.

Here is a simple example of how we can assess the validity of an argument in the language of sentential logic.

**p & q, therefore p.**

The premise is true only in those models that assign T to both 'p' and 'q'; all these models assign T to 'p'. So the argument is valid.

Models for the language of classical logic are more complex, involving a non-empty domain of objects, and assignments of subsets from this domain to predicates, and elements from it to individual constants.

Like a model, a proof is a mathematical structure, though of a very different kind. It is a sequence of formulae meeting highly specific conditions based purely on physical features of the formulae: their shape or form. The aim is that when these conditions are met, later formulae will intuitively 'follow from' earlier ones. This gives rise to an alternative definition of validity:

**an argument is (proof-theoretically) valid if there is a proof of the conclusion from the premises.**

(For details you will need to consult one of the books mentioned earlier: Sider (2010) gives the most detailed account of proofs.)

An interesting fact, which has done much to increase the appeal of classical logic, is that it is **sound and complete**. Its soundness consists of the fact that anything provable (i.e. proof-theoretically valid) is model-theoretically valid, and its completeness in the fact that anything model-theoretically valid is provable. Because models and proofs are structures of very different kinds, their convergence is reassuring, encouraging (rightly or wrongly) the view that classical logic has locked on to a genuine feature of reasoning.

## 1.5 What is a logical constant?

The classical logical constants are the sentence connectives (&, v, →, ¬), the identity sign (=), and the quantifiers (∃, ∀). They are counted 'constants' because their interpretation does not vary from model to model; they are the constant expressions upon which validity hinges. By contrast, sentence letters, individual constants, predicate letters and variables may be assigned different things in different models. They contribute to validity not in themselves, but through the patterns they help create.

Listing the logical constants in a specific language (here the language of classical logic) doesn't give a general account of what it is to be a logical constant. We don't know whether the list should be extended and, if so, how. Should we include  $ext{□}$ ; the expression that is supposed to correspond to 'necessarily'? And  $ext{∈}$  representing set-theoretic membership? If the only criterion is that

some system of models gives an expression a constant interpretation, what's to stop there being a system of models that assigns a constant interpretation to 'London' or 'dances', thus making these expressions logical constants?

A standard view is that logical constants are characterised as expressions that introduce no special subject matter: they are 'topic neutral'. They are therefore available to structure an argument on any topic, and give substance to the suggestion that validity is a matter of structure. Is this criterion necessary? Is it sufficient?

Perhaps identity is a 'special subject matter'. If so, we should not count '=' as a logical constant.

Traditionally, 'but' is not counted as a logical constant, yet it seems to introduce no special subject matter.

### Activity 1.9

Can you think of any other words of which the same might be said?

*Feedback to this Activity can be found on p.43.*

These points throw doubt on the necessity and sufficiency of the topic neutral criterion for being a logical constant. At a minimum, they show that the criterion is somewhat vague. For a full discussion, see John Macfarlane's *article* (2003); and for a defence of the topic-neutral idea, Batchelor (2011).

Let's continue to take classical logic as our guide. On a certain assumption, we can use classical logic to help determine the validity of English arguments. The assumption is that we can match English sentences with formulae of classical logic in such a way that if the formulae constitute a valid argument (in the model theoretic sense), then the matching English argument is valid (in the informal sense). When the matching is successful, in that it meets some yet-to-be-explained standard, we say that the formulae give the logical form of the English argument. So long as we can count on the methodology of logical form, validity in classical logic provides an enormously powerful way of classifying valid arguments in English. To take a simple example, this is a (model-theoretically) valid argument in classical logic:

**Fa therefore 3xFx.**

Assuming a suitable correspondence between English and the language of classical logic, this tells us that a huge number of arguments in English are valid: all those that share the logical form, for example:

**Fido barks, therefore something barks**

**Mary dances, therefore something dances; and so on.**

So formulae which abstract from specific subject matter, and focus just on the logical skeleton, provide the kind of generality logic seeks.

I have presented the idea of the logical constants, and the idea of logical forms (or structures, or skeletons), as part of the same picture. This has been disputed by Gareth Evans (1976), who argues that two notions are in play: (1) validity engendered by some favoured group of expressions, the logical constants; and (2) validity engendered by purely structural features, independently of the specific properties of individual expressions. The inference from 'p & q' to 'p' depends crucially on the meaning of '&' (it fails if we replace '&' by '→'). A purely structural inference, by contrast, would not be engendered by the meaning of any specific expression, but merely by the semantic kind to which the expressions belong and the way they are put together. For example, you could think of this inference as valid purely by virtue of its semantic structure:

**John is a large man; therefore John is a man.**

The essence of Evans's idea is that 'large' belongs to the semantic kind *extensional adjectives*, ones that output a subset of the noun they qualify (large men are a subset of men). This is the structural feature that guarantees the inference. Its validity is independent of the meaning of any specific expression, but is shared with many arguments which use wholly different words: 'This is a red house, so it's a house', 'Mary is a fast runner, so Mary is a runner', and so on.

Evans (1976) is worth a close look, though perhaps not just yet, as it is quite advanced (it would be good to read Macfarlane's SEP article, mentioned above, before embarking on Evans). You will need to decide whether, as Evans suggests, common notions of logical form involve a confusion between the idea of distinctively 'logical' expressions (the logical constants) and semantic structure (definable independently of specific expressions).

# Truth

## Reading

Glanzberg, M. 'Truth', *The Stanford Encyclopedia of Philosophy* (Spring 2009 edition), Edward N. Zalta (ed.), <http://plato.stanford.edu/archives/spr2009/entries/truth/>.

### 2.1 Introduction

Truth occupies a central place in logic. It is involved in the definition of validity. Validity is guaranteed **truth-preservation**: if the premises of a valid argument are true, this guarantees the truth of the conclusion.

Classical logic (and other formal logics) use a notion of **truth in a model**. You can think of a model as like a world or a situation. For example, a model for a sentential language, which assigns a truth value to every sentence, can be likened to a possible situation: one in which how things are accords with the sentences assigned **T** (and so with the negations of sentences assigned **⊥**). We could then define truth itself as **truth in the actual model**, that is, the model in which the sentences are assigned the truth values they actually have. But this would reverse the appropriate direction of explanation. Truth in a model is a notion constructed out of the notion of truth and the notion of a model. We need to understand these components before we can understand the complex they form. The right conclusion is that a full understanding of truth in a model requires an understanding of the unqualified notion of truth.

**Truth is correspondence to the facts. It is the crucial property our beliefs ought to have. Knowledge requires truth. One ought not to assert something unless it is true. Truths cannot be inconsistent. Anything that follows from a truth is true.**

Any adequate account of truth must explain these observations (or explain them away).

We'll explore truth in three phases.

1. There are 'theories of truth' (\$§3-5), for example **disquotational** or **minimalist** theories, the **correspondence theory**, **pragmatist theories**, and **coherence theories**. I'll give some details about the first two, and for the others I'll offer dictionary style entries and pointers to further reading. In thinking about truth, a good plan is to digest at least two of the systematic theories, understand how they are motivated, and appreciate the difficulties they confront.
2. Classical logic assumes a **principle of bivalence**, which is often supposed to apply also to natural language:

there are just two truth values, and every sentence has exactly one of them. This is related to a logical 'law': the Law of Excluded Middle. These claims relate closely to truth (\$§6).

1. Finally, there is an astonishing fact, which forms a topic in its own right: truth gives rise to paradox. We'll start with this (\$2), since the other aspects need to be cognizant of the threat of paradox.

### 2.2 The paradox of the Liar

#### Readings

Beall, J.C. and M. Glanzberg 'Liar Paradox', *The Stanford Encyclopedia of Philosophy* (Spring 2011 edition), <http://plato.stanford.edu/archives/spr2011/entries/liar-paradox/> Sainsbury, R.M. *Paradoxes*. (Cambridge; New York: Cambridge University Press, 2009) third edition [ISBN 9780521720793] Chapter 6.

**A sentence is true iff things are as it says they are; and false iff things are not as it says they are.**

This idea, which goes back to **Aristotle**, would appear to be basic to our understanding of truth. Since work by **Tarski**, it has been customary to suggest that our idea of truth can be captured by **Tarski's schema**, **T**:

**T**: *s is true iff  $p$ .*

*'iff' abbreviates 'if and only if'.*

The position marked by *'s* is to be occupied by an expression that refers to a sentence (typically, we achieve this by placing the sentence in quotation marks); in the place marked by *'p'* we put that same sentence, but this time actually used rather than merely referred to. A classic instance of **T** is:

**'Snow is white' is true iff snow is white. (Compare Tarski, 1944, p.63)**

This is supposed to represent the 'disquotational' character of truth: to assert of a sentence that it is true is equivalent to asserting the sentence itself; it's as if one were removing the quotation marks. It also connects with an idea underlying the correspondence theory of truth: the *iff* in Tarski's schema requires that a true sentence (referred to on its left) should match the world (as described on the right).

Tarski's schema is apt to seem platitudinous, indeed trivially correct. But that's demonstrably not right, since the schema leads to contradictions. Consider the following sentence, L (also known as the Liar sentence):

**L is not true.**

I've just displayed a sentence, the Liar sentence, and I'm telling you a name for it, viz. 'L'. L purports to say of itself that it is not true.

A moment back, we applied **T** to 'Snow is white'. Now let's apply it to L, using the same rules. The result is

**L is true iff L is not true.**

This implements **T**, since 'L' (replacing 's') is a way of referring to a sentence which occurs (and is used) on the right side of the 'iff' (replacing 'p'). But it is tantamount to a contradiction.

It's natural to feel a bit queasy about L. Has it really been properly defined, given that we have used the name 'L' in saying what the name stands for?<sup>2</sup> Even if such considerations gave reasons for not allowing L itself into Tarski's schema, truth would still generate a similar paradox. The following dialogue contains perfectly understandable sentences, yet leads to essentially the same paradox:

<sup>2</sup>Here's a more user-friendly version of essentially the same paradox. The *University of Texas Philosophy Department used to sell a T-shirt which had on the front the words 'What's written on the back of this shirt is true'. On the back were the words 'What's written on the front of this shirt is not true'.*

A (on Monday): Everything B will say tomorrow is true.

A said nothing else on Monday.

B (on Tuesday): Nothing A said yesterday is true.

B said nothing else on Tuesday.

(Compare Burge, 1978, p.90; he attributes the example to Buridan.) What B said is true only if what A said, in saying 'Everything B will say tomorrow is true', is false. So what B said is true only if it is false. If what B said is false, then something A said on Monday is true. But A said only one thing, and that entails that what B said on Tuesday is true. So what B said is true iff it is false.

### Activity 2.1

Show that the reasoning depends upon **T**, or something like it.

Feedback to this Activity can be found on p.43.

Here are some of the ways proposed to deal with this paradox (for general discussion, see Martin, 1984, Introduction):

1. Tarski himself thought that the paradox showed that no language could contain its own truth predicate (a word applying to just the true sentences of the

language). Instead, we need to ascend to a higher level (a metallanguage). The technicalities of this 'Tarskian hierarchy' are fairly daunting. Philosophically, an interesting question (about which Tarski seems to have changed his mind) is whether the paradoxes show that our ordinary conception of truth is incoherent.<sup>3</sup> See Sainsbury (2008).

<sup>3</sup>One thing he could think is that English is a single language, and so cannot contain its own truth predicate; that's what leads to the idea that English is incoherent. Another thought is that there is an implicit hierarchy of languages within what we call English, so that our ordinary language (or rather languages) have the resources to contain coherent truth predicates.

1. Paraconsistent logicians have held that the Liar sentence is an example of a *dialetheia*: a sentence that is both true and false. On this view, bivalence fails, and it's important that the logic should not contain Explosion (see above). The classic source is Priest (1987); see also his SEP entry.

### Activity 2.2

Why is it important that a logic which permits dialetheias should not contain Explosion?

Feedback to this Activity can be found on p.43.

1. Bertrand Russell held that the problem arose from a kind of circularity, and he proposed the 'vicious circle' principle. Liar paradoxical sentences would infringe the principle, and so should not be counted as genuinely intelligible sentences. An early presentation is in Russell (1908), embedded in some very difficult material. A brief informal presentation is in Sainsbury (2008).
2. On various grounds, it has been suggested that the Liar sentence is neither true nor false (another way of rejecting bivalence). The best-known version of this approach is by Kripke (1975). As Kripke recognises, his theory has difficulties dealing with the specific Liar sentence presented here (as opposed to something more like 'This very sentence is false'). More details can be found in Sainsbury (2008).

It's possible that a final solution of the Liar paradox will require abandoning Tarski's schema, but in the remainder of this chapter I shall assume that it will survive (perhaps in a qualified form).

## 2.3 Deflationism

### Readings

Blackburn, S. and K. Simmons (eds) *Truth*. (Oxford: Oxford University Press, 1999) [ISBN 9780198752509].

Horwich, P. The minimalist conception of truth in Blackburn, S. and K. Simmons (eds) *Truth*. (Oxford: Oxford University Press, 1999) [ISBN 9780198752509].

## Chapter 2: Truth

Horwich, P. *Truth*. (Oxford: Basil Blackwell, 1990) [ISBN 0631173161].

Wright, C. *Truth and Objectivity*. (Cambridge, Mass.: Harvard University Press, 1992) [ISBN 0674910877].

Once we have Tarski's schema, what **else** needs to be said about truth? One possible answer is: nothing (or almost nothing). Theorists who offer this response are often called deflationists. The terminology here is not fixed, but I see deflationists as coming in at least three varieties: disquotationalists, redundancy theorists and minimalists. These theorists do indeed end at a similar point, but there are differences of emphasis.

**Disquotationalists** appeal to Tarski's schema as constituting all, or almost all, we need to say about truth. Truth is anything that can correctly fill the blank in

s is — iff p

provided that what is referred to by what replaces 's' also replaces 'p'.

Another way to put much the same underlying idea is this. Suppose someone speaks a language which does not contain the predicate 'true', or any equivalent. We could introduce him to the predicate in the following way: whenever he utters something assertively, for example 'p', we could say: you could just as well have said "p' is true'. We use the notion of equivalence (just as well as), but this does not make use of the notion of truth. We use instances of the schema to explain truth, without taking truth itself for granted.

This approach, as its adherents appreciate, needs to do something about the Liar paradox, which threatens the correctness of Tarski's schema. Adherents often say that there has to be some way of restricting the schema, and they will simply adopt that way (Horwich, 1990, pp.41–42). A proper question is whether the restriction can be characterised independently of the notion of truth.

Disquotationalists need to differentiate being true from various apparently distinct notions which seem to be candidates for playing a similar role, for example: is knowable, corresponds to the facts, is useful to believe, will be accepted by all impartial enquirers in the long run. It seems that these are all candidates for correctly filling the blank in s is — iff p. They also need to say more about what a sentence is, or at least a sentence apt for truth. Liar sentences raise their heads at this juncture, but there are other problems: nonsense sentences, imperatives and, arguably, value judgments. Sentences like 'Torture is wrong' have been claimed not to be the sort of sentence to which truth or falsehood can be significantly applied, and so we ought to reject

**'Torture is wrong' is true iff torture is wrong.**<sup>4</sup>

<sup>4</sup>David Hume (1740, Book 3) is often cited as an early proponent of this view. A version of a broadly Humean position might use the following premises: (a) a sentence can express a belief iff it is the sort of thing to which the notion of

**truth significantly applies**, (b) every action's motivation must include something which is not a belief (a desire), and (c) a moral view, together with beliefs, is enough to motivate an action. From these it follows that a moral view is not a belief, and hence that an expression of it is not the sort of thing to which truth or falsehood significantly applies.

In the 'emotivist' school of ethics, sentences like 'Torture is wrong' have been likened to expressions of feeling, like 'Ugh!' or 'Boo!' (for disapproval) and 'Wow!' or 'Hooray' (for approval). (See, for example, Ayer, 1936, Chapter 6.) It looks as if we are using a prior grasp of the notion of truth to restrict Tarski's schema, rather than extracting all we need to know about truth from the schema.

### Activity 2.3

Horwich (1999, pp.246–47) suggests that this 'anxiety' reveals 'philosophical confusion'. Is he right?

**Redundancy theorists** claim that truth is a redundant notion, for instead of using it to say of a sentence that it is true, we could as well just assert the sentence itself (see Ramsey, 1927).

This needs some qualification. We can predicate truth even in situations in which we are in no position to assert the sentences of which we predicate it. For example, knowing that you are invariably honest and well-informed, but not knowing what you said when you spoke on the radio, I might say 'Everything you said on the radio is true'. Since I don't know what you said, I cannot simply repeat your sentences; I need the predicate 'true'.

The standard response by redundancy theorists is that even in cases like this I don't need to use 'true', because I could have expressed myself as follows:

**For all p, if you uttered p during your radio talk, then p.**

How is the quantification to be understood? Perhaps 'p' ranges over sentences, occupying the kind of position that could be occupied by a **name** of a sentence. (Compare: In 'for x, if x is a man, x is mortal', the variable ranges over objects. That is, it could be replaced by a **name** of an object, e.g. by 'Socrates') This will make sense of the occurrence of 'p' in 'He uttered p', for here we do state (in a general way) a relationship between the speaker and a sentence we refer to. But it will not make sense of its last occurrence. This marks a position which needs to be occupied by a sentence, and not by a name of a sentence.

### Activity 2.4

Could matters be improved if we replaced 'uttered p' by 'said that p', and construed the quantification as over propositions – the things which sentences state?

The redundancy theorist may suggest construing the quantifier as **substitutional**.<sup>5</sup> The displayed formula would amount to the claim that, whatever sentence you put for 'p' in the following:

<sup>5</sup>See Sainsbury (2001), 4.18.

**if you uttered p during your radio talk, then p**

the result is true. This may serve to make sense of the quantification (though even this is debatable), but it clearly does not serve the purposes of the redundancy theory of truth, since the quantification is explained in terms which make essential use of the supposedly redundant predicate 'true'.

A standard criticism of the redundancy theory (made, for example by, Dummett, 1959) is that it fails to make room for the desirability of truth: for the fact that it's a property we want our beliefs to have and the informative utterances of others to have. Horwich (1999, p.256) counters that there is no real problem here, for our desires can be expressed without alluding to truth. We want to believe that it's raining iff it's raining, that today is Tuesday iff today is Tuesday, and so on.

## Activity 2.5

How adequate is this reply?

*Feedback to this Activity can be found on p.43.*

**Minimalists** (e.g. Horwich, 1990) draw on Tarski's schema and some of the ideas behind redundancy theories, and conclude that truth is not a 'substantive' property and does not have a 'nature'. They allow, however, that the word 'true' has a valuable use: it enables us to express generalisations, for example that every instance of the schema 'if p then p' is true. What is it for a property not to be substantive or not to involve a 'nature'?

Horwich allows that if we have a very weak conception of what a property is, so that every intelligible predicate expresses a property, then there is such a property as truth. What he denies is that truth is a property in a richer sense, one that would make further investigation of the nature of this property appropriate. Tarski's schema tells us everything there is to know about truth. Hence there is no scope for any further investigation into its nature. That's not because we lack the tools to undertake the investigation, but because there is nothing further to investigate.

Here are two problems that have been raised for minimalism (they apply to some extent to all deflationary accounts of truth):

(i) As Horwich (1999) is aware, opponents will claim that Tarski's schema is not enough to deliver various alleged platitudes about truth: that one should aim to believe what is true, that one should tell the truth, that to assert is to present as true, that truths cannot conflict, and so on. Unless you have grasped the role of truth in believing,

speaking and asserting, you have not fully understood it. You will need to decide whether Horwich's responses to these charges are adequate.

(ii) Since distinct properties might apply to the same things (e.g. the property of having a heart and the property of having kidneys), we might know how to apply 'true' (apply it to just those sentences you are disposed to assert with sincerity) without thereby knowing what property the word expresses, and thus without having fully understood it. For example, the predicate 'is true and 17 is a prime number' holds of just the things that 'true' holds of, yet it plainly has a different meaning. Is Horwich's response to this objection adequate?

## 2.4 Correspondence

### Readings

Horwich, P. *Truth*. (Oxford: Basil Blackwell, 1990) [ISBN

0631173161] Chapter 7.

Strawson, P. 'Truth', *Supplementary Proceedings of the Aristotelian Society* 24 (1950) pp.129–56.

A sentence is true just if it corresponds to the facts. No one could dispute this claim, as it is naturally understood. 'Is true' and 'corresponds to the facts' appear interchangeable. One question is whether the correspondence theory contains anything helpful or whether it gives us just an uninteresting terminological variant of 'is true'.

If we take the notion of correspondence seriously, we need to have two domains that are independently specifiable. On one side, language or thought supplies the things that have the property of being true. These are the 'truth bearers', the entities that are suitable candidates for being ascribed truth and falsity. On the other side, facts or reality need to be things that can be specified independently of the truth bearers, things to which the truth bearers may or may not correspond. Thinking about facts with this need in mind may make you wonder whether they are really independent of truth-bearers.

This suspicion was famously raised by Strawson: 'facts are what statements (when true) state... If you prise the statements off the world you prise the facts off it too; but the world would be none the poorer' (1950, pp.38–39). The suggestion is that facts, the things to which statements correspond iff they are true, are really no more than the true statements themselves. In some trivial sense there is correspondence; but this is not correspondence with a language-independent reality.

The view that facts are language-dependent, and so unfit to be the worldly relatum in a correspondence theory of truth, can be reinforced by considering when facts are the same and when they are different. Is the fact that Leningrad is on the Neva the same as, or different from, the fact that St Petersburg is on the Neva? There is

some temptation to say we have just one fact, expressed differently. Then the sentences 'Leningrad is on the Neva' and 'St Petersburg is on the Neva' correspond to the same fact. In that case, it shouldn't matter which sentence you use. But in many circumstances it does matter. Suppose someone is planning a trip to St Petersburg and has no historical knowledge. He asks 'Is there a river there?' The answer 'St Petersburg is on the Neva' is fine; but 'Leningrad is on the Neva' is not. This is hard to explain if the answers state the very same fact.

A further consideration points in the same direction. If we make the 'liberal' response just considered, then why not regard 'The town founded by Peter the Great is on the Neva' as stating the same fact? But then you might as well say that the same fact is also stated by a sentence along the lines of 'The town founded by Peter the Great, who was tall and thin and made great strides towards modernising Russia, is on the Neva', and the notion of a fact will get entirely out of hand.<sup>6</sup>

*<sup>6</sup>This is a very informal version of an argument (the so-called 'slingshot') made use of by Davidson (1970 and other writings).*

So suppose that we say, instead, that all the facts just discussed are distinct. The problem is that it seems that the only reason we can give for the difference is that we have used different words to refer to the town. This suggests that facts are not the language-independent entities they were meant to be.

Does this problem show that the correspondence theory is not the truism it seems? I think there are two theses at issue: one genuinely platitudinous and the other quite substantive. The platitudinous thesis makes no attempt to say which facts a given truth corresponds to. Instead of saying that truth consists in correspondence to the facts, one could as well present this view as that truth corresponds to how things are, or to reality. There is no attempt to set up a detailed correspondence between truths and their distinctive proper part of reality. That yields the platitudinous thesis. The substantive thesis is that for every truth there is a tailor-made part of reality. That's what requires, for example, a carefully worked out doctrine of facts. And that's what leads people to associate adherence to a correspondence theory with such philosophical positions as realism (as opposed to idealism), empiricism (as opposed to rationalism) and so on. The non-platitudinous correspondence theory does have to say a lot about the nature of reality, and in doing so is likely to presuppose, or exploit, substantive metaphysical positions.

A currently much-debated view, which has its origins in the kinds of intuitions that have animated correspondence theories, is truth-maker theory (see e.g. Rodriguez-Pereyra, 2006). The idea is that every truth is made true by some specific stretch of reality. As with the original correspondence theory, truths like 'Dodos are extinct' raise problems – and exercise good minds.

## 2.5 Pragmatism, coherence, identity

**Pragmatist theories** of truth are associated with Charles Pierce and William James. According to one version, truth is that on which opinion is destined to converge:

The opinion which is fated to be ultimately agreed to by all who investigate, is what we mean by the truth.

(Houser and Kloesel (eds), 1992, p.139)

According to another version, the true is what it is expedient to believe (James, 1907, p.106).

**Coherence theories** of truth claim that truth is a matter of coherence with some specified set of sentences (perhaps those expressing everything we believe at present).

**Identity theories** of truth may start with the thought that if what is believed is true, that very thing is the case. When we have true belief, what is believed (for example, that snow is white) is strictly identical with this thing (for example, that snow is white).

## 2.6 Bivalence and excluded middle

The principle of **Bivalence** says that every sentence (or every bearer of truth or falsehood) is either true or false and not both. This is a 'semantic' principle: it concerns how sentences relate to the world. There is an associated logical principle, the **Law of Excluded Middle (LEM)**. Applied to the language of classical logic, it says that every formula of the form

A  $ightarrow$   $ext{ extasciitilde} A$ 

is valid. Applied to English, it says that every sentence of the form

**S or it is not the case that S**

is true. Bivalence is not the same as LEM (although there are connections, as we will see in a moment). To state LEM you have to refer to some specific expressions ('v' and ' $ext{ extasciitilde}$ ', or 'or' and 'not'); this is not so for Bivalence.

Classical logic is bivalent and LEM holds in it. Does that reflect how things are in English? **Many-valued logics** reject Bivalence; so, in a different way, do **paracomistent logics**. So there's a question: which logic's treatment of Bivalence is right?

Aristotle wondered whether the claim that there would be a sea battle tomorrow was true or false. He thought that neither answer was correct, since the future is open: maybe there will be a battle, maybe not. It's not merely that we don't know whether 'There will be a battle' is true or false: it simply is neither, so Bivalence is abandoned.

If we think of truth as truth-now and falsity as falsity-now, and we think that the future is not yet determined, it follows that 'There will be a sea-battle tomorrow' is neither

true nor false. We could introduce a third truth value – say **Indeterminate** – to mark this status. Then there would be three truth values, contrary to Bivalence.

Aristotle himself thought that either there would or there would not be a sea battle tomorrow. In other words, although he wanted to reject Bivalence, he wanted to keep LEM. Even if it's **not** determinate whether there will be a battle or not, it **is** determinate that either there will be a battle or there will not. Making room for this combination of views in a systematic way is not entirely straightforward (one approach uses supervvaluations – see Macfarlane, 2003), but there's no doubt that it's coherent.

**Intuitionist logicians** argue that to assert something is to commit to there being a proof of it. Proving a disjunction requires proving at least one disjunct. Since we cannot prove that there will be a battle tomorrow and cannot prove that there will not be, we are in no position to assert the disjunction. So we cannot assert LEM. (We cannot deny it either, on intuitionist principles, for to deny something is to commit to being able to prove an absurdity from it, and in general no absurdity follows from 'S or not-S') Intuitionists, however, cannot affirm Bivalence. Any logic that accepts Bivalence would have to have implausible views about negation or disjunction or both to avoid commitment to LEM. Given Bivalence, 'S' is either true or false. If it is true, the disjunction is true. If 'S' is false, then the only value 'not-S' can reasonably have is true, in which case, again the disjunction is true.

Many-valued logics are sometimes called 'gap' logics, since they say there is a gap between truth and falsity and some sentences fall in the gap. Paraconsistent logics, by contrast, are sometimes called 'glut' logics, since they hold that one and the same sentence can be both true and false. This is a different way of denying Bivalence. (As in the case of Aristotle, these logicians can coherently affirm LEM.)

## Activity 2.6

Explain how one can coherently deny Bivalence yet affirm LEM.

*Feedback to this Activity can be found on p.43.*

There is a nice phrase from a leading paraconsistent logician suggesting a philosophical basis for truth value gluts:

**Truth and falsity come inextricably intermingled... One cannot, therefore, accept all truths and reject all falsehoods...**

(Priest, 1986, p.106; cf. Priest, 1987, p.124)

If truth and falsity are thus intermingled, they can perhaps characterise a single sentence. The Liar sentence would be a prime example.

Let's step back and reconsider whether Bivalence or LEM hold for a natural language like English. Plainly there are English sentences that are neither true nor false, for example, questions, commands and sentences with indexicals, such as 'I am hungry'. Sentences in the last category may be said to be true or false of some person, at some time, but they cannot sensibly be regarded as simply true or simply false. This consideration does not show that English is not Bivalent, for, properly stated, the thesis is this:

**Bivalence:** Every truth-bearer has just one of the two truth values (true, false).

Questions, sentences with indexicals and so on are not truth-bearers, so the fact that they are neither true nor false is irrelevant to the thesis. On the other hand, 'There will be a future sea battle tomorrow' and the Liar sentence both look to be truth-bearers, so if they have either no truth value or both truth values, it seems that Bivalence doesn't hold for English.

Another reason for denying Bivalence and/or LEM for English stems from vagueness. If something is on the borderline between red and orange, perhaps 'This is red' is neither true nor false, but has some indeterminate status (see Chapter 7).

Finally, you may deny Bivalence for sentences exhibiting reference failure. A historically famous example is 'The present King of France is bald' (see Chapter 5).

# Modality

## Reading

Melia, J. *Modality*. (Durham: Acumen, 2003) [ISBN 0198247125].

### 3.1 Boxes and diamonds

In recent years modal logic has become very influential. The resurgence in philosophical interest in it is associated in particular with Saul Kripke and David Lewis. Kripke produced some ground-breaking formal results (1959, 1963) and went on to offer arguments about names, reference, the apriori and the mind-body problem that were in some ways influenced by these results.<sup>1</sup> (The arguments are in *Naming and Necessity*, lectures given in 1970, and published in book form in 1980.) David Lewis is best known for his radical metaphysical view that merely possible worlds are just as real as the actual world (see, in particular, Lewis, 1986). This chapter gives an indication of the logical aspects of some of this work.

<sup>1</sup>His conception of rigid designation, though neither his arguments for its presence in natural language, nor his applications of it, was anticipated by Ruth Barcan Marcus. For an amusing journalist's account of the feud over priority (far from amusing for the protagonists) see Holt, 1997.

In natural language, various notions of necessity are expressed by various idioms, including 'necessarily', 'must', 'have to', 'guarantees':

1. **Necessarily**, if sparrows are birds, sparrows are birds.
2. You **must** leave now or you'll miss your plane.
3. You **have to** make adequate financial provision for your children.
4. Pressing down on one end of a rigid rod, freely balanced at its centre, **guarantees** that the other end will go up.

In these examples, no doubt different standards or criteria of necessity are invoked. Perhaps only (1) invokes logical necessity. Perhaps the necessity in (2) has something to do with the demands of prudence, in (3) with the demands of morality and in (4) with natural laws. We'll first try to specify the notion of **logical** necessity, and then say something about how it is standardly formalised in quantified modal logic (QML).

Logical necessity ought to be necessity that is engendered by logical features. Intuitively, we think of logical necessity as some single (if possibly not fully clear) notion. Yet, as we have seen, there are many logics: classical logic, paraconsistent logic, intuitionist logic and so on. Does this mean that, contrary to intuition, there are as many notions of logical necessity?

That's a matter for dispute. My own suspicion is that the notion of logical necessity is fully cogent only if there is a unique 'right' logic. Logical necessity would then correspond to validity in this favoured logic. There is a unique right logic only if there is a unique right answer to the question, raised earlier: what is a logical constant?

#### Activity 3.1

Suppose there is a unique set of 'right' logical constants. Does it follow that there is a unique 'right' logic?

*Feedback to this Activity can be found on p.43.*

Without resolving this issue, logicians can nonetheless study a notion of necessity, and leave it to philosophers to say how it should be interpreted. The standard approach uses the language of QML, arrived at by adding a symbol, '□' (pronounced 'box'), to the language of classical logic. Thinking of this as expressing necessity, one can define the notion of possibility, ◇ (pronounced 'diamond'), as follows:

$$\text{◇A} = \text{df} \neg \text{□}\neg \text{A}.$$

Expressed more informally: what is possible is, by definition ( $\text{◇}_A$ ), what is not necessarily not the case.

The quality of some philosophical discussions has been raised by an appreciation of scope distinctions that are easy to see in QML.<sup>2</sup> For example, the ordinary English 'Mathematicians are necessarily mathematicians' is arguably ambiguous, in ways that can be brought out either in rather unidiomatic English, or with all the clarity of QML:

<sup>2</sup>The examples will make it plain what scope is: the scope of a logical constant is the part of the formula it modifies.

1. Necessarily, any mathematician is a mathematician.  
    $\square \forall x (Mx \to Mx)$
2. Any mathematician is necessarily a mathematician.  
    $\forall x (Mx \to \square Mx)$

Intuitively the first is true and the second false.

Mathematicians could have chosen other careers. In the QML formalisations, it's easy to see how the box has very different scopes in the two cases.

#### Activity 3.2

Use this distinction to diagnose a fallacy in the following claim: a bachelor can never marry – for then he would not be a bachelor.

Another ambiguous English modal sentence is 'Something has to be human', which can be disambiguated as follows:

1. Necessarily, something is human.  $\square\exists x(Hx)$
2. Something is such that it is necessarily human.  $\exists x\square(Hx)$

The first is false: it could easily have been that no planet would support life. The second is arguably true, for, arguably, anything which is in fact human has to be human.

### Activity 3.3

Ovid tells of Achtaea, a man who was turned into a stag. Does this show that a human could fail to be human?

Feedback to this Activity can be found on p.43.

The distinction in these pairs has sometimes been referred to as the distinction between *de dicto necessity* (for the first member of each pair) and *de re necessity* (for the second member). *De re necessity* is expressed by using the box in narrow scope. This has been crucial in the formulation of **essentialist** theses, theses according to which some objects have some properties essentially (as (8) suggests that humans have the property of being human essentially). Formulated roughly, an **essential** property of an object is one it could not lack (see Chapter 7 below).

What are the **laws** of necessity? What does modal logic tell us? As with logic in general, we again find variety where we might have hoped for a single body of doctrine. This variety starts right at the beginning, with the sentential fragment of QML (the part that's left after the quantifiers, predicates letters, variables and individual constants have been removed). (Adding the quantifiers back in raises a lot of further issues which we'll not discuss, though you'll find a good account in *James Garson's* contribution to the SEP.)

Sentential modal logic is normally developed in the first instance through proofs rather than models. The ambition is to see what theorems should govern  $\square$ , and how sentences dominated by  $\square$  or  $\Diamond$  affect proofs. Two principles are generally taken to be indispensable:

Necessitation: if A is a theorem, so is  $\square A$ .

Importation:  $\square(A \to B) \to (\square A \to \square B)$ .

As an example of necessitation: ' $p \to p'$  is a theorem, hence so is  $\square(p \to p')$ '. Modal logics which have these two principles are said to be K-logics. But we clearly need more. For example, we need to reflect in the logic that anything that is necessary is in fact the case:

M:  $\square A \to A$ .

When M is added to a K-logic, the result is sometimes called an M-logic (or a T-logic). So far, there is little controversy. Two more controversial additions are:

S4:  $\square A \to \square \square A$ 

S5:  $\Diamond A \to \square \Diamond A$ .

Logics which add these axioms to M are called, respectively, S4-logics and S5-logics. Both axioms are controversial.

Lewis (1932) said that which truths are necessary is not a contingent matter: what is necessary has to be necessary. This speaks in favour of S4. Yet the suggestion is debatable. Perhaps God is the source of necessity, but is unconstrained in how he distributes this property: it is not necessary that he should assign it as he does, so what is in fact necessary might not have been necessary.

S5 has a surprising consequence that might call its correctness into question. Consider this version of the ontological argument for God's existence:

1. The notion of God, as a necessary being, is conceivable, and so possible.

10. Whatever exists of necessity, exists.

11. So God exists.

(10) might be seen as a consequence of (M). If (9) is understood as saying that possibly necessarily God exists, and S5 is correct, (11) follows: from  $\square\Diamond$ God exists' we can infer 'God exists'. Even atheists, it may be argued, should accept the premise; so, given S5, they are forced to abandon their atheism.

### Activity 3.4

Can you spell out the argument in more detail? It's enough to establish that the following is a theorem of S5:  $\square\Diamond A \to A$ .

Feedback to this Activity can be found on p.44.

Models for modal logics are standardly given in terms of **possible worlds**. These are complete possible states of affairs that could obtain (but only one of which actually does, namely the actual world). Examining models that exploit possible worlds may help us decide what the 'right' modal logic is. A model for a modal sentential logic assigns to each sentence or formula not merely a truth value with respect to the actual world, but a truth value with respect to every possible world. For every world and every sentence letter, a truth value is assigned to that sentence letter with respect to that world. These assignments lead to assignments to every formula by the following rules:

& for all worlds,  $w$ ,  $M$  assigns  $\top$  to  $f1$  &  $f2$  with respect to  $w$  iff  $M$  assigns  $\top$  to  $f1'$  with respect to  $w$  and  $\top$  to  $f2'$  with respect to  $w$ 

<sup>1</sup> 'iff' is the abbreviation for 'if and only if'.

 $v$ : for all worlds,  $w$ ,  $M$  assigns  $\top$  to  $f1$  v  $f2$  with respect to  $w$  iff  $M$  either assigns  $\top$  to  $f1'$  with respect to  $w$  or assigns  $\top$  to  $f2'$  with respect to  $w$ 

 $f1'$  with respect to  $w$  or assigns  $\top$  to  $f2'$  with respect to  $w$ 

 $\to$ : for all worlds,  $w$ ,  $M$  assigns  $\top$  to  $f1 \to f2$  with respect to  $w$  iff  $M$  either assigns  $\top$  to  $f1'$  with respect to  $w$  or assigns  $\top$  to  $f2'$  with respect to  $w$ 

→: for all worlds,  $w$ ,  $M$  assigns  $T$  to  $\neg f1'$  with respect to  $w$  iff  $M$  assigns  $\perp$  to  $f1'$  with respect to  $w$ .

□: for all worlds,  $w$ ,  $M$  assigns  $T$  to  $f1'$  with respect to  $w$  iff for all worlds  $w'$  accessible to  $w$ ,  $M$  assigns  $T$  to  $f1'$  with respect to  $w'$ .

◊: for all worlds,  $w$ ,  $M$  assigns  $T$  to  $\neg f1'$  with respect to  $w$  iff for some world  $w'$  accessible to  $w$ ,  $M$  assigns  $T$  to  $f1'$  with respect to  $w'$ .

Validity is truth on every model with respect to every world.

What is this relation among possible worlds, according to which a world can be 'accessible to' another? Technically, it is a primitive in the semantics, so it can vary as you wish. Let's start by supposing that the relation imposes no restrictions at all, in other words, that for any worlds  $w1$  and  $w2$ ,  $w1$  is accessible to  $w2$ . Then  $S5$  is valid. Informally, suppose an arbitrary model,  $M$ , assigns the antecedent  $\langle A \rangle$  of the conditional  $T$  with respect to some world  $w$ . Then  $M$  assigns  $T$  to  $A$  with respect to some world  $w'$ . Every world  $w^*$  is accessible to  $w'$ , so  $M$  must assign  $T$  to  $\langle A \rangle$  with respect to every  $w^*$ . That is to say that  $M$  must assign  $T$  to  $\langle A \rangle$  with respect to  $w$ .

Are there reasons to restrict the accessibility relation, so that it does some real work? Here is one possible argument – you will need to decide whether it is sound. For many things, notably artifacts, we are inclined to allow that some changes in its parts are consistent with its surviving (I can replace the wheels on my bike, and it's still the same bike). But to replace all the parts would be for the original no longer to exist (if, in one afternoon, I change out all the parts on my bike, frame included, I have a new bike, not a modified old one).

To simplify, let's suppose there is some object,  $O$ , meeting this condition: if you change two of its parts, it remains the same thing, but if you change more, it ceases to exist. Could  $O$  survive the replacement of no more than two parts? Yes, that follows from what has just been said. Could it survive the replacement of exactly three parts? No; that follows too. We might try to represent these facts as follows:

 $\langle O \rangle$  survives a 2-change) and  $\neg \langle O \rangle$  survives a 3-change).

The notion of 2-change and 3-change is implicitly relative to  $O$ 's actual condition. What's at issue is how many parts are changed relative to how  $O$  is here and now. Suppose  $w$  is a world at which  $O$  has undergone a 2-change. We know that  $O$  exists at that world. But then could it not undergo a further 2-change? That is, is there not a world,  $w'$ , at which it has changed 2 parts relative to how it was in  $w$ ? At  $w'$ , it would have undergone a 4-change relative to its actual condition, but only a 2-change relative to its condition at  $w$ . Does not the last point mean that, if it exists in  $w$ , it exists in  $w'$ ? And then, since it could exist at  $w$ , are we not forced to say that it could exist at  $w'$ , in conflict with the original ruling that  $O$  could not survive a 3-change?

What we are being asked to consider is whether the fact that a change is possible relative to  $w$  entails that it is possible relative to our actual world. If every world were accessible to every other, we would have to answer that it is, and that leads to a contradiction:  $O$  could have both survived 4-change and also could not have done so. This is the argument suggesting that we ought to restrict the accessibility relation. Moving from models to questions of what to take as provable, the considerations would show that we should not allow  $\langle A \rangle \to \neg \langle A \rangle$  as a theorem.

### Activity 3.5

The argument is presented rather sketchily. It needs filling out – and then it needs to be evaluated.

Feedback to this Activity can be found on p.44.

## 3.2 Counterpart theory

It's normal to use possible worlds in giving semantics for modal logics. Lewis has suggested that we bypass modal logic altogether, and instead speak directly of worlds. He says that this has expressive advantages (I won't consider these here, but you'll find a discussion in Sainsbury, 2001, section 5.8). Moreover, as we'll see, it suggests a way of giving a reductive account of what necessity is.

Lewis invites us to think of possible worlds, and their merely possible inhabitants, as just as real as our actual world and its actual inhabitants. To be merely possible is just to be non-actual, not to be unreal. To say that there might have been unicorns is to say that there are (real but) non-actual possible worlds in which there are unicorns (real but non-actual beasts). To say that everything scarlet has to be red is to say that in every possible world, the scarlet things in it are red.

Within this metaphysical framework, Lewis develops what he calls 'counterpart theory' (Lewis 1968, 1986). There are two leading ideas. One is that objects are 'world-bound': no object exists in more than one world. Lewis gives an argument for this view, though I'll not rehearse it. The upshot is that one cannot treat the possibility that Socrates should have had an aquiline nose as amounting to there being a world containing an aquiline-nosed Socrates. The actual Socrates was snub-nosed, and he does not exist at any world other than the actual one. So the possibility in question has to be registered as there being a world containing an aquiline-nosed **counterpart** of Socrates. A counterpart at a world  $w$  of an object  $O$  resembles  $O$  more closely than does anything else in  $w$ . Since each object exists at just one world, in identifying an object we have thereby fixed a world. So we can simplify the account of Socrates possibly being aquiline-nosed: he has an aquiline-nosed counterpart. Similarly, 'Socrates is necessarily human' can be rendered in counterpart theory as 'All counterparts of Socrates are human'.

The other leading idea is that what it is for a sentence to be true 'at' or 'with respect to' a possible world is for it to be true when its quantifiers are restricted to things in that world. For 'All beer is good' to be true in Australia is for all beer in Australia to be good. Rather similarly, for 'All beer is good' to be true with respect to a world  $w$  is for all beer in  $w$  to be good.

The language of counterpart theory results from adding four primitive predicates to the language of classical logic:  $Wx$  ( $x$  is a possible world);  $lx$  ( $x$  is in possible world  $y$ );  $Ax$  ( $x$  is actual); and  $Cxy$  ( $x$  is a counterpart of  $y$ ). Lewis claims that the resulting language can express more than one can express with just boxes and diamonds.<sup>4</sup>

*<sup>4</sup> This claim is uncontroversial. It's more controversial whether counterpart theory can express more than QML supplemented with an operator meaning 'actually'.*

He also claims that counterpart theory can help resolve disputes. For example, he claims that it reveals that identity is not a necessary relation, in the sense that neither of the following is valid in counterpart theory:

$$a=b \rightarrow \square a=b$$

$$a \neq b \rightarrow \square a \neq b.$$

The first says that if  $a$  and  $b$  are identical, they have to be identical. The second says that if  $a$  and  $b$  are distinct they have to be distinct. The first is not valid in counterpart theory since one object may have more than one counterpart. The second is not valid in counterpart theory since two objects may share a counterpart.

### Activity 3.6

Does counterpart theory give the right verdict? Can't we argue from the premise that everything is necessarily itself to the conclusion that identity is a necessary relation? (See also *Chapter 8*.)

*Feedback to this Activity can be found on p.44.*

A natural reaction to the use of possible worlds in explaining necessity and possibility is that we have made no progress: if the notion of possibility is obscure, so will be the notion of possible worlds. This criticism might be aimed at QML, in the light of its use of possible worlds in its models; and it might more obviously and directly be aimed at counterpart theory.

In neither application is the criticism entirely fair, for two reasons. First, the machinery of possible worlds, either in the models for QML or in counterpart theory itself, does enable one to clarify issues and distinctions, even if it does not deliver a reductive analysis of the notion of possibility. The second reason is that David Lewis has proposed a reductive analysis of what a possible world is: a possible world is the sum of all those things that are related in space and time. The analysis draws on the assumption that

things in different worlds stand in no spatial or temporal relations. Take an arbitrary object, actual or possible. Its world consists of all the things that are spatially or temporally related to it. No use of a modal notion has been made in this analysis.

### Activity 3.7

Could there be a single world with two discrete parts, where things in the one part are not spatially or temporally related to things in the other? Lewis (1986) has further discussion.

# Conditionals

Edgington, D. 'Conditionals', *The Stanford Encyclopedia of Philosophy* (Winter 2008 edition), <http://plato.stanford.edu/archives/win2008/entries/conditionals/>.

## 4.1 'if' and '→'

In learning classical logic, one is told to formalise English conditional sentences (like 'if London is not chosen for the Olympics, Paris will be') using '→'. Following this precept, the logical form of an English conditional is given by the formula  $p \to q$ , whose truth conditions are precisely defined (see Chapter 1.4): 'p → q' is assigned T iff either q is assigned T or p is assigned  $\perp$ . But there seem to be a number of differences between the behaviour of English conditionals and the behaviour of '→' formulae:

1. If 'p' is assigned  $\perp$ , then 'p → q' is assigned T (no matter what 'q' is assigned). But some English conditionals with false antecedents strike us as false, for example 'If ice is denser than water, then ice floats on water'.
2. If 'q' is assigned T, then 'p → q' is assigned T (no matter what 'p' is assigned). But some English conditionals with true consequents strike us as false, for example 'If ice is as dense as lead, then ice floats on water'.
3. The following argument is classically valid:  
    $p \to q$ ; so ( $p$  &  $r$ ) →  $q$  (whatever  $r$  may be).  
   Some corresponding arguments in English appear not to be valid, for example:  
   'If I put sugar in this cup of tea, it will taste fine; so if I put sugar in this cup of tea and also put in diesel oil, it will taste fine.'
4. 'If ... then' seems to require some kind of connection between antecedent and consequent, for example a causal connection. No such requirement holds for '→'.
5. There are conditionals that cannot be formalised by '→', since their components are not self-standing propositions, for example:
   1. If someone is in debt, she should curb her expenditure.
   2. If Oswald hadn't shot Kennedy, someone other than Oswald would have.

The last point deserves further comment. Models for the classical language treat sentences letters ( $p$ ,  $q$ ,  $r$  ...) as capable of receiving a truth value as their interpretation, the value true, T, or false,  $\perp$ . There are no restrictions: the assignments are entirely independent. In 5(a), 'she should curb her expenditure' is not capable of being assigned a truth value. It would be so capable if 'she'

referred to a specific person. But as used here, it does not. It is dependent upon the 'someone' in the antecedent. In 5(b), 'Someone other than Oswald would have [shot Kennedy]' cannot be assigned a truth value, since it is in the subjunctive mood.

Despite these problematic cases, there are arguments for the equivalence of 'if' and '→'. Most people think that if there is a divergence, it is because 'if' is stronger than '→', in the sense that it takes more for an English 'if' conditional to be true than for the corresponding '→' formula to be true. In short:

**Any sentence of the form 'if A then B' entails the corresponding sentence 'A → B'.**

*'A → B' is technically not a formula of the language of classical logic, but comes from, e.g. 'p → q' by replacing the sentence letters by English sentences A and B.*

To challenge this principle, one would need to find a true conditional in English with a true antecedent and a false consequent, which is hard to do. If we could also establish

**Any sentence of the form 'A → B' entails the corresponding sentence 'if A then B'**

we would have established the equivalence of the idioms 'if' and '→'. Here is an argument for the second, more problematic, principle.

The following argument seems to be valid (see Stalnaker, 1975):

Either the butler did it or the gardener did it.  
Therefore if the gardener didn't do it, the butler did.

The premise would seem to be equivalent to '(the butler did it) v (the gardener did it)' and so to '(the gardener didn't do it) → (the butler did it)'.<sup>2</sup> But in that case, the '→' sentence entails the corresponding 'if' sentence, which is an instance of what we wished to prove. If we can count on this result holding generally, we have established the necessary equivalence.

<sup>2</sup>This is a feature of the formal properties of 'v' and '→', and can easily be established by a truth table.

### Activity 4.1

Can you think of an example of an English argument where the relevant equivalences seem more doubtful?

Attempts to reinstate the view that English 'if' can be formalised by '→' typically rely on a distinction between

what is strictly said by the utterance of a sentence and what is thereby implicated (the distinction goes back to Grice, 1975). If, when asked to write a reference for a philosophy student to go to graduate school, I write: 'She is very appealing, well mannered and has great keyboard skills' and nothing else, I 'implicate' that she is not a suitable candidate for graduate school, even though I don't explicitly say anything of the sort (I 'damn by faint praise'). Perhaps the differences between 'if' and '→' arise only as differences in implicature, rather than any differences in truth conditions. Applying the idea to one of the purported differences between 'if' and '→': maybe 'If ice is denser than water, then ice floats on water' is strictly speaking true (it could be refuted only by finding some ice that is denser than water but which doesn't float, and we are never going to be able to do that!). We wrongly take it to be false because we take it to implicate that things that are denser than water float, and this generalisation is certainly false. Not many philosophers find this kind of defence appealing, but you need to evaluate it for yourself (Grice, 1975; Sainsbury, 2001, section 2.7; Jackson, 1979).

## 4.2 Conditionals and probabilities

When we consider sentences with a concern for whether or not to believe them, we may evaluate them as true or false. We should believe the true ones, and avoid the false ones. We can also evaluate sentences from essentially the same perspective, but in a different way: according to how **likely** we think they are to be true or to be false. In short, we often engage in an assessment of the probability or likelihood of a sentence.

We believe we are very unlikely to win the lottery. We can combine this belief with also thinking that the following is very unlikely:

1. If we win the lottery, we will not pay off the mortgage. Of course we'll pay it off if we win – though winning is very unlikely. This presents a further reason for denying the equivalence of 'if' and '→'. Given that we're almost certain that the antecedent of (1) is false, if 'if' meant '→' we should be almost certain that (1) is true. But it's just the reverse: we're confident that (1) is false.

### Activity 4.2

Explain this reasoning in more detail.

A natural way to estimate the likelihood of a conditional is to suppose the antecedent, and then consider how likely the consequent is under that supposition. This gives the right result at least in some cases. For example, the likelihood of 'if I roll an even number, it will be a six' is 1/3. Suppose I roll an even number. Then I roll a 2, a 4, or a 6. So rolling a six has a probability of 1/3, under the supposition; and this seems the right probability to assign to the conditional as a whole. Likewise, (1) is unlikely because,

supposing we win the lottery, it's highly likely that we would immediately pay off the mortgage.

Put more formally, the idea is that the probability of a conditional is the probability of the consequent, conditional upon the antecedent. Abbreviating 'the probability of sentence s' as 'Pr(s)', and abbreviating 'the probability of B, conditional on A' as 'Pr(B|A)', the suggestion can be written:

2.  $Pr(\text{if } A \text{ then } B) = Pr(B|A)$ .

This hypothesis seems plausible (it traces back to Adams, 1970), but it has a surprising consequence: conditionals are not capable of being true or false, simpliciter. As it is sometimes put, they are not genuine propositions. This was established by a rather technical proof by Lewis (1976, see also 1986), sometimes referred to as 'the bombshell'. A more informal argument for the same conclusion is given by Edgington (1995). (I won't give either of these arguments here, but those taking this aspect of conditionals seriously will need to read at least Edgington's version.)

Suppose we agree with Lewis and Edgington that, if (2) is correct, there are no conditional propositions. These authors both conclude that conditionals are not propositions: we'll call them 'non-propositionalists'. But we might go the other way, and conclude that (2) is incorrect. The view that there are no conditional propositions faces difficulties. One is that the view must treat asserting a conditional sentence as making a conditional assertion of its consequent. Another is that we appear to be able to embed conditional sentences in the kinds of context that call for propositions. I'll amplify these problems.

For a non-propositionalist, asserting a conditional, for example asserting 'if Mary is in Italy, then she is in Rome', is making a **conditional assertion**. It is not asserting the proposition that if Mary is in Italy, then she is in Rome, for there is no such proposition. Rather, it is like a conditional bet. The bet 'If Mary's in Italy, I'll bet you \$100 she's in Rome' only comes into effect if Mary's in Italy. If she isn't, no one wins and no one loses – there is no bet. Likewise the non-propositionalist will say that if Mary isn't in Italy, there's no assertion. Denial would likewise be conditional, best expressed as: 'No! If Mary's in Italy, she's not in Rome.' One problem with this picture is that, intuitively, there is another form of denial, in which we just negate the conditional without conditionally denying the consequent. Suppose I merely believe there's no reason to think that Mary, if in Italy, would be in Rome. Then I can say, 'No! I don't think that if Mary's in Italy she's in Rome', without making the stronger commitment to her being somewhere other than Rome, if in Italy. The conditional assertion account of asserting conditional sentences does not seem to square with our practice.

The other problem for non-propositionalism is that of **embedding**. Sentences like the following seem perfectly natural:

3. If John is someone who backs down if challenged, your best strategy is to challenge him.

One could think of this as having the structure 'if (if p then q) then r', so a conditional is the antecedent of the overall conditional. Even if, as non-propositionalists say, conditionals are not propositions, their antecedents and consequents are meant to be propositions. In particular, the antecedent is meant to be something we can suppose, in order to determine the probability of the consequent under that supposition. Once again, non-propositionalism threatens to conflict with our ordinary practice. So there is a case for jumping in the opposite direction to Lewis and Edgington, and denying (2). In that case, one has to face from scratch the task of explaining how the probability of conditionals is to be assessed.

### 4.3 Subjunctive and counterfactual conditionals

A subjunctive conditional is one expressed using the subjunctive mood, for example:

1. If Oswald hadn't shot Kennedy, someone else would have done.

We imagine one who asserts (1) to suppose, and to expect her audience to suppose, that the antecedent is false: it is common knowledge that Oswald in fact did shoot Kennedy, and one would expect an assertion of (1) to be the promulgation of a conspiracy theory. That's why subjunctive conditionals are sometimes called 'counterfactuals': their antecedents often describe situations that run counter to the facts, and are known to do so. But this is a misnomer, since we can perfectly well use a subjunctive conditional when we are agnostic about whether the antecedent is true, or even think it is probably true. For example, even if we think it likely that the Ascam Banking Corporation will default, we can properly assert and believe:

2. If Ascam were to default, I would lose all my money.

This assertion is subjunctive, but not counterfactual. The following could well be counterfactual, in the sense that the speaker believes, and expects her audience to believe, that the antecedent is false, but it is not subjunctive:

3. If Ascam stays afloat, I will be happy.

Some seemingly indicative sentences are probably best classified as subjunctive (and in some languages the antecedent would be expressed in a tense called 'conditional'). For example, it is hard to tell much difference between (2) and

4. If Ascam defaults, I'll lose all my money.

We could justify classifying (4) as subjunctive in virtue of its equivalence to the manifestly subjunctive (2).

There are cases in which indicative and subjunctive conditionals clearly differ. For example, one might think (1) is false (there was no conspiracy), even if one thinks a corresponding indicative conditional is true:

5. If Oswald didn't shoot Kennedy, someone else did.

That Kennedy was shot seems enough for the truth of (5), but not for the truth of (1). This suggests that we need a different account for subjunctive conditionals from whatever account we give of indicative conditionals.

The most famous account of subjunctive conditionals is one given by Lewis (1973), and it's roughly this (you'll need to check his paper for a fully accurate presentation, and he uses 'counterfactual' where I use 'subjunctive'):

which A is true, some world at which B is true  
is more similar to the actual world than any  
world at which B is not true. If it had been the  
case that A, it would have been the case that  
B' (abbreviated 'A $o$ B') is true iff among all  
the possible worlds at

We'll apply this idea to a famous example from Lewis:

6. If kangaroos had no tails, they would fall over.

According to Lewis's account, to see if this is true we must consider all the possible situations in which kangaroos have no tails. No doubt, in some of these, kangaroos don't fall over: good natured animal lovers fashion crutch-like supports and train the kangaroos to use them, so they don't fall. But very likely there are also worlds in which the animal lovers don't come to the rescue, and in which kangaroos fall. These worlds are more like our actual world (for kangaroos actually get no crutch-like supports). If the point generalises, we can conclude that, considering just worlds in which kangaroos lack tails, there's a world at which they fall that's more similar to the actual world than any world at which they don't. If that's right, then (2), treated as Lewis recommends, is true.

Lewis admits that the notion of similarity between worlds that is crucial to his account is 'extremely vague'. The discussion of the previous paragraph can be used to illustrate this. I said that a world in which kangaroos lack tails and in which no animal lovers help out is more similar to the actual world than one in which kangaroos lack tails and animal lovers supply kangaroo-crutches. The basis for this was simply that in the actual world, there are no kangaroo-crutches. But in the actual world, there are plenty of animal lovers, who would no doubt come to the rescue if kangaroos were struck by an illness that caused them to lose their tails. They would have fund raisers and websites, they would get experts in prosthetic technology to supply their services *pro bono*, and would equip the kangaroos with fall-preventing devices. So isn't a world in which all this happens more similar to the actual world than one in which it does not?

Lewis thinks that subjunctive conditionals are vague and various, and so vagueness and variability in the similarity relation is just what's needed. I expected you to take (6) to be true. But when you think about animal lovers, you may have felt inclined to change your mind. The possible different reactions to the question whether (6) is true seem to be nicely matched by the different reactions one might have to whether a kangaroo-crutch world or a kangaroo-crutchless world would be more similar to actuality.

Lewis himself gives a famous example of the way in which subjunctive conditionals can be hard to evaluate. Which of the following should we prefer?

1. If Verdi and Bizet had been compatriots, Verdi would have been French.
2. If Verdi and Bizet had been compatriots, Bizet would have been Italian.

### Activity 4.3

Should we say both are true? Both are false? Or could we use these as an example of the failure of Bivalence?

According to Lewis, we can properly be guided in our spelling out of the similarity relation by our intuitions about subjunctive conditionals. He explicitly denies that we have independent access to a conception of similarity that would do the work for us. (He compiles (1979) a list of priorities that help fix similarity.) Even so, there are problems. Suppose, during the Cold War, that a world leader, say Richard Nixon, had pressed the button to launch a nuclear attack against the USSR. The following is intuitively true:

1. If Nixon had pressed the button, things would have been radically different.

But worlds most similar to ours in which he pressed the button are those in which there is a misfire, so that instead of nuclear catastrophe things go on more or less as before. Evidently Lewis's account needs at least some touching up, and if you read his papers on this you will find some ideas for how to do this.

The main theories to consider are: English 'if' means the same as '→', and the seeming differences are to be explained in terms of pragmatic effects (first proposed by Grice, 1961, and discussed by Sainsbury, 2001, pp.87–105); probabilistic theories (going back to Adams, 1970, and a version of it championed by Edgington, 1995); and possible worlds theories (stemming from Lewis, 1976 and Stalnaker, 1975). These are reviewed in Sainsbury, 2001, Chapter 3.

# Reference – names and descriptions

## Introduction

For more than 100 years, the goal of understanding the logic of ordinary language has been shaped by the idea that the best way to begin is to compare it with the language of classical logic. The basic formulae of this language are formed from individual constants or variables together with predicates: Fa, Rxy and so on. Do these give the logical form of English sentences like, respectively 'John dances', 'Sally loves Peter'?

The question raises two issues. One that has been less salient is how the predicate letters relate to English 'predicates'. One immediate difference is that predicate letters come first in classical formulae, whereas predicates in English sentences rarely do.<sup>1</sup> More significantly, the category of 'predicate' emerges as one that contains fairly disparate kinds of expressions. There are intransitive verbs, like 'dances'; transitive verb phrases, like 'loves' and 'thinks about'; indefinite noun phrases preceded by the copula, like 'is a doctor'; adjectives preceded by the copula, like 'is happy'. A study of English uninfluenced by classical logic might wish to draw distinctions. It might also wish to say something about the copula, to which no single expression corresponds in classical logic. And it would take note of many expressions that seem to have nothing similar in classical logic: adverbs, like 'quickly' or 'probably'; intensifiers and hedges, like 'very' and 'somewhat'; verbs like 'believes' that seem rather unlike 'loves'; and so on. The list is long.

*'They come first in such sentences as: 'Happy is the man who spends less than he earns.'*

The lion's share of philosophical attention, however, has fallen on the other issue: what expressions in ordinary language correspond to individual constants and variables? Variables are standardly likened to pronouns in so called 'bound' occurrences. Thus the 'he' in

**If anyone has money, he buys real estate**

is held to correspond to the 'x' in a formula like

 $orall x (Mx 
ightarrow Rx)$ 

(where 'M' abbreviates 'has money' and 'R' abbreviates 'buys real estate'). There are plenty of problematic issues, including how we should deal with *'donkey sentences'*. But in this section we'll focus on issues relating to individual constants. Can they properly be matched with proper names, like 'Napoleon'? How should we handle expressions which seem to play a similar role, like 'The first emperor of

the French'? The latter are called definite descriptions, and we'll start by discussing a famous theory concerning their logical form.

## 5.1 Russell's theory of descriptions

### Readings

Neale, S. *Descriptions*. (Cambridge, Mass.; London: MIT Press, 1990) [ISBN 0262640317].

Russell, B. 'On denoting', *Mind* 14 (1905), pp.479–93.  
Russell, B. *Introduction to Mathematical Philosophy*. London, George Allen and Unwin, 1919) Chapter 16.

Russell (1905) famously raised a puzzle about the sentence:

#### 1. The present King of France is bald.

'If we enumerated the things that are bald, and then the things that are not bald, we should not find the present King of France in either list' (Russell, 1905, p.485). Russell thinks that (1) is 'plainly false'; yet that this is hard to account for. In particular, we can't account for it if we think that 'The present King of France' is a **referring expression** (he does not use this phrase), which is an expression whose meaning consists in its referring to something. For then an expression like 'The present King of France', which refers to nothing, would have no meaning.

To put essentially the same point another way, if 'The present King of France' were a referring expression, referring to some object O, (1) would be true just if O is bald, and false just if O is not bald. For (1) to be false, O would need to be on the list of things that are not bald. The King of France is not on this list. So that's not how (1) is false. Another explanation is needed.

Russell (1905) adopts an interesting procedure in this paper. He starts by simply setting out, without argument, his theory of descriptions, his theory of how expressions of the form 'the so-and-so' and 'a so-and-so' work. He makes some rather cryptic criticisms of alternative theories, and then seeks to justify his account in terms of its capacity to solve puzzles, which, in philosophy, 'serve much the same purpose as is served by experiments in physical science' (Russell, 1905, p.485). 'I'll follow his method, and simply state the theory to start with, and then turn to the puzzles he says it solves. Although he says he is going to discuss both indefinite descriptions (phrases of the form 'a so-and-so') and definite descriptions (phrases of the form 'the so-and-so'), the former receive very little attention in the article (and were largely neglected until the 1980s).

Russell's theory of definite descriptions:

1. A sentence of the form 'The F is G' is true iff exactly one thing is F and that thing is G. In the language of classical logic:  $\exists x(Fx \land \forall y(Fy \to x=y) \land Gy)$ .
2. A sentence of the form 'The F exists' is true iff exactly one thing is F. In the language of classical logic:  $\exists x(Fx \land \forall y(Fy \to x=y))$ .

Russell thought that an important feature of his approach was that he did not attempt to define the word 'the' on its own. Rather, he tells one how to account for the truth conditions of sentences containing definite descriptions (phrases formed using 'the'). The approach has become known as 'contextual definition'.

According to part (a) of the definition, 'The present King of France is bald' is true iff exactly one thing is King of France at present and that thing is bald. Since nothing is King of France at present, the sentence in question is false.

This connects with one of Russell's three puzzles (the second, in his ordering). Russell says that a proper theory of descriptions must be consistent with the law of excluded middle, which he characterises as follows:

either 'A is B' or 'A is not B' must be true (1905, p.485)

The problem is that it initially seems that neither 'The present King of France is bald' nor 'the present King of France is not bald' is true. In addressing this issue, Russell delivers one of his major innovations, which transformed a great deal of thinking: he argues that the problem can be resolved if we are properly sensitive to distinctions of logical **scope**.

The theory of descriptions could be applied in either of two ways to 'The present King of France is not bald':

1. Exactly one thing is King of France at present and that thing is not bald.
2. It is not the case that: exactly one thing is King of France at present and that thing is bald.

In (2), the sign for negation ('not') is said to have narrow scope, governing just 'bald'. In Russell's terminology, (2) treats the definite description in (1) as having 'primary occurrence', that is, as not being in the scope of any operator. In (3), the sign for negation ('It is not the case that') is said to have wide scope: it scopes over the whole sentence. In Russell's terminology, (3) treats the definite description as having 'secondary occurrence', that is, as occurring within the scope of a negation operator. (3) is true, and is what should be involved in a proper statement of the law of excluded middle. (It would be clearer to write the law as: either 'A is B' is true or 'It is not the case that A is B' is true.) Thus understood, there is no conflict with the law. (2) is indeed false, just like (1), for it claims that something is King of France, but this fact does not conflict with any law of logic: (2) is not the negation of anything.

This is a brilliantly neat solution, and the distinction of scope on which it depends has become a major tool in philosophical logic.<sup>2</sup>

<sup>2</sup> Russell (1905) uses *scope distinctions to bring out an amusing ambiguity in: 'I thought your yacht was longer than it is'. Check it out.*

Another of Russell's three puzzles (the first in his ordering) concerns the 'Law of Identity', which he describes thus:

If *a* is identical with *b*, whatever is true of the one is true of the other, and either may be substituted for the other in any proposition without altering the truth or falsehood of that proposition (1905, p.485).

This Law seems to conflict with the fact that whereas George IV wished to know whether Scott was the author of *Waverley* (and Scott was indeed the author of *Waverley*), he did not wish to know whether Scott was Scott, for he knew that already. We could set out the problem more fully as follows:

1. George IV wished to know whether Scott was the author of *Waverley*.
2. Scott was the author of *Waverley*.
3. So, according to the Law, we can replace 'the author of *Waverley*' by 'Scott' in (i) to yield

<sup>3</sup> This substitution of linguistic expressions may not be what Russell had in mind. More likely he was thinking of objects rather than expressions. This leads to deep questions about Russell's philosophy. See Proops (2011).

iv. George IV wished to know whether Scott was Scott.

The steps in the inference appear legitimate, yet we have moved from a truth to a falsehood, so appearances must be deceptive.

It is not entirely clear how Russell thought his theory of descriptions solved this puzzle. Here's something that's suggested by some (but not all) of his remarks (see especially the discussion on p.489): the definite description in (i) has narrow scope relative to the operator 'George IV wished to know whether'. In Russell's terminology, it's a 'secondary occurrence'. In such contexts, the law of identity does not apply. The law should be qualified to permit substitution only for primary occurrences. As we'll see in the next section, it seems to be a pervasive feature of ascriptions of thoughts that we cannot replace names or definite descriptions by co-referring ones, without risking changing truth into falsehood. For example, Cicero was Tully, but if one did not know this, one might believe that Cicero was an orator without believing that Tully was.

Russell's third puzzle relates to existence, drawing on part (b) of his theory, which we'll discuss in section 3 of this chapter.

According to Russell's theory of descriptions, a definite description is really a kind of quantifier phrase. 'The King' should be grouped with 'Some King' and 'All Kings', rather

than with 'George IV' or 'Napoleon'. (So one could think of 'the' as a kind of derived logical constant.) We shouldn't say that the job of a definite description is to pick out an object, but rather that its job is to specify a condition satisfied by just one thing. The contrast is somewhat similar to a contrast between two kinds of thoughts. I might believe on entirely general grounds that the tallest spy is a spy. Intuitively, I am not thereby thinking about any specific person. On the other hand, if I think that John is a spy, I do have a specific person 'in mind'. Russell probably thought his theory of descriptions, considered as a theory about language, matched this distinction in kinds of thoughts (see Russell, 1912, Chapter 5).

Russell's theory of descriptions has been subjected to endless debate and criticism. Here are three main lines of attack (for more discussion, see Neale, 1992):

**Failure of uniqueness:** Many definite descriptions of the form 'The F' are used in situations in which it is plain to speaker and hearer that there is more than one F, yet the speaker's remark is treated as true. For example, when parents say things like 'The baby is crying' they don't take themselves to imply that there is only one baby in the world. Even if there are many books on many tables in my vicinity, I may be able to use a sentence like, 'The book is on the table' to say something that, intuitively, counts as true. This is at odds with Russell's theory, which implies that the sentences are true only if there is exactly one baby or exactly one book. It's generally agreed that Russell's theory needs at least some amplification at this point, in order to do justice to the impact of context on the use of definite descriptions.

### Activity 5.1

Elaborate the view that context supplies an amplification of the description, so that it becomes unique. For example, 'The book' is amplified by context to something like 'the book we have been discussing'. Can a development of this kind save Russell's theory of descriptions?

**The empty case:** If there is no F, 'The F is G' is false, according to Russell's theory. In some cases we might prefer to say that the question of truth or falsehood does not arise (Strawson, 1950). Suppose you are innocent of theft, and someone asks where the money is that you stole. You can't give a straightforward answer. You need to say something like, 'Since I am no thief, the question you ask does not arise'. Similarly, if the accuser says, 'The money you stole was less than \$100', it would not be good to reply, 'No, it wasn't: what you've said is false'. That would suggest you stole more than \$100. You have to explain that the accuser's claim has a false presupposition. In some empty cases, we even have an inclination to say that the sentence is true, for example: 'The best-selling book in 2012 sold more than 10,000 copies' might count as true, even if there is strictly no single best-selling book, since

several books sold the same number of copies.<sup>4</sup>

<sup>4</sup> *There are hard-to-explain differences among empty cases. Many people are inclined to sympathise with Strawson's claim that, 'The present King of France is bald' is neither true nor false. Yet most people would count the following as clearly false: 'Yesterday, I met the present King of France.'*

**Referential versus attributive:** A speaker can use a definite description while intending it to apply to something which does not satisfy it. In some cases, no problems ensue, and we may intuitively count what he says as true. Russell's theory takes no account of this. A famous example, going back to Donnellan (1966), is of a person at a party who points at another guest, whom she takes to be drinking a martini but who is in fact drinking water out of a martini glass, and says, 'The man drinking a martini is drunk'. If the person the speaker has in mind in uttering these words is indeed drunk, we are inclined to count what she said as true. We need make no enquiry about how many martini drinkers there are in the world, or even in the room. This does not harmonise with Russell's analysis, according to which truth requires that there be exactly one martini drinker, and that that person be drunk. Donnellan calls this a 'referential use' of a description, contrasting it with what he calls 'attributive uses', as in the example of 'The tallest spy is a spy'.

Most people think that there is something important in the distinction between referential and attributive uses. The more disputed question is the extent to which the phenomenon is inconsistent with Russell's theory. Russell himself paid rather scant attention to how English is used in practice. It's at least arguable that his theory can stand, provided that it is supplemented with a suitable account of the way in which speakers' intentions interlock with the semantic facts (see Kripke, 1977).

## 5.2 Proper names: Millian versus descriptive theories

John Stuart Mill said that proper names 'denote the individuals who are called by them; but they do not indicate or imply any attributes as belonging to those individuals' (1843, p.34). The contrasting view is that proper names function more like definite descriptions: a name like 'Napoleon' is really a 'truncated or telescoped description' (Russell, 1912, Chapter 5), perhaps 'the first Emperor of the French' or 'the general defeated at Waterloo'. If this view is right, proper names, contrary to Mill's opinion, certainly do imply attributes of their bearers.

The debate between Millian theorists of names and descriptive theorists of names has rumbled on for more than a century. It's often assumed that these two theories exhaust the options, so that arguments against one view are thereby arguments for the other. This presupposition is, happily, starting to be undermined, so that in recent years some promising intermediate positions have started

to emerge (e.g. Sainsbury, 2005). Here I will just sketch the standard dialectic.

Mill appealed to two semantic properties: denotation and connotation. Some words, for example 'white', have both properties: 'white' connotes the attribute whiteness, and this attribute determines what it denotes: all and only possessors of the attribute, that is, all and only white things. Proper names, by contrast, have denotation but no connotation: they don't introduce any denotation-fixing attribute.

It might seem there are exceptions: is not 'Dartmouth' so-called thanks to lying at the mouth of the river Dart? So is not the attribute of being thus located a semantic property of the name 'Dartmouth', one that fixes its denotation, and so a connotation? No, Mill replies:

If sand should choke up the mouth of the river, or an earthquake change its course, and remove it to a distance from the town, the name of the town would not necessarily be changed... Proper names are attached to the objects themselves, and are not dependent on the continuance of any attribute of the object.

(Mill, 1843, p.34).

The upshot is a very simple picture: proper names just name their bearers. In this respect they are indeed like individual constants in classical logic, which are simply assigned an object from the domain.

The simple view confronts at least two problems: identity sentences and empty names (names with no bearer). Given Mill's resources, he cannot make any distinction between the following:

1. Hesperus is Hesperus
2. Hesperus is Phosphorus.<sup>5</sup>

<sup>5</sup> 'Hesperus' is a name given to Venus, based on its appearances in the evening. 'Phosphorus' is a name given to the same heavenly body (at one time thought to be a star but now known to be a planet) on the basis of its appearances in the morning (and at a different time of year). It was a significant astronomical discovery that they are one and the same.

Yet (1) seems trivial, whereas (2) reports a significant empirical discovery. For Mill, 'Hesperus' and 'Phosphorus' have all and only the same semantic properties: both refer to Venus. In Mill's theory, there's no semantic difference between (1) and (2). That's the problem of identity.

The problem of empty names is that we happily use names with no bearer, like 'Pegasus' and 'Eldorado'. And we use names, like 'Homer' and 'Atlantis', about which there is dispute as to whether or not they have a bearer. According to Mill's view, a name with no bearer is a name with no semantic properties at all (no connotation, no denotation): there is nothing to distinguish it from a mere scribble or grunt. But, intuitively, empty names can make perfectly

good contributions to the meaning of a sentence and can be essentially involved in truths (e.g. 'The children are excited tonight they're expecting Santa Claus').

Frege (1892), in one of the most important and most cited articles in this area, starts out with a question about how we should distinguish sentences like (1) from those like (2). He suggests that proper names need to be accorded *sense* (Sinn) as well as reference (Bedeutung). The distinction resembles Mill's distinction between connotation and denotation. The sense of a name is the 'mode of presentation' of its reference. Although 'Hesperus' and 'Phosphorus' have the same reference, they differ in sense, one presenting Venus as (say) the evening star, the other presenting it as (say) the morning star. This explains how the sentences can differ in some important way, even though they agree point-by-point in reference.

Moreover, Frege thought that an expression could have sense without reference. He gives the example of 'Odysseus'. Such an expression can make a meaningful contribution to a sentence or thought, despite its lack of reference. Something like Frege's view was also adopted by Russell, at least for the proper names we ordinarily use. (Russell thought there were also names in a 'logically proper' sense, and these, he claimed, are essentially Millian.) A good place to look for his version is his *Problems of Philosophy* (Russell, 1912, Chapter 5).

An attraction of the descriptivist views of Frege and Russell is that they offer solutions to the problems Mill's view encounters. But they, in turn, have been attacked, notably in Kripke's brilliant book *Naming and Necessity*, first given as lectures at Princeton in 1970, and published in book form in 1980. I strongly recommend it. The lectures were given without notes, so the tone is informal and relaxed, and although deep issues are discussed, it's engaging to read and doesn't seem at all heavy or stuffy.

Kripke assumes that, in the Frege–Russell view, a sense or mode of presentation is (or can be expressed by) a definite description.<sup>6</sup> In a series of fun examples, he points out that

<sup>6</sup> Not everyone agrees with this interpretation of Frege: see, for example, Dummett (1973). The interpretation of Russell is also less than fully straightforward: see Sainsbury, 1993.

1. Names and descriptions may differ in modal profile.
2. Commonly associated descriptions may fail to fix a name's reference.
3. There may be no description shared by a community of users of a given name.

I'll quickly review these claims – but I think you should read Kripke himself.

1. Kripke argued that proper names are 'rigid designators': they designate the same thing with respect to every possible world. If we consider whether 'Aristotle was

fond of dogs' is true with respect to some non-actual situation, our question concerns our very own actual Aristotle. But many definite descriptions are non-rigid. For example, 'The last great philosopher of antiquity' refers to Aristotle at our world. But consider a world in which Aristotle had suffered an unfortunate accident as a child and never grew up to become a philosopher (or anything else). At that world, the definite description would have designated Plato. At that world, the question whether 'The last great philosopher was fond of dogs' is true is to be answered in terms of Plato's canine sensibilities, not Aristotle's.

The standard response on behalf of Frege, or more generally descriptive theories of names, is that the relevant descriptions need to be rigid ones, for example 'The **actual** last great philosopher of antiquity'. In this context, 'actual' is to be understood as an expression which ensures that, even with respect to a world in which Aristotle died young and was not a philosopher, the **actual** last great philosopher was nonetheless Aristotle – the person who, in our actual world, was the last great philosopher of antiquity. For further debate, see Soames (1998).

1. Many of us associate the name 'Gödel' with the definite description 'the person who first proved the incompleteness of arithmetic.' Kripke invites us to imagine a situation in which someone else, Schmidt, was the first prover: he died under mysterious circumstances and his papers were never found. The proof was published under Gödel's name, but was really Schmidt's. In this situation, the reference of the name diverges from that of the most commonly associated definite description.

<sup>7</sup> Gödel was a professor at Princeton when Kripke's lectures were delivered there.

1. Though we typically associate information with names, the information does not always add up to a **definite** description. Kripke gives the example of someone who, intuitively, uses the name 'Feynman' correctly, but whose associated information is fairly sparse, and applies to more than one person: 'a famous physicist'. If this is right, then one can use a name correctly without knowing any definite description; a description theorist would need to consider whether there is a worthwhile descriptivist thesis that can accommodate this.

Another aspect of this problem is that even when speakers associate definite descriptions with a name, speakers who intuitively use a name in the same way may associate it with different descriptions. Descriptive theorists usually focus on names of famous dead people, which helps make us think we all share definite descriptions. But even in those cases it seems clear that successful users of

the name may fail to share. Gödel's mother might have used his name as others do, while having no disposition at all to associate with it the intellectual definite descriptions salient to his fellow academics.

### Activity 5.2

Russell (1912, Chapter 5) considers a recipe for generating descriptions from names, exemplified by: the description associated with 'Julius Caesar' is 'the person called "Julius Caesar"'. Consider which (if any) of the standard objections to description theories this suggestion could block.

## 5.3 Existence and ontology

How do we account for the truth of singular negative existential sentences like:

1. The greatest prime number does not exist

1. Vulcan does not exist.

Of what do we say it does not exist? If we say this of nothing, then there seems to be something incomplete about what we say. But if we say it of something, it seems that what we say is false, for the something of which we speak presumably does exist.

One solution to this problem, sometimes called Meinongian,<sup>8</sup> is to allow that there are things that do not exist. Then we gaily take the second horn of the dilemma above: (1) and (2) refer to non-existent things, the greatest prime, Vulcan, and truly say that they do not exist.

<sup>8</sup> In deference to Alexius Meinong, although his work calls for careful interpretation.

Straightforward and logically elegant as this solution is, it has not received endorsement from the majority. Philosophers regard it as inconsistent with 'ontological parsimony', the 'taste for desert landscapes', in which we do not assume things we do not have to. Referring to Meinong, Russell put the point vividly:

In such theories [as Meinong's], it seems to me, there is a failure of that feeling for reality which ought to be preserved even in the most abstract studies. Logic, I should maintain, must no more admit a unicorn than zoology can; for logic is concerned with the real world just as truly as zoology, though with its more abstract and general features.

(1919, p.169)

Logicians should temper their strictly logical views by a 'feeling for reality'. So logic makes contact with metaphysics and ontology.

Russell (and others) have suggested we can resolve our problems with (1) and (2) without accepting that there

are non-existent things. Part (b) of Russell's theory of descriptions tells us that the proper analysis of (1) treats it as:

3. It is not the case that there is exactly one greatest prime number. [In the language of classical logic:  $\neg(\exists x)(Px) \& \forall y(Py \to x=y))$ , where 'P' stands for 'is a greatest prime number']

This does not look as if it refers to anything non-existent. It merely denies that there is anything meeting a certain condition (being a unique greatest prime).

Russell's solution to (2) comes in two stages. First he applies his descriptivist view of proper names to 'Vulcan', perhaps replacing it with 'The planet responsible for the perturbations in the orbit of Mercury'; (2) can then be treated just like (1):

4. It is not the case that there is exactly one planet responsible for the perturbations in the orbit of Mercury.

That's all very well for those who accept descriptivist theories of names, but what about those who do not? The best non-Meinongian attempt to deal with the problem is by Evans (1982, Chapter 10). The core idea is that we pretend that certain names have referents, and we exploit that pretence in making singular negative existential claims. The chapter is fairly accessible, and is really interesting – recommended even if you are not persuaded of the view of names it attempts to defend.

## 5.4 Reference and the *de re/de dicto* distinction

Russell distinguished knowledge by description from knowledge by acquaintance (1912, Chapter 5). We saw earlier that we could think about the tallest spy in one of two ways. In one, we think 'purely descriptively': we work out on general grounds that some spy must be taller than the others (we could do a little stipulation to determine what to do in case of a tie for height, perhaps using birthdays), and we think 'about him'. In another way of thinking of this spy, we are actually acquainted with him: he is our neighbour and we see him often on the street. Our thoughts appear to be 'about' the same person in both cases, but in very different ways (see Evans, 1982, p.64).

The distinction is sometimes put by saying that in the first case (no personal knowledge) we think about the spy '*de dicto*' (through words) whereas in the second we think about the spy '*de re*' (as the man himself). As many people have remarked, it's rather hard to clarify this distinction. However, there is one fairly clear application: to ways in which we attribute beliefs. For example, in the first case it would seem wrong to say:

1. Concerning the tallest spy, John believes he is a spy even though it's right to say

2. John believes that the tallest spy is a spy.

The ascription of belief in (1) is called *de re*, and in (2) *de dicto*. In these cases, scope provides an explanation. In (1), the specification of the object has wider scope than the description of the belief; in (2) it's the other way about.

This story fits with a *de re/de dicto* distinction in modal contexts. Contrast

3. Concerning the tallest spy, he's necessarily a spy  
4. Necessarily, the tallest spy is a spy.

Here (3) is false: no one is required to be a spy (not by logic, at any rate); (4) is arguably true: it's necessary that if you're the tallest spy, you're a spy. Again, a distinction of scope seems to offer an explanation. We'll return to the modal case in Chapter 8.

Before leaving the topic, it's worth stressing that although the scope distinctions we have noted are clear enough, the contrast in mental reality they are supposed to introduce is much less clear. The difficulty can be highlighted by considering this question: how does someone need to be related to the tallest spy if a *de re* ascription of belief (like (1), as contrasted with (2)) is to be justified?

### Activity 5.3

A well-known case to consider: suppose I introduce the name 'New' for the first child to be born in 2020. Can I think *de re* thoughts about this child, for example, that New will have no idea how special he or she is for at least the first year of life?

# Non-extensional language

## Reading

Forbes, G. 'Intensional Transitive Verbs', *The Stanford Encyclopedia of Philosophy* (Spring 2010 edition), Edward N. Zalta (ed.), <http://plato.stanford.edu/archives/spr2010/entries/intensional-trans-verbs/>.

Classical logic is 'extensional', in a technical sense I am about to explain, but on the face of it there is a great deal of non-extensionality in English. This raises problems for the project of using the language of classical logic to provide logical forms for English sentences.

When we claimed that one could believe that Cicero was an orator without believing that Tully was an orator, we were marking an aspect of 'non-extensionality' in English. If English were extensional, we should be able to exchange co-referring names without changing truth value.

A sentence is **extensional** with respect to a position for an expression (sentence, name or predicate) iff replacing an expression in that position with any other expression having the same extension leaves the truth value of the sentence unchanged.

To apply the definition, we need to know what the **extension** of an expression is. This is given by these stipulations:

- ► The extension of a sentence is its truth value, true or false.
- ► The extension of a predicate is the set of things of which it is true.
- ► The extension of a name is its bearer.

'Tully' and 'Cicero' are coextensive, since they have the same bearer, but this does not guarantee that 'John believes that Cicero is an orator' has the same extension as 'John believes that Tully is an orator': these sentences may differ in truth value. So the sentence 'John believes that Cicero is an orator' is non-extensional with respect to the position occupied by 'Cicero'.

Sentences dominated by 'Necessarily' are non-extensional with respect to the dominated sentence. For example 'Necessarily, 2 + 2 = 4' is true, '2 + 2 = 4' has the same truth value as 'France produces more wine than Canada', but 'Necessarily, France produces more wine than Canada' is false.

The language of classical logic is extensional. Interpretations assign extensions to expressions, and the extension of a formula, on an interpretation, depends only on the extensions assigned to its components.

The language of sentential (propositional) logic is 'truth functional': the truth value of a complex formula on an interpretation depends on nothing but what the interpretation assigns to the sentence letters. Truth functionality is thus extensionality with respect to the positions occupied by sentences.

What I have called non-extensionality is sometimes loosely called intensionality (or, sometimes, intentionality). I think that intensionality should be a positive property, like extensionality: it should be the property of invariance of truth value under substitution of co-intensive expressions. The intension of an expression is a function from every possible world to the expression's extension at that world. It follows that augmenting the language of classical logic with modal operators results in an intensional language. That's because the truth value of 'Necessarily, p' depends only on the intension of p: Any co-intensive sentence can be substituted without affecting truth value.

If we use 'intensional' in this positive way, we find that English contains sentences that are neither extensional nor intensional. Belief ascriptions are an example. We've already seen that these are not extensional. To show that they are also not intensional, consider that there is no sound inference from:

**John believes that 2 + 2 = 4**

to

**John believes that 7<sup>9</sup> = 40,353,607**

despite the fact that the embedded sentences are co-intensive, being both necessarily true, and so true at every possible world. Non-extensional and non-intensional contexts are sometimes called 'hyperintensional'. The idea behind the nomenclature is that an appropriate substitution-permitting condition will be something more fine-grained than intensions.

All this is rather dry stuff, and I've included it because you will often find discussions which exploit the terminology with no explanation. But the phenomenon of intensionality is really quite riveting philosophically, as I'll now try to persuade you.

Arguably, what makes something a mind is its capacity to direct thought on objects. In making such a claim, we need to include not only cases in which people direct their thought on London or on King George IV; we must also include cases in which they direct their minds on dragons or Santa Claus. The capacity to do this seems central to having anything like the kind of mental life we have. But there are no dragons, there is no Santa Claus, so

there is nothing for the mind to direct itself on. This seems problematic, especially so if we bring to bear the outlook generated by the language of classical logic, in which a sentence of the form 'Rab' can be true only if both 'a' and 'b' refer to something. There simply is no room, within the classical mindset, for a truth of this form corresponding to 'John thought about Santa Claus'.

### Activity 6.1

To appreciate some of the difficulties, ask yourself why we can infer that Sandra wants a sweater from the premise that she wants a red sweater, but cannot infer that she is afraid of dogs, from the premise that she is afraid of rabid dogs. Again, ask yourself why, if Sandra dreamed of many unicorns, it's right to say she dreamed of something – why isn't it 'some things' (to agree in number with 'unicorns')?

Hallucinations, dreams and stories are an essential part of our lives. But if Macbeth hallucinates a dagger, or Sandra dreams of a unicorn, or Conan Doyle makes up a story about Holmes, we have facts that look as if they are relational, but which we cannot think of as relational in the way that 'London is close to Oxford' is relational.

The difficulty would be mitigated (not resolved, I think – but that is another story) by adopting a Meinongian ontology. If there really are non-existent daggers, non-existent unicorns and non-existent detectives, hallucinating, dreaming and making up can be genuine relations after all, though relations to non-existents. But many philosophers cannot bring themselves to think there are such things, and so cast around for a different solution. There is no agreement even on where to turn.

The problematic verbs ('thinks about', 'hallucinates', 'fears' and so on) are sometimes called 'intensional transitive' verbs. They are 'transitive' in that they typically have two slots needing to be filled by a noun phrase. They are 'intensional' because the result can be true even if one of the noun phrases does not refer to anything.

Intensional transitives serve to report the most important features of our mental lives. Inconveniently, they contrast sharply with the language of classical logic, and suggest that we will need a very different language in which to express the logical forms of some of the sentences that matter most to us.

# Vagueness

## Readings

Keefe, R. *Theories of Vagueness*. (Cambridge: Cambridge University Press, 2000) [ISBN 0521650674].

Sainsbury, R. M. *Paradoxes*. (Cambridge; New York: Cambridge University Press, 2009)

third edition [ISBN 9780521720793] Chapter 3.

Vagueness raises important issues in philosophical logic, and throws some light on alternatives to classical logic.

If you take grains of sand away, one by one, from a heap of sand, eventually there will be no sand left. Before this point is reached, you will not have enough grains to qualify as a heap. Before that, you will be in doubt about whether the remaining grains make a heap. In deciding what to think, you could reasonably be moved by the following thought:

1. Taking away a single grain from a heap of sand (with minimal disturbance) cannot turn a heap into something that is not a heap.

But now there is a puzzle: if no one act of grain-removal can turn a heap into a non-heap, how can you possibly end up without a heap by repeating such acts? We can express the puzzle as a seemingly valid argument:

1. One thousand grains of sand make a heap.
2. If you take away just one grain from a heap, the result still makes a heap.
3. So just one grain makes a heap.

The premises seem true, the conclusion is false, so we have a paradox.<sup>1</sup>

*'A paradoxical argument is one which seems sound (that is, seems valid and seems to have true premises) but seems to have a false conclusion. Things cannot be as they seem in every respect, since the conclusion of a sound argument must be true.'*

The paradox arises from the vagueness of 'heap'. A mark of vagueness in a word is the existence of borderline cases, ones in which we do not know whether the word applies or not, where our ignorance seems irremediable. We're looking at some grains of sand in good light; there's no further information we could ask for to help us determine whether these grains count as a heap or not; yet we may remain unsure whether or not these grains form a heap.

This kind of paradox is called a 'sorites' paradox, after a Greek word meaning 'heap'. Many people find the colour spectrum a potent example of logically the same paradox. Imagine a long wall, painted red on the left, with the shade progressing very gradually towards orange, the colour on

the right side of the wall. A small viewer, with a vertical dividing line, is used to make two adjacent small areas of the wall visible. Wherever this is placed, it is impossible to detect any difference in colour between the region on the left and the region on the right of the viewer window. Two regions that look the same should be judged to have the same colour. But then, moving the viewer by increments, so that, after a move, the left area is just what was the right area in the previous position, we will end up judging a clearly orange area to be red. We could think of this version of the paradox in terms of an initial judgment to the effect that the leftmost area is red, followed by a series of conditionals: if the left area is red, so is the right. Classically valid inference cascades you to the manifestly incorrect conclusion that the rightmost area is red.

Vagueness raises some logical problems, and also shows how classical model theoretic semantics can be adapted. Among the classical logical and semantic principles that theorists have considered abandoning in response to vagueness are Bivalence (semantic), Law of Excluded Middle (logical) and Law of Non-contradiction (logical). I'll briefly review these options.

In various different ways, vagueness has prompted the denial of Bivalence (the principle that every truth-bearer has just one of two truth values). According to the most natural form of this denial, sentences in which a vague predicate like 'is a heap' is applied to a borderline case are neither true nor false, nor do they have any other truth value. You might begin to justify this by saying that when 'Is this a heap?' is asked of a borderline case, it cannot be correctly answered by either 'Yes' or 'No', and the lack of a truth value matches this fact.

### Activity 7.1

Can we not infer from 'It's not true that this is a heap' to 'This is not a heap'? If so, what should we conclude about the idea that 'This is a heap' is neither true nor false?

The denial of Bivalence can also take the form of saying that there are more than two truth values: three perhaps, with a third marking the borderline cases. Or non-denumerably many, if we adopt 'degree-of-truth theories', according to which sentences are associated not with the classical truth values, but with measures of how true the sentences are. Borderline sentences will receive intermediate values.

A final way of denying Bivalence is to say that borderline sentences are both true and false. An initial justification

might be our tendency to describe borderline cases by such a phrase as 'It is and it isn't'.

Those who deny Bivalence have to reconsider their logic. For example, those who hold that borderline sentences have a 'glut' of truth values, both true and false, need to adopt a paraconsistent logic, one in which Explosion fails. (Explosion is the principle that anything follows from a contradiction.)

### Activity 7.2

Why should this be so?

Those who opt for degrees of truth may wish to reconsider LEM (the Law of Excluded Middle). Suppose degrees of truth are represented by the real numbers between 0 and 1. An intermediate degree of truth would be 0.5. If a sentence  $p$  is true to degree 0.5, then you might well expect its negation to have the degree 1–0.5, and so also to have the value 0.5. Independent justification for this result might come from our similar reaction to both 'This is a heap' and 'This is not a heap', said of a borderline case. However, you also might expect the conjunction of two sentences intermediate in truth value to have an intermediate truth value. This would mean that the Law of Non-Contradiction, which says that every sentence of the form 'p & not-p' is (fully) false, has exceptions.

It is possible to deny Bivalence yet retain LEM. This is the approach taken by **supervalutional** theories of vagueness. The idea is that vagueness consists in a kind of incompleteness in the meaning of vague expressions. 'Heap', for example, has a meaning which simply fails to settle some cases. This incomplete meaning can be specified in terms of the various ways in which it could be made complete. Compare: a house is partly completed. We could specify the stage it is at by describing all the possible ways it could be completed.

Supervaluationists call the things to which a predicate definitely applies its **positive extension**, the things to which it definitely does not apply its **negative extension**, and the remaining things its **penumbra**. In their formal account, they introduce the notion of a **sharpening** (or precisification). A sharpening is like a classical interpretation: it assigns each predicate, even if it is vague, a positive extension, and its negative extension will simply be everything else (that is, the complement within the domain of the positive extension). Sharpenings are constrained by the requirement that they should assign a positive extension, which includes all the things to which the predicate definitely applies (its intuitive positive extension); it may also include things from the intuitive penumbra, but must include nothing from the intuitive negative extension. It follows that the negative extension, relative to some sharpening, will include everything in the predicate's intuitive negative extension, perhaps along with some things from the penumbra. Sharpenings are

bivalent in this sense: for every sentence, every sharpening, either the sentence is true on the sharpening or it is false on the sharpening.

### Activity 7.3

This account of a sharpening is incomplete. Thinking about a vague predicate like 'red', can you see what is missing?

*Feedback to this Activity can be found on p.44.*

The canny move of Supervaluationists is to define a derived notion of unqualified truth, which is not bivalent: truth is truth on **every** sharpening, and falsehood is falsehood on **every** sharpening. Take a borderline sentence, for example 'This is a heap', said of something neither clearly a heap nor clearly not a heap. It follows from the stipulations that the sentence will be true on some sharpenings and false on others. It is not true on every sharpening, so it is not true. For the same reason, it is not false. By contrast with the bivalent notion of truth on a sharpening, unqualified truth is not bivalent.

On the other hand, LEM remains valid on this approach. A sharpening which assigns truth to 'A' must assign truth to 'A' or not-A'. A sharpening which does not assign truth to 'A' assigns falsehood to it and so assigns truth to 'not-A' and so to 'A' or not-A'. The LEM law will be true on every sharpening on every model, and so valid.

Can supervalational semantics resolve the sorites paradox? Suppose the paradox is presented, not as I did above, but as a series of conditionals:

1. 1,000 grains of sand make a heap
2. if 1,000 grains of sand make a heap, so do 999 grains
3. if 999 grains make a heap, then so do 998 grains, etc.

There is then a cascade of *modus ponens* inferences (inferences of the form: if  $p$  then  $q$ ,  $p$ , therefore,  $q$ ) leading to the absurd result that 0 grains of sand make a heap. According to supervaluationism, not all these premises are true. Every sharpening picks a smallest heap from among the heaps in the predicate's penumbra. For example, perhaps there's a sharpening that picks as the smallest heap one with 112 grains. Then the conditional 'if 112 grains make a heap, then 111 grains make a heap' will be false on this sharpening, and so not true on every sharpening, and so not true. So the reasoning considered above is not sound: at least one premise will fail to be true. That's a point in favour of supervaluationism.

On the other hand, it fares equivocally with the paradox as formulated earlier. At first, it seems that it triumphs again, since it rules that premise (3) ('There's no number,  $n$ , such that  $n$  grains make a heap but  $n-1$  grains do not') is false. But the explanation is unsettling. According to supervaluationism, 'there is a number,  $n$ , such that  $n$  grains make a heap but  $n-1$  grains do not' is true on every

sharpening, and so true. Every sharpening draws a sharp line somewhere, and so supplies a number that verifies the claim. Admittedly, each sharpening draws the line in a different place, but the fact remains that the general claim comes out true, and seems to amount to a commitment to there being a sharp boundary to 'heap'. That's not happy, since intuitively we are strongly disposed to think there is no sharp boundary, and that premise (3) is true.

One standard further problem for supervational semantics is that the threefold division between positive extension, penumbra and negative extension seems unrealistic. There seem to be no sharp boundaries between definite heaps and heaps that are not definite heaps. So we have traded vagueness at one point (between heaps and non-heaps) for vagueness at two other points (between definite heaps and non-definite heaps, and between definite non-heaps and non-definite non-heaps). We here encounter so-called 'higher-order vagueness', which is sometimes characterised as the fact that if a predicate is vague, so is the complex predicate obtained by prefixing it by 'definitely'.

Supervaluationism at least needs some tweaking before it could be said to do justice to vagueness (and there have been many suggestions about how to tweak it). I have thought it worth mentioning here in part because it shows that even if we share much of the spirit that animates classical logic, we can make interesting departures: we do not have to be hidebound by it.

Degree theory provides another such departure, and is also worth considering as an example of imaginative variations on the classical approach. Degree theorists replace the bivalent truth values of classical logic by degrees of truth given by the real numbers between 0 and 1. This enables them to do justice to such intuitions as that, in a borderline case for 'heap', 'that is a heap' is true-ish, even if not true. Sainsbury (2009, pp.56–63) gives a brief overview of a standard degree of truth theory. A more recent version of such a theory, deserving careful study, is provided by Edgington (1997). For a good textbook on a variety of theories (ultimately favouring supervaluationism) see Keefe (2000).

# Essentialism

## Readings

Quine, W. van O. *Word and Object*. (New York: Technology Press of MIT and John Wiley and Sons Inc., 1960).

Standard criticisms:

Neale, S. 'On a milestone of empiricism' in A. Orenstein and P. Kotatko (eds) *Knowledge, Language and Logic*. (Dordrecht: Kluwer, 2000) [ISBN 140200253X].

Plantinga, A. *The Nature of Necessity*. (Oxford: Oxford University Press, 1974) [ISBN 0198244142] Chapter 2.4.

## 8.1 Necessary, *apriori*, analytic

Essentialists hold that objects have some of their properties of necessity. Otherwise put, they believe that there are *de re* necessary truths (see *Chapter 3*). Within this general framework, they hold more specific views. For example, many essentialists hold that enduring objects have their origins essentially (in that they could not have originated otherwise than they in fact did). This chapter gives a brief introduction to such views, beginning by drawing distinctions between necessity and the related notions of **analyticity** and the **a priori**.

A necessary truth is one that could not fail to be true. Standard examples are truths of arithmetic and logic. These are necessary *de dicto*: expressed in QML (see *Chapter 3*), the  $\square$  operator will take widest scope, as in:

 $\forall x((x \text{ is a mathematician}) \to (x \text{ is a mathematician}))$ .

Although it is a necessary truth that all mathematicians are mathematicians, it is not an essentialist claim. Such a claim would involve the attribution of a necessary property to an object, and would be represented in QML by a  $\square$  having narrow scope, for example:

 $\forall x((x \text{ is a mathematician}) \to \square(x \text{ is a mathematician}))$ .

This says that anyone who is a mathematician has the property of being a mathematician of necessity. So it is false, since mathematicians don't have to become mathematicians. Other essentialist claims take a similar form, but are much more plausible, for example:

 $\forall x((x \text{ is human}) \to \square(x \text{ is a human}))$ .

This says that humans have to be humans: they could not belong to another species, or be non-biological. This claim is certainly not obviously false, and many philosophers believe it is true.

'Necessary' marks a metaphysical classification: to be necessarily true is a way or mode (hence 'modal') of being true. It is being true at every possible world. At one time, people were not careful to distinguish between this classification and an epistemic one. An 'a priori' truth is one that can be known independently of experience. The same examples spring to mind: arithmetic and logic are a priori subjects. A natural thesis, often presupposed rather than argued for, is that all and only necessary truths are a priori. As we'll see shortly, one of the most interesting developments in this area is the challenge Kripke (1980) presented to this thesis.

The category of the 'analytic' comes from Kant's *Critique of Pure Reason* (1781). Kant gave non-equivalent (and somewhat obscure) definitions, but the most common gloss nowadays would be that an analytic truth is one true in virtue of meanings, like 'All mathematicians are mathematicians' and possibly 'Nothing can be red and green all over'. It is not clear whether arithmetic truths will be good examples of analyticity. People have tried to suggest that it's part of the meaning of '4' that it refers to a number which can be obtained by adding 2 and 2 together, but this is by no means universally accepted, and seems even less plausible when more refined truths are at issue. If it's part of the meaning of  $\pi$  that its value starts 3.14159265 ..., should anyone who knows its meaning know this? Yet I imagine this is known to a fairly small subset of those who 'know the meaning of  $\pi$ ', as that phrase would normally be understood (to include myself, for example: I had to look up all but the first three decimals places).

Here's an argument towards the view that the three classifications – necessary, a priori and analytic – are coextensive (just the same things fill all three classes). If a truth is necessary, its truth is independent of how things actually are. Hence we don't need experience of our actual world to come to know whether or not it's true: our knowledge of it will be a priori. Going in the other direction: if something can be known a priori, it can be known without appealing to experience of our actual world. That strongly suggests that its truth is independent of worlds, i.e. that it is true at every world.

To connect the a priori with the analytic: what do we draw upon in arriving at a priori knowledge? Not, by definition, on experience. It seems that the only remaining resource is our knowledge of meaning. But this could deliver a priori knowledge only if the a priori truths were fixed as true by meanings: only if, that is, a priori truths are true in virtue of

meaning, and so analytic. Going in the other direction: if a truth is analytic it is true in virtue of meaning. But since our knowledge of meaning is a priori, we can arrive at knowledge of analytic truths a priori. (Somewhat similar lines of reasoning can be found in Quinton, 1963.)

Although these arguments may seem plausible, they have some pretty dubious elements. Moreover, their conclusions have been challenged by counterexamples made by Kripke (1980). Providing these was part of his reinvigoration of essentialism, the main topic of this chapter.

## 8.2 Kripke's counterexamples to the coincidence

Kripke claims that although it is necessary that Hesperus is Phosphorus, it is not knowable a priori. This counterexample to the coincidence of the necessary and the a priori is widely accepted. Let's consider both aspects: the necessity and the non-a priori.

Kripke argued that identity is a necessary relation: if it holds at all, it holds of necessity. This claim can be formalised as:

1.  $\forall x(x=y \rightarrow \square x=y)$ 

It does not follow that every sentence which, intuitively, expresses an identity is necessarily true. Perhaps the greatest ruler is the wisest ruler, but this might be so only contingently. Is this a counterexample to (1)?

Kripke says that it is not, since the contingency arises from the way in which the objects (the greatest ruler, the wisest ruler) are referred to. What is contingent is that both descriptions are true of the same thing. That thing itself, however, is necessarily what it is and not another thing, and this is a claim that is closer to (1).

Kripke argued for (1) from Leibniz's Law, which can be expressed:

2.  $\forall x \forall y (x=y \rightarrow \forall F (Fx \leftrightarrow Fy))$ 

Less formally: if  $x=y$ , then any property of  $x$  is a property of  $y$ . Since being necessarily  $x$  is a property of  $x$ , if  $x=y$  this is also a property of  $y$ , and (1) follows.

### Activity 8.1

Most people accept that, necessarily, everything is self-identical. But even those who do so may argue that a thing does not have to be that very thing. In QML, the distinction is between the relatively uncontroversial  $\square \forall x(x=x)$  and the more controversial  $\forall x \square (x=x)$ . Compare Lewis, 1986. Which of these principles about identity is required for (2) to be used in support of (1)?

Given (1), necessarily, Hesperus is Phosphorus. This accords with Kripke's doctrine that names are rigid designators. Given that 'Hesperus' and 'Phosphorus' rigidly designate the

same thing, the sentence 'Hesperus = Phosphorus' is true at every world, if it is true at all; that is, it is necessarily true. Kripke tells those who think they can imagine a situation in which Hesperus is distinct from Phosphorus that what they are really imagining is an arrangement of the heavens such that one star (or planet) was the earliest to be seen in the evening and another star or planet was the last to disappear in the morning. But at least one of these would not be Hesperus (i.e. would not be Phosphorus).

Most people<sup>1</sup> agree that it is not a priori that Hesperus is Phosphorus. Telescopes, and observations, followed by careful calculation, were needed to establish this fact. So the identity is an example of a necessary truth not knowable a priori.

<sup>1</sup> *Exceptions are adamant Millians, who hold that the proposition in question is knowable a priori, since it is the same proposition as that Hesperus is Hesperus. (On this view, proper names which have the same bearer have the same meaning.)*

Essentialists (and perhaps even some non-essentialists) affirm the necessity of identity. A distinctively essentialist claim is the necessity of origin. Kripke claimed that a person could not have come from gametes other than those he actually came from. (A person's gametes are the sperm and egg involved in his or her conception.) Suppose the G are the gametes Kripke came from, where G is short for something like 'the gametes that you can just make out on these old micrographs'. On his view, Kripke could but have come from the G; that is, necessarily Kripke came from the G; but this is not a priori.

Kripke gave a rather controversial example of an a priori truth that is not necessary. Using S' to refer to the standard meter bar, held under temperature controlled conditions in Paris, he suggested that we can know a priori that S is a metre long, but that this is not necessary. Had the temperature controls failed, the stick might have expanded. Since this is possible, it's not necessary that it is a metre long. But we know the contingent fact a priori, since the very meaning of 'meter' is fixed by S.

There is a less controversial example. Consider:

If p, then actually p.

Let's think of 'actually' as a kind of 'rigid' adverb: no matter what the world of evaluation may be, 'actually' takes us back to this world, the one you and I share. Now consider some contingent falsehood, for example, 'Paris is larger than London'. The relevant conditional is true:

if Paris is larger than London, then actually Paris is larger than London

and we can know a priori that this is so. We don't have to know anything about the relative size of the cities. Relative to a world in which things had developed differently – a world in which Paris is larger than London – the

conditional is false: it will have a true antecedent, but a false consequent (since 'actually' in the consequent takes us back to how things actually are, in which London is larger).

Summarising, Kripke offered putative examples both of necessary truths not knowable a priori, and of contingent truths knowable a priori. If the examples succeed, the supposed coincidence of the necessary and the a priori has been refuted.

### Activity 8.2

Can you suggest counterexamples to the view that anything analytic is necessary? And to the view that anything necessary is analytic?

## 8.3 Quine's arguments against essentialism

Writing before Kripke, Quine had developed a number of arguments against essentialism which were, in their day, highly influential. It has to be said that, viewed with post-Kripkean eyes, they seem straightforwardly fallacious. But the fallacies (if that is indeed what they are) are instructive. I'll discuss two of Quine's arguments.

We'll start with a famous account of what essentialism is:

[Aristotelian essentialism] is the doctrine that some of the attributes of a thing (quite independently of the language in which the thing is referred to, if at all) may be essential to the thing and others accidental. E.g., a man, or talking animal, or featherless biped (for they are all the same things), is essentially rational and accidentally two-legged and talkative, not merely qua man but qua itself.

(Quine, 1966, pp.173–74)

This will serve our purposes. For more detail, see Teresa Robertson's SEP article (2008).

**1. The number of the planets** If anything has essential properties, numbers do. In particular, nine is necessarily greater than seven. The number of the planets = nine: they are the same object. So, necessarily, the number of the planets is necessarily greater than seven. However, this is false: with slight variations in some parameters at the Big Bang, there would only have been seven planets. The essentialist premise, that nine is necessarily greater than seven, leads to a conclusion (that there are necessarily more than seven planets) which even an essentialist must reject.

An essentialist will see the argument as trading on a scope confusion. The premise can be represented as a true de re necessity:

1. Nine has this property: being necessarily greater than seven.

If we understand the conclusion in such a way that the argument is valid, it will also express a true de re necessity:

1. The number of the planets has this property: being necessarily greater than seven.

However, this does not entail the false de dicto necessity:

1. Necessarily, there are more than seven planets.

If Quine's conclusion is represented as (2), then it is true, and the argument is valid, but there is no problem for the essentialist. If the conclusion is represented as (3), then it is false but the argument is invalid. Again, no problem for the essentialist.

Quine's idea is that necessity springs not from the nature of the objects, but from how we refer to them. If we refer to a certain number as the number nine, we get the necessity; if we refer to it as the number of the planets, we lose the necessity. Here's another argument he offered to make this view plausible. He says that essentialists will subscribe to the following two claims:

1. All bachelors are necessarily unmarried but not necessarily army officers.
2. All majors are necessarily army officers but not necessarily unmarried.

But, according to Quine, Major Smith poses a problem for this combination of views. He is a bachelor and a major. Qua bachelor he is not necessarily an army officer, but qua major he is. Qua major he is not necessarily unmarried, but qua bachelor he is. So we can't think of modal properties as belonging to objects: they arise from the way we refer to the objects, not from the objects themselves.

Essentialists should accept all save the last part. Neither being a bachelor nor being a major are good candidates for being essential properties. Essentialists, and anyone else, should accept (4) and (5) only as de dicto claims:

1. $\square \forall x(\text{if } x \text{ is a bachelor } x \text{ is unmarried})$  but  $\neg \square \forall x(\text{if } x \text{ is a bachelor } x \text{ is an army officer})$
2. $\square \forall x(\text{if } x \text{ is a major } x \text{ is an army officer})$  but  $\neg \square \forall x(\text{if } x \text{ is a major } x \text{ is unmarried})$ .

The de re style of necessity, distinctive of essentialist claims, is absent. It's as if Quine had said: here are some non-essential properties, so essentialism is false. That's a non sequitur, for essentialists claim only that **some** properties are essential to their possessors, not that all are.

Quine (especially in 'Two dogmas of empiricism', 1951) is also well known for an attack on the notion of analyticity. The considerations don't connect closely with his anti-essentialist arguments. They are mainly based on the fact that there is no behaviourist definition of analyticity which at all closely matches the way philosophers have in fact used the word. The closest behaviourist approximation

to 'true in virtue of meaning' is 'will be accepted under any conditions of stimulation'. This is both significantly broader than our normal use of 'analytic' (maybe under every condition of stimulation we will accept that there are or have been dogs, but this is not normally counted analytic) and also narrower (since rather complex analytic statements may not be accepted under every condition of stimulation).

Quine's criticism of analyticity, though often challenged (see, for example, Grice and Strawson, 1956), was highly influential, and for many years only an incisive philosopher would advocate a theory involving the notion. I suspect that there has recently been some change in this respect (see Boghossian, 2010), and that the notion of analyticity may come in for some refurbishment.

# The justification of deduction

## Readings

Dummett, M. 'The Justification of Deduction', *Proceedings of the British Academy* (1973); reprinted in his *Truth and Other Enigmas* (Cambridge, MA: Harvard University Press, 1978) pp.290–318.

Rumfitt, I. (2008) 'Meaning and possibilities: the semantic justification of logical laws', Inaugural lecture at Birkbeck College.

Tennant, N. 'Rule-Circularity and the Justification of Deduction', *Philosophical Quarterly* 55 (2005), pp.625–48.

How, if at all, can we justify logical reasoning? In an entertaining article, Lewis Carroll (1895) – yes, the author of the Alice books, who, as Charles Dodgson, was a mathematician and logician when not writing fiction – envisages a conversation between Achilles and the Tortoise that throws light on one aspect of the question. Here I'll simplify the details of the example, to help the main point stand out more clearly.

The Tortoise challenges Achilles to show him why he ought to accept the conclusion of an argument of the following form, given that he accepts the premises:

1. A
2. If A then B

So: B

Achilles insists that the Tortoise ought to accept B, since it 'follows **logically**' from the premises. The Tortoise says that the argument as it stands is insufficient. To bring it closer to sufficiency, the Tortoise suggests that Achilles add the premise 'If A, and also if A then B, then B'. But then the Tortoise protests: I would accept B, on the basis of this new argument, if only I saw some reason to accept that the conclusion followed from the premises. The argument with the extra premise is:

1. A
2. If A then B
3. if A, and also if A then B, then B

So: B

The Tortoise is saying, in effect, that he needs reasons to accept the following:

**if the premises (1–3) are true, so is the conclusion.**

The regressive nature of the argument is that even if Achilles adds the needed premise, and the Tortoise accepts it, he has a fresh ground for doubt concerning the argument that results: whether all the premises in

the longer argument together require him to accept the conclusion. Evidently, this doubt is not to be assuaged by moving to longer arguments, with ever more complex conditional premises.

One lesson that's hardly in dispute is that Achilles' method of responding to the Tortoise's doubts is not effective. What response would be better? Might we say that there is no way to justify the claim, concerning an argument that is in fact valid, that it is valid?<sup>1</sup> That seems a defeatist response, and is at variance with our actual practice, in which we sometimes find ourselves explaining that an argument is valid or invalid, and so, it seems, justifying its status as valid or invalid, as the case may be. For example, we might usefully point out that an argument is invalid on the grounds that although it somewhat resembles a modus ponens argument (A, if A then B, so B), it is really of the form 'if A then B, B, so A'(the 'fallacy of affirming the consequent'). Making this distinction can show that it is a mistake to regard a certain argument as valid or (in another case) that it is correct to do so.

<sup>1</sup> *This is a more interesting question than: are valid arguments valid? The interesting question relates to the validity of an argument that we can pick out independently of its validity.*

There are many tricky issues here, and I'll briefly discuss just two. The first is that we need to distinguish the fact that, by definition, the truth of the premises of a valid argument 'guarantees' the truth of the conclusion, from the question of whether we can have any guarantee that we have reached the truth, in using a certain argument. Human fallibility being what it is, it is evidently possible that someone should use an invalid argument while taking themselves to be using a valid one. Likewise, it is possible that, although we are using a valid argument, we are mistaken in thinking its premises are true. No amount of excellence in the quality of an argument can guarantee excellence in the cognitive processes of a human reasoner. It's better to use valid arguments when reasoning, but doing so is not enough to guarantee you will end up believing only truths, even if you start from truths.

The other point is that the contrast between model-theoretic and proof-theoretic conceptions of validity (see Chapter 2) suggests a non-circular way of quieting sceptical doubts. Take a seemingly model-theoretically valid argument, and allow sceptical juices to flow. The scepticism takes the form of doubting whether the argument really is the way it seems. At this point, the proof-theorist appears to have something to offer, showing

us how to prove the conclusion from the premises, using inferential steps we have no reason to dispute.

As this lame last phrase suggests, we are certainly not out of the woods. Doubt can attach to the model-theoretic validity of the steps involved in the proof (by definition these will be proof-theoretically valid). For some logics, classical logic being a salient example, there are arguments to the effect that everything model-theoretically valid is provable (the logic is 'complete') and everything provable is model-theoretically valid (the logic is 'sound'). 'But wait,' a certain kind of sceptic may object, 'how do we know the arguments for the soundness and completeness of the logic are acceptable?'

Someone unprepared to accept any kind of reasoning will not accept any proffered justification for anything. By the same token, their doubts are empty. A delicate issue in considering how, if at all, deduction can be justified is to decide just what kinds of reasoning one could accept in a purported justification. For example, some theorists suggest that we can use some elements of logic to justify others.

Another approach is to maintain that justification consists in a dynamic equilibrium: we accept certain logical laws because we find that the particular arguments they classify as valid strike us independently as valid. We may also reject the validity of a particular argument that strikes us as valid on the grounds that its validity is not vouchsafed by general laws we accept. Justification is not a linear and once-for-all enterprise, but consists in a to-and-fro of this kind, which stops, if it stops at all, when some equilibrium is reached. This kind of picture of justification may also be appropriate in other areas, for example, the justification of induction (Goodman, 1953).

# Feedback to Activities

## Chapter 1

### Activity 1.4

You'll have to read an introduction to formal logic. Take a look at Guttenplan (1997) and Hodges (2005) and see which appeals most (choose just one). They both contain more than everything you need to know, and both have proved invaluable to countless students. [Return to activity](#).

### Activity 1.5

The formula says that every property has an instance. This is false: the property of being a witch has no instance. [Return to activity](#).

### Activity 1.6

'A  $U$  B' = { $x$ :  $x \in A$   $\lor$   $x \in B$ }. ['A  $U$  B' abbreviates: the union of set A with set B] [Return to activity](#).

### Activity 1.9

Further examples might include 'very', 'however', 'main'. Some apparently topic-neutral words like 'a' and 'the' will be claimed to be logical constants: 'a' is  $\exists$ ; and 'the' is definable in logical terms in the way described in Chapter 4. [Return to activity](#).

## Chapter 2

### Activity 2.1

Call what A said A\* and what B said B\*. We start by assuming that A\* is true, and show that it follows that it is not true.

1. Assume A\* is true.
2. Everything B will say on Tuesday is true. [from 1, using T]
3. B says B\* on Tuesday.
4. B\* is true [from 2 and 3]
5. Nothing A said on Monday is true. [from 4, using T]
6. A said A\* on Monday.
7. A\* is not true [from 5 and 6]
8. If A\* is true, it is not true. [1 led to 7]
9. Suppose A\* is not true.
10. Then not everything B said on Tuesday is true. [from 8, using T]
11. The only thing B said on Tuesday is B\*.

12. B\* is not true [from 9 and 10]

13. It's not the case that nothing A said on Monday is true [from 11, using T]

14. Something A said on Monday is true. [from 12]

15. The only thing A said on Monday is A\*.

16. A\* is true.

17. If A\* is not true, it is true [9 led to 16]

We could apply so-called 'consequentia mirabilis' reasoning to (8) and (17) to infer that A\* is true and A\* is not true. The reasoning has one of the patterns: if  $p$  then  $\neg p$ , so  $\neg p$ ; or: if  $\neg p$  then  $p$ , so  $p$ . It's easy to see, from the model theoretic definition of validity, that these are valid patterns. (Consider which models verify the premise in each case.) [Return to activity](#).

### Activity 2.2

If there is a true contradiction, Explosion ensures that every sentence is true. This would 'trivialise' the logic. [Return to activity](#).

### Activity 2.5

A critic will say that we wish to say that today is Tuesday iff today is Tuesday **because** we wish to tell the truth. We can't explain the general desire in terms of its instances. [Return to activity](#).

### Activity 2.6

Paraconsistent logicians typically believe that there are dialetheias, sentences that are both true and false; that's the denial of Bivalence. Let D be such a sentence. Then D is true, and 'D  $\lor$  D' follows straightforwardly. We should conclude that LEM cannot be informally characterised as a law that ensures 'tertium non datur'. [Return to activity](#).

## Chapter 3

### Activity 3.1

No. For example, intuitionistic logicians agree with classical logicians about which are the logical constants. They disagree about their logic. [Return to activity](#).

### Activity 3.3

Some think the answer is 'yes'. But the other answer can be defended: properly speaking, it's not that Achtaeon becomes a stag; rather, he assumes a stag-like form. He's a human in a stag's body (and the

tragedy of knowing his own dogs will kill him, ones whose names he vainly tries to call, requires him to remain human). [Return to activity.](#)

#### Activity 3.4

Spelling out the proof is quite tricky, I find. Any modal logic text will take you through the steps. But here's a way to convince yourself that  $\Diamond A \to A$  is model-theoretically valid (according to the account of models given on the next page of the text):  $\Diamond A$  is true iff  $A$  is true at some world. But if  $A$  is true at some world, then  $A$  is true at every world. So if  $\Diamond A$  is true, so is  $A$ . This depends upon taking no notice of the 'accessibility' relation among worlds, in the sense that we assume that any world is accessible to any other. By placing significant restrictions on accessibility, one can block the validity of  $\Diamond A \to A$ . [Return to activity.](#)

#### Activity 3.5

First we need to relativise to worlds the principle governing change, making the accessibility relation explicit. One might end up with this:

For any pair of accessible worlds,  $w, w'$ , if  $O$  is in  $w$ , and an object  $X$  that results from changing out two or fewer parts of  $O$  is in  $w'$ , then  $O= X$ ; otherwise  $O$  is not in  $w'$ .

If this is taken as a premise, one can show that not every pair of worlds accessible. The upshot would be the rejection of the theorem mentioned in the text: what could be possible may not in fact be possible.

[Return to activity.](#)

#### Activity 3.6

There's no valid move from  $\Box \forall x(x=x)$  to  $\forall x \Box (x=x)$ . [Return to activity.](#)

## Chapter 7

#### Activity 7.3

If a sharpening excludes a somewhat red thing from its positive extension, it must also exclude anything less red. It must also respect relations between predicates: a borderline case of scarlet is a clear case of red. [Return to activity.](#)