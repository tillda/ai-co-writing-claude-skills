---
book: "Logical Forms"
title: "Chapter 01 Validity"
chapter_number: "1"
chapter_name: "Validity"
author: "Mark Sainsbury"
table_of_content: |
  1 What is logic about?
  3 Possibility: logical and physical
  4 Validity, inconsistency and negation
  5 Arguments and argument-claims
  6 Some important properties of validity
  7 Validity and usefulness: "sound", "relevant", "persuasive"
  8 Sentences and propositions
  9 Validity and truth conditions
  10 Formal validity
  11 The logical constants
  12 The project of formalization
    (1) Lexical ambiguity
    (2) Structural ambiguity
    (3) Syntactic irregularity
    (3) Syntactic irregularity
---

# 1 Validity

## 1 What is logic about?

The philosophy of logic gives an account of what logic is, of the concepts that it uses, and of how it relates to other disciplines and to our ordinary thought and talk.

Logic is about reasons and reasoning. There are reasons for acting: wanting to keep thin is a reason for avoiding fatty foods. There are reasons for believing: that the potatoes have been boiling for twenty minutes is a reason for believing that they are ready to eat. Historically, logic has primarily concerned itself with reasons for believing.

We may give a reason for believing when we answer the question “Why does so-and-so believe such-and-such?”. But such a question can be answered in two different kinds of way.

Suppose we ask of an orthodox Hindu: why does he suppose that one should not eat meat? One kind of answer is: this belief was instilled in him by his family at an early age, and has been sustained by a variety of social and personal pressures. This kind of answer may explain the origin of the belief. But it does not give a reason for the belief, in the sense of “reason” in which logic is concerned with reasons. Explanations of this kind belong to psychology or sociology. They are quite foreign to logic.

Suppose we answer the question in a different way, saying: the Hindu believes that killing, and everything which requires killing, is wrong; and that eating meat requires killing. This answer may explain the origin of the belief. But it also does, or purports to do, something else: it justifies the belief. Understood in this way, as attempting to provide a justification, the answer shows a concern with reasons in the sense in which logic can be said to be the study of reasons.

Logic is a normative discipline. It aims to say what reasons are good reasons. It does not merely describe the reasons that in fact move people. It lays down standards. It says what reasons ought to move one. Even so, the starting-point has to be what we generally think of as good reasons. Logic starts with an intuitive commonsensical and pretheoretical distinction between good and bad reasons, a distinction made by people pursuing their ordinary daily concerns. From this the logician hopes to fashion an articulate and defensible distinction between good reasons and bad. One would expect a large measure of agreement between the logician’s technical distinction and the commonsensical one. But one should not turn one’s back on the possibility of a divergence: common sense may need to be corrected in the light of reflection.

Here are some examples, of an everyday kind, of the commonsensical distinction at work. Most people would agree that

James is a banker and all bankers are rich is a good reason for

James is rich.

By contrast, most people would agree that

Henry is a playwright and some playwrights are poor is not a good reason for

Henry is poor.

There is (or until recently was) no general agreement about whether

James and Henry lead pretty similar lives except that James is a non-smoker and Henry smokes twenty cigarettes a day is or is not a good reason for

Henry is more likely to die of heart disease than James.

We can regard a reason as a good reason without having to believe it ourselves. We do not have to believe that all bankers are rich to see that “James is a banker and all bankers are rich” constitutes a good reason for “James is rich”. Traditionally, the logician has supposed that one can investigate whether one thing is or is not a good reason for another without having to form a view about whether the supposed reason, or what it is a reason for, is true.

When we talk about reasons, we do not have to talk about particular people and what they believe. Even if no one had ever had the beliefs we attributed to the Hindu, we could still say that

Killing, and everything which requires killing, is wrong; eating meat requires killing together form good reasons for

One should not eat meat.

What one means can be partly understood in this way: if anyone were to believe that killing, and everything which requires killing, is wrong, and were also to believe that eating meat requires killing, he would thereby be right (rational, reasonable, logical, justified) also to believe that one should not eat meat.

When we want to consider something like

Killing is wrong in abstraction from whether anyone believes it or not, we shall call it a proposition. A proposition is the sort of thing that can be believed, or asserted, or denied, but it does not have to be: it can be disbelieved, or merely entertained, or not even thought of at all. Perhaps no one believes, or had even until just this moment supposed or entertained, the proposition that Julius Caesar built New York single-handed in a day. We shall, nevertheless, say that there is such a proposition.


The most general question which confronts the logician can now be expressed as follows: what makes one proposition (or collection of propositions) a good reason for a proposition?

We shall call the propositions offered as reasons premises, and the proposition which the premises are supposed to support the conclusion.

071 007100 07171 071 0001 00 0 0 0 0 0 0 0 0 0

When some premises and a conclusion are assembled together, we shall call the result an *argument*. The technical use of these terms, as just introduced, differs in some ways from the ordinary use. In particular, as used in logic, the term “argument” does not imply any kind of disagreement or dispute.

We have already considered various arguments:

1) **Premises**: Killing, and anything which requires killing, is wrong; eating meat requires killing.

*Conclusion*: One should not eat meat.

2) **Premise**: James is a banker and all bankers are rich.

*Conclusion*: James is rich.

3) **Premise**: Henry is a playwright and some playwrights are poor.

*Conclusion*: Henry is poor.

4) **Premise**: James and Henry lead pretty similar lives except that James is a non-smoker and Henry smokes twenty cigarettes a day.

1) All men are mortal. Socrates is a man. So Socrates is mortal.

2) The sun has risen every morning so far; so (probably) it will rise tomorrow.

The first is a standard example of an argument classified as valid by deductive logic. The second is an argument which is not classified as valid by deductive logic. However, the inductive logician is supposed to accord it some reasonably favourable status. Certainly, the reasons which the premises of *`(2)`* give for its conclusion are better by far than those given by the same premises for the opposite conclusion:

3) The sun has risen every morning so far; so (probably) it will not rise tomorrow.

This may seem a silly argument, but apparently something quite like it moves some gamblers. The "Monte Carlo fallacy" consists in the belief that if there has been a long run of reds on the roulette wheel, it is more likely to come up black next time.

Ex. 1.2 What is the statistical truth, of which the Monte Carlo fallacy is a distortion? Can the truth be used to formulate a rational betting policy for roulette?

11

The deductive logician contrasts *`(1)`* and *`(2)`* by saying that the first but not the second is valid. The inductive logician will make a contrast between *`(2)`* and *`(3)`* – probably not by using the word “valid”, but perhaps by saying that *`(2)`*, unlike *`(3)`*, is “inductively strong”. The premises of *`(2)`*, but not those of *`(3)`*, provide strong reasons for the conclusion.

The premises of *`(1)`* also provide strong reasons for its conclusion. How are we to distinguish strong deductive reasons from strong inductive ones? We have a suggestion before us: the truth of the premises of a valid deductive argument makes the falsity of its conclusion impossible, but this is not so in the case of inductively strong arguments. Another way of putting this is: the reasons given by a deductively valid argument are *conclusive*: the truth of the premises guarantees the truth of the conclusion. This way of making the contrast fits *`(1)`* and *`(2)`*. The truth of the premises of *`(2)`* may make the conclusion that the sun will rise tomorrow *probable*, but it does not guarantee it: it does not make it *certain*.

Inductive logic, as the terminology of inductive strength suggests, must be concerned with a relation which holds to a greater or lesser degree. Some non-conclusive reasons are stronger than others. So unlike deductive logic, which will make a sharp dichotomy between valid and invalid arguments, inductive logic will discern a continuum of cases, along which *`(2)`*, perhaps, registers fairly high, whereas *`(3)`* registers very low indeed.

Deductive validity is, as logicians say, *monotonic*. That is, if you start with a deductively valid argument, then, no matter what you *add* to the premises, you will end up with a deductively valid argument. Inductive strength is not monotonic: adding premises to an inductively strong argument can turn it into an inductively weak one. Consider *`(2)`*, which is supposed to be a paradigm of inductive strength. Suppose we add the premises: there is a very large meteor travelling towards us; by tonight it will have entered the solar system and will be in stable orbit around the sun; it will lie between the sun and the earth, so that the earth will be in permanent shadow. When these premises are added, the resulting argument is far from strong. (I have assumed one particular interpretation of what it is for the sun to “rise”. However one interprets this phrase, it is easy enough to find premises adding which would weaken the argument.)

Much everyday reasoning is non-monotonic, and there are endless much simpler and more realistic cases than the one just given. At the The start of the investigation, Robinson's confessing to the crime gives you a powerful reason for believing him guilty. But you may rightly change your mind about his guilt, without changing your mind about whether he confessed, when a dozen independent witnesses testify to his being a hundred miles away at the time of the crime. This is a typical case in which adding information can weaken reasons which, on their own, were strong.

Table 1.1

|   | Valid deductive reasoning | Strong inductive reasoning  |
| --- | --- | --- |
|  Truth of premises gives good reason for truth of conclusion | ☑ | ☑  |
|  Truth of premises makes falsity of conclusion impossible | ☑ | ☐  |
|  Premises are conclusive reasons | ☑ | ☐  |
|  Monotonic | ☑ | ☐  |
|  Degrees of goodness of reasons | ☐ | ☑  |


Table 1.1 summarizes the differences between deductive and inductive logic that we have so far mentioned.

I said that not everyone would agree that there is any such thing as inductive logic. A famous proponent of an extreme version of this view is Karl Popper ([1959], ch. 1, §1). He has argued that the only sort of good reason is a deductively valid one. A consequence of his view is that there is nothing to choose between *`(2)`* and *`(3)`*, considered simply as arguments: both are equally bad, being alike deductively invalid. He would therefore reject the ticks in the first and last rows of the right-hand column of table 1.1. For Popper, there is no such subject matter as the one I have tried to demarcate by the phrase "inductive logic"; no inductive argument gives a good reason; and there is no difference of degree among the goodness of "inductive reasons", all being equally bad. Accordingly, Popper sees the main activity of science not as a search for supporting evidence for hypotheses, but as an effort to weed out false hypotheses by showing by experiment that they have false deductive consequences.

