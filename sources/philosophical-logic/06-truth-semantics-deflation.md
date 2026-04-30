---
book: "Philosophical Logic"
title: "Chapter 06 Truth: Semantics, Deflation, Indefinability and Evaluation"
chapter_number: "6"
chapter_name: "Truth: Semantics, Deflation, Indefinability and Evaluation"
author: "Anthony C. Grayling"
table_of_content: |
  Introduction
  The Semantic Theory of Truth
    The underlined sentence on this page is false.
  A Formal Sketch
  Tarski, Neutrality and Physicalism
  Is Tarski’s Theory a Correspondence Theory?
  Formal versus Natural
  The Redundancy Theory of Truth
  Proforms and Redundancy
  Deflation and Minimalism
  Truth and Indefinability
  Definition
  Truth and Objectivity
  Truth and Evaluation
  Constraints on Evaluation
  Notes
---

# 6 Truth: Semantics, Deflation, Indefinability and Evaluation


## Introduction

Theories of truth fall into two classes. One consists in those theories stating that truth is a *substantive property* of whatever the truth-bearers are. The property might be a relational one, where the relation is some form of correspondence or coherence; or a functional one, for example, epistemic utility, as in the pragmatic theory. A further member of this class asserts that truth is a substantial but *indefinable* property; Davidson takes such a view.

The other class comprises theories stating that truth is not a substantive notion; *there is nothing more* to truth, these theories say, than use of the predicate ‘... is true’ as a convenience for certain logical and rhetorical purposes. Such views are called, for obvious reasons, ‘deflationary’ theories.

This chapter considers deflationism and certain substantive views of truth other than those canvassed in the preceding chapter. But I begin with discussion of a theory which, although not a theory of truth in the same sense as the others (for strictly speaking it offers a definition of the predicate ‘... is true’ for a formal language only), has been especially influential in its wider philosophical applications. This is the Semantic Theory of Truth, devised by Alfred Tarski.¹

## The Semantic Theory of Truth

Tarski set himself the task of giving a satisfactory definition of truth, meaning by ‘satisfactory’ a definition which is both *materially adequate* and formally correct,² and which does justice to the intuition expressed in what he calls the ‘classical Aristotelian conception of truth’,³ namely ‘to say of what is that it is not, or of what is not that it is, is false, while to say of what is that it is, or of what is not that it is not, is true’, which, as noted in the preceding chapter, would find expression in contemporary terminology as a correspondence theory.⁴ In Tarski’s view both Aristotle’s formulation and contemporary correspondence theories are, however, imprecise and a source of misunderstanding. Accordingly he sought to provide a more precise expression of these intuitions by meeting a specific set of demands: ‘we must determine on what the formal correctness of the definition depends. Thus, we must specify the words or concepts which we wish to use in defining the notion of truth; and we must also give the formal rules to which the definition should conform. Speaking more generally, we must describe the formal structure of the language in which the definition will be given.’⁵


One way into an exposition of Tarski’s proposals is to note a proffered solution to the Antinomy of the Liar (the Liar Paradox).⁶ The solution turns on a distinction between what is said in a sentence of a language, and what it is said about this sentence in a ‘metalanguage’, that is, a language of higher order than the language which it takes as its ‘object language’ and in which this latter is discussed. Consider this version of the Liar:

### The underlined sentence on this page is false.

The paradox is that if what is written in the box is false, then it is true; and if it is true, then it is false. Tarski diagnosed the source of the paradox as the self-reference of the sentence, that is, the fact that it talks about itself. Strictly, the fault lies in the fact that the sentence belongs to a ‘semantically closed’ language, that is, one containing not only its normal stock of expressions, but also the names of these expressions, and semantic terms such as ‘true’ referring to its sentences; and moreover, the tacit assumption is that all sentences which determine the use of ‘true’ can be asserted in that language itself.⁷ Tarski drew the object language–metalanguage distinction to prohibit self-reference of this sort, and held that ascriptions of truth or falsity to sentences are metalinguistic: thus “New York is a large city” is true’ is a metalinguistic assertion about the sentence ‘New York is a large city’. Truth is construed as a predicate of a metalanguage applicable to sentences of its object language; it is a semantic property of sentences of the latter, predicated whenever the metalanguage states that an object language sentence designates what is in fact the case.


Sentences can only be true or false as components of a given language. There might be a language, say English, in which ‘snow is black’ means the same as is meant by the English expression ‘snow is white’, for the reason that in English ‘black’ designates what ‘white’ standardly designates in English. Then ‘snow is black’ is true in English, because the extension of ‘black’ is identical to that of ‘white’ in English, and because snow is white. So to say a sentence S is true is to say it is true in some language L. But then to say ‘S is true in L’ cannot be a sentence of L itself (at risk of paradox), but is a sentence of a metalanguage that takes L as its object language, and in which the sentences of L are not used but only mentioned and discussed. This affords one of the clearest illustrations of the importance of the distinction between use and mention.

Tarski sought to provide a definition of the expression ‘true sentence’ for a given language L in the metalanguage M of L, such that it will entail all sentences of M of the form ‘S is a true sentence of L if and only if p’, where ‘S’ is the name, or a structural description, of a sentence in L, and ‘p’ is the translation of that sentence into M. Since M may include L as part of itself, such sentences of L are their own translation into M. The requirement that the definition entails sentences of this form constitutes a criterion of material adequacy for any satisfactory definition of truth, and is called ‘Convention*`(T)`*’.

To say that Convention *`(T)`* furnishes a criterion of adequacy for truth definitions is to say that any acceptable definition of truth should have as a consequence all instances of the schema:

**`(T)`** S is true in L if and only if p.

An example of an instance of this schema is:

‘Snow is white’ is true in English if and only if snow is white.

Here ‘snow is white’ on the left-hand-side of ‘if and only if’ is the ‘name’ of the sentence on the right-hand-side. Note again that Convention *`(T)`* is not a definition of truth but a material adequacy condition, requiring that all its instances must be entailed by any definition of truth if that definition is to be minimally satisfactory. Thus the *`(T)`* schema determines not the *intension* of the concept of truth (the meaning of the word ‘true’), but its *extension* – its range.


In order to provide a *definition* of truth something has to be added to the adequacy condition – namely, proof of formal correctness in respect both of the structure of the language in which truth is defined, and of the concepts employed in the definition. Definitions of truth are given in L’s metalanguage M, and this is why L must be included in or translated into M. Because all equivalences of the form *`(T)`* must be implied by a definition of truth as required by the adequacy condition, not only must M contain L or translations into itself of all L-sentences, but also the equipment to refer to L-sentences; for *`(T)`* instances have L-sentences and expressions referring to them on the right- and left-hand-sides respectively. Moreover, Tarski required that both M and L should be ‘formally specifiable’; we must be able to specify the well-formed formulae (the ‘wffs’) of L in order to define truth-in-L, since these are the items which the predicate ‘true-in-L’ qualifies. Since no natural language (for example English, Swahili, Japanese) is formally specifiable, Tarski regarded this requirement as ruling out the possibility of defining ‘true’ for natural languages. This prompts controversy, for some believe that Tarski’s theory can indeed be extended to natural language, or at least part of it. I return to this point below.

Tarski’s definition of truth turns on the concept of ‘satisfaction’, which is a relation between objects, on the one hand, and on the other hand expressions called ‘sentential functions’, such as ‘x is white’ or ‘x is greater than y’. These expressions are sentential *functions* rather than sentences because they contain free variables marking gaps into which, to form a sentence proper, suitable terms must be inserted. The definition of a sentential function involves the notion of a ‘recursive procedure’. First the simplest sentential functions are described, and then it is shown what operations can be performed to construct compound functions out of them. Examples of such an operation are the formation of the logical disjunction or conjunction of any two functions, by ‘or’ and ‘and’ respectively.

A sentence, accordingly, can be defined as a sentential function containing no free variables. To explain satisfaction heuristically, one could say: a given object satisfies a given function if the function can be turned into a true sentence by replacing the free variable occurring in it by the name of the given object. Thus, for example, snow (not the name ‘snow’ but the actual stuff) satisfies ‘x is white’ because the sentence 'snow is white' is true. However this is a merely heuristic way of explaining satisfaction, for 'true' is being used here; because we wish to define 'true' we must seek for an account not involving 'true'.


This is done, again recursively, by first indicating which objects satisfy the simplest sentential functions, and then by stating under what conditions given objects satisfy compound functions constructed out of those simple functions. For example, we say of certain numbers that they satisfy the disjunction 'x is greater than y or x is equal to y' if they satisfy either the function 'x is greater than y' or the function 'x is equal to y'.

The notion of satisfaction thus defined applies automatically to sentential functions containing no free variables – that is, to sentences. On investigation of the formal details it turns out that only two cases are possible for a sentence: it is either satisfied by all objects, or by no objects. The sentence is true in the first case and false in the second.⁹

This is an informal presentation of the key concepts used by Tarski to define truth. I now give a condensed formal account of the same points, which those who have no taste for technicality may ignore.¹⁰

## A Formal Sketch

Open sentences such as Fx do not have truth-values, but are satisfied (or not satisfied) by sequences of objects – which is to say, by pairs of objects, or triples of objects – in general, by any ordered n-tuple of objects. Thus 'x is a man' is satisfied by Socrates; 'x is the teacher of y' is satisfied by <socrates, plato=""> (though not the other way round; hence the importance of the ordering of n-tuples); and 'x taught y who taught z' is satisfied by <socrates, Aristotle="" plato,="">. Thus satisfaction is a relation between open sentences and ordered n-tuples of objects.

Since $n$ could be any number whatever, Tarski defined satisfaction as the relation between open sentences and infinite sequences under a certain convention, viz., that $F(x_1, x_2, \ldots, x_n)$ is to be satisfied by the sequence $\langle O_1, \ldots, O_2, \ldots, O_n, \ldots \rangle$ (where $O$ is any object) in those cases where it is satisfied by the first $n$ numbers of the sequence; the rest of the sequence is ignored. \n\nThe negation of an open sentence $S_1$ will be satisfied by all sequences which do not satisfy $S_1$; the conjunction of $S_1$ and $S_2$ will be satisfied by those sequences which satisfy both $S_1$ and $S_2$; and the existential quantification of an open sentence will be satisfied by a sequence of objects in those cases where there is another sequence differing from the first sequence in at most the $i$th place, where the $i$th is the variable bound by the quantifier, which satisfies the sentence obtained by dropping the quantifier. For example, $(\exists x)(x \text{ is a country between } y \text{ and } z)$ is satisfied by the sequence (a) $\langle \text{London, Holland, Spain} \rangle$ because for example the sentence (b) $\langle \text{France, Holland, Spain} \rangle$ satisfies '$x$ is a country between $y$ and $z$'. Here the difference in the sequences ('London' in (a) and 'France' in (b)) occurs at no more than the place of the bound variable $x$; and sequence (b) satisfies the open sentence which results from dropping the existential quantifier in front of '$x$ is a country between $y$ and $z$'.


