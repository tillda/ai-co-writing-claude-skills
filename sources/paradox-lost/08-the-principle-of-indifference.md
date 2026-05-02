---
book: "Paradox Lost"
title: "Chapter 08 The Principle of Indifference"
chapter_number: "8"
chapter_name: "The Principle of Indifference"
author: "Michale Huemer"
table_of_content: |
  8.1 The Principle of Indifference
  8.2 The Paradoxes of the Principle of Indifference
    8.2.1 The Colored Book
    8.2.2 France and England
    8.2.3 The Car Ride
    8.2.4 The Cube Factory
    8.2.5 The Circle and Chord
  8.3 Wherefore Indifference?
    8.3.1 Theories Rejecting the PI
    8.3.2 The PI Is Intuitive
    8.3.3 The PI Is an Analytic Truth
    8.3.4 The PI Underlies the Least Controversial Probability Assessments
  8.4 Interpreting the Principle of Indifference : The Explanatory Priority Proviso
  8.5 Solutions
  8.4 Interpreting the Principle of Indifference : The Explanatory Priority Proviso
  8.5 Solutions
    8.5.1 The Colored Book
    8.5.2 France and England
    8.5.3 The Car Ride
    8.5.4 The Cube Factory
    8.5.5 The Circle and the Chord
  8.6 A Philosophical Application: The Problem of Induction
    8.6.1 The Traditional Problem
    8.6.2 A Probabilistic Formulation of the Problem
    8.6.3 A Solution
    8.6.4 The Mathematics of the Inductivist Solution
  8.7 Another Application: The Mystery of Entropy
    8.7.1 Why Entropy Increases
    8.7.2 The Reverse Entropy Law
    8.7.3 Reverse Entropy Is Crazy
    8.7.4 The Reverse Argument Misuses the Principle of Indifference
    8.7.5 The Isolated Box
    References
    Footnotes
---

© The Author(s) 2018

Michael Huemer, Paradox Lost

https://doi.org/10.1007/978-3-319-90490-0_8

# 8. The Principle of Indifference

<span class="mathjax_ignore">Michael Huemer&#36;^{1}&#36;</span>

(1) Philosophy Department, University of Colorado Boulder, Boulder, CO, USA

$\square$ Michael Huemer

## 8.1 The Principle of Indifference

The Principle of Indifference is a principle about how to assign probabilities to proposition s in the absence of evidence:

**Principle of Indifference:** If there is no reason to favor one alternative over another, then the two are equally likely.

Thus, if we have $n$ alternatives, with no reason to prefer any alternative over any other, each alternative has probability $1/n$. This is meant to apply to epistemic probability, which is a measure of the degree of justification or evidential support a proposition has. (Of course it does not apply to other kinds of probability.)

What if we have a variable with a continuum of possible values, and no information except that its value falls within certain boundaries? A natural extension of the above formulation is to say that in this case, equal-sized ranges (within the given boundaries) are equally likely to contain the variable's true value; in technical terms, the probability density should be uniform. For instance, if you know that $X$ takes some real-number value between 1 and 4, then the probability of its falling between 1 and 2 is $\frac{1}{3}$ (2 minus 1, divided by 4 minus 1). I shall take this also to be part of the Principle of Indifference.$^{1}$


There are some cases that can't be covered by the Principle of Indifference, such as those where there are infinitely many possible discrete values, or a continuous variable with no limits on its value. In these cases, assigning equal probabilities to all alternatives, or to equal-sized ranges, results in the total probability being either 0 (if all the assigned probabilities are zero) or infinity (if the probabilities are nonzero). We won't talk about such cases, as I don't have a solution for how to assign probabilities in such cases. But we will have plenty of paradox to worry about even without these cases.

## 8.2 The Paradoxes of the Principle of Indifference

### 8.2.1 The Colored Book

A new book by your favorite author has just been published. So far, all you know about the cover design is that the cover is either red or green or blue. Given just this information, what is the probability that the book is blue?²

Here are two attempts to solve the problem using the Principle of Indifference.

**Solution 1:**

The book is red, green, or blue. With no information to favor any of these alternatives over any other, each has probability $\frac{1}{3}$.

**Solution 2:**

The book is either red or not red. With no reason to favor either of these alternatives over the other, each has probability $\frac{1}{3}$. Similarly, it is either green or not green, each with probability $\frac{1}{2}$; and blue or not blue, each with probability $\frac{1}{2}$. But then the probability of its being red, green, or blue is $\frac{1}{2} + \frac{1}{2} + \frac{1}{2} = 1\frac{1}{2}$, which is impossible.

### 8.2.2 France and England

Suppose you know nothing about France, England, and the U.K., other than that all three are places, and England is a proper part of the U.K. (So you are even more geographically challenged than the average American high school student.) On this information, what is the probability that England is larger than France?³ You have no information suggesting which region is more likely to be the larger, so the probability is $\frac{1}{2}$ that England is larger, and $\frac{1}{2}$ that France is larger. (We assume that no two territories are exactly the same size.)


Now, what is the probability, on the same information, that the U.K. is larger than France? Again, with no reason to favor "the U.K. is larger than France" over "France is larger than the U.K." or vice versa, both of these alternatives have probability $\frac{1}{2}$.

But this cannot be. Since you know the U.K. contains England as a proper part, the U.K. has to be bigger than England. Since you know for sure that the U.K. is larger than England, the U.K. has to be more likely than England is to be larger than France.

### 8.2.3 The Car Ride

Sue has taken a car ride of 100 miles. It took her between one and two hours; equivalently, her (average) velocity was between 50 and 100 miles per hour. This is all you know. Based on this information, what is the probability that her trip lasted between an hour and an hour and a half?⁴

**Solution 1:**

The range of possible times is from 1 to 2 hours. So the probability of the actual time falling between 1 and $1\frac{1}{2}$ hours is $(1\frac{1}{2} - 1) / (2 - 1) = \frac{1}{2}$.

**Solution 2:**

If Sue's trip took 1 hour, then her (average) velocity was 100 miles per hour. If her trip took $1\frac{1}{2}$ hours, then her velocity was $100 / 1\frac{1}{2} = 66\frac{2}{3}$ miles per hour. So the trip was between 1 hour and $1\frac{1}{2}$ hours if and only if her speed was between $66\frac{2}{3}$ mph and 100 mph.

The total range of possible speeds was 50 mph to 100 mph. So the probability that her speed was between $66\frac{2}{3}$ and 100 is $(100 - 66\frac{2}{3}) / (100 - 50) = \frac{2}{3}$.

And the only problem here is that one half does not equal two thirds.

The above calculations are both mathematically correct. If you phrase the problem in terms of possible times, you get a different answer than if you phrase it in terms of possible velocities. Given a velocity, you can calculate the corresponding time, and vice versa, but the relationship between the two is nonlinear. Thus, a given range of possible times correlates to a different-sized range of possible velocities, as illustrated in figure 8.1. This kind of problem recurs in the next two examples.

![img-0.jpeg](_images-ocr/chapter7/p3-img-0.jpeg)

Range of Possibilities

Fig. 8.1 Mapping between time and velocity

### 8.2.4 The Cube Factory

There is a factory in Princeton that produces cubes, for some unknown reason. All you know about their size is that they are at most 2 inches wide. Equivalently, they are at most 8 cubic inches in volume. Given just this information, what is the probability that the cubes are between 0 and 1 inch wide (equivalently, between 0 and 1 cubic inch in volume)?

Solution 1:

We are given that the width is between 0 and 2. Thus, the probability of its falling between 0 and 1 is $(1 - 0) / (2 - 0) = \frac{1}{2}$.

Solution 2:

The width is between 0 and 1 if and only if the volume is between 0 and 1. We are given that the volume is between 0 and 8. The probability of its falling between 0 and 1 is thus $(1 - 0) / (8 - 0) = \frac{1}{8}$.

Again, we get different answers depending on what variable we describe the problem in terms of – in this case, width or volume.

### 8.2.5 The Circle and Chord

There is a circle with an equilateral triangle inscribed in it (figure 8.2). Someone has chosen a chord of the circle at random. What is the probability that this chord is longer than a side of the triangle?

![img-1.jpeg](_images-ocr/chapter7/p5-img-1.jpeg)

(a)

![img-2.jpeg](_images-ocr/chapter7/p5-img-2.jpeg)

(b)

![img-3.jpeg](_images-ocr/chapter7/p5-img-3.jpeg)

(c)

Fig. 8.2 Bertrand's Paradox: (a) solution 1, (b) solution 2, (c) solution 3

Solution 1:

Rotate the inscribed triangle so that one of its sides is parallel to the chosen chord. Now imagine a radius of the circle drawn perpendicular to the chosen chord, as in figure 8.2a. The chord intersects the radius at some distance from the center of the circle. If that distance is less than half the radius, then the chord is longer than the side of the triangle. If it is more than half the radius, then the chord is shorter than the side of the triangle. (This can be proven geometrically and is apparent from the diagram.) With no reason to favor either of these alternatives over the other, we give equal probability to each. So the probability of the chord being longer than a side of the triangle is $\frac{1}{2}$.

