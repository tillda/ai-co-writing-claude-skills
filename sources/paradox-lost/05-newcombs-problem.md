---
book: "Paradox Lost"
title: "Chapter 05 Newcomb's Problem"
chapter_number: "5"
chapter_name: "Newcomb's Problem"
author: "Michale Huemer"
table_of_content: |
  5.1 The Paradox
  5.2 Objections to the Scenario
  5.3 The Right Expected Utility Principle
    5.3.1 The Right Way to Make Good Things More Likely
    5.3.2 Two-Boxing Maximizes Expected Utility: Doing the Math
    5.3.3 Why This Is the Best Solution
  5.4 The Case of Perfect Reliability
  5.5 Rationality and Long-Run Benefit
    5.5.1 One-Boxers as a Group Do Better
    5.5.2 One-Boxers Tend to Do Better in any Given Case
    5.5.3 One-Boxers Do Better in Repeated Games
    5.5.4 Being a One-Boxer Is Predictably Advantageous
  5.6 Uncertainty About Decision Theory
    References
---

# 5. Newcomb's Problem

Michael Huemer

(1) Philosophy Department, University of Colorado Boulder, Boulder, CO, USA

Michael Huemer

## 5.1 The Paradox

Scientists have just invented a wonderful device for predicting human behavior.1 Here is how it works. First, scientists scan a person's brain with a state-of-the-art brain scanner, which records the configuration of all the dendrites, axons, neurotransmitters, and such. They feed this information into a powerful computer, along with a precise description of a possible situation that a person could be in. The computer takes this information, does some ridiculously complicated calculations, and figures out what a person with the specified brain configuration would most likely do in the specified situation. Based on extensive testing with a wide variety of subjects, the prediction system has been found to be 90% reliable: 90% of the time, if the person whose brain was scanned is placed in the relevant situation, the person does what the machine predicted.

<span class="mathjax_ignore">Yesterday, your brain was scanned, so that you might participate in an experiment involving the prediction machine. You are placed in front of two boxes, box A and box B. Box A definitely has &#36;1000 in it. Box B contains either &#36;1 million or nothing. You are offered a choice: you may take either box B, or both A and B. So far, this might seem like an easy choice: if you take both boxes, you get &#36;1000 more than if you take only B.</span>

Wait, there is one more piece of information to consider. Yesterday, after scanning your brain, the scientists gave the computer a description of the choice you are presently facing (including the information you are now being presented with) and asked it to predict what you would do. If the machine predicted that you would take only box B, then the scientists put $1 million in box B. (They have a lot of funding.) If the machine predicted that you would take both boxes, then (just to mess with you) they put nothing in box B. With all that in mind, how should you choose?


<span class="mathjax_ignore">There are two plausible answers. First answer: Take both boxes. Box B contains either &#36;0 or &#36;1 million. If it contains &#36;0, then you are in effect choosing between &#36;0 and &#36;1000. If it contains &#36;1 million, then you are choosing between &#36;1,000,000 and &#36;1,001,000. Either way, the optimal choice is the same. &#36;1000 is better than &#36;0, and &#36;1,001,000 is (slightly) better than &#36;1,000,000, so either way, two boxes are better than one.</span>

<span class="mathjax_ignore">Second answer: Take only B. The correct choice is the one that maximizes your expected gain. Expected gain is a mathematical construction found by adding up the possible amounts that you stand to gain from a given course of action, weighted by the probability of each possibility. For simplicity, assume that you only care about money, and that your wellbeing increases linearly with your wealth (so, ignore the diminishing marginal value of money). If you take only B, there is a 90% chance that the machine would have correctly predicted this, so that there will be &#36;1 million in box B. There is only a 10% chance that the machine will have made an error, in which case you will get &#36;0. So your expected gain from taking only box B is:</span>

$$(\text{The probability that B will contain \$1 million if you choose only B})(\text{Your profit if it contains \$1 million}) + (\text{The probability that B will contain \$0 if you choose only B})(\text{Your profit if it contains \$0})$$

$$= (0.9)(1,000,000) + (0.1)(0) = 900,000$$

<span class="mathjax_ignore">If, on the other hand, you take both boxes, then there is a 90% chance that the machine would have correctly predicted this, so box B will prove empty, and you will get only &#36;1000. There is a 10% chance that the machine will have made an error, and there will be &#36;1 million in box B, in which case you will get &#36;1,001,000. So your expected gain from taking both boxes is:</span>

$$(\text{The probability that B will contain \$1 million if you take both boxes})(\text{Your profit if it contains \$1 million}) + (\text{The probability that B will contain \$0 if you take both boxes})(\text{Your profit if it contains \$0})$$

$$= (0.1)(1,001,000) + (0.9)(1000) = 101,000$$

900,000 is much greater than 101,000, so take only box B.

It seems, then, that we have a conflict between two widely accepted principles of rational choice:

The Dominance Principle : Suppose you are given a choice between $x$ and $y$. Suppose you know that for every possible current state of the world, $s$, if $s$ obtains, then $x$ is better than $y$. In that case, the rational choice is $x$.

Expected Utility Maximization: The rational choice in any situation is the one with the highest expected utility, where this is calculated by multiplying, for each possible outcome, the probability that the outcome will occur if you take that choice by the benefit you will receive if that outcome occurs, and then summing these products for all outcomes. Thus, for example, a 10% chance of getting ten units of good is exactly as good as a 100% chance of getting one unit.

The Dominance Principle supports taking both boxes. Expected Utility Maximization supports taking only box B.²

## 5.2 Objections to the Scenario

