---
book: "Understanding Knowledge"
title: "Chapter 14 SCIENTIFIC KNOWLEDGE"
chapter_number: "14"
chapter_name: "SCIENTIFIC KNOWLEDGE"
author: "Michael Huemer"
table_of_content: |
  14.1. Confirmation Puzzles
    14.1.1. The Idea of Confirmation Theory
    14.1.2. Does Everything Confirm Everything?
    14.1.3. The Ravens Paradox
    14.1.4. Bayesian Analysis
  14.2. Falsifiability
    14.2.1. The Idea of Falsificationism
    14.2.2. The Origin of Falsificationism
    14.2.3. A Bayesian Account of the Virtue of Falsifiability
  14.3. Simplicity
    14.3.1. Occam's Razor and the Burden of Proof
    14.3.2. Why Accept Occam's Razor?
    14.3.3. What Shouldn't We Multiply?
    14.3.4. Seven Weak Defenses of Simplicity
    14.3.5. The Likelihood Account
    14.3.6. Philosophical Applications
  14.4. Realism &amp; Skepticism
    14.4.1. The Underdetermination Problem
    14.4.2. Scientific Anti-Realism
    14.4.3. A Realist Interpretation
    14.4.4. The Skeptical Induction
  14.5. Why Isn't Everyone a Bayesian?
    14.5.1. The Problem of Old Evidence
    14.5.2. The Probability of the Laws
    14.5.3. The Problem of Priors
  14.6. Conclusion
---

# 14. SCIENTIFIC KNOWLEDGE

In this part of the book, we discuss some areas of knowledge that have attracted particular philosophical attention. We start with scientific knowledge: How does it work, what makes a scientific theory a good one, and do we really know our scientific theories to be true?

The main issue about scientific knowledge is really the problem of induction, which we have already discussed (ch. 12). Here we will address some further issues about scientific reasoning that are also interesting.

## 14.1. Confirmation Puzzles

### 14.1.1. The Idea of Confirmation Theory

In the philosophy of science, people try to figure out how scientific reasoning works to produce knowledge, or at least justified beliefs. It is common to use the word “confirms” to mean “provides at least some amount of support for”. E.g., the observation of a white raven confirms [All ravens are white] (albeit only slightly!). Please note that this is a technical use of “confirm” and that “confirm” does not mean “to provide conclusive evidence for”!

So one thing we’d like is a theory of when some evidence, <em>e</em>, confirms some hypothesis, <em>h</em>. In the twentieth century, some people tried to articulate qualitative conditions for this, and it led to paradoxes.[133]

### 14.1.2. Does Everything Confirm Everything?

Here are two plausible qualitative conditions for confirmation:

1. If <em>h</em> entails <em>e</em>, then <em>e</em> confirms <em>h</em>.

**Comment:** Scientific method tests theories by testing their observational predictions, i.e., the things that the theory entails about what we should observe in particular circumstances. When a prediction is found to be true, that counts as support for the theory.


2. If <em>e</em> confirms <em>h</em>, and <em>h</em> entails <em>x</em>, then <em>e</em> confirms <em>x</em>.

Comment: If you have evidence for a theory, then you thereby also have at least some evidence for the other things that that theory predicts.

You might want to add some qualifications to condition (1), e.g., that <em>e</em> can't be a tautology. This eliminates the problem where a hypothesis would be confirmed by any tautology (since everything entails a tautology). We could also stipulate that <em>h</em> cannot be contradictory; this eliminates the case where a contradictory hypothesis would be confirmed by any evidence (since a contradiction entails anything). We could add similar qualifications to condition (2); these qualifications are not important to the problem we're about to discuss.

Here is the problem: Conditions (1) and (2) entail that every proposition confirms every other proposition (with minor qualifications, if you want). Let <em>A</em> and <em>B</em> be any two randomly chosen (non-tautological, non-contradictory) propositions. Note that (<em>A</em> & <em>B</em>) entails <em>A</em>. Therefore, by condition (1), <em>A</em> confirms (<em>A</em> & <em>B</em>). Now, since (<em>A</em> & <em>B</em>) entails <em>B</em>, by condition (2), <em>A</em> also confirms <em>B</em>. That seems wrong, to put it mildly.

### 14.1.3. The Ravens Paradox

Here are two more plausible conditions on confirmation:

I. Nicod's Criterion: [134]

