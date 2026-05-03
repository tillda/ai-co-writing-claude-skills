---
book: "Logical Forms"
title: "Chapter 04 Quantification"
chapter_number: "4"
chapter_name: "Quantification"
author: "Mark Sainsbury"
table_of_content: |
  1 The classical quantificational language
---

# 4 Quantification

This chapter introduces a richer artificial language, **Q**, capable of representing *quantifiers* like “all” and “some”. Readers already familiar with this language should merely skim the first two sections, to check on the terminology and symbolism used here. (Of particular importance is a grasp of the precise notions of interpretation and **Q**-validity.) Later sections consider problems of formalizing English in **Q**.

## 1 The classical quantificational language

In **P**, the smallest unit was the sentence-letter. English sentences are composed of parts that are not themselves sentences, and this finer structure is sometimes relevant to validity. A sentence like “John runs” is composed of a *name*, “John”, and a *verb*, “runs”, yet the deepest **P**-formalization of this sentence is simply a **P**-letter, in which this structure is obscured. The valid argument

**`1)`** John runs; so someone runs

has no more revealing **P**-logical form than

**`2)`** $p; q$

which is plainly not **P**-valid.

The language **Q** is to include **P**, so that every **P**-sentence automatically counts as a **Q**-sentence, but is also to include further devices to reach structures **P** cannot reach.

Sentences of **Q** are composed of the following kinds of symbol:

Sentence-letters: $p, q, r, p', \ldots$ etc.: These are exactly as in $\mathbf{P}$.

Name-letters: $\alpha, \beta, \gamma, \alpha', \ldots$ etc.: These will be used to correspond to ordinary English names like “Ronald Reagan”.

Predicate-letters: $F, G, H, F', \ldots$ etc.: These will be used to correspond to English verbs, like “runs”, some expressions involving adjectives, like “is hungry”, and some involving nouns, like “is a man”. “John runs” will be $\mathbf{Q}$-formalized as “$F\alpha$” (to be read “$\alpha$ is $F$” or “$F$ of $\alpha$”), and so will “John is hungry” and “John is a man”.

Predicates: $=$: The only $\mathbf{Q}$-predicate (as opposed to predicate-letter) is “$=$”, the sign for identity (being the same as); we can formalize “Hesperus is Phosphorus” as “$\alpha = \beta$”.

Variables: $x, y, z, x', \ldots$ etc.: Their role will be explained shortly.

Operators: the sentence-connectives of $\mathbf{P}$, together with “$\forall$” (the universal quantifier, corresponding to “all” or “every”) and “$\exists$” (the existential quantifier, corresponding to “some” or “a”).

Giving the meaning of the operators new to $\mathbf{Q}$ (as opposed to the sentence connectives carried forward from $\mathbf{P}$) will be deferred until the basic ideas of how the language works have been introduced informally.

A predicate is an expression which takes one or more names to form a sentence. “Is a man” is a predicate which takes one name (e.g. “John”) to form a sentence (“John is a man”). “Loves” is a predicate which takes two names (e.g. “John” and “Mary”) to form a sentence (“John loves Mary”). “Is between . . . and . . .” is a predicate which takes three names (e.g. “Austin”, “San Antonio” and “Waco”) to form a sentence (“Austin is between San Antonio and Waco”). The number of names a predicate takes to form a sentence is called its degree. “Runs” is of degree 1, “loves” of degree 2, “is between . . . and . . .” of degree 3. Every predicate and predicate-letter of $\mathbf{Q}$ is stipulated to have some one fixed degree. (In a fully explicit notation, we could superscript every predicate and predicate letter with its degree, e.g. writing “$F^3$” for a predicate-letter fit to formalize a predicate of degree 3. We adopt the more flexible policy of letting predicate-letters take on whatever degree is appropriate to the task in hand.) The notion of a predicate makes no distinction among categories which traditional grammar distinguishes (e.g. verbs, nouns, adjectives) and includes expressions which traditional grammar does not recognize (e.g. “is between . . . and . . .”).

Ex. 4.1 What is the degree of “=”?

The atoms of $\mathbf{Q}$ are predicates or predicate-letters, combined with an appropriate number of names (the number equals the degree of the predicate or predicate-letter). Examples of atoms which formalize the three sentences mentioned in the last paragraph are “$F\alpha$”, “$F\alpha\beta$”, “$F\alpha\beta\gamma$”. In the first example, “$\alpha$” corresponds to “John”, and “$F$” to the degree-1 predicate “is a man”; in the second, “$\alpha$” corresponds to “John”, “$\beta$” to “Mary”, and “$F$” to the degree-2 predicate “loves”; in the third, “$\alpha$” corresponds to “Austin”, “$\beta$” to “San Antonio”, “$\gamma$” to “Waco” and “$F$” to the degree-3 predicate “is between . . . and . . .”.

The atoms can be compounded using the sentence connectives just as if they were $\mathbf{P}$-letters. Thus all of the following are $\mathbf{Q}$-sentences:

$$
\begin{array}{l}
F\alpha \rightarrow G\beta \\
(H\alpha\beta \land F\alpha) \vee p \\
F\gamma\alpha\beta \rightarrow \alpha = \beta.
\end{array}
$$

It remains to introduce the role of quantifiers and variables. Physicalists wish to affirm that everything is physical. They could use any of the following English, or more or less English, sentences:

Everything is physical.

Take anything you like, it is physical.

For all things, $x$, $x$ is physical.

<span class="mathjax_ignore">The standard &#36;\mathbf{Q}&#36;-formalization of the English is more like the last of these variants:</span>

**`3)`** $\forall x Fx$

read “for all $x$, $F$ of $x$”. Here the quantifier “$\forall$” corresponds roughly to “for all things”, and “$F$” corresponds to “physical”. The variable, “$x$”, plays something like the role of the pronoun “it” in “Take anything you like, it is physical”. “Something is physical” is formalized

**`4)`** $\exists x Fx$.

(*`3)`* and (*`4)`* are called, respectively, a universal quantification and an existential quantification. By contrast,

**`5)`** $\forall xFx \rightarrow \exists xFx$

is a conditional and neither a universal nor an existential quantification. This is because “$\rightarrow$” has wider scope than either quantifier, and so is the *dominant operator*. (Compare the definition of scope in (2.1.6).)

We can now give a fuller account of what it is to be Q-sentence:

**`6)`** $X$ is a $\mathbf{Q}$-sentence iff

**`(i)`** $X$ is a sentence-letter or

**`(ii)`** $X$ is an atom (a predicate or predicate-letter of degree $n$ combined with $n$ names) or

**`(iii)`** there are Q-sentences $Y$ and $Z$ and a variable $\nu$ not occurring in $Y$ such that $X$ is one of

a) $\neg Y$

b) $(Y \land Z)$

c) $(Y \lor Z)$

d) $(Y \to Z)$

e) $\forall \nu Y^{\star}$

f) $\exists \nu Y^{\star}$ (where $Y^{\star}$ results from $Y$ by replacing at least one occurrence of a name by $\nu$).

