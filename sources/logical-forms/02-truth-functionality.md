---
book: "Logical Forms"
title: "Chapter 02 Truth functionality"
chapter_number: "2"
chapter_name: "Truth functionality"
author: "Mark Sainsbury"
table_of_content: |
  1 The classical propositional language
  (2) Interpretations
  (3) P-interpretation rules
  (4) Nomenclature
  (5) P-validity
  (6) Scope
  2 Truth functional sentence connectives
  3 Formalizing English in P
  4 Comparison of P-connectives and English
  5 The case against the material implication account of “if”
  6 Implicature
  7 “If”: implicature in defence of the truth functional interpretation
  8 "If": direct arguments for the truth functional interpretation
    (1) The first argument
    (2) The second argument
  9 Non-truth functionality in English
    (1) John believes that
    (2) Because
    **(3) But**
    (4) When
  10 From P-validity to validity
---

# 2 Truth functionality

This chapter begins (in §§1–2) by introducing an artificial language: the language of propositional truth functional logic, here called P. Readers already familiar with this language should merely skim these sections, to check on the terminology and symbolism used here. (Of particular importance is a grasp of the precise notion of *interpretation*, in terms of which an appropriate notion of validity – here called P-validity – is defined.) In the later sections, the following question is discussed: what can the validity of arguments expressed in this artificial language tell us about the validity of arguments expressed in English? A crucial prior question will be whether the logical constants of P adequately translate the English expressions to which they are taken to correspond.

## 1 The classical propositional language

The two main features of P are these: (i) the only logical constants it recognizes are *sentence connectives*; (ii) all its sentence connectives are *truth functional*.

Sentences of $P$ are composed of two kinds of symbol: the letters of $P$; and the sentence connectives of $P$. The letters of $P$ are $p, q, r, p'$ etc. (we here envisage an endless supply), and they are used to formalize sentences which express propositions.

The P-logical constants are the following sentence connectives:

- (corresponding to “it is not the case that”; the symbol is called “tilde”);

- &amp; (corresponding to “and”; called “ampersand”);

$\vee$ (corresponding to “or”; called “vel”);

$\rightarrow$ (corresponding to “if . . . then . . .”; called “arrow”);

$\leftrightarrow$ (corresponding to “if and only if”; called “double arrow”).¹

The $\mathbf{P}$-sentences are the following:

1) a letter, standing alone. (That is, the letters themselves also count as sentences.)

2) (a) any sentence preceded by “$\neg$”. We can write this more economically as follows: if $X$ is a sentence, so is $\neg X$.

(b) if $X$ and $Y$ are sentences, so are

$(X \land Y)$;

$(X \vee Y)$;

$(X \rightarrow Y)$;

$(X \leftrightarrow Y)$.

Examples: (i) "$\neg p$" is a sentence; for "$p$" is a sentence by *`(1)`*, and "$\neg p$" results from it by preceding it by "$\neg$"; so, by *`(2a)`*, it is a sentence. (ii) "$(\neg p \land (r \leftrightarrow s))$" is a sentence, since "$(r \leftrightarrow s)$" is a sentence, by *`(1)`* and *`(2b)`*, and so is "$\neg p$", which establishes, by a further application of *`(2b)`*, that "$(\neg p \land (r \leftrightarrow s))$" is a sentence.

The above gives what is called the syntax of the language $\mathbf{P}$: rules which determine what is to count as a sentence of $\mathbf{P}$. (We sometimes omit outer parentheses around $\mathbf{P}$-sentences, provided that there is no danger of confusion.) We now turn to the semantics of $\mathbf{P}$. These are rules which in some sense specify the meanings of sentences of $\mathbf{P}$.

(1) Truth values

“Coal is white” is false, but “Snow is white” is true. We shall record this information by saying that “Coal is white” has the truth value false and “Snow is white” has the truth value true. We are thus thinking the truth values, truth and falsity, the true and the false, as kinds object. True sentences stand in the special relation of having to the t false sentences stand in that very relation to the false. This way of putting things has become standard, having been proposed, for subtle philosophical reasons, by Frege ([1892b], esp. p. 47). If you are reluctant to posit these abstract objects, true and false, you are in good company (see Dummett [1973], pp. 401–27). However, truth values, conceived of as objects (and so as capable of being “assigned” to sentences), are standardly assumed in logic; let us go along with this assumption.


## (2) Interpretations

3) An interpretation of P assigns exactly one of the truth values, true or false, to each sentence-letter in P.

For any one letter of P, there are two interpretations, one which assigns it the true, and one which assigns it the false. For any two letters, there are four interpretations, one assigning the true to both, one assigning the false to both, and two assigning different values. We cannot properly speak of a P-letter as being true or false, without qualification. Rather, a letter can be spoken of as true (or false) upon an interpretation. This means that P is the shell or structure of a language, rather than a real language which can be used to say things true or false (cf. Kirwan [1978], pp. 3–8, 32–41, Smiley [1982]): the structure requires completion by an interpretation.

Interpretations are supposed to be a contribution to semantics, and semantic theory is supposed in some sense to specify meaning. It is obvious that the meaning of a sentence cannot consist in its truth value. So how can an interpretation, in the sense of *`(3)`*, be counted as part of semantics? The hope is that interpretations will specify enough meaning for the logical purpose in hand: enough for the study of validity to the extent that this arises from the presence of P-logical constants. For this, the meaning of these constants will be critical, and arguably it can be specified just in terms of interpretations.

#### Ex. 2.1 Give a simple argument for the conclusion that the meaning of a sentence cannot consist in its truth value.

*`(3)`* is not a complete specification of what an interpretation is, for it applies only to P-letters, whereas there are (infinitely many) P-sentences which are not P-letters. In extending the account of an inter- pretation to other P-sentences, one arguably fixes the meaning of the P-logical constants. This extension is effected by interpretation rules which fix the ways in which truth values are transmitted upwards, from P-letters to more complex P-sentences.

Table 2.1

|  X | Y | ¬X | X ∨ Y | X & Y | X → Y | X ↔ Y  |
| --- | --- | --- | --- | --- | --- | --- |
|  T | T | F | T | T | T | T  |
|  T | F | F | T | F | F | F  |
|  F | T | T | T | F | T | F  |
|  F | F | T | F | F | T | T  |


## (3) P-interpretation rules

Henceforth “if and only if” will be abbreviated “iff”.

4) For any interpretation of P, say i,

$\neg X$ is true upon $i$ iff $X$ is false upon $i$;

$(X \land Y)$ is true upon $i$ iff $X$ is true upon $i$ and $Y$ is true upon $i$;

$(X \lor Y)$ is true upon $i$ iff $X$ is true upon $i$ or $Y$ is true upon $i$;

$(X \rightarrow Y)$ is true upon $i$ iff $X$ is false upon $i$ or $Y$ is true upon $i$;

$(X \leftrightarrow Y)$ is true upon $i$ iff either both $X$ and $Y$ are true upon $i$ or both $X$ and $Y$ are false upon $i$.

One standard way to codify this information is by means of *truth tables*. In table 2.1 a “T” (“F”) below an expression indicates that it is true (false) upon an interpretation which assigns the values to $X$ and $Y$ which are indicated at the left of the row. Thus, for example, the third row of the table for the “$\rightarrow$” column says that an interpretation upon which $X$ is false and $Y$ is true is one upon which $X \rightarrow Y$ is true.

Neither the interpretation rules nor the truth tables could be adequately represented by using just P-sentences. Suppose the rule for “¬” were written:

“¬p” is true on an interpretation iff “p” is false on that interpretation.

The displayed condition tells us what the truth value of “$p$” preceded by a tilde is, relative to an assignment of a truth value to “$p$”, but does not tell us what truth value will be accorded, relative to an assignment of a truth value to “$p$”, to the result of prefixing a tilde to “$q$”, nor what truth value will be accorded, relative to an assignment of a truth value to “$p$”, to the result of prefixing a tilde to a complex sentence, not a sentence-letter, for example, to the result of prefixing “$\neg p$” by a tilde. We thus use “$X$” and “$Y$” to stand for arbitrary P-sentences; they are called metalinguistic variables relative to P. We could have attained the required generality without using “$X$” and “$Y$” by, for example, writing the rule for “$\neg$”:

A P-sentence consisting of a tilde followed by a P-sentence is true upon an interpretation iff the latter sentence is false upon the interpretation.

In the light of the rules, an interpretation will determine a truth value for every P-sentence. There are just as many interpretations as there are ways of assigning truth values to the P-letters; each assignment to the letters determines, via *`(4)`*, a unique truth value for every P-sentence.

## (4) Nomenclature

$\neg X$ is called the P-negation of $X$;

$(X \land Y)$ is called the P-conjunction of the P-conjuncts $X$ and $Y$;

$(X \lor Y)$ is called the P-disjunction of the P-disjuncts $X$ and $Y$;

$(X \rightarrow Y)$ is called the (material) P-conditional with P-antecedent $X$ and P-consequent $Y$;

$(X \leftrightarrow Y)$ is called the (material) P-biconditional of $X$ and $Y$.

## (5) P-validity

5) An argument in $\mathbf{P}, X_1, \ldots, X_n; Y,$ is $P$-valid iff every interpretation upon which all the premises are true is one upon which the conclusion is true.

Abbreviation: $X_1, \ldots, X_n \models_{\mathbf{P}} Y$.

The “P-” prefix and subscript will be dropped when there is no danger of ambiguity. The point of it is to facilitate the formulation of various comparisons, for example with English sentences. Thus we have already defined negation for English. A question to be asked later is: is P-negation essentially the same thing as negation? Equally, we have given a definition of validity for English. A question to be asked later is: is P-validity (represented by “$\models_P$”) essentially the same thing as validity in English (represented by plain, unsubscripted, “$\models$”)?


The sentence connectives of P are so called because they take one or more sentences to make a fresh sentence. Languages other than P contain sentence connectives. For example, “It is not the case that” is a sentence connective in English: it takes one sentence, say “John is happy”, to form a fresh sentence, “It is not the case that John is happy”. Typically (setting aside the kinds of irregularity discussed at (1.12.20)), the sentence thus formed is the negation of the sentence from which it was formed. “And” is a sentence connective which takes two sentences to make a sentence. For example, it can make “John is happy and Mary is sad” from the two sentences “John is happy” and “Mary is sad”. Let’s call the sentence or sentences a sentence connective takes to make a fresh sentence the component(s) of the fresh sentence; and let’s call the fresh sentence itself the resultant sentence.

## (6) Scope

6) The scope of an occurrence of a sentence connective is the shortest P-sentence in which it occurs.

Thus the scope of “&amp;” in

7) $\neg(p \land q)$

is “$(p \land q)$”, whereas in

8) $(\neg p \land q)$

its scope is the whole of *`(8)`*. An occurrence of a sentence connective is said to dominate the sentence which is its scope. Nomenclature of P-sentences is determined by their dominant connective.

## 2 Truth functional sentence connectives

This section gives an account of truth functionality. It can be skipped by those already familiar with the notion.

Standard (“classical”) propositional logic deals with sentence connectives having a special property: they are *truth functional*. The terminology derives from the mathematical notion of a function, and one can use this to give a mathematically precise definition of truth functionality.² Alternatively, we can define a truth functional sentence connective in more informal terms:

1) *A sentence connective is truth functional* iff whether or not any resultant sentence it forms is true or false is determined completely by, and only by, whether its components are true or false.

Take, for example, “it is not the case that . . .”, as this is used to form the negation of what follows. Suppose what fills the dots is true. Then the resultant is false. Suppose what fills the dots is false. Then the resultant is true. So “it is not the case that” is truth functional, according to the definition.

**Ex. 2.2** Show that the claim that “it is not the case that . . .” is truth functional with respect to what fills the dots needs qualification. (Compare (1.12.20).)

All the sentence connectives of $\mathbf{P}$ are truth functional, according to the definition, as can be seen from (1.4) above.

Not every expression which we are inclined to classify as a sentence connective is a truth functional one. For example, we might naturally think of “Napoleon knew that” as a sentence connective. It can take the sentence “St Helena is in the Atlantic Ocean” to form the sentence: “Napoleon knew that St Helena is in the Atlantic Ocean”. However, it is not truth functional. The component is true, but this does not, in and of itself, determine whether or not the resultant sentence is true. The mere fact that “St Helena is in the Atlantic Ocean” is true does not settle whether Napoleon knew this or not.


Truth functionality is subject to the substitution test. If a sentence connective is truth functional, then the truth or falsehood of every resultant sentence which it forms depends only on the truth or falsehood of the components. So replacing a true component by another true one will make no difference to whether the resultant is true or false, and likewise for replacing a false component by another false one. Let us apply the substitution test to “Napoleon knew that St Helena is in the Atlantic Ocean”. We assume that this resultant sentence is true. (Anyone who disagrees can choose their own example of a truth of the form “Napoleon knew that . . .”). The component “St Helena is in the Atlantic Ocean” is also true. If “Napoleon knew that” were a truth functional sentence connective, it would form only sentences which pass the substitution test. But it does not. Consider any truth which Napoleon did not know, for example, “Quarks come in four colours”. “Napoleon knew that quarks come in four colours” is false, whereas “Napoleon knew that St Helena is in the Atlantic Ocean” is true. So “Napoleon knew that” fails the substitution test. Substituting one true component for another does sometimes yield resultants which differ in truth value.

Ex. 2.3 (a) Can substituting one false component for another in the context “Napoleon knew that . . .” lead to different truth values for the resultants?

**`(b)`** On the assumption that “necessarily”, in, for example, “necessarily no even prime number is greater than 2”, is a sentence connective use the substitution test to determine that it is not a truth functional one.

