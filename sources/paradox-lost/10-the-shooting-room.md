---
book: "Paradox Lost"
title: "Chapter 10 The Shooting Room"
chapter_number: "10"
chapter_name: "The Shooting Room"
author: "Michale Huemer"
table_of_content: |
  10.1 The Paradox
  10.2 Solution
    10.2.1 Solving the Finite Case
    10.2.2 The Impossibility of the Infinite Case
    References
    Footnotes
---

© The Author(s) 2018

Michael Huemer, Paradox Lost

https://doi.org/10.1007/978-3-319-90490-0_10

# 10. The Shooting Room

Michael Huemer$^1$

(1) Philosophy Department, University of Colorado Boulder, Boulder, CO, USA

Michael Huemer

## 10.1 The Paradox

Somewhere in the world is an awful place called “the shooting room”.$^1$ The people who own the shooting room have decided to play an evil game. They play the game once and only once. The game works like this: first, they call one person, randomly selected from all the people in the universe, into the room. When called into the room, a person is forced to go. The sinister organizers then flip a fair coin. If it lands heads, they shoot the person, whereupon the game ends.

If the coin lands tails, they let the person go, then call 9 new people into the room, and flip the coin a second time. If it lands heads on the second toss, they shoot the 9 people, and the game ends.

If it lands tails the second time, they let the 9 people go, call 90 new people into the room, and flip the coin a third time. If it lands heads, they shoot the 90 people, and the game ends.

If it lands tails, they let the 90 people go, call 900 new people into the room ... and so on. The game continues until some shooting occurs. In general, for each round $n$ after the first one, the organizers call $9 \times 10^{n-2}$ people into the room, then flip the fair coin for the $n$th time. If it lands heads on this $n$th toss, they shoot everyone in the room and the game concludes. If it lands tails, they let the people in the room go, then begin round $n+1$.

Now suppose that you learn that a particular individual, Vic, was called into the shooting room some time ago. What is the probability that Vic got shot? There are two plausible answers to this.

Answer 1: When Vic was called into the room, a fair coin was flipped. There is a 50% chance that it landed heads, in which case Vic was shot, and a 50% chance that it landed tails, in which case Vic was released unharmed. Therefore, the probability that Vic was shot is 50%.

Answer 2: Consider what percentage of all the people called into the room get shot. If the game went for only one round, then 100% (one out of one) of the people called into the room got shot. If the game went for exactly two rounds, then the one person from the first round was released unharmed, but then the 9 people in the second round were shot, so 90% of all the people called into the room were shot. If the game went for exactly three rounds, then 10 people (from rounds one and two) were called into the room but were released unharmed, while 90 (from round three) were shot. So again, 90% of all the people called into the room were shot. And so on. In general, if the game lasted for $n$ rounds (for any $n > 1$), then 90% of all the people called into the room were shot. The coin must eventually come up heads. So we know, with probability 1, that the percentage of people called into the room who are shot is at least 90%. Therefore, given that Vic was one of these people, the probability that he was shot is at least 90%.

These two methods of calculating the answer turn on two different, plausible principles about probability. I will call them the Objective Chance Principle and the Proportion Principle:

|  Objective Chance Principle :  |
| --- |
|  Given that event A happens if and only if B happens, and B has an objective chance c of occurring, the probability that A happens is c.3  |
|  Proportion Principle :  |
|  Given that x is an A, and the proportion of A's that are B is p (with no reason for regarding x as being more or less likely to be B than any of the other A's), the probability that x is B is p.  |

In the present case, Vic's getting shot turns on the coin's coming up heads, which has a 50% objective chance of occurring. No other information given in the scenario affects the probability of the coin's coming up heads, so, applying the Objective Chance Principle, we should assign a 50% probability to Vic’s getting shot. At the same time, you know that Vic is a person called into the shooting room, and at least 90% of people called into the shooting room are shot, and there is no reason for regarding Vic as more or less likely to be shot than any other person called into the room. Hence, applying the Proportion Principle, we should assign at least a 90% probability to Vic’s being shot.


So, which of these principles must we reject: the Objective Chance Principle, or the Proportion Principle?

## 10.2 Solution

### 10.2.1 Solving the Finite Case

