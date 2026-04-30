---
book: "Philosophy of Language: A Contemporary Introduction"
title: "Chapter 10 Truth-Condition Theories: Possible Worlds and Intensional Semantics"
chapter_number: "10"
chapter_name: "Truth-Condition Theories: Possible Worlds and Intensional Semantics"
author: "William G. Lycan"
table_of_content: |
  Overview
  Truth Conditions Reconceived
  Advantages Over Davidson's View
  Remaining Objections
    **`Objection 7`**
    **`Objection 8`**
    First Reply
    Second Reply
  Summary
  Questions
    Notes
  Further Reading
---

# 10 Truth-Condition Theories: Possible Worlds and Intensional Semantics


## Overview

Kripkean possible worlds (as presented in Chapter 4) afford an alternative notion of a truth condition: We saw that a contingent sentence is true in some worlds but not in others. So a sentence’s truth condition can be taken to be the set of possible worlds in which the sentence is true. Moreover, possible worlds can be used to construct “intensions” or meanings for subsentential phrases, and particularly for individual words or meaning atoms, that are like Frege’s “senses” in being independent of actual referents. For example, a predicate has different extensions in different worlds, and its intension can be taken to be the function that associates any given world with the predicate’s particular extension in that world. Then a grammar can show how those sub-sentential intensions combine to make a truth condition, hence a meaning, for a complete sentence of which they are components.

The resulting view neatly avoids several of the objections that beset Davidson’s theory, most notably objection 4, the problem of coextending but nonsynonymous terms, and objection 5, the problem of non-truth-functional connectives. It also affords attractive semantical treatments of constructions that give Davidson’s model a very hard time: different types of necessity and possibility, counterfactual conditionals, and belief sentences. It also lends a hand with the Problem of Substitutivity. But it inherits the rest of Davidson’s difficulties and incurs one or two more.

## Truth Conditions Reconceived

As we saw in the previous chapter, the Truth-Condition Theory understands meaning as representation, as mirroring or correspondence between sentences and actual or possible states of affairs. But we can take the notion of a hypothetical state of affairs more seriously than Davidson is willing to, and consider “possible states of affairs/circumstances/conditions” as Kripkean *possible worlds* (Chapter 4). Recall that a possible world (other than the actual world, our own) is an alternative universe, in which things go otherwise than the way they go here. And, because worlds differ among themselves in respect of their component facts, of course the truth of a given sentence depends on which world we are considering.

This affords a new version of the idea of a sentence's truth condition. The sentence is true in some possible circumstances and not in others. Which, in the vernacular of possible worlds, is to say that the sentence is true in some worlds and not in others. When two sentences have the same truth condition, they will be true in just the same circumstances, in just the same worlds. When they differ in truth condition, that means there will be some worlds in which one is true but the other is false, so they will not be true in just the same worlds. As a first approximation, then, let us take a sentence's truth condition simply to be the set of worlds in which it is true.

For the truth-condition theorist, of course, that set of worlds will also be the sentence's meaning. It would follow that synonymous sentences are true in just the same worlds, while for any two nonsynonymous sentences there will be at least one world in which one of the sentences is true but the other false. This idea generalizes to the meanings of subsentential expressions. But, to show how that works, I must backtrack for a paragraph or two.

We saw in Chapter 2 that, unlike Russell, Frege (1892/1952b) had rejected thesis **`J3/K3`** ("A meaningful subject-predicate sentence is meaningful (only) in virtue of its picking out some individual thing and ascribing some property to that thing"), by positing abstract entities that he called "senses" and arguing that a singular term has one of these over and above its putative referent. And Frege defended compositionality: According to him, the subject-predicate sentence has a composite sense made up of the individual senses of its parts, and is meaningful in virtue of having that composite sense, whether or not its subject even has a referent at all. (Thus did Frege attack the Problem of Apparent Reference to Nonexistents.)

As sketched so far, Frege's view sounds like a version of the Proposition Theory. And so it is; it is prey to the various objections raised against that theory in Chapter 5. But Rudolf Carnap (1947/1956), Richard Montague (1960, 1970), and Jaakko Hintikka (1961) developed intensional logic, giving a possible-worlds interpretation and explication of Fregean senses. Here, roughly, is the idea.

A singular term or a predicate is said to have both an extension (in the sense introduced in the previous chapter) and a Fregean sense or "intension." The trick is to construe a term's intention as a function from possible worlds to extensions. Thus, the intention of a predicate is a function from worlds to sets of things existing in those worlds that are in the predicate's extensions in those worlds. For example, the intention of "fat" looks from world to world and in each world picks out the class of fat things there. "Fat" means not just the actual fat things, but whatever would be fat in other possible circumstances. (To put the idea in more human terms, if you know the meaning of "fat," you know what various hypothetical things would count as fat as well as just the list of which things actually are fat.)