Solution 2:

The chord has two endpoints. Take either endpoint, and rotate the triangle so that the endpoint coincides with a vertex of the triangle, as in figure 8.2b. The other endpoint is some distance away along the circumference of the circle. If that distance is less than a third of the circumference, in either direction, then the chord is shorter than a side of the triangle. This is true of two thirds of the points on the circumference. If the distance is more than a third of the circumference away, then the chord is longer. This is true of one third of the points on the circumference. So the probability of the chord being longer than a side of the triangle is $\frac{1}{3}$.

Solution 3: Imagine a circle inscribed within the equilateral triangle, as in figure 8.2c. The midpoint of the chosen chord is either inside this smaller circle or outside it. If the midpoint is inside the smaller circle, then the chord is longer than a side of the triangle. If the midpoint is outside the smaller circle, then the chord is shorter than a side of the triangle. The smaller circle has one quarter of the area of the larger circle; therefore, the chord's midpoint has probability $\frac{1}{4}$ of falling within the smaller circle. So the probability of the chord being longer than a side of the triangle is $\frac{1}{4}$.

This last problem is known as Bertrand's Paradox, after Joseph Bertrand, who introduced it in 1889.⁶ I have left it till last since it is more complicated than the others, but it is the same sort of problem.

All of these problems, from the colored book through the circle and chord, follow a common pattern. They all derive contradictory results by applying the Principle of Indifference to different ways of describing the same problem. In the case of discrete alternatives, there are different ways of dividing up the space of possibilities. In the case of continuous alternatives, there are different variables in terms of which the possibilities can be described.

## 8.3 Wherefore Indifference?

### 8.3.1 Theories Rejecting the PI

Probably the dominant response to the paradoxes of the Principle of Indifference is to declare the Principle false. It is said that the above examples show the Principle to be inconsistent.[7]

How, then, should we answer the questions about the colored book, France and England, and so on? It is usually said that these questions, as posed, have no determinate answers. For instance, with no information other than that a book is red, blue, or green, one simply cannot calculate a probability that the book is blue. Some would say that we always need empirical information to assign probabilities – for instance, statistics on how often publishers produce blue books, or at least some experience with book covers and their appearances. This I call the Empiricist view.[8]

Others say that, in the absence of evidence, it is permissible to assign any probability to the book's being blue, as long as all of one's probabilities cohere with each other. This is the Subjectivist view.[9] Both Empiricism and Subjectivism about probability are popular views, and both reject the Principle of Indifference.

We should distinguish qualification from wholesale rejection of a principle. If we wish to qualify the Principle of Indifference, we might hold that the principle applies only in a certain range of cases, or that it requires additional principles, for example, governing how one should partition the space of possibilities.

To reject the principle wholesale, on the other hand, would be to say that there is nothing at all to it – that in no case is it correct that two alternatives must be assigned equal probability due to a lack of information favoring either over the other. Empiricists and Subjectivists reject the Principle of Indifference in opposite ways: Empiricists think that in the absence of relevant evidence, one cannot assign any probabilities; Subjectivist s think that in the absence of relevant evidence, one may assign any coherent probabilities one likes. The Principle of Indifference, by contrast, counsels adopting a specific probability distribution for such cases.

Following are some reasons why a wholesale rejection of the PI is unsatisfactory.

### 8.3.2 The PI Is Intuitive

<span class="mathjax_ignore">First, there is something extremely intuitive about the Principle of Indifference. So much so that in probability problems, it is generally not necessary even to state the Principle; one can simply presuppose it, and most audiences see nothing controversial. Take the Simple Envelope problem from chapter 7: you are to choose between two indistinguishable envelopes, one of which contains &#36;2 and the other of which contains &#36;4. You have no information about which is which. Which one should you choose?</span>

The standard answer: it doesn't matter, since each is equally likely to contain the larger amount. This turns on the Principle of Indifference. Those who reject the Principle must therefore say that this answer is not correct. Empiricists must hold that we cannot say whether the two envelopes are equally likely to contain the larger amount until we have some experience with envelopes like these. This doesn't mean that one should be indifferent between the two – it means that we can't assign expected utilities to the two options, so we can't say anything at all about whether one envelope should be preferred over the other, and if so, which one.

Subjectivists must say that one can rationally assign any probability to either envelope containing the larger amount, provided one is consistent. So a person could decide, for no reason, that the envelope on the left was 99% certain to contain the $4 – and there would be nothing unreasonable about this.

Neither of these views seem correct. It seems that the correct probabilities in the scenario are 50/50. There are many similar cases in which all people uncorrupted by philosophy share the intuition that a set of alternatives are equally likely, where the best explanation for this is something like the Principle of Indifference.

### 8.3.3 The PI Is an Analytic Truth

The Principle of Indifference also has a straightforward rationale based on the meaning of "epistemic probability". The epistemic probability of a proposition for a person, by definition, is a matter of how strongly their evidence supports or undermines that proposition.¹⁰ If one's evidence does not favor either of two alternatives over the other, then it supports the two alternatives to the same degree; hence, they have the same epistemic probability. Note that "supporting to the same degree" is compatible with "not supporting at all". Compare: if I donated to neither Oxfam nor UNICEF last year, then I "gave the same amount" to both charities, namely, zero.

This last analogy might seem to suggest that if one has no evidence for A, then the epistemic probability of A must be zero. This is mistaken, simply because the probability scale, by convention, includes degrees of counter-support as well as positive support; hence, “P(A) = 0” means that one’s evidence conclusively refutes A, not that it merely fails to support A.¹¹ What probability, then, indicates that A is neither supported nor undermined by one’s evidence? The answer can only be: 1/n, where n is the number of alternative possibilities.


How could one avoid this argument?

(i)

One might try a different definition of epistemic probability. One might say: “The epistemic probability of A is the degree of justification you have for A” or “The epistemic probability of A is the credence that an ideally rational agent would have in A.” But the argument for the PI succeeds on these formulations too, and on any formulation in the vicinity: if there is no reason at all for preferring one alternative over another, it is hard to see how one could have a higher degree of justification than the other, nor yet how an ideally rational agent would have more credence in one than in another. So how could one have higher probability than the other?

(ii)

Perhaps the critics of the Principle of Indifference would reject the notion of epistemic probability altogether. This is highly undesirable theoretically, as there are many contexts in which epistemic probability appears to be in play. How can we understand expected utility in decision theory, without epistemic probability? How could we understand such statements as “The theory of evolution is almost certainly true” without epistemic probability?

(iii)

Perhaps we could accept the general notion of epistemic probability, but claim that epistemic probabilities are indeterminate when one lacks relevant evidence; a proposition can only have a determinate epistemic probability in the light of some evidence that supports or undermines it. This does not accommodate intuitions about cases such as the Simple Envelope problem, where we lack evidence about the alternatives; it is, however, meant to accommodate such judgments as “The theory of evolution is almost certainly true.”

I maintain, however, that it does not accommodate even those cases. I have discussed this elsewhere, so I will be very brief here.¹² Our best account of how evidence renders a conclusion probable or improbable relies on the conclusion’s having an initial probability. According to Bayes’ Theorem, the probability of a hypothesis, h, in the light of some evidence, e, is given by:

$$P(h|e)=\frac{P(h)\cdot P(e|h)}{P(e)}$$

where P(h) is the initial probability of h, P(e) the initial probability of e, and P(e|h) the likelihood that e would hold if h were true. So if P(h) is indeterminate, then P(h|e) is also indeterminate. Thus, if nothing has a probability prior to empirical evidence, then nothing has a probability in the light of empirical evidence either.

### 8.3.4 The PI Underlies the Least Controversial Probability Assessments

Here is a common mistaken thought: There are more and less controversial ways of assigning probabilities. Applying the Principle of Indifference is one of the most controversial and least reliable ways. More reliable ways rely on randomization techniques or inductive evidence. [13]

This is mistaken because the least controversial, most reliable ways of assigning probabilities are themselves based on the Principle of Indifference. We simply tend to overlook this fact because we instinctively presuppose the PI in probabilistic reasoning.

If you draw a card from a normal deck, what is the probability that the card will be an ace? Answer: There are 52 cards, including 4 aces; therefore, the probability is 4/52. This is not an arcane philosophical hypothesis; this is as banal and uncontroversial a probability assessment as one can find. But this answer rests on the assumption that each of the 52 cards is equally likely to be the one drawn. This, in turn, rests on the absence of evidence favoring any card over any of the others.

Reply: “No, no, it rests on the assumption that the deck is shuffled before the drawing, which randomizes the cards’ order. If you don’t shuffle the deck, then you can’t say anything about the probability of drawing an ace.”

Counter-reply: That reasoning also presupposes the Principle of Indifference. There are many possible precise sequences of movements that would count as shuffling a deck of cards. If you reproduce precisely the same deck-shuffling movements a million times, starting from a deck in precisely the same initial state, you will get the same sequence of cards in the shuffled deck every time. (There is no intervention of quantum mechanical randomness at the level of playing cards!) The reason we consider shuffling to “randomize” the order of cards is that human beings never in fact reproduce precisely the same movements when they shuffle decks, and we never in fact know enough about a particular deck-shuffling to be able to predict the order of the cards. Nevertheless, given the precise way that you shuffled the deck, and the precise initial state that it was in, the resulting sequence of cards is uniquely determined.


