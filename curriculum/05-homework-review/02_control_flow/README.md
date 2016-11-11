---
title: Title of the Lesson
duration: "1:25"
creator:
    name: John Doe
    city: NYC
---

> #### *Guiding Questions When Using This Template*
>
> - [ ] Are the learning objectives measurable?
>   - [ ] Are there at least two objectives? ( All learning objectives should be pulled from the [Front End Standards](https://docs.google.com/spreadsheets/d/11SzdbIIa9PLJ6kknGXXoBYOtL5ycwMK2N8lkI5THFak/edit#gid=1968474545) doc.  If you would like to add or remove any Learning Objectives, please contact amy.almeida@ga.co)
>   - [ ] Does the lesson address all the learning objectives?
>
> - [ ] Are activities spaced out with enough time for each?
>   - [ ] Did you include knowledge "Checks" or activities at the end of every component to test comprehension?
>   - [ ] Is there an even distribution of intructor-led and active learning portions?
>
>
> - [ ] Did you provide guidance for both students & instructors?
>   - [ ] What will instructors have to do to prepare for this lesson?
>   - [ ] What will students have to do to prepare for this lesson?
>   - [ ] What additional resources do you provide for students who are "hungry for more," or need additional practice?
>
> #### *How to Use This Template*
> * Static Components: Reserve roughly 5 min for Opening, 5 unscheduled "buffer" mins for overrun, & at least 5 min for Conclusion (end of lesson review).
>
>
> * Modular Components: The units of instruction are: Intro, Demo, Guided-Practice, & Independent-Practice. These can be cycled or intermixed in various orders, depending on the topic / content.

> #### *Components of the lesson plan*

> - Opening: this only happens once; used to introduce the agenda, review material, and provide a motivating example / the problem we're trying to solve with this skill/content
> - Introduction: this is a section dedicated to introducing and contextualizing new vocabulary, ideas, and code syntax that will be practiced in later sections
> - Demo: an instructor-led session demonstrating proper techniques or syntax examples
> - Guided Practice: interactive instructor by which the instructor engages with and probes students for answers to guide the discussion or activity
> - Independent Practice: a block of time where students are able to practice what they've learned; the instructor provides directions and the students use the directions to complete an exercise
> - Conclusion: a time to sum up the lesson, review the answers to a final independent practice, and/or pose discussion questions
> - Check: a moment to check to understand students are following; it can be done with a question about content, a general "How comfortable are you with this?", or the instructor can check the output of students code to ensure they've completed the assignment properly.

> NOTE: the lesson you create does not have to follow a progression of Introduction > Demo > Guided Practice > Independent Practice - a combination of these is often ideal - but a lesson must always begin with an Opening and end wth a Conclusion.



---
# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Lesson Title (# mins)

| Timing | Type | Topic |
| --- | --- | --- |
| x min | [Introduction](#introduction) | Topic |
| x min | [Demo/Codealong](#demo) | Topic |
| x min | [Guided Practice](#guided-practice) | Topic |
| x min | [Independent Practice](#ind-practice) | Topic |
| x min | [Conclusion](#conclusion) |Topic |

### LEARNING OBJECTIVES
*After this lesson, you will be able to:*
- Describe some concept
- Explain how to do something
- Do or build something

### STUDENT PRE-WORK
*Before this lesson, you should already be able to:*
- Describe some concept
- Explain how to do something
- Do or build something

### INSTRUCTOR PREP
*Before this lesson, instructors will need to:*
- Gather materials needed for class
- Complete Prep work required
- Prepare any specific instructions

---
<a name="opening"></a>
## Opening (# mins)
- Review pre-work, projects, or exit ticket, if applicable
- Review current lesson objectives
- Reference general course content or topics (e.g. code or concepts that have been used across multiple lessons)
- Include Hook / Real-world Relevance (why the content from this lesson is useful or important)

What is control flow? Watch this [video](https://generalassembly.wistia.com/medias/zhahjd0c7t) where developers talk about the role control flow plays in development.

In the last lesson, we briefly learned about true or false statements, which are also known as booleans.

Comparison and logical operators, which we will learn more about in this lesson, result in Booleans.

A boolean can have one of two values — true or false.

Think of a boolean like a light switch — it can either be switched on or off, but it can't be both at the same time.

<img src="assets/lightswitch.svg)" width="150px">


***

<a name="comparison-logical"></a>
## Introduction: Comparison and Logical Operators (# mins)

Comparison and logical operators are useful in JS because they help us compare different conditions to one another.

Conditions are usually made up of a mathematical statement that uses an operator (the signs that allow us to make the comparison, such as equals, less than, or greater than).

Conditions are often found in parentheses and must evaluate to true or false.

The results of these comparisons can control the flow of the program.

For instance, when information is incorrect, JavaScript can help identify the comparison as false.

So if you're filling out a form that requires your birthday, you can't say you were born in the year 2045 because that year hasn't occurred yet.

You also can't say that you were born on December 45th, because that day doesn't exist.

When you try entering information like this, JS will identify that it is wrong by comparing the information you entered against information it knows to be accurate.

<img src="assets/Slide-5-Form-X.svg)" width="150px">

Making comparisons is almost like asking questions about the information the user has entered.

Is the year less than or equal to 2016 and more than or equal to 1900? If the answer to this question is "true," then we know the user has entered a valid year, and that he or she was born somewhere between 1900 and 2016.

<img src="assets/Slide-6-Form-Check.svg)" width="200px">

Did you notice how we used the term "less than or equal to" to check, or compare, two things? This is how our comparison operators help us make decisions.

Although this concept may seem abstract, in JavaScript we'll often have to make decisions based on Boolean values.

For example, did the user above enter a valid country of residency?

<img src="assets/mars.svg)" width="200px">

If the country chosen is valid (i.e., if that statement is true), then we will allow him or her to submit the form.

Otherwise (if that statement is false and the country chosen is invalid), we will display an error message.

Okay, so statements can either be true or false. But what exactly are statements?

Essentially, statements in JavaScript perform an action.

In the case of the country-of-residence form, the action was allowing the user to submit the form if the statement is true.



## Guided Exercise: Operators (# mins)

#### Comparison Operators
Comparison operators are binary in that they compare two values against one another and return a boolean value — either true or false.

Comparisons in JavaScript can be made using <, >, <=, and >=, and work for both strings and numbers.

<img src="comparison_operators.svg)" width="250">

<!--
ID NEEDED: Help formatting the following exercise

Type each command given in the console below. Before you press enter, take a moment to think about what value the console will return.

7 > 7
The console returns false.
7 >=7
The console returns true.
7 < 7
The console returns false.
7 < 13
The console returns true.
7 <= 13
The console returns true. -->


#### Equality Operators

Now let's take a look at equality operators (these can be a bit more complex).

Equality operators check to see whether two values are the same as, or equal to, one another.

There are two ways to verify equality in JavaScript:

The `==` operator or the `===` operator. In this course, we will always use the `===` operator, because it is more accurate.

<img src="assets/equality_operators.svg)" width="200px">

##### `==`

First let's take a look at the `==` operator.

While verifying equality using the double equal (`==`), JavaScript performs something called "type coercion".

Type coercion means that, if the values on both sides of the equality operator have a different type (e.g., the number 1 and the string "1"), JavaScript will try to change the type of both operands to check whether or not they are equal.
<!--
ID NEEDED: Help formatting the following exercise
Type each command in the console. Before you press enter, take a moment to think about what value the console will return.

7==7
The console returns true
7=="7"
The console returns true
-->


Note that the second statement evaluates to true, even though we are comparing a number and a string.

#### Type coercion

So why is that?

This is because behind the scenes, JavaScript is trying to convert the values before comparing them.

```
7 == 7    // true
7 == "7"  // true
```

Here, the interpreter (aka, the console) would first try to convert 7 to a string ("7") and then compare "7" with "7".

Because those values are equal, this would return `true`.

Remember the difference between a number and a string?

A string is used for textual information and is surrounded by quotation marks (single or double), whereas a number is used for a quantity and is not surrounded by quotation marks.

We use numbers any time we want to do a calculation.

Because JS tries to change an expression so that both types are equal, it's easier for expressions to return true. If we're not careful, this can cause some unexpected (and unwelcome) behavior. As a reminder, *expressions* are written whenever a value is expected.

#### The Strict Equals Operator `===`

To avoid type coercion and ensure stricter comparisons, use the triple equals operator, also known as the Strict Equality Operator (===).

The === operator checks to make sure the type and the value on both sides of the === are the same.

<!--
ID NEEDED: Help formatting the following exercise
Type each command in the console. Before you press enter, take a moment to think about what value the console will return.
7 === 7
The console returns true.
7 === "7"
The console returns false.
0 === false
The console returns false.
false === "false".
The console returns false. -->

Now, let's take a closer look at the answers:

<img src="assets/strict_equals.svg)" width="250px">

The double equals signs (==) can be useful when both the type and value are the same, but, because their type coercion could potentially derail your program, they're best avoided when you're just getting started out.

By sticking to the === operator, we can ensure that we are checking both the type and the value.

#### The Not Equals Operator `!==` and `!=`
Now, what do we do if we want to check and see if two values are not equal to one another?

Easy — we replace the first equals signs in the previously mentioned operators with a `!`.

These are inequality operators (`!=` and `!==`).

The `!=` operator checks to see if two values are not equal to one another. Similar to the `==` operator, it performs type coercion before checking the two values against one another.

The `!==` compares two values to one another without performing type coercion, so both the values and the types are compared.

<!--
ID NEEDED: Help formatting the following exercise
Type each command in the console. Before you press enter, take a moment to think about what value the console will return.
7 !== 7
The console returns false.
7 !== “7”
The console returns true.
0 !== false
The console returns true.
false !== “false”
The console returns true.
 -->

Inequality operators allow us to make sure that the values to the left and right of the operator are not the same.

To be on the safe side and avoid bugs and unexpected behavior, use the `!==` over the `!=` to ensure that you are comparing both the value and the type.

Let’s review the operators we have learned so far:

<img src="assets/review.svg)" width="250px">


#### Logical Operators
Finally, let’s have a look at *logical operators*. The logical operators are NOT, OR, and AND.

We can use these to combine several boolean statements into a single statement.

For instance, if it is raining AND I have an umbrella, then I will go outside with an umbrella.

BOTH conditions have to evaluate to true for the entire expression to be true.

<img src="assets/umbrella.svg)" width="250px">

Logical operators let us check to see if two conditions are both true or if _at least one_ of the conditions is true.

We can also use logical operators to reverse a value or check to see whether or not something is false.

AND is written with double ampersands (`&&`)

OR is written with double pipes (`||`)

NOT is written as the exclamation point (`!`)

<img src="assets/logical_operators.svg)" width="200px">

For example, let’s assume that A = 5, B = 10, and C = 8.

Is A less than B AND is A also less than C?

Yes. 5 is less than 10 AND 5 is less than 8.

Once we check multiple conditions to see if they’re true, we can do something with the results.

NOT (`!`) will reverse the value of any Boolean (i.e, `!true` `// false`).

OR (`||`) takes in two boolean arguments; if at least one is true, then it will evaluate to true. But, if both are false, it will evaluate as false.

AND (`&&`) also takes in two boolean arguments; however, it will only evaluate as true if both of the arguments are true. Otherwise, it will evaluate to false.

By this point, you already know the basic ins and outs of expressions.

However, there are a few things we've glossed over, especially when it comes to boolean logic.

We'll start with *undefined* and *null* values. These two values represent a lack of data.

f we want to check if our variable is in fact undefined, we can do so in the console.

Checking to see if a variable is undefined is an important step that allows you to verify that something exists before you use it (and thus prevents you from making a mistake that could potentially cause major program errors).

We can fix this by:

Making sure to give our variables a value when they are first defined.

Checking to see if a variable is undefined. If it is, we can assign it a value like so:

```
if (someData === undefined) {
  console.log('someData has not yet been defined.');
  someData = 'We are now assigning a value.';
}
```

Null values are values that you declare to have no value.

But why would you want to do this? Why not use undefined instead?

It's best practice to assign a variable to "null" only if you want the variable to represent nothing.

Variables in JavaScript are only undefined until they've been assigned a variable for the first time.

Null gives us a way to 'reset' the value of a variable to nothing.

Null values are designed to represent the lack of a value.

Whenever variables are defined without any value, they are undefined. And, because undefined is a catch all for everything without a value, relying on it can make things tricky to troubleshoot.

So, it’s best to avoid using undefined and use null instead.

To reset something back to 0, we use null. For example, let’s look at a player scoring system within a game.

We can declare our variables as null to represent that there is no data.

// we will define a variable with no value, or null
      var playerScore = null;
We can then evaluate if our value is null:

playerScore === null // 'The player has not started playing yet.'
playerScore === 0 // 'The player has started playing but has started playing but has not scored any points.'

Like most computer languages, JavaScript supports Boolean values, or True/False values.

Everything in JavaScript — from the strings we learned about in Unit 1 to the null and undefined values we just covered — has an inherent Boolean value, generally known as either _truthy_ or _falsey_.

Truthy: Something is truthy when it evaluates to True. In JavaScript, truthy values include:

- Strings
- Non-zero numbers
- True

Falsey: Something is Falsey when it evaluates to False. The "falsey" category of values includes:

- False
- 0 (zero)
- "" (empty string)
- Null
- Undefined
- NaN (a special Number value meaning Not-a-Number!)

Below are the exact rules Boolean operators follow when dealing with non-Boolean input values.

<img src="assets/falsey_truthy.svg)" width="200px">

The best way to determine if something is truthy is to determine that it’s not falsey.

As you saw in the table, there are six Falsey values in JS:

`undefined`, `null`, `NaN`, `0`, `""` (empty string), and `False`, of course.

Earlier, we looked at the logical operators NOT(`!`), OR (`||`), and AND (`&&`).

These operators accept inputs with data types such as strings and numbers.

When operators accept input values, they categorize these inputs as being either "falsey" or "truthy."

The boolean operators `!`, `||`, and `&&` follow a set of rules that determine how they behave.

NOT(`!`): If the input is truthy, return `false`; if the input is falsey, return `true`.

OR (`||`): Return the first truthy value; if both values are Falsey, return the last falsey value.

AND `(&&):` Return the first falsey value; if both values are truthy, return the last truthy value.

Let’s take a closer look:

```js
7 >= 7 && 12 < 8
```

The logical operator (in this case, `&&`) will categorize the inputs on each side as either falsey and truthy:

truthy (`7 >= 7`) && falsey (`12 < 8`)

Now, we'll see what happens with different input types:

```js
"Hello Dolly" && 7
```

Again, the logical operator (&&) will categorize the inputs on each side as either falsey and truthy:

```js
truthy ("Hello Dolly") && truthy (7)
```

See how the values were converted to truthy/falsey and then compared? “Hello Dolly” evaluates to true, as it's a non-empty string, and 7 also evaluates to true, as it's a number that's not 0.

As they say:

"To a hammer, everything looks like a nail."

But in our case, the hammer is a boolean operator and the nail is a boolean value.

Although this may seem somewhat abstract, understanding which values are “truthy” and “falsey” will help us ease our workflow and troubleshoot problems as we move along.

<img src="assets/hammer.svg)" width="150px">

Let’s learn a bit more about how we use boolean values in practice.

We program computers to make decisions based on the data they have currently.

For example, a thermostat system might be programmed to turn on if a house drops below 45 degrees.

Logic is the process of combining multiple conditions to form true/false values that enable a computer to make "decisions." We most often use AND and OR to combine boolean expressions.

*Truth Tables* are a helpful way to remember the result of combining any two boolean expressions using AND, OR, or NOT.


>Exercise: Looking at the following table, see if you can predict the results in the last three columns given the values for A and B in each row. Try not to click back to see the answer!


> Answer:

Before wrapping up the lesson, let’s practice what we've learned one last time.

Can you predict how the following expressions will be evaluated?

Try typing each expression into your console in Chrome.


<!--
ID NEEDED: Help formatting teh following exercise
!('')
The console returns true.
false && undefined
The console returns false.
true && !0
The console returns true. -->



<!-- @sarahholden Insert video: Truthy and falsey -->




## Conditional Statements (# mins)

<!-- @sarahholden insert video conditional statements -->

Now we’re going to learn a bit more about conditional statements and how we can use them to control the flow of a program.

For example, we can use a conditional statement to skip over a block of code if it does not pass a boolean expression.

Don’t worry if that sounds confusing, because we’re about to break it all down.

Let’s say our condition is `7 > 5`.

This is an example of a condition that the interpreter will know as either true or false.

Once we have this type of condition, we can add in our conditional statements to take one path if the condition is true and another if the condition is false.

Take a look, and see if you can pinpoint where the operators we learned about in the last lesson come in handy:

```js
if (condition) {
  // Take one path
} else {
  // Take another path
}
```

```js
if (7 > 3 && 1 < 5) {
  // Take one path
} else {
  // Take another path
}
```

Don’t worry about how everything is written at this point, we’ll go over that in detail later in this lesson.

Let's take a look at the answer:

condition.svg)

There are two types of conditional statements in JavaScript:

`if...else` statements

and

`switch` statements.

Let’s start by looking at `if...else` statements.

As you may have guessed from its name, the first component of the `if...else` statement is the *if statement*.

An *if statement* allows us to check whether or not a condition is true and, if it is, run our code.

The conditional below is an `if` statement.

An `if` statement will take in a condition and, if that condition is truthy, run whatever code you specify.

condition_zoom.svg)

Let’s look at an example:

truty.svg)

If the condition (in this case, `x > 10`) is truthy, the lines of code inside the curly braces (`{...}`) will be evaluated one by one. Note: the code between the curly brackets is a block of code.

truthy_2.svg)
truthy_3.svg)


You're probably already familiar with a common real-world application of the `if` statement: the *flow chart*.

A *flow chart* is a visual diagram that tells us how to behave depending on a certain set of conditions.

flow_chart.svg)

If we were to draw a flowchart to describe the following if statement:


```js
if (x > 10) {
  x += 10;
  y += 10;
}
```

We might come up with something like this:

As you can see, a person making their way through this diagram would need to make a decision.

Depending on whether or not our condition is truthy, he or she would either enter the block of code or skip over it entirely.

flow_chart_1.svg)

`If` can actually be modified in several ways to change its behavior.

One of these ways is through the use of an *else statement*.

For instance, adding an `else` to our `if` statement allows us to specify a second condition to test.

However, this second condition will *only* be tested if the first condition fails.

For example, let's say we want to offer both a senior discount and a student discount for movie tickets:

```js
if (age < 18) {
  console.log("Student discount applied");
} else if (age > 65) {
  console.log("Senior discount applied");
}
```

Notice how we are now able to check to see if multiple conditions are true.

Let’s look at another example:

code_example_2.svg)