"Individual senses," the intensions of singular terms, are functions from worlds to individual denizens of those worlds. That should sound a bit familiar from Chapter 4; a rigid designator expresses a constant function in that it picks out the same individual in every world. But a flaccid designator changes its referent from world to world: as we saw, “the British Prime Minister (in 2017)” designates Theresa May in the actual world, but various other people (or other creatures) in other worlds and no one at all in still others. The sense or intention of “the British Prime Minister” looks (or hops) from world to world and picks out whoever is currently Prime Minister there. As with predicates, if you know the meaning of the phrase “the British Prime Minister,” you know who would be the Prime Minister under various hypothetical conditions, even if you do not know who is actually Prime Minister now.


Functions of this sort combine to make senses or intensions for whole sentences. Take:

**`(1)`** The present British Prime Minister is fat.

In another possible world, *`(1)`*’s subject denotes whoever is Prime Minister there, and “fat” has an extension there that probably differs from the actual class of fat things. So, compositionally, we know how to tell whether *`(1)`* is true in that world: *`(1)`* will be true in that world if and only if the Prime Minister there belongs to that local extension. Therefore, if we know the intention of “the present British Prime Minister” and the intention of “fat,” we know whether a given world is one that makes *`(1)`* true, which is to say that we know how to tell in which worlds *`(1)`* is true; for we have in effect a composite function from worlds to truth-values. Therefore we know what set of worlds is *`(1)`*’s truth set. (Strictly speaking, the sentence’s intention is the function rather than the resulting truth set itself, but I shall ignore this technical distinction hereafter.) And that is to say that we know the proposition expressed by *`(1)`*, which is to say that we know *`(1)`*’s meaning. (Do not be misled: all this talk of our “knowing” things does not mean we are slipping into verificationism. I am speaking metaphorically of how one computes a complex intention given some primitive, simple intensions and subject-predicate grammar.)

If a proposition is in this way construed as a set of possible worlds, then we do, after all, obtain nontrivial explanations of the meaning facts. Two sentences will be synonymous if and only if they are true in just the same worlds. A sentence will be ambiguous if there is a world in which it is both true and false but without contradiction. And the possible-worlds construal affords an elegant algebra of meaning by way of set theory: For example, entailment between sentences is just the subset relation. $S_1$ entails $S_2$ if and only if $S_2$ is true in any world in which $S_1$ is; that is, the set of worlds that is $S_2$’s meaning is a subset of $S_1$’s meaning.

Thus, the implementation of truth conditions in terms of possible worlds saves this sophisticated version of the Proposition Theory from Harman’s objection 3 (Chapter 5), for it tells us what a “proposition” is, in terms that we can work with independently: A proposition is a set of worlds. (One may have metaphysical qualms about the idea of a "nonactual possible world," but at least one already knows what a world is supposed to be.) The present view also avoids our second objection to ideational theories, which carried over to the Proposition Theory, for it tells us what an abstract "concept" is: a function from worlds to extensions. (Shortly I shall introduce a complication.)


Finally, there is a direct argument for the possible-worlds version of the Truth-Condition Theory, given very briefly in Lewis (1970):

> In order to say what a meaning is, we may first ask what a meaning does, and then find something that does that. A meaning for a sentence is something that determines the conditions under which the sentence is true or false. It determines the truth-value of the sentence in various possible states of affairs, at various times, at various places, for various speakers, and so on.
>
> **(p. 22)**

I believe the idea is this: If you understand a certain sentence 5, and you are shown a possible world at random—we fly you there and dump you down in that world, miraculously making you omniscient as regards its facts—then right away you know whether 5 is true or false. (If you know every single fact of that world and you still cannot tell whether 5 is true there, then you cannot understand 5.) So one thing that a meaning does is to spit out a truth value for any world it is given. Which is to say that a meaning is at least a truth condition in the sense of a particular set of worlds. (This leaves it open that a meaning may include more than just a truth condition.)

## Advantages Over Davidson's View

The possible-worlds view has some important advantages over Davidson's version of the Truth-Condition Theory. Specifically, it avoids objections 4 and 5 that we made against Davidson.