We can show that (*`3)`* and (*`4)`* are Q-sentences as follows: "$F\alpha$" is a Q-sentence, being an atom; it does not contain "$x$"; "$Fx$" results from "$F\alpha$" by replacing at least one occurrence of a name by "$x$"; then (6iii) and (6iii) respectively entail that placing "$\forall x$" or "$\exists x$" before "$Fx$", forming (*`3)`* and (*`4)`*, yields a Q-sentence. Given this, (6iii) tells you that (*`5)`* is a Q-sentence.

**`7)`** $\exists x \forall y Fxy$

is also a Q-sentence; we must see it as built up in stages. Starting with, say, "$F\alpha\beta$", we see that "$\forall y F\alpha y$" is a Q-sentence, and from this it follows that (*`7)`* is also.

**`8)`** $\exists y \forall y Fyy$

is not a Q-sentence, as we can see by trying the same pattern of construction. "$F\alpha\beta$" is a Q-sentence, so "$\forall y F\alpha y$" is also a Q-sentence, as before. But we cannot go on to infer that (*`8)`* is, since "$\forall y F\alpha y$" contains "$y$", so the condition at the beginning of (6iii) is not met.
## 2 Interpretations and validity

An interpretation of $\mathbf{P}$ is an assignment of truth values to all $\mathbf{P}$-letters. The definition of the sentence connectives ensures that every interpretation of $\mathbf{P}$ determines a truth value for every sentence of $\mathbf{P}$, not just the sentence-letters. We can see the process of interpretation as containing two elements: the assignment of entities (here, truth values) to the simple expressions (the letters); and rules or definitions which bring it about that assignments to the simple expressions have determinate consequences for all the sentences.

$\mathbf{P}$-validity, we saw in **`(2.1.5)`**, is defined in terms of interpretations as follows:

An argument in $\mathbf{P}$ is $\mathbf{P}$-valid iff every interpretation upon which all the premises are true is one upon which the conclusion is true.

The notion of *interpretation of $\mathbf{Q}$* is designed to play an essentially similar role in the definition of $\mathbf{Q}$-validity. Each $\mathbf{Q}$-interpretation is associated with a specific domain of entities. These are, intuitively, the objects the language talks about. In interpreting natural language, we may need to consider different domains in different contexts. If, as a physicalist, I say “Everything is physical”, then I mean to speak of absolutely everything, or at least of all concrete things. But if, in a lecture, I say “There’s no more chalk”, the domain is presumably restricted to the objects in the room, or to hand: I say of all of these that none is chalk, and I do not say that no object in the whole wide world is chalk. In defining domains of interpretation for $\mathbf{Q}$, the only restriction we place is that every domain contains at least one object. The stipulations with regard to the simple expressions are as follows:

**`1)`** In any interpretation of $\mathbf{Q}$, with respect to any domain, $D$:

each sentence-letter is assigned a truth value (just as in $\mathbf{P}$);

each name-letter is assigned one object in $D$ (e.g. “$\alpha$” might be assigned Ronald Reagan);

each predicate-letter of degree $n$ is assigned a set of $n$-tuples ($n$-membered sequences) of objects in $D$ (e.g. if “$F$” is of degree 2, some interpretation will assign to it a set of ordered pairs (2-membered sequences) such that the first member of each pair loves the second);

“$=$” is assigned the set of ordered pairs of members of $D$ such that in each pair the first object is the same thing as the second; variables are not assigned anything.

Expressions of the form “$i(\ldots)$” can be used to denote what some $\mathbf{Q}$-interpretation, $i$, assigns to some expression $(\ldots)$. Instead of saying that $i$ assigns Ronald Reagan to “$\alpha$”, we can say: $i(\alpha) = \text{Ronald Reagan}$.

In virtue of the rules for the operators, an interpretation of the simple expressions determines a truth value (relative to that interpretation) for every $\mathbf{Q}$-sentence. (For the sentence connectives, these are just the rules from $\mathbf{P}$, but they are restated for completeness.) A preliminary notion:

The expression “$X_{\nu}^{n}$” is to be read “the result of replacing every occurrence of the variable $\nu$ in $X$ by the first name-letter $n$ not occurring in $X$”.

Talk of the first name-letter is to ensure that there is a unique result of the transformation. It presupposes some conventional (e.g. alphabetical) ordering of the name-letters. For example, if $X$ is $G\alpha x$, then $X_{\nu}^{x}$ is $G\alpha\beta$.

**`2)`** (i) $\neg X$ is true upon an interpretation iff $X$ is false upon that interpretation.

**`(ii)`** $(X \land Y)$ is true upon an interpretation iff $X$ is true upon that interpretation and so is $Y$.

**`(iii)`** $(X \lor Y)$ is true upon an interpretation iff $X$ is true upon that interpretation or $Y$ is true upon that interpretation.

(iv) $(X \to Y)$ is true upon an interpretation iff $X$ is false upon that interpretation or $Y$ is true upon that interpretation.

(v) An atom is true upon an interpretation whose domain is $D$ iff the sequence of the object(s) from $D$ assigned to the name-letter(s) by the interpretation belongs to the set it assigns to the predicate or predicate-letter; it is false iff the sequence does not belong to the set.

(vi) $\forall \nu X$ is true upon an interpretation whose domain is $D$ iff $X_{\nu}^{n}$ is true upon that interpretation, and also upon every other interpretation whose domain is $D$ and which agrees with that one except in point of what is assigned to $n$; otherwise it is false. 

If we say that an $n$-variant of $i$ is an interpretation which agrees with $i$ on its domain and on all its assignments except, perhaps, that to $n$, we can abbreviate this condition as follows: 

$\forall \nu X$ is true upon an interpretation, $i$, whose domain is $D$ iff $X_{\nu}^{n}$ is true upon every $n$-variant of $i$; otherwise it is false.

**`(vii)`** $\exists \nu X$ is true upon an interpretation, $i$, whose domain is $D$ iff $X_{\nu}^{n}$ is true upon some $n$-variant of $i$; otherwise it is false.

I will offer some explanation of the Q-specific clauses (v), (vi) and (vii).

For (v), consider an atom, say “$G\beta$”. Suppose that an interpretation assigns the set of 1-membered sequences whose members are presidents of the USA to “$G$” and Ronald Reagan to “$\beta$”. Then “$G\beta$” is true upon this interpretation, since the 1-membered sequence $\langle\text{reagan}\rangle$ does belong to the set the interpretation assigns to “$G$”. A given Q-sentence may be true upon one interpretation, false upon another. Consider an interpretation which assigns Reagan to “$\beta$” but the set of 1-membered sequences each of whose members is a Chinese emperor to “$G$”. “$G\beta$” is false upon this interpretation.

For the point of the talk of sequences in (v), consider the Q-sentence “$F\alpha\beta$” and an interpretation $i$ which assigns to “$F$” the set of ordered pairs (2-membered sequences) such that the first member of each pair loves the second. Suppose that the interpretation assigns John to $\alpha$ and Mary to $\beta$: in shorthand, suppose that $i(\alpha) = \text{John}$ and $i(\beta) = \text{Mary}$. Then (v) rules that $i(F\alpha\beta)$ is true iff the ordered pair $\langle\text{john, mary}\rangle$ belongs to $i(F)$, that is, iff John loves Mary. Order is crucial here: it may be that $\langle\text{john, mary}\rangle$ belongs to $i(F)$, yet $\langle\text{mary, john}\rangle$ does not.

Turning to (vi), intuitively we want to say that a universal quantification in English, say “Everything is physical”, is true just on condition that “physical” is true of everything. Applying this to $\mathbf{Q}$, we want to say that “$\forall xFx$” is true upon an interpretation, $i$, just on condition that $i$ assigns to “$F$” the set of all the 1-membered sequences that can be formed out of members of its domain. (vi) instructs us to consider the sentence ���$F\alpha$” which results from “$\forall xFx$” by deleting the quantifier with its adjacent “$x$”, and replacing the other occurrence of “$x$” by the first name-letter not in “$\forall xFx$”; it holds that our target sentence is true upon $i$ iff “$F\alpha$” is true upon all $\alpha$-variants of $i$: all interpretations which agree with $i$ on their domain and on what set they assign to “$F$”, though perhaps differing from $i$ in what they assign to “$\alpha$”. For each object in the domain of $i, D$, at least one of these interpretations will assign “$\alpha$” to it. Just on condition that “$F\alpha$” is true whatever object “$\alpha$” is interpreted as standing for, that is, just on condition that “$F\alpha$” comes out true upon all these interpretations, “$\forall xFx$” is true upon $i$. “$\forall xFx$” is true upon any interpretation that assigns to “$F$” the set containing all the singleton sequences which can be formed from the $D$-members; that is, it is true upon any interpretation, $i$, such that for every object, $x$ in $D$, $\langle x \rangle$ belongs to $i(F)$. It is, for example, false upon an interpretation with respect to the domain of all persons that assigns to “$F$” the set of all 1-membered sequences whose member is happy.


Talk of sets of sequences in connection with assignments to monadic predicate-letters is tiresome, and is needed only in order to achieve a smooth general statement of truth-upon-an-interpretation conditions, applicable to predicates of arbitrary degrees. Otherwise one could think of an interpretation as associating monadic predicate-letters with subsets of its domain, and I will routinely adopt this convention when convenient. Then one could say, for example, that “$\forall xFx$” is true upon any interpretation which assigns its domain to “$F$”.

(vii) works just like (vi), except that instead of every $n$-variant we now talk of some $n$-variant. Simplifying as in the previous paragraph, “$\exists xFx$” is true upon any interpretation which assigns to $F$ a non-empty set.

The definition of $\mathbf{Q}$-validity is as follows:

**`3)`** An argument is $\mathbf{Q}$-valid iff every interpretation upon which all the premises are true is one upon which the conclusion is true.

Since each interpretation has a domain, and since every domain is the domain of many interpretations, there is an implicit quantification over domains in this definition.

There are a number of different ways in which semantics for $\mathbf{Q}$ can be given. One motivation for my choice is that I wanted to bring out the unity of functioning of the sentence connectives as they occur in $\mathbf{P}$ and as they occur in $\mathbf{Q}$. Consider a $\mathbf{Q}$-sentence like

**`4)`** $\exists x(Fx \land Gx)$.

By our present criteria, “\&” is not a sentence connective in (*`4)`* since “$Fx$” and “$Gx$” are not sentences. Some people like just to stipulate that they are sentences, but this loses the connection between something's being a sentence and its being usable in a complete act of communication, for example, to make an assertion: you cannot use the expression “$x$ is a man” to make an assertion; for who is $x$? On the semantics given here, “\&”, even as it occurs in (*`4)`*, makes its contribution to truth conditions through functioning as a genuine sentence connective connecting the Q-sentences “$F\alpha$” and “$G\alpha$”. The fact that it can be treated by exactly the same interpretation rule for both languages shows that its semantic functioning is the same in both.


The present account is closely related to Tarski's [1937], but is simplified: truth is defined directly rather than via satisfaction, and infinite sequences have been avoided. The difference is that his language makes no distinction between name-letters and variables. He therefore counts "open sentences", sentences containing variables not bound by a quantifier, as sentences which receive truth-upon-an-interpretation conditions. This means that there is not an immediate correspondence between the kind of expression which has truth-upon-an-interpretation conditions and the kind which has truth conditions. On both Tarski's account and the present variant, what matters to the truth of a universal quantification is that all the objects in the domain be a certain way.

This initially contrasts with an approach, sometimes associated with Frege, which begins by identifying the truth of a universal quantification with the truth of its instances: “∀xFx” is true iff every instance (Fα, Fβ, etc.) is true. This makes the truth of quantifications depend upon what instances are available in a language. As the account stands, to get the right result one would need to ensure that there is an instance in the language for every object in the world; since there are very many objects, there would be very many names in such a language, which would make it unlike any natural language. This is just a technical difficulty, which can be overcome by talking of extensions of the language (for any object there will be some small extension of the actual language which will contain a name for it) but the net result has no advantages over the present approach.

## 3 Universal quantification

What makes a Q-formalization of an English sentence adequate? The "truth conditions" test provides only a necessary condition: the truth-upon-an-intended-interpretation conditions of the $\mathbf{Q}$-sentence should match the truth conditions of the English sentence. The other test, the "same saying" test, comes close to sufficiency: the recovered sentence or argument – the result of replacing the name- and predicate-letters by the English names and predicates specified in the correspondence scheme, and replacing the $\mathbf{Q}$-operators by their stipulated English correlates – should say the same as the original. An intended interpretation is one which assigns to the name-letters the same entities as those to which the corresponding names (in English) refer, and to the predicate-letters the same sets as the sets of things in the domain of which the corresponding predicates (in English) are true. The relevant correspondence is that given by the correspondence schema associated with each formalization. Truth-upon-an-interpretation conditions typically cannot be the same as the truth conditions of a quantified English sentence, for the former is specific about the domain of quantification in a way that the latter usually are not. I say that "match" obtains when the interpretation is over a domain that is appropriate to the English sentence.


The formalization of "Everything is physical" by “$\forall x Fx$” meets both tests relative to an interpretation that assigns the set of all physical things in its domain to “$F$”. The $\mathbf{Q}$-sentence is true on such an interpretation, $i$, iff $i(F)$ is its domain (that is, is the same set as the interpretation’s domain). This matches the truth conditions of the English, setting aside the potentially greater specificity of domain, so the formalization passes the truth conditions test for adqequacy. (The English sentence does not make explicit the domain of the English quantifier (should it, perhaps, include only concrete things?), so various interpretations, differing in their domains, will count as intended.) Moreover, the recovered sentence (“For all $x$, $x$ is physical”) says the same as the original English, so the formalization also passes the same saying test.

How should sentences like

1) All men are happy

be formalized? The standard answer is:

2) $\forall x(Fx \rightarrow Gx)$,

with “$F$” corresponding to “is a man” and “$G$” to “is happy”. Despite the fact that (2) contains no visible occurrence of “if”, it is treated as if it were the same as

*`3)`* For any object, $x$, if $x$ is a man then $x$ is happy.

Is this adequate?

It is not clear how one should proceed in order to test its adequacy relative to the same saying test. However, we can use the truth conditions test. Take an intended interpretation, $i$, with some domain, $D$. It will assign to “$F$” the set of men in $D$, and to “$G$” the set of happy things in $D$. From *`(2.2vi)`* we know that “$\forall x(Fx \to Gx)$” is true upon $i$ iff “$F\alpha \to G\alpha$” is true upon every $\alpha$-variant of $i$. These interpretations fall into three classes:

**`(i)`** Those which assign something in $D$ other than a man to “$\alpha$”. Since “$F\alpha$” is false on all these interpretations, “$F\alpha \to G\alpha$” is true upon all of them, by *`(2.2iv)`*.

(ii) Those which assign a happy man in $D$ to “$\alpha$”. “$F\alpha \to G\alpha$” is true upon all these interpretations, by *`(2.2iv)`*

(iii) Those which assign an unhappy man in $D$ to “$\alpha$”. “$F\alpha \to G\alpha$” is false upon all these interpretations, by *`(2.2iv)`*.

The upshot is that “$\forall x(Fx \to Gx)$” is true upon $i$ iff no $\alpha$-variants belong to case (iii), iff there are no unhappy men in the domain of $i$. So all we have to decide, to determine whether the formalization passes the truth conditions test of adequacy, is whether (1) is true iff there are no unhappy men.

There is no doubt that (1) is false if there are unhappy men. The doubt concerns whether there being no unhappy man is sufficient for its truth. Suppose there were no men at all. Then there would be no unhappy ones. But would this make (1) true?

Peter Strawson ([1952], pp. 173–6) has argued that if John has no children then

*`4)`* All John’s children are asleep

is not true, whereas a Q-formalization of (4) as (*`2)`* would be true upon an interpretation assigning to “$F$” the set of children of John and to “$G$” the set of all sleepers. The first set would be empty, and so all the relevant interpretations will make “$F\alpha$” false, and thus verify “$F\alpha \to G\alpha$”. On Strawson’s view, truth conditions would not match truth-upon-an-intended-interpretation conditions.

A problem with the suggestion that (4) is not true if John is childless is that it is unclear how it should be generalized. We think the following is true, despite the fact that there are no bodies acted on by no forces:

**`5)`** All bodies acted on by no forces continue in a uniform state of rest or motion.

So the doctrine cannot be that no sentences of the form of (4), and whose first predicate is true of nothing, are true.

The situation is markedly similar to the case of conditionals with false antecedents. Indeed, on the standard kind of Q-formalization, the relevant problem is precisely the same. So the standard dialectic can be replayed. For example, it may be suggested that (4) conversationally implicates that John has children, but does not entail it. To support this, it may be urged that even a community whose natural language had Q-quantifiers would tend to utter sentences of the form “$\forall x(Fx \to Gx)$” only if they believed that something is $F$, because they would otherwise be more informative by saying that nothing is $F$.

This response does not do justice to all the issues. As well as being affirmed, the relevant sentences express things which we may believe or disbelieve; there need be no conversation, and so no operation of a conversational mechanism. One who thinks that (4) is not true, given that John has no children, will either say that there is no corresponding belief or that the corresponding belief is not true.

Moreover, the response does not do justice to the fact that we have different attitudes to different universal quantifications, alike in having an empty first predicate. For example,

**`6)`** All bodies acted on by no forces undergo random changes of velocity

is intuitively false, yet its standard Q-formalization as (2) would be true upon an intended interpretation (one assigning to “$F$” the set of bodies acted on by no forces).

A defence of (2) as Q-formalization of both (*`5)`* and (*`6)`* might draw on the idea that in some contexts the assertion of a quantified conditional (as (*`5)`* and (*`6)`* are taken to be) implicates that what is asserted is a law of nature. Since this is a false implicature in the case of (*`6)`*, we think of (*`6)`* as unassertible and then, confusedly, come to think of (*`6)`* as false. A hearer, in order to understand a speaker's full intentions in uttering (*`5)`* and (*`6)`*, would have to recognize him as intending to state a natural law. As one sentence expresses a natural law and the other does not, there is room for a contrast between them, a contrast which need not be reflected in truth values. The full development of the defence needs to do justice to the fact that (4) does not purport to express a natural law. Perhaps (*`5)`* and (*`6)`*, but not (4), are reformulable in counterfactual terms:


If any bodies were acted on by no forces, they would continue in a uniform state of rest or motion

and

If any bodies were acted on by no forces, they would undergo random changes of velocity.

The "implicates natural law" idea would be applied just to the counterfactually reformulable quantifications, leaving some other story to be told for quantifications like (4). It is not easy to see how these various ideas could be applied in a systematic and illuminating way.

There are more straightforward problems with formalizing universal quantifications in English.

**`7)`** Not all men are happy

is standardly formalized as

**`8)`** $\neg \forall x(Fx \rightarrow Gx).$

On the other hand

**`9)`** All men are not happy

is probably ambiguous. On one reading, encouraged by heavy stress on "all", it is equivalent to (*`7)`*, and so to be formalized as (*`8)`*. The other reading, in my view more correct, treats it as appropriately formalizable as

**`10)`** $\forall x(Fx \to \neg Gx)$

and thus as equivalent to

**`11)`** No men are happy.

"Every", "any" and "whatever" are often to be formalized by "$\forall$". Thus (*`2)`* $(\forall x(Fx \to Gx))$ is standardly held to formalize all of:

**`12)`** Every person in the room was happy.

**`13)`** Any person who interferes will be shot.

**`14)`** Whatever you buy you will charge to me.

This formalization is not always the "deepest". For example, it does not discern a possible conjunctive structure in "person in the room". A candidate for a deeper formalization of (*`12)`* is

**`15)`** $\forall x(Fx \land Gx \to Hx)$

where "F" corresponds to "is a person", "G" to "is in this room" and "H" to "was happy".

Ex. 4.2 (a) The following arguments present problems for the standard Q-formalizations of English universal quantifications. Formalize the arguments, showing your correspondence scheme, state the problems, and briefly indicate how, if at all, you think they might be resolved:

(i) It is not the case that all bodies acted on by no forces undergo random changes of velocity. Therefore there are bodies acted on by no forces.

(ii) If anyone plays cricket, he does not also play squash. So anyone who plays both cricket and squash does not play cricket.

(iii) Every parent who loves all of his children is saintly. So every person who loves all of his children is saintly. (Cf. McCawley [1981], p. 163.)

**`(b)`** Formalize the following in $\mathbf{Q}$, noting any problems or deficiencies. The only quantifier to be used is "$\forall$".

(i) If Pedro owns a donkey, he beats it.

(ii) If Pedro owns a donkey, he is lucky.

(iii) Old soldiers never die.

**`(iv)`** It is not invariably the case that love is requited. [$\alpha$'s love for $\beta$ is requited iff, in addition, $\beta$ loves $\alpha$.]

**`(v)`** Anyone who needs something should have it.

**`(vi)`** Jones never leaves his desk.

(vii) If $a$ is greater than $0$, $0$ is less than $a$.

**`(viii)`** None but the brave deserve the fair.

**`(ix)`** Someone who ever lies is someone you should never trust.

**`(x)`** If no one telephones her Jane will be miserable.

**`(xi)`** No one runs faster than John.

**`(xii)`** No one runs faster than himself.

**`(xiii)`** Not everyone runs faster than himself.

**`(xiv)`** If all the people in the world were stretched end to end, they would circle the globe.

## 4 Existential quantification

The English sentence

1) Someone is happy is standardly formalized

*`2)`* $\exists x Fx$.

Given the correspondence of “$F$” to “is happy”, an intended interpretation, $i$, assigns the set of all happy things in its domain to “$F$”. (2) is true upon $i$ iff some interpretation with the same domain making the same assignment to “$F$” assigns someone happy to “$\alpha$”, and this is intuitively the correct truth condition.

How should sentences like

*`3)`* Some elephants are greedy be formalized? A standard answer is:

4) $\exists x(Fx \land Gx)$, pronounced: “there is an $x$ such that $F$ of $x$ and $G$ of $x$”. Despite the fact that (3) contains no visible occurrence of “and”, it is treated as if it were the same as

*`5)`* Something is both an elephant and greedy.

On an interpretation $i$ which assigns to “$F$” the set of elephants, and to “$G$” the set of greedy things, (*`4)`* is true iff at least one $\alpha$-variant of $i$ assigns a greedy elephant to “$\alpha$”. The formalization represents (3) as true iff at least one thing is greedy and an elephant. (3) appears to imply that there is more than one greedy elephant, and this aspect is not preserved in the formalization. Moreover, some have said that “some” implies “some but not all”, so that (3) would imply that some elephants are not greedy. These alleged implications appear stronger in some cases than others. For example,

6) She ate some of the cakes

seems to imply quite strongly that some cakes were left and that more than one was eaten.

The “some but not all” implication could be approached in at least two ways. One could explicitly add to the formalization of, say, (3) that not all elephants are greedy. This is simply the denial of “All elephants are greedy”, and so the formalization proposed is

*`7)`* $\exists x(Fx \land Gx) \land \neg \forall x(Fx \rightarrow Gx)$.

Alternatively, one could say that the implication is a matter of implicature only, and so need not be registered in the formalization. To support this view, one could say it would be misleading to use “some” if one knew something expressible by “all”: misleading, but not false. The cancellability of the implicature would support this view:

8) She (certainly) ate some of the cakes – all of them in fact

is consistent.

The implicature story does not work well for the implication from “some”-sentences to “more than one”-sentences. Since, for example,

*`9)`* She ate a cake

does not entail

10) She ate some cakes,

they cannot both correctly be given the same formalization, viz. (4). Similarly, we do not have the cancellability one would expect from implicature, since the following is inconsistent:

*`11)`* She ate some of the cakes – in fact, just one.

Compare also

12) A hungry man is at the door

and

13) Some hungry men are at the door.

While the first could be adequately formalized along the lines of (*`3)`*, the second could not be.

We should not infer that the meaning of "some" differs from that of "∃". The entailment in question need not be seen as due to "some", because where it obtains it is adequately explained by the presence of the plural nouns ("cakes" rather than "cake", "men" rather than "man"). In §9 we will discuss how the effect of plurals can be captured in Q. Probably the safest way to read "∃x" is "There is at least one thing, x, such that"; and we can be confident that, in using "∃" in the manner of (*`4)`*, we are adequately formalizing English sentences containing quantifiers like "some", "something", "a" – as in "A man is here to see you" – just on condition that we can rephrase without distortion in terms of "There is at least one thing such that . . .".

Ex. 4.3 Consider the following pair:

(i) Some Buddhists are vegetarians.

(ii) Some vegetarians are Buddhists.

Is the apparent difference between them one which could affect the validity of some argument? Can the apparent difference be reflected in different Q-formalizations? If so how? If not, does this give a new reason for thinking that the meaning of "some" differs from that of "∃"? (Cf. McCawley [1981], p. 123.)

There is no need for Q to contain both "∀" and "∃", since they are interdefinable. This corresponds to the facts about English that

"everything is ..." means "it is not the case that something fails to be ..." and that "something is ..." means "it is not the case that everything fails to be ...".

Ex. 4.4 (a) Assuming “∀” is primitive in Q, show how you could introduce “∃” by a definition.

(b) Assuming “∃” is primitive in Q, show how you could introduce “∀” by a definition.

**`(c)`** Formalize the following in Q, noting any problems or deficiencies:

(i) If Pedro owns a donkey he is lucky. [Do not use “∀”.]

(ii) There is a town between Oxford and London.

(iii) I met a man.

(iv) A puppy is a young dog.

(v) Some men are touchy and vain.

(vi) Some people have everything.

(vii) Every cloud has a silver lining.

(viii) When beggars die there are no comets seen.

(ix) There is a skeleton in every cupboard.

(x) Nothing lasts for ever.

(xi) Jones never feeds any of his dogs.

(xii) Who laughs last laughs longest.

## 5 Adjectives

A sentence like

1) Tom is a greedy man

is usually formalized as

2) $F\alpha \land G\alpha$,

with “F” corresponding to “is greedy”, “G” to “is a man” and “α” to “Tom”. The adjectival construction of the English, in which the adjective “greedy” qualifies the noun “man”, is rendered as a conjunction in Q. The truth conditions appear to come out correctly. (1) does indeed seem equivalent to

*`3)`* Tom is a man and is greedy.

Moreover, upon an interpretation which assigns to “$F$” the set of men, to “$G$” the set of greedy things, and to “$\alpha$”, Tom, (2) is true iff Tom is a man and is greedy, which seems correct with respect to (1).

In Q, adjective phrases like “is greedy”, noun constructions like “is a man”, and verbs like “runs” are treated as all of essentially the same kind – predicates – and hence are matched with predicate-letters in Q-logical forms. This policy ensures that some familiar English adjectival constructions cannot be adequately formalized in Q to a reasonable depth. Consider

*`4)`* Tom is a large man

and suppose we formalize this as (2): “$F\alpha \land G\alpha$”, with “$F$” corresponding to “is a man” and “$G$” to large. Continuing this policy, how should we formalize

5) Tom is a businessman but not a large businessman?

The policy dictates:

*`6)`* $H\alpha \land \neg (H\alpha \land G\alpha)$

with “$H$” corresponding to “is a businessman” and “$G$” to “large”. However, (4) and (5) are consistent, whereas (2) and (6) are not. Hence the policy of formalizing (4) and (5) by the conjunctive treatment of adjectives has failed. It has wrongly represented consistent sentences as inconsistent.

#### Ex. 4.5 Explain why (5.2) and (5.*`6)`* are inconsistent.

There is a class of adjectives like “large” (and “heavy”, “expensive”, etc.) which resist Q-formalization. And there are other resistant adjectives. For example, it is obvious that

7) Tom is an alleged murderer

is not to be formalized as (*`2)`* (with “$F$” corresponding to “is a murderer” and “$G$” to “alleged”). Although it would be reasonable to formalize
8) Tom loves only happy women

as

*`9)`* $\forall x(H \alpha x \rightarrow (Fx \land Gx))$

(with “$F$” corresponding to “is a woman”, “$G$” to “is happy” and “$Hxy$” to “$x$ loves $y$”), it would not be reasonable, but nonsense, to adopt the same formalization of

*`10)`* Tom loves only three women.

An intended interpretation would assign to “$G$” the set of all things which are three. But it is nonsense to speak of an object (one single object) being three. There is no such property. I discuss in §9 how adjectives like “three” are Q-formalized.

In general, we can reflect adjectival modification by conjunction only if, where “$n$” is a name, “$A$” an adjective, and “$C$” the common noun it qualifies, the following is true (and has an intelligible conclusion):

*`11)`* $n$ is a (or an) $AC \models n$ is $A$ and $n$ is a (or an) $C$.

Adjectives (or adjectival phrases) satisfying (*`11)`* (like “happy”, “greedy”, “red”, “weighs 12 pounds”) are called “predicative”. Among non-predicative adjectives, there are various distinctions. There is a category of adjectives which qualify other adjectives, for example “dark” (qualifying colour adjectives), and these, though ruled non-predicative by (*`11)`*, behave rather differently from “large”. “Three” and “alleged”, though both classified as non-predicative, differ in that while “three” can be adequately represented in Q, “alleged” cannot.

**Ex. 4.6** Show by example that the following suggestion is mistaken: If “weighs 20 stone” is predicative “heavy” must also be predicative.

Sentences containing non-predicative adjectives, like (4), can be Q-formalized. We could let "$F$" correspond to "is a large man" and formalize (4) as "$F \alpha$". We can make sense of the idea of an interpretation which assigns to "$F$" the set of large men. However, this Q-formalization is not deep enough to bring out the distinctive contribution of "large". "Is a large man" is complex, composed of "large" and "man". This complexity of structure is not revealed in the envisaged Q-formalization.


Ex. 4.7 Explain why we cannot make sense of an interpretation which assigns to "F" the set of large things.

The formalization could not reflect the validity of arguments like:

*`12)`* Tom is a small businessman. Therefore Tom is a businessman.

The most revealing Q-formalization would be

*`13)`* $F\alpha, G\alpha$

(with "F" corresponding to "is a small businessman" and "G" to "is a businessman"), which is plainly Q-invalid. Does this matter? The idea of artificial languages was to capture generalizations about formal validity, but, by the standards set in chapter 1.10 and 1.11, (*`12)`* is not formally valid. While this may give the Q-formalizer relief from the burden of finding a formalization of (*`12)`* which reflects its validity, it also carries with it an objection concerning cases in which there are validity-reflecting Q-formalizations. For example, the validity of

*`14)`* Tom is a happy man. Therefore Tom is a man

is reflected by the validity of the obvious Q-formalization. Hence the conjunctive method of Q-formalization has captured more validity than was intended: it has reflected as formally valid an argument that, though valid, is not formally valid, according to our original definition. There is a tension here. The original definition of formal validity could be revised, or else the project of formalization recharacterized.

Ex. 4.8 Explain why (5.*`12)`* does not count as formally valid, by the standard of chapter 1. Is there any other standard of formal validity which would be more appropriate?

I have given examples of supposedly predicative adjectives - "happy", "greedy", "red", "weighs 12 pounds" - but a doubt remains. Are all these adjectives really predicative? One sign of non-predicativity comes from the pattern discerned in the case of "large":

you can be a mouse and an animal and a large mouse without being a large animal. Suppose that humans are on the whole rather less greedy than most animals. Then you could be a man and an animal and a greedy man without being a greedy animal. Like “large”, there is a relativization to a comparison class, which is introduced by the noun, and which could be expressed more explicitly by saying “He’s large for a mouse, but not large for an animal”, “He’s greedy for a man, but not greedy for an animal”. So perhaps “greedy”, and by similar considerations “happy”, are, after all, non-predicative.

Ex. 4.9 Can you find expressions $T_1$ and $T_2$ such that there is no inconsistency in supposing that someone could be happy for a $T_1$ but not happy for a $T_2$?

The difference between “large” and “greedy” is this: “large”, associating with the noun it qualifies, thereby determines, at least in part, the appropriate standards of size to be applied. This does not hold for “greedy”, which in this resembles adjectives like “tall”. Even when “tall” occurs modifying a noun, as in “Tom is a tall man”, it may not be this noun which determines the relevant comparison class. That determination is left to context. Being tall for a Swede involves being taller than does being tall for an Eskimo.

Does the growing shadow of non-predicativity extend even to an adjective like “red”? It’s one thing for a house to be red (quite in order for the windows, doors, mortar and interior not to be red), another for a colour sample to be red (should be uniform red all over), another for a tomato to be red (painted red doesn’t count) and yet another thing for hair to be red. Correct as these observations are, they do not establish non-predicativity. There is no general term, $T$, not itself having colour entailments, yielding the pattern: “This is a tomato and a $T$ and is a red tomato but not a red $T$”. Moreover, (*`11)`* holds for “red” combined with any appropriate noun. So the phenomenon is not non-predicativity. Although the different nouns it qualifies impose different standards for what is to count as a red thing of that kind, it appears impossible for a thing to belong to two different kinds and count as red by the standards appropriate to one and as non-red by the standards appropriate to the other. With non-predicativity, like that of “large”, by contrast, the different possible comparison classes can give different verdicts with respect to the applicability of the adjective.

Ex. 4.10 (a) Formalize:

This is a gold ingot. Therefore it is made of gold.

(b) Give three examples each (not in the text) of predicative and non-predicative adjectives.

(c) Provide Q-formalizations of the following, noting any inadequacies:

(i) Some greedy men are vain.

(ii) Some vain men are greedy.

(iii) John loves a beautiful actress.

(iv) John loves a former actress.

## 6 Adverbs

In traditional grammar, an adverb or adverbial phrase is seen as modifying a verb. No such construction is available in Q. Hence there is no straightforward validity-reflecting Q-logical form of, for example,

1) John walked quickly. Therefore John walked.

We could merge “walked” with “quickly”, and formalize “walked quickly” by a single predicate letter; but we would have to choose a different letter to correspond to plain “walked”, as it occurs in the conclusion, so the formalization would patently be Q-invalid.

We can reach a deeper formalization by a roundabout route, which has been proposed by Donald Davidson. It seems that

2) John walked

is true iff there is something – a walk – which John walked. So, though there is no visible existential quantifier in (*`2)`*, we could offer the following formalization of it:

*`3)`* $\exists x F \alpha x$

with “$Fxy$” corresponding to “$x$ walked $y$”, and “$\alpha$” to “John”.

John’s walk might be quick or slow, uphill or downhill, with a stick or with a dog. This suggests that (1) should be formalized:

*`4)`* $\exists x(F\alpha x \land Gx); \exists x F\alpha x$

with “$F$” and “$\alpha$” as before, and “$G$” corresponding to “is quick”. It is perfectly in order for an interpretation of “$G$” to assign a set of quick things: quick walks and quick swims and quick runs, but not slow walks, etc., and not trees or lamp-posts, since these things cannot be quick.

**`(4)`** is Q-valid. The premise says that there is something with two properties – being $F$ to $\alpha$ and being $G$ – and it is clearly correct to infer from this that there is something with just the first of these properties.

In general, the sort of thing that can be walked or can be quick is an event. We can sum up Davidson’s proposal as involving two theses: (i) many verbs (those like “walk”, “run” and “swim”) introduce events, and many sentences containing these verbs, like (2), introduce (implicit) existential quantification over events; (ii) adverbs are adjectives which qualify events. Thus Davidson’s proposal sees the premise of (1) as containing an implicit existential quantifier, and sees “quickly” as an adjective whose intended interpretation associates it with a subset of events. (The notion of a sentence containing an “implicit” occurrence of a quantifier is discussed in chapter 6, especially 6.6.)

How widely can this account be applied? One class of adverbs can be exempted from the account at the outset: those which, like “allegedly”, “necessarily”, “probably” and “rarely”, modify sentences rather than verbs: they are sentence adverbs (cf. Taylor [1985]). It is plain that in

5) John allegedly shot Jane

we are not saying that there is (really is!) a shooting with the property of being alleged. Rather we are saying something like: it is alleged that John shot Jane. We are not asserting that a shooting has a certain property, but rather qualifying a whole sentence (“John shot Jane”). Davidson ([1967b], p. 121) says that his account is not intended to apply to any sentence adverbs.

To bring out the difference between sentence adverbs and the kind with which we are concerned, consider the ambiguity of

6) John trod carelessly on a snail.

If we hear “carelessly” as a sentence adverb, we will regard this as equivalent to

7) It was careless of John to tread on a snail.

If we hear “carelessly” as genuinely modifying “trod”, we will reject this equivalence: John may have set out with full deliberation and care to tread on a snail, so (7) is false, but in the end executed his plan carelessly, so one reading of (6) is true.

**Ex. 4.11** What considerations, if any, should incline one to classify “necessarily”, “probably” and “rarely” as sentence adverbs?

There is another resistant category of adverbs, exemplified by “intentionally”. We cannot paraphrase “John intentionally trod on a snail” as “It was intentional that John trod on a snail”, since the latter is ungrammatical. So “intentionally” is not a sentence adverb. Yet we cannot see the adjective “intentional” as true of events. The very same event may be an intentional switching on of the light and an unintentional scaring off of an intruder. As Davidson says ([1967b], p. 121), events as such can neither be intentional or otherwise. Hence the adverb “intentionally” cannot be treated as an adjective applying to events.

Does Davidson’s account hold of all adverbs which are neither sentence adverbs nor ones like “intentionally”? No: for in some cases — including “quickly” — the adjective that would be discerned on Davidson’s account is non-predicative, and hence its distinctive contribution cannot be captured in Q. John swam the channel, and thereby broke the record for cross-channel swims. On Davidson’s account

8) John swam the channel quickly

should be true in virtue of whatever swim verifies (8) being a quick one. On the other hand, compared to most channel-crossings, John’s self-propelled crossing was slow. So we also have as true

9) John crossed the channel slowly.

But the very same event is both the swim and the crossing, and verifies both (8) and (9). If we applied Davidson’s account, we would be committed to the view that some particular event (John’s swim, that is, his crossing) is both quick and slow, which is unacceptable.

Davidson's account should therefore be applied only to those adverbs not in any of the three resistant categories we have mentioned, viz.: sentence adverbs, those like "intentionally", and those corresponding to non-predicative adjectives. Whether there is a positive characterization of the remaining adverbs, and whether they genuinely form a special category of adverb, are questions we will not pursue. Failure of predicativity, or at least some closely related phenomenon, may be more prevalent than one might at first suppose (cf. Wiggins [1985]). For example, a walk can be uphill, and "uphill" appears predicative. A walk can also be a warning. But it is open to question whether it is intelligible to qualify a warning as an uphill one. We seem to have the pattern of non-predicativity: something is a walk and a warning and an uphill walk but not an uphill warning.

Ex. 4.12 (a) Formalize the following, stating your correspondence scheme, and noting any inadequacies:

(i) John ambled down the hill.

(ii) Quickening his pace, John strode up the hill.

(iii) John worked for the whole night.

(iv) John worked in Boston for four years.

(b) Davidson has argued that pairs of sentences like
(i) Shem kicked Shaum. It happened in the gymnasium.

constitute evidence in favour of the view that sentences like the first in the pair introduce events. For the "it" of the second sentence appears to be linked to the first sentence in the way that "he" is linked to "a man" in the pair

(ii) I met a man. He was bald.

(The "he" here is called an "anaphoric" pronoun.) Formalize (i), showing your correspondence scheme, and say whether your formalization supports Davidson's claim.

## 7 Names

Names in English, like "Tom" and "London", are supposed to be Q-formalized by the use of name-letters. What is the common feature of names that justifies this common treatment? When we have answered this question, we will be in a position to say whether expressions like "the present Prime Minister of Great Britain", "water", "Pegasus" and "Vulcan", which in many ways resemble names, should also be formalized by name-letters.


In Q, a name-letter is simply assigned an object (in the domain of interpretation). So one would expect the category of English names to be a category of expressions which stand for objects. "Tom" and "London" fall into this category. But may it not turn out to include many other expressions as well? For example, why does not an expression like "happy", in the sentence "Tom is happy", count as standing for an object: the property of being happy, or, perhaps, the set of happy persons? Indeed, predicate-letters are interpreted in Q by being assigned objects (viz. sets), so should we not also construe English predicates as standing for objects, and thus, by the proposed criterion, counting as names?

A predicate takes a name to form a sentence. If predicates were a species of name, then a sentence like "Tom is happy" would be construed as two names juxtaposed. But two names juxtaposed do not make a sentence, only a list. Hence predicates cannot count as names.

This argument does not prevent one seeing common nouns as names, and analysing, say,

1) Tom is a man

as

2) $F\alpha\beta$

with “$\alpha$” corresponding to “Tom”, “$\beta$” to “the property of being a man”, and “$F$” to “having” (as when we say an object has a property). I know of no decisive objection to the policy, though we will not follow it. Pursuing it cannot construe all predicates as names: there remains the predicate “having”, matched to the predicate-letter “$F$”.

Expressions like “the present Prime Minister of Britain” are called “definite descriptions”. Many of them stand for objects, like the one just mentioned, so they are prima facie cases of names. Some, like “the golden mountain”, do not. Hence if all definite descriptions are to be treated in the same way, none of them should be formalized by name-letters. Other reasons for not formalizing them by name-letters are given in §10.


Does “water” stand for an object? One is inclined to say yes: of course, “water” stands for water! But what is this object, water? Not, presumably this puddle or glassful, but the scattered totality of water throughout the universe. There is no objection to allowing this totality to count as an object. Most objects are spatially cohesive in the sense that between any two spatially separated parts of the object lies a route (not necessarily a straight line) at each point of which is another part of the object. But there is no need to insist that all objects must be like this. So far, then, “water” passes the test for being a name.

There are cases in which it is unnatural to treat it as a name, for example:

3) There is some water here.

One could try formalizing “water” as a predicate:

4) $\exists x(Fx \land Gx\alpha)$

with “Fx” corresponding to “x is water”, “Gxy” corresponding to “x is present at y” and “α” corresponding to “here”. There is something suspect: if we use the test of reading “∃” as “there is at least one thing which”, we find we are treating (3) as saying “There is at least one thing which is water here”. Likewise, an interpretation would have to assign to “F” a non-empty set of waters, or things which are water. What things are these? Pools and lakes? If so, we misrepresent (3) as equivalent to something like “there is at least one pool (or lake, or quantity) of water here”. If “F” is assigned the single scattered object, water, one could as well revert to the idea that “water” is a name, and adopt a formalization like:

5) $\exists x(Fx\beta \land Gx\alpha)$

with the correspondences for “$G$” and “$\alpha$” as before, “$\beta$” corresponding to “water” (now treated as a name) and “$Fxy$” corresponding to “$x$ is part of $\gamma$”. Again, this is not a perfect mirror of (3), for it treats it as equivalent to "Something is water here", and it's not clear that (3) involves any such thing.


More ingenuity is required to get even this close in the case of sentences like

6) Oil is lighter than water.

This sentence is true. But if we formalize as

*`7)`* $F\alpha\beta$

with “$F$” corresponding to “lighter than”, and “oil” and “water” to “$\alpha$” and “$\beta$” respectively, we say something which is true iff the weight of the total amount of oil in the universe is less than that of the total amount of water. This may still be true, but it is clearly not what (6) says. Rather, (6) says something like: any volume of oil weighs less than the same volume of water, and this would have to be the basis for an appropriate formalization, using the notion of “part of” as in (5).

In the case of words that are in many respects similar, for example "gold", a similar strategy would be called for in formalizing such sentences as

*`8)`* This ring is made of gold.

Made of gold it may be, but not composed of the scattered totality of all the gold in the world.

Ex. 4.13 Provide formalizations of (7.6) and of (7.8), showing your correspondence scheme. Are your formalizations true upon an intended interpretation?

Does "Pegasus" stand for an object? If it does, the object is a mythological one. Are there mythological objects, or is applying "mythological" a way of saying that there is no such object? Opinions differ. If, like me, you think that there are not really any such objects as Pegasus, you cannot formalize names like "Pegasus" by name-letters. One alternative is given in §10.

Even if you think that there is such a thing as Pegasus, you will not, I presume, think there is any such thing as Vulcan. "Vulcan" was introduced in the nineteenth century by astronomers. They posited an additional planet, lying between the planet Mercury and the Sun, whose presence they felt was required to explain the course of Mercury. They were wrong: there is no such planet between Mercury and the Sun. So you cannot think that "Vulcan" stands for an object, so you cannot formalize it by a name-letter. An alternative is given in §10.

## 8 Identity

"=" is a genuine predicate (or, in some terminologies, a predicate constant). Unlike predicate-letters, which are assigned different sets in different interpretations, "=" is assigned a set specifiable in the same way in every interpretation: the set of all ordered pairs whose members belong to the domain and whose first member is the same as the second. This stipulation about interpretations reflects the intention that "=" should mean identity.

To conform to tradition, we will abbreviate expressions like " = αβ" and " ∇ = αβ" to "α = β" and "α ≠ β".

It follows from what was said in the first paragraph that

1) α = α

is true on every interpretation, that is, |_{Q} α = α. This is enough to establish that

2) |_{Q} ∀x x = x.

By contrast,

3) |_{Q} ∀xFxx

is false. For though (3) is true upon some interpretations (for example, those which assign to “F” what is assigned to “=”), it is false on others (for example, those which assign to “F” the set of ordered pairs such that the first is larger than the second).

The following true argument-claim illustrates the so-called principle of *substitutivity of identicals*:

4) $F\alpha, \alpha = \beta \vdash_{\mathbb{Q}} F\beta.$

This reflects the intuitive truth that if $\alpha$ is the same thing as $\beta$, then any predication true of $\alpha$ is also true of $\beta$. The point can be put more generally as follows:

5) An interpretation upon which “$\alpha = \beta$” is true is one upon which: “...$\alpha$...” is true iff “...$\beta$...” is true.