The paradox makes crucial use of the infinite: the setup of the problem assumes that the game can simply continue until some shooting occurs, however long this takes. This requires that the shooting room has infinite size, that the people running the scheme have an infinite supply of bullets, that there is an infinite population of people from which they can draw their potential victims, that they have had an infinite amount of time to complete the game (or else that they can move with unlimited speed, so that they could complete any number of rounds in a finite time), and so on. These assumptions are impossible; as a result, there is no need to answer what would result from such a scenario.⁴ The question is like the question of what would occur if an irresistible force encountered an immovable object – the proper response to which is, “There cannot be any such things.”

What happens if we replace the impossible assumptions with assumptions that are in principle realizable? Rather than supposing that the game can continue indefinitely, let us suppose that there is a finite but large limit to the number of rounds that the game could continue. This might be, say, because there are only so many people in the world who could be called into the shooting room; thus, if the game should get to the point where it requires calling more new people into the room than the number of new people who exist, the game simply ends with no one being shot. But we may assume that the number of available victims is very large, so that the probability of running out of potential victims is very small.⁵

This version of the scenario is metaphysically possible, unlike the original version. In this case, what is the probability of Vic’s getting shot, given that Vic is called into the room? Again, there are two ways of calculating this. The first way is to look at the chance of the coin coming up heads when it is flipped while Vic is in the room. This is 50%, so Vic has a 50% probability of getting shot.

The second method is to look at the percentage of all the people called into the room who are shot. But we no longer know for sure that this percentage is at least 90; if the game goes on long enough, with the coin repeatedly coming up tails, then everyone will escape unharmed. This does not mean that we cannot use this method; it just means that the calculation must be more complex. We can still use the principle that, given that $x\%$ of people called into the room are shot, the probability of Vic's being shot is $x\%$. The proportion of people shot is either $100\%$ or $90\%$ or $0\%$. So we will have to calculate the probability, given that Vic is called into the room, that $100\%$ of the people called into the room are shot, as well the probability that $90\%$ of the people are shot, and that $0\%$ of the people are shot.


Now, speaking informally, the key point is going to be that the probability of Vic being called into the room increases as the game goes on; therefore, when you learn that Vic has been called into the room, this provides evidence that the game has gone on for a long time, which in turn raises the probability that the organizers would have run out of potential victims and thus had to conclude the game with no one having been shot. After taking this into account, it is going to turn out that the overall probability of Vic's having been shot is $50\%$.

To illustrate, let us assume that there are only one million people in the world (the results we will derive can be generalized to any finite population). If the shooting room organizers run out of people to call into the room, then the game ends. Thus, if the coin comes up tails seven times in a row (at which point the next round of the game would require 9 million new people to be called into the room), the game ends with no one having been shot. If the coin comes up tails fewer than seven times before coming up heads, then some people get shot. Thus, there are eight possible outcomes of the game, which I will call $O_1$, $O_2$, and so on:

|   | Coin toss results | People shot | Total people called into room | Proportion of people shot | Probability of outcome  |
| --- | --- | --- | --- | --- | --- |
|  O1 | H | 1 | 1 | 1 | 1/2  |
|  O2 | TH | 9 | 10 | 0.9 | 1/4  |
|  O3 | TTH | 90 | 100 | 0.9 | 1/8  |
|  O4 | TTTH | 900 | 1,000 | 0.9 | 1/16  |
|  O5 | TTTH | 9,000 | 10,000 | 0.9 | 1/32  |
|  O6 | TTTH | 90,000 | 100,000 | 0.9 | 1/64  |
|  O7 | TTTH | 900,000 | 1,000,000 | 0.9 | 1/128  |
|  O8 | TTTH | 0 | 1,000,000 | 0 | 1/128  |

We want to calculate the probability that Vic is shot, given that Vic is called into the room. Call this $P(S|C)$. ($S$ is the proposition that Vic is shot; $C$ is the proposition that Vic is called into the room.) According to probability theory, given that $O_1, \ldots, O_8$ are the only possible outcomes,

$$P(S|C) = P(O_1|C)P(S|O_1, C) + P(O_2|C)P(S|O_2, C) + \dots + P(O_8|C)P(S|O_8, C) \tag{10.1}$$