A less radical sceptic about inductive logic may allow that there are good reasons which are not deductively valid, but deny that there is any systematic discipline worthy of the name “inductive logic”. Reflection on the role of background knowledge in what are called inductively strong arguments, like *`(2)`*, may ground such a scepticism. Inductive strength, as we have seen, is non-monotonic. Hence an argument cannot be assessed as inductively strong absolutely: some possible background information would greatly weaken the conclusion. This means that every assessment of inductive strength must be relativized to a body of background knowledge. It is far from obvious how the project of inductive logic should attempt to accommodate this point, for it is quite unclear how the background knowledge could be specified in a way which is neither question-begging (for example, saying that such-and-such an argument is inductively strong relative to any bodies of background knowledge not containing any information which would weaken the conclusion), nor quite unsystematic (for example, listing various bodies of background knowledge). There is thus a genuine (I do not say decisive) ground for doubting whether inductive logic could aspire to the kind of system and generality attained by deductive logic.

A still less radical scepticism about the possibility of inductive logic takes the form: there is such a subject matter, but it does not deserve to be called logic. Here is one reason why a person might hold this view. It may be said that anything worthy of the name of logic must be formal: the property of arguments with which it is concerned must arise wholly from the form or pattern or structure of the propositions involved. Whatever exactly “formal” means (see below, §10), it certainly seems to be the case that no formal question is at issue between those who do, and those who do not, think that the evidence shows that smoking increases the risk of heart disease.²

Another form of this kind of scepticism is as follows. Logic is apriori, but inductive “logic” is not, so it is not really logic. Consider the assessment of (1.4), the argument about smoking and heart disease. No doubt the interpretation of statistical evidence would be important, and perhaps there is an apriori discipline of statistics. But even conceding


Table 1.2

|   | Deductive logic | Inductive “logic”  |
| --- | --- | --- |
|  Truth of premises gives good reason for truth of conclusion | ✓ | ?  |
|  Systematic | ✓ | ?  |
|  Formal | ✓ | ?  |
|  Apriori | ✓ | ?  |

this, it seems at least arguable that some non-apriori material is involved. If so, if, that is, it is not a purely apriori matter whether or not some argument is inductively strong, then inductive “logic” would not be an apriori discipline, and this would make it very unlike deductive logic.

**Ex. 1.3** What is likely to be at issue between one who does and one who does not think that the evidence shows that smoking increases the risk of heart disease?

Table 1.2 summarizes the various kinds of scepticism about the possibility of inductive logic.

I offer no assessment of the sceptical claims. However, from now on I shall discuss only deductive logic – logic, for short – and deductive validity – validity, for short.

## 3 Possibility: logical and physical

Consider the following two arguments:

1) This young tomato plant has all the moisture, nutrients, warmth and light that it needs; so it will grow good tomatoes.

2) This person is an adult male and has never married; so he is a bachelor.

Tradition has it that the first is invalid (i.e. not valid) and the second is valid. We suggested in §2 that a valid argument is one whose premises cannot be true without the conclusion being true also. But is there not a sense of “impossible” in which it is impossible for the premises of (1) to be true without the conclusion also being true?


Perhaps. But there is also a sense of “possible” in which this does not hold. The plant might be attacked by wireworms or destroyed by a meteorite before the tomatoes grow, even though it has all the moisture etc., that it needs.

The following two claims will help us distinguish two kinds of possibility: physical possibility and logical possibility.³

3) It is impossible for an internal combustion engine, used on level roads on the earth’s surface, to return 5,000 mpg.

4) It is impossible for there to be a car which, at a given time, both has exactly three and exactly four wheels.

(3) is probably true, if the kind of impossibility involved is physical: the laws of nature being what they are, no ICE could be as efficient as that. But it is not true if the kind of impossibility involved is logical. What is logically impossible involves some kind of contradiction or inconsistency, as illustrated in (4). Logical impossibility typically issues from the very nature of the concepts involved, and is not beholden to the laws of nature. It is logically possible for the laws of nature to be very different from what they actually are.

Ex. 1.4 (a) Why should a difference in natural law not be a physical, rather than a logical, possibility?

**`(b)`** Give three examples, not in the text, of states of affairs which are logically possible but physically impossible.

**`(c)`** Give three examples, not in the text, of states of affairs which are logically impossible.

**`(d)`** Are any states of affairs logically impossible but physically possible?

**`(e)`** Are the following logically impossible, physically impossible, or neither? (“Don’t know” may be the best response in some cases!).


**`(i)`** Mr Stamina has at last perfected his perpetual motion machine.

**`(ii)`** Mary has precisely twice as many children as Jane: she has the twin girls and little William.

**`(iii)`** Jock ("the Flash") McVite ran the mile in under 3.5 minutes.

**`(iv)`** The notorious swindler. Siva Malgavany, who died in 1880 in the arms of one of his many mistresses, was reincarnated in 1997 as a small Irish terrier, owned by Mrs Fortescue-Brown of Egham, Surrey.

**`(v)`** On 15 March 1998, Dr Chronowski stepped into his time machine, and stepped out again to find himself present at the battle of Waterloo.

A definition of validity needs to draw upon the notion of logical rather than physical possibility, if it is to give a correct account of the logician's usage. Consider the following example:

5) This creature has the form of a finch; so it will not discourse intelligently about Virginia Woolf.

As the word "valid" is standardly used in logic, this is not a valid argument. This classification might be challenged: intelligent discourse requires suitable musculature and thorax, and suitable complexity of brain; but it is impossible that a creature having the form of a finch should have such a thorax etc., and a sufficiently large brain. So it is impossible for the premise of the argument to be true without the conclusion also being true. So the argument is valid.

This objection uses the notion of physical rather than logical possibility. The laws of nature that we actually have rule out there being a brain of sufficient complexity for discourse in a finch-sized skull. So it is physically impossible for the premise of (5) to be true yet its conclusion false. But it is not logically impossible. We might have had different laws of nature. There is no logical guarantee that discourse requires a larger than finch-sized brain. So it is logically possible for the premise of (5) to be true yet the conclusion false. So the argument is not valid.

We can now set out our preliminary definition of validity:

Ex. 1.5 (a) Is *`(3.5)`* nevertheless inductively strong? Compare its inductive strength with that of *`(3.1)`*, justifying your comparison.

(b) Would it make a difference to the validity of the argument in *`(3.5)`* if the first premise were "This creature is a finch"?

An argument is VALID if and only if it is logically impossible for all the premises to be true yet the conclusion false.

Ex. 1.6 (a) In each of the following cases, say whether the argument is deductively valid, inductively strong, or neither. Justify your answers:

(i) I told you to add more pepper if you thought the stew was too bland. You added more pepper even though you didn't think the stew was too bland. So you disobeyed me.

(ii) You must know how to make a sling, if you are really a qualified nurse. But evidently you don't know how to make a sling. So you are not a qualified nurse.

(iii) He has coughed up arterial blood, so his lungs must be extensively damaged.

(iv) My father was born in London, yours in Paris. So we can't be brothers.

(v) This plant grew from a seed produced by a tomato plant. So it, too, is a tomato plant.

**`(vi)`** Frank Whittle died in poverty. Therefore, the inventor of the jet engine died in poverty. [Historical note: Frank Whittle invented the jet engine.]

**`(vii)`** The satellite picture shows a cold front sweeping in from the Atlantic, and it should reach our shores by morning. So it will probably rain tomorrow.

**`(viii)`** The explanation of any fact is in terms of other facts. So if any facts can be explained, there are facts which cannot be explained.

**`(ix)`** If you know anything, you can't be mistaken. So any proposition that could be false is one which you do not know.

**`(x)`** The proposition "All propositions are false" is false. For if it were true it would be false. [In ordinary English, the conclusion of an argument may be presented before the premises.]

**`(xi)`** Geraniums are not frost hardy. There are frequent frosts in Iceland. So geraniums are not native to Iceland.

**`(xii)`** If either the CIA agent or the KGB agent killed the President, he used a gun. But the President died of cyanide poisoning. So neither the CIA agent nor the KGB agent killed him.

(b) Think of a stack of four cards with numbers on one side and letters on the other. Someone tells you that all cards which have an even number on one side have an "E" on the other. Say which of the following cards you need to turn over in order to tell whether what he said is true:

|  6 | 3 | E | A  |
| --- | --- | --- | --- |

Explain how this example relates to the validity of various arguments involving what the person said as one of its premises.

(c) We can use cards in the manner of the previous example to specify situations. Thus each card might represent a person in a bar, one side indicating whether he is an adult or a minor, the other side indicating whether he is drinking alcohol or a soft drink. Suppose there are again four cards having visible sides as follows:

|  Alcohol | Soft | Adult | Minor  |
| --- | --- | --- | --- |

Which cards do you need to turn over in order to check whether the bar is violating the rule that only adults may drink alcohol? Explain how your answer relates to the validity of arguments having as a premise "Only adults drink alcohol".

This definition has some merits. For one thing, it suggests an answer to why we should use valid arguments: valid arguments are necessarily truth-preserving. So long as you start out with truth, you will never depart from the truth if you keep to valid arguments. Moreover, it is rather surprising how much can be extracted about the nature of validity from even this preliminary definition (see §6).

However, the definition has many defects. We characterized logic as the study of validity. But now, in defining validity, we have used the notion of logical impossibility. If we fully understood what logical impossibility is, presumably we would already know what logic itself is. So our characterizations have run in a circle.

We mentioned a connection between logical impossibility and inconsistency and contradictoriness. But these terms themselves were left unexplained.

This unsatisfactory state of affairs will have to persist for some time. One feature of definitions of validity for the formal languages to be considered in later chapters is that they can entirely avoid such notions as logical possibility and inconsistency (in the ordinary sense). For the moment, we shall see how far the ordinary notions can take us.


## 4 Validity, inconsistency and negation

A collection of propositions is *inconsistent* if and only if it is logically impossible for all of them to be true. Here logical impossibility is used to explain inconsistency, whereas in §3 inconsistency was used to explain logical impossibility. This shows that the two notions are closely related. It also shows that we could reasonably hope for a further elucidation of both notions, one which takes us out of the circle. For the moment, we shall simply take for granted the notion of logical impossibility.

Consider the propositions:

1. The earth is spheroid.

2. The earth is not spheroid.

It is logically impossible for both these propositions to be true and logically impossible for both of them to be false. In short, *`(1)`* and *`(2)`* are *contradictories*: each is a contradictory of the other. Moreover, *`(2)`* is the *negation* of *`(1)`*. You get the negation of a proposition if you insert “not” (or some equivalent expression) into it in such a way as to form a contradictory of it.