The last line is to be read as follows: any sentence containing “$\alpha$” is true (upon the interpretation) iff the corresponding sentence, but with “$\alpha$” replaced by “$\beta$”, on any number of occurrences, is true (upon the interpretation). A rough summing up: identical objects have identical properties.

Ex. 4.14 (a) Formalize the following, using “=” where appropriate:

(i) Mr Hyde is the same person as Dr Jekyll.

(ii) Everything is what it is and not another thing.

(iii) John is wiser than anyone else.

(iv) Apart from John no one brought a present.

(v) Mary loves only John.

(vi) If Mary loves anyone John is that person.

(vii) Mary loves John but John loves someone else.

(viii) Mary loves John and Sally loves someone else.

(ix) John loves himself and so does Mary.

(x) Who laughs last laughs longest.

(b) Show that in English there are counterexamples to the claim that if $x = y$, then "...$x$..." is true iff "...$y$..." is true. Do these discredit *`(8.5)`*?

## 9 Numeral adjectives

Consider

1) There are two men at the door.

Though “two” is, by some standards, an adjective attached to “man”, it does not modify “man” in the predicative way. We cannot formalize (1) as

2) $\exists x(Fx \land Gx)$

with "$F$" corresponding to "is a man at the door" and "$G$" corresponding to "two". An intended interpretation would have to assign to "$G$" the class of all things which are two, and this is nonsense: no (one) object is two.

**Ex. 4.15** Discuss the following objection:

One book may be a hundred pages; so one object can be a hundred.

We can provide adequate formalizations of sentences like (1) by using quantifiers and “=”. (1) is probably ambiguous between

3) There are exactly two men at the door

and

4) There are at least two men at the door.

We can formalize (4) as

5) $\exists x \exists y(Fx \land Fy \land x = y).$

This is true upon an interpretation, $i$, iff at least two things are in $i(F)$. Applying the interpretation rules of (2.2) in some detail, (5) is true upon an interpretation, $i$, iff “$\exists y(F\alpha \land Fy \land \alpha \neq y)$” is true on some $\alpha$-variant of $i$, say $i'$. This is turn is true on $i'$ iff “$F\alpha \land F\beta \land \alpha \neq \beta$” is true on some $\beta$-variant of $i'$, say $i''$. Any such $i''$ must assign different objects to “$\alpha$” and “$\beta$”, hence it must assign to “$F$” a set having at least two members. But $i'$ and $i$ agree with $i''$ in their assignment to “$F$”. So (5) is true on an interpretation iff it assigns at least two things to “$F$”. Hence (5) is an adequate formalization of (4).

We saw (in §4) that “$\exists xFx$” adequately formalizes “At least one thing is $F$”. It is easy to modify (5) so that it formalizes “At least three things are $F$”. More generally, the following schema can be seen as giving instructions for formalizing “At least $n$ things are $F$”, for an arbitrary numeral $n$:

6) $\exists x_{1} \ldots \exists x_{n}(Fx_{1} \land \ldots \land Fx_{n} \land x_{1} \neq x_{2} \land \ldots \land x_{1} \neq x_{n} \land x_{2} \neq x_{3} \land \ldots \land x_{2} \neq x_{n} \land \ldots \ldots \land x_{n-1} \neq x_{n})$.

To apply this recipe, we imagine the variables to be ordered in some way, with “$x_1$” corresponding to the first variable in the ordering, and so on. The recipe enjoins you to write $n$ instances of the existential quantifier followed by a variable (a different variable each time), followed by $n$ instances of “$F$” followed by each of the variables, followed by instances of $v \neq v'$ for every pair of distinct variables. Applying it to the case $n = 4$, so that the aim is to formalize “At least four things are $F$”, we get:

7) $\exists x \exists y \exists z \exists x' (Fx \land Fy \land Fz \land Fx' \land x \neq y \land x \neq z \land x \neq x' \land y \neq z \land y \neq x' \land z \neq x').$

Exactly $n$ things are $F$ is true iff (at least $n$ things are $F$ and at most $n$ things are $F$). So if we can formalize “at most $n$”, it will be easy to formalize “exactly $n$”.

Suppose that

*`8)`* At most two things are $F$

is true. Then, if ever we find objects, $o_1, o_2, o_3$, which are all $F$, we know that we must have counted one object twice, which means that either $o_1 = o_2$ or $o_1 = o_3$ or $o_2 = o_3$. This justifies the formalization of (*`8)`* as

*`9)`* $\forall x \forall y \forall z ((Fx \land Fy \land Fz) \rightarrow (x = y \lor x = z \lor y = z)).$

Similarly

*`10)`* At most one thing is $F$

is formalized

*`11)`* $\forall x \forall y (Fx \land Fy \rightarrow x = y)$.

In general, at most $n$ things are $F$ is formalized by the recipe:

*`12)`* $\forall x_1 \ldots \forall x_{n+1} ((Fx_1 \land \ldots \land Fx_{n+1}) \rightarrow (x_1 = x_2 \lor \ldots \lor x_1 = x_{n+1} \lor x_2 = x_3 \lor \ldots \lor x_2 = x_{n+1} \lor \ldots \lor x_n = x_{n+1}))$.

To formalize (3) – “there are exactly two men at the door” – we can simply conjoin (5) and (*`9)`*. The result is equivalent to the neater:

*`13)`* $\exists x \exists y (Fx \land Fy \land x \neq y \land \forall z (Fz \rightarrow (z = x \lor z = y)))$.

This says that some $x$ and $y$ are $F$ and are distinct, and that any $F$ thing is one of these. It adequately captures the idea that exactly two things are $F$. The general recipe on the lines of (13) is

*`14)`* $\exists x_1 \ldots \exists x_n (Fx_1 \land \ldots \land Fx_n \land x_1 \neq x_2 \land \ldots \land x_1 \neq x_n \land x_2 \neq x_3 \land \ldots \land x_2 \neq x_n \land \ldots \land x_{n-1} \neq x_n \land \forall x_{n+1} (Fx_{n+1} \rightarrow (x_{n+1} = x_1 \lor \ldots \lor x_{n+1} = x_n)))$.

Faced with the task of formalizing an English sentence containing numeral adjectives, the recipes in (6) and (14) may be useful. More insight into the ideas involved is provided by appreciating the possibility of a recursive approach. For example, the notion of “exactly $n$” (for some positive numeral $n$) can be abbreviated by a quantifier of the form “$\exists^n x$”, and captured by a basis clause (15) and a recursive clause (16):

*`15)`* $\exists^1 x Fx =_{df} \exists x (Fx \land \forall y (Fy \rightarrow x = y))$.

**`16)`** $\exists^n x Fx =_{df} \exists x (Fx \land \exists^{n-1} y (Fy \land x \neq y))$.

**`(15)`** defines “exactly one thing is $F$” as “something is $F$ and everything which is $F$ is that thing”. (This is how Russell defined “The $F$ exists”.)

**`(16)`** defines “exactly $n$ things are $F$” as “something is $F$ and there are exactly $n-1$ other things which are $F$”.

Ex. 4.16 (a) Following the pattern of *`(9.15)`* and (9.*`16)`*, provide general definitions (for arbitrary $n$) of the “at least” and “at most” quantifiers.

(b) Explain what, if anything, would be wrong with the following in place of (9.*`16)`*:

$$\exists^{n}x Fx =_{df} \exists^{1}x(Fx \land \exists^{n-1}y(Fy \land x \neq y))$$

(c) Can “There are finitely many foxes” be adequately Q-formalized as $\exists x(Gx \land \exists^{x}y(Fy))$

with “$G$” corresponding to “is a natural number” and “$F$” to “is a fox”?

We can use these ideas to capture the plurality involved in sentences in which an existential quantifier attaches to a plural noun. Thus (4.3)

Some elephants are greedy

may mean something like

17) More than one elephant is greedy.

If so, it can be formalized as

**`(18)`** $\exists x \exists y(Fx \land Fy \land Gx \land Gy \land x \neq y)$

with the intended interpretation assigning to “F” the set of elephants, and to “G” the set of greedy things. If (17) seems more precise than (4.3), it may be that we need to turn to implicature for an explanation. If, looking at a large bag of nails, I exclaim

19) Some of the nails have gone rusty

my audience may well expect there to be more than two rusty ones, but it seems wrong to say that this is actually entailed, rather than implicated, by (19).

The recipes (7), (12) and (14) can be used to formalize sentences in which number words like “one”, “two” and “three” qualify nouns or noun phrases (like “men” or “men at the door”). In virtue of this role, number words in these occurrences have been called “numeral adjectives”. A contrasting role is when the same words are used, apparently, as names of numbers, as in the series “one”, “two”, “three”, or in a sentence like “one plus two is three”. In this role, the words are sometimes called, simply, numerals; and in this role, one cannot rely on the recipes to provide formalizations. A sentence like

20) Five plus seven equals twelve

has to be formalized using name-letters to correspond to the numerals.

Ex. 4.17 (a) Formalize the following sentences, showing your correspondence scheme. (You may if you wish use the “exactly” quantifier defined by (9.15) and (9.16), and the quantifiers defined in your answer to Ex. 4.16a.)

(i) Mary kissed two people at once.

(ii) Three kings came to Bethlehem.

(iii) If two persons are present, there is a quorum. There are three of us present. So there is a quorum.

(iv) John is happy and so is Mary. So at least two people are happy.

(v) Bananas and apples are fruits. You have eaten two bananas and three apples. So you have eaten five fruits.

(vi) $2 + 3 = 5$.

(b) Is the following consistent?

I don’t have two racquets, I have three.

What does your answer show about the correct interpretation of numeral adjectives in English? (Cf. K. Bach [1987], p. 78.)

(c) Formalize the following, noting any problems.

Shem kicked Shaum twice. It happened in the gymnasium.

**`(d)`** Does the displayed sentence in (c) above pose any problem for the alleged evidence, presented in Ex. 4.12b, in favour of the event analysis of action sentences? In your discussion, consider also the fact that the following seems ungrammatical, yet arguably should be acceptable on the event analysis:

Three times the red flag was unfurled. They happened in the main square.

## 10 Descriptions

We saw in §7 that there is a case for saying that definite descriptions like “the present Prime Minister of Great Britain” and “the moon” should not be formalized by name-letters. This section explores that case in more detail. First, I present part of the only serious alternative pattern of Q-formalization, provided by Bertrand Russell’s theory of descriptions.

The theory comes in two parts, one of which deals with sentences like:

1) The moon is cold.

Russell’s idea was that such a sentence should be Q-formalized as if it were “There is exactly one moon and it is cold”:

*`2)`* $\exists x(Fx \land \forall y(Fy \rightarrow x = y) \land Gx).$

The second part deals with sentences like

*`3)`* The moon exists

which Russell treats as an instance of *`(9.14)`* for $n = 1$:

*`4)`* $\exists x(Fx \land \forall y(Fy \rightarrow x = y)).$

In both cases, an intended interpretation should assign to “F” the set of moons, and to “G” the set of cold things. (2) in effect says that exactly one thing is F and that thing is G. If it correctly formalizes (1), then (1) is false if there is more than one moon or less than one or if there is exactly one moon which is not cold; and otherwise (1) is true. On an intended interpretation, (*`4)`* says that there is exactly one moon.

We need some relativization, or else (2) and (4) will be false on an intended interpretation whereas (1) and (3) are naturally understood as true. Many planets other than the earth have moons. Hence there is more than one moon. Hence (2) and (4) are false on the intended interpretation. There are various options:

**`(a)`** Regard (1) and (4) as elliptical for something like “The earth’s moon is cold”, “the earth’s moon exists”. This may seem acceptable in the present case, but a speaker may utter something similar without having any idea of how to complete it in that kind of way. For example, one who utters “The door is closed” in a room with many doors, may not have troubled to think of any restriction on “door” which only one door satisfies.

(b) Restrict the domain of intended interpretations, or restrict what an intended interpretation assigns to “F”. The restriction might be to Earth moons or contextually salient moons. It may be hard to give any general rule whose application would do justice to the meaning of English sentences. Such issues were relatively unimportant to Russell himself, whose initial interest in definite descriptions was in connection with mathematics, in which such contextual sensitivity does not typically arise.

The only serious alternative Q-formalization of (1) and (3) uses a name-letter for "the moon". One advantage of formalizing (1) by (*`2)`*, in accordance with Russell's theory of descriptions, is that this captures the validity of some arguments that the name-letter approach cannot capture, for example

*`5)`* The moon is cold. Therefore a moon is cold

and

6) The author of Mein Kampf is a maniac. Hitler wrote Mein Kampf. Therefore Hitler is a maniac.

The name-letter method yields the following:

7) $G\alpha; \exists x(Fx \land Gx)$

(the correspondences being “G” for “is cold”, “α” for “the moon”, “F” for “is a moon”) and

8) $F\alpha, G\beta; F\beta$

(the correspondences being “F” for “is a maniac”, “α” for “the author of Mein Kampf”, “G” for “wrote Mein Kampf” and “β” for “Hitler”). Both of these are patently invalid, whereas (*`4)`* and (5) are valid.

On Russell's theory, by contrast, we get the following Q-valid formalizations:

9) $\exists x(Fx \land \forall y(Fy \to x = y) \land Gx); \exists x(Fx \land Gx)$

(the correspondences being “F” with “is a moon” and “G” with “is cold”) and

10) $\exists x(Fx \land \forall y(Fy \to x = y) \land Gx), F\alpha; G\alpha$

(the correspondences being “F” with “wrote Mein Kampf”, “G” with “is a maniac” and “α” with “Hitler”). The Q-validity of (9) is evident. (10) is also Q-valid: an interpretation upon which the premises are true will assign a set containing just one object to “F” (on the intended interpre- tation, “F” will be assigned the set of writers of Mein Kampf, that is, just Hitler), and this object will both be assigned to “α” and belong to what is assigned to “G”. This ensures that any interpretation upon which the premises are true is one upon which the conclusion is true also.


The fact that Russell’s theory of descriptions makes it possible to reflect the validity of some arguments whose validity cannot be captured by the method of name-letters would decisively establish its superiority only if the arguments in question were formally valid. Here, however, we find a circle: they are formally valid iff “the” is a logical constant, and, by the present standards, “the” is a logical constant iff Russell’s theory of descriptions is correct. Then, and only then, is it definable in terms of the stipulated constants “all”, “some”, “if” and “is the same as”.

Ex. 4.18 Russell gave an argument in favour of his theory of descriptions on the following lines:

> “The King of France is bald” is obviously false, since France is a Republic.
>
> But then it would seem that “The King of France is not bald” ought to be true.
>
> My theory can explain how this is possible.

The explanation involved discerning a scope ambiguity in “The King of France is not bald”. Use distinct Q-formalizations of this sentence (stating the intended correspondences) to bring out the ambiguity. Cf. Russell [1905], p. 53.

If we tried to use name-letters to formalize sentences like (*`3)`* (“The moon exists”) we would represent all of them as true, even

11) The golden mountain exists.

For all would be formalized as “Fα”, which entails

12) $\exists x (x = \alpha)$.

This connects with an argument for Russell’s theory of descriptions mentioned in §7: (i) some definite descriptions – we will call them “empty” ones – stand for no object, for example, “the golden mountain”; and (ii) all definite descriptions should be treated in the same way. Since the empty descriptions cannot be adequately formalized by means of a name-letter, (ii) tells us that none should be. Since there are only these two candidates for methods of formalizing, Russell's triumphs.


To reiterate why an empty description cannot be adequately formalized by a name-letter: our standard of adequacy for a formalization is that its truth-upon-an-intended-interpretation conditions should match the truth conditions of the original English. But what could be an intended interpretation when an empty description is formalized by a name-letter? We have to choose some object, since every interpretation assigns objects to all name-letters. Perhaps we should designate an arbitrary object, say the number 0 or the null set, as what an intended interpretation should assign to a name-letter which corresponds to an empty description (cf. Frege [1892b], p. 70). But it seems that whatever object we choose we will get the wrong result. Thus

*`13)`* Someone was the unique author of *Principia Mathematica*

is false (it was jointly authored by Russell and A. N. Whitehead), whereas

*`14)`* No one was the unique author of *Principia Mathematica*

is true. Formalizing by the method of name-letters would yield, respectively, (12) and its negation:

15) $\neg \exists x (x = \alpha)$

Whatever object we choose as what an intended interpretation assigns to “$\alpha$”, (12) will be true upon the interpretation and (15) will be false. This gets the truth values just the wrong way about, so there is no adequate formalization to be had by this method.

According to Russell’s theory of descriptions, sentences which would naively be classified as identity sentences are formalized not as identity sentences but as existential quantifications. For example, we might naively classify

*`16)`* Scott was the author of *Waverley*

as an identity sentence. However, an appropriate Q-formalization, using Russell’s theory of descriptions, is:

17) $\exists x(Fx \land \forall y(Fy \rightarrow x=y) \land x=\alpha)$

where “F” corresponds to “wrote Waverley” and “α” to “Scott”. This Q-sentence, being dominated by an existential quantifier, must be classified as an existential quantification and not as an identity sentence. In particular, something of the form of (17) does not yield a premise fit for an application of *`(8.5)`*, the substitutivity of identicals.² Russell [1905] thought he could establish this by the fact that whereas George IV wished to know whether Scott was the author of Waverley, he did not wish to know whether Scott was Scott.

Ex. 4.19 George IV perhaps wished to know whether Hesperus was Phosphorus but not whether Hesperus was Hesperus. Evaluate the impact this has upon Russell’s argument for the conclusion that (10.*`16)`* is not an identity sentence.

Russell’s view also represents some initially plausible principles as false, for example:

18) The F which is G is F;

The F which is G is G;

19) “The F is not G” is the negation of “The F is G”.

The Q-formula corresponding (18) is not Q-valid, and there are two Q-formulae corresponding to “The F is not G”, only one of which is the negation of a Q-formula corresponding to “The F is G” (see Ex. 4.18). Russell exploited the attractiveness of these principles in an argument against a position he attributed to Meinong, according to which there are no really empty definite descriptions, merely some which refer to non-existent things. If this view is combined with (18) and (19) it leads to contradiction, as we can see by putting “square” for “F” and “not square” for “G”.

Ex. 4.20 Show how to derive a contradiction from *`(10.18)`* and *`(10.19)`*. How should someone who accepts the view Russell attributed (possibly incorrectly) to Meinong respond?


The principle that all definite descriptions should be treated alike is open to question. If we apply the same sort of principle to names, saying that all names must be treated alike, we find that we should treat "Vulcan" and "Reagan" alike. Since, for reasons already seen in §7, we cannot formalize "Vulcan" by a name-letter we also should not formalize "Reagan" by a name-letter. Russell himself accepted this consequence. Indeed, he held that the only expressions that could be adequately formalized by name-letters were expressions that we do not ordinarily classify as names (but rather as demonstrative pronouns): "this" and "that", as these are used to refer to momentary subjective experiences (these are his so-called "logically proper" names: Russell [1918], pp. 200–1). We will return in §12 to the question of names and descriptions.

Ex. 4.21 (a) Use the "exactly one" quantifier of *`(9.15)`* to formalize "The moon is cold".

(b) Using Russell's theory of descriptions where appropriate, formalize the following, giving alternative formalizations in any cases of ambiguity:

(i) The cat sat on the mat.

(ii) The cat did not sit on the mat.

(iii) The cat did not sit on the mat, but on the table.

(iv) The average family has 2.4 children.

(v) Someone was the unique author of *Principia Mathematica*.

(vi) Sally ate some of the cakes.

Russell's own first response to the problem of formalizing descriptions was to introduce a new device, going beyond the syntax of Q, the (inverted) iota-operator, “i”. This is a variable binding operator, rather like a quantifier, but it forms what at first look like singular terms. Using it, one could write (1) as

20) is cold $(\iota x)(\text{moon } x)$.

This could be expressed in something more like English as “$(\iota x)(\text{such that } x \text{ is a moon})$ is cold” or “the $x$ such that $x$ is a moon is cold”. Russell found that in order to indicate the scope of these apparent singular terms he needed further complications (see *Principia Mathematica*, Russell and Whitehead [1910], *14.03). He claimed that the iota-

expressions were strictly unnecessary: wherever they occur, one can use the methods exemplified by (2) and (4) to replace them by ordinary Q-formulae. Russell called the iota-expressions, like “$(\iota x)(\text{moon } x)$”, “incomplete symbols”, because they do not need to be “completed” by an object in the world in order to function significantly in language.

## 11 Existence

(10.3) and (10.*`13)`* raise the question of how we should formalize sentences which affirm or deny existence. The latter could have been rephrased:

1) The unique author of *Principia Mathematica* does not exist.

This is not very idiomatic as compared with (10.13), but it seems to mean the same. We are perhaps more familiar with this phrasing in mathematical contexts, for example:

2) The greatest prime number does not exist.

There are also such truths as

*`3)`* Vulcan does not exist,

in which a name is used rather than a description.

“∃” is the “existential” quantifier, so one might expect it to have a role to play in formalizing assertions and denials of existence. On the other hand, “exists” is grammatically a predicate, so one might think to formalize it by means of a predicate-letter.

An example of a use of “exists” which cries out for treatment by “∃” is

*`4)`* Mad dogs exist.

Though “exists” is grammatically a predicate, its function here is not to predicate existence of each and every mad dog. Rather, its role should be compared with “rare” in

5) Mad dogs are rare.

"Rare" does not predicate rareness of each mad dog and is not appropriately formalized by a predicate-letter. The interpretation of a predicate letter (of degree 1) will assign it a set of objects, of each one of which the predicate-letter is, on the interpretation, true. "Rare" is not an expression which intelligibly applies to a single object; and it is tempting to think that the same goes for "exists". There is certainly a difficulty in understanding "exists" as like an ordinary predicate in denials of existence, for example:

6) Mad dogs do not exist.

It is clear that there is no object in the universe of which it is being said that that object does not exist.

Ex. 4.22 What, if anything, would be wrong with the view that an intended interpretation should assign its domain to a predicate-letter used to correspond to "exists"?

Suppose we try to use a predicate-letter to correspond to "exists" in these cases. We might try formalizing (4) by

*`7)`* $\forall x((Fx \land Gx) \to Hx)$

and (6) by

8) $\forall x((Fx \land Gx) \to \neg Hx)$

with "F" corresponding to "is a dog" "G" to "is mad" and "H" to "exists". If there are no mad dogs, both (7) and (8) come out true, upon an intended interpretation, whereas (*`4)`*, which (7) is supposed to formalize, should certainly be false in this case. If we try instead

9) $\exists x(Fx \land Gx \land Hx)$

for (*`4)`*, and

10) $\exists x(Fx \land Gx \land \neg Hx)$

for (6) (with correspondences as before) we find that both require for their truth upon an intended interpretation that the domain should contain mad dogs which, on the face of it, is just what (6) denies.

One attempt to meet this difficulty involves distinguishing between being and existence. The category of being is the wider, embracing plenty of non-existent things, like Pegasus, the golden mountain, round squares, as well as the existing things like Ronald Reagan and Italy. The existential quantifier, expressed in English by “there is”, relates to the category of being, “exists” to the narrower category of existence. Thus

11) There are things which do not exist

expresses a truth, on this theory. It could be formalized, with correspondences as before, as

*`12)`* $\exists x\neg Hx.$

Let us call this “Meinong’s Theory of Existence” after a famous proponent of a not too dissimilar view. Russell accused the view of showing a “lack of that robust feeling for reality which must be preserved in logical studies” ([1919], p. 170). One may not feel that this observation is enough to refute the view. However, Russell did show that the logical considerations under discussion in this section do not on their own force one to adopt it.

In the case of (4) and (6), non-Meinongian formalizations are attained by using the existential quantifier to correspond to “exists”, rather than a predicate-letter:

13) $\exists x(Fx \land Gx)$

14) $\neg \exists x(Fx \land Gx)$

with “$F$” corresponding to “is a dog” and “$G$” to “is mad”. So some sentences containing “exists” can be adequately formalized using “$\exists$” rather than a predicate-letter.

The cases so far discussed have had plural subjects (for example, “mad dogs”). I now turn to singular existential sentences, for example (3):

Vulcan does not exist.

This is a negative sentence, and we should also have an example of a positive one:

*`15)`* The third man exists.

Imagine (*`15)`* to be uttered in connection with some intrigue. There is a debate about how many people were involved. You believe there were three: two well-known villains and a third whose name you do not know. You might utter (*`15)`* to state your position on the controversy.

We cannot in any straightforward way apply the policy adopted in the plural case to the singular case. In (4),

Mad dogs exist,

the plural subject contained predicates for the quantifier to attach to. (3) does not on the face of it contain such a predicate. If we try to formalize it by

*`16)`* ¬∃xFx,

we need to ask what “F” corresponds to. It seems it must correspond to “Vulcan”, but it cannot do that since it has to correspond to a predicate and “Vulcan” is a name. We will return to this question shortly.

In the case of (*`15)`*, we would have exactly the same problem, if we were to think of “the third man” as formalizable by a name-letter. The fact that there are predicates contained in the phrase should encourage the view that they could be made accessible to existential quantification. The theory of descriptions given in §10 has the merit of taking seriously the fact that definite descriptions contain predicates. If we mechanically apply the theory to (*`15)`*, the result is:

17) ∃x(Fx &amp; ∀y(Fy → x = y) &amp; Gx)

where “F” corresponds to “is a third man” and “G” to “exists”. However, if we agree with Russell, we will hold that everything exists. In that case, the intended interpretation of “G” will be the domain of interpretation. This means that “&amp; Gx” adds nothing to the truth-upon-an-interpretation conditions of (17). So we might as well formalize (*`15)`* as

18) $\exists x(Fx \land \forall y(Fy \rightarrow x = y))$

(with $F$ as before). The remaining part of Russell’s theory of descriptions proposed precisely this. Your opponent’s denial of (15) will be formalized by prefacing (18) with $\neg$. These formalizations seem adequate, yet avoid the view that there are things that do not exist.

We saw in §7 that “Vulcan” cannot be adequately formalized by a name-letter. This blocks the formalization of (3) as

19) $\neg F\alpha$

with $F$ corresponding to “exists” and $\alpha$ to “Vulcan”. The previous paragraph, however, suggests how one might find existential quantifier formalizations of “exists” as it occurs in (*`3)`*: discern a hidden predicate beneath the occurrence of the name “Vulcan”. Two versions of this approach are available.

20) $\exists x\ x = \alpha$

asserts the existence of whatever the interpretation assigns to $\alpha$. It does so by saying that something exists which is identical to $\alpha$, which is just a way of saying that $\alpha$ exists. (This corresponds to the English equivalence between “Napoleon exists” and “There is something which is (identical to) Napoleon”.) The name-letter $\alpha$ is converted into a predicate $= \alpha$ – an expression which when coupled with a name or name-letter forms a sentence. This is one way to find a predicate hidden in the occurrence of a name, and it can be applied generally (cf. Quine [1948], Hochberg [1957]). Applying it to (*`3)`*, we could see it as saying that it is not the case that something is identical to Vulcan, and formalize it as:

21) $\neg \exists x\ x = \alpha$

with $\alpha$ corresponding to “Vulcan”.

The trouble with this suggestion is that (21) is not true upon any interpretation, whereas (3) is true, so the formalization is inadequate.

**`(20)`** is Q-valid, that is, true upon every interpretation. By (2.2), **`(20)`** is true upon an interpretation $i$ iff $\beta = \alpha$ is true upon some $\beta$-variant

interpretation. There is a $\beta$-variant of any $i$, an interpretation which assigns the same object to both $\alpha$ and $\beta$. We rely upon the stipulation that every domain contains at least one object; if the empty domain were allowed, there would be no interpretation with respect to it which assigned one and the same object to the two name-letters. (For a relaxation of these stipulations, see §20.)

One way to find a predicate hidden in a name, as just described, sees the name, $n$, as concealing a predicate “$= n$”. We have seen that this will not always yield the desired results. The other proposal is more radical. It is that at least some names are “really” definite descriptions, in an abbreviated or truncated form. Perhaps “Vulcan” abbreviates the definite description “The intra-mercurial planet”. Then (*`3)`* is equivalent to

22) The intra-mercurial planet does not exist

and we have already seen how (for (15)) one could give an adequate Q-formalization of a sentence like this (as (18)). If we hold to the view that everything classified as a name in English should be treated alike, and take it that the truth of (*`3)`* gives us a compelling reason to regard “Vulcan” as really a definite description, then we are committed, as Russell was, to the view that all English names are really “abbreviated” or “truncated” descriptions (Russell [1918], pp. 200, 24*`3)`*.

To summarize: in formalizing plural affirmations and denials of existence, like “Mad dogs exist”, the quantifier approach gives the right result and the predicate-letter approach the wrong result. Singular assertions and denials of existence superficially divide into two categories: (i) those involving a name, like “Vulcan exists” and (ii) those involving a description, like “The third man exists”. Assuming that we adopt Russell’s general recipe for formalizing descriptions, the quantifier does all that is needed in regard to (ii). Use of a predicate-letter corresponding to “exists” would be otiose, unless one accepts Meinong’s theory. Existential sentences in (i) can only be adequately Q-formalized if they are “really” in category (ii): that is, if the names in question are treated as “really” descriptions. Whether this seeming distortion of English can be justified is discussed in the next section, which, as it departs from the question of Q-formalization, can be omitted without loss of continuity.

Our policy will be to formalize English names by name-letters, unless, as in (3), this leads to an inadequate formalization.

Ex. 4.23 (a) Formalize the following, noting any difficulties: Not all the characters in fiction exist.

> *(b) Assess the following argument: “As regards the actual things there are in the world, there is nothing at all you can say about them that in any way corresponds to this notion of existence. . . . if there were such a thing as this existence of individuals that we talk of, it would be absolutely impossible for it not to apply, and that is the characteristic of a mistake.” (Russell [1918], p. 241.)*
>
> (c) Assess the following argument: “Exists” is not a logical predicate; that is to say, there is no corresponding predicate in first-order logic.

## 12 Are names “really” descriptions?

One of Russell’s motivations for holding that English names are definite descriptions sprang from his engagement in a project very similar to that of finding Q-formalizations of all English sentences. He was using a richer language than Q, the language of *Principia Mathematica*, but its richness has no bearing on the issue we are now discussing, so I shall bracket that difference. Russell believed that some interpretation of Q would express anything that could be said or thought in any language, and Q would have the advantages of clarity, and accessibility to logical manipulations. This belief entails that at least some apparent names (e.g. “Vulcan”) are descriptions, and yields a more general conclusion if we assume that all names should be treated alike. This was not Russell’s only reason: names, especially in the context of existential sentences, raise problems quite independently of the project of Q-formalization. This section briefly introduces some of those problems.

(i) Consider again (11.*`3)`*: Vulcan does not exist.

This is true (or so we all ordinarily believe). But how does the sentence work? It appears to introduce an entity, viz. Vulcan, and then go on to say of this entity that it does not exist. Unless we are Meinongians, a sentence which does that would be contradictory, and not true. The description theory dissolves this mystery. "Vulcan" does not introduce an entity, but rather a claim to the effect that exactly one thing has a certain property (being a planet between Mercury and the sun), and the rest of the sentence serves to negate that claim.


(ii) Consider how names are learned. It is as often as not by means of a definite description. "Who was Gödel?", you enquire. When I tell you that he was the Austro-Hungarian logician best known for his proof of the incompleteness of arithmetic, you come to be in a position to use the name. A natural hypothesis is that the mechanism here is definition: the description defines the name, and thus gives you its meaning.

(iii) Consider those names which have bearers (like "Reagan" and unlike "Vulcan"). Understanding such a name involves knowing who or what its bearer is. How is this knowledge represented in your mind? A natural answer is that it is represented by a definite description: if someone uses a name, N, he must be able to answer the question: "who or what do you mean by N?", and it seems the only appropriate answer he could make would consist either in pointing to the bearer of "N" or in citing a description true of it.

(iv) Consider an identity statement like

1) Lewis Carroll is Charles Dodgson.

This is no trivial truth, but a discovery that became known to a wider and wider circle in the late nineteenth century. Suppose that, instead of the view that names are really descriptions, we hold the view that a name simply stands for an object. Then it seems hard to explain how you could understand both of the names "Lewis Carroll" and "Charles Dodgson" without knowing that (1) is true. In understanding each, you must know who or what the name stands for, so how could you fail to know that they stand for the same object? Yet clearly one can understand (1) without knowing whether it is true, and this is incontrovertibly allowed for by the description theory: you may associate the names with different descriptions.

I now turn to some criticisms of the description theory, and comment on the above four arguments for it.

(a) It would seem that two people could both understand a name perfectly well, yet associate different descriptions with it. If you are a White House janitor you may associate quite different descriptions with "Reagan" from those associated with the name by an El Salvadorian, perhaps living beyond the reach of television. So do we have to say that the name is ambiguous? This would seem implausible.

Russell was quite well aware of this issue, and explained how it was no objection to his theory (however objectionable it may be to theories sometimes attributed to him, for example by Kripke [1972], p. 27). He allowed that two people could communicate satisfactorily using a name, even though they associated different descriptions with it, provided that the different descriptions were true of the same thing. The definite description which a name "really" is should not be thought of as something that has to be common to speaker and hearer when they communicate. Rather, the relevant definite description varies with speaker and occasion: it is whatever description would make explicit the thought in the speaker or thinker's mind on the occasion in question (Russell [1912], p. 29). There is no one description steadily and universally associated with the name. Hence in one good sense of "meaning", that in which meaning is what is common to speaker and hearer in communication, Russell's theory is not intended as an account of the meaning of names.

Ex. 4.24 (a) Say whether you think Russell's account of the relation between names and descriptions makes it vulnerable to the following line of argument:

Suppose the description associated with "Reagan" is "The President of the United States (in 1987)". Then the proposition expressed by "Reagan is the President of the United States" is the same as that expressed by "The President of the United States is the President of the United States". But the second of these is trivial and the first is not, so they cannot express the same proposition.

(b) Comment on the following argument, preferably in the light of reading Russell [1912], pp. 29-31:

The claim that names are descriptions is ambiguous between an claim (that for every name, there is a description such that whenever the name is used it is equivalent to the description) and an claim (that for every name, every occasion of its use, there is a description to which it is equivalent). The former is wildly implausible; Russell's is the latter.

This very fact, however, may make the logician regard the theory as unsuitable for his purposes. If someone asserts something, the logician will want to know the consequences of what is asserted. These consequences need to derive from something publicly shareable, to derive from something common to speaker and hearer in communication. If someone idiosyncratically thinks of Reagan via the description "The person who always misses the ashtray when stubbing out his cigarettes", we do not want to count as a consequence of this man's assertion that Reagan will give a press release today, that someone who misses the ashtray when stubbing out his cigarettes will give a press release today. Descriptions deriving from these subjective sources are not appropriate for the study of logic (cf. Frege [1892b], p. 59).

(b) The argument of (i) is probably the strongest. Its immediate application is only to names without bearers. Its strength lies largely in the absence, until quite recently, of a plausible non-Meinongian alternative (cf. Evans [1982], ch. 10).

Russell thought one should treat names with and without bearers in the same way on the grounds that one might not know, of some group of names, which have bearers and which do not, even though one understood all the names in the group, so that the use of a name does not make the appropriate division. For example, we can sensibly discuss whether or not Homer existed. In doing so, we use the name "Homer", presumably correctly, without knowing whether it is a name with a bearer or a name without. Logic is supposed to proceed without empirical knowledge, drawing just on the understanding of sentences. So logic ought not to discriminate between names with bearers and names without. This certainly puts the onus on the person wanting to discriminate to find a distinction between the two classes that shows up in the use of language.

(c) The argument of (ii) is not decisive, since the phenomena adduced are consistent with the view that the use of the description in learning is to get the learner to know who or what the bearer of the name is. This task can be achieved without giving an expression which means the same as the name (cf. Kripke [1972], pp. 53 ff.).

(d) It is not clear that, as (iii) alleges, we can always give a definite, uniquely identifying, description corresponding to every name we use with understanding. Suppose we notice someone on our way to work each day whom we inwardly name "Fred". We can recognize him when we see him, but any attempt to describe his features will probably (as the police know only too well) yield a description which fits hundreds of people.


**`(e)`** The argument of (iv) is fallacious. There is no valid argument from

$$ a = b $$

He knows what the name "a" stands for

He knows what the name "b" stands for

to

He knows that "a" and "b" stand for the same thing.

Imagine Dodgson's colleagues at Christ Church, who obviously understand the name "Dodgson" and know who Dodgson is. In addition, they are aware of Lewis Carroll's success, and so understand the name "Carroll", and know who Carroll is. They may have no basis for supposing that that Dodgson is Carroll.

**`(f)`** On Russell's theory of descriptions, "the" is a kind of quantifier, meaning "there is exactly one . . .". It is plain that we can understand a sentence like

2) The inventor of the jet engine died in poverty

without (by one natural standard) knowing who the inventor was or even if there was one. (Perhaps the jet was the product of team research.) In particular, if there is a unique inventor, we need have no link with him in order to understand the sentence. (2), on Russell's theory, is a general statement: no particular object enters into its interpretation.

We tend to think of names otherwise. Understanding

3) Frank Whittle died in poverty

does require knowing who Whittle was. We have to have met him or been told about him or seen traces of him in order to use his name.

It seems that the conditions required for using a name are different from those required for using a definite description, and this counts against Russell's theory that names are descriptions.

## 13 Structural ambiguity in English

Q has no structural ambiguity. One way to clarify structural ambiguities in English (see chapter 1.12) is to provide distinct Q-formalizations, one for each distinct reading of the English. Being structurally ambiguous is treated as having more than one logical form.

It is often said that

1) Everyone loves someone

is ambiguous between a (weak) reading upon which everyone is such that there is someone he loves, and a (strong) reading according to which some lucky person is loved by everybody. With “Fxy” corresponding to “x loves y” the unambiguous formalizations are, respectively:

2) $\forall x \exists y Fxy$