a. Observation of an <em>A</em> that is <em>B</em> confirms [All <em>A</em>'s are <em>B</em>].

b. Observation of an <em>A</em> that is non-<em>B</em> disconfirms [All <em>A</em>'s are <em>B</em>].

c. Observation of a non-<em>A</em> is irrelevant to (neither confirms nor disconfirms) [All <em>A</em>'s are <em>B</em>].

II. The Equivalence Condition: If <em>p</em> and <em>q</em> are logically equivalent, then whatever confirms <em>p</em> confirms <em>q</em>.

I take condition II to be self-evident. To illustrate condition I, if you see a black raven, that supports "All ravens are black." If you see a white raven, that refutes "All ravens are black." And if you see a white shoe, that is irrelevant to "All ravens are black."

Problem: Let's think about that white shoe again. It isn't black, and it also isn't a raven. That is, it is a nonblack nonraven. So by condition Ia, it confirms "All nonblack things are nonravens." But "All nonblack things are nonravens" is logically equivalent to "All ravens are black." So by condition II, it actually is evidence for “All ravens are black.” But this contradicts condition Ic.


### 14.1.4. Bayesian Analysis

The leading responses (which are also the correct responses) to the above problems are probabilistic. First, Bayesians define confirmation in terms of raising the probability of a theory:

**Bayesian Account of Confirmation:**

e confirms h =<sub>df</sub> P(h|e) &gt; P(h).

Now we can analyze the proposed qualitative conditions of confirmation in terms of probability theory.

**“If <em>h</em> entails <em>e</em>, then <em>e</em> confirms <em>h</em>”:** This is true as long as P(<em>e</em>) and P(<em>h</em>) have non-extreme (neither 0 nor 1) probabilities. You can see this from Bayes’ Theorem: P(<em>h</em>|<em>e</em>) = <em>P</em>(<em>h</em>) × <em>P</em>(<em>e</em>|<em>h</em>)/<em>P</em>(<em>e</em>). Since <em>h</em> entails <em>e</em>, P(<em>e</em>|<em>h</em>) is 1. Assuming P(<em>e</em>) is less than 1, P(<em>e</em>|<em>h</em>)/P(<em>e</em>) is going to be greater than 1, so the whole right hand side is greater than P(<em>h</em>), so P(<em>h</em>|<em>e</em>) > P(<em>h</em>).

**“If <em>e</em> confirms <em>h</em>, and <em>h</em> entails <em>x</em>, then <em>e</em> confirms <em>x</em>”:** This is definitely false. Evidence may raise the probability of a theory but fail to raise, or may even lower, the probability of some of the theory’s consequences. To take an intuitive example, let’s say you know that either Jon, Sue, or Mike stole some money from the cash register during the lunch hour. Then you view a security video which shows Mike peacefully eating a salad during the time that the money was stolen, so it could not have been Mike. This evidence confirms that it was Jon, and also confirms that it was Sue (i.e., it raises the probability of both of those hypotheses). But note that [It was Jon] entails that it wasn’t Sue. So the evidence confirms a hypothesis ([It was Jon]) while also lowering the probability of a logical consequence of that hypothesis ([It wasn’t Sue]).

**“If <em>p</em> and <em>q</em> are logically equivalent, then whatever confirms <em>p</em> confirms <em>q</em>”:** This is correct. It’s a theorem of probability that logically equivalent propositions always have the same probability (including the same probability conditional on any chosen evidence).

**“Observation of an <em>A</em> that is <em>B</em> confirms [All <em>A</em>’s are <em>B</em>]”:** This is typically true, but it depends upon how the observation was made. Say there’s a giant bag labelled “Ravens”, and another giant bag labelled “Black Things”. You can reach in and randomly pick an object from either bag. If you pick a random raven from the raven bag and it turns out to be black, that confirms [All ravens are black]. But if you pick a random black thing from the Black Things bag, and it turns out to be a raven, that's irrelevant to [All ravens are black],[135] since you knew in advance that you had no chance of getting a nonblack raven from that bag, even if nonblack ravens existed.


"Observation of an A that is non-B disconfirms [All A's are B]": Obviously true.

"Observation of a non-A is irrelevant to [All A's are B]": Again, this depends on how the observation was made. Say there's a giant bag of Nonblack Things and a giant bag of Nonravens. If you randomly sample from the Nonblack Things and get a white shoe, then yes, that does support [All ravens are black] because, if there were nonblack ravens, there was a chance that this observation would have turned one up. Since it didn't, you have a tiny bit of evidence that there aren't any nonblack ravens (it's tiny since nonblack ravens would be such a small portion of the set of all nonblack things that you'd have been very unlikely to find one). On the other hand, if you randomly sample from the Nonravens and you turn up a white shoe, that's irrelevant to [All ravens are black] since this method had no chance of turning up a nonblack raven.

## 14.2. Falsifiability

### 14.2.1. The Idea of Falsificationism

Many people today believe that scientific method has a lot to do with falsifiability. It is said that any scientific theory must be capable of being tested so that, if it were false, we could prove that it was false. People are often criticized for advancing "unfalsifiable" theories, which is generally treated as in some way fallacious or otherwise bad. This view is popular not only among lay people but also among scientists. To illustrate the idea:

The Elusive Psychic: Uri claims to have psychic powers. You propose to do some scientific tests to determine whether this is true. Uri then explains that the psychic powers don't work in the presence of skeptics. Hence, if you do your tests, the psychic powers won't show up; nevertheless, he insists, they are perfectly real.

---

You would probably see Uri for the scammer that he is. Methodologically, the problem is that Uri has designed his theory so as to make it untestable, or at least very hard to test, which makes it unscientific.

### 14.2.2. The Origin of Falsificationism

The source of this view of science is the 20th-century philosopher of science, Sir Karl Popper. Few people who use his idea, however, know what motivated it. Popper's fundamental motivation was inductive skepticism: He thought David Hume was right and thus that there is never any reason whatsoever to believe any scientific theory.

By the way, even though he is completely explicit about it, many people who have been exposed to Popper fail to realize that that is his core view. There are two main reasons for this. First, Popper's emotional attitude toward science is highly positive, which comes out in his writing; second, inductive skepticism is so ridiculous that people have a hard time believing that Popper means it when he says it. So in case you don't believe me, I have collected a few quotations from Sir Karl:

"We must regard all laws and theories as guesses." "There are no such things as good positive reasons." "Belief, of course, is never rational: it is rational to suspend belief." "I never assume that by force of 'verified' conclusions, theories can be established as 'true', or even as merely 'probable'." "[O]f two hypotheses, the one that is logically stronger, or more informative, or better testable, and thus the one which can be better corroborated, is always less probable—on any given evidence—than the other." "[I]n an infinite universe [...] the probability of any (non-tautological) universal law will be zero."[136]

Now, after deciding that non-deductive reasoning is completely impotent, Popper didn't want to just throw out science. So he had to come up with a way that scientific method is somehow based on deduction. And what he came up with was this: Even though it's impossible to establish any scientific theory by deduction, it is possible to refute a scientific theory by deduction. No amount of evidence ever proves that all swans are white; yet a single observation of a black swan deductively proves that not all swans are white. Popper concluded, therefore, that science must all be about refuting theories, rather than about confirming them. That led him to posit that a theory is unscientific if it could not in principle be refuted.


Now, you might be thinking that once a scientific theory survives many attempts to refute it, we will then have a reason to believe it, or that the theory will be rendered more probable, or something like that. But that is not Popper's view. He explicitly rejects that; no matter what, you never have any reason to believe a scientific theory.

All of which raises the question: Why on Earth would we care about science? And what, exactly, is good about falsifiable theories?

### 14.2.3. A Bayesian Account of the Virtue of Falsifiability

Popper was onto something with his emphasis on falsifiability: Unfalsifiable theories really are bad in some way, and that principle really is important to scientific reasoning. (This observation applies to empirical theories in general but not to a priori "theories", such as most philosophical theories.) Unfortunately, Popper was in no position to explain why this is the case, because he explicitly rejects all non-deductive reasoning.

The correct account of the virtue of falsifiability is probabilistic. A falsifiable theory is, in essence, a theory that makes definite, non-trivial predictions about the evidence that we should expect to see. If the predictions turn out false, the theory is refuted. On the other hand, if the predictions turn out true, then the theory is supported in accordance with Bayes' Theorem:

P(h | e) = \frac{P(h) \times P(e | h)}{P(e)}.

Since <em>h</em> predicts <em>e</em>, P(<em>e</em>|<em>h</em>) = 1. As long as <em>e</em> is something non-trivial, P(<em>e</em>) should be less than 1. So on the right-hand side of the equation, you have P(<em>h</em>) multiplied by something greater than 1, which gives you something greater than P(<em>h</em>). Thus, a falsifiable theory is confirmed (has its probability raised) when it survives a test that could have refuted it.

On the other hand, suppose <em>h</em> makes no predictions at all and is therefore untestable. In that case, the theory is also unsupportable. It's a general theorem of probability that P(<em>h</em>|<em>e</em>) > P(<em>h</em>) if and only if P(<em>h</em>|~ <em>e</em>) < P(<em>h</em>). [137] On the Bayesian account of confirmation, this amounts to saying: <em>e</em> confirms <em>h</em> if and only if ~ <em>e</em> would disconfirm <em>h</em>. So a theory that can't be disconfirmed can't be confirmed.

Note, however, that the Bayesian would broaden the concept of falsifiability. Popper, being an inductive skeptic, defines falsifiability in terms of being able to deductively prove that a theory is false. The Bayesian would (rightly) employ the broader notion of being able to disconfirm (lower the probability of) the theory. Thus, a good scientific theory must make at least probabilistic predictions, such that the probability of the theory could be raised or lowered by evidence gathered. The sharper the predictions are (that is, the higher  P(<em>e</em>|<em>h</em>)  for specific values of  <em>e</em> ), the more confirmable or disconfirmable the theory is.


## 14.3. Simplicity

### 14.3.1. Occam's Razor and the Burden of Proof

It is widely agreed in scientific reasoning and much of ordinary life that, other things being equal, the simplest explanation of some evidence is most likely to be correct. This, or something close to it, is often dubbed Occam's Razor. The other common statement of the Razor is "entities must not be multiplied beyond necessity."[138] A closely related idea is the burden of proof principle, which states that the burden of proof is on those who make positive claims; the presumption rests with negative claims. Here, a positive claim is understood as one asserting that something exists or that something has some property, whereas a negative claim denies that something exists or that something has some property.

As conventionally understood, these principles postulate an epistemological asymmetry between positive and negative claims. In the absence of specific evidence either for or against the existence of some particular thing, the negative thesis (that it doesn't exist) is held to be somehow privileged—more reasonable to believe, more reasonable to have a higher credence in, more reasonable to assume for practical purposes, or something like that. For a randomly chosen possible thing, the default assumption, so to speak, is that it doesn't exist.

### 14.3.2. Why Accept Occam's Razor?

Before we talk about why Occam's Razor might be true, or even what exactly it means, let's get the motivation for it. That way, we can interpret and explain the principle in a way consistent with that motivation.

The main reason for believing something like Occam's Razor is that there are various examples in which the appeal to simplicity is very intuitively compelling. Perhaps the most famous case is that of Copernican (geocentric) vs. Ptolemaic (heliocentric) astronomy. Back in the  16<sup>th</sup>  century, people were debating the structure of the cosmos. The old, Ptolemaic theory had the Sun and the planets all moving around the Earth. Copernicus proposed instead that the Sun is stationary and the Earth and planets orbit the sun.


![img-0.jpeg](img-0.jpeg)

Figure 7: Ptolemaic model of a planetary orbit

It turns out that, in the Ptolemaic system, in order to explain the observed positions of planets in the night sky, you have to complicate your model a bit. You can't just have each planet moving in a circle with the Earth at the center. Rather, the Earth is located off center within those orbits. There was no theoretical explanation for this; the distance of the Earth from the center was just posited to get the right observational predictions. The other, more famous complication was the epicycle: Rather than moving in a simple circle around the Earth, the planets were held to be moving in smaller circles called "epicycles", where the epicycle itself would move around the Earth (fig. 7).

The Copernican model did not require any such epicycles, nor did it place anything off center (the sun was at the center of the cosmos). It thus gave a simpler explanation of the same set of observations. This greater simplicity has long been considered an important advantage of the Copernican theory. Indeed, the term "epicycle" has become a pejorative term for ad hoc complications that someone adds into a theory to try to save the appearances.

It's useful to have a few examples of different types, so here's another case, also from astronomy. The way that Neptune was discovered was that astronomers first noticed some anomalies in the orbit of Uranus—it wasn't moving in exactly the way expected based on Newton's laws and the theory of gravity. The astronomer Urbain Le Verrier figured out that these anomalies could be explained if one posited a hitherto-unobserved planet whose mass was influencing Uranus. This turned out to be correct, and the new planet is now known as Neptune. Now, when Le Verrier wanted to explain the anomalies, he could have posited six unknown planets, or seventy-three, or any other number. But he didn't do any of these things, nor would any normal person have done so, given that a single planet of the right mass and orbit was sufficient to explain the data.


A similar case is the discovery of the neutrino. The neutrino was originally postulated in order to explain an apparent loss of energy that occurs in beta decay (never mind exactly what that is)—basically, the physicist Wolfgang Pauli proposed that the energy that appeared to be lost was carried away by a new, previously-unobserved particle produced during beta decay.[139] That particle was subsequently detected and named the "neutrino". Notice that Pauli could have postulated that during beta decay, seventy-three different kinds of particle are produced, each of which carries away some of the lost energy. That would also have explained the data. But no one would have seriously entertained such a theory, given that a single theoretical particle would suffice to explain the same evidence.

I have one more example, this one from ordinary life. Let's say you're sitting in your apartment, in which you have exactly two electrical devices turned on: a lamp and a computer. Suddenly, both the lamp and the computer shut off. You consider two hypotheses: (i) Maybe there was a power failure, or (ii) maybe the light bulb burned out and the computer crashed at the same time. It seems that the simpler explanation, (i), is the more likely.

### 14.3.3. What Shouldn't We Multiply?

Some say that we should strive to minimize the number of individual entities whose existence we postulate. Others say that we should strive to minimize the number of kinds of entity that we postulate. And still others say that we should strive to minimize the number of adjustable parameters in our theories. Adjustable parameters are essentially numbers whose values could be adjusted (consistent with intuitively still having "the same theory") to try to accommodate the available data. For instance, the gravitational constant in Newton's theory of gravity is an adjustable parameter.

All three of these are natural interpretations of the value of simplicity, and all three are illustrated in the preceding examples. The Neptune example illustrates the virtue of minimizing the number of individual entities (sometimes called “quantitative parsimony”). The neutrino example illustrates the virtue of minimizing the number of types of entities (a.k.a. “qualitative parsimony”). And the Copernican Astronomy example illustrates the virtue of minimizing the number of adjustable parameters in a theory. In the Copernican model, you have the radius and speed of each orbit as adjustable parameters. In the Ptolemaic model, you have the radius and speed of the main orbit, plus the radius and speed of each epicycle, plus the distance of the Earth from the center. The computer/lamp example also illustrates this kind of simplicity. The power failure theory has one adjustable parameter, the time of the power failure. The burnout/crash theory has two parameters, the time of the light bulb burnout and the time of the computer crash.


This suggests that all three kinds of simplicity matter for assessing theories. We should avoid multiplying individuals, kinds, or parameters beyond necessity.

### 14.3.4. Seven Weak Defenses of Simplicity

Although almost everyone accepts the theoretical virtue of simplicity at least in some contexts, most people (even philosophers!) have no clue why simplicity is a theoretical virtue, which of course puts one in a poor position to judge when it is a theoretical virtue. Let’s start by considering some accounts of this that are wrong.

**Account #1: The world is simple.**

On the face of it, when you hear the statement “other things being equal, simpler explanations are better”, it sounds as if the principle is that we get to assume, a priori, that the world is probably simple. But why on Earth would that be? I certainly don’t think that the world is probably simple; I think it is probably extremely complex. Over the history of science, our accounts of the world have steadily grown more complex as they have become more accurate. Modern physics is way more complicated than Aristotelian physics.

Nobody seems to be able to explain why it makes sense to assume the world is probably simple, so let’s consider some other explanations.

**Account #2: It is impossible to prove a negative.**

If a thing doesn’t exist, then there won’t be any (positive) evidence left behind by its non-existence. This is supposed to show that the burden of proof must lie on those who assert the positive, since a negative claim in principle couldn't be proved.


There are just two problems with this account. First, it's false. You can sometimes prove a negative. If there is no beer in my refrigerator, I can prove this by doing an exhaustive search of the refrigerator. Some people claim to have proved that God doesn't exist by pointing to contradictions in the concept of God.

Second, it's irrelevant even if true. Just because a claim could not be proved false does not mean that it is true. So why would we get to start by assuming negative claims?

**Account #3: (A &amp; B) is less likely than A.**

This is a theorem of probability: As long as P(<em>B</em>|<em>A</em>) ≠ 1, P(<em>A</em> & <em>B</em>) must be strictly less than P(<em>A</em>). Therefore, if you can explain all your evidence by citing <em>A</em>, you should not go on to assert <em>B</em> in addition, because that lowers the probability of your theory.

Problem: This fails to identify any asymmetry between positive and negative claims. The following is also a theorem of probability: As long as P(<em>B</em>|<em>A</em>) ≠ 0, P(<em>A</em> & ~ <em>B</em>) is strictly less than P(<em>A</em>). Therefore, if you can explain all your evidence by citing <em>A</em>, you should not go on to deny <em>B</em> in addition, since that lowers the probability of your theory. The argument against affirming <em>B</em> is also an argument against denying <em>B</em>. So it does not support any kind of burden of proof or presumption for one side.

Note also that the account, even if it worked, would only apply to a small minority of cases. Though people often appeal to simplicity to justify preferring one theory over another, virtually never is one theory equivalent to the conjunction of another theory with some other proposition.

**Account #4: We're just saying don't believe unjustified propositions.**

Sometimes, people explain Occam's Razor as the trivial principle that if there is no justification for believing a positive claim, then one should not believe that claim. This is entirely consistent with the (presumably equally correct) principle that if there is no justification for denying a positive claim, then one also should not deny it.

The only thing to be said about this is that this isn't a defense of Occam's Razor or a burden of proof principle, since this view posits no asymmetry between positive and negative claims or between simple and complex theories. The view would be that entities should not be posited or denied unnecessarily; negative claims would have just as much burden of proof as positive claims.


Account #5: Simple theories are convenient and pretty.

Sometimes people propose simplicity as a pragmatic virtue: Simpler theories are easier for us to understand and work with. They might also be more aesthetically pleasing.

The problem is that the pragmatic/aesthetic benefits of simplicity would typically be swamped by the value of truth. We use non-deductive inferences to plan our actions all the time, where what matters is whether our conclusions are true. When you're building a bridge, you want your predictions about how much weight it supports to be correct. How aesthetically pleasing or convenient the calculations are is an utterly trivial consideration by comparison.

And indeed, we do not merely think that our theories are aesthetically pleasing or convenient. We clearly think of them as true (at least we think their predictions about future observations are true), given how much we use them to plan our actions. In the examples from §14.3.2, the simpler theories clearly seem more likely to be true. For instance, when your lamp and your computer both shut off, it is more likely that there was a power failure rather than that the bulb burned out at the same time that the computer crashed. That is what needs to be explained.

Account #6: There are fewer simple theories.

Maybe the world isn't more likely to be simple than complex. Maybe it's equally likely to have each possible degree of complexity, but there are generally more complex theories than there are simple theories. (Example: You're trying to solve a burglary case, and you could hypothesize either one burglar or three. With three burglars, there would be many more ways to fill in how the whole crime might have happened.) Thus, each particular simple theory gets a higher prior probability than each complex theory.

The main problem with this account is that we don't have a clear rationale for applying the Principle of Indifference to the possible degrees of simplicity of theories, i.e., there is no obvious reason to assume that each degree of simplicity is equally likely.

Account #7: Complexity is unbounded.


The "complexity" dimension is unbounded in one direction. That is, there is a minimum possible degree of complexity, but there is no maximum. However complex a theory is, it could always get more complex. Now, in the case of any variable that is unbounded in one direction, probability theory requires you to assign decreasing probabilities (approaching zero as a limit) as the variable increases. That's the only way to have probabilities add up to something less than or equal to 1. Example: Suppose theories have possible levels of complexity 1, 2, 3, and so on (these might represent, e.g., the number of entities postulated). You can't give an equal probability to each degree of complexity, because then you're going to get the sum of all the probabilities being infinity (or zero). What you could do is give probability  1/2  to complexity level 1, then probability  1/4  to complexity level 2, then  1/8  to level 3, and so on. Then all the probabilities add up to 1. (Of course, there are other ways to do it so that the sum comes out to 1, but they all require the probability to approach zero as complexity increases without bound.)

![img-1.jpeg](img-1.jpeg)

Figure 8: Probability distributions that add up to 1

![img-2.jpeg](img-2.jpeg)


### 14.3.5. The Likelihood Account

You might be able to guess at this point that a Bayesian account of the virtue of simplicity is coming. Here it is. Simpler theories tend to be better supported by evidence that they accommodate, because they tend to have higher likelihoods.

In this account, we understand degree of complexity in terms of number of adjustable parameters (see §14.3.3). As a general rule, the more adjustable parameters a theory has, the wider the range of possible data that the theory could accommodate by adjusting those parameters. Thus, in the Ptolemaic system of astronomy (as discussed in §14.3.2), a wide range of possible planetary motions in the night sky could be explained by adjusting the distance of the Earth from the center of the cosmos, the speed and radius of each main orbit, and the speed and radius of each epicycle. The Copernican model has fewer parameters to work with, so it could accommodate fewer possible sets of observations.

![img-3.jpeg](img-3.jpeg)

Figure 9: The likelihood account of simplicity

This matters because when there is a wide range of possible evidence that a theory accommodates,  P(<em>e</em>|<em>h</em>)  is correspondingly low for any given  <em>e</em> ; when there is a narrow range of allowable evidence, then the value of  P(<em>e</em>|<em>h</em>)  is higher within that range. The reason is that  P(<em>e</em>|<em>h</em>)  has to add up to 1 for all possible values of  <em>e</em>  that the theory accommodates (see fig. 9). Another way to describe the situation is to say that simple theories tend to be more falsifiable than more complex theories, in that the simpler theories make more specific predictions (see §14.2). How does this account explain the virtue of minimizing the number of entities (or kinds of entity) that we postulate in a theory? Well, postulating new entities typically introduces new adjustable parameters having to do with the properties of these entities. A wider range of possible evidence can be explained by the postulated causal powers of a larger collection of entities.


This account of simplicity, it should be noted, does not imply that simpler theories are always better (even in one respect) than more complex theories. The claim is merely that simpler theories tend to have higher likelihoods than more complex theories, though there may be exceptions to this. Note also that simple theories are not held to be a priori more probable than complex theories; they are only held to be more easily supported by evidence (but also more easily refuted by evidence—these two traits go together). In the absence of evidence, simple and complex theories are (for all this account says) on a par.

### 14.3.6. Philosophical Applications

A final issue about simplicity. Some people apply the virtue of simplicity not only to scientific but also to philosophical contexts, suggesting that simpler philosophical theories are more likely to be correct, other things being equal —e.g., that physicalism is more likely than dualism, and nominalism is more likely than Platonism. Are these applications legitimate?

Typically no. Mostly they result from philosophers not having thought about why simplicity is supposed to be a theoretical virtue. In most cases, philosophical theories are not at all like scientific theories. When you have a scientific theory, normally there is a specific range of possible evidence that it accommodates, and there is little to no dispute over the fact that it accommodates that evidence. Competing theories accommodate different ranges of possible evidence, so we can perform experiments to discriminate among them.

When you have a philosophical theory, by contrast, typically the theory either contradicts pretty much all the evidence, or it accommodates all possible evidence; and the core dispute concerning the theory is about whether it does or doesn't accommodate the evidence. This makes the likelihood account of simplicity inapplicable to philosophical theories.

E.g., take the case of nominalism, the theory that universals (as defined in §10.5.4) don't exist. What evidence does this theory predict? There are two views about this:


(1) Realists think that nominalism entails that nothing has any characteristics. So one “prediction” of the theory would be that nothing is red. Since some things are red, nominalism fails to accommodate the evidence. Since the virtue of simplicity only applies to theories that accommodate the actual evidence, simplicity is not a reason in favor of nominalism.

(2) Nominalists claim that their theory is compatible with the fact that some things are red. If they’re right about this, then their theory is compatible with any things being any way. So the theory has no predictions whatever. Since simplicity is only a virtue to the extent that simpler theories tend to make sharper predictions, simplicity considerations again fail to support nominalism.

## 14.4. Realism &amp; Skepticism

Scientific realists are basically people who think that science reveals to us important truths about mind-independent reality. Scientific anti-realists are people who deny this. “Why isn’t everyone a scientific realist?” you might wonder. Well, let’s see ...

### 14.4.1. The Underdetermination Problem

The underdetermination of theory by empirical data is the phenomenon that the available evidence never uniquely determines the correct scientific theory. There is always more than one possible interpretation of the data. This is true because scientific reasoning isn’t deductive. If your theory isn’t entailed by the evidence, then by definition there are alternative ways the world could be in which the evidence is the same but your theory is false.

Philosophical skeptics like to come up with all-purpose alternative explanations of our evidence, such as that you’re a brain in a vat, God is deceiving you, or you’re dreaming everything. These suffice to make the point that there are always alternative explanations of the evidence. However, many people find these silly and would prefer more plausible examples. So here you go:

Say you learn that, within the U.S., jurisdictions that have stricter gun laws tend to have higher violent crime rates. (This is true.) A conservative might say: “That’s because gun restrictions exacerbate crime, because victims are prevented from defending themselves." A progressive might say: "No, it's because, when leaders see high crime rates, they wisely respond by regulating private gun ownership more." Someone else (a moderate?) might say: "Maybe population density contributes to both variables. Heavily populated places tend to have more crime. They also tend to have more left-leaning voters, which independently causes stricter gun laws."


It's not as if one side is being stupid and ignoring the evidence. Each side has its own scheme for making sense of the same evidence. You could look at other pieces of evidence, but much the same thing is going to happen: People with different theories will come up with their own ways of interpreting the evidence within their system.

A similar situation transpired in the debate between Ptolemaic and Copernican astronomy (§14.3.2). Both systems could explain approximately the same set of data consisting of observations of planetary positions in the night sky, even though they told very different stories about the structure of the cosmos.[141]

Usually, when you have two interpretations of the same evidence (unless one of them is a skeptical scenario designed to be irrefutable, like the brain-in-a-vat scenario), it's possible to gather further evidence that differentiates between them. In the geocentric/heliocentric cosmology case, we have, e.g., Foucault's Pendulum.[142] This is basically a big pendulum that swings back and forth for a long time. Over the course of many hours, the plane of oscillation of the pendulum can be seen to rotate, with the rate of rotation calculable based on your latitude (it rotates faster near the North or South pole). This is explained by the fact that the Earth itself is rotating. This was unknown to Copernicus (let alone Ptolemy), but it's a pretty powerful demonstration that the Earth rotates.

Does this eliminate underdetermination? Not really. It would be possible to maintain Ptolemaic astronomy despite demonstrations like that, provided that you're willing to complicate your physics, e.g., by giving up the principle of conservation of momentum and introducing some more complicated laws of motion that are relative to the Earth's location. No one wants to do that, but it's still philosophically interesting to consider exactly why we don't do that.

A more modern example is the different interpretations of quantum mechanics. Here's a very vague, basic outline of the situation. Quantum mechanics provides a certain algorithm for predicting the results of experiments. This algorithm makes use of vectors that are used to represent the physical state of a system. When you do certain mathematical operations on the vectors, you can calculate probabilities for different measurement outcomes, and those probabilities match the statistics you get if you do the measurements.


People have come up with multiple interpretations of what's going on—different theories about why the algorithm works and what the mathematical objects that it uses correspond to in reality. There is the Copenhagen Interpretation, in which objects are regularly in indeterminate states and observers cause them to jump to a randomly chosen determinate state when we make an observation. There is the Many-Worlds Interpretation, in which the universe is constantly splitting into many universes, where each possible thing that might happen happens in some universe. There is Bohm's Interpretation, in which a physical system is a particle located in a definite but unknowable-to-us position in a many-dimensional space, and the particle is deterministically pushed around by the wave function. And there are multiple others.

I'm not going to explain those theories. Here's what matters for our purposes: Those are all theories that use the same algorithm for predicting experimental results, so they explain the same evidence.[143] But they're incompatible with each other. So how, if at all, could we distinguish among them?

This last example (quantum mechanics), despite being esoteric, is a good example of the underdetermination problem because the alternative interpretations are seriously advanced by actual scientists (unlike skeptical scenarios, which no one believes), and we don't have any evidence that can differentiate among them (unlike the Ptolemy/Copernicus example).

### 14.4.2. Scientific Anti-Realism

Scientific anti-realists take a skeptical lesson from the underdetermination problem: They think there is no objective, purely rational way of choosing among different interpretations of the same evidence. Of course, we make choices anyway—scientists adopt particular theories, often forming a consensus in a given field as to the "right" theory. Since the evidence underdetermines theory, by definition these choices aren't dictated by the evidence. So instead they must be based on subjective, non-rational factors—our preferences, intuitions (where these are not viewed as genuine evidence), aesthetic tastes, and intellectual fashions. Because of this, anti-realists think, we can't view accepted scientific theories as rationally justified portrayals of the objective truth. Thomas Kuhn got famous for advancing this sort of view in The Structure of Scientific Revolutions, which became literally the most cited book in the world.[1144]


### 14.4.3. A Realist Interpretation

How should scientific realists respond to the underdetermination problem? They should say different things about different kinds of cases.

(i) One kind of case is the general skeptical scenario. Here, I have in mind things like the brain in a vat scenario, or the hypothesis that all emeralds are grue. (Once you've understood "grue", you can see how to generate skeptical theories rivalling any inductive generalization.)

These general skeptical arguments really do show that theory is underdetermined by data. But that only means that our evidence does not entail our conclusions, which should only worry you if you're a deductivist, i.e., you think only deductive reasoning is legitimate. It doesn't show that we can't inductively or otherwise non-deductively infer our conclusions from our evidence. Realists may cite partly a priori reasons why our actual beliefs are superior to the skeptical theories, e.g., that the skeptical theories are needlessly complicated, that they're less falsifiable, and generally that they're improbable. (See ch. 12 and §§8.3, 14.2, 14.3.)

(ii) There are also some alternative theories that are not general skeptical scenarios but also would not be seriously advanced by any scientist—e.g., a Ptolemaic theory of astronomy conjoined with an alternative physics designed to explain away Foucault's Pendulum (and all other evidences of the Earth's motion). It would be possible to construct such a theory, but it would be full of silly ad hoc complications. About cases like this, the scientific realist should and would say that the alternative theories are just extremely improbable due to all the needless complexities.

(iii) Another kind of case (and the kind most often discussed) concerns serious scientific theories for which we do not have enough evidence to decide between them, as in the case of Ptolemaic and Copernican astronomy in the 1500s. In these cases, it is still plausible that a priori considerations might strongly favor one theory over another, as the simplicity of Copernican astronomy favored it over Ptolemaic astronomy.


If no such a priori reasons can be found, it is open to the realist to say that we should suspend judgment until further evidence is gathered. In some cases, as in that of the interpretations of quantum mechanics, we may never gather enough evidence to know which theory is correct.

This last situation is the only one that should seriously bother us. However, it does not pose a threat to scientific realism in general, because it only occasionally occurs. (Obviously, scientific realists don't hold that science is omniscient.) In advanced, theoretical physics, there may indeed be serious alternatives that we cannot now decide among and even will never be able to decide among.

But this really does not generalize across science. In biology, there is no serious alternative to the theory of evolution. No one has some other, completely different account that explains the same evidence (without being a skeptical scenario). In astronomy, there is no serious alternative to heliocentric cosmology—no one seriously thinks anymore that the planets might be orbiting the Earth, or that they're all orbiting Jupiter, etc. In chemistry, there is no serious alternative to the theory that water is  H<sub>2</sub>O . In geology, there is no serious alternative to plate tectonics. In all these cases, no one has any examples of underdetermination, unless one wants to resort to general skeptical theories or silly theories that no scientist would seriously advance. So it remains open to us to maintain that science has told us a lot, though not everything, about the objective nature of the world we live in.

### 14.4.4. The Skeptical Induction

The best reason for being skeptical about science is history: Ever since human beings started theorizing about nature, we have been wrong. More precisely, almost every theory that people have ever held about natural phenomena has later been rejected. A good example is how Aristotelian physics, after holding sway in Western science/philosophy for many centuries, was superseded by Cartesian physics, which was then superseded by Newtonian physics, which was superseded by relativity and quantum mechanics, which may themselves be superseded by string theory. It would be foolish to think that you just happen to be born in the first time ever that human beings correctly understood how the world works. So probably our current theories are going to be rejected by future generations too. And thus, we shouldn't take our current theories as telling us the true nature of reality.


Some people concede that we don't currently know the actual truth about the world, but they maintain that we are getting closer to the truth. You could consider this a weaker form of scientific realism: Science tells us the approximate truth about objective reality, and it is becoming more accurate (a closer approximation) over time. People with this view like to point to how, as our basic physical theories advanced, we got more precise predictions. Newtonian physics gives you very accurate predictions for most cases and gives significant errors only in unusual cases, such as for very fast-moving or very tiny objects. Relativity and quantum mechanics then make good predictions for all the cases that Newtonian physics works for, plus also the cases of very small and very fast-moving objects. But maybe they don't work so well for some even weirder cases, like explaining what goes on in a black hole or at the beginning of the universe. Then maybe string theory gets those cases right. Etc.

This, however, isn't such a great response. It confuses accuracy of observational predictions with accuracy of the underlying explanation. Two theories may give only slightly different quantitative, empirical predictions from one another, yet give radically different explanations for those predictions. Take the case of Copernican and Ptolemaic astronomy. These theories give extremely similar predictions; there are only slight differences in where you would expect to see a planet in the sky if you used these two theories (and both gave you small errors). Yet the underlying stories they tell about how the cosmos is structured are completely different. So, from the standpoint of Copernican astronomy (which really is approximately correct), Ptolemaic astronomy is not approximately correct. It's totally wrong, because none of the planets is in fact circling the Earth, nor is any of them doing anything close to circling the Earth.

The same is true about classical physics and quantum mechanics. True, QM only makes significantly different observational predictions from classical physics in certain special circumstances, with very small systems. But it (in most interpretations) gives a totally different picture of the underlying reality. For example, if observers create reality, or if there are infinitely many parallel worlds appearing at every instant, that really is not at all close to anything that classical physicists thought. Thus, from the quantum mechanical standpoint, the classical picture is not approximately correct.


The implication seems to be that, if and when our current theories are overthrown by some revolutionary future theory, that future theory will probably also judge our current theories as not even close to correct.

A better response to the Skeptical Induction from the history of science is to point out that—like the underdetermination problem—it only has plausibility in certain areas, particularly advanced, theoretical physics. It is completely implausible, for example, that the Theory of Evolution is going to be overthrown by some alternative biological theory that explains the same evidence without relying on anything like genes or natural selection. It is similarly implausible that a future scientific revolution will overthrow plate tectonics, heliocentric cosmology, the theory that water is  H<sub>2</sub>O , the germ theory of infectious disease, the theory that lightning is an electrical discharge, the DNA theory of genes, etc.

Apropos of which, there really haven't been that many scientific revolutions in very many areas. Granted, the theories that people had in prescientific times (diseases being caused by imbalances of the four bodily humors; the material world being made of earth, air, fire, and water; etc.) were indeed totally wrong. But since the basics of the modern scientific method were established, there are not that many cases of a theory being firmly established, using modern scientific methods, and then later being overthrown. That's why the examples people give are always the same examples, in theoretical physics.

Granted, the theoretical physics examples are very interesting, and the skeptic may well be right that we do not know the underlying truth of theoretical physics. But that doesn't stop us from knowing plenty of useful and interesting stuff about the real, mind-independent world.

## 14.5. Why Isn't Everyone a Bayesian?

We've seen the usefulness of probability theory, especially Bayes' Theorem, for analyzing issues about scientific reasoning, from the paradoxes of confirmation theory, to the virtue of falsifiability, to the virtue of parsimony. Nearly every issue about justification has a Bayesian analysis. From the way I've talked about it, you might be wondering, "Is everyone a Bayesian?"


Sadly, no. Most epistemologists are not Bayesians. Most are neither Bayesian nor anti-Bayesian; they just choose not to work on that, perhaps because all the mathematical stuff isn't that fun.

Some philosophers, however, are serious critics of Bayesianism. I should probably tell you something about that, lest people accuse me of undue bias.

### 14.5.1. The Problem of Old Evidence

One objection claims that Bayesians can't account for how a theory is supported by "old evidence", i.e., evidence that was known before the theory was devised. According to Bayes' Theorem,

P(h | e) = \frac{P(h) \times P(e | h)}{P(e)},

you get confirmation if and only if P(<em>e</em>|<em>h</em>) > P(<em>e</em>). But since the evidence is already known, you have P(<em>e</em>) = 1. P(<em>e</em>|<em>h</em>) cannot be greater than that, so you can't have confirmation.

In response, Bayesians typically say that to assess P(<em>e</em>), you're supposed to look at the probability of <em>e</em> before it was discovered, or imagine a hypothetical state in which you didn't know <em>e</em> but the rest of your knowledge was otherwise as similar as possible to the actual state, or something like that.

### 14.5.2. The Probability of the Laws

Sir Karl (Popper) really didn't like Bayesianism for some reason (maybe because it undercuts the foundation of his entire philosophy). So he made some criticisms that try to use probability theory against the Bayesians; i.e., he tried to show that probability theory doesn't lead to the results that Bayesians want.

One of his claims (mentioned in §14.2.2) was that you should assign a prior probability of zero to any proposed law that applies to infinitely many things. This would include the Law of Gravity, the Conservation of Momentum, etc. The reason is basically that he thinks you can calculate the probability of the generalization as

P(<em>A</em><sub>1</sub>) × P(<em>A</em><sub>2</sub>) × P(<em>A</em><sub>3</sub>) × …

where <em>A</em><sub>1</sub> is the proposition that the first thing the law applies to satisfies the law, <em>A</em><sub>2</sub> is the proposition that the second thing satisfies the law, and so on. He thinks all of the <em>A</em><sub>i</sub> should have the same, nonzero probability, so the infinite product comes to 0. And note that if P(<em>h</em>) = 0, then P(<em>h</em>|<em>e</em>) also = 0 by Bayes' Theorem.


Reply: Popper is wrong to assume that <em>A</em><sub>1</sub>, <em>A</em><sub>2</sub>, and so on are probabilistically independent of each other. Rather, <em>A</em><sub>1</sub> probabilistically supports <em>A</em><sub>2</sub>, <em>A</em><sub>1</sub> &amp; <em>A</em><sub>2</sub> supports <em>A</em><sub>3</sub>, and so on. The correct formula is:

P(A<sub>1</sub>) × P(A<sub>2</sub>|A<sub>1</sub>) × P(A<sub>3</sub>|A<sub>1</sub> & A<sub>2</sub>) × …

(recall Axiom IV, §12.3.2). In that product, each factor is greater than the previous one. When you take that into account, you can get a nonzero product. (This is correct.)

Second reply: Some people think that laws of nature hold in virtue of relationships between universals. Now, if you reject universals, so you think that a law can only consist in an infinite conjunction of particular facts, then you would calculate the probability of the law as

P(A<sub>1</sub> & A<sub>2</sub> & A<sub>3</sub> & …) = P(A<sub>1</sub>) × P(A<sub>2</sub>|A<sub>1</sub>) × P(A<sub>3</sub>|A<sub>1</sub> & A<sub>2</sub>) × …

But if you posit relations between universals, then to determine the probability of a law, say, "All <em>A</em>'s are <em>B</em>", you would start with the possible ways that the two universals might be related to each other, e.g.: <em>A</em> necessitates <em>B</em>, <em>A</em> precludes <em>B</em>, <em>A</em> is irrelevant to <em>B</em>, <em>A</em> raises the probability of <em>B</em> (where this last possibility divides into infinitely many sub-possibilities). Each of those would then get a nonzero initial probability (perhaps each would get probability 1/4?).

### 14.5.3. The Problem of Priors

The one serious objection to Bayesianism is the problem of prior probabilities. On the Bayesian view, to determine how justified any theory is in the light of any evidence, you need to first know the probability of the theory prior to the evidence, P(<em>h</em>). And what the heck is that? What, for example, is the initial probability that humans evolved by natural selection, as assessed prior to collecting any evidence relevant to that? Any answer seems arbitrary.

It's no use saying, "Apply the Principle of Indifference." To do that, you would first need to list all the possible accounts of the origin of human beings. To avoid inconsistencies (per §12.6.3), you'd also need to identify the uniquely natural, or the most natural, way of describing that set of possibilities. Of course, no one can do these things.


The problem is pervasive. What, for example, is the a priori prior probability of the Earth orbiting the Sun? Of the Theory of Relativity being true? Of water being a compound of hydrogen and oxygen? Nobody knows these things.

Bayesians can make two related observations that might make you feel better about all this. The first is that the importance of the priors tends to diminish as you collect more evidence. I.e., people who start from different priors will tend to move closer together in their posterior probabilities as the evidence accumulates. The second observation is that to deploy Bayesian thinking, we need not have precise prior probabilities; we could instead start with a range of prior probabilities that we deem reasonable (but this range cannot just be the whole range from 0 to 1; see §12.5.6). Application of Bayes' Theorem would then get you a range of reasonable posterior probabilities, and that would typically be a smaller range than the range of priors you started with.

So, when you first hear "Maybe humans evolved by natural selection", no exact number suggests itself to you as the probability of that being true. But perhaps you have a pretty clear sense that you shouldn't say that's over  90%  probable in the absence of any evidence, nor should you say it's less than  0.000000001%  probable. If you can at least say that much, then the Bayesian machinery gets some purchase.

If you don't like this, you try giving a general account of justification that tells us the degree of justification any theory has in the light of any evidence. What's the alternative whereby you get to assess this without relying on any sense of the initial plausibility of the theory?

## 14.6. Conclusion

Scientific reasoning is non-deductive, but this isn't a problem. There are good reasons for why scientific method works the way it does—in particular, there are good, probabilistic explanations for why it makes sense to prefer falsifiable theories over unfalsifiable ones and simple theories over complex ones. Falsifiability matters due to the theorem of probability that, if nothing would be evidence against  <em>h</em> , then nothing is evidence for  <em>h</em>  either. Simplicity matters because simpler theories typically make more specific predictions, and therefore receive greater confirmation if their predictions come true, than complex theories. This is because more complex theories have more parameters that could be adjusted to accommodate different possible data.


Science tells us a lot about objective reality, but not everything. E.g., we know that the Earth orbits the Sun, that humans evolved by natural selection, that salt is sodium chloride, that earthquakes are caused by tectonic shifts. Some big questions in fundamental physics remain up for debate and perhaps will never be resolved (it's too early to say now).