Ex. 1.7 Without using “not” (or any equivalent word or phrase) form a contradictory of each of the following:

(i) Tom has no children.

(ii) Richard Nixon died in 1981.

(iii) London is north of Paris or south of Paris.

Being the negation of a proposition is one way, but not the only way, of being a contradictory of it. Being contradictories is one way, but not the only way, for two propositions to be *inconsistent*. I shall amplify these points, and then connect the notions of contradictory, inconsistency and negation with that of validity.

If one proposition is the negation of another, if follows trivially from the definition that the two propositions are contradictories. The converse does not hold. Two propositions can be contradictories without either being the negation of the other. For example:

3) John is more than six feet tall

and

4) John is either exactly six feet tall or else less than six feet tall

are contradictories, but neither is the negation of the other. Negation is one way, but not the only way, of forming a contradictory.

Inserting "not" into a proposition does not always yield the negation of it, for inserting "not" does not always yield a contradictory. Consider:

5) Some men are happy.

6) Some men are not happy.

The second results from the first by inserting a "not", but the two propositions are not contradictories, since both could be - and presumably actually are - true. So *`(6)`* is not the negation of *`(5)`*.

Similarly,

7) Reagan believes that Shakespeare was a genius

8) Reagan believes that Shakespeare was not a genius

are not contradictories, since both could be false. They would be false if Reagan had no view one way or the other about Shakespeare's qualities. Hence *`(8)`* is not the negation of *`(7)`*.

Ex. 1.8 Which of the following pairs consists of a proposition and its negation?

(i) I hope you will come.

I hope you will not come.

(ii) I hope you will come.

I do not hope you will come.

(iii) I am pleased with your progress.

I am not at all pleased with your progress.

(iv) Everyone who goes to see Mick the Fix is satisfied with his handling of their problem.

Everyone who goes to see Mick the Fix is not at all satisfied with his handling of their problem.

(v) You must not walk on the grass.

You must walk on the grass.

Any collection of propositions containing a contradictory pair is inconsistent. It is impossible for both of two contradictory propositions to be true, so it is impossible for all the propositions in a collection containing a contradictory pair to be true. The converse does not hold: there are inconsistent collections containing no contradictory pair. For example:

9) John is over six feet tall. John is under six feet tall

is an inconsistent collection, for it cannot be that both propositions are true. Since both could be false (and would be, if John were exactly six feet tall), they are not contradictories.

Ex. 1.9 Give three examples (not in the text) of collections of propositions which are inconsistent, but where no member of the collection is a contradictory of any other member.

Figure 1.1 summarizes the relationships mentioned. All pairs of propositions of which one is a negation of the other are contradictories, and all contradictories are inconsistent. However, there are inconsistencies which are not contradictories, and contradictories of which neither is a negation of the other.

Part of the link between validity and inconsistency, mediated by the notion of contradictoriness, consists in the following fact:

10) If an argument is valid, a collection of propositions consisting of its premises together with a contradictory of its conclusion is inconsistent.

![img-0.jpeg](_images-ocr/chapter1/p17-img-0.jpeg)

Figure 1.1

To illustrate, consider the following argument:

11) Anyone who drives a car risks death. Anyone who risks death is brave. So all car drivers are brave.

**Ex. 1.10 Is the argument in (4.11) valid? Is the conclusion true?**

The following collection contains the premises of *`(11)`* as (i) and (ii) and the negation of its conclusion as (iii):

12) (i) Anyone who drives a car risks death.

(ii) Anyone who risks death is brave.

(iii) Not all car drivers are brave.

Take any two of these propositions. We can see that, if these two are true, then the third cannot be. So the collection is inconsistent.

We can argue quite generally for (10), using the definition of validity given in §3. Take any valid argument. By definition, it is logically impossible for its premises to be true yet its conclusion false. In other words, it is logically necessary that if all the premises are true, so is the conclusion. But if the conclusion is true, then, necessarily, any contra dictory of it is false. So, necessarily, if the premises are true, any contradictory of the conclusion is false. So it is logically impossible for the premises and a contradictory of the conclusion all to be true. So this collection is inconsistent.


The link between validity and inconsistency also runs in the other direction:

13) If a collection of propositions is inconsistent, any argument whose premises consist of all but one of the collection, and whose conclusion is a contradictory of the remaining proposition, is valid.

The argument for this is rather like the one just given for *`(10)`*. Taking *`(10)`* and *`(13)`* together shows that we could have defined validity in terms of inconsistency, rather than in terms of logical impossibility.

Ex. 1.11 Provide an argument which justifies (4.13).

Ex. 1.12 Give a definition of validity in terms of inconsistency.

## 5 Arguments and argument-claims

We use “argument” to refer to any collection of propositions, one of which is singled out as the conclusion. It is useful to have a standard pattern for writing out arguments. We adopt the convention that where there is no contrary indication, the conclusion of an argument is the last proposition in a list, and is marked off from its predecessors by being preceded by a semicolon. Thus if an argument has two premises, $A$ and $B$, and a conclusion, $C$, we shall write it:

$$A, B; C.$$

More generally, where the argument has $n$ premises, and its conclusion is $C$, we write:

$$A_{1}, \ldots, A_{n}; C.$$

($n$ may be equal to or greater than zero. For the case in which $n = 0$ (there are no premises) see §6.)

A useful abbreviation is “$\models$”, short for “is valid”. It works like this:

1) $A_{1}, \ldots, A_{n} \models C$ abbreviates $A_{1}, \ldots, A_{n}; C$ is valid.

$A_{1}, \ldots, A_{n} \not\models C$ abbreviates $A_{1}, \ldots, A_{n}; C$ is not valid.

The symbol “$\models$” is pronounced “(double) turnstile”.

An argument $(A_{1}, \ldots, A_{n}; C)$ must be distinguished from what I shall call an argument-claim: $A_{1}, \ldots, A_{n} \models C$, or $A_{1}, \ldots, A_{n} \not\models C$. The component propositions in an argument are true or false, but the argument itself cannot significantly be said to be true or false. One correct dimension of assessment for an argument is whether it is valid or not; another is whether it is persuasive or not; but truth and falsehood do not provide a proper dimension of assessment. By contrast, an argument-claim is true or false: true if it is a positive argument-claim $(\models)$ and the argument in question is valid, or if it is a negative argument-claim $(\not\models)$ and the argument in question is not valid; and otherwise false.

In an argument-claim, "$\models$" appears in the very place in which, in an expression of the argument in ordinary English, one would find a word like “so”, “therefore” or “hence”: a word used to show that one has come to the conclusion which is being drawn from the previous propositions. This gives rise to a tendency to confuse the role of “$\models$” with that of conjunctions like “therefore”. But the roles are really very different.

First, “$\models$” and “therefore” belong to different grammatical categories. “$\models$” is a predicate, the sort of expression which can be used to attribute a property to something. “Therefore” is not a predicate, but rather a word used to join sentences together. To see the force of this point, consider the fact that we can meaningfully say “Some arguments are valid but others are not” (bearing in mind that “$\models$” abbreviates “is valid”), though we cannot meaningfully say “Some arguments are therefore, but some are not”.

Secondly, something of the form “$A_1, \ldots, A_n$, therefore $C$” is an argument, about which the question arises whether or not it is valid. By contrast, something like “$A_1, \ldots, A_n \models C$” is not itself an argument, but rather a claim about an argument, the claim that it is valid.

Thirdly, in ordinary circumstances, one who propounds an argument, $A_1, \ldots, A_n$, therefore $C$, is thereby committing himself to the truth of all of $A_1, \ldots, A_n$. But one who makes the claim that $A_1, \ldots$

$$A_n \models C$$

makes no such commitment, since there are valid arguments whose premises are not true.⁴

Ex. 1.13 (a) What is the relation between “;”, as used here in setting out arguments, and “hence” or “therefore”?

(b) For each of the following pieces of discourse, state what argument, if any, you think the speaker is intending to propound. If you think he is intending to propound one, say what its premises and conclusion are:

(i) My opinion, for what it’s worth, is that you should take to robbing banks. This is a demanding career, requiring a high degree of responsibility, but offering greater than average financial rewards. Moreover, it gives you the opportunity to be your own boss and to develop your talents of leadership and initiative. If all else fails, it provides you with free board, lodging and protection at the expense of Her Majesty’s Government.

(ii) If John and Mary are godparents of the same child, as indeed they are, they cannot be married according to Christian rites.

(iii) Since John and Mary are god parents of the same child, they cannot be married according to Christian rites.

(iv) John and Mary are god parents of the same child. Therefore, they cannot be married according to Christian rites.

(v) Treason doth never prosper. What’s the reason? Why, if it doth, then none dare call it treason.

(vi) No contemporary politician understands the French as well as de Gaulle did. Mitterrand is at home with the intellectual Left, and d’Estaing knows the aristocracy and the haute bourgeoisie. But de Gaulle knew something about the traditional peasant class, which is what sets him apart from our contemporaries.

(vii) Authors of sentimental novels were not being so ridiculous as they appeared to later generations when they described so many abductions, ladders, musketeers and escapes from convents. All these exciting events actually took place, and frequently, too. It was part of the current vogue for aggressive Spanish manners.

(viii) It was late and I was tired. So I took a taxi.


## 6 Some important properties of validity

Although our definition of validity in §3 is not as illuminating as one might wish, it none the less enables us to discover some important general features of validity.

The key property of validity is that it logically guarantees the preservation of truth. If you start with truth and argue validly then you are bound to end up with truth. That is why it is a good thing to argue validly. But validity does not always generate truth (see 1)), nor does truth always generate validity (see 3)).

Ex. 1.14 (a) Are there any valid arguments with false premises and a true conclusion? If so, give an example. (Here and elsewhere, select examples of propositions which are well known to be true, or false, as the case may be.)

(b) Are there any valid arguments with true premises and a false conclusion? If so, give an example. If not, say why not.

(c) If an argument is invalid and at least one of its premises is false, what can be inferred about whether or not its conclusion is false?

(d) If an argument is valid and has a false conclusion, what can be inferred about whether or not its premises are true?

1) There are valid arguments with false conclusions.

Example:

2) All heavenly bodies revolve around the earth. The sun is a heavenly body. Therefore the sun revolves around the earth.