and

3) $\exists y \forall x Fxy$.

The strong reading entails the weak:

4) $\exists y \forall x Fxy \models_{Q} \forall x \exists y Fxy$

but the converse does not hold.

Ex. 4.25 Specify an interpretation upon which $\forall x \exists y Fxy$ is true but $\exists y \forall x Fxy$ is false.

The inference from $\forall \exists$ to $\exists \forall$ is known as the “quantifier shift fallacy” and it is commonly attributed to philosophers and others. For example, there is an argument for a foundationalist view of knowledge which, denuded of some of its protective covering, runs as follows:

*`5)`* Every justification of a proposition has to end somewhere. Therefore some propositions cannot be justified, but have to be taken for granted.

#### Ex. 4.26 Formalize (13.5) to show that it is an instance of the quantifier shift fallacy. (The argument of Ex. 4.24b depends upon exposing an example of this fallacy.)

Some of the ambiguity of (1.12.9) was of this kind:

Logic, epistemology and metaphysics are all the philosophical subjects there are. Nicholas has written a book about logic. Nicholas has written a book about epistemology. Nicholas has written a book about metaphysics. Therefore, Nicholas has written a book about every philosophical subject.

The correspondences:

- “α” for “logic”;

- “β” for “epistemology”;

- “γ” for “metaphysics”;

- “δ” for “Nicholas”;

- “F” for “is a philosophical subject”;

- “Gxy” for “x has written y”;

- “Hxy” for “x is about y”;

- “J” for “is a book”.

The premises have no structural ambiguity, and can be formalized as follows:

6) $\forall x(Fx \rightarrow (x = \alpha \lor x = \beta \lor x = \gamma))$

$$\exists x(Jx \land G\delta x \land Hx\alpha)$$

$$\exists x(Jx \land G\delta x \land Hx\beta)$$

$$\exists x(Jx \land G\delta x \land Hx\gamma).$$


The weak version of the conclusion upon which the argument is valid is

*`7)`* $\forall x(Fx \rightarrow \exists y(Jy \land G\delta y \land Hyx)).$

The strong version of the conclusion upon which the argument is invalid is:

*`8)`* $\exists y(Jy \land G \delta y \land \forall x(Fx \rightarrow Hyx)).$

**`(7)`** is consistent with Nicholas writing various books, perhaps one on each of the three subjects. (8) requires him to have written a compendious book, treating all the subjects at once. In **`(7)`** the universal quantifier has wide scope relative to the existential quantifier. In (8) the scopes are reversed, the universal falling in the scope of the existential.

The use of variables in $\mathbf{Q}$ helps keep track of the application of quantifiers. In (8) it is important which quantifier is applying to the first position in "$Hyx$" and which to the second. This is shown by the attachment of "$x$" to both the universal quantifier and the second position, and "$y$" to both the existential quantifier and the first position.

Pronouns sometimes play a similar role in English, as in

*`9)`* Someone called today and he brought his wife.

They also play another role, as shorthand for the reapplication of a name, as in

*`10)`* Oscar kissed Joan and he made her cry.

Here "he" and "her" are stylistic variants of the reuse of "Oscar" and "Joan".

Ex. 4.27 (a) Why cannot the "he" in (13.9) be regarded as a stylistic variant of the reuse of "someone"?

(b) Why cannot the "himself" in the following be regarded as a stylistic variant of the reuse of "every American"?

Every American admires himself.

(Cf. McCawley [1981], p. 126.)

Sometimes it is unclear in English which role a pronoun is playing, for example "he" in

11) If Oscar kissed anyone, he will be pleased.

The formalization upon which "he" is equivalent to a reuse of "Oscar" is

12) $\forall x(F \alpha x \rightarrow G \alpha)$

with “$Fxy$” corresponding to “$x$ kissed $y$”, “$G$” to “is pleased” and “$\alpha$” to “Oscar”. The formalization upon which “he” marks the application of the quantifier is

13) $\forall x(F \alpha x \rightarrow Gx)$.

**Ex. 4.28 Which of (13.12) and (13.13) suggests that Oscar kissed a male person?**

The word “only” often gives rise to ambiguity in English.

14) John only eats organically grown vegetables

would normally be interpreted in a way consistent with John eating meat, the claim being that, as far as vegetables go, all the ones he eats are organically grown. This reading is formalized

15) $\forall x((F \alpha x \land Gx) \rightarrow Hx)$

with ���$Fxy$” corresponding to “$x$ eats $y$”, “$G$” to “is a vegetable”, “$H$” to “is organically grown”, and “$\alpha$” to “John”.

In my view, the more correct reading of (14), the reading that would be favoured by teachers of English, entails that John eats nothing but vegetables. This reading is formalized

16) $\forall x(F \alpha x \rightarrow (Gx \land Hx)).$

This is not literally a scope difference in Q: it is not that (15) and (16) differ only in point of the relative scopes of some pair of operators. The phenomenon is more like the ambiguity that can arise concerning the multiple qualification of noun phrases. For example, in

17) John is a dirty window cleaner

it is unclear whether “dirty” is meant to qualify the complex “window cleaner” or just the word “window”. The alternatives are brought out respectively by the very approximate formalizations:

18) $\exists x(Fx \land Gx \land H \alpha x)$

19) $\exists x(Fx \land G \alpha \land H \alpha x)$

with “$F$” corresponding to “is a window”, “$G$” to “dirty”, “$H$” to “$x$ cleans $y$” and “$\alpha$” to “John”. The formalizations are only very approximate, for it takes more (and also perhaps less) than cleaning one or a dozen windows to be a window cleaner.

**Ex. 4.29** Which of (13.18) and (13.19) requires Harry to be dirty?

Representations based on Q can clarify structural ambiguities in English sentences, even when those sentences resist Q-formalization in any reasonably revealing way. The technique involves mixing English and Q. For example,

20) I am trying to buy a house

is ambiguous between the claim that there is a house I have set my eye on and towards which my buying efforts are directed, and a claim which can be true even if there is no such house — even if all I have done is ask the real estate agents to send details. We could represent these claims as follows:

21) $\exists x(x \text{ is a house} \land \text{I am trying to buy } x).$

22) I am trying to bring it about that: $\exists x(x \text{ is a house } \land \text{ I buy } x).$

This is, or is analogous to, a scope distinction: in (21), “$\exists$” has wide scope relative to “trying”, in (22) narrow scope. We sometimes express the first reading in English by saying “I am trying to buy a particular house”. All houses are particular houses, so “particular” here is not serving to qualify “house”; it is best seen as effecting a scope distinction.

In discussions of the theory of knowledge, it is often claimed that

23) If you know you can’t be wrong

is ambiguous in a way which can be represented as follows:

24) necessarily $\forall x \forall y(x \text{ knows that } y \rightarrow y \text{ is true}).$

25) $\forall x \forall y(x \text{ knows that } y \rightarrow \text{necessarily } y \text{ is true}).$

This is also a difference of relative scope. A familiar view in epistemology is that (24) is true, but not terribly interesting, and (25), which indeed entails wholesale scepticism about the contingent, is false.

Russell gave a pleasing example of a scope distinction. He argued that

26) I thought your yacht was longer than it is

could be heard as an absurd claim, deserving the reply: “Everything is just as long as itself”. With “F” corresponding to “x uniquely numbers in meters the length of y”, “Gxy” for “x is greater than y”, and “α” for “your yacht” (ignoring, for present purposes, our earlier resolution to treat definite descriptions, like “the yacht which you own”, by Russell’s theory), the absurd claim could be represented as:

27) I thought that: $\exists x(Fx\alpha \land Gxx)$.

What the speaker of (26) no doubt meant is something more like:

28) $\exists x(Fx\alpha \land \exists y((I \text{ thought that } Fy\alpha) \land Gyx)).$

“Gyx” is not part of the thought I attribute to myself in uttering (26). A more long-winded clarification is: the length I thought your yacht was is greater than the length it actually is.

In ethics, people ask whether there can be genuinely incompatible obligations. One way in which the issue might be made more precise is by asking whether it is ever possible for the following both to be true:
29) You ought to do $A$

30) You ought not to do $A$

where “A” stands for some type of action. It is unclear whether (30) is really the negation of (29). Arguably, it is ambiguous between:

31) It is not the case that you ought to do $A$

and

32) You ought to do not-$A$.

In (31), "not" dominates the sentence, in (32) it has narrow scope relative to "ought". Classical logic precludes the joint truth of (29) and (31), for they have the overall logical form of $p$ and $\neg p$. If there are incompatible obligations in this sense, logic needs to be revised. By contrast, classical logic as such finds nothing problematic in the joint truth of (29) and (32).

Ex. 4.30 (a) Use distinct Q-formalizations to bring out any ambiguities in the following:

(i) Winston is always smoking a big cigar.

(ii) He always carries a large stick.

(iii) Only non-smoking males are eligible for this job.

(iv) I watched the tennis-match in bed.

(v) Only sensible dogs are taken by somebody kind for all their walks.

(vi) Everyone has a problem.

(b) Use mixed English and Q-formalization (in the manner of (13.21), (13.22) etc.) to bring out any ambiguities in the following:

> *(i) "In the whole wide beautiful world, Aldo Cassidy was the only person who knew where he was." (Le Carré, The Naive and Sentimental Lover, p. 8)*
>
> *(ii) "Most of all I would like to thank my students, who have taught me more than they know." (E. Bach, [1974], p. vi)*

(iii) Gerry means everything he says ironically.

(iv) If John is to enter a university, he must pass his examinations.

(v) I thought you were someone else.

## 14 Q-validity and decision

There is no method like that of truth tables for determining Q-validity. There are, however, systematic methods for determining, for any Q-valid argument, that it is Q-valid. The trouble is that if such a method has still not pronounced an argument valid (say after a hundred or a million steps), we do not know whether the right thing to believe is that the argument is not valid, or whether the right thing to believe is that the argument is valid but the method has not yet managed to show it.

We can get a feel for Q-validity, without anything so grand as a systematic method, simply by working on some examples. It is not at first obvious whether the following is Q-valid or not:

1) $\forall x \exists y(Fx \to Gy); \exists y \forall x(Fx \to Gy).$

A natural first reaction would be to suppose that it is invalid, by analogy with the invalid

2) $\forall x \exists y Fxy; \exists y \forall x Fxy.$

This reaction would be incorrect. An interpretation, $i$, upon which the premise of (1) is true must either assign the empty set to "$F$" or some non-empty set to "$G$". The conclusion is true upon $i$ iff "$\forall x(Fx \to G\alpha)$" is true upon some $\alpha$-variant, $i'$. If $i(F)$, and so $i'(F)$, are empty, then "$\forall x(Fx \to G\alpha)$" is true upon $i'$ (for reasons spelled out in §3); if $i(G)$ is a non-empty set, then some $\alpha$-variant (agreeing with $i$ on "$F$" and "$G$") will assign to "$\alpha$" a member of what it assigns to "$G$", so again "$\forall x(Fx \to G\alpha)$" will be true on $i$. So however $i$ makes the premise true, it will make the conclusion true also.

If an argument is $\mathbf{Q}$-invalid, we can establish this if we can find a counterexample: an interpretation upon which the premise(s) are true and the conclusion false. For example, an interpretation which assigns to "$F$" the set of ordered pairs whose first member is smaller than the second, and whose domain is the (positive) integers, is a counterexample to the $\mathbf{Q}$-validity of (2).

The equivalences between universal and existential quantifiers

3) $\vdash_{\mathbf{Q}} \exists x Fx \leftrightarrow \neg \forall x \neg Fx$

4) $\vdash_{\mathbf{Q}} \forall x Fx \leftrightarrow \neg \exists x \neg Fx$

can be confirmed by reasoning that uses the same equivalences in the English which we use to describe the interpretations. Thus for (3) a crucial consideration is that any interpretation, $i$, upon which "$\exists x Fx$" is true is one such that there is an interpretation, agreeing with $i$ on "$F$", upon which "$F\alpha$" is true; that is, it is not the case that every interpretation agreeing with $i$ on "$F$" fails to bring out "$F\alpha$" as true; that is, it is not the case that every interpretation agreeing with $i$ on "$F$" brings out "$\neg F\alpha$" as true; that is, "$\forall x \neg Fx$" is false upon $i$; that is, "$\neg \forall x \neg Fx$" is true upon $i$.

Universal quantifications are true only upon interpretations which make the corresponding existential quantification true, for example

5) $\forall x Fx \vdash_{\mathbf{Q}} \exists x Fx.$

However,

6) $\exists xFx \not\vdash_{\mathbf{Q}} \forall xFx.$

Any interpretation which assigns a non-empty set other than the domain serves as a counterexample.

The following general truth reflects the fact that we require an interpretation to assign an object to every name-letter:

7) $X \models_{\mathbf{Q}} \exists \nu X^{\star}.$

This is to be read: for every sentence $X$ for which there is an appropriate $X^{\star}$ (one which results from $X$ by replacing one or more occurrences of a name-letter in $X$ by a variable, $\nu$), every interpretation upon which $X$ is true is one upon which the result of prefixing $X^{\star}$ by “$\exists$” followed by $\nu$ is also true.

8) $\forall x(Fx \to Gx), \exists xFx \not\vdash_{\mathbb{Q}} \exists xGx.$

An interpretation upon which the second premise is true must assign a non-empty set to “$F$��; but for the first premise to be true, the conditional “$F\alpha \to G\alpha$” is true in at least one case in which “$F\alpha$” is true, which means that “$G$” must be assigned a non-empty set. Such an interpretation is one upon which the conclusion is true.

9) $\forall x(Fx \to Gx), \exists xGx \not\vdash_{\mathbb{Q}} \exists xFx.$

A counterexample is an interpretation which assigns the empty set to “$F$”, and a non-empty set to “$G$”.

We need to distinguish between:

10) $\exists x(Fx \land Gx) \not\vdash_{\mathbb{Q}} \exists xFx \land \exists xGx$

and

11) $\exists xFx \land \exists xGx \not\vdash_{\mathbb{Q}} \exists x(Fx \land Gx).$

Ex. 4.31 Establish the truth of (14.10) and (14.11), in the latter case by providing a counterexample.

Working through examples like these should give a good feel for Q-validity, but what has become of an ideal mentioned earlier: that there be an entirely mechanical test for validity in an artificial language fit for logical purposes?

A decision procedure for Q is a mechanical method for determining, with respect to an arbitrary Q-sentence, and in a finite number of steps, whether or not it is valid. The existence of a decision procedure would indeed satisfy the hankering for mechanical tests. However, it can be proved that there is no decision procedure for Q. So that is a hankering which one must simply abandon.

There are systematic procedures which, for every Q-valid Q-sentence will determine in a finite number of steps that it is valid. As one is putting them through their paces, passing from step to step in accordance with the instructions, there is no point at which one can say: we haven't proved the sentence valid, therefore it is invalid. True, there will be a proof of validity in a finite number of steps, if the sentence is valid, but one does not know what that number is, and any number of steps one has taken may fall just short of the number required for a proof of validity.

I will simply mention three systematic procedures, for the benefit of readers who may already be acquainted with them: axiom systems; systems of natural deduction; and semantic tableaux (or tree) methods. Working with these procedures leads to a sharpened perception of Q-validity, and the fact that these procedures exist is, of course, of great importance.

Ex. 4.32 (a) Argue for the truth of the following:

(i) $\forall x(Fx \to Gx) \models_{Q} \exists x(Fx \to Gx)$

(ii) $\models_{Q} \exists x(Fx \vee \neg Fx)$

(iii) $\models_{Q} \forall x((Fx \to Gx) \vee (Gx \to Fx))$

(b) Devise counterexamples to the following. (A counterexample to an argument is an interpretation upon which the premises are true and the conclusion false. A counterexample to a sentence is an interpretation upon which it is false.)

(i) $\forall x(Fx \to Gx); \exists xFx$

(ii) $\exists x \exists y(x \neq y)$

(iii) $\forall x(Fx \to Gx), \exists x \neg Fx; \exists x \neg Gx$

## 15 Formalizing arguments

A valid argument which is not P-valid:

1) John runs. Therefore someone runs.

There is a Q-valid formalization of it:

2) $F\alpha \vdash_{\mathbb{Q}} \exists x Fx,$

with the obvious correspondences. We will for the moment take it for granted that the truth of (2) establishes the validity of (1).

An old favourite:

3) All men are mortal. Socrates is a man. Therefore Socrates is mortal.

This has a valid Q-formalization:

4) $\forall x(Fx \to Gx), F\alpha \vdash_{\mathbb{Q}} G\alpha$

with “$F$” corresponding to “is a man”, “$G$” to “is mortal” and “$\alpha$” to “Socrates”.

One early method of formalizing everyday arguments, Aristotle’s syllogistic, had particular trouble with arguments like:

5) All horses are animals. Therefore all heads of horses are heads of animals.

This is Q-validly formalizable:

*`6)`* $\forall x(Fx \to Gx) \vdash_{\mathbb{Q}} \forall x \forall y((Fx \land Hyx) \to \exists z(Gz \land Hyz))$

with “$F$” corresponding to “is a horse”, “$G$” to “is an animal” and “$Hxy$” to “$x$ is a head of $y$”. We can argue informally for the truth of (*`6)`* as follows. Suppose some interpretation, $i$, verifies the premise. Then every member of $i(F)$ is a member of $i(G)$. To falsify the conclusion, some $\alpha + \beta$-variant of $i$, $i^*$, must verify “$F\alpha \land H\beta y$” and falsify “$\exists z(Gz \land H\beta z)$”, which means that no $\gamma$-variant verifies “$G\gamma \land H\beta y$”. But there

is such a variant, $i'$, where $i'(\gamma) = i^{\star}(\alpha)$. This object belongs to $i^{\star}(F)$ and so to $i'(F)$ and so to $i'(G)$, so $i'$ verifies "$G\gamma$"; and since $\langle i^{\star}(\beta), i^{\star}(\alpha) \rangle$ belongs to $i^{\star}(H)$, the same goes for $\langle i'(\beta), i'(\gamma) \rangle$ and $i'(H)$. So $i'$ verifies "$G\gamma \land H\beta\gamma$". So there can be no counterexample. The idea is that if we have a horse and a head which satisfy the conclusion's antecedent, the premise assures us that we thereby have an animal and a head which satisfy the conclusion's consequent.

Aristotle's syllogistic has been criticized on the grounds that it counts as valid arguments which are not valid. An alleged example is:

*`7)`* All unicorns are self-identical. All unicorns are non-existent. Therefore some self-identical things are non-existent.

Aristotelian logic regarded this as an instance of a valid argument-form because it took the truth conditions of a universal quantification, "All $F$s are $G$s", to require the existence of $F$s. Setting aside the question whether the argument is valid, it is certainly the case that:

*`8)`* $\forall x(Fx \to Gx), \forall x(Gx \to Hx) \not\vdash_{\mathbb{Q}} \exists x(Gx \land Hx).$

An interpretation which assigns the null set to every predicate-letter establishes the truth of (*`8)`*.

Consider

*`9)`* Only the brave deserve the fair. Harry is brave and Mary is fair. So Harry deserves Mary.

*`10)`* $\forall x\forall y((Gxy \land Hy) \to Fx), F\alpha \land H\beta; G\alpha\beta$

with “$Gxy$” corresponding to “$x$ deserves $y$”, “$H$” to “is fair”, “$F$” to “is brave”, “$\alpha$” to “Harry” and “$\beta$” to “Mary” yields a Q-invalid argument. The invalidity can be seen by considering an interpretation which assigns the set of even numbers to “$F$”, the set of odd numbers to “$H$”, 8 to “$\alpha$”, 3 to “$\beta$” and to “$G$” the set of ordered pairs such that the first member of each pair is greater by one than the second.

A valid argument resembling (*`9)`* is:

11) Only the brave deserve the fair. Mary is fair but Harry isn't brave. So Harry doesn't deserve Mary.

With correspondences as before, this can be $\mathbf{Q}$-validly formalized:

12) $\forall x\forall y((Gxy \land Hy) \to Fx), G\beta \land \neg F\alpha; \neg G\alpha\beta.$

The $\mathbf{Q}$-validity is plain if we reflect that all that matters about the premise is its instance “$(G\alpha\beta \land H\beta) \to F\alpha$”, and that the following is true:

13) $(p \land q) \to r, q \land \neg r \models_{\mathbf{P}} \neg p.$

Now for some examples of arguments involving identity, definite descriptions and numeral adjectives.

*`14)`* Hesperus is a planet. Hesperus is identical to Phosphorus. So Phosphorus is a planet.

With “$\alpha$” corresponding to “Hesperus”, “$\beta$” to “Phosphorus” and “$F$” to “is a planet”, we can formalize $\mathbf{Q}$-validly:

*`15)`* $F\alpha, \alpha = \beta \models_{\mathbf{Q}} F\beta.$

Any interpretation upon which the premises are true assigns the same object to “$\alpha$” and “$\beta$” and that object to the set it assigns to “$F$”; so it verifies the conclusion.

Compare:

*`16)`* John believes that Hesperus is a planet. Hesperus is identical to Phosphorus. So John believes that Phosphorus is a planet.

