---
book: "Paradox Lost"
title: "Chapter 02 The Liar"
chapter_number: "2"
chapter_name: "The Liar"
author: "Michale Huemer"
table_of_content: |
  2.1 The Paradox
  2.2 A Third Truth-Value
  2.3 True Contradictions
  2.4 Meaninglessness
    2.4.1 Self-Reference
    2.4.2 False Presupposition
    2.4.3 Lack of Communicative Use
  2.5 Putting the Blame on Truth
  2.6 A Solution
    2.6.1 An Inconsistent Language
    2.6.2 Meaning Deficiency
    2.6.3 The Truth-Teller
    2.6.4 "The Liar Sentence Is Not True" Is True
    2.6.5 This Sentence Is False or Meaning-Deficient
    2.6.6 Liar Cycles
    2.6.7 Prohibiting Liars
  2.7 Curry's Paradox
  2.8 The Paradox of Non-Self-Applicability
  2.9 Russell’s Paradox
    References
    Footnotes
---

© The Author(s) 2018

Michael Huemer, Paradox Lost

https://doi.org/10.1007/978-3-319-90490-0_2

# 2. The Liar

Michael Huemer¹

(1) Philosophy Department, University of Colorado Boulder, Boulder, CO, USA

Michael Huemer

## 2.1 The Paradox

Consider the following sentence, which I will call sentence L:

(L) This sentence is false.

L (or something like it) is called "the liar sentence" because it says something like "I am a liar." (Actually, a liar is a person who says what he does not believe, which of course is different from saying something false. But never mind that.)

Is sentence L true or false? Well, if it is true, then it is true that the sentence is false, so it's false. But if it is false, then it is false is that the sentence is false, so it isn't false, so it's true. To state the reasoning more explicitly:

1. If a sentence says that $a$ is $F$, then the sentence is true if and only if $a$ is $F$. (Premise.)¹

2. L says that L is false. (Premise.)

Therefore, L is true if and only if L is false. (From 1, 2.)

4. L is either true or false. (Premise.)

5. Therefore, L is both true and false. (From 3, 4.)

The conclusion is absurd since truth and falsity are incompatible by definition. We seem to be forced into contradiction just by thinking about sentence L.

## 2.2 A Third Truth-Value

Maybe the mistake is (4), the assumption that "true" and "false" are the only possibilities. Suppose there is a third truth-value called being "indeterminate". By stipulation, the "indeterminate" category includes all statements that don't fit under either "true" or "false". Perhaps, then, L is indeterminate.

But consider another sentence, L':

