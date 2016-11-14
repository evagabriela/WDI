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


<!-- @sarahholden

Examples on context here: https://github.com/ga-wdi-lessons/js-scope/blob/master/context.md


-->


---
# <img src="https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Lesson Title (# mins" width="300px">

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

> Instructor Note: Use instructor notes to talk directly to instructors. Otherwise, write out lesson directions and materials in a student-facing voice.

Check: Ask students to define, explain, or recall any **general** prior concepts or tools.

***

<a name="introduction"></a>
## Introduction: Topic (# mins)

In this unit, our focus is objects, an exciting aspect of JavaScript that ties into many of the concepts you’ve already learned.

Once you get to know objects, you’ll realize how much easier your coding life can be.

#### The limitations of Arrays
So far, we’ve learned about fairly simple data types: strings, numbers, booleans, and arrays.

However, as our applications become more complex, we need more structure in our code.

All of the arrays we've seen so far store and manage their elements by their indices.

This is a convenient way of managing elements, but it also has some disadvantages.

#### Easier access to data
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


#### Properties and Methods - An Overview

Each object can also have its own **properties** and **methods**.


##### Properties
First, let’s explore **properties**.

**Properties** are characteristics associated with an object.

If a variable is part of an object, it becomes a property. In other words, properties tell us about an object.

Let’s look at another example:

If you were to describe a motorcycle, you might include its color, make, model, max-speed and year.

Each property has a name and a value, and each name/value pair tells us something about that individual object.

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4563/Slide-20-Chart.svg" width="300px">

##### Method
Let’s now focus on methods.

If a function is part of an object, it becomes a **method**.

Methods are used to represent how people interact with an object in the real world. In other words, **methods** are the actions that can be performed on objects.

We can use methods to:

1.  Retrieve the values of an object's properties to find out something about that object.
3.  Update the values of an object's properties.

Consider our motorcycle example. The following actions are common ways that humans interact with motorcycles:

We can use methods to retrieve the values of an object's properties (such as the motorcycle’s model) or change its properties (such as when we start, stop, brake, or accelerate our bike).

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4518/Slide-23-Chart.svg" width="300px">


---
<a name="creating-objects"></a>

## Creating Objects (# mins)
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
1.  As you may have noticed while examining object oriented code, we often run into the keyword `this`. We’ll cover `this` in more detail later on. But, for now, know that, in the context of our objects, `this` is used in place of the object name to refer to the current object instance.


In our Superman example, within the function, we can use the `this` keyword to access different properties for our object.

For example, we can use `this.firstName` to access the value for the `firstName` property (in this case, 'Clark').

#### Independent Practice

Let's practice!

1.  Create an object called `currentlyReading`
2.  Add the following properties to the object:

*   Title: The Wind-Up Bird Chronicle
*   Author: Haruki Murakami
*   Year: 1994
*   Rating: 4.2


> Solution

```js
var currentlyReading = {
  title: "The Wind-Up Bird Chronicle",
  author: "Haruki Marukami",
  year: 1994,
  rating: 4.2
};
```



<img src="http://circuits-assets.generalassemb.ly/prod/asset/4527/Slide-11-haruki-murakami-book.jpg" width="150px">


## Dot Notation (# mins)

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
##### Updating Properties using Dot Notation
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

## Square Bracket Notation (# mins)
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


Dot notation can only work with the _exact literal name of the property_ since you can’t type something like `superman.’firstName’` or `superman.yourVariableName`, while the square brackets allow for substituting in the value of a string or variable in place of the property name.


Let’s update the `firstName` and `lastName` of our object again, but use the square bracket syntax this time:

```js
superman['firstName'] = 'Susan';
superman['lastName'] = 'Storm';
```

As with dot notation, we use the name of the object, followed by the property name wrapped in quotes and square brackets (`[ ]`). Next, we use the assignment operator (`=`), followed by the new value.

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



## Removing Properties (# mins)
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

#### Accessing Methods
Lastly, let’s talk about accessing methods. We will use **dot notation** to access methods for our objects.

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4531/Slide-29-Clark-Kent.svg" width="300px">

If we wanted to access — or call, our `revealIdentity` method — we could do so using the following syntax:

```js
var supermanIdentity = superman.revealIdentity(); => 'Clark Kent is Superman'
```

1. Here, we use the object name `superman`, followed by a period, followed by the method name, followed by parenthesis.
2. We are saving the value that is returned in a variable, `supermanIdentity`, so we can reference it later.

#### Summary: Dot notation vs. Square Bracket Notation
Although dot notation is often a popular method, as it’s slightly easier to write out, we'll need to use square bracket syntax anytime we are generating our property names dynamically, i.e. when we want to use a variable for a property name.



## Constructor Notation
There might be instances where we want to create multiple objects to represent similar things.

For example, if we built a superhero fan site, we’d want to store similar information for a range of superheroes: first name, last name, superhero name, etc.