flow_chart_2.svg)

We can add as many `else if` statements as we want. You just keep tacking them on.

These statements allow us to add complex logic to our program, which can check for multiple conditions and specify an action for each result, making our program seem more intuitive and user friendly.

else_if.svg)

At this point, if none of the conditions we check for are true, then nothing will happen.

We need a way to check several conditions and have the ability to move forward if none of these conditions are true— a default, or fallback, course of action.

To specify behavior for this outcome, we must add an `else` to the end of our statement.

Let's look at an example of an else statement:

Slide-25-If-Else.svg)

Here’s an example of an else statement as a flow chart:

Slide-27-Code.svg)

Slide-26b-Example.svg)

Let's try an example!

Imagine you work the information booth at a theme park and help recommend rides to guests.


If a person is less than 8 years old, recommend the merry-go-round.

Else if a person is more than 8 years old and less than 65 years old and more than 4.5 feet tall, recommend the roller coaster.

Else recommend the lazy river.

Here's how that would look in JS. Try it in the console below!

var age = 25;
var height = 5;
if (age <= 8) {
  console.log("Check out the Merry-Go-Round. You'll love it!");
} else if (age > 8 && age < 65 && height > 4.5) {
  console.log("Check out the Roller Coaster. It's awesome!");
} else {
  console.log('Why not enjoy a float down the Lazy River?');
}

Within our conditions, we will often need to check to see whether or not two values are equal to one another, and perform an action based on the results.

Example:

```js
if (result === true) {
  // Congratulate the user on passing
}
```

Notice that we used a triple equals instead of a single equals in the condition.


This is important to note, as confusing the assignment operator with the comparison operator is a common mistake for beginners.

Slide-30-Assignement-Comparison.svg)

Remember: An *assignment* is when we give a variable a value.

A *comparison* checks the relationship between two values.

A single equals sign is reserved for assigning a value to a variable, whereas a triple equals sign can be used to compare two values.

Take a look at the following example:

Here, we are not comparing x with the number 3. We're assigning the variable x the value of 3 by using = instead of ===.

if (x = 3) {
  console.log("boo");
}

If we wanted to see if x is equal to 3, we would use a comparison operator (the triple equals sign):

if (x === 3) {
  console.log("boo");
}

Let’s turn to a summary of conditionals and test ourselves with a short quiz.

Using if...else statements allows us to write code that can behave very differently in different circumstances.

Consider the following conditional statement:


if (x > 5) {
  y = 50;
} else if (x < 5) {
  y = 33;
} else {
  y = 100;
}


Use the same example to answer the questions given:

if (x > 5) {
  y = 50;
} else if (x < 5) {
  y = 33;
} else {
  y = 100;
}
What value will be assigned to y if x is 10?
Answer: 50
What value will be assigned to y if x is 4?
Answer: 33
Under what circumstances will y be assigned a value of 100?
Answer: x=5

These are just some of the foundational tools you'll use while building your applications with JavaScript.

You'll probably need to refresh yourself on the exact syntax a few times before you memorize it, but it's important to be able to remember these core "control flow" concepts in general, as they'll come up in pretty much every programming language you'll ever encounter.

Video: Looping Conditionals

In the past few lessons we’ve only been able to operate on one value at a time. For example:

`If` a bank has more than $20, allow a withdrawal. `Else` show an error message.

In this lesson, we’re going to learn about collections and loops and why they’re useful.


**Collections** are groups of values. An example of a collection is an array. One of the most useful things about collections (and arrays in particular) is that if we structure our code correctly, we can repeat the same operation on each value within a collection.


