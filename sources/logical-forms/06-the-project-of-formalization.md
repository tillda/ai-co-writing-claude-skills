---
book: "Logical Forms"
title: "Chapter 06 The project of formalization"
chapter_number: "6"
chapter_name: "The project of formalization"
author: "Mark Sainsbury"
table_of_content: |
  1 Logical versus grammatical form
  2 Analysis and the Tractarian vision
  3 Proof
  4 Formal and structural validity
  5 Logical constancy
    Ex. 6.8 Propose suitable introduction and elimination rules for “=”.
    Ex. 6.9 Give a counterexample to EXISTS I as a rule for English.
    7) Hesperus is Phosphorus
  6 Language, form and structure
    4) Tom is married.
  7 Conclusion
  Bibliographical notes
    Notes
---

# 6 The project of formalization

## 1 Logical versus grammatical form

In chapter 1 I gave some preliminary motivations for studying validity through the medium of artificial languages. In subsequent chapters I presented some of these languages, indicating how they could be used to formalize arguments expressed in English, and in many cases illustrating detailed limitations. We now have to raise our heads from the trees, and try to discern the overall character of the wood.

The main subject of my discussion is the view that formalizing a sentence or argument of a natural language in one of the artificial languages we have discussed reveals something about the nature of the natural language, something that would otherwise be apt to remain hidden. It is this revelation which justifies the efforts we have expended in formalizing. Q has been especially favoured by proponents of this view, so it will occupy centre stage.

The revealed must look at least superficially different from the concealed, or there could be no revelation. Here are some apparent differences between natural language sentences and their formalizations.

1) Quantifiers: Some English universal (existential) quantifications not containing an occurrence of “if” (“and”) are formalized by a Q-sentence containing “→” (“&amp;”).

2) Adjectives: English adjectival modification is formalized by Q-conjunction.

3) Descriptions: An English sentence of the form “The F is G” is subject-predicate but its Q-formalization is an existential quantification, containing constants like “→” and “=” whose correlates are not visible in the English.


4) “Exists” is a predicate in English but must often be matched by a quantifier in a Q-formalization.

5) Numeral adjectives: An English sentence like “Three men are at the door” contains neither an existential quantifier nor the identity sign, but its Q-formalization contains “∃” and “=”.

6) Verbs of action: An English sentence like “John walks” is subject-predicate but its Q-formalization (on Davidson’s proposal) is an existential quantification.

7) Adverbs: Adverbial modification is (on Davidson’s proposal) formalized by Q-conjunction.

8) Propositional attitudes: An English sentence like “John believes that the earth is flat” is a single complex sentence, but its Q-formalization (on Davidson’s proposal) is two separate sentences.

9) Necessity: “Socrates is necessarily human” is in English a necessitated atom, whereas its QN-formalization is the necessitation of a conditional, containing the extraneous concept of existence.

10) Counterpart theory: “Socrates is necessarily human” is in English a necessitated atom, whereas its QC-formalization is a universally quantified conditional, containing the extraneous concept of a counterpart.

The confident classifications of English sentences (e.g. the assertion that an English sentence of the form “The F is G” is subject-predicate) are intended to reflect, not a theoretically grounded view, but some sort of “intuition”. The tradition I am describing has it that formalization shows many of our intuitive classifications of natural sentences to be incorrect: universal quantifications in English are shown, by formalization, to be “really” quantified conditionals, definite description sentences are shown to be “really” existential quantifications; and so on. These facts are concealed from the naive and untrained eye, which sees only “grammatical form”, but they are revealed by formalization, and these revelations are the project's main contribution to understanding natural language.


The thesis is sometimes expressed in the slogan: "Grammatical form misleads as to logical form" (cf. Strawson [1952], p. 51). The slogan may fail to capture the thesis. Using "logical form", as we are, to mean a sentence in some favoured artificial language, the truth of the slogan simply points up the existence of divergences like those noted in **`(1)-(10)`**. The thesis, however, requires the further point that the divergences are only superficial, for at bottom the natural sentences have the features that are so readily visible in their logical forms. The slogan does more justice to the thesis upon a different interpretation of "logical form", according to which the phrase signifies not a formalization into some possibly alien language, but the intrinsic logical and semantic properties of the sentence. The thesis is that a natural sentence's logical form in my sense reveals its logical form in this other sense.

In the rest of this section, I shall elaborate some more precise versions of the traditional thesis about logical form. First, however, I want to emphasize how strange the thesis should initially appear. Nothing about our own language seems clearer than that "All men are happy" does not contain an expression for conditionality, or that "Shem kicked Shaum" does not contain an existential quantifier. Could one mitigate the strangeness of the thesis by likening logical theory to scientific theory? Perhaps logic, like physics, needs idealizations, and perhaps the discrepancies we are discussing are the differences between the ideal and the messier real.

Suppose we are concerned with the motion of real billiard balls on a real billiard table. We may find it convenient to make simplifying assumptions: the table is completely flat and frictionless, the balls are perfectly elastic, there is zero resistance from air and baize, and so on. We can with justice say that we are still studying the original concrete phenomena through the idealization. Laws statable in terms of the idealization can be applied to the real balls to yield fairly accurate (if not perfect) predictions of their motions. We could at any point achieve greater accuracy by removing some of the simplifying assumptions. No doubt we would do this until the cost of the additional time taken to solve the equations exceeded the benefit of extra accuracy, a balance that would depend on idiosyncratic needs and interests. There would be nothing sacrosanct about any one idealization, and there would be absolutely no temptation whatsoever, on finding, for example, that the assumption of perfect elasticity yielded adequately accurate predictions, to infer that the real balls are "really" perfectly elastic. The approach builds in the acknowledgement that the idealization differs from the phenomena.


The phenomena for logical theory are arguments in a natural language, say English, and the theory should pick out their validity-relevant features. An idealization can properly abstract from other features, for example from the actual mechanisms whereby specific truth conditions are expressed. Regarded as idealizations, formalizations might not capture all the features of English, but they should enable one to give reasonably accurate predictions of the validity of English arguments. A divergence, for example a case in which an intuitively valid argument in English is formalized as invalid in some artificial language, may simply reflect, what we knew already, that the idealization does not exactly correspond to the phenomena. Alternatively, it may lead us to reconsider our intuitive judgement, though a divergence alone could never be a good reason to abandon such a judgement.

While one could not reasonably quarrel with this approach to validity in natural language, it is not one which yields the distinctive theses of the tradition I have in mind. The approach would not license the attribution to English sentences of all the features of the idealization. For example, to say that "All men are happy" is "really" a quantified conditional would be as ludicrous as saying that billiard balls are "really" perfectly elastic.

To understand the traditional conception of logical form, we need to distinguish variants. Let us start by making a very rough distinction, to be refined in §4, between logical features of a sentence or argument and semantic features. A prominent logical feature of a sentence would be its logical constants, and the pattern of occurrence of the non-logical expressions. Logical features would be those relevant to validity, or at least formal validity. Semantic features would include logical features, but would also include any other features pertaining to the meaning of the sentence and the words which compose it. We can distinguish two groups of theses about logical form: those which speak only to logic, and those which speak also to semantics. I shall begin by discussing a series of theses (*`(11)`*, *`(14)`* and *`(15)`*) which fall into the latter category.

11) The logical form (i.e. adequate and deep formalization) of a sentence of a natural language gives a representation of its truth conditions.

We imposed the following condition of adequacy upon formalization: a formalization is adequate iff the recovered sentence or argument agrees with the original in truth conditions; iff the truth-upon-an-intended-interpretation conditions of the formalization agree with the truth conditions of the original. This ensures the truth of *`(11)`*. Some of the most famous claims about the truth conditions of English sentences, like Russell's claim about the truth conditions of sentences containing definite descriptions, have arisen within the context of the project of formalization.

1) has no exotic consequences for the real logical nature of the language sentences. In general, two sentences may agree in truth conditions, but in other respects be quite unlike, for example the pair

.) Either snow is white or it is not

3) If snow is white it is white.

The identity of the truth conditions gives us no reason to say that (.) is "really" a conditional, or that *`(13)`* is "really" a disjunction. The fact that a natural sentence's logical form matches the sentence in point of truth (-upon-an-interpretation) conditions does not in itself show that there is any other interesting relation between the two. Sameness of truth conditions is symmetric. It accordingly gives as much reason for thinking that the arrow in a Q-formalization of an English quantification is not "really" there as for thinking that the English "really" contains an (invisible) "if".¹

The following strengthening of *`(11)`* would introduce an asymmetry:

14) The logical form of a sentence of a natural language gives a perspicuous representation of its truth conditions.


Perspicuity is normally defined as the co-incidence of syntax and semantics. To attain the definition, we need to define syntactic and semantic categories. Let us say that two expressions belong to the same syntactic category iff for every sentence containing one, the result of replacing it by the other is a meaningful sentence. In $\mathbf{Q}$, the syntactic categories include the following:

```txt
unary sentence connectives: ¬
binary sentence connectives: &amp;, ∨, → and ↔
name-letters
1-place predicate-letters
2-place predicates (=) and predicate-letters
3-place etc.
...
quantifiers: ∀, ∃
sentences (including sentence-letters)
```

Let us say that a semantic category is determined by the following test: expressions $e_1$ and $e_2$ belong to the same semantic category iff either they are assigned the same kind of entity by the interpretation rules, or else they are treated by the same kind of interpretation rule. In virtue of the first disjunct, all and only name-letters belong to one single semantic category, since they, and only they, are unrestrictedly assigned members of the domain; likewise all and only sentences belong to one single semantic category, since they, and only they, are invariably assigned truth values; likewise predicate-letters of any given degree, say, 3, belong to a single semantic category since they, and only they, are all assigned a set of triples of members of the domain. The second disjunct is intended to be read in such a way that all binary sentence connectives count as belonging to a single category, since they, and only they, are given rules of interpretation which fix a truth value for the resultant sentence on the basis of the truth values of two components. (We could have managed with just the first, more specific, disjunct in the definition had we required that an interpretation assign $n$-ary truth functions to each $n$-ary connective, and also made a suitable assignment of kinds of functional entity to the quantifiers.)

A language is perspicuous iff its semantic and syntactic categories coincide; that is, iff for any syntactic category there is a semantic one containing just the same things; and vice versa. $\mathbf{Q}$ comes out as perspicuous. This is not surprising: $\text{Q}$ was devised with perspicuity in mind; and my account of the semantics and syntax of $\text{Q}$ was guided by the wish that it should count as perspicuous. Otherwise, I might have counted a semantic category for each interpretation rule, corresponding to the thought that members of a semantic category have "the same kind of meaning", but this would have placed "$\&$ " and "$\lor$" in different semantic categories, even though they are in the same syntactic category. I could also have defined syntactic category differently, stipulating one syntactic category for each clause in the specification of a $\text{Q}$-sentence (4.1.6). This would have placed the sentence connectives in different syntactic categories, but would have eliminated the connection with the idea of a syntactic category as one fixed by substitution with preservation of meaningfulness. This, in turn, would have made it unclear whether we could apply the notion of syntactic category to English; or rather, would have made it unclear that we could apply it to English in the rather casual way characteristic of the logical form tradition, and in advance of having, for English, the analogue of the recursive specification of a $\text{Q}$-sentence.


An alleged example of the non-perspicuity of English is that names and quantifier phrases belong to the same syntactic category but different semantic categories. The semantic difference is fairly uncontroversial: the semantics for a name like "Carter" require it to refer to a particular man, but this is not so for a quantifier phrase like "no one". The sameness of syntactic category is harder to establish, as it requires looking at every possible context. True, both "Clinton is a bachelor" and "No one is a bachelor" (1.12.10 and 11) are meaningful, and the one results from the other by replacing a name by a quantifier phrase. But to establish that "Clinton" and "no one" belong to the same syntactic category, it would be necessary also to consider sentences like "No one ever complains" (cf. Ex. 1.30), "Clinton never complains", "No one with back ache complains" and many more (cf. Oliver [1999], pp. 253-4). These show decisively that names and quantifier phrases do not belong to the same syntactic category by the criterion under consideration.

Ex. 6.1 Refute by example the following claim:

"No one" is an exception. Other quantifier phrases do belong to the same syntactic category as names.

For a more promising example of sameness of syntactic category with difference of semantic category we might turn to names like "Carter" and definite descriptions like "The current US President". The semantic difference is, in the first instance, that "Carter" is semantically simple, whereas definite descriptions are semantically complex. If a view considered in chapter 4.12 is correct, the semantic differences are considerably more far-reaching, surfacing (in the apparatus of this book) as the suitability of names, but the unsuitability of descriptions, for formalization by a name-letter. Sameness of syntactic category may initially look more promising than with names and quantifier phrases, but in the end it, too, proves impossible to establish: "No Carter ever told a lie", but not "No the current US President ever told a lie", "The remarkable and talented Carter addressed the Senate", but not "The remarkable and talented the current US President addressed the Senate"; and many others (cf. Oliver [1999], pp. 253-4). One is forced to conclude that, at least on this account of syntactic category, the logical form tradition has been too quick to brand English as non-perspicuous.

The motivation for the branding is that perspicuity is connected with two features prized by logicians. One can fairly easily devise rules of proof for a language only if it is perspicuous; these rules, stated in terms of the physical make-up of sentences, would specify patterns of derivations of sentences from others in a way which mirrors validity. The other prized feature is that one can fairly easily devise rules of interpretation for a language only if it is perspicuous; these rules would apply to sentences specified in terms of their physical make-up, delivering for each a truth (-upon-an-interpretation) condition. For languages like Q we possess rules of both kinds; we do not possess comprehensive rules of either kind for English. Although it clearly does not follow that English is not perspicuous, the difficulty of devising such rules for English has, I suspect, encouraged this conclusion. In order to continue our exploration of the logical form tradition, we will need at least provisionally to accept the non-perspicuity of natural languages.

Ex. 6.2 Show why the non-perspicuity of English does not follow from the claims about the ease of devising rules. (You might find it helpful to formalize the premises, using “→”)

Given this provisional acceptance, thesis *`(14)`* specifies a relation which, unlike sameness of truth conditions, is not symmetric: a sen- tence of an artificial language like Q is a sentence of a perspicuous language, whereas its equivalent in a natural language is not. However, there is no inference from this to some more exotic thesis, expressible by such remarks as that English universal quantifications are really universally quantified conditionals. Given that English is not perspicuous, there must be some vital difference between the way in which an English sentence and its formalization present their truth conditions. Indeed, there would be something paradoxical in the assertion that those features of the artificial languages which make the formulation of rules of proof and interpretation relatively easy are really present in the English sentences, for which the formulation of such rules is hard or impossible.


We get closer to what many people have had in mind by the idea of logical form in the following strengthening of *`(14)`*:

15) The logical form of a sentence of a natural language gives a perspicuous and systematic representation of its truth conditions.

The notion of a systematic representation, which will be refined in §6 below, is linked to the notion of compositional semantics. The rough idea is as follows. The meaning of a sentence is determined by the meanings of the words of which it is composed, and by their manner of composition. Compositional semantics for a language will specify word meanings, and the semantic import of modes of composition, in such a way that, from these specifications, the meaning of any sentence in the language can be derived. As with meaning, so with truth conditions. Setting aside ambiguity, a word makes the same contribution to the truth conditions of any sentence in which it occurs, and a compositional semantics will specify this contribution. A systematic representation of truth conditions, alluded to in *`(15)`*, is a representation within the perspective of a compositional semantics. On this view, a sentence's logical form will contribute to an understanding of how the words in the sentence contribute systematically to the truth conditions of the whole.

Thesis *`(15)`* offers an important aspiration. However, it is at first sight hard to see how its achievement would be consistent with some of the specific classical claims about logical form. For example, on the face of it, one who aspires to give a systematic representation of the truth conditions of universal quantifications in English should not

pretend that such quantifications standardly contain an expression for conditionality.

I return to thesis *`(15)`* in §6. *`(15)`*, in common with its weaker predecessors, (11) and *`(14)`*, concerned semantic features. I now want to introduce two theses relating specifically to logical features:

16) If an argument in natural language is adequately formalizable as valid, then it is formally valid.

17) The formalization of a natural sentence renders the proposition it expresses accessible to formal deductive manipulations.

*`(16)`*, which I discuss more fully in §2, does not entail that the nature of the features responsible for formal validity is intrinsically characterized by the logical form. For example, the Q-validity of the formalization of, say, "All men are mortal, Socrates is a man, therefore Socrates is mortal" assures us, according to *`(16)`*, that the argument is formally valid, but gives us no assurance that it is valid in virtue of having a quantified conditional as its first premise. The English will have a formal feature corresponding to being a universally quantified conditional, but *`(16)`* makes no commitment to the intrinsic nature of that feature. Such a position requires that one have a standard of formal validity independent of formalization. This question is discussed in §5. The notion of deductive manipulation, required by *`(17)`*, is discussed in §3.

In the next section, I look briefly at a very ambitious version of the thesis of the revealingness of logical forms.

## 2 Analysis and the Tractarian vision

Russell toyed with the idea, and Wittgenstein embraced it in the Tractatus, that all validity is formal validity: indeed, is validity in virtue of Q-logical form. Contrary appearances are to be explained by the fact that our language is not fully analysed. Analysis would reveal all validity as formal. If we find a valid argument that apparently does not formalize as Q-valid, this shows that there is some defect in our formalization: we have not uncovered enough logical structure, we have not carried analysis far enough.

First, a historical correction. The language of logical forms that Russell had in mind was not $\mathbf{Q}$, but the richer language of *Principia Mathematica*. The language of logical forms that Wittgenstein had in mind was also not $\mathbf{Q}$, but a language that at least superficially seems less rich. The differences between them, and between them and $\mathbf{Q}$, had no impact either on the basis of the vision or on its subsequent rejection by both philosophers.²

Let us see how this *Tractarian vision* would view a very simple case. A standard example of a valid argument which is not formally valid is:

1) Tom is a bachelor, so Tom is unmarried.

One might suppose that the deepest $\mathbf{Q}$-formalization is:

2) $F\alpha; \neg G\alpha$

with "$\alpha$" corresponding to "Tom", "$F$" to "is a bachelor" and "$G$" to "is married". However, the *Tractarian view* has it that we have overlooked some hidden structure in the English. We can reveal it, and at the same time show *`(1)`* to be formally valid, by the formalization

3) $F\alpha \land \neg G\alpha; \neg G\alpha$

with correspondences as before except that "$F$" now corresponds to "is a man". The formalization depends upon the analysis of "is a bachelor" as "is a man and is not married".

*`(3)`* counts as an adequate formalization of (1) by the standards previously given, and nothing we have so far said gives grounds for objecting to it. These standards are consistent with intuitively more unacceptable proposals. In general, if an argument $A; C$ is valid, our current standard of adequacy counts as adequate a formalization "$p \land q; q$". For if $A$ entails $C$, then "$A$" and "$A \land C$" have the same truth conditions. In this sense it is trivial that all validity can be represented as formal validity, and the maxim of formalizing in such a way as to


maximize the amount of validity that can be represented might lead to no more than this trivial result.

Russell always had doubts about the possibility of representing all validity as formal, and although Wittgenstein explicitly affirmed the position in the *Tractatus*, he explicitly retracted it later. For both of them, the decisive factor was that the vision was unrealizable because there are valid arguments which no amount of analysis can represent as formally valid. They were both influenced by the case of colour incompatibilities. Thus the valid argument

4) This is red (all over), so it is not blue (all over)

cannot be represented as formally valid, however one analyses. One might try analysing “red” as “not yellow and not blue and not etc.” But first, it is doubtful whether the analysis can be brought to a conclusion, and secondly it would involve treating “yellow” etc. as primitive (not to be analysed) and a similar valid argument could be stated using just these primitives.³

Contemporary opinion would reject the Tractarian vision not just for this kind of reason, but also on the grounds that it fails to distinguish between a claim about logical form and a claim about analysis. Davidson, among others, has emphasized the distinction ([1967a], pp. 31 ff.; [1970a]). If it can be made good, it puts a curb on the Tractarian vision. Something like *`(3)`* would be said to be unsatisfactory as a logical form of *`(1)`* even if satisfactory as an analysis.

The distinction between analysis and form is quite intuitive. For example, a traditional “analysis of knowledge” might start off on lines such as these:

5) S knows that A iff

**`(i)`** A

**`(ii)`** S believes that A

**`(iii)`** . . .

The rule of the game is that you do not re-use the word “knows” in the numbered clauses after the “iff”. The clauses thus in some sense explain the meaning of "knows". This does not even begin to look like a claim about logical form. By contrast, Davidson's account of propositional attitudes rules that the logical form of "S knows that A" is


6) $F\alpha\beta, p$

(with "Fxy" corresponding to "x knows y", "α" to "S", "β" to "that" and "p" to "A"). This does not even begin to look like an analysis of knowledge. There is no attempt, in the logical form, to avoid the word "knows". Davidson's thought is that we must first get the logical form straight, leaving analysis as a separate issue.

Russell and Wittgenstein would not have been moved by this distinction. In the relevant period, both philosophers were primarily interested in thought or judgement rather than in language. For them, the structure revealed by logical form is the structure of thought, and this is what is so often hidden by natural language. Revealing the thought expressed by the premise of *`(1)`* as a conjunction is part and parcel of the very same enterprise as revealing the thought expressed by "All men are happy" as a quantified conditional. Once you become hardened to, or even rejoice in, the marked differences between the logical structure of thought and the grammatical structure of natural language, one sort of difference is likely to seem much like another. Language condenses complex structures in various ways: hiding the conjunction really present in the thought expressed by *`(1)`* is no different in kind from hiding the conditionality really present in the thought expressed by "All men are happy". In both cases, it is the job of "philosophical logic" to reveal what is hidden.

Davidson's own basis for the distinction between analysis and logical form depends upon considerations rather foreign to the discussion so far, considerations which will be introduced in §6 below. In the remainder of this section, I want to consider whether a well-grounded curb on the Tractarian vision can emerge from the kind of perspective we have adopted. In particular, the fact that *`(3)`* counts as adequate by our present standards may seem to constitute a criticism of these standards. The view for which I shall argue is that curbing the Tractarian vision on the basis of ideas we have already to hand is possible only by disqualifying, as inadequate, some standardly accepted Q-formalizations of English.

One way to motivate the distinction between logical form and analysis is to say that the logical form of a sentence should specify its logical constants, and the way in which they relate to the pattern of occurrence of the non-logical expressions. Analysis, by contrast, should concern the contribution to meaning of some expression, ideally providing a more complex equivalent expression built up out of unanalysable primitives. This simple-minded idea could be implemented by the following constraint upon formalizations:

7) A formalization is adequate only if each of its logical constants is matched by a single English expression making the same contribution to truth conditions.

On this view, formalization effects only notational changes, so far as the logical constants are concerned.

*`(7)`* corresponds to a deeply unambitious conception of logical form. The logical form of a sentence is given by how its logical constants occur, and the pattern of occurrence of the non-logical expressions. An artificial language would be just a convenient way of schematizing the non-logical expressions, rather as we did in chapter 1, and providing a usefully standardized notation for the logical constants. The idea of an artificial language would not essentially enter into the account of the nature of logical form.

Although *`(7)`* would rule that formalizations like *`(3)`* of (1) are inadequate, since they introduce constants (in this case “&amp;”) having no corresponding expression in the English, it would play havoc with traditional practice in formalization. English universal quantifications could not be formalized by universally quantified conditionals since that would involve importing a constant (“→”) to which there corresponded no English expression; similarly for English existential quantifications. Adjectival and adverbial modification could not be formalized by the conjunctive method. Necessitated atoms could not be formalized in QN. This narrow and unambitious view appears to be required, if one is to hold to the thesis (1.16):

If an argument in natural language is adequately formalizable as valid, then it is formally valid.

If such a thesis is not to be trivial, it requires a conception of formal validity that applies directly to English without any detour through formalizations. The only available conception is that already offered in chapter 1.10: an argument is formally valid iff its validity turns only upon the meanings of the logical constants it contains and upon the pattern of occurrence of the non-logical expressions. On this definition,