Moreover:

3) There are invalid arguments with true premises and true conclusions.

Example:

4) Petroleum can be used as a fuel. More people live in Paris than in Boston. Therefore, the first man on the moon was an American.

We have already seen that deductive validity is monotonic. Using the notation of §5, this can be expressed:

5) If $[A_1, \ldots, A_n \models C]$,

then $[A_1, \ldots, A_n, B \models C]$, whatever $B$ may be.$^5$

In other words, you cannot turn a valid argument into an invalid one by adding to the premises. This elaborates what is meant by saying that deductive logic aims to pick out arguments in which the premises give conclusive reasons for the conclusion.

Another important property of validity, as classically conceived, and as defined in §3, is a kind of transitivity. Chaining arguments together will preserve validity:

6) If $[A_1, \ldots, A_n \models C]$ and $[B_1, \ldots, B_k, C \models D]$,

then $[A_1, \ldots, A_n, B_1, \ldots, B_k \models D]$.

The intermediate conclusion, $C$, can be cut out, since the premises which establish it can establish anything it can establish.

**Ex. 1.15** Using the displayed definition of validity near the end of §3, show that (5.6) is true.

Validity has a property akin to reflexivity:

7) If $C$ is among the $A_1, \ldots, A_n$, then $[A_1, \ldots, A_n \models C]$.

**Ex. 1.16** Using the displayed definition of validity near the end of §3, show that (5.7) is true.

This shows that circular arguments are valid. (Of course, they are not normally useful: see (7.4) below.)


A new piece of terminology: we shall express the claim that a collection of propositions $(A_1, \ldots, A_n)$ is inconsistent by writing:

$$
(A_1, \ldots, A_n) \models .
$$

The terminology is justified by the fact that if an argument's premises are inconsistent, it is valid; and this is suggested by the blank after the turnstile, accepting any completion. More formally:

8) If $[(A_1, \ldots, A_n) \models]$, then $[A_1, \ldots, A_n \models B]$, whatever $B$ may be.

**Ex. 1.17** Use this notation to express the claim: “If a collection of propositions is inconsistent, it remains inconsistent whatever proposition is added to it.” Now argue for the truth of this claim.

Like all the other properties of validity described in this section, this one follows from the definition given in §3. If premises are inconsistent, they cannot all be true. If premises cannot all be true, then, in particular, the following case cannot arise: that all the premises are true, and also some arbitrary proposition, $B$, is false. So it is impossible for all the premises to be true yet $B$ false. So an argument with inconsistent premises is valid, whatever its conclusion.

(8) should not be read as saying that you can infer anything from an inconsistency. As we normally speak of inference, one can infer something from one or more premises only if those premises are true. A detective can draw inferences, correct or incorrect, from the footprints, but if there were no footprints, and he were merely hallucinating, we wouldn't normally allow that he could no any inferring, because we would not normally allow that there was anything from which to infer. Given this conception of inference, (8) does not license inferences from inconsistencies, for no inconsistencies are true.

A further piece of terminology. Let us write

$$
\vdash A
$$

to abbreviate: “it is logically impossible for $A$ to be false”. The terminology is justified by the fact that if an argument’s conclusion cannot be false, then it is valid; and this is suggested by the blank before the turnstile, accepting any completion. This claim can be expressed as follows:


9) If $\models A$, then $B_1, \ldots, B_n \models A$, whatever $B_1, \ldots, B_n$ may be.

This shows how we can extend the notion of an argument to include the case in which there are zero premises. This does not reflect anything in ordinary usage, but it is convenient for logic.

Ex. 1.18 (a) Show that: If $\models B$, then $A_1, \ldots, A_n \models C$ if and only if $A_1, \ldots, A_n, B \models C$. This shows that necessary truths are redundant as premises. You may now wish to think back to your answer to Ex. 6a(vi).

(b) Show that: If $B \models$, then $A_1, \ldots, A_n, B \models C$, whatever $A_1, \ldots, A_n, C$ may be. Could "if" here be strengthened to "if and only if"? Justify your answer.

The properties of validity mentioned in this section are properties of the traditional notion. In various ways, some of which we shall discuss in §7, the traditional notion may seem to fall short of what we want. This has prompted the development of various "non-classical" conceptions of validity. Our concern is confined to the classical notion.

Ex. 1.19 (a) Say whether or not you think that: $A_1, \ldots, A_n \models C$ if and only if $\models$ If $A_1$ and $\ldots$ and $A_n$ then $C$. Briefly justify your view.

(b) Show that:

$A \models$ if and only if $\models$ It is not the case that $A$.

(c) Is it true that

$A \models$ if and only if $\nvdash A$?

Justify your answer.

## 7 Validity and usefulness: "sound", "relevant", "persuasive"

Even if an argument is valid, it may not be *useful*: it may not be a good one to use, either to discover what is true or to persuade an audience of something. For example, consider:

1) Some circles are square. Therefore there will be no third world war.

Since it is logically impossible for any circles to be square, (1) is valid (its validity follows from (6.8)). But the argument would not be a good one to use for any purpose, and certainly not to convince someone that there will be no third world war. Normally, a good argument is not merely valid. In addition, it has true premises. An argument which has true premises and is valid is called *sound*.

The last remark is qualified by "normally" since there is at least one circumstance in which it is useful to propound a valid argument with a false premise. This is when one hopes that one's hearer will recognize that the conclusion is false and that the argument is valid, and so will be persuaded that at least one premise is false. This mode of argument is called *reductio ad absurdum*.

Suppose your hearer believes that Harry is a merchant seaman, but you disagree. Suppose also that you both know that Harry's arms are not tattooed. Then you might say:

2) Suppose Harry is a merchant seaman. All merchant seamen have tattoos on their arms. So Harry must have tattoos on his arms.

One intends one's hearer to recognize the validity of the argument, and, persisting in his belief that the conclusion is false, to come to infer that at least one premise is false. One has to hope that he will be more firmly persuaded of the truth of "All merchant seamen have tattoos on their arms" than of "Harry is a merchant seaman", so that he will retain the former belief and abandon the latter.

A sound argument may fail to persuade an audience if the audience does not realize that the premises are true, or does not realize that the argument is valid. Here the fault lies with the audience, not with the argument. But a sound argument can still be defective, in that it may not be useful. Consider:

3) Washington is the capital of the USA. Therefore all dogs are dogs.

Since it is logically impossible for “All dogs are dogs” to be false, (3) is valid (its validity follows from (6.9)). Since the premise is true, it is also sound. But the argument is not useful. Part of the reason is that no argument is needed in order to persuade someone of something so trivial as the conclusion of (3). Another part of the reason is that the premise has no proper relevance to the conclusion. For an argument to be useful, it must, normally, be sound, and must, always, be relevant. Logicians have tried to devise special logics to reflect the concept of relevance. But this is one more topic we shall not pursue (see Anderson and Belnap [1975], Read [1988]).

Consider:

4) The whale will become extinct unless active measures are taken to protect it. Therefore the whale will become extinct unless active measures are taken to preserve it.

This is valid (its validity follows from (6.7)). It is sound, since its premise is true (if you disagree, select your own example). It is intuitively relevant, for whatever precise account we give of this notion it appears that nothing could be more relevant to whether a proposition is true than whether that very proposition is true. But the argument is plainly useless. It could not persuade anyone of anything, and it could not help in the discovery of truth.

For an argument to be persuasive for a person he must be willing to accept each of the premises but, before the argument is propounded to him, be unwilling to accept the conclusion. When the premise is the conclusion, he cannot be in this state. This is the general reason for the uselessness of circular arguments.

Ex. 1.20 (a) Could there be invalid arguments which are:

(i) sound?

(ii) relevant?

(iii) persuasive?

If so, give examples. If not, say why not.

(b) An argument can be sound and relevant, yet fail to be persuasive through being too elliptical. Give an example.

How could a valid argument ever be persuasive? It is possible because we do not always acknowledge or take explicit note of all the logical consequences of our beliefs. If we did explicitly hold before our minds all the logical consequences of our beliefs, seeing them as consequences, we would already have accepted the conclusion of any valid argument whose premises we have accepted. Hence no valid argument could be persuasive. This is how things would be with a perfectly rational being. The utility of valid arguments is a monument to our frailty: to the fact that we are not completely rational beings.

To sum up this section: validity is not the only desirable property in an argument. But it is the only one which normally concerns logicians.

## 8 Sentences and propositions

An argument consists of propositions. A proposition is what is believed, asserted, denied, and so on. This section elaborates this idea.

We can start with the relatively straightforward idea of a meaningful sentence. A sentence is a series of words arranged in accordance with the grammatical rules of the language in question in such a way that it can be used to say something (or to ask something or order something). "The cat sat on the mat" is a sentence which can be used to say that the cat is on the mat, but "cat sat mat on the the", though composed of just the same words, is not a sentence. Properly speaking, we should say: not an English sentence, for a sentence is defined relative to a language. The same series of words could be a sentence in one language but not in another. Thus:

1) Plus Robert court, plus Juliette change

is not an English sentence, despite being composed only of English words. But it is (or so I am told) a French sentence.

It is disputed both whether every grammatical sentence is meaningful, and whether every meaningful sentence is grammatical. On the latter point, most people occasionally speak ungrammatically, yet they are understood; and if the sentence they use can be understood, it is hard to justify counting it as not meaningful. On the first point, a standard example of grammatical sentences which are not meaningful is:

2) Green ideas sleep furiously together.

Arguably, this conforms with the rules of grammar, yet is not meaningful. The notion that will be important in this book is that of being meaningful, usable to say something (or to ask something or to order something). To the extent that being grammatical is not a useful guide to being meaningful, it should be set aside.

A preliminary definition of a proposition might run as follows:

3) A proposition is what is expressed, in a given context, by a meaningful, declarative, indicative sentence.

Various aspects of this definition require comment. A declarative sentence is one that could be used to make an assertion, to affirm that something is or is not the case. Thus:

4) The King is in his counting house

is a declarative sentence. By contrast

5) Is the King in his counting house?

is not a declarative sentence, but rather an interrogative one. Its typical use is not to affirm how things are, but to ask how things are.

6) Put the King in his counting house

is not a declarative sentence, but rather an imperative one. Its typical use is not to affirm that things are so-and-so, but to order that they be so-and-so.