Sentences with no free variables, that is, sentences in which all the variables are bound by quantifiers, are 'closed' sentences, and closed sentences are in effect special cases of open sentences – they are open sentences with no places (they are 0-place open sentences). Now, the first and all subsequent members of a sequence are irrelevant to whether or not that sequence satisfies a 0-place open sentence. Accordingly Tarski defined a sentence as true in those cases where it is satisfied by all sequences whatever, and false when it is satisfied by none. For example, the open sentence with two places '$x$ is the teacher of $y$' is satisfied by all sequences, for example $\langle \text{Socrates, Plato}, \ldots \rangle$, no matter what their third, fourth, and subsequent members. The one-place open sentence '$x$ is a teacher' is satisfied by all sequences, for example $\langle \text{Socrates}, \ldots \rangle$, irrespective of their second and subsequent members. And the 0-place open sentence – that is, closed sentence – $(\exists x)(x \text{ is a teacher})$ is satisfied by all sequences $\langle \ldots, \dots, \dots \rangle$ no matter what their first and subsequent members – for there is a sequence, for example $\langle \text{Socrates}, \dots \rangle$, which is different from any other sequence you like in at most the first place, and which satisfies the sentence (formed by dropping the quantifier) '$x$ is a teacher'. Closed sentences cannot be satisfied by just these and not some other sequences; they are satisfied by all sequences or by none.

So Tarski's definition is that 'true $=_{\text{df}}$ satisfied by all sequences' and 'false $=_{\text{df}}$ satisfied by no sequences'. To see why, consider the closed sentence $(\exists x)(x \text{ is a teacher})$ again, and let there be a sequence of objects $A$. As stated, this sentence is satisfied by any sequence of objects if and only if there is some other sequence $B$, different from $A$ in at most the first place, which satisfies the sentence '$x$ is a teacher' formed by dropping the quantifier. This sentence will be satisfied by an object $O$ where $O$ is a teacher; so there is such a sequence if there is some object which is a teacher. Accordingly $(\exists x)(x \text{ is a teacher})$ is satisfied by all sequences if something is a teacher.


One can give the formal definition as follows. Tarski defined truth for a class calculus using a formalized metalanguage. Following Quine and Haack, however, it is simpler to demonstrate the procedure for a sparse version of standard first-order predicate calculus.$^{11}$ We have the usual variables and predicate letters; just two sentence-forming operators, $\sim$ and $\cdot$; the existential quantifier; and brackets. That completes the syntax. The atomic sentences are strings consisting of $n$-place predicates followed by $n$ variables. Nothing is a wff other than atomic sentences $A, B, \ldots$, and whatever can be well-formed from them by applying $\sim$, $\cdot$, and $(\exists \ldots)$; thus $\sim A$ is a wff, $(A \cdot B)$ is a wff, $(\exists x)A$ is a wff.

The recursive definition is then as follows. Let $A$ and $B$ range over sentences of our sparse first-order language, and let the expressions $X$ and $Y$ range over sequences of objects, with the expression $X_i$ denoting the $i$th member of any sequence $X$. Satisfaction is then defined for atomic sentences thus:

1.i. For all $i$ and $X$:

X satisfies ‘Fxi’ if and only if Xi is F.

This provides a clause for one-place predicates.

1.ii. For all $i$ and $X$:

X satisfies ‘Gxi ixj’ if and only if Xi and Xj stand in the relation G.

This provides a clause for two-place predicates. And so on for all predicates. We then turn to negation, conjunction and quantification in similar fashion.

2. For all X and A:

$X$ satisfies '$\sim A$' if and only if $X$ does not satisfy '$A$'.

3. For all X, A, and B:

X satisfies ‘A and B’ if and only if X satisfies A and X satisfies B.

4. For all $X$, $A$, and $i$:

$X$ satisfies $(\exists x_i) A$ if and only if there is a sequence $Y$ such that $X_j = Y_j$ for all $j \neq i$, and $Y$ satisfies $A$.

A closed sentence, that is a wff with no free variables, will be satisfied by all sequences or none. ‘True’ accordingly is defined thus for this sparse first-order language L: a closed sentence of L is true if and only if it is satisfied by all sequences. That, in essentials, is the manner of Tarski’s definition of ‘true’.

## Tarski, Neutrality and Physicalism

As noted above, Tarski held that his formal correctness conditions rule out the possibility of an adequate definition of truth for any language which is semantically closed, that is, which itself contains such semantic terms as ‘true’ and ‘refers,’ and which is not formally specifiable; hence there can be no adequate definition of truth for natural languages, because it is only formal languages which have the required characteristics of semantic openness and formal specifiability.

Natural languages, in short, contain their own metalanguages, and this in Tarski’s view is the source of paradox in them. Moreover they are living things, constantly in a state of change and development, and infested with such features as vagueness, indexicality, and ambiguity. These considerations persuaded Tarski that natural languages are not amenable to a truth-definition.¹² He also believed that because his theory applies only in a formal context, it is neutral with respect to traditional epistemological and metaphysical controversies; we could, in his view, accept the semantic theory of truth and retain whatever philosophical convictions we had antecedently nourished.¹³

However, Tarski’s own assessment of the implications and applications of his theory has not been accepted; it is claimed that philosophical consequences of moment follow from it, and that it rests on philosophically significant assumptions. Consider first the facts that (a) Tarski’s account makes use of an objectual reading of the quantifiers – (∃x) Fx is true if there is an object which is F; (b) that the objects over which the variables range are located in the world, and not in a model domain or possible world – ‘x is white’, in his own example, is satisfied by snow (the stuff, not the name ‘snow’); and (c) that the material adequacy condition rules out all non-bivalent truth theories, as is demonstrated by the fact that if ‘p’ in “p” is true if and only if p’ is truth-valueless, then “p” is true’ is false, with the result that “p” is true if and only if p’ as a whole must be, if not false, then at least not true. The net result of (a)–(c) is that Tarski’s theory appears both to assume and to promote a particular metaphysical view, namely ‘physicalism’.¹⁴


This point is made by Field.¹⁵ Tarski’s intentions are revealed by his saying that truth must be defined without appeal to semantic primitives, because such an appeal produces unclarity and makes it ‘difficult to bring this method into harmony with the postulates of the unity of science and of physicalism’.¹⁶ Tarski wished to make semantics a respectable enquiry from the viewpoint of science,¹⁷ and since it is an assumption of the notion of unified science – that is, of ‘physicalism’ in Tarski’s sense – that all phenomena can be so reduced that they admit of subsumption by physical laws, it follows that Tarski took himself to be providing a characterization of truth of an appropriately physicalist kind.

Having identified Tarski’s non-neutral objectives in this way, Field argues that Tarski failed to realize them. He did not succeed in providing an account of semantic primitives in acceptable physicalist terms, Field says, for his definition turns out to rest on them. Tarski demonstrates how to reduce truth to the relation of satisfaction, and satisfaction to the relation of primitive denotation; but this is to reduce semantic notions to other semantic notions, and does not amount to definition in physicalistic terms. To achieve a reduction that defines the target notions in non-semantic terms, one has to appeal to facts about the circumstances of their employment. Field accordingly offers a reworking of Tarski’s theory, turning chiefly on the claim that extensional equivalence is not enough for a successful semantic-term to physical-term reduction, but that something stronger is required; his suggestion is that one gets true reduction by defining reference as a causal relation obtaining between the physical facts and the semantic facts they sustain. (Causal accounts of reference are discussed in chapter 7 below.)¹⁸

## Is Tarski’s Theory a Correspondence Theory?

In what respect, if any, does the semantic theory support, or preserve the essential intuitions of, or even perhaps constitute, a correspondence theory of truth? Popper’s grateful reception of Tarski’s theory as at last providing what had hitherto been lacking in correspondence theories, namely a proper characterization of the correspondence relation, suggests the third possibility;¹⁹ but Tarski’s own comments at very most suggest the first two.²⁰ Popper’s claim is a strong one; it is that Tarski has

'rehabilitated the correspondence theory of absolute or objective truth' and 'vindicated the free use of the intuitive idea of truth as correspondence to the facts'.²¹ The claim merits investigation.

One way of looking at such instances of the *`(T)`* schema as “snow is white” is true if and only if snow is white’ is to take it that the left-hand-side refers to a linguistic item – a sentence – and that the right-hand-side refers to an extralinguistic item – a fact or state-of-affairs. It then looks as if the *`(T)`* schema itself – that is, “p” is true if and only if p’ – states a recipe for correspondence between linguistic and extralinguistic items. But this, by Tarski’s own account, will not in fact do; for the *`(T)`* schema, constituting as it does no more than a condition of adequacy for any truth theory, does not specify the correspondence theory as uniquely correct, but is consonant with other truth theories too. For example, it shows that a redundancy theory – in the form ‘(p) (p is true if and only if p)’ – is materially adequate; and, as Haack observes, it is even compatible with fanciful theories of the sort we would get if “p” is true’ were defined as, say, “p” is asserted by a philosopher’, for “snow is white” is asserted by a philosopher if and only if snow is white’ is an instance of the *`(T)`* schema in just the required sense that anyone who accepted this definition of “p” is true’ would accept or reject the left-hand-side just in case he accepted or rejected, respectively, the right-hand-side.²²

Matters are slightly more promising if, instead, one looks at Tarski’s definition of truth itself. The definition seems to contain material for supporting a correspondence construal in this sense, that it proceeds in terms of a definition of satisfaction, and satisfaction is a relation between sentences and sequences of objects. But the difficulty is that Tarski’s definition states that true and false sentences are respectively satisfied by all sequences and none, with no appeal being made to specific sequences.²³ Moreover, as Haack points out, ‘it is symptomatic that analytic as well as synthetic truth is embraced by Tarski’s theory; yet it is surely less plausible to suppose that analytic truth consists in “correspondence to the facts” than that synthetic truth does so’.²⁴