Now suppose we are wondering whether “and” is truth functional. If it is, then it is clear that it will express the same truth function as “&amp;”, as specified by (1.4): that is, “A and B” will be true iff “A” is true and “B” is true. “Paris is west of Berlin” and “London is north of Paris” are both true. If “and” is truth functional, then the conjunction “Paris is west of Berlin and London is north of Paris” is true. Moreover any true conjuncts will yield a true conjunction. So we could replace, say, “Paris is west of Berlin”, in the conjunction, by any other truth whatsoever, for example, “5 + 7 = 12”, and the new conjunction (“5 + 7 = 12 and London is north of Paris”) will be true. The results of this application of the substitution test are consistent with “and” being truth Now suppose we are wondering whether “and” is truth functional. If it is, then it is clear that it will express the same truth function as “&amp;”, as specified by (1.4): that is, “A and B” will be true iff “A” is true and “B” is true. “Paris is west of Berlin” and “London is north of Paris” are both true. If “and” is truth functional, then the conjunction “Paris is west of Berlin and London is north of Paris” is true. Moreover any true conjuncts will yield a true conjunction. So we could replace, say, “Paris is west of Berlin”, in the conjunction, by any other truth whatsoever, for example, “5 + 7 = 12”, and the new conjunction (“5 + 7 = 12 and London is north of Paris”) will be true. The results of this application of the substitution test are consistent with “and” being truth functional. The results do not establish the truth functionality of "and". For that, it would be necessary and sufficient to show that whatever sentences composed a conjunction, any replacement of either component by any like truth-valued sentence fails to affect the truth or falsity of the conjunction.

Standard (“classical”) propositional logic deals with sentence connectives having a special property: they are *truth functional*. The terminology derives from the mathematical notion of a function, and one can use this to give a mathematically precise definition of truth functionality.² Alternatively, we can define a truth functional sentence connective in more informal terms:

1) A sentence connective is *truth functional* iff whether or not any resultant sentence it forms is true or false is determined completely by, and only by, whether its components are true or false.

Take, for example, “it is not the case that . . .”, as this is used to form the negation of what follows. Suppose what fills the dots is true. Then the resultant is false. Suppose what fills the dots is false. Then the resultant is true. So “it is not the case that” is truth functional, according to the definition.

**Ex. 2.2** Show that the claim that “it is not the case that . . .” is truth functional with respect to what fills the dots needs qualification. (Compare (1.12.20).)

All the sentence connectives of $\mathbf{P}$ are truth functional, according to the definition, as can be seen from (1.4) above.

Not every expression which we are inclined to classify as a sentence connective is a truth functional one. For example, we might naturally think of “Napoleon knew that” as a sentence connective. It can take the sentence “St Helena is in the Atlantic Ocean” to form the sentence: “Napoleon knew that St Helena is in the Atlantic Ocean”. However, it is not truth functional. The component is true, but this does not, in and of itself, determine whether or not the resultant sentence is true. The mere fact that “St Helena is in the Atlantic Ocean” is true does not settle whether Napoleon knew this or not.


Truth functionality is subject to the substitution test. If a sentence connective is truth functional, then the truth or falsehood of every resultant sentence which it forms depends only on the truth or falsehood of the components. So replacing a true component by another true one will make no difference to whether the resultant is true or false, and likewise for replacing a false component by another false one. Let us apply the substitution test to “Napoleon knew that St Helena is in the Atlantic Ocean”. We assume that this resultant sentence is true. (Anyone who disagrees can choose their own example of a truth of the form “Napoleon knew that . . .”). The component “St Helena is in the Atlantic Ocean” is also true. If “Napoleon knew that” were a truth functional sentence connective, it would form only sentences which pass the substitution test. But it does not. Consider any truth which Napoleon did not know, for example, “Quarks come in four colours”. “Napoleon knew that quarks come in four colours” is false, whereas “Napoleon knew that St Helena is in the Atlantic Ocean” is true. So “Napoleon knew that” fails the substitution test. Substituting one true component for another does sometimes yield resultants which differ in truth value.

Ex. 2.3 (a) Can substituting one false component for another in the context “Napoleon knew that . . .” lead to different truth values for the resultants?

(b) On the assumption that “necessarily”, in, for example, “necessarily no even prime number is greater than 2”, is a sentence connective, use the substitution test to determine that it is not a truth functional one.


Instead of saying that a connective is truth functional, I shall sometimes say, equivalently, that it expresses a truth function.

P can represent only truth functional connections between sentences. English can, it seems, also represent non-truth functional connections between sentences. How extensive is this dissimilarity? And to what extent does it undermine the project of using P-validity to understand validity in English? This question is addressed later (especially in §9 and §10 below). The next section considers specific cases of formalizing English arguments in P, and using P-validity, where possible, to say something about validity.

## 3 Formalizing English in P

Does P-validity give a partial characterization of validity, or formal validity? The question divides: can we be sure that if a rendering in P of an English argument is P-valid, the English argument is valid (or formally valid)? And can we be sure that if a rendering in P of an English argument is not P-valid, the English argument is not valid (or not formally valid)? The examples which follow suggest some detailed considerations which bear on these questions.

Following a standard terminological practice, we shall call rendering an English sentence or argument in P formalizing it (more fully, P-formalizing it). Consider how one might formalize the following:

1) The battery is flat. If the battery is flat the car will not start. So the car will not start.

First, we stipulate a correspondence scheme between English sentences and P-letters. For *`(1)`* we might choose:

2) Let “p” correspond to “The battery is flat” and “q” to “The car will not start”.

Using this correspondence scheme, *`(1)`* is standardly formalized by

3) $p, (p \rightarrow q); q.$

This is $\mathbf{P}$-valid (in the sense of (1.5) above). Any interpretation, $i$, upon which all the premises are true is one upon which "$p$" is true. By the rule for "$\rightarrow$" (specified in (1.4) above), if "$p \rightarrow q$" is true upon $i$, then either "$p$" is false upon $i$ or "$q$" is true upon $i$. So if both "$p$" and "$p \rightarrow q$" are true upon $i$, then "$q$" is also true upon $i$. Hence every interpretation upon which all the premises are true is one upon which the conclusion is true. Standardly, one infers from the $\mathbf{P}$-validity of *`(3)`*, together with the correspondences of *`(2)`*, to the validity of *`(1)`*. The correctness of this inference is a main theme of this chapter. The examples of this section contribute to the answer, and an explicit statement is defended in §10.

A further straightforward example (compare (1.10.1)):

4) You can buy a ticket only if you have the exact fare. You haven't got the exact fare. So you cannot buy a ticket.

Let "$p$" correspond to "You can buy a ticket", "$q$" to "You have got the exact fare". Then the following formalizes *`(4)`* and is $\mathbf{P}$-valid:

5) $(p \rightarrow q), \neg q; \neg p.$

If the premises are to be true upon an arbitrary interpretation, $i$, then "$q$" must be false upon $i$, and so, by the "$\rightarrow$" rule, "$p$" must also be false upon $i$, so "$\neg p$" must be true upon $i$. So all interpretations upon which the premises are true are ones upon which the conclusion is also true.

We obviously cannot expect to make any inference from the quality of a $\mathbf{P}$-argument to the quality of an English argument supposedly formalized by it unless the formalization meets some standard of adequacy. We stipulate that if a formalization is to be adequate, the associated correspondence scheme should be such that if we replace the $\mathbf{P}$-letters by the corresponding English sentences, and then replace the $\mathbf{P}$-connectives by the corresponding English connectives, the result is a sentence (argument) that says the same as the original English. (Which English expressions correspond to which $\mathbf{P}$-connectives was stipulated

in §1.) Let us call the result of applying the correspondences to an argument the recovered argument. The proposed standard of adequacy is that the argument to be formalized should say the same as the recovered argument.

A related test of a formalization's adequacy can be given in terms of the notion of an intended interpretation. An intended interpretation is one which assigns to the relevant sentence-letters the same truth values as the ones the corresponding English sentences possess. A necessary condition for adequacy is that every sentence in the formalization should be true (false) on an intended interpretation iff the corresponding English sentence is true (false). In other words, an intended interpretation, by assigning the "right" truth values to the sentence-letters, must thereby assign the right truth values to the complex sentences (those which are not letters). We do not always know what the truth values of the English sentences are, so we cannot always apply this test for adequacy.

#### Ex. 2.4 Why would it be incorrect to speak of the intended interpretation?

The adequacy of a formalization is relative to a correspondence scheme. Hence, presenting a correspondence scheme is an essential part of presenting a formalization.

There may be more than one adequate formalization. Consider the argument:

6) If the figure is closed and has sides of equal length, then it is square or rhomboid. The figure is closed. The figure has sides of equal length. So it is square or rhomboid.

We could set up the following correspondence scheme:

7) “p” corresponds to “if the figure is closed and has sides of equal length, then it is square or rhomboid”, “q” to “The figure is closed”, “r” to “The figure has sides of equal length” and “s” to “The figure is square or rhomboid”.³


Relative to the correspondences of *`(7)`*, the $\mathbf{P}$-formalization of *`(6)`* is:

8) $p, q, r, s$.

According to the definition *`(1.5)`* of $\mathbf{P}$-validity, *`(8)`* is not $\mathbf{P}$-valid, for the premises are all true and the conclusion false upon an interpretation which assigns truth to "$p$", "$q$" and "$r$" and falsehood to "$s$". Intuitively, *`(6)`* is valid, yet by our stipulations *`(8)`*, given *`(7)`*, is adequate.

An alternative correspondence scheme is as follows:

9) "p" corresponds to "the figure is closed", "q" to "the figure has sides of equal length", "r" to "the figure is square" and "s" to "the figure is rhomboid".

Relative to *`(9)`*, an adequate formalization is:

10) $(p \land q) \rightarrow (r \vee s), p, q; (r \vee s)$.

(I omit parentheses where no confusion can result.) *`(10)`* is $\mathbf{P}$-valid. For consider an interpretation, say $i$, upon which all the premises are true. Then "$p$" and "$q$" are true upon $i$. So, by the rule for "\&", "$(p \land q)$" is true upon $i$. The rule for "$\rightarrow$", together with the supposition that the premise "$(p \land q) \rightarrow (r \vee s)$" is true upon $i$, ensures that "$(r \vee s)$" is also true upon $i$. So any interpretation upon which all the premises are true is one upon which the conclusion is true. For short:

11) $(p \land q) \rightarrow (r \vee s), p, q \models_{\mathbf{P}} (r \vee s)$.

So *`(10)`*, relative to *`(9)`*, is a candidate for demonstrating the validity of the English.

We could have used the following correspondence scheme:

12) "p" corresponds to "the figure is closed", "q" to "the figure has sides of equal length" and "r" to "the figure is square or rhomboid".

Relative to (12), the formalization is:

13) $(p \land q) \rightarrow r, p, q; r$.

This is P-valid. So *`(13)`* is also a candidate for demonstrating the validity of the English.

**Ex. 2.5** Show that (3.13) is P-valid either by informal reasoning using the definitions of the connectives and P-validity given in §1, or, if you know one, by a formal method.

All of *`(8)`*, *`(10)`* and *`(13)`*, coupled with their correspondence schemes, count as adequate formalizations of *`(6)`*: intuitively, they are faithful to the meaning of the English, or at least to those aspects of the meaning of the English that are relevant to propositional logic. But as only *`(10)`* and *`(13)`* are P-valid, only they could purport to demonstrate the validity of *`(6)`*.

(8), (10) and (13) differ in how much of the structure of (6) they make manifest. (8) captures the least, (10) the most. (10) captures more than is necessary to demonstrate the validity of (6), (8) captures less than is necessary. How much of a given sentence's structure needs to be reflected in its P-formalization will vary, depending on specific facts about the argument in which the sentence occurs. I shall say that the more structure an adequate formalization captures, the deeper it is. When people speak of "the" logical form of a sentence, they have in mind a formalization which goes as deep as possible.

If a formalization is invalid, can we infer that the argument formalized is also invalid? Consider the following example:

14) If you are good at mathematics, you will find logic easy. But you are not good at mathematics. So you'll find logic hard.

Let "p" correspond to "You are good at mathematics", and "q" to "You will find logic easy". Then a candidate for a formalization of (14) is:

15) $$ (p \to q), \neg p; \neg q. $$

This is not P-valid. For consider an interpretation, $i$, which assigns truth to "$q$" and falsehood to "$p$". The conclusion is false upon $i$. But both premises are true upon $i$, by the rules for "$\neg$" and "$\to$". Is *`(15)`* an adequate formalization of *`(14)`*?

To obtain the recovered argument from *`(15)`*, replace the letters by the corresponding English sentences as specified in the correspondence scheme, “→” by “if . . . then . . .” and “¬” by “it is not the case that”. The result is:


16) If you are good at mathematics then you will find logic easy. It is not the case that you are good at mathematics. So it is not the case that you will find logic easy.

The sentence from *`(14)`* “You’ll find logic hard” is replaced by “It is not the case that you will find logic easy”. You can fail to find something easy without finding it hard. So *`(16)`* does not say the same as *`(14)`* and so *`(15)`* is an inadequate formalization of it. Does this show that there is no inference from the invalidity of *`(15)`*, together with the associated correspondences, to the invalidity of *`(14)`*?

Consider a different correspondence scheme. Let “p” correspond to “You are good at mathematics”, “q” to “You will find logic easy”, “r” to “You’ll find logic hard”. Then the P-formalization is:

17) $(p \to q), \neg p; r.$

This is, obviously, P-invalid. Moreover it does not fail the condition for adequacy. Yet *`(17)`* is, intuitively, in some respect a less good formalization of *`(14)`* than is *`(15)`*. Can we make sense of this intuition?

Ex. 2.6 Specify an interpretation which demonstrates the P-invalidity of (3.17), by saying what truth values the interpretation assigns to its P-letters.

(14) is an argument which someone might actually propound in good faith, believing it to be valid. *`(17)`* gives no hint about how this mistake is possible, whereas (15) does. *`(17)`* is miles from anything that looks valid. But (15) might for a moment look valid, because of its passing resemblance to the P-valid

18) $(p \to q), \neg q; \neg p.$

One of the advantages of formalization is that it makes logical mistakes easier to spot. It is intelligible that one who is reasoning in English should think that the validity that attaches to an argument having the logical form of *`(18)`* attaches to *`(14)`*. This explanation is abetted by *`(15)`*, but not by (17).