An indicative sentence, one in what grammarians call the indicative mood, contrasts with a subjunctive sentence. Corresponding to the indicative (4) is the subjunctive:

7) Were the King in his counting house.

Subjunctive sentences are not used by themselves to affirm anything, but they may occur in sentences usable to affirm things. One common use is in subjunctive conditionals, for example:

8) Were the King in his counting house, the Queen would be content.

Two distinct sentences can express the same proposition. The English sentence

9) Snow is white

expresses the same proposition as the French sentence

10) La neige est blanche.

Even within a single language, distinct sentences can express the same proposition if they have the same meaning.

11) Blackie is a puppy

expresses the same proposition as

12) Blackie is a young dog.

Two sentences with different meanings can express the same proposition if they are used in different contexts, which is why the definition (3) mentions contexts. Suppose you are my only audience, and I address the following remark to you:

13) You are hungry.

Suppose that you then utter the sentence:

14) I am hungry.

We both express the same proposition. The first sentence, in the context of being directed at you, expresses the same proposition as the second, in the context of being uttered by you. Had you uttered the same sentence as me, (13), you would not have expressed the same proposition. This shows that the same sentence can, with respect to different contexts, express different propositions.

Ex. 1.21 (a) Suppose Tom utters the following sentence, directed at you: "I like kissing you". Give an example of a sentence you could utter and thereby express the same proposition as Tom expressed.

(b) Suppose Tom yesterday in London uttered the sentence "It is raining here". Give an example of a sentence you could utter today in Paris and thereby express the same proposition as Tom expressed.

(c) Suppose Tom, walking in the woods yesterday, dimly perceived what was in fact a boa constrictor (though he did not know it was), and, referring to that object, uttered: "That is the strangest looking rabbit I ever saw". Give an example of a sentence that you could utter today, in the comfort and security of your own home, and thereby express the same proposition as Tom expressed.

There is another way in which this can occur. A sentence may be ambiguous. For example, "There's that crane again" may refer to a lifting-device or a bird. There is no such thing in general as the proposition such a sentence expresses.

I have simply stipulated certain features of propositions, and their relations to sentences. What makes this an appropriate definition to adopt in logic? A standard answer is this: validity is defined in terms of truth conditions, and so one should identify a proposition by truth conditions. This answer relies on ideas that will be introduced in §9. However, we can see at once something of the motivation for the notion of a proposition, as used by logicians.

Consider the argument:

15) I am hungry; therefore I am hungry.

Intuitively this should count as valid. But suppose we thought of the components of arguments as sentences, and suppose we imagine the context shifting between the utterance of the premise and the utterance of the conclusion. Suppose you are hungry and utter the premise, and I am not hungry and utter the conclusion. Then we would have a true premise and a false conclusion, so the argument could not be valid. Clearly we need to avoid such problems, and introducing the notion of a proposition, in the style of this section, is one way of doing so.

We still could have defined an argument as a collection of sentences, but we would have had to say something about the context being held constant over all the sentences of an argument. The upshot would have been the same. On some occasions, it is easiest to think of arguments as composed of propositions, on others it is easiest to think of them as composed of sentences, with a background assumption of constancy of context. We will help ourselves to both notions, as convenient.

## 9 Validity and truth conditions

A sentence like “Snow is white” is true in some but not all logically possible circumstances. There are logically possible circumstances, including those which actually obtain, in which the sentence is true, and logically possible circumstances (in which, say, snow is black) in which the sentence is false. A circumstance is one in which a sentence is true just on condition that if the circumstance actually obtained, then the sentence would be true.

Some sentences, for example, “Snow is snow”, are true in all logically possible circumstances. Some sentences, for example “7 is less than 5”, are true in no logically possible circumstances.

We shall say that a sentence’s truth conditions are the circumstances in which it is true. We can think of these circumstances as bundled together in a collection or set – a set with no members, in the case of sentences like “7 is less than 5”. Using this notion, we can give yet another definition of validity:

1) $A_1, \ldots, A_n \models C$ if and only if the truth conditions of $C$ include those of $A_1, \ldots, A_n$.

We could put it another way: every circumstance in which all of $A_1, \ldots, A_n$ is true is one in which $C$ is true. Equivalently: the truth conditions of $A_1, \ldots, A_n$ are included in those of $C$. (1) and these variants define the same notion as that defined in §3.

Ex. 1.22 Show that an argument is valid according to (10.1) iff it is valid according to the definition of validity displayed near the end of §3.

The importance of this definition is that it shows that only the truth conditions of a sentence matter to the validity or otherwise of any argument in whose expression it occurs. A consequence is that if a sentence occurs in the expression of an argument and you replace it by one having the same truth conditions, the argument will remain valid, if it was valid before, or invalid, if it was invalid before. This will bear importantly on questions of formalization, to be considered later.

## 10 Formal validity

Logic, or at any rate formal logic, is not primarily concerned merely with the very general notion of validity which we have so far discussed. It is concerned with a particular species: *formal validity*. Formal validity, being a kind of validity, has all the properties of validity; but it has some additional distinctive features.

We could try to define formal validity by saying that an argument is formally valid if and only if it is valid in virtue of its form or pattern. This captures part of what is intended, though it will need supplementation. Here is a pair of arguments which are said to have the same form:

1) Frank will marry Mary only if she loves him. But Mary does not love Frank. So he will not marry her.

2) The whale will be saved from extinction only if active measures are taken. But active measures will not be taken. So the whale will not be saved from extinction.

These have a common form or pattern, which we could distil out as follows:

3) . . . only if——. It is not the case that——. So it is not the case that . . .

The dots are meant to be filled on both occurrences by the same sentence, and likewise the dash. It is more convenient to use letters, rather than dots and dashes, thus:

4) $A$ only if $B$. It is not the case that $B$. So it is not the case the $A$.

This can be called an *argument-form*. It is an argument-form of each of *`(1)`* and *`(2)`*, since these both result from it by making suitable replacements for $A$ and $B$.

**Ex. 1.23** Give two further instances (not in the text) of (10.4). Can you find any invalid instances?

The logician wants to say that *`(1)`* and *`(2)`* are valid in virtue of their pattern or form, the same in each case. This represents among other things an attempt to attain generality. It would be hopeless to try going through each argument in turn, picking out the valid ones. But if we are granted the idea of an argument-form we can say: not only is this specific argument valid; so are all of the same form.

One way to elaborate this a little is to define a notion of validity for argument-forms:

5) An argument-form is valid if and only if, necessarily, each of its instances is valid.

**Ex. 1.24** Why is the qualification “necessarily” needed in (10.5)?

So (4) is an example of a valid argument-form.⁶ An argument is valid *in virtue of* its form just on condition that it is an instance of a valid argument-form.

This goes some way towards saying what formal validity is, and we can reinforce the idea with two more examples before showing that an important ingredient is missing.

Consider:

6) All camels are herbivores. All herbivores are pacific. Therefore all camels are pacific.

This is an instance of the argument-form: “All . . . are——, all——are ***; therefore all . . . are ***.” “Camel” and “herbivore” are traditionally classified as nouns, “pacific” as an adjective. We shall call both of these, as they occur in *`(6)`*, *predicates*. We shall also include among predicates


relational expressions like “loves” and “is bigger by . . . than”. To mark the sort of gap that a predicate can fill, we shall use capital letters starting with “$F$”, so we shall write out the argument-form:

7) All $F$ are $G$. 
All $G$ are $H$. 
Therefore, all $F$ are $H$.

Assuming that this is a valid argument-form, it follows that *`(6)`* is not merely valid, but also formally valid.

**Ex. 1.25** Give a further instance (not in the text) of (10.7). Can you find any invalid instances?

8) Ian is Scottish. All Scots are prudent. So Ian is prudent.

This is an instance of the argument-form:

9) $\alpha$ is $F$. 
All $F$ are $G$. 
So $\alpha$ is $G$.

Here we use “$\alpha$” (and if needed, “$\beta$”, “$\gamma$”, . . .) to mark the position which a name can occupy. Assuming that (9) is valid, (8) is formally valid.

**Ex. 1.26** (a) Give a further instance (not in the text) of (10.9). Can you find any invalid instances?

(b) Specify valid argument-forms for any of the following which are formally valid:

(i) Some politicians are liars and all liars are charming. So some politicians are charming.

(ii) Some politicians are liars. Veredici is a politician. So Veredici is a liar.

(iii) If you are going to die by drowning, then there is no point in learning to swim. If you are not going to die by drowning, then there is no point in learning to swim. Therefore, there is no point in learning to swim.

(iv) Everyone who has studied logic is able to spot an invalid argument when he sees one. You haven’t studied logic. So you are not able to spot an invalid argument when you see one.

(v) 7 is prime. 
$7 = 5 + 2$. 
So $5 + 2$ is prime.

(vi) The battle of Marengo occurred before the French invasion of Moscow, and the battle of Waterloo came after that. So the battle of Marengo occurred before the battle of Waterloo.

(vii) He will die unless he is given a blood transfusion. But he will not be given a blood transfusion. So he will die.

This discussion has already begun to include some controversial elements. Highlighting these must wait for later chapters. For the moment, I want to bring out what is missing from the account so far: a gap which makes it inadequate as a presentation of the traditional idea of formal validity.

The idea was formal validity should be a special kind of validity. But as presented so far, nothing has been said to rule out formal validity coinciding with validity. For nothing has been said which prevents an argument itself counting as an argument-form. This is no accident of the particular way in which I have presented the idea. The general problem is this: what is the difference between pattern or form, and what fills it: substance or content? In *`(4)`*, for example, the remaining English words correspond to the pattern or form, the letters A and B to the places where one could insert content or substance to yield a genuine argument. But what is the basis for this distinction?

To bring out the problem, consider the sort of example that would standardly be given in a logic text of an argument which is valid but is not formally valid:

10) Tom is a bachelor. Therefore, Tom is unmarried.

This is certainly valid (reading "bachelor" in a familiar way). A case for saying that it is not formally valid might start by pointing out that *`(10)`* is an instance of the invalid argument-form.

11) $\alpha$ is $F$. Therefore $\alpha$ is $G$.

Ex. 1.27 (a) Justify the claim that (10.11) is invalid by finding an invalid instance of it. (To make the invalidity plain, pick an example with an obviously true premise and obviously false conclusion.)