If we could make “$Fx$” correspond to “John believes that $x$ is a planet”, then (16) would be formalizable by (*`15)`*, but, intuitively, (16) is invalid. Suppose John does not realize that Hesperus is identical with Phosphorus. He uses “Hesperus” of a heavenly body he sees in the evening. He uses “Phosphorus” of a heavenly body he sees in the morning (never suspecting that these are one and the same). He believes that Hesperus is a planet, but believes that Phosphorus is not a planet but a star. (When you ask “Is Phosphorus a planet?” he replies, firmly, “No”.) So for this case the premises are true and the conclusion false, so (16) is not valid.

The moral is that “John believes that $x$ is a planet” should not be allowed to count as a predicate. If a predicate is something adequately formalizable by a predicate-letter, the justice of this ruling can be shown not just by the example considered, but more generally. A predicate-letter is, on any interpretation, assigned a set of things of which the predicate-letter is true upon the interpretation. But there is no set of things of which “John believes that $x$ is a planet” is true. This is shown by the fact that Hesperus ought to be both a member of and not a member of any such set, and this is impossible.

Consider

17) Only the fastest walker will reach London. John walks faster than Mary. So Mary will not reach London.

We might offer the formalization

18) $\exists x(\forall y (x \neq y \rightarrow Fxy) \land Gx \land \forall z (Gz \rightarrow z = x)), F\alpha\beta; \neg G\beta$

with “$Fxy$” corresponding to “$x$ walks faster than $y$”, “$G$” to “will reach London”, “$\alpha$” to “John” and “$\beta$” to “Mary”. The idea is to treat the first premise of (17) as saying that someone walks faster than anyone else and will reach London, and no one else will reach London. However, (18) as it stands is not Q-valid. We need to add to the premises “$\alpha \neq \beta$”, and replace “$F\alpha\beta$” by “$\neg F\beta\alpha$”; thus amended, the argument is Q-valid. We have interpreted “only” in such a way that “Only $\alpha$ is $F$” entails “$\alpha$ is $F$”. We have not needed to use Russell’s theory of descriptions to formalize “the fastest walker”, and hence we have not included the uniqueness, which “the” imparts, in the formalization. If “$F$” is assigned the set of ordered pairs such that the first loves the second, then “$\forall y (\alpha \neq y \rightarrow F\alpha y)$” can be true on interpretations differing only in what they assign to “$\alpha$”. That is, more than one person can satisfy the condition of loving everyone else. If no more than one person can walk faster than everyone else, that is to do with the nature of the faster than relation rather than with the logical form of (18).

Ex. 4.33 Are there occurrences of “Only $F$” which are more plausibly interpreted as not entailing that there are $Fs$? (Cf. McCawley [1981], pp. 180–2.)

The following argument requires the uniqueness to be shown in the formalization, if the formalization is to be valid:

19) Only the fastest walker will reach London. John will reach London. So only John walks faster than anyone else.

Using the style of (18), and the same correspondences, we would get:

20) $\exists x(\forall y (x \neq y \rightarrow Fxy) \land Gx \land \forall z (Gz \rightarrow z = x)), G\alpha; \forall x(\forall y (x \neq y \rightarrow Fxy) \rightarrow x = \alpha) \land \forall y (\alpha \neq y \rightarrow F\alpha y)$

This is not Q-valid, though (19) is valid. (20) fails to capture the validity through failing to formalize the uniqueness implied by “the” in the premise. This can be captured by:

21) $\exists x(\forall z (x \neq z \rightarrow Fxz) \land \forall y (\forall z (x \neq z \rightarrow Fyz) \rightarrow x = y) \land Gx \land \forall z (Gz \rightarrow z = x)), G\alpha; \forall x(\forall y (x \neq y \rightarrow Fxy) \rightarrow x = \alpha) \land \forall y (\alpha \neq y \rightarrow F\alpha y)$

The first premise of (21) is easier to read if we see the first part of it as an instance of the familiar:

$$\exists x (Fx \land \forall y (Fy \rightarrow x = y))$$

with “$F$” replaced by “$\forall z (x \neq z \rightarrow Fxz)$”.

#### Ex. 4.34 Provide a counterexample to (4.20).

### Consider

22) Every man has two hands. Every hand has a thumb. So every man has two thumbs.

This may strike one as valid, even reading the “two” in the conclusion as “exactly two”, but only by making explicit a number of presuppositions can it be formalized as Q-valid, with this reading of the conclusion. First, we assume that “two” in the first premise is intended as “exactly two”. Secondly, we assume that “a thumb” in the second premise is intended as “exactly one thumb”. Thirdly, we assume, and make explicit as a third premise, that the relation of having, as obtaining between a person and his bodily parts, is transitive, so that if the person has a hand, and the hand a thumb, then the person has a thumb.

"F" corresponds to "is a man", "Gxy" to "x has y", "H" to "is a hand" and "J" to "is a thumb".

23) $\forall x(Fx \to \exists y \exists z(y \neq z \land Gxy \land Gxz \land Hy \land Hz \land \forall w((Gxw \land Hw) \to w = y \lor w = z))), \forall x(Hx \to \exists y(Jy \land Gxy \land \forall z((Gxz \land Jz) \to z = y))), \forall x \forall y \forall z((Gxy \land Gyz) \to Gxz); \forall x(Fx \to \exists y \exists z(y \neq z \land Gxy \land Gxz \land Jy \land Jz \land \forall w((Gxw \land Jw) \to w = y \lor w = z)))$

The example shows how formalization can bring to light hidden assumptions in an argument.

Finally, a valid argument that is not formalizable as $\mathbf{Q}$-valid:

24) Necessarily, if there is a first moment in time, the history of the universe up to now is finite. Therefore if there had to be a first moment in time, the history of the universe up to now has to be finite.

In a Q-formalization, we cannot reach beyond the non-truth functional sentence connective "necessarily". The deepest Q-formalization of the premise which is not inadequate is "p", and it is obvious that however hard we try with the premise we cannot find an adequate Q-valid argument.

Ex. 4.35 (a) Formalize the following arguments and determine the validity of the formalizations:

(i) Harry loves anyone who loves him. Mary loves Harry. So Harry loves Mary.

(ii) Only Harry loves himself. So only Harry loves Harry.

(iii) No one but Harry lives in the house and Harry is not mad. So the inhabitant of the house is not mad.

(b) This book is silent on the problems of time and tense. Some appreciation of the problems can be obtained by attempting to formalize the following in such a way that the formalizations are Q-valid iff the arguments are intuitively valid (cf. Lacey [1971]):

(i) George is marrying Mary. Mary is an orphan. So George is marrying an orphan.

(ii) George married Mary. Mary is a widow. So George married a widow.

## 16 Attitudes

We saw from (15.*`16)`* that an adequate formalization of “John believes that Hesperus is a planet” cannot match “John believes that $x$ is a planet” with a predicate-letter. It might seem that the task of providing Q-formalizations of sentences of this kind is hopeless. But one should not despair too quickly, since there is a proposal, due to Donald Davidson, for (in some respects adequately) Q-formalizing any sentence of the form “John believes that . . .”, provided that what fills the dots is itself Q-formalizable. Indeed, the essence of the proposal applies more widely, to include also sentences of the forms: “John knows that . . .”, “John said that . . .”, “John wonders whether . . .”. The italicized expressions are called *verbs of propositional attitude*.

Davidson called his proposal “paratactic”, on the grounds that it sees the relevant sentences as really pairs of sentences. Thus

1) John believes that Hesperus is a planet is held to consist of

2) John believes that. Hesperus is a planet.

“That” is held to be a demonstrative pronoun, referring forward to the subsequent “Hesperus is a planet”. The Q-formalization is thus:

Ex. 4.36 On Davidson’s own account ([1969], pp. 105–6) the word “that”, as used in reporting a propositional attitude, refers to the utterance token which follows. (For the distinction between token and type: if you are obey a request to say something twice, you may make two utterance tokens of a single utterance type.)

(a) Evaluate the suggestion that the existence of beliefs that never have been and never will be expressed argues for regarding “that”, in sentences like (16.2), as referring forward to an utterance type rather than a token.

(b) Evaluate the suggestion that the truth of a sentence like John believes that she is happy, uttered in circumstances which make plain the referent of “she”, argues for regarding “that”, in sentences like (2), as referring forward to an utterance token rather than a type.

3) $F\alpha\beta, G\gamma$

with “$Fxy$” corresponding to “$x$ believes $\gamma$”, “$G$” to “is a planet”, “$\alpha$” to “John”, “$\beta$” to “that” and “$\gamma$” to “Hesperus”. An intended interpretation of (*`3)`* will assign to “$\beta$” a certain sentence, namely the second sentence in (2).

This proposal formalizes (15.16):

John believes that Hesperus is a planet. Hesperus is identical to Phosphorus. So John believes that Phosphorus is a planet.

as follows

4) $F\alpha\beta, G\gamma, \gamma = \delta; F\alpha\varepsilon, G\delta$

with “$F$”, “$\alpha$”, “$\beta$”, “$\gamma$” and “$G$” as before, “$\delta$” corresponding to “Phosphorus” and “$\varepsilon$” corresponding to the second “that” (the one referring to “Phosphorus is a planet”). Since the demonstrative pronouns refer to different things, they must be formalized by different name-letters.

Q-validity is strictly speaking undefined for (4), since there are two sentences in the conclusion. A standard proposal is to say that for such an argument to be valid, the truth of at least one of the sentences in the conclusion must be guaranteed by the truth of the premises, and so it is in (4). However, that would clearly not satisfy someone who wanted to use (15.16) in reasoning, for what would matter would be what corresponds to $F\alpha\varepsilon$ rather than what corresponds to $G\delta$. It is clear that the desired truth is not guaranteed by the truth of the premises in virtue of the Q-logical forms of (4). Given the invalidity of (15.16), this is a point in favour of Davidson’s proposal.

The proposal has the merit of giving Q-valid Q-formalizations to intuitively valid English arguments involving propositional attitudes. The valid

*`5)`* John believes that Hesperus is a planet. That is true. Therefore John believes something true

can be given a valid Q-logical form as follows:

*`6)`* $F\alpha\beta, G\gamma, H\beta \vdash_{\mathbb{Q}} \exists x(F\alpha x \land Hx)$

with "H" corresponding to "is true", and other correspondences as before. We have to regard both occurrences of "that" as referring to the same thing, and thus as formalizable by the same name-letter. The fact that English contains a sentence like the conclusion of (*`5)`*, which seems naturally formalizable by the conclusion of (*`6)`*, supports Davidson's proposal by suggesting that "believes" is at least sometimes a predicate of degree two. And if sometimes, why not always?

Ex. 4.37 Using Davidson's paratactic proposal, formalize (making explicit any assumptions you need to make):

John believes that Hesperus is a planet. "Hesperus is a planet" is true. Therefore John believes something true.

A problem with the proposal is that we can also derive “Gγ”, which corresponds to “Hesperus is a planet”. This happens to be true, but it ought not to follow from “John believes that Hesperus is a planet”, and in other cases we would move from truth to falsehood. If we formalize

7) John believes that the earth is flat

as

8) Fαβ, Gγ

(with "α", "β" and "F" as before, "G" corresponding to "is flat" and "γ" to "the earth") we would formalize an argument with (7) as premise and "the earth is flat" as conclusion as Q-valid, which is obviously unsatisfactory. Davidson's proposal involves a contrast between what one asserts, and what one says without asserting. In an assertive utterance of "John believes that the earth is flat", Davidson's theory has it that "John believes that" is asserted, but "the earth is flat" is not asserted. Hence Davidson's view is not subject to the difficulty just noted. But such distinctions are not accommodated within Q.

Ex. 4.38 (a) Using Davidson's paratactic proposal, formalize:

Galileo said that the earth moves, and Newton said the same. So there is something that they both said.

(b) Can Davidson's proposal be modified so as to provide an adequate formalization of, for example,

Referring to Jones' murderer, John said that he was innocent?

See Platts [1979], ch. 5, §5; Hornsby [1977].

(c) Can Davidson's proposal give an adequate account of the truth conditions of, for example,

John believes something which no one has ever or will ever express in an utterance?

See Schiffer [1987], ch. 5.

## 17 Binary quantifiers

There are quantifier expressions with no correlates in $\mathbf{Q}$, for example "most" and "few". Let us see whether we can formalize English sentences containing these quantifiers by just adding them to $\mathbf{Q}$, to form a new language, call it $\mathbf{Q}+$.

We will write the new quantifiers "T" (for "most") and "W" (for "few") and add the syntactic rule that all Q-sentences are Q+ sentences, and if X is a Q+-sentence and X* results from X by replacing a name-letter by some variable, v, not in X, then the following are Q+-sentences:

TvX*, WvX*.

(We need to add that the modes of combination, e.g. by “&amp;”, which form Q-sentences also form Q+-sentences.) Using these quantifiers to formalize sentences which are (in a respect to be made more precise shortly) like “Everything is physical”, there are no problems.

1) Most things are physical

and

2) Few things are physical

are Q+-formalizable as

*`3)`* TxFx

and

4) WxFx.

Thinking just of such cases, appropriate rules for interpretations could be modelled on the rule (2.2vi), replacing talk of all interpretations by talk of most or a few. However, quantifiers thus specified cannot adequately formalize sentences like

5) Most men lead lives of quiet desperation

(or the corresponding optimistic sentence with “few” for “most”). If we modelled our attempt on the method used to formalize similar sentences starting with “all” we would write:

*`6)`* Tx(Fx → Gx)

with “F” corresponding to “is a man” and “G” to “leads a life of quiet desperation”. However, this formalizes not (5) but rather:

7) Most things are such that: if they are men then they lead lives of quiet desperation.

(7) is true if most things are not men, for it is true iff most things in the universe have this property: that if they are men then they lead lives of quiet desperation. One way in which this could be true, at least as formalized by (*`6)`*, is for most things not to be men. Then most things vacuously have the property in question. But this is not a condition upon which (5) is true. Hence (*`6)`* is not an adequate formalization of (5).

Perhaps only the details of the strategy were wrong, and “→” simply the wrong connective to use. But we also cannot use “&amp;”, as we do when formalizing similar existentially quantified sentences. For, with correspondences as before,

8) Tx(Fx &amp; Gx)

is true only upon an interpretation which assigns most things to the intersection of what it assigns to “F” and “G”. In other words, for-

malizing (5) by (8) misrepresents the former as requiring for its truth that most things in the universe are both men, and also leaders of quietly desperate lives. No truth functional sentence connective can be inserted in the place marked $\phi$ in

9) $Tx(Fx \phi Gx)$

in such a way as to yield an adequate formalization of (5).

Ex. 4.39 To show that no truth fractional connective can replace “$\phi$” in (10.9) so as to produce an adequate formalization of “most”, one has to proceed by an enumeration of cases. The ones considered in the text show that the falsity of the antecedent to the supposed connective must not be sufficient for the truth of the compound, and that the truth of both antecedent and consequent must not be sufficient for the truth of the compound. Establish the result for the remaining cases.

This is one motivation for a somewhat different conception of quantification, which I shall now introduce. Let us say that an open sentence is what results from a $\mathbf{Q}+$ or $\mathbf{Q}$-sentence by replacing a name-letter by a variable not already contained in the sentence. (In this terminology, an open sentence is a kind of non-sentence.) We can characterize the quantifiers of $\mathbf{Q}$ as unary quantifiers because they take just one open sentence to make a sentence. This is why the formalization of sentences like “Everything is physical” was so straightforward, whereas the formalization of sentences like “All men are happy” was not. This last sentence contains two predicative expressions, “man” and “happy”, welded into a sentence by the quantifier and the copula “are”. To $\mathbf{Q}$-formalize it we have to find a single open sentence for the quantifier to attach to. What seems approximately to do the trick is “$Fx \rightarrow Gx$”. The problem with formalizing sentences like (5) was precisely that, with the available resources, we could not find a suitable single open sentence for the “T” quantifier to apply to.
A natural response is to introduce a quantifier which takes two open sentences to make a sentence: a binary quantifier. Let us add binary quantifiers “$\mu$” (for “most”) and “$\varphi$” (for “few”) to $\mathbf{Q}$, to create the language $\mathbf{QB}$, by the stipulation that every $\mathbf{Q}$-sentence is to be a $\mathbf{QB}$-sentence, and if $X^{\star}$ and $Y^{\star}$ result from $\mathbf{QB}$-sentences $X$ and $Y$, by replacing in both some occurrence(s) of a name-letter by a vari-

able, $v$, which occurs in neither, then the following are also $\mathbf{QB}$-sentences:

$$
\mu v (X^{\star} : Y^{\star}), \varphi v (X^{\star} : Y^{\star}).
$$

These are to be read: "most (few) $X$s are $Y$s". The mark ":" functions merely as punctuation.

Applying this to (5) yields:

*`10)`* $\mu x(Fx:Gx)$

with correspondences as for (6). On the appropriate interpretation, this will say that most things which are men lead lives of quiet desperation.

A rule of interpretation for “$\mu$” could be phrased on the following lines (after *`(2.2vi)`*):

11) $\mu \nu(X:Y)$ is true upon an interpretation iff most $n$-variants upon which $X_{\bar{\nu}}^{\sigma}$ is true are interpretations upon which $Y_{\bar{\nu}}^{\sigma}$ is also true.

The English "most" used in the statement of the rule is naturally seen as a binary quantifier.

Ex. 4.40 (a) Would it make any difference to replace "most" in (17.11) by "more than half"?

(b) Give an account of "Most natural numbers are non-prime" upon which it is false.

(c) Give an account of "Most natural numbers are non-prime" upon which it is true. Would the account also give the right result when applied to finite cases? (For the claim that "most" and "few" are not formalizable in first order logic, see Van Benthem and Doets [1983], p. 277.)

It is hard to resist the thought that "every" and "most" belong to the same linguistic category, and so should be treated in the same way. Any sentence containing "most" is still grammatical if that quantifier is replaced by "every"; and conversely. So it is natural to conclude that if "most" is a binary quantifier, so is "every". Since we have the antecedent of this conditional, its conclusion comes naturally.


It is straightforward to add a binary universal quantifier to $\mathbf{QB}$, say "$\lambda$". With the obvious correspondences, we could formalize "all men are happy" as

*`12)`* $\lambda x(Fx:Gx)$

which looks somewhat more like the English. On the formalization by a unary universal quantifier, an "$\rightarrow$" appeared which was invisible in the English, and there is no such distortion in (12).

Sentences like "everything is physical" appeared well adapted to the unary treatment. A closer look suggests that a binary treatment is closer to English even in this case. We cannot say "every is physical". "Thing" appears to function precisely as a first term to the quantifier, so that the appropriate formalization is still (*`12)`*, but now with "$F$" corresponding to "is a thing" and "$G$" to "is physical". An intended interpretation will assign every thing in its domain to "$F$".

We saw earlier that there is room for doubt concerning whether English universal quantifications imply the existence of something corresponding to the first term (of John’s children, for example, in (3.4) "All John’s children are asleep"). The treatment of quantifiers as binary is neutral on this issue. The obvious rule of interpretation for "$\lambda$" is

13) $\lambda v(X:Y)$ is true on an interpretation iff all $n$-variants upon which $X_{\bar{v}}^{\sigma}$ is true are interpretations upon which $Y_{\bar{v}}^{\sigma}$ is also true.

The question of whether "$\lambda x(Fx:Gx)$" is true on an interpretation, $i$, which assigns the empty set to "$F$" becomes the question of whether it is true that "all $\alpha$-variants upon which '$F\alpha$' is true are interpretations upon which '$G\alpha$' is also true", given that there are no $n$-variants upon which "$F\alpha$" is true. Presumably, those who are most struck by the suggestion that "All John’s children are asleep" is not true if John has no children will answer the last question negatively; whereas those who are impressed by the truth of (3.5) (All bodies acted on by no forces continue in a uniform state of rest or motion) will incline to answer it positively, laying themselves open to the charge that perhaps in that case they ought also to assign truth to (3.6) (All bodies acted on by

no forces undergo random changes of velocity). Binary quantification as such does not speak to the debate.

Ex. 4.41 (a) Define a binary quantifier (by giving the syntax and an appropriate rule of interpretation) suitable for formalizing "the". Illustrate by examples of formalizations. Do the truth conditions your formalizations attribute differ from those attributed by Russell's Theory of Descriptions?

(b) Define a binary quantifier (by giving syntax and an appropriate rule of interpretation) suitable for formalizing the quantifier "no". Formalize the following pair, using binary quantifiers in both cases:

(i) Every student will pass if he works.

(ii) No student will pass if he works.

Compare this treatment of (i) and (ii) with that awarded by unary quantifiers (i.e. their Q-formalizations). (For discussion, see Higginbotham [1986].)

There is another approach to quantifiers which is motivated by similar considerations and yields an essentially similar language. On this approach, a quantifier attaches to a predicate to form a "restricted quantifier", like "all men", which is then fit to attach to a second predicate, say "mortal", to form a sentence ("all men are mortal").

Either of these approaches offers an insightful way of specifying the contribution which quantifiers make to truth conditions. "All $F_s$ are $G_s$" is true iff the set of $F_s$ is a subset of the set of $G_s$; "Most $F_s$ are $G_s$" is true iff the cardinality of the set of $F_s$ which are $G_s$ exceeds the cardinality of the set of $F_s$ which are not $G_s$; "The $F$ is $G$" is true iff the cardinality of the set of $F_s$ is 1 and the set is a subset of the set of $G_s$. (The cardinality of a set is the number which says how many members it has.) Using $|\sigma|$ to express the cardinality of a set $\sigma$, and with $i$ ranging over interpretations, the truth conditions of various binary quantifications can be listed:

*`14)`* $\lambda x(Fx:Gx)$ is true upon $i$ iff $i(F) \subseteq i(G)$

some $x(Fx:Gx)$ is true upon $i$ iff $|i(F) \cap i(G)| > 0$

$$\mu x(Fx:Gx) \text{ is true upon } i \text{ iff } |i(F) \cap i(G)| > |i(F) - i(G)|$$

$$\varphi x(Fx:Gx) \text{ is true upon } i \text{ iff } |i(F) - i(G)| > |i(F) \cap i(G)|$$

the $x(Fx:Gx)$ is true upon $i$ iff $|i(F)| = 1 \land i(F) \subseteq i(G)$.

