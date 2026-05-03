---
book: "Logical Forms"
title: "Chapter 03 Conditionals and probabilities"
chapter_number: "3"
chapter_name: "Conditionals and probabilities"
author: "Mark Sainsbury"
table_of_content: |
  1 Degrees of confidence
  3 Probabilistic logic
  4 Lewis’s proof
    (1) Details of the proof
    (2) Alternative arguments
  5 Conditionals without truth conditions?
  Bibliographical notes
---

# 3 Conditionals and probabilities

## 1 Degrees of confidence

We hold our beliefs with more or less confidence. We may believe with considerable confidence that we will not win the lottery; though if we bought a ticket we are presumably not absolutely certain that we will not win. We may believe we will not die within the week, but it would be foolish to be entirely confident of this, or perhaps even very confident. We may believe that some outsider will win the race, but evidently the bookmakers are much less sure.

We display different degrees of confidence towards conditionals. Suppose there are two urns, each containing a million marbles. Urn A's marbles are all white; urn B's are all white except for one black one. Suppose you know all this for certain, but do not know which of these urns is now before you. You reach into it and take a marble, and don't look to see what colour it is. You should be certain that

1) If this is urn A, I am not holding a black ball

and that

2) If I am holding a black ball, this is urn B.

But what about:

3) If this is urn B, I am not holding a black ball?

Perhaps one should not be certain of this, but it seems one ought to have a very high degree of confidence in it, for there is nearly a million to one chance against "I am not holding a black ball" being false, given that "This is urn B" is true (cf. Appiah [1985], p. 172).


Facts (or apparent facts) about our degrees of confidence in conditionals can be used to provide a further argument against the view that English conditionals are properly formalized by “→”, that is, that they are material conditionals. Suppose I have no confidence in winning the lottery. It seems consistent to be, in addition, very unconfident in the following:

4) If I win the lottery I will not pay off the mortgage.

On the contrary, the first thing I would do with a lottery win is eliminate the mortgage. These degrees of confidence are hard to explain on the view that conditionals are material conditionals.

5) (I will win the lottery) → (I will not pay off the mortgage)

has an antecedent which I think is almost certainly false, and so I should think that *`(5)`* is almost certainly true (since the falsity of the antecedent of a material conditional is enough for the truth of the conditional itself). This conflicts with my apparently reasonable lack of confidence in *`(4)`* (cf. Edgington [1997], p. 106).

The systematic study of degrees of confidence began with an interest in betting, and a point similar to the one just made in connection with *`(4)`* and *`(5)`* can be made in this context. Betting lends itself to the assignment of numbers to measure degrees of confidence. How confident should you be that the die will land 6? There are just six possibilities, and nothing to choose between them, so the right answer appears to be 1/6. How confident should you be that

6) If the die lands with an even number, it will land 6?

There are three ways in which it can land with an even number, and just one of these three is 6, so the right answer seems to be 1/3. How confident should you be that

7) The die lands with an even number → it will land 6?

There are only two ways in which *`(7)`* can be false: by the die landing 2 or 4. On all four other possibilities *`(7)`* is true. So one should have a degree of confidence of $4/6 = 2/3$. This is double the degree of confidence appropriate to *`(6)`*, which would make it hard to explain how, as the material conditional thesis claims, *`(6)`* and *`(7)`* could have the same truth conditions (cf. Edgington [1997], p. 106).


Ex. 3.1 What degree of belief should you have in the following conditional:

Subjective degrees of confidence, represented by expressions of the form $\operatorname{Pr}(A)$, can be evaluated as correct or incorrect, rational or irrational. For example, a person who thinks the die is not biased is irrational if, in addition, his beliefs can be described by "$\operatorname{Pr}(\text{the die lands an even number}) = 0.75$".

The method of representation incorporates some of the minimum principles of rationality, for example: "$\operatorname{Pr}(A) = 1 - \operatorname{Pr}(\neg A)$". If you believe it almost certain that John will come (call this $A$) then you should regard it as extremely unlikely that he will not come. Figure 3.2 makes plain that the values of $A$ and $\neg A$ must sum to 1 (the total height of the possibility space). Certainty in $A$ would be represented by making it fill the whole space, leaving no room for $\neg A$.

We can juxtapose possibility spaces for distinct propositions in a way which reveals the relations between them. For example, suppose $A$ and $B$ are contradictory, and that this is reflected in a subject's degrees of belief. The situation can be represented by figure 3.3. Reading horizontally, the idea is that the possibilities in which $A$ holds are just those in which $\neg B$ holds, and those in which $\neg A$ holds are just those in which $B$ holds.

![img-1.jpeg](_images-ocr/chapter3/p4-img-1.jpeg)

Figure 3.2


We are not only more or less confident about simple propositions, like whether John will come back today, but also about complex ones, like whether John will come back and it will rain, and whether John will come back if it rains. We can use the diagrams to show how the degrees of belief in the more complex are related to degrees of belief in the less complex. Suppose I believe that $A$ is quite likely and $B$ significantly less so. One way for this to be so is represented by the diagram in figure 3.4. In order to represent some relationships between $A$ and $B$, the probability associated with $\neg B$ has had to be displayed non-contiguously: it is the sum of the heights labelled $\neg B$ ($x + z$). The significance of the horizontal juxtaposition in the representation of degrees of belief can be explained by example:

The height $\gamma$ represents the probability associated with "$A \land B$".

The height $x + \gamma + w$ represents the probability associated with $A$ and also with "$A \lor B$".

The probability associated with "A or not-B" is 1.

The probability of $P$ given $Q$ is the proportion of the $Q$ height with horizontally matched $P$ height. In figure 3.4:

![img-2.jpeg](_images-ocr/chapter3/p5-img-2.jpeg)

Figure 3.3

![img-3.jpeg](_images-ocr/chapter3/p5-img-3.jpeg)