(b) Show by example that each of (10.1), (10.2) and (10.6) are instances of invalid argument-forms.

(c) Show that every argument is an instance of at least one invalid argument-form.

How could the case be pressed further? What is needed for formal validity is that there be some valid argument-form of which the argument is an instance. So to establish failure of formal validity, it is not enough to cite one invalid argument-form of which the argument is an instance (cf. Ex. 1.27). You have to show that it is not an instance of any valid argument-form. But who is to say that *`(10)`* itself is not an argument-form? If it is, then, since *`(10)`* itself is its only instance, it is an instance of a valid argument-form, and so formally valid, contrary to the intention.

We might try to block this difficulty by stipulating that every argument-form must have some gaps (marked by dots and dashes, or letters). So every argument-form will have more than one instance. But (10) would still come out as formally valid, in virtue of being an instance of the valid

12) $\alpha$ is a bachelor. Therefore, $\alpha$ is unmarried.

If the concept of formal validity is to be narrower than that of validity, as the logician intends, the concept of form will have to be made more restrictive. The logician will stipulate that in an argument-form the only expressions we may use, other than the dots or dashes or letters which mark the gaps for the "content", are the logical constants. "Bachelor" and "unmarried", which occur in (12), are not logical constants, so (12) is not an argument-form, and so does not establish the formal validity of (10).

## 11 The logical constants

I shall begin by giving a list of expressions that are generally held to be logical constants:

1) it is not the case that

and

or

if . . . then . . .

if and only if

some

a

everything

all

is

are

is the same as

[plus any expression definable just in terms of the above].

It is a matter for philosophical debate whether the list should be extended to include, for example, “necessarily” or “is a member of” (as used in set theory). The debates arise from the fact that there is no general agreement about what makes an expression a logical constant. A list like the above fails to speak to this issue.

Historically, logical constants are so-called because they are given a constant interpretation within a logical system. Corresponding to words like “Socrates” and “man”, by contrast, there are variable interpretations. This gives a clear guide to what expressions are treated as logical constants by a logical system, but it does not explain or justify the selection of the logical constants: any expression could, in principle, be given a constant interpretation.

A widely held view, which certainly captures part of the truth, is that an essential feature of a logical constant is that it introduces no special subject matter. It should be “topic-neutral”. This is because, in logic, we are concerned with reasoning in general, and not with this or that special area of knowledge. It is all very well for an anthropologist concerned with kinship to take a particular interest in what is signified by such words as “bachelor” and “married”. The logician aims at greater generality. He will concern himself only with expressions which can occur in an argument on any subject whatsoever. The expressions in the list, but not expressions like “bachelor”, satisfy this requirement.

Bearing in mind the suggestion that argument-forms should contain, apart from devices for marking gaps, only logical constants, we can verify that (10.4), (10.7), (10.9) are argument-forms, but (10.12) is not one. This is consistent with the formal validity of (10.1), (10.2), (10.6) and (10.8), but is hostile to the formal validity of (10.10). If our list of logical constants can be assumed to be complete, or at least to exclude expressions like "bachelor" and "unmarried", then it seems that no argument-forms for (10.10) would be more apt to reveal it as formally valid than either the invalid (10.11) or the equally invalid


2) $A; B.$

If so, (10.10) is not formally valid.

In chapter 6.5 we will ask whether there is any illuminating and general account of logical constancy. If there is, then we can use it to give an account of formal validity: it will amount to validity in virtue of the meaning of the logical constants, and in abstraction from other than structural features of premises and conclusion. By structural features I mean facts about the recurrence of certain non-logical elements, for example the fact that "camels" occurs in the two places it does in (10.6). For the moment, we will make do with a relativized notion: given some list of constants, we will say that an argument is formally valid if and only if it is valid in virtue of the meanings of the constants on the list, and in abstraction from other than structural features of premises and conclusion.

The investigation of formal validity has in practice proceeded by turning away from ordinary English and studying artificial, "logical" languages like the language of the propositional calculus, and the language of the predicate calculus. What is the rationale for introducing these unfamiliar languages? The standard answer is in terms of their "clarity", but it is not clear that ordinary English is other than clear. In the following section, I consider some supposed defects of natural languages like English, considered from a logical point of view.

## 12 The project of formalization

If logicians really aim to study validity, as it occurs in our everyday thought and talk, why do they study artificial languages, which no one speaks? Why not stick to English, or French, or some other natural language?

An argument is a collection of propositions. But, according to a traditional justification of the turn towards formal languages, the sentences of natural languages like English do not adequately reflect the logical properties of the propositions they express. Formal logic is concerned with the very arguments we use in daily life, but it has to express these arguments in a different way.

This introduces the crucial idea of the logical form of a sentence. A sentence's logical form is supposed to lay bare the logical features of the proposition which it expresses. This logical form, it is said, is often hidden by ordinary language.

A traditional hope is that logic should provide a mechanical means of testing for validity.⁷ But how could you present a machine with arguments? If arguments are composed of propositions, then you cannot present a machine with arguments in any direct way, for propositions are too abstract. What you would have to feed into the machine are sentences. If the machine is to test the validity of the argument the sentences express, every logically relevant feature of the propositions must be correlated with some property of the physical make-up of the sentences.

It has been held that such a correlation does not obtain, or at least does not obtain in any readily statable fashion, between sentences of natural languages and the propositions they express. Hence the need for artificial languages. The idea is that these will supply the logical forms of sentences in natural languages. By translating a natural sentence into an artificial one, the hidden logical features of the proposition expressed will be brought to the surface.

Let us now consider some ways in which natural sentences may be supposed inadequate for logical purposes: inadequate as vehicles for bringing out the logical features of arguments.

### (1) Lexical ambiguity

As a special case of *`(6.7)`* it holds quite generally that:

$$
C \vDash C
$$


This holds whatever proposition $C$ may be. But, as we saw in connection with (8.15), it does not hold for arbitrary sentences of natural languages. One reason is that many sentences are ambiguous: they have more than one meaning, express more than one proposition. When this is due to the sentence containing a word with more than one meaning, we shall call the ambiguity *lexical*.

1) John cut the painter. Therefore John cut the painter

is not valid if we interpret “painter” in the first sentence to mean an artist, and interpret this word in the second sentence to mean a rope used to secure a boat; for then the first sentence may be true while the second is false.

An obvious way to deal with this problem is to distinguish two words, say “painter₁” and “painter₂”, one for each of the meanings, and throw away the ambiguous word. Then the proposed interpretation of (1) would look like this:

2) John cut the painter₁. Therefore John cut the painter₂

and no one would be particularly tempted to think that this expressed an argument of the form: $C$; $C$. (No doubt one would also have to distinguish ��cut$_1$” and “cut$_2$”.) The strategy of eliminating ambiguous words already involves departing from natural languages, in which ambiguous words are rife. But the proponent of artificial languages envisages altogether more radical departures.

### (2) Structural ambiguity

Some sentences are ambiguous, yet the ambiguity cannot be attributed to the ambiguity of one or more words in the sentence: the ambiguity is not lexical but *structural*. Here are some examples of allegedly structurally ambiguous sentences, with alternative interpretations added in brackets.

3) Harry is a dirty window cleaner. [(a) Harry is a dirty cleaner of windows; (b) Harry is a cleaner of dirty windows.]

4) Tom and Mary are visiting friends. [(a) Tom and Mary are visiting some people, and they are friends with these people;

(b) Tom and Mary are friends with one another, and they are visiting some people; (c) Tom and Mary are visiting some people, and these people are friends with one another.]

5) Receipts from this source are not liable to income tax under section iv, paragraph 19. [(a) Section iv, paragraph 19, exempts receipts from this source from liability to income tax; (b) section iv, paragraph 19, does not impose a liability to income tax on receipts from this source.]

6) I thought you were someone else. [(a) I thought you were someone other than the person you in fact are; (b) I thought you were someone who is not identical to himself.]

7) First speaker: "I ought to send flowers."

Second speaker: "No you ought not."

[(a) You are not under an obligation to send flowers; (b) you are under an obligation not to send flowers.]

8) Nicholas has written a book about everything. [(a) Nicholas has written a book, and it treats every subject; (b) for every subject, Nicholas has devoted at least one whole book exclusively to it.]

In none of these cases can the alleged ambiguity be attributed to any word. One way to test for this is to verify that each of the words can occur in a variety of sentences lacking the corresponding ambiguities, and this is not to be expected if the words are ambiguous.

Ex.1.28 Consider the following objection to the test mentioned in the text:

Despite the fact that "cut" is ambiguous, "I cut the string with my pocket knife" is not. Hence the fact that a word can occur in unambiguous sentences does not show that is unambiguous.

The existence of structural ambiguity shows that the elimination of lexical ambiguity is not enough. Some more radical approach is required.

Structural ambiguity seems to affect even logical constants, for example "not" in *`(7)`* and "a" and "everything" in (8). On one reading of *`(7)`* we think of "not" as dominating the sentence, to form its negation, a reading which we might write as "Not: you ought to send flowers". On the other reading, we think of "not" as governing just the description of the action, a reading which we might write as "You ought to do this: not send flowers". On one reading of (8) we think of "a" as dominating the sentence, a reading which we might write as: "A book by Nicholas is like this: it is about everything". In the other reading, we think of "everything" as dominating the sentence, a reading which we might write as: "Everything has this property: Nicholas has written a book about it". The logical constants determine formal validity (see §10 and §11). If structural ambiguity can affect the logical constants, then the hope of giving a general characterization of formal validity for English as it stands is undermined. Consider:


9) Logic, epistemology and metaphysics are all the philosophical subjects there are. Nicholas has written a book about logic. Nicholas has written a book about epistemology. Nicholas has written a book about metaphysics. Therefore, Nicholas has written a book about every philosophical subject.

If (9) is valid, the standard view is that it is formally valid. But there is no straightforward answer to the question whether it is valid. It all depends on how we understand the conclusion, which is structurally ambiguous in the same fashion as (8).

The problem for the account of formal validity is as follows. We said that a formally valid argument is valid in virtue of its form, and that this in turn is a matter of it being an instance of a form all of whose instances are valid. However, (9), read as invalid, is an instance of every argument-form of which (9), read as valid, is an instance. Hence (9) is not an instance of a valid argument-form. The problem of structural ambiguity threatens to deprive even the apparently formally valid reading of (9) of its formal validity.