Part of the problem here is that because there are no satisfactory correspondence theories, it is hard to see what features Tarski’s theory must display in order to count as one. There are, for instance, considerable differences between Austin’s account of correspondence and Tarski’s theory, yet Austin’s account was offered as an alternative to such ‘congruity’ views as Russell’s, improving on all those respects in which such views fail. Thus in Austin’s account, indexical statements (not sentences) occupy centre-stage, whereas Tarski ignores indexicality altogether and takes sentences (not statements) as truth-bearers. Tarski selects sentences as truth-bearers because crucial use is made of their syntactic structure in order to define truth by means of satisfaction. Austin on the other hand held that the descriptive conventions – that is, the conventions correlating expressions to types of situations in the world – are purely conventional; any words would do, let structure fall where it may.²⁵


If therefore Austin’s theory is at least a good example of an attempt at a correspondence theory, Tarski’s theory is after all unlike a correspondence theory. If Tarski’s theory is considered a correspondence theory because it is analogous to, say, Russell’s theory in relying on structure, then for one thing the analogy is to an unsuccessful version of a correspondence theory, and for another the analogy, turning as it does on the notion of ‘structure’, is weak, because in the one case the appeal is to an isomorphic relation, in the other to syntactic features of object–language sentences.

The question asked about Tarski’s theory is ‘does it support, or at least preserve the intuitions of, a correspondence theory?’, and one is tempted to reply that if it does either, it is because it is also compatible with other truth-theories (which must be at least to say that it does not impugn the intuitions they embody), and therefore it does not do so in any specially significant way. Thus far, one element of Tarski’s own claim that his definition is neutral is vindicated, at the cost of contradicting his other claim that the theory makes precise the intuitions of the correspondence notion.

This result makes claims about the objectivity of Tarski’s theory problematic. On the face of it, it would seem inappropriate to characterize Tarski’s view of truth as ‘absolute and objective’ because it views truth as essentially language-relative; the definition is not of ‘true’ simpliciter but ‘true-in-L’. ‘The extension of the concept to be defined,’ Tarski wrote, ‘depends in an essential way on the particular language under consideration. The same expression can, in one language, be a true statement, in another a false or meaningless expression. There will be no question at all here of giving a single general definition of the term’.²⁶ There are two very good reasons from Tarski’s point of view why this must be so; the definition relies essentially on syntactic structure, and language-relativity is required for avoidance of the paradoxes.

One of the critics answered by Tarski had complained that the semantic theory involves itself in an ‘uncritical realism’, because a sentence like ‘snow is white’ is true if and only ‘if snow is in fact white’.²⁷ Tarski objected to the ‘in fact’, replying that the definition of ‘true’ implies nothing whatever as to the conditions under which ‘snow is white’ can be asserted; instead it only implies that whenever we do assert or reject ‘snow is white’ we must be ready to assert or reject the correlated sentence ‘the sentence “snow is white” is true’.²⁸ And Tarski goes on immediately to remark, ‘Thus, we may accept the semantic conception of truth without giving up any epistemological attitude we may have had; we may remain naïve realists, critical realists or idealists, empiricists or metaphysicians – whatever we were before. The semantic conception is completely neutral towards all these issues.’²⁹


Because Tarski’s definition is compatible with rival views of truth – rival in both senses of supplying different definitions of truth and different criteria or tests for ascription of truth – what Tarski says about the semantic theory’s independence from particular philosophical commitments appears unexceptionable. But this claim conflicts with what was identified earlier as the physicalist character of Tarski’s views. Could it be that the charge of assumed realism has some basis after all, despite Tarski’s own pronouncements?

Two suggestions seem to support this possibility. One is to deny that, in the end, there are different languages. If this is so, then Tarski’s theory ceases to be genuinely relative, but applies across the board. Davidson has argued, for example, that no sense attaches to the idea of genuinely different – in the sense of mutually unintelligible or inaccessible – languages, for the very criterion of languagehood is ‘translatability into a familiar idiom’ (see the discussion of relativism in chapter 9 below).³⁰ A related idea underlies Popper’s view that if p is a true sentence of L and there is a translation p₁ of p in another language L₁, then p and p₁ have the same truth-value.³¹

However, even if this is right, it only goes as far as supporting the contention that Tarski’s theory is ‘absolute’ – that is, universally applicable – for it is a further matter to show how, or even perhaps that, this entails its also being objective. For the most that one seems entitled to claim is that a notion’s being absolute is a necessary condition for its being objective; something more is required for sufficiency.

The other suggestion arises from the fact that Tarski’s view countenances only bivalent theories of truth. It is a tenet of Dummett’s arguments that bivalence is closely linked to realism, on the grounds that if sentences are determinately true or false something independent of us and our knowledge must make them so. (This is discussed in chapter 8 below.) To be a realist about truth is indeed to regard truth as in some strong sense objective. If these thoughts are right, they lend support to Field’s account of Tarski as described above.


## Formal versus Natural

But Tarski’s own strictures, as noted, rule out adaptation of the semantic theory to understanding ‘true’ in natural language contexts. This is not a difficulty to be solved by so rationalizing natural language as to make it apt for Tarski-style theory; in ordinary speech the truth-value of what is said is heavily indexed to speaker, time and context of utterance, so the mere sentence uttered appears too thin a plank to bear truth’s load, and the whole indexed complex too complex to be explained just in terms of entailment via Convention *`(T)`*. In this respect Tarski’s pessimism seems justified. And this consideration touches only on indexicality; matters are in fact more complex owing to the presence in natural language of ambiguity, vagueness, ellipsis, irony, and other complicated features.

To say that a Tarski-style definition of truth cannot be given for natural languages does not of course amount to saying that truth cannot be explained for natural languages – still less that there are no truths expressed or expressible in natural languages. What it might rather mean is that Tarskian truth, because it is specific to formal contexts, is not truth but truth-in-a-formal-context, a quite different matter and therefore irrelevant to truth simpliciter if there is such a thing (Tarski contemplates the possibility that a number of different things get misleadingly lumped under the label ‘truth’). Tarski was prepared to acknowledge as much, offering if necessary to call his account of truth an account instead of ‘fruth’, where ‘frue’ means, roughly, ‘true-in-a-formally-specifiable-language’. But this should not be permitted to mislead, as it would if it suggested that truth is to natural languages what fruth is to formal; that, in other words, points of analogy might appear on inspection. For we do not have a theory of truth of which a theory of truth can be the formal analogue.

Moreover, as Strawson argued, it might be that even if a Tarski-style theory could be extended to natural language, it would not really explain the meaning of ‘true’, but, at best, of ‘true if and only if; because such equivalences as “New York is a large city” is true if New York is a large city’ could be construed as degenerate cases of equivalences in which we could read ‘means that’ for ‘true if, as for example in “New York est une grande cité” is true if New York is a large city’. Davidson, as we shall see, takes this to be no criticism at all, but the specification of a virtue (again, see chapter 8).


Evidently, then, the general (as opposed to strictly formal) relevance and, if relevant, importance of Tarski’s theory of truth is something that can only be determined by looking at an attempt like Davidson’s to make it work in the context of natural language. It is plain that Tarski’s work has great merit in its formal setting; truth-conditional semantic theory, if successful, extends that merit to philosophy in general.

## The Redundancy Theory of Truth

In his criticism of Austin as described in the preceding chapter, Strawson put forward an alternative view of truth, which is that to say a statement is true is in effect to support or endorse it, as if to say ‘yes’ or to nod in agreement – a view sometimes therefore called the ‘performative’ theory of truth. Strawson claimed that the right question to ask about truth is, ‘how is “true” used?”, the answer implying that there is no more to truth than the performance of agreement, endorsement or emphasis just sketched. This view has affinities with the ‘Redundancy Theory’ put forward by Ramsey.³²

In the course of discussing judgement Ramsey offered some remarks about truth ‘to show that there is really no separate problem of truth but merely a linguistic muddle’³³ His argument is as follows. Truth and falsity are primarily ascribed to propositions, and propositions can either be explicitly given or described. In the case of an explicitly given proposition such as ‘Caesar was murdered’, it is evident, in Ramsey’s view, that ‘it is true that Caesar was murdered’ means precisely the same as ‘Caesar was murdered’, and ‘it is false that Caesar was murdered’ means precisely the same as ‘Caesar was not murdered’. Accordingly, the ascriptions of truth and falsity in these cases are redundant; at best they add emphasis, or mark the place the proposition has in the argument, or are placed there for stylistic reasons.³⁴ One could equally well say ‘it is a fact that Caesar was murdered’ or ‘that Caesar was murdered is contrary to fact’. Yet appeal to ‘facts’ is as redundant as appeal to truth and falsity.

Similarly, ‘is true’ and ‘is false’ are redundant in the case of described propositions, although matters are somewhat more complex here. If I say ‘he is always right’, I mean that ‘the propositions he asserts are always true’, and on the face of it there seems no way to dispense with the word ‘true’ in expressing the point. However Ramsey suggests an analysis to eliminate ‘true’; the first step is to recast ‘the propositions he asserts are always true’ as ‘for all p, if he asserts p, p is true’, and then we see that the propositional function ‘p is true’ is simply the same as p, just as in the Caesar case above; ‘for all p, if he asserts p, then p’.³⁵

Ramsey suggested that we add ‘is true’ in English to give the sentence a verb, forgetting that ‘p’ already contains one. The point is clearer if one considers, say, the relational form of the proposition, aRb; then ‘he is always right’ can be put as ‘for all a,R,b, if he asserts aRb, then aRb’. Adding ‘is true’ is obviously superfluous.

In general, Ramsey took it that our real interest in this connection does not concern the nature of truth and falsity, but the nature of judgement or assertion; for the problem in the foregoing example is how to analyse ‘He asserts aRb’.

The redundancy view comes down, then, to saying that ‘true’ and ‘false’ are predicates which can be dropped without semantic loss, having only a stylistic or otherwise pragmatic role. There are certain virtues attaching to this view; for one thing, it avoids all the difficulties of a correspondence theory, for no question arises about any of the three correspondence terms – the relata of facts and propositions and the relation of correspondence itself. ‘It is a fact that’ is as redundant as ‘it is true that’, which does away with facts; and because ‘is true’ is an eliminable predicate, it does not introduce a genuine property to be attached to whatever is asserted, and so there is no need to invoke propositions as truth-bearers – for where there is no truth to be borne, no bearers of truth are required. And then, if neither facts nor propositions occur in the picture essentially, there is no need to specify a relation between them. Thus every difficulty encountered by the correspondence theory is avoided.

