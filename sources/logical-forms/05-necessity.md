---
book: "Logical Forms"
title: "Chapter 05 Necessity"
chapter_number: "5"
chapter_name: "Necessity"
author: "Mark Sainsbury"
table_of_content: |
  1 Adding “☐” to P
  2 Non-indicative and counterfactual conditionals
  3 Adding “☐” to Q
    Ex. 5.13 Assess the following argument:
    Ex. 5.14 Formalize the following in QN (omitting parenthetical material), commenting on the validity of your formalizations of (ii) and (iii):
  4 Necessity de re and de dicto
---

# 5 Necessity

If you are a physicalist, you may wish to assert not merely that everything is physical – which is consistent with this important fact being accidental – but also, more strongly:

1) Necessarily, everything is physical.

This chapter explores how one might augment $\mathbf{Q}$ so as to capture the distinctive contribution of English expressions like "necessarily". Superficially, at least, *`(1)`* appears to be composed of "everything is physical", dominated by the non-truth functional sentence operator "call necessarily". One option is to take appearances at face value, and add suitable non-truth functional sentence operators to $\mathbf{Q}$ (stipulating that these be counted among the logical constants). This augmented language will be called $\mathbf{QN}$.

*`(1)`* appears to be equivalent to

2) It is necessarily the case that everything is physical.

This seems to ascribe something – the property of being necessarily so – to a proposition. Possibility and necessity are interdefinable. A proposition is possible iff it is not impossible, iff its negation is not necessary. Possibility and necessity are called modal notions, and studying them is part of the study of modality.

Modal notions surface in idioms other than "necessarily" and "possibly", for example in "has to" and "must" as used in sentences like the following:

3) You have to make adequate financial provision for your children.

4) You must leave now or you'll miss your plane.

5) If you press down on one end of a rigid rod, freely balanced at its centre, the other end must go up.

6) This just has to be a herring.

These examples exploit different standards or criteria for the necessity they invoke: *`(3)`* is naturally heard as invoking moral necessity, *`(4)`* prudential necessity, *`(5)`* natural necessity and (6) epistemic necessity. We will discuss necessity of the broadest kind, so-called logical or metaphysical necessity. We make no attempt to give any account of what that is. It is exemplified in *`(1)`*, and there will be many subsequent examples.

## 1 Adding “☐” to P

We approach QN by an intermediate stage, a language, to be called PN, obtained from P by adding a new sentence operator, “☐”, pronounced “box”, with the intended meaning of “necessarily”. PN is called a “propositional modal language”.

Syntactically, “☐” is just like “¬”: if X is a PN-sentence, so is ☐X. A sentence of the form ☐X is called a “necessitation”.

Intuitively, we want ☐A to be true iff A has to be true, iff A is true however things might have been or may be, iff A is true in all possibilities, iff A is true at every possible world. A possible world is, as David Lewis [1973b] put it, a way our world could have been. Possible worlds are “maximal” in the following sense: for any possible world, every sentence is either true at it or false at it. To say that snow could have been black is to say that snow is black at some possible world. All modal auxiliaries (like “could” and “must”) and modal adverbs (like “possibly” and “necessarily”) are removed from the main body of sentences (in the example just given, “could” becomes plain “is”), and their contribution is regimented into locutions like “at some possible world”.

Ex. 5.1 Assuming that the sentences to which “☐” can be applied are as rich as the sentences of English, show that “☐” is a non-truth functional sentence connective.

The maximality of possible worlds makes them different from possibilities as we ordinarily conceive them. If we think about the possibility of rain, nothing in the possibility determines whether, in the possibility in question, kangaroos have tails. But at each possible world either "kangaroos have tails" is true, or else it is false.

We can use possible worlds to give semantics for PN. An interpretation of PN specifies, for each PN-letter, at which of the possible worlds it is true and at which it is false. This corresponds to the intuitive idea that the meaning of a sentence determines, among other things, in what circumstances it would be true, and in what circumstances it would be false. The interpretation rules likewise require that truth be relativized to a world as well as to an interpretation. Our rules from chapter 2.1 have to be rewritten; one way to do so is as follows:

1) For any set of possible worlds, $W$, any world, $w$, in $W$, and any interpretation $i$ of PN,

$\neg X$ is true at $w$ upon $i$ iff $X$ is false at $w$ upon $i$;

$(X \land Y)$ is true at $w$ upon $i$ iff $X$ is true at $w$ upon $i$ and $Y$ is true at $w$ upon $i$;

$(X \lor Y)$ is true at $w$ upon $i$ iff $X$ is true at $w$ upon $i$ or $Y$ is true at $w$ upon $i$;

$(X \rightarrow Y)$ is true at $w$ upon $i$ iff $X$ is false at $w$ upon $i$ or $Y$ is true at $w$ upon $i$;

$(X \leftrightarrow Y)$ is true at $w$ upon $i$ if either both $X$ and $Y$ are true at $w$ upon $i$ or both $X$ and $Y$ are false at $w$ upon $i$.

$\square X$ is true at $w$ upon $i$ iff for every world $w'$ in $W$, $X$ is true at $w'$ upon $i$.

We can add a symbol for "possibly" by the following definition:

2) $\diamondsuit X =_{df} \neg \square \neg X.$

"$\diamondsuit$" is pronounced "diamond". Validity is defined as follows:

3) $X_1, \ldots, X_n \models_{\mathsf{PN}} Y$ iff: for all interpretations, $i$, and all sets of worlds, $W$, if, for any world $w$ in $W$, all of $X_1, \ldots, X_n$ are true at $w$ upon $i$, $Y$ is true at $w$ upon $i$.

These semantics determine a system of propositional modal logic known as S5 (the terminology derives from Lewis and Langford [1932]). In the rest of this section we will explore its properties. Towards the end of the section I will briefly indicate how the semantics can be varied to give alternative propositional modal logics.


Consider the following argument:

4) Possibly, no one will come. Possibly, many people will come. Therefore it's possible that both no one and many people will come.

The argument is plainly invalid, rather in the way that

5) Some numbers are odd and some are even, therefore some numbers are both odd and even

is invalid.

With "p" corresponding to "no one will come" and "q" to "many people will come", the obvious PN-formalization of *`(4)`* is

6) $\diamond p, \diamond q; \diamond (p \land q)$

To show that *`(6)`* is PN-invalid, we need to find an interpretation and a set of worlds such that the premises are true at a world in the set upon the interpretation, whereas the conclusion is false at that world upon the interpretation. The definition of “$\diamond$”, together with the interpretation rule for “$\square$”, gives the derived interpretation rule for “$\diamond$”:

7) $\diamond X$ is true at $w$ upon $i$ iff for some world $w'$ in $W$, $X$ is true at $w'$ upon $i$.

**Ex. 5.2 Show how (1.7) is derived from the interpretation rule for “$\square$” together with the definition of “$\neg$”.**

Let $i$ assign truth at $w_1$ to “$p$”, falsehood at $w_1$ to “$q$”, falsehood at $w_2$ to “$p$”, truth at $w_2$ to “$q$”; and falsehood at all other worlds in $W$ to both “$p$” and “$q$”. This can be set out as in table 5.2, in which the assignment of falsehood to a letter is represented as the assignment of truth to its negation. “$\diamond p$” is true upon $i$, since there is a world, viz. $w_1$, at which “$p$” is true upon $i$; and at $w_1$, “$\diamond q$” is true upon $i$, since there is a world, viz. $w_2$, at which “$q$” is true upon $i$; but at $w_1$, “$\diamond (p \land q)$” is false upon $i$, since there is no world at which “$p \land q$” is true upon $i$. Hence $i$ is a counterexample to the validity of *`(6)`*. The essential point is structurally like what needs to be said to identify the fallacy of *`(5)`*: that there is a world at which “$p$” is true and one at which “$q$” is true does not entail that there is one at which both are true. Table 5.1 can be extended to show the relevant further features of $i$, as determined by *`(2)`* and *`(7)`* (see table 5.2). The justification for adding “$\diamond p$” to the $w_1$ column is that “$p$” occurs elsewhere in the table; the justification for adding “$\neg \diamond (p \land q)$” is that “$(p \land q)$” occurs nowhere in the table.

Table 5.1 Interpretation $i$

|  w_{1} | w_{2} | w_{3} | ...  |
| --- | --- | --- | --- |
|  p | ¬p | ¬p | ¬p  |
|  ¬q | q | ¬q | ¬q  |

Table 5.2 Further features of interpretation $i$

|  w_{1} | w_{2} | w_{3} | ...  |
| --- | --- | --- | --- |
|  p | ¬p | ¬p | ¬p  |
|  ¬q | q | ¬q | ¬q  |
|  ◊p | ¬(p & q) | ¬(p & q) | ¬(p & q)  |
|  ◊q |  |  |   |
|  ¬(p & q) |  |  |   |
|  ¬◊(p & q) |  |  |   |


Ex. 5.3 (a) Draw a diagram illustrating a set of worlds and an interpretation which establish the falsehood of:

$$\diamond p, \diamond (p \rightarrow q) \models_{PN} \diamond q$$

**`(b)`** Say whether the following is true, and argue informally for your view:

$$\square p, \diamond (p \rightarrow q) \models_{PN} \diamond q$$

The following is also invalid:

8) $p, \square (p \rightarrow q); \square q$

Table 5.3

|  w_{1} | w_{2}  |
| --- | --- |
|  p | ¬p  |
|  q | ¬q  |
|  p → q | p→q  |
|  □(p → q) |   |
|  ¬□q |   |

**Ex. 5.4** Give an English argument of the form of (1.8) in which the premises are plainly true and the conclusion plainly false.

This can be established by appealing to a set of worlds, $W$, containing just $w_1$ and $w_2$, as shown in table 5.3. The justification for adding “$\neg \square q$” to $w_1$ is that “$q$” does not appear in every world in the table, corresponding to the fact that at some world “$q$” is false upon the interpretation represented.

In contrast to *`(8)`*, the following is a cardinal principle of modal logic:

9) $\square X, \square (X \to Y) \vdash_{\mathsf{PN}} \square Y.$

The truth of *`(9)`* can be established informally by reflecting that an interpretation upon which both premises are true at some world in some arbitrary set of worlds, $W$, assigns truth at every world in $W$ to both $X$ and $X \to Y$, and so, by the interpretation rule for “$\to$”, must also assign truth to $Y$ at every world in $W$. Hence for any set of worlds, $W$, and any world in $W$, any interpretation upon which the premises are true at that world is one upon which the conclusion is true at that world.

Since the interpretation rules of $\mathbf{P}$ are mirrored in those for PN, we have

10) If $[\vdash_{\mathbf{P}} X]$, then $[\vdash_{\mathbf{PN}} X].$

In other words, any P-valid sentence is also a PN-valid sentence. We also have the stronger

11) If $[\vdash_{\mathsf{P}} X]$, then $[\vdash_{\mathsf{PN}} \square X].$

This says that the result of prefixing a $\mathbf{P}$-valid sentence by box is PN-valid. It reflects the thought that a valid $\mathbf{P}$-sentence corresponds to a necessary truth. If $\vdash_{\mathbb{P}}$ is enough for $\vdash$, in the way argued in chapter 2.10, and box corresponds to “it is logically necessary that”, then *`(11)`* must hold. For “$\vdash A$” is equivalent to “it is logically necessary that $A$” (cf. chapter 1.6).

The intuitively natural thought that what is necessarily true is true is verified by the interpretation rule for “$\square$”. It can be expressed by the truth of the generalization

12) $\square X \vdash_{\mathsf{PN}} X.$

This yields the stronger

13) $\vdash_{\mathsf{PN}} \square X \rightarrow X.$

Ex. 5.5 The move from (1.12) to (1.13) applies the “Deduction Theorem” to PN. We saw that an analogue of it for “if . . . then” and $\vdash$ can be put to a controversial use (1.8.14). The present application is not controversial, as you can establish by using the interpretation rules for PN to show:

If $[X, Y \vdash_{\mathsf{PN}} Z]$ then $[X \vdash_{\mathsf{PN}} Y \rightarrow Z]$.

By the definition of “$\diamond$”, this delivers

14) $\vdash_{\mathsf{PN}} \neg X \rightarrow \diamond \neg X$

and (after some intermediate steps)

15) $\vdash_{\mathsf{PN}} X \rightarrow \diamond X$.

Ex. 5.6 Use (1.14) to establish (1.15). Remember that “$X$” and “$Y$” are metalinguistic variables, so you can replace them by any PN-formula.

This accords with the intuition that anything actual is possible: what is in fact true can be true.

More controversially, PN has it that

16) $\vdash_{\mathsf{PN}} \square X \rightarrow \square \square X.$

This says that any conditional is valid in PN if its antecedent starts with an occurrence of “□” and its consequent consists of the antecedent prefixed by an occurrence of “□”. This corresponds to the claim that anything that is necessarily true is of necessity necessarily true. It is no accident which truths are necessary.

It is not entirely uncontroversial that *`(16)`* accurately reflects our intuitive views about necessity. Suppose, for example, that necessity is not an objective feature of the world, but is a product of human thinking. Suppose, further, that our patterns of thinking are determined by evolutionary pressures, but in a way that is not necessary (random mutations might be involved). Then we do not necessarily think as we do, so something which is in fact a necessary truth might not have been.

There is also in PN a stronger version of *`(15)`*:

17) $\vdash_{\mathsf{PN}} X \rightarrow \square \diamond X.$

An interpretation upon which $X$ is true at a world, $w$, is one upon which $\diamond X$ is true at that world and every other world, and so is one upon which $\square \diamond X$ is true at that world.

It is not uncontroversial that this correctly reflects our modal notions. You might agree that the fact that something is true guarantees that it is in fact possible, but not agree that it had to be possible. This is certainly correct for some restricted notions of necessity. For example, it is true (let us suppose) that you will catch the train, and this shows that it is possible for you to catch it. But it did not have to be possible: something could have happened to delay you, and then it would not have been possible for you to catch it (even though you will in fact catch it). So we have both "You will catch the train" and "It is not necessarily possible for you to catch the train", contrary to *`(17)`*. The modality here is related to time, and it would seem that the claim that it did not have to be possible for you to catch the train relates to an earlier time than the claims that you will catch it and that it is possible for you to catch it.

A further fact about PN which might be regarded as only dubiously appropriate to our intuitions about modality is that

18) $\vdash_{\mathsf{PN}} \diamond \diamond X \rightarrow \diamond X.$