8) This is a red house, so this is a house

is not formally valid. Hence, by (1.16), it should not be adequately formalizable as valid, and the only way to secure this result would appear to be the adoption of *`(7)`*.

(7) is one way in which one could give a criterion for the difference between logical form and analysis, and thus limit the Tractarian dream. The motivation is coherent, but is far from doing justice to ambitious theses about logical form. Is there an alternative criterion?

We might prefer to think along the following lines. Logic, and thus formalization, must have no truck with non-logical expressions. These must be recognized as contributing only through the pattern of their occurrence, and not through their specific meaning. Hence a formalization should not, as *`(3)`* does, introduce a predicate-letter (in this case “F”) which, according to the correspondence scheme, corresponds to an expression (“is a man”) which does not occur in the sentence to be formalized. Let us call a generalization of this condition the “correspondence requirement”. It rules that if the correspondence scheme associated with a formalization has it that, say, “F” corresponds to “...” then that actual expression, “...”, must occur in the sentence of natural language which is formalized. This requirement is clearly not met by *`(3)`* relative to *`(1)`*: the correspondence scheme mentions “is a man”, which does not occur in *`(1)`*. Yet the requirement would seem more liberal than *`(7)`*, since it allows modes of composition in English to be represented as the application of Q-constants.

The correspondence requirement must be understood with some generosity if all its liberality is to be reaped. For example, the spirit of the requirement should allow the conjunctive formalization of adjectival modification. Yet in a standard Q-formalization of *`(8)`* as

9) $F\alpha \land G\alpha; G\alpha$

we find ourselves saying that “F” corresponds to “is red”, whereas that expression does not literally occur in the premise of *`(8)`*. While the difference is important for a detailed understanding of the work- ings of natural language, let us agree to interpret the correspondence requirement in such a way that such differences will not count.


With this rather vague liberalization, the correspondence requirement comes closer than (7) to the traditional view, in that it allows the standard formalizations of sentences containing, for example, adjectival modification and quantifiers. It rules out a few of the Q-formalizations proposed in this book, but there is in addition at least one major category of formalizations which it brings under suspicion: Davidson's treatment of verbs of action and some of their adverbs. Consider, for example, the formalization of

10) Shem kicked Shaum

as

11) $\exists x(Fx \land G \alpha x \land Hx\beta)$

with “F” corresponding to “is a kick”, “Gxy” to “x kicked y”, “Hxy” to “x was received by y”, “α” to “Shem” and “β” to “Shaum”. Perhaps our vague liberalization of the correspondence requirement allows that *`(10)`* contains something close enough to “is a kick” (viz. “kicked”), and also contains something close enough to “x kicked y” where the position marked by y is supposed to be occupied by an expression standing not for a person or a rock but for a kick. But the liberalization cannot allow that *`(10)`* contains an expression close enough to “was received by”. Either the tradition or else the correspondence requirement is at fault.

The correspondence requirement is clearly violated by QW and QC.⁴ On our current understanding of what is to count as a logical constant, furnished by the list in chapter 1.11, the predicates “W” and “C” of these languages are not logical constants. Hence they are non-logical expressions, yet the English expressions to which they correspond (“is a world”, “is a counterpart of . . . in . . .”) do not occur in the natural language sentences.


Ex. 6.3 Do QN-formalizations meet the correspondence requirement?

With the ideas currently to hand, I can find no way of curbing the Tractarian vision by providing a criterion for the distinction between logical form and analysis, except by stipulations which classify as incorrect some traditional logical form proposals. I believe that this shows that the ideas to hand are insufficient. To justify the kinds of logical form proposal one finds in the founders of the logical form tradition, Russell and Frege, one needs ideas, notably that of compositional semantics, that only came fully into view in the second part of the twentieth century.

## 3 Proof

A comprehensive grasp of the activities of the logician requires understanding the notion of proof. In addition to its intrinsic importance, and its connection with certain traditional aspirations in logic, it has a role to play in giving an account of what it is to be a logical constant.

I mentioned in chapter 1 that a traditional logical aspiration has been the mechanization of inference. Where there is disagreement about what follows from what, it would be good to feed premises and conclusion into a calculating engine, and wait for the computation of a verdict. Such an engine has to be fed sentences. It cannot be fed propositions, for these are too abstract. It is important that one express the argument in a language in which the validity-relevant features correspond conveniently to the physical make-up of the sentences, for it is to this physical make-up that, in the first instance, we can expect the machine to be sensitive. The mechanical aspiration thus provides a motivation for creating perspicuous artificial languages.

We saw in chapter 4.14 that this aspiration cannot be satisfied in full with respect to a language as rich as Q, for there is demonstrably no decision procedure for Q. This fact has added to the importance of the notion of proof. For it is demonstrably the case for Q that there are systems of proof in which, if an argument is valid, a proof will be found for it in a finite number of steps. This does not add up to a decision procedure because if following the system has not resulted in a proof of a certain conclusion after a million or ten million steps, you do not know whether this is because a few or a million more steps are needed or because the argument under test is invalid.


There are various different kinds of rules of proof, but I shall give a sketch of a system of natural deduction. A reader wanting to become proficient in using natural deduction must look elsewhere (for example to Lemmon [1965]), and one already proficient could skip to §4.

Confining our attention just to propositional logic, a standard system of natural deduction associates with each sentence connective two kinds of rules of proof: introduction rules, which specify from what premises one can derive a P-sentence dominated by the connective, and elimination rules, which specify what conclusions one can derive from premises containing a P-sentence dominated by the connective. The intuitive idea behind the introduction rule for "&" is that from a pair of sentences as premises you can infer their conjunction. For the elimination rule, the idea is that from a conjunction you can infer either conjunct. In setting out a full system, it is easiest to express these ideas in a slightly more complicated way. Using "$\Gamma$" and "$\Delta$" to stand for (possibly empty) sets of sentences, and a horizontal line to express that from what is above one can derive what is below, we write the rules as follows:

&E: if $$\frac{\Gamma}{X \land Y}$$ then $$\frac{\Gamma}{X}$$ and $$\frac{\Gamma}{Y}$$

and

&I: if $$\frac{\Gamma}{X}$$ and $$\frac{\Delta}{Y}$$ then $$\frac{\Gamma \cup \Delta}{X \land Y}$$.

(Here "$\cup$" represents set-theoretic union: $\Gamma \cup \Delta$ is the set of all the sentences belonging to $\Gamma$ or to $\Delta$.) The elimination rule, &E, tells you that if $X \land Y$ is derivable from $\Gamma$, then each conjunct is also derivable from $\Gamma$. The introduction rule, &I, tells you that if $X$ is derivable from $\Gamma$ and $Y$ from $\Delta$, then the conjunction can be derived from the premises obtained by adding $\Gamma$ to $\Delta$. "Derivable" in these contexts is not supposed to have any independent meaning. Rather, its meaning is to be fixed by the specification of the rules of proof for all the connectives.

For "$\neg$" the elimination rule is straightforward:

$\neg$E: if $$\frac{\Gamma}{\neg \neg X}$$ then $$\frac{\Gamma}{X}$$.

The introduction rule is based on reductio ad absurdum style argument, for example:

$\neg$I: if $$\frac{\Gamma, X}{Y \land \neg Y}$$ then $$\frac{\Gamma}{\neg X}$$.

This rule tells you that if you can derive a contradiction from a sentence $X$ together with zero or more other premises $\Gamma$, then you can derive $\neg X$ from $\Gamma$.

In addition to the rules for each connective, the system also requires general structural rules. All the rules mentioned so far are hypothetical. They tell you that if such-and-such is derivable, then so is something else. But unless there is at least one categorical rule, there will be no categorical facts of derivability. The categorical rule is

**`A`**: $$\frac{X}{X}$$

sometimes called, perhaps misleadingly, the rule of assumptions. The only way in which derivations can get going is by one or more applications of *`A`*.

To illustrate an application of these rules, let us adopt a standard convention. We will write sentences on numbered lines, the numbers enclosed in parentheses. To the left of the line number, we will indicate, by numbers, not enclosed in parentheses, the line number of "assumptions": sentences introduced into the proof by *`A`* and used as premises at some point, possibly remote, in the derivation of the sentence on the line. To the right we cite the rule to which appeal is made in writing the line:

1 (1) $p \land \neg p$ *`A`*

(2) $\neg (p \wedge \neg p)$ $\neg I$

In the application of ¬I on line (2), Γ has no members, and the instance of Y &amp; ¬Y is p &amp; ¬p. No number occurs to the left of “(2)”, since any number appearing there should refer to a member of Γ.

The system is completed by associating each connective with suitable introduction and elimination rules.

**Ex. 6.4 State suitable introduction and elimination rules for v, → and ↔.**

The motivation for the rules is to reflect valid patterns of reasoning, but in the statement of the rules there is no mention of validity, truth or any other “semantic” notion. Whether or not something is a correct application of a rule can be determined just by inspecting the shapes of the sentences. Mechanical testing can determine whether or not a rule has been correctly applied. The rules fix the extension of a relation of derivability, which can be written “ℍₚ”. Thus our little proof above established that

1) ℍₚ ¬(p &amp; ¬p),

in other words, that ¬(p &amp; ¬p) is derivable by the rules relating to P on the basis of no assumptions.

How is “ℍₚ” related to “ℍₚ”? We shall say that for a language, L, any system of rules of proof, π, for L, and any semantics, σ, for L, in terms of which validity is defined, π is complete with respect to σ iff

2) if Γℍ₀X then Γℍ₀X;

and that π is sound with respect to σ iff

3) if Γℍ₀X then Γℍ₀X.

There are standard systems of natural deduction which are both sound and complete with respect to the semantics we gave for P, so, using “ℍₚ” to relate to such a system,

4) ΓℍₚX iff ΓℍₚX.

In short, “$\vdash_{\mathbf{P}}$” and “$\vdash_{\mathbf{P}'}$” are equivalent, and there are rules for $\mathbf{Q}$ relative to which “$\vdash_{\mathbf{Q}}$” and “$\vdash_{\mathbf{Q}'}$” are also equivalent. For this result to have significance, it is obviously important that the two relations be defined in different ways. In the standard terminology, “$\vdash_{\mathbf{P}}$” is defined purely syntactically whereas “$\vdash_{\mathbf{P}'}$” is defined semantically.$^{5}$

A hypothesis is that there is no way of devising rules of proof for English that would come anywhere near being both sound and complete relative to our intuitive semantics. So if you want to be able to mechanize inference along the lines of rules of proof, it helps to transform English into some language for which there are rules of proof: Q would be an example of such a language. This hypothesis is, in effect, (1.17):

The formalization of a natural sentence renders the proposition it expresses accessible to formal deductive manipulations.

This claim can be understood in a way upon which it is true. However, it does nothing to establish an ambitious thesis according to which the semantic mechanisms of a formalization are the very ones at work in the natural sentence. By using a quantified conditional to express the proposition expressed in English by a quantification, you may be able to use rules of proof to prove some conclusion; but this does not begin to show that the English sentence is really itself a quantified conditional. It shows at most that it has the same truth (upon-an-intended-interpretation) conditions as such a conditional, but these truth conditions may be expressed by quite different mechanisms.

## 4 Formal and structural validity

A traditional view is that the logical form of a sentence shows how its primitive expressions are organized so as to engender its overall meaning: logical form displays semantic structure. One way in which this thought arises is as follows: formal validity is validity purely in virtue of structure, abstracted from content. However, Gareth Evans has argued, I think entirely convincingly, that it is possible to distinguish a coherent and important notion of validity in virtue of semantic structure (structural validity) which contrasts sharply with the traditional notion of formal validity. The main point of contrast is that formal validity turns on the specific contribution – the “content” – of the logical constants, whereas the conception Evans articulates is one in which validity depends upon no such specific contribution: the validity is purely structural.


Evans’s starting point is the notion of a categorial semantics: a semantic theory having a number of semantic categories, each primitive expression being assigned to just one category. Members of the same category are assigned the same kind of entity by the semantics. Thus an $n$-place predicate might be assigned a set of $n$-tuples; an $n$-place sentence connective an $n$-ary truth function (i.e. a function from $n$-tuples of truth values to a truth value); and so on. Roughly speaking, a structurally valid inference is one whose validity is independent of the particular assignments that are made within the semantic categories, but which is wholly dependent on the pattern of the categories in the argument. For example, it is arguable that

1) John is a large man, so John is man