If a formalization that counts as inadequate by the present standards can none the less be useful in explaining how someone might wrongly think an argument valid, would it not be better to revise the standards of adequacy? Consider again the first correspondence scheme, and the relationship between *`(16)`* and *`(14)`*. It is logically impossible for someone to find logic hard, yet not fail to find it easy. As we shall say, "You will find logic hard" entails "You won't find logic easy". In general, $A$ entails $B$ iff it is logically impossible for $A$ to be true yet $B$ not true. If $A$ entails $B$ but $B$ does not entail $A$, we say that $A$ is stronger than $B$ and that $B$ is weaker than $A$. The argument that one recovers from the formalization *`(15)`* by using the correspondences thus has a weaker conclusion than the conclusion in *`(14)`*. However, if some premises are inadequate to establish even a weaker conclusion, they are inadequate to establish a stronger one. So if we allow that the invalidity of *`(15)`* establishes the invalidity of *`(16)`*, then it should also be allowed to establish the invalidity of *`(14)`*.

This suggests the following emendation of the account of adequacy: we allow that an invalid formalization may be adequate to an invalid argument even if, though the premises of the recovered argument say the same as the original premises, the recovered conclusion is weaker. A parallel relaxation, a case of which will be considered shortly (see (21) and (22)), would allow that a valid formalization may be adequate to a valid argument even if the recovered argument has weaker premises.

To be able to use these relaxations, however, we would need already to be in a position to recognize the validity of arguments in English, whereas we were investigating whether we could use $\mathbf{P}$ to test for this property. A test which required us to recognize the target property before we could apply the test would not be much help. So I shall not allow the relaxed standards of adequacy.

Is there any way, using P-methods, that we can establish the invalidity of *`(14)`*? One possibility we would need to rule out is that *`(14)`* has a deeper formalization which is valid. Think how mistaken it would have been to have concluded that *`(6)`* was invalid on the basis of *`(8)`*. A necessary condition for there being no deeper formalization is that every truth functional sentence connective in English be somehow reflected by sentence connectives in the formalization. This condition is clearly met by *`(15)`*.

However, the fact that the deepest P-formalization is invalid is still not sufficient to establish the invalidity of the English. This is because there are valid arguments whose validity cannot be represented in P, for example:

19) All football supporters are interested in sport. Some football supporters are hooligans. So some hooligans are interested in sport.

The following correspondence scheme will ensure we go as deep as we can: let “p” correspond to “All football supporters are interested in sport”, “q” to “Some football supporters are hooligans” and “r” to “Some hooligans are interested in sport”. This correspondence goes as deep as possible, for there are no words in the sentences corresponding to P-letters which correspond to any of the P-connectives. Hence no further complexity in the formalization could be justified. Yet the resulting formalization is the P-invalid

20) $p, q; r.$

The conclusion is that we cannot hope that all validity should be reflected as P-validity.

Sometimes an argument’s premises are stronger than required for the conclusion. A putative example is:

21) If the mare dies, the farmer will go bankrupt, and then he will not cultivate the ground. The result will be that the wheat will fail, and this, in turn, will lead to local food shortages. Then the revolutionary spirit of the people will become inflamed, and they will man the barricades. So if the mare dies, the people will man the barricades.

An appropriate correspondence scheme is:

“p” for “The mare dies”;

“q” for “The farmer will go bankrupt”;

“r” for “The farmer will cultivate the ground”;

“s” for “The wheat will fail”;

“t” for “There will be local food shortages”;

"u" for "The revolutionary spirit of the people will become inflamed"; "v" for "The people will man the barricades".

A possible candidate formalization is:

22) $$ (p \to q) \land (q \to \neg r), (\neg r \to s) \land (s \to t), t \to (u \land v); p \to v. $$

The formalization corresponds only approximately to the original. There is a syntactic aspect: for example, the sentence "This will lead to local food shortages" is formalized as a conditional, whereas it is not one. In the project of formalization, this kind of reorganization is standard (though it is hard to find, or devise, an explicit justification for this practice). There is a semantic aspect: explicitly causal idioms like "the result will be" and "this will lead to" have been formalized by weaker P-conditionals, e.g. "¬r → s". What the correspondences recover from the latter is entailed by "If the ground is not cultivated, then, as a causal consequence, the wheat will fail", but does not entail it.

However, *`(22)`* is P-valid. So, provided we have no qualms about the adequacy of "p → v" as a formalization of the conclusion, and provided we have the general assurance that P-validity can establish validity, we can use *`(22)`* to establish the validity of *`(21)`*, despite the fact that the former does less than full justice to the strength of the latter's premises. The idea is that *`(21)`* would still have been valid, even if the premises had been weaker, as weak as the premises of the argument recoverable from *`(22)`*.

This approach is not available when the P-conclusion (more exactly, the conclusion recoverable from the P-formalization) is weaker than the English conclusion. For example, consider

23) Putting garlic in the salad will make Richard think that we care nothing for his preferences, and if he thinks that he will be upset. So putting garlic in the salad will make Richard upset.

A suitable correspondence scheme is:

"p" for "Garlic will be put in the salad";

"q" for "Richard will think we care nothing for his preferences";

"r" for "Richard will be upset".

The obvious formalization is:

24) $(p \to q), (q \to r); (p \to r)$

and this, plainly, is $\mathbf{P}$-valid. However, “If garlic is put in the salad then Richard will be upset” is weaker than “Putting garlic in the salad will make Richard upset”. The falsehood of “Garlic is put in the salad” is enough for the truth of “If garlic is put in the salad, Richard will be upset” on the assumption that “$\to$” correctly translates the “if” that occurs here. (To check this, consult the rule for “$\to$” in §1.) However, the falsehood of “Garlic is put in the salad” is not enough for the truth of “Putting garlic in the salad will make Richard upset”. So the $\mathbf{P}$-validity of *`(24)`* does not show that the premises of *`(23)`* establish the stronger conclusion: “Putting garlic in the salad will make Richard upset”.

I think that *`(23)`* is valid. The trouble is that, like *`(19)`*, its validity cannot be shown by $\mathbf{P}$-formalization. As we shall say: it is not valid in virtue of its $\mathbf{P}$-logical form.

The next example shows how $\mathbf{P}$-formalization may be used to resolve ambiguities:

25) John will choose the colour for his new bathroom and will paint it with his own hands only if his wife approves. But his wife doesn’t approve. So he will not paint it with his own hands.

A suitable correspondence scheme is:

“$p$” for “John will choose the colour for his new bathroom”;

“$q$” for “John will paint his new bathroom with his own hands”;

“$r$” for “John’s wife approves”.

Two formalizations are possible, depending on how we understand the organization of the first sentence:

26) $((p \land q) \to r), \neg r; \neg q.$

27) $(p \land (q \to r)), \neg r; \neg q.$

*`(27)`* is $\mathbf{P}$-valid, but *`(26)`* is not. One cannot speak of the validity invalidity of *`(25)`*. Rather, one must speak of it as valid on one reading (the one corresponding to *`(27)`*), and invalid on another (the one

corresponding to *`(26)`*). The formalizations treat the ambiguity of the first premise of *`(25)`* as a matter of scope. In *`(26)`*, “→” dominates the first premise: it has wide scope relative to “&amp;”. Analogously, we shall say that *`(26)`* treats “if”, in the first premise of *`(25)`*, as having wide scope relative to “and”. In *`(27)`*, “&amp;” dominates the first premise: it has wide scope relative to “→”. Analogously, we shall say that *`(27)`* treats “and”, in the first premise of *`(25)`*, as having wide scope relative to “if”.

Ex. 2.7 Give assignments to the letters of (3.26) to establish its P-invalidity. Show (by informal reasoning, or by a formal method) that (3.27) is P-valid.

Ex. 2.8 Give English versions of (3.26) and (3.27) which make plain the contrast between them.

The final example shows how finding the P-logical form of an argument may lead one to the view that it is valid, even though one was not clear whether it was valid or not when one looked at the English version:

28) If common sense is correct, then physics is true. If physics is true, then common sense is incorrect. Therefore common sense is incorrect.

Using obvious correspondences, this formalizes to the P-valid

29) $p \to q, q \to \neg p \models_{\mathbb{P}} \neg p.$

Ex. 2.9 (a) Demonstrate the P-validity of (3.29).

(b) Formalize each of the following arguments in P, showing your correspondence scheme. Determine the P-validity of the formalizations, and say what you think can be inferred about the validity of the English:

**`(i)`** Peter or Quentin killed Richard. If it was Peter, then the motive was jealousy. If it was Quentin, the motive was greed. But in fact the motive was not greed. So Peter killed Richard.

**`(ii)`** Peter will win the election unless Quentin does. Quentin won't win unless he buys all the electors drinks, and that is something he won't do. So Peter will win.

**`(iii)`** Neither Peter nor Richard will win the election unless Quentin doesn't stand. But Quentin's not standing would ensure Richard's success. So whatever happens, Peter will not win.

**`(iv)`** Although protective legislation has been enacted in most communities, the number of sperm whales is continuing to decline. The cause is either illegal whaling by nationals of countries participating in the protective legislation, or whaling by nationals of non-participating countries, which, under the circumstances, cannot be regarded as illegal. If the first alternative is ruled out, then the decline in numbers will be halted by bringing pressure on the non-participating governments. No doubt they will yield in exchange for subsidized loans. So if the decline in numbers of the sperm whale is not caused by illegal whaling, halting the decline requires making subsidized loans to non-participating governments.

**`(v)`** We can infer that the local plonk is good. For if it is not good, some people will not be drinking it. But some people are drinking it.

**`(vi)`** Either, if Tokyo is the capital of Japan, the EEC will collapse before 2007, or else, if the EEC will collapse before 2007, then Tokyo is the capital of Japan.

Two main questions have been raised in this section: can the validity of an argument be inferred from the P-validity of its P-logical form? And can the invalidity of an argument be inferred from the P-invalidity of its P-logical form? The second question has been answered negatively. The first question has not been explicitly answered, though the formalizations of examples like (1), (4) and *`(6)`* may encourage optimism. I return to these questions more systematically in §10 below.

## 4 Comparison of P-connectives and English

In §3, we took for granted that the connectives of P, though given their official definitions by the interpretation rules, correspond closely to their English counterparts. It is now time to examine that assumption.

First, we must try to state what sort of correspondence we require. The simplest idea is that when we recover an argument from a logical form by applying the correspondences, the result should be the original argument. But this standard is unduly restrictive. The tradition allows for a certain amount of reorganization, allows one, at the very least, to match "unless" with "√". A more relaxed standard is that the recovered argument should have all the validity-relevant features of the original.


Ex. 2.10 Show that there is a case for thinking that "He will die unless he is given penicillin" is equivalent to "He will be given penicillin or die".

If this standard is to be met, the P-connectives must have all the validity-relevant features of the English expressions they are matched with in formalizing. Since validity is definable in terms of truth conditions, the requirement can be put: the P-connectives must make the same contribution to truth conditions as the English connectives with which they are matched. The contribution to truth conditions of a P-connective is given by the appropriate interpretation rule. The standard is thus that the English expressions should express the same truth function as the P-connectives with which they are matched. A precondition for an expression's expressing a truth function is that it be a sentence connective. This is because it is sentences that are true or false (possess truth values), and a truth function fixes a truth value from (a sequence of) truth values. (For example, the truth function expressed by “&amp;” fixes the value false for a conjunction on an interpretation iff one of the conjuncts is false on the interpretation.) The discussions thus tend to fall into two parts: putative cases in which the English expression corresponding to a P-connective is not a sentence connective, and putative cases in which, though a sentence connective, it is not truth functional.

The important notion of *implicature* which is mentioned here is discussed in more detail in §6.

(1) “¬” and “not”

The P-connective “¬” corresponds closely to the English word “not”, and similar phrases like “it is not the case that”, as these are used to form negations. If “John is here” is true (false), then “John is not here” and “It is not the case that John is here” are false (respectively, true). So it appears that on at least some occurrences, “not” is a sentence connective and expresses the same truth function as “¬”.

There are cases in which "not" does not form a negation. For example, if "Some cows eat grass" is true, it does not follow that "Some cows do not eat grass" is false. Here "not" does not seem to function as a sentence connective, let alone as a sentence connective expressing the same truth function as "not". Rather, it seems to form a new predicate, "do not eat grass".

There are other cases in which "not" seems not to function as a sentence connective. For example:

1) Not Abraham, but George, chopped down the cherry tree.

Here, on the face of it, "not" attaches to a name rather than a sentence. However, it could be argued that (1) is merely a fanciful way of expressing

2) Abraham did not chop down the cherry tree but George did

and here "not" does, after all, form a sentence from a sentence (from "Abraham did chop down the cherry tree"), and in a way that expresses the truth function expressed by “¬”.

There are no cases in which "not" appears to function as a sentence connective, but a non-truth functional one.

Ex. 2.11 (a) Suppose "p" corresponds to "Some cows eat grass". Why does "¬p" not formalize "Some cows do not eat grass"? (Check the definition of "¬" in §2.)

(b) Suppose "¬q" formalizes "Some cows do not eat grass". To what does "q" correspond?

**`(c)`** Are there any difficulties in interpreting "not" as it occurs in the following sentences as expressing the same truth function as "¬"? If there are none, provide a P-formalization (showing your correspondence scheme). If there are any difficulties, explain.

(i) I am not very optimistic about the upshot of the talks.

(ii) The world will end not with a bang but with a whimper.

(iii) You ought not to smoke.

(iv) All the passengers who have not got tickets will wait in line.

**`(d)`** Suppose someone affirms:

This book isn't bad it's very bad.

Should we see "not" as non-truth functional? How else might we understand such an utterance?

(2) “&amp;” and “and”

The P-connective “&amp;” is fairly closely matched by the English “and”. “Two is an even number and three is an odd number” is indeed true iff “Two is an even number” is true and so is “Three is an odd number”. But there are, arguably, some discrepancies.