Some consider this scenario unrealistic. Human beings are complicated creatures; furthermore, we have free will, which (arguably) means that our actions are not fully determined by causes occurring prior to the moment of choice. It is unlikely that scientists could create a prediction machine that was 90% reliable. And, however reliable the prediction machine might be, it is also unrealistic that there would be a single number representing its reliability across all conditions, regardless of whom the machine was applied to, what the choice situation was, or how many options the agent had available to them. There are some who are bothered by such unrealism and who have an aversion to contemplating such scenarios or answering questions about what would occur in them. If you are among them, this section is for you.

One way of replying to the concern would be to insist that it does not matter if the scenario is unrealistic, because there can still be an answer to what one should do in a highly unrealistic situation. That would be the standard philosophical response, but if you needed a response in the first place, you probably won't like that one.

Here is a more satisfying response: Let's make the scenario more realistic. Let's grant that people have free will, and thus that it is never possible to predict human behavior with perfect accuracy. Nevertheless, free will certainly does not imply that people are maximally unpredictable – it does not mean that in any given circumstance, you are equally likely to do anything that you're capable of doing. (If that were so, life would be crazy.)

So the scientists have made a computer algorithm. It looks at a variety of pieces of information, including such things as neurotransmitter levels, past behavior, and scores on personality tests. Different bits of this information are relevant to different choice scenarios, and the scientists have done a great deal of experimentation to fine tune the algorithm, adjusting the weights for different situations, and so on. The algorithm has been found to be between 53% and 75% reliable at predicting human choices, across a wide variety of situations in which it has been tested out. These situations include the Newcomb scenario – the scientists have already given the Newcomb problem to a random sample of 1000 other people, and the machine correctly predicted most of those people's choices. The algorithm's reliability also varies according to characteristics of the person whose choices it is used to predict, including the person's age, IQ, personality type, and so on.


After thoroughly reviewing all the experimental evidence, you estimate that the machine should be about 60% reliable at predicting the choices of people like you, give or take a few percentage points, in circumstances like the one you are now in.

<span class="mathjax_ignore">Now you sit down to do your expected utility calculation. If you take one box, there is about a 60% chance that the prediction algorithm will have correctly predicted this, and you'll get &#36;1 million. If you take both boxes, there is about a 60% chance that the algorithm will have correctly predicted that, and you'll get &#36;1,000. You thus calculate the expected values as follows:</span>

Given 60% reliability:

Expected utility of taking one box: (.6)(1,000,000) + (.4)(0) = 600,000

Expected utility of taking two boxes: (.6)(1,000) + (.4)(1,001,000) = 401,000

So it looks like your expected utility is higher if you take one box.

But since you're still not sure of your reliability estimate, you decide to calculate the break-even point – the level of reliability such that "one-boxing" (taking one box) and "two-boxing" (taking both boxes) would have equal expected utility. It turns out that this point is 50.05%:

Given 50.05% reliability:

Expected utility of taking one box: (.5005)(1,000,000) + (.4995)(0) = 500,500

Expected utility of taking two boxes: (.5005)(1,000) + (.4995)(1,001,000) = 500,500

If the prediction algorithm is more than 50.05% reliable, then you get more expected utility by taking one box. If it is less than 50.05% reliable, then you get more expected utility by taking two boxes. Having looked at the research on the device, you are extremely confident that the algorithm is more than 50.05% reliable for cases relevantly like yours. I take it that now no one will claim that this is an unrealistic supposition.

But at the same time, the old dominance reasoning still applies: if you take both boxes, you get whatever is in box A (which was already determined yesterday) plus $1000.

## 5.3 The Right Expected Utility Principle

### 5.3.1 The Right Way to Make Good Things More Likely

In his original discussion, Nozick presented the problem, as I have above, as a conflict between the Dominance Principle and the principle of Expected Utility Maximization. If those two principles are really in conflict, then we have a serious intellectual problem, since both principles seem correct; more precisely, both clearly seem to capture a certain type of rationality, instrumental rationality. The best solution to the paradox would be one that somehow reconciles the two principles of rational choice, showing how Expected Utility Maximization really recommends the same course of action as Dominance reasoning.

This can in fact be done. The solution maintains that one-boxers (the people who think you should take only box B) are misunderstandings the notion of probability in expected utility maximization. We can all agree that, in some sense, if an action makes it more likely that you will get something you want, then that counts as a reason in favor of the action; if it makes it less likely that you will get what you want, that counts as a reason against. Expected Utility Maximization is just a more precise and general formulation of that intuition.

Here is the mistake the one-boxers appear to be making: they read "makes it more likely" as meaning "gives you evidence". So they think that if your performing act A would give you evidence that something you want will happen, then that counts as a reason in favor of A. This point of view is called "evidential decision theory". In the Newcomb problem, if you decide to take one box instead of two, the fact that you are making that choice gives you evidence that the machine predicted that you would so choose, which means there is probably a million dollars in box B. So the one-boxers think that you are "making it more likely" that there is a million dollars in box B.

In fact, however, rational agents do not endeavor to give themselves evidence that their ends will be realized; rational agents endeavor to cause their ends to be realized (which usually has the side effect of giving themselves evidence that their ends will be realized). This point of view is known as "causal decision theory". In the Newcomb problem, if you decide to take one box instead of two, this has no chance at all of causing there to be a million dollars in box B, so you have no reason to take one box instead of two.

To elaborate: The prediction machine scanned your brain yesterday. For simplicity, suppose there is a brain configuration $b_1$ that tends to cause people to choose only one box in Newcomb's problem, and another brain configuration $b_2$ that tends to cause people to choose both boxes. The prediction machine makes its prediction based upon which of those states it detects. At the time your brain was scanned, it was in either $b_1$ or $b_2$. Since it is impossible to change the past, it makes sense to treat that state as fixed. That means that you should calculate expected utilities given each possible brain configuration that you might have had yesterday.