Nevertheless there are problems beneath the surface simplicity of Ramsey’s proposal. His account demands a suitable handling of second-order quantification for the case where propositions are described – that is, where what is asserted is not explicitly given but introduced obliquely. Ramsey’s offering was ‘for all p, if he asserts p, p’ as an analysis of such cases, containing no use of ‘true’. But now the question arises: is the

universal quantifier ‘for all . . .’ to be understood objectually or substitutionally?³⁶

If objectually, then for one thing it looks as though propositions might after all have to be retained as the objects quantified over, and if the bound variables, ‘p’s, are to have the syntactic function of singular terms, as on this interpretation is required, then the final ‘p’ in ‘for all p, if he asserts p, then p’ will have to be regarded as an ellipsis of ‘p is true’ for it to be sufficiently sentence-like to serve as the conditional’s consequent. And if so, ‘is true’ is not redundant after all.

If on the other hand the quantifier is interpreted substitutionally, then ‘for all p, if he asserts p, then p’ turns into ‘all substitution instances of “if he asserts p, then p” are true’; and again ‘true’ remains firmly entrenched in the analysis.

## Proforms and Redundancy

Because ‘true’ refuses to be redundant on either of these standard interpretations of the quantifiers, another tack is required. An ingenious idea to this end is proposed by Grover.³⁷ It has often been remarked that there are words and expressions which behave, in respect of other grammatical categories, in the same useful portmanteau fashion as pronouns (‘he’, ‘it’) which stand in for nouns and descriptions. Thus the verb ‘do’ can serve in place of most active verbs, and ‘nice’ is a portmanteau adjective of positive purport. On analogy with pronouns, such words can be called proverbs and pro-adjectives respectively. Grover specifies a general category of *proforms* to collect pronouns, proverbs, pro-adjectives, and the like, and this category has the feature that all of its members must be capable of anaphoric use – that is, can be cross-referentially used in the way pronouns are as in ‘Tom wished to buy it, but he hadn’t enough money’, or ‘if a bomb falls, get out of its way’.

The proform Grover is chiefly concerned to introduce is a *prosentence*, ‘thatt’, which can be used anaphorically for any sentence. The proposal is that ‘for all p, if he asserts that p, then p’ is to be recast as ‘for all propositions, if he asserts that thatt, then thatt’. The idea is that the difficulty encountered by Ramsey’s view arises only because there are no words or phrases which can stand for sentences as pronouns stand for nouns, thus blocking the required richer reading of the quantifiers. Supplying prosentences removes the difficulty. One virtue of the sugges- tion is that, from the purely formal point of view, this reading is compatible with both the objectual and substitutional interpretations of the quantifiers.


Two difficulties infect Grover’s manoeuvre. One is that there have to be strong reasons for supplementing English in this way, or, at least, it must be the case that there is room, made available by the analogical similarity of prosentences to other anaphoric devices already available in the language, which as it were invites just this kind of proform to fill it. The room does not naturally exist (English gets along without prosentences), and so the question becomes: does anything oblige us to make that room? Now, the chief motive for inventing the prosentence is to free us from having to make essential use of ‘is true’ and ‘is false’. But is it clear we have to be free in this way? Ramsey’s argument itself does not, at least as it stands, show that the notions of truth and falsity are genuinely redundant, still less (as he claimed) misleading. Why then accept the neologism ‘thatt’ in the first place, if its purpose is merely to force a reading of the quantifiers which will conform to Ramsey’s view?

The answer lies in the fact, as Grover and before her Prior noted, that without suitable expressions for second-order quantifiers, we appear to be bound to use noun-like idioms such as ‘everything’ and ‘something’ with all the objectual implications of so doing.³⁸ Prior himself suggested using ‘–whether’ as the appropriate reading, so that (∃p) would be ‘somewhether’ and (p) ‘anywhether’, and thus such a string as ‘(p)(p → p)’ would be read ‘if anywhether, then thether’.³⁹ Grover’s proposal is a refinement along the same lines. The thought is, in other words, that Ramsey had groped for a way of saying that if one could only make out a proper account of propositional quantification, predications of ‘true’ and ‘false’ would be recognized as otiose, just as it appears when we see that ‘it is true that Caesar was murdered’ says no more than ‘Caesar was murdered’. The innovations provided by Prior and Grover supply materials for such an account.

Still, there is the second difficulty, and it is more of a difficulty. Grover and others applied the prosentence idea to the redundancy theory by proposing that ‘that is true’ is itself to be regarded as a prosentence.⁴⁰ Use of ‘it is true’ as an atomic prosentence eliminates the need for ascriptions of truth; ‘true’ itself remain only residually as a non-separable part of the prosentence. But will this do? Haack, for one, thinks not: “True”, one is told, is eliminable; not from English, to be sure, but from English [plus] “thatt”. But how are we to understand “thatt”? Well, there’s nothing exactly like it in English, but it works like “that’s true”, except for being atomic rather than compound’ – and so ‘true’ remains.⁴¹


## Deflation and Minimalism

But what is the truth that thus remains? Not all deflationary theories are redundancy theories; they reserve a role for the concept of truth, but claim that it is a minimal one. What they deny is that truth is a *substantive* property. Ramsey’s theory (and Strawson’s performative version of it) are in a sense too deflationary, because they deprive the notion of truth of an important role in inference. On the redundancy theory, ‘it is true that p’ and ‘p’ mean the same. But this blocks an understanding of how we can conclude ‘p is true’ from ‘S said p’ and ‘what S said is true’; the inference turns on applying Leibniz’s Law – if x and y are identical, they have all and only the same properties – which one cannot do unless truth is a property. But according to Horwich’s version of a deflationary theory, which he calls ‘Minimalism’, truth *is* a property (and a property of propositions) but not a substantive one. There is however no more to truth than its use in the logical role just illustrated. For the reason offered by that illustration, it is, he says, therefore better to limit the deflationary view to a weaker claim, namely, that ‘p is true’ and ‘p’ are equivalent.⁴²

Horwich claims that the truth predicate’s only *raison d’être* is to satisfy the logical need felt in the above example. The claim is more fully made out as follows. We have the need on occasion to adopt an attitude to a proposition, for example, to believe or assume it; but we do not exactly know what the proposition is (maybe we did not hear clearly what someone said when expressing it). Perhaps we just know that it is ‘What Oscar thinks’, say. ‘In such situations,’ Horwich writes, ‘the concept of truth is invaluable. For it enables the construction of another proposition, intimately related to the one we can’t identify, which is perfectly appropriate as the alternative object of our attitude. Consider, for example,

**`(1)`** What Oscar said was true.

Here we have something of the form

**`(2)`** x is F

whose meaning is such that, given further information about the identity of $x$ – given a further premise of the form

**(3)** $x = 	ext{the proposition that } p$

– we are entitled to infer

**`(4)`** p.

And it is precisely from this inferential property that propositions involving truth derive their utility.⁴³

The concept of truth is able to play this role because for any declarative sentence $p$ we can give an equivalent sentence ‘the proposition that $p$ is true’ where the sentence ‘$p$’ has been replaced by the noun phrase ‘the proposition that $p$’ and the truth predicate ‘is true’ has simply been employed to keep a sentence structure (‘it acts simply as a de-nominalizer’, Horwich says).⁴⁴ Nothing more about truth need be assumed; this exhausts the notion. Nevertheless Horwich claims, and sets out to show, that the minimalist view is neither too obvious nor too weak to have significant philosophical implications. Both in respect of general principles involving truth – for example, that verification indicates truth and that true beliefs conduce to successful action – and with regard to solutions of problems about, for example, vagueness and scientific realism, the minimalist view is, he argues, sufficient.⁴⁵ It is summed up in the claim that the notion of truth contains nothing more than is expressed by uncontroversial instances of the equivalence schema:

(3) It is true that $p$ if and only if $p$.

The theory to this effect is the ‘minimalist theory’; the account of the motivations, consequences and defences of the theory Horwich calls ‘the minimalist conception’, and it is from this latter, rather than the theory as such, that some of the material for discussion of problems about vagueness and scientific realism come.

There are a number of objections to deflationism thus conceived. One is that there are some clearly false instances of the equivalence schema *`(3)`*. Horwich gives as an example, ‘THE PROPOSITION EXPRESSED BY THE SENTENCE IN CAPITAL LETTERS IS NOT TRUE’. Substitution of this into *`(3)`* generates a Liar-type paradox: ‘The proposition that the proposition expressed by the sentence in capital letters is not true is true if and only if the proposition expressed by the sentence in capital letters is not true' easily yields a contradiction. So not all instances of *`(3)`* can be included in the theory of truth; but it is hard to specify which they are. Horwich remarks, in defence, that deflationism is not alone in this dilemma.46


Another objection is that although the theory can be described it cannot be formulated explicitly, for it has an infinite number of axioms. Horwich argues that the response to this, in the form of the construction of theories showing how the truth of propositions derives from their constituents' referential properties, faces two difficulties: that we cannot be sure that all propositions get their truth in this way, and that anyway there is no satisfactory finite theory of reference in the offing.47

A number of Horwich's critics object to his choice of propositions as truth-bearers, on the familiar grounds of their alleged unsatisfactory character. They apply the deflationary account to sentences instead: a schema might be, “‘s” is true if and only if s’. In this guise the redundancy theory is called the ‘disquotational theory’, for, as Quine puts it, ‘Attribution of truth to “Snow is white” just cancels the quotation marks and says snow is white. Truth is disquotation.’48 In Horwich's view the disquotational theory fails to cope with terms that change their reference according to occasions of use, as with indexicals (‘now’, ‘here’) and demonstratives (‘that’). It is not true, for example, that every instance of ‘I am weary’ is true if and only if I am weary. To adapt the disquotation schema to accommodate these cases is difficult; Horwich recommends defending propositions instead – among the virtues of doing which, he says, is fidelity to ordinary language and a plausible concomitant account of belief.49

