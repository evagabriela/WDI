---
title: Title of the Lesson
duration: "1:25"
creator:
    name: John Doe
    city: NYC

---

# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Intro to Pseudocode (60 mins)

| Timing | Type | Topic |
| --- | --- | --- |
| 5 min | [Opening](#opening) | What is pseudocode? |
| 15 min | [Guided Practice](#guided-practice) | Reading Pseudocode |
| 10 min | [Independent Practice](#ind-practice) | Solve the Waiter Problem |
| 10 min | [Intro to New Material](#approaching-problem) | Approaching a Problem |
| 15 min | [Independent Practice](#real-world-practice) | Pseudocode |
| 5 min | [Conclusion](#conclusion) |Recap/ Q&A |

### LEARNING OBJECTIVES
*After this lesson, you will be able to:*
- Describe the role of pseudocode in development
- List steps for problem solving
- Create pseudocode to describe a basic problem

---
<a name="opening"></a>
## Opening (5 mins)

According to wikipedia, [pseudocode is](https://en.wikipedia.org/wiki/Pseudocode):
> Pseudocode is an informal high-level description of the operating principle of a computer program or other algorithm.

> It uses the structural conventions of a programming language, but is intended for human reading rather than machine reading.

This is a great opportunity to turn tech speak into, well, human speak.

Let's break that down and translate it.

#### What does that mean?

> A. Pseudocode attempts to be a way to describe the solution to a problem, that is easier and more concise than code.  It is a stepping stone toward writing the code.  It forces you to think critically about the problem and allows us to attempt multiple solutions.

I've heard Washington D.C. described as where Northern hospitality meets Southern efficiency.

<!--I feel like the quote above is backwards.  Shouldn't it be Northern efficiency and Southern hospitality? :)  We can also make this an example that is more applicable to all markets globally.  -->

Pseudocode lives in that "in between" place too.  It has more logic than English, without all the structure of code.

#### What Role Does it Play in Development?

Is writing out pseudocode a step that real-world developers take? Watch this video to hear developers talk about the importance pseudocode plays in their workflow:

-  [Pseudocode - Interviews with Developers](https://generalassembly.wistia.com/medias/8axbgun2i4)


***
<a name="guided-practice"></a>
## Guided Practice: What does that look like? (15 min)

Pseudocode should describe the entire logic of the algorithm so that programming becomes a task of translating line by line of pseudocode into real code.

For each of following, let's discuss why each one could be considered "Good" or "Poor" examples of pseudocode:

#### Problem 1 - Determining If a Number is Even or Odd

***Example 1.1:***
```
PROGRAM IsEvenOrOdd:
  var num = number;
  IF (num % 2 === 0)
    THEN Print "even";
    ELSE Print "odd";
  ENDIF;
END.
```

***Q. What do we think?***

> A. This is not a great example. Here we are using "var" in our pseudocode when it should read plain english! Also, we should not be using the javascript syntax "===" in our conditional.  Would a non-programmer know that `num % 2 === 0` indicates an even number?

***Example 1.2:***
```
PROGRAM IsEvenOrOdd:
  Read number;
  IF (number divided by two has no remainder)
      THEN Print the number is even;
      ELSE Print the number is odd;
  ENDIF;
END.
```

***Q. What do we think?***

> A. This is better.  It's closer to english.  It clearly states what we are trying to achieve and how, without getting bogged down in the minutia of code.  Even someone that doesn't code can help us check our logic.  Is any number that can be divided by two, cleanly -- without leaving a remainder -- even? Is anything else odd?

#### Problem 2 - How to Make a PB&J Sandwich

*From [Get Creative Today](http://getcreativetoday.com/lessons/pseudo-code-flowcharts/)*

> Instructor Note: Optional - Make this activity interactive by bringing in bread, peanut butter, and jelly. Have one volunteer sit in front of the class, telling this student that they are to take instructions from the class very literally. Then go around the room and have each student provide one line of instruction for the volunteer until the sandwich is complete. Write down each line of instruction the students provide, the pseudocode.

***Example 2.1:***
```
Make PB&J Sandwich:
  Gather bread, peanut butter and jelly.
  Apply peanut butter to slice of bread.
  Apply jelly to another slice of bread.
  Bring to two slices of bread together.
  Eat and enjoy.

```

***Q. What do we think?***

> A. This is a good place to start.  It is a good set of instructions and intuitive for us to follow.  However, we still don't know what physical steps are required.

Take a second to imagine.  Imagine if you had never made a sandwich before.  Ever.  Think about the instructions you would need for that for that first sandwich.  A computer has no real memory.  Every time it starts a task, it has no recollection of performing it before.  We must tell it every single step, every single time.  We need to break these down into smaller steps for the computer to understand.

***Example 2.2:***
```
PROGRAM MakePB&JSandwich:
  Grab a paper plate;
  Open bread container;
  Grab bread package;
  Untwist bread package;
  Open bread bag and remove two slices;
  Place slices on paper plate;
  Grab a plastic knife;
  Open peanut butter jar;
  Use knife to scoop out peanut butter;
  Apply peanut butter to one slice of bread;
  Spread peanut butter on slice;
  Place knife on plate;
  Close peanut butter jar;
  Open jelly bottle;
  Squeeze jelly onto second bread slice;
  Close jelly bottle;
  Place down jelly;
  Pick up knife;
  Spread jelly on slice;
  Bring two slices of bread together;
  Cut slices in half down the middle;
  Throw knife in the trash;
  Pick up one half of sandwich;
  Enjoy;
END.  
```

****Q. What do we think?****

> A. This example's sequence is very thorough! However, we are still assuming certain conditions that our utensils or ingredients already exist. What if we are out of plates? Will we grab a napkin instead to place our sandwich on? What if we are out of jelly? Will you throw the sandwich away or eat it with just peanut butter?

Computers are not smart. We need to give them step by step instructions to account for conditions. They can not adapt to make changes without being explicitly told. Programming is a series of tasks, which can be completed only if a certain number of conditions are met.

Computers can not adapt, but we can.  Your first pass at pseudocode will probably not cover everything.  Once you know more, you may come back to update and refactor your pseudocode.

***
<a name="ind-practice"></a>
## Independent Practice: Solve the Waiter Problem (10 min)
<!--I think between giving students time to solve this, and then discuss the answer, it will take closer to 10-15 minutes. What do you think?-->

Using your new found skills, you have 5 minutes to solve this:

- A waiter has N tables, each with 2-4 guests.
- The waiter makes rounds between each of their tables, the bar, and the kitchen.
- The waiter takes drink orders for a new table, then submits them to the bar.
- Drinks are delivered when all table orders are ready.
<!--Does this mean when the orders for all N tables, or all the orders for guests at one table?  -->
- The waiter takes food orders for a new table, then submits them to the kitchen.
- Food is delivered when all table orders are ready.
<!--Does this mean when the orders for all N tables, or all the orders for guests at one table?  -->
- The waiter checks idle tables for additional requests, then submits them appropriately.
- Additional requested items are delivered when all table orders are ready.


***Q. In one sentence, what problem were you solving?***

> A. Discuss the answers and the importance of identifying the problem.

We realize you didn't have enough time to solve it.  We hope that, through this exercise, you learned the importance of clearly identifying the problem.

***
<a name="approaching-problem"></a>
## Approaching a coding problem (10 min)
<!--Consider making this a guided practice and walking through a real example for each step.  It might help students understand how to apply these questions to a pseudocode exercise.  -->

Pseudocode isn't just about writing down the steps that you already know.  It's a tool to help you work through the problem.  Before we can write pseudocode to solve the problem, we need to know the problem.  

Here are some steps that can help with problem solving:

- Identify the Problem
- Conceptualize
- Break it down
- Start small

#### Identify the Problem

- What exactly are we trying to solve?  - From who's viewpoint?  
- Who will benefit?  
- What are we delivering?

#### Conceptualize

- Look at the big picture, the major steps
- Avoid details
- At this stage we recommend drawing on whiteboards or with crayon, anything that screams "temporary", "play", or "brainstorm".

#### Break it down

- We break the conceptual models down into concrete steps, actionable items.
- We identify risks (gaps in knowledge, technology, and infrastructure).

#### Start small, stay small

Finally, we take some action.  This is when we finally start writing code.  We fight hard to take small steps, verify that each step achieves what we want, what we expect, before continuing on.  If we do too much at once and things break, which they always do, we won't know what is causing the problem.  We won't know which part to trust.  Humans thrive on easy wins. We need to see forward progress.  Remember that.  Use that.  Celebrate your wins.


#### Review: the Steps

- Identify the Problem
- Conceptualize
- Break it down
- Start small


****Q. Where does pseudocode fit in these steps?****

> A. Break it down OR Start small

This process is iterative.  We keep circling around and repeating the earlier steps, just at a different level.

When we first approach a problem, we see the big picture.  "Break it down" gives us big steps.  Then, we take one of those steps and "Break it down".  Now, starting small, we write pseudocode to help illustrate the problem.  

Pseudocoding proves that we have *identified* the problem, understand it *conceptually*, and have *broken it down* into *small steps* that we can follow.


#### Syntax for Pseudocode:

There is no one, fixed syntax for pseudocode.  It just needs to be clear, simple, and concise.  

If you feel stuck, feel free to use this syntax:

***Referencing: [Introduction to Pseudocode](http://www.slideshare.net/DamianGordon1/pseudocode-10373156)***

* General Structure of Pseudocode
  ```text
  PROGRAM <ProgramName>:

  <Do Stuff>

  END.
  ```

* Selection: IF/ELSE Statements
  ```
  IF (<Condition>)
    THEN <Statements>;
    ELSE <Statements>;
  ENDIF;

  ```
* Iteration: LOOP
  ```
  WHILE (<Condition>)

  ENDWHILE;
  ```
***
<a name="real-world-practice"></a>
## Independent Practice: Pseudocode a real-world problem (15 min)

Break into small groups and pick one of the following programs to pseudocode:

#### Option 1: A Trivia Game

The game should have a preset list of questions, which are shown one at a time
to the user. The user submits their answer and goes the the next question. After
each question they can see whether they were correct or incorrect. They can also
see their total score.

#### Option 2: Concentration

The user should see a grid of cards. Clicking a card reveals it and allows them
to click another card. If they match, the cards stay up and if not they flip
back over. Users get a point for every pair they flip. The game ends after 1
minute or all cards have been matched.

#### Option 3: Flash Cards

The user should start with a shuffled list of pre-existing cards. They can go
back and forth between cards and 'flip' the flash card to go from back-to-front
or front-to-back.

Optionally, users may mark a card 'correct' if they knew the answer on the back
of the flash card, in which case it's temporarily removed from the deck.

#### Option 4: War (Card Game)

Users can play the [game of 'war'](https://en.wikipedia.org/wiki/War_(card_game)
against a computer. The game continues until one player runs out of cards.

#### Timing & Review

- Students should work in pairs to pseudo-code the first problem of their choosing (15 minutes).
- After
time is up, they should 'swap' code with another team and review each other's code, leaving feedback (5 minutes).
- If time permits, switch teams and tackle an option that neither partner has yet attempted (10 minutes).
- Repeat the the review process (5 minutes).

<!-- ID NEEDED -  Should these bonus exercises be split out into a separate file? -->
<!--Sarah, yes I would split them in to separate files in the attempt to make things as modular as possible.  That way, they can more easily be linked to in different ways depending on how an instructor chooses to use them.  -->


## Bonus Exercise: Pseudocode FizzBuzz (15 min - If time permits)

Break into small groups and solve this puzzle:

You're given a robot. The robot has no imagination or creativity whatsoever, but it's good at following rules.

The robot can only obey 9 commands:

- Add two numbers together
- Subtract two numbers
- Multiply two numbers
- Divide two numbers
- Find the remainder of one number divided by another
- Remember a number
  - For example, "Number A is 42"
- Say something
- Go back to an earlier step in the instructions
- Tell if two numbers are equal, and if they are do one thing, and otherwise do another thing
  - For example, "If Number A equals 42, say 'Hello'. Otherwise, go back to step 3."

#### Our task

We need to instruct the robot, using only these commands, to perform the following actions.

When the robot is given a number &mdash; say, 10 &mdash; for each number between 1 and 10:

- If the number is divisible by 3 it says "Fizz"
- If the number is divisible by 5 it says "Buzz"
- If the number is divisible by 3 and 5 it says "FizzBuzz"
- If the number isn't divisible by 3 or 5 is says the number

So if the provided number was 10, the robot would say:

```
"One"
"Two"
"Fizz"
"Four"
"Buzz"
"Six"
"Seven"
"Eight"
"Nine"
"Buzz"
```

To start, consider:

- How would you get the robot to count to 10? You can't just say, "Count to 10." That's not one of the commands the robot knows. Of the 9 commands you've been given, which might be helpful?

- How can you tell if one number is divisible by another? (For example, 8 is divisible by 2, but not by 3.)

## Bonus Exercise: If there are eggs (25 min - If time permits)

A programmer is going to the grocery store and his wife tells him, "Buy a gallon of milk, and if there are eggs, buy a dozen."

So the programmer goes, buys everything, and drives back to his house.

Upon arrival, his wife angrily asks him, "Why did you get 13 gallons of milk?"

The programmer says, "There were eggs!"

#### We Do: Only milk (10 min)

1. Write the pseudocode that shows why he only bought milk.

#### You Do: Milk and eggs (15 min)

1. Write pseudocode that gets the programmer to buy milk and eggs.

> Instructor Note: See possible solution in the solutions folder [here](solutions/eggs.MD)

<a name="conclusion"></a>
## Conclusion (5 mins)
- Review independent practice deliverable(s)
- Recap topic(s) covered in today's lesson
- Preview topics that will be covered in today's lessons.

- Check for understanding by asking the following questions:
  1. What are some helpful steps for solving problems?
  2. What does pseudocode help us do?
  3. Do we only pseudocode at the start of a project?


  ### ADDITIONAL RESOURCES
  - Exercises
    - [Additional Examples/Exercises from GA JS Circuit](labs/circuit.MD) (Easy)
    - [Pseudocode Exercises by Thom Page](labs/pseudo-code.MD) (Medium/Advanced)
  - Readings

    - [Pseudocode is](https://en.wikipedia.org/wiki/Pseudocode) (Wikipedia)
    - [Introduction to Pseudocode](http://www.slideshare.net/DamianGordon1/pseudocode-10373156)
    - [Get Creative Today](http://getcreativetoday.com/lessons/pseudo-code-flowcharts/)
  - Videos
    - [Matt, WDI-DC-8 Screencast](https://www.youtube.com/playlist?list=PL-6bwUTtCRVTMUUSjqIYVXYyfZBzs8saD)
    - [GA JS Circuit - Pseudocode](https://generalassembly.wistia.com/medias/ym3vdun7n3)