Now, if your brain was $b_1$, then there is $1 million in box B, and that will (with certainty) continue to be true whether you now choose one box or two. If, on the other hand, your brain was in $b_2$, then there is nothing in box B, and that will (with certainty) continue to be true whether you choose one box or two. So the probability of your getting the $1 million is just the probability that your brain was in $b_1$ yesterday.

The one-boxer argument turns on the claim that you are more likely to get the $1 million if you take one box than if you take two. For the reason just explained, that is not true. Let's say that, since you have no idea what state your brain was in yesterday, you consider it 50% likely that it was in $b_1$ and 50% likely that it was in $b_2$. Then the probability of your getting the million dollars if you take one box is 50%. And the probability of your getting the million dollars if you take both boxes is also 50%.

Now, having gone through that reasoning (if you were persuaded by that), you have just learned something about yourself: that you are the sort of person who accepts the two-box reasoning. So now you might be more confident that your brain was in fact in $b_1$ yesterday. Let's say you are now 90% confident that your brain was in $b_1$ yesterday. If you like, you can redo the expected utility calculation using this new probability. Now the probability of your getting the million dollars if you take one box is 10%, and the probability of your getting the million dollars if you take both boxes is 10%. But the probability of your getting the thousand dollars is zero if you take one box, and 100% if you take both. So again, you should take both. In the relevant sense, taking both boxes makes you more likely (in fact, 100% likely) to get the thousand dollars and does not make you any less likely to get the million dollars.

Why is this the correct sense of "making more likely"? Because this is the sense that matters to one who is trying to bring about good things, and not merely to produce evidence of good things. Since you know that your past brain state, whether it was $b_1$ or $b_2$, cannot now be changed, the relevant question is whether, given that brain state (and more generally, given all the things that you cannot affect), taking one box will make you more likely to get what you want.

### 5.3.2 Two-Boxing Maximizes Expected Utility: Doing the Math

Taking the above points into account, we can reformulate the principle of expected utility maximization. Earlier, we said that the rational choice is the one with the highest expected utility, where the expected utility of a choice is calculated by multiplying, for each possible outcome, the probability that the outcome will occur if you make that choice by the benefit you will receive if that outcome occurs, and then summing these products for all outcomes. In other words,

$$
\begin{aligned}
\mathrm{EU}(A) &= \mathrm{P}(O_1 | A) \cdot \mathrm{V}(O_1) + \mathrm{P}(O_2 | A) \cdot \mathrm{V}(O_2) + \dots \\
&= \sum_{i} \mathrm{P}(O_i | A) \cdot \mathrm{V}(O_i)
\end{aligned}
$$

where $\mathrm{EU}(A)$ is the expected utility of choice $A$; the possible outcomes of the choice are $O_1, O_2, O_3$, and so on; $\mathrm{P}(O_i|A)$ is the probability of $O_i$ occurring given that you do $A$; and $\mathrm{V}(O_i)$ is the value to you of outcome $O_i$.

How should we modify this to take account of the reasoning of section 5.3.1 above? Here is a way: we should understand “$\mathrm{P}(O_i|A)$” as denoting the probability-weighted average value of $\mathrm{P}(O_i|A)$ given each of the alternative hypotheses about how the fixed facts about the world might be.

In other words: let's refer to all the things that you cannot affect as "the fixed world". There are many ways that the fixed world could be; call them $W_1$, $W_2$, $W_3$, and so on. Then the proper value of $\mathrm{P}(O_i|A)$ to use in an expected utility calculation is

$$
\begin{aligned}
&\mathrm{P}(O_i | A, W_1) \mathrm{P}(W_1) + \mathrm{P}(O_i | A, W_2) \mathrm{P}(W_2) + \mathrm{P}(O_i | A, W_3) \mathrm{P}(W_3) + \dots \\
&= \sum_{j} \mathrm{P}(O_i | A, W_j) \mathrm{P}(W_j)
\end{aligned}
$$

Plugging this into the formula for expected utility:

$$\mathrm{EU}(A) = \sum_{i} \mathrm{V}(O_i) \cdot \mathrm{P}(O_i | A) = \sum_{i} \left( \mathrm{V}(O_i) \cdot \sum_{j} \mathrm{P}(O_i | A, W_j) \mathrm{P}(W_j) \right)$$

<span class="mathjax_ignore">On this understanding of Expected Utility Maximization, here is how we should assess the expected utilities in Newcomb's problem. The possible outcomes of the scenario are that you get &#36;0, that you get &#36;1000, that you get &#36;1,000,000, and that you get &#36;1,001,000. We assume for simplicity that the value you get from each outcome is just equal to the amount of money you get. Then:</span>

Expected utility from taking one box

= (0)(Probability of getting $0 if you take one box)

+ (1000)(Probability of getting $1000 if you take one box)

+ (1,000,000)(Probability of getting $1,000,000 if you take one box)

+ (1,001,000)(Probability of getting $1,001,000 if you take one box)

The first term cancels since it is something multiplied by zero. The second and fourth terms are both zero, since there is no chance of winding up with either 1,000 or 1,001,000 if you take one box. So the above reduces to

(1,000,000)(Probability of getting $1,000,000 if you take one box)

$$ = (1,000,000)[P(B_1)(\text{Probability of getting } \$1,000,000 \text{ if you take one box, given } B_1) + P(B_2)(\text{Probability of getting } \$1,000,000 \text{ if you take one box, given } B_2)] $$

= (1,000,000)[P(B₁)(1) + P(B₂)(0)]

= 1,000,000 · P(B₁)

where B₁ is the proposition that your brain was in state b₁ yesterday, and B₂ is the proposition that it was in state b₂. Next, we find the expected utility from taking two boxes:

Expected utility from taking two boxes

= (0)(Probability of getting $0 if you take two boxes)

+ (1000)(Probability of getting $1000 if you take two boxes)