Ex.1.29 If any of the following is ambiguous, give unambiguous paraphrases of the alternative interpretations:

(i) I am going to buy a book.

(ii) Everyone has a problem.

(iii) "In the whole wide beautiful world, Aldo Cassidy was the only person who knew where he was." (Le Carré [1971], p. 8)

(iv) "Most of all I would like to thank my students, who have taught me more than they know." (E. Bach [1974], p. vi)

(b) Tom and Mary are friends with one another, and they are visiting some people; (c) Tom and Mary are visiting some people, and these people are friends with one another.]

5) Receipts from this source are not liable to income tax under section iv, paragraph 19. [(a) Section iv, paragraph 19, exempts receipts from this source from liability to income tax; (b) section iv, paragraph 19, does not impose a liability to income tax on receipts from this source.]

6) I thought you were someone else. [(a) I thought you were someone other than the person you in fact are; (b) I thought you were someone who is not identical to himself.]

7) First speaker. "I ought to send flowers."

Second speaker. "No you ought not."

[(a) You are not under an obligation to send flowers; (b) you are under an obligation not to send flowers.]

8) Nicholas has written a book about everything. [(a) Nicholas has written a book, and it treats every subject; (b) for every subject, Nicholas has devoted at least one whole book exclusively to it.]

In none of these cases can the alleged ambiguity be attributed to any word. One way to test for this is to verify that each of the words can occur in a variety of sentences lacking the corresponding ambiguities, and this is not to be expected if the words are ambiguous.

Ex.1.28 Consider the following objection to the test mentioned in the text:

Despite the fact that "cut" is ambiguous, "I cut the string with my pocket knife" is not. Hence the fact that a word can occur in unambiguous sentences does not show that is unambiguous.

The existence of structural ambiguity shows that the elimination of lexical ambiguity is not enough. Some more radical approach is required.

Structural ambiguity seems to affect even logical constants, for example "not" in (7) and "a" and "everything" in (8). On one reading of (7) we think of "not" as dominating the sentence, to form its negation, a reading which we might write as "Not: you ought to send flowers". On the other reading, we think of "not" as governing just the description of the action, a reading which we might "You ought to do this: not send flowers". On one reading of think of "a" as dominating the sentence, a reading which we write as: "A book by Nicholas is like this: it is about everything the other reading, we think of "everything" as dominating the sentence, a reading which we might write as: "Everything has this property: Nicholas has written a book about it". The logical constants determine formal validity (see §10 and §11). If structural ambiguity can affect the logical constants, then the hope of giving a general characterization of formal validity for English as it stands is undermined. Consider:


9) Logic, epistemology and metaphysics are all the philosophical subjects there are. Nicholas has written a book about logic. Nicholas has written a book about epistemology. Nicholas has written a book about metaphysics. Therefore, Nicholas has written a book about every philosophical subject.

If (9) is valid, the standard view is that it is formally valid. But there is no straightforward answer to the question whether it is valid. It all depends on how we understand the conclusion, which is structurally ambiguous in the same fashion as *`(8)`*.

The problem for the account of formal validity is as follows. We said that a formally valid argument is valid in virtue of its form, and that this in turn is a matter of it being an instance of a form all of whose instances are valid. However, (9), read as invalid, is an instance of every argument-form of which (9), read as valid, is an instance. Hence (9) is not an instance of a valid argument-form. The problem of structural ambiguity threatens to deprive even the apparently formally valid reading of (9) of its formal validity.

Ex.1.29 If any of the following is ambiguous, give unambiguous paraphrases of the alternative interpretations:

(i) I am going to buy a book.

(ii) Everyone has a problem.

(iii) "In the whole wide beautiful world, Aldo Cassidy was the only person who knew where he was." (Le Carré [1971], p. 8)

(iv) "Most of all I would like to thank my students, who have taught me more than they know." (E. Bach [1974], p. vi)

It is theoretically possible that structural ambiguity could be filtered out of natural languages. In (3)-(8) unambiguous paraphrases in English were given; perhaps structurally unambiguous paraphrases are always available. But it is unclear whether precise rules can be given which would effect this filtering. One can see why logicians might prefer artificial languages: they are constructed from the ground up in such a way that structural ambiguity is impossible.

### (3) Syntactic irregularity

The *syntax* or *grammar* of a language is a set of rules which determine how sentences are constructed from the language’s vocabulary. A syntactic distinction is one which we have to make in order to devise such rules.

As we have seen, there are two possible answers to the question: what ought to be picked out as sentences? One answer is: just the series of words which constitute *grammatical* sentences, where it is supposed that we have some antecedent grasp on what it is for a series of words to be a grammatical sentence. The other answer is: just the series of words which constitute *meaningful* sentences. (Cf. (8.2) and related discussion.) Without prejudice to this debate, I shall in this section mean by syntactic rules ones which determine the class of meaningful sentences.

We have already been obliged to make various syntactic distinctions in English, for example, between sentences, predicates and names. We used $A_{1}, \ldots, A_{n}, B, C$, as letters marking the sort of position that can be occupied by a sentence; $F, G, H$ as letters marking the sort of position that can be occupied by a predicate; and $\alpha$ as a letter marking the sort of position that can be occupied by a name. We have attempted no definition of these categories. Rather, we have simply picked out examples, and gestured towards the category as a whole.

The gesture is supposed to determine the category from the example in the following way. Anything belongs to the category if it can replace the example (at least in the context under consideration) without turning sense into nonsense. Given that “Tom” belongs to the category of names, we can infer that “Harry” does too, since it can replace “Tom” without turning sense into nonsense. But neither “herbivores” nor “2 + 2 = 4” are names, by this test, since replacing “Tom” in “Tom is a bachelor” yields the nonsensical “Herbivores is a bachelor” and “2 + 2 = 4 is a bachelor”. I call this way of determining syntactic cate- gories the naive syntactic test. The taxonomy the test produces is inadequate for the study of validity. It places expressions with similar logical powers in different categories; and it places expressions with dissimilar logical powers in the same categories.


The expressions "Mount Everest" and "Ronald Reagan" have logically similar powers. Each serves to pick out an object. Yet it is at least arguable that replacing the latter by the former in "Ronald Reagan is thinking of Vienna" turns sense into nonsense. If so, these names fall into different categories, according to the naive syntactic test. The uncertainty reveals the vagueness of the distinction between sense and nonsense.

Here are some examples which suggest that the taxonomy produced by the naive syntactic test places expressions with dissimilar logical powers in the same categories. By the naive syntactic test, it would seem that the category of names would contain not only expressions like "Clinton" and "Harry" but also what logicians call quantifier phrases, like "everyone", "no one", "someone". For example, the results of replacing "Clinton" in "Clinton is a bachelor" by any of "everyone", "no one" or "someone" make perfectly good sense. But the logical powers of "Clinton" and "no one" are very different, as is brought out by the fact that *`(10)`* is valid but (11) is not:

10) Clinton is a bachelor. So someone is a bachelor.

11) No one is a bachelor. So someone is a bachelor.

Ex.1.30 Although as they occur in sentences like (10) and (11), "Clinton" and "no one" can be interchanged without turning sense into nonsense, it does not follow that they belong to the same syntactic category by the naive syntactic test: this requires that they be everywhere substitutable. Doubts are raised by examples like "No one ever complains" (since "Clinton ever complains" isn't acceptable in contemporary English). Can you think of other, perhaps more decisive, cases? (Cf. Oliver [1999], pp. 253-4.)

The contrast is exploited by Lewis Carroll [1872]:

12) "Who did you pass on the road?" the King went on, holding out his hand to the Messenger for some more hay.

It is theoretically possible that structural ambiguity could be filtered out of natural languages. In (3)-(8) unambiguous paraphrases in English were given; perhaps structurally unambiguous paraphrases are always available. But it is unclear whether precise rules can be given which would effect this filtering. One can see why logicians might prefer artificial languages: they are constructed from the ground up in such a way that structural ambiguity is impossible.

### (3) Syntactic irregularity

The *syntax* or *grammar* of a language is a set of rules which determine how sentences are constructed from the language’s vocabulary. A syntactic distinction is one which we have to make in order to devise such rules.

As we have seen, there are two possible answers to the question: what ought to be picked out as sentences? One answer is: just the series of words which constitute *grammatical* sentences, where it is supposed that we have some antecedent grasp on what it is for a series of words to be a grammatical sentence. The other answer is: just the series of words which constitute *meaningful* sentences. (Cf. (8.2) and related discussion.) Without prejudice to this debate, I shall in this section mean by syntactic rules ones which determine the class of meaningful sentences.

We have already been obliged to make various syntactic distinctions in English, for example, between sentences, predicates and names. We used $A_1, \ldots, A_n, B, C$, as letters marking the sort of position that can be occupied by a sentence; $F, G, H$ as letters marking the sort of position that can be occupied by a predicate; and $\alpha$ as a letter marking the sort of position that can be occupied by a name. We have attempted no definition of these categories. Rather, we have simply picked out examples, and gestured towards the category as a whole.

The gesture is supposed to determine the category from the example in the following way. Anything belongs to the category if it can replace the example (at least in the context under consideration) without turning sense into nonsense. Given that “Tom” belongs to the category of names, we can infer that “Harry” does too, since it can replace “Tom” without turning sense into nonsense. But neither “herbivores” nor “2 + 2 = 4” are names, by this test, since replacing “Tom” in “Tom is a bachelor” yields the nonsensical “Herbivores is a bachelor” and “2 + 2 = 4 is a bachelor”. I call this way of determining syntactic cate- gories the naive syntactic test. The taxonomy the inadequate for the study of validity. It places expressions logical powers in different categories; and it places expression similar logical powers in the same categories.


The expressions "Mount Everest" and "Ronald Reagan" have the same categories as the other categories. Each serves to pick out an object. Yet it is not possible that replacing the latter by the former in "Ronald Reagan" with "Hurry" turns sense into nonsense. If so, these names are not in the same category as the other categories, according to the naive syntactic test. The uncertainty reveals the vagueness of the distinction between sense and nonsense.