**`(a)`** Cases in which “and” appears not to function as a sentence connective, in which case it certainly could not be translated by “&amp;”, which is a sentence connective:

3) Tom and Mary came to dinner.

On the face of it, far from taking two sentences to make a fresh sentence, “and” in *`(3)`* takes two names to make a complex subject expression “Tom and Mary”. In this sort of case you might argue that appearances are superficial, and that *`(3)`* abbreviates

4) Tom came to dinner and Mary came to dinner.

Even if the suggestion works for some cases in which “and” is, superficially, a name connective rather than a sentence connective, it may not work for all. Consider:

5) Tom and Mary lifted the piano.

Arguably this is not equivalent to

6) Tom lifted the piano and Mary lifted the piano.

*`(5)`* suggests a joint effort, which *`(6)`* does not. (One could add “together” at the end of *`(5)`*, to make the collaboration entirely plain.) In such cases, it seems we have to regard “and” as forming a complex name out of two simple names. For different reasons, we seem to have to say the same for examples like the following:

7) Tom and Mary are compatriots.

This is not equivalent to

8) Tom is a compatriot and Mary is one too.

We seem to have another kind of case in which "and" joins names rather than sentences.

Yet another putative example of "and" occurring as something other than a sentence connective is the following:

9) Some girls are pretty and flirtatious.

Ex. 2.12 There is an analysis of (4.7) according to which "and" functions in (4.7) the same way as it does in (4.9). Can you discover it?

Here "and", at least superficially, joins two adjectives, "pretty" and "flirtatious", to form a complex adjectival expression. Perhaps *`(9)`* is an abbreviation of a sentence in which "and" is genuinely a sentence connective. But what sentence? Not

10) Some girls are pretty and some girls are flirtatious.

For *`(10)`* does not have the same truth conditions as *`(9)`*: *`(10)`* could be true, yet not *`(9)`*, if it were the case that ugly girls, and only ugly girls, flirt.

11) John washed immediately and thoroughly.

Here "and", at least superficially, joins two adverbs, "immediately" and "thoroughly", to form a complex adverbial expression. Perhaps *`(11)`* is an abbreviation of a sentence in which "and" is genuinely a sentence connective. But what sentence? Not

12) John washed immediately and John washed thoroughly.

For *`(12)`* does not have the same truth conditions as *`(11)`*: *`(12)`* would be true yet not *`(11)`*, if John washed twice, once immediately but not thoroughly, and once thoroughly but not immediately.

(b) Cases in which "and" is a sentence connective but is, allegedly, not truth functional, and so not equivalent to "&amp;".

A standard kind of example is:

13) Mary got married and had a baby.

14) Jane Austen died in 1817 and was buried at Winchester.

Here there is no question about “and”’s claim to be a sentence connective. (There is a slight element of abbreviation: the second component elides the name in each case.) But it is argued that “and” cannot be translated by “&amp;”. If it could be, then the truth or falsehood of *`(13)`* and *`(14)`* would depend on nothing more than the truth or falsehood of the components. The objection is that this is not so: *`(13)`* and *`(14)`* require for their truth that the event reported in the second component occur after that reported in the first.

From the interpretation rule for “&amp;”, we know that “X &amp; Y” is true iff “X” is true and “Y” is true. So “X &amp; Y” is true iff “Y &amp; X” is true: as we shall say, “X &amp; Y” and “Y &amp; X” are equivalent. This fact is reflected in the general truth about P-validity:

15) $X \land Y \models_{P} Y \land X.$

This is to be read as follows: if X and Y are any P-sentences, the result of forming their conjunction in that order serves as a premise to a P-valid argument whose conclusion is the conjunction of X and Y in the other order.

If “&amp;” expressed the same truth function as “and” in (13) and (14), the following arguments would be valid:

16) Mary got married and had a baby. So Mary had a baby and got married.

17) Jane Austen died in 1817 and was buried at Winchester. So Jane Austen was buried at Winchester and died in 1817.

Those who think that the premises do not entail the conclusion will hold that *`(16)`* and *`(17)`* are not valid, so that in these cases “and” does not express the truth function that “&amp;” expresses.

The standard response is to say that *`(16)`* and *`(17)`* are valid, the contrary appearance being created by the fact that *`(13)`* implicates, but does not entail, that Mary got married before having the baby, and similarly for *`(14)`*.

Ex. 2.13 (a) Are there any difficulties in interpreting “and” as it occurs in the following sentences as expressing the same truth function as “&amp;”? If there are none, provide a P-formalization (showing your correspondence scheme). If there are any difficulties, explain.

(i) John and Mary bought a boat.

(ii) All elephants have short ears and long tails.

(iii) Some elephants have short ears and long tails.

(iv) You and I are the only people who matter.

(b) Evaluate the following claim:

“&amp;” is binary, but “and” is not. For example, in John is happy, Mary is tall and Sarah is weak “and” makes a sentence out of three sentences.

Cf. McCawley [1981], pp. 49–54.

(3) “√” and “or”

The nearest English equivalents to “√” are “or” and “either . . . or . . .”. These are certainly sometimes sentence connectives, as in:

18) You’re a fool or you’re a rascal.

19) Either you’re a fool or you’re a rascal.

It certainly seems that *`(18)`* and *`(19)`* are true iff at least one of “You’re a fool” and “You’re a rascal” is true. So there is a case for saying that “or” expresses the same truth function as “√”.

Another class of cases in which “√” seems close to “or” is provided by a certain kind of game. “I’ll give you a clue: either William hid the silver or Tom hid the gold . . . Which box contains the silver, which the gold, which the lead?”

As with “and”, I divide the alleged discrepancies into those cases in which “or” (or “either . . . or . . .”) is supposedly not a sentence connective, and those in which it supposedly occurs as a sentence connective which does not express the same truth function as “√”.

(a) Cases in which “or” appears not to function as a sentence connective.

20) Tom or Mary could help you.

Here "or", at least superficially, joins not two sentences to form a sentence, but two names to form a complex subject expression. (20) cannot be regarded as an abbreviation of

21) Tom could help you or Mary could help you,

for most people hear *`(20)`*, but not *`(21)`*, as meaning that Tom could help you and so could Mary.

Ex. 2.14 (4.20) does not seem to entail that Tom and Mary could both help you (simultaneously), for it could be true in a situation making it impossible for there to be more than one helper. Give an example to show this. Does this suggest a way of avoiding the unattractive suggestion that "or" in (4.20) really means "and"? Provide details.

22) Every number is odd or even

should be compared with (9). At least superficially, "or" here joins two adjectives, "odd" and "even", to form a complex adjectival expression. Could (22) be an abbreviation of a sentence in which "or" is genuinely a sentence connective? What sentence? Not

23) Every number is odd or every number is even

for this plainly means something different from *`(22)`*. Indeed, *`(22)`* is true, *`(23)`* false.

A problematic case is:

24) He asked whether John would win or not.

We cannot understand this as meaning

25) He asked whether the following is true: John will win or John will not win.

Everyone knows that "John will win or John will not win" is true: this cannot have been what the questioner wanted to know. But it is not easy to see how "or" as a sentence connective could be used to express what is being asked.


(b) Cases in which "or" is a sentence connective but is, allegedly, not equivalent to "v".

These cases are of two kinds: (i) those in which it is agreed that "or" expresses some truth function, and the disagreement is over whether it expresses the same one as "v"; (ii) those in which it is contended that "or" does not express a truth function.

(i) “v” expresses what is standardly called inclusive disjunction. If “X” and “Y” are both true, so is “X ∨ Y”. It is sometimes claimed that “or”, and, more especially “either . . . or . . .”, express exclusive disjunction. The exclusive disjunction of X with Y is true just on condition that exactly one of “X” and “Y” is true. We can, of course, easily define a P-connective which expresses this function. And if “or” does, sometimes or always, express exclusive disjunction, we need, sometimes or always, to avoid matching it simply with “v”.

Ex. 2.15 Show how the exclusive disjunction of any P-sentences X and Y can be expressed using just the P-connectives already defined (in §2).

26) This number is odd or this number is even

might be offered as a candidate example of exclusive disjunction. However, the case is inconclusive. We must admit that the truth of both disjuncts is excluded, but it remains to be shown that the excluding is done by "or" rather than by the particular senses of the disjuncts, which already preclude their joint truth. This phenomenon is entirely consistent with "or" expressing inclusive disjunction.

A better example is:

27) You are welcome to come to dinner on Monday or Tuesday.

If "or" is a sentence connective here, it presumably connects "you come to dinner on Monday" and "you come to dinner on Tuesday", so that *`(27)`* is an abbreviation of something like:

28) I would welcome your making it true that: you come to dinner on Monday or you come to dinner on Tuesday.

But many people hear *`(27)`*, and so, presumably, *`(28)`*, as constituting an invitation for just one dinner, not two.⁴ If this is right, there is a case for thinking that “or” sometimes expresses exclusive disjunction, and so on such occasions should not be matched simply with “∨”.

Ex. 2.16 A restaurateur who puts on the menu “dessert or fruit” commits himself only to allowing you one of these, but he does not falsify his menu, or violate any undertaking to which his menu commits him, if he gives you both. Does this support the inclusive or the exclusive interpretation of “or”? Reflection on this case should, in my view, remove any appearance of exclusive disjunction in (4.27). Can you explain how this line of thought runs?

(ii) The most telling reason for thinking that “or” is not truth functional issues from such cases as:

29) Either the superpowers will abandon their arms race, or there will be a third world war.

The suggestion is that *`(29)`* requires for its truth not merely the truth of at least one (or exactly one) of its disjuncts, but in addition that there be some special connection, presumably in this case causal connection, between the falsehood of one disjunct and the truth of another. *`(29)`* asserts, it may be said, that the arms race will lead to war.

If this is right, then we ought to be able to discover failures of the substitution test (see §2). The test is rather hard to apply in such a case, because there is likely to be disagreement about whether the disjuncts are true or false. Suppose we think that *`(29)`* is true, but that the first disjunct is false (i.e. it is false that the superpowers will abandon their arms race). Then, if the “or” it contains is truth functional, we ought to find the following true, despite the fact that no one could for a moment suppose that there is any causal connection between the truth of the first disjunct and that of the second:

30) Either $2 + 2 = 22$ or there will be a third world war.


Holding our suppositions firmly in mind (the truth of *`(29)`*, the falsehood of its first disjunct), it actually seems rather unlikely that one should find *`(30)`* false. The suppositions entail that there will be a third world war; and this seems to entail *`(30)`*. So it seems as if the result of replacing the first disjunct of *`(29)`* (which we are supposing to be false) by an arbitrary falsehood results in a sentence with the same truth value as *`(29)`*. This is a partial fulfilment of the substitution test.

Ex. 2.17. What else needs to be done to complete the substitution test? Try at least one further substitution in (4.29), and report whether you think it consistent or inconsistent with the truth functionality of "or".

Completing the substitution test would be hard work, so one might try to find a more general argument either for or against the view that *`(29)`* would fail it. One might suggest that *`(29)`* is equivalent to

31) If the superpowers will not abandon their arms race, there will be a third world war.

If this equivalence holds generally, the question of the truth functionality of "or" reduces to the question of the truth functionality of "if".

(4) “→” and “if”

The nearest English equivalents of “→” are: “If . . . then . . .”; “. . . if . . .”; and “. . . only if . . .”. I will concentrate on the first of the idioms, calling “if . . . then . . .” sentences conditionals, the sentence filling the first blank the antecedent, the sentence filling the second blank the consequent. A common view is that conditionals cannot be adequately formalized by “→”.

One ground for this view is that a sentence “if A then B” requires for its truth some special connection between what would make “A” true and what would make “B” true, a causal connection, for example. No such connection is required for the truth of “p → q”. Consider a volume of water which in fact will not be heated to 90° at any time in the coming year, so that the sentence “this volume of water is heated to 90° at some time during the coming year" is false. Let this correspond to the P-letter "p". Let "q" correspond to "this volume of water will turn to ice". It follows that


32) $p \to q$

is true upon an intended interpretation, whereas, so the claim runs,

33) If this volume of water is heated to 90° at some time during the coming year, this volume of water will turn to ice

is false. (32) is an inadequate formalization, since "if" does not express the same truth function as "→".

Ex. 2.18 Why is (4.32) true? (Refer back to the definition of “→” at (1.4).)

Ex. 2.19 It might be suggested that the following example shows that "if" sometimes expresses a truth function, but not that of "→":

If you need bandages, there are some in the first aid box.

Here, according to the suggestion, the conditional is true iff its consequent is. Discuss the suggestion.

The question of the relation between “→” and “if” has been very widely discussed. I shall divide up the issues as follows. In the remaining part of this section, I will try to demarcate the area of the controversy: it concerns “indicative” rather than “subjunctive” conditionals, but it is not easy to give adequate criteria for this distinction. In subsequent sections, I present the case against the truth functional interpretation (§5), the outline of an implicature defence against this case (§§6, 7), and finally (§8) some general arguments in favour of the truth functional interpretation. The issue is not resolved in these discussions, and the question is taken up again in chapter 3, and again in chapter 5.2.

Consider the following two “if” sentences:

34) If Oswald didn't shoot Kennedy, someone else did.

35) If Oswald hadn't shot Kennedy, someone else would have.