This holds because for any world $w$, any interpretation upon which the antecedent is true at $w$ is one upon which $\diamond X$ is true at some world, and thus one upon which $X$ is true at some world; this last condition is enough to ensure that $\diamond X$ is true at $w$.

Do we intuitively believe that if something is possibly possible it is actually possible? A case for a negative answer is as follows (cf. Salmon [1981]). This table on which I am writing could not have been made out of entirely different parts, for a table made out of entirely different parts would not have been this table. However, it could have been made out of slightly different parts. We can put this as follows. Let $\alpha_{1}$ be the collection of parts out of which my table was in fact made, and let $\alpha_{2}$ be a slightly different collection. Then it seems plausible to say that my table could have been made out of $\alpha_{2}$. Let $\alpha_{3}$ be a collection of table parts differing slightly from $\alpha_{2}$ but significantly from $\alpha_{1}$. It seems plausible to say that if my table had been made of $\alpha_{2}$, as I allow is possible, then it could have been made from $\alpha_{3}$, but that as things are it could not have been made from $\alpha_{3}$ since these parts are too different from the actual parts. We might express this by the combination of claims, inconsistent with *`(18)`*:

19) $\diamond \diamond \text{(my table is constructed out of } \alpha_{3});$

$\neg \diamond \text{(my table is constructed out of } \alpha_{3}).$

PN has an interesting property, called modal collapse: given a non-modal sentence, $X$, that is, one containing no boxes or diamonds, there are only two non-equivalent fresh sentences you can form from it just by adding modal operators. They are, simply, $\square X$ and $\diamond X$. However many other boxes and diamonds you may stick in front of $X$, in whatever order, the result will be equivalent to one of these two sentences. To take two examples: *`(12)`* and *`(16)`* together ensure that

20) $\vdash_{\mathsf{PN}} \square \square X \leftrightarrow \square X$

which means that any pair of boxes can be collapsed to a single box. In addition,

Table 5.4 Failure of transitivity

|  w_{1} | ⇒ | w_{2} | ⇒ | w_{3}  |
| --- | --- | --- | --- | --- |
|  p |  | p |  | ¬p  |
|  □p |  | ¬□p |  |   |
|  ¬□□p |  |  |  |   |

21) $\vdash_{\mathsf{PN}} \square \diamond X \leftrightarrow \diamond X,$

which shows that box followed by diamond can be collapsed to just a diamond. Those who think that some PN-validities are inappropriate to our ordinary conception of modality can devise weaker modal languages by restricting in various ways the worlds which are relevant to truth upon an interpretation. The standard way to do this is to introduce a relation between worlds: the accessibility relation, call it $R$. Truth at a world depends at most upon how things are at $R$-related worlds. So, for example, the last clause of (1.1) will be revised to

22) $\square X$ is true at $w$ upon $i$ iff $X$ is true upon $i$ at every $w'$ such that $R w' w$.

The original rule for box is equivalent to letting $R$ hold universally, between arbitrary pairs of worlds. Restrictions on $R$ reduce the class of PN-valid sentences. For example, *`(13)`* $(\vdash_{\mathsf{PN}} \square X \rightarrow X)$ holds only if $R$ is reflexive (that is, only if every world is $R$-related to itself), so anyone wishing not to have this formula as valid could stipulate that $R$ is to be non-reflexive (that is, that there is at least one world, $w$, such that $\text{not-}Rww$).

Instances of *`(16)`* $(\square X \rightarrow \square \square X)$ hold only if $R$ is transitive (that is, only if for arbitrary worlds, if $Rw_1w_2$ and $Rw_2w_3$ then $Rw_1w_3$). Using open arrows to indicate the $R$-relation between worlds, table 5.4 shows a non-transitive $R$ and a counterexample to *`(16)`*. If $w_1$ were $R$-related to $w_3$, "$\square p$" would not be true at $w_1$. In the case of purely logical modality, it is doubtful whether we have any independent intuitions about what sort of relation $R$ should be. Rather, we shape $R$ to capture our intuitions about what logical principles should hold. However, for some restricted conceptions of necessity, it may be that we can have intuitions which relate directly to $R$. For instance, it might be suggested that what is morally necessary is what obtains in all morally perfect worlds, worlds in which what is morally required obtains. Then a natural account of what it would be for $Rw_1w_2$ to hold is that the moral requirements that obtain at $w_1$ are satisfied at $w_2$. It is not likely that this would be a transitive relation.


Ex. 5.7 Say whether you think that the accessibility relation for moral necessity would be transitive, and justify your view.

## 2 Non-indicative and counterfactual conditionals

A conditional apparently involving the subjunctive mood, like (2.4.35) (If Oswald hadn't shot Kennedy, someone else would have), appears to involve something modal. It seems to suggest some kind of necessary connection between Oswald not shooting and someone else shooting. It invites us to consider a possible world in which Oswald did not shoot Kennedy and its truth seems to require that in such a world someone else shot Kennedy. In this section, I consider how far we might go in understanding such conditionals using the modal notions we now have to hand: box, diamond, and possible worlds and accessibility relations. The first issue is taxonomy: how should we characterize these "subjunctive" or "counterfactual" conditionals?

In chapter 2 a preliminary distinction was drawn between indicative conditionals and others, based on contrasting sentences like (2.4.35) with ones like (2.4.34) (If Oswald didn't shoot Kennedy, someone else did). An initial guide was that indicative conditionals are expressed by using the indicative mood, and the other kind by using the subjunctive mood. However, we mentioned that this might be a less than reliable guide, and that (2.4.39) (If John dies before Joan, she will inherit the lot) might best be classified as "subjunctive" rather than "indicative" even though standard grammar would count both verbs as indicative. We now need to re-examine this classification.

One way to divide conditionals into two classes is to contrast the "counterfactual" ones with the rest, where a counterfactual conditional is defined by this feature: one who asserts it thereby represents its antecedent as false (or, in the case in which the antecedent is subjunctive, and so does not have a truth value, represents the corre sponding indicative as false). For many people, (2.4.35) is a conditional which counts as counterfactual by this test. However, some conditionals which resemble (2.4.35) – they have “had” in the antecedent and “would” in the consequent – can properly be used both by one wishing to represent the antecedent as false, and by one with no such wish. Suppose John has been accused of taking the bribe in the form of a large bundle of banknotes; suppose John is innocent and he and his lawyer believe, falsely, that the banknotes were discovered in the cleft of a certain apple tree. His lawyer can reasonably assert

1) If John had taken the bribe, he wouldn't have put the money in the apple tree,

representing the antecedent (or rather its corresponding indicative) as false: John did not take the bribe. But one of the detectives, thinking John to be guilty, and knowing that the money was not put in the apple tree, may also affirm *`(1)`* with the aim of showing that the fact that the money was not put in the apple tree does not count against John's guilt. The detective thus uses *`(1)`* not representing the antecedent to be false, but rather as part of a strategy designed to show that it is true.

Edgington ([1997], p. 99) puts the point in a strikingly general context. It is a general feature of empirical reasoning concerning some hypothesis, $H$, that we try to determine its truth by finding out how things would observably be it if were true. Such an enterprise cannot represent $H$ as false in advance of the enquiry. We say “if $H$ were true, we would observe such-and-such” with no commitment to the falsehood (or, for that matter, the truth) of $H$. There does not appear to be a category of conditionals the correct use of which requires representing the antecedent as false. This way of marking the contrast between the two “Oswald”-conditionals does not seem to yield a good general classification.

Ex. 5.8 Would the counterfactual/non-counterfactual contrast (as developed in the text) separate the two Oswald conditionals?

I shall use a more grammatical criterion, which starts by regarding the presence of the subjunctive in the antecedent as sufficient condition for belonging to one category, which I call that of “non-indicative” conditionals. This places (2.4.35) but not (2.4.34) in the category of non-indicatives, and also places in this category

2) If I were braver, I would stand up to her.

In this context, "were" is subjunctive. But, in English, the subjunctive is not always easy to identify and its use is not wholly systematic. It would be hard to believe that *`(2)`* deserves to be treated differently from

3) If I was braver, I would stand up to her.

One may think that "was" should be classified as a past tense rather than a subjunctive. Even if this is right, I would still wish to adopt a criterion which includes *`(3)`* among the non-indicatives. One way to achieve this is to stipulate that anything equivalent to a non-indicative is to count also as non-indicative. Another way is to say that having "would" in the consequent is a further sufficient condition for belonging to this category. I make both stipulations. There is a distinct reason for counting *`(3)`* as non-indicative. There is no genuine pastness about the use of "was" in *`(3)`*, any more than there is in such a sentence as

4) I wish I was braver.

This gives us a reason for not counting this occurrence of "was" as a straightforward indicative past tense, and so for including *`(3)`* among the non-indicatives. (In some languages, words used like "was" in *`(3)`* are counted as belonging to the "conditional" tense.)

**Ex. 5.9 What words would you use to express a wish about your bravery that related to some occasion now in the past?**

There are some reasons to think that conditionals like

5) If John attends tomorrow, he will vote for the motion

should not be classified with indicative ones. Suppose that Mary uttered *`(5)`* on Monday, the meeting takes places on Tuesday, and on Wednesday I am asked to report what Mary told me. The following seems appropriate:

6) Mary said that if John had attended yesterday, he would have voted for the motion.

In my report I use a non-indicative conditional to report what was said by an apparently indicative one. The switch seems to be of the same kind as the switch from "tomorrow" to "yesterday". In further support of classifying *`(5)`* as non-indicative, it can be pointed out that "John attends tomorrow" is no ordinary present tense indicative. Used assertively on its own, it would not be strictly intelligible (unless, perhaps, it issued from the mouth of an almighty creator fixing the future behaviour of his creatures, a use which has no bearing on *`(5)`* – cf. Edgington [1997], p. 98). This kind of bogus present tense seems to be widespread in English conditionals in which "will" governs the main verb in the consequent. If these points are accepted, (2.4.39) (If John dies before Joan, she will inherit the lot) would get classified with non-indicatives.

The suggestion has been disputed. One's willingness to make the switch exemplified in *`(5)`* and *`(6)`* seems to vary with the kind of reason one has for accepting the seemingly indicative conditional. The switch is most natural if I believe *`(5)`* for the more obvious kinds of reason: I know John's views on the matter, he has made sincere expressions of intention, etc., but there may be some uncertainty about whether he will be able to be present. Contrast this with a less usual scenario: John is hostile to the motion and its proponents are planning to prevent him voting against it: they will either bribe him to vote for the motion (plan A), or, if he won't be bought, they will kidnap him and so prevent him from attending (plan B). Knowing all this, Mary can affirm *`(5)`* before the meeting: if John attends, then plan A has worked, so he will vote for the motion. But afterwards, if Mary knows John didn't attend, she will not be disposed to believe that if he had attended he would have voted for the motion: if he didn't attend, the likely explanation is that the villains adopted plan B, given which, if John had attended, if would be because he had escaped from his kidnappers, in which case he would have voted against. (Cf. Edgington [1991], Bennett [1995].)

For present purposes, this issue does not need to be resolved: it is enough that we have clear cases of non-indicatives, marked by the subjunctive or by the modal auxiliaries like "would" (in the consequent) and "had" (in the antecedent), exemplified by (2.4.35) (if Oswald hadn't...), and clear cases of indicatives like (2.4.34) (if Oswald didn't...). We can be neutral about the classification of conditionals like *`(5)`*.

To say that there is a contrast between indicative and non-indicative conditionals is not to say that “if” is ambiguous. It could be that “if” functions in the same way in both kinds of conditional, and that the contrast is due to the contrasting indicative or non-indicative character of the verbs (cf. Woods [1997], p. 10).

With this rough account of our subject matter as non-indicative conditionals, we can return to the main question of whether we can give an account of them using our current resources (P supplemented by boxes and diamonds, and semantics using possible worlds and accessibility relations). The non-indicative “Oswald”-sentence (2.4.35) (If Oswald hadn’t shot Kennedy, someone else would have) carries a suggestion of necessity, so an obvious first thought is to formalize it:

7) $$\square(\neg p \to q)$$

with “p” corresponding to “Oswald shot Kennedy” and “q” to “Someone else shot Kennedy”. (We will ignore the fact that PN obviously cannot express the quantificational structure.)

In favour of the formalization, it might be argued that all possible worlds divide into two classes: those in which Oswald did shoot Kennedy, and those in which he did not. “$\neg p \to q$” is true (upon an intended interpretation) at all members of the first class of worlds, which will include the actual world (on the assumption of Oswald’s guilt), in virtue of the falsity of the antecedent; and if *`(7)`* is true, there is some appeal in the thought that “$\neg p \to q$” is true at every world in the second class as well. *`(7)`* may seem to say that any world in which Oswald didn���t shoot Kennedy is one in which someone else did.

However, this is much too demanding relative to the English, which is not falsified by a world in which Kennedy never existed, nor by a world in which he never came before the public eye, and so was not a target for assassination, nor by a world in which the most stringent security precautions were invariably taken.

The defect may seem easy to remedy. Let us restrict the worlds that are relevant to the truth of a formalization of (2.4.35) to worlds that are similar, in certain contextually determined respects, to the actual one. For (2.4.35) the relevant worlds are restricted at least to those in which Kennedy exists, became President, and was not always subject to the most stringent security precautions.

No PN-operator carries this restriction to similar worlds. However, let us use “$\square \rightarrow$” to formalize non-indicative conditionals, introduce a special interpretation rule for them, and use “PNS” to stand for the result of adding this symbol and this rule to PN.

The syntax of “$\square \rightarrow$” (pronounced “box arrow”) is that it takes two indicative sentences to form a sentence. (This formalization carries a substantive commitment: it presupposes that the non-indicative aspects of the conditional can be bundled into the box arrow, and that the overall content is fixed by indicative contents that are not explicitly expressed.) With the correspondences of *`(7)`*, (2.4.35) will be formalized

8) $$p \ \square \rightarrow q$$

An interpretation rule for “$\square \rightarrow$” which would reflect the considerations so far adduced is

9) $X \ \square \rightarrow Y$ is true at $w$ upon $i$ iff for every world $w'$ in $W$ which is similar to $w$, $X \to Y$ is true at $w'$ upon $i$.

This rule will validate intuitively invalid inferences using non-indicative conditionals. For example, we have

10) $$X \ \square \rightarrow Y \vdash_{\text{PNS}} (X \land Z) \ \square \rightarrow Y$$