+ (1,000,000)(Probability of getting $1,000,000 if you take two boxes)

+ (1,001,000)(Probability of getting $1,001,000 if you take two boxes)

The first term is zero. The third term is also zero since there is no way of getting exactly $1,000,000 if you take both boxes. So the above reduces to

(1,000)(Probability of getting $1,000 if you take two boxes)

+ (1,001,000)(Probability of getting $1,001,000 if you take two boxes)

$$= (1,000)[P(B_1)(\text{Probability of getting \$1,000 if you take two boxes, given } B_1) + P(B_2)(\text{Probability of getting \$1,000 if you take two boxes, given } B_2)]$$

$$+ (1,001,000)[P(B_1)(\text{Probability of getting \$1,001,000 if you take two boxes, given } B_1) + P(B_2)(\text{Probability of getting \$1,001,000 if you take two boxes, given } B_2)]$$

= (1,000)[P(B₁)(0) + P(B₂)(1)]

+ (1,001,000)[P(B₁)(1) + P(B₂)(0)]

= 1,000 · P(B₂) + 1,001,000 · P(B₁)

Since B₁ and B₂ are the only alternatives in this scenario, P(B₂) = 1 - P(B₁). So the above reduces to

= 1,000(1 - P(B₁)) + 1,001,000 · P(B₁)

= 1000 + 1,000,000 · P(B₁)

These formulas give the expected utilities in terms of P(B₁), the probability that your brain was in b₁ when it was scanned yesterday. But it does not matter what this probability is, because whatever it is, 1000 + 1,000,000 · P(B₁) is greater than 1,000,000 · P(B₁). So taking two boxes gives more expected utility than taking one box.

For illustration: suppose that at the start of your deliberations, you have no opinion about whether your brain was in $b_{1}$ or $b_{2}$, so you assign probability $\frac{1}{2}$ to each alternative. Then the calculated expected utilities would be 500,000 for taking one box, and 501,000 for taking both boxes. So you should take both boxes.

But after doing these calculations, you become pretty sure that you are going to choose both boxes, and you also become pretty sure that there is going to be nothing in box B. So you lower $P(B_1)$ to, say, $10\%$, and raise $P(B_2)$ to $90\%$. If you like, you can then redo the calculations using these new probabilities: now the expected utilities are 100,000 for taking one box and 101,000 for taking both boxes. This is disappointing, but you should still take both boxes.

### 5.3.3 Why This Is the Best Solution

Intuitively, expected utility maximization and dominance reasoning are both rational. This is a reason for thinking that they are not truly in conflict. In fact, the Dominance Principle seems as if it ought to be a special case of Expected Utility Maximization – namely, the case where you know for certain which act will give you greater actual utility (not merely expected utility). In that special case, surely Expected Utility Maximization ought to recommend that one take the act that in fact maximizes utility – surely that is in accord with our intuitive understanding of what the principle is getting at.

All this is to say that, if there is an interpretation of the two rational choice principles that reconciles them, then, other things being equal, we should prefer that interpretation over one that makes them incompatible. The account given above reconciles the two principles. Evidential decision theory does not – it requires us to simply reject the Dominance Principle. So we should prefer causal decision theory over evidential decision theory.

## 5.4 The Case of Perfect Reliability

<span class="mathjax_ignore">Now consider a variation on the Newcomb case. Imagine that the scenario is as described before, except that the machine is not merely &#36;90\%&#36; but &#36;100\%&#36; reliable. It never makes an error. Many, even among those who prefer two boxes in the original case, think that surely in this case you should take one box.</span>

<span class="mathjax_ignore">But, it appears, the above reasoning says otherwise: even in the case of &#36;100\%&#36; reliability, you should still take two boxes. The dominance argument still applies: either box B contains &#36;\&#36;1&#36; million, or it contains nothing. If it contains &#36;\&#36;1&#36; million, then you should take both boxes, since you will then get &#36;\&#36;1,001,000&#36; instead of &#36;\&#36;1,000,000&#36;. If it contains nothing, then you should take both boxes, since you will then get &#36;1,000 instead of nothing. So you should take both boxes. As you go through this reasoning, you realize with a sinking feeling that box B is in fact empty. This doesn't dissuade you from taking both boxes, though, since you now know that the best you can do is to get the thousand dollars.</span>


This is also the way to maximize your expected utility. The expected utilities are, again, as follows:

Expected utility from taking one box: 1,000,000 · P(B₁)

Expected utility from taking two boxes: 1000 + 1,000,000 · P(B₁)

The latter is still larger than the former. Nothing has changed, because the reliability of the device did not appear anywhere in the calculations.

And the argument about causal versus evidential probabilities still applies. Choosing one box now gives you conclusive evidence that you will get $1 million. But it still cannot cause this result, since the million dollars was already placed in the box yesterday. Choosing two boxes gives you conclusive evidence that box B is empty, but, again, it cannot cause this to be the case. So by the reasoning of section 5.3.1, you still have no reason to choose one box instead of two.

You might think this is a problem. Surely in the 100% reliability case, you should take one box. Since the standard two-boxer arguments apply in the 100% reliability case just as much as they apply in the 90% reliability case, that just shows that the standard two-boxer argument s must be wrong. Or so one might claim.

I don't think that's correct. My diagnosis: normal methods of prediction could plausibly be highly reliable, but not 100% reliable. There are only two ways in which a prediction device could be 100% accurate. The first is if all our actions are entirely pre-determined. The machine knows what we are going to do because, given the antecedent causes, that is the only thing we can do. However, if this is the case, then there is no free will, and if there is no free will, then deliberation doesn't make sense (we cannot rationally deliberate on the assumption that we have no choice about anything), and it makes no sense to speak of what choice one "should" make.[10]