is structurally valid. Imagine a categorial semantics which treats “John” as belonging to the category of names, marked by the fact that to each member of the category the semantics assigns a member of the domain; which treats “man” as belonging to the category of 1-place predicates, marked by the fact that to each member of the category the semantics assigns a set of members of the domain; and which treats “large” as belonging to the category of extensional adjectives, marked by the fact that to each member of the category the semantics assigns a function from a set (the set associated with the one-place predicate to which the adjective applies) to a subset of that set. Relative to this semantics, (1) is structurally valid, since any argument whose premise consists of a name followed by an extensional adjective followed by a one-place predicate, and whose conclusion consists of that name followed by that one-place predicate, is valid. The validity of (1) is thus

due to its semantic structure: due only to the semantic categories to which its elements belong, and not to the special contribution the elements make within their categories.

If there were no restrictions on the categorial semantics, then any inference whatsoever would count as structurally valid (relative to some semantics or other). For example, we might subdivide the category of one-place predicates into three as follows: (a) those to each of which the set of all and only bachelors is assigned; (b) those to each of which the set of all and only unmarried persons is assigned; (c) those to which any other set of objects is assigned. In the light of this categorization

2) Tom is a bachelor, so Tom is unmarried

is structurally valid, since any argument whose premise consists of a name followed by an (a)-type one-place predicate and whose conclusion consists of that name followed by a (b)-type one-place predicate is valid.

Evans places the followed constraint upon categorial semantics:

> *We will construct a new category out of an older and more comprehensive category only when we can make an assignment to members of the new category which provides a different explanation for the behaviour which members of the new category had in common with the old, the provision of which explanation would show that the apparent unity in the behaviour of members of the old category was deceptive, concealing deep differences in functioning. ([1976], p. 64)*

A semantics which makes the envisaged threefold division among one-place predicates will not meet this constraint. By contrast, here is a putative case in which a division would be justified. Imagine a language containing both names and definite descriptions of the form "the so-and-so", and a semantic theory which lumps them into the single category of "singular terms". The theory assigns members of the domain to some (perhaps all) names and some (perhaps all) definite descriptions. Some inferential behaviour is common to singular terms. For example, there is a valid pattern of inference from a premise applying to a singular term a predicate, $F$, to a conclusion which says that there is at least one $F$. Now imagine a new semantic theory which proposes a division of the category of terms, separating names from descriptions, treating names as before, and associating with “the” a function from pairs of sets to truth values: the function takes the value true iff the first set in the pair has a unique member and that member belongs to the second. The new semantic theory gives a new explanation of the inferential behaviour common to singular terms. In the case mentioned, there are two explanations, one for the case in which the premise contains a name, patterned on the explanation provided by the old theory, and another for the case in which the premise contains a definite description. In the second case, the explanation alludes to two assignments, that to “the” and that to “$F$”, whereas the old theory alluded to a single assignment to “the $F$”. This surely satisfies Evans’s condition that the new theory’s division of the category of singular terms shows “that the apparent unity in the behaviour of members of the old category was deceptive, concealing deep differences in functioning”.


In our earlier listing of the semantic categories of $\mathbf{Q}$, the 2-place connectives were bundled into a single category, and this categorization is justified by Evans’s test. The only inferential behaviour common to all of them is the substitution of equivalents, which can be represented in the following scheme:

3) For any 2-place connective, $\xi$, any interpretation, $i$, if $i(Y) = i(Z)$ then $i(X \xi Y) = i(X \xi Z)$ and $i(Y \xi X) = i(Z \xi X)$.

Specification of the different truth functions expressed by the three 2-place sentence connectives of $\mathbf{Q}$ gives no new explanation of this common behaviour. The explanation still resides simply in the fact that the connectives express some truth function or other. No further subdivision of the semantic category of 2-place connectives is justified. Hence an argument of the form

4) $p \land q; p,$

while it may count as formally valid, does not count as structurally valid. The relevant structure is:

5) sentence₁ sentence connective sentence₂ sentence₃

But not all instances of this structure, permuting just within the specified categories, are valid; for example:

6) $p \vee q; p.$

The notion of a structurally valid argument corresponds to the idea that there are some arguments which are valid, not in virtue of the specific meanings of their expressions, but rather in virtue of the way in which the sentences are constructed. Though formal validity is sometimes thought to answer to this intuitive idea, it does not, for formal validity is validity partly in virtue of the specific meanings of certain favoured expressions, the logical constants, and if this idea is to have importance there has to be a deep reason for selecting some expressions rather than others as the logical constants.

On Evans’s view, a sentence’s semantic structure will be represented by a sequence of categories. A Q-formalization will not constitute such a representation. If you looked to Q-logical form to give answers about semantic structure you would, arguably, get wrong answers. You would infer that English quantifiers are unary, whereas the evidence is that they are binary. You would infer that English universal generalizations contain an expression belonging to the category of two-place sentence connectives, whereas they do not. You would infer that adjectives belong to the same category as predicates, being associated with a set of sequences, whereas the category they really belong to is of expressions assigned functions from sets to subsets.

Instances of adjectival detachment (for example (2.8): This is a red house, so this is a house) and instances of explicit conjunction elimination (on the pattern of *`(4)`*) both suggest patterns of validity. Evans’s insight is that the pattern of adjectival detachment abstracts from the meaning of any specific expression, whereas the pattern of conjunction elimination essentially involves a sign for conjunction.

If the draconian standard of (2.7) is adhered to, whereby each Q-constant must be matched by an English expression, there is a good sense in which a formalization reveals the logical structure of the natural sentence. It shows how the English sentence is structured around the logical constants it contains: what those constants are, and how the non-logical expressions contribute to truth conditions. The same is not true of the more relaxed standard provided by the correspondence requirement. (For example, the requirement permits the formalization of adjectival modification by conjunction, whereas there may be no expression for conjunction in such an English idiom.) None the less one can see how people might be led into thinking that formalizations meeting this requirement speak to the question of logical structure. Given, finally, that logical structure might well be confused with semantic structure one can see how the view that logical form reveals semantic structure found space within the traditional conception of logical form. Crudely put, the progression goes as follows: formalization singles out the logical constants of English and the way in which the non-logical material is organized by the constants; thus formalization identifies logical structure, the mechanisms whereby expressions contribute to truth conditions; thus logical form identifies semantic structure. The starting point is not secured by traditional practice in formalization, and the steps are unjustified.


## 5 Logical constancy

One goal we attributed to the logician is the characterization not merely of validity, but also of formal validity. A formally valid argument is one valid just in virtue of the meanings of the logical constants it contains and the pattern of occurrence of the other expressions. An account of the goal of logic thus essentially involves an account of what it is to be a logical constant. Once we have that, we will be able to specify the border between logic and other disciplines. A language fit for logic will have no constants other than logical constants. A sentence will be logically true iff it is true in virtue of the meanings of the logical constants it contains together with the pattern of occurrence of non-logical expressions. Logical necessity is necessity owed to the meanings of the logical constants, and to the meanings of no other expressions.

Within a formal language like $\mathbf{Q}$, it is simply stipulated which are the logical constants: they are the expressions which receive a constant interpretation. However, there is no limit to what expressions could be accorded a constant interpretation. For example, one could introduce a Q-like language with the additional stipulation that some symbol was, upon every interpretation, to be assigned the set of cats. The present section asks what principles underlie our sense that the symbol thus treated in that language as a logical constant is not really one.

In chapter 1 we gave a list of the logical constants, mentioning that this does not even hint at a rationale for grouping the listed expressions together. I quite cavalierly ignored the original list in chapter 5, in order to investigate the logic of modality.

We will consider four accounts of what makes an expression a logical constant. We will find that there is a large measure of convergence between them. The first, briefly mentioned in chapter 1.11, is that the logical constants are topic-neutral: they can be distinguished by the fact that they introduce no special subject matter. Thus "if" and "some" are intuitively not "about" anything at all, whereas a name like "Ronald Reagan" is about Reagan, and "happy" is about happiness.

The view is encouraged by the thought that logic concerns reasoning in general. It should therefore give special attention just to those expressions which can be used in reasoning on any subject matter whatsoever, and this may suggest that the logical constants should not introduce any specific subject matter.

If standard views about what expressions are logical constants are correct, the topic-neutral account as so far formulated does not give a sufficient condition for an expression to be a logical constant. Take a world like "therefore", which can certainly be used in connection with reasoning on any subject whatsoever, and is as topic-neutral as any expression one can think of. Yet orthodoxy does not include it among the logical constants. "Therefore" is normally used not as part of an argument, but rather to indicate what the conclusion of the argument is. Since it is not part of the argument, it cannot contribute to its validity. If we think of an argument in an abstract way, as a collection of sentences one of which is the conclusion, its validity is independent of whether anyone has ever "indicated" which sentence is the conclusion. Since logical constants should certainly contribute to the validity of arguments, "therefore" should not count as a logical constant, despite its topic-neutrality.

Ex. 6.5 Discuss the following suggestion:

"⊢" is a logical symbol and represents "therefore", so the latter is, in effect, counted as among the logical constants.

This suggests how the topic-neutral theory should be reformulated. A logical constant is an expression whose meaning contributes to the validity of arguments and which introduces no special subject matter. With this amendment, the main problem is the vagueness of the notion of topic-neutrality, which leaves unsettled, concerning some expressions, whether they are logical constants or not. One example is "but", not normally accounted a logical constant. My earlier suggestion was that it makes the same contribution to validity as "and", since it expresses the same truth function, while "A but B" suggests that in the context of A it is surprising, poignant, or worthy of special note or emphasis, that B is true. Does this additional component in the meaning of "but" constitute the introduction of a specific subject matter (surprise, poignancy or special notice)? The topic-neutral theory delivers no answer, whereas traditionally, and intuitively, "but" does not count as a logical constant.


The vagueness of the topic-neutral theory is conspicuous in the case of a traditional logic constant, “=”. On the one hand, this perhaps ought not to count as topic-neutral, for it might seem that identity is a specific topic, not involved in all reasoning. On the other hand, perhaps it ought to count as topic-neutral, for no specific objects are introduced when we introduce “=”. The second idea seems to point in a helpful direction, but we cannot rest content with it as it stands, for it could as well be said that identity introduces every object, since every object is related by it to something.

A possible approach is to refine the notion of "introducing objects" in terms of understanding conditions. Perhaps there are no objects, and no kind of object, knowledge of which is required to understand “=”. Arguably, there are objects, or a kind of object, knowledge of which is required to understand a non-logical constant like “cat”.

This criterion would arguably count "necessarily" as a logical constant, for even if a philosophical account of the notion introduces worlds, it would appear that knowing about these is not essential to a grasp of the adverb. By contrast, the criterion would exclude the constants "W", "w*" and "C" of QW and QC respectively, since there are objects, worlds and counterparts, which one must know about to understand these expressions.

The criterion would exclude the set-theoretic expression “∈” (for “is a member of”), since in order to understand this expression one has to know about sets. However, it would remain a matter for dispute whether or not the criterion counted second order logic as logic; whether, that is, it counted second order quantifiers as logical constants. On the one hand, arguably it does not, since these quantifiers have a

special subject matter, properties or sets, and one needs to know about these to understand the quantifiers. On the other hand, the criterion must obviously be so understood as to count first order quantifiers as topic-neutral, which means that the fact that their range is confined to objects in the domain must not count against their neutrality. However this is achieved, it might have the result that the fact that the range of a second order quantifier is (for example) confined to subsets from the domain should also not be a mark of non-neutrality.

Although topic-neutrality corresponds to an intuitive strand in traditional thinking about the logical constants, it is hard to make the idea precise. We will therefore turn to other criteria.

Ex. 6.6 Consider a sentence operator: "It was the case that . . .". Does this count as a logical constant by the topic-neutral criterion? Are there any other reasons for judging the issue either way?