This process of doing something over and over and over again in a loop, for each element in a set, is called **iteration**. while (someCondition) { //A block of code. }


To tell your program to repeat something, you use a tool called a **loop**. Loops work just like you might imagine: Once your program has finished running a block of code, it 'loops' back to the beginning and starts again.

Remember our `if` statement from the previous lesson? Let's loop it back on itself.


![](http://circuits-assets.generalassemb.ly/prod/asset/4819/Slide-14-Flow-Chart.svg)



All we have to do is make one small (but very important) change: instead of advancing to the next bit of code after executing the block, we loop back to our condition.


![](http://circuits-assets.generalassemb.ly/prod/asset/4820/Slide-6-Flow-Chart.svg)




Now, we have a loop — so long as our condition remains true (or at least truthy), we will continue to run that block of code over and over again. This type of loop is called a **while loop**, and it can be found in nearly every programming language.


The general rule for writing a **while loop** in JavaScript is: while (someCondition) { // A block of code. } As you can see, it's written in almost exactly the same way as an `if` statement.

Let’s look at an example. If x = 10 and we're subtracting 2 each time we go through the loop, how many times will this loop run?


![](http://circuits-assets.generalassemb.ly/prod/asset/4931/Slide-8a-Loop.svg)



If you guessed 3 times, you're right! The final value of x will be 4. Remember, you can use `console.log(x)` to find this answer in the console.


![](http://circuits-assets.generalassemb.ly/prod/asset/5137/Slide-11-Loop-3-Times.svg)




Let’s look at another example: var x = 10; var y = 1; while (x < 20) { y += 1; } How many times will this loop run?


var x = 10; var y = 1; while (x < 20) { y += 1; }

The loop would run indefinitely. Since x is defined as 10 and x is less than 20, the computer will run it forever because it is always true.


var x = 10; var y = 1; while (x < 20) { y += 1; }

A `while` loop can run **indefinitely** as long as your condition remains true or until a condition is met.


var x = 10; var y = 1; while (x < 20) { y += 1; }

The advantage is the computer will run code until a condition is met; the disadvantage is that you have no idea how long that will take (_and it will most likely cause your computer to freeze!_).


var x = 10; var y = 1; while (x < 20) { y += 1; }

When using a `while` loop, it's **very important** to plan out beforehand how you will 'escape' the loop by making your condition evaluate to false.

Take a look at the following example: ![](http://circuits-assets.generalassemb.ly/prod/asset/4933/Slide-11-myString-Example.svg)
Questions to consider: * How many times does this loop run? * What's the final value of myString?

![](http://circuits-assets.generalassemb.ly/prod/asset/4934/Slide-12-myString-Annotated.svg)
Each time this loop runs, the value of z increases by 1. Since its initial value is 0, and the condition becomes false the moment that z becomes 5, our loop will run exactly 5 times.

![](http://circuits-assets.generalassemb.ly/prod/asset/4934/Slide-12-myString-Annotated.svg)
As a result, the string myString has a final value of "XXXXX" (5 Xs).

![](http://circuits-assets.generalassemb.ly/prod/asset/4934/Slide-12-myString-Annotated.svg)
So each time we use z += 1, we increase the value of z so that eventually our condition, z < 5, will be false. If we increase z by one each time, there is no way that z will always be less than 5! This is our **“escape plan”** for this while loop.


Confused? Don’t worry, here's the play-by-play:
## LOOP 1
![](http://circuits-assets.generalassemb.ly/prod/asset/4935/Slide-14-myString-Example.svg)
* `z` starts with the value 0 and `myString` is set to `""`. * Since `z = 0`, the statement `z < 5` is true; so the block gets executed. * In the 4th line, `"X"` gets added to the end of `myString`; it is now `"X"` * In the 5th line, `z` is increased by 1; its value is now 1. * Now that the block is done, we loop back to the condition.
## LOOP 2
![](http://circuits-assets.generalassemb.ly/prod/asset/4937/Slide-16-X-Added.svg)
* Now `z` has the value 1; however z < 5 is still true; so the block still gets executed. * In the 4th line, `"X"` gets added to the end of `myString`; it is now `"XX"` * In the 5th line, `z` is increased by 1; its value is now 2. * Now that the block is done, we loop back to the condition once again.
## LOOP 3
![](http://circuits-assets.generalassemb.ly/prod/asset/4938/Slide-17-Z-Increased.svg)
* Now `z` has the value 2, so once again `z < 5` is true and the block gets executed. * In the 4th line, `"X"` gets added to the end of `myString`; it is now `"XXX"` * In the 5th line, `z` is increased by 1; its value is now 3. * Now that the block is done, we go back to the condition.

![](http://circuits-assets.generalassemb.ly/prod/asset/4934/Slide-12-myString-Annotated.svg)
This continues until `z` has the value 5. Once `z` is 5, `z < 5` will become **false**; and therefore, the block will not get executed again.

![](http://circuits-assets.generalassemb.ly/prod/asset/4934/Slide-12-myString-Annotated.svg)
What's most interesting about this kind of setup is that if we changed that condition from `z < 5` to `z < 10`, or `z < 100`, the loop would change to run exactly 10 or exactly 100 times, respectively.

![](http://circuits-assets.generalassemb.ly/prod/asset/4934/Slide-12-myString-Annotated.svg)
Basically, we’ve changed the `while` loop so that it always runs for a fixed, controllable number of times—ensuring that it will never get stuck in an infinite loop.

![](http://circuits-assets.generalassemb.ly/prod/asset/4934/Slide-12-myString-Annotated.svg)
This kind of setup is so useful, and gets used so frequently, that most languages include a special kind of loop used for just this kind of behavior, called a `for` loop.


Despite being one of the most basic ways to iterate through an array in JavaScript (and many other languages), the `for` loop is also one of the most versatile ones!

Let's make a few modifications to our `while` loop from earlier. As you can see, there are a couple of key ingredients to making our `for` loop work.


![](http://circuits-assets.generalassemb.ly/prod/asset/4365/Slide-27-Flow-Chart.svg)



Let’s break down what we’ll need: 1\. An 'initialization', which sets up a starting situation (e.g. var i = 0) 2\. A condition, which gets evaluated each time we're about to execute the block (e.g. i < 10) 3\. A 'finalExpression', which gets evaluated immediately after the block executes _but before the condition is evaluated again_ (e.g. i += 1;)


![](http://circuits-assets.generalassemb.ly/prod/asset/4365/Slide-27-Flow-Chart.svg)




The general syntax for a `for` loop is: for (initialization; condition; finalExpression) { // A block of code. }

## Let’s practice! Look at the code below: var x = 10; for (var i = 0; i < x; i += 1) { console.log('HELLO'); } Use the console below to answer the questions.
1\. How many times will `HELLO` be printed out in the console? * `Hello` will be printed out 10 times. 3\. What if we changed the starting value of i to 1 instead of 0? How many times would `HELLO` get printed to the console then? * `Hello` will be printed out 9 times. 5\. What would happen if we changed the condition from `i < x` to `i <= x?` * `Hello` will be printed out 11 times. 7\. What would happen if we changed the final condition from `i += 1` to `i += 2`? * `Hello` will be printed out 5 times. Great job!


Let’s take a step back and recap what we have learned. What is the difference between `for` loops and `while` loops

The `while` loop is usually used when you need to repeat something until a given condition is true: inputInvalid = true; while(inputInvalid) { //ask user for input inputInvalid // check valid input; }
On the other hand, the `for` loop is usually used when you need to iterate a given number of times: for(var i = 0; i < 100; i+=1) { ...//do something for a 100 times. }


You can learn more about the differences between `for` and `while` loops [here](http://programmers.stackexchange.com/questions/244393/what-are-the-differences-between-a-while-loop-and-a-for-loop).

Let’s look at a temperature converter for an example of a `for` loop.


![](http://circuits-assets.generalassemb.ly/prod/asset/4366/Slide-34-Thermometer.svg)



Suppose that we were given an array of starting values to work with—a group of temperatures in degrees Fahrenheit. Now let’s say we want to convert them into another set of values—temperatures in degrees Celsius—which would then be stored in a separate array.
var tempsInF = [100, 72, 88, 15, 25, 32]; var tempsInC = [];


The formula for converting between Fahrenheit and Celsius temperatures is **C = (F - 32) * 5/9**, where F is the temperature in degrees Fahrenheit and C is the temperature in degrees Celsius.


So how do we go about operating on the elements in tempsInF? Well, we could just start at the beginning and work our way through, one value at a time. tempsInC.push((tempsInF[0] - 32) * (5 / 9));


Then, we could run an almost identical command to operate on each element in tempsInF and push the converted value onto the tempsInC array: tempsInC.push((tempsInF[1] - 32) * (5 / 9)); tempsInC.push((tempsInF[2] - 32) * (5 / 9)); tempsInC.push((tempsInF[3] - 32) * (5 / 9)); tempsInC.push((tempsInF[4] - 32) * (5 / 9)); tempsInC.push((tempsInF[5] - 32) * (5 / 9)); However, this code is extremely repetitious, and it also forces us to "hard code" exactly how many times we want the operation to be performed.


What is "hard coding"? Generally you’ll want to avoid hard coding because it means you’ve set a value as fixed. If you want to go in and change it, you’d have to manually change the code in every single place it appears (which could be a lot of times if you have a long complex program). It is better to let the code input actual values or write code so that if you want to change a value you can change it once and it will change throughout. tempsInC.push((tempsInF[1] - 32) * (5 / 9)); tempsInC.push((tempsInF[2] - 32) * (5 / 9)); tempsInC.push((tempsInF[3] - 32) * (5 / 9)); tempsInC.push((tempsInF[4] - 32) * (5 / 9)); tempsInC.push((tempsInF[5] - 32) * (5 / 9));


Let’s return to our temperature example. You wouldn’t want to hard code the temperature to be 72 degrees, as temperature constantly changes. What if the temperature was 60? You would have to go through and manually change each value to 60. Rather you’d want to create code that can take whatever the current temperature is and perform an operation.


It'd be better if there were a way to run this code exactly as many times as there are elements in the first array. Fortunately, there is a tool perfectly suited for this task—our old friend, the `for` loop. for (var i = 0; i < tempsInF.length; i += 1) { tempsInC.push((tempsInF[i] - 32) * (5 / 9)); }



For Loop

for (var i = 0; i < tempsInF.length; i += 1) { tempsInC.push((tempsInF[i] - 32) * (5 / 9)); }


Operating One Element At a Time

tempsInC.push((tempsInF[1] - 32) * (5 / 9)); tempsInC.push((tempsInF[2] - 32) * (5 / 9)); tempsInC.push((tempsInF[3] - 32) * (5 / 9)); tempsInC.push((tempsInF[4] - 32) * (5 / 9)); tempsInC.push((tempsInF[5] - 32) * (5 / 9));

Take a minute to think about what's going on above. By starting our count at zero `var i = 0`, increasing `i` by one every time, and stopping before `i` reaches the length of the array `i < tempsInF.length`, we are running the loop one time for every item in the array.



For Loop

for (var i = 0; i < tempsInF.length; i += 1) { tempsInC.push((tempsInF[i] - 32) * (5 / 9)); }


Operating One Element At a Time

tempsInC.push((tempsInF[1] - 32) * (5 / 9)); tempsInC.push((tempsInF[2] - 32) * (5 / 9)); tempsInC.push((tempsInF[3] - 32) * (5 / 9)); tempsInC.push((tempsInF[4] - 32) * (5 / 9)); tempsInC.push((tempsInF[5] - 32) * (5 / 9));

`i` will be successively set to the index of every element in our array, allowing us to perform the same operation on each element.


So, in other words, we are looping through each item in the tempsInF array, converting that value to celsius, and then adding the celsius value to the end of the tempsInC array. We could just as easily have gone in the opposite direction—starting at the last element, and ending with the first—simply by specifying different settings in the `for` loop: for (var i = (tempsInF.length - 1); i >= 0; i -= 1) { tempsInC.push((tempsInF[i] - 32) * (5 / 9)); }


We could even operate only on every third element, by changing the value we increment `i` with, like so `i += 3`: for (var i = 2; i < tempsInF.length; i += 3) { tempsInC.push(fahrToCelc(tempsInF[i])); }


We’ve seen how loops can be used to easily repeat a certain set of actions numerous times. You will learn throughout this course how you can utilize loops in order to make your work more efficient and simpler.


<!-- U2L4 -->

Now that you’re feeling more comfortable with if...else statements, let's go back to the other type of conditional statement we mentioned earlier in this unit: **switch statements**. We've seen how a person can check numerous conditions by simply tacking on **else if statements**.

if (x > 10) {
x += 10;
y += 10;
} else if (x > 5) {
x += 5;
} else if (x > 3) {
x += 3;
}

Here’s a refresher of what the flowchart for this action would look like: ![](http://circuits-assets.generalassemb.ly/prod/asset/4408/Slide-4-Flow-Chart.svg)

However, if we have a lot of conditions, the code becomes repetitive and hard to read. For example:



// day of the week in a number, sunday is 0, saturday is 6
var dayNumber = 1;
if(dayNumber === 0){
day = 'Sunday';
} else if(dayNumber === 1) {
day = 'Monday';
} else if(dayNumber === 2) {
day = 'Tuesday';
} else if(dayNumber === 3) {
day = 'Wednesday';
} else if(dayNumber === 4) {
day = 'Thursday';
} else if(dayNumber === 5) {
day = 'Friday';
} else if(dayNumber === 6) {
day = 'Saturday';
} else {
day = null;
alert('wrong value for day');
}

// day of the week in a number, sunday is 0, saturday is 6
var dayNumber = 1;
if(dayNumber === 0){
day = 'Sunday';
} else if(dayNumber === 1) {
day = 'Monday';
} else if(dayNumber === 2) {
day = 'Tuesday';
} else if(dayNumber === 3) {
day = 'Wednesday';
} else if(dayNumber === 4) {
day = 'Thursday';
} else if(dayNumber === 5) {
day = 'Friday';
} else if(dayNumber === 6) {
day = 'Saturday';
} else {
day = null;
alert('wrong value for day');
}


What the code to the left does, fundamentally, is pretty simple — it takes in a number (representing a particular day of the week) and spits out a string containing the name of that day. However, this code is not easy to read, and a lot of it is repeated. For one, `} else if(dayNumber === __ ) {` is repeated seven times. What's more, if we ever want to change the name of our `dayNumber` variable, we'll need to swap it out every place it appears.

Enter the `switch statement`. A **switch statement** is used to perform different actions based on different conditions. It is a replacement for if/else statements when our code gets long and nested. Take a look at how the previous example would be written as a switch statement:



var dayNumber = 1;
switch (dayNumber) {
case 0:
  day = 'Sunday';
  break;
case 1:
  day = 'Monday';
  break;
case 2:
  day = 'Tuesday';
  break;
case 3:
  day = 'Wednesday';
  break;
case 4:
  day = 'Thursday';
  break;
case 5:
  day = 'Friday';
  break;
case 6:
  day = 'Saturday';
  break;
default:
  day = null;
  alert('wrong value for day');
}

This code works exactly the same as our `if/else` statement, and, even though it contains more lines, it's significantly easier to read. In a switch statement, the variable in parentheses (in this case, `dayNumber`) is evaluated; if there is a `case` listed for the value it evaluates to, the code between `case __:` and `break` will be executed. If there is no `case` that matches the value of the variable, the `default` will be executed (if it is specified, that is — if not, the program will do nothing).

![](http://circuits-assets.generalassemb.ly/prod/asset/4409/Slide-9-Code.svg)



If there is no `break;` at the end of a case, the computer will not skip to the end. Instead, it will start executing the next case's code (even if the case's value is different than the variable’s), and will continue doing so until it eventually hits a `break;` statement.

![](http://circuits-assets.generalassemb.ly/prod/asset/5014/Slide-10-Break.svg)



For this reason, default never needs a `break;` statement, as it's the last case in the switch. Include breaks on all other statements to makes sure the program breaks out of switch once it executes the matched statement.  


![](http://circuits-assets.generalassemb.ly/prod/asset/5014/Slide-10-Break.svg) The main advantages of switch statements is the increase in readability and the decrease in repetition, both of which make your code more maintainable. Although the switch statement has some advantages over `if...else`, it also has some major disadvantages. For instance, a switch statement will only work if you are testing the same variable (or expression) in every condition; if not, the `if...else` is your only option. Also, depending on the circumstances, using `if...else` might scan more naturally. As a rule, use switch statements when you are working with only one variable, or if you have three or more conditions to check.

![](http://circuits-assets.generalassemb.ly/prod/asset/4411/Slide-12-Chart.svg) Use `if...else` when you have multiple variables (or expressions) or only need one `else...if` statement.

![](http://circuits-assets.generalassemb.ly/prod/asset/4411/Slide-12-Chart.svg)  

Now it’s time to test yourself. Take a look at the following `switch` statement:

switch (2 * x) {
case 2:
  y = 49;
  break;
case 4:
  y = 37;
  break;
case 6:
  y = 25;
  break;
case 8:
  y = 13;
  break;
default:
  y = 1;
}



What value will `y` be assigned when `x` is ...

*   1?
*   4?
*   0?
*   "Hello"?

You can do mental math first, or use the console below to check your answers:

Pause and come up with your answers before clicking forward. Let’s take a look at the answers.

switch (2 * x) {
case 2:
  y = 49;
  break;
case 4:
  y = 37;
  break;
case 6:
  y = 25;
  break;
case 8:
  y = 13;
  break;
default:
  y = 1;
}



What value will `y` be assigned when `x` is ...

*   1 ?
*   Answer: 49
*   4?
*   Answer: 13
*   0 ?
*   Answer: 1
*   "Hello"?
*   Answer: 1

Great job! Now that we’ve had a chance to gain some experience with switch statements, let’s move on. Another shortcut for a simple JavaScript if...else statement is the **ternary statement**. A ternary statement is a one-line shorthand for an if...else statement. Similar to an `if...else` statement, it evaluates a condition and then returns one of two results based on whether the condition is true or false. Take a look at the following `if...else` statement:

var studentPasses;
if (score > 80) {
studentPasses = true;
} else {
studentPasses = false;
}



![](http://circuits-assets.generalassemb.ly/prod/asset/4407/Slide-16-Exam.svg) The code from the last slide could be shortened to a single line using a ternary statement.  

Let's take a look on the next slide.



var score = 90;
var studentPasses = score > 80 ? true : false;
studentPasses;
//=> true

`condition ? result1 : result2;`

Whatever the `if` condition is will be used as the condition here. Again, a condition is a statement that evaluates to true or false.  


var score = 90;
var studentPasses = score > 80 ? true : false;
studentPasses;
//=> true

`condition ? result1 : result2;`

So, in the example, the condition would be `score > 80`. The condition is then followed by a question mark (`?`).  


var score = 90;
var studentPasses = score > 80 ? true : false;
studentPasses;
//=> true

`condition ? result1 : result2;`

`result1` and `result2` are our possible outcomes. If the condition is true, the operator will return the value of `result1`, otherwise it will return the value of `result2`.



Let’s look at the difference between the two code blocks below. Do you notice the difference in syntax between the `if...else` statement and ternary operators?



var score = 90;
var studentPasses;
if (score > 80) {
studentPasses = true;
} else {
studentPasses = false;
}
//studentPasses would evaluate to true


var score = 90;
var studentPasses = score > 80 ? true : false;
//studentPasses would evalute to true


Here's a second example:

var weather;
if (temperature > 60) {
weather = "fair";
} else {
weather = "poor";
}



This could be shortened to the following:

var weather = temperature > 60 ? "fair" : "poor";



![](http://circuits-assets.generalassemb.ly/prod/asset/4412/Slide-18-Weather.svg)



Although having clean and succinct code is useful, readability is also important. Sometimes ternary statements can be harder to scan and understand than a simple `if...else` statement. So, if you’re ever in doubt, remember to choose readability over less code. Let’s give it a try! Take this `if...else` statement, and turn it into a ternary statement:

var day = "Monday";
var goToWork;
if (day === "Saturday" || day === "Sunday") {
goToWork = false;
} else {
goToWork = true;
}



Try practicing in the console below. Pause and come up with your answer before clicking forward.Does your answer look something like this?

var goToWork = day === "Saturday" || day === "Sunday" ? false : true;

![](http://circuits-assets.generalassemb.ly/prod/asset/4414/Slide-21-Lazy-Sunday.svg)![](http://circuits-assets.generalassemb.ly/prod/asset/4413/Slide-20-Calendar.svg)

# Let's Practice!

What will the value of `goToWork` be under the following circumstances? (Try figuring it out in your head or type the code out in the console.

1.  `var day = "Wednesday"`

*   The console returns `true`

3.  `var day = "Saturday"`

*   The console returns `false`

5.  `var day = "Friday"`

*   The console returns `true`

Great job!



var goToWork;
if (day === "Saturday" || day === "Sunday") {
goToWork = false;
} else {
goToWork = true;
}

Now that you have some experience with ternary statements, let’s talk a bit more about the use of switch statements. First you'll write out the following scenario as a long if...else statement, and then you'll refactor the if...else statement to be a switch statement in the next step.

# Let's Practice!

First, declare a variable grade and set it equal to "B". Then, create an `if...else` statement that checks to see if the student got an A, B, C, D, or F.

*   If the student received an A, log "Awesome Job" to the console.
*   If student received a B, log "Pretty Great" to the console.
*   If student received a C, log "Pretty Average" to the console.
*   If student received a D, log "Need to Study" to the console.
*   If the student received an F, log "Bad Job" to the console.

Here's what the scenario would look like as an if...else statement:



var grade = "B";

if (grade === "A") {
console.log("Awesome Job");
} else if (grade === "B") {
console.log("Pretty Great");
} else if (grade === "C") {
console.log("Pretty Average");
} else if (grade === "D") {
console.log("Need to Study");
} else if (grade === "F") {
console.log("Bad Job");
}


Now, rewrite the if...else statement as a switch statement.  

Here's what this if...else statement will look like when refactored into a switch statement:

var grade = "B";

switch (grade) {
case "A":
  console.log("Awesome Job");
  break;
case "B":
  console.log("Pretty Great");
  break;
case "C":
  console.log("Pretty Average");
  break;
case "D":
  console.log("Need to Study");
  break;
case "F":
  console.log("Bad Job");
  break;
default:
  console.log("Nonexistent");
}

Which is faster—the if...else statement or the switch statement?



var grade = "B";

if (grade === "A") {
console.log("Awesome Job");
} else if (grade === "B") {
console.log("Pretty Great");
} else if (grade === "C") {
console.log("Pretty Average");
} else if (grade === "D") {
console.log("Need to Study");
} else if (grade === "F") {
console.log("Bad Job");
}





var grade = "B";

switch (grade) {
case "A":
  console.log("Awesome Job");
  break;
case "B":
  console.log("Pretty Great");
  break;
case "C":
  console.log("Pretty Average");
  break;
case "D":
  console.log("Need to Study");
  break;
case "F":
  console.log("Bad Job");
  break;
default:
  console.log("Nonexistent");
}

Consider how many computations run in each approach. When evaluating for grade `D` using the `if...else` approach, the condition `grade === 'x'` is evaluated four times. What if the `if...else` statement had 10 conditions? 100? How would this impact the speed of the program? In contrast, when using a switch statement, the condition is only evaluated one time. ![](http://circuits-assets.generalassemb.ly/prod/asset/4415/Slide-24-Awesome-Job.svg) As our scripts grow in size and complexity, we want to make sure that each time we work on a piece of code, we think about how we can make that code perform as effectively as possible. Throughout this course, we’ll be covering small ways to improve performance that will have a big impact, especially on projects with much more code. We saw earlier how `break;` plays a major role in switch statements. Again, if there is no `break;` at the end of a case, the computer will not skip to the end. Instead, it will start executing the next case's code (even if the case's value is different from the variable’s) and do so until it hits a `break;` statement. Can you guess what would happen if you removed the breaks from the switch statement you created? Run the code to find out! In this lesson, we looked at how we can keep our code readable and concise by using ternary and switch statements. We saw how these statements can make our code more concise, more readable, and more effective. Often, developers will write code to get things up and running first and then look back over the code to see how it could be streamlined. Switch and ternary statements are excellent tools for doing just that!





In the last unit we looked at how we can control the flow of a program by using conditional statements and loops, and after that, you probably noticed how quickly a program can grow in length and complexity.




In this unit we’ll be taking a look at how we can use functions to group together statements that perform a specific task and reduce repetition in our programs.




**Function** is a term that comes out of mathematics. You may remember hearing it in your high school algebra class.

The basic idea of a function is simple — it’s a relationship between a set of inputs and a set of outputs.




Take a look at the relationship between variable x and function f in this example.

Function f takes the input x and spits out a single output ( f(x) ).

Can you guess what this function does to the value of x?

If you guessed "multiplies x by 2," you're right!


![](http://circuits-assets.generalassemb.ly/prod/asset/4416/Slide-5-Funnel-Chart.svg)



In JavaScript, a function can be made up of either a single reusable statement or a group of reusable statements.

Functions can be called from anywhere in the program, which allows for the statements inside a function to not be written over and over again.

Functions are especially useful because they enable a developer to segment large, unwieldy applications into smaller, more manageable pieces.




Here's an example of what a function can do:

If you’ve watched enough Matt Damon movies, you may have noticed that the government often spends a lot of time and money to go save his characters.


![maaaaatt daaaamon](http://circuits-assets.generalassemb.ly/prod/asset/5031/matt-damon.jpg)



Even if you haven’t watched a single Matt Damon movie, take our word for it—the guy can’t keep himself out of trouble.

Now let’s take a look at a program that breaks down some of Matt Damon’s movies and their respective rescue costs.


![maaaaatt daaaamon](http://circuits-assets.generalassemb.ly/prod/asset/5031/matt-damon.jpg)



As you can see from the code, a director only wants to save Matt Damon if the cost is less than a 1000 dollars.

This then repeats for every additional movie.


![](http://circuits-assets.generalassemb.ly/prod/asset/4429/mattDamon.png)



This is all easy enough to write out, but because Matt Damon has been in so many movies where he needs to be rescued this code is going to get pretty lengthy!

Let’s try to keep our code from getting out of hand by using a function.


![](http://circuits-assets.generalassemb.ly/prod/asset/4429/mattDamon.png)



Notice how much cleaner and simpler this function looks than our repeated lines of code?

Now if Matt Damon decides to film more movies where he needs to be rescued, all we have to do is type:

MattDamon(“MovieTitleHere”, CostHere)



![](http://circuits-assets.generalassemb.ly/prod/asset/4418/Slide-10b-Screenshot-Annotated.svg)  



Using functions is a great way to save time for yourself, and simplify things for your team members.

Take a look at the MattDamon examples side by side:


![](http://circuits-assets.generalassemb.ly/prod/asset/4429/mattDamon.png)

![](http://circuits-assets.generalassemb.ly/prod/asset/4417/Slide-10a-Screenshot.svg)



Functions are a critical component of programming because they allow us to execute on a key tenant of engineering:

"**D**on't **R**epeat **Y**ourself" (aka "DRY" code).

Our goal is to craft our programs in as few lines of code as possible, while still being clear.




Why should we avoid repetition?

1.  **Performance -** Having repeated code will lead to longer scripts. Longer scripts take up more memory and will take more time to load, which can make a website seem slow.

3.  **Maintainability -** Imagine that we have the same line of code repeated 10 times in our program. If we ever want to change that functionality, we would have to search for all 10 places where that code is repeated and make 10 individual changes.




Let’s look at an example of DRY in action.

You’ve probably noticed that there are some common pieces of code that often pop up on websites (such as a “Your shopping cart is full!” or an “Are you sure you want to leave this page?” alert).

**These are examples of functions**.


![](http://circuits-assets.generalassemb.ly/prod/asset/4419/Slide-16-Cart-Full.svg)



Developers often create functions just so they can reuse them later.

Doing so can make a developer’s workflow more efficient and increase the processing speed of the program.


![](http://circuits-assets.generalassemb.ly/prod/asset/4419/Slide-16-Cart-Full.svg)



Let's review the three main reasons that functions are created:



![](http://circuits-assets.generalassemb.ly/prod/asset/5016/Slide-17-Chart.svg)




Now we know what functions are and why we use them. But how do we create them?




As you saw in our Matt Damon Rescue example, just as we do with a variable, we must define a function before we call or “use” it.

In JS, functions can be defined in several ways. Two of the more common methods of defining a function are **function declaration** and **function expression**.

Let’s take a look at **function expressions** first.




A **function expression** defines a function by producing a value that’s stored in a variable.

This is similar to the way an expression produces a value that’s stored in a variable—hence its name.

![](http://circuits-assets.generalassemb.ly/prod/asset/4421/Slide-19.svg)


Have you ever tried to move forward to the next page of an online form, only to be greeted by an alert that says “Please fill out all the required fields”?

This kind of pop-up is created by using functions. Let's code for this popup alert using a function expression:

![](http://circuits-assets.generalassemb.ly/prod/asset/5049/code_block_1.png)


Let's take a look at the function in more detail:

As you can see, the first line begins by declaring a variable called `errorAlert`. This is the name that we can then use to call that function.

![](http://circuits-assets.generalassemb.ly/prod/asset/5050/code_block_2.png)


Let's look at the next part of the code:

This is followed by the word `function`, which is a keyword we use to let JS know that we are creating a function.

![](http://circuits-assets.generalassemb.ly/prod/asset/5052/code_block_3.png)


Next, you have a list of parameters surrounded by parenthesis. Even though the parameters that can go within the parentheses are optional, the parentheses themselves are _always_ required.

We'll take a look at what can go within these parentheses in the next lesson, but for now we will just add some empty ones as shown in the example: `()`.

![](http://circuits-assets.generalassemb.ly/prod/asset/5053/code_block_4.png)


Now let’s look at the statements inside the function—the code that will run every time the function is called.

In the example above, this is the alert with the message “Please be sure to fill out all required fields”. The function body must always be wrapped in curly braces `{ }`, even when it consists of only a single statement (as in the example above).

![](http://circuits-assets.generalassemb.ly/prod/asset/5054/code_block_5.png)


Now that we’ve learned about function expressions, let’s discuss naming conventions. You got a brief introduction to how we name things in Unit 1, but this becomes especially important as things get more complex.

You should try and keep your function names short and simple, and have them describe the function’s action as best as possible.




You may have noticed how we capitalize names in JavaScript using the camelCase style.


![](http://circuits-assets.generalassemb.ly/prod/asset/4427/Slide-25-Camel.svg)



To make it easier to read a name like nameofmyfunction, you’d capitalize the first letter of each word after the first word (e.g.nameOfMyFunction — see the resemblance to a three-humped camel?).


![](http://circuits-assets.generalassemb.ly/prod/asset/4427/Slide-25-Camel.svg)



The first word is always lowercase. Keep in mind that identifiers (how we name things) can't use spaces between them.


![](http://circuits-assets.generalassemb.ly/prod/asset/4427/Slide-25-Camel.svg)



Let’s take a quick look at some good and bad examples function names, and what can cause them to break down:

*   **Bad:** thisfunctioncalculatestheperimeterofarectangle  
    (no camelCase, too verbose)

*   **Bad:** my new function  
    (contains spaces)

*   **Bad:** myNewFunction  
    (doesn't explain what it does!)

*   **Good:** calculateArea  
    (describes what it does, short, and uses camelCase)




To run the code in a function, we **call**, or invoke, the function by using the function name followed by parenthesis.

Defining a function is different than calling a function—the code in a function will not run when the function is defined. The code will only run when the function is called.  
![](http://circuits-assets.generalassemb.ly/prod/asset/5055/code_block_6.png)




# Let's Practice!


1.  Write a function `catTalk`.
2.  Inside the function, log `"Meow"` to the console. [Hint: add `console.log()`]
3.  Call the `catTalk` function. [Hint: make sure you use parenthesis]
4.  Check your console to make sure “Meow” is displayed.

Great job!




# Let's practice!


1.  Write a function `area`.
2.  Within the function:

*   Declare a variable `width` and give it the value of 5.
*   Declare a second variable `length` and give it the value of 3.
*   Log `width * length` to the console.

4.  Call the `area` function.
5.  Check your console to make sure 15 is displayed.

Great job!




In this lesson we discussed a key concept of programming  —  **Don't Repeat Yourself**. Our goal is to craft our programs in as few lines of code as possible, while still being clear.

By using functions we can group steps, create code that is reusable, and easily store steps.




In the next lesson we’ll take a look at how we can make functions even more useful by adding parameters — pieces of information that can change the outcome of a function  — to the mix.




Now that we know how to call functions, let’s see how we can add more details to our functions through parameters and arguments.





In the last lesson, we created a function that calculated the area for a space with a width of 5 and length of 3\.

    var area = function () {
      var width = 5;
      var length = 3;
      console.log(width * length);
    }

    area();





What would we do if we also wanted to find the area of our kitchen, a room that is 12 feet wide and 16 feet long?

We could create another function for that area:

    function area() {
      var width = 12;
      var length = 16;
      console.log(width * length);
    }

    area();






What if we wanted to find the area of all the rooms in our house?

We don't want to have to create a separate function for each room—that’s a lot of work on our end.

It will also burden our program with repeated code, which we want to avoid.

Remember, keep it DRY! (Don’t Repeat Yourself).



![](http://circuits-assets.generalassemb.ly/prod/asset/4430/Slide-6-Mansion.svg)






Wouldn't it be nice if we had some way to provide the area function with the information it needs to calculate the area for any given space?

In this lesson, we'll take a look at how we can do just that using **parameters**.



![](http://circuits-assets.generalassemb.ly/prod/asset/4431/Slide-7-House-Parameters.svg)





**Parameters** are the names listed in the function definition.

Let’s take a look at how we can provide our area function with a width and a length for each room so we won’t need to create a separate function every time we want to measure the dimensions of a new room.



![](http://circuits-assets.generalassemb.ly/prod/asset/4432/Slide-9-Parameter.svg)


![](http://circuits-assets.generalassemb.ly/prod/asset/4433/Slide-10-Width-Length.svg)


![](http://circuits-assets.generalassemb.ly/prod/asset/4435/Slide-11-Arguments.svg)


![](http://circuits-assets.generalassemb.ly/prod/asset/4436/Slide-12-Arguments.svg)




To write functions with more than one parameter, use a comma separated list:

e.g., (parameter1, parameter2, parameter3, parameter4, etc.)





Here is an example of a function with four strings as parameters:


    var greetUser = function(firstName, lastName, year, city) {
      console.log("Hello" + firstName + lastName + "born in "+ year + "from" + city + "!" );
    }




What would happen to this...

    var greetUser = function(firstName, lastName, year, city) {
      console.log("Hello " + firstName + " " + lastName + " born in " + year + " from " + city + "!");
    }



...if we input the following argument?

    greetUser("Bruce", "Wayne", 1939, "Gotham");




We would get this result:

    => "Hello Bruce Wayne born in 1939 from Gotham!"





Let’s review parameters and arguments:

![](http://circuits-assets.generalassemb.ly/prod/asset/5017/Slide-16-Chart.svg)




Here's a quick test. Take a look at this function:

![](http://circuits-assets.generalassemb.ly/prod/asset/4534/Slide-18-varPricecheck-no-annotation.svg)

Can you point out the parameters?

Before you click forward, take a moment to think about your answer.





Here's a quick test. Take a look at this function:

![](http://circuits-assets.generalassemb.ly/prod/asset/4438/Slide-18-varPricecheck.svg)

It's the ordered list `(title, listPrice, salesTax)` after the `function`.






1.  Create a function named `disney`.
2.  It should accept two parameters, `villain` and `movie`.
3.  The function should take the parameters and log the result to the console saying “`villain` is the meanest character in `movie`.”
4.  Now, call that function, passing in `Ursula` and `The Little Mermaid` as the arguments.
5.  Check the console to make sure the correct sentence is displayed!

Great job!



# Let's Practice!





We now know how to communicate with functions in one direction, by passing values to functions using parameters and arguments.

But, functions can also communicate back to you and return values.





Sometimes we don’t necessarily want to show or log something immediately to the console, or update something on the page.

Instead, we might just want to update a variable within a function, or even call another function without showing its effects.

To do this, we use a `return` statement.





Let's look at an example of updating a variable within a function.

    // Here this function "spits out" the sum of the parameters x and y
    var sum = function (x, y) {
      return x + y;
    }

    // We then save that sum to the variable totalSum.
    var totalSum = sum(3, 4); => 7
    The variable totalSum will now hold the value 7.





The `return` statement stops the execution of a function and returns a value from that function.



You simply write:

    return value;


Let’s look at an example!






When we `return` something, it ends the function’s execution and “spits out” whatever we are returning.

We can then store this returned value in another variable.





    function addBonusPoints (score) {
        if (score > 50) {
            return score + (score * .10);
            // 60.5 will be returned
        }

        return score;
    }

    var totalPoints = addBonusPoints(55);
    // The variable totalPoints will now hold 60.5








Explained differently, when the function is called in the same example, the function will be executed from top to bottom.

Because the score in this case is greater than 50, we will hit the return statement `return score + (score * .10)` and the function will stop running after that point.





    function addBonusPoints (score) {
        if (score > 50) {
            return score + (score * .10);
            // 60.5 will be returned
        }

        return score;
    }

    var totalPoints = addBonusPoints(55);
    // The variable totalPoints will now hold 60.5








This means that the code inside the function block that is below the `return` statement will never be executed and will be ignored completely.

Pretty powerful, right?





    function addBonusPoints (score) {
        if (score > 50) {
            return score + (score * .10);
            // 60.5 will be returned
        }

        return score;
    }

    var totalPoints = addBonusPoints(55);
    // The variable totalPoints will now hold 60.5







We can also use `return;` by itself as a way to exit the function and prevent any code after it from running.

Here's an example.





Take a look at this:

![](http://circuits-assets.generalassemb.ly/prod/asset/5056/jsc-u3l2-code-graphic.png)

Here, we use `return;` as a way to exit the function instead of returning any value.



![](http://circuits-assets.generalassemb.ly/prod/asset/5056/jsc-u3l2-code-graphic.png)

So now, even if we add:

    console.log("Now playing: " + song + " by " + artist);

this statement will not run.  
![](http://circuits-assets.generalassemb.ly/prod/asset/4440/Slide-29-Rolling-Stones.svg)




Let’s quickly review how functions are written with `return` statements. Remember, JS is sensitive to syntax, and therefore you cannot forget a single bracket, comma, or a semicolon in your code.

![](http://circuits-assets.generalassemb.ly/prod/asset/5045/Slide-39-Function-adScore-Graphic.svg)




In this lesson, we learned how we can pass pieces of information to our function in order to say hello to our friend Bruce Wayne.

We also saw how we can use a `return;` statement when we want to stop the rockAndRoll function from displaying that we’re listening to the Rolling Stones.





In the next lesson, we'll take a look at another way to define functions (function declarations) and how these differ from the function expressions we've been using in the last two lessons.





In the last lesson, we talked about parameters and saw how they related to mansions and to people who may have secret lairs under those mansions (looking at you, Bruce Wayne).

In this lesson, we'll check back in with our old friend Matt Damon and see how he can help us learn about function declarations.






Remember the `mattDamon()` function from Lesson 1?

(Of course you remember, how can you forget a function that decides to “FORGET MATT DAMON”?!)



![](http://circuits-assets.generalassemb.ly/prod/asset/5028/Slide-3-Matt-Damon.svg)






This program uses a function expression.

We can turn that function expression into a **function declaration** simply by changing the way we declare the function.



![](http://circuits-assets.generalassemb.ly/prod/asset/5028/Slide-3-Matt-Damon.svg)






Take a look at the same function, which now uses a function declaration:

Notice that `var` is gone, and now, our function name `mattDamon` immediately follows `function`.

![](http://circuits-assets.generalassemb.ly/prod/asset/5029/Slide-4-function-Matt-Damon.svg)




Let's look at them together:

![](http://circuits-assets.generalassemb.ly/prod/asset/5030/Slide-5-var-function-Matt-Damon.svg)

Both functions do the exact same thing, they’re just written differently.

We’ll tell you more about the different uses for each in a bit, but first let’s review the syntax for function declarations.






As you can see, a function declaration always has:

*   The keyword `function`.
*   A descriptive name that refers to the function (this can be anything you want, as long as it's in camelCase).
*   An optional list of parameters surrounded by parenthesis.



![](http://circuits-assets.generalassemb.ly/prod/asset/4535/Slide-9-Function-Declaration-New.svg)





Let's go back to our favorite function example, `mattDamon()`.

The syntax for a function declaration is pretty similar to function expressions, with a few small differences.

See if you can pick them out in the chart below:

![](http://circuits-assets.generalassemb.ly/prod/asset/4961/Slide-10-Function-Chart.svg)




Function expressions are often referred to as **anonymous functions**, and function declarations are often called **named functions**.

Don’t worry about the terminology right now, we’ll get back to it in just a bit.

![](http://circuits-assets.generalassemb.ly/prod/asset/4962/Slide-11-Function-Chart-Annotated.svg)




Right now, let’s dive deeper into the differences between function declarations and function expressions. While both methods are similar, one of their main differences is the concept of **hoisting**.





In JS, function declarations are always moved, or “hoisted,” to the top of their scope by the interpreter. (Remember, the interpreter is the console in JS — the software that runs the code).

In other words, you can call a function declaration before defining it.





Let's look at an example of hoisting:

![](http://circuits-assets.generalassemb.ly/prod/asset/5022/Slide-13-Hoisting-Chart.svg)




Now we can get back to why we refer to some functions as named and some as anonymous.

Function declarations are often referred to as **named functions** because, in order to be able to call a function declaration, we must give it a name after the keyword `function()`.

Function expressions are often referred to as **anonymous functions**, because the name of the function is omitted after the keyword `function()` and therefore the function itself doesn't have a name--hence, it's considered “anonymous.”





Take a look at this chart to get a better understanding of the differences between named and anonymous functions:

![](http://circuits-assets.generalassemb.ly/prod/asset/4451/Slide-15-Annotated.svg)




Now that you're familiar with both ways of declaring and assigning functions, you can choose which one works best for you.

Let’s watch a video on how programmers choose their favorite method.





You already have some experience using both function expressions and function declarations with parameters and arguments.

Now, we’re going to take a look at one of the complexities that comes with using functions — **variable scope**.

We’ll also dig deeper into how we can use our newfound knowledge of scope to make our scripts run faster and avoid variable naming conflicts.





In JavaScript, where you declare a variable affects where that variable can be used within your code.

When we declare variables inside a function, those variables will only be accessible from within that function. This is known as **scope**.

Let’s look at the two different types of scope: global and local.





Before you even write a line of JavaScript, you're in what is known as the **global scope**.

When a variable is declared outside a function, it is referred to as a **global variable**. A global variable has global scope, which means all scripts and functions on a web page can access it.





For example, when you declare a variable at the very top of your script outside of any function, it's defined globally and can be accessed from anywhere in your script.

Let’s take a look:

![](http://circuits-assets.generalassemb.ly/prod/asset/5015/Slide-7-Annotated.svg)




Conversely, if a variable is declared inside a function, it is local to that function and therefore referred to as a **local variable**.

This also means it has **local scope**. When we have a variable with local scope, it cannot be referenced outside of that function, which means it cannot be called or used outside of the brackets in which it’s contained.






Let’s go back to the brother Bill example from earlier in this lesson to see how we can change our variables to have local scope:

Notice how the variable `brother` is now defined from within the function?  
This is means it is now a local variable and can only be accessed from within that function.



![](http://circuits-assets.generalassemb.ly/prod/asset/5057/jsc-u3l4-code-graphic.png)





Let’s review each type of scope again:

![](http://circuits-assets.generalassemb.ly/prod/asset/5023/Slide-11-Chart.svg)




Another difference between global and local variables is the use of memory.

Every variable takes up memory. The more memory our script requires, the slower our web page.

Let’s take a look at how local and global variables use memory differently.




The interpreter creates local variables when it runs a function and removes them right after that function finishes running.



![](http://circuits-assets.generalassemb.ly/prod/asset/4457/Slide-13-Global-vs-Local.svg)






Global variables, on the other hand, are stored in the processor’s memory for as long as the page is loaded in the browser.



![](http://circuits-assets.generalassemb.ly/prod/asset/4457/Slide-13-Global-vs-Local.svg)






As a result, global variables can be inefficient, because they will continue to take up memory space even when they are not actually in use.



![](http://circuits-assets.generalassemb.ly/prod/asset/4457/Slide-13-Global-vs-Local.svg)





As you begin coding, you’ll find that a typical project can contain thousands of lines of code.

When working on a project with several developers, there is a high probability that two developers might use the same name for variables, which will result in a naming conflict.





You can imagine how easy it can be to accidentally give two variables the same name and overwrite the value of one with the other.

Luckily, by declaring local variables, we are able to avoid these kinds of naming collisions.





As local variables are created when a function runs and then deleted from memory right after that function stops running, two different functions can use local variables with the same name without any sort of naming conflict.

For example:


    var sayHello = function() {
        var sister = "Jane"; // this is created when function runs, deleted immediately after
        console.log("Hello " + sister);
          };

    var sayGoodbye = function() {
      var sister = "Sue"; // this is created when function runs, deleted immediately after
      console.log("Goodbye " + sister);
     };




Conversely, when using global variables, our variables are stored in memory as long as a web page is loaded. This makes it easy to accidentally overwrite the value of one variable with another.

For example:


    var sister = "Jane";
    var sayHello = function() {
        console.log("Hello " + sister);
        }

    var sister = "Sue"; // => Oops! We forgot that we alread had a variable sister and we overwrote it here.
    var sayGoodbye = function() {
        console.log("Goodbye " + sister);
        }




As you can see, local variables help us avoid the risk of naming collisions. Keeping track of which variables we've used inside a function is far easier than keeping track of all the variables used throughout the script.

In the next unit, you’ll learn more about objects, a key to making JS much more efficient. Objects will take your JS programming skills to a whole new level.





In this unit, our focus is objects, an exciting aspect of JavaScript that ties into many of the concepts you’ve already learned.

Once you get to know objects, you’ll realize how much easier your coding life can be.







So far, we’ve learned about fairly simple data types: strings, numbers, booleans, and arrays.

However, as our applications become more complex, we need more structure in our code.






![](http://circuits-assets.generalassemb.ly/prod/asset/4385/Slide-7-Grocery.svg


All of the arrays we've seen so far store and manage their elements by their indices.

This is a convenient way of managing elements, but it also has some disadvantages.







Consider the following:

Say we have a line of friends waiting to get a cup of coffee at Central Perk.

![](http://circuits-assets.generalassemb.ly/prod/asset/4512/Slide-6-Friends.svg)

Here's Rachel, Monica, Phoebe, Joey, Chandler, and Ross.







We can represent this line using the array below:


    var friends = ['Rachel', 'Monica', 'Phoebe', 'Joey', 'Chandler', 'Ross'];


We can refer to each person by their position in the coffee line: Rachel is first (index 0), followed by Monica (index 1), Phoebe (index 2), and so on.







Remember, in JavaScript, we always start an index with the number 0.







But, suppose that Monica rushes out to go clean her apartment. What happens to the coffee line when she leaves?


    var friends = ['Rachel', 'Monica', 'Phoebe', 'Joey', 'Chandler', 'Ross'];
    friends.splice(1, 1);
    friends = ['Rachel', 'Phoebe', 'Joey', 'Chandler', 'Ross'];


Notice that we use the dot notation `.splice` here. We haven’t learned this yet, but no worries! Let's focus on the changing array index for now.







Take a look again at the new array:

    friends = ['Rachel', 'Phoebe', 'Joey', 'Chandler', 'Ross'];

Rachel stays in the same place, because she was standing in front of Monica.

But suddenly, Phoebe isn't at index 2, she's at index 1, right behind Rachel. And Joey has moved into the index 2 spot.

In fact, every person standing in line after Monica ends up taking one big step forward in line. This throws all of our index references into, as it were, “disarray.”







This system does a good job of keeping track of everyone's order, but its biggest drawback is that our method of referencing any element is tied to its position rather than the element itself.

If we wanted to refer to the third person in line, we would no longer be referring to Phoebe.

Fortunately, there are other ways to keep track of our elements: objects.







We’ll illustrate how objects work through the following scenario:

Imagine you have an office fridge containing everyone's lunch.

There's Floyd's salad, Shannon's soup, Matt's tuna sandwich, and Josh's pasta.



![](http://circuits-assets.generalassemb.ly/prod/asset/4560/Slide-10-Fridge.svg)







If Floyd eats his salad, it doesn't affect the placement of anyone else's food.

Similarly, in an object, the association between each label name (reference) and the food item (value) it refers to is preserved.



![](http://circuits-assets.generalassemb.ly/prod/asset/4514/Slide-11-Chart.svg)







It’s important to note that, because each key/value pair is independent. an object doesn't keep a consistent "order" to its elements.



![](http://circuits-assets.generalassemb.ly/prod/asset/4515/Slide-12-Chart.svg)







This is the basic principle underlying objects:

An **object** associates each value (in this case, the type of lunch kept in the fridge) with a reference called a key (the person's name). If a value is removed, it is represented with `null`.



![](http://circuits-assets.generalassemb.ly/prod/asset/4515/Slide-12-Chart.svg)







Let’s go back to our Friends example, where Monica has just rushed out of line to clean her apartment.

What would the code look like as an object instead of an array?

The value for 'Monica' would be represented with `null`.



![](http://circuits-assets.generalassemb.ly/prod/asset/4516/Slide-13-Chart.svg)







Objects are often called **associative arrays**, as they associate keys with values.

As you start building applications, you'll encounter many situations where you'll want to associate keys to values.







Objects are extremely useful when we want to easily access data.

Let's take a look at an example where it would be helpful to associate keys with values to easily access data.







Let's say we are developing a fantasy football website. Using a regular array, we would store each player's info like so:

    var player = ["Aaron", "Rodgers", 12, 32];







There are only a handful of values in this array, but there is no context for any of them.

    var player = ["Aaron", "Rodgers", 12, 32];







Is 12 the number of touchdowns that player has scored? The number of years he's played in the NFL?

    var player = ["Aaron", "Rodgers", 12, 32];







It's difficult to tell because we have no clear references for each data point.

    var player = ["Aaron", "Rodgers", 12, 32];







Take a look at how we could represent the player with an object. Don't worry about syntax for now, we'll cover that in the next lesson. Just use the following example to get a feel for how to associate keys with values.

    var player = {
      firstName: "Aaron",
      lastName: "Rodgers",
      jerseyNumber: 12,
      age: 32
     }







By associating keys with values, we can more accurately represent our player object.

Now, we know at a glance what 12 is — our player's jersey number!



![](http://circuits-assets.generalassemb.ly/prod/asset/4562/aaron.png)

<small style="color:gray">(Source: ESPN)</small>







Objects serve two main purposes in JavaScript:

1.  They act as a simple, structured data store. And, while they are similar to arrays, they access values using keys instead of indices.

3.  They provide a fundamental programming paradigm that helps us structure and categorize code. We'll explore this programming paradigm, known as Object Oriented Programming, later in this lesson.







In JavaScript, every physical thing can be represented as an object.

For example, if we’re working on an airline booking site, we can represent how many seats are both open and booked on any given flight.

![](http://circuits-assets.generalassemb.ly/prod/asset/4577/Delta-Slide_20.png






On the airline site, we can also represent the customers booking those seats as objects, each with a first and last name, country of residency, birthdate, and so on.

Each object can also have its own **properties** and **methods**.

First, let’s explore properties.







**Properties** are characteristics associated with an object.

If a variable is part of an object, it becomes a property. In other words, properties tell us about an object.







Let’s look at another example:

If you were to describe a motorcycle, you might include its color, make, model, max-speed and year.

Each property has a name and a value, and each name/value pair tells us something about that individual object.

![](http://circuits-assets.generalassemb.ly/prod/asset/4563/Slide-20-Chart.svg






As we said earlier, objects have properties and methods. Let’s now focus on methods.

If a function is part of an object, it becomes a **method**.

Methods are used to represent how people interact with an object in the real world. In other words, **methods** are the actions that can be performed on objects.







We can use methods to:

1.  Retrieve the values of an object's properties to find out something about that object.

3.  Update the values of an object's properties.







Consider our motorcycle example. The following actions are common ways that humans interact with motorcycles:

We can use methods to retrieve the values of an object's properties (such as the motorcycle’s model) or change its properties (such as when we start, stop, brake, or accelerate our bike).

![](http://circuits-assets.generalassemb.ly/prod/asset/4518/Slide-23-Chart.svg






In Lesson 2, we'll take a look at how to actually create objects and add their properties and methods.

But first, let’s dive into Object-Oriented Programming (OOP)!







One of the most useful ways of breaking down large problems in code is thinking of them as smaller, simpler problems.

To do so, we need to consider the world and our representation of it in code as a collection of objects interacting with one another.

If we consider everything in terms of objects, we have a powerful tool for organizing both our code and our thoughts.







When you work with HTML elements in JavaScript (JS), you will work with them as JS objects. (We’ll learn more about converting HTML elements into objects in the next unit).

Here's a reminder of what an HTML element looks like:

    Hello

Let's look at how we can work with objects in JavaScript.







As a programming language, JavaScript is oriented around objects.

This is called **Object-Oriented Programming**, or OOP. The following video explains **OOP** in more detail.







As you’ve seen in the video, object-oriented programming models (“objects") are given functionality ("methods") that allow them to perform various actions.

Basically, each object can also hold information.







In OOP, each object can receive messages, process data, and send messages to other objects. Each object can be considered an independent little machine with a distinct role or responsibility.

![](http://circuits-assets.generalassemb.ly/prod/asset/4519/Slide-29-Robots.svg)







OOP promotes greater flexibility and maintainability in programming, and is widely popular in large-scale software engineering.

Because OOP emphasizes modularity, it is easier to develop and understand. It also promotes more direct analysis and synthesis of complex situations and procedures than less modular programming techniques.







The fundamental unit in OOP is an object, which can contain other objects in itself.

It’s a lot like a Russian Matryoshka nesting doll.

![](http://circuits-assets.generalassemb.ly/prod/asset/4520/Slide-30-Russian-Dolls.svg






To understand OOP a little more clearly, let’s consider this real-world scenario:

A user browses a shopping website in search of size 8 shoes. She examines several pairs before deciding which one to purchase.

Our user will need several key details from the website in order to complete the purchase.




![](http://circuits-assets.generalassemb.ly/prod/asset/4566/vans.jpg






The website needs to store the item name ("Vans Checkered Sneakers"), the item color ("black and white”), and the product SKU (234234239).

Additionally, the user will have to select the correct size (8).



![](http://circuits-assets.generalassemb.ly/prod/asset/4521/Slide-33-Chart.svg)







Once the shopper has selected shoes to purchase, he or she will want to add those shoes to the site’s shopping cart.

Anytime we want to associate verbs like “add” with our objects while coding, methods come in handy.



![](http://circuits-assets.generalassemb.ly/prod/asset/4522/Slide-34-Chart.svg)







If we’re coding the website for the shoe store, it’s likely we will also need shopping cart objects that hold information about our shoppers.

Possible object options include the shopper's ID number, the items in his or her shopping cart, and the total cost of the purchase.



![](http://circuits-assets.generalassemb.ly/prod/asset/4523/Slide-35-Chart.svg)







We can also add methods associated with our shopping cart.

Think of the verbs you might use to describe a shopping experience. To purchase the items in the shopping cart, we could add a method using functions.



![](http://circuits-assets.generalassemb.ly/prod/asset/4524/Slide-36-Chart.svg)







In this lesson, we looked at how we can use objects to store key/value pairs. This allows us to store information in a way that closely resembles real-world objects.







We also covered why arrays can be problematic. For example, say we wanted to store a user's information using an array like this:

    var user = ['Damien', 'Lee', 26, 'Web Developer'];

Here, we store values in an ordered list. If we wanted to access a certain value, such as Damien's last name, we would have to know at which position, or index, we could find that value:

    user[1]







We also found out that, by using an object to store our user information instead of an array, we can give these values context with a key.







We'll dig into writing objects in the next lesson, but, for now, take a look at the object below, and see how each key is associated with a value.

For example, we know that our user's first name is `Damien`:

    var user = {
      firstName: 'Damien',
      lastName: 'Lee',
      age: 26,
      profession: 'Web Developer'
    }







With objects, we can look up our user's last name and access it by simply using a key instead of having to know an exact index number.  
Check out below at how we can find our user's last name using the `.lastName` key instead of an index number:

    var user = {
      firstName: 'Damien',
      lastName: 'Lee',
      age: 26,
      profession: 'Web Developer'
    }

    user.lastName  => 'Lee'

See how natural the syntax is for our objects? We now have an easier way to look up any values that we need!







In the next lesson, we'll dig into:

*   How to write objects with properties and methods,
*   How to access, add and update properties and methods.

Are you ready?







We kicked off this unit with a look at how objects can be used to connect keys with values in JavaScript. If you remember, we saw how each object can also have its own associated properties and methods.

Now, let’s explore how we can add properties and methods when creating objects.







First, we’ll learn how to create an object using **literal notation**.

Much like we write normal arrays using square brackets `[ ]`, we write an object — or associative array — using curly braces `{ }`.

Key-value pairs (properties and methods) are separated by commas `,`, just like individual values are in a normal array.

Within each of these pairs, keys are separated from their values by colons `:`.







Let's say we want to create objects for several popular superheros, starting with Superman.

We might want to add some properties for Superman — firstName, lastName, and superheroName.

We might also want to add a method to our Superman object — revealIdentity, which will return Superman's real first and last name (`Clark` and `Kent`), followed by his superhero name (`Superman`).




![](http://circuits-assets.generalassemb.ly/prod/asset/4526/Slide-5-Superman.svg)






Here's how we would write this object using literal notation:

    var superman = {
      // Properties
      firstName: "Clark",
      lastName: "Kent",
      superheroName: "Superman",

      // Methods
      revealIdentity: function() {
        return this.firstName + " " + this.lastName + " is " + this.superheroName;
      }
    };





Let’s look at the syntax breakdown:

    var superman = {
      // Properties
      firstName: "Clark",
      lastName: "Kent",
      superheroName: "Superman",

      // Methods
      revealIdentity: function() {
        return this.firstName + " " + this.lastName + " is " + this.superheroName;
      }
    };

*   Our object is contained within curly braces `{ }`
*   We are storing our object in a variable, called `superman`
*   We separate each key from its value using a `:`





Let’s look at the syntax breakdown:

    var superman = {
      // Properties
      firstName: "Clark",
      lastName: "Kent",
      superheroName: "Superman",

      // Methods
      revealIdentity: function() {
        return this.firstName + " " + this.lastName + " is " + this.superheroName;
      }
    };

*   To add a property, we use a property name, such as `firstName`, `lastName`, or `superheroName`, followed by a `:`, followed by the corresponding value: `'Clark'`, `'Kent'`, or `'Superman'`.





Let’s look at the syntax breakdown:

    var superman = {
      // Properties
      firstName: "Clark",
      lastName: "Kent",
      superheroName: "Superman",

      // Methods
      revealIdentity: function() {
        return this.firstName + " " + this.lastName + " is " + this.superheroName;
      }
    };

*   To add a method, we would use the method name `revealIdentity`, followed by a `:`, followed by an anonymous function (`function ()`).






Here are some important concepts to note:

1.  As you may have noticed while examining object oriented code, we often run into the keyword `this`. We’ll cover `this` in more detail later on. But, for now, know that, in the context of our objects, `this` is used in place of the object name to refer to the current object instance.

3.  We separate each key-value pair (properties and methods) using a comma. But, similar to arrays, we don't include a comma after the last property.







Back to our Superman example:

Within the function, we can use the `this` keyword to access different properties for our object.

For example, we can use `this.firstName` to access the value for the `firstName` property (in this case, 'Clark').







Let's practice!

1.  Create an object called `currentlyReading`
2.  Add the following properties to the object:

*   Title: The Wind-Up Bird Chronicle
*   Author: Haruki Murakami
*   Year: 1994
*   Rating: 4.2

Click through to the next slide to see the answer.







Did your code look like this?

    var currentlyReading = {
      title: "The Wind-Up Bird Chronicle",
      author: "Haruki Marukami",
      year: 1994,
      rating: 4.2
    };



![](http://circuits-assets.generalassemb.ly/prod/asset/4527/Slide-11-haruki-murakami-book.jpg)







Great! You’ll have a chance to keep practicing this later on.

Now, let’s turn to accessing properties.







We can get and set object properties using either **dot notation** or **square bracket syntax**.







**Dot notation** is common for simple scenarios.

Remember the syntax we used in Unit 1 to find out the length of an array?

    var fruits = ["blueberries", "strawberries", "apples"];
    fruits.length => 3

By using our array name, followed by `.length`, we were able to access the length property of our array.

This is the dot `.` notation.




![](http://circuits-assets.generalassemb.ly/prod/asset/4528/Slide-12-Fruit.svg)







We can access values using the object name, followed by a period `.`, followed by the name of the property we want to access.







Here, we've created the variables `heroFirstName` and `heroLastName` to store the information we want to retrieve.

    var heroFirstName = superman.firstName;   => 'Clark'
    var heroLastName = superman.lastName;   => 'Kent'

![](http://circuits-assets.generalassemb.ly/prod/asset/4526/Slide-5-Superman.svg)







We can also update values using dot notation.

To do so, we use the name of the object (in this case, `superhero`), followed by the name of the property we want to update (in this case, `.firstName` or `.lastName`).

We then use the assignment operator (`=`), followed by the new value.

    superhero.firstName = 'Susan';
    superhero.lastName = 'Storm';







Let’s learn more about adding properties.

The syntax we use to update a property can also add a new one. If the property we are trying to update doesn't yet exist, it will be added automatically.

    superhero.favoriteFood = 'Beef Bourguignon';

We've now added a new favorite food for Superman!






![](http://circuits-assets.generalassemb.ly/prod/asset/4529/Slide-15-Superman-Beef.svg)







# Let's practice!

Consider the following object:

    var pet = {
      species: 'iguana',
      gender: 'female',
      age: 12,
      name: 'Godzilla'
    };

What code could we write to retrieve the value for `name` from the object and store this value in a variable name?

Answer: `var name = pet.name;`



![](http://circuits-assets.generalassemb.ly/prod/asset/4530/Slide-16-Lizard.svg)

Type your answer below: `var pet = {species:'iguana',gender:'female',age:12,name:'Godzilla'}







# Let's practice!

Consider the following object:

    var pet = {
      species: 'iguana',
      gender: 'female',
      age: 12,
      name: 'Godzilla'
    };

Now, how would you assign `13` as the value for `age`?

Answer: `pet.age= 13;`



![](http://circuits-assets.generalassemb.ly/prod/asset/4530/Slide-16-Lizard.svg)

Type your answer below: `var pet = {species:'iguana',gender:'female',age:12,name:'Godzilla'}







# Let's practice!

Consider the following object:

    var pet = {
      species: 'iguana',
      gender: 'female',
      age: 12,
      name: 'Godzilla'
    };

How would you add a new property, `'favoriteFood'` using the value `'crickets'`?

Answer: `pet.favoriteFood = 'crickets';`



![](http://circuits-assets.generalassemb.ly/prod/asset/4530/Slide-16-Lizard.svg)

Type your answer below: `var pet = {species:'iguana',gender:'female',age:12,name:'Godzilla'}







Let's go back to our superhero example.

To access values, we can also use **square bracket syntax** to access and update the properties for an object.

    var heroFirstName = superman['firstName'];   => 'Clark'
    var heroLastName = superman['lastName'];   => 'Kent'







Once again, the name of our object is `superman`, followed by the property name, contained within quotes and square brackets.

The square bracket syntax is commonly used when a variable name is used in place of a property name:

    var propertyName = 'firstName';
    var supermanFirst = superman[propertyName];   => 'Clark'







Dot notation can only work with the exact literal name of the property since you can’t type something like superman.’firstName’ or superman.yourVariableName, while the square brackets allow for substituting in the value of a string or variable in place of the property name.

    var propertyName = 'firstName';
    var supermanFirst = superman[propertyName];   => 'Clark'







Let’s update the `firstName` and `lastName` of our object again, but use the square bracket syntax this time:

    superman['firstName'] = 'Susan';
    superman['lastName'] = 'Storm';

As with dot notation, we use the name of the object, followed by the property name wrapped in quotes and square brackets (`[ ]`). Next, we use the assignment operator (`=`), followed by the new value.







Now you try! Let's return to our pet, Godzilla. ![](http://circuits-assets.generalassemb.ly/prod/asset/4530/Slide-16-Lizard.svg)







# Let's practice!

Consider the following object:

    var pet = {
      species: 'iguana',
      gender: 'female',
      age: 12,
      name: 'Godzilla'
    };

How would you retrieve the value for `'name'` from the object, and store this value in a variable name using square bracket syntax `[ ]`?

Answer: `var name = pet['name'];`



![](http://circuits-assets.generalassemb.ly/prod/asset/4530/Slide-16-Lizard.svg)

Type your answer below: `var pet = {species:'iguana',gender:'female',age:12,name:'Godzilla'}







# Let's practice!

Consider the following object:

    var pet = {
      species: 'iguana',
      gender: 'female',
      age: 12,
      name: 'Godzilla'
    };

How would you assign `13` as the value for `'age'` using square bracket syntax `[ ]`?

Answer: `pet['age'] = 13;`



![](http://circuits-assets.generalassemb.ly/prod/asset/4530/Slide-16-Lizard.svg)

Type your answer below: `var pet = {species:'iguana',gender:'female',age:12,name:'Godzilla'}







# Let's practice!

Consider the following object:

    var pet = {
      species: 'iguana',
      gender: 'female',
      age: 12,
      name: 'Godzilla'
    };

How would you add a new key, `'favoriteFood'`, with value `'crickets'` using square bracket syntax `[ ]`?

Answer: `pet['favoriteFood'] = 'crickets';`



![](http://circuits-assets.generalassemb.ly/prod/asset/4530/Slide-16-Lizard.svg)

Type your answer below: `var pet = {species:'iguana',gender:'female',age:12,name:'Godzilla'}







Excellent! Now, let’s discuss how we can use the `delete` operator to remove a property from our object.

Here's what the syntax for deleting a property looks like (using the dot notation or the square bracket syntax):

    delete object.property      // Dot notation
    delete object['property']   // Square bracket syntax







Here’s an example:

    var superman = {
      // Properties
      firstName: "Clark",
      lastName: "Kent",
      superheroName: "Superman",

      // Method
      revealIdentity: function () {
        return this.firstName + " " + this.lastName + " is " + this.superheroName;
      }
    };

Dot Notation: `delete superman.firstName;`  
Square Bracket Notation: `delete superman['firstName'];






Lastly, let’s talk about accessing methods. We will use **dot notation** to access methods for our objects.





![](http://circuits-assets.generalassemb.ly/prod/asset/4531/Slide-29-Clark-Kent.svg)

If we wanted to access — or call, our `revealIdentity` method — we could do so using the following syntax:


            var supermanIdentity = superman.revealIdentity(); => 'Clark Kent is Superman'




![](http://circuits-assets.generalassemb.ly/prod/asset/4531/Slide-29-Clark-Kent.svg)

Here, we use the object name `superman`, followed by a period, followed by the method name, followed by parenthesis.


            var supermanIdentity = superman.revealIdentity(); => 'Clark Kent is Superman'




![](http://circuits-assets.generalassemb.ly/prod/asset/4531/Slide-29-Clark-Kent.svg)

We are saving the value that is returned in a variable, `supermanIdentity`, so we can reference it later.


            var supermanIdentity = superman.revealIdentity(); => 'Clark Kent is Superman'






In this lesson, we learned how we can create objects and add properties and methods to those objects using literal notation.

We also discussed how object literal notation is very useful, easy, and popular for quickly creating objects.







We now know how to use dot notation or square bracket syntax to access, update, and add properties to our objects.

Although dot notation is often a popular method, as it’s slightly easier to write out, we'll need to use square bracket syntax anytime we are generating our property names dynamically, i.e. when we want to use a variable for a property name.







In the next lesson, we'll look at how we can use constructor notation to create a "template" for creating multiple objects that represent similar things.







There might be instances where we want to create multiple objects to represent similar things.

For example, if we built a superhero fan site, we’d want to store similar information for a range of superheroes: first name, last name, superhero name, etc.

To do this, we can create a "template" object that contains any properties and methods we want to add for each superhero.



![](http://circuits-assets.generalassemb.ly/prod/asset/4536/Slide-3-Superhero-Fan-Site.svg)







We create object templates with a function called a constructor.

Constructor notation can be used to:

1.  Create a single, empty object.
2.  Create multiple instances of similar objects.







First, let's first take a look at how we can create a single, empty object using constructor notation.







Take a look:

    var superman = new Object();

Here, we save our object to the variable `superman`.

Then, we create the new object by using the `new` keyword followed by the object constructor.







The result is an empty superman object. It doesn't have any associated properties or methods yet, so we need to add them.

![](http://circuits-assets.generalassemb.ly/prod/asset/4537/Slide-6-Superman.svg)







We can add properties to our object using either the dot notation (`.`) or square bracket syntax (`[ ]`).

    superman.firstName = 'Clark';
    superman.lastName = 'Kent';
    superman.superheroName = 'Superman';







We can add methods to our objects using the dot notation:

    superman.revealIdentity = function () {
    return this.firstName + " " + this.lastName + " is " + this.superheroName;
    };







We can also access and update properties using either the dot notation or square bracket syntax, just like we did with our object literals:

    // Accessing Values
    var heroFirst = superman.firstName;

    // Updating Values
    superman.firstName = 'Bill';
    superman['superheroName'] = 'Super Duper Man';







# Let's Practice!

1.  Create an object `currentlyListening`
2.  Add the following properties to your object:

*   The `album` is "Wild Honey"
*   The `artist` is "The Beach Boys"
*   The `releaseDate` is 1967
*   The `label` is "Capitol Records"



Type your answer below:

Click through to the next slide to see the answer.







There are several correct ways to create the object `currentlyListening`, using either the dot notation or the square bracket syntax.

Let's take at look both.







    var currentlyListening = new Object();
    currentlyListening.album = "Wild Honey";
    currentlyListening.artist = "The Beach Boys";
    currentlyListening.releaseDate = 1967;
    currentlyListening.label = "Capitol Records";

Or:

    var currentlyListening = new Object();
    currentlyListening["album"] = "Wild Honey";
    currentlyListening["artist"] = "The Beach Boys";
    currentlyListening["releaseDate"] = 1967;
    currentlyListening["label"] = "Capitol Records";






![](http://circuits-assets.generalassemb.ly/prod/asset/4538/Slide-10-Beach-Boys-Album.jpg)







Whew! With that under our belt, it’s now time to turn to creating many objects using **constructor notation**.

The real power of constructor notation comes into play when we create multiple objects to represent similar things.







Think about our superhero fan site.

As you’ll recall, we want a way to store similar info for many superheroes: first name, last name, superhero name, etc.

We need to create a "template" object, which contains the properties we want to add for each superhero.







To create this object template, we use a function called a **constructor**.

This is really just a function like any other, but, when you call it in a particular way, JavaScript works its magic.

Let’s see an example of an object constructor function.







Here, we are creating a `Superhero` function. It’s just like creating any other function in JavaScript.

    var Superhero = function () {};







Note that it is convention to capitalize the name of the function when creating an object using constructor notation. We'll take a look at this again in a moment.

    var Superhero = function () {};







Creating an instance of our `Superhero` object is similar to creating a new empty object using constructor notation:

    var clark = new Superhero();
    var bruce = new Superhero();







Here, we save our new objects to the variables `clark` and `bruce`. We use the `new` keyword, similar to when we created a new empty object above. We then use the name of the constructor function `Superhero`, followed by parenthesis `()`.

    var clark = new Superhero();
    var bruce = new Superhero();







Note that the name of a constructor function usually begins with a capital letter — unlike other functions — to remind developers to use the `new` keyword when creating an object using that function.

    var clark = new Superhero();
    var bruce = new Superhero();







The constructor function is called at the moment that our `new` object is **instantiated**.

For example:

    var SuperHero = function () {
      console.log('Superhero instance created');
    };

    var clark = new Superhero(); // console logs "Superhero instance created"
    var bruce = new Superhero(); // console logs "Superhero instance created"

Messages are logged to the console as soon as we create a new instance of our object.







Up until this point, we've set property names manually, for every new object we create.

The point of our objects/constructors is to create blueprints of our data models, so that, when we create a new instance, we can change particular properties instead of resetting all of the object’s keys.







Properties can be set in the constructor so they are set specifically for each instance. In other words, we pass them as parameters in our constructor function.

Take a look at the following example:

    var Superhero = function (firstName, lastName, superheroName) {
      this.firstName = firstName;
      this.lastName = lastName;
      this.superheroName = superheroName;
      this.revealIdentity = function () {
        return this.firstName + " " + this.lastName + " is " + this.SuperheroName;
      }
        console.log('superhero instantiated');
    };







Let's break this down, line-by-line.


![](http://circuits-assets.generalassemb.ly/prod/asset/5108/code0.png)






1\. Overview: We are using a constructor function to create a template for our `Superhero` objects.


![](http://circuits-assets.generalassemb.ly/prod/asset/5109/code1.png)






2\. We pass three parameters, i.e., the property names each superhero will have in common: `firstName`, `lastName`, and `superheroName`.


![](http://circuits-assets.generalassemb.ly/prod/asset/5110/code2.png)






3\. The object properties `firstName`, `lastName` and `superheroName` are then set through the `this` keyword with the value.


![](http://circuits-assets.generalassemb.ly/prod/asset/5111/code3.png)






4\. Within the function, `firstName` refers to the parameter name we passed to the function. Same with `lastName` and `superheroName`.


![](http://circuits-assets.generalassemb.ly/prod/asset/5112/code4.png)






5\. We then add a method for our object, similar to how we've done it in the past. To add a method, we use the method name `revealIdentity`, followed by an equal sign, followed by an anonymous function (a function without a name).


![](http://circuits-assets.generalassemb.ly/prod/asset/5113/code5.png)






6\. Within the function, we use this to access the properties of the instance of the individual object we are creating.


![](http://circuits-assets.generalassemb.ly/prod/asset/5114/code6.png)






Now, we can create as many superheroes as we want using this template. The steps are easy! Let's review.

![](http://circuits-assets.generalassemb.ly/prod/asset/5115/more_code0.png)







1\. Create an instance of our `Superhero` object.

![](http://circuits-assets.generalassemb.ly/prod/asset/5116/more_code1.png)







2\. Use the `new` keyword followed by the name of our constructor function, `Superhero`.

![](http://circuits-assets.generalassemb.ly/prod/asset/5117/more_code2.png)







3\. Pass in three arguments, which are the property values that correspond to the three parameters we passed into our `Superhero` constructor function: `firstName`, `lastName`, and `superheroName`.

![](http://circuits-assets.generalassemb.ly/prod/asset/5118/more_code3.png)







We've now created a new instance of our Superhero object!

![](http://circuits-assets.generalassemb.ly/prod/asset/4550/Slide-19-Charts.svg






We can create as many superheroes as we want using our Superhero constructor function.







We also have a blueprint, or template, of our object. So, in the future, when we create a new instance, we won’t need to reset all the keys.

All we’ll have to do is give values for different properties.


    // We can access properties of our object instances using dot or square bracket notation
      console.log(superman.firstName + ' ' + superman.lastName);
      => 'Clark Kent'






Notice our `revealIdentity` method is also copied over to each individual object.

    // We can also access methods using our new object instances:
    superman.revealIdentity(); => 'Clark Kent is Superman'
    batman.revealIdentity(); => 'Bruce Wayne is Batman'







In this unit, we explored the creation of objects using constructor notation.

We've seen that the real power of constructor notation is that it provides us with a "template" object we can use when creating multiple objects to represent similar things.







Creating objects is now much more scalable than if we used literal notation to create every individual object.

Our code will also be cleaner, as we avoid repetition when creating similar objects.







In the next unit, we'll take a closer look at the `this` keyword.

We'll also learn about JSON (JavaScript Object Notation), a data format similar in syntax to object literals that allows us to send and receive data over a network.







In the last few lessons, we covered how to use the `this` keyword to access properties and methods for our objects.

We also mentioned that `this` is used in place of the object name to refer to the current object instance.







In this lesson, we'll take a closer look at `this` and how it can refer to different things depending on the context.

We'll also look at **JSON** (JavaScript Object Notation), a text-based data format with syntax that closely resembles the objects we've covered thus far. JSON allows us to send and receive data over a network.







`this` is a keyword commonly used inside functions and objects. It can sometimes be tricky to know what `this` refers to, because it refers to different things in different contexts.

Let's take a look:







We’ll start off talking about a function with a global scope.

When a function is created at the top level of a script — meaning it is not defined in an object or inside of another function — it has **global scope** (similar to the variable scope we discussed in the last unit).







In this context, the default object is also considered the **window object**. The window object represents the current browser window or tab. It contains other objects that tell you about the browser.

The window object also contains properties that tell us about the current browser window.

Let's look at some examples!








`window.innerHeight`  
→ Returns the height of browser window



![](http://circuits-assets.generalassemb.ly/prod/asset/4678/Screen_Shot_2016-06-24_at_3.26.40_PM.png)








`window.location`  
→ Current URL



![](http://circuits-assets.generalassemb.ly/prod/asset/4680/Screen_Shot_2016-06-24_at_3.28.48_PM.png)








`window.scrolly`  
→ Returns the distance we've scrolled



![](http://circuits-assets.generalassemb.ly/prod/asset/4679/Screen_Shot_2016-06-24_at_3.26.58_PM.png)







Now, let's see how the window object relates with the `this` keyword.

When `this` is used in a function that is defined in the global scope, `this` refers to the window object.

Here's an example:



    this.innerWidth => Width of browser window

    function windowInfo() {
    //Width of browser window object
       var windowWidth = this.innerWidth;
    //Height of browser window object
       var windowHeight = this.innerHeight;
    }







The first time we use `this`, we are using it in the global scope, as it’s not contained within an object.

The second and third time you see `this`, we are also using it in the global scope. Even though it is contained within a function, it is not a part of any object.

In each of these instances, using `this` is the equivalent of using window.



    this.innerWidth => Width of browser window

    function windowInfo() {
    //Width of browser window object
       var windowWidth = this.innerWidth;
    //Height of browser window object
       var windowHeight = this.innerHeight;
    }







Let’s learn about what happens when a method is contained inside an object. We saw in the last unit that, when a function is defined inside an object, we call it a method.

In a method, `this` refers to the object containing the function.







For example, in the function below, `this` refers to the animal object that contains the function/method `makeNoise`.

    var animal = {
      name: 'Rover',
      species: 'dog',
      breed: 'Golden Retriever',
      noise: 'bark!',
      makeNoise: function () {
        console.log(this.noise);
      }
    }




![](http://circuits-assets.generalassemb.ly/prod/asset/4551/Slide-10-Rover-Bark.svg)







Because `this` refers to the animal object, using it would be the same as writing out:

    console.log(animal.noise);

However, when we create several objects using constructor notation, `this` refers to the individual instance of that object.

Let's look at an example:







    function Pet (name, species, breed, noise)  {
      this.name = name;
      this.species = species;
      this.breed = breed;
      this.noise =  noise;
      this.makeNoise = function () {
        console.log(this.noise);
      }
    }

    var wolfman = new Pet ('wolfman', 'cat', 'Tuxedo Cat', 'meow');
    var rover = new Pet ('Rover', 'dog', 'Golden Retriever', 'bark');






![](http://circuits-assets.generalassemb.ly/prod/asset/4552/Slide-12-Cat-Tux-Meow.svg)







Here, `this` refers to the individual instance of the object we are creating.


    function Pet (name, species, breed, noise)  {
      this.name = name;
      this.species = species;
      this.breed = breed;
      this.noise =  noise;
      this.makeNoise = function () {
        console.log(this.noise);
      }
    }

    var wolfman = new Pet ('wolfman', 'cat', 'Tuxedo Cat', 'meow');
    var rover = new Pet ('Rover', 'dog', 'Golden Retriever', 'bark');






So, when we create our wolfman object, `this` will refer to the wolfman object and `this.noise` will return `'meow'`.


    function Pet (name, species, breed, noise)  {
      this.name = name;
      this.species = species;
      this.breed = breed;
      this.noise =  noise;
      this.makeNoise = function () {
        console.log(this.noise);
      }
    }

    var wolfman = new Pet ('wolfman', 'cat', 'Tuxedo Cat', 'meow');
    var rover = new Pet ('Rover', 'dog', 'Golden Retriever', 'bark');






When we create our rover object, `this` will refer to our rover object, and `this.noise` will return `'bark'`.


    function Pet (name, species, breed, noise)  {
      this.name = name;
      this.species = species;
      this.breed = breed;
      this.noise =  noise;
      this.makeNoise = function () {
        console.log(this.noise);
      }
    }

    var wolfman = new Pet ('wolfman', 'cat', 'Tuxedo Cat', 'meow');
    var rover = new Pet ('Rover', 'dog', 'Golden Retriever', 'bark');






Test yourself! See if you can guess what `this` refers to in the following situations.







    function Pet (name, species, breed, noise)  {
      this.name = name;
      this.species = species;
      this.breed = breed;
      this.noise =  noise;
      this.makeNoise = function () {
        console.log(this.noise);
      }
    }

    var batman = new Pet ('Batman', 'bird', 'parrot', 'chirp');

When we create our batman object, what will `this` refer to? What will be logged to the console from within the `makeNoise` method?:

`console.log(this.noise);`

Take a moment to consider your answer. Then, click through to the next slide to see how you did.







    function Pet (name, species, breed, noise)  {
      this.name = name;
      this.species = species;
      this.breed = breed;
      this.noise =  noise;
      this.makeNoise = function () {
        console.log(this.noise);
      }
    }

    var batman = new Pet ('Batman', 'bird', 'parrot', 'chirp');

Answer:  
`this` will refer to `batman`.  
`this.noise` will return `‘chirp’`.







    var paintbrush = {
      tool: 'paintbrush',
      brand: 'Winsor & Newton',
      price: 12.23,
      pattern: 'zig zag',
      drawShape: function () {
        console.log(this.pattern);
      }
    }

What does `this` refer to within the `drawShape` method? What will be logged to the console?

Answer: `this` refers to `‘paintbrush’`. The console will log: `‘zig zag’`.







We'll end this unit with **JSON**.

[JSON](http://json.org/) (JavaScript Object Notation) is a lightweight, text-based data format that's based on JavaScript.

Because it's text—and looks like JavaScript—JSON is both easy for us to read and write AND easy for programs to parse and generate.




![](http://circuits-assets.generalassemb.ly/prod/asset/4553/Slide-15-JSON.svg)







JSON is completely language-independent, but it uses conventions familiar to programmers of the “C” family of languages, including C, C++, C#, Java, JavaScript, Perl, Python, and many others.

These properties make JSON an ideal language for data interchange.







The JSON syntax closely resembles the object literal notation we met earlier in this unit.  
However, it’s not an object — just plain text data.

We cannot transfer actual objects over a network, so we send text, and the receiving browser converts this text into objects.







We use JSON to transfer data between applications and JavaScript.

To keep everything consistent, all JSON code must follow a number of strict conventions (stricter even than normal JavaScript!) in order to be syntactically correct. Take a look:

    {
      "name": "Sasha Li",
      "occupation": "Web Developer",
      "location": "San Francisco",
      "age": 43
    }







JSON rules include:

*   Property names must be double-quoted strings (not single quotes).
*   Trailing commas are forbidden.
*   Leading zeros are prohibited.
*   In numbers, a decimal point must be followed by at least one digit.
*   Most characters are allowed in strings; however, certain characters (such as `'`, `"`, `\`, and newline/tab) must be “escaped” with a preceding backslash (`\`) in order to be read as characters (as opposed to JSON control code).
*   All strings must be double-quoted.
*   No comments allowed!







We’ll take a look at how we can send and receive JSON data later on, but, first, let's see how we can convert our JavaScript objects into a JSON format that’s ready to send to an outside application.







We mentioned before that, although JSON looks like our object literals, it is just plain text data and not an object.







If we want to send JavaScript objects from a browser to another application, we can use `JSON.stringify()` to convert our objects into JSON format.

Check out our JavaScript object:

    var favoriteMovie = {
      title: 'Thelma and Louise',
      director: 'Ridley Scott',
      year: 1991,
      imdb: 7.4
    }







Here, we call `JSON.stringify()`, passing in our object, `favoriteMovie`, as a parameter. We store the results back in the `favoriteMovie` variable.



    favoriteMovie = JSON.stringify(favoriteMovie);
      // Our favoriteMovie variable now holds a JSON string:
      {
        "title": "Thelma and Louise",
        "director": "Ridley Scott",
        "year": 1991,
        "imdb": 7.4
      }







Our `favoriteMovie` object now holds a JSON string that can be sent from the browser to another application.

We'll dive into how we can send JSON `this` a bit later.



![](http://circuits-assets.generalassemb.ly/prod/asset/4555/Slide-22-thelma-and-louise-movie.jpg)







Now let’s talk about converting JSON to JavaScript objects.







We can use `JSON.parse()` to process a string containing JSON data. The action converts the JSON data into a JavaScript object.

Here's what that looks like:

    var favoriteMovie = {
      "title": "Thelma and Louise",
      "director": "Ridley Scott",
      "year": 1991,
      "imdb": 7.4
     }







We call `JSON.parse()` to process the string and convert it into a JavaScript object.

    favoriteMovie = JSON.parse(favoriteMovie);

Our `favoriteMovie` variable now holds a JavaScript object:

    var favoriteMovie = {
         title: 'Thelma and Louise',
         director: 'Ridley Scott',
         year: 1991,
         imdb: 7.4
    }







Our `favoriteMovie` variable now holds a JavaScript object we can manipulate.

There will also be instances in which we receive JSON data from an outside application and will want to convert it into an object so that we can work with it in our application.

We’ll cover this in a later unit.







In this lesson, we learned how we can use the `this` keyword to access properties and methods within our objects.

We've seen that what `this` refers to may change depending on context. When we use `this` inside an object, it refers to the individual instance of that object. `this` is particularly useful when using the constructor notation as a template for creating many similar objects.







We also learned about JSON, a text-based data format with a syntax that closely resembles the literal notation of objects.

We can now convert our objects into JSON format, and convert our JSON into JavaScript objects.

This will come in handy when we cover how to send and receive data.





<a name="conclusion"></a>
## Conclusion (# mins)
- Review independent practice deliverable(s)
- Recap topic(s) covered in today's lesson
- Cover homework and/or upcoming tasks

***

### BEFORE NEXT CLASS
|   |   |
|---|---|
| **HOMEWORK** | Example Assignment [#](Instructions)  |
| **UPCOMING PROJECTS**  | Project Assignment: Title [#](Instructions)  |

### ADDITIONAL RESOURCES
- Exercises
- Videos
- Readings
- Decks

> Instructor Note: When possible, provide a brief description of Additional Resources, classifying whether it is for advanced or beginner students.  