For example, the last line says that a sentence of the form “the $x(Fx:Gx)$” is true upon $i$ iff the cardinality of the set $i$ assigns to $F$ is 1, and everything which belongs to what $i$ assigns to $F$ belongs to what $i$ assigns to $G$. This is the familiar Russellian truth condition in new notation.

## 18 Substitutional quantifiers

The Q-quantifiers are called “objectual��: whether or not a quantification is true upon an interpretation depends on how things are with the objects in the domain of interpretation. For example, the rule for “$\exists$” entails that “$\exists xFx$” is true on an interpretation, $i$, iff some object in the domain of $i$ is a member of what $i$ assigns to “$F$”.

An alternative style of quantifier is called “substitutional”. The rule for such a quantifier makes whether a quantification is true upon an interpretation depend on whether sentences resulting from the quantification by deleting the quantifier and substituting a name for the variable of quantification are true. For an existential substitutional quantifier, written “E”, the rule might be:

1) $\mathsf{E}\nu X^{\star}$ is true upon an interpretation, $i$, iff for some name, $N$, $X\frac{N}{\nu}$ is true upon $i$.

Analogously, for a universal substitutional quantifier, written “A”, the rule might be:

2) $\mathsf{A}\nu X^{\star}$ is true upon an interpretation, $i$, iff for all names, $N$, $X\frac{N}{\nu}$ is true upon $i$.

Here, $X^{\star}$ results from a sentence by replacing a name-letter by some variable, $\nu$, not already in the sentence, and $X\frac{N}{\nu}$ results from $X^{\star}$ by replacing each occurrence of $\nu$ by some name, $N$. We do not require that $N$ be absent from $X^{\star}$.

**Ex. 4.42** Show how requiring the absence of “$N$” from $X\frac{N}{\nu}$ would lead to unwanted truth-upon-an-interpretation conditions for sentences like “$\exists x \exists y Fxy$”.

Q, as defined so far, contains no names, but only name-letters. Names should be related to name-letters as predicates to predicate-letters. Whereas a predicate is assigned the same set on every interpretation (modulo differences of domain), a predicate-letter is assigned different sets upon different interpretations. Likewise, a name, as opposed to a name-letter, will be assigned the same object in every interpretation. Let us call a language “QS” if it adds to Q the two substitutional quantifiers recently mentioned, and also adds names, specifying, for each name, the object which any interpretation must assign to it.

QS is still underspecified, since we have not said what names it contains. Let us suppose, first, that it contains just the name “Reagan”, and we stipulate that in every interpretation this is to be assigned Ronald Reagan, the famous American political film star. In conjunction with (1) and (2), this would ensure that “AxFx” and “ExFx” would alike be true upon an interpretation, *i*, iff Ronald Reagan is the member of what *i* assigns to “F”. This is not incoherent, but has no discernible utility.

Could we specify QS in such a way that a substitutional quantification in QS is true upon an interpretation iff the corresponding objectual quantification in Q is true upon the corresponding interpretation? A necessary condition is that QS contain a name for every object in the domain of interpretation. If it did not, it would be “easier” for “AxFx” than for “∀xFx” to be true upon an interpretation. A further necessary condition is that QS should not contain a name for some object not in the domain of interpretation.

The two necessary conditions are jointly sufficient for coincidence of objectual quantifiers of Q and the substitutional quantifiers of QS. If we held to these conditions, there would be no interest in substitutional quantification. There are two ways of modifying QS which would make substitutional quantification of interest. One is to allow QS to contain empty names; the other is to allow it to contain opaque contexts. I will discuss only the latter. (§20 below contains some material on empty names.)

An opaque context with respect to names is one in which there is no guarantee that two co-referring names can be substituted *salva veritate*; that is, it is a context in which the substitutivity of identicals – (8.5) – fails; that is, the context “... ...” is opaque with respect to names iff there is no guarantee that “... N₁ ...” and “... N₂ ...” have the

same truth value, despite the fact that “N₁” and “N₂” have the same bearer. The context

3) John believes that . . . is a student of Christ Church is opaque with respect to names, since it may be that the first but not the second of the following is true

4) John believes that Charles Dodgson is a student of Christ Church

5) John believes that Lewis Carroll is a student of Christ Church even though Dodgson is Carroll.

We cannot regard (3) as a predicate, for reasons already noted in §15 (see (15.16)). Let us instead call it a “quasi-predicate”. To formalize sentences like (4) and (5) we need what I shall call “quasi-predicate-letters”. These letters cannot be interpreted by being assigned a set of objects. We will not consider how they are to be interpreted, but let us assume that somehow or other they can be, so that there are QS-formalizations of (4) and (5) which, upon an intended interpretation, are true and false respectively. Then by the interpretation rules for the substitutional quantifiers, both of the following are true upon an intended interpretation (where “ψ” corresponds to the quasi-predicate (3)):

6) Exψx

7) Ex¬ψx.

These quantifiers are not objectual: the truth of (6) and (7) on an intended interpretation does not turn on how things are with some object, for the same object is involved in the verification of both, yet no one object can be both ψ and not-ψ.

Substitutional quantification is intelligible in contexts in which objectual quantification would not be. Consider the quasi-predicate “was so-called because of his size”. The objectual quantification

8) ∃x(x was so-called because of his size)

is nonsense. What does the “so” refer back to? On the other hand, if a formalization has a quasi-predicate-letter, say ψ, corresponding to the quasi-predicate, and, moreover, the formalization of

*`9)`* Giorgione was so-called because of his size

is true upon the interpretation, and if, finally, “Giorgione” (or its formal equivalent) is included in the substitution class of names with respect to which the quantifier is defined, then the substitutional quantification

10) $\exists x \wp x$

is also true upon the interpretation.

Substitutional quantifiers are perfectly intelligible. It is unclear whether any English quantifiers are substitutional. The best candidates are substitutional quantifiers whose variables occupy *predicate position* (see §19). If there are substitutional quantifiers in English whose variables occupy name position, then what (*`10)`* formalizes would be expressible in English, and true. But anything like

11) Something was so-called because of his size

would seem to have all the unintelligibility of (*`8)`*.

**c. 4.43** “Snow is white” is true iff snow is white.

This appears to hold not just for the sentence “snow is white”, but quite generally. Attempt to formalize an appropriate generalization both in Q and in QS, and comment on the success of your efforts.

## 19 Predicate quantifiers and second order logic

Second order logic involves quantification over properties or sets. Such quantification can also be effected in the first order logic of Q. Hence we need to add some further specification if we are to say what second order logic is. I will begin by dwelling upon the way in which Q can be used to formalize English sentences apparently involving quantification over properties.

We seem to be able to generalize from a sentence like

1) Reagan and Thatcher are both powerful

in two kinds of way. One way is familiar:

2) Someone, $x$, and someone, $y$, are such that $x$ is powerful and $y$ is powerful

which is easily formalized in $\mathbf{Q}$. The other way is:

*`3)`* There is something which both Reagan and Thatcher are.

The "something" is a property, and the generality in (3) is inferred from the fact that *powerful* is something both Reagan and Thatcher are, a fact expressed (in a slightly different way) by (1). Pressed to Q-formalize, we might offer

*`4)`* $\exists x(H\alpha x \land H\beta x)$

with “$\alpha$” and “$\beta$” corresponding (on an intended interpretation) to the two leaders and “$H$” to the relation of *having*, the relation that holds between an object and a property when the object *has* the property. Nothing in $\mathbf{Q}$ restricts the domains of interpretation, so there is no reason not to include properties, on the assumption that there are such things. (Sometimes the word “individuals” is used in a technical sense, to mean all the entities in the interpretation domains of some first order language like $\mathbf{Q}$. Then one must say, with only superficial awkwardness, that properties may be among the individuals.) So there is no special problem about “quantifying over properties” in $\mathbf{Q}$. (If there are no properties, as nominalists maintain, then no matter what one’s linguistic or logical resources one will not be able to quantify over them.)

Adopting this approach threatens to obscure some logical relations. (3) is supposed to follow from (1), but (4) will not be the conclusion of a Q-valid argument with a straightforward formalization of (1) as premise. So one might offer a non-straightforward formalization of (1) as:

5) $H\alpha\pi \land H\beta\pi$

with “$H$”, “$\alpha$” and “$\beta$” as before and “$\pi$” corresponding to the property of being powerful, regarded as an object fit to belong to a domain of $\mathbf{Q}$-interpretation. (*`4)`* and (5) represent the argument whose premise is (1) and whose conclusion is (3) as $\mathbf{Q}$-valid. The formalization of (1)

as (5) may seem unnatural, but it has a point, though it would be misguided to attempt to formalize every predicate by a name.

#### Ex. 4.44 Why would it be misguided to attempt to formalize every predicate by a name?

The $\mathbf{Q}$-quantifiers are “name quantifiers”: their variables occupy the kind of position that names can occupy. We could extend $\mathbf{Q}$ by adding predicate quantifiers, quantifiers whose variables occupy the kind of position that predicates can occupy. Using “$\nabla$” for the universal quantifier and “$\Delta$” for the existential, the syntactic rule could be:

6) If $X$ is a $\mathbf{Q}$-sentence then so are $\nabla f X^*$ and $\Delta f X^*$, where $X^*$ results from $X$ by replacing one or more occurrences of a predicate or predicate-letter in $X$ by $f$.

Instead of (4), we could formalize (2) as

*`7)`* $\Delta f(f\alpha \land f\beta)$.

The proposal can be intended in more than one way.

(a) It merely provides notational abbreviations for the kinds of $\mathbf{Q}$-formulae we have already, in particular the kind used in (4) and (5). No new semantic ideas are invoked: “$\nabla$” and “$\Delta$” are used in essentials like “$\forall$” and “$\exists$”, except for the suggestion that an intended interpretation will see an expression of the form “$fx$” as abbreviating something like “$Hfx$” and will assign to “$H$” a set of ordered pairs whose first member is a property and whose second member is a possessor of that property. This conservative way will not treat as logical truths some expressions which arguably are logical truths, for example

8) Everything has some property,

which emerges as

*`9)`* $\forall x \exists f (fx)$.

If this is as an abbreviation of “$\forall x \exists y(Hxy)$” (containing special guidance about intended interpretations) it is not Q-valid.

(b) We can restrict the interpretation of the new quantifiers in specific ways. Given the examples considered so far, the natural restriction would be to properties. The effect of this stipulation would be unclear in two ways. First, it is unclear what the general (“logical”?) truths about properties are. For example, must every property have an instance? Second, it is unclear why this would achieve anything significantly different from what is achieved by (a). It would seem that we could have simply included properties in the domain anyway, in which case the truth of sentences containing the existing quantifiers would have been sensitive to how things are with properties.

These unclarities are resolved by an alternative proposal, which gives the core of the standard form of second order logic: the new quantifiers are to range over subsets of the domain of interpretation. This allows set theory to supply definite answers to some questions. For example, not every subset of the domain must have a member, but everything in the domain is a member of some subset of the domain, thus showing that (9) is valid on these semantics. Moreover, the proposal gives a clear answer to why the new entities could not have been simply members of the domain. The Russian-born mathematician Cantor proved that the subsets of a set are more numerous than the set; so the cardinality of the set of entities the predicate quantifiers are sensitive to is greater than the cardinality of the set of entities the name quantifiers are sensitive to. The effect of this proposal could not be achieved in the style of (a).

On this approach, second order logic stands in some intimate relation to set theory, for set-theoretical truths are instrumental in determining which sentences are valid (as we just saw with (9)). This is not to say that second order logic is set theory. For example, “There is a set which contains everything as a member” is not true on standard set theories (to suppose it to be true would quickly lead to paradox), whereas

*`10)`* $\exists f \forall x(fx)$

is valid in the proposed second order logic. This disparity is explained by the fact that (10) does not say that there is a set which contains everything as a member in some absolute way. Rather, it is valid because for every interpretation, there is a set, namely the domain itself, to which everything in the domain belongs.

(c) Second order logic, as developed along the lines of (b), does not treat the relation between predicate variables and predicates on a par with that between name variables and names. We can replace a name variable by an expression fit to refer to some entity to which name quantifiers are sensitive, that is, some entity in the domain of interpretation, and the result is an intelligible sentence; but we cannot replace a predicate variable by an expression fit to refer to some entity to which predicate quantifiers are sensitive, that is, some subset of the domain of interpretation, with the guarantee that what results will be an intelligible sentence. We can lop off the “∃x” in “∃x x = x” and replace the variable by a name and end up with the fully intelligible “Reagan = Reagan”. But if we perform a similar operation upon, for example, (7) (Δf(fα &amp; fβ)) the result is not strictly intelligible: (the set of men)α &amp; (the set of men)β. What is missing is the use of the predicate to ascribe something to something, to say something about something. This is what makes the juxtaposition of a name and a predicate more than a mere list, and is the feature of predication which Frege [1892a] referred to as “unsaturatedness”. Not suggesting a philosophical account of this matter is of no significance whatever for the purposes for which second order logic was introduced: a juxtaposition like “(the set of men)α” can be regarded as an abbreviation of “α belongs to the set of men”. But it is of some significance in connection with the attempt to understand what appear to be predicate quantifiers in English, as in (3) (There is something which both Reagan and Thatcher are). This differs both from “There is something to which both Reagan and Thatcher belong – viz., a set” and from “There is something which both Reagan and Thatcher have – viz., a property”. We can naturally add a videlicet clause to (3) as follows:

11) There is something which both Reagan and Thatcher are – viz., powerful.

“Powerful” is an adjective, and not a noun or noun phrase (like “power” or “being powerful”) fit to refer to a property. (Compare “There is something which both Reagan and Thatcher are – viz., happy”. “Happy” does not, or does not just, refer to happiness: “happiness” is the closest word which does that, but we cannot intelligibly conclude the sentence just quoted with “– viz., happiness”.

Quantification is naturally thought of as quantification over entities: over individuals, or properties or sets. Yet no entity seems to capture the predicative character of predicates. Genuine predicate quantification would be quantification into genuinely predicate position, that is, position in which predicative character is retained. Hence there is a tension in the very notion of predicate quantification: there is pressure to think of it as over entities, and pressure to think of it as involving more than entities. In standard second order logic, quantification is over entities, and there is no attempt or need to explain “unsaturatedness”.

A type of quantification more apt to retain the predicative character of predicates would be substitutional quantification into predicate position. “∇f(…f…)” would be true iff the result of replacing the variable in “(…f…)” by a predicate (from some specified class of predicates) is true. This would give a natural understanding of the *videlicet* clause in (11): it supplies a predicate which verifies the quantification. Though this may shed some light on some English idioms, I do not know that it has any significance for logic.

## 20 Free logics

A “free logic” is one which rejects the following assumption:

1) Every name (or name-letter) refers to something.

A “universally free logic” is one which rejects the following assumption:

2) Only non-empty domains feature in the definition of validity.

The assumptions are independent: either can be rejected without the other. $\mathbf{Q}$ is committed to both assumptions, as the following facts make plain:

3) $\models_{\mathbf{Q}} \exists x\ x = \alpha.$

4) $\models_{\mathbf{Q}} \exists x(Fx \lor \neg Fx).$

In this section, I shall mostly consider various ways in which (1) can be rejected, and some philosophical motivations. I close the section with some brief remarks about (2).

### Motivations for rejecting (1):

(a) Our language seems to contain names with no bearers, like "Vulcan", and an adequate logic should be able to deal with them; so $\mathbf{Q}$ falls short of its aspiration to formalize English sentences.

(b) Logic is apriori, and so are logical relations like validity. We cannot tell apriori whether any of our names have bearers. In the case of many names, like "London", we are confident that they do have bearers, but the confidence is based on non-apriori empirical knowledge; in other cases, like "Vulcan", we are confident that they do not have bearers, but this emerged from an astronomical discovery (there was observed to be no planet between Mercury and the sun), not from apriori reflection; in yet other cases, the issue is in dispute (perhaps experts still differ on the question whether there was really any such person as Homer). If an English argument guaranteed the truth of its conclusion only on the assumption that the names occurring in it had bearers, we could not tell apriori whether, if the premises were true, so would the conclusion be. To formalize these names with name-letters would wrongly suggest that we can tell apriori that they have bearers, for name-letters are by stipulation assigned objects (bearers).

(c) Some Q-valid arguments formalize invalid English arguments, if there actually are empty names; since there are, Q is incorrect. For example, the English argument

*`5)`* Everything is just as heavy as itself; so Vulcan is just as heavy as Vulcan

has a premise which is true but a conclusion which is not, yet if we use Q-validity as our guide to validity we might be tempted to classify (*`5)`* as valid (since $\forall x Rx \models_{\mathbf{Q}} R\alpha\alpha$).

Ex. 4.45 Can there be an "intended interpretation" of $R\alpha\alpha$, regarded as a formalization of "Vulcan is just as heavy as Vulcan"? Use your answer to evaluate the claim that the practice of Q-formalizing would lead us to classify as valid arguments with premises which are true and conclusions which are not.

(d) Some Q-valid arguments formalize invalid English arguments, if some actual entities might not have existed. For in that case

*`6)`* Everything is perishable; so Socrates is perishable,

though supposedly an example of $\forall xFx \models_{\mathbf{Q}} F\alpha$, is not valid: since Socrates might not have existed, it might have been that the premise is true and the conclusion is not (Socrates could not be perishable without existing). This point does not depend on the supposition that there are any empty names.

**Ex. 4.46** Show how a formalization of (20.6) using binary quantifiers would undermine this argument for free logic.

Those who find one or more of these arguments convincing will reject (1). There is general agreement that doing this requires changes in the quantifier rules. Using “$\forall x(\ldots x\ldots)$” to represent an arbitrary universal quantification, Q says:

7) $\forall x(\ldots x\ldots) \models_{\mathbf{Q}} (\ldots \alpha \ldots)$.

Using “QF” for free logic, the closest correct QF claim is

8) $\forall x(\ldots x\ldots), \exists x\ x = \alpha \models_{\mathbf{QF}} (\ldots \alpha \ldots)$.

The logical rule of “universal quantifier elimination” or “specification” must be restricted so that only a name with a bearer can replace the quantified variable. QF requires a similar modification to the existential quantifier.

**Ex. 4.47** Using an example, explain why the argument in (20.7) ought not to be QF-valid.

These generally agreed changes in quantifier rules do not resolve what to go on to say about sentences with empty names.

*Negative free logic*: All atoms containing a bearerless name are false. So “Vulcan is a planet” is false; since the negation of a falsehood is a truth, “It is not the case that Vulcan is a planet” is true (Burge [1974]; Bostock [1997], pp. 356 ff.).

Positive free logic: Some atoms containing a bearerless name are true. A likely example would be “Vulcan is Vulcan” given that this “follows from the unexceptionable identity principle $x = x$” (Lambert [1991b], p. 25). Sensible versions of this view will draw back from holding that all are true; not, for example, “Vulcan is a noted logician”.

Fregean free logic: all sentences containing a bearerless name lack truth value. This seems to have been Frege’s view. If $S$ is neither true nor false, “not-$S$” (assuming “not” to introduce the standard kind of negation) is also neither true nor false: not true, for that would require $S$ to be false, and not false, for that would require $S$ to be true. In general, the idea is that however complex the sentence in which the bearerless name occurs, it will lack a truth value. (Frege [1892b]; Lehman [1994].)

I will review some motivations for these various options.

### (1) Predication

One of the most basic acts in thought or speech would appear to be that of predicating something of something, for example, predicating being happy of John. The result is true iff there is something of which something is predicated, and that object is as it is said to be. Hence a predication which fails to be of anything cannot be true.

If this is accepted, as I think it should be, positive free logic is excluded, but the point is consistent with both Fregean and negative free logic. The argument can be developed into one for the Fregean view if we add that to predicate falsely is to say of something that it is other than it is: no object, no falsehood.

### (2) Fiction

We discriminate among fictional sentences, holding, for example, that

*`9)`* Holmes was a detective

is true whereas

*`10)`* Holmes was a farmer

is false. Since there was no such person as Holmes, we must treat “Holmes” as an empty (bearerless) name. This supposedly shows that free logic should be positive.

The argument has more than one weakness. First, it is not uncontroversial that “Holmes” is an empty name, for arguably it is a name of a fictional character. One ought to be specially inclined to this view if one accepts without qualification that (9) and (10) are literally true and false respectively.

Secondly, it is unclear that one ought to accept this. To check that (10) is true we go to the works of Conan Doyle, and it is enough that this sentence follows from what Doyle wrote. This strongly suggests that either (9) is elliptical for something like

11) According to the stories, Holmes was a detective