The second criterion to be considered, the rules criterion, focuses in a different way upon the role of the logical constants in reasoning. The claim is that a logical constant is an expression whose meaning can be wholly specified by rules of proof, rules stating what you can validly infer from a sentence dominated by it, and from what you can validly infer a sentence dominated by it.

Various constraints can be appropriately imposed on the rules exploited by the rules criterion.⁶ Those for a target expression must not mention any other expressions in the language. Without this restriction, the door would be open to counting a large number of expressions as logical constants which intuitively are not. For example, I might otherwise claim that "ruish" has a meaning wholly fixed by the following introduction rule and pair of elimination rules:

$$
\text{RUISH I: if } \frac{\Gamma}{x \text{ is Jewish and } x \text{ is Russian}} \text{ then } \frac{\Gamma}{x \text{ is ruish}}.
$$

$$
\text{RUISH E (i): if } \frac{\Gamma}{x \text{ is ruish}} \text{ then } \frac{\Gamma}{x \text{ is Russian}}.
$$

$$
\text{RUISH E (ii): if } \frac{\Gamma}{x \text{ is ruish}} \text{ then } \frac{\Gamma}{x \text{ is Jewish}}.
$$


The justification for excluding such rules is that the target expression is supposed to sustain the validity of the reasoning all by itself. If other expressions were mentioned in the rules, there would be a suspicion that these were responsible for some of the validity-relevant features.

A further appropriate restriction is that introduction rules should not contain any occurrences of the target expression in the conditions for the introduction. This would exclude the introduction rule for “¬” given earlier:

if $\frac{\Gamma, X}{Y \land \neg Y}$ then $\frac{\Gamma}{\neg X}$.

The justification is that it should not be assumed that there is some way justifiably to get the expression into the language other than through the introduction rule; for if there were, that other way could be relevant to the meaning of the target expression. This means that, in order to count “¬” as a logical constant by the rules criterion, one needs to specify some arbitrary falsehood, say “2 + 2 = 5”, perhaps abbreviated “⊥”, and give the introduction rule as:

if $\frac{\Gamma, X}{\perp}$ then $\frac{\Gamma}{\neg X}$.

On plausible assumptions, the rules criterion determines that the English truth functional sentence connectives are logical constants. The assumptions are that rules for “and” just like those given for “&amp;” enable the derivation only of valid arguments, and that the meaning of “and” is fixed by the fact that a conjunction is true iff both conjuncts are. The validity of the elimination rule ensures that the truth of a conjunction is sufficient for the truth of each conjunct, and the validity of the introduction rule ensures that the truth of each conjunct is sufficient for the truth of their conjunction.

Although exactly the same rules would be valid for the binary connective “... and 2 + 2 = 4 and ...”, we need not fear that the latter will wrongly be counted a logical constant, for it is not plausible to say that its meaning is fixed by the rule that “A and 2 + 2 = 4 and B is true iff A is true and B is true”: a component of the meaning is left undetermined.

This sort of example poses a different problem for rules theory. Consider the connective “$\xi$”, where “$A \notin B$” expresses the denial of the disjunction of “not-$A$” and “not-$B$” (cf. Peacocke [1987]). The rules of “and”-introduction and elimination are valid for $\xi$, yet it is plausible to hold that although “$\xi$” expresses the same truth function as “and”, the two expressions differ in meaning. Someone could sincerely accept “$A$ and $B$” and sincerely deny “$A \notin B$”; this is some evidence that they believe that $A$ and $B$ and do not believe that $A \notin B$, which in turn is some evidence that the sentences differ in meaning. If so, one would have to confess that the rules criterion does not rule “and” a logical constant, since its meaning is not fixed by the validity of the rules, since the validity of the rules does not distinguish between the meaning of “and” and the meaning of “$\xi$”.

If we replace “meaning” by “truth conditions” in the rules criterion, we would be returned to the difficulty that “$\ldots$ and $2 + 2 = 4$ and $\ldots$” would counterintuitively be accounted a logical constant.

Intuitively the meaning of “$\xi$” is more detailed or specific than the meaning of “and”. This suggests amending the rules criterion as follows: an expression is a logical constant iff its meaning is the least specific meaning which validates the introduction and elimination rules. The problem now is that “$\xi$” will not be a logical constant, either relative to the rules for “and” or to any others, since to assign it the less specific meaning of “and” will validate any rules which it would validate, yet will not assign it the correct meaning. This problem can be overcome by distinguishing between primitive and defined constants. The category of primitive logical constants is as determined by the amended rules criterion. The category of logical constants is the closure of this category under definition.

Ex. 6.7 (a) How does the rules criterion treat “but”?

**`(b)`** Could there be a logical constant that was primitive in the sense of being typically learned directly, and not via a definition, and yet which had the meaning of “$\xi$”?

We have tried applying the rules criterion to English expressions. Now let us check whether it delivers the right results for our formal languages. The $\mathbf{P}$-validity of the rules for “\&” entails that every interpretation upon which a conjunction is true is one upon which each conjunct is true; and every interpretation upon which each conjunct

is true is one upon which their conjunction is true. To recover the actual interpretation rules for “&amp;”, we need to add the assumption that every sentence not true upon an interpretation is false upon that interpretation.

Similar considerations, upon similar assumptions, substantiate the claims of the other truth functional sentence connectives, in English and in P, to be logical constants.

Quantifier elimination and introduction rules for Q would take the form:

$$
\forall E: \frac{\forall v X}{X_v^n}
$$

where $X_v^n$ results from $X$ by replacing one or more occurrences of $v$ by $n$.

$$
\forall I: \text{if } \frac{\Gamma}{X_v^n} \text{ then } \frac{\Gamma}{\forall v X} \text{ provided that } n \text{ does not occur in } \Gamma.
$$

The validity of $\forall E$ ensures that any interpretation upon which “$\forall v X$” is true is one upon which “$X_v^n$” is true, regardless of what the interpretation assigns to “$n$”. Since each interpretation assigns just one thing to each name-letter, this enables us to infer the stronger: any interpretation upon which “$\forall v X$” is true one such that “$X_v^n$” is true upon it and upon any $n$-variant interpretation. The correctness of $\forall I$ ensures that if “$X_v^n$” is true on some bunch of interpretations which include every possible assignment to “$n$” then “$\forall v X$” is true upon any member of the bunch. Thus the interpretation rules for $\forall$ are recoverable from the validity of the rules of proof.

It would not be easy to apply similar reasoning to English. For one thing, although one can see roughly what sort of rules should correspond to $\forall E$ and $\forall I$, it is unclear how they should be couched in detail. It would also be unclear whether the least specific meaning verifying these rules would be the meaning of “all” or “every”. For example, an important type of reasoning involving “all”-sentences, inductive reasoning from instances of a generalization to the generalization itself, might be argued to be partially constitutive of the meaning of “all”, and it is not obvious whether this part would be captured by rules of ��all” elimination and introduction. It might be better

to argue indirectly: if “all” matches $\forall$ in meaning, and the latter is a logical constant, then so is the former.

### Ex. 6.8 Propose suitable introduction and elimination rules for “=”.

(See Tennant [1978], p. 77.)

What does the rules criterion exclude from the category of the constants? Name-letters and predicate-letters are not even candidates for constancy, since they have no fixed interpretation. Likewise, names in English could not be constants, since there appear to be no valid rules special to any name.

The case of predicates is more delicate, since the classical view is that the English predicates “is the same as” and “exists” should count as logical constants, in view of their formalizability by the Q-constants “$=$” and “$\exists$”. On anti-Meinongian assumptions, the rule

$$
\text{EXISTS I: if } \frac{\Gamma}{\ldots n \ldots} \text{ then } \frac{\Gamma}{n \text{ exists}}
$$

is valid for extensional parts of English, and it would be plausible to argue that the least specific meaning assignable to “exists” which would validate it is its actual meaning. The significance of this is diminished by the fact that EXISTS I is not in general valid in English. There is a valid rule for Q corresponding to EXISTS I, so that one would expect an existential predicate to be a (non-primitive) logical constant of Q, as indeed it is: “$\exists x(x = \ldots)$”. Rather similar remarks apply with respect to identity. The non-extensionality of English means that there is no generally valid elimination rule, whereas the extensionality of Q means that there is such a rule.

### Ex. 6.9 Give a counterexample to EXISTS I as a rule for English.

This means that the rules criterion turns out to have an implicit relativity to a language. We must say either that “is the same as” and “=” do not mean the same, or else that of two expressions with the same meaning, it may be that one is a logical constant (in its language) while the other is not (in its language).

Though the topic-neutral criterion counts “$\square$” among the logical constants, this ruling has been disputed, so it would be useful if it could

be confirmed by an alternative criterion. The elimination rule appropriate to PN is obvious:

$$
\square \mathrm{E}: \quad \text{if} \quad \frac{\Gamma}{\square X} \quad \text{then} \quad \frac{\Gamma}{X}.
$$

Validating this rule (by the standards of PN-validity) requires that for all worlds $w$ and interpretations $i$, if $\square X$ is true at $w$ upon $i$, then $X$ is true at $w$ upon $i$. By itself, this does not entail any significant feature of the interpretation rule for $\square$. For example, it is consistent with $\square$ having a much less specific meaning than it actually has, for example being a "null" operator, with the interpretation rule:

$\square X$ is true at $w$ upon $i$ iff $X$ is true at $w$ upon $i$.

If the rules criterion is going to count “$\square$” as a logical constant, everything must turn upon the introduction rules.

One possible such rule is:

$$
\square \mathrm{I}(i) \quad \text{if} \quad \frac{\Gamma}{X}, \quad \text{and every member of } \Gamma \text{ has } \square \text{ as its main connective, then } \frac{\Gamma}{\square X}.
$$

If this connection holds for PN-validity, then if for all interpretations $i$ and all worlds $w$ such that all the $\Gamma$ are true at $w$ upon $i$, $X$ is true at $w$ upon $i$, then for all interpretations $i$ and all worlds $w$ such that all the $\Gamma$ are true at $w$ upon $i$, $\square X$ is true at $w$ upon $i$. The standard interpretation rule will verify this conditional (given the assumption about the composition of $\Gamma$) but it is hard to see whether this is the least specific meaning that will do so. One cannot derive “$\diamond X \to \square \diamond X$” from $\square \mathrm{I}(i)$, so this rule does not determine the meaning “$\square$” possesses in PN.⁷

The following rather similar rule, but with a less demanding restriction upon $\Gamma$,


$$\square \mathrm{I}(ii) \quad \text{if} \quad \frac{\Gamma}{X}, \quad \text{and every sentence-letter in every member of } \Gamma \text{ is within the scope of some occurrence of “}\square\text{”, then } \frac{\Gamma}{\square X},$$

permits the derivation of just the arguments that are PN-valid. This is some evidence that it, together with the elimination rule, fixes the interpretation rules for “☐”; but it is not decisive, since these interpretation rules may attribute more meaning than is needed for the validities.

Though not conclusive, the rules criterion adds some support to the case for the constanthood of “☐”. However, it would appear to give no encouragement to the constanthood of “W”, “at”, “w*” or “C”. So far as I know, no one has attempted to formulate elimination and introduction rules for these expressions, and I have no idea how such an attempt would begin. This is an odd result, given that what is expressible in QN is expressible in QW and QC. The criterion has some other counterintuitive features.

First, as it stands, the theory does not provide a sufficient condition for constancy. Let us stipulate that the meaning of the two-place sentence connective, “*”, is to be fixed by the two rules:

$$*\mathrm{I} \quad \frac{X}{X * Y}$$

$$*\mathrm{E} \quad \frac{X * Y}{Y}$$

The rules together ensure that we can correctly infer any sentence from any sentence (by first using the introduction rule for “*”, then the elimination rule), and no expression can have a meaning which legitimates that. Hence the fact that one can state introduction and elimination rules for an expression does not even ensure that the expression has a coherent meaning, let alone that it is a logical constant.

Ex. 6.10 Show why no expression can have a meaning such that *I and *E are both valid, making explicit any assumptions upon which you need to rely. Cf. Prior [1960].