for arbitrary $Z$. The premise is true at a world, $w$, upon an interpretation, $i$, iff $X \to Y$ is true at all worlds in $W$ which are similar to $w$. But any world at which $X \to Y$ is true upon $i$ is one at which $(X \land Z) \to Y$ is true upon $i$. So the conclusion is true at $w$ upon $i$. However, we do not accept that arguments like the following are valid (compare (2.5.28)):

11) If I had put sugar in this cup of coffee, it would have tasted good. So if I had put sugar and diesel oil in this cup of coffee, it would have tasted good.

Ex. 5.10 Assess the following argument:

The antecedent of (2.11) is false, taken quite literally, though what is intended is true, and could be more properly expressed along the lines: "If I had added sugar to this cup of coffee and everything else had remained as much the same as possible, then it would have tasted good."


Cf. Urbach [1988], p. 197.

This sort of case suggests that there cannot be a fixed standard of similarity of worlds, applicable to all non-indicative conditionals. For example, consider evaluations with respect to the actual world, and suppose that I put sugar but not diesel into my cup: if we set the standard of similarity high, then “(I put sugar and diesel oil in this cup of coffee) → (it tastes good)” is true at every similar world, since every world which is very similar to ours is one in which the antecedent is false. This high standard would formalize the conclusion of (11) as true upon an intended interpretation, which is not what we want. If we set the standard low, then “(I put sugar in this cup of coffee) → (it tastes good)” is false at some similar world, for example a world in which diesel is added as well as sugar. This low standard would formalize the premise of (11) as false upon an intended interpretation, which is not what we want. What is needed, therefore, is variability in how great the similarity must be, as a function of the content of the antecedent. The worlds we need to consider are not all those which are similar to the actual one, but only those at which the antecedent is true. I shall call such accounts of conditionals “A-world” accounts, and will consider two quite similar versions, one by Lewis and one by Stalnaker.

I start by showing that the desirability of an A-world account can be arrived at from a quite different direction. We can start by considering how we tell whether or not to accept a conditional. Following a discussion by Frank Ramsey [1929], Stalnaker proposed the following approach:

> *First, add the antecedent (hypothetically) to your stock of beliefs; second, make whatever adjustments are required to maintain consistency . . . finally consider whether or not the consequent is then true. (Stalnaker [1968], p. 44)*

Although this speaks to the conditions under which we should believe a conditional, Stalnaker argued that we can use the same basic idea to arrive at truth conditions for conditionals:

Table 5.5

|  Less similar  |   |   |
| --- | --- | --- |
|  World of evaluation, w* | w1 | w2  |
|  ¬X | X | X  |
|  ¬Y | Y | ¬Y  |
|  ¬Z | ¬Z | Z  |

> *Consider a possible world in which $A$ is true, and which otherwise differs minimally from the actual world. "If $A$, then $B$" is true (false) just in case $B$ is true (false) in that possible world. (p. 45)*

This is an $A$-world account, for it implies that if a world is relevant to the truth of a conditional it is a world at which the antecedent is true. Converting the proposal to the present approach and terminology, we can express it thus:

12) $X \square\rightarrow Y$ is true at $w$ upon $i$ iff $Y$ is true upon $i$ at a world maximally similar to $w$ at which $X$ is true upon $i$. (If there is no such world, that is, if $X$ is impossible, $X \square\rightarrow Y$ is true upon $i$.)¹

The account is appealing for its claim to mirror our actual conditional thinking. It correctly classifies as invalid the pattern of reasoning exemplified by *`(11)`*:

13) $X \square\rightarrow Y; (X \land Z) \square\rightarrow Y.$

Table 5.5 shows an interpretation in a structure of worlds upon which the premise is true and the conclusion false. In this structure, there are just three worlds: $w^*$ (which we may think of as the actual world), which is the world of evaluation, and two others, both $X$-worlds (worlds at which $X$ is true). Of these two, the one at which $Y$ holds is more similar to $w^*$ than is the other, so the structure verifies $X \square\rightarrow Y$. However, it does not verify $(X \land Z) \square\rightarrow Y$, for the most similar $(X \land Z)$-world to $w^*$ is not a $Y$-world.


Table 5.6

|  World of evaluation, w* | Less similar | w_{1}  |
| --- | --- | --- |
|  ¬X | ¬X | X  |
|  ¬Y | Y | Y  |
|  ¬Z | Z | ¬Z  |

These semantics for $\square \rightarrow$ make it non-transitive (in the sense of (2.5.21): the following argument pattern is not valid:

14) $X \square \rightarrow Y, Y \square \rightarrow Z; X \square \rightarrow Z.$

This will be welcome if we find arguments like the following invalid:

15) If Hoover had been born a Russian, he would have been a communist.

If he had been a communist, he would have been a traitor.

So if he had been born a Russian, he would have been a traitor.

**Ex. 5.11** What happens if the two premises of (2.15) are conjoined into a single premise? For a defence of transitivity for $\square \rightarrow$ (the principle of which (2.15) is an instance), see Urbach [1988], p. 198.

Table 5.6 serves as counterexample. It makes vivid that only $A$-worlds are relevant to the truth of a $\square \rightarrow$ sentence; and among $A$-worlds, only ones more similar to the world of evaluation.

The logic which results from these semantics coincides (in terms of what it says is valid) with the probabilistic logic of chapter 3.

Can we assume that for each world, and in particular for the actual world, there is a unique “maximally similar” world? For example, should we say that a world in which Verdi and Bizet were both French is more similar or less similar to the actual world than one in which they were both Italian? The question would appear to need an answer (on Stalnaker’s semantics) if we are to evaluate conditionals like

16) If Bizet and Verdi had been compatriots, Bizet would have been Italian.

17) If Bizet and Verdi had been compatriots, Verdi would have been French.

If a “both Italian” world is closer than a “both French” world then *`(16)`* is true and *`(17)`* false; and vice versa. If both worlds are equally close, then there is no such thing as “the” $A$-world closest to actuality.

Stalnaker’s approach, in more detail, uses a selection function which, for every antecedent–world pair, $\langle a, w \rangle$, delivers a unique $A$-world “most similar” to $w$. Formally, then, there is no problem about non-uniqueness. However, Stalnaker proposes that, in interpreting a conditional, context may determine which of various distinct selection functions is appropriate. Suppose that *`(15)`* is being considered against the background of some fantastic tale in which both musicians are born with no nationality, but are rescued from an international orphanage, and given name and nation. The parents who ended up adopting Verdi were Italian (so the story goes), and very nearly adopted Bizet as well, whereas the French parents who in fact adopted Bizet had no intention of adopting more than one child. Arguably, in this background, it will be natural, in interpreting *`(15)`*, to prefer a selection function which assigns to the pair consisting of the world of the story and “Bizet and Verdi are compatriots” a world in which both are Italian.

Stalnaker’s approach, in more detail, uses a selection function which, for every antecedent–world pair, $\langle a, w \rangle$, delivers a unique $A$-world “most similar” to $w$. Formally, then, there is no problem about non-uniqueness. However, Stalnaker proposes that, in interpreting a conditional, context may determine which of various distinct selection functions is appropriate. Suppose that *`(15)`* is being considered against the background of some fantastic tale in which both musicians are born with no nationality, but are rescued from an international orphanage, and given name and nation. The parents who ended up adopting Verdi were Italian (so the story goes), and very nearly adopted Bizet as well, whereas the French parents who in fact adopted Bizet had no intention of adopting more than one child. Arguably, in this background, it will be natural, in interpreting *`(15)`*, to prefer a selection function which assigns to the pair consisting of the world of the story and “Bizet and Verdi are compatriots” a world in which both are Italian.

There may also be cases, and as things are (15) and (16) are examples, in which we have no reason to prefer one selection function rather than another. In this case, there is no determinate assignment of truth value.²

Stalnaker’s account has been criticized for rendering all sentences of the following form valid:

18) $(X \square\rightarrow Y) \vee (X \square\rightarrow \neg Y)$.

There is something to be said on behalf of its validity: to deny a non-indicative conditional of the form $X \square\rightarrow Y$, a good thing to say is $X \square\rightarrow \neg Y$. Arguably, either you or your protagonist must be right, in which case *`(18)`* should be valid.


Its validity on Stalnaker's semantics follows from the facts that (i) Stalnaker's worlds are classical, in that the law of excluded middle $(X \vee \neg X)$ holds at each; and (ii) any selection function will choose a unique $X$-world. Since either $Y$ or $\neg Y$ will hold at the selected world, so will one or other disjunct of *`(18)`*.

There appear to be counterexamples to the validity of *`(18)`*, for example

19) Either, if it were not $30^{\circ}$ outside it would be $40^{\circ}$, or if it were not $30^{\circ}$ it would not be $40^{\circ}$.

If it is not $30^{\circ}$ it might or might not be $40^{\circ}$, but it seems wrong to affirm, under this supposition, that it would be $40^{\circ}$ and wrong to affirm that it would not (cf. Pollock [1976], p. 16).

Logical space contains a number of $A$-worlds accounts. One of the most discussed has been offered by Lewis [1973b]. Adapting it to present purposes and terminology, it is this:

20) $X \square\rightarrow Y$ is true at $w$ upon $i$ iff some world at which $X \land Y$ is true upon $i$ is more similar to $w$ than any world at which $X \land \neg Y$ is true upon $i$, if there are any worlds at which $X$ is true (if there are none, $X \square\rightarrow Y$ is true).

This does not require a unique $X$-world or a unique $(X \land Y)$-world: there can be any number. But it does require that if an $(X \land Y)$-world ties for most similar with an $(X \land \neg Y)$-world, the conditional is false. This makes formalizations of *`(16)`* and *`(17)`* false upon an intended interpretation (assuming that both-Italian worlds and both-French worlds are equally similar to actuality). It also withholds validity from *`(18)`*. Consider the instance

Ex. 5.12 What is the truth value upon an intended interpretation of an adequate PNS-formalization of the following (applying (2.20))?

If Bizet and Verdi had been compatriots, they would have either both been Italian or else both French.

What impact does your answer have upon the correctness of Lewis's proposal?

21) (If the coin had been tossed it would have landed heads) or (if the coin had been tossed it would not have landed heads).

If the coin is never actually tossed, a head-landing and a non-head-landing world seem not to differ in degree of similarity to ours; hence no tossing-world in which it lands heads is *more* similar to actuality than any in which it doesn’t; nor is any tossing-world in which it doesn’t land heads more similar to actuality that any in which it does. So both disjuncts are false. As the example suggests, it is not entirely clear that this is a desirable result. Even if one has doubts about the validity of *`(18)`*, one might be keen that it have some true instances — and *`(21)`* is, arguably, true.

Lewis says that the notion of overall similarity involved in his account is “extremely vague”. He counts this as a virtue, for the non-indicative conditionals under discussion “are both vague and various. Different resolutions of overall similarity are appropriate in different contexts” ([1979], p. 56). Let us see how he applies these ideas by considering an objection. Intuitively, the following is true:

22) If Nixon had pressed the button, there would have been a nuclear holocaust. (Cf. Fine [1975]; Lewis [1979], in Jackson [1991], p. 59)

But it might seem to come out false on Lewis’s semantics. A world in which Nixon pressed the button but through some fault nothing happened (and soon thereafter he changed his mind) would seem much more similar to our own world than one in there was no fault and so there was a holocaust. We don’t think a fault was at all likely: we think that if the button had been pressed, the ICBMs would have taken to the skies. But we think this would have made for a world very unlike ours, much more unlike it than one in which there was a fault. For we also hold true the following:
23) If Nixon had pressed the button, things would have been radically different.

Lewis does not think that we have an entirely independent conception of similarity upon which we can simply draw to effect an analysis of conditionals. Rather, he thinks we can allow an explication of the relevant conception of similarity to be shaped and guided by our judgements about non-indicative conditionals. The shaping, he suggests, involves weighting similarities. In evaluating conditionals like *`(22)`*, we implicitly operate with a notion of similarity among worlds which gives greatest weight to avoiding “big, widespread, diverse violations of law”; next greatest to maximizing “the spatio-temporal region throughout which perfect match of particular fact prevails”; next greatest to avoiding “even small, localized, simple violations of law”; and least importance to securing “approximate similarity of particular fact” (cf. Lewis [1979], in Jackson [1991], p. 64). A world in which Nixon presses the button is somewhat unlike ours; to match ours perfectly where possible, we take everything to be in order with the wiring and the rockets. If we add that the holocaust occurs, we need not suppose any difference in laws. There are two ways to develop the supposition that the signal never gets to the rockets. Upon the first, the signal failure is the only difference in law. So the light waves carrying the image of Nixon pressing the button continue on their journey through space, Nixon’s memories are different, and so on. In that case, we lose perfect match at that point, which is a grade 2 point of dissimilarity (we have approximate match, but this is only grade 4.) The idea is that this dissimilarity should outweigh the similarities. Alternatively, we secure reconvergence by a host of nomic differences (the light waves mysteriously peter out, etc.), but now we are involved in widespread violations of law, a grade 1 dissimilarity. Arguably, therefore, with appropriate weighting of similarities Lewis’s semantics for conditionals assigns truth to *`(22)`*.


There are some rather different difficulties about incremental similarities. Intuitively, a world in which I am taller than I actually am by being 6ft 6in is more similar to the actual world than one in which I am taller by being 6ft 7in. This leads to the strange consequence that

24) If I were taller, I would only be a tiny bit taller

is true. Any world in which I am taller by a given amount is less similar to actuality than one in which I am taller by a smaller amount. We might again see this case as calling for an adjustment in the concept of similarity. The original intuition, shared by Lewis and Stalnaker, was, in Lewis’s words this time, that a conditional of the kind in question is true “iff it takes less of a departure from actuality to make the conse- quent true along with the antecedent than it does to make the antecedent true without the consequent” (Lewis [1973c], p. 164, my emphasis). However, it is plausible to suggest that one world can by some standard be more similar to actuality than another while involving no less of a departure from actuality (cf. Pollock [1976], p. 21). I actually live in London; a world in which I live in Slough departs from actuality and so does a world in which I live in Oxford. There is nothing to choose between these departures from the point of view of evaluating any non-indicatives I can think of. However, there is a standard of similarity by which the first world is more similar to actuality than the second, for Slough is nearer to London than is Oxford. This difference is not to be taken seriously in evaluating a conditional like “If I didn’t live in London I would live in Slough”. It would be absurd to suppose that if I didn’t live in London I would live near it: on the contrary, if I didn’t live in London, I would live in the heart of the country.