The second factor in each of those terms $(P(S|O_n, C))$ can be determined by applying the Proportion Principle: we simply take the proportion of all people called into the room who are shot, given each possible outcome, and treat this as the probability of Vic being shot, given that he is called into the room and given that particular outcome. This proportion is $0.9$ in each outcome, except the first (where it is $1$) and the last (where it is $0$). Thus:

$$\begin{array}{l} P(S|O_1, C) = 1 \\ P(S|O_2, C) = \dots = P(S|O_7, C) = 0.9 \tag{10.2} \\ P(S|O_8, C) = 0 \end{array}$$

Substituting Eq. 10.2 into Eq. 10.1 yields (with a little arithmetical manipulation):

$$P(S|C) = P(O_1|C) + (0.9)[P(O_2|C) + \dots + P(O_7|C)] \tag{10.3}$$

Next, what is the value of $P(O_1|C)$? According to Bayes' Theorem (given that $O_1, \ldots, O_8$ are the only possible outcomes),

$$P(O_1|C) = \frac{P(O_1) \times P(C|O_1)}{P(O_1) \times P(C|O_1) + \cdots + P(O_8) \times P(C|O_8)} \tag{10.4}$$

The values of $P(O_1)$, $P(O_2)$, and so on can be read off the table above:

$$
\begin{array}{l} \nP(O_1) = 1/2 \\\nP(O_2) = 1/4 \\\nP(O_3) = 1/8 \\\nP(O_4) = 1/16 \\\nP(O_5) = 1/32 \tag{10.5} \\\nP(O_6) = 1/64 \\\nP(O_7) = 1/128 \\\nP(O_8) = 1/128 \\
\end{array}
$$

What about $P(C|O_1)$, the probability of Vic being called into the room, given that the coin comes up heads on the first toss? If the coin comes up heads on the first toss, then the total number of people ever called into the room is 1. We have assumed that the world population is one million. Therefore, the probability of Vic being the person called into the room would be one in a million. With each round that the game goes on, the total number of people who have been called into the room increases by tenfold; thus, Vic's probability of being called in multiplies by ten, up until the last round, when everyone in the world has been called in. Thus, we obtain:

$$
\begin{array}{l}\nP(C|O_1) = 1/1,000,000 \\\nP(C|O_2) = 1/100,000 \\\nP(C|O_3) = 1/10,000 \\\nP(C|O_4) = 1/1,000 \\\nP(C|O_5) = 1/100 \\\nP(C|O_6) = 1/10 \\\nP(C|O_7) = 1 \\\nP(C|O_8) = 1 \\
\end{array}
\tag{10.6}
$$

All of this is in accordance with the Proportion Principle for assigning probabilities. Plugging Eqs. 10.5 and 10.6 into Eq. 10.4 yields:

$$
\begin{array}{l}\nP(O_1|C) = \frac{\left(\frac{1}{2}\right)\left(\frac{1}{1,000,000}\right)}{\left(\frac{1}{2}\right)\left(\frac{1}{1,000,000}\right) + \cdots + \left(\frac{1}{128}\right)(1)} \\
= \frac{1}{35,156} \\
\end{array}
$$

We can find $P(O_2|C)$, $P(O_3|C)$, and so on, using the same method. Omitting the remaining tedious arithmetic, I display the results as follows:

P(O₁|C) = 1/35, 156

P(O₂|C) = 5/35, 156

P(O₃|C) = 25/35, 156

P(O₄|C) = 125/35, 156

P(O₅|C) = 625/35, 156

P(O₆|C) = 3, 125/35, 156

P(O₇|C) = 15, 625/35, 156

Finally, plugging Eq. 10.7 into Eq. 10.3:

P(S|C) = 1/35,156 + 0.9(5/35,156 + 25/35,156 + 125/35,156 + 625/35,156 + 3,125/35,156 + 15,625/35,156) = 0.5.

This result, obtained by applying the Proportion Principle for assigning probabilities, is identical to the result obtained by applying the Objective Chance Principle: the probability of Vic being shot given that he is called into the room is ½. This was just a much more tedious way of obtaining the result.

That result was obtained assuming a population size of one million. But the same result emerges for any finite population size. For instance, if we instead suppose that the population of people available for the shooting room is one billion, then the final equation will be:

P(S|C) = P(O₁|C) + 0.9[P(O₂|C) + · · · + P(O₁₀|C)] = 1/4,394,531 + 0.9(5/4,394,531 + 25/4,394,531 + · · · + 1,953,125/4,394,531) = 0.5.

So we need not choose between the Objective Chance Principle and the Proportion Principle. The two principles yield the same result, 0.5, for all possible population sizes. They disagree only in the impossible case of an infinite population.

### 10.2.2 The Impossibility of the Infinite Case

Now, you might ask: What’s so impossible about an infinite population? On some current cosmological theories, the physical universe is held to be infinite. Thus, for all we know, the population of intelligent beings in the universe might actually be infinite.

Fair point. The impossibility in the original statement of the Shooting Room scenario does not really lie in the fact that the scenario assumes an infinite population. There may in fact be infinitely many persons in the universe. It is just that only finitely many of them could have been called into the shooting room, as of any given time. To see this, it suffices to reflect on the temporal processes described in the scenario. In each round of the game, some people must be gathered together, a coin flipped, and then the people in the room either shot or released. This takes time. Since the game has a first round, it must have begun at some time. Whatever that time was, only a finite time has elapsed since then. Therefore, only finitely many rounds of the game can have been played up till now. In that sense, at any given time, only finitely many people can have been called into the room. If the coin has thus far always come up tails, then, so far, 0% of all the people ever called in have been shot. This is enough for the logic of our above solution.

“But,” you might think, “what if the organizers play the game faster and faster with each round? They take one day to play the first round; then, if there is a second round, they take half a day for that; then a quarter of a day for the third round; and so on. In that case, they can complete an unlimited number of rounds within two days.”

This, however, is really impossible. To be thus capable of playing the game faster and faster without limit, the organizers would require an infinite store of energy located within a finite region. There cannot be such infinite energy density in any region.⁶ In addition, of course, the organizers would need the ability to violate various laws of physics to be able to play the game faster and faster without limit. Since the scenario is impossible, it does not matter that the Objective Chance Principle and the Proportion Principle would conflict in this case. Since the principles agree in all genuinely possible cases, we can continue to endorse both.

### References

Hamade, Rufus. 1996. “Black Holes and Quantum Gravity”, Cambridge Relativity and Cosmology, University of Cambridge, http://www.damtp.cam.ac.uk/research/gr/public/bh_hawk.html, accessed May 31, 2017.

Huemer, Michael. 2016. *Approaching Infinity*. New York: Palgrave Macmillan.

Leslie, John. 1996. *The End of the World*. London: Routledge.

Lewis, David. 1980. "A Subjectivist's Guide to Objective Chance", pp. 263–93 in Richard C. Jeffrey, ed., *Studies in Inductive Logic and Probability*, vol. II. Berkeley, Calif.: University of California Press.

Wald, Robert M. 1984. *General Relativity*. Chicago: University of Chicago Press.

### Footnotes


#### Notes


1. This chapter's paradox (with slight modification) is based on Leslie 1996, pp. 235–6, 251–6.

2. Leslie (1996, pp. 252–5) maintains that the 50% answer is correct if the coin flip result is genuinely random, but that 90% is correct if the coin flip is deterministic (though unpredictable to you). I think this a very odd view.

3. This is applying Lewis' (1980, p. 266) "Principal Principle". Background assumption: our evidence includes only information about what happens at and before the time at which chance $c$ exists. We don't, for example, have access to a crystal ball that detects future events via backwards causation.

4. See Huemer 2016, pp. 143–53, 223–8.

5. Leslie (1996, p. 252) briefly considers such a scenario and suggests that the 90% answer would still be correct.

6. It is metaphysically impossible for anything to possess an infinite, natural, intensive magnitude; see Huemer 2016, ch. 10. Energy density counts as a natural, intensive magnitude. You might object that, according to General Relativity, the center of a black hole has infinite energy density. This, however, is generally regarded as a problem for physicists to solve – physicists are seeking theories that eliminate the infinite quantities in such cases (Wald 1984, pp. 211–12; Hamade 1996). In any case, if the organizers of the Shooting Room gather together enough energy in a small enough space to create a black hole, it is doubtful that they would still be able to carry out their game.