Figure 3.4

The totality of the $B$ height has horizontally matched $A$ height; so the probability of $A$ given $B$ is 1; equivalently, the probability of $A$ conditional upon $B$ is 1. In condensed form:

$$\operatorname{Pr}(A \mid B) = 1.$$

Alternative formulation: in all the possibilities in which $B$ is true, so is $A$. So on the supposition that $B$, $A$ is certain (though, as the height of not-$A$ shows, in the absence of that supposition it is not certain).

Consider the not-$B$ height $(x + z)$. The majority of it has horizontally matched $A$ height $(x + w)$. (The part of its height not having horizontally matched $A$ height is only $(z - w)$.) So the probability of $A$ conditional upon not-$B$ is greater than $1/2$:


$$
\Pr(A \mid \text{not-}B) > 1/2
$$

Alternative formulation: On the supposition that not-$B$, our confidence in $A$ would be measured as the proportion of the cases in question in which $A$ is true to all the relevant cases. This ratio is $(w + x)/(x + z)$, and is more than a half.

In calculating the size of the conditional probability of $P$ given $Q$, one pays no heed at all to not-$Q$: a conditional probability is the probability of a proposition on a supposition, so only the supposition, and not its negation, is relevant.

The explanation takes for granted that one cannot believe to be true a proposition which one is certain is not true. There is no such thing as the conditional probability of a proposition given some proposition assigned probability zero. This is encoded in the diagrams: we are to calculate $\Pr(A \mid B)$ by taking the possibilities in which $B$, and comparing them with those in which $A$ also holds. The procedure is inapplicable if there are no possibilities in which $B$; that is, if $B$ is represented as having zero height.

Conditional probability is closely related to the probability of conjunctions, in a way that has sometimes been used to offer a definition of it:
1) if $\Pr(A) > 0$, $\Pr(B \mid A) = \Pr(B \land A) / \Pr(A)$.

One cannot challenge the equation; but one can question whether it provides a useful definition of conditional probability. For how are we to understand the probability of a conjunction? A standard answer is given by the equation:
2) $\Pr(B \land A) = \Pr(B \mid A) \times \Pr(A)$, if $\Pr(A) > 0$.

We could either take conditional probability as a primitive notion and use it to define the probability of a conjunction, or take the probability of a conjunction as primitive and use it to define conditional probability. The former seems the preferable option. To use (1) as a definition of $\Pr(B \mid A)$ would imply that there can be no such thing as $\Pr(B \mid A)$ if there is no such thing as $\Pr(A)$. However, we may assign a conditional probability even when we do not assign any probability to the components. We may think that

3) $\Pr(\text{The streets in Moscow are wet} \mid \text{it is raining in Moscow})$

is close to 1, while being unwilling to assign any definite probabilities to “The streets in Moscow are wet” or to “it is raining in Moscow” or to the conjunction of these. What one is confident of is that, supposing that it is raining in Moscow, the chance of the streets being wet is high, that is, high relative to the supposition, whatever the probability of the supposition may be. This means that there is such a thing as $\Pr(B|A)$ even when there is no such thing as $\Pr(A)$; so (1) would not be a useful definition in the sense of one which we would always or typically use in estimating conditional probabilities.

Conditional probability plays a more fundamental role in our reasoning than the probability of a conjunction, to which (1) accords a defining role. It is very common to suppose that such-and-such is so, in order to assess, for example, how to act: supposing I do such-and-such, how will things turn out? Or supposing such-and-such happened, what should I do? The notion of how likely one thing is, on the supposition of another, belongs with very familiar notions. By contrast, it is not clear that we have so natural an everyday use for reaching an assignment of a probability to a conjunction.

## 3 Probabilistic logic

The conditional probability of $B$ given $A$ seems to express the right probability to assign to the conditional “if $A$ then $B$”. In considering the degree of belief I should assign to “if $A$ then $B$”, it is natural to reason: suppose that $A$; how likely it is that $B$? We can state this as the following hypothesis:

$$1) \Pr(\text{if } A \text{ then } B) = \Pr(B|A).$$

Ex. 3.2 Show that the conditional probability of $B$ given $A$ may differ from the degree of belief in “if $A$ then $B$” based on the rule:

Suppose you believe that $A$; how certain are you that $B$?

Consider *`(1.3)`*:

If this is urn B, I am not holding a black ball.

Given that you know that just one of the million balls in urn B is black, it seems right to believe *`(1.3)`* with great confidence. The related conditional probability is likewise very high: given that this is urn B, the chances of holding a white ball are nearly a million to one. One can arrive at this conditional probability without having assigned any absolute probability to "this is urn B".

The assignments of probability claimed in §1 to pose a difficulty for the view that English conditionals are material conditionals coincide with what one would expect if *`(1)`* were true. It is consistent to assign a low absolute probability to "I will win the lottery" and also a low probability to "I will not pay off the mortgage" on the supposition that I do win the lottery. I suppose, unlikely as it is, that I win the lottery, and I consider what I do; paying off the mortgage presents itself as a highly likely first step, not paying it off seems most unlikely; so the conditional probability of not paying off the mortgage, given that I win the lottery, is low. If *`(1)`* is right, this means that I assign low probability to *`(1.4)`*:

If I win the lottery I will pay not off the mortgage.

What matters to the conditional probability of $B$ upon $A$ is not the size of the probability one awards to $A$, but how much of the probability space awarded to $A$ is also occupied by $B$. This emerges clearly with examples like *`(1.6)`*:

If the die lands with an even number, it will land 6.

The reasoning given in §1 for the conclusion that one should believe this to degree 1/3 in effect invited one to suppose the die lands with an even number, and then to count the ratio of those cases in which that even number is 6 to the totality of cases (the totality, that is, consistent with the supposition, that is, all the even numbers). This is diagrammatically presented in figure 3.5. Because a third of the possibilities, given that the die lands even, are that it lands 6, one should, according to *`(1)`* and common sense, assign 1/3 as the probability of *`(1.6)`*.

