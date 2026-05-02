---
book: "Paradox Lost"
title: "Chapter 07 The Two Envelopes"
chapter_number: "7"
chapter_name: "The Two Envelopes"
author: "Michale Huemer"
table_of_content: |
  7.1 The Paradox
  7.2 The Use of Probability in the Paradox
    7.2.1 An Objection
    7.2.2 Three Interpretations of Probability
    7.2.3 Rational Choice Uses Epistemic Probabilities
    7.2.4 Probabilities in Causal Decision Theory
  7.3 The Use of Variables in the Paradox
  7.4 The Correct Analysis
    References
    Footnotes
---

# 7. The Two Envelopes

Michael Huemer^{1}

(1) Philosophy Department, University of Colorado Boulder, Boulder, CO, USA

Michael Huemer

## 7.1 The Paradox

A friendly experimenter has approached you and shown you two identical-looking envelopes, envelope A and envelope B.^{1} All you know is that both contain money, and one of them contains twice as much as the other. (Let's say they contain checks, so you can't tell anything from the thickness.) The experimenter offers to give you one of them, whichever one you choose.

Let's say you choose envelope A. She hands it over. But just before you open it to see how much money you got, she says, “Before you open that, would you like to trade it for envelope B?”

Assume that the friendly experimenter has no particular agenda (she is not, for example, trying to get envelope A for herself because she knows what's in it). Her job is to go around offering these envelopes to people, and every time, no matter which envelope the person chooses, she is supposed to ask if they want to trade it for the other. (Why? I don't know; maybe it's an experiment on the endowment effect.^{2})

Should you trade your envelope for the other one? There are three possible answers: (i) “Yes, you should switch”, (ii) “No, you should keep your envelope”, and (iii) “It doesn't matter; you should be indifferent between switching and keeping.”

Most people think the third answer is obviously correct. But here is an argument for the first. The envelope in your hand contains some amount of money. Call this amount $a$. The other envelope contains either $2a$ or $a/2$. Each of those possibilities is equally likely, given your (lack of) information. So if you switch, there is a 50% probability that you will gain $a$ dollars, and a 50% probability that you will lose $a/2$ dollars. The amount you stand to gain is twice as great as the amount you stand to lose. So it's a good bet. Your expected profits from switching and from not switching are as follows:


Switch envelopes:

$$(.5)(2a) + (.5)(a/2) = 1.25a$$

Keep envelope A: $a$

$1.25a$ is greater than $a$, so you should switch.

After you do so, but before you open your new envelope, the experimenter offers you the chance to switch back to the original one. We can construct a similar argument to show that you should switch back. Let $b$ be the amount of money you now have, the amount in envelope B. The other envelope, which you originally chose, contains either $2b$ or $b/2$, with equal probability. So your expected profits are as follows:

Switch back to A:

$$(.5)(2b) + (.5)(b/2) = 1.25b$$

Keep envelope B: $b$

So switch back.

Finally, we can construct an argument that it doesn't matter whether you switch. Let $c$ be the total amount of money in the two envelopes. One of them contains $(1/3)c$ and the other contains $(2/3)c$. Given your (lack of) information, each envelope is equally likely to be the one containing $(1/3)c$. So, whichever envelope you presently have, your expected profits of switching and not switching are as follows:

Switch envelopes:

$$(.5)(2/3c) + (.5)(1/3c) = c/2$$

Keep envelope:

$$(.5)(1/3c) + (.5)(2/3c) = c/2$$

If you switch, you are equally likely to go from $\frac{1}{3}c$ to $\frac{2}{3}c$, or from $\frac{2}{3}c$ to $\frac{1}{3}c$. So it doesn't matter.

This last argument, intuitively, has the correct conclusion. But all three arguments seem parallel. How is it that the first two are wrong and the third correct?

## 7.2 The Use of Probability in the Paradox

### 7.2.1 An Objection

Some who hear the paradox think that the paradoxical reasoning misuses the notion of probability. In calculating the expected utility of switching envelopes, you are supposed to assign 50% probabilities each to the alternatives (i) that you would gain a dollars and (ii) that you would lose a/2 dollars. But one of these alternatives is, in an objective sense, not possible, because the amounts in the two envelopes have already been determined. If envelope B in fact has the greater amount, then there is no real chance of your losing money by switching; if envelope B in fact has the lesser amount, then there is no chance of your gaining money by switching. One of these alternatives is already determinately the case, and you have no chance of altering it. So there is something suspect about the 50% probabilities assigned to the two alternatives.

### 7.2.2 Three Interpretations of Probability

The above objection is not correct; the paradoxical reasoning does not misuse the concept of probability. To see this, let us first consider how probability can be understood. Several interpretations of probability appear in the literature; here are three prominent ones:

i. Epistemic Probability: The epistemic probability of a proposition for a particular person is the degree to which that person's evidence supports the proposition, or the degree of justification the person has for the proposition. A proposition with probability 1 is a proposition that one has conclusive justification for accepting; a proposition with probability 0 is a proposition that one has conclusive justification for rejecting. Note that epistemic probability is relative to an individual and depends on that individual's current information.

ii. Subjective Probability (a.k.a. credence): The subjective probability of a proposition for a particular person is the degree of confidence the person actually has in that proposition (whether or not this confidence is justified). A proposition with probability 1 is one of which the person is absolutely convinced. Subjective probability, like epistemic probability, is relative to an individual.

iii. Propensity: The propensity of an event is the degree to which the causally relevant factors have a tendency to produce that event. An event with probability 1 is one that must happen; it could not be avoided. Also, if an event has already occurred, its propensity is 1, since it cannot be altered. Note that propensities are objective and not relative to individuals. An event has a particular propensity independent of what we believe or know and independent of whether there are any people around at all.

These are commonly accepted as three distinct, legitimate senses of "probability". (It does not matter which of these, if any, best matches the meaning of "probability" in English. We are not here to debate semantic questions.)

### 7.2.3 Rational Choice Uses Epistemic Probabilities

In rational choice theory, it is commonly held that the rational choice is the one that maximizes the agent's expected utility, where the expected utility of an action is calculated by adding up, for every possible result of the action, the probability that the result would occur if one performed the action times the value to the agent of that result.

What is the correct interpretation of probability here? By that, I mean: what is the interpretation that makes Expected Utility Maximization a correct principle of rational choice?

The answer is either epistemic or subjective probability (but only, I think, if your subjective probabilities are rational, in which case they are hard to distinguish from epistemic probabilities). The answer is not propensity.

<span class="mathjax_ignore">Why not propensity? Consider what I shall call the Simple Envelope Case. In this case, you are presented with two indistinguishable envelopes, with only the information that one contains &#36;2 and the other &#36;4. (Assume that you care only about money, and you value &#36;4 twice as much as &#36;2.) This time, there is no question about switching. The question is simply: which envelope should you take? There are three answers: (i) you should take the one on the left, (ii) you should take the one on the right, (iii) it doesn't matter; you should be indifferent between the two envelopes.</span>

The correct answer is of course (iii). How could that answer come out of an expected utility calculation? Here is how: since we have no evidence favoring either envelope to be the one containing the $4, each envelope has a 50% epistemic probability of containing $2, and a 50% probability of containing $4. So the expected value of the envelope on the left is $(.5)(\$2) + (.5)(\$4) = \$3$; similarly, the expected value of the envelope on the right is $3.

<span class="mathjax_ignore">But in this case, just as in the original two-envelope case in section 7.1, the amounts in the envelopes have already been determined. So one of the envelopes has a 100% propensity to contain the &#36;2, and the other has a 100% propensity to contain the &#36;4. Neither has any 50% propensity. So, if decision theory used propensities rather than epistemic probabilities, then the above argument would be an error, and the two envelopes would not have the same expected value.</span>

### 7.2.4 Probabilities in Causal Decision Theory

In our discussion of Newcomb’s Paradox in chapter 5, we learned that the correct interpretation of the probabilities in expected utility calculations is the interpretation offered by causal decision theory, rather than evidential decision theory. This is because rational agents seek to cause good outcomes, not merely to have evidence of good outcomes.

You might think this conflicts with the conclusion of section 7.2.3. Doesn’t causal decision theory hold that we must use causal probabilities rather than evidential probabilities? And doesn’t that mean that we should not use epistemic probabilities as I just claimed?

No, it doesn’t. Despite the name, the probabilities used in causal decision theory are still epistemic or subjective. They are not propensities, frequencies, or any other sort of physical probabilities. What is “causal” about causal decision theory is not the type of probabilities that are used, but what the probabilities are applied to. In one version of causal decision theory (which we have not discussed), the probabilities are applied to subjunctive conditionals. In my version of causal decision theory, from section 5.3.2, the expected utility of an action is defined as follows:

$$\mathrm{EU}(A) = \sum_{i} \mathrm{V}(O_{i}) \cdot \mathrm{P}(O_{i} | A)$$

where the O_{i} are the possible outcomes of your action, V(O_{i}) is the value you receive if outcome O_{i} occurs, and P(O_{i}|A) is the probability of O_{i} occurring if you do A. That conditional probability, in turn, is calculated as follows:

$$\mathrm{P}(O_{i} \mid A) = \sum_{j} \mathrm{P}(O_{i} \mid A, W_{j}) \cdot \mathrm{P}(W_{j})$$

where the $W_{j}$ are the possible ways the unalterable world might be (the sets of circumstances that you cannot affect). The notion of causation comes in in identifying those circumstances. It does not enter into the interpretation of probability. All of the probabilities in the above two equations are epistemic probabilities.

The reason for this is that an agent cannot rationally be criticized for what the actual effects of their actions are or would have been per se; they can only be rationally criticized for what they had reason to believe about what those effects would be. Hence, in decision theory, causation should only enter into the contents of the propositions to which one assigns epistemic probabilities.

## 7.3 The Use of Variables in the Paradox

The expected utility calculation for switching envelopes,

$$\mathrm{EU}(\text{switch}) = (.5)(2a) + (.5)(a/2) = 1.25a$$

appears confused. The expected utility of a particular action is a specific quantity. "a" is a variable, not the name of a specific quantity; hence, "1.25a" does not name a possible value for the expected utility of anything.

<span class="mathjax_ignore">The actual expected utility of switching (more precisely, the expected monetary payout, which we're using as a proxy for utility) would be calculated by adding up, for each possible dollar value that one might get, the probability of getting that amount multiplied by the amount. In this calculation, one must plug in the specific dollar amounts, &#36;1, &#36;2, and so on.</span>

You might object: "But a is a specific quantity. By stipulation, it is the amount of money in envelope A, whatever that is. This amount is unknown, but that does not prevent it from being a specific amount."

Okay. But the argument claims that the expected dollar payout of keeping your own envelope is $a$, and that of the other envelope, $1.25a$. So now the claim is that the expected dollar amount in your envelope is equal to the amount that is actually in the envelope, whatever that is. For example, if (unbeknownst to you) there is actually $1 in your envelope, then the expected payout of your envelope is $1; if there is actually (unbeknownst to you) $100 in it, then the expected payout is $100.

This is false. The expected value of a variable, by definition, is determined by the information you have available to you (more specifically, by your epistemic probabilities); it is not determined by whatever is the actual value of the variable.

Assume for simplicity that the envelopes must contain integer dollar values. Then the expected amount of money in envelope A is:

$$\$1 \cdot P(A_1) + \$2 \cdot P(A_2) + \$3 \cdot P(A_3) + \ldots$$

where $P(A_1)$ is the probability that envelope A contains \$1, $P(A_2)$ is the probability that it contains \$2, and so on. The value of this sum depends on your probability distribution, but it is very unlikely to equal the actual amount that is in the envelope; indeed, it is unlikely even to be one of the possible amounts.

Consider this analogy: the average number of children for an American family is 1.87. So if you pick a random American family, 1.87 is the expected value of the variable "number of children in the family". But that is never the actual value – no family has 1.87 children. Similarly, the expected monetary value of envelope A is (almost certainly) not its actual value.

On this diagnosis, the argument for switching given in section 7.1 is badly confused. So is the argument for keeping your envelope, and so is the argument that it doesn't matter. The argument that it doesn't matter gets the correct conclusion, but it does so by means of the same conceptual confusion as the other two arguments.

So what is the correct analysis?

## 7.4 The Correct Analysis

Again, assume for simplicity that the envelopes must contain integer dollar amounts. The expected utility calculation for an action starts by listing the possible ways that the unalterable world might be, that is, the circumstances that are beyond your control. One assigns a probability to each of these circumstances. Then, for each of these circumstances, one assesses how much benefit one would gain if that circumstance obtains and one performs the action in question. In the case of switching or keeping one's original envelope, then, one could make the following table³:

|  Possible Circumstance | Probability | Payout if you keep | Payout if you switch  |
| --- | --- | --- | --- |
<span class="mathjax_ignore">|  A contains &#36;1, B contains &#36;2 | p1 | &#36;1 | &#36;2  |</span>
| --- | --- | --- | --- |
<span class="mathjax_ignore">|  B contains &#36;1, A contains &#36;2 | p2 | &#36;2 | &#36;1  |</span>
<span class="mathjax_ignore">|  A: &#36;2, B: &#36;4 | p3 | &#36;2 | &#36;4  |</span>
<span class="mathjax_ignore">|  B: &#36;2, A: &#36;4 | p4 | &#36;4 | &#36;2  |</span>
<span class="mathjax_ignore">|  A: &#36;3, B: &#36;6 | p5 | &#36;3 | &#36;6  |</span>
<span class="mathjax_ignore">|  B: &#36;3, A: &#36;6 | p6 | &#36;6 | &#36;3  |</span>
|  : | : | : | :  |

I have left the probabilities as “$p_1$”, “$p_2$”, and so on, because I don’t know what these probabilities should be. They have to be some series of numbers for which the (infinite) sum is 1. Fortunately, we won’t need the exact numbers. Here is the important point: The first circumstance in the table (“A contains \$1, B contains \$2”) is identical to the second (“B contains \$1, A contains \$2”), except that A and B have been switched. But the two envelopes are indistinguishable, and you have no different information about the one than about the other. It seems that you should assign the same probabilities to any two circumstances that differ only in that “A” and “B” have been interchanged. So you should assign probabilities such that $p_1 = p_2$, $p_3 = p_4$, $p_5 = p_6$, and so on. Note: you should not assign $p_1 = p_3$, $p_3 = p_5$, and so on. Circumstances involving different total amounts of money do not have the same probabilities; larger amounts are generally less likely to be in the envelopes than smaller amounts (for example, it is highly unlikely that someone is going to give you a check for \$1 billion).

The expected utilities of switching and of keeping your envelope are calculated as follows, based on the above table:

$$EU(\text{keep}) = (p_1)(\$1) + (p_2)(\$2) + (p_3)(\$2) + (p_4)(\$4) + \cdots$$

$$EU(\text{switch}) = (p_1)(\$2) + (p_2)(\$1) + (p_3)(\$4) + (p_4)(\$2) + \cdots$$

Since $p_1 = p_2$, and $p_3 = p_4$, and so on, this reduces to:

$$
\text{EU}(\text{keep}) = (p_1)(\$1) + (p_1)(\$2) + (p_3)(\$2) + (p_3)(\$4) + \dots
$$

$$\text{EU}(\text{switch}) = (p_1)(\$2) + (p_1)(\$1) + (p_3)(\$4) + (p_3)(\$2) + \dots
$$

The expressions on the right hand sides of those two equations are identical, only with the terms slightly rearranged.⁴ So the expected value of switching and of keeping your envelope are the same. So it doesn't matter if you switch.

Now you might ask: don't the above equations commit the putative error mentioned at the start of section 7.3, that of using variables in place of numbers? "$p_1$", "$p_3$", and so on, are variables, not names of specific quantities. Therefore, the right hand sides of the above equations are not possible expected values.

In reply: Yes, these are variables rather than specific values, but no, that isn't a problem. Granted, the above equations don't tell us what the expected values are, unless and until we figure out what $p_1$, $p_3$, and so on are, plug those in, and then do the calculations. But this is okay. We didn't need to know what the expected values are of switching and of keeping your envelope. All we wanted to know was: which has more expected value? No matter what values you plug in for $p_1$, $p_3$, and so on, the above two sums will be equal to each other. Different people can reasonably use different probabilities, depending on how generous they think the experimenter might be. All will still agree that it doesn't matter whether you switch envelopes.

### References

Clark, Michael. 2002. *Paradoxes from A to Z*. London: Routledge.

Kraitchik, Maurice. 1942. *Mathematical Recreations*. New York: W.W. Norton.

Thaler, Richard. 1980. "Toward a Positive Theory of Consumer Choice", *Journal of Economic Behavior and Organization* 1: 39–60. [Crossref]

### Footnotes

1


#### Notes


This chapter's paradox derives from Kraitchik 1942, pp. 133–4. The original version concerned a pair of neckties: persons A and B each own a necktie; each knows the value of his own tie but not that of the other person. They have a chance to make a deal whereby a third party will judge the quality of the ties, and the person with the superior tie will have to give his tie to the other. Each reasons that he will either lose his tie, or gain a better tie (with equal probability?); since the potential gain is greater than the potential loss, the deal is to his advantage. Kraitchick then discusses a version involving sums of pennies.

2. This is the phenomenon where people value something more merely because they presently have it (Thaler 1980, pp. 43–7).

3. Cf. Clark’s (2002, p. 204) parallel table and analysis.

4. Rearrangement can sometimes make a difference in infinite sums. However, in this case, assuming that the probabilities sum to 1, the two infinite sums on the right hand sides will come to the same amount.