It would be perfectly reasonable to regard one of these sentences as true and the other false. For example, you might reasonably believe *`(34)`*, simply on the ground that someone did shoot Kennedy (he wasn't poisoned, etc.). Yet you might not believe *`(35)`*, and would not if you thought that Oswald was a maniac working alone, and that no one else would have wanted Kennedy dead. The fact that *`(34)`* and *`(35)`* may diverge in truth value encourages the view that we cannot have a uniform account of the two kinds of sentence: we will need one account of the way in which "if" works in indicative conditionals, like *`(34)`*, another of the way in which it works in subjunctive conditionals like *`(35)`* (see chapter 5.2). The target of our discussion is the claim that indicative (rather than subjunctive) conditionals can be adequately formalized by material conditionals, those dominated by “→”.

The attempt to formalize *`(35)`* as a material conditional leads to an instructive kind of nonsense:

36) (Oswald hadn't shot Kennedy) → (someone else would have shot Kennedy).

We can extend the definitions of the P-connectives in the obvious way to allow them to stand between English sentences, A and B: “A → B” is true iff either “A” is false or “B” is true. A sentence connective connects only sentences which are capable of having truth values; if it is a truth functional sentence connective, these are the values that are inputs to the truth function, and the sentences must possess them independently of their role in some putatively truth functional context. The components of *`(36)`* do not have this property. “Someone else would have shot Kennedy” arguably has no self-standing use at all, and so we cannot talk of its truth value. “Oswald hadn't shot Kennedy” does have a self-standing use, for example in a chronicle of Dallas: “At that time, Dallas was a peaceful city. The strains of unregulated growth had not become apparent, and Oswald hadn't shot Kennedy.” This use is plainly not what is at issue in *`(36)`*, which does not in that way carry an implicit reference to a past time. “Oswald hadn't shot Kennedy”, as used in *`(36)`*, cannot be used self-standingly. This means that *`(36)`* is not really intelligible, and that there can be no question of treating *`(35)`* on the pattern of *`(36)`*. sentences that are capable of being true or false when standing alone, so that “if” is not functioning as a sentence connective. One kind of example will be familiar from (9) and (22):

There are other ways in which, even where the mood is not explicitly subjunctive, the English conditional does not link two


37) If someone is in debt, he should curb his expenditure.

Here the consequent “he should curb his expenditure” is not a complete sentence, since the referent of “he” is not determined. Hence the consequent is not capable, on its own, of being true or false. Hence we cannot translate *`(37)`* as

38) (Someone is in debt) → (he should curb his expenditure).

Ex. 2.20 What, if anything, would be wrong with the translation: (someone is in debt) → (someone should curb his expenditure)?

There are also conditionals which it is not obviously correct to classify as indicative conditionals, even though their components are in the indicative mood, and appear capable of being used self-standingly. For example, someone contemplating the future might truly affirm:

39) If John dies before Joan, she will inherit the lot.

The components are capable of being evaluated for truth and falsehood as self-standing sentences. However, it also seems that *`(39)`* is equivalent to

40) If John should die before Joan, she would inherit the lot.

This means that there is a case for saying that *`(39)`*, despite being grammatically indicative, is best classified as a subjunctive rather than as an indicative conditional (cf. chapter 5.2).

There are other uses of “if” which we would not wish even to try to formalize using “→”, for example

41) John wonders if his life is meaningful.

It is literally true that each of “John wonders” and “John’s life is meaningful” are capable of being evaluated for truth and falsehood as self-standing sentences, but it should also be clear that their use as self-standing sentences differs from their use in *`(41)`*. This could be brought out by sentences similar to *`(41)`*, for example

42) John wanted to know if he had been born in wedlock.

It is not that this is a subjunctive conditional. It is not a conditional at all. Rather, “if” in *`(42)`* is being used to form an indirect question, and could be replaced by “whether”.

## 5 The case against the material implication account of “if”

The view to be attacked in this section is that we can adequately formalize (indicative) conditionals by “→” -sentences; equivalently, that conditionals are P-material implications; equivalently, that “if” (as it occurs in the cases under discussion) expresses the same truth function as “→”. As a preliminary, let us see if we can establish the following:

1) Any truth functional occurrence of “if . . . then . . .” expresses the same truth function as “→”.

(The phrasing allows for the possibility of non-truth functional occurrences of “if . . . then . . .”). If we can establish *`(1)`*, then the question whether conditionals are material conditionals becomes the question whether “if”, as it occurs in English conditionals, is truth functional.

If “if . . . then . . .” were truth functional, and functioned in the same way on all its occurrences, there would be a simple way to establish (1). It would be enough to find “if . . . then . . .” sentences whose truth values, in point of their components and resultant, match the truth table for “→”. For example, suppose we find a true “if . . . then . . .” sentence with false antecedent and true consequent, perhaps “if New York is south of Beirut, then New York is south of Paris”. The supposition that "if . . . then . . ." is always truth functional would enable us to infer that any "if . . . then . . ." sentence with false antecedent and true consequent is true, which corresponds to the third line of the truth table for "→" (table 2.2). It is not hard to do the same for the remaining three lines of the table. The result would be a correct table in which "if A then B" could replace X → Y.

Table 2.2

|  X | Y | X → Y  |
| --- | --- | --- |
|  T | T | T  |
|  T | F | F  |
|  F | T | T  |
|  F | F | T  |


Ex. 2.21 For each of the first two and the last line of table 2.2, find a conditional which has the truth value indicated in the last column, and whose antecedent and consequent are well known to have the truth values indicated in the first two columns.

This approach assumes that "if . . . then . . ." makes the same contribution on every occurrence. If it were ambiguous, having one meaning in one of our sample sentences, another in another, we would not have shown that on any of its meanings it expresses the "→" truth function. Suppose one of our sample sentences were "If you need bandages, there are some in the first aid box" (cf. Ex. 2.19). It might be argued that on this occurrence it expresses a different truth function from the one it more typically expresses, on the grounds that this sentence is true iff its consequent is.

Here is an argument which goes some way towards meeting this difficulty. Suppose some arbitrary sentence "if A then B" is truth functional with respect to A and B. Suppose also that:

2) Using "if . . . then . . ." as it occurs in "if A then B", every instance of "if A and B then A" is true.

3) "and" expresses the same truth function as "&amp;".

4) Using "if . . . then . . ." as it occurs in "if $A$ then $B$", there are falsehoods of this form.

We can argue as follows, starting from *`(2)`*. Take an instance of "if $A$ and $B$ then $A$" in which $A$ is false. Then "$A \land B$" is also false (by *`(3)`*). So by the assumption of truth functionality, every instance of "if . . . then . . ." with false antecedent and false consequent is true, establishing the fourth line of a truth table for "if . . . then . . .". Now suppose that $A$ is true. There are two subcases. On one of them, $B$ is true, so "if $A$ and $B$ then $A$" is a truth with true antecedent and true consequent, which, given truth functionality, establishes the first line of the table. One the other subcase, $B$ is false, so "if $A$ and $B$ then $A$" is a truth with false antecedent and true consequent, which, given truth functionality, establishes the third line of the table. The second line of the table is then established by *`(4)`*. So given *`(2)`*-*`(4)`*, we can establish *`(1)`*. The upshot is that the question whether (some occurrence of) "if . . . then . . ." expresses the same truth function as "$\rightarrow$" reduces to the question whether (that occurrence of) "if . . . then . . ." is truth functional, that is, expresses some truth function or other. In this section, I present the case for a negative answer to this question.

(a) The falsehood of $X$ upon an interpretation is enough for the truth of $X \to Y$ upon that interpretation. But the falsehood of the antecedent is not enough for the truth of an indicative conditional formed with "if" or "if . . . then". Examples:

5) If ice is denser than water, then ice floats on water

6) If ice does not float on water, then ice floats on water

are usually held to be false. But, using "p" to correspond to "ice is denser than water", and "q" to correspond to "ice floats on water", "p → q" and "¬q → q" are both true upon an intended interpretation, viz. one in which the truth values of the P-letters match those of their corresponding English sentences, viz. one which assigns false to "p" and true to "q".

This is connected with a fact about validity. In $\mathbf{P}$ we have:

7) $X \models_{\mathbf{P}} [\neg X \to Y]$, whatever $Y$ may be.

Ex. 2.22 Show that (5.7) in true.

This says that any P-sentence constitutes the premise of a P-valid argument for any P-conditional having the negation of that sentence as antecedent. But, it is claimed, the following is false for English:

8) $A \vDash [\text{if not-}A \text{ then } B]$, whatever $B$ may be.

That is, the fact corresponding to *`(7)`* does not obtain for English. You cannot always validly infer from an English sentence to an arbitrary indicative conditional having the negation of that sentence as its antecedent. If this contrast is correct, then “if” does not make the same contribution to validity as “$\rightarrow$” does; hence it does not make the same contribution to truth conditions; in particular, it is not truth functional.

(b) An interpretation upon which $Y$ is true is one upon which $X \to Y$ is true. But the truth of the consequent is not enough for the truth of an indicative conditional formed with “if” or “if . . . then”. An example is:

9) If ice is as dense as lead, then ice floats on water.

A connected claim is that whereas

10) $Y \vDash_{\mathbf{P}} [X \to Y]$, whatever $X$ may be,

it is not the case that

11) $B \vDash [\text{if } A \text{ then } B]$, whatever $A$ may be.

Ex. 2.23 (a) To serve as an example, (5.9) needs to be false. Put the case for the view that it is true (even if you don't accept this view!).

(b) Can you think of a convincing example to show the falsehood of (5.11)?

(c) Suppose you believe that there will be a third world war whether or not there is a summit meeting next spring. Suppose you also firmly believe that there will be no summit meeting next spring. Should you accept or reject the conditional "If there is a summit meeting next spring, there will be a third world war"? What bearing does your answer have upon whether (5.11) is true?


(c) Whereas

12) $\neg(X \to Y) \models_{\mathbb{P}} X,$

it is not the case that

13) [it is not the case that (if $A$ then $B$)] $\models A$.

For example, it is claimed that the following is invalid:

14) It is not the case that if the number three is even then it is prime. So the number three is event.

Ex. 2.24 Which answer to Ex. 2.23(c) undermines the claim that (5.14) is invalid? Explain your answer.

(d) Whereas

15) $\neg(X \to Y) \models_{\mathbb{P}} \neg Y,$

it is not the case that

16) [it is not the case that (if $A$ then $B$)] $\models$ it is not the case that $B$.

For example, it is claimed that the following is invalid:

17) It is not the case that, if I go to the party tonight, I shall get drunk tonight. So I shall not get drunk tonight.

**`(e)`** Whereas

18) $(X \to \neg Y), Y \models_{\mathbb{P}} \neg X,$

it is not the case that

19) [if $A$ then not-$B$, $B$] $\models$ not-$A$.

For example, it is claimed that the following is invalid:

20) If it rains, then it will not rain heavily. It will rain heavily. So it will not rain.

**`(f)`** “If” is not transitive, whereas “$\rightarrow$” is. By the *transitivity* of “$\rightarrow$” is meant the following:

21) $X \to Y, Y \to Z \models_{\mathsf{P}} X \to Z$.

The non-transitivity of “if” can be analogously represented by the claim

22) if $A$ then $B$, if $B$ then $C \nVdash$ if $A$ then $C$.

This is said to be established by the invalidity of arguments like:

23) If Smith dies before the election, Jones will win.

If Jones wins, Smith will retire from public life after the election.

So, if Smith dies before the election, he will retire from public life after the election.

**`(g)`** Whereas

24) $(X \land Y) \to Z, X \models_{\mathsf{P}} Y \to Z,$

the alleged invalidity of the following example purportedly shows that the analogous fact does not hold for English:

25) If this room is getting warmer and the mean kinetic energy of the molecules of its contents remains the same, then the scientific world will be astonished.

This room is getting warmer.

So if the mean kinetic energy of the molecules of this room’s contents remains the same, then the scientific world will be astonished.

Ex. 2.25 (a) Explain how one who thinks that (5.25) is invalid could best justify his position.

(b) Explain how the following argument could be used to strengthen the case against the truth functional interpretation of "if".

If John is in Paris, then he is in France. If he is in Istanbul, then he is in Turkey. So if he is in Paris, he is in Turkey, or if he is in Istanbul, he is in France.

In other words, it is claimed that

26) [if (A and B) then C, A] ≠ if B then C.

**`(h)`** Whereas

27) $(X \to Y) \models_{\mathbb{P}} (X \land Z) \to Y$, whatever $Z$ may be,

the alleged invalidity of the following example purportedly shows that the analogous fact does not hold of English:

28) If I put sugar in this cup of tea it will taste fine.

So, if I put sugar and also diesel oil in this cup of tea, it will taste fine.

In other words, the claim is that

29) [if A then B] ≠ [if (A and C) then B], whatever C may be.

(i) Whereas

30) $\models_{\mathbb{P}} (X \to Y) \vee (Y \to X),$

it is not the case that

31) $\models$ Either (if A then B) or (if B then A).

Suppose that Peter says that there will be a third world war and Quentin denies this. Then it seems that both "If Peter is right, then so is Quentin" and also "If Quentin is right then so is Peter" are false, so that substituting these sentences in *`(31)`* leads to a falsehood (cf. Read [1988], pp. 23-6).

One who would defend the view that “if” or “if . . . then . . .” are truth functional against these charges will need some impressive resources. They will include the notion of implicature, mentioned, but not yet discussed.

I offer no separate discussion of the correspondence between “↔” and “if and only if”.

## 6 Implicature

How is one to tell whether, for example

1) Jane Austen was buried at Winchester and died in 1817

is true or not (cf. 4.17))? Clearly it would help to know where and when Jane Austen died. There can be no general answer to how we know things like this, but let’s pretend we do know that (1) correctly specifies the place and date of Jane Austen’s death. It is debatable whether this is enough to answer the question of whether (1) is true.

One way to proceed is to imagine someone addressing this remark to us. The thought irresistibly presents itself that there is something wrong. But does what is wrong consist in the remark failing to be true?

There are all sorts of ways in which a remark can sound “wrong” even if it is true; and sound “right” even if it is false. On being introduced to an ugly person, it would be wrong – morally wrong – to say

2) You are without question the ugliest person I have ever met,

even if (2), as uttered in the circumstances, would be a literal truth. Now suppose that someone enquires whether you know anything about birds, and you wish to convey, in as graphic a fashion as possible, that you know next to nothing. You say

3) I can’t tell a crane from a canary.

This, we shall suppose, is not true. Still, it can be a perfectly proper thing to say – a permissible, and readily understood, exaggeration. No one would take you quite literally.