![img-4.jpeg](_images-ocr/chapter3/p9-img-4.jpeg)

Figure 3.5

Typically, our premises when we reason are less than certain, but we want to reason in such a way as not to increase our uncertainty. If we believe a proposition to degree 0.75, that is, if we assign it this probability, then our uncertainty in it is 0.25. In other words, the uncertainty of a proposition is equal to the probability of its negation. Not increasing uncertainty is a constraint upon reasoning, and indicates how we can define a notion of probabilistic validity:

2) An argument $A_{1}, \ldots, A_{n}; C$ is probabilistically valid (for short, $A_{1}, \ldots, A_{n} \vdash C$) iff necessarily, the uncertainty of the conclusion does not exceed the sum of the uncertainties of the premises.

The "necessarily" requires that however a rational person assigns probabilities to the components of the arguments, there can be no increase in uncertainty. Valid reasoning, according to (2), is all and only reasoning which cannot introduce new uncertainty. It can be shown (cf. Adams [1975]) that if we consider a propositional language with no conditionals, the classically valid arguments (those for which $\models_{\mathbb{P}}$ holds) are

![img-5.jpeg](_images-ocr/chapter3/p10-img-5.jpeg)

Figure 3.7

The probability of a disjunct is represented by the net sum of the heights of the disjuncts (that is, overlapping heights are not counted twice). In Figure 3.6, the uncertainty of $A$ or $B$ is small, but the uncertainty of if not-$A$ then $B$ is 1; so the argument in *`(5)`* is not probabilistically valid. However, arguments on the pattern of *`(5)`* appear valid, so perhaps we have here a reason to suspect that principles *`(1)`* and *`(2)`*, which respectively offer a conditional probability account of the probability of conditionals and a probabilistic account of validity, do not provide a correct picture of our reasoning with conditionals.

The earlier argument of the form of *`(5)`* was given in *`(2.8.1)`*, viz.:

Either the butler or the gardener did it. Therefore if the gardener didn't do it, the butler did.

This seems to be valid, and seems to be so in virtue of its form; so it seems that such reasoning could not increase uncertainty.

The probability theorist disputes this. Suppose you believe that the gardener is overwhelmingly the most likely suspect, and you are sure that if the butler was involved it was simply as the gardener's accomplice (he would not have acted alone). There is nothing irrational about these assignments of probability. Yet they appear to involve thinking that the premise of *`(2.8.1)`* is highly likely, and the conclusion certainly false. If this is correct, there is, after all, a reason for thinking that *`(2.8.1)`* is not valid, for if an argument is valid it is not rational to assign high probability to its premise and low probability to its conclusion.


**Ex. 3.5** If you think the premise of (2.8.1) can be highly likely, yet its conclusion certainly false spell out why. Would your reasons be accepted by one who analysed conditionals truth functionally?

Other examples suggest that there are invalid instances of the form in *`(5)`*, for example:

6) Either he will throw an even number or he will throw a 6. Therefore, if he does not throw an even number, he will throw a 6.

This strikes many as invalid, which would be enough to refute (5). It is certainly probabilistically invalid. By contrast, a truth functional theorist will insist that if the premise is true because an even number is thrown, the conclusion is automatically true; otherwise the premise is false, so there can be no counterexample. The appearance of invalidity of *`(6)`*, according to the truth functional theorist, adds nothing to the already admitted oddness of conditionals whose antecedents are known to be false.

**Ex. 3.6** Demonstrate the probabilistic invalidity of (3.6) by specifying the uncertainty of premise and conclusion.

The other argument given in chapter 2.8 for the truth functional interpretation of conditionals was based on the principle of conditional proof, *`(2.8.8)`*, viz.:

If $[A_1, \ldots, A_n, B \models C]$ then $[A_1, \ldots, A_n \models \text{if } B \text{ then } C]$.

We can show that we can have

![img-6.jpeg](_images-ocr/chapter3/p12-img-6.jpeg)

Figure 3.8

7) $A, B \vdash C$

without having

8) $A \vdash \text{if } B \text{ then } C$.

One way to do so is to consider the instance in which “$A \vee C$” replaces “$A$” and “not-$A$” replaces “$B$”. Since this involves no conditionals, and since $\vdash$ and $\vdash_{\mathbb{P}}$ coincide for such cases, we can be confident that we have a truth of the form of *`(7)`*. But we have already seen that the corresponding instance of *`(8)`* is false (in the discussion of *`(2.8.1)`*).

Other classical principles of validity which hold for “$\rightarrow$” fail on the probabilistic approach, for example, contraposition (cf. 2.5.19) and transitivity (cf. 2.5.22). Contraposition can be represented as:

9) If $A$ then $B$; if not-$B$ then not-$A$.

Figure 3.8 demonstrates the probabilistic invalidity of the argument in *`(9)`*.

![img-7.jpeg](_images-ocr/chapter3/p13-img-7.jpeg)

Figure 3.9

Ex. 3.7 Stalnaker (1984, pp. 124-5) gives a general argument for thinking that contraposition is unacceptable. The crucial assumption is:

If $(B \vdash C)$ then (if $A$ then $B \vdash$ if $A$ then $C$).

Can you complete the argument? What would be the best response that could be made by one who thought conditionals were truth functional?

Transitivity can be represented as:

10) If $A$ then $B$, if $B$ then $C$; if $A$ then $C$.

Figure 3.9 demonstrates the probabilistic invalidity of *`(10)`*. In chapter 2, the following example *`(2.5.23)`* was offered to suggest that our ordinary reasoning with conditionals does not always conform to transitivity:

If Smith dies before the election, Jones will win.

If Jones wins, Smith will retire from public life after the election.