Here are some examples which suggest that the taxonomy produced by the naive syntactic test places expressions with dissimilar logical powers in the same categories. By the naive syntactic test, it would seem that the category of names would contain not only expressions like "Clinton" and "Harry" but also what logicians call quantifier phrases, like "everyone", "no one", "someone". For example, the results of replacing "Clinton" in "Clinton is a bachelor" by any of "everyone", "no one" or "someone" make perfectly good sense. But the logical powers of "Clinton" and "no one" are very different, as is brought out by the fact that (10) is valid but (11) is not:

10) Clinton is a bachelor. So someone is a bachelor.

11) No one is a bachelor. So someone is a bachelor.

Ex.1.30 Although as they occur in sentences like (10) and (11), "Clinton" and "no one" can be interchanged without turning sense into nonsense, it does not follow that they belong to the same syntactic category by the naive syntactic test: this requires that they be everywhere substitutable. Doubts are raised by examples like "No one ever complains" (since "Clinton ever complains" isn't acceptable in contemporary English). Can you think of other, perhaps more decisive, cases? (Cf. Oliver [1999], pp. 253-4.)

The contrast is exploited by Lewis Carroll [1872]:

> 12) "Who did you pass on the road?" the King went on, holding out his hand to the Messenger for some more hay.
>
> "Nobody", said the Messenger.
>
> "Quite right", said the King: "this young lady saw him too. So of course Nobody walks slower than you."
>
> "I do my best", the Messenger said in a sullen tone. "I'm sure nobody walks much faster than I do!"
>
> *"He can't do that", said the King, "or else he'd have been here first." (pp. 143-4)*

The King pretends to treat "Nobody" as a name rather than as a quantifier phrase.

Despite its vagueness, the naive syntactic test at least doesn't definitely rule out counting both the expressions "is sensitive to pain" and "is evenly distributed over the earth's surface" as predicates. Since "Harry is sensitive to pain" is clearly sense, this means allowing that "Harry is evenly distributed over the earth's surface" is sense too. (Presumably the sentence is false, and so meaningful. Perhaps we could imagine it also being true, if Harry were chopped into small pieces, which were then dropped at regular intervals from an aeroplane.) If both expressions belong to the same category, however, we run into a problem.

13) Human beings are sensitive to pain. Harry is a human being. So Harry is sensitive to pain

would standardly be said to be formally valid. Does not its validity turn only on the logical constants it contains? It is an instance of the argument-form

14) $F$ are $G$. $\alpha$ is an $F$. So $\alpha$ is $G$.

It is tempting to believe that *`(14)`* is valid, and explains the formal validity of (13). But the temptation must be resisted, as the invalidity of (at least one reading of) the following shows:

15) Human beings are evenly distributed over the earth's surface. Harry is a human being. So Harry is evenly distributed over the earth's surface.

Ex. 1.31 What, if anything, is the reading of (12.15) upon which it is valid?

The invalidity of *`(15)`* establishes the invalidity of *`(14)`*. We need a more refined notion of a predicate, if we are to attain interesting generalizations about valid forms of argument.

#### Ex. 1.32 Give two further invalid instances of (12.14)

The following argument would generally be considered formally valid:

16) Every candidate is a clever or industrious person. Every clever or industrious person is worthy of praise. So every candidate is worthy of praise.

But the argument-form we would reach for to sustain this judgement is invalid:

17) Every $F$ is a $G$. Every $G$ is $H$. So every $F$ is $H$.

For the following instance of *`(17)`* is invalid:

18) Every number is a number or its successor. Every number or its successor is even. So every number is even.⁸

Expressions which look similar, at least to the naive eye, can contribute in very different ways to the meanings of sentences in which they occur. This is the phenomenon I refer to by the phrase *syntactic irregularity*. A closely allied phenomenon is that in natural languages it seems to be impossible, or at least difficult, to characterize properties which are of logical importance in the way which would make mechanical testing possible: that is, on the basis of the physical makeup of sentences.

This can be illustrated by the relation of *negation*, which is clearly important to logic, as its connection with inconsistency and validity has already made plain. We saw in (4.6) and (4.8) that there are many sentences in which one can insert a negative particle, for example “not”, without forming the negation of the sentence. This means that This can be illustrated by the relation of *negation*, which is clearly important to logic, as its connection with inconsistency and validity has already made plain. We saw in (4.6) and (4.8) that there are many sentences in which one can insert a negative particle, for example “not”, without forming the negation of the sentence. This means that


"Nobody", said the Messenger.

"Quite right", said the King: "this young lady saw him too. So of course Nobody walks slower than you."

"I do my best", the Messenger said in a sullen tone. "I'm sure nobody walks much faster than I do!"

"He can't do that", said the King, "or else he'd have been here first." (pp. 143-4)

The King pretends to treat "Nobody" as a name rather than as a quantifier phrase.

Despite its vagueness, the naive syntactic test at least doesn't definitely rule out counting both the expressions "is sensitive to pain" and "is evenly distributed over the earth's surface" as predicates. Since "Harry is sensitive to pain" is clearly sense, this means allowing that "Harry is evenly distributed over the earth's surface" is sense too. (Presumably the sentence is false, and so meaningful. Perhaps we could imagine it also being true, if Harry were chopped into small pieces, which were then dropped at regular intervals from an aeroplane.) If both expressions belong to the same category, however, we run into a problem.

13) Human beings are sensitive to pain. Harry is a human being. So Harry is sensitive to pain

would standardly be said to be formally valid. Does not its validity turn only on the logical constants it contains? It is an instance of the argument-form

14) $F$ are $G$. $\alpha$ is an $F$. So $\alpha$ is $G$.

It is tempting to believe that (14) is valid, and explains the formal validity of (13). But the temptation must be resisted, as the invalidity of (at least one reading of) the following shows:

15) Human beings are evenly distributed over the earth's surface. Harry is a human being. So Harry is evenly distributed over the earth's surface.

Ex. 1.31 What, if anything, is the reading of (12.15) upon which it is valid?

The invalidity of (15) establishes the invalidity of (14). We need a more refined notion of a predicate, if we are to attain interesting generalizations about valid forms of argument.

#### Ex. 1.32 Give two further invalid instances of (12.14).

The following argument would generally be considered formally valid:

16) Every candidate is a clever or industrious person. Every clever or industrious person is worthy of praise. So every candidate is worthy of praise.

But the argument-form we would reach for to sustain this judgement is invalid:

17) Every $F$ is a $G$. Every $G$ is $H$. So every $F$ is $H$.

For the following instance of *`(17)`* is invalid:

18) Every number is a number or its successor. Every number or its successor is even. So every number is even.⁸

Expressions which look similar, at least to the naive eye, can contribute in very different ways to the meanings of sentences in which they occur. This is the phenomenon I refer to by the phrase *syntactic irregularity*. A closely allied phenomenon is that in natural languages it seems to be impossible, or at least difficult, to characterize properties which are of logical importance in the way which would make mechanical testing possible: that is, on the basis of the physical make-up of sentences.


it will be hard to formulate a general rule picking out just those pairs of sentences one of which is the negation of the other. Might one at least give an infallible rule for one way of forming the negation, for example the rule that, for any sentence, S, “it is not the case that S” is its negation? The rule works well in many cases. For example, it says, correctly, that “It is not the case that the earth is flat” is the negation of “The earth is flat”. But it does not work for all. For example, prefixing:

19) I will marry you, if you change your religion

with “It is not the case that” yields

20) It is not the case that I will marry you, if you change your religion.

This is at best ambiguous between the negation of (19) and something equivalent to “If you change your religion, I will not marry you”.

We need some kind of bracketing device. We might write: “It is not the case that (I will marry you, if you change your religion)”. In spoken English, a similar effect can be achieved by inflection, for example one which includes a small pause after “that”.

The introduction of such special devices is typical of the formal logician’s approach. One point of the devices is that they facilitate the characterization of relations which are of logical importance (like negation) purely in terms of the physical make-up of sentences.

The question remains open whether such a result could be achieved merely by tinkering with a natural language, or whether it requires starting from scratch. The idea of starting from scratch, constructing an artificial language constrained only by the demands of logic, has inspired a philosophical tradition (though one whose merits are nowadays being questioned). Russell, for example, coined the expression “philosophical logic” to represent his view that the workings of natural language, and of our thought, could be adequately represented only by an artificial language, the language of his *Principia Mathematica*.

With this approach comes a problem. How are whatever results are obtained for the artificial language to be applied to natural language and to our everyday thoughts? A project opens up, which I call the project of formalization. The idea is to pair each natural sentence with an artificial one. The latter is, or reveals, the logical form of the former. Thanks to the pairing, the results about validity which we have been able to obtain, with relative ease, for the artificial language can be transferred to the natural one. To put it in another idiom: the results about validity which we have obtained by expressing arguments in an artificial language become relevant only if these arguments are, or are specially related to, those we use in our everyday thought and talk. One demonstrates the relevance by showing how to pair natural language sentences with artificial language sentences in such a way that the propositions expressed by the former are the very same as, or specially related to, the arguments expressed by the letter.


Within this tradition, the first question to ask about an argument expressed in a natural language is: what is its logical form? The answer is to be given by translating the argument into some artificial language: by, as it is called, formalizing the argument. In the next four chapters, we examine in detail how the project of formalization proceeds.


#### Notes


¹ A slightly fuller account of “apriori” is given in the glossary, which also glosses some terms which are not explained in the text.

² The view that inductive “logic” is not a formal discipline has been given impetus by a famous discussion by Goodman [1955], Part II. For a general introduction to problems of induction, see Skyrms [1966], esp. chs 1–3.

³ For a good discussion, see Plantinga [1974]. By logical possibility I mean approximately what he calls “broadly logical possibility” (p. 3). (For a qualification, see chapter 6.5 below.)

⁴ The contrast between whether a speaker is propounding an argument or not, and thus the contrast between whether he has said something appropriately assessed for validity or not, is not as clear as the text would suggest. This should be apparent from reflection on Ex. 1.13. Cf. also van Dijk [1977].

⁵ Square brackets [,], are used for greater legibility.

⁶ One could show this by applying the propositional calculus, if one were willing to make a certain assumption about the relationship between that language and English. See chapter 2.10.

⁷ The hope has a long history, going back at least to Leibniz. If it were made precise in terms of the technical notion of decidability, it is a hope which will be disappointed for any interesting logic: see e.g. Delong [1970], pp. 132ff., or Kirwan [1978], pp. 169ff.

⁸ The example is from Geach [1972], pp. 492–3.

⁸ The example is from Geach [1972], pp. 492–3.