I am actually 6ft 4in. Both being 6ft 6in and being 6ft 7in are departures from actuality. But when we are asked, by Lewis or Stalnaker, to consider $A$-worlds which involve “minimal departures” from actuality, the relevant minimality means worlds in which there are no changes other than something required to make the world an $A$-world: no “gratuitous” changes, as Lewis sometimes puts it. This gives a basis for a standard of similarity in which, relative to the antecedent of *`(24)`*, 6ft 6in worlds are no smaller departures than are 6ft 7in worlds.

The discussion is designed to show that the resources of possible worlds accounts are rich: if non-indicative conditionals have truth conditions at all (an issue raised for indicative conditionals in chapter 3.5) it would be surprising if they could not be stated with more or less the resources specified here.

Stalnaker thought that just the same semantic clause would do for conditionals of every kind, the differences between indicatives and non-indicatives emerging simply at the “pragmatic” level in the choice of selection function. This is an extreme version of the view that conditionals need a unified treatment. Lewis, by contrast, holds that indicative conditionals are truth functional. It is open to him to regard his treatment of indicative and non-indicative as, in a sense, unified. Lewis’s semantics for non-indicatives in effect require the truth of the corresponding truth functional conditional at a subset of possible worlds. He could regard “if” as contributing the truth functional conditional, and departures from the indicative as contributing the rather complex modal material, so that there is no question of “if” having more than one meaning.


Supposing appears to be a mental act crucial in understanding conditionals. It is one thing to suppose that Oswald didn’t kill Kennedy and another to suppose that he hadn’t killed Kennedy; supposing is a kind of mental act which is normally involved in both non-indicative and indicative cases. This should encourage the view that there is a deep unity between these kinds of conditional.

## 3 Adding “☐” to Q

QN results from adding box to Q, treating it as having the syntactical properties of tilde. This gives rise not only to sentences like

1) $\square \forall x(Fx \rightarrow Fx)$

which, with “$F$” corresponding to “is a mathematician”, seems a reasonable formalization of

2) Necessarily, all mathematicians are mathematicians;

but also to sentences like

3) $\forall x(Fx \rightarrow \square Fx)$

which, with correspondences as before, would formalize

4) All mathematicians are necessarily mathematicians.

The reading of (4) formalized by *`(3)`* intuitively strikes one as false. People who become mathematicians don’t have to turn to mathematics: there is an element of choice.

The interpretation rules for PN are silent on the question of how quantifiers interact with modal operators. Intuitively we want an interpretation with respect to the actual world to falsify (3), for a mathematician who didn’t have to be a mathematician would be a counterexample to the conditional. In the obvious way of understand- ing this idea, this means that some mathematician needs to occupy two worlds, one at which he is a mathematician and one at which he is not. The latter fact ensures the falsity of the consequent of the conditional (as instanced on this person), and the former the truth of its antecedent. Not all theorists allow that we can make sense of objects which exist at more than one world (see §9 below). Even if one can make sense of it, we need to say whether interpretations have the same domain relative to each world, or whether the domain varies from world to world. Choices on these issues are controversial, and have an impact on validity. In this section I will adopt one mainstream view. It has an unrestricted accessibility relation (so this will not be mentioned); it allows objects to exist at more than one world; and it allows interpretations to have different domains with respect to different worlds.


We stipulate that for each world $w$ there is a non-empty domain $D^w$ (the entities in $w$). In chapter 4, we used expressions like "$i(F)$" to designate the set assigned by a Q-interpretation, $i$, to the predicate letter "$F$". Here we extend that notation, using expressions of the form "$i_w(X)$" to designate what a QN-interpretation, $i$, assigns to an expression, $X$, with respect to a world, $w$.

5) For any set of worlds, $W$, any world, $w$, in $W$, and any interpretation $i$ of QN:

for each sentence-letter $P$, $i_w(P)$ is a truth value, either T or F;

for each name-letter $n$, for some world $w'$, $i_{w'}(n)$ is an object, $\alpha$, in $D^{w'}$ and for every world, $w''$, if $\alpha$ belongs to $D^{w''}$, $i_{w''}(n)$ is $\alpha$ and if $\alpha$ does not belong to $D^{w''}$ there is no $i_{w''}(n)$ (e.g. "$\alpha$" might be assigned Ronald Reagan with respect to any world at which Reagan exists, and assigned nothing with respect to the other worlds);

for each predicate-letter $\phi$ of degree $n$, $i_w(\phi)$ is a set of $n$-tuples ($n$-membered sequences) all of whose members belong to $D^w$ (for example, $i_w(F)$ might be a set of ordered pairs in $w$ such that the first member of the pair loves the second);

$i_w(=)$ is the set of ordered pairs of members of $D^w$ such that in each pair the first object is the same thing as the second.

An intended interpretation of a QN-sentence will assign to each name-letter in the sentence, with respect to each world $w$, the actual bearer of the corresponding name, if that thing exists at $w$, and otherwise will assign nothing to the letter with respect to $w$; it will assign to each $n$-ary predicate-letter in the sentence, with respect to each world $w$, those $n$-tuples of members of $D^w$ which possess the property associated with the corresponding predicate.


6) For any set of worlds, $W$, any world, $w$, in $W$, and any interpretation $i$ of QN,

**`(i)`** $i_w(\neg X)$ is T iff $i_w(X)$ is F.

**`(ii)`** $i_w(X \wedge Y)$ is T iff $i_w(X)$ is T and $i_w(Y)$ is T.

**`(iii)`** $i_w(X \vee Y)$ is T iff $i_w(X)$ is T or $i_w(Y)$ is T.

**`(iv)`** $i_w(X \to Y)$ is true iff $i_w(X)$ is F or $i_w(Y)$ is T.

**`(v)`** $i_w(\phi n_1 \ldots n_k)$ is T iff all of $i_w(n_1) \ldots i_w(n_k)$ belong to $D^w$ and $\langle i_w(n_1) \ldots i_w(n_k) \rangle$ belongs to $i_w(\phi)$; otherwise $i_w(\phi n_1 \ldots n_k)$ is F.$^3$

**`(vi)`** $i_w(\forall \nu X)$ is T iff $X_\nu^n$ is T upon every $n$-variant of $i$ which assigns something to $n$ at $w$.

**`(vii)`** $i_w(\exists \nu X)$ is T iff $X_\nu^n$ is T upon some $n$-variant of $i$ which assigns something to $n$ at $w$.

**`(viii)`** $i_w(\square X)$ is T iff for all worlds $w'$ in $W$, $i_{w'}(X)$ is T.

QN-validity can be defined exactly like PN-validity. What makes the difference is the richer notion of interpretation for QN as compared with PN.

An intended interpretation is one which assigns entities to the various simple expressions in such a way as not to depart from their actual meaning. Such an interpretation should deliver adequate formalizations: ones whose truth-upon-an-intended interpretation conditions match the truth conditions of the English. Applying our interpretation rules to *`(3)`*, an intended interpretation, $i$, will, for each of its domains, assign the set of mathematicians in the domain to “$F$”. (When a domain contains no mathematicians, $i(F)$ is the empty set.) This interpretation will assign truth to *`(3)`* with respect to the actual world, $w^{\star}$, iff $\alpha$-variants of it which assign something to $\alpha$ at $w^{\star}$ assign truth to "$F\alpha \to \square F\alpha$" with respect to $w^{\star}$. Some $\alpha$-variant $i'$ of $i$ will assign Cantor to $\alpha$ at $w^{\star}$. He was a mathematician, but he didn't have to be one. So $i'_{w^{\star}}(F\alpha)$ is $T$, but there is a world $w$ other than $w^{\star}$ such that $i'_{w}(F\alpha)$ is $F$, so $i'_{w^{\star}}(\square F\alpha)$ is $F$, so $i'_{w^{\star}}(F\alpha \to \square F\alpha)$ is $F$, so $i_{w^{\star}}(\forall x(Fx \to \square Fx))$ is $F$.


Whether (6viii) is appropriate to the ordinary notion of necessity raises a number of issues, for example those relating to whether or not the accessibility relation between worlds needs to be restricted (cf. §1 above). Here we raise just one issue, concerning existence and a distinction between "strong" and "weak" necessity.

We have given an example in which a sentence of the form “$\square F\alpha$”, “Necessarily, Cantor was a mathematician”, is false. Are there any examples of truths of this form? One candidate is
7) Necessarily, Socrates is human.

You might well think that this is true: anything non-human – a stone or a crocodile – simply could not be Socrates. Even if there is room for doubt on this point, it would seem that an appropriate language for necessity should not preclude the truth of a sentence like *`(7)`*. However, the QN-formalization of *`(7)`* as “$\square F\alpha$” will not be true upon an intended interpretation, $i$. With respect to each world, $w$, $i_w(F)$ is the set of all humans in $D^w$; and $i_w(\alpha)$ is Socrates with respect to every world at which Socrates exists. Any reasonably rich set of worlds will contain one whose domain does not include Socrates – a world at which Socrates does not exist. (We all agree that Socrates might not have existed, and would not have done if the world had ended ten years before the year in which he was born.) With respect to such a world, $w$, $i_w(F\alpha)$ is $F$, by (6v), so $i_{w^{\star}}(\square F\alpha)$ is false. An intended interpretation assigns $F$ to a QN-sentence which is supposed to formalize a truth (or at least something whose truth is plausible); and this is a sign that something is wrong.

There are at least two ways of responding to this difficulty. One involves weakening the interpretation rule for $\square$ so that $\square X$ is true upon an interpretation $i$ iff $X$ is true upon $i$ at every world at which all the objects which $i$ assigns to any name-letters in $X$ exist. Then we could formalize (7) straightforwardly, as “$\square F\alpha$”, and it would not be false upon an intended interpretation merely in virtue of the fact that Socrates might not have existed.

Alternatively, we could keep to the original interpretation rule for $\square$, and formalize sentences like *`(7)`* as

8) $$\square((\exists x \, x = \alpha) \to F\alpha)$$

with “$F$” corresponding to “is human”. The semantics for QN do not preclude *`(8)`* being true upon an intended interpretation. Worlds at which Socrates does not exist will be worlds at which “$(\exists x \, x = \alpha) \to F\alpha$” is true upon an intended interpretation in virtue of the falsity of the antecedent at such worlds.

The first response introduces the so-called “weak” interpretation of necessity; the interpretation rule (6viii) expresses the “strong” interpretation.

Necessitated existential sentences themselves provide a reason for preferring the strong interpretation, and thus for adopting the more complex formalizations, in the style of *`(8)`*, of sentences like *`(7)`*. We might debate whether the following is true:

9) Necessarily, the number 7 exists.

We could formalize this by

10) $$\square \exists x \, x = \alpha$$

with “$\alpha$” corresponding to “the number 7”. Keeping to our rule (6viii), that is, treating the box as expressing strong necessity, the question of the truth of *`(10)`* upon an intended interpretation is not foreclosed by the formalization. If we interpret box as expressing weak necessity, *`(10)`* will express a trivial truth upon an intended interpretation: it will in effect say that $\alpha$ exists at every world at which it exists. This would make it a poor candidate for formalizing *`(9)`*, and a hopeless candidate for formalizing “necessarily, Socrates exists”.

On the strong interpretation of box, *`(10)`* is false upon some interpretations at some worlds and so is not trivial. Consider an interpretation assigning Socrates to “$\alpha$”. “$\exists x \, x = \alpha$” will be false upon this interpretation at a world at which Socrates does not exist, so upon this interpretation *`(10)`* will be false (at every world).

This virtue of the strong interpretation carries with it a worry. The fact that *`(10)`* is not QN-valid means that we cannot accept for QN the correlate of (1.11) for PN. That is, the following is false:

11) If $[⊢_{\mathbb{Q}} X]$, then $[⊢_{\mathbb{QN}} \square X]$.

We have $\vdash_{\mathbb{Q}} \exists x \, x = \alpha$, but not $\vdash_{\mathbb{QN}} \square \exists x \, x = \alpha$. Given the philosophical motivation for (1.11), this should be genuinely disturbing. It would not be satisfactory to try to reinstate *`(11)`* by insisting that every name-letter is always assigned something by every interpretation with respect to every world, for then, intuitively, a name-letter cannot adequately formalize a name for a contingent being, one which actually exists but which might not have done.

### Ex. 5.13 Assess the following argument:

True, valid sentences should correspond to necessary truths. The problem raised by (3.10), however, is a problem with $\mathbb{Q}$, not with strong necessity. For $\mathbb{Q}$ invites us to formalize the doubtful sentence "Homer exists" by the $\mathbb{Q}$-valid $\exists x \, x = \alpha$. Modify $\mathbb{Q}$ so that it is a free logic, and (3.11) will be, as it should be, true.

This raises deep issues about the role of names.$^{4}$ At the more superficial level, the strong version of necessity has the advantage noted of giving natural formalizations both of claims like *`(7)`* and claims like *`(9)`*, so I shall persist with it.

Any sentence formalizable as “$\square F\alpha$” can be read as ascribing a property to an object: it ascribes to $\alpha$ the property of being necessarily $F$. Sentences like (3) speak generally of things being Word necessarily thus-and-so. For a number of different reasons, philosophers have held that such ways of talking are illegitimate. If they are right, then it is bootless to investigate much further the properties of QN, since it is committed to this supposedly illegitimate way of talking.

### Ex. 5.14 Formalize the following in QN (omitting parenthetical material), commenting on the validity of your formalizations of (ii) and (iii):

(i) Causation is a necessary relation.

(ii) A necessary condition for the possibility of experience is that there are causally related events. So the existence of our experience establishes the necessity of the causal relation.

(iii) It is possible for my body to exist when I do not (e.g. after my death). Therefore I am not my body.

(iv) What is known must be true.

(v) A married man must be married to someone.

## 4 Necessity de re and de dicto

A sentence expresses "necessity de re" iff it is adequately QN-formalizable by a sentence in which there is a name-letter within the scope of some occurrence of box or if there is an occurrence of box within the scope of a quantifier. Let us say that a sentence expresses "necessity de dicto" just on condition that it expresses necessity but does not express necessity de re. The doubts alluded to at the end of the last section are doubts concerning the coherence of the notion of de re necessity.

As I have defined the difference between de re and de dicto necessity, it is simply a matter of scope. The definitions do not introduce two concepts of necessity. We could with our available resources make an exactly parallel distinction between "negation de re" and "negation de dicto", but the distinction would give no support to the thought that there are two distinct concepts of negation.

Ex. 5.15 Give a pair of examples to contrast "negation de re" with "negation de dicto".