So, if Smith dies before the election, he will retire from public life after the election.

Some arguments which instantiate transitivity seem valid, for example

11) If the battery's dead, then the car won't start.

If the car won't start, then I won't be able to get to work.

So, if the battery's dead, then I won't be able to get to work.

The fact that this argument is not probabilistically valid needs to be explained by the probability interpretation. If one could show how uncertainty could be increased by reasoning in this way, one would show that it cannot really be valid, however it may appear. One might also be able to explain the semblance of validity, perhaps along the following lines: this argument form is probabilistically valid:

12) If $A$ then $B$, if $A$ and $B$ then $C$; if $A$ then $C$.

Ex. 3.8 Can you suggest a scenario in which it is reasonable to accord high probability to the premises of (3.11) but low probability to its conclusion?

Perhaps arguments like *`(11)`* strike us as valid because we are quite happy to add the antecedent of the first conditional to the antecedent of the second; in other words, we assimilate the form of *`(11)`* to *`(12)`*. Were we to do this in the case of *`(2.5.23)`*, we would have the following:

13) If Smith dies before the election, Jones will win.

If Jones wins and Smith dies before the election, Smith will retire from public life after the election.

So, if Smith dies before the election, he will retire from public life after the election.

Many people find the second premise unacceptable, and so would have no use for the argument.

A seemingly convincing argument concludes that we should not expect transitivity. The relevant assumptions are:

14) For some $A, B$, "if $A$ then $B$" is true even though $A$ does not entail $B$ (so it is logically possible that $A$ is true yet $B$ false).

15) Any conditional with a possibly true antecedent and a consequent incompatible with its antecedent is false.

Ex. 3.9 Show with an example why (3.15) would be unacceptable to the theorist who views English conditionals as material conditionals. Compare with (2.3.28), which might be abbreviated to: "If common sense is correct, then common sense is incorrect. Therefore common sense is incorrect."

Consider the following instance of *`(10)`*:

16) If $A$ and $C$ then $A$, if $A$ then $B$; if $A$ and $C$ then $B$

(putting “$A$ and $C$” for “$A$”, “$A$” for “$B$” and “$B$” for “$C$”). If dropping a necessarily true premise cannot make a valid argument invalid, and assuming that “if $A$ and $C$ then $A$” is necessarily true, then if *`(16)`* is valid so is

17) If $A$ then $B$; if $A$ and $C$ then $B$.

Take an instance in which we put "not-$B$" for "$C$". "If $A$ then $B$" is to be a true conditional which does not entail its consequent (*`(14)`* assures us that there is one), so "if $A$ then not-$B$" is possibly true. So by *`(15)`* the conclusion of *`(17)`* is false, though the premise is true. So we must reject the supposition that *`(16)`* is valid, and so also the supposition that *`(10)`* is valid.

We have already noticed an apparent counterexample to the validity of *`(17)`* in (2.5.28), viz.:

If I put sugar in this cup of tea it will taste fine.

So, if I put sugar and also diesel oil in this cup of tea, it will taste fine.

The probability theory, as characterized in this section, gives an account of the degree of belief one should have in a conditional (equal to the conditional probability of the consequent upon the antecedent) and tells us how to reason with conditionals (so as not to reduce uncertainty, characterized, for conditionals, in terms of conditional probabilities). It does not say anything about the truth conditions of conditionals, which is a topic we turn to later (in §4). Moreover, I have not presented this theory as saying anything about the conditions under which conditionals should be asserted. Assertibility will be discussed briefly now, under the heading of asserted difficulties with the probability theory.


Ex. 3.10 If any of the following are incorrect, draw a diagram to establish this, in each case giving an example of an argument which is intuitively invalid:

i) It is not the case that if $A$ then $B \vdash A$.

ii) It is not the case that if $A$ then $B \vdash$ it is not the case that $B$.

iii) If $A$ then not-$B$, $B \vdash$ not-$A$.

**`(a)`** Even if the theory gives the right account of degrees of belief, it is wrong to link this with degrees of assertibility. For example, it may be urged that even if I allow only a slight chance of *`(1.3)`*, viz.:

If this is urn B, I am not holding a black ball

being false, I still ought not to assert it.

Although probability theories are sometimes cast in terms of assertibility, this is not essential (and that casting has been avoided here: for a discussion, see Edgington [1997] p. 101–5). The theorist does best to admit that the relation between the degree of one's belief and the appropriateness of assertion is a complex issue. There is certainly no immediate inference from high degree of credence to appropriateness of assertion, as one can see at once by considering the demands of etiquette.

Ex. 3.11 Give an example of a conditional belief with a high degree of probability and a situation in which asserting it would be highly misleading or otherwise inappropriate.

**`(b)`** The conditional probability of $B$ given $A$ is undefined when $\Pr(A) = 0$. Yet surely we believe some conditionals which have antecedents we regard as certainly false. I will consider some putative examples.

18) If the longhorns lose, then I’m a monkey’s uncle.

One who says this represents himself to be as sure that the longhorns will win as he is that he is not uncle to a monkey, that is, as assigning Pr(the longhorns lose) = 0. Yet the conditional appears entirely in order.

Options for the probability theorist include (i) saying that this is a special idiom from which no general lesson can be inferred; (ii) saying that one who asserts or believes *`(18)`* must allow the possibility of the longhorns' defeat: *`(18)`* expresses, not complete certainty in victory, but merely very high probability; (iii) having a special rule for the case in which the antecedent has zero probability, for example, that every such conditional is to count as certain.