The chief difficulty, or set of difficulties, with the Minimal Theory, or indeed any deflationary theory, is the stubbornness of the idea that truth is a substantive notion that plays an explanatory role in thought. Ramsey, like Strawson after him, cited examples in which 'is true' is used merely corroboratively, and pointed out that there are more ways of agreeing or endorsing than by saying 'that's true' or affixing 'is true' to a repetition of what is said; and took this as among the reasons for thinking appeals to truth are redundant. But 'is true' might have such uses, yet in other typical uses might also introduce a substantive property. It might function in some of its uses in the way Horwich describes, and yet also introduce a substantive property. It might disquotationally capture the triviality that

's' is true if and only if s, and in other typical uses introduce a substantive property. In short, everything deflationists say about truth could be true except that there is no more to truth than these uses. This is the essence of the deflationary claim, and it is what that stubborn thought about truth resists.

The stubborn thought arises whenever something important hangs on whether or not some proposition is true. Suppose Tom tells Dick something of central importance to Dick's life, liberty or estate. Dick may urgently wish to know whether what Tom said is as Tom said, and accordingly checks with Harry. If Harry says 'what Tom said is true', what is of crucial interest to Dick is that Harry means 'things are actually as Tom says they are', for it would be much less interesting to Tom if what Harry meant was, say, 'I agree with or endorse what Tom said'. It is the fact that there is a difference between saying 'that is the case' and 'hear, hear' that makes for the interest – and puzzle – in truth; and in any case one suspects that the notions of corroboration and agreement in part turn on an account of 'taking to be true' and hence again of 'true'. It might be that there is 'no separate problem of truth', as Ramsey argued, in the sense that truth might turn out to be inextricably linked to epistemological or semantic considerations; but it is not immediately clear that this entails some form of deflation.

For this reason the test of deflationism is whether it can satisfy us on a range of questions where truth seems to play a substantive role – as the goal of enquiry; as explanatorily powerful; as the reason for the empirical success of theories; as required to sustain realist conceptions turning on a distinction between truth and verification; as figuring in an explanation of valid inference; and much more. These points are considered by Horwich, who as noted takes his view to be adequate to them. If right, he shows that it is indeed a misconception, as he claims, to think truth has a hidden structure which, if we could discover it, would explain fundamental philosophical principles and solve many problems.⁵⁰ He diagnoses the cause of this misconception to be a misleading linguistic analogy: 'Just as the predicate, "is magnetic", designates a feature of the world, magnetism, whose structure is revealed by quantum physics, and "is diabetic" describes a group of phenomena, diabetes, characterizable in biology, so it seems that "is true" attributes a complex property, truth – an ingredient of reality whose underlying essence will, it is hoped, one day be revealed by philosophical or scientific analysis.' This characterization of what truth is not suggests a different misconception, about what is meant in saying that truth is a substantive property of its bearers; I discuss this below, after first turning to the idea that it is a *primitive* substantive property which cannot therefore be defined.


## Truth and Indefinability

The idea that truth is an indefinable substantive property is put forward by Davidson. Truth plays a crucial role in his views about meaning and other matters (see chapters 8 and 9 below), and therefore the idea that a concept so fundamental and consequential can just, so to speak, be *available* without requiring definition or analysis, is a seductive one. In this view the burden lies not on the concept of truth itself but on the indefinability claim. What follows discusses this claim.

‘Truth is beautifully transparent compared to belief and coherence,’ Davidson claims, ‘and I shall take it as primitive.’⁵¹ The comparison is drawn because whereas belief and coherence might be thought necessary for a definition of truth as coherence among beliefs, Davidson has no intention of so defining it. To take truth as primitive is to say that it is indefinable. This strategy turns out to recommend itself generally to Davidson as a way of dealing with most major concepts in philosophy.

In the introduction to his paper ‘The Folly of Trying to Define Truth’⁵² Davidson tells us how to address the concept of truth and by extension these other major concepts, such as belief, memory, perception and causality. The proposal amounts in effect to a suggestion about philosophical method. His suggestion is that we are to eschew the strategy of seeking *definitions* of a certain sort, and to practise instead what might be called a Strawsonian strategy (not Davidson’s term) of tracing connections among concepts.

Davidson begins with a cautionary tale, concerning the failure of Socrates ever to arrive at what he seeks in Plato’s earlier dialogues, namely, definitions of beauty, courage, justice and other important notions. His quest seems bound to fail because he seeks a *sharp* answer to the questions (where X is justice or beauty or some such) ‘what is Xness?’, ‘what makes X things X?’ And Socrates does not accept definition by extensional paradigms, that is, proffered examples of, say, beautiful people or just actions.

Davidson appears to identify the kind of definition Socrates mistakenly seeks as *reduction* of a target concept to ‘other concepts that are simpler, clearer and more basic’.⁵³ He also describes this style of definition as the 'formulation in a clearer, more basic vocabulary' of the elements that must figure in the analysis of some concept.⁵⁴ In Davidson’s view, Plato failed to notice that some philosophically important concepts are not amenable to such definition. When you add the fact that in discussing one concept – say, knowledge – philosophers typically pretend they understand the other concepts required – in this case, at least truth and belief – you see a moral: in Davidson’s words: ‘however feeble or faulty our attempts to relate these various basic concepts to each other, these attempts fare better, and teach us more, than our efforts to produce correct and revealing definitions of basic concepts in terms of clearer or more fundamental concepts.⁵⁵


And he goes on to say that this is only to be expected, because the concepts that attract philosophical attention – truth, action, knowledge, belief, cause, the good and the right – are ‘the most elementary concepts we have’ without which we might not have any others. So why do we presume that they can be definitionally reduced to simpler, more basic concepts? ‘We should’, he concludes, ‘accept the fact that what makes these concepts so important must also foreclose on the possibility of finding a foundation for them which reaches deeper into bedrock’.⁵⁶

And this insight is to be applied to the concept of truth: we cannot hope ‘to underpin it with something more transparent or easier to grasp’; it is indefinable.⁵⁷ Nevertheless, to say that truth – along with the important concepts – is indefinable is not to say that nothing revealing can be said about it, or that it is ‘mysterious, ambiguous, or untrustworthy’, for the strategy of tracing its connections with other concepts (such as belief, desire and action) shows otherwise.⁵⁸

There is much to say about these points. Davidson’s preferred strategy, that of tracing connections among concepts, is reminiscent of Strawson’s ‘descriptive metaphysics’ in *Individuals*. Davidson contrasts it with the strategy of trying to understand what is problematic in terms of something clearer, simpler, or more fundamental, a strategy which perhaps should be called Russellian rather than Socratic; it does not merit the label Socratic, for Davidson has chosen to treat definition in effect as analysis, which Russell distinguished sharply from definition. Socratic definition, so far as it can be separated from Platonic definition associated with the Theory of Forms, is *exact specification of the essence* of something – typically, an abstract reality such as piety or goodness. Plato took it that the Theory of Forms offers an account of this which is lacking in Socrates, although his procedure can also sometimes be construed as definition of

concepts rather than things, however conceived, as when in the Theaetetus he discusses knowledge.

The point of remarking the historical prefigurings of the opposition Davidson sets up is that they help us to understand his argument. He identifies definition with the Russell-like strategy of analysing concepts into clearer and simpler ones, cites examples of how this fails, and urges in its place a Strawson-like strategy of tracing conceptual connections. I shall give reason for saying that the two strategies are not exclusive, that the Russellian strategy has much going for it, but is not one of stating definitions (Russell expressly conceived analysing as distinct from defining), and that the Strawsonian strategy is not entirely satisfactory for Davidson's purposes, and anyway suffers a severe limitation. All this shortly.

Davidson's remark that most philosophically significant concepts 'are the most elementary concepts we have' invites comment.⁵⁹ The examples, recall, are truth, action, knowledge, belief, cause, the good and the right. There would be near consensus that these are among the most important in philosophy. The quite different claim that they are the most basic – even in the weaker sense that they are the most basic in some respect or for some discourse – precisely constitutes the substance of much philosophical debate, against which it begs the question simply to claim that they are. For one example, consider a view of truth which has it that truth is a portmanteau concept for a range of more specific evaluatory concepts individuated by discourse.⁶⁰ Such a view denies that the concept of truth is basic, but affirms its importance against deflationary views; it says that truth is not one insubstantial thing but several substantial ones, each in its different way more fundamental than the generic concept. It is the possibility rather than the merits of such a theory that illustrates the present point: that the question whether a given concept is basic is frequently moot, and in every such case the claim that it is indeed so needs an argument.

It might be the result of a Strawsonian enquiry into the order of dependence among concepts that we can specify which are more and which are less basic, but to begin such an enquiry with the ordering already assumed renders such enquiry pointless.

But here is the respect in which a Strawsonian strategy – and more specifically, Strawson's own strategy – seems not to fit Davidson's bill in any case. As the foregoing remarks imply, for Strawson a major part of the tracing task is to identify the order of dependence among concepts, with the target, or at least the guiding ideal, being the discovery of which occupants of the logical space under scrutiny are fundamental to others. This strategy naturally fits one that finds transcendental arguments a useful device for identifying fundamental concepts, for their purpose is to show which concepts must be in one’s possession as a condition for the possession of given others. This strategy, when successful, offers an anchorage in certain concepts which, although they might not turn out to be simpler than the concepts whose possession they make possible, would by the argument be more fundamental, and might therefore constitute a resource for analysis or even definition of non-fundamental concepts. It seems implicit in the Strawsonian strategy, in other words, that tracing connections yields an ordering of the more and the less fundamental; and analysis (or what Davidson calls definition) is thereby made possible.


The question whether a concept is basic is quite different again from the question whether it is elementary or simple. Basic concepts can be complex, and arguably many are. That is why we think them in need of analysis, or explication, or perhaps even definition. Elementary or simple concepts are those which are by definition incapable of further analysis. But this by itself – and I return to the point later – does not mean that they are incapable of definition. It again begs questions to label a concept ‘elementary’ if the point is thereby to warrant its indefinability, for the two are not the same thing.

To call a concept ‘elementary’ is to accord it a distinctive structural role in some conceptual edifice – in effect, a foundational one. When the foundation in question is that of our thought we require the elements to be more exact and perspicuous than less elementary parts of the structure – that is, than the dependent concepts in the scheme. But this is obviously, in fact notoriously, not so with the concepts Davidson describes as elementary.

