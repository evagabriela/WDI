<!--@sarahholden - Add Checks for understanding throughout, pull from Circuits code challenges if needed.-->


---
# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Objects (90 mins)


<!-- ID NEEDED Can you add the below sections here? -->
| Timing | Type | Topic |
| --- | --- | --- |
| x min | [Introduction](#introduction) | Topic |
| x min | [Demo/Codealong](#demo) | Topic |
| x min | [Guided Practice](#guided-practice) | Topic |
| x min | [Independent Practice](#ind-practice) | Topic |
| x min | [Conclusion](#conclusion) |Topic |

### LEARNING OBJECTIVES
*After this lesson, you will be able to:*

- Compare objects and key-value stores to arrays as data structures
- Explain the difference between object properties and methods
- Create empty objects and objects with multiple properties and methods using object literal syntax
- Compare adding and retrieving properties to an existing object using the dot and bracket notations
- Create objects using constructor notation and instances of those objects using the new keyword.
- Compare and contrast creating objects using literal notation vs. constructor functions.
- - From within a method, reference properties of the same object using this.



### STUDENT PRE-WORK
*Before this lesson, you should already be able to:*

- Create variables in JavaScript
- Differentiate between data types (strings, numbers, booleans)
- Use if/else if/else conditionals to control program flow based on boolean conditions
- Create arrays and access/manipulate elements in arrays



***

<a name="opening"></a>
## Opening (10 mins)

In this unit, our focus is objects, an exciting aspect of JavaScript that ties into many of the concepts you’ve already learned.

Once you get to know objects, you’ll realize how much easier your coding life can be.

Check: Think/Pair/Share: Ask students to define, explain, or recall anything they already know about objects. 


#### The limitations of Arrays
So far, we’ve learned about fairly simple data types: strings, numbers, booleans, and arrays.

However, as our applications become more complex, we need more structure in our code.

All of the arrays we've seen so far store and manage their elements by their indices.

This is a convenient way of managing elements, but it also has some disadvantages.

#### Easier access to data
Objects are a type of data structure that is nearly universal across programming languages, although they may have different names in different languages (in Python they're called a dictionary, in Ruby they're called Hashes).

Watch this short [video](https://generalassembly.wistia.com/medias/wk0zfyxxsc) for an example of the limitations of arrays and how storing data in objects using key/value pairs can help us structure and manage complex data more efficiently.

Objects are often called **associative arrays**, as they associate keys with values.

As you start building applications, you'll encounter many situations where you'll want to associate keys to values.

Objects are extremely useful when we want to easily access data.

Let's take a look at an example where it would be helpful to associate keys with values to easily access data.


Let's say we are developing a fantasy football website. Using a regular array, we would store each player's info like so:

```js
var player = ["Aaron", "Rodgers", 12, 32];
```
There are only a handful of values in this array, but there is no context for any of them.

Is 12 the number of touchdowns that player has scored? The number of years he's played in the NFL?

It's difficult to tell because we have no clear references for each data point.

Take a look at how we could represent the player with an object. Don't worry about syntax for now, we'll cover that soon. Just use the following example to get a feel for how to associate keys with values.

```js
var player = {
  firstName: "Aaron",
  lastName: "Rodgers",
  jerseyNumber: 12,
  age: 32
 }
```

By associating keys with values, we can more accurately represent our player object.

Now, we know at a glance what 12 is — our player's jersey number!

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4562/aaron.png" width="300px">


#### Objects - What are they good for?
Objects serve two main purposes in JavaScript:

1.  They act as a simple, structured data store. And, while they are similar to arrays, they access values using keys instead of indices.
3.  They provide a fundamental programming paradigm that helps us structure and categorize code. We'll explore this programming paradigm, known as Object Oriented Programming, later in this lesson.

In JavaScript, every physical thing can be represented as an object.

For example, if we’re working on an airline booking site, we can represent how many seats are both open and booked on any given flight.

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4577/Delta-Slide_20.png" width="300px">

On the airline site, we can also represent the customers booking those seats as objects, each with a first and last name, country of residency, birthdate, and so on.

***

<a name="properties-methods"></a>
## Properties and Methods - An Overview (10 mins)

Each object can also have its own **properties** and **methods**.


#### Properties
First, let’s explore **properties**.

**Properties** are characteristics associated with an object.

If a variable is part of an object, it becomes a property. In other words, properties tell us about an object.

Let’s look at another example:

If you were to describe a motorcycle, you might include its color, make, model, max-speed and year.

Each property has a name and a value, and each name/value pair tells us something about that individual object.

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4563/Slide-20-Chart.svg" width="300px">

#### Methods
Let’s now focus on methods.

If a function is part of an object, it becomes a **method**.

Methods are used to represent how people interact with an object in the real world. In other words, **methods** are the actions that can be performed on objects.

We can use methods to:

1.  Retrieve the values of an object's properties to find out something about that object.
3.  Update the values of an object's properties.

Consider our motorcycle example. The following actions are common ways that humans interact with motorcycles:

We can use methods to retrieve the values of an object's properties (such as the motorcycle’s model) or change its properties (such as when we start, stop, brake, or accelerate our bike).

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4518/Slide-23-Chart.svg" width="300px">


#### Independent/Paired Practice

1. In pairs, spend 2 minutes thinking about what attributes (properties) a WDI student should have (think of at least 5!) and write them out.
2. Take 2 minutes to write out the methods the student should have.
3. Bonus - Think of a property for our student that might contain an array of data.

> Instructor Note: Whiteboard ideas from each pair.


---
<a name="creating-objects"></a>

## Creating Objects (15 mins)
We kicked off this lesson with a look at how objects can be used to connect keys with values in JavaScript. If you remember, we saw how each object can also have its own associated properties and methods.

Now, let’s explore how we can add properties and methods when creating objects.

#### Object Literal Notation
First, we’ll learn how to create an object using **literal notation**.

Let's say we want to create objects for several popular superheros, starting with Superman.

We might want to add some properties for Superman — firstName, lastName, and superheroName.

We might also want to add a method to our Superman object — `revealIdentity`, which will return Superman's real first and last name (`Clark` and `Kent`), followed by his superhero name (`Superman`).


<img src="http://circuits-assets.generalassemb.ly/prod/asset/4526/Slide-5-Superman.svg" width="300px">



Here's how we would write this object using literal notation:

```js
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
```

Let’s look at the syntax breakdown:


*   Our object is contained within curly braces `{ }`
*   We are storing our object in a variable, called `superman`
*   We separate each key from its value using a `:`
*   To add a property, we use a property name, such as `firstName`, `lastName`, or `superheroName`, followed by a `:`, followed by the corresponding value: `'Clark'`, `'Kent'`, or `'Superman'`.
*   To add a method, we would use the method name `revealIdentity`, followed by a `:`, followed by an anonymous function (`function ()`).


#### This - A brief Overview


In the context of our objects, `this` is used in place of the object name to refer to the current object instance.


In a method, `this` refers to the object containing the function.


For example, in the function below, `this` refers to the animal object that contains the function/method `makeNoise`.

```js
var animal = {
  name: 'Rover',
  species: 'dog',
  breed: 'Golden Retriever',
  noise: 'bark!',
  makeNoise: function () {
    console.log(this.noise);
  }
}
```


<img src="http://circuits-assets.generalassemb.ly/prod/asset/4551/Slide-10-Rover-Bark.svg" width="300px">



Because `this` refers to the animal object, using it would be the same as writing out:

```js
console.log(animal.noise);
```

In our Superman example, within the function, we can use the `this` keyword to access different properties for our object.

For example, we can use `this.firstName` to access the value for the `firstName` property (in this case, 'Clark').


Check:

What does `this` refer to in the following scenario and why? What will be logged to the console?


```js
var paintbrush = {
  tool: 'paintbrush',
  brand: 'Winsor & Newton',
  price: 12.23,
  pattern: 'zig zag',
  drawShape: function () {
    console.log(this.pattern);
  }
}
```

> Answer: `this` refers to `‘paintbrush’`. The console will log: `‘zig zag’`.

#### Independent Practice

Let's practice!

1.  Create an object called `currentlyReading`
2.  Add the following properties to the object:

*   Title: The Wind-Up Bird Chronicle
*   Author: Haruki Murakami
*   Year: 1994
*   Rating: 4.2


<!--ID NEEDED: Help formatting question/solution? Or is this okay? -->

**Solution**

```js
var currentlyReading = {
  title: "The Wind-Up Bird Chronicle",
  author: "Haruki Marukami",
  year: 1994,
  rating: 4.2
};
```

<br>

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4527/Slide-11-haruki-murakami-book.jpg" width="150px">

---
<a name="dot-notation"></a>
## Dot Notation (10 mins)

#### Accessing Properties using Dot Notation
Now, let’s turn to accessing properties.

We can _get_ and _set_ object properties using either **dot notation** or **square bracket syntax**.

**Dot notation** is common for simple scenarios.

Remember the syntax we used when learning about arrays to find out the length of an array?

```js
var fruits = ["blueberries", "strawberries", "apples"];
fruits.length => 3
```

By using our array name, followed by `.length`, we were able to access the length property of our array.

This is the dot `.` notation.

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4528/Slide-12-Fruit.svg" width="300px">

We can access values using the object name, followed by a period `.`, followed by the name of the property we want to access.

Here, we've created the variables `heroFirstName` and `heroLastName` to store the information we want to retrieve.

```js
var heroFirstName = superman.firstName;   => 'Clark'
var heroLastName = superman.lastName;   => 'Kent'
```
#### Updating Properties using Dot Notation
We can also update values using dot notation.

To do so, we use the name of the object (in this case, `superhero`), followed by the name of the property we want to update (in this case, `.firstName` or `.lastName`).

We then use the assignment operator (`=`), followed by the new value.

```js
superhero.firstName = 'Susan';
superhero.lastName = 'Storm';
```

#### Adding New Properties
The syntax we use to update a property can also add a new one. If the property we are trying to update doesn't yet exist, it will be added automatically.

```js
superhero.favoriteFood = 'Beef Bourguignon';
```

We've now added a new favorite food for Superman!

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4529/Slide-15-Superman-Beef.svg" width="300px">


#### Independent Practice

Let's practice!

Consider the following object:

```js
var pet = {
  species: 'iguana',
  gender: 'female',
  age: 12,
  name: 'Godzilla'
};
```

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4530/Slide-16-Lizard.svg" width="150px">

1. What code could we write to retrieve the value for `name` from the object and store this value in a variable `petName`?
  - Answer: `var petName = pet.name;`
2. Now, how would you assign `13` as the value for `age`?
  - Answer: `pet.age= 13;`
3. How would you add a new property, `'favoriteFood'` using the value `'crickets'`?
  - Answer: `pet.favoriteFood = 'crickets';`


---
<a name="square-bracket-notation"></a>
## Square Bracket Notation (10 mins)
Let's go back to our superhero example.

To access values, we can also use **square bracket syntax** to access and update the properties for an object.

```js
var heroFirstName = superman['firstName'];   => 'Clark'
var heroLastName = superman['lastName'];   => 'Kent'
```

Once again, the name of our object is `superman`, followed by the property name, contained within quotes and square brackets.

The square bracket syntax is commonly used when a variable name is used in place of a property name:

```js
var propertyName = 'firstName';
var supermanFirst = superman[propertyName];   => 'Clark'
```

#### Square Bracket vs. Dot Notation
Dot notation can only work with the _exact literal name of the property_ since you can’t type something like `superman.’firstName’` or `superman.yourVariableName`, while the square brackets allow for substituting in the value of a string or variable in place of the property name.


Let’s update the `firstName` and `lastName` of our object again, but use the square bracket syntax this time:

```js
superman['firstName'] = 'Susan';
superman['lastName'] = 'Storm';
```

As with dot notation, we use the name of the object, followed by the property name wrapped in quotes and square brackets (`[ ]`). Next, we use the assignment operator (`=`), followed by the new value.

Although dot notation is often a popular method, as it’s slightly easier to write out, we'll need to use square bracket syntax anytime we are generating our property names dynamically, i.e. when we want to use a variable for a property name.

#### Independent Practice
Now you try! Let's return to our pet, Godzilla.

Consider the following object:

```js
var pet = {
  species: 'iguana',
  gender: 'female',
  age: 12,
  name: 'Godzilla'
};
```

1. How would you retrieve the value for `'name'` from the object, and store this value in a variable name using square bracket syntax `[ ]`?
  - Answer: `var name = pet['name'];`
2. How would you assign `13` as the value for `'age'` using square bracket syntax `[ ]`?
  - Answer: `pet['age'] = 13;`
3. How would you add a new key, `'favoriteFood'`, with value `'crickets'` using square bracket syntax `[ ]`?
  - Answer: `pet['favoriteFood'] = 'crickets';`


---
<a name="removing-properties"></a>
## Removing Properties (5 mins)
Excellent! Now, let’s discuss how we can use the `delete` operator to remove a property from our object.

Here's what the syntax for deleting a property looks like (using the dot notation or the square bracket syntax):

```js
delete object.property      // Dot notation
delete object['property']   // Square bracket syntax
```

Here’s an example:

```js
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
```

Dot Notation: `delete superman.firstName;`  
Square Bracket Notation: `delete superman['firstName'];`


---
<a name="accessing-methods"></a>
## Accessing Methods (5 mins)
Next, let’s talk about accessing methods. We will use **dot notation** to access methods for our objects.

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4531/Slide-29-Clark-Kent.svg" width="300px">

If we wanted to access — or call, our `revealIdentity` method — we could do so using the following syntax:

```js
var supermanIdentity = superman.revealIdentity(); => 'Clark Kent is Superman'
```

1. Here, we use the object name `superman`, followed by a period, followed by the method name, followed by parenthesis.
2. We are saving the value that is returned in a variable, `supermanIdentity`, so we can reference it later.

<!--@sarahholden add CFU-->


---
<a name="iterating-through-objects"></a>
## Iterating through an Object (10 mins)

Like arrays, you can use a loop to iterate through an object. Say we want to print out all of an object's keys...

```js
// Iterate through object keys
for (attribute in car) {
  console.log( attribute );
}
```

> Knowing this, how could we go about getting all the values in an object?

Javascript objects also have native methods that take care of this for us...

```js
// .keys()
Object.keys( car );
```

### Exercise

Create a variable named `wdiStudent` and assign it to an object literal.

1. Give your student at least three properties.
2. One must have a key that contains a hyphen.
3. One must contain an array or object.
4. Update two properties, one of which is the hyphenated.
5. Give your student a new property using dot or bracket notation.
6. Delete one attribute.
7. Iterate through and print out all of the student's key-value pairs.

**Bonus:** Write a function that returns your `wdiStudent` object

> [Solution](https://gist.github.com/nolds9/efdb0a320e7143f42e96)


---
<a name="nested-collections"></a>
## Nested Collections (5 mins) -- If time permits

Object properties aren't limited to simple data types. We can also nest collections inside of collections.

```js
var car = {
  make: "Honda",
  model: "Civic",
  year: 1997,

  // An array within an object.
  gears: ["Reverse", "Neutral", "1", "2", "3", "4"],

  // An object within an object.
  engine: {
    horsepower: "6 horses",
    pistons: 12,
    fast: true,
    furious: false
  }
}
```

Check: In the above examples, how do we access...
* "Neutral" (i.e., array value within an object)?
* "6 horses" (i.e., object value within an object)?


---
<a name="lab-session"></a>
## Independent Practice - Objects (10 mins)

In pairs, work to solve the following problem:

Create an example 'User' object, complete with several 'Meals'.

A 'User' needs to have:

-   a name (`name`)
-   a date-of-birth (`bornOn`)
-   a target daily calorie intake (`calorieTarget`)
-   a list of 'Meals' that they've eaten (`meals`)

Every 'Meal' must have:

-   a title (`title`), e.g. 'breakfast', 'lunch', 'dinner'
-   a date (`date`), represented as a string e.g. "2016-06-25"
-   a description (`description`)
-   a number of estimated calories (`calories`)

Then, create the following methods for your instance of a 'User':

-   `caloriesEatenOn`, which accepts a date (in the format above) and calculates
    the total number of calories consumed on that date.
    
Bonus Tasks -- create the following methods for your instance of a 'User':
-   `avgDailyCalories`, which (as indicated), calculates the average number of
    calories consumed per day, rounded down to the nearest whole calorie.
-   `onTrack`, which compares averageDailyCalories to the User's target daily
    calorie intake, and returns `true` if average caloric intake is at or below
    the target (or `false` if the reverse is true).

***

<a name="conclusion"></a>
## Conclusion (5 mins)
- Review independent practice deliverable(s)
- Recap topic(s) covered in today's lesson
- Cover homework and/or upcoming tasks

***


### ADDITIONAL RESOURCES
- Exercises
	- [JS Calculator](exercises/js_calculator.MD) (30 Mins - Int / Adv)
	- [Pets and Owner](exercises/pet_owner.MD) (30 mins - Beg)
- Videos
  - JS Circuits - [Intro to Objects](https://generalassembly.wistia.com/medias/m8d1oq04br)
  - JS Circuits - Why use objects? [Sports analogy](https://generalassembly.wistia.com/medias/wk0zfyxxsc)
- Readings
	- Eloquent JavaScript Chapter 6 - [The Secret Life of JS Objects](http://eloquentjavascript.net/06_object.html) (Great resource!)
	- MDN - [Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
	- MDN - [Working with Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)
- Decks

> Instructor Note: When possible, provide a brief description of Additional Resources, classifying whether it is for advanced or beginner students.  
> 
> 



<!--

@sarahholden Put these labs in another folder and format

SECOND EXAMPLE:

## `this`

One way to break up the complexity of a problem is by using multiple kinds of
objects together, and having each object be responsible for representing a small
part of the problem. But these objects don't need to exist in isolation -
objects can have other objects (or even collections of other objects) as
properties.

Suppose that we wanted to create a simple program ('RunTracker') that helps
people prepare for running a 5k. Each day that a person runs, they create a
record of their run which contains:

-   the date and time of the run
-   the distance covered, in meters
-   the time taken, in seconds

The program also stores information about the user (the user's name and email
address) and can perform some calculations (total distance run, longest run
so far, and average speed).

## Lab: Diagram and Model

Using the description of the program above, create an entity diagram.

1.  Identify the entities (kinds of objects) needed in the program.
1.  Draw a box for each entity and label it with the singular, capitalized
    entity name.
1.  Connect any entities that are related using a line.
1.  List attributes and methods of each entity separately within each entity's
    box.

## Demo: Write Methods With `this`

```js
let user = {
  name: "Person McFace",
  email: "wdi@personmcface.com",
  runs : [
    {
      date: "2016-05-25 15:00",
      distance: 1200,
      timeTaken: 600
    },
    {
      date: "2016-05-25 15:00",
      distance: 1400,
      timeTaken: 800
    }
  ],

  totalDistance : function() {},
  longestRun : function() {},
  averageSpeed : function() {}
}
```

When we start thinking about how the methods for 'User' will work, we run into a
difficulty. A method for calculating the longest run so far needs to be able to
see, and refer to, all of the runs associated with that particular user. How do
we do that?

Follow along as I demonstrate how to complete writing each method.

## Lab: Self-Referential Objects

In groups, you're going to work on a similar program to our previous one, this
time for meal tracking. In particular, you're going to create an example 'User'
object, complete with several 'Meals'.

A 'User' needs to have:

-   a name (`name`)
-   a date-of-birth (`bornOn`)
-   a target daily calorie intake (`calorieTarget`)
-   a list of 'Meals' that they've eaten (`meals`)

Every 'Meal' must have:

-   a title (`title`), e.g. 'breakfast', 'lunch', 'dinner'
-   a date (`date`), represented as a string e.g. "2016-06-25"
-   a description (`description`)
-   a number of estimated calories (`calories`)

Then, create the following methods for your instance of a 'User':

-   `caloriesEatenOn`, which accepts a date (in the format above) and calculates
    the total number of calories consumed on that date.
-   `avgDailyCalories`, which (as indicated), calculates the average number of
    calories consumed per day, rounded down to the nearest whole calorie.
-   `onTrack`, which compares averageDailyCalories to the User's target daily
    calorie intake, and returns `true` if average caloric intake is at or below
    the target (or `false` if the reverse is true).

Add your code to [`lib/meals.js`](lib/meals.js), structured similarly to
[`lib/runs.js`](lib/runs.js).


THIRD OPTION:

### Bonus
### You Do: Big Ol' Twitter Object (15 / 125)

As this course continues you will encounter plenty of Javascript objects in the wild. Spend **10 minutes** on the following...
* Follow the link below and answer the questions in bold.
* Along with each answer, write down how we would access the property in question.
* Let's do the first one together...

[Twitter JSON Exercise](https://github.com/ga-dc/big_ole_twitter_object)



-->