The special rule proposal is antithetical to the spirit of the probability theory, and would bring its account closer to the material conditional account. More than one rule is possible, but if we take *`(18)`* at face value, an appropriate one is: a conditional to whose antecedent I assign zero probability is one I should regard as certain. Suppose my confidence in $A$ decreases over time, finally reducing to zero. As far as "$A \rightarrow B$" goes, this corresponds to gradually increasing confidence in its truth. But if no part of the $A$ height at the beginning of this process is horizontally opposite to the $B$ height, then on the probability theory, if it adopts the envisaged special rule, I start with certainty of the falsity of "if $A$ then $B$" and suddenly, as I move from being almost to completely certain of the falsehood of $A$, the conditional becomes certainly true. This is not plausible. An analogous difficulty would affect the special rule that if $\Pr(A) = 0$ then $\Pr(\text{if } A \text{ then } B) = 0$; and either rule will have difficulty explaining away the intuition that some conditionals with certainly false antecedents are true and others false.

Ex. 3.12 Can you give an example of a true conditional with a certainly false antecedent, and an example of a false conditional with a certainly false antecedent?

A more everyday example than *`(18)`* makes the "special idiom" option less attractive:

19) If someone broke in, they must have repaired the damage before they left.

This might be said as a way of reassuring a worried homeowner: since we all know that burglars do not repair the damage they cause, the

audience is intended to achieve complete confidence that no one broke in. The audience is supposed to believe the conditional and so, like the speaker, assign Pr(someone broke in) = 0.

There are various similar kinds of case in which we seem to have a use for a conditional with an antecedent we are absolutely certain is false. I know I am innocent of the murder, which occurred in London. In my interrogation I affirm:

20) If I committed the murder, then I was in London on Tuesday evening.

If I can get the police to agree, then their acceptance of my alibi showing I was in Oxford on Tuesday evening commits them to accepting my innocence. In cases like this, I don't expect my audience already to be certain of the falsehood of the antecedent. The probability theorist might see both *`(19)`* and *`(20)`* as conniving or deferential uses: I adopt for the sake of argument the degrees of belief of my of my audience, which, at that point, is non-zero for the antecedent. But it would seem that I can steadily believe *`(20)`*, and perhaps also *`(19)`*, regardless of the rhetorical or conversational context which makes their utterance natural.

In mathematical reasoning, it is common to introduce assumptions for reductio ad absurdum, and these may figure as antecedents of conditionals. For example, a famous proof that there is no greatest prime may be represented as starting from

21) If there is a greatest prime, then it is odd.

There seems no question but that many users of *`(21)`* assign zero credence to the antecedent. While we are no doubt less than certain of many necessary truths (of logic or mathematics, for example) there seem to be many of which we are completely certain, and it seems that this confidence does not prevent us using their negations as antecedents of intelligible conditionals.

The best response for the probability theorist, in my view, is to pursue the notion of conniving or deferential use, an idea mentioned (rather briefly) by Edgington: a conditional is only used when the speaker or thinker takes the antecedent to be not certainly false "at least for the sake of argument, at least temporarily, at least to co-operate with her audience" ([1995], p. 265). All that is required for there to be a conditional probability is that there be a rational non-zero assignment of a positive degree to the antecedent. We are good at putting ourselves in the epistemic states of others or in imaginary epistemic states. We are willing suspenders of disbelief; we can suppose to be so what we know not to be so. There would be nothing strange in the idea that a full description of these activities saw in them pretended or imagined shifts in our degrees of belief. It is not that when I suppose that $A$ I suppose that I believe that $A$, but that seriously entering into the supposition may also involve rearranging actual degrees of credence.


**`(c)`** The final issue for probabilistic logic to be mentioned here is that it ought to provide an explanation of why the probability of a conditional should be equal to the probability of its consequent, given its antecedent. This is the main topic of §4.

## 4 Lewis’s proof

One possible explanation for why it is that *`(3.1)`*, viz.

$$\Pr(\text{if } A \text{ then } B) = \Pr(B|A)$$

is that a conditional “if $A$ then $B$” expresses some proposition, say $X$, meeting the condition that in every reasonable distribution of degrees of belief,

1) $\Pr(X) = \Pr(B|A)$.

Having initially identified $X$ in terms of appropriate degrees of belief, we might be able go on to determine its truth conditions. David Lewis [1976, 1986] has proved the remarkable fact that, on certain assumptions, there is no such proposition $X$. The proof requires more precision and some additional material. Many readers will prefer to skip it, and take up the thread again at §4(2) on p. 47.

Ex. 3.13 On present assumptions, one way to show that conditionals are not material conditionals is to show that $X$ cannot be $A \to B$. Show that:

$$\Pr(A \to B) \neq \Pr(B|A)$$

### (1) Details of the proof

A *probability function*, $\operatorname{Pr}$, is an assignment of numbers to all the sentences of the language in accordance with the following rules:

2) $1 \geq \operatorname{Pr}(A) \geq 0$.

Pr assigns every sentence a number between 1 and 0.

3) If $\models (A \leftrightarrow B)$ then $\operatorname{Pr}(A) = \operatorname{Pr}(B)$.

Pr assigns logical equivalents the same value.

4) If $\models (A \rightarrow \neg B)$ then $\operatorname{Pr}(A \lor B) = \operatorname{Pr}(A) + \operatorname{Pr}(B)$.

Pr assigns to a disjunction of incompatible sentences the sum of the numbers it assigns to each disjunct.

5) $\operatorname{Pr}(A \land B) = \operatorname{Pr}(A \mid B) \times \operatorname{Pr}(B)$, if $\operatorname{Pr}(B) > 0$.

If $\operatorname{Pr}(B) > 0$, Pr assigns a conjunction of $A$ and $B$ the product of the probability of $A$ given $B$ with $\operatorname{Pr}(B)$.

6) $\operatorname{Pr}(A) = 1 - (\operatorname{Pr}(\neg A))$.

The probability of a sentence and its negation sum to 1.

7) If $\models A$ then $\operatorname{Pr}(A) = 1$.

Pr assigns 1 to logically necessary truths.