Davidson says that ‘we should accept the fact that what makes these concepts so important must also foreclose on the possibility of finding a foundation for them which reaches deeper into bedrock.’ One has to guard against versions of what might be called the ‘argument from impotence’, employed by Descartes in saying that the mind-body problem is best solved by being ignored because it defeats human understanding, a view repeated by McGinn in claiming that humans are constitutionally barred from knowing how consciousness arises from brain-function. Arguments from impotence are an objectionable re- source for philosophers to employ: such arguments release one from thinking about the allegedly unsolvable problems, which is the opposite of what one should be doing. For present purposes, the remark suggests that Davidson’s version of the Strawsonian strategy sees it as tracing conceptual connections on the same epistemic and logical level; it is an anti-foundational version of the strategy; and this arguably compounds what is anyway the most serious limitation of the strategy: its invitation to a form of relativism not envisaged in Davidson’s other well-known anti-relativistic arguments (see chapter 9 below).⁶¹ Of this, more in a moment.


The worst problem with allegedly elementary concepts as with allegedly indefinable ones is that they can be over-permissive. Specifying a concept as elementary or indefinable without also specifying constraints on its use, carries a risk. It is that such concepts permit too much in the way of inferences. Consider this comparison: suppose you count into your scheme the concept of an omnipotent deity. Then almost anything goes; because, for example, the laws of nature can be suspended at any time, in any way, and therefore practically nothing is ruled out as to what can and might happen. I say ‘almost anything goes’ because one does not know whether an omnipotent deity can do logically impossible things, or eat himself for breakfast, and so forth. But almost everything else goes. So we approximate to the acceptance of a contradiction as a premiss: here absolutely anything goes. Simple or indefinable concepts, if unconstrained, or not subjected to the government of conditions of application, are over-permissive in this way, allowing anything or at least too much to be thought or inferred. But the danger is that if anything or too much is licensed by employment of some concept, nothing or too little of any use is. This is a cousin of the thought that if a theory explains everything and accommodates all cases, it explains nothing.

To deal with this problem Davidson says that although truth is indefinable, this does not mean that there is nothing revealing to be said about truth. The revealing things consist in tracing conceptual connections.

This is, however, as stated, a strategy with serious limitations. Consider as an example the sentence, ‘He has Jupiter on the midheaven, with Sagittarius rising, and Mars in the seventh house’. This introduces a spate of concepts whose interrelations, once grasped, clarify one other. But the question is not whether astrological concepts clarify each other by their interrelations, but whether any sort of reality answers to them; or more weakly, even whether they stand up to scrutiny, however well they hang together from an internal perspective.


Now, Davidson might say that this misses a point, namely, that these clusters of concepts must themselves relate to yet others in the larger discourse, and our adjudications of their value flow from understanding those larger relations. For example, theological claims compete for the truth with scientific ones over such matters as the origin of the universe, or whether water can turn into wine without the help of grapes; and when we see how the concepts domiciled in each more largely relate to others, we see which are the more acceptable.

But this reply only enlarges the scope of the difficulty. Contrast the Strawsonian strategy with what looks like a legitimate ambition to understand individual concepts (no insignificant matter even for the task of ascertaining how the nature of each influences the relations it can have with others) and to find some maximally stable basis for doing so in the light of how things are in the world, or in the limits of experience, or in the constraints of logic or at least of rationality — all in the hope of securing objectivity, or its closest approximation, for them. This is not something a Strawsonian strategy even tries to offer. That strategy offers an account only of *relations among concepts*; and therefore what applies to theological or astrological concepts as a family — namely, that the Strawsonian strategy offers no guide to their legitimacy or justification beyond what that family of concepts internally claims for itself — applies to the whole family of all our concepts.⁶² We do not escape what is wrong with parochiality and relativism by claiming that the whole scheme is the parish. (Rorty finds Davidson’s views agreeable for this very reason, which suggests some familiar forms of criticism.) It might be questioned how far anything has been clarified if the terminus of enquiry is just: an internal mapping of connections.

## Definition

One might remark that Socrates’ refusal to accept definition by extensional paradigms is a serious mistake. This form of definition operates by the giving of focal examples, grasping which as such enables normally intelligent persons to apply the concept thereafter in usual conformity with their fellow-conceptualizers. Many general concepts, such as those of colours, are not amenable to definition by, say, the statement of

necessary and sufficient conditions for their application; rather, they are learned and used on the basis of agreements about focal cases, focal non-cases, and shared hesitancies at the margins. The ability to display the right skills in application, and to behave in closely similar ways to other conceptualizers in cases of vagueness, constitutes our test of whether someone has mastery of given concepts. *Mutatis mutandis*, the same applies for mastery of the general terms that denote them.

This prompts one to remember that there are many kinds of definition. This is not the place for a detailed taxonomy, but it is helpful to recall the following, doubtless incomplete, assortment: there is ‘analytic definition’ in Moore’s sense, where ‘analytic’ has its chemical connotation (analysis into constituents or components), and his preferred view of philosophically proper definition, which is analytic in the semantic sense. There are lexical definitions, of the kind familiar in dictionaries, where approximating paraphrases do as well as the provision of synonyms. There is ostensive definition, which is actually a family of procedures of defining by showing, manifesting, displaying or demonstrating the definiendum, of which denotative definition – pointing a finger, perhaps while uttering the name of the thing picked out – is a focal case. There is definition in use, there is definition by paradigms (these differ technically from ostensive definitions because in order to grasp them the beneficiary of such definition must be able to extend application to relevantly like cases – the complexity of the procedure is considerable on the take-up side). There are stipulative and abbreviating definitions, the latter in Russell’s and Whitehead’s *Principia Mathematica* sense. And all these are to be distinguished from – though they stand in close relation to – explication, description, analysis in the standard Russellian sense, and the tracing of connections between concepts as in the Strawsonian strategy.

Of these many kinds of definition Davidson considers only two: the extensional paradigms kind just mentioned, and what he describes as the ‘definitional reduction’ to simpler, clearer, and more basic concepts of the target concept. As already noted, this definition of definition is problematic. Russell insisted that definition and analysis are different, and that where a definition cannot be given, an analysis often can and should be.⁶³ But, again as noted earlier, Russell meant by ‘analysis’ exactly what Davidson means by ‘definition’. Russell contrasted analysis both with definition as he and Whitehead defined it in *Principia*⁶⁴ and - for the cases he recognized as more germane to the treatment of problems outside the formal context – with definition as Moore understood it. The first kind is stipulative; it records a decision to use symbols in a certain way. Moore’s famous account focuses upon concepts; he rejects what, for present purposes, he confusingly calls ‘analytic definitions’, namely, definitions of *things* in terms of their parts and arrangements, as philosophically irrelevant. As to concepts, he requires that definitions should be analytic; definiens and definiendum must be synonymous if the former is to provide us with what we want in respect of the latter.


But for Russell an analysis breaks up and typically dissipates its target in the analysandum, so that it does not figure in the analysans. The lump of rock vanishes into a cloud of charged particles; the sentence with a definite description in grammatical subject place becomes a tripartite conjunction with, in the perfect language, bound variables in logically proper place: the definite description has vanished.⁶⁵ So there is a sharp contrast between Russellian analysis and Moorean definition. Might it be that Davidson tacitly assumes Moore-leaning constraints in the reduction he has in mind as defining of definition? The fact that one has to ask suggests that we need a fuller account of what he takes definition to be; we cannot properly evaluate claims that important concepts resist such definition until we have it.

Definition and analysis are, however, closely related, in a family whose other members include explication, description, classification, and what philosophers loosely call ‘making sense’ and ‘giving an account’. It might be that these last two convey the inclusive notion, with the others as different members. In carrying on what James described as ‘the dogged struggle to achieve clarity’ we are accordingly not without resource, even if restricted to these. We should therefore be untroubled to find that *strict* and *precise* definitions, of the kind respectively possible in formal contexts and the natural sciences, are not generally available in contexts outside these. Certainly, few if any of the concepts important to philosophy admit of that kind of definition; irrespective of the exact nature of Davidson’s understanding of definition, he is surely right about that.

But to say that such concepts cannot be *strictly* or *precisely* defined is not to say that they cannot be defined. The mistake arises from thinking that definitions must be definite. Think of the etymology of the term: to seek to define is to seek to find or – just as importantly – to draw limits, to mark boundaries, to feel the edges of application. Often we have to negotiate and renegotiate these. A fuzzy boundary does not fail to be a boundary because it is fuzzy; as we have seen, we would have a very impoverished stock of general concepts if that were so.


A surely unintended implication of Davidson’s remarks is that stating definitions (however conceived) and tracing conceptual connections exhaust the alternatives for philosophical method. But as suggested already, these are not mutually exclusive procedures. And apart from these – together with analysis and explication – there are a number of other characteristic vehicles of philosophy: for example, proof and argument, construction of theory, assembling reminders, persuasion, taxonomizing, criticism. It does not do to circumscribe, even by implication. So it seems that our ambition to get to grips with the important concepts of philosophy, not least among them truth – even to arrive at definitions of them in one of the many ways of definition – does not involve so much folly after all.

## Truth and Objectivity

What of the matter left hanging earlier, the question of *objectivity*, which the strategy of tracing conceptual connections seems not to provide? A feature of Davidson’s views – his ‘externalism’ – might be supposed to help here.

Davidson holds that language-users understand one another by being interpreters of one another’s utterances. Interpretation at its simplest is a mutual activity of two speakers who share experience of a portion of the world, and who hold each other’s beliefs about that portion of the world to be true (the interpretative principle that another’s beliefs are largely true is called the ‘Principle of Charity’). The two speakers, and the portion of the world available to both, form a triangle. The three-way relation underwriting mutual interpretation is called ‘triangulation’. It is this that might secure the objectivity that the Strawsonian strategy fails to provide.

We learn from Davidson’s views about triangulation that this essentially relational condition of interpretation is tied to the causal role of the world in giving beliefs their content. Events in the world cause beliefs, Davidson says, in a ‘fairly direct’ way by sensory stimulation; we have to connect beliefs with what they are about as regards their empirical content – truth-value and empirical content come from perception, or more precisely, the circumstances of perception.


So far, these remarks have a reassuringly familiar ring. But their tendency is not, it turns out, to give our beliefs extra-mental anchorage of the kind offered in traditional theories. Davidson’s talk of the ‘environment, the shared distal stimulation’ that plays a part in causing our beliefs is, first, not talk of what provides justification for them. Only beliefs can be evidence for beliefs; what gives rise to beliefs cannot. A dualism between our concepts and what they are of – their content – is rejected because there cannot be content by itself, and because it is not propositionally articulated, and therefore cannot do what empiricists want it to do, namely, provide warrant for the scheme (see chapter 8 below).⁶⁶ This rejects the empiricist claim that sensory awareness is the uniquely authoritative source of contingent knowledge.