**`Objection 4`** was the problem of coextensive but nonsynonymous terms. On the possible-worlds view, that is no problem at all. "Renate" and "cordate" differ in meaning because, although they apply to just the same things in the actual world, their extensions diverge in other possible worlds; countless worlds contain renates that are not cordates and vice versa. End of story (though shortly we shall resurrect Frege's solution to the Problem of Substitutivity).

**`Objection 5`** was the problem of non-truth-functional sentence connectives. Here the possible-worlds view displays a unique strength. For it enables us to state truth conditions for certain connectives directly in terms of worlds. Take the simple modal operator "It is possible that," as in "It is possible that the present U.S. President is fat." The latter sentence will be counted as true if and only if there is a world in which the present U.S. President is fat. And if we wanted to say "Necessarily, if there is a U.S. President, the United States exists," intensional semantics would count that as true if, and only if in every world, there is a U.S. President, the United States exists.


From this we can see that our original formula needs qualification: not every simple expression's sense or intention can be cast as a function from worlds to an extension or referent. Some are functions from intensions to other intensions; "It is possible that" takes the intention of the sentence to which it is applied and turns it into a different intention. Another, sub-sentential example would be adverbs, such as "slowly." "Jane swims" is true in a world if and only if the referent of "Jane" in that world is among the things that swim there, because the extension of "swims" is just the class of that world's denizens that swim. But what about "Jane swims slowly"? Grammatically, "slowly" modifies the predicate "swims," making it into the complex predicate "swims slowly." And the intensional semanticist maintains that the semantics follows in just the same way: The intention of "slowly" is a function from intensions to intensions; it picks up the intention of "swims" and turns it into a modified intention, namely the function that looks at a world and picks out the class of things that swim slowly in that world.¹

As noted in response to objection 5, the possible-worlds theory shines when we come to modal sentences, constructions that deal with various kinds of necessity and possibility. Talk of possibilities in particular is ubiquitous in language, and there are many kinds of possibility: physical, biological, moral, social-conventional, and so on without end. If we continue to understand "possible" as "true in at least one world," we capture some obvious felt implications, such as that which is actual is possible. More interestingly, we are able to distinguish different kinds of possibility by restricting the class of worlds we are talking about: to be physically possible is to obtain in some world that obeys our laws of nature, the ones that hold in the actual world. Moral possibilities are things that occur in some world at which all moral standards M are obeyed. (Yes, you will have noticed that our actual world is not morally possible in that sense!—so the implication I mentioned a moment ago, from actual to possible, depends on which sort of possibility we are talking about.) Epistemic possibility, i.e., possibility for all we know, is what happens in at least one world compatible with what we do know; etc.

The possible-worlds approach to modal constructions offers an attractive solution to the problem of counterfactual conditionals, which had previously plagued philosophers for years. It is hard to say what to make of

**`(2)`** Had Jerry known what was waiting for him in Birmingham, he would never have gone near the place

or

**`(3)`** If I were king, I would outlaw weird ice cream flavors.

Given that the conditional suppositions are presumed false—that of *`(3)`* in particular being completely fanciful—how are we supposed to say under what conditions such conditional sentences as wholes will be true?²

In the terminology of logic books, a conditional sentence has an “antecedent” (what I just now called a “conditional supposition”), typically though not always introduced by “if,”³ and a “consequent,” which is what is said to be true given the antecedent condition. For short, we can represent such a conditional as $A ightarrow C$. Modifying an important Inferentialist idea of Adams’ (1965), Robert Stalnaker (1968) proposes that the conditional is true iff, at the possible world where $A$ is true that is otherwise most similar overall to our own (real) world, $C$ is true also. The idea is that $A$ is a supposition or hypothesis, and we are to consider the class of worlds in which $A$ holds. But when we make such a supposition, we hold the rest of our real-world beliefs true so far as we can, allowing for $A$; so within the class of $A$ worlds, we choose the one that is otherwise most like our own actual world. Then we see if $C$ is true in that world.

To see how this works, let us first test a counterfactual that, though contingent, is obviously true.

**`(4)`** If I had thrown this table lamp out this fourth-story window, it would have smashed on the pavement below.

We consider worlds in which I did throw the lamp. In some of those worlds it plummets to the pavement and smashes; in others it bounces harmlessly, in others it does not fall, but flies away toward Boston singing “Dirty Water” (the Red Sox’ victory song). But we choose the world that is overall most like this world. Any world in which the lamp did anything but fall and break would be deeply unlike our world in its laws of nature and physical constitution, so in the most similar world, the lamp does do that.

So, for *`(2)`*: Look at the worlds in which Jerry did know what was waiting for him. In some of those he stays away from Birmingham; in others he goes there anyway. But which of them is overall most like this world? Is it one in which he stays away, or one in which he goes? And similarly for *`(3)`*; consider all the worlds in which I am king ...

Lewis (1973) tweaked and extensively elaborated Stalnaker’s proposal, and a huge literature has blossomed.

The possible-worlds theory has a deft way with belief sentences also. Let us return for a moment to Frege. As a solution to the Problem of Substitutivity, Frege proposed that a belief sentence can change its truth-value as a result of substitution of coreferring terms because, even though the two terms have the same referent, they may have different senses, and so a different composite sense may result from the substitution. (And belief, a cognitive state, has a “thought” or composite sense as its object, not any referent.) As always with unexplicated versions of the Proposition Theory, that sounds right but explains hardly anything so long as “sense” is merely taken for granted. But the possible-worlds theorist can give the explanation more content: Although the two terms corefer in the actual world, they diverge in other worlds, so their intentions differ. Therefore the composite intensions of otherwise similar sentences in which they appear will differ also. If believing is a relation between the believer and a proposition—that is, a sentence intension—then of course the believer may believe the one intension without believing the other. (Notice, however, that this solution assumes that at least one of the referring terms is flaccid.)


At this point an adjustment is needed. As I noted above, the present version of the possible-worlds theory counts two sentences as being synonymous when and only when the two are true in just the same worlds. But what of necessary truths that hold in every world? It would follow that every such truth is synonymous with every other; for example, “Either pigs have wings or they don’t” and “If there are edible mice, then some mice are edible” would mean exactly the same, which they obviously do not. Moreover, any sentence would be counted as being synonymous with any other sentence necessarily equivalent to it: “Snow is white” would be said to mean just the same as “Either snow is white or pigs have wings and pigs are mammals and no mammals have wings”; and whoever believed the former would be automatically counted as believing the latter. Something has to give.

The source of the problem seems to be that complex intensions can be necessarily coextensive even when they are made up out of quite different concepts. The cure, then, as Carnap (1947/1956) saw, was to require that, for synonymy, sentences should not only have the same intension but have that intension composed in the same way (or much the same way) out of the same atomic intensions. This is what he called *intensional isomorphism*, and it rules out all the foregoing problem cases. For example, “Either pigs have wings or they don’t” and “If there are edible mice, then some mice are edible” are composed out of entirely different intensions (those of “pig” and “wing” in the first case and those of “mouse” and “edible” or “eat” in the second).

## Remaining Objections

The possible-worlds theory inherits several of the objections raised against Davidson’s version: 1 (nondeclaratives), 2 (non-fact-stating sentences), and 6 (taking truth for granted); an intensional theorist would make much the same range of replies as we did on Davidson’s behalf. Objection 3 (deixis) arises in a different way, since the possible-worlds approach does not involve T-sentences, but it does arise, since no provision has as yet been made for deixis in the intensional apparatus. Objection 3 will be the main business of the next chapter.

The possible-worlds view also inherits the first two objections made against the Proposition Theory in Chapter 5: weirdness and alienness. As I noted in Chapter 4, it is one thing to take “possible worlds” as a metaphor or heuristic for explaining a way of looking at things, as I did in explaining Kripke's view of proper names. It is another to appeal to them directly in serious theorizing, as the intensional semanticists do. In what sense are there really alternative worlds that do not really exist? But this is a large subject and I cannot go into it here.⁴


The possible-worlds view is also subject to objection 4 against the Proposition Theory (neglect of meaning's "dynamic feature"). At the time, we replied simply that, even if propositions do not help in the explanation of human behavior, behavior is not the primary thing that needs explaining; rather, the meaning facts are. But the objection has been pushed further against both versions of the Truth-Condition Theory.

### **`Objection 7`**

There is still a problem of substitutivity. For there seem to be contexts in which synonymous (not just coextensive) terms cannot be intersubstituted without possible change of truth-value. "Ophthalmologist" and "eye doctor" are synonymous (or so we may suppose for convenience). But, if Sheila does not know that, "Sheila believes that every eye doctor doctors eyes" may be true while "Sheila believes that every ophthalmologist doctors eyes" is false; likewise "Irving went to an ophthalmologist because an ophthalmologist is an eye doctor" is true while "Irving went to an ophthalmologist because an eye doctor is an eye doctor" is false.

### **`Objection 8`**

Some Davidsonians (for example, Lycan 1984) and some intention theorists think of the kind of semantically charged syntax I have been describing as a machine program for computing large meanings from smaller ones, a program that is in some sense being run in the brains of speakers and hearers. But that idea is problematic. Here is a more specific worry about the "dynamic feature," pointed out by Michael Dummett (1975) and by Hilary Putnam (1978). Dummett's and Putnam's own writings are dense and somewhat obscure, but here is a simple way of putting one of their concerns: A sentence meaning is what one knows when one knows what a sentence means. But to know what a sentence means is just to understand that sentence. And understanding is a psychological state, one that inheres in a flesh-and-blood human organism and affects that organism's behavior. Now, if what a sentence means is just its truth condition, how can knowledge of a truth condition per se affect anyone's behavior, when (as is easily shown by Twin-Earth examples) truth conditions are often "wide" properties of sentences in the sense that they "ain't in the head" and knowledge of truth conditions is a conspicuously wide property of people? The truth condition of "Dogs drink water," here, differs from that of "Dogs drink water" on Twin Earth, but the difference is irrelevant to behavior and cannot affect it. But understanding (= knowing meaning) must and does affect behavior. Therefore understanding is not, or not merely, knowledge of truth condition, and so meaning is not, or not simply, truth condition.


### First Reply

Put in this way, the argument assumes that “understanding” must itself be a “narrow” or “in the head” concept. That is, to say the least, not obvious. (I leave to you the exercise of constructing a Twin-Earth counterexample.) Realizing that the argument needs a narrow concept of understanding also should make us reconsider the simple equating of “knowing meaning” with understanding and vice versa, truistic as that equating may have sounded at first.

### Second Reply

Further, the argument assumes that wide concepts cannot per se figure in the etiology of behavior. As is made clear by the “intentional causation” literature of some years ago,⁵ “figuring in” can be done in many ways. There is no doubt that behavior depends counterfactually on wide states of people: Had I wanted water (H₂O), I would have gone into the kitchen to get some. And I think that is the strongest etiological notion guaranteed by common sense. If anyone thinks that understanding affects behavior in a stronger sense of “affect” than just that the behavior depends counterfactually on the understanding, we would have to hear some defense.

The “use” theorist is not quite finished with the truth-condition view. We shall begin Chapter 12 by considering a further objection.

## Summary

- A sentence’s truth condition can be taken to be the set of possible worlds in which the sentence is true.

- More generally, possible worlds can be used to construct “intensions” for subsentential expressions, which will combine compositionally to determine the containing sentence’s truth condition.

- The resulting view avoids both the problem of coextending but nonsynonymous terms and the problem of non-truth-functional connectives.

- The possible-worlds theory affords solutions to some difficult semantic problems: the distinction between types of necessity and possibility; the truth conditions of counterfactual conditionals; and our understanding of belief sentences.

- The possible-worlds theory also deepens Frege's solution to the Problem of Substitutivity.

- But the theory inherits a number of Davidson's original difficulties and incurs one or two more.

## Questions

1. Evaluate Lewis' direct argument for the possible-worlds version of the Truth-Condition Theory.

2. Discuss the possible-worlds theory further, pro, con, or both. (If you do not already know some possible-worlds semantics, you will want to do at least a bit of outside reading; I recommend Lewis (1970).)

3. Consider the sort of truth condition for counterfactual conditionals offered by Lewis and Stalnaker, and try to find counterexamples to it.

4. Adjudicate objection 7 or objection 8.

### Notes


## Further Reading

- The simplest and most natural introduction I know to the possible-worlds version of truth-conditional semantics is Lewis (1970). Then work up to Cresswell (1973). (Tough stuff, requiring knowledge of formal logic and set theory; but it all came from something much tougher, collected posthumously in Montague (1974).)

- Two good textbook introductions to Montague Grammar are Chierchia and McConnell-Ginet (1990) and Weisler (1991).


#### Notes


1. Montague (1960) built up a structure of such higher- (and higher-) order intensions corresponding to more and more abstract parts of speech. In fact, out of a desire to one-up Quine, Montague explicitly assigned very rarefied individual intensions to "sake," "behalf," and "dint." As I mentioned in Chapter 1, in this way he meant also to strike a blow on behalf of the Referential Theory. (But it is at best a glancing blow: the words are not taken as denoting their intensions as if they were proper names.)

2. Here is a counterfactual I thought up the other day, for a friend: "If I had a girlfriend, she'd be rich, if she were rich." It is thoughts like that that give philosophy a bad name.

3. Not to be confused with the antecedent of an anaphor, introduced in Chapter 2. Nor is a counterfactual the same sort of explicitly truth-defined conditional you will find in a textbook system of propositional logic.

4. See again Lewis (1986) and Lycan (1994).

5. See, for example, Heil and Mele (1993).