The conclusion is that the truth of a remark is neither necessary nor sufficient for it being a right and proper one.

It is possible to *convey* something without strictly and literally *saying* it. By uttering (2) you convey that you care nothing for the other person’s feelings, though you do not say this. What is right about (3) is that it correctly conveys that you know next to nothing about birds.

The distinction is made even more graphically in a famous example. H asks S his opinion about Jones’s qualities as a philosopher. (Jones is a student of S’s, and H has every right to know S’s opinion.) S replies:

4) Jones has beautiful handwriting

and says nothing further. S conveys that Jones is a bad philosopher, but he does not say this.

Ex. 2.26 Say which if any of the following could have been used by S to convey his unflattering opinion:

(i) Either he is a good philosopher or he isn’t.

(ii) He has a beautiful wife.

(iii) He has appalling handwriting.

(iv) His handwriting is average.

In general, what are the necessary and sufficient conditions for an utterance to be usable by S, in this context, to convey his low opinion of Jones?

I once asked Gilbert Ryle whether he liked music. He replied

5) I can tell the difference between loud and soft.

Ryle conveyed that he did not like music; but this is not what he said. In *Can You Forgive Her?* Mr Bott says to Alice Vavasor:

6) The frost was so uncommonly severe that any delicate person like Lady Glencowrer must have suffered in remaining out so long. (Trollope [1864], ch. 28)

Alice knew that Mr Bott knew that Alice had been out with Lady Glencora, yet Mr Bott had made no enquiry about Alice’s health.

According to Trollope, Mr Bott thereby conveyed that Alice was not delicate (and so not upper class). But he did not say this. What is conveyed may be false even when what is said is true.

The nurse, beaming brightly, announces to the newly delivered mother

7) Congratulations! It's a baby.

The nurse conveys (presumably in jest) that there was some significant possibility of the mother having given birth to something other than a baby. But she does not say this.

Ex. 2.27 Can one say that A and thereby convey that —A? If so, give an example. If not, why not?

H. P. Grice coined the phrase “implicature” to apply to what, in such examples, is conveyed but not said.⁶ A truth may implicate something false. *`(7)`* would normally be an example of this, but any of the other cases might be examples, in appropriately altered circumstances. This possibility could be exploited by someone wanting to defend a truth functional interpretation of (1). On this view, an utterer of (1) may implicate that the burial occurred before the death, and this may be false; but all that (1) strictly and literally says is that the two events occurred, so it is true. Hence it is not after all a counterexample to the truth functionality of “and”.

Grice claimed that what he called “cancellability” is a mark of implicature, and will help us differentiate what belongs to implicature and what belongs to strict and literal saying.⁷ If A entails B, then “A, but not B” will be contradictory. Thus “Tom is a bachelor” entails “Tom is unmarried", and "Tom is a bachelor, but he's not unmarried" is contradictory. This shows that Tom has to be unmarried, if what is strictly and literally said by "Tom is a bachelor" is to be true.


By contrast, the following, uttered in the situation we envisaged for (4), is perfectly consistent:

8) Jones has beautiful handwriting – though I don't mean to suggest that he is other than an excellent philosopher.

This shows that Jones's being a bad philosopher, or being thought by S to be such, is not a necessary condition for the truth of (4), even as uttered in the special kind of context in question.

A defender of the truth functional interpretation of "and" can allow that in some sentences in which "and" occurs, something more like "and then" is implicated. But cancellability will show that it belongs to implicature only, and not to what is strictly and literally said. For example, in the circumstances envisaged for (4.13), one could quite consistently have said:

9) Mary got married and had a baby, but I'm not willing to pronounce on the correct order of these occurrences.

In place of (1) it would be quite consistent to say

10) Jane Austen died in 1817 and was buried at Winchester, but I'm not saying which happened first.

(A plausible conversational background for this case would be one in which the general topic of discussion is cases of people being buried alive. One wishes to make clear that one is carefully remaining neutral on the question of whether Jane Austen was an example.)

The phenomena we have discussed in connection with "and" can be reproduced merely by the use of separate sentences. There is little to choose between (4.13) and

11) Mary got married. She had a baby.

Putting things in this order might well implicate that the corresponding events occurred in that order. But it would be absurd to suggest that either of the sentences, or the utterance as a whole, would be false (as opposed to, say, misleading) if the birth preceded the wedding. That the same phenomenon can arise in the absence of "and", and in a context in which it cannot be attributed to the truth conditions of any expressions involved, suggests that it should not be attributed to the truth conditions of "and".


Let us now resume the essential features of an implicature defence of a truth functional interpretation, applying it to the interpretation of "and" as expressing the truth function expressed by "&amp;".

The objector claims that there are cases in which a compound has a truth value inconsistent with the truth functional interpretation. In the present case, the allegation is that conjunctions can fail to be true, even when both conjuncts are.

The defence consists in saying that a sentence which is strictly and literally true may have false implicatures. The objector, it will be claimed, has mistaken the falsity of an implicature for the falsity of the sentence itself — that is, for the falsity of what the sentence strictly and literally says. So the examples allegedly of false conjunctions with true conjuncts are really examples of true conjunctions which have false implicatures.

This summary involves some oversimplifications, which would need to be addressed by a full-scale defence. As we have seen, it cannot be quite right to say that sentences have implicatures: one test for an implicature is its cancellability, which shows that what is implicated does not belong to the content of the sentence as such. Implicature is determined by conversational context, and so is not a stable feature of the sentence, but a feature of its use on a specific occasion, within a given dialogue. As Grice presents the notion of implicature, the kind of use liable to generate implicature is a use (typically assertive) of the whole sentence; a more cautious deployment of an implicature defence would have to take into account cases in which the sentence in question is not asserted, for example, when the sentence occurs within a larger compound. Granting that "Mary had a baby and got married", used assertively on a specific occasion, may be true yet generate a false implicature, a story needs to be told about how something similar can happen when the sentence is not used assertively. For example, the following pair might be claimed to differ in truth value:

12) If Mary had a baby and got married, her parents must have been ashamed.

13) If Mary got married and had a baby, her parents must have been ashamed.

In *`(12)`*, “Mary had a baby and got married” is only a part of the larger sentence which is used in the whole speech-act: the conjunction itself is not used assertively, and so cannot generate implicature in the way Grice typically envisaged. Yet if *`(12)`* and *`(13)`* differ in truth value, the natural explanation is that their antecedents can differ in truth value. The implicature defence would need additional resources to deal with this argument for the claim that “and”, used as a sentence connective, does not always express the “&amp;” truth function.

Despite these difficulties, my own view is that “and”, used as a sentence connective, does express the same truth function as “&amp;”. The relation between “if” and “→” is more complex.

## 7 “If”: implicature in defence of the truth functional interpretation

I envisage two strategies at the disposal of the defender of the truth functional interpretation of “if”. The first is to exploit the notion of implicature to try to defuse alleged counterexamples. The second strategy, deferred until the next section, is to provide direct arguments for the interpretation.

A defence of the truth functional interpretation of “if” requires a more systematic account of implicature. Consider an utterance which, though true, would give rise to a false implicature. For example, suppose that Jones really does have beautiful handwriting, and that you utter (6.4) assertively in the envisaged circumstances. It will be entirely reasonable for your hearer to infer that you think ill of Jones as a philosopher. Suppose that in fact you think highly of him. Then, in uttering (6.4) you have spoken truly, but misleadingly. You should not have asserted (6.4). In the context, (6.4), though true, had (as I shall put it) a low degree of assertibility. One goes some way to providing an account of implicature by giving principles which determine features of an utterance which raise or lower its degree of assertibility.

One relevant feature (suggested by Grice) is that an utterance is more assertible the more informative it is, relative to the needs of the conversation. For example, if you are asked where Tom is and you know he is in the library, you should not reply


1) He is either in the library or in a lecture

despite the fact that (1) is true. (1) is less assertible, because less informative, than the equally true

2) He is in the library.

The principle is:

3) The more informative a true utterance is (relative to the conversational needs in question), the more assertible it is.

Ex. 2.28 What would be wrong with (7.3) without the parenthetical qualification?

A consequence of this principle is that very uninformative true utterances will normally have very low assertibility.

Ex. 2.29 Can you suggest an example of something which is rather uninformative but highly assertible? If so, could (7.3) be amended to allow for your example? If not, is there a way of showing that there could be no such example?

Let us apply this to the problem for the truth functional account of "if" posed by (5.10) and (5.11). Consider the argument

4) Ice floats on water. So, if ice is denser than water, it floats on water,

and the allegation that this argument is invalid (having true premise but false conclusion), whereas formalizing "if" by "→" yields a P-valid argument. Then the defence of the truth functional interpretation using *`(3)`* claims that the conclusion is not really false, and the argument is not invalid. If we think the conclusion is false, it is because we imagine it being asserted in the context of the propounding of an argument like (4). In such a context, the premise is much more informative than the conclusion, which is very uninformative. Anyone in a position to use the argument must be in a position to assert its premise. So *`(3)`* has it that, as conclusion of the argument, “if ice is denser than water, it floats on water” is highly unassertible. If anyone wrongly thinks it is false, it is because they confuse low assertibility with falsehood.


One problem with this account is that it is open to question whether *`(3)`* is true. But there is also a more internal problem. Consider

5) Ice floats on water. So, if ice does not float on water, it floats on water.

Here, again, we have an apparent counterexample to the truth functional interpretation of “if”, for we have an argument which is intuitively invalid, having true premise but false conclusion, but which would be P-valid were “if” formalized by “→”.

However, the same defence cannot be brought to bear on this case as on (4). For:

6) $\vdash_{\mathbf{P}} X \leftrightarrow (\neg X \rightarrow X).$

In other words, any sentence is equivalent to the material conditional having it as consequent and its negation as antecedent. Hence in one good sense of what it is for two sentences to be equally informative, a sense which the proponent of the truth functional interpretation of “if” cannot very well despise, the premise and conclusion of (5) are equally informative. Hence the defence of the truth functional interpretation which relies on *`(3)`* cannot be applied here: the conclusion of (5), if it is as informative as the premise, ought to be no less assertible. This casts doubt on whether the defence of *`(4)`* was legitimate. *`(4)`* and (5) appear to pose a common problem, requiring a single solution.

An alternative defence is based on the following principle:

7) The utterer of a conditional implicates that he has good grounds, of certain standard kinds, for his utterance.

Standardly, a conditional is used only when the truth or falsity of the components is not known. One standard kind of ground is that one has good evidence for a generalization of which the conditional is an instance. For example, one may well know, from general principles governing floating and density, that anything denser than water will sink in water. You may be ignorant of the density of some particular substance, say bakelite, relative to water. Still, you know from the general principle that if bakelite is denser than water, it will sink in water. The defence of the truth functional interpretation based on *`(7)`* has it that many of the apparent anomalies can be explained in terms of the falsity of implicatures relating to the grounds envisaged for the conditional.


For example, (4.33), viz.:

If this volume of water is heated to $90^{\circ}$ at some time during the coming year, this volume of water will turn to ice

will be held to implicate that there is, or that the speaker believes there is, some general connection between heating water and it turning to ice. Given that there is no such connection, the implicature is false. When people allege that (4.33) is false, they are responding to the falsity of the implicature. On the assumption that this volume of water will not be heated to $90^{\circ}$ at any time during the coming year, what (4.33) strictly and literally says is true, or so the defender of the truth functional interpretation will urge. The different approaches are marked by the fact that those who are confident of the falsity of (4.33), unlike the defender of the truth functional interpretation, feel no need to find out whether or not its antecedent is true.

The style of defence has some plausibility for a number of the alleged counterexamples to truth functionality given in §5. For example, it says something relevant to (5.14), viz.:

It is not the case that if the number three is even then it is prime. So the number three is even.

To serve as a counterexample, it is necessary that the premise be true. For this, it is necessary that

8) if the number three is even then it is prime

be false. But, the defence goes, what we are responding to when we think (8) is false is merely the false implicature that being even is in general a sufficient condition for being prime. This is only an implicature: what (8) strictly and literally says is true.

There are counterexamples about which *`(7)`* has little to say. It is hard to see how it could even address the problem posed by (5.23), viz.:

If Smith dies before the election, Jones will win.

If Jones wins, Smith will retire from public life after the election.

So, if Smith dies before the election, he will retire from public life after the election.

There may well be appropriate general grounds for the premises: for the first, that it is a two-horse race; for the second, the honourable Smith's sincere declarations. It seems that only a determination to defend a truth functional interpretation come what may would lead one to accept that the conclusion is, despite appearances, true. Likewise, *`(7)`* would appear unable to address (5.20), viz.:

If it rains, then it will not rain heavily. It will rain heavily. So it will not rain.

And it has nothing to say about the sentence discussed in connection with (5.30):

Either, if Peter is right then so is Quentin, or, if Quentin is right then so is Peter.

Ex. 2.30 Evaluate the following argument in favour of the claim that "if Smith dies before the election, he will retire from public life after the election" is false:

The truth of the antecedent would make the truth of the consequent impossible, and it is hard to see how more than this could be required for the conditional as a whole to be false.

Here is one further principle that might serve the cause of defending a truth functional interpretation of "if".

9) It is conveyed (but not said) that a conditional is “robust with respect to its antecedent”.

One principal use of conditionals is in *modus ponens* arguments: ones having the form

10) If $A$, then $B$

$A$

Therefore $B$.

For this use to be possible, it must be possible to hold both to the conditional, “if $A$ then $B$”, and to its antecedent, “$A$”. This means that it has not to be the case that were one to come to have evidence for “$A$”, one’s evidence for “if $A$ then $B$” would thereby be undermined: in short, “if $A$ then $B$” must be robust with respect to “$A$”. If a conditional were not robust with respect to its antecedent, then one could never use it in a modus ponens argument, for one could not have a body of evidence which would support both of the needed premises. (Cf. Jackson [1979], [1987]; Lewis [1986b] – postscript to Lewis [1976].)

Here is an example of failure of robustness in a different connection. Suppose in January I am convinced that:

11) John will finish his book by April, or at any rate by May.

If I learn in June that the book is still unfinished, and hence infer

12) John did not finish his book by May,

I do not combine (11) and (12) and go on to infer

13) John will finish his book by April.

Rather, I abandon (11). We can express the phenomenon by saying that (11) is not robust with respect to the falsity of its second disjunct.

Let us apply *`(9)`* to the allegedly invalid pattern of argument (5.8):

$A \models$ [if $\neg A$ then $B$], whatever $B$ may be.

If I used this to establish a conditional, it would not be robust with respect to the antecedent. For to use the argument in this way depends upon having good evidence for “A”. Hence, subsequently acquiring evidence for the antecedent of the conditional would lead me to abandon the conditional, rather than use it to infer B. We are invited to conclude that arguments of this kind are valid, though as the conclusions will be very fragile indeed with respect to their antecedents, by principle (9) they will have very low assertibility. Confusing low assertibility with falsehood, we wrongly think the conclusions are false, and so think that the pattern of argument is invalid.

**Ex. 2.31** Jackson has argued that one should sometimes assert something weaker in the interests of robustness. Suppose “A &amp; B” is something of which you are sure and is relevant to the conversational needs in question, but that all you really care about is that your audience believe A. Show how the demands of robustness will conflict with the requirement of being maximally informative.

An interesting application of *`(9)`* is to (5.20). However, it is far from clear that *`(9)`* could deal with all the alleged counterexamples: (5.23) and (5.30) again appear to be resistant.

**Ex. 2.32** Apply (7.9) to (5.20).

Perhaps what is needed is some combination of the principles we have discussed, supplemented with further principles at well. But you may be impatient: isn’t all this rather ad hoc? And in any case, how convincing is the crucial claim that we mistake low assertibility for falsehood? Let us ask ourselves not whether we would be happy to assert the sentences having low assertibility but whether we would happily believe what they say. How could assertibility enter into belief? Yet we are inclined to suppose, for example, that even if we believe that A it does not follow that we are in error if we fail to believe that if not-A then B, with respect to every B. It is not obvious that the case against the truth functional interpretation essentially involves thinking of particular assertive utterances of conditional sentences, as opposed to thinking of how things are, and ought to be, with conditional beliefs.

It is hard to find neutral ground from which to assess these issues. If they can be treated adequately, it will be on the basis of comparing the truth functional account of indicative conditionals with alternatives. I turn now to the second strategy available to the defender of the truth functionality of "if".

Ex. 2.33 What is the best response a defender of the truth functional interpretation can make to the claims related to (5.17), (5.23), (5.25), (5.28) and (5.30)?

## 8 "If": direct arguments for the truth functional interpretation

I shall consider two direct arguments for the truth functionality of "if". They both proceed by making claims about the validity of argument patterns involving "if", differing only in which argument patterns they select.

### (1) The first argument

The following argument appears valid:

1. Either the butler or the gardener did it. Therefore if the gardener didn't do it, the butler did.

Suppose, as is natural, that the first premise is equivalent to

2. (the butler did it) ∨ (the gardener did it).

Then it is equivalent to

3. (the gardener didn't do it) → (the butler did it).

Replacing the premise of *`(1)`* by *`(3)`*, the following ought also to be valid:

4. (the gardener didn't do it) → (the butler did it), therefore if the gardener didn't do it, the butler did.

Table 2.3

|  A | B | If A then B  |
| --- | --- | --- |
|  T | T |   |
|  T | F | F  |
|  F | T |   |
|  F | F |   |

Assuming that this holds generally as a matter of form, and is independent of the particular subject matter of gardeners and butlers, then we can conclude

5) Any sentence of the form “$A \rightarrow B$” entails the corresponding sentence “if $A$ then $B$”.

It is generally accepted, and seems in any case obvious, that

6) Any sentence of the form “if $A$ then $B$” entails responding sentence “$A \rightarrow B$”.

(5) and (6) together ensure that “$\rightarrow$” and “if” are equivalent they ensure the truth functionality of “if”.

The most promising way to avert the conclusion of this is to deny the validity of *`(1)`* (cf. chapters 3 and 5.2 for view would underwrite this denial).

### (2) The second argument

First premise:

7) $A$, if $A$ then $B \models B$.

This is the principle of modus ponens, and is generally uncontested. It ensures that a true antecedent and a false consequent is enough for a false conditional. If we imagine trying to construct a truth table for “if” on the lines of the truth table for “$\rightarrow$”, this fact secures the correctness of the second line of the truth table (see table 2.3)

Second premise:

8) If $[A_1, \ldots, A_n, B \models C]$ then $[A_1, \ldots, A_n \models \text{if } B \text{ then } C].$

This is a more controversial premise. It says, in effect, that if we have a valid argument for a conclusion, any one of the premises can be dropped, provided that it is made the antecedent of the conditional whose consequent is the original conclusion; and then the reduced premises will entail the new, conditional, conclusion. Let us take this principle, which might be called that of “conditional proof”, on trust for the moment, and show how it would establish the remaining properties needed for the truth functionality of “if”. Later we shall see how one might argue for the principle of conditional proof itself.

Let us recall two results from chapter 1: (1.6.5), viz.:

If $[A_1, \ldots, A_n \models C]$ then $[A_1, \ldots, A_n, B \models C]$, whatever $B$ may be and (1.6.7), viz.:

If $C$ is among the $A_1, \ldots, A_n$, then $[A_1, \ldots, A_n \models C].$

As a special case of the latter, we have

9) $B \models B$.

So, using (1.6.5), we have

10) $B, A \models B$.

So, by *`(8)`*, we have

11) $B \models$ if $A$ then $B$.

This shows that a true consequent is sufficient for a true conditional, establishing the first and third lines of the table. Our table now becomes table 2.4.

Ex. 2.34 Explain how (8.11) can be used to establish that a true consequent is sufficient for a true conditional.

Table 2.4

|  A | B | If A then B  |
| --- | --- | --- |
|  T | T | T  |
|  T | F | F  |
|  F | T | T  |
|  F | F |   |

Table 2.5

|  A | B | If A then B  |
| --- | --- | --- |
|  T | T | T  |
|  T | F | F  |
|  F | T | T  |
|  F | F | T  |

Another result from chapter 1 is (1.6.8), viz.:

If $A_1, \ldots, A_n \models$, then $A_1, \ldots, A_n \models B$, whatever $B$ may be.

This says that if the premises of an argument are inconsistent, then the argument is valid, no matter what its conclusion is. Hence we have:

12) $B, \neg B \models A$.

So by *`(8)`*:

13) $B \models$ if $\neg B$ then $A$.

This establishes that the falsity of the antecedent is enough for the truth of a conditional, and so establishes the third (again!) and fourth lines of the table. We now have the complete table for “if $A$ then $B$” (table 2.5). We can conclude that *`(7)`* and *`(8)`* between them entail that English conditionals expressed by “if . . . then . . .” are truth functional, and express the same truth function as “$\rightarrow$” (cf. Hanson [1991]). The question now is whether *`(7)`* and *`(8)`* themselves can be justified.

(7), expressing modus ponens, is hardly ever questioned, so I shall assume that we can accept it without further ado. (8), the principle of conditional proof, is more controversial, so let us see if we can find an argument for it. It will be easier if we abbreviate “$A_1, \ldots, A_n$” as “$A$”, and so write (8) as follows:

14) if $A, B \models C$, then $A \models$ if $B$ then $C$.

The antecedent of this conditional means (using an equivalent of the definition of “$\models$” in chapter 1.3):

15) It is logically necessary that, if $A$ and $B$ are true, then so is $C$.

So:

16) It is logically necessary that, if $A$ is true, then, if $B$ is true, so is $C$.

So:

17) It is logically necessary that, if $A$ is true, then if $B$ then $C$ is true.

But this means:

18) $A \models$ if $B$ then $C$. QED.

The principles of reasoning involved seem to be modest. But they have been firmly resisted by theorists who contest the truth functional interpretation of “if”. Until we examine alternative theories of “if”, our conclusion has to be simply that such theories will have to provide good reasons for thinking that the reasoning (14) to (17) above is unsound.

Ex. 2.35 Which step in (8.14) to (8.17), if any, do you regard as suspect, and why?

We can summarize the conclusions of §5 and §8 as follows: there are apparently compelling arguments for the conclusion that “if” is not truth functional, and apparently compelling arguments for the conclusion that it is. Appearances must deceive. Some attempts to say how they deceive are considered in chapter 3.


In considering the use of $\mathbf{P}$-validity in the investigation of validity in English, we will explore the consequences both of "if" being truth functional and of it not being truth functional.

## 9 Non-truth functionality in English

To deepen understanding of claims to the effect that some English expression is a truth functional sentence connective, let us examine claims to the effect that an expression is a sentence connective, but one which is not truth functional.

### (1) John believes that

This expression seems to be syntactically like "not": it seems to be a *unary sentence connective*, taking a sentence like "the earth is flat" to form a new sentence, "John believes that the earth is flat". So the expression appears to function as a sentence connective (contrast chapter 4.16). If it is a sentence connective, it is certainly not truth functional: John may have both true and false beliefs, so the truth value of "John believes that $A$" is not a function of the truth value of "$A$".

### (2) Because

On at least some occurrences, "because" seems to function as a *binary sentence connective* (one which takes two sentences to make a sentence). For example

1) John shot Robert because Robert betrayed him.

If we take this appearance at face value, the straightforward response is to see "John shot Robert" (abbreviate to A) and "Robert betrayed John" (abbreviate to B) as the two components, in which case we are forced to regard "because", thus used, as non-truth functional. This view could be vindicated by attempting to construct a truth table in which we envisage various theoretically possible truth

Table 2.6

|  A | B | A because B  |
| --- | --- | --- |
|  T | T | ?  |
|  T | F | F  |
|  F | T | F  |
|  F | F | F  |

values for the components, and ask, with respect to each, whether (1) would then be true or false (table 2.6). A necessary condition for the truth of “because” sentences is the truth of both components. But this is not sufficient. If it were, the result of inserting “because” between arbitrary truths would always be a truth, and this is plainly not so.

Ex. 2.36 Give an example of a false “because” sentence whose components are both true.

Frege ([1892b], pp. 76–7) suggested that “because” sentences are truth functional, but are not a truth function of the components we have so far identified. Discussing the sentence

2) Because ice is less dense than water, it floats on water,

he suggested that there is a concealed component, in addition to “ice is less dense than water” and “ice floats on water”, namely

3) Whatever is less dense than water floats on water.

The truth function is simply that of conjunction, applied to the three components.

A difficulty with this suggestion (and I think the difficulty is insuperable) is that there is no systematic way of eliciting the concealed component. What stands to (1) as (3) does to (2)? It would be absurd to suggest that (1) entails that whoever Robert betrays shoots him, or that whoever betrays John is shot by him, or that whoever betrays anyone is shot by the betrayed.

A more promising suggestion is that "because" is not really a sentence connective at all, but rather functions, somewhat analogously to "therefore", to mark an act of inference. We saw in chapter 1.5 that something like "A therefore B" cannot be evaluated as true or false. Rather, we have to ask whether the argument thereby presented is valid. "Therefore" is not a sentence connective, since what is produced by placing it between two sentences is not itself a sentence, something capable of having a truth value. Similarly, perhaps "because" forms not a sentence, but something more like an argument. (Very often, as in (1), one would be expected to evaluate the argument by inductive rather than deductive standards.)

**Ex. 2.37** Explain how, contrary to what is said in the text, a Frege-style concealed component truth functional analysis might be applied to "A therefore B".

How could this suggestion be tested? One relevant point is that certain complexes containing "because" appear not to operate in the way one expects of genuine sentences. For example, if $\xi$ is a sentence connective, then "if $A$, then $(B \xi C)$" is a conditional, and on every account of conditionals neither the truth of $B$, nor of $C$, nor of $B \xi C$ can be necessary for the truth of the conditional. But consider

4) If John comes to the party, then (Mary will leave because she has quarrelled with him).

It would seem that (4) is true only if Mary has quarrelled with John, and this would be hard to explain if "because" were a sentence connective.

**Ex. 2.38** Could it be persuasively argued that, provided the scope-indicating brackets are held firmly in place, the truth of (9.4) does not require the truth of "Mary quarrelled with John"?

### **(3) But**

I hold that "but" differs in meaning from both "and" and "&amp;". This does not show that "but" does not express the conjunction truth

function, for there can be differences of meaning which do not impinge on truth. When "but" functions as a sentence connective (which it does not always do) it expresses precisely the conjunction truth function – that expressed by "$\&$". The only doubt is whether the truth of both $A$ and $B$ is enough for that of "$A$ but $B$". This doubt is assuaged by the reflection that it is correct to infer from the falsehood of "$A$ but $B$" that at least one of $A, B$ is false.

Ex. 2.39 Give an example of an occurrence of "but" in which it is not a sentence connective.

The additional component in the meaning of "but", as opposed to "and", is reflected in the fact that one who asserts that $A$ but $B$ represents himself as supposing that in the context there is some contrast between the truth of $A$ and that of $B$, something surprising, poignant, or worthy of special note or emphasis in the fact that both are true. Sometimes the element of surprise, or whatever, derives from $A$ itself, as in the stock example "She was poor but honest". Sometimes it derives from something else, as in "The best smoked salmon comes from Scotland but unfortunately it's rather expensive" (cf. Jackson [1981], §3).

### (4) When

Consider

5) When beggars die, there are no comets seen.

The following argument might be used to show that "when", on such an occurrence, is a non-truth functional sentence connective: "Beggars die" and "There are no comets seen" are both declarative, indicative sentences, capable of being used self-standingly, and each evaluable for truth and falsehood. So "when" is a sentence connective. But it is not truth functional, since the truth value of the two components leaves undetermined the truth value of the whole. Equally, it fails the substitution test. If (5) is true, it does not remain so when "Comets are seen" replaces "Beggars die", yet these components have the same truth value.