Nor is the relation between the apex of the triangle in triangulation and its base angles to be understood as connected to a familiar set of various relations: perception and its objects, thought about things, truth and its makers, reference and singled-out bits of the world. Davidson rejects all these, or at least – in the case of reference – accepts only a severely deflated version, as conceptually toxic versions or by-products of the scheme-content dualism.⁶⁷

So we know what is not meant by talk of ‘the world’ in Davidson, and we note that it consorts well with a particular choice of emphasis. The objectivity of our concepts on what Davidson calls ‘the social or externalist view’ is a function of the mutuality of interpretation. In setting out this view Davidson gives the environment an error-or-divergence-adjusting role, but ‘nature does not speak to us’, it is not on its own a contributor to meaning. For meaning we must look to mutual interpretation, and interpretation is essentially social. Objectivity for Davidson is therefore intersubjectivity. And this is consistent both with the coherence flavour of much that Davidson says – ‘no point in looking outside sentences’ – and his advocacy of a Strawsonian-like strategy.

Despite having entitled a paper ‘A Coherence Theory of Truth and Knowledge’, Davidson dislikes the coherence label, and for the very reason identified above as a flaw in the Strawsonian strategy, namely, that it provides only internal justification for beliefs. The point can be put by saying that in addition to seeing connections between beliefs, we need a reason to think that most of them are true. And familiarly, instead of seeking an external anchorage to provide this assurance, Davidson thinks

that we have one in the Principle of Charity. To get our interpretations of others going, we must take it that most of their beliefs are true. So let us just do ourselves the same good turn, and take it that most of the beliefs in our own scheme are true. The principle is: ‘belief is in its nature veridical’. Here then is a further feature of the interpretational considerations that yield objectivity.

Two large objections suggest themselves. First, one is left feeling multiply dissatisfied with the claim that one can invoke ‘the world’ as playing a causal role in determining the content of beliefs, and that one can invoke ‘bits of the world’ to serve in a lean account of reference, while at the same time being told that these relations have nothing to do with questions of meaning and epistemic justification. Dissatisfaction is prompted when a notion of ‘the distal’, or ‘the environment of communication’, or just ‘the world’, is invoked to tidy the edges of a theory which has no substantive role for them, when one wishes to know – in relation to ‘the world’ or ‘the environment of communication’ – something about how the concepts of knowledge, truth and meaning engage with our interest in ‘the world’, by no means an intuitively misplaced concern. After all, we take language to range over an independently existing realm of spatio-temporal items, including events, and we wish to know – that is, to have a way of recognizing – which sentences about this realm are true, so that we can know what we can know: for we have severely practical interests at stake.

The dissatisfaction here is with Davidson’s seeming to have and eat several cakes at once. It is prompted, for example, by the opening paragraphs of ‘A Coherence Theory of Truth and Knowledge’, where he speaks of ‘meaning being given by objective truth conditions’ which can be satisfied (that is, by a thought-independent world), while yet it is absurd to speak of a confrontation between belief and reality. We can be realists and ‘can insist that knowledge is of an objective world independent of our thought and language’, but no sense attaches to talking about a scheme-content duality (a duality between thought and language, on the one hand, and an objective world on the other).⁶⁸

Secondly, Davidson’s way out of the coherence problem prompts questions. It rests on the claim that ‘coherent belief is in its nature veridical’.⁶⁹ But the history of science suggests that this claim is false, and that beyond its being an hypothesis with some utility in getting radical interpretation started, it is not an invariably good guide otherwise. For in understanding others, one often has to understand that what they are saying is false, or at least, that they hold certain beliefs true which we take to be false, perhaps for the reason that they are in error, or lying. These two points need to be taken together. The history of science teaches that the truth and the utility – within limits – of our beliefs do not invariably coincide, and historically have often been systematically divergent; and the point about falsehoods suggests that the false beliefs, ignorance, interests, or even malice of others can undermine our confidence in their reliability as truth-tellers, so that the interpretation of their discourse must surely make plenty of room for defeasibility. Taken together, we find that the Principle of Charity is questionable beyond its heuristic applications.


These dissatisfactions over objectivity prompt a direct challenge. Davidson urges the Strawsonian strategy, and commits himself to what we might for convenience call the coherence plus charity view (coherentism saved by the principle of the inherent veridicality of belief). He also says that the world plays a part in causing our beliefs. But then he also says that the world's causal activity with respect to us does not enter into the justification of our beliefs, and is not therefore the source of their objectivity – which, instead, is social. Meanings – reverting to the coherence mode – are functions of mutual interpretation. But the world contributes to the empirical content of our beliefs, and perceptual beliefs are basic to empirical knowledge.

These views do not seem to be consistent. If they are consistent, they have to be so on the grounds of the fine detail of their supporting argument.

## Truth and Evaluation

Here is the sketch of an argument to suggest that truth is neither deflatable nor indefinable, but instead consists in a family of cognitively significant notions. Among its side benefits this thesis gives us a diagnosis of why traditional theories of truth are unsatisfactory – but it also shows what is right about them. It shows further that Ramsay is right about truth in a certain respect; namely, that the important task is to state a theory of assertion. But successor conceptions of his redundancy account get no comfort here, for the thesis says that truth is not one insubstantial thing, but many substantial things, none of which is truth as attempts have traditionally been made to conceive it.

First one needs to note something about the way certain expressions function. Consider again the words *thing, do, nice*. ‘Thing’ does general duty for any noun, ‘do’ for any or at least many active verbs, ‘nice’ for any adjective of a generally positive purport. It might be illuminating to call each respectively a ‘substitute’ or ‘dummy’ noun/verb/adjective, because each marks places in sentences where more precise expressions go when the utterer is less hurried or lazy. In fact, with a nod towards ‘pronouns of laziness’ (because although they are not essentially anaphoric, they can have such uses) one might describe these expressions as ‘lazy’ to give an informative contrast with ‘busy expressions’ that do more precise and particular work.

Now for these purposes we need to introduce a notion of ‘lazy predicates’, to be understood as expressions marking a place in sentences for more precise property-denoting expressions. As with the lazy expressions just cited, the lazy predicate tell us something about the range and kind of the busier substitutes it takes: its use implies that whatever they are, use of them in predication implies observance of certain constraints, or at least the aspiration to realise certain desiderata. So the lazy expressions are not mere dummies. There are in fact quite a number of lazy predicates, and they play important roles in the economy of thought. Something more is said about this later. At this point the task is to use the notion of a lazy predicate to state the present thesis about truth, as follows.

The predicate ‘– is true’ is a lazy predicate. It holds a place for more precise predicates, denoting evaluatory properties appropriate to the discourse in which possession of those properties is valued. The properties are explicitly discourse-sensitive properties. As examples one might cite candidates from the history of related debates: verification in the case of discourse about the spatio-temporal realm; constructability in the case of a certain view about mathematics; and, say, universalizability in the case of ethical claims. These are merely examples of more specific properties; well-known debates about these candidates do not make one confident that they are the right ones; and to add to dissatisfaction with at least some of them one might suggest that, anyway, different subdiscourses are themselves likely to vary the evaluations (and associated evaluatory procedures) for which saying ‘– is true’ goes proxy. To see the point one need only think of the difference between talk of Quakers and talk of quarks, both in some sense referents in what we take to be an explanatorily-continuous domain. Indeed the situation is even more complex: how we evaluate perceptual claims, tensed claims, theoretical claims, claims about social objects (and much besides) is a highly various matter; yet in some sense such claims relate to a unified world of temporal and spatio-temporal things, so this is independent of the differences between such evaluations and those applicable to purely formal realms and – differently again – different value realms.


The thesis need not argue for any specific set of values and evaluatory procedures for given discourses. To do so would be for it to engage in the appropriate philosophical enquiry. The concern is more general: to find and state constraints on evaluations which reveal why the same lazy predicate ‘– is true’ collects them all.

So the view is that a theory of truth is (a) globally, a theory of evaluation, and (b) locally, a theory of subject-matter-specific evaluation for a discourse.

Evaluation is an epistemic matter in many cases, but not in all. The aesthetic case and aspects of the moral case are not so – and this observation is important, for the reason that since evaluation is about identifying and measuring value, it might be natural to think that there are fruitful comparisons to be drawn between busy substituends of ‘– is true’ on the one hand, and ‘– is good’ and ‘– is beautiful’ on the other. But the comparisons are not smooth, and this suggests that general constraints on evaluation will have to be understood disjunctively – some evaluations are constrained by one subset of constraints, others by others, and as usual one major interest lies in seeing whether the subsets share any common members.

## Constraints on Evaluation

The claim then is that the busy substituends of ‘– is true’ are predicates that denote evaluatory properties of such kinds as, or in appropriate cases better specified than, verification, constructability, universalizability (and so on for discourses not mentioned). As just noted, the task is not one of making out some particular local theory of evaluation, but to say something general about evaluation.

We wish to evaluate propositions, claims, beliefs, theories. I shall speak generally of evaluating propositions. What is it to evaluate – to assess the value of – something? Consider a sheepdog. We know what we need it for, and what we need it to be like; and if it answers our needs, and performs as required, we value it – and if it does not, we disvalue it qua sheepdog. We need it to herd sheep, not eat them or frighten them; so we require that it be docile and responsive to command, and to have the appropriate temperament. These are among the desiderata it has to satisfy, which can be summarized by saying that it has to be apt for the job we wish it to do. Now, as regards propositions we naturally wish them to be true, because then we can rely on them in inference, we can trust them to convey information about how things are, we can use them to test other claims, we can agree on them (at least eventually, as providing the stable points on which we can converge); and because they exercise rational authority over us and therefore provide tests for norms of rationality. Moreover, we are entitled to assert them, and they are typically far more useful than false ones.


Now compare this list of desiderata for truth with what we wish to say about evaluation. If, on the basis of evaluatory procedures appropriate to their domain, we are to attach ‘value’ (antonym: disvalue) to claims, what we mean is that we at least require them to be:

1. reliable in inference,

2. consistent with other propositions we value,

3. usable in evaluating other propositions,

4. agreement-inviting/promoting,

5. authoritative for us in the domain,

6. such as to entitle us to assert them,

7. such that acceptance of them is a norm for rationality,

8. such that they help us organize the subject-matter they concern more effectively – by appropriate and negotiated standards of effectiveness – than competitors.