So in what sense is it true that, say, the ace of spaces has a 1/52 probability of winding up on top? The answer is that, of all the possible ways of shuffling the deck, about 1.92% of them (1/52) result in the ace of spades being on top, and the same goes for each other card . . . and we have no reason to think that the actual deck-shuffling you did was any more or less likely to fall into that class of possible ways of shuffling than into any of the other classes that also contain 1.92% of the possible ways of shuffling a deck. In other words, given ignorance of the precise details of the deck-shuffling, we apply a uniform probability distribution over possible ways of shuffling the deck.

A similar point applies to all other uncontroversial probability assignments. Suppose I want to know what proportion of philosophers are Platonists. I take a random sample of 400 philosophers and ask them how they feel about the Forms. 20% of the sample think Platonism is true. Though the sample was only a small fraction of the total population of philosophers, I infer that about 20% of philosophers are Platonists. Why?

Let's say there are a total of 10,000 philosophers in the world. There are many possible ways of choosing a sample of 400 philosophers out of 10,000. (How many? There is a formula for that; the answer is 10,000!/(400!)(9,600!).) Of these ways, the overwhelming majority constitute representative samples, in the sense that the proportion of Platonists in the sample would be close to the proportion in the general population – this fact is provable within combinatorics, and it holds regardless of the proportion of Platonists in the population. If we assign equal probability to each of the possible ways of choosing the sample, then we can infer that it is highly probable that our sample is representative.[14] That equal-probability assignment rests on the Principle of Indifference.

If you are tempted to say that the equal probability assignment instead rests on the fact that our sampling technique randomizes the selection of survey respondents, recall the above point about shuffling cards. Given the full, precise details of how survey respondents were selected, and the initial conditions of the world, the actual selection was fully determined. The sampling technique only "randomizes" in the sense that it makes the results fully unpredictable to us – that is, it prevents us from having any reason to think Platonist philosophers more likely than any other, equal-sized group of philosophers to get the survey.

That is what all "randomization" techniques do (unless you have access to some quantum mechanical device). So all probability assessments that rely on an assumption of randomization – which includes all those that are considered the most reliable and least controversial – rest on the Principle of Indifference.

## 8.4 Interpreting the Principle of Indifference : The Explanatory Priority Proviso

Not everything in the world is equally fundamental; some things are explained by other things. The things that do the explaining are more fundamental than, or *explanatorily prior* to, the things that get explained. Some examples:

(i)

The properties and relations of an object’s parts generally explain the features of the whole. The table is solid *because* its molecules have a stable configuration with relatively fixed distances from each other, not vice versa. (Note: explanatory priority is a necessary but not a sufficient condition for explanation. Microscopic features in general, including those that are not relevant to explaining solidity, are prior to such macroscopic features as solidity.)

(ii)

Earlier events explain later events, and causes explain their effects. The Treaty of Versailles helps to explain World War II, whereas World War II could play no role in explaining Versailles, since World War II hadn’t yet happened at the time the Versailles Treaty was signed.

(iii)

General facts are explained by the more specific facts that make them true. An apple is colorful in virtue of being red, not vice versa. Michael Jordan is tall in virtue of being six feet six inches, not vice versa.

This relation of explanatory priority must be taken account of in assigning probabilities: if one set of possible facts is explanatorily prior to another, then the *initial* probabilities we assign to the more fundamental possibilities must constrain the probabilities of the less fundamental possibilities, not vice versa. Given two variables, *X* and *Y*, if *X* explains *Y*, then the initial probability distribution for *Y* must be derived from that for *X* (or something even more fundamental). Here, by “initial probabilities”, I mean probabilities prior to relevant evidence. Thus, if we are applying the Principle of Indifference, we should apply it at the more fundamental level. I call this the Explanatory Priority Proviso to the Principle of Indifference. [15] This will prove key to resolving the paradoxes of section 8.2.

## 8.5 Solutions

## 8.4 Interpreting the Principle of Indifference : The Explanatory Priority Proviso

Not everything in the world is equally fundamental; some things are explained by other things. The things that do the explaining are more fundamental than, or *explanatorily prior* to, the things that get explained. Some examples:

(i)

The properties and relations of an object’s parts generally explain the features of the whole. The table is solid *because* its molecules have a stable configuration with relatively fixed distances from each other, not vice versa. (Note: explanatory priority is a necessary but not a sufficient condition for explanation. Microscopic features in general, including those that are not relevant to explaining solidity, are prior to such macroscopic features as solidity.)

(ii)

Earlier events explain later events, and causes explain their effects. The Treaty of Versailles helps to explain World War II, whereas World War II could play no role in explaining Versailles, since World War II hadn’t yet happened at the time the Versailles Treaty was signed.

(iii)

General facts are explained by the more specific facts that make them true. An apple is colorful in virtue of being red, not vice versa. Michael Jordan is tall in virtue of being six feet six inches, not vice versa.

This relation of explanatory priority must be taken account of in assigning probabilities: if one set of possible facts is explanatorily prior to another, then the *initial* probabilities we assign to the more fundamental possibilities must constrain the probabilities of the less fundamental possibilities, not vice versa. Given two variables, *X* and *Y*, if *X* explains *Y*, then the initial probability distribution for *Y* must be derived from that for *X* (or something even more fundamental). Here, by “initial probabilities”, I mean probabilities prior to relevant evidence. Thus, if we are applying the Principle of Indifference, we should apply it at the more fundamental level. I call this the Explanatory Priority Proviso to the Principle of Indifference. [15] This will prove key to resolving the paradoxes of section 8.2.

## 8.5 Solutions

### 8.5.1 The Colored Book

The paradoxical reasoning claims that the book has an equal chance of being red or non-red, an equal chance of being green or non-green, and an equal chance of being blue or non-blue, so that the total probability of its being red, green, or blue is $1 \frac{1}{2}$ (see section 8.2.1).

The color categories we use in ordinary language – such as “red”, “green”, and “blue” – are not fundamental. When an object is red, it is always red in virtue of its having some other, precise color shade, including a precise hue, saturation, and intensity. These perfectly precise shades lack names in English, but they are the more fundamental properties.

Therefore, given the Explanatory Priority Proviso of section 8.4, the correct application of the Principle of Indifference would not be to assign equal probabilities to "red" and "non-red", nor would it be to assign equal probabilities to "red", "green", and "blue". It would be to assign a uniform probability distribution over the color solid, that is, the space of possible precise color shades. This is a three-dimensional space with hue, saturation, and brightness as dimensions. (Since each of these dimensions has a limited range of possible values, it is possible to have a uniform, nonzero probability distribution over the space.) Each perfectly precise color is a point in the color solid. Given no information other than the ordinary understanding of colors based on our visual experiences of color, it would be rational to assign a uniform probability distribution over the region of the color solid that counts as red, green, or blue. The probability of the book's being blue is then equal to the proportion of that region that counts as blue.

<span class="mathjax_ignore">If you view color samples arranged by visual appearance to human observers (for example, Munsell color chips), you will see that there are more visually discriminable shades of blue than there are of either green or red. Blue is a larger color, so to speak; it occupies more of the color solid. Thus, the book is more likely to be blue than to be either of the other given colors. Taking this into account, a reasonable estimate of the probability of the book's being blue is about  &#36;40\%&#36; .</span>

All this is assuming, again, that you have nothing to go on but the ordinary notion of color based on our visual experience thereof; thus, that you have no knowledge of the physical properties underlying the phenomenon of color, no knowledge of the processes by which book cover designs get selected, and so on.

If you have background information about the physical properties that underlie the phenomenon of color, then you must assign a uniform probability distribution over the possible ways that these underlying physical properties might be, rather than the possible visually discriminable color shades. This is because the physical properties would be explanatorily prior to the colors that we see.

If you have background information about how book covers are chosen, then you must instead assign a uniform probability distribution over the possible mental states of the people choosing the book cover (their beliefs, preferences, and other states rele vant to their choice of book covers). This would be explanatorily prior (because causally prior) to the physical properties of the book cover. Of course, figuring out the results of such a probability distribution would be very difficult, as it involves us in trying to enumerate possible states of an editor's mind. Fortunately, our goal here is not to figure out what the actual probability would be in that situation. Our goal is merely to explain why the paradoxical reasoning is mistaken. It is mistaken because it applies the Principle of Indifference to the wrong sets of possibilities.


Here is another way of describing the error. It is said that since we have no reason to think the book more likely to be red than not, we should assign probability $\frac{1}{2}$ to its being red and $\frac{1}{2}$ to its not being red. But in fact, we have a reason to think the book more likely not to be red than to be red. This reason is that there are more color-shades that count as non-red than shades that count as red. So the Principle of Indifference does not apply to the set of alternatives {red, non-red}.