The second way a prediction device could be 100% accurate would be if there is backwards causation, that is, a person's decision at a given time somehow reaches into the past and causes the machine to predict that very decision.

This, I suppose, is how crystal balls and other forms of precognition are supposed to work (they would work this way if they worked). When you see an ordinary object, this works by the object's causing you to have a sensory experience of it. Analogously, when you "see" the future (if you could do so), this would work by the future events' causing you to have an experience representing them. This ability of course would not have to be 100% reliable. But in order to be 100% reliable, in a world where the future isn't predetermined, you would have to have some such ability to be affected by the future.


But in this case, the reasoning for taking two boxes no longer applies, since it is no longer true that you cannot affect the past prediction. If you take one box, that could cause there to be a million dollars in that box – not by causing the money to suddenly appear there now, but by causing the money to have been put there yesterday.

So, if the machine is 100% reliable due to backwards causation, then you should take one box. If the machine is 100% reliable because everything is predetermined, then you have no free will, in which case it does not make sense to discuss what you should or should not do. If the machine could somehow be 100% reliable without either backwards causation or determinism, then you should still take both boxes. However, this last alternative is not really possible.

The case of the merely 90% reliable predictor does not face this problem, because a machine might be 90% reliable without backwards causation or determinism. Assuming that that is the case, our earlier reasoning in favor of two boxes applies.

## 5.5 Rationality and Long-Run Benefit

### 5.5.1 One-Boxers as a Group Do Better

Here is another argument for one-boxing. Our conception of rationality should have some connection with being better off or having one's goals better satisfied. (Let's assume that our only goal is to be better off, so that these two notions of rationality, as promoting one's interests and as promoting one's goals, will coincide. This isn't true in general, but it could be true of some agents.) Of course, it need not be that rational people always wind up better off, since even the most rational people are sometimes fooled, and even the best laid plans sometimes go awry. But there ought to be a general tendency for the rational to be better off.

Newcomb gives us a scenario in which one-boxers typically wind up better off than two-boxers. This isn't just an occasional accident, like someone who foolishly spends his life savings on the lottery and then luckily wins. It is systematic and predictable. If you watch a large group of one-boxers and a large group of two-boxers go into a Newcomb choice situation, you know that the one-boxers, on average, are going to come out well ahead. This might tempt us to think that it is the one-boxers, after all, who are the rational ones. We might even be tempted to define rationality in terms of whatever ways of thinking and choosing systematically tend, in the long run, to get agents what they want.

I think this line of thinking does not really make any progress over the original one-box argument. The scenario in which you track a large group of one-boxers and a large group of two-boxers, and the one-boxers wind up better off, fails to support one-boxing, because rationality is not about trying to satisfy the goals of your group. It is about trying to satisfy your own goals.

There are other well-known cases in which a group of rational individuals systematically does worse than a group of non-rational individuals. Consider the Prisoner's Dilemma, in which each of two people has a choice between two actions, "cooperating" and "defecting".[11] If one player cooperates while the other defects, then the defector gets the best available outcome while the cooperator gets the worst. If both cooperate, then both get the second-best outcome. If both defect, then both get the second-worst outcome. The payoffs are shown in the following table ("1,4" means player 1 gets 1 unit of good while player 2 gets 4, etc., where larger numbers are better):

|  Player #1 | Player #2  |   |   |
| --- | --- | --- | --- |
|   |   | Cooperate | Defect  |
|   |  Cooperate | 3, 3 | 1, 4  |
|   |  Defect | 4, 1 | 2, 2  |

By stipulation, both players want to get higher numbers for themselves, and that is all they care about. In this case, the rational choice for each is to defect; this is generally accepted in decision theory. To figure out what Player 1 should do, first suppose Player 2 will cooperate. Then Player 1 should defect, since doing so will give him 4 units of benefit instead of 3. Now suppose Player 2 will defect. Then again, Player 1 should defect, since doing so will give him 2 units instead of 1. So either way, Player 1 is better off defecting, and this is all he cares about. Parallel reasoning shows that Player 2 is better off defecting. Thus, both players, if rational, wind up defecting and getting the 2-unit payout.

If both players instead cooperate, then they are irrational. However, groups of people who are irrational in that particular way will reliably tend to end up better off (getting 3-unit payouts instead of 2) when playing Prisoner's Dilemma with each other, than groups who are rational. This does not show that cooperating is really rational, because, again, rationality (in the sense we're concerned with here) is not about making the group of like-minded people better off. It is about making yourself better off.

### 5.5.2 One-Boxers Tend to Do Better in any Given Case

In reply, one might say the issue is not really about what happens in a large collection of cases. The point is simply that in each case, one-boxers are more likely to walk away with a million dollars than two-boxers are; the fact that one-boxers as a group do better in the long run is just a symptom of the fact that they are more likely to do better in any given case.

This, however, is nothing but a repeat of the original argument for one-boxing: the claim that taking one box makes you more likely to get the million dollars. We have already explained above why this is false. In the relevant sense, taking one box instead of two has no effect on your chances of getting the million.

### 5.5.3 One-Boxers Do Better in Repeated Games

<span class="mathjax_ignore">One might propose a case in which a single individual is going to participate in many Newcomb choices. If you repeat the Newcomb choice a thousand times, then you will come out, overall, with about &#36;900 million if you are a consistent one-boxer, and only &#36;101 million if you are a consistent two-boxer. Doesn't this show that one-boxers are more rational?</span>

But two-boxers can reasonably argue that this is a different choice situation. Because the game is repeated, it is possible for your choice in any given iteration (except the last) to affect what happens in a future iteration. It is plausible that if you choose one box the first time, this might cause you to get $1 million the next time. Perhaps choosing the one box will put your brain into the state of a one-boxer's brain, so the next time it is scanned, the machine will predict a one-box choice.