This list has some overlaps with the list for truth, but is more inclusive. Neither list is non-redundant. Some items in both are restatements of one or more others. I list them in this way to bring out aspects of the desiderata. In both it may be that what occurs as 6 in the evaluation list – viz., assertability – is something which the others constitute, as the principal mark and chief point of value – including the case where value is taken to be unanalysed truth.

A valued proposition, by satisfying these desiderata, accordingly has these properties:

**`(a)`** Acceptability: it invites acceptance on grounds that involve negotiated ways of maximizing agreement on a triangulation of evidence, aims and context. This is not just 4; it is all of 1–7 in the list of desiderata.

(b) Adequacy: that is, fittingness or appropriateness for the task of meeting needs in that domain of concerns; 1, 5.

**`(c)`** Utility: it does the job of providing information, generating predictions, licensing inferences, settling disputes; 1, 3, 5.

(d) Stability: it forms part of a view (for the domain) which is cogent, stable, robust in tests and other demands upon it; 2, 6, 7; it is thus a ‘fact’ for the domain; 1, 5, 6.

Disvalued propositions are those that fail to have at least *`(a)`* and *`(c)`* because they fail to satisfy the desiderata (but note that 4 and 8 can – for a time – be failed by novel ideas). Disvalued propositions are rejected. In ordinary parlance we call them ‘false’ but even when we are using our lazy predicate ‘true’ it would be more correct to call them ‘not true’ to mark the fact that there are different ways in which they can fail to be true other than by being false (for example, by being meaningless, inappropriate to the domain, neither true nor false, and so forth).

We allow ourselves to talk of information being conveyed by true propositions. This is allied to the notion of fact, which is what true propositions are said to ‘correspond to’. The chief use of this resides in inference: having information enables one to get to further information. (It might also just be satisfying to know it.) On the evaluation theory there is no mention of information or facts; nevertheless we can say, regarding desiderata 1, 5, and 6, that a valued proposition is a fact in the sense that it has the property of standing firm for the domain.

Now the point is that if you take a subdomain of the spatio-temporal case, or a formal case, or an ethical or aesthetic case, the content of evaluations and the procedures involved in them will be specific to the subject-matter in hand. We can evaluate sheep-dogs and we can evaluate grand pianos, but although we can say general things about what we are looking for (not 1–8, for here we are evaluating things, not claims or theories), the specifics will differ. If we thought that there must be one thing that all evaluation consists in or results in, then we would find ourselves testing, say, to see whether Steinways bite sheep. (Although it is surely true of Steinways that they do not bite sheep, this cannot be what we want them for. Saying this is what is meant by denying that truth is a univocal concept.)


To say that ‘– is true’ is a dummy for ‘– is constructible’, ‘– is verifiable’, and so for other cases, is to say that there are, literally, different kinds of truth, individuated by subject-matter. Tarski, as noted, suspected that this might be so. And in line with his hint, this theory is consistent with the view that ‘truth’ in formal languages should anyway be considered quite separately; the idea being that talk of the *semantics* of a formal language is actually metaphorical, so that what is called ‘truth’ (or ‘constructibility’, say) is in fact a metalinguistic description of a syntactic property, such being the only kind of properties formal languages have.

But to say that there are literally different kinds of truth is not to make a relativist remark: the discussion here has nothing to do with such claims as that different points of view upon the same subject-matter can legitimately result in different distributions of truth-value across the propositions expressing it. That suspect claim is the subject of a different debate (see chapter 9).

So much is the merest sketch of a theory, but it offers resistance to the deflationary thought that it is a misconception to think that there is a property denoted by ‘truth’ with explanatory structure. This theory says that there are a number of such properties, which allow ‘– is true’ to serve lazily for them all because the global desiderata apply to them all in virtue of their epistemic role.

## Notes


#### Notes


1. A. Tarski, ‘The Concept of Truth in Formalised Languages’, in *Logic, Semantics, Metamathematics*, pp. 152–278; and (a very good introduction) Tarski, ‘The Semantic Conception of Truth’, in Feigl et al. *Readings in Philosophical Analysis*, pp. 52–84. I shall call these 1 and 2 respectively in references to follow.

2. Tarski, 2, p. 52.

3. Ibid., p. 53–4; 1, p. 155.

4. Aristotle, *Metaphysics*, 1011 b 26; a better translation than the one given earlier.

5. Tarski, 2, p. 54; cf. 1, p. 155.

6. Tarski, 1, pp. 157–65; 2, pp. 58–9.

7. Cf. Tarski, 2, p. 59.

8. Tarski, 2, p. 60; 1, pp. 162–5.

9 This informal presentation has closely followed Tarski's own in 2, p. 63.

10 A clear formal account of the notions of satisfaction by sequences and recursion is given by Quine, *Philosophy of Logic*, ch. 3, passim, esp. pp. 35–40, which precedes a discussion of Tarski p. 40 *et seq.*; see also Haack, *Philosophy of Logics*, pp. 106–8. My presentation follows hers.

11 Quine, *Philosophy of Logic*, pp. 40–2; Haack, *Philosophy of Logics*, pp. 108–9. Again I follow Haack.

12 Cf. Tarski, 1, p. 153; 2, p. 54.

13 Tarski, 2, pp. 70–4.

14 ‘Physicalism’ is the thesis that ‘1. all events are physical events, i.e., have physical descriptions, and 2. under their physical descriptions, all agents are susceptible to total explanation, of the kind paradigmatically afforded by physics, in terms of physical laws’. J. McDowell, ‘Physicalism and Denotation in Field on Tarski’, in M. Platts, (ed.), *Reference, Truth and Reality*, p. 128.

15 H. Field, ‘Tarski’s Theory of Truth’, *Journal of Philosophy*, lxix, 13, 1972, reprinted in Platts, *Reference, Truth and Reality*, pp. 83–110; cf. esp. Siii, pp. 91–4.

16 Tarski, 1, p. 406.

17 Ibid., and cf. 2, pp. 56–7.

18 Field, ‘Tarski’s Theory of Truth’. See esp. pp. 84–90, 94–103; and McDowell’s reply, ‘Physicalism and Denotation in Field on Tarski’.

19 K. Popper, *Conjectures and Refutations*, p. 223. See also Popper’s *Objective Knowledge*, p. 320.

20 Tarski, 1, p. 155, 2, pp. 53–4.

21 Popper, *Conjectures and Refutations*, p. 224.

22 S. Haack, ‘Is It True What They Say About Tarski?’ *Philosophy*, 51, 1976, p. 25.

23 Ibid. See also Haack’s *Philosophy of Logics*, p. 113.

24 Ibid.

25 Ibid., pp. 326–7.

26 Tarski, 1, p. 153.

27 Tarski, 2, p. 71. The critic was Gonseth, writing in the *Review Thomiste* xliv, 1938.

28 Ibid.

29 Ibid.

30 D. Davidson, ‘On the Very Idea of a Conceptual Scheme’, *Proceedings of the American Philosophical Association*, 1974; in *Inquiries into Truth and Interpretation*.

31 Popper, *Objective Knowledge*, p. 45.

32 F. P. Ramsey, ‘Facts and Propositions’, *Proceedings of the Aristotelian Society*, supp. vol., 1927; reprinted as excerpt in Pitcher, pp. 16–17.

33 Ibid., p. 16.

34 Ibid.

35 Ibid., p. 17.

36 Cf. chapter 4 above.

37 Cf. D. L. Grover, ‘Propositional Quantifiers’, *Journal of Philosophical Logic*, 1, 1973.

38 Cf. A. N. Prior, *The Objects of Thought*, p. 37f et seq.

39 Ibid., p. 37.

40 D. L. Grover, J. Camp and N. D. Belnap, ‘A Prosentential Theory of Truth’, *Philosophical Studies*, 27, 1973. See D. L. Grover, *A Prosentential Theory of Truth*, esp. pp. 3–45.

41 Haack, *Philosophy of Logics*, p. 133. For other discussions see B. Loar, ‘Ramsey’s Theory of Belief and Truth’, in D. H. Mellor, *Prospects for Pragmatism*, p. 49f et seq.

42 Paul Horwich, *Truth*, see esp. Ch. 1.

43 Ibid., p. 3.

44 Ibid., p. 5.

45 Ibid., p. 7.

46 Horwich, ‘Theories of Truth’ in J. Dancy and E. Sosa, *A Companion to Epistemology*, p. 513.

47 Ibid.

48 Quine, ‘Truth’ in *Quiddities*, p. 213, and see *The Pursuit of Truth*, passim.

49 Horwich, *Truth*.

50 Ibid., p. 2.

51 D. Davidson, ‘The Coherence Theory of Truth and Knowledge’ in Le Pore E. (ed.), *Truth and Interpretation*, p. 308.

52 Davidson, ‘The Folly of Trying to Define Truth’, *Journal of Philosophy*, vol. xciii, 1996, pp. 263–78.

53 Ibid., p. 263.

54 Ibid.

55 Ibid., p. 264.

56 Ibid., pp. 264–5.

57 Ibid.

58 Ibid.

59 Ibid.

60 See below.

61 See Davidson, ‘On the Very Idea of a Conceptual Scheme’ in *Inquiries into Truth and Interpretation*, and ‘The Myth of the Subjective’ in M. Kraus (ed.), *Relativism: Interpretation and Confrontation*.

62 But we can break the epistemic circle if we are serious about what transcendental arguments can deliver. Strawson himself does not think they can deliver enough; he accords them at most and at best a role in identifying orderings, not in giving objectivity or its closest approximation to our scheme. In my view transcendental arguments can indeed give this: see my *Refutation of Scepticism*, and related discussion in chapter 9 below.


63 See Russell in the *Lectures on Logical Atomism*.

64 Russell and Whitehead, *Principia Mathematica*, vol. i, p. 11.

65 See the remarks about truth as ‘lazy’ for evaluation, below.

66 Davidson, ‘On the Very Idea of a Conceptual Scheme’ in *Inquiries into Truth and Interpretation*.

67 See Davidson in any of ‘Reality without Reference’, ‘A Coherence Theory of Truth and Knowledge’, ‘The Content of Truth’, ‘The Folly of Trying to Define Truth’ in *Inquiries into Truth and Interpretation*.

68 ‘A Coherence Theory of Truth and Knowledge’ in *Inquiries into Truth and Interpretation*, p. 307, my italics.

69 Ibid., p. 309.