There are no constraints on how a probability function assigns numbers to atomic sentences: there is a probability function $\operatorname{Pr}_1$ such that $\operatorname{Pr}_1(\text{the earth is flat}) = 0$ and also a probability function $\operatorname{Pr}_2$ such that $\operatorname{Pr}_2(\text{the earth is flat}) = 1$, and indefinitely many other functions assigning intermediate values.

**Ex. 3.14** Why does (4.7) not constrain how a probability function assigns numbers to atomic sentences?

The claim *`(3.1)`* is intended to generalize over probability functions: for any such function, or at least any reasonable one (that is, any function which could represent the way a rational thinker could assign probabilities to his beliefs), $\operatorname{Pr}(\text{if } A \text{ then } B) = \operatorname{Pr}(B \mid A)$. In his original proof, Lewis assumed that reasonable probability functions would be *closed under conditionalization* (subsequent work, by Lewis and others, has shown how to weaken this assumption). The assumption is that if $\operatorname{Pr}_i$ is reasonable and $\operatorname{Pr}_i(C) > 0$, then there is a reasonable function $\operatorname{Pr}_j$ such that, for all $A$, $\operatorname{Pr}_j(A) = \operatorname{Pr}_i(A|C)$.


For reductio, suppose that "if" is a non-truth functional sentence connective whose meaning ensures that *`(3.1)`* holds for any reasonable probability function. Reasonable probability functions satisfy the following condition:

8) $\operatorname{Pr}((\text{if } A \text{ then } B) \mid C) = \operatorname{Pr}(B \mid (A \text{ and } C)), \text{ if } \operatorname{Pr}(A \text{ and } C) > 0.$

Here we find "if $A$ then $B$" used as a component in a conditional probability. This is justified by the assumption for reductio: "if $A$ then $B$" is a proposition like another, and so can be an instance of a sentence letter.

To establish *`(8)`*, take an arbitrary probability function, say $\operatorname{Pr}_i$. Since the functions are closed under conditionalization, there is also a function, $\operatorname{Pr}_k$, such that, for some $C$ for which $\operatorname{Pr}_i(C) > 0$, for all $A$, $\operatorname{Pr}_k(A) = \operatorname{Pr}_i(A|C)$. The remainder of the argument for *`(8)`* can be set out thus:
9) $\operatorname{Pr}_k(B \land A) = \operatorname{Pr}_i((B \land A) \mid C)$ (definition of $\operatorname{Pr}_k$)

$$
\begin{aligned}
&= \operatorname{Pr}_i(A \mid C) \times \operatorname{Pr}_i(B \mid (A \land C)) \quad (\text{by *`(5)`*}) \\
&= \operatorname{Pr}_k(A) \times \operatorname{Pr}_i(B \mid (A \land C)) \quad (\text{definition of } \operatorname{Pr}_k)
\end{aligned}
$$

$$
\begin{aligned}
\operatorname{Pr}_k(B \land A) &= \operatorname{Pr}_k(A) \times \operatorname{Pr}_k(B \mid A) \quad (\text{by *`(5)`*}) \\
&= \operatorname{Pr}_k(A) \times \operatorname{Pr}_k(A \rightarrow B) \quad (\text{by *`(3.1)`*})
\end{aligned}
$$

Ex. 3.15 Show how to use (4.5) to establish:

$\operatorname{Pr}_i((B \land A) \mid C) = \operatorname{Pr}_i(B \mid (A \land C))$

Hint: you have to use (4.5) more than once; and a strict setting out of the proof would also invoke (4.3).

Hence

$$
\operatorname{Pr}_k(A) \times \operatorname{Pr}_k(A \rightarrow B) = \operatorname{Pr}_k(A) \times \operatorname{Pr}_i(B \mid (A \land C))
$$

and so

$$
\operatorname{Pr}_k(A \rightarrow B) = \operatorname{Pr}_i(B \mid (A \land C))
$$

which, given the definition of $\operatorname{Pr}_k$, and the fact that $\operatorname{Pr}_i$ was arbitrary, amounts to (8).

Now take arbitrary sentences $A$, $B$ and some probability function such that $\operatorname{Pr}(A \land B) > 0$ and $\operatorname{Pr}(A \land \neg B) > 0$. From *`(2)`*-*`(7)`* it follows that

10) $\operatorname{Pr}(A \rightarrow B) = \operatorname{Pr}((A \rightarrow B) \land B) + \operatorname{Pr}((A \rightarrow B) \land \neg B)$.

Hence by *`(5)`*

11) $\operatorname{Pr}(A \rightarrow B) = (\operatorname{Pr}((A \rightarrow B) \mid B) \times \operatorname{Pr}(B)) + (\operatorname{Pr}((A \rightarrow B) \mid \neg B) \times \operatorname{Pr}(\neg B))$.

Applying *`(8)`* to this gives:

12) $$\operatorname{Pr}(\text{if } A \text{ then } B) = (\operatorname{Pr}(B \mid (A \text{ and } B)) \times \operatorname{Pr}(B)) + (\operatorname{Pr}(B \mid (A \text{ and } \text{not-}A)) \times \operatorname{Pr}(\text{not-}A)).$$

This simplifies to

13) $$\operatorname{Pr}(\text{if } A \text{ then } B) = (1 \times \operatorname{Pr}(B)) + (0 \times \operatorname{Pr}(\text{not-}A)) = \operatorname{Pr}(B).$$

*`(13)`* is unacceptable: it says that for an arbitrary probability function, and an arbitrary conditional, the probability of the conditional is the same as the probability of its consequent. There are plenty of counterexamples. A premise which leads to this absurdity must be rejected, so Lewis claims that we must reject the assumption that “if” is a non-truth functional sentence connective whose meaning ensures that *`(3.1)`* holds for any reasonable probability function.

#### Ex. 3.16 Give a counterexample to (4.13).