Similarly, it is said that of the alternatives "red", "green", and "blue", we have no reason to favor any of the three over any other. This is false, because we have a reason to favor blue over red: there are more shades of blue than there are shades of red. Likewise, we have a reason to favor blue over green: there are more shades of blue than there are of green. So the Principle of Indifference does not apply to the set of alternatives {red, green, blue}.¹⁶

### 8.5.2 France and England

The paradoxical reasoning claims that "England is larger than France" has the same probability as "France is larger than England", and also that "The U.K. is larger than France" has the same probability as "France is larger than the U.K." But these can't both be true, given the knowledge that England is a proper part of the U.K. (see section 8.2.2).

This reasoning misapplies the Principle of Indifference twice. "England is larger than France" does not have the same probability as "France is larger than England", because in the example, we are given that England is smaller than the U.K., whereas we are not given that France is smaller than the U.K. France might be smaller than the U.K. for all we know, but England is definitely smaller. So our information speaks to the smallness of England (slightly) in a way that it does not speak to the smallness of France. If you had to bet, you should bet on England to be the smaller region.

Similarly, if you had to bet on which was larger, the U.K. or France, you should bet on the U.K. to be the larger, since you have information that (slightly) speaks to the largeness of the U.K. (namely, that at least it is larger than England), with no parallel information speaking to the largeness of France.

A correct application of the Principle of Indifference would be something like this. Given that the U.K. is larger than England, and assuming no two territories are of exactly equal size, there are the following possible sets of relationships:

1. U.K. $>$ England $>$ France

2. U.K. $>$ France $>$ England

3. France $>$ U.K. $>$ England

(where "$>$ " denotes the larger-than relation). We assign equal probability to each of these alternatives. The probability of England being larger than France is then $\frac{1}{3}$, and the probability of the U.K. being larger than France is $\frac{2}{3}$.

### 8.5.3 The Car Ride

The paradoxical reasoning claims that the probability of Sue's trip having lasted between 1 and $1\frac{1}{2}$ hours is $\frac{1}{2}$, and the probability of her velocity being between $66\frac{2}{3}$ and $100$ mph is $\frac{2}{3}$. This can't be, since we know that the time was between 1 and $1\frac{1}{2}$ if and only if the velocity was between $66\frac{2}{3}$ and 100 (see section 8.2.3).

The correct solution is the one based on velocity; the solution based on time is in error. This is explained by the Explanatory Priority Proviso: Given a fixed distance, the speed at which Sue drove causally explains the amount of time that her trip took, not vice versa. If someone asks, "How come it took so long?", you could answer, "Because she was driving very slowly." But if someone asks, "Why was she driving so slowly?", you could not sensibly answer, "Because it took her a long time."

The priority relation in question is metaphysical, not psychological or conceptual. Thus, it does not matter that velocity is commonly defined in terms of a ratio of distance to time; how we define things does not matter to what we should consider likely to happen. Actual dependence relations in the objective world (that we know about) do matter. So what matters is the causal relation, not the conceptual relation.

So the correct probability is $\frac{2}{3}$.

### 8.5.4 The Cube Factory

The paradoxical reasoning claims that the probability of the cube's side being less than 1 inch is $\frac{1}{2}$, and the probability of its volume being less than 1 cubic inch is $\frac{1}{8}$; yet the side is less than 1 if and only if the volume is less than 1 (see section 8.2.4).

In this case, both solutions are conceptually in error, but the solution given in terms of volume gives the correct probability.

The size of an object is determined by the amount of material present and its arrangement. Assuming a fixed arrangement, the size is determined by the quantity of material. For instance, if the object is a cube of iron, its size is determined by the number of iron atoms. The cube may take up a lot of space because there are so many atoms in it; it is not the case that there are many atoms in it because it takes up a lot of space. Therefore, given the Explanatory Priority Proviso, the correct application of the Principle of Indifference is to assign a uniform probability distribution over the possible amounts of material that might be present. This has the same result, mathematically, as a probability distribution based on volume, since volume for an object of a given material is proportional to the quantity of material (at least approximately, for ordinary objects – of course, if you have an object with the mass of a star, matters may be different).

So the correct probability in this case is $\frac{1}{8}$.

### 8.5.5 The Circle and the Chord

The paradoxical reasoning claims that the probability of the chord being longer than the side of the triangle is $\frac{1}{2}$, and $\frac{1}{3}$, and $\frac{1}{4}$ (see section 8.2.5).

It is stipulated that the chord was chosen at random. However, there are many ways of choosing a chord that would qualify as "choosing a chord randomly". One way is to randomly select a point on the circumference, then randomly select a second point on the circumference, then connect the two. Another method is to randomly select a direction, then randomly select a distance (between zero and the length of the radius), then draw a chord whose midpoint is the chosen distance from the center of the circle, in the chosen direction. A third method is to randomly select a point inside the circle, then construct a chord with that point as its midpoint. These methods correspond to the three solutions discussed in section 8.2.5.


The method of selection is explanatorily prior to the result obtained. Therefore, the correct application of the Principle of Indifference would be to assign a uniform probability distribution over the possible methods of random selection. Each possible method of random selection generates its own probability distribution, including, in particular, a probability for the chosen chord to be longer than the side of the triangle. We need to take an average of these probabilities. Thus, suppose we have exactly three possible random selection methods, M1, M2, and M3. Then the overall probability of the chord being longer than the side of the triangle is given by:

$$
\begin{aligned}
\mathbf{P}(\text{chord is longer than side}) = & \frac{1}{3} \mathbf{P}(\text{chord is longer than side if } M_1 \text{ is used}) \\
& + \frac{1}{3} \mathbf{P}(\text{chord is longer than side if } M_2 \text{ is used}) \\
& + \frac{1}{3} \mathbf{P}(\text{chord is longer than side if } M_3 \text{ is used})
\end{aligned}
$$

$\frac{1}{3}$ is the probability of each of the three possible methods having been the method of selection. Applying this to Bertrand's three methods of selecting a chord, this yields

$$
\mathbf{P}(\text{chord is longer than side}) = \left(\frac{1}{3}\right) \left(\frac{1}{2}\right) + \left(\frac{1}{3}\right) \left(\frac{1}{3}\right) + \left(\frac{1}{3}\right) \left(\frac{1}{4}\right) = \frac{13}{36}.
$$

In other words, with no information suggesting that any of Bertrand's methods is more likely to have been the chosen method of selecting a chord, we consider each method equally likely, and thus take the average of Bertrand's three solutions.

But this is assuming that Bertrand's three methods are the only random selection methods. Some think that there are actually infinitely many random selection methods, perhaps because every probability distribution over the set of possible chords corresponds to a possible "random selection method".[17]