The argument shows that one who would introduce his constants by rules should place further restrictions on the nature of the rules. A commonly suggested restriction, which would suffice to rule out the combination of *E* and *I*, is this (cf. Belnap [1962]). Suppose we have a set, σ, of rules, one pair of which relates to a constant, ϕ. Now imagine removing the ϕ-rules from σ, and call the diminished result σ′. The proposed restriction is that σ′ should permit all the derivations not involving ϕ that σ permits. That a set containing just * does not satisfy this restriction is shown by the fact that the derivation of Y from X (neither containing *), which is available in the presence of *, is unavailable in its absence. With this restriction, “*” gives no reason to think that an expression could meet the rules criterion without being, intuitively, a logical constant. The doubt is not whether the account rules in too much, but whether it rules in enough.

It looks as if the meaning of “few” could not be fixed by elimination and introduction rules; and, depending upon the other expressive resources of the language, the same might go for “most”. But “few” and “most” would appear, intuitively, to have as much right to count as logical constants as “all” and “some”, and this intuition is supported by the topic-neutral criterion. To exclude them is to show that one is willing to count as a logical constant only what yields the sorts of results in which one is interested, and this suggests that there is no objective borderline between the constants and other expressions.

The third criterion for constancy derives from Davidson [1973] and from Dummett [1981]. It is motivated by the thought that the logical constants are the expressions which act as “cement” in the construction of longer sentences out of the bricks of the symbols of the language; I shall call it the “cement criterion”. Davidson has implemented this idea by saying that a logical constant is an expression which, in a semantic theory for a language containing it, receives a recursive rather than a basis clause. In the kind of semantic framework we have used, a basis clause is the specification of what an interpretation may or must assign to an expression (an object from the domain, a set of n-tuples, or whatever). The recursive clauses are the “interpretation rules”. Their effect is to transform the question of the truth-upon-an-interpretation conditions for a sentence into questions about the truth-upon-an-interpretation conditions for its parts. A part may contain a further occurrence of the expression treated by the rule of interpretation, so that that rule, and also perhaps others, may have to be reapplied before the question of the truth-upon-an-interpretation conditions is resolved. The final resolution is purely in terms of the basis clauses. Looking at it from the bottom up, rather than the top down, once the assignments of the basis clauses are fixed, so is the truth upon the interpretation of every sentence in the language.


The criterion excludes “$=$”, since this receives a basis clause. This is not a decisive refutation of the cement theory, since we cannot assume that our original list of logical constants is well motivated. More seriously, the cement theory will include as constants expressions which clearly are not, for example “large” (cf. Evans [1976], p. 69). In terms of our semantic framework, we can find a rule which, rather than assigning something outright to “large”, as a basis clause does, makes what is assigned depend systematically upon the assignments effected by the basis clauses. For example, one could introduce “large” into $\mathbf{Q}$ by the syntactic rule that attaching it to a 1-place predicate (or predicate-letter) forms a new 1-place predicate, and the semantic rule that an interpretation which assigns a given set, $\sigma$, to a 1-place predicate, $\phi$, must assign the subset of large members of $\sigma$ to “large $\phi$”. Just as assignments to the sentence-letters of $\mathbf{P}$ thereby determine the truth values of all $\mathbf{P}$-sentences in virtue of the recursive rules for the sentence connectives, so the assignments to the “large”-free predicates and predicate-letters thereby determine the assignments to all the predicates and predicate-letters in virtue of the recursive rule for “large”.

Ex. 6.11 Some logics have a constant to express falsehood, or some arbitrary absurdity: “⊥” is often used. Do you think “⊥” would receive a basis or a recursive clause? What does your answer show about the appropriateness of defining logical constants as just those which receive recursive clauses?

Though the cement theory must be rejected, one can see how holding it makes it hard to find use for a distinction between logical structure and semantic structure. Semantic structure might be thought of as the way a sentence is built up out of its parts. On the cement theory, this structure is supposed to be given by the logical constants.

The fourth criterion is due to Peacocke [1973]. I shall call it the “apriori” criterion. Consider this property of truth functional sentence connectives: if you know what truth values an interpretation has assigned to the components of a sentence dominated by a truth functional sentence connective, and you know the interpretation rule for the connective, then you can work out apriori what truth value the interpretation accords to the resultant. Perhaps some generalization of this property will constitute a distinctive feature of the logical constants.


In the semantic framework we have adopted, an interpretation assigns a truth value to every sentence of the language (relative to a domain, and perhaps also relative to a world – but we will omit these qualifications). It does so in the following way: it makes outright assignments of entities to the sentence-letters, name-letters and predicate-letters. The operators, that is, the sentence connectives and quantifiers, are not themselves assigned anything, but each is associated with a clause specifying a condition upon which a sentence dominated by the operator would be assigned the value true. The outright assignments are the basis clauses, the assignments upon a condition the recursive clauses. We can say that an outright assignment “treats” the expression to which the assignment is made, and that a recursive clause “treats” the expression which dominates the type of sentence which the clause addresses.

The version I shall consider of Peacocke’s formulation of the generalization (adapted to our semantics and terminology) is:

1) $\alpha$ is a logical constant iff $\alpha$ is non-complex and, for any expressions $\beta_{1}, \ldots, \beta_{n}$ on which $\alpha$ operates to form the expression $\alpha(\beta_{1}, \dots, \beta_{n})$, knowledge of what each interpretation assigns to each $\beta_{i}$, together with knowledge of how $\alpha$ is treated, enables one to infer apriori what each interpretation assigns to $\alpha(\beta_{1}, \dots, \beta_{n})$.

This excludes the case in which some $\beta_{i}$ or $\alpha(\beta_{1}, \ldots, \beta_{n})$ is an operator (and so not assigned anything upon an interpretation). This has no practical importance, and could be avoided without damaging the spirit of the proposal.

*`(1)`* clearly rules that truth-functional sentence connectives are constants. Also it excludes, for example, predicate-letters. We can apply the test to “$F\gamma$”, where we think of this as corresponding to “$\alpha(\beta)$” in *`(1)`* (so that “$F$” takes the place of “$\alpha$” and “$\gamma$” of “$\beta_1$”). Suppose you know what each interpretation assigns to “$\gamma$”, and so you know in particular that, for some specific interpretation, $i$, $i(\gamma)$ is Ronald Reagan. Suppose you also know how the unary predicate-letter “$F$” is treated (each interpretation assigns it a set), and you know in particular that $i(F)$ is the set of honest men. You cannot infer apriori what truth value $i$ assigns to “$F\gamma$”, because nothing in what you know about $i$’s assignment to “$\gamma$” and treatment of “$F$” contains any information about Reagan’s honesty. So a predicate-letter fails the test for being a logical constant, which is as it should be.


(1) does not count Q-quantifiers among the constants. One reason is the trivial one that, given the semantics we have adopted, the truth-upon-an-interpretation condition of a quantification depends not upon how the interpretation treats any component, but rather upon how certain interpretations treat a sentence related in a certain way to the contained open sentence. I shall ignore this problem: let us assume, to assist the discussion, that we are dealing with a semantics in which interpretations assign objects to variables. Then it might seem as if (1) does count the quantifiers as constants. For suppose you know what each interpretation assigns to “$Fx$” (truth or falsehood, as the case may be), and you know the interpretation rule for “$\forall$”, then it may seem that you can come to know apriori what each interpretation assigns “$\forall xFx$”. For you know that an interpretation, $i$, assigns truth to this sentence just on condition that all interpretations agreeing with $i$ on their assignment to “$F$” assign truth to “$Fx$”.

However, knowledge of what $i$ assigns to “$\forall xFx$” cannot be extracted apriori from the knowledge we have supposed. One might not know that all the interpretations whose assignments to “$Fx$” one knew about are all the interpretations there are. Moreover, there is an unclarity about what it is to know what something, for example a predicate-letter, is assigned. Suppose that $i_1$ assigns the set of featherless bipeds to “$F$” and $i_2$ assigns to this letter the set of men. It is not an apriori matter whether they agree on their assignment to “$F$”. You might know that “$Fx$” is true upon both $i_1$ and $i_2$, but because you do not know that these interpretations agree on their assignment to “$F$”, you might not realize that $i_2$ is one of the interpretations relevant to the truth upon $i_1$ of the universal quantification. To deal with this problem, Peacocke ([1973], pp. 226–7) in effect stipulates that included in the knowledge which is to be the basis for the apriori inference is this: for any letter, $L$, any pair of interpretations, if the interpretations agree on what they assign to $L$, you know that they do.

As Peacocke stresses, this does not entail that, for any pair of letters, if an interpretation assigns the same thing to each, you know that it does. For this reason, identity does not, as the criterion stands, count as a logical constant. Suppose you know that an interpretation assigns Hesperus to “$\alpha$” and Phosphorus to ��$\beta$”, and you also know that, like every interpretation, it assigns to “$=$” the set of ordered pairs whose first member is the same as the second. You cannot work out apriori whether or not “$\alpha = \beta$” is true upon the interpretation. You need in addition the non-apriori information whether or not Hesperus is identical to Phosphorus.

This limitation, like the previous one relating to quantification, could be stipulated away, but then one would begin to wonder whether such stipulations have any rationale other than that of endorsing a predetermined list of constants, a list drawn up on the basis of some criterion other than (1). Why not add “is the same height as” to the list, by stipulating that the knower has access to the relevant information? It would seem that the way to argue for the rejection of such a suggestion is not from within the criterion (1), but from the independent intuition that information pertaining to heights must be irrelevant to logic. Again, “☐” can be included among the constants, if we are prepared to add the following to the available information: with respect to which worlds the interpretations make the sentences of the language true, and, for each world, what each interpretation assigns to each letter with respect to that world. But the question arises whether or not we should be willing to suppose this information to be available.

It would, of course, be pleasing to have a way of giving our intuitions about constancy a precise technical embodiment, and this may well be provided by Peacocke’s account, but it seems that it will not serve to underwrite these intuitions. Doubts about whether “$\Box$” or even “$=$” is a constant would not be resolved by the criterion.

To summarize this part of the discussion, it is not clear whether it is possible to make a marked improvement on the first of the criteria – the topic-neutral one. It does not give definite rulings on certain cases, but perhaps this is simply because the concept of logical constancy is vague. The cement criterion seemed to be on the wrong lines, but the other three criteria showed some encouraging convergence. The indeterminacy in the rules theory related to the question whether the rules-determined meaning was really the least specific that would sustain the validities; and there were problems concerning whether it

introduced a language-relative notion of constancy. The apriori criterion did not conflict with the topic-neutral criterion, but, rather, appeared to rely upon it when it came to crucial decisions about the formulation of the criterion.

The boundary to the class of logical constants determines the boundary to the class of logical truths: truths true solely in virtue of the meaning of the logical constants, together with the pattern of occurrence of non-logical expressions. This in turn provides a boundary to the domain of logic: it could be identified with the class of logical truths.

Let us use "C" to refer to the claim that a truth is a logical truth iff it is true just in virtue of the meanings of the logical constants and the pattern of occurrence of other expressions. C has come under attack by Quine [1963]. In Quine's work one finds attacks on at least the following five claims which might be held to be consequences of C:

2) Logical truths are true by convention.

3) Logical truths are true independently of how the world is.

4) "The truths of logic have no content over and above the meanings they confer on the logical vocabulary" (ibid., p. 109).

5) A truth of logic "is a sentence which, given the language, automatically becomes true" (ibid., p. 108).

6) Logical truths are "true by virtue purely of the intended meanings . . . of the logical words" (ibid., p. 110).

The assertion of (2) is not part of the intention of the adherent of C, and I will ignore the question of whether it is a consequence of C. (It may seem to be, on the assumption that meanings are conventional.) C is certainly not intended to entail (3), and (4) is, on the face of it, false. As Quine remarks, the truth of “ $\forall x (x = x)$ ” depends not just on words but on the world, on the fact that everything is self-identical. So we should understand C as saying that to the extent that meaning contributes to the truth of a logical truth it is only the meaning of the logical constants and the pattern of occurrence of the non-logical expressions that are relevant. (4) is foreign to the approach of this book, in which no assumptions are made about how the logical vocabulary