<span class="mathjax_ignore">To avoid this argument, we might suppose that your brain is scanned only once at the beginning, and this one scan is the basis for the machine's predictions in all subsequent cases where you play the game. In that case, according to causal decision theory, you should always pick both boxes, since you cannot affect the machine's predictions. But people who do so wind up repeatedly getting only &#36;1,000 instead of &#36;1 million. Does this, finally, show that there is something wrong with my conception of rationality?</span>

I don't think it does. Here is the more fundamental reply to all the arguments of this sort. It is possible to cook up an unusual scenario that rewards irrationality. Here is a simple one: a machine scans your brain to find out whether you have any intransitive preferences or not. If you do, then the scientists operating the machine reward you with $1 million. If you have only transitive preferences, then they beat you up. In this scenario, people with intransitive preferences wind up, systematically and predictably, much better off than people with only transitive preferences. But that hardly shows that intransitive preferences are rational.

In case you think intransitive preferences actually are rational,^{12} you can change the example to use any other common criterion of irrationality – the sunk cost fallacy, hyperbolic discounting, even self-contradiction.^{13} The criteria for rationality could be as uncontroversial as any ever are. A machine scans your brain to see whether you are guilty of these errors, and then someone rewards you if you are. Predictably and systematically. Surely this does not show that the sunk cost fallacy, hyperbolic discounting, and inconsistency are rational.

### 5.5.4 Being a One-Boxer Is Predictably Advantageous

Here is another try at the one-box argument: Being the sort of person who would choose one box in Newcomb’s problem is clearly advantageous, as such people tend to walk away rich. Furthermore, being this sort of person clearly does cause you to receive the money. It is because you are this sort of person in general (which means you are, in general, in brain state $b_1$) that the machine predicts that you will choose one box, and that gets you the $1 million. So if you can decide what sort of person to be, you clearly should decide to be a one-boxer. Having done so, you will choose one box in the Newcomb situation.

The standard analysis of this, which I endorse, is as follows: there are two distinct decision theoretic questions: (i) If given the choice between one box and two boxes in the Newcomb scenario, which should I choose? (ii) If given the choice, before my brain is scanned, between being a one-boxer and being a two-boxer, which should I choose? The answer to (i) is “two boxes”. The answer to (ii) is “one-boxer”. These are two different scenarios, so it is perfectly consistent to give this pair of answers. That is, if I know in advance that I am going to be in a Newcomb situation some time in the future, and if I can control my own dispositions and attitudes, then I should work on turning myself into the sort of person who would take one box. That is consistent with the fact that, if I am now in a Newcomb situation, and my brain has already been scanned (so it is too late to develop the brain state that would have caused the machine to predict one box), then I should now choose two boxes.

One-boxers might nevertheless argue that there is a tension between these views about the two choice problems. For one might argue:

1. It is rational to be a one-boxer (that is, to be the sort of person who would choose one box in Newcomb’s scenario).

2. If $x$ is rational, and $x$ entails $y$, then $y$ is rational.

3. Being a one-boxer entails choosing one box if one is in the Newcomb scenario.

4. Therefore, it is rational to choose one box if one is in the Newcomb scenario.

What is wrong with that argument? One objection is that the premises fail to specify the times at which traits or choices are rational. Let's say that you are told in advance about the Newcomb situation that you are going to face. At $t_1$, your brain is being scanned. Later, at $t_2$, you are asked to pick either one box or two. Then it is rational at $t_1$ to be a one-boxer (if you can). But being a one-boxer at $t_1$ does not entail choosing one box at $t_2$, since by $t_2$, you might have lost the disposition. So we can coherently maintain that it is rational to be a one-boxer at $t_1$ but then to choose two boxes at $t_2$.

One might be tempted to posit a disposition so robust that it cannot later be changed. Assume that you can control whether you have such a disposition at $t_1$, and the machine will detect whether you have it. Then it would be rational to adopt that disposition. By stipulation, this is incompatible with your later changing in such a way that you would take two boxes at $t_2$. This gets around the preceding objection. However, it opens up the objection that, if the disposition is truly unalterable, then the agent has no control over his action at $t_2$, in which case principles of rational choice fail to apply – there is no meaningful question about what an agent should do in a situation in which the agent cannot control his behavior.

Here is a more general objection to the one-boxing argument. The preceding argument for the rationality of one-boxing could be applied to any paradigm form of irrational behavior. Suppose a machine scans your brain to detect whether you are prone to the sunk cost fallacy. If you are, you get a great reward. It would be rational (if possible, and if you are not already like this) to make yourself the sort of person who falls prey to the sunk cost fallacy. Suppose you could cultivate a disposition so firm that it could not later be changed, and that only such a disposition will get you the reward. Then we could argue:

1'. It is rational in this scenario to make oneself prone to the sunk cost fallacy.

2'. If $x$ is rational, and $x$ entails $y$, then $y$ is rational.

3'. Being prone to the sunk cost fallacy entails making decisions based on that fallacy when given the opportunity.

4'. Therefore, making decisions based on the sunk cost fallacy when given the opportunity is rational.