(L') This sentence is either false or indeterminate.

We can construct a parallel argument about L':

1'. If a sentence says that $a$ is $F$ or $G$, then the sentence is true if and only if $a$ is $F$ or $G$. (Premise.)

2'. L' says that L' is false or indeterminate. (Premise.)

3'. Therefore, L' is true if and only if L' is false or indeterminate. (From 1', 2'.)

4'. L' is either true, false, or indeterminate. (Premise.)

5'. Therefore, L' is both true and either false or indeterminate. (From 3', 4'.)

The conclusion is still contradictory, and now there would be no point in questioning the fourth step. So something else must be wrong with this argument. Whatever it is, presumably it is also the problem with the original argument about sentence L.

## 2.3 True Contradictions

Some believe that the answer is to accept that sentence L is both true and false. Now, I take it that "false" entails "not true" (note: there's no point in denying this, since I could just replace sentence L with a sentence that says of itself that it is not true). So this view amounts to embracing a logical contradiction, namely, that L is true and not true.

What is wrong with embracing contradictions, after all? Here is one answer: according to standard logic, if you accept a contradiction, then you can validly infer any conclusion whatsoever from it. Here is how: assume that you accept a proposition A, and you also accept its denial, ~A (read, "it is not the case that A"). Let B be any arbitrarily chosen other proposition. Then you can argue:

|  6. | A | Premise  |
| --- | --- | --- |
|  7. | ~A | Premise  |
|  8. | A or B | From 6²  |
|  9. | B | From 7, 8  |

For example, let A be the proposition that the liar sentence is true, and B the proposition that blue unicorns built the Taj Mahal. If you accept that the liar sentence is both true and not true, then you'll be committed to thinking that blue unicorns built the Taj Mahal. This is generally considered to be a bad result.

Some philosophers respond by adopting alternative systems of logic ("paraconsistent logics") in which contradictions can be true but in which one cannot derive any arbitrary proposition from a contradiction. These logics reject some of the standard rules of inference, so that the move from steps 7 and 8 above to step 9 is not allowed.

I reject this approach. My reason is not (and never was) that I'm worried about being committed to the claim that unicorns built the Taj Mahal. My reason is that the law of non-contradiction is self-evident. Indeed, I'd be hard pressed to think of anything more obvious. I think that if someone claims to believe that contradictions can be true, then that person has simply misunderstood the meaning of "contradiction".

Here is the classical understanding of the concepts of contradiction and negation in logic: let $A$ be any proposition. There are certain possible situations in which $A$ would count as true. Now, the negation of $A$ ($\neg A$), by definition, holds in all and only the other situations (see figure 2.1). If you think there is a situation in which both $A$ and $\neg A$ hold, then you're confused, because it is just part of the meaning of "not" that $\neg A$ fails in any case where $A$ holds. The lack of overlap between $A$ and $\neg A$ is the main point of the concept of negation. Now, a contradiction is a statement of the form $(A \wedge \neg A)$. So, by definition, any contradiction is false.[4]

![img-0.jpeg](_images-ocr/chapter1/p3-img-0.jpeg)

Fig. 2.1 Classical concept of negation

Here is a simpler way to put the point: a contradiction is a statement that entails two incompatible propositions. By definition, two propositions are "incompatible" when they can't both be true. So, by definition, contradictions can't be true.

Suppose I am wrong about this – suppose it is I who am confused about language (along with the classical logicians), and that "not" in English is actually used in such a way that the truth of "A" needn't exclude the truth of "not-A", that is, that there are situations in which both "A" and "not-A" count as being true. While we're at it, let us also allow that perhaps "A" and "not-A" don't exhaust the possibilities, that is, that there may be situations in which neither "A" nor "not-A" count as true.

This is represented in figure 2.2. The points in the diagram represent possible situations. The circle on the left represents the possible situations in which "A" holds; this includes regions 1 and 2. The circle on the right represents those in which "~A" holds, including regions 2 and 3. We have just supposed that regions 2 and/or 4 might be nonempty (there might be situations in which both "A" and "~A" hold, or in which neither holds).

![img-1.jpeg](_images-ocr/chapter1/p4-img-1.jpeg)

Fig. 2.2 A non-classical conception of negation

Now I am going to introduce a new operator, which I call "not!" (with the exclamation point). I hereby stipulate that "not!" is to be used in such a way that "not!-A" includes exactly regions 3 and 4 in the diagram. That is, even if there are situations in which both "A" and "~A" hold, these situations are by definition excluded by "not!-A"; also, if there are situations in which neither "A" nor "~A" hold, these situations are by definition included in "not!-A".


Now you can see that any puzzle that would be avoided by adopting a non-classical interpretation of "not" can be recreated using "not!". In particular, if your solution to the Liar Paradox involves claiming that the Liar sentence and its negation are both true, or that neither of them is true, we can recreate the paradox using the strengthened liar sentence $L^{l}$:

($L^{l}$) This sentence is not! true.

It is not open to maintain that $L^{l}$ is both true and not! true, nor can we claim that it is neither true nor not! true, since both of those options are ruled out by the definition of "not!". Since $L^{l}$ creates the same sort of paradox originally ascribed to $L$, there is no point in disputing my account of the meaning of "not" or "contradiction".[5]

The response for paraconsistent logicians would have to be to deny that "not!" is a legitimate concept – that is, to deny that it is even possible to refer to all and only the situations that fail to make "A" true.[6] It certainly seems that this is possible, and that I in fact just did it. If you understood what I said above in explaining "not!", then you, too, possess this concept that the paraconsistent logicians deny exists.

## 2.4 Meaninglessness

Perhaps L is meaningless in the sense that it fails to express a proposition. In that case, L is neither true nor false. We saw in section 2.2 that, to avoid paradox, it is not enough to reject premise 4 ("L is either true or false"). However, if we hold that L is meaningless, then we can also reject premise 2 -

2. L says that L is false. (Premise.)

Perhaps L does not say that L is false, because L does not say anything. In that case, the paradoxical reasoning stops cold. But why might L be meaningless?

### 2.4.1 Self-Reference

Perhaps self-referential sentences are meaningless or otherwise illegitimate. For in the case of such a sentence, a proper part of the sentence (e.g., the subject term) is required to stand for the whole sentence, and one might hold this to be impossible or otherwise illegitimate. But that can't be right, for consider the following sentence:

(S) This sentence is written in comic sans font.

S is certainly not meaningless. It is just false.

Well, perhaps it is permissible for a sentence to refer to its physical or syntactic properties, but not to its semantic properties. Truth and falsity are semantic properties, so a sentence may not talk about its own truth or falsity. But this doesn't suffice to avoid paradox, for consider:

(L1) The following sentence is true. (L2) The preceding sentence is false.

Neither refers to its own semantic properties, but the pair still generates a paradox. So to avoid paradox, we would need a stronger prohibition on discussing semantic properties.

Perhaps a sentence may not refer to semantic properties in general; perhaps there is something wrong with talking about truth and falsity. But that can't be right, because the following trio of sentences is perfectly acceptable:

(L3) The following sentence is true.

(L4) All bears are white.

(L5) The preceding sentence is false.

Notice that L3 and L5 are intrinsically indistinguishable from L1 and L2, respectively. And L3 and L5 are both meaningful (the former being false; the latter, true). So there is nothing internal to sentence L1 or L2 that renders either defective.

### 2.4.2 False Presupposition

Perhaps L is neither true nor false because L contains a false presupposition. According to some philosophers, a sentence with a false presupposition is neither true nor false.[9] In this view, it is important to distinguish what a sentence asserts from what it presupposes. For example, the question, "Have you stopped kissing squirrels yet?" does not assert that the addressee has been kissing squirrels; it merely presupposes that the addressee has been kissing squirrels. Similarly, the sentence "The King of America is foolish" does not assert that America has a king; it merely presupposes this. If one asserts that America has a king, then one speaks falsely. But when one merely presupposes that America has a king, then (some would say) what one says is neither true nor false.

Perhaps L lacks a truth-value (that is, is neither true nor false) because it contains a false presupposition. For perhaps to call a sentence false is simply to say that the proposition expressed by the sentence is false, and this presupposes that there is a unique proposition expressed by the sentence. L does not express a proposition, because for it to do so, there would have to be some independent way of identifying that proposition; that is, it would have to be possible to specify the proposition it expresses without first presupposing that there is such a proposition.

We need not settle whether this view about false presuppositions is correct. It doesn't matter whether L contains a false presupposition, or whether statements with false presuppositions should be considered neither true nor false, because we can simply rephrase the liar sentence to avoid the putative false presupposition. Thus, consider:

$L^{\dagger}$

This sentence expresses a proposition, and it is false.

$L^{\dagger}$ (perhaps unlike $L$) does not presuppose that it expresses a proposition; it explicitly asserts this. In general, whatever we might think about presuppositions, if one explicitly asserts something false, then one speaks falsely (compare: "America has a king, and he's foolish" is simply false, not indeterminate). So if $L^{\dagger}$ fails to express a proposition, then $L^{\dagger}$ is false, not indeterminate.

### 2.4.3 Lack of Communicative Use

Perhaps to be meaningful, a sentence must have a possible communicative use.[10] That is, there must be a possible situation in which the sentence could be used to convey information. But in what possible situation could the liar sentence be used to convey information? What state of affairs might it be attempting to describe? It seems that the answer to these questions is "none".

But the demand that a sentence have a possible communicative use is too strong. For a sentence to be meaningful, all that is required is that it express a proposition. There might be other reasons why it could not communicate information, for instance, that no one could believe the proposition that it expresses; this would not render it meaningless in the relevant sense.

Consider a slightly modified liar sentence,

(L") Sentence L" is not true.

On the theory presently under consideration, L" is neither true nor false because it is meaningless. So, in particular, L" is not true. In other words, the following is part of this theory:

(N) Sentence L" is not true.

Notice that L" and N are syntactically identical. N is true. So N must be meaningful. L" at least purports to express the same proposition that N in fact expresses. If N can be used to convey information, then why should we not say that L" can also be used to convey information – namely, the same information that N conveys?

Perhaps the liar sentence is meaningless because (unlike N), no one could seriously and sincerely assert it. But note that one could seriously and sincerely assert some relevantly similar sentences: I walk into my classroom and see the words "Donald Trump will make America great again!" written on the chalkboard on the west wall. I go to the chalkboard on the north wall and write, "The sentence written on the west wall of this room is false."11 Oh wait . . . I got confused about the compass directions. Actually, the sentence about Trump was written on the south wall, and my own sentence was written on . . . the west wall. Now, what I intended to say with that sentence was correct. But what about what I actually said: true or false?

## 2.5 Putting the Blame on Truth

Some blame the paradox on the general concept of truth, claiming that a language is "inconsistent" if it contains a truth predicate applicable to every sentence in the language.12

To explain: There are first-order sentences, sentences that talk about ordinary things, such as squirrels and clouds. For instance, "Most squirrels are furry" is a first-order sentence. Then there are second-order sentences, which talk about first-order sentences. For instance, "The sentence 'Most squirrels are furry' is true" is a second-order sentence. Then there are third-order sentences (which talk about second-order sentences), and so on.


Now, we can define a property of first-order truth (or truth $_1$), which is had by a first-order sentence when the ordinary object that the subject term refers to really has the property the predicate ascribes to it. $^{13}$ Then there is a property of second-order truth (truth $_2$), which is had by second-order sentences that ascribe properties to first-order sentences that really have those properties. Then there is truth $_3$, truth $_4$ and so on.

According to some philosophers (notably, Alfred Tarski), the liar paradox should be avoided by rejecting any general notion of truth – that is, we should allow talk of truth $_1$, truth $_2$, and so on, but we should not recognize any truth predicate that applies to all sentences regardless of their order. If we follow these rules, the liar paradox cannot be formulated. For consider: which truth predicate is the liar sentence supposed to be using? If it is truth $_1$, then we get the following reasoning about the new liar sentence, $L_1$ (modified from the original paradoxical reasoning):

|  (L1) | This sentence is not true1.  |
| --- | --- |
|  11. | If a first-order sentence says that a is not F, then the sentence is true1 if and only if a is not F. (Definition of truth1.)  |
|  21. | L1 says that L1 is not true1. (Premise.) |
|  31. | Therefore, if L1 is a first-order sentence, then L1 is true1 if and only if L1 is not true1. (From 1, 2.)  |

Premise $1_1$ must include the phrase "If a first-order sentence says . . .", to accommodate the fact that truth $_1$ only applies to first-order sentences. Step $3_1$ is then forced to include the same qualifier regarding "first-order" sentences. But from $(3_1)$, nothing interesting follows, except that $L_1$ is not a first-order sentence. 
\nSimilarly, if we try to formulate the paradox using truth $_2$, all we get is the conclusion that the liar sentence is not second-order. In general, if we try to formulate the paradox using truth $_n$, we get the conclusion that the liar sentence is not $n$th-order - which, after all, is correct; the liar sentence cannot be $n$th-order, for any $n$; the liar sentence has no order. So we avoid paradox.

Now, there are two ways of taking this proposal, an uninteresting way and an interesting way. The uninteresting interpretation: the solution proposes a convention whereby we simply refrain from talking about the general property of truth, so that we won't have to confront any sentences that generate paradoxes. I think this is approximately as satisfying as the following solution that could be proposed for any intellectual problem: "Suppose we change the subject." The liar sentence is in fact a sentence of English, and English appears to contain a general truth predicate. The puzzle about this sentence is hardly solved by switching attention to a possible language in which the liar sentence would not exist.

Here is the interesting interpretation: it is not merely that we can refuse to talk about truth; it is that there is no property of truth in general; there is only truth $_1$, truth $_2$, and so on. Thus, there is something inherently illegitimate about a general truth predicate, and any sentence that purports to ascribe generic truth must lack any determinate meaning. Why think there is no property of generic truth? Perhaps because there is no satisfactory way of defining the property without engendering paradoxes.

Note that it is not only the word "true" that creates problems. Similar paradoxes can be generated using other semantic terms, such as "refer", "ascribe", and "assert", for instance:

(R)

the smallest natural number not referred to by this expression

(A)

This sentence lacks the feature that this sentence ascribes to it.

(W) What this sentence asserts is not the case.

We encounter paradoxes when trying to figure out what R refers to, whether A has the feature that A ascribes to itself, and whether what W asserts is the case. So we would have to reject the existence of general relations of referring, ascribing, or asserting, in addition to the general property of truth.[14]

This view seems wrong. I surely can refer to both physical objects and words, in the same sense of "refer" (indeed, I just did so). Likewise, when we think about truth $_1$, truth $_2$, and so on, there clearly is something they have in common. There clearly is a sense in which a first-order sentence and a second-order sentence can both be true. For instance, suppose a colleague says to me, "The statement ‘Obama is a Muslim’ is false. Obama is not a Muslim.” I could then say, “Everything you just said is true.” I would not then be talking nonsense or misusing the word “true”, though I apply “true” to both a first-order and a second-order claim. I would be making an easily understandable and correct observation.


A partial reply: we can introduce a new truth predicate, call it “truth_{N}”, where a sentence is true_{N} provided that there is some natural number n such that the sentence is true_{n}. Then we can say that both first- and second-order sentences can be true in the same sense, namely, both may be true_{N}. This does not threaten to reintroduce the liar paradox, because we still lack any truth-predicate that could apply to sentences (such as the Liar sentence) that have no order.

This reply improves the theory; nevertheless, it still seems that we can understand a completely general notion of truth, namely, a sense in which a sentence that says that a is F (regardless of the order of the sentence, or whether it has an order at all) is true if and only if a is F.

A related problem is that the proponent of this theory would be unable to claim that his own theory is true. Since the theory discusses the whole hierarchy of sentences of different orders, the theory itself does not have any particular order. Thus, no truth predicate could apply to it. By the same token, the sentences used to express the theory could not be held to say, assert, or refer to anything, nor to have any other semantic properties, since all semantic properties are subject to the same sort of restrictions as the property of truth.

## 2.6 A Solution

### 2.6.1 An Inconsistent Language

My solution to the liar paradox holds that the liar sentence fails to express a proposition due to an inconsistency built into our language. As a result, premise 2 in the paradoxical reasoning – “L says that L is false” – is false.

Consider an analogous puzzle: an (adult, male) barber in a certain village shaves all and only the men who do not shave themselves. Question: Who shaves the barber? Since the barber shaves all and only the men who do not shave themselves, it must be that the barber shaves the barber if and only if the barber doesn’t shave himself. This is a contradiction parallel to that generated by the liar paradox. But few find the barber paradox very challenging. The proper response: there is no such barber. [15] There cannot be such a barber, because the description given of him is inconsistent. The inconsistency is a bit hidden, but the situation is essentially the same as if I had announced that there was a triangular square, and then asked you how many corners it has. You should just reject my scenario.


Something similar holds for the liar paradox: our language imposes inconsistent requirements on the proposition supposed to be expressed by the liar sentence, and as a result there can be no proposition expressed by the liar sentence. What inconsistent requirements? Roughly, the rules of our language require that the liar sentence be assigned, as its meaning, the proposition that holds if and only if that very proposition does not hold. But there cannot be a proposition that holds when it doesn't hold. Hence, there is nothing to serve as the meaning of the liar sentence. Hence, the sentence cannot be either true or false.

To explain that more slowly: first, what is a proposition? Without getting overly metaphysical, let us simply say that propositions are the sort of things that one can assert, deny, believe, or doubt; they can be true or false, probable or improbable, possible or impossible.[16] Proposition s are not to be confused with sentences, since more than one sentence may express the same proposition; for instance, "Squirrels are furry" expresses the same proposition (asserts the same thing) as "Les écureuils sont poilu" – two sentences, one proposition. Nor should proposition s be confused with beliefs in an individual's mind, since it is possible for two different people to believe the same thing; that 'thing' is a proposition.

Proposition s can be identified by their truth conditions. That is, given any determinate set of conditions, there is a proposition that holds (or obtains, or is true) just in case those conditions are satisfied; and for every proposition, there is a determinate set of conditions under which the proposition is true. When we speak of "the proposition that so-and-so", this refers to the proposition that holds whenever so-and-so. For instance, "the proposition that squirrels are furry" denotes the proposition that holds if and only if squirrels are furry.

Now, what does it mean to say that a sentence is false? It means that the proposition expressed by the sentence is false. Thus, the liar sentence,

(L) This sentence is false.

is intended to assert that the proposition expressed by L is false. That is, L is supposed to express some (unique) proposition, and it is also intended to assert that that very proposition is false. These intentions can only be satisfied if there is a proposition that is identical to the proposition that that very proposition is false – in other words, there would have to be a proposition that holds precisely when it does not hold. But of course there is no such proposition. So L lacks any determinate meaning.

Some find the notion of an inconsistent language puzzling. In what sense can a language be inconsistent? To clarify, note first that I am not saying that the liar sentence is inconsistent. If that were so, then the liar sentence would simply be false. But it is neither true nor false. Nor am I saying that any other sentence is inconsistent. (Some sentences are inconsistent, but that fact does not explain the liar paradox. Nor is a language rendered inconsistent merely because it permits one to formulate inconsistent sentences.)

Second, I am not saying that our language embodies an inconsistent theory. Rather, the sort of inconsistency I have in mind is like the inconsistency in inconsistent instructions. Suppose you open the instructions for your new smart phone and you read, "Do not drop the phone into the bathtub. Also, drop the phone into the bathtub." Then you could call the instructions inconsistent. It is not that the instructions endorse a false or inconsistent theory; it is that the instructions logically could not all be followed.

How could our language embody inconsistent instructions? Not, of course, in the same way that an instruction booklet would contain inconsistent instructions, for the booklet would do so by containing certain sentences written in a natural language. Our language is not a collection of sentences. Rather, our language is constituted by a set of conventions, conventions that govern how linguistic expressions are supposed to be used and interpreted. These conventions can sometimes be described in words, but they may exist independent of their being linguistically formulated, simply by our having certain practices that we are disposed to conform to. Among other things, the conventions of our language dictate the meanings that should be assigned to sentences, including what proposition (if any) a given declarative sentence should be understood as expressing.

Sometimes, a set of instructions is inconsistent only when applied to certain cases. For instance, suppose that your phone instructions tell you, "Hold the power button for three seconds, but do not hold the top button on the right side of the phone." These instructions would be fine for some models of phone. But suppose that you find that the top button on the right side of your phone is in fact the power button. Then the instructions, as applied to this phone, are inconsistent.

Similarly, our language implicitly contains a set of instructions for interpreting sentences, and these instructions are fine for most sentences. But as applied to the liar sentence, they are inconsistent, that is, they cannot be followed, because they require us to understand the liar sentence as expressing a kind of proposition that can't exist.

Lastly, note that I am not saying, as Tarski suggested, that the concept of truth is inconsistent, nor is any other particular concept or sentence relevant to this discussion inconsistent. The inconsistency at issue arises jointly from the conventions for interpreting each of the individual words in the liar sentence, the conventions for interpreting the sentence structure that the liar sentence instantiates, and the particular syntax of the liar sentence. It is all those things together that generate inconsistency – just as it was the phone instructions together with the particular configuration of your phone that generated an inconsistency in the above example.

The liar paradox, in my view, is like the following puzzle: "Consider the proposition that both holds and does not hold. Does that proposition hold?" Either answer gets you into a contradiction. But this is not a very challenging puzzle. We should just deny that there is any such proposition. The liar paradox seems more challenging only because, instead of directly describing a proposition that supposedly holds and does not hold, it exploits our natural disposition to follow the rules of our language to induce us to attempt to interpret a sentence as expressing a proposition that holds and does not hold.

### 2.6.2 Meaning Deficiency

We may be tempted to call L meaningless. But this would seem off: unlike "Blug trish ithong", which is really completely meaningless, "This sentence is false" seems to have some sort of meaning. After all, we can understand each word in it, we understand the way in which they are combined, and we know how to make inferences that depend on its meaning – for instance, we know that if the sentence is taken to be true, one can infer that it is false.

In general, the meaning of a sentence is established by the conventions, language usage patterns, and intentions of speakers of the language. These things provide the "instructions" for interpreting the sentence – at the least, they place constraints on how the sentence can be faithfully interpreted. In the case of "Blug trish ithong", there are no instructions since there are no relevant conventions, usage patterns, or intentions; hence, it is properly called "meaningless". A meaningful sentence is one for which there are some (more or less determinate) instructions. In the ideal case, the implicit instructions are fully determinate and consistent, in which case they determine a unique proposition; that is, the constraints rule out all but one proposition as the meaning of the sentence. But actual sentences commonly fall short of this ideal. The result is sentences that are not meaningless, but merely have a defective meaning.

There are two kinds of meaning deficiency. The first occurs when the instructions for interpreting a sentence are insufficiently determinate, that is, they rule out too little. In this case, there are multiple propositions that the conventions fail to rule out as interpretations of the sentence. This includes cases of ambiguity and vagueness, the latter of which will be discussed in chapter 3.

The second kind of meaning deficiency occurs when the instructions for interpreting a sentence are inconsistent, that is, they rule out too much. In this case, there is no proposition that can satisfy all the constraints created by the linguistic conventions (etc.). This is the case with the liar sentence and related paradoxical sentences.

### 2.6.3 The Truth-Teller

Compare another sentence, which I will call "the truth-teller sentence":

(T) This sentence is true.

Reasoning about the truth-value of T does not lead to a contradiction in the way that reasoning about L seems to. (T is true if and only if T is true – nothing wrong with that.) Nevertheless, T poses a puzzle. We could consistently deem it either true or false, but there seems to be no basis for calling it one rather than the other. To the question, "Is it true or false?", either answer seems arbitrary. What does my view say about this case?

In my view, T fails to express a proposition and thus lacks a truth value. For T is intended to express the proposition that the proposition expressed by T is true. In other words, T is supposed to express the proposition that holds if and only if that very proposition holds. This time, the problem is not that there is no such proposition; the problem is that this is true of every proposition, and we are given no further guidance about what specific proposition T is supposed to express. Nor is there any proposition whose sole truth-condition is that it be true. So there is no determinate proposition singled out by T. In that sense, T is meaning-deficient.

The problem with L was that there are too many constraints on the proposition it is supposed to express. It is analogous to the description, "The man who is female", to which nothing corresponds. The problem with T is that there are too few constraints on the proposition it is supposed to express, so that more than one thing satisfies them. It is analogous to the description, "The man who is male," which lacks a determinate referent.

A non-deficient sentence is one for which we have just enough constraints so that a single proposition satisfies them. Such sentences are analogous to the description, "The man who wrote this book", which specifies a unique individual.

### 2.6.4 "The Liar Sentence Is Not True" Is True

Now consider again the following pair of sentences$^1$${^9}$ :

(L") Sentence L" is not true. (N) Sentence L" is not true.

On my view, L" fails to express a proposition ; thus, in particular, it fails to express a true proposition. So it isn't true. (Nor is it false, of course.)

Now, I just asserted that L" is not true, and there was nothing wrong with that. In general, it is perfectly fine for a sentence other than L" itself to assert that L" is not true. For instance, sentence N, on my view, is correct. N expresses the proposition that L" is not true; yet L" does not express that proposition, even though L" is syntactically identical to N. Why is this? Because when we read L", we are invited to accept an inconsistent story about the proposition that it expresses; but when we read N, there is no inconsistent story about what N expresses.

Remember the analogous barber paradox. Contrast the following two stories about the barber. Story #1: There is an (adult, male) barber living in Boulder who shaves all and only the Boulder men who do not shave themselves. Who shaves the barber? Answer: There cannot be any such barber, because you gave an inconsistent description of him. Story #2: There is an (adult, male) barber living in Denver who shaves all and only the Boulder men who do not shave themselves. Who shaves the barber? Answer: It could be anyone (maybe he shaves himself, maybe someone else shaves him). Note that there is no reason why this second barber can't exist, since there is nothing inconsistent in this story.

Similarly: L" invites us to accept an inconsistent story about the proposition that it expresses (L" does not explicitly assert this story; rather, the "story" is implied by the rules of our language, the rules for how one is supposed to interpret sentences). The story is that there is a proposition that (i) is expressed by L", and (ii) holds if and only if L" doesn't express a truth. Conditions (i) and (ii) are inconsistent. Since these are the requirements for something to be the proposition expressed by L", there is no proposition expressed by L".

Matters are otherwise with sentence N. Sentence N only requires that there be a proposition that (i) is expressed by N, and (ii) holds if and only if L" fails to express a truth. Now there is no inconsistency in supposing that a proposition satisfies both (i) and (ii). So there is no obstacle to holding that N expresses such a proposition. In general, sentences express what they are supposed to express, unless there is some reason why they can't. So N expresses the proposition that holds if and only if L" fails to express a truth.

### 2.6.5 This Sentence Is False or Meaning-Deficient

What if we modify the liar sentence to something like LM:

(LM) This sentence is either false or meaning-deficient.

? I have said that L is meaning-deficient. If I claim, similarly, that LM is meaning-deficient, won't it follow that LM is actually true (and therefore not meaning-deficient)?

No, it won't. LM is neither true nor false, because LM does not express any proposition. In particular, LM does not express the proposition that LM is either false or meaning-deficient; hence, LM is not made true by LM's being either false or meaning-deficient. In other words, if we consider the following reasoning -

1*. If a sentence says that $a$ is $F$ or $G$, then the sentence is true if and only if $a$ is $F$ or $G$.

2*. LM says that LM is false or meaning-deficient.

3*. Therefore, LM is true if and only if LM is false or meaning-deficient.

- I reject premise 2*. Why? Because for something to be the proposition expressed by LM, it must (i) be expressed by LM, and (ii) be a proposition that holds if and only if LM is false or meaning-deficient. Nothing could satisfy both conditions. (By the definition of "true" as applied to sentences, if a proposition is expressed by LM, then that proposition is true if and only if LM is true. It could not also be the case that that proposition is true if and only if LM is false or meaning-deficient.)

### 2.6.6 Liar Cycles

What about series of sentences that generate paradoxes, such as this pair:

(L1) The following sentence is true. (L2) The preceding sentence is false.

? Each sentence, considered by itself, seems alright; neither sentence introduces an inconsistent set of conditions for the proposition to be expressed. This is shown by the fact that if some other sentence – say, “Squirrels are furry” – were inserted between L1 and L2, then both L1 and L2 would be perfectly meaningful and would have determinate truth values.

As things stand, however, neither L1 nor L2 is either true or false. Both fail to express propositions. The reason is that the rules for determining what propositions L1 and L2 express are circular, given the actual situation (namely, that L2 immediately follows L1). Propositions are individuated by their truth conditions. The rules of our language dictate that (given the actual syntax of L1 and L2)

i)

to find the truth conditions for L1, one is to first find the truth conditions for the sentence that follows it (which happens to be L2), and one is to assign L1 the same truth conditions; also,

ii)

to find the truth conditions for L2, one is to first find the truth conditions for the sentence that precedes it (which happens to be L1), and one is to assign L2 the opposite truth conditions.

This set of instructions cannot be followed; they send us into an interminable cycle.²⁰

Why not say that one of the two sentences is meaning-deficient, but the other fully meaningful? This would be enough to avoid paradox. Perhaps L1 expresses a proposition, since, when we read L1, we seem to understand it. If a normal sentence, such as "Squirrels are furry", appears next, then things are fine. It is only when we get to L2, finding that L2 refers us back to L1, that the breakdown occurs. So we might be tempted to say it is L2 that is meaning-deficient.

But there is no reason to single out L2 for the blame. Though we usually read from top to bottom, someone could start reading with L2. Thinking everything is fine so far, they proceed next to L1, and that is when the breakdown occurs. (We could also imagine a piece of paper that has "The sentence on the other side of this page is true" written on one side, and on the other side, "The sentence on the other side of this page is false.") Since there is no relevant difference between L1 and L2, if either of them is meaning-deficient, they both are.

Here, I have spoken of a procedure for assigning the meanings of L1 and L2, noting that this procedure would never terminate. This is loose talk; the reason L1 and L2 lack meaning is not that a human being cannot determine their truth-conditions. (There could be a sentence whose meaning cannot be determined by a human being – say, because the sentence is too complicated for a human being to grasp – but it need not therefore be meaning-deficient.) The reason L1 and L2 lack meaning is that the rules of the English language, together with certain features of the actual situation (notably, the fact that L2 immediately follows L1 on the page) fail to pick out a unique set of truth conditions for the two sentences. These rules and features require that L1 express a proposition that holds if and only if the proposition expressed by L2 is true, and that L2 express a proposition that holds if and only if the proposition expressed by L1 is false. But no pair of propositions can satisfy these conditions. So L1 and L2 fail to express propositions.

What if "false" in L2 were replaced with "true", to remove the contradiction? Then the problem would change from inconsistency to indeterminacy: the rules of the language, given the factual situation, would dictate only that L1 and L2 must be assigned propositions with the same truth value. This meagre constraint fails to pick out a unique pair of propositions.

### 2.6.7 Prohibiting Liars

As noted earlier (section 2.5), some philosophers believe that natural languages such as English are defective since they allow sentences like the liar sentence to be constructed. On their view, we should have a language in which the grammatical rules for forming sentences do not allow the liar sentence, or other paradoxical sentences or sets of sentences, to be formulated in the first place.

While it may be in some sense a defect of English that it allows the liar sentence to be formulated, I think this is not an important defect, and the project of formulating rules whereby one could declare the liar sentence "ungrammatical" or syntactically ill-formed is not a useful project.[21]

Why? Compare another social construction: the law. There are undoubtedly many inconsistencies in the body of law governing, say, the United States. In addition, many legal doctrines are sufficiently vague or ambiguous that there are many possible cases in which it is indeterminate whether an action is legal or not. How serious of a problem is this? The answer depends on how often we in fact run into inconsistencies or cases of indeterminate legality. If we can easily, unequivocally classify almost all actual actions as legal or not, then the law may serve its functions well enough – at least, it won't be prevented from doing so by the mere possibility of cases in which we cannot say what is legal. Note that the existence of inconsistencies in the body of law does not mean, for example, that murder is legal, or that we don't know whether it is legal, or that it is both legal and illegal. It is unequivocally illegal.

Similarly, our language is not prevented from serving its function by the mere possibility of a grammatical sentence that fails to express a proposition. The purpose of language is to communicate, which we do well enough in normal circumstances. We do not have a persistent problem where people fail to communicate due to their having unwittingly (or wittingly) uttered liar-like sentences. There are some possible grammatical sentences that fail to express proposition s due to inconsistency in the rules for interpreting them, but these sentences are hardly ever used (due precisely to the fact that they fail to express proposition s). The fact that contradictions can be derived if we take certain sentences to express propositions does not prevent us from assigning consistent, unequivocal interpretations to most sentences. Hence, liar sentences do not pose a significant obstacle to the functioning of language.

Nor is there any reason to expect that there must be some purely syntactic rule whereby all and only the paradox-generating sentences of English can be excluded. I would, however, be happy to provide a non-syntactic rule for identifying meaning-deficient sentences: if the rules of our language, when combined with the actual relevant facts (about, e.g., the circumstances in which a sentence is uttered), entail contradictory claims about the proposition expressed by a given sentence, or if they fail to single out a unique proposition as the one expressed by the sentence, then the sentence fails to express a proposition. In short: the meaning-deficient sentences include the ones for which there exists paradoxical reasoning (as in the case of sentences L, L1, L2, and the like), plus the ones for which there is nothing that would make them true or false (as in the case of sentence T). It is precisely the paradoxical reasoning about L that tells us that L is meaning-deficient.


## 2.7 Curry's Paradox

Sometimes philosophy students ask for advice on how to get a job after graduation. Fortunately, I have discovered a logically fool-proof method. When you apply for the job that you desire, just include the following sentence in your cover letter:

C Either this sentence is false, or you will hire me.²²

This guarantees that you will be hired. For suppose C is false. In that case, the first disjunct is true. But if the first disjunct is true, then the whole disjunction is true. So actually, C cannot be false.

So now suppose C is true. In that case, the first disjunct is false. Since the whole sentence is true while its first disjunct is false, it must be that the second disjunct is true. So you will be hired. It doesn't matter what your qualifications are, who recommended you, or how good you are in interviews; the hiring committee will simply be logically compelled to choose you, on pain of contradiction.

Here is a more explicit statement of the reasoning:

1. If a sentence says that $p$ or $q$, then the sentence is true if and only if either $p$ or $q$. (Premise.)

2. Sentence C says that C is false or you will be hired. (Premise.)

3. C is true if and only if either C is false or you will be hired. (From 1, 2.)

If C is false, then C is true. (From 3.)

5. C is true. (From 4.)

6. Either C is false or you will be hired. (From 3, 5.)

7. You will be hired. (From 5, 6.)

My solution to this puzzle parallels my solution to the Liar Paradox: premise 2 is false, because sentence C fails to express a proposition. The reason is that the rules for determining what proposition C expresses are inconsistent: they require that C be assigned, as its meaning, the proposition that holds if and only if either that very proposition fails to hold, or you will get the job. This would be a proposition that would be made true by its own failure to be true. But there cannot be a proposition that would be made true by its own failure to be true. So C does not express a proposition.

## 2.8 The Paradox of Non-Self-Applicability

Here is another paradox cut from the same cloth as the Liar.²³ Some properties apply to themselves. For instance, the property of being a property is itself a property; hence, it applies to itself (or possesses itself, or instantiates itself). The property of abstractness, I suppose, is abstract. Hence, abstractness is also self-applicable. On the other hand, most properties fail to apply to themselves. For instance, the property of being a cat is not itself a cat. Therefore, cathood is not self-applicable. The property of being happy is not itself happy (only people can be happy, not properties). So happiness, too, is non-self-applicable.

Now consider the property of non-self-applicability (the property of failing to apply to oneself): does this property apply to itself? Well, it applies to itself if and only if it does not apply to itself. Contradiction.

My solution: there is no such property as non-self-applicability, because it has an inconsistent definition. Non-self-applicability is defined to be the property that applies to each thing, $x$, if and only if $x$ does not apply to $x$. That definition yields a contradiction when "non-self-applicability" is plugged in for $x$. So there is no such property.

You might protest: it certainly seems as if there is such a property. When I say that cathood does not apply to itself, and happiness does not apply to itself, it seems that I am in each case saying something sensible (and true). It seems that I am pointing out something that cathood and happiness have in common.

I think this intuition can be captured by acknowledging the existence of properties that are very similar to the supposed property of non-self-applicability. Here are two of them:

Non-self-applicability$^{(+)}$:

The property that applies to each thing, other than non-self-applicability$^{(+)}$ itself, if and only if that thing does not apply to itself, and which also applies to itself.

Non-self-applicability$^{(-)}$:

The property that applies to each thing, other than non-self-applicability$^{(-)}$ itself, if and only if that thing does not apply to itself, and which does not apply to itself.

Thus, the intuition that cathood is non-self-applicable may be replaced, say, with the judgment that cathood is non-self-applicable$^{(+)}$.

## 2.9 Russell’s Paradox

It used to be thought that, for any well-defined predicate, there is a set containing all and only the things to which the predicate applies. For instance, corresponding to the predicate “is red”, there is the set of all red things – that is, the set such that for any $x$, $x$ belongs to the set if and only if $x$ is red.

This idea runs into paradox when we consider the predicate “is not a member of itself”. The corresponding set would be the set of all things that are not members of themselves. Call this “the Russell set” (after its inventor, Bertrand Russell).$^{24}$ Is the Russell set a member of itself or not? For any $x$, the Russell set contains $x$ if and only if $x$ isn’t a member of itself; that’s the definition of the Russell set. If we substitute the Russell set itself for $x$, we see that the Russell set contains the Russell set, if and only if the Russell set isn’t a member of itself. That is a contradiction:

$$R \in R \leftrightarrow R \notin R$$


The standard solution: The Russell set does not exist. Everyone agrees on that, though there are several different accounts of exactly why the Russell set does not exist. There are, that is, a variety of proposed principles describing what sorts of sets exist; each proposed set of principles, to be considered adequate, must exclude the Russell set.

I don't have a comprehensive theory of what sets exist.²⁵ But I know this much: a putative set does not exist if it has an inconsistent definition. "The set that has exactly three members and has exactly two members" does not denote anything. Nor does "the set that contains itself if and only if it does not do so". Nor, for the same reason, does "the set that contains all and only the things that don't contain themselves".

### References

Beall, J.C. 2009. *Spandrels of Truth*. Oxford: Oxford University Press.

Beall, J.C. and Michael Glanzberg. 2011. "Liar Paradox", *Stanford Encyclopedia of Philosophy*, http://plato.stanford.edu/entries/liar-paradox/, accessed April 30, 2017.

Braakuis, H.A.G. 1967. "The Second Tract on Insolubilia Found in Paris, B.N. Lat. 16.617. An Edition of the Text with an Analysis of Its Contents," *Vivarium* 5 (1967): 111–45.

[Crossref]

Clark, Michael. 2002. *Paradoxes from A to Z*. London: Routledge.

Curry, Haskell B. 1942. "The Inconsistency of Certain Formal Logics", *Journal of Symbolic Logic* 7: 115–117.

[Crossref]

Eklund, Matti. 2002. "Inconsistent Languages", *Philosophy and Phenomenological Research* 64: 251–75.

[Crossref]

Geach, Peter. 1950. "Russell's Theory of Descriptions", *Analysis* 10: 84–8.

[Crossref]

Grelling, Kurt and Leonhard Nelson. 1908. "Bemerkungen zu den Paradoxien von Russell und Burali-Forti" ("Remarks on the Paradoxes of Russell and Burali-Forti"), Abhandlungen der Fries'schen Schule n.s. 2: 301-34.

Herzberger, Hans G. 1967. "The Truth-Conditional Consistency of Natural Language", Journal of Philosophy 64: 29-35.

[Crossref]

Huemer, Michael. 2016. Approaching Infinity. New York: Palgrave Macmillan.

[Crossref]

Irvine, Andrew David and Harry Deutsch. 2016. "Russell's Paradox", The Stanford Encyclopedia of Philosophy, ed. Edward N. Zalta, https://plato.stanford.edu/archives/win2016/entries/russell-paradox/, accessed May 28, 2017.

Littmann, Greg and Keith Simmons. 2004. "A Critique of Dialetheism", pp. 314-35 in The Law of Non-Contradiction, ed. Graham Priest, J.C. Beall, and Bradley Armour-Garb. Oxford: Oxford University Press.

[Crossref]

Priest, Graham. 2006a. In Contradiction: A Study of the Transconsistent, expanded ed. Oxford: Clarendon.

[Crossref]

Priest, Graham. 2006b. Doubt Truth to Be a Liar. Oxford: Clarendon.

Prior, Arthur N. 1955. "Curry's Paradox and 3-valued Logic", Australasian Journal of Philosophy 33: 177-82.

[Crossref]

Quine, Willard van Orman. 1986. Philosophy of Logic, second ed. Cambridge, MA: Harvard University Press.

Rescher, Nicholas. 2001. Paradoxes: Their Roots, Range, and Resolution. Chicago, IL: Open Court.

Russell, Bertrand. 1902. Letter to Frege dated 16 June, 1902, reprinted on pp. 124-5 in Jean van Heijenoort, ed. From Frege to Gödel: A Source Book in Mathematical Logic, 1879-1931. Cambridge, MA: Harvard University Press, 1967.

Russell, Bertrand. 1903. *The Principles of Mathematics*. Cambridge: Cambridge University Press.

Russell, Bertrand. 1908. "Mathematical Logic as Based on the Theory of Types", *American Journal of Mathematics* 30: 222–62.

[Crossref]

Russell, Bertrand. 1972. "The Philosophy of Logical Atomism", pp. 1–125 in *The Philosophy of Logical Atomism*. London: Routledge.

Sainsbury, Richard M. 2009. *Paradoxes*, 3rd ed. Cambridge: Cambridge University Press.

[Crossref]

Sloman, Aaron. 1971. "Tarski, Frege and the Liar Paradox", *Philosophy* 46: 133–147.

[Crossref]

Spade, Paul Vincent. 1975. *The Mediaeval Liar: A Catalogue of the Insolubilia-Literature*. Toronto, Canada: Pontifical Institute of Mediaeval Studies.

Strawson, Peter F. 1950. "On Referring", *Mind* 59: 320–44.

[Crossref]

Tarski, Alfred. 1944. "The Semantic Conception of Truth: And the Foundations of Semantics", *Philosophy and Phenomenological Research* 4: 341–76.

[Crossref]

Tarski, Alfred. 1983. "The Concept of Truth in Formalized Languages", pp. 152–278 in *Logic, Semantics, Metamathematics: Papers from 1923 to 1938*, 2nd ed., ed. John Corcoran, tr. Joseph Henry Woodger. Indianapolis: Hackett.

### Footnotes


11


12


13


14


15


16


17


18


19


20


21


22


23


24


25


#### Notes


1. Why not use the more general T-schema, “P is true if and only if P”, where the second “P” may be replaced with any declarative sentence, and “P’” replaced with a name for that sentence (as in Tarski 1983)? This is *usually* correct; for instance, the following is correct: “Snow is white’ is true if

and only if snow is white." But the schema does not always work; consider: "This is the beginning of this sentence' is true if and only if this is the beginning of this sentence." The formulation given in the text avoids such complications.

2. Unless otherwise stated, I use "or" inclusively; thus, "A or B" means "At least one of {A, B} holds, possibly both."

3. Priest 2006a, b; Beall 2009.

4. Cf. Quine 1986, p. 81: "[S]urely the notation ceased to be recognizable as negation when they took to regarding some conjunctions of the form [p &amp; ~p] as true."

5. Objections of this sort appear in Littman and Simmons 2004, pp. 322-4, and Sainsbury 2009, pp. 157-8.

6. Priest (2006b, ch. 5) and Beall (2009, pp. 48-50) take essentially this line, except that they frame the issue in terms of whether the negation operator validates explosion (the principle that (A &amp; ~A) entails B, for any arbitrary B). My claim is not that the meaning of negation by definition validates explosion. My claim is that the meaning of negation directly rules out a sentence and its negation both being true.

Priest and Beall construct arguments that the classical notion of negation is incoherent, which I will not discuss in detail. Priest's main argument turns on shifting the burden of proof onto classical theorists to show that classical negation is coherent, and then arguing that they cannot do so without begging the question. I believe, though I will not argue the point here, that the burden is on Priest to show that "not!" is incoherent. Beall's argument, in essence, uses the Liar Paradox itself to impugn the existence of the "not!" operator. In reply, I have a solution to the paradox that does not require abandoning classical logic.

7. This appears to be the most common view. See, e.g., Rescher 2001, pp. 196-203; Clark 2002, p. 102. Philosophers with this view disagree, however, on exactly why L fails to express a proposition.

8. This sort of view was taken by some medieval philosophers; see the anonymous authors discussed in Braakuis 1967 and in Spade 1975, pp. 33-4. Cf. Rescher (2001, pp. 196-7).

9. Geach 1950; Strawson 1950.

10. I thank Iskra Fileva (p.c.) for this suggestion.

Cf. Beall and Glanzberg 2011, section 2.3.1.

Tarski 1944. Russell (1908) adopts a similar but more restrictive view.

Of course, this only applies to simple sentences in subject-predicate form; however, if you know what this footnote means, then you probably already know how to extend the definition of truth_{1} to other sentence forms. If you don’t know what this footnote means, then you probably don’t care.

This means that the second premise in the paradoxical reasoning, “L says that L is false”, is also problematic, since it attempts to deploy a generic notion of “saying” something. If “saying” is limited to first-order saying, second-order saying, and so on, then the liar sentence does not say any-thing, since it does not first-order say anything, nor does it second-order say anything, and so on.

This is what everyone says about it, e.g., Rescher 2001, p. 144; Sainsbury 2009, pp. 1–2; Irvine and Deutsch 2016, section 4. The “paradox” first appears in Russell (1972, p. 101; originally published 1918), attributed to an unnamed person. Russell appears to have found it so trivial that he does not bother to state the solution.

More specifically, propositions are the primary bearers of truth, falsity, and so on; that is, anything else that is true, false, or the like, is so in virtue of its relation to a true or false, etc., proposition. A true sentence is one that expresses a true proposition, a true belief is a belief directed at a true prop-osition, and so on.

Herzberger (1967), for example, argues that it is impossible for a language to be inconsistent.

As Eklund (2002) maintains.

Previously mentioned in section 2.4.3 above.

Cases like this are discussed by Sloman (1971, pp. 136, 139).

Sloman (1971, pp. 142–3) takes a similar view.

This paradox derives from Curry 1942; see also Prior 1955.

This paradox derives from Russell (1902, 1903, p. 102). Grelling and Nelson (1908) restate the paradox in slightly different words, which somehow has led some to call it “Grelling’s Paradox” or “the Grelling-Nelson Paradox” (as in Clark 2002, pp. 80–81).

Russell 1902, 1903, p. 102.

Except that perhaps no sets exist; see my 2016, ch. 8.