If we are willing to hold on to *`(3.1)`* (as Lewis is not) it would have been enough to assume something more general: that conditionals are propositions, as *`(1)`* affirms. By *`(3.1)`*, if they are propositions they are ones whose probability is always the conditional probability of the consequent, given the antecedent. The assumption that they are propositions is used in taking *`(8)`* to be intelligible: if “if $A$ then $B$” is not a proposition, we cannot intelligibly ask after its probability given $C$. Lewis’s result has therefore been taken by some (though not by Lewis himself) to show that there are no conditional propositions. This view will be considered in §5. In order to get a clearer fix on what it is, let us consider an alternative argument for this conclusion, given by Edgington.


### (2) Alternative arguments

If there is a proposition $X$ which satisfies *`(1)`*, then either it is a material conditional or else it affirms a stronger-than-material link between its components. Edgington suggests we can eliminate both possibilities. For:

> (i) Minimal certainty that $A$ or $B$ is enough for certainty that if $\text{not-}A$ then $B$;
>
> (ii) It may be rational to disbelieve both $A$ and also if $A$ then $B$. (cf. Edgington [1995], p. 279)

The idea is that the truth functional account meets (i) but not (ii), and any stronger-than-material link meets (ii) but not (i).

To be minimally certain that $A$ or $B$ is to assign 1 to "$A$ or $B$" but not to $A$ and not to $B$. (We saw earlier that one who assigns high credence to "$A$ or $B$" just because, or largely because, they assign high credence to $A$, may also assign low credence to "if $\text{not-}A$, then $B$". Such persons are certain but not "minimally" certain that $A$ or $B$.) We have already seen both that the truth functional account meets (i) and that it fails to meet (ii).

A stronger-than-material account of conditionals might require that the conditional should represent a causal or inferential connection between antecedent and consequent. The details do not matter. The point is that though such an account may meet (ii), it cannot meet (i), since minimal certainty that $A$ or $B$ is not enough for certainty of a special link between $A$ and $B$.

The divergence which upsets *`(1)`* arises because a degree of belief in $B$ given $A$ is insulated from $\text{not-}A$ facts: the only thing relevant is the proportion of ways in which $A$ is true which are also ways for $B$ to be true. By contrast, a proposition $X$, with $A$ and $B$ as components, and purportedly satisfying *`(1)`*, will not be thus insulated: some such propositions will be true when $\text{not-}A$ and some will be false when $\text{not-}A$. (It cannot be that $\text{not-}A$ is true whenever $X$ is true, nor that $\text{not-}A$ is false whenever $X$ is true: not only would either link be inconsistent with our use of conditionals, either link would prevent $\operatorname{pr}(X)$ always aligning with $\operatorname{pr}(B \mid A)$.) Distinct reasonable probability functions may diverge in what they assign to $\text{not-}A$ while coinciding on $B \mid A$ (to which assignments to $\text{not-}A$ are irrelevant), and hence diverge in what they assign to $X$. This would be enough to show that $X$ does not satisfy *`(1)`*.


**Ex. 3.17** Show that if $X$ (a supposedly conditional proposition with $A$ and $B$ as components) was either true whenever $\text{not-}A$, or false whenever $\text{not-}A$, it would not correspond to "if $A$ then $B$".

If there is no proposition satisfying (1) then conditionals are not propositions. How, then, can we use them in reasoning? The positive account might start by pointing out that there is a range of conditional acts: conditional bets, conditional questions, conditional commands:

14) I bet you that if Oswald doesn't kill Kennedy, someone else will.

15) If Oswald doesn't kill Kennedy, was it you?

16) If Oswald doesn't kill Kennedy, kill him yourself!

These acts do not have a content which is exhausted by some proposition. This would encourage one to add to the list conditional assertion and conditional belief. Conditional bets, questions and commands are in some sense "cancelled" if their antecedent does not obtain: the bet is off (no one wins and no one loses), it is as if no question had been asked, and nothing you can do counts as obeying or disobeying the order. In the case of belief and assertion, the analogue might be that if the antecedent does not obtain, you have no commitment to the consequent. This does not mean that to make a "conditional assertion" of $B$, given $A$, is to do something which, given $B$, amounts to an assertion of $A$. If I utter "if $A$ then $B$" assertively, and $A$ is true, it does not follow that I have asserted that $B$ (though normally I am in that case somehow committed to $B$). Similarly, if my belief state can be described by "if $A$ then $B$" and $A$ is true it does not follow that I believe that $B$. The notion of "cancellation" associated with falsehood of the antecedent of a conditional bet, question or order could be applied in more than one way to conditional assertion or belief.

On this theory there can be no account of the truth conditions of conditionals: they have none. In the following section, we will consider a difficulty for this theory.

## 5 Conditionals without truth conditions?

One main difficulty for the view that conditionals lack truth conditions is that conditionals appear to embed within propositions, and this seems hard to explain unless they are themselves propositions, where a proposition is, by definition, something which has truth conditions. Let us start with a case which enables us to bring the “no-proposition” view more clearly into focus:

1) John believes that if Mary is not in Rome, she is not in Italy.

In the first instance, the no-proposition view is that this is true just in case John believes that Mary is not in Italy on the supposition that she is not in Rome. The theorist might decline to say what it is to believe on a supposition, other than in terms of assigning a fairly high conditional probability. The mental state is not purely hypothetical: it is not that there is nothing special to John’s belief state unless or until the supposition is realized. The negative part of the view is the denial of the orthodoxy that (1) affirms a relation between a person (John) and a proposition (that if Mary is not in Rome, she is not in Italy).

One whose probability function is like John’s will often be ready to use the sentence

2) If Mary is not in Rome, she is not in Italy