of English gets its meaning, and according to which, if anything confers meaning on the Q-logical vocabulary, it is the interpretation rules of the metalanguage and not the logical truths of the object language. *`(5)`* and *`(6)`*, as recently qualified so as not to exclude a contribution to truth "from the world", are indeed consequences of criterion C.

Quine's argument against these last two theses, the only ones to which C is clearly committed, stems from a quite general scepticism about meaning. Certainly, if there is no such coherent concept as meaning there is no coherent doctrine of truth in virtue of meaning. It would take us too far afield to discuss this general scepticism, so I will simply turn aside from it.

On one interpretation, to say that a sentence is logically necessary is just to say that it is logically true. This requires amplification. If truths like

### 7) Hesperus is Phosphorus

are necessary, then there is a kind of necessity that it is not logical necessity, in the sense just defined, while also not being merely physical, epistemic or moral necessity, or necessity which is a restriction of logical necessity (in the sense of logical truth). *`(7)`* exemplifies the kind of necessity that Plantinga refers to as "broadly logical" necessity and which Kripke, for example, has called "metaphysical necessity". By contrast, the logical necessity that equates with logical truth is termed by Plantinga "narrowly logical" necessity. Not all broadly logical necessities, like *`(7)`*, are knowable apriori. So if logic is to fulfil its promise of being an apriori subject, it should study and use only a narrower notion. This means that our original definition of validity in chapter 1.3 should be understood as employing a narrower notion.

## 6 Language, form and structure

The sentences of the artificial languages I have discussed have a strange feature upon which I have not explicitly remarked: for the most part they do not say anything, and cannot be characterized as true or false. The reason is that the letters, sentence-letters, name-letters and predicate-letters, have no fixed interpretation. They are empty vessels, waiting to be filled; the fillings are interpretations. Thus a Q-sentence

like “∃xFx” does not say anything, nor is it true or false. Rather, it awaits an interpretation. Relative to an interpretation which, say, assigns the set of dogs to “F”, the sentence says that there are dogs, and is true. In Q there is no truth (or saying) *simpliciter*, but only truth (or saying) upon an interpretation.

We could have proceeded differently, introducing Q-symbols like “F” and “α” as abbreviations of specified expressions in a natural language, for example “is a dog” and “Fido”. Let us call such a language Q*. It will have the same definitions of interpretation and validity as Q, but its non-logical symbols will be thought of as (non-logical) constants for which just one interpretation is correct, and this interpretation, call it *i***, will be specified. For Q*-sentences, truth equates with truth upon *i***.

This alternative procedure makes Q* a real language, one whose sentences all say something, and are all true or false. For the purposes so far discussed, it makes little difference whether one formalizes in Q or in Q*. For this section we need to focus on Q*. The suggestion I want to discuss is that we can use semantics for Q* to give a compositional semantics for natural language. In more detail, the suggestion is that in devising a semantics for English, we proceed in two stages:

1) First, English sentences will be translated into Q*.

2) Secondly, the semantic resources discussed in connection with Q will be applied to the sentences of Q*; the English expression “true” will be regarded as abbreviating “true upon *i**”.

The second step assigns intuitively correct truth (that is, truth-upon-*i***) conditions to the Q*-sentences, on the basis of the contributions systematically made by their parts. The first step ensures that none but correct truth conditions get assigned to English sentences which have Q*-translations. Let us call a two-tiered theory of this kind a *proxy semantics*. In the version given above, English semantics are given by proxy of Q*, which can be called the *proxy language*.

Something like this idea may well have been influential for some time, for example in Russell’s early work, but it is only rather recently that a version of it has been explicitly formulated. Donald Davidson has proposed that English should be given proxy semantics. He uses

Q* as an example of a suitable proxy language, while explicitly denying any commitment to the view that this is the only possible proxy language. He does not favour the type of semantic theory we have introduced, in which symbols are assigned entities of various kinds, preferring instead a “truth theory”. I will not attempt to describe what this is, but will note that a truth theory recognizes exactly the same semantic categories as the semantics presented here, and, like our semantics, it provides truth conditions for every sentence on the basis of the elements from which it is constructed, and it is because of the perspicuity of Q* that it is quite easy to produce a truth theory for it.

The essentially Davidsonian project of proxy semantics specified by (1) and (2) provides a definition of logical form in the spirit of (1.15):

3) The logical form of a sentence is the sentence of the proxy language into which it needs to be translated in order to provide its semantics.

(Cf. Davidson [1977], esp. p. 203.) This gives the project of formalization an importance of a new kind. Formalization would not merely help to characterize validity, or formal validity, for a natural language, but, more widely, would help to give a general characterization of meaning, or at least truth conditions, for natural language. (3) would vindicate the view that logical forms provide insight into the semantic mechanisms of natural language.

On Davidson’s view, logical form is essentially relative to a proxy language. Relative to a propositional language, the logical form of an English universal quantification will just be “p”. This tells us very little about the semantics of the English sentence. For example, it would be absurd to infer that the English quantification is “really” unstructured. Some constraints must be placed upon the choice of proxy language.

Intuitively, we want to say that an appropriate proxy language will mirror the structure of the natural language. It would be a pity to make this into a criterion of adequacy for a proxy language, for we wish to allow logical form proposals to provide a conduit for discoveries about the semantic structure of natural languages. For example, Davidson has proposed that a sentence like “Shem kicked Shaum” should be matched with an existential quantification in the proxy language, and it would defeat such a purpose to protest, on the basis of some pretheoretical “intuition” to the effect that the English sentence is atomic and not a generalization, that this proposal does violence to semantic structure.


The intuitive idea which, according to Davidson, should guide us is that semantics, including proxy semantics, should provide an answer to the question: "What are these familiar words doing here?" If we ask this of "Shem kicked Shaum", the answer given by Davidson's proposed Q*-translation would be that "Shem" and "Shaum" serve to refer to objects, that "kicked" introduces kicks, and that the sentence as a whole introduces existential quantification. (I follow Davidson in ignoring tense.)

One more precise test of the adequacy of proxy semantics upon which Davidson insists is that if an English argument is, intuitively, formally valid, its translation in the proxy language should be formally valid. For example, an important component in his argument for his logical form proposal for action sentences is that the Q*-translation (or Q-formalization) of "Shem kicked Shaum in the face, so Shem kicked Shaum" is Q-valid. This places significant limitations upon what could be an adequate proxy language for English. For example, it rules out the adequacy of a propositional language.

Ex. 6.12 Could the same effect be achieved by requiring that the translation procedure envisaged in (6.1) be statable in a finite number of rules? Could this requirement rule out the claim that an English quantification has a sentence-letter as its logical form?

A further Davidsonian adequacy condition upon semantic theory is that the theory have only finitely many axioms. This forces a semantic theory to recognize some structure in the object language. Languages typically have infinitely many sentences, so a finitely axiomatized semantic theory can deliver a correct assignment of truth conditions to every sentence only by seeing sentences as made up of parts drawn from a finite total stock, each part making a distinctive contribution to the truth conditions of whatever sentence may contain it. Applied to proxy semantics, this means that there must be a finite manual for translating English into the proxy language, and a finitely axiomatized semantic theory for the latter. Let us call this the finite axiomatization constraint.

The idea of proxy semantics enables one to make good sense of some extreme-sounding claims about logical form, for example, the

claim that "Shem kicked Shaum" is "really" an existential quantification. The claim amounts to no more than that such a sentence will be translated into an existential quantification for the purposes of proxy semantics. Likewise the claim that "All men are happy" is "really" a quantified conditional amounts to no more than that such a sentence will be translated into a quantified conditional for the purposes of proxy semantics. This is more ambitious than the claim that, say, an English quantification and its $Q^{\star}$-rendering are alike in truth conditions, for it makes the further claim that their likeness in this respect is of a special kind, engendered by a single scheme of translation; yet it is suitably less ambitious than the absurd claim that an English quantification contains an invisible occurrence of "if" or "$\rightarrow$".

Some puzzlement may remain. Consider two logical form proposals for English quantifications: one made by standard $Q^{\star}$-translations, the other by translations into a language containing binary quantifiers. Both proposals might meet all of Davidson's criteria, yet we are intuitively inclined to believe that they cannot both be right, cannot both be true to the semantic structure of English. Intuition clearly sides with treating English quantifiers as binary rather than unary. It seems perfectly possible that a natural language sentence should have a David-sonian logical form, and yet exploit different mechanisms to achieve the same truth conditions from the same non-logical primitives. Hence it seems possible that a proxy semantics meeting Davidson's constraints should give an incorrect account of semantic structure.

The root of the puzzlement is that whereas Davidson's notion of logical form is relative to a proxy language, we tend to suppose that there is an absolute fact about the semantic mechanisms a sentence exploits.

We saw that the choice of a suitable proxy language is crucial to the value of Davidson's conception of a proxy semantics. Intuitively, we want to say that the proxy language must mirror English in point of semantic structure. We should not make this a condition of correctness, or else the project of proxy semantics will be unable to contribute to our understanding of what the semantic structure of English is. Davidson's finite axiomatization constraint is an attempt to require proxy semantics to recognize semantic structure, without explicit allusion to this notion. However, it fails in this aim: even if it forces the recognition of some structure, it does not guarantee recognition of the right structure. For example, it does not prevent a proxy semantics, adequate by Davidson's standards, from regarding "Socrates is wise" as a conjunction, since the requirement of finite axiomatization would not be flouted by a finite translation manual with the rule that an English atom of the form "$x$ is wise" be translated into $Q^{\star}$ by something of the form "$Wise\ x \land (2 + 2 = 4)$". Moreover, it would not give a basis for choosing between proxies with binary quantifiers and proxies with unary quantifiers.


When we speak of the "right" semantic structure, or of the "intuition" that English quantifiers are binary, to what standard are we appealing? An extreme Davidsonian might argue that there is no intelligible standard beyond what emerges from the project of proxy semantics. To object that, for example, it is "counterintuitive" to regard "kicked" as a 3-place predicate is to invite the response that the intuition is worthless. Semantic classifications have no role other than to assist in the specification of truth conditions of all the sentences of a language on the basis of the contributions of subsentential expressions. If this is provided by a theory which regards "kicked" as 3-place, there is no room for a standard relative to which this is the wrong semantic classification.

Davidson at one point suggested ([1967a], p. 25) that semantic structure mirrors the structure of our ability to speak and understand a language. This suggests that an appropriate standard is psychological: semantic structure should reveal the features which one who understands a sentence exploits in coming to understand it. One cannot tell apriori what these features are, though certain "intuitions", for example, that English quantifications are not all quantified conditionals, constitute our unsubstantiated hunches. These need to be tested empirically, since we know that introspection is not always a reliable guide to our mental processes. Empirical data for such views could be obtained in a number of ways, of which the following is an extreme example. Suppose we found that severing a certain nerve in the brain had the effect of making a person incapable of understanding explicit conditionals, sentences like "if John is a man, then he is happy". Suppose that this same person continued to understand quantifications like "All men are happy". This would be evidence that the semantic structure of English quantifications is not that suggested by their Q-formalizations.


The criterion of psychological correctness provides a basis for preferring one rather than another of two logical form proposals which meet all the other criteria. It sets a standard for semantic structure that is not relative to a proxy language, and harmonizes well with the tradition. For example, Russell on more than one occasion said, concerning a logical form proposal, that it gave a better picture of what was going on in the mind of a person using or understanding a sentence (e.g. [1912], p. 29). This would be assured, if logical form mirrors actual processing mechanisms. This makes logical form the form of thought as well as the form of language.


The various constraints on logical form, regarded as a proxy in $Q^{\star}$ designed to serve the purposes of proxy semantics, are that: 
(i) the logical form should coincide in truth conditions with the English sentence; 
(ii) semantics and translation manual should be finitely axiomatized; 
(iii) English arguments we intuitively count as formally valid should correspond to $Q$-valid proxy arguments; and 
**`(iv)`** the semantics for $Q^{\star}$ should in some way reflect the processing mechanisms speakers of English actually employ. One ought to be cautious in supposing that, by these standards, English sentences have unique logical forms.

For some English sentences, there is room for doubt whether there is even one logical form meeting all these conditions. We have already registered the thought that one who understands an English quantification like "All men are happy" may not need to bring to bear an understanding of the conditional, so that the $Q^{\star}$-formalization may not meet all the envisaged constraints. Various other constructions raise the same worry, for example:

### 4) Tom is married.

This needs to be $Q^{\star}$-formalized as an existential quantification, so as to represent the argument "Tom is married to Susan, so Tom is married" as formally valid. Yet it is very much an open question whether speakers invoke their understanding of the existential quantifier in understanding *`(4)`*, so the fourth constraint, (iv) of the preceding paragraph, may not be met. One reason this problem arises is that $Q$-predicates are of fixed degrees (unary, binary or whatever) whereas arguably there are English predicates of variable degree, like "are compatriots", which seems to make a sentence however many names (separated by "and") we put in front of it. This kind of problem may show not a problem with the general methodology, but an inadequacy of

Q*. Future work may deliver languages as perspicuous as Q* but with predicates of variable degree.

One should be cautious in supposing that Q* is uniquely well suited to be the proxy language. Russell’s theory of descriptions seems much less likely to meet criterion (iv) (mirroring processing mechanisms) than one which treats definite descriptions by proxy languages closer in form to English: either those which treat “the” as a binary quantifier (e.g. Neale [1990]) or those which treat it as a singular term (e.g. Burge [1974]).

The proxy language approach to logical form takes for granted that it must be possible to provide compositional semantics for English, but this assumption can be disputed. It is based on the idea that we come to understand sentences in virtue of our understanding of the meanings of their parts. While this may be true in some sense, there is room for doubt whether the meanings of the parts entail the meaning of the whole. Perhaps we often understand sentences by guesswork and probabilistic reasoning, so that there is no clear demarcation between our specifically linguistic competence and our general cognitive abilities. For example, it would appear that no correct assignment of semantic properties to “carpet”, “vacuum”, “sweeper” and “cleaner” entails that a carpet sweeper is something to sweep carpets with, whereas a vacuum cleaner is not for cleaning vacuums. Yet speakers of English have no trouble picking up the use of these compounds once they understand their constituents. Another example is the use of demonstratives, with respect to which general knowledge about what objects are likely to be conspicuous for speakers plays a crucial role in interpretation. Context plays a role in such cases, but perhaps it is one which can be brought under the heel of theory.

A more radical challenge is that context can exert an influence that could not be systematized in a way consistent with the traditional conception of compositional semantics. On this conception, meaning determines truth conditions; so, relative to the same state of affairs, a sentence with a single meaning can have only one truth value. Suppose some brown leaves have been painted green and consider an utterance, concerning those leaves, of “Those leaves are green”. Suppose we are part of a commission inspecting Vietnam to determine whether Pentagon denials that it has used exfoliants are true. Brown leaves are signs of the early stages of the action of exfoliants. Charles Travis has sug-

gested that, relative to these concerns, the truth about the painted leaves is that they are not green. The utterance has a meaning upon which the facts just described make it false. Now suppose that we are trying to select camouflage material. Only green things will do, and more or less anything green will do. Relative to these concerns, Travis suggests, the truth about the leaves is that they are green. The utterance has a meaning upon which the same leaf-related facts make it false. Yet the sentence uttered is not ambiguous, so it ought to have only one meaning, determined by the meaning of its parts; so relative to a single state of affairs, it ought to have only one truth value, yet it seems to have two. This gives rise to doubt whether there is, in every case, anything both compositionally determined and determinative of truth conditions.

The conception of logical form guided by proxy semantics carries a further debatable commitment. Whereas we incline to think of our language as public, in the sense of being invariant among a community of speakers of (what we perhaps fecklessly call) a single language, there is no inference from this to the conclusion that the common language is implemented in the same way in the psychology of the individual speakers. Proper names are a much discussed case in which it seems quite likely that there is individual variation (and Frege, at least tentatively ([1892b], first footnote), and Russell quite explicitly ([1912] p. 29) said that there was). It may well be that my ability to use a name like “London” is bound up with various things I know about the city, and that your ability is bound up with a number of different things you know about the city. Even though we mean the same thing by the word (judged by ordinary standards), the underlying psychological processes may be different. If semantic structure has to mirror this underlying psychology, it may lose touch with the shared language. Russell thought that this was just how things are, which is why he firmly rejected the classification of his theories of names and descriptions as contributions to the philosophy of language as opposed to the philosophy of thought or judgement. What we think of as a single common language is no such thing, but is an artefact of a certain isomorphism among the way individual thinkers use words. For Russell, the fundamental subject matter was the individual thinker.

In its early days, the project of formalization seemed to give centre stage to notions of validity and proof; but more ambitious logical form proposals cannot be defended with just these materials. A conception of logical form as a proxy in a formalized language which will serve the purposes of semantics is better able to justify such claims. It faces the difficulty that logical form may not be unique, as different proxies may serve the semantic task equally well. If at this point we try to narrow the possibilities by requiring proxies to be psychologically realistic, to mirror somehow the semantic processing speakers actually engage in, we reach a position which, however controversial, is in some ways quite close in spirit to that which originally animated the project. In particular, it helps explain why the founding fathers of the project saw thought or judgement as more fundamental than language.


## 7 Conclusion

The original motivation for the introduction of artificial languages into logical studies was the lack of perspicuity in natural languages. If the only ambition is to use the perspicuity of an artificial language to attain some generalizations about validity in natural language, the connection between the artificial and the natural is unproblematic. The adequacy of a formalization ensures that if the formalization is valid, so is what it formalizes; and the notion that the formalization is an idealization diminishes any anxieties about validities in the natural language that are not reflected in adequate formalizations.

Once the aim is to segregate out formal validity in the natural language, a tension arises. This is because there are independent, even if vague, tests for whether or not a valid argument in natural language is formally valid. It turns out that arguments in natural language which, though valid, are not formally valid (for example, arguments involving adjectival detachment), can be adequately and validly formalized. It would seem a pity to pass up this opportunity; but seizing it is inconsistent with concentrating upon only formal validity in the natural language.

The relationship between the artificial and the natural seems most strained in connection with exotic logical form proposals, for example the view that English universal quantifications are quantifications of conditionals. Making sense of such claims requires Davidson's conception of logical form, but this does not necessarily substantiate the claims. This is because resistant intuitions (for example, the intuition that English quantifiers are binary) are some evidence, albeit inconclusive, that the logical form proposals, even if they get the truth conditions right within the project of proxy semantics, do not satisfy the psychological constraint.


The semantics that can be provided for languages like $\mathbf{Q}^{\star}$ offer a model of rigour and precision, and have provided an essential stimulus to research. What is overambitious is to suppose that these semantics are already, by proxy, what we seek for our natural language, since there is little evidence that they satisfy the psychological constraint. Indeed, it is overambitious to assume that compositional semantics of any form are possible for natural languages. But if they are not, that will be a most important fact, and one only statable against the background of what compositional semantics for artificial languages are like.

Davidson's conception offers the most ambitious prospect for the project of formalization, but let us not underestimate its other achievements. First, the very thought that specifying truth conditions is a useful contribution to specifying meaning (and perhaps sometimes exhausts what is required) grew up in the context of the project. Looking in his (somewhat distorting) rear-view mirror, Russell said that in his early years he thought that the logician's task in connection with "the" was to identify some weird abstract object to which it referred (Russell [1959], p. 150). Specification of the way in which the truth of "the"-sentences depends upon the truth of their components is a vastly improved goal. Secondly, it is surprising how much room for disagreement there is about the truth conditions of the sentences of the language we actually speak. We have encountered cases in connection with apparently very simple sentences: universal and existential quantifications, and sentences containing definite descriptions. Such disagreements could in practice only be discovered and expressed in connection with attempts at formalization in artificial languages for which truth conditions can be precisely stated. Thirdly, it is hard to overestimate the importance of formalization in the resolution of ambiguity. For example, once you have been introduced to the quantifier shift fallacy in the context of formalization, your ability to spot instances of it in English is greatly enhanced.

My concern with formal logic has been guided by the limited aim of describing and understanding the project of formalization. Formal logic is a discipline – a branch of mathematics – which can be pursued for its own sake and with no eye to this project. Many of the results obtained in this discipline have – or have been claimed to have – a philosophical importance of a kind not envisaged within the project of formalization.⁸


## Bibliographical notes

The traditional view of logical form derives from Frege and Russell. Neither of them is very explicit. Russell comes closest, in the quotation with which this book opened: “Some kind of knowledge of logical forms, though with most people it is not explicit, is involved in all understanding of discourse” [1914], p. 53.

For the Tractarian vision in its purest form, see Wittgenstein [1921]. Russell’s version [1918] already contains doubts. For its repudiation, see Wittgenstein [1932].

For an introduction to the techniques of natural deduction see Lemmon [1965] or (for more advanced texts) Prawitz [1965] and Tennant [1978].

For discussions of the logical constants, see Peacocke [1973] and [1987], Harman [1986], Prawitz [1977] and [1979] and Warmbröd [1999]. For logical truth, see Quine [1960], esp. §13, Peacocke [1987]. Quine’s attacks on meaning begin with [1951] and are continued in many later works, e.g. [1960]. Attacks on this position include those by Chomsky [1975], Evans [1975] and Boghossian [1996].

For a criticism of certain uses of schematic letters (like the name- and predicate-letters of Q), see Smiley [1982].

For compositional semantics see Davidson [1965], [1967a], [1970b], [1973], Davies, [1981], Schiffer [1987] and Travis [1996]. For the relation between semantics and the psychology of speakers, see Davies [1987], Evans [1981] and Wright [1981].

For Davidson’s conception of logical form, see especially his [1967b], [1970a] and [1973]. For an excellent presentation and criticism, see Foster [1976]. For a gentle shift of perspective, see Wiggins [1985]. For a quite different interpretation from mine of Davidson’s view, see Lycan [1984], pp. 31–2.

Further reading in philosophical logic could well take the form of following up works mentioned in connection with specific discussions. For something both wide-ranging and introductory I recommend Haack [1978]. Gabbay and Guenthner [1983], [1984], [1986] and [1989] contain survey pieces at an advanced level. For shorter introductions see Read [1994], Sainsbury [1996].


### Notes


¹ I use "truth conditions" in the way explained in chapter 1.9: the truth conditions of a sentence are the actual or possible circumstances in which it is or would be true. There is, however, another usage, according to which the truth condition (singular) of a sentence is its meaning.

² The *Tractarian dream* was dreamed before the notion of completeness for logical systems was available. No doubt the incompleteness of second order logic would have affected Russell’s version of the dream. (A consequence of incompleteness is that some valid sentences would be formalized by unprovable ones.)

³ It is presupposed that an expression has its analysis once and for all. Otherwise, the second point could be evaded by proposing different sets of primitives for different cases.

⁴ Even one who accepted the correspondence requirement need not be worried by this fact. Those who have done so much fruitful work on languages like QW and QC would have no cause for alarm if some of the results were to get classified as contributing to analysis rather than logical form.

$^5$ The contrast is not as clear as it might appear. Using the word “truth” in a definition does not automatically render it semantic, and the “semantic” features ascribed by interpretation rules are identified on the basis of purely syntactic features, the shapes of the sentences. The algebraic view of semantics mentioned in chapter 5.11 detaches semantics from the ordinary notions of truth etc., so could be regarded as belonging to syntax, yet it mentions no rules of proof. Equally, if in stating rules of proof you read the horizontal line as showing that what is below *follows from* what is above, you are viewing the rules in a semantic light.

⁶ For requirements not mentioned here, notably that of "harmony" between elimination and introduction rules, see Dummett [1991], esp. pp. 215 ff. See also Harman [1986], esp. pp. 117 ff.

$^7$ Cf. Prawitz [1965]. $\square \mathrm{I}(i)$ determines the logic known as S4. (In this system of classification, deriving from Lewis and Langford [1932], PN is known as S5.) Arguably, the English word “necessarily” is ambiguous, and one can see some modal logics, including S4, as specifying various disambiguations of it.

⁸ To choose two examples from dozens: John Lucas [1961] claimed that Gödel’s incompleteness theorem shows that men are not mechanisms; and Hilary Putnam [1980] claimed that the Löwenheim–Skolem theorem has far-reaching consequences for metaphysics.