This is not correct. Not every possible probability distribution can be produced by something that we would recognize as random selection. Only probability distributions that are uniform over some natural variables (for example, the distance of the chord from the circle's center, or the distance between the points where the chord intersects the circumference) count as random selection methods. Bertrand's three methods qualify. There may also be other methods one can think of that qualify.[18]

How can we ensure that we have enumerated every random selection method? I know of no way of ensuring this. However, the correct application of the Principle of Indifference would be to assign equal weight to every such method that one is aware of. This avoids paradox. If one becomes aware of an additional method not previously considered, this does not threaten a paradox; one should simply incorporate that method, and recalculate the probability accordingly.

"But," one might ask, "which was the correct probability? Was the probability one originally calculated correct? If so, how could the new probability, calculated after discovering a new selection method, also be correct?"

In reply, there are two ways of thinking about epistemic probability. One way is that the probability of a proposition is the degree of belief one should rationally have in that proposition, given one's present information and taking into account one's cognitive limitations. On this account, the probability of the chord being longer than the side of the triangle changes when you acquire new information, namely, the information that there is an additional possible random selection method you had not previously considered.

Another way of thinking about probability is more idealized: perhaps the probability of a proposition is the degree of belief that an ideal reasoner would have in it, where this ideal reasoner sees all logical possibilities and all the logical consequences of his beliefs. On this account, ordinary people may often be unable to determine the probability of a proposition. We could only estimate the probability of the chord being longer than the side of the triangle, by enumerating as many random selection methods as we can. When we discover additional methods, we can then revise our estimate, seeking to make it more accurate.

In either case, there is no paradox, that is, there is no valid way of deriving incompatible probabilities. In the idealized conception of probability, there is a single correct answer to Bertrand's problem, though we may not know it. In the less idealized conception, there are probabilities that change as our logical and mathematical knowledge increases, but there are never two different probabilities for the same person at the same time.


## 8.6 A Philosophical Application: The Problem of Induction

### 8.6.1 The Traditional Problem

Inductive reasoning is (roughly) reasoning that extrapolates from particular cases, applying what is known to be true of observed cases to the unobserved.¹⁹ For instance, suppose that I observe a large number of honey badgers, and all of them turn out to be mean. I might then inductively infer (a) that the next honey badger I meet will be mean, or even (b) that all honey badgers are mean.²⁰

This type of reasoning appears to presuppose some such principle as the following:

**The Uniformity Principle:** Unobserved objects of a given kind tend to be similar to observed objects of that kind.

If we don't assume anything like the Uniformity Principle, then it is unclear why, after observing some mean honey badgers, we would expect the hitherto unobserved ones to be mean, rather than nice.

Therefore, it seems that we need some reason for believing the Uniformity Principle; otherwise, all our inductive conclusions will be unjustified. What reason can we give for believing the Uniformity Principle?

Notice, first, that we cannot verify the Uniformity Principle by observation, since the Uniformity Principle makes a claim about unobserved objects. By definition, we cannot know by observation that unobserved things are similar to observed things. Second, the Uniformity Principle does not seem to be a self-evident truth, or derivable from self-evident truths, like the fact that 2+2=4 or the fact that there is no largest prime number. One reason for saying this is that it seems perfectly possible that unobserved things should be completely different from observed things, whereas things that are self-evident are things that could not possibly have been false. Third, the Uniformity Principle could not be known by induction, since any inductive argument for the Uniformity Principle would have to be circular, given that induction presupposes the Uniformity Principle.

But these three alternatives – observation, (inference from) self-evident truths, and induction – seem to exhaust the possible ways in which we might try to justify the Uniformity Principle. Since none of them work, it looks as though the Uniformity Principle can- not be justified. Since the Uniformity Principle is the basis for all inductive reasoning, it looks as though inductive reasoning cannot be justified.


This conclusion is known as inductive skepticism. Note that inductive skepticism is not the view that inductive conclusions are not conclusively justified, or that they are merely probable and never certain. Inductive skepticism is the view that there is no justification whatsoever for any inductive conclusion.[21]

This view is crazy. Nearly all our beliefs about the world around us depend on induction, including, for example, my belief that the sun will rise tomorrow, my belief that other people exist and have mental states, even my belief that the world outside this room exists. It is absurd to say that all of these beliefs are completely unjustified, just like, say, the belief that purple unicorns built the Taj Mahal.

The problem of induction is the problem of explaining how induction is justified. What went wrong in the argument for inductive skepticism?

### 8.6.2 A Probabilistic Formulation of the Problem

The problem of induction, it turns out, is closely connected to the paradoxes of the Principle of Indifference. Consider a simplified version of the honey badger inference: assume that there are two personalities an animal can have: nice and mean. Assume that you can tell by observing an animal for a short time whether it is nice or mean. You are about to observe a honey badger. Given no further information than the preceding, what is the probability that it will be mean? Using the Principle of Indifference, we can assign equal probabilities to the two alternatives; thus, the answer is “½”.

Now consider a slightly modified problem. Suppose that things are as described above, except that this time, you know that 98 honey badgers have previously been observed, and all of them proved to be mean. Given this information, what is the probability that the next one you observe will be mean?

Here is one way to calculate that. Consider the sequence of 99 honey badger observations (the previous 98 plus the one you are about to do). There are $2^{99}$ possible outcomes for this sequence of observations. Each outcome can be described by listing, for each observed badger, whether it was nice or mean. (The first possible outcome is 99 nice badgers. The second possibility is 98 nice badgers followed by one mean one. The third is 97 nice badgers, one mean, then one nice. And so on.) Applying the Principle of Indifference, we can consider each of these possibilities to have an equal initial probability, namely, $1/2^{99}$. Now, to calculate the probability of the $99^{\text{th}}$ badger being mean given that the first 98 badgers were mean, we simply take the following ratio:

The number of sequences in which the first 98 badgers are mean and the 99th is also mean

The number of sequences in which the first 98 badgers are mean

This ratio is $\frac{1}{2}$. (There is one possible sequence in which the first 98 badgers are mean and the 99th is mean, and one sequence in which the first 98 badgers are mean and the 99th is nice.)

Notice that this is the same as the initial probability that the next observed badger would be mean, before you knew that 98 previous badgers were observed to be mean. In symbols:

$$\mathrm{P}(\mathrm{M}_{99} \mid \mathrm{M}_1, \ldots, \mathrm{M}_{98}) = \mathrm{P}(\mathrm{M}_{99})$$

The probability of badger #99 being mean given that badgers 1 through 98 were mean is the same as the initial probability of badger #99 being mean. In other words, the information about the niceness or meanness of the first 98 observed badgers is completely irrelevant. It tells us nothing about what the next badger will be like. This is the inductive skeptic’s conclusion.

Thus, inductive skepticism is actually supported by (a certain way of applying) the Principle of Indifference.

### 8.6.3 A Solution

Above, we applied the Principle of Indifference to the possible sequences of observation results. But, just as in the case of the earlier problems involving the Principle of Indifference, there are other ways of describing the possibilities in the honey badger problem, and hence there are other ways of applying the Principle of Indifference to the problem, which result in different answers.

Here is one of them. Assume that there is in general a fixed objective chance for a randomly chosen honey badger to be mean. This objective chance (unlike epistemic probabilities) is a matter of objective, physical facts about honey badgers, their environment, and the laws of nature; it is not dependent on our knowledge or evidence concerning honey badgers, or anything else about our minds. This objective chance is initially unknown to us, but we may be able to make inferences about the value of the objective chance. Assume also, as is widely accepted, that if you knew that the objective chance of a honey badger being mean was $c$, then the epistemic probability for you of a given badger being mean, given only that information, would be equal to $c$.

Now suppose we apply the Principle of Indifference to the possible values of this objective chance. This requires that we assign a uniform probability density to the possible values of the objective chance. Thus, for example, the epistemic probability that the objective chance is between 0 and 0.1 is 1/10; the epistemic probability that the objective chance is between .3 and .7 is 4/10; and so on.

This approach gives us a non-skeptical solution. Informally, what happens is that our observations of badgers give us information about the value of the objective chance of honey badger meanness. As we collect more and more instances of mean badgers, this tends to confirm that this objective chance is high, since otherwise it would be very unlikely that we would observe so many mean badgers. That, in turn, enables us to predict that the next observed badger will probably be mean. Working this out mathematically requires a little knowledge of calculus and probability theory. Because some readers are averse to reading mathematical derivations, I will relegate the derivation to the following subsection. For now, I will just tell you the result: in general, we can show that if the first $n$ badgers are all mean, then the probability of the next one being mean given just that information is $\frac{n+1}{n+2}$ [22]. So, given that the first 98 badgers were mean, the probability of the next one being mean is 99%. This is a strong rebuttal to inductive skepticism.

Why should we apply the Principle of Indifference in this way, rather than the manner described in the previous section that leads to inductive skepticism? Because of the Explanatory Priority Proviso: the objective chance of honey badger meanness is a pre-existing, physical fact about how the honey badger system works. This sort of fact could be used to (partly) explain our observations, whereas the reverse is not true (the sequence of observation results does not explain the objective chance). So the objective chance is explanatorily prior to the particular sequence of observation results. Therefore, the Principle of Indifference should be applied to the possible values of the objective chance, not to the possible sequences of observation results.

Now, the preceding reasoning all assumes that there are such things as stable, objective chances. So you might wonder: how do we know that there are such things? Isn’t this something that we would have to learn by induction – and wouldn’t that involve us in the sort of circular reasoning that the inductive skeptic initially warned us against (section 8.6.1)?

The answer is that we can construct a probabilistic argument for the existence of stable objective chances, and this argument does not require any circular reasoning. We may start by assigning, say, a 50% probability to the hypothesis that there are stable objective chances, and a 50% probability to the hypothesis that there are no such things. From this point, the degree of uniformity in our experiences gives us information about whether stable objective chances exist or not. As we notice more and more stable patterns in our experience, it becomes more and more (epistemically) probable that stable objective chances exist, since otherwise such stable patterns would be unlikely. Notice that this does not involve any sort of circular reasoning: the starting position does not amount to assuming that there are stable objective chances, since it does not require assigning a high prior probability to this hypothesis [23].

### 8.6.4 The Mathematics of the Inductivist Solution

Let $A_n$ be the proposition that all of the first $n$ observed badgers are mean (where $n$ can be any positive integer). What is the initial epistemic probability of $A_n$? In general, the probability of $A_n$ given that the objective chance of a mean badger is $c$, is $c^n$. (For instance, if badgers have a 0.7 objective chance of being mean, then, given just this information, the probability of finding 99 mean badgers in a row is $(0.7)^{99}$.) If there were finitely many possible values of the objective chance, then we would simply add up, for each possible value of the objective chance, the (epistemic) probability that the objective chance has that value times the (epistemic) probability of $A_n$ given that the objective chance has that value (which, again, would be $c^n$). But because we are "summing" for infinitely many alternatives, we need to use an integral and a probability density. The appropriate formula is the following:

$$\mathrm{P}(A_n) = \int_{c=0}^{1} c^n \rho(c) dc$$

where $\rho(c)$ is the (epistemic) probability density for the objective chance. In accordance with the Principle of Indifference, we take this probability density to be uniform, which requires that $\rho(c) = 1$ for all $c$ between 0 and 1. Plugging this into the above equation yields

$$\mathrm{P}(A_n) = \int_{c=0}^{1} c^n dc = \left. \frac{c^{n+1}}{n+1} \right|_0^1 = \frac{1^{n+1}}{n+1} - \frac{0^{n+1}}{n+1} = \frac{1}{n+1}.$$

Now, we would like to know the probability of the $(n+1)^{\text{th}}$ badger being mean given that the first $n$ are mean. This is equivalent to $\mathrm{P}(A_{n+1} \mid A_n)$, which, from the definition of conditional probability, is $\mathrm{P}(A_{n+1} \wedge A_n) / \mathrm{P}(A_n)$. Applying the above expression for $\mathrm{P}(A_n)$ we obtain:

$$P(A_{n+1}|A_{n}) = \frac{P(A_{n+1} \wedge A_{n})}{P(A_{n})} = \frac{P(A_{n+1})}{P(A_{n})} = \frac{\frac{1}{(n+1)+1}}{\frac{1}{n+1}} = \frac{n+1}{n+2}.$$

Thus, when we observe 98 mean badgers in a row, the probability of the next one being mean is 99/100.

## 8.7 Another Application: The Mystery of Entropy

### 8.7.1 Why Entropy Increases

The Second Law of Thermodynamics – the Entropy Law – states that the entropy of a closed system always increases until the system reaches maximum entropy, at which point entropy will remain constant. Roughly, this means that the world becomes less ordered, or more random, over time. This explains the fact that when a warm object comes in contact with a cold object, heat flows from the warm to the cold; we never see heat spontaneously flowing from the cold to the warm. Similarly, when you put a spoonful of cream in your coffee, the cream disperses throughout the coffee; you never see the cream gather back into a single spot.

This is sometimes said to be the key to understanding “the arrow of time”, or how the future direction in time differs from the past direction. Most of the laws of physics are time symmetric, that is, they treat the forward and backward directions of time the same, so that for any process that satisfies the laws, a similar process happening in reverse would also satisfy the laws. The entropy law is one of very few exceptions – it treats the future and past differently. This makes it a very philosophically interesting law.

Why is the entropy law true? Imagine an insulated box filled with air. At time $t$, the left half of the box, for whatever reason, is ten degrees warmer than the right half. The entropy law predicts that, say, a minute in the future, the two sides of the box will be more uniform: heat will have moved from the warmer side to the cooler, bringing their temperatures closer together. Heat will not move from the colder side to the warmer side. Why is this?

The molecules in any macroscopic object are in rapid, random motion. In a gas, these molecules are free to move throughout their container. The temperature of a given material is just the average kinetic energy that the molecules have in virtue of this random motion. To say the left half of the box is warmer than the right half is to say that the average kinetic energy of the molecules in the left half is greater than that of the molecules in the right half.

Let “$M_t$” stand for the given macroscopic state of the box at time $t$, that is, the state in which the left half is ten degrees warmer than the right half. There are many possible microscopic states of the box that would realize $M_t$ – that is, different sets of precise locations and momenta for the molecules that would make it true that the left half of the box was ten degrees warmer than the right half. Of these many micro-states, the overwhelming majority would lead to a future in which the halves of the box are more uniform in temperature. Therefore, if (in accordance with the Principle of Indifference) we assign a uniform probability distribution to the possible states that realize $M_t$, we should expect the halves of the box to have a more uniform temperature a minute later, which counts as an increase in entropy.

How do I know that most realizations of $M_t$ result in the box being more uniform in temperature after $t$? Since the air molecules in the box are moving randomly, periodically one of them crosses from the left side to the right side of the box, and periodically one crosses from the right to the left. Consider the first molecule to cross from the left to the right after $t$. We know nothing about this molecule except that, at $t$, it is on the left. By stipulation, the molecules on the left at $t$ have a higher average kinetic energy than those on the right at $t$. So, on average, we would expect this molecule to be more energetic than the average molecule on the right side of the box. Therefore, probably, when it crosses over it will result in raising the temperature of the right side of the box.

Parallel reasoning shows that the first molecule to cross from the right to the left will probably lower the temperature of the left side. If we repeat this for trillions of trillions of molecules, the probability becomes extremely high that, on net, the left half of the box gets cooler and the right half warmer. So high that we should never expect to see an exception in real life. This continues to be true until the two halves of the box are the same temperature.

That seems to explain the entropy law. Notice how the explanation turns on the Principle of Indifference.

Now, you might think: “Wait, the Principle of Indifference is a normative epistemological thesis, a thesis about what we are justified in believing. But the Second Law of Thermodynamics is an empirical, physical law. How can a normative epistemological principle explain the truth of an empirical law of physics?” Well, the above explanation for the entropy law does not make it physically impossible for heat to move from the cold side to the warm side; it is just that, given the appropriate initial probability distribution, we should have an incredibly tiny credence that we would ever observe that happening.

### 8.7.2 The Reverse Entropy Law

Now here is a puzzle to think about. The entropy law, as standardly understood, is time-asymmetric. It predicts entropy increasing in only one direction in time. We just gave a probabilistic explanation for why entropy should increase in the future. But why is there a temporal asymmetry? Why can’t we construct a parallel piece of reasoning that treats the backward direction in time in the same way that the above reasoning treats the forward direction? This reasoning would lead to what we might call the Reverse Entropy Law , which states that the entropy of a closed system always increases into the past until it reaches maximum entropy; more colloquially, that entropy has spontaneously decreased over time, from a maximum-entropy state.

Let’s try to construct that reasoning. Again, assume that at t, the left half of the box is warmer than the right. As noted earlier, the molecules are in random motion, and periodically one crosses from one side of the box to the other. Consider the last molecule that crossed over from the right to the left, before t. We know nothing about this molecule except that, at t, it is on the left side of the box. By stipulation, the molecules that are on the left side of the box at t have higher average kinetic energy than those on the right. Applying the Principle of Indifference, any of these molecules is equally likely to have been the last one that crossed over. So, on average, we would expect this molecule to have higher kinetic energy than the average molecule that is on the right side at t. Therefore, probably, when it crossed over it resulted in lowering the temperature of the right side; the right side was warmer just before it crossed over.

Similarly, consider the last molecule that crossed from the left to the right before t. All we know is that, at t, it is on the right. The molecules on the right at t are, on average, less energetic than those on the left at t. So probably, this molecule is less energetic than the average molecule that is on the left at t. So when it departed the left side, it raised the average energy level of the left side.

Thus, probably, just before t, the left side was cooler and the right side warmer than it is at t. If we repeat the reasoning for trillions of trillions of molecules, the probability becomes overwhelming that the left side was cooler and the right side warmer in the past. That is, there is an overwhelming probability that entropy was higher in the past.

Notice that this reasoning is all perfectly parallel to the reasoning from section 8.7.1 above, except with the temporal directions switched. There is no mathematical or logical error here. If there’s an error, it’s a philosophical one having to do with the nature of time.

According to the reasoning of section 8.7.1, if you see a system in a state of less-than-maximal entropy, you should expect that, a minute later, it will be in a higher entropy state. This was taken to imply that, in any spontaneous process, entropy increases.

Similarly, the reasoning of this section tells us that, if you see a system in a state of less-than-maximal entropy, you should infer that, a minute ago, it was in a higher entropy state.[25] Why, then, can we not infer that, in any spontaneous process, entropy decreases?

### 8.7.3 Reverse Entropy Is Crazy

Perhaps we could accept the Entropy Law and the Reverse Entropy Law. Or more precisely, we could accept this generalization: given that a closed system has some nontrivial degree of order at $t$, it tends to have higher entropy both before and after $t$. Entropy increases as you move farther in time from the low-entropy state, in either direction. Call this the Two-Way Entropy Law (figure 8.3).[26]

![img-4.jpeg](_images-ocr/chapter7/p28-img-4.jpeg)

Fig. 8.3 Two-Way Entropy Law

The Two-Way Entropy Law is a coherent theory. It is, however, completely crazy. Suppose you come upon a cup of coffee with a bit of cream in the middle of it. You didn't see how it got that way; all you know is what it is like now. You should expect that, a minute later, that cream will be uniformly dispersed throughout the coffee. This much is common sense.

According to the Two-Way Entropy Law, you should also think that, a minute in the past, that cream was widely dispersed throughout the coffee. From that dispersed state, the cream spontaneously gathered together in the middle, in a time-reversed version of the sort of dispersion we usually see. You should assign the same probability to this hypothesis about the past as you do to the hypothesis that the cream is going to disperse in the future.

Or suppose that you see a rock in the air, unsupported. You just got a glance for an instant, so you don't get to see what happens to the rock after that moment, nor what happened to it before.

You should assume that the rock will fall to the ground. As it hits the ground, its energy will be transmitted to the molecules in the ground, which wind up moving a little faster, that is, the rock's kinetic energy is converted into thermal energy and sound waves in the ground. You expect that thermal and sound energy to disperse outward from the site of impact. The rock will then probably continue to sit on the ground for a long time.

According to the Two-Way Entropy Law, the future that you predict for this system is perfectly analogous to the past that you should retrodict. So probably the rock was sitting on the ground for a long time to begin with. A very large number of molecules in the ground, starting from very far away in all different directions, started, by chance, moving toward the rock. Not all of the molecules in the ground, of course; rather, of the trillions of trillions of molecules in the ground surrounding the rock, it just happened that a slightly larger percentage of them were headed towards the rock than away from it. These molecules bumped into other molecules closer to the rock, which bumped into other molecules still closer, and so on. And these molecules happened to be on trajectories such that a large number of them all wound up colliding with the rock at about the same time and knocking it into the air. That's probably how it got in the air.

"But," you say, "that sequence of events is astronomically improbable. How could there be a coherent view on which one expects that to be true?"

Indeed, that sequence of events is astronomically unlikely, considered in itself. The Two-Way Entropy theory does not deny this. It only says that given the state of the rock at the moment you saw it, the foregoing story is the most likely explanation. Of course, it's incredibly unlikely that a rock would be in the air like that at any given time. Something incredibly unlikely has to have happened. The alternative – that the rock was in an even lower entropy state before you saw it – is (allegedly) even more unlikely.


You might point out that we don't actually observe such decreasing-entropy events. We see many low-entropy states, but whenever we observe a low-entropy state coming into being, what we seem to recall is that it evolved from an even lower entropy state, not from a high-entropy state. For instance, of all the times I recall seeing some cream in the middle of some coffee, it always started out with the cream completely separate from the coffee and then being poured into it.

But that is assuming that we can trust our memory. If we don't assume any temporal asymmetry in the physics, then our memories are exactly as likely to be reliable indicators of the past as they are to be reliable indicators of the future. Or so one might argue.

You have certain expectations about your own future and that of the world around you. Not very precise expectations, but broad, qualitative expectations about how things will go. Based on the Two-Way Entropy Law, you should also think that a time-reversed version of that is most likely how the present state of yourself and the world around you came about – including your current brain state, including your current collection of memories, and so on. It is highly unlikely that the current state of the world (including your current collection of seeming-memories) is going to lead to a time-reversed version of the events that you seem to recall happening over the past year. Your memories don't predict the future. Similarly, then, the current state of the world (including your current collection of seeming-memories) is highly unlikely to have arisen from the events that you seem to recall happening over the past year. That is, your memories probably don't reflect the real past.

All this is assuming that we start with knowledge only of the present, macroscopic state of the world, and we reason from there to hypotheses about the past in the same way that we reason to hypotheses about the future.

Of course, if we could not trust our memories, then we would have no way of coming to know the basic physical theory that the above reasoning takes for granted. So the Two-Way Entropy theory cannot be justified. But that observation does not address the problem. The intellectual problem is to explain why our physical theory does not support Reverse Entropy, as it does the regular Entropy Law. If our current physical theory predicts that it is incredibly unlikely that our memories are reliable, then that would be strong evidence against that physical theory.

### 8.7.4 The Reverse Argument Misuses the Principle of Indifference

I assume I don't have to argue against the Two-Way Entropy theory. It's probably too crazy even for a philosopher to embrace.[27] What is needed is a diagnosis of the error. The argument for the Reverse Entropy Law seems parallel to the account of why the real Entropy Law holds. Is there something wrong with the account of the real Entropy Law? Or is the parallel reasoning somehow relevantly different?


Here is a possible diagnosis. The reasoning for the real Entropy Law respects the Explanatory Priority Proviso to the Principle of Indifference given in section 8.4. It begins with a uniform distribution over states of the world at a time, and uses this to constrain judgments about the probabilities of states at a later time.

The reasoning for the reverse law does the opposite: it begins with a uniform probability distribution over states at a given time, and uses this to constrain the probabilities for states at an earlier time. Because earlier states of the world are explanatorily prior to later states, it is an error to reason in this way. Given the Explanatory Priority Proviso, the correct application of the Principle of In-difference is to assign uniform probabilities to possibilities at an earlier point in time, and infer probabilities at a later point, not vice versa.

Now to explain that more clearly: recall the box in macroscopic state $M_t$ at time $t$, where the left half is warmer than the right. Our above reasoning (section 8.7.2) considers the most recent molecule that crossed from the right side to the left before $t$. Since this molecule is on the left at $t$, we are supposed to take its expected energy level to be the average of the molecules that are on the left at $t$, and therefore take its expected energy level as higher than the average of the molecules on the right. Therefore, this molecule, in crossing over, probably cooled down the right side. So the two sides were probably closer in temperature in the past. Call this "the Reverse Argument" (because it supports the Reverse Entropy Law).

Here is an alternative argument. Consider the last molecule that crossed from right to left. Since this molecule was on the right side shortly before $t$, its expected energy level is the average of the molecules that were on the right side at that time. Since only one molecule has crossed from right to left since that time, that average must be almost identical to the average at time $t$. The molecules on the right at $t$ are relatively low-energy molecules. So we should expect the last molecule that crossed over from the right to be a low-energy molecule. More precisely, we should take the expected energy level of that molecule to be the average energy level of the molecules on the right just before $t$. Which means that when it crossed over, it cooled the left side. Call this "the Forward Argument" (because it suggests entropy increasing forwards in time).

Parallel reasoning shows that the last molecule that crossed from the left to the right probably heated up the right side. Hence, before $t$, the two sides of the box were probably even more disparate in temperature, with the right side hotter and the left side cooler.

The difference between the Reverse Argument and the Forward Argument comes down to two different ways of applying the Principle of Indifference. For simplicity, let's assume that there are just two kinds of molecules, fast and slow. The box contains equal

numbers of each kind, but at $t$, the left side contains $60\%$ of the fast molecules and only $40\%$ of the slow molecules, while the right side contains $60\%$ of the slow molecules and $40\%$ of the fast ones. If $x$ is the last molecule that crossed from right to left just before $t$, what are the odds of $x$ being a fast molecule?

The Reverse Argument: $x$ is on the left at $t$, where $60\%$ of the molecules are fast. $x$ is equally likely to be any of the molecules that are on the left at $t$. So it has a $60\%$ chance of being fast, and a $40\%$ chance of being slow.

The Forward Argument: just before $t$, before $x$ crossed over, there were a certain number of molecules on the right side, of which $60\%$ were slow. Consider each possible way of choosing one of those molecules to be the one that crosses over. $60\%$ of these ways result in a slow molecule crossing over, so the odds are 60-40 that a slow molecule was the last one to cross over.

Here is an analogy (see figure 8.4). The average height of people in the Netherlands is 6.0 feet, while the average height in Indonesia is 5.2 feet. Issi recently moved from Indonesia to the Netherlands. Assume that people's height does not change when they move from one country to another. What is the expected value of Issi's height given the preceding information?

![img-5.jpeg](_images-ocr/chapter7/p32-img-5.jpeg)

Fig. 8.4 Migrant from Indonesia to the Netherlands

Answer 1:

Issi's expected height is 6 feet, since she is now in the Netherlands, and that is the average for people in the Netherlands.

Answer 2:

Issi's expected height is 5.2 feet, since she was just in Indonesia, where that was the average height.

Answer 2 is better, because it takes account of explanatory priority: Issi was originally in Indonesia, and her original height explains her present height, not vice versa.

You might want to say: "Actually, we should look at the collection of all people who first live in Indonesia and then move to the Netherlands. If we know the average height of that group, that will be Issi's expected height." But assume you do not have that information, or the group is too small to have reliable statistics. Then Answer 2 above is best.

### 8.7.5 The Isolated Box

I think there is something right about the preceding line of thought. But there seems to be something wrong with it as well.$^{29}$ Take this scenario: assume that you know at the start that the box of gas molecules has been isolated for a long time (long enough to have reached thermal equilibrium long ago, whatever its initial state). Stipulate that there has been nothing to interfere with the random motion of the particles in it during this time. Now, at time $t$, you measure the temperature with thermometers on opposite sides of the box, finding the left side, to your great surprise, 10 degrees warmer than the right. What is the best account of what happened?

You should think that the box was in thermal equilibrium for a while, then it reached its current low-entropy state by a random fluctuation away from thermal equilibrium, and it will soon return to thermal equilibrium again. Such a fluctuation is incredibly improbable, but it's the only explanation that makes sense given the rest of the scenario.

But the reasoning of the preceding subsection (section 8.7.4), if correct, would seem to apply to this scenario just as well as to the case where the box's history is merely unknown. According to the argument of section 8.7.4, we should think that a few seconds before $t$, the box was probably in an even lower entropy state than it is at $t$, with the two sides even more divergent in temperature.

This goes back to the time the box was created, when it was in an incredibly low-entropy state; by chance, it must have failed to ever reach thermal equilibrium since then. But this is very unreasonable; this requires an even greater improbability than the hypothesis of the preceding paragraph.

In this example, we are supposed to assume (i) that the box has been undisturbed for a long time, with nothing to interfere with the random motions of the particles therein, and (ii) that your temperature measurements at $t$ are completely trustworthy. In any realistic case, these assumptions could not be justified (once you seemingly observe the ten-degree temperature difference, you should infer that your temperature measurements are not accurate, that the box was not really isolated, or something similar). Nevertheless, if we take assumptions (i) and (ii) as fixed, then the hypothesis of an incredibly coincidental thermodynamic fluctuation is the correct inference.

So there are two kinds of cases:

(a)

Cases like the Indonesia/Netherlands case, in which we should accept the Forward Argument.

(b)

Cases like that of the isolated box considered here, in which we should accept the Reverse Argument.

What is the key difference between (a) and (b)?

I think the difference is that in type (b) cases, we are given that a system has been isolated long enough, with nothing to interfere with the random behavior of its particles, to reach thermal equilibrium. In reality, the world never gives us such guarantees. In reality, if you see a significant difference between two large groups, the rational inference is never that it came about by some astronomical coincidence; the rational inference is that some mechanism produced it systematically, even if the mechanism is wholly unknown to you.

Thus, if we observe that people in the Netherlands are on average 0.8 feet taller than those in Indonesia, we should not take this to be the result of purely random distribution of human heights. We should assume that some mechanism systematically produces taller people in the one region than in the other. This mechanism might, for example, have to do with differing evolutionary pressures in different climates – but one need not know anything about the mechanism to be justified in concluding that there is some systematic mechanism or other. The idea that such large groups of people have such a large average height difference by pure chance is just so improbable that we are justified in inferring that there is some more fundamental cause, even if we can't guess what it might be. From there, it is reasonable to expect that the person who recently migrated from Indonesia was a relatively short person.

Similarly, the idea that the universe has its present low-entropy state by pure chance is so incredibly improbable that we should assume that there is some (presently unknown) more fundamental cause that preferentially brought about an extremely low-entropy universe fourteen billion years ago, or whenever our physical universe came into being. We should assume this, even if we don't know what could make the universe have such low entropy. Of this, we will have more to say in our discussion of the Fine Tuning Argument in section 11.2.

### References

Aerts, Diederik and Massimiliano Sassoli de Bianchi. 2014. "Solving the Hard Problem of Bertrand's Paradox", Journal of Mathematical Physics 55: 083583.

Bayes, Thomas. 1763. "An Essay Towards Solving a Problem in the Doctrine of Chances", Philosophical Transactions of the Royal Society 53: 370-418. [Crossref]

Bertrand, Joseph. 1889. *Calcul des Probabilités*. Paris: Gauthier-Villars.

Carnap, Rudolf. 1962. Logical Foundations of Probability, 2nd ed. Chicago: University of Chicago Press.

de Finetti, Bruno. [1937] 1964. "Foresight: Its Logical Laws, Its Subjective Sources", tr. Henry Kyburg, pp. 99-158 in Henry Kyburg and Howard Smokler, eds., Studies in Subjective Probability. New York: Wiley.

Fumerton, Richard. 1995. Metaepistemology and Skepticism. Lanham: Rowman &amp; Littlefield.

Howson, Colin and Peter Urbach. 1993. Scientific Reasoning: The Bayesian Approach, 2nd ed. Chicago: Open Court.

Huemer, Michael. 2009. "Explanationist Aid for the Theory of Inductive Logic", *British Journal for the Philosophy of Science* 60 (2009): 1-31.

Huemer, Michael. 2017. "There Is No Pure Empirical Reasoning," Philosophy and Phenomenological Research 95: 592-613. [Crossref]

Hume, David. 1975. *Enquiry Concerning Human Understanding* in L. A. Selby-Bigge and P. H. Nidditch, eds., *Enquiries Concerning Human Understanding and Concerning the Principles of Morals*, 3rd edn. Oxford: Clarendon.

Hurley, James. 1986. "The Time-asymmetry Paradox", *American Journal of Physics* 54: 25–8. [Crossref]

Keynes, John Maynard. 1921. *A Treatise on Probability*. London: Macmillan.

Laplace, Pierre Simon. 1995. *Philosophical Essay on Probabilities*, tr. Andrew Dale, New York: Springer.

Marinoff, Louis. 1994. "A Resolution of Bertrand's Paradox", *Philosophy of Science* 61: 1–24. [Crossref]

Popper, Karl. 1961. *The Logic of Scientific Discovery*. New York: Science Editions.

Randall. 2011. "The Crazy Nastyass Honey Badger" (video), YouTube, January 18, https://www.youtube.com/watch?v=4r7wHMg5Yjg, accessed December 10, 2017.

Rawls, John. 1999. *A Theory of Justice*, revised ed. Cambridge, MA: Harvard University Press.

Reichenbach, Hans. 1938. *Experience and Prediction: An Analysis of the Foundations and the Structure of Knowledge*. Chicago: University of Chicago Press.

Shackel, Nicholas. 2007. "Bertrand's Paradox and the Principle of Indifference", *Philosophy of Science* 74: 150–75. [Crossref]

Stove, David C. 1986. *The Rationality of Induction*. Oxford: Clarendon.

van Fraassen, Bas. 1989. *Laws and Symmetry*. Oxford: Clarendon. [Crossref]

### Footnotes


#### Notes


1. This might be entailed by the original formulation, because for any pair of equal-sized intervals, we would have no reason to think the true value more likely to fall into one interval than the other. (For *different*-sized intervals, we *have* a reason to think one is more likely to contain the true value – namely, that it’s larger.) So equal-sized intervals must in general contain equal probability, so the probability density must be uniform.

2. This example is from Keynes 1921, p. 43. Keynes’ intention, however, is not to refute the Principle of Indifference but to refine it (pp. 55–64).

3. From Keynes 1921, p. 44.

4. From Fumerton 1995, p. 215.

5. From van Fraassen 1989, p. 303.

6. Bertrand 1889, pp. 4–5.

7. van Fraassen 1989, ch. 12; Howson and Urbach 1993, pp. 59–62; Shackel 2007.

8. See Reichenbach 1938, pp. 340, 348–57 (defending the “straight rule”, according to which the probability of A occurring in circumstances C = the number of observed occurrences of A divided by the number of observed occurrences of C); van Fraassen 1989, ch. 12.

9. de Finetti [1937] 1964; Howson and Urbach 1993.

10. Taking evidence broadly, to include everything that might serve as a source of epistemic justification for or against a proposition.

11. Exception: if A has probability zero simply because A is one of a continuous infinity of possibilities, this does not mean that one’s evidence refutes A.

12.

See Huemer 2017; 2009, pp. 27–9.

13

See, for example, Rawls 1999, pp. 145–50, explaining why the parties in his original position thought experiment allegedly cannot rationally rely on the Principle of Indifference (which Rawls refers to as “the principle of insufficient reason”) when making decisions.

14

This is not quite correct: since we know who the members of our sample are, we needn’t assign probabilities to different hypotheses about who they are. The correct statement is too complicated for the main text: let n be some particular possible number of Platonists that the population might have. Consider each possible way of distributing n instances of “being a Platonist” across the 10,000 members of the population. Assign equal probability to each of those. It will turn out that most of those ways would result in our sample of 400 being roughly representative. This will turn out to be true for each n between 0 and 10,000. Thus, the prior probability of our sample being roughly representative is high, no matter what probability distribution we give to n. This is essentially the basis for David Stove’s (1986, pp. 55–75) probabilistic defense of induction, though Stove does not bring out the dependence on the Principle of Indifference explicitly.

15

This is explained and defended further in Huemer 2009.

16

Cf. Keynes’ (1921, p. 59) treatment of the case.

17

Aerts and de Bianchi 2014; Shackel 2007, pp. 173–4.

18

Here is another one: select a random position in the circle, then select a random angle, then construct a chord that passes through the chosen point, with the chosen angle to the vertical. See Marinoff 1994 for more methods.

19

More precisely, inductive reasoning is reasoning that non-demonstratively infers, from the fact that certain things of kind A have feature B, that other things of kind A also have B. The fact that certain A’s have B need not be observed; it might be, say, intuited or discovered by inference. For instance, from the fact (i) that each of the first billion even numbers can be written as the sum of two prime numbers, one might inductively infer (ii) that all even numbers can be written as the sum of two prime numbers. Nevertheless, I shall continue to speak of observed and unobserved objects, since the most common and widely discussed examples of induction involve inference from the unobserved to the observed.

20

For more on the character of the honey badger, see Randall 2011.

21

This view is defended by Hume (1975, pp. 25–39) and Popper (1961, pp. 27–30), among others.

22

This is the famous Rule of Succession, first employed by Bayes (1763, scholium to Proposition 9) and later Laplace (1995, pp. 10–11) and Carnap (1962, pp. 567–8).

23

This is shown in my 2009, pp. 24–6.

24

If the wave function collapse in quantum mechanics is real, the law governing it is also temporally asymmetric. Also, some elementary particle interactions violate temporal symmetry.

25

For further explanation, see Hurley 1986.

26

Why is Fig. 8.3 drawn as it is? The farther we are from thermal equilibrium, the higher the proportion of possible transitions that lead toward equi-librium rather than further away. Thus, the lower entropy is, the higher the rate at which entropy increases. So as we move forward from the low-entropy time, entropy increases at a decreasing rate, i.e., the curve is concave down. The curve in the past direction is just the mirror image of the future-oriented curve.

27

Though perhaps I should reserve judgment until Peter Unger has weighed in.

28

Thanks to Iskra Fileva for this analogy.

29

I thank Randall McCutcheon (p.c.) for pointing this out.