(The conclusion here can be understood as conditional on the supposition that you initially face the scenario in which you are to be rewarded for having the unalterable disposition to commit the sunk cost fallacy – just as the conclusion in the one-boxer's argument above must be understood as conditional on the supposition that you are given advance notice that you will face a Newcomb choice.) Again, the argument could be adjusted to conclude that any paradigm form of irrationality is actually rational (in the scenario imagined) – hyperbolic discounting, acting on intransitive preferences, acting on contradictory beliefs, and so on. I take that to be a reductio ad absurdum of the argument.

Where did the reasoning go wrong? The false step is premise 2, "If $x$ is rational, and $x$ entails $y$, then $y$ is rational." It could be rational to cause yourself to later behave irrationally, say, because, as in the above scenarios, someone will reward you for the later irrationality. That is not a contradictory supposition.

What would make the later action irrational? Wouldn't the mere fact that the later action flowed from an earlier rational choice render the later act rational too? No. The later action might be irrational because, say, it violates the Dominance Principle, or it fails to maximize the agent's expected utility at the later time, or it commits the sunk cost fallacy, etc.

## 5.6 Uncertainty About Decision Theory

Let's take a final variant on the Newcomb situation. In this variant, box B still contains either  $1 million or nothing, but box A only contains a dollar. Everything else is as before. Does this alter what we should choose?

Now it seems much more tempting to go for one box. Who cares if you miss out on one measly dollar? To be clear, a dollar has some value – if you saw one on the street, you'd pick it up. But its value is very low.

But the arguments for two-boxing still apply. As long as a dollar is worth something, two boxes dominate one box: if there is nothing in box B, then you're choosing between $0 and $1; if there is $1 million in box B, then you're choosing between $1,000,000 and $1,000,001. $1 is better than $0, and $1,000,001 is better than $1,000,000. So either way, you should take both boxes. Similarly, according to section 5.3.2, the expected utility of taking one box is $1,000,000 \times P(B_1)$, and the expected utility of taking two boxes is $1 + 1,000,000 \times P(B_1)$. The latter is greater.


So in terms of the theoretical arguments, this scenario is no different from the original version of the Newcomb choice situation. But it seems different; it seems rational to take one box in this new scenario.

Here is my account of this. I believe the account of rational choice that I gave earlier. Nevertheless, I am not 100% certain of it. I think the one-boxers are very probably wrong, but I am not dogmatic about this – I concede that there is a chance they might be right.

On my preferred account of rational choice, taking two boxes in the new Newcomb situation (the one with $1 in box A) is very slightly better than taking one box – namely, by a margin of one expected dollar. But on the alternative account (the one-boxers' view), taking one box is much better than taking two – namely, by a margin of 799,999 expected dollars. Since I am to some degree uncertain about the right theory of rational choice, I should give some weight to both theories, proportional to my confidence in each. But then, even a very small uncertainty about my account of rational choice enables the possible advantage of one-boxing to outweigh that of two-boxing, when the apparent advantage of two-boxing is so small.

<span class="mathjax_ignore">Consider the following situation: suppose there is a lottery with a prize of &#36;1 million. There are ten tickets, exactly one will win, and the tickets cost &#36;1. Should I buy one? I will probably lose money if I do. But I should still buy a ticket if I care about money, because buying a ticket gives me a very large expected monetary profit.</span>

Similarly, even though taking two boxes probably has greater expected utility than taking one box, I should still take one box if I care about expected utility, since the expected expected utility of taking one box is higher. Expected expected utility is a mathematical construct used for decision-making in cases where you are uncertain of the correct account of expected utility. Expected expected utility is found by adding up, for each possible theory of rational choice, the expected utility of an action according to the theory, weighted by the epistemic probability of the theory itself being correct.

Admittedly, something about this reasoning is weird. It looks like there are now three theories of rational choice in play:

R₁ Causal decision theory: The rational choice is the one that maximizes expected utility, calculated as described in section 5.3.2.

R₂ Evidential decision theory: The rational choice is the one that maximizes expected utility, calculated using evidential probabilities, as in section 5.1.

R_{3} Maximize EEU: The rational choice is the one that maximizes expected expected utility (EEU), calculated by taking a weighted average of the expected utilities of an action according to each viable theory of rational choice, weighted by the probabilities of the theories.

These seem to be three incompatible theories: they all name different criteria for rational choice, which could diverge in some cases. So if R_{3} is correct, then R_{1} and R_{2} are both false. And if, hypothetically, I were completely convinced that R_{3} was correct, then I’d have to assign probability zero to R_{1} and R_{2}. Then, when I tried to apply R_{3}, I’d have to assign zero weight to R_{1} and R_{2}, which of course leaves the EEU undefined. Surely this is not right.

This puzzle can be resolved by introducing a distinction between ideal rationality and bounded rationality. Ideal rationality is what an ideal rational agent – one with unlimited intelligence, reasoning abilities, and understanding of all relevant reasons – would practice. Bounded rationality is what a being like us should practice, given our various imperfections.^{14}

To illustrate, suppose I am playing chess. Suppose that on move 63, the move pawn to e6 on my part would in fact put me in a position to ultimately win the game, even with perfect play by my opponent. However, I am not aware of this fact at the time; it will only be revealed after the game when we analyze the position using computers. Furthermore, suppose that, as of move 63, I am short on time and in danger of losing to my opponent on time. I consider moving pawn to e6, but I realize that it would take me several minutes to think through the consequences of that move. So I reject it and focus on moves that are easier to think through but which (later analysis will reveal) do not enable me to force a win.

Now, in some sense, pawn to e6 was the correct move, the move I “should have” made in my position. At the same time, there is another sense in which I was rational to reject that move. Roughly speaking, an ideal player would have moved pawn to e6, but I would not have been wise to do this, given my known limitations.

R_{1} and R_{2}, I take it, are theories of ideal rationality. The ideal rational agent would follow one of them – almost certainly R_{1}, in my opinion. R_{3} is a theory of bounded rationality for beings like us. It tells us to weight the theories of ideal rationality by the probabil-ities we assign to them. My arguments leading up to this section have all been addressed to ideal rationality. Only this section addresses bounded rationality. So it is consistent to hold that R_{1} and R_{3} are both correct in their own domains.^{15}

Can the principle of EEU Maximization (R_{3}) be used to justify choosing one box in the original Newcomb scenario, with the $1,000 in box A? The answer depends on how convincing you find the arguments for causal decision theory, and how much more you value a million dollars than a thousand dollars. In principle, you could well be boundedly rational in choosing one box for this reason, even with a high confidence in causal decision theory. But the ideal rational agent would (very probably) take two.

### References

Huemer, Michael. 2000. "Van Inwagen's Consequence Argument," *Philosophical Review* 109: 524–43. [Crossref]

Lewis, David. 1979. "Prisoners' Dilemma Is a Newcomb Problem", *Philosophy &amp; Public Affairs* 8: 235–40.

Nozick, Robert. 1969. "Newcomb's Problem and Two Principles of Choice", pp. 114–46 in Nicholas Rescher, ed., *Essays in Honor of Carl G. Hempel*. Dordrecht: D. Reidel. [Crossref]

Quinn, Warren S. 1990. "The Puzzle of the Self-Torturer", *Philosophical Studies: An International Journal for Philosophy in the Analytic Tradition* 59: 79–90. [Crossref]

Rachels, Stuart. 1998. "Counterexamples to the Transitivity of Better Than", *Australasian Journal of Philosophy* 76: 71–83. [Crossref]

Sainsbury, Richard M. 2009. *Paradoxes*, 3rd ed. Cambridge: Cambridge University Press. [Crossref]

Simon, Herbert A. 1955. "A Behavioral Model of Rational Choice", *Quarterly Journal of Economics* 69: 99–118. [Crossref]

Skyrms, Brian. 1982. "Causal Decision Theory", *Journal of Philosophy* 79: 695–711. [Crossref]

Footnotes


9.


10


11


12


13


14


15


#### Notes


1. This chapter’s paradox is based on the discussion of Robert Nozick ( [1969]), who credits the physicist William Newcomb.

2. This was Nozick’s ( [1969]) original understanding of the problem.

3. You might object: “But if I give myself evidence that a good thing will happen, then I’ll come to believe the good thing will happen, and this belief will make me feel good. So I do have reason to give myself such evidence after all.” This might be true – but only in virtue of your having an additional goal, beyond having the good thing happen – namely, the goal of making yourself feel good. The only thing you have reason to do merely by virtue of having goal G is to (try to) bring about G. If you also have the goal of believing that G will happen, then that gives you a reason to cause yourself to believe that G will happen (but it does not, e.g., give you any reason to give yourself evidence that you will believe that G will happen, unless you also have a goal of believing that you will believe that G will happen . . . and so on).

4. See Skyrms [1982]; Sainsbury [2009], pp. 81–2 (but note that Sainsbury defends a different version of causal decision theory from that of Skyrms and myself).

5. To be more precise, you can think of $b_{1}$ as a set of brain configurations, namely, those that, when the brain scanner detects one of them, it causes the prediction machine to predict that you will choose one box when placed in the Newcomb choice situation. And similarly for $b_{2}$, mutatis mutandis.

6. To state the point mathematically: $P(M|T_{1} \wedge B_{1}) = P(M|T_{2} \wedge B_{1}) = 1$, and $P(M|T_{1} \wedge B_{2}) = P(M|T_{2} \wedge B_{2}) = 0$, where $M = [\text{Box B contains a million dollars}]$, $T_{1} = [\text{You take one box}]$, $T_{2} = [\text{You take both boxes}]$, $B_{1} = [\text{Your brain was in } b_{1}]$, and $B_{2} = [\text{Your brain was in } b_{2}]$. As we say, the past brain state “screens off” your decision from the question about whether the box contains a million dollars.

7. Here we assume that the $O_{i}$ form a partition and that they include everything that matters to value.

8. Assume that the $W_{i}$ form a partition.

My formula here is mathematically equivalent to Skyrms' (1982, p. 697) formula for expected utility in causal decision theory.

I here assume that determinism is incompatible with free will, which is controversial. For defense of this assumption, see my 2000.

For a stronger parallel between Newcomb's Problem and the Prisoners' Dilemma, see Lewis 1979. Lewis argues that the other player in the Prisoner's Dilemma acts like a sort of "predictor" of one's own behavior, since there is likely to be a nonzero statistical correlation between the choices of the two players; therefore, by cooperating, one gives oneself evidence that the other player will cooperate, though one does not cause the other player to cooperate. Thus, says Lewis, the Prisoners' Dilemma is a kind of Newcomb problem.

Some philosophers think this; see Rachels 1998; Quinn 1990.

The sunk cost fallacy consists of thinking that because you previously expended some resources on option A, you now have a reason for favoring A – for instance, that you should sit through a movie you aren't enjoying, simply because you paid for it. Hyperbolic discounting consists of ascribing drastically more weight to near-term benefits than to longer-term benefits – for instance, spending all night drinking and partying when you have an important exam the next day. You might think the example of self-contradiction does not fit with the others because it is an instance of epistemic irrationality, not practical rationality. If you prefer, assume the example is one of using contradictory assumptions to make choices.

The term "bounded rationality" was introduced by Simon (1955) to describe the sort of approximately-rational decision-making appropriate under conditions of limited knowledge and calculating abilities. I extend the notion to include conditions of ignorance about rational choice theory itself.

This distinction between ideal and bounded rationality is (even) less clean cut than it sounds. Rather than a simple qualitative distinction between idealized and bounded senses of rationality, what we really have is a spectrum of different degrees of idealization in different respects. Almost any rational criticism of an action presupposes some degree of idealization. For instance, we criticize agents for committing the sunk cost fallacy, which is widely taken to be irrational. But one could argue that in some sense, it is rational to commit this fallacy, given the actual limitations of most who commit it, including the fact that they can't see at the time that it is a fallacy.

Of course, you might now wonder what you should do if you are uncertain even about the correct theory of bounded rationality, for instance, if you are uncertain as to whether $R_3$ is correct. But that question is too difficult and confusing to address here.