Quine does not use the distinction between de re and de dicto given in §4. Rather, he identifies a de re statement by a claim of (4.1): it is one which ascribes a property to an object. However, a sentence judged by this last standard to be one of de re necessity is also de re by our official standard. If the premise of (1) ascribes the property of being necessarily greater than 7 to the number 9, then it is appropriately QN-formalizable as:

2) $\square F\alpha$

Here the name-letter "$\alpha$" falls within the scope of box; so we must follow Quine in counting it, and hence the first premise of *`(1)`*, de re.

We can also agree with Quine that an essentialist *may* view (1) as sound. The following formalization is QN-valid:

3) $\square F\alpha, \alpha = \beta; \square F\beta$

(The correspondence scheme is: "$F$" to "is greater than 7", "$\alpha$" to "9" and "$\beta$" to "the number of the planets").) The essentialist will allow that the premises are true upon an intended interpretation. So he must allow that the conclusion is also true upon an intended interpretation. So he should hold that the conclusion of (1) is true. Why does Quine say that it is false?

His ground is that there might not have been nine planets. If there had been only 5, then the number which numbers them would not have been greater than 7, let alone necessarily greater than 7. Although this is correct, it is not inconsistent with the truth upon an intended interpretation of the conclusion of (3). Let us see what an intended interpretation, $i$, assigns to "$\beta$", "$F$" and "$F\beta$" with respect to a world, $w$, at which there are just 5 planets. First, $i_{w}(\beta)$ is the very object that $i$ assigns to "$\beta$" with respect to the actual world, viz. the number 9 (assuming it belongs to $D^{w}$); $i_{w}(F)$ is the set of members of $D^{w}$ which, at $w$, are greater than 7. Thus 9 will be a member of $i_{w}(F)$, and so $i_{w}(F\beta)$ is T. That there are worlds in which there are only 5 planets is irrelevant to the truth of the conclusion of (1), as it will be understood by one who takes the argument to be formalizable by (3), and so valid.

## 7 Trans-world identity

Evaluating de re sentences by the interpretation rules of QN requires attention to the identity of objects at various possible worlds. The rule for interpreting name-letters requires an interpretation to assign the same object to any name-letter with respect to each world at which the object exists. Hence this rule already incorporates the notion of trans-world identity: an interpretation must settle which object in, say, $w$ is the object which it has assigned to "$\alpha$" with respect to some other world.

The assumption of trans-world identity also emerges in connection with de re quantifications. Compare

**`1)`** $\square \forall x Fx$

**`2)`** $\forall x \square Fx$