Ex. 2.40 Explain why the truth value of (9.5) is not a function of the truth values of "Beggars die" and "No comets are seen".

The argument is fallacious, for, as they occur in (5), "Beggars die" and "There are no comets seen", are not genuine self-standing sentences. (5) means something like

6) Any time at which beggars die is not a time at which comets are seen.

Here there is no plausibility to the idea that there are two sentential components. Used self-standingly, "Beggars die" means something like

7) Every beggar dies sometime;

and "There are no comets seen" means something like

8) No comets are visible now/ever,

context determining the choice of "now" or "ever". It is plain that this is not what the expressions mean as they occur in (5).

"When", as it occurs in (5), is thus not an example of a non-truth functional sentence connective, since in that occurrence it is not an example of a sentence connective (cf. Frege [1892b], p. 72). This does not preclude there being other sentences in which it is a genuine sentence connective.

Ex. 2.41 (a) Give an example of a sentence in which "when" occurs as a genuine sentence connective. Is "when" truth functional, as it occurs in your example?

(b) For each of the following expressions, say whether it always, sometimes, or never occurs as a sentence connective. If always or sometimes, say whether it expresses a truth function on these occurrences, and, if so, which. Use examples to justify your answers.

(i) Iff

(ii) It is surprising that

(iii) It is true that

(iv) It is probable that

116 2 - Truth functionality

|  (v) | Unfortunately  |
| --- | --- |
|  (vi) | Fortunately  |
|  (vii) | Science shows that  |
|  (viii) | Although  |
|  (ix) | Unless  |
|  (x) | Hopefully  |
|  (xi) | Even  |
|  (xii) | Yet  |
|  (xiii) | Not only . . . but also . . .  |
|  (xiv) | Hastily (compare chapter 4.6)  |
|  (xv) | In the park  |
|  (xvi) | Before (enthusiasts may wish to compare the discussion in Davidson [1970a], pp. 138–9)  |
|  (xvii) | Possibly  |
|  (xviii) | Despite the fact that.  |

## 10 From P-validity to validity

Logic is the study of reasoning, and of one vital feature that reasoning should possess, namely validity. There are two ways in which the language $\mathbf{P}$ may help us to understand validity in English: first, it may enable us to attain useful generalizations about validity in English, and offer ways of testing for validity in English in doubtful cases; secondly, the definition of $\mathbf{P}$-validity may have virtues lacked by the original definition of validity in chapter 1.

In §3 we discussed some ways of formalizing English arguments, but we left two questions with at best incomplete answers. One was: what can be inferred from the fact that an argument’s logical form is $\mathbf{P}$-valid? The other was: what can be inferred from the fact that an argument’s logical form is not $\mathbf{P}$-valid?

With some qualification, the answer to the first question is that one can infer the validity of the English. What we have to show is that if a $\mathbf{P}$-argument $\phi$ is $\mathbf{P}$-valid and is an *adequate* formalization of an English argument $\psi$, then $\psi$ is valid.

The adequacy of the formalization ensures that, where $\phi'$ is the argument recovered from $\phi$ by applying the correspondences associated with the formalization, $\phi'$ says the same as $\psi$. The notion of “saying the same” that is required here is that the sentences of $\phi'$ should have the same truth conditions as the corresponding sentences in $\psi$. Validity can be defined in terms of truth conditions, and if two arguments are related as $\psi$ and $\phi'$ then, necessarily, both or neither is valid. So it will be enough if we can show that if $\phi$ is $\mathbf{P}$-valid then $\phi'$ is valid.


A necessary condition for there being any adequate formalizations is that the $\mathbf{P}$-connectives make the same contribution to truth conditions as the corresponding English expressions. We saw that this was doubtful in the case of “$\rightarrow$” and “if”. Let us suspend this doubt for the moment. Then the following argument establishes what is needed:

1) (i) Suppose $\phi$ is $\mathbf{P}$-valid.
(ii) Then every interpretation upon which the premises of $\phi$ are true is one upon which the conclusion is true.

(iii) Hence whatever may be the truth values of the components of $\phi'$, if the premises of $\phi'$ are true, so is the conclusion.

(iv) Hence, of logical necessity, all the conditions under which the premises of $\phi'$ are true are conditions under which its conclusion is true.

(v) Hence, the truth conditions of the premises of $\phi'$ are contained within those of the conclusion.

(v) is equivalent to the claim that $\phi'$ is valid, in the sense of $\vDash$.

One crucial step is from (ii) to (iii). This essentially requires that every English expression in $\phi'$ corresponding to a constant in $\phi$ expresses the same truth function as the $\mathbf{P}$-constant. Those who dispute that “if” is truth functional will dispute this step.

Another crucial step is that from (iii) to (iv). The former makes no explicit mention of logical necessity, the latter does. How can the intrusion of this notion be justified?

Consider a very simple argument, like

2) Either John is happy or Mary is. But John is certainly not happy. Therefore Mary is happy.

No doubt there are all sorts of intrinsically different conditions under which the premises are true. For example, John’s unhappiness might stem from frustrated ambition, misfortune in love, or whatever. (iii) appears not to allude to all these possibly different conditions, yet (iv) does: it speaks without qualification of all the conditions under which the premises are true.


Conditions, like anything else, can be classified either coarsely or finely. It is not that (iii), as applied to (2), fails to speak to some conditions under which the premises are true; rather, it classifies these conditions rather coarsely. In this example, they in effect fall into a single category: those in which “John is happy” is false (as required for the truth of the second premise), and in which “Mary is happy” is true (as required for the truth of the first premise, given what is required for the truth of the second). However the conditions in this category may vary, they all have the common property of verifying the conclusion. Hence all the conditions – all logically possible conditions – under which the premises are true are conditions under which the conclusion is true.

If “if” is not truth functional, (iii) does not follow from (ii). We will continue to assume that, even so, “if” entails “→”, and that it is only the converse entailment that fails. In other words, an “if” sentence is stronger than the corresponding “→” sentence.

There are two cases, which have to be treated separately:

(a) The English argument contains “if” at most in the premises. In this case, the inference from P-validity to validity goes through. The reason is that the P-premises will be weaker than the English premises, and strengthening an argument’s premises cannot invalidate it (cf. 1.6.5).

(b) The English argument contains “if” in the conclusion. This divides into a number of subcases, depending on whether “if” is or is not the dominant connective. Let’s just consider the case in which it is. Then the P-conclusion is weaker than the English conclusion. That the P-premises establish a weaker conclusion leaves open that they might not be strong enough to establish the stronger one. So there is no correct inference from P-validity to validity.

If a P-argument is invalid, there are three possibilities for the validity of the English argument:

3) It is valid in virtue of its P-logical form.

4) It is valid, but not valid in virtue of its P-logical form.

5) It is invalid.

I shall illustrate these possibilities in turn.

The first possibility is illustrated by (3.8): we saw that the formalization of an argument which is not only valid, but valid in virtue of its P-logical form, may be adequate yet invalid, through failing to be deep enough. In general, any argument with $n$ premises can be formalized by an invalid P-argument which uses $n$ sentence letters to correspond to the premises, and a further distinct letter to correspond to the conclusion.

The second possibility, (4), is illustrated by (3.19):

All football supporters are interested in sport. Some football supporters are hooligans. So some hooligans are interested in sport.

The argument is valid, but its validity depends upon expressions which are not P-logical constants, "all" and "some".

The third possibility, (5), is illustrated by (3.14):

If you are good at mathematics, you will find logic easy. But you are not good at mathematics. So you'll find logic hard.

P-logic offers us, naturally enough, no way of differentiating between cases (4) and (5), so the strongest conclusion we can reasonably draw from the P-invalidity of the deepest P-formalization we can find is that validity in virtue of P-logical form is a property which the formalized English argument lacks.

|  Ex. 2.42 Say what is wrong with the following reflections on some English argument, call it φ:  |
| --- |
|  The deepest P-formalization of φ is not valid in P-invalid.  |
|  Hence φ is not valid in virtue of its P-logical form.  |
|  Hence, in virtue of its P-logical form, φ is invalid.  |

The definition of validity offered in chapter 1 used a notion which could do with elucidation: that of it being logically impossible for all the premises to be true, yet the conclusion false. The definition of P-validity dispenses with this notion, and employs instead the notion of interpretation.

Generalizing from the remarks adduced to support the move from (iii) to (iv) in (1), one way to classify the logical possibilities for the truth of a sentence dominated by a truth functional sentence connective is according to the truth values for the components which determine the sentence itself as true. All conditions for the truth of the sentence will be embraced by this classification, though there are finer classifications available which this one ignores. The notion of a P-interpretation thus gives a partial elucidation of the notion of logical impossibility (or logical necessity) used in the definition of validity in chapter 1. Interpretations mirror logical possibilities. A sentence whose formalization is true on no interpretation represents a logical impossibility. A sentence whose formalization is true on all interpretations represents a logical necessity.

We can draw a stronger conclusion: if an English argument's formalization is valid, the argument itself is not merely valid, but formally so. This is because its validity depends only upon the meanings of the logical constants (the expressions corresponding to the P-connectives) and the pattern of occurrence of the sentences.

A traditional aim of logic has been to render mechanical the determination of the validity of arguments. P satisfies this aim. One can construct truth tables to check mechanically for the P-validity of P-arguments. There are also many computer programs which will do the same job.⁸

Finally, $\models_{\mathbb{P}}$ has the general properties ascribed to $\models$ in chapter 1.6.

Ex. 2.43 Using the definition of a P-interpretation, establish the following:

(i) If $[X_1, \ldots, X_n \models_{\mathbb{P}} Z]$ then $[X_1, \ldots, X_n, Y \models_{\mathbb{P}} Z]$, whatever $Y$ may be. (Compare (1.6.5).)

(ii) If $[X_1, \ldots, X_n \models_{\mathbb{P}} Z]$ and $[Y_1, \ldots, Y_k, Z \models_{\mathbb{P}} W]$, then $[X_1, \ldots, X_n, Y_1, \ldots, Y_k \models_{\mathbb{P}} W]$. (Compare (1.6.6).)

(iii) If $Z$ is among the $X_1, \ldots, X_n$, then $[X_1, \ldots, X_n \models_{\mathbb{P}} Z]$. (Compare (1.6.7).)

(iv) If $[(X_1, \ldots, X_n) \models_{\mathbb{P}}]$, then $[X_1, \ldots, X_n \models_{\mathbb{P}} Y]$, whatever $Y$ may be. (Compare (1.6.8).)

(v) If $[\models_{\mathbb{P}} X]$, then $[Y_1, \ldots, Y_n \models_{\mathbb{P}} X]$, whatever $Y_1, \ldots, Y_n$ may be. (Compare (1.6.9).)


#### Notes


¹ “$\neg$” and “$\sim$” (the last being a tilde properly so-called) are sometimes used in place of “$\neg$”; “$.$”, “$\land$” or simple juxtaposition in place of “$\&$”, “$\supset$” instead of “$\rightarrow$”, and “$\equiv$” instead of “$\leftrightarrow$”. For a fuller list of variants, see Kirwan [1978], p. 280.

² Where a sentence connective $\mathfrak{q}$ takes some number $n$ of sentences to make a sentence, let’s call $\mathfrak{q}$ an $n$-ary sentence connective. We can write an arbitrary sentence resulting from applying $\mathfrak{q}$ to the appropriate number of sentential components, $x_1, \ldots, x_n$, as $\mathfrak{q}(x_1, \ldots, x_n)$. An $n$-ary truth function is a function from $n$-ary sequences of truth values to a truth value. An $n$-ary sentence connective, $\mathfrak{q}$, expresses an $n$-ary truth function $f$, iff $f$ is an $n$-ary truth function and for every sentence $\mathfrak{q}(x_1, \ldots, x_n)$, where $\Sigma$ is the sequence of truth-values possessed by $x_1, \ldots, x_n$, $f(\Sigma)$ is the truth value of $\mathfrak{q}(x_1, \ldots, x_n)$.

² Where a sentence connective $\xi$ takes some number $n$ of sentences to make a sentence, let’s call $\xi$ an $n$-ary sentence connective. We can write an arbitrary sentence resulting from applying $\xi$ to the appropriate number of sentential components, $x_1, \ldots, x_n$, as $\xi(x_1, \ldots, x_n)$. An $n$-ary truth function is a function from $n$-ary sequences of truth values to a truth value. An $n$-ary sentence connective, $\xi$, expresses an $n$-ary truth function $f$, iff $f$ is an $n$-ary truth function and for every sentence $\xi(x_1, \ldots, x_n)$, where $\Sigma$ is the sequence of truth-values possessed by $x_1, \ldots, x_n$, $f(\Sigma)$ is the truth value of $\xi(x_1, \ldots, x_n)$.

³ Officially, “s” is not a P-letter, but let it be regarded as an abbreviation of “p”; similarly for “r”, “u”, etc.

⁴ The best putative examples of exclusive disjunction tend to involve rather complex and poorly understood constructions, like the one in (27). It may well be that it is these constructions, rather than “or”, which are responsible for any exclusivity. For an illuminating account, see Higginbotham [1988], esp. pp. 226–7.

5 For a justified protest at the standard treatment of “A only if B” as an idiomatic variant of “if A then B”, see McCawley [1981], pp. 49–54.

⁶ Grice’s phrase was “conversational implicature”. He distinguished this from “conventional implicature”. Arguably, some of the implicatures associated with the assertion of conditionals (though not, I think, conjunctions) should count as conventional rather than conversational. (See Jackson [1981].) To allow room for this alternative (which I do not explicitly discuss), I have mostly dropped the qualifier “conversational”.

⁷ In Grice, cancellability is a sign of conversational, but not of conventional, implicature. See previous note. For example, Grice suggested that “and” and “but” agree in expressing the same truth function, but differ in that “but” has some kind of contrastive conventional implicature (see also below, §9), which is, accordingly, not cancellable.

⁸ P is decidable, that is, there exists a decision procedure for it (cf. e.g. Kirwan [1978], pp. 169 ff.).