or else that in believing that (*`9)`* is true we are really believing that it is true-in-the-stories.�� If the former, then (*`9)`* and (10) are not strictly speaking fictional sentences after all; if the latter, (*`9)`* is not strictly true.

Perhaps the examples can still serve the cause of positive free logic; for even after reinterpretation, we have cases of both true and false sentences containing a name which is arguably empty. This suggestion needs to be set within a positive account of the kinds of context generated by the envisaged kind of operator (“according to the stories”). Suppose, for example, that “according to the stories (p)” meant something like “among the sentences making up the stories, there occurs ‘p’”. Then “Holmes” would not really be being used in a sentence like (9), understood as elliptical for (11): it would merely be being mentioned, and so there is no inference to the conclusion that an empty name can be used in a true sentence.

In any case, this conclusion would tell at most only against Fregean free logic. It could be accepted by both negative and positive versions. The negative free logician says only that all atoms containing an empty name are false, and (11) is clearly not atomic.

### (3) Logic

If we have limitless respect for “laws of logic” like “p ∨ ¬p” or “α = α”, we may incline to suppose that they hold quite unrestrictedly; hence that we must have truths like


*`12)`* Vulcan is a planet or Vulcan is not a planet

*`13)`* Vulcan = Vulcan.

On second thoughts, logic does not hold for quite all sentences, for we exclude questions, commands, nonsense, etc. Frege [1892b] seems to have believed that fiction was a species of nonsense: there are no genuine thoughts in fiction, but only mock thoughts; we do not really make assertions, true or false, but merely play at making them. He would presumably have assimilated sentences like (12) and (13) to unwitting examples of this sort of nonsense.

The view is especially implausible when extended in the way just envisaged beyond the sphere of fiction. Whereas fiction is an activity engaged in wittingly, the possibility of unwitting fiction makes which sentences are "nonsense" and which are not a matter not available apriori, so it would be inconsistent with the supposed apriori status of logic.

One could imagine (12) having been used in some kind of reductio proof of Vulcan's non-existence. Something similar is used in a classical proof that there is no greatest prime ("either the greatest prime is odd, or it is even"). So there are non-negligible reasons to reject the Fregean version of free logic.

Negative and positive free logicians agree that (12) is true: they are separated by (13). Both agree that it does not follow from "$\forall x x = x$" (cf. (8)). The positive free logician may well adopt a semantics which allows for the truth of (13) by positing an additional "null" entity, lying outside the domain, and which serves as the referent of the empty names; more exactly, being assigned the null entity is a reflection of the fact that the name is empty (cf. Scott [1967]). Though this method may not be essential to positive free logic, it has the unfortunate consequence (from the present point of view) of also validating:

14) Vulcan = Holmes.

The negative free logician may offer the following points in favour of not treating (*`13)`* as true: (i) to do so would be inconsistent with our intuitions about predication (a true predication must be a predication of some object); (ii) to do so is unnecessary, since all we need from the logic of identity can be obtained without allowing

that there are true instances of "$\alpha = \alpha$" with "$\alpha$" empty (cf. Burge [1974]).

### (4) Denial and scope

The topic is horses. There are mares and foals, Arabs and Palaminos, greys and chestnuts. You say: “And winged and wingless. After all, Pegasus was a winged horse.” I disagree, and so wish to deny what you said. I say

### 15) No: Pegasus was not a winged horse.

This sounds unnatural. This is consonant with Fregean free logic, which sees (15) as neither true nor false, and so as incapable of expressing a truth fit to disabuse someone who has been deceived by a myth. The unnaturalness of (15) raises a prima facie problem for negative free logic, according to which “Pegasus is a winged horse” should be false and so its negation should be straightforwardly true. Yet (15) does not strike many people as a straightforward truth.

For the negative free logician, a sentence containing a name and a sign for negation raises the possibility of significant scope distinctions. (15) is true only if the “not” has wide scope. If it had narrow scope, (15) would be attempting to make a negative predication of Pegasus, to ascribe to him the property of being not a winged horse. This cannot be true, on the negative free logical view, for a true predication needs an object to be a predication of. Perhaps, then, the problem with (15) is that it doesn’t clearly deliver the wide-scope reading: it is not clearly a denial of “Pegasus was a winged horse”. Yet however much we try to make the wide-scope reading salient (for example, by saying “It is not the case that Pegasus was a winged horse”), we do not get a sentence which seems straightforwardly true. The negative free logician requires an explanation of this.

I think the explanation is that special conventions govern the ways in which we should disabuse those we take to have been seduced by myth or fiction. We should say something like: “Pegasus is just a mythical creature”. That’s why sentences like (15), which are indeed true according to negative free logic, don’t sound natural or appropriate.

More distinctive data favouring negative free logic come from cases in which fact and fiction are mixed. Utterances of the following (in obvious kinds of factual context) seem unequivocally true:

That man's not Odysseus.

That foal wasn't sired by Pegasus.

There may be more than one way to systematize such data, but Fregean free logic is not a serious starter, and negative free logic handles everything fine, including scope distinctions. Using square brackets in an obvious way to indicate scope, candidate formalizations include:

**`[a]`** [b] ¬ Rab

[a] ¬ [b] Rab

¬ [a] [b] Rab.

resumably the second is the most plausible; and this explains the less tisfactory status of

Odysseus isn't that man.

Pegasus didn't sire that foal.

These sound unnatural, at the very least. If they contain occurrences of empty names with wide scopes relative to the negation sign (as marked by the formalization [a] [b] ¬ Rab), they are false according to negative free logic, and this would explain our disinclination to assert them.

Logic has various purposes, like developing a foundation for mathematics, or providing resources for computer science. To the extent that logic aims to reflect ordinary reasoning, and the ordinary language in which we reason, some form of free logic seems to me preferable; and of the versions discussed, negative free logic seems closest to ordinary language.

Universally free logic rejects (2); that is, its definition of validity makes room for the empty domain. The primary motivation is that the interpretations involved in the definition of validity are supposed to represent all the logical possibilities, but it does not appear to be logically impossible that there should be nothing. Hence one does not do justice to genuine validity if one defines it in terms of

"all" interpretations, yet excludes interpretations whose domain is empty.

The allegedly unsatisfactory view would show up in connection with such truths as:

16) $\forall xFx \models_{Q} \exists xFx.$

With respect to an empty domain, one expects the premise to be true, given the equivalence between $\forall$ and $\neg \exists \neg$: there is no counterexample to the universal quantification. Yet, intuitively, the conclusion should be false with respect to the empty domain, for there is nothing in it which is any way at all, let alone something which is $F$.

As things stand, there are, by explicit stipulation, no Q-interpretations whose domain is empty, so it would be nonsense to say that (16) was falsified by the empty domain. However, let us adjust the definitions in Q in the direction of the present line of thought. Once we remove the stipulation that an interpretation requires a non-empty domain we must adjust the rules of interpretation. For example, (2.1) requires that any interpretation assign to each name-letter an object in its domain. This is impossible if the domain is empty. One global and systematic option is to rephrase to something like: "any interpretation assigns to each letter either nothing or else an object from its domain". This means that we no longer think of interpretations as (complete) functions (in the mathematical sense): it may be that nothing is identical to $i(\alpha)$.

On a natural reading of the Q-clause for the truth-upon-an-interpretation of atoms, it will produce unwanted results (2.2v):

an atom is true upon an interpretation whose domain is $D$ iff the sequence of the object(s) from $D$ assigned to the name-letter(s) by the interpretation belongs to the set it assigns to the predicate-predicate-letter; it is false iff the sequence does not belong set.

An interpretation over the empty domain will not assign anything a name-letter; in this case, a natural way to read "the sequence of the object(s) assigned to the name-letter(s) by the interpretation" is a denoting the null sequence, the sequence with no members. Since this belongs to every set of sequences, the upshot would be that any atom would be true upon any interpretation over the empty domain. No theorist would want this, and it is the antithesis of the result desired by a negative free logician.


We could revise *`(2.2v)`* as follows:

17) an atom is true upon an interpretation over $D$ iff it assigns an object from $D$ to each name-letter in the atom, and the sequence of the object(s) assigned to the name-letter(s) belongs to the set the interpretation assigns to the predicate or predicate-letter; otherwise it is false.

This makes the conclusion of (16) false upon an interpretation over the empty domain. However, given the existing Q-rule for “$\forall$”, it also has the unwanted result of making the premise false: its truth would require the truth of some atom, say “$F\alpha$” upon all $\alpha$-variants, but these interpretations must also be over the empty domain, so they will not assign anything to $\alpha$, so they will none of them meet the first part of the truth-upon-an-interpretation condition of (16). This result is unwanted, for intuitively we wanted there to be a counterexample to the validity of an argument from $\forall$ to $\exists$, and this means an interpretation (over some domain) which makes the $\forall$-sentence true and the sentence false, and this we have not yet found.

We can work our way towards appropriate adjustments of $\mathbf{Q}$ by selecting on the intuitive reason for thinking of an $\forall$-sentence, for example $\forall xFx$, as true with respect to the empty domain: there is no counterexample. This means that there is no object (in the domain) to falsify $\forall xFx$ by verifying $\neg F\alpha$. This suggests the following modification of the quantifier rule (2.2vi):

18) $\forall vX$ is true upon an interpretation, $i$, whose domain is $D$ iff there is no object $z$ in $D$ and no $n$-variant $i'$ of $i$ such that $i'(n) = z$ and $i'(X_{\bar{v}}^n) = F$.

(Cf. Bostock [1997], p. 368.) On this rule, being an $n$-variant is not a reflexive relation: the $n$-variants of an interpretation which assigns nothing to $n$ will not include the interpretation itself. When coupled with an analogous rule for existential quantification, (18) ensures the failure of the validity of the argument from $\forall$ to $\exists$, for it

ensures that $\forall$-sentences are true upon interpretations over empty domains.

Ex. 4.48 Provide an existential quantifier rule that is analogous to *`(20.18)`*.

Even though there are free logics which allow the empty domain without allowing for interpretations which assign nothing to some or all name-letters, the way in which the empty domain has been allowed for here does allow for interpretations which assign nothing to name-letters. It therefore provides interpretations which would count as intended interpretations of English sentences containing empty names (at least if these are known to be empty). (For an argument that if one allows the empty domain one should allow empty names, see Bostock [1997], pp. 348–51.)

One moral to be drawn from the discussion of free logics is the reminder that there are coherent alternatives to $\mathbf{Q}$. Almost every supposedly inviolable “logical law” has been challenged: dialetheic logic holds that there are true contradictions; some logics repudiate modus ponens; intuitionistic logic does not affirm double negation (the inference from “not not-$A$” to “$A$”); some logics deny the validity of the inference from not-$A$, together with $A$ or $B$, to $B$. The choice among the alternatives is not to be made on the grounds that “logic” demands, for example, the validity of “Something exists”. Rather, it has to be made upon the basis of philosophical arguments: we look to these to say what a correct logic should validate, and what it should not. Some departures from the classical logic of $\mathbf{Q}$ are larger than others, and some are better motivated than others. Free logic is a small departure and scores highly on motivating reasons.

## 21 Depth

A $\mathbf{Q}$-formalization may be adequate, yet not reveal all the logical structure of the English. Thus

1) $F\alpha$

is an adequate Q-formalization of

2) John is not happy

(with “F” corresponding to “is not happy”). The truth conditions of (2) coincide with the truth-upon-an-intended-interpretation conditions of (1). Yet (1) does not reflect the fact that (2) contains an occurrence of a logical constant. We shall say that, relative to (2), (1) is a less deep Q-formalization than

3) $\neg F\alpha$

with “$F$” corresponding to “is happy”.

Sometimes lack of depth in a formalization may prevent the validity of an argument becoming manifest. For example, the following is valid:

4) John will enjoy any book about cosmology. The First Three Seconds is about cosmology. Therefore John will enjoy The First Three Seconds.

The following meets the standard for being an adequate Q-formalization (truth-upon-an-intended-interpretation conditions match truth conditions):

5) $F\alpha\beta, G\gamma\beta; H\alpha\gamma$

with “$Fxy$” corresponding to “$x$ will enjoy any book about $y$”, “$Gxy$” to “$x$ is a book about $y$”, “$Hxy$” to “$x$ will enjoy $y$”, “$\alpha$” to “John”, “$\beta$” to “cosmology” and “$\gamma$” to “The First Three Seconds”. Yet (5) is plainly $\mathbf{Q}$-invalid.

Lack of depth may not prevent the manifestation of validity. The following is Q-valid and an adequate formalization of (4):

6) $\forall x(Kx \to H\alpha x); K\gamma; H\alpha\gamma$

with “$K$” corresponding to “is a book about cosmology” and the other correspondences as before. The following is also adequate but deeper:

7) $\forall x(Gx\beta \to H\alpha x), G\gamma\beta; H\alpha\gamma$

(correspondences as before). If $X$ and $Y$ are adequate formalizations of $A$, and $Y$ is deeper than $X$, and $X$ is Q-valid, then $Y$ is also Q-valid.

How far should depth go? One extreme idea, to be explored in chapter 6.2, is that wherever there is validity in the English, then some adequate Q-formalization is valid. Putting this idea into practice would require one, for example, to formalize the argument

8) Tom is a bachelor. Therefore Tom is not married along the lines of

9) $F\alpha \land \neg G\alpha; \neg G\alpha$

(with “$F$” corresponding to “is a man” and “$G$” to “is married”). And it would require one to formalize

10) Socrates is mortal. Therefore he is or will be dead along the lines

11) $\exists x(Fx \land G \alpha x); \exists x(Fx \land G \alpha x)$

(with “$F$” corresponding to “is a time”, “$Gxy$” to “$x$ dies at $y$” and “$\alpha$” to “Socrates”).

As in the case of P, that an adequate formalization of an argument is not Q-valid does not in itself enable us to infer anything about the validity of the argument. Perhaps a deeper Q-formalization would reveal it as valid – and valid in virtue of its Q-logical form. Or perhaps it is valid, but not in virtue of its Q-logical form (pace the proponents of the extreme idea just mooted).

Standard practice shrinks not at all from introducing in a Q-formalization logical constants that do not visibly appear in the English. Examples are the formalizations of two-term universal and existential quantifications (e.g. “All (some) men are happy”), the former seen as introducing an occurrence of “→”, the latter an occurrence of “&amp;”. Indeed, it is not unknown for practitioners to go further, and introduce predicate-letters not corresponding to predicates visible in the English. Some versions of Davidson’s theory of adverbs, for example, see a sentence like “John runs” as formalizable by a Q-sentence containing a predicate-letter which, on an intended interpretation, will be assigned the set of runs. No such predicate is visible in the English, for “runs” appears to be true of people rather than of runs.


## 22 From Q-validity to validity

If an adequate formalization of an English argument is not Q-valid, what can be inferred about the validity of the English? Answer (given in the previous section): Nothing.

Suppose, however, that an English argument is adequately formalized by a Q-valid one. The exercise would have been pointless unless we could infer that the English argument is valid – valid, as we shall say, in virtue of its Q-logical form. How can this inference be justified?

We have to show is that if a Q-argument $\phi$ is Q-valid and is an adequate formalization of an English argument $\psi$, then $\psi$ is valid.

The adequacy of the formalization ensures that, where $\phi'$ is the argument recovered from $\phi$ by applying the relevant correspondences, $\phi'$ says the same as $\psi$. The notion of “saying the same” that is required here is that the sentences of $\phi'$ should have the same truth conditions as the corresponding sentences in $\psi$. Validity can be defined in terms of truth conditions, and if two arguments are related as $\phi$ and $\phi'$ then, necessarily, both or neither are valid. So it will be enough if we can show that if $\phi$ is Q-valid then $\phi'$ is valid.

A necessary condition for there being any adequate formalizations is that the Q-operators make the same contribution to truth conditions as the corresponding English expressions. Let us suspend any doubts on this score for the moment. We will use a phrase like “corresponding name”, “corresponding predicate”, etc., to refer to a name in $\phi'$ to which, by the correspondence schema, a name-letter in $\phi$ corresponds; likewise for the other cases. The following argument establishes what is needed:

1) (i) Suppose $\phi$ is $\mathbf{Q}$-valid

(ii) Then every interpretation upon which the premises of $\phi$ are true is one upon which the conclusion is true.

(iii) Hence whatever the corresponding names in $\phi'$ refer to, whatever the corresponding predicates in $\phi'$ are true of, and whatever the truth values of the corresponding sentences, if the premises of $\phi'$ are true, so is the conclusion.

(iv) Hence, necessarily, if the premises are true so is the conclusion.

The step from (ii) to (iii) requires that every English expression in $\phi'$ corresponding to a constant in $\phi$ express the same as the Q-constant.

The step from (iii) to (iv) requires justification, for the former makes no explicit mention of logical necessity, yet the latter does. (iv) could be re-expressed as the claim that all logical possibilities which verify the premises also verify the conclusion. To reach this from (iii) we need to suppose that the various Q-interpretations, by taking into account every possible assignment to the letters, run through all the logical possibilities. This in turn requires the following (to be refined in chapter 5.1 into the conception of extensionality):

2) the truth of a sentence which is adequately Q-formalizable of necessity depends on nothing except the reference of any corresponding names it contains, what any corresponding predicates are true of, and whether any corresponding sentences are true or false.

If all logical possibilities for what the corresponding names refer to, what the corresponding predicates are true of, and what truth value the corresponding sentences have, are ones upon which the conclusion is true if the premises are, as the Q-validity of $\phi$ in effect assures us is the case, then we can legitimately infer that, necessarily, if the premises are true so is the conclusion.

$\vdash_{\mathbf{Q}}$ shares the formal properties of $\vdash$. Were this not so, its claim to give even a partial representation of $\vdash$ would be undermined.

Ex. 4.49 Using the definition of a Q-interpretation, establish the following:

(i) If $[X_1, \ldots, X_n \models_Q Z]$ then $[X_1, \ldots, X_n, Y \models_Q Z]$ whatever $Y$ may be. (Compare (1.6.5).)

(ii) If $[X_1, \ldots, X_n \models_Q Z]$ and $[Y_1, \ldots, Y_k, Z \models_Q W]$, then $[X_1, \ldots, X_n, Y_1, \ldots, Y_k \models_Q W]$. (Compare (1.6.6).)

(iii) If $Z$ is among the $X_1, \ldots, X_n$, then $[X_1, \ldots, X_n \models_Q Z]$. (Compare (1.6.7).)

(iv) If $[(X_1, \ldots, X_n) \models_Q]$ then $[X_1, \ldots, X_n \models_Q Y]$, whatever $Y$ may be. (Compare (1.6.8).)

(v) If $[\models_Q X]$ then $[Y_1, \ldots, Y_n \models_Q X]$, whatever $Y_1, \ldots, Y_n$ may be. (Compare (1.6.9).)

## Bibliographical notes

#### §§1–4

Gamut [1991] (vol. 1) treats most of the topics of this and the previous chapter from the perspective of understanding natural language. Strawson [1952], chs 5 and 6, provides useful comparisons between Q-quantifiers and English; see also McCawley [1981]. For a claim that Q-quantifiers cannot represent everything we want to say in English by the corresponding quantifiers, see Quine [1970], pp. 89–91 (branched quantifiers). For the claim that other quantifiers (e.g. “most”) cannot be represented in the style of the Q-quantifiers, see below, §17.

#### §5

For more detailed discussions of adjectives, see Platts [1979], ch. 7, and Kamp [1975].

#### §6

For Davidson’s proposal see his [1967b] and [1970a]. For discussion, see Platts [1979], pp. 190–201 and Taylor [1985]. For a different approach, see Clark [1970] and Parsons [1972]. For a proposal which accepts much of the spirit of Davidson’s, while rejecting the full appropriateness of Q-formalization, see Wiggins [1985].

#### §§7 and 12

Mill [1879], book 1, held that names and descriptions differ. Frege [1892b], p. 59, footnote, suggests that the sense of a name might be given by a definite description, but this is not a consequence of his general doctrines on the subject (see Dummett [1973], pp. 97–8: “there is nothing in what [Frege] says to warrant the conclusion that the sense of a proper name is always the sense of some complex description”), and might even be inconsistent with them (Evans [1982], pp. 22–38). None the less, the theory that names are descriptions is frequently attributed to Frege, for example by Kripke [1972], esp. p. 27, and Searle [1958]. Russell thought there are two kinds of name: “logically” proper names formalizable by name-letters, but in natural language consisting in only “this” and “that”; and “ordinary” proper names, like “Aristotle”, which are "really" abbreviations for descriptions. See Russell [1912], ch. 5, and [1918], pp. 200 ff. Russell does not intend this as a doctrine about the meaning of names, if meaning is what is in common between speaker and hearer in communication, but rather as contributing to an account of "the thought in the mind of a person using a proper name correctly" ([1912], p. 29); cf. Sainsbury [1993].


A gentle introduction to opposing views is Searle [1958]. Kripke [1972] attacks description theories of names, and his arguments have been widely discussed, for example by Dummett [1973], appendix to ch. 5. Some subtle distinctions are brought to bear by McDowell [1977]. See also Platts [1979], ch. 6, Linsky [1977], Davies [1981], esp. pp. 103 ff., Pollock [1982], chs 2-3, and Evans [1982], chs 1-3 and 11.

§8

See Quine [1960], §24.

§9

This standard treatment of numeral adjectives derives from Frege [1884], esp. §55 ff.

§10

Russell's theory of descriptions was first presented in Russell [1905], along with a general theory of quantification. A much clearer presentation, detached from the general theory of quantification, is in Russell [1919], ch. 16. A classic criticism is by Strawson (see his [1950], and his [1952], pp. 184-90), and a source of much debate is Donnellan [1966]. For further discussion, see Peacocke [1975], Sainsbury [1979], ch. 3, Davies [1981], ch. 7, and Pollock [1982], ch. 4. The best single source is Neale [1990].

§11

For Russell's account, together with his attack on Meinong, see Russell [1905] and [1918], lecture 5. For Meinong's theory see Meinong [1904]. For a philosophical discussion, see Lambert [1983], ch. 5. For a formal defence of a Meinongian position, see Parsons [1974]. For a philosophical plea for non-existents, see Yourgrau [1987].

For a brilliant account of negative singular existential truths which treats "exists" as a predicate, see Evans [1982], ch. 10.

§16

For Davidson's proposal, see Davidson [1969]. For discussion, see Platts [1979], ch. 5.

§17

See Platts [1979], pp. 100-6, Davies [1981], esp. pp. 123 ff., and Wiggins [1980a].

§18

A classic text on substitutional quantification is Kripke [1976]. A gentler introduction is by Quine [1969a]. See also Davies [1981], pp. 142 ff.

§19

For philosophical discussion, see Strawson [1974], Davies [1981], pp. 136 ff, and, for a sceptical view, Quine [1953b] and [1970], pp. 66-8. Predicate quantification may not be well motivated by considering natural English idiom, but there is certainly a case for it in the formalization of mathematics. Both Russell [1908] and Frege [1879], in their early attempts at formalizing mathematics, found it quite natural to use predicate quantifiers. A justification is provided by Boolos [1975], and Boolos and Jeffrey [1974 (1989)] provide a classic account of second order logic.


#### §20

A brief history of free logic is given in Lambert [1991a], editor's introduction, and the collection itself contains most of the classic papers. A longer history is provided by Bencivenga [1986]. My introduction to the topic was through Burge [1974], who argues for negative free logic in a truth theoretic setting. See also Schock [1968], Lambert [1965] and [1983], esp. ch. 5, and references therein. Bostock [1997] introduces the subject briefly, clearly and with philosophical insight. For an interesting application, see Evans [1979]. For the empty domain, see Quine [1952], p. 98, and Bostock [1997]. For a philosophical discussion of whether “Something exists” is a logical truth, see Cohen [1962], §33.


#### Notes


1 There would be a decisive objection if there were no properties: cf. Armstrong [1978].

² In *Principia Mathematica*, Russell proved that in restricted contexts you could treat the formal equivalents of English expressions of the form “The F is the G” (for example, “the most powerful man in the world is the President of the World Bank”) as if they were identity sentences: see Russell and Whitehead [1910], *14.272.

³ We certainly need an operator like the one envisaged in (11) to do justice to the thought that fictions are sometimes woven around real objects, a thought which might have a form along the lines:

$\exists x$ (according to some story) $(\ldots x \ldots)$.