In interpreting (*`1)`*, a de dicto sentence, we do not have to consider how the entities at various worlds are related to the ones at the world of evaluation. For any interpretation, $i$, any world, $w$, any $n$-ary predicate, $F$, all we have to consider is whether all $n$-tuples formed from the members of $D^w$ (whatever they may be) belong to $i_w(F)$. In interpreting (*`2)`*, a de re sentence, with respect to $w$, we have to consider which objects from $D^w$ also belong to the domains of other worlds. Suppose the question is whether (*`2)`* is true upon an interpretation, $i$, with respect to a world $w$. Then it is as if the quantifier of (*`2)`* ranged just over $D^w$, since the interpretation rule for "$\forall$" makes the truth of (*`2)`* turn on the truth of "$\square F\alpha$" with respect to $\alpha$-variants of $i$ which assign something, say $o$, to $\alpha$ at $w$. Each of these variants has to determine, for each world, whether $o$ belongs to what it assigns to "$F$" at that world. So each variant has to trace $o$ through various worlds, and thus has to settle questions of "trans-world identity".

Imagine two types of atheistic views about God’s existence. They are both “soft” atheisms, in that they agree that although there is no God, there could have been one. One view is formalizable:

**`3)`** $\diamond \exists x Fx$

with "$F$" corresponding to "is omnipotent, benevolent etc." (here insert a complete list of the attributes appropriate to God). The other view is formalizable:

**`4)`** $\exists x \diamond Fx$

with the correspondence as before. The first view is de dicto: it is true upon an intended interpretation, $i$, with respect to $w$, iff for some world $w'$, $i_{w'}(F)$ has at least one member. The second view is de re: it is true upon an intended interpretation, $i$, with respect to $w$, iff for some $\alpha$-variant which assigns an object, say $o$, to $\alpha$ at $w$ verifies "$\diamond F\alpha$"; iff there is a world at which $o$ belongs to $i(F)$. So (*`4)`* corresponds to the claim that someone exists who could have been God. The interpretation will settle whether someone who exists at the world of evaluation, $w$, is God at some possibly distinct world, $w'$, so it involves trans-world identity.

**Ex. 5.20** (a) Say which of the sentences (7.3), (7.4) entails the other. (b) Suppose that there is a single domain of actual and possible objects, common to each world. Show that in this case (7.3) and (7.4) would be equivalent.

We must agree with Quine that de re sentences, as QN-formalized, involve trans-world identity. If Quine is right, trans-world identity is unintelligible, and so QN, and all languages adequately formalizable therein, would likewise be unintelligible.

The issue is metaphysical, not epistemic. How, if at all, we know, concerning a possible world, that it does or does not contain a given individual is not at issue. If there is a fact of the matter which we do not know, then de re modality is intelligible, but permits the expression of propositions whose truth values we do not know.

It seems as if the intelligibility of trans-world identity is ensured by the fact that we can introduce a counterfactual situation by referring to a particular object. We might say: envisage a situation in which Nixon tells the truth. If this introduces a possible situation at all, there seems no room for doubt about whether it is a situation in which Nixon exists. We have specified the situation in terms of an object in it (cf. Kripke [1972]). On the face of it, Nixon belongs to at least two worlds, the actual world and a world where he is honest. How can there be some hidden difficulty here?

A difficulty arises if one holds the following two theses: (i) the only legitimate specification of a possible world is purely qualitative; and (ii) a purely qualitative specification is insufficient to determine which actual individuals are present at a world. If the only facts which could determine trans-world identity, namely purely qualitative facts, fail to do so, then, of course, the trans-world identities are not determined. But theses (i) and (ii) are an unattractive combination. If you believe that all facts are determined by qualitative facts, then, fair enough, you will hold thesis (i); but, by the same token, you will reject thesis (ii). If you believe thesis (ii), then you have a reason to reject the view that all facts are determined by qualitative facts, and thus a reason not to agree that only qualitative specifications of worlds are legitimate.


That is the end of the discussion, unless we can find some arguments against the intelligibility of trans-world identity. I shall mention one, and briefly discuss another.

Lewis [1986a] has given a powerful argument, but it has two features which make it inappropriate for discussion here. First, it depends upon Lewis's preferred method of constructing non-actual worlds (as mereological sums of genuinely existing, though non-actual, spatiotemporally related things), and is therefore only available to one who is familiar with, and accepts, that construction. Secondly, it in no way impugns the intelligibility of de re modality, but simply justifies Lewis's preferred method of representing it.

The argument I shall briefly discuss is due to Quine. He compares trans-world identity with trans-moment identity:

> *Our cross-moment identification of bodies turned on continuity of displacement, distortion and chemical change. These considerations cannot be extended across worlds, because you can change anything to anything by easy stages through some connecting series of possible worlds. ([1976], p. 861)*

Quine is claiming that we can make sense of identity across moments, because this is determined by various kinds of continuity, but that we cannot make sense of identity across worlds, because it is not determined by anything. For example, this table on which I am writing, $\alpha_0$, could have been made of slightly different parts. So there is a world, $w_1$, and a $w_1$-object, $\alpha_1$, such that $\alpha_1$ is identical with $\alpha_0$ yet is made of slightly different parts. $\alpha_1$ could also have been made of slightly different parts. So there is a world, $w_2$, and a $w_2$-object, $\alpha_2$, such that $\alpha_2$ is identical with $\alpha_1$ but is made of slightly different parts. Continue this process through a hundred or a hundred million stages, making small variations to design as well as to parts, and you will end up with a submarine, or anything else you choose. So there are no limits on how something could be at another world. This is a reductio ad absurdum of the view that there are facts of the form: $\alpha$ at $w$ is the same object as $\beta$ at $w'$ and is distinct from $\gamma$ at $w'$.


Quine underplays the paradoxical nature of the argument upon which he relies. We do not happily accept that $\alpha_0$ could have been made of the parts that some remote successor in the series is made of. So we are not happy to accept that "anything can be changed into anything by easy stages". The reasoning is on a par with the reasoning that seems to force us to accept that a heap of sand can never be destroyed by one-by-one removal of grains (for taking away one grain can never turn a heap into a non-heap). The reasoning is powerful, yet we all know that there must be something wrong either with it or with the premises, for we all know that the conclusion is unacceptable.

He also underplays the problem-free nature of identity through time. There are well-known puzzles. For example, we are drawn to a continuity account of identity through time, as is shown by the fact that we allow that a ship that has been endlessly repaired over many years, in gentle stages, is the very same ship, even if in its later years it is composed of none of its original parts. In addition, we are drawn to a compositional account of identity through time, as shown by the fact that if we imagine a ship's parts being successively replaced, but the old parts kept and finally reassembled into a ship, we have some inclination (of varying strength depending upon context) to hold that this is really the original ship, the one bearing a continuity relation to the original being merely a replica.[11]

Finally, Quine seems to assume something that these sorts of cases themselves give one reason to doubt: namely, that relations like "could have been made of slightly different parts" are transitive.


Quine can indeed be justly read as presenting a believer in trans-world identity with a challenge to give a systematic account of it, but he cannot be said to have shown that it is any more incoherent than our talk of ships and heaps.

One way to take up the challenge has been proposed by Lewis. He does not, as I said, allow trans-world identity in the sense that Quine intends, though he does provide a substitute that is said to yield everything for which trans-world identity was needed, and is governed by fairly well-articulated principles. This theory is discussed in §9.

Kripke has suggested that some of the distrust of trans-world identity is fostered by a faulty picture: thinking of a possible world as like something viewed through the wrong end of a telescope. By contrast, he suggests, the question of whether Socrates could have been an alligator is not to be addressed by envisaging an alligator-infested world, and reviewing the individuals therein to “see” if one of them is Socrates. Rather, it is to be answered by connecting it with other questions, like: must an individual of a species be propagated by individuals of that species? Could anyone have had different parents (propagators) from the ones he actually had? Kripke seems to have in mind an epistemic version of the problem of trans-world identity. He is certainly right to say that possible worlds are not going to supply the answers to questions like the one about Socrates. Rather, worlds provide a way of expressing the answers, once found.

A version of the third thesis about de re modality mentioned in §4 is correct as applied to QN: QN-formalizations expressing de re necessity do involve, in their QN-interpretation, questions of trans-world identity. (We will see in §9 that there is an alternative approach.) We now very briefly consider the other two theses, *`(4.1)`* and *`(4.2)`*, viz.:

In ascribing de re necessity we attribute a property to a non-linguistic object; in ascribing de dicto necessity we attribute a property to a sentence.

A de re necessary truth records how things are in the world; a de dicto necessary truth records only linguistic facts.

De re necessity does indeed involve the ascription of properties to non-linguistic objects, but we have seen no reason at all to suppose that de dicto expressions of necessity attribute it to a sentence. It is a property of people that they are, necessarily, unmarried if bachelors. Likewise, though our discussion sits happily with the thought that a de re necessary truth records how things are in the world, we have seen no reason to suppose that a de dicto necessary truth is made true by linguistic facts. There is a prima facie case against any such view. As far as we have seen, the de re/de dicto distinction is merely one of scope, so that the very same concept of necessity is involved in both cases. Hence one would expect it to be true in both cases or neither that they are “made true by linguistic facts”.


## 8 “∀” for “☐”

The semantics for QN have been given in terms of possible worlds: “☐” is associated with universal quantification over worlds, “♀” with existential quantification. The connection suggests that we could have proceeded in a different way: instead of enriching Q with the non-truth functional sentence connectives, we could instead have enriched it with a further predicate constant, “W”, stipulating that every interpretation assigns to “W” the set of all possible worlds. Let us call the result of enriching Q in this way QW. We might then hope to express a QN-sentence of the form “☐ . . .” by a corresponding QW-sentence of the form “∀x(Wx→ . . . x . . .”). Let us refer to any approach on these lines as a quantifier treatment of necessity.

Intuitively, the idea is to exploit the equivalence between it being necessarily true that A and it being true at every possible world that A. As soon as we look at the details of QW, however, some difficulties arise. What, in QW, should correspond to the QN-sentence “☐p”? We cannot simply write

**`1)`** $\forall x(Wx \to p).$

This severs the connection between “p” and the possible worlds: the idea was to say that “p” is true at each possible world. There are a number of different tacks one might take, of which I shall consider only two. In both cases, the base language (corresponding to our Q) is envisaged to have no sentence-letters, so let us imagine that modification of Q to have been made. Our original problem emerges in the same way if we ask: how should we fill the dots in

“∀x(Wx→...x...)” when formalizing what in QN is formalized as “□Fα”?

The first suggestion I shall call the “extra argument place” treatment. Suppose we are to formalize

**`2)`** Socrates is necessarily human.

The proposal is that we use

**`3)`** $\forall x(Wx \to F'\alpha x)$

where “F′xy” corresponds, not to “human”, but to “x is human at y”. On an intended QW-interpretation, “F′” will be assigned the set of ordered pairs σ such that, for each world, w, and each object o in w, <o,u> belongs to σ just on condition that o is human at w.

The idea can be generalized. Every n-ary predicate in an English necessitation will be formalized by an n+1-ary predicate-letter of QW, the extra argument place being filled by a variable bound by a quantifier in the phrase “∀x(Wx→...x...)”.

This approach provides an extensional treatment of modality. The extensionality of QW follows from the fact that its semantics are in essentials those of Q: the interpretation rules attend only to the extensions of expressions. Apparent evidence of non-extensionality disappears. Consider the invalidity of the argument:

**`4)`** Necessarily Socrates is human;

Socrates is human iff Socrates is snub-nosed.

Therefore necessarily, Socrates is snub-nosed.

(*`4)`* is evidence for non-extensionality only if we can construe the first premise as consisting in the application of a sentence connective to a sentence. On the extra argument place treatment, the premise is not construed in this way, but rather as having the logical form of (*`3)`* in which there is no sentential component. The invalidity of (*`4)`*, as formalized in QW on the extra argument place approach, is quite consistent with QW’s extensionality.

Ex. 5.21 Provide a QW-formalization of (8.*`4)`*, showing your correspondence scheme.</o,u>

The approach provides a vivid example of how proposed logical forms may differ from the way a sentence would intuitively be supposed to be constructed. The divergence will hinder **QW** in formalizing as valid intuitively valid arguments. For example, intuitively the following argument is valid:

**`5)`** Necessarily Socrates is human. Therefore Socrates is human.

The present **QW** approach cannot, on the face of it, even discern a common constituent in premise and conclusion corresponding to “Socrates is human”. “Human” in the premise has to be matched with a 2-place predicate letter, whereas in the conclusion it will, for all that has been said, be matched with a 1-place one.

**Ex. 5.22** Provide a **QW**-formalization of (8.5), showing your correspondence scheme. Assuming that **QW** uses the standard notion of validity (paralleling **PN**- and **QN**-validity), is your formalization **QW**-valid?

To remedy this, we could use a 2-place predicate-letter in formalizing the conclusion, filling the additional argument place by a name for the actual world. Another remedy would be to use “/” to mark a special semantic relation between predicate letters, the interpretations being constrained to behave according to the following rule: if an interpretation assigns to “F” the set of all things meeting a condition, C, then it must assign to “F/” the set of all ordered pairs <o,w> such that o meets condition C with respect to w.

**Ex. 5.23** Evaluate the following argument against the suggestion that we should formalize apparently 1-place predicates, like “green”, by 2-place ones:

If we transform “x is green” to “x is green at w*” (where “w*” rigidly names the actual world) we will get the wrong results, for something green will be green-at-w* with respect to every world at which it exists, but will not be green with respect to every such world.

The extra argument place treatment takes all of a thing’s properties as really relations between it and a world. You may think that this page</o,w> has the intrinsic property of being rectangular, but on the proposed treatment, we have to say that there is no such intrinsic property. To permit QW-formalization of, say,

**`6)`** This page is rectangular

we regard it as abbreviating something like

**`7)`** This page is rectangular-at-w

where the relevant world $w$ is contextually determined (presumably as the actual world in a self-standing utterance of (*`6)`*). Lewis has criticized this implicit repudiation of intrinsic properties as unjustified. Being white or rectangular are properties which objects have in themselves, and are not relations the objects bear to other things.

EX. 5.24 Evaluate the following response on behalf of the extra argument place account:

On my view, to say that rectangularity is a property this page has "in itself" is simply to say that it is a 2-place property of this page: a property the possession of which relates this page to only one other object, a world. A relational property of this page is one which is more than 2-place.

An alternative way to implement a quantifier approach to modality uses what I shall call "open-sentence formers" (cf. Lewis [1968, 1986a]). Lewis begins by suggesting that a phrase like "In Australia . . ." can be seen as a 1-place sentence operator which works by restricting the quantifiers in what follows. To evaluate

**`8)`** In Australia, all beer is good

one need attend only to a proper subset of all the beer there is, viz. that which is in Australia. A phrase like "At the actual world . . ." functions in a similar way, so that an affirmation of

**`9)`** At the actual world, all beer is good

is perfectly intelligible, and avoids commitment to the goodness of non-actual beer. (Compare: "As things are, all beer is good; but had the proposed Trans-National Brewery come into being, this would not have been so.")


Lewis's suggestion is that a phrase like "at $v$", where "$v$" is a variable ranging over possible worlds, can function in a similar way to "in Australia" and "at the actual world". The main difference is that such a phrase contains a variable of quantification that can fall in the scope of a quantifier, as in

**`10)`** $\forall x(\text{at } x(p))$.

Syntactically, "at $x$" forms from "$p$" an open sentence "at $x(p)$", and hence something from which a quantifier can form a closed sentence. I call any phrase "at $v$" ($v$ any variable) an "open-sentence former": it takes a sentence, open or closed, to make an open sentence. Semantically, the basic idea is that "at $x(p)$" is true iff $p$ is true with respect to $x$ (a condition which will fail if $x$ is not a world).

Let us take the syntax of QW to be enriched by the addition of the open-sentence former "at". How should the interpretation rules be modified? All QW-interpretations must be relativized to worlds: a sentence like "at $\alpha(p)$", which will be involved in interpreting a sentence which quantifies over worlds (assuming we leave the quantifier rules unchanged), should be true upon an interpretation iff "$p$" is true upon an interpretation with respect to whatever the interpretation assigns to "$\alpha$".

To be true to Lewis's ideas, we cannot simply take over the QW-interpretation rules as they stand. Lewis wants quantifiers to range over absolutely everything there is, and he takes this to include non-actual objects as well as actual ones. Thus he takes there to be a reading of

**`11)`** There are talking donkeys

upon which it is true (with respect to the actual world): a reading which treats the quantifier as ranging over everything, actual and possible (cf. §11 below). Context can implicitly restrict or derestrict quantifiers, and the same can be done explicitly by the "at $v$" operators. Lewis sees the effect of replacing "are" by "could be" in (*`11)`* as that of unambiguously ensuring that the quantifier will be completely unrestricted, and thus range over non-actual as well as actual objects.

One way to implement this idea within the present framework is to use two styles of variables and name-letters, one style for quantification restricted by some "at $\nu$" operator, and another for unrestricted quantification. A variable of quantification, say "$x$", occurring within the immediate scope$^{12}$ of an "at $\nu$" operator needs to be thought of as quantifying over objects in the world assigned to "$\nu$". Hence one style of name-letter replacing variables like "$x$" for the purposes of interpretation requires a corresponding relativity: the interpretation must assign it something in the world assigned to "$\nu$". Unrestricted quantifiers are thought of as quantifying over the totality of actual and non-actual objects (including the actual and all non-actual worlds). A corresponding distinct style of name-letter can be used, and to such a name-letter an interpretation is free to assign anything from any world. The quantifier rules will need to use name-letters of the unrestricted sort to mark positions occupied by variables whose quantifier does not fall in the scope of any "at $\nu$" operator, and name-letters of the restricted sort to mark positions occupied by variables whose quantifier does fall within the scope of an "at $\nu$" operator. The full details are not necessary for present purposes. The general idea is that "at $n$, $X$" is true upon an interpretation, $i$, with respect to a world, $w$, iff $X$ is true upon $i$ with respect to whatever $i$ assigns to "$n$".

In Q, and therefore in QW, the order of quantifiers of the same sort is irrelevant. For example, the prefixes "$\exists x \exists y$" and "$\exists y \exists x$" are equivalent. But "$\exists x \lozenge$" and "$\lozenge \exists x$" are far from equivalent prefixes, the first expressing possibility de re, the second de dicto. (Compare *`(7.3)`* and *`(7.4)`*.)

The difference is not brought out in QW by the following pair of formalizations:

**`12)`** $\exists x \exists y (W y \land \text{at } y (\ldots x \ldots))$

**`13)`** $\exists y \exists x (W y \land \text{at } y (\ldots x \ldots))$

for these are equivalent. Rather, Lewis will see the de re English phrase "there is something which could be . . ." as involving an implicit restriction of the quantifier to the actual world. To bring this out in $\mathbf{QW}$, we can add a name for the actual world, say "$w^*$". (The rule will be that every interpretation, with respect to every world, $w$, assigns the actual world to "$w^*$". "At $w^*$" thus forms closed sentences from closed sentences.) The de re sentence could be formalized:

**`14)`** $$\exists x(\text{at } w^*(\exists y y = x) \land \exists y(Wy \land (\text{at } y(\ldots x \ldots))))$$

(*`12)`* or (*`13)`* serve to formalize the de dicto sentence. The de re/de dicto distinction is not submerged.

$\mathbf{QW}$ (henceforth understood in its open-sentence former version) and $\mathbf{QN}$ use pretty similar semantic resources, despite their syntactic differences. For example, in the semantics for $\mathbf{QN}$ there is quantification over worlds, including non-actual worlds, and their domains, including domains containing non-actual objects. Is there any reason to prefer one of these languages to the other?

One might initially be tempted to suppose that there could be little to choose between the languages. However, Lewis has argued that $\mathbf{QW}$ has greater expressive resources than $\mathbf{QN}$, revealed in the greater depth of the formalizations of English the former can provide.

As $\mathbf{QN}$ and $\mathbf{QW}$ stand, it is true that the expressive resources of the latter outstrip the former. One reason for this is connected with the addition made to $\mathbf{QW}$ of the name "$w^*$". There is no corresponding device in $\mathbf{QN}$. The difference can be brought out by considering the following sentence.

**`15)`** It is possible that everything that is actually red should also have been shiny.

This is formalizable in $\mathbf{QW}$ as

**`16)`** $$\exists x(Wx \land \forall y(\text{at } w^*(Fy) \rightarrow \text{at } x(Gy)))$$

with "$F$" corresponding to "is red" and "$G$" to "is red and shiny". However, (*`15)`* cannot be adequately $\mathbf{QN}$-formalized as either of

**`17)`** $$\forall x(Fx \rightarrow \Diamond Gx)$$

**`18)`** $$\Diamond \forall x(Fx \rightarrow Gx)$$

with correspondences as before.

Ex. 5.25 Show how the truth-upon-an-intended-interpretation conditions of (8.*`17)`* and (8.*`18)`* differ from the truth conditions of (8.*`15)`*. (See Davies [1981], pp. 220–1.)

A suitable supplementation of QN that keeps to the sentence connective approach to modality, and does for QN something like what “w*” does for QW, is a one-place sentence connective, say “A” and the interpretation rule:

**`19)`** For any interpretation, $i$, any world, $w$, $i_w(\mathsf{A}X)$ is T iff $X$ is true upon $i$ with respect to the actual world.

One should then QN-formalize (*`15)`* as

**`20)`** $\diamondsuit \forall x(\mathsf{A}Fx \to Gx)$.¹³

The claim that there are non-actual objects can be QN-formalized as

**`21)`** $\exists x(\diamondsuit \exists y(y = x) \land \neg\mathsf{A}\exists y(y = x)),$

or QW-formalized as

**`22)`** $\exists x\exists y(\mathsf{W}y \land \text{at } y(\exists z(z = x)) \land \text{at } w^*(\neg\exists z(z = x))).$

If we build in to our definition of QW-interpretation that there are non-actual objects, then (*`22)`* will come out as QW-valid; otherwise not. Similarly, one has a choice whether or not so to engineer the interpretation rules of QN, in particular one’s account of the worlds and their domains, as to make (*`21)`* valid, or even to make its negation valid. A common prejudice among logicians would be to prefer neutrality on this issue, which might well be seen to belong to “metaphysics”.

Lewis gives various examples of natural claims formalizable in QW but allegedly not formalizable (to any reasonable depth) in QN. If even one allegation is correct, this would constitute a powerful reason for preferring QW. I shall consider three of the examples.

**`23)`** It might happen in three different ways that a donkey talks.

In this example, we appear to talk of, indeed count, various different possibilities. These, says Lewis, can be represented by possible worlds, but not by boxes and diamonds. (*`23)`* is QW-formalizable as

**`24)`** $\exists x\exists y\exists z(\mathsf{W}x \land \mathsf{W}y \land \mathsf{W}z \land x \neq y \land x \neq z \land y \neq z \land \text{at } x(\exists vFv) \land \text{at } y(\exists vFv) \land \text{at } z(\exists vFv))$

with “$F$” corresponding to “is a talking donkey”. One might doubt if this is entirely adequate, since the differences between the worlds might be ones irrelevant to the way a donkey talked, whereas intuitively what is required for the truth of (*`23)`* is, for example, that a donkey might be made to talk by special training, or by the injection of a chemical, or by genetic engineering. However, it may seem that in QN one cannot get even as close as this, since there would seem to be no way in which numeral adjectives can be conjured out of boxes and diamonds.

In fact, one can use resources going at most a very little beyond QN to produce a formalization of (*`23)`* that rivals (*`24)`*. The idea is to understand the English as saying that there are three different properties a donkey could have, and a possessor of any of these properties is talker. I shall treat the quantification over properties in the way that includes predicate quantification within a first order language, and so minimizes alterations to QN (compare the discussion surrounding .19.4): I shall assume that properties are among the objects in some (or all) domains of interpretation. A QN-formalization is

**`25)`** $\exists x\exists y\exists z(Fx \land Fy \land Fz \land x\neq y \land x\neq z \land y\neq z \land \square \forall v(Gvx \to Hv) \land \square \forall v(Gvy\to Hv) \land \square \forall v(Gvz\to Hv) \land \diamondsuit \exists v(Jv \land Gvx) \land \diamondsuit \exists v(Jv \land Gvy) \land \diamondsuit \exists v(Jv \land Gvz))$

with “$F$” corresponding to “is a property”, “$Gxy$” to “$x$ possesses (the property) $y$”, “$H$” to “talks” and “$J$” to “is a donkey”. (*`25)`* is better than (*`24)`*, since it connects the different ways with different ways of being a talker. It may not be perfect, since the connections between having any one of the properties and being a talker are rather weak, but the fact remains that we have yet to find any expressive superiority of QW over QN.

This suggestion, like some later ones, could be criticized for its treating properties as among the individuals. This treatment would be wrong if there are no properties. Using this reply as part of a case for preferring QW to QN (as opposed to a case simply against QN) would depend on showing that, though properties do not exist, non-actual worlds do. This would form a controversial basis for a preference for QW. A separate point is that the main feature of the suggestion which led to (*`25)`* would be retained if properties were replaced by sets.

Another example which Lewis uses to ground a preference for QW is

**`26)`** A red thing could resemble an orange thing more closely than a red thing could resemble a blue thing.

A possible QN-formalization is

**`27)`** $\diamondsuit \exists x \exists y \exists z \exists v (Fx \land Gy \land Fv \land Hz \land Jxyvz)$

with “F”, “G” and “H” corresponding to the three colour predicates “red”, “orange” and “blue”, and “Jxyvz” to “x resembles y more than v resembles z”. Lewis objects that (*`27)`* wrongly requires there to be a single world containing all the objects, whereas it is enough for the truth of (*`26)`* that there be two worlds, one containing one pair, another the other. Lewis sums up his case by saying that English essentially involves cross-world comparisons of similarity. His account of (*`26)`* would suggest the formalization

**`28)`** $\exists x \exists y \exists z \exists v (Fx \land Gy \land Fv \land Hz \land Jxyvz),$

the force of the English “could” being reflected simply in the fact that the quantifiers are quite unrestricted, each ranging over the totality of actual and non-actual objects.

There is certainly a formal difference between the claim that there could be things $x, y, z, v$, such that . . . and the claim that there could be things $x, y$ and there could be things $z, v$, such that. . . . We could imagine worlds in which the very presence of a red and an orange thing ensures that there is no blue thing, thus preventing the “all in one world” comparison. This would not lead to a conflict with the intuitive truth of (*`26)`*, which requires only one world in which all three colours are exemplified. If there is a world with a closely similar red-orange pair, and a world with a less closely similar red-blue pair, then surely there is some world where both pairs co-exist. (Indeed, this conclusion apparently follows from Lewis's own principles determining what worlds exist.) So it is still not clear that there are sentences of idiomatic English whose truth is differentially sensitive to the distinction Lewis makes between within-a-world and cross-world comparisons.


Ex. 5.26 Give the best formalization of the following in (a) QN and (b) QW:

My car could have been the same colour as yours actually is.

See Forbes [1985], p. 92.

A kind of example upon which Lewis places a good deal of weight are supervenience claims. These have the general form:

**`29)`** There could be no differences of one sort without differences of another sort.

A specific supervenience claim is that the mental supervenes upon the physical. In Lewis's words:

> *The idea is that the mental supervenes on the physical . . . [i.e.] there could be no mental difference between two people without there being some physical difference, whether intrinsic or extrinsic. Reading the "could" as a diamond, the thesis becomes this: there is no world . . . wherein two people differ mentally without there being some physical difference, whether intrinsic or extrinsic, between them. That is not quite right. We have gratuitously limited our attention to physical differences between two people in the same world, and that means ignoring those extrinsic differences that only ever arise between people in different worlds. ([1986a], p. 16)*

"Reading the 'could' as a diamond" goes over into my terminology as "supposing that the English is QN-formalizable".

There is no doubt that QW can express things which cannot be expressed in QN. In QW there is explicit quantification over worlds, and resources to count and differentiate distinct possibilities, and these are not explicitly available in QN. It may well be that for some philosophical discussions, about essence, origin and substance, for example, these resources are essential. However, the question I am raising here is whether they are required in the understanding of ordinary idiomatic English sentences and our intuitive judgements of whether these are true or false. The ordinary sentences are the neutral territory. The competing theorists are to formalize these in the languages QW or QN. If the truth-upon-an-intended-interpretation value of one of the theorist's formalizations does not match that of the English sentence (according to our intuitive judgements), that theorist loses a point. (He might regain it if he can convince his opponent that our intuitive judgements are faulty.)


The paragraph quoted from Lewis should identify some feature of the neutral territory not matched by a QN-formalization: a mismatch between the truth value of the English and the truth-upon-an-intended-interpretation value of the QN-sentence. What we in fact discover is some remarks couched in the non-neutral idioms of Lewis's preferred account, including reference to special features that he attributes to worlds. For example, on his construction of worlds, a person in a Riemannian spacetime cannot inhabit the same world as a person in a Lobachevskian spacetime. Such details, however, do not belong to the neutral territory. Only within the framework for which Lewis is arguing is there a gratuitous limitation of attention in the QN approach.

One might base a QN-formalization of the supervenience of the mental upon the physical upon the idea that the claim amounts to: necessarily, any things differing in mental properties necessarily differ also in physical ones. This suggests

**`30)`** $$\square\forall x\square\forall y\square(\exists z(Mz \land Fxz \land \neg Fyz) \rightarrow \exists z(Pz \land Fxz \land \neg Fyz)),$$

where “M” corresponds to “is a mental property” “Fxy” to “x possesses (the property) y” and “P” to “is a physical property”. This appears to be no weaker than the English.

Lewis allows that the alleged failure of QN with respect to this case makes little odds, but he suggests that it is more serious with respect to another, structurally similar, thesis, the supervenience of laws. The thesis is that two worlds could not differ in their laws without also differing in local qualitative character. Here is the supposed problem with QN-formalization:


> *if we read the "could" as a diamond, the thesis in question turns into this: it is not the case that, possibly, two worlds differ in their laws without differing in their distribution of local qualitative character. That's trivial – there is no world wherein two worlds do anything. At any one world W, there is only the single world W. ([1986a], p. 16)*

"World" here is playing two roles which should be kept distinct. One role is the special one which Lewis is developing and defending in his book: a world, in this technical sense, is the sort or thing quantification over which will be said to translate English modal idioms. As we might put it in our terminology: it is open to the defender of the expressive advantages of QW to add whatever further constraints he feels are necessary to his interpretation rule for "W". In the technical sense, it is certainly correct for Lewis to say: "At any one world w, there is only the single world w", for on his construction, for all worlds w, the only world which exists at w is w.

The other role for "world" is non-technical, and it cannot be taken for granted that any Lewisian thesis holds with respect to it. The non-technical sense is that used in stating the thesis that two worlds could not differ in their laws without also differing in local qualitative character. A suitable QN-formalization is:

**`31)`** $$\square \forall x\square \forall y\square ((Gx \land Gy) \rightarrow (\exists z(Mz \land Fxz \land \neg Fyz) \rightarrow \exists z(Pz \land Hxz \land \neg Hyz))),$$

with "G" corresponding to "is a (non-technical) world", "M" to "is a law", "Fxy" to "x is governed by y", "P" to "is a local qualitative property" and "Hxy" to "x possesses (the property) y". No doubt a full appreciation of this thesis will require a more detailed understanding of what sort of entity will be assigned to "G" upon an intended interpretation. But (i) one must not assume that these entities are the possible worlds used in giving the semantics for QN; and (ii) a formalization can be entirely adequate even if it gives no analysis of the concepts employed. (One does not criticize the Q-formalization of "Socrates is human" as “Fα” on the grounds that it offers no analysis of the concept of humanity.) (*`31)`* is far from trivial: there are endless interpretations upon which it is false.


While we have not yet encountered an ordinary English sentence better formalizable in QW than in QN, it is certainly true that the expressive resources of QW outstrip those of QN. The existence of the predicate constant, “W”, in QW but not QN, is enough to establish this. (For example, “There are worlds” is adequately formalizable as QW-valid, but not as QN-valid.) Further, a QW-sentence like

**`32)`** $$\exists w\mathsf{W}w \land \forall w^{\prime}(\mathsf{W}w^{\prime} \rightarrow \forall z(\text{at } w^{\prime}(\exists y\ y=z) \rightarrow \text{at } w(\exists y\ y=z)))$$

corresponds to an important claim about the structure of worlds (that some world contains all possible and actual individuals), yet has no obvious QN-correlate. (Cf. Hazen [1976]; Forbes [1985], pp. 90–1.)

**`33)`** $$\diamondsuit\forall x(\diamondsuit\exists y\ y=x \rightarrow \exists y\ y=x)$$

is not an adequate formalization, for it corresponds to the trivial claim that it is possible for all possible existents to exist.

One way to progress is to introduce a device which will enable “A” to refer back to what would have been actual if the possibility introduced by “$\diamondsuit$” were realized. We can achieve this effect in QN by indexing the operators. A$X$ will, by default, be true on an interpretation, $i$, with respect to a world, $w$, iff $X$ is true upon $i$ with respect to the actual world; but if it is indexed and occurs in the scope of an operator with the same index, A$_{i}X$ will be true upon an interpretation, $i$, with respect to any world, $w$, iff $X$ is true upon $i$ with respect to $w^{\prime}$, where $w^{\prime}$ is the world introduced, according to the semantics, by the previous $n$-indexed operator (cf. Forbes [1985], p. 91, n. 28 for a more accurate specification). Using this device, what corresponds to (*`32)`* is:

**`34)`** $$\diamondsuit_{1}\forall x(\diamondsuit\exists y\ y=x \rightarrow \underline{A}_{1}\exists y\ y=x).$$

The interpretation of “$\underline{A}_{1}$” will pick up the variable attached to the existential quantifier introduced, by the interpretation rules, in the interpretation of “$\diamondsuit_{1}$”.

These considerations suggest that the framework of QN can be extended to increase expressive power. Two questions remain: would there be any point in making these additions to QN, given the availability of QW? And do these additions keep to the spirit, as well as the letter, of the operator account?

The most promising basis for a positive answer to the first question is that there is a case for saying that QN but not QW can avoid committing itself to non-actual objects, for example, non-actual worlds. This view will be considered in §11.

In answer to the second question, a distinctive feature of quantification is the possibility of back reference that can be achieved by associating quantifiers with variables. If this feature is simply being mirrored by indexing, then it looks as if indexed operators are really quantifiers in all but name. What is certain is that the indexed operators are explicitly linked, by the envisaged rules of interpretation, to variables of quantification. It is natural to conclude that unless these rules mislead, the indices function as variables. If this conclusion is justified, then it would seem that we could also conclude that even the unindexed operators are "really" quantifiers over worlds. The proponent of the suggestion just mentioned, that QN can avoid commitment to non-actual entities, will need to speak to this question (see §11).

## 9 Counterpart theory

Lewis's quantifier treatment of modal operators is combined with another distinctive, but theoretically separable, view. He holds (for reasons we will not consider) that nothing exists at more than one world. If no changes were made in QW, this doctrine would imply that all de re ascriptions of possibility are false. If Socrates, for example, exists only in our world, there is no world in which he is foolish: he is not foolish at our world, and he does not exist at any other. If we formalized

**`1)`** Socrates might have been foolish

in the QW style of

**`2)`** $\exists w \text{ at } w(F\alpha)$

we would formalize a truth as a falsehood.

Lewis proposes that de re modalities address the question not of how actual objects are in other worlds, but how their counterparts are. A counterpart of an object, $o$, at a world is something than which nothing in the world resembles $o$ more closely. To say that Socrates might have been foolish is to say that some counterpart of Socrates is foolish: something very like Socrates, or at any rate more like Socrates than anything else in its world, is foolish. “Something” quantifies over all actual and possible objects. Using “$C$” to express the counterpart relation, (1) is formalized:

**`3)`** $\exists x(Cx\alpha \land Fx)$

with “$\alpha$” corresponding to “Socrates” and “$F$” to “foolish”. Likewise

**`4)`** Socrates is necessarily human

is formalized

**`5)`** $\forall x(Cx\alpha \rightarrow Fx).$

Because each counterpart determines a world, we have no need to use the “at $w$” idiom in these formalizations. We do need to use it in other cases, for example in the formalization of

**`6)`** 9 is a necessary existent

which could become

**`7)`** $\exists y\forall w \text{ at } w(y = \alpha)$

with “$\alpha$” corresponding to “9”. Let us call QC the language which results from adding “$C$” to QW.

Ex. 5.27 Provide QC-formalizations of:

**`(i)`** Socrates is a contingent being.

**`(ii)`** All mathematicians must be mathematicians. (Bring out the possible ambiguity by providing two formalizations of this sentence, one de re and the other de dicto.)

It has been objected to counterpart theory that it fails to represent de re modality as about the right “rem” or thing (cf. Kripke [1972], p. 344n; Plantinga [1974], pp. 115–16; for a criticism, see Hazen [1979]). When we say that Socrates might have been foolish, we mean to speak of Socrates himself, and predicate possible folly of him rather than of someone else who is similar to him. Lewis [1986a] replies, entirely justly, that (*`3)`*, for example, is about Socrates, and attributes possible folly to him by means of saying that he has a foolish counterpart. To the counterpart it attributes not possible folly, but folly.

Lewis explicitly allows an object in one world to have two counterparts at another. (If this were not allowed, one might wonder whether the counterpart relation differed from identity.) He is committed to this view by founding the counterpart relation upon overall similarity. A red circle and a red square are similar in one respect, and a red circle and a blue circle in another. There is no absolute fact about which other things the red circle is more similar to. This feature of similarity is not exclusive to counterpart theory: it is recorded in the consistency of such mundane beliefs as “x and y are very alike, and also very different”.

Lewis can appeal to different respects of similarity to ward off another objection. Plantinga has claimed that, intuitively, Socrates could have been very much like Xenophon actually is, and Xenophon could have been very much like Socrates actually is. We can envisage a situation in which extreme versions of these possibilities both obtain: a world in which Socrates is just like Xenophon actually is and Xenophon is just like Socrates actually is. Suppose we make “F” correspond to some predicate which gives a reasonably comprehensive account of Socrates’s features (those that Xenophon would have to possess to be “just like” Socrates), and “G” to some predicate which does the same for Xenophon’s features. Then, according to the objection,

**`8)`** $\diamond(G\alpha \land F\beta)$,

with “α” corresponding to “Socrates” and “β” to “Xenophon”, is true whereas a QC-formalization is false: since counterparts are determined by similarity, the possessor of the features associated with “G” must be a counterpart of Xenophon and not of Socrates, and the possessor of

the features associated with “$F$” must be a counterpart of Socrates and not of Xenophon.

Lewis replies that the features which Plantinga has in mind, corresponding to $F$ and $G$, are only some among the similarities that can obtain between people in different worlds. Perhaps they are features of appearance, character and life history. But there are ways in which Socrates can resemble someone who is very different in appearance etc., for example by having similar genes and similar parentage. When we think of Plantinga’s situation, we hold these similarities constant, and these are what can sustain a suitable counterpart relation.

Relational possibilities, like

**`9)`** Oxford might not have been north of London,

have a single formalization within QN ($\diamondsuit \neg G\alpha\beta$) but there are three possibilities within QC, depending on which name introduces a counterpart, or whether both do:

**`10)`** $\exists x(Cx\alpha \land \neg Gx\beta)$

**`11)`** $\exists x(Cx\beta \land \neg G\alpha x)$

**`12)`** $\exists x\exists y(Cx\alpha \land Cy\beta \land \neg Gxy)$.

Since the counterpart relation is reflexive, each of the first two entails the third. When the topic is a relation like “north of”, which, according to Lewis, cannot hold between objects at different worlds, the distinctions between (*`10)`*–(*`12)`* correspond to no difference of substance. This may not be the case when the topic is interworld relations like non-identity: relations which can in principle hold between objects which belong to different worlds.

In QN, identity is a necessary relation, which implies that

**`13)`** $\alpha = \beta \land \diamondsuit \alpha \neq \beta$

is false upon every QN-interpretation, with respect to every world. One QC-formalization of (*`13)`*, modelled on (*`12)`*, is

**`14)`** $\alpha = \beta \land \exists x\exists y(Cx\alpha \land Cy\beta \land x \neq y)$.

Suppose that $\alpha = \beta$ and that, as Lewis allows is possible, $\alpha$ has more than one counterpart at some world: two objects both satisfy the condition that nothing at that world is more similar to $\alpha$ than they are. Then (*`14)`* is true. So there is a conflict between QN and QC.

Lewis ([1986a], ch. 4.5) holds that the conflict tells in favour of QN: identity is contingent, in the sense that there are truths of the form of (*`13)`* and (*`14)`*. For example, consider a plastic utensils factory. The various utensils are manufactured by filling moulds with the precursors of plastics. The plastic itself is synthesized in the mould, so there is no gap between a certain lump of plastic coming into being, and some plastic utensil coming into being. Suppose a bowl made in this way is incinerated a few days later, so that both it and the lump of plastic are destroyed. At every moment of time, both or neither the bowl and the lump of plastic exist, and when they exist, they do so in the same place, weigh the same, and so forth. This gives us reason to hold that the bowl is the lump of plastic, so the first conjunct of (*`13)`* is true. However, it is possible that the factory should have received a different order that morning. Suppose the precursors were already divided up into utensil-sized heaps, and that the heap which in fact became the bowl was instead made into a waste-basket. Suppose that the mould from which the bowl was made went unused that day, but was used on the next day to make a bowl (a bowl, say, fulfilling the special order which our actual bowl fulfilled, so we can properly speak of the bowl). The possibility we are describing appears to be one in which the original bowl and the original lump of plastic both exist, but are distinct, the lump of plastic being a different utensil, a waste-basket, and the bowl being a different lump of plastic. If so, this will make the second conjunct of (*`13)`* true.

In Lewis's scheme, what makes the waste-basket a counterpart of the original bowl is that it is made out of the same stuff; what makes the other bowl a counterpart of the original bowl is that both fulfilled the same order, were made in the same mould, and were the $n^{\text{th}}$ bowl to be made by the factory. There are different dimensions of similarity, and this is one way in which there can be more than one counterpart.

This position might seem inconsistent with Leibniz's Law, which can be used to mount an argument for the necessity of identity, the claim that there are no truths of the form of (*`13)`*.

**`15)`** (i) Leibniz's Law: identicals have all their properties in common. More formally, every instance of the following (obtained by replacing “$\Pi$” by any predicate) is true: $\forall x\forall y(x = y \rightarrow (\Pi x \rightarrow \Pi y))$.

(ii) $\forall x \square x = x$ (assumption).

(iii) $\forall x \forall y(x = y \rightarrow (\square x = x \rightarrow \square x = y))$ (from (i), replacing “$\Pi$” by “$\square x =$” (the predicate ascribing the property of being necessarily identical to $x$)).

**`(iv)`** $\forall x \forall y(x = y \rightarrow \square x = y)$ from (ii) and (iii).

This appears to establish quite generally that identicals are necessarily identical. (Cf. Barcan [1947]; also Wiggins [1980b], pp. 109–11 and 214–17.)

In material added to his [1968], Lewis objects to step *`(15iii)`*: he denies that Leibniz's Law is correctly applied. He holds, in effect, that there is no unequivocal property being necessarily identical to $x$ applicable now to $x$, now to $y$. The justification for this emerges from the counterpart-theoretic representation of *`(15iii)`*. A necessitated relational expression, which would be represented in QN as

16) $$\square R\alpha\beta$$

Applying this to (iii) yields:

18) $$\forall x \forall y(x = y \rightarrow (\forall z((Czx \rightarrow z = z) \rightarrow \forall z'((Czx \land Cz'y) \rightarrow z = z'))))$$

On its first occurrence, “Πζ” (I use “ζ” to mark the gap in the predicate, the position to be filled by a name or variable) is replaced by

19) $$\forall z(Cz\zeta \rightarrow z = z)$$

On its second occurrence it is replaced by

20) $$\forall z'((Cz\zeta \land Cz'y) \rightarrow z = z')$$

<span class="mathjax_ignore">Since (19) and (20) are distinct, (iii) is not an instance of Leibniz's Law. This suggests that the argument of (15) cannot be used as a basis for rejecting counterpart theory. The defence needs some amplification: to accept the formalization of (16) as (17) we would need to be convinced that there are no cases in which objects have very few counterparts, so that (17) holds even when the objects are not necessarily &#36;R&#36;-related. Any qualms on this score can be set to rest by the formalization</span>

**`21)`** $$\forall w \text{ at } w \exists x \exists y(Cxa \land Cy\beta \land Rxy)$$

This would not affect the point that the application of Leibniz's Law envisaged in (*`15)`* is counterpart-theoretically invalid.

**Ex. 5.28** Discuss from the point of view of counterpart theory whether there is a pair of distinct objects which are necessarily distinct.

Counterpart theory offers rich expressive possibilities. It arises from a metaphysical position, the view that no object can exist at more than one world. From a strictly logical point of view, it cannot be criticized, for its syntax and semantics are essentially that of Q. Doubts about counterpart theory arise not from logic but from metaphysics: to lovers of desert landscapes, there is no appeal in an ontology which includes genuinely existing but non-actual worlds and inhabitants thereof.

## 10 Necessity and vagueness

Vagueness gives rise to borderline cases. Think, for example, of a colour spectrum. There are clear cases of red and clear cases of orange, and in between there are borderline cases: shades which we don't feel inclined to classify either as red or as orange. This feature of vagueness has its analogue in the case of the possible original constitution of artefacts. There are clear cases of possible differences in a thing's original parts; clear cases of impossible differences; and, in between, cases about which we don't know what to say.

It is natural to suppose that, if an area on the spectrum is red, then if you move a tiny distance in either direction, the area you get to must be red too; but if you move a large distance the area may not be red. In other words, a small difference does not matter to the correctness of applying "red" but a large difference does. The first fact amounts to what has been called a "tolerance principle": if two objects differ minutely in shade, then the predicate "red" applies to both or neither. This principle is in tension with the fact that large differences do make a difference to whether "red" is applicable, because you can create large differences out of a number of small differences.

6) Small differences in membership of two sets make no difference to the applicability of “$\alpha$ could have been constituted out of . . .” to them.

If this is intuitively acceptable, then (5) genuinely constitutes a sorites paradox: it is valid, according to classical principles, has intuitively true premises, and an intuitively false conclusion. Sorites paradoxes are due to vagueness. The question I want to raise is whether in the present case the vagueness attaches to our modal concepts or rather to our artefact concepts. There is a prima facie case for the latter option.

Replace our actual artefact concepts by precise ones, and the paradox disappears. For example, “ship*” is a precise artefact concept: any given ship* could have been made out of just one different part, but not out of more than one different part. The tolerance principle (6) will obviously fail for ships*, and so there is no reason to think of an argument with the form of (5) as sound. There is now no whiff of a paradox. A complete explanation of the paradoxes has not alluded to special features of modal notions.

In the context of counterpart theory, the paradoxical reasoning does not even get off the ground, as I shall show by formalizing it in QC.

Not every kind of semantics for a language with the operator syntax of QN involve quantifiers. Just as one could specify the contribution of "not" by a sentence like

1) A sentence "not-$A$" is true iff it is not the case that "$A$" is true

so one could, arguably, specify the contribution of "$\square$" or "necessarily" by a sentence like

2) A sentence "$\square A$" is true iff it is necessarily the case that "$A$" is true.

Whether such semantics will serve the purpose of defining validity is another question, and a disputed one.¹⁶

Finally, I turn to a second more or less metaphysical issue: analysis. Those looking for a reductive explanation, or "analysis", of what modal concepts mean will not have found even the beginnings of one in this chapter. A reductive explanation of a concept is one any part of which you can fully understand without yet understanding the concept to be explained. However, to be told that "necessarily $A$" is true iff "$A$" is true in all possible worlds is circular, relative to reductive aims, because the account makes free use of the notion of "possible", and "necessary" and "possible" are interdefinable: if we already understood "possible" we would not need the account, and if we did not understand it the account would be useless.

It was no part of our aim at any point to provide a reductive explanation. Exactly the same objection of circularity could be levelled at the account of "all" and "$\forall$", if that were supposed to be reductive. We start with English "all"-sentences. We formalize them using "$\forall$" and explain the meaning of "$\forall$" by giving an interpretation rule which crucially involves "all". Were this an exercise in analysis, it would be unrewardingly circular. It was not such an exercise, but rather an attempt to fashion an artificial language in which the notion of validity would be more accessible to theory than it is in ordinary English. If that is the modest aim of introducing a language like QN, the alleged "circularity" is beside the point.


One candidate for a reductive account of modality is that offered by David Lewis [1986a]. He says that one can say what a possible world is without using any modal notions: a possible world is a sum of (not necessarily actual) objects linked by space-time relations. The explanation essentially involves non-actualism. If one found the explanation attractive, it might help one overcome the commonsensical appeal of actualism.

## Bibliographical notes

### §1

Gamut [1991] (vol. 2, chs 1–3) provides good discussions of most of the topics of this chapter. For a comprehensive and fairly formal introduction to propositional modal logic, see Chellas [1980]; for a formal introduction to predicate modal logic, see Hughes and Cresswell [1996]. For a philosophical account of modality, which includes both formal semantics and arguments for many substantive essentialist claims, see Forbes [1985]; and, for critical discussions of this, Mackie [1987] and Edgington [1988]. Lewis's most famous use of "ways things could have been" as an introduction to possible worlds is in his [1973b], ch. 4.1, p. 84; for criticism, see McGinn [1981]. For Lewis's more recent view on possible worlds, see Lewis [1986a].

### §2

For taxonomy (the distinction between indicatives and non-indicatives), see Dudman, esp. [1984a], Edgington [1991], Bennett [1995]. The earliest presentation of Lewis's theory is Lewis [1973a]; see also Lewis [1973b], [1979] (reprinted with a postscript in Lewis [1986b]). For Stalnaker's theory, see his [1975]; and for his response to Lewis's criticisms, see, for example, his [1984], ch. 7. For general discussion, see Edgington [1995].

### §3

The historical source of the accessibility relation is Kripke [1963]. See also Chellas [1980] and Bull and Segerberg [1983].

### §4

In the empiricist tradition, necessity was held to be de dicto, and coextensive with analyticity. For an expression of this view, see Quinton [1963]. For distinctions between necessary, analytic and apriori see Kripke [1972]. These lectures were responsible for a considerable revival of interest in de re necessity. The present formulation of the contrast between de re and de dicto derives from Forbes [1985], p. 48.

§5 For Quine’s arguments, see his [1953c], [1953d] and [1960] §41. For criticism, see Plantinga [1974], App., pp. 222–51, and Linsky [1977], ch. 6; for detailed discussion, see Neale [2000].

§6 For Quine’s version, see his [1960], pp. 148–9. Davidson uses the argument in a number of places, for example [1967c], pp. 153. The account I follow most closely is Davies [1981], pp. 210–11. See also Neale [1995].

§7 For discussions of the problems of trans-world identity, see Plantinga [1974], pp. 88 ff., Kaplan [1979], Forbes [1985], esp. chs 3 and 7, Van Inwagen [1985], Fine [1985] and Lewis [1986a], pp. 210–20. For a discussion of the linguistic theory of necessity, see Pap [1958], esp. part II, ch. 7, and Van Fraassen [1977].

§8 See Lewis [1968] and [1986a]. In the latter, see pp. 5–20 for the introduction of the open-sentence formers, and pp. 199–202 for the case against treating intrinsic properties as relations. (NB: although I use this to attack the extra argument place theory, in Lewis’s book the argument has a different target.) Lewis, in both places, argues for counterpart theory (see §9). There are two separable questions: whether to adopt any quantifier treatment of modality, and whether to adopt the specific form of quantifier treatment embodied in counterpart theory. See also Hazen [1976], Davies [1981], ch. 9, esp. §1, Forbes [1985], pp. 89–95 and Melia [1992].

§9 The main texts for counterpart theory are, again, Lewis [1968] and [1986a]. See also Mondadori [1983], Forbes [1985], esp. chs 3.4 and 3.5, and App. 3, Ramachandran [1989]. For discussions of contingent identity, see Gibbard [1975], Wiggins [1980b], and, especially, Forbes [1985].

§10 Lewis’s remark about the non-transitivity of the counterpart relation shows that the paradox will not arise in his scheme, but it does not give any details of the semantic mechanisms. For such details, see Forbes [1985], ch. 7. For some current work on essentiality of origins, see Robertson [1998].

§11 For Lewis’s views, see his [1986a]. See also Forbes [1985], esp. ch. 4, Kripke [1972] and esp. [1980] and Chikara [1998]. Non-realism about modality is endorsed by, for example, Wittgenstein [1921], Ayer [1936], and, in the form that necessary truths reflect merely human conventions, is famously opposed by Quine [1936]. A new twist has been given by Blackburn in various writings, e.g. [1986b]. See also: Wright [1986] and [1989], Craig [1985], Hale [1989]. Ersatzism is argued for in Plantinga [1974], ch. 8, and [1976] (though in this article Plantinga’s target is the view that there are non-existent objects, rather than the view that there are non-actual objects). An argument against ersatzism by Lewis is discussed in Van Inwagen [1986]. For a criticism of Lewis’s [1973b] argument for the reality of non-actuals, see McGinn [1981].


#### Notes


**`[11]`** Kaplan has suggested a context in which the inclination to take this view is strong: a museum has sent a philosopher to Greece to buy, crate and dispatch the ship of Theseus for reassembly in the museum. As the philosopher removes a plank, he replaces it with a brand-new one of exactly the same shape, so that when he has finished he has an assembled ship of new parts and a dismantled ship of old parts. He sends the latter to the museum. Should the museum director be seriously perturbed when he gets a phone call from the philosopher announcing that he has the real ship of Theseus, still in Greece?

¹² What counts is the “at $\nu$” operator closest to the left of the first occurrence of the variable, say $x$. The objects relevant to the quantification are those in the world which is assigned to $\nu$, even if $x$ subsequently occurs in the scope of some distinct operator “at $\nu$”.

¹³ Adding an “actually” operator may not the only way to express sentences like (15): see Teichmann [1990].

¹⁴ Some theorists treat iterated modus ponens as invalid, and so construe sorites reasoning as invalid: see Goguen [1969], or, for a discussion closer to present concerns, Forbes [1985], ch. 7, §3.

¹⁵ There are at least two importantly different versions of the approach I am calling non-realist. One version does, the other does not, see an account of necessity, moral or logical, in terms of subjective responses as showing that our ordinary conceptions are in error. For the contrast, see Blackburn [1986b].

¹⁶ One aspect of the dispute involves the relationship between truth theoretic semantics (as exemplified in (1) and (2)) and model theoretic semantics — the style of semantics in terms of interpretations provided throughout this book. Cf. Evans [1976].