To do this, we can create a "template" object that contains any properties and methods we want to add for each superhero.

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4536/Slide-3-Superhero-Fan-Site.svg" width="300px">


We create object templates with a function called a constructor.

Constructor notation can be used to:

1.  Create a single, empty object.
2.  Create multiple instances of similar objects.

#### Creating an Object using Constructor Notation
First, let's first take a look at how we can create a single, empty object using constructor notation.


Take a look:

```js
var superman = new Object();
```

Here, we save our object to the variable `superman`.

Then, we create the new object by using the `new` keyword followed by the object constructor.

The result is an empty superman object. It doesn't have any associated properties or methods yet, so we need to add them.

#### Adding Properties
We can add properties to our object using either the dot notation (`.`) or square bracket syntax (`[ ]`).

```js
superman.firstName = 'Clark';
superman.lastName = 'Kent';
superman.superheroName = 'Superman';
```

We can add methods to our objects using the dot notation:

```js
superman.revealIdentity = function () {
return this.firstName + " " + this.lastName + " is " + this.superheroName;
};
```

#### Accessing/Updating Properties
We can also access and update properties using either the dot notation or square bracket syntax, just like we did with our object literals:

```js
// Accessing Values
var heroFirst = superman.firstName;

// Updating Values
superman.firstName = 'Bill';
superman['superheroName'] = 'Super Duper Man';
```

#### Independent Practice

1.  Create an object `currentlyListening`
2.  Add the following properties to your object:

*   The `album` is "Wild Honey"
*   The `artist` is "The Beach Boys"
*   The `releaseDate` is 1967
*   The `label` is "Capitol Records"


Answer option 1:

```js
var currentlyListening = new Object();
currentlyListening.album = "Wild Honey";
currentlyListening.artist = "The Beach Boys";
currentlyListening.releaseDate = 1967;
currentlyListening.label = "Capitol Records";
```

Answer option 2:

```js
var currentlyListening = new Object();
currentlyListening["album"] = "Wild Honey";
currentlyListening["artist"] = "The Beach Boys";
currentlyListening["releaseDate"] = 1967;
currentlyListening["label"] = "Capitol Records";
```

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4538/Slide-10-Beach-Boys-Album.jpg" width="300px">


## Creating Multiple Objects using Constructor Notation
Whew! With that under our belt, it’s now time to turn to creating many objects using **constructor notation**.

The real power of constructor notation comes into play when we create multiple objects to represent similar things.

Think about our superhero fan site.

As you’ll recall, we want a way to store similar info for many superheroes: first name, last name, superhero name, etc.

We need to create a "template" object, which contains the properties we want to add for each superhero.

#### Constructor Function
To create this object template, we use a function called a **constructor**.

This is really just a function like any other, but, when you call it in a particular way, JavaScript works its magic.

Let’s see an example of an object constructor function.

Here, we are creating a `Superhero` function. It’s just like creating any other function in JavaScript.

```js
var Superhero = function () {};
```

Note that it is convention to _capitalize the name of the function_ when creating an object using constructor notation. We'll take a look at this again in a moment.


#### Creating Object Instances
Creating an instance of our `Superhero` object is similar to creating a new empty object using constructor notation:

```js
var clark = new Superhero();
var bruce = new Superhero();
```


Here, we save our new objects to the variables `clark` and `bruce`. We use the `new` keyword, similar to when we created a new empty object above. We then use the name of the constructor function `Superhero`, followed by parenthesis `()`.

Note that the name of a constructor function usually begins with a capital letter — unlike other functions — to remind developers to use the `new` keyword when creating an object using that function.


The constructor function is called at the moment that our `new` object is **instantiated**.

For example:

```js
var SuperHero = function () {
  console.log('Superhero instance created');
};

var clark = new Superhero(); // console logs "Superhero instance created"
var bruce = new Superhero(); // console logs "Superhero instance created"
```

Messages are logged to the console as soon as we create a new instance of our object.

#### Setting Up Properties/Methods
Up until this point, we've set property names manually, for every new object we create.

The point of our objects/constructors is to create blueprints of our data models, so that, when we create a new instance, we can change particular properties instead of resetting all of the object’s keys.


Properties can be set in the constructor so they are set specifically for each instance. In other words, we pass them as parameters in our constructor function.

Take a look at the following example:

```js
var Superhero = function (firstName, lastName, superheroName) {
  this.firstName = firstName;
  this.lastName = lastName;
  this.superheroName = superheroName;
  this.revealIdentity = function () {
    return this.firstName + " " + this.lastName + " is " + this.SuperheroName;
  }
    console.log('superhero instantiated');
};
```

Let's break this down, line-by-line.


<img src="http://circuits-assets.generalassemb.ly/prod/asset/5108/code0.png" width="500px">


1. Overview: We are using a constructor function to create a template for our `Superhero` objects.
2. We pass three parameters, i.e., the property names each superhero will have in common: `firstName`, `lastName`, and `superheroName`.
3. The object properties `firstName`, `lastName` and `superheroName` are then set through the `this` keyword with the value.
4. Within the function, `firstName` refers to the parameter name we passed to the function. Same with `lastName` and `superheroName`.
5. We then add a method for our object, similar to how we've done it in the past. To add a method, we use the method name `revealIdentity`, followed by an equal sign, followed by an anonymous function (a function without a name).
6. Within the function, we use this to access the properties of the instance of the individual object we are creating.


#### Creating and Instance
To create an instance of our `Superhero` object.



1. Use the `new` keyword followed by the name of our constructor function, `Superhero`.

  <img src="http://circuits-assets.generalassemb.ly/prod/asset/5117/more_code2.png" width="500px">

2. Pass in three arguments, which are the property values that correspond to the three parameters we passed into our `Superhero` constructor function: `firstName`, `lastName`, and `superheroName`.
  <img src="http://circuits-assets.generalassemb.ly/prod/asset/5118/more_code3.png" width="500px">


We've now created two new instances of our Superhero object!

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4550/Slide-19-Charts.svg" width="300px">

We can create as many superheroes as we want using our Superhero constructor function.

We also have a blueprint, or template, of our object. So, in the future, when we create a new instance, we won’t need to reset all the keys.

All we’ll have to do is give values for different properties.

```js
// We can access properties of our object instances using dot or square bracket notation
  console.log(superman.firstName + ' ' + superman.lastName);
  => 'Clark Kent'

```




Notice our `revealIdentity` method is also copied over to each individual object.

```js
// We can also access methods using our new object instances:
superman.revealIdentity(); => 'Clark Kent is Superman'
batman.revealIdentity(); => 'Bruce Wayne is Batman'
```


Creating objects is now much more scalable than if we used literal notation to create every individual object.

Our code will also be cleaner, as we avoid repetition when creating similar objects.



---

## This (# mins)

In this lesson, we covered how to use the `this` keyword to access properties and methods for our objects.

We also mentioned that `this` is used in place of the object name to refer to the current object instance.


Now we'll take a closer look at `this` and how it can refer to different things depending on the context.

`this` is a keyword commonly used inside functions and objects. It can sometimes be tricky to know what `this` refers to, because it refers to different things in different contexts.

Let's take a look:

We’ll start off talking about a function with a global scope.

When a function is created at the top level of a script — meaning it is not defined in an object or inside of another function — it has **global scope** (similar to the variable scope we discussed in the last unit).

In this context, the default object is also considered the **window object**. The window object represents the current browser window or tab. It contains other objects that tell you about the browser.

The window object also contains properties that tell us about the current browser window.

Let's look at some examples!


`window.innerHeight`  
→ Returns the height of browser window



<img src="http://circuits-assets.generalassemb.ly/prod/asset/4678/Screen_Shot_2016-06-24_at_3.26.40_PM.png" width="300px">


`window.location`  
→ Current URL



<img src="http://circuits-assets.generalassemb.ly/prod/asset/4680/Screen_Shot_2016-06-24_at_3.28.48_PM.png" width="300px">


`window.scrollY`  
→ Returns the distance we've scrolled



<img src="http://circuits-assets.generalassemb.ly/prod/asset/4679/Screen_Shot_2016-06-24_at_3.26.58_PM.png" width="300px">

Now, let's see how the window object relates with the `this` keyword.

When `this` is used in a function that is defined in the global scope, `this` refers to the window object.

Here's an example:


```js
this.innerWidth => Width of browser window

function windowInfo() {
//Width of browser window object
   var windowWidth = this.innerWidth;
//Height of browser window object
   var windowHeight = this.innerHeight;
}
```


The first time we use `this`, we are using it in the global scope, as it’s not contained within an object.

The second and third time you see `this`, we are also using it in the global scope. Even though it is contained within a function, it is not a part of any object.

In each of these instances, using `this` is the equivalent of using window.







Let’s learn about what happens when a method is contained inside an object. We saw in the last unit that, when a function is defined inside an object, we call it a method.

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

However, when we create several objects using constructor notation, `this` refers to the individual instance of that object.

Let's look at an example:

```js
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
```







<img src="http://circuits-assets.generalassemb.ly/prod/asset/4552/Slide-12-Cat-Tux-Meow.svg" width="300px">







Here, `this` refers to the individual instance of the object we are creating.

So, when we create our wolfman object, `this` will refer to the wolfman object and `this.noise` will return `'meow'`.

When we create our rover object, `this` will refer to our rover object, and `this.noise` will return `'bark'`.





Test yourself! See if you can guess what `this` refers to in the following situations.

```js
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
```

When we create our batman object, what will `this` refer to? What will be logged to the console from within the `makeNoise` method?:

`console.log(this.noise);`

> Answer:  
`this` will refer to `batman`.  
`this.noise` will return `‘chirp’`.






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

What does `this` refer to within the `drawShape` method? What will be logged to the console?

> Answer: `this` refers to `‘paintbrush’`. The console will log: `‘zig zag’`.



***

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