assertively. On conventional views, John is asserting the proposition that if Mary is not in Rome, she is not in Italy. On the no-proposition view, John is engaged in an act of conditional assertion. If it turns out that Mary is not in Rome, John is committed to her not being in Italy. But what if it turns out that Mary is in Rome? Clearly John is not committed to her not being in Italy; but his assertive use of (2) commits him to something. If I believe what John believes, I know that there is no point searching for Mary anywhere in Italy except Rome. This knowledge is not purely hypothetical, but can immediately guide action.

Conditionals are said to embed within a variety of contexts other than those of which (1) is an example. Here are four troublesome kinds of case:

3) It's not the case that if you *will* to succeed then you'll succeed.

4) If you apply to us then, if you get other offers, you'll be in a position to choose.

5) If John is someone who tends to back down if challenged, then your best bet is to challenge him.

6) There is a student who, if I criticize him, will get angry (cf. Kölbel [2000]).

The cases are troublesome because they suggest that a conditional can be an element of a compound proposition in a way that would seem to require that conditionals themselves are propositions.

In many circumstances, the natural way to deny a conditional “if $A$ then $B$” is to make an assertive utterance of “if $A$ then not-$B$”. You say that if the match is played at home then Arsenal will win, but I disagree and could naturally express my disagreement by

7) If the match is played at home, Arsenal won't win.

This poses no problem for the no-proposition view, for an assertive utterance of *`(7)`* can be regarded as a conditional assertion of “Arsenal won't win”. However, there are also cases in which denial doesn't happily take this form. My son says that he doesn't need to go on a course: all he needs to do, in order to succeed, is to exercise his will to succeed. I am not convinced. It's not that I think that if he exercises his will he won't succeed; I merely think *`(3)`*. This appears to be the negation of a proposition my son has affirmed; but this cannot be so on the no-proposition view. It's true that I don't have to use what appears to be a negated conditional to express my view. I could instead say something like: willing to succeed isn't a sufficient condition for success. But the fact remains that *`(3)`* is an entirely natural mode of expression. (Contrast Edgington [1995], pp. 283, 284.)

*`(4)`* appears to be a conditional with a conditional consequent. Appearances must deceive, if the no-proposition view is right: if the consequent is a conditional, it cannot as such have truth conditions, and so cannot be asserted, even conditionally. One response is that we can understand such conditionals as having conjunctive antecedents, and so not as embedding a conditional at all. The proposal is that *`(4)`* really has the logical form

8) If you apply to us and you get other offers, you'll be in a position to choose.

Within the no-proposition framework there is a specific justification: there is no difference between on the one hand supposing $A$ and going on to suppose $B$, and, on the other, supposing $A$ and $B$.

To say that John tends to back down if challenged is pretty much to say that John is lacking in assertiveness. It would therefore be surprising if there was anything significantly more difficult about explaining (5) than about explaining

9) If John is lacking in assertiveness, then your best bet is to challenge him.

Yet according to the no-proposition view, while one can suppose that John is lacking in assertiveness, one cannot suppose that he will tend to back down if challenged, for what can be supposed can be true or false. According to this view, whereas one should regard an assertive utterance of *`(9)`* as a conditional assertion that your best bet is to challenge him, one cannot take the same view of *`(5)`*.

One way of dealing with these cases of conditionals with apparently conditional antecedents is to claim that we "decode" sentences like *`(5)`* by finding a "basis" for the antecedent conditional, say John's lack of assertiveness, and then treat the sentences as if they were simple conditionals, like *`(9)`*. This strategy will not work in all cases, and it can also backfire: as I have just suggested, some kind of equivalence between *`(5)`* and *`(9)`* is no less apt to suggest that *`(5)`* can be taken as genuinely a case in which a conditional is antecedent to a conditional.

Ex. 3.18 Give an example of what appears to be a conditional with a conditional antecedent for which it is less plausible to say: the antecedent introduces a basis, so the whole conditional can be understood as having a non-conditional antecedent.

This widespread phenomenon not only offers many cases in which a conditional apparently has a conditional antecedent; it also brings out a more direct conflict between the no-proposition view and naive assumptions. For example, "fragile" means something like "tends to break if dropped". It is easy to think of apparent conditionals whose antecedent ascribes fragility ("if this vase is fragile, it needs careful handling"). The more direct conflict is that we would be extremely reluctant to think that "fragile" cannot be true of some things and false of others, yet if it has the supposed conditional meaning, this ought not to be so, given the no-proposition account of conditionals.

The final case, *`(6)`*, involves a conditional apparently embedded in an existential quantification. In uttering *`(6)`* assertively, I seem to make an unconditional assertion to the effect that there is a student who . . . Intuitively, what I say is false if "if I criticize him, he will get angry" is false of each student. But on the no-proposition view, a conditional can no more be true of someone than it can be true.

Many of these examples pose serious difficulties for any theory, especially examples like *`(5)`* (cf. Edgington [1995], pp. 280 ff.). (A particular interest of *`(6)`* is that it does not pose special problems for propositional accounts of conditionals.) No-proposition theorists have offered various defences, though they, in common with propositional theorists, have not found a single strategy which looks plausible for all cases.

The considerations of this chapter relate to "indicative" conditionals. A somewhat more detailed exploration of the taxonomy, and a discussion of non-indicative conditionals, is in chapter 5.2.

## Bibliographical notes

Serious work in this area could well begin with Edgington [1995] which reviews the main positions, and argues for the author's "no-proposition" view. Two good collections are Harper, Stalnaker and Pearce [1981] and Jackson [1991]. Adams [1975] is the classic text for probabilities of conditionals (though the view traces back to Ramsey [1929]). A similar logic, though on a very different basis, was devised by Stalnaker [1968, 1975], the account is briefly discussed in chapter 5.2 below. Lewis [1976b] is the classic "bombshell" paper, developed in his [1986b]. The embedding problem for the no-proposition theory is interestingly discussed in an exchange between Kolbel [2000] and Edgington [2000]. Eels and Skyrms [1994] contains some advanced material.