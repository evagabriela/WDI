---
title: Mastering Control Flow
duration: "1:25"
creator:
    name: John Doe
    city: NYC


---
# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Mastering Control Flow (90 mins)

| Timing | Type | Topic |
| --- | --- | --- |
| x min | [Introduction](#introduction) | Topic |
| x min | [Demo/Codealong](#demo) | Topic |
| x min | [Guided Practice](#guided-practice) | Topic |
| x min | [Independent Practice](#ind-practice) | Topic |
| x min | [Conclusion](#conclusion) |Topic |

### LEARNING OBJECTIVES
*After this lesson, you will be able to:*
- Differentiate between true, false, 'truth-y', and 'false-y'
- Use if/else if/else conditionals to control program flow based on boolean conditions
- Use switch conditionals to control program flow based on explicit conditions
- Use comparison operators to evaluate and compare statements
- Use boolean logic (!, &&, ||) to combine and manipulate conditionals

### STUDENT PRE-WORK
*Before this lesson, you should already be able to:*
- Create variables in JavaScript
- Differentiate between data types (strings, numbers, booleans)
- Use a text editor

---
<a name="opening"></a>
## Opening (5 mins)
- Review pre-work, projects, or exit ticket, if applicable
- Review current lesson objectives
- Reference general course content or topics (e.g. code or concepts that have been used across multiple lessons)
- Include Hook / Real-world Relevance (why the content from this lesson is useful or important)

What is control flow? Watch this [video](https://generalassembly.wistia.com/medias/zhahjd0c7t) to discover more about the role control flow plays in development.

JavaScript supports a compact set of statements, specifically control flow statements, that you can use to incorporate a great deal of interactivity in your application.

<a name="comparison-logical"></a>
## Introduction: Comparison and Logical Operators (10 mins)


#### Intro to Conditions
Comparison and logical operators are useful in JS because they help us compare different conditions to one another.

**Conditions** are usually made up of a mathematical statement that uses an operator (the signs that allow us to make the comparison, such as equals, less than, or greater than).

Conditions are statements that make comparisons that evaluate to true or false in order to control the flow of the program.

Take a look:

```js
if (score > 50) {
  console.log("Congrats! You've passed this level.")
}
```

Here the condition is the comparison that is within the parentheses:

```js
score > 50
```

#### How Conditions Are Used
When information is incorrect, JavaScript can help identify the comparison as false.

So if you're filling out a form that requires your birthday, you can't say you were born in the year 2045 because that year hasn't occurred yet.

You also can't say that you were born on December 45th, because that day doesn't exist.

When you try entering information like this, JS will identify that it is wrong by comparing the information you entered against information it knows to be accurate.

<img src="assets/Slide-5-Form-X.png" width="300px">

Making comparisons is almost like asking questions about the information the user has entered.

Is the year less than or equal to 2016 and more than or equal to 1900? If the answer to this question is "true," then we know the user has entered a valid year, and that he or she was born somewhere between 1900 and 2016.

<img src="assets/Slide-6-Form-Check.png" width="300px">

Did you notice how we used the term "less than or equal to" to check, or compare, two things? This is how our comparison operators help us make decisions.



## Guided Exercise: Comparison Operators (15 mins)

Comparison operators are binary in that they compare two values against one another and return a boolean value — either true or false.

Comparisons in JavaScript can be made using <, >, <=, and >=, and work for both strings and numbers.

<img src="assets/comparison_operators.png" width="350">

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

<img src="assets/equality_operators.png" width="350px">

#### `==` Equals Operator

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

Because JS tries to change an expression so that both types are equal, it's easier for expressions to return true. If we're not careful, this can cause some unexpected (and unwelcome) behavior.

#### The Strict Equals Operator `===`

To avoid type coercion and ensure stricter comparisons, use the triple equals operator, also known as the Strict Equality Operator (===).

The === operator checks to make sure the type and the value on both sides of the === are the same.


Now, let's take a closer look at the answers:

<img src="assets/strict_equals.png" width="500px">

The double equals signs (==) can be useful when both the type and value are the same, but, because their type coercion could potentially derail your program, they're best avoided when you're just getting started out.

By sticking to the === operator, we can ensure that we are checking both the type and the value.

#### The Not Equals Operator `!==` and `!=`
Now, what do we do if we want to check and see if two values are not equal to one another?

These areWe use the inequality operators (`!=` and `!==`).

The `!=` operator checks to see if two values are not equal to one another. Similar to the `==` operator, it performs type coercion before checking the two values against one another.

The `!==` compares two values to one another without performing type coercion, so both the values and the types are compared.

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
The console returns false.
7 !== 7
The console returns false.
7 !== “7”
The console returns true.
0 !== false
The console returns true.
false !== “false”
The console returns true.
 -->



## Logical Operators (5 mins)
Finally, let’s have a look at *logical operators*. The logical operators are NOT, OR, and AND.

We can use these to combine several boolean statements into a single statement.

For instance, if it is raining **AND** I have an umbrella, then I will go outside with an umbrella.

BOTH conditions have to evaluate to true for the entire expression to be true.

<img src="assets/umbrella.png" width="250px">

Logical operators let us check to see if two conditions are both true or if _at least one_ of the conditions is true.

We can also use logical operators to reverse a value or check to see whether or not something is false.

<img src="assets/logical_operators.png" width="200px">

<br>
NOT (`!`) will reverse the value of any Boolean (i.e, `!true` `// false`).

OR (`||`) takes in two boolean arguments; if at least one is true, then it will evaluate to true. But, if both are false, it will evaluate as false.

AND (`&&`) also takes in two boolean arguments; however, it will only evaluate as true if both of the arguments are true. Otherwise, it will evaluate to false.


For example, let’s assume that a = 5, b = 10, and c = 8.

Is the following condition true?

```js
a < b && a < c

```

Yes. 5 is less than 10 AND 5 is less than 8.

Once we check multiple conditions to see if they’re true, we can do something with the results.

## Truthy and Falsey (15 mins)
Like most computer languages, JavaScript supports Boolean values, or True/False values.

Everything in JavaScript — from the strings we learned about in Unit 1 to the null and undefined values we just covered — has an inherent Boolean value, generally known as either _truthy_ or _falsey_.

#### Truthy
Something is truthy when it evaluates to True. In JavaScript, truthy values include:

- Strings
- Non-zero numbers
- True

#### Falsey
Something is Falsey when it evaluates to False. The "falsey" category of values includes:

- False
- 0 (zero)
- "" (empty string)
- Null
- Undefined
- NaN (a special Number value meaning Not-a-Number!)


#### Summary
Below are the exact rules Boolean operators follow when dealing with non-Boolean input values.

<img src="assets/falsey_truthy.png" width="500px">

The best way to determine if something is truthy is to determine that it’s not falsey.

As you saw in the table, there are six Falsey values in JS:

`undefined`, `null`, `NaN`, `0`, `""` (empty string), and `False`, of course.
<br>
<br>
#### Logical Operators and truthy/falsey values
Earlier, we looked at the logical operators NOT(`!`), OR (`||`), and AND (`&&`).

These operators accept inputs with data types such as strings and numbers.

When operators accept input values, they categorize these inputs as being either "falsey" or "truthy."

The boolean operators `!`, `||`, and `&&` follow a set of rules that determine how they behave.

- NOT(`!`): If the input is truthy, return `false`; if the input is falsey, return `true`.
- OR (`||`): Return the first truthy value; if both values are Falsey, return the last falsey value.
- AND `(&&):` Return the first falsey value; if both values are truthy, return the last truthy value.

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


#### Exercise

Can you predict how the following expressions will be evaluated?

Try typing each expression into your console in Chrome.


<!--
ID NEEDED: Help formatting the following exercise
!('')
The console returns true.
false && undefined
The console returns false.
true && !0
The console returns true. -->



<!-- @sarahholden Insert video: Truthy and falsey -->

Let's review the concept of truthy and falsey by watching this short [video](https://generalassembly.wistia.com/medias/jdz1fp4ys8)


## Conditional Statements (25 mins)

Now we’re going to learn a bit more about conditional statements and how we can use them to control the flow of a program.

Take a look at this short [video](https://generalassembly.wistia.com/medias/afk2hatfe0) that describes how conditional statements tie in with the material we just covered.

We can use a conditional statements to skip over a block of code if it does not pass a boolean expression.

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

#### `if...else` statements

Let’s start by looking at `if...else` statements.

As you may have guessed from its name, the first component of the `if...else` statement is the *if statement*.

An *if statement* allows us to check whether or not a condition is true and, if it is, run our code.

The conditional below is an `if` statement.

An `if` statement will take in a condition and, if that condition is truthy, run whatever code you specify.

<img src="assets/condition_zoom.png" width="400px">

#### Flow Charts
You're probably already familiar with a common real-world application of the `if` statement: the *flow chart*.

A *flow chart* is a visual diagram that tells us how to behave depending on a certain set of conditions.

<img src="assets/flow_chart.png" width="500px">

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

<img src="assets/flow_chart_1.png" width="300px">

#### Else If Statements
Adding an `else` to our `if` statement allows us to specify a second condition to test.

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

We can add as many `else if` statements as we want. You just keep tacking them on.

These statements allow us to add complex logic to our program, which can check for multiple conditions and specify an action for each result, making our program seem more intuitive and user friendly.

<img src="assets/else_if.png" width="250px">

#### Else Statements

At this point, if none of the conditions we check for are true, then nothing will happen.

We need a way to check several conditions and have the ability to move forward if none of these conditions are true — a default, or fallback, course of action.

To specify behavior for this outcome, we must add an `else` to the end of our statement.

Let's look at an example of an else statement:

<img src="assets/Slide-25-If-Else.png" width="600px">


#### Exercise

Imagine you work the information booth at a theme park and help recommend rides to guests.

If a person is less than 8 years old, recommend the merry-go-round.

Else if a person is more than 8 years old and less than 65 years old and more than 4.5 feet tall, recommend the roller coaster.

Else recommend the lazy river.

Try typing this out in your console.

Sample solution:

```js
var age = 25;
var height = 5;
if (age <= 8) {
  console.log("Check out the Merry-Go-Round. You'll love it!");
} else if (age > 8 && age < 65 && height > 4.5) {
  console.log("Check out the Roller Coaster. It's awesome!");
} else {
  console.log('Why not enjoy a float down the Lazy River?');
}
```

#### Note: Assignment vs. Comparison Operator
Within our conditions, we will often need to check to see whether or not two values are equal to one another, and perform an action based on the results.

Example:

```js
if (result === true) {
  // Congratulate the user on passing
}
```

Notice that we used a triple equals instead of a single equals in the condition.

This is important to note, as confusing the assignment operator with the comparison operator is a common mistake for beginners.

<img src="assets/Slide-30-Assignement-Comparison.png" width="400px">

Take a look at the following example:

Here, we are not comparing x with the number 3. We're _assigning_ the variable x the value of 3 by using `=` instead of `===`.

```js
if (x = 3) {
  console.log("boo");
}
```

If we wanted to see if x is equal to 3, we would use a *comparison* operator (the triple equals sign):

```js
if (x === 3) {
  console.log("boo");
}
```

#### Switch Statement
Video: https://generalassembly.wistia.com/medias/sew8suaz5l


The switch statement can be used for multiple branches based on a number or string:

```javascript
var food = "apple";

switch(food) {
  case 'pear':
    console.log("I like pears");
    break;
  case 'apple':
    console.log("I like apples");
    break;
  default:
    console.log("No favorite");
}
//=> I like apples
```

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




## Conditionals Summary (5 min)
Let’s turn to a summary of conditionals and test ourselves with a short quiz.

Using `if...else` statements allows us to write code that can behave very differently in different circumstances.

Consider the following conditional statement:

```js
if (x > 5) {
  y = 50;
} else if (x < 5) {
  y = 33;
} else {
  y = 100;
}
```

- What value will be assigned to y if x is 10?
  <!-- Answer: 50 -->
- What value will be assigned to y if x is 4?
  <!-- Answer: 33 -->
- Under what circumstances will y be assigned a value of 100?
  <!-- Answer: x=5 -->

<!-- SME Needed: Would be helpful to have someone build out a 15 minute exercise that uses only conditionals and variables, the current exercise also uses loops (FizzBuzz)

Another option: pull from circuits
-->
## Independent Practice


#### Solution

## Conclusion (5 mins)
These are just some of the foundational tools you'll use while building your applications with JavaScript.

You'll probably need to refresh yourself on the exact syntax a few times before you memorize it, but it's important to be able to remember these core "control flow" concepts in general, as they'll come up in pretty much every programming language you'll ever encounter.

***


### ADDITIONAL RESOURCES
- Exercises
- Videos
- Readings
  [Control Flow MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling)
- Decks

> Instructor Note: When possible, provide a brief description of Additional Resources, classifying whether it is for advanced or beginner students.  
