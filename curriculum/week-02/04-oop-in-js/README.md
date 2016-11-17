
# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Object Oriented Programming (90 mins)
<!--
ID NEEDED: Help with jumplinks / Transferring lesson sections & times up here-->

| Timing | Type | Topic |
| --- | --- | --- |
| x min | [Introduction](#introduction) | Topic |
| x min | [Demo/Codealong](#demo) | Topic |
| x min | [Guided Practice](#guided-practice) | Topic |
| x min | [Independent Practice](#ind-practice) | Topic |
| x min | [Conclusion](#conclusion) |Topic |

### LEARNING OBJECTIVES
*After this lesson, you will be able to:*

<!--@sarahholden update-->
Define methods on custom objects by attaching them to the prototype
Refactor code with OOP concepts such as
encapsulation
abstraction
Recognize when objects can help in creating simpler tasks
Recognize, understand and write prototype functions
Build practical and useful objects using Javascript constructors
Demonstrate a working knowledge of object properties and methods
Convert previous projects to utilize Object Oriented Programming techniques
Understand Object Inheritance
Understand SOLID
Understand private, protected, and public scopes

- **Build** practical and useful objects using Javascript constructors
- **Demonstrate** a working knowledge of  object properties and methods
- **Convert** previous projects to utilize Object Oriented Programming 


### STUDENT PRE-WORK
*Before this lesson, you should already be able to:*

<!--@sarahholden update-->
- Describe some concept
- Explain how to do something
- Do or build something


---
<a name="opening"></a>
## Opening (# mins)
- Review current lesson objectives

Before we get started, watch this short [case study](https://generalassembly.wistia.com/medias/0bgiqqwd68) where a developer describes the role Object Oriented Programming (OOP) plays in his personal workflow and in programming in general.

Understanding OOP concepts gives us an excellent frame of reference for a lot of information that comes later in the course. OOP concepts are the most common way that developers think about organizing code at a high level.

Object oriented programming is a common pattern throughout many languages. Its patterns will enable you to write more readable, organized, and declarative programs. Simply put, understanding Object Oriented Programming will make us better developers.


***

<a name="introduction"></a>
## Introduction: Topic (# mins)

Think about a game of soccer.  Let's think about all the pieces that make up that game, what are they?  What are some of their properties, things that describe them?  How about their methods, what do they do?

> Instructor Note: Pause for 1 minute, then cold-call and write this on white board as students fill in details. 

***

<a name="review"></a>
## Review: What is an Object? (10 mins)
So far in this course, we have been writing our Javascript code using mainly functions, Strings, numbers, and Arrays.

Last lesson we introduced objects as a way to store and work with more complex data. 

Before we begin, let's review what objects look like by taking a look at the following object:

<!--@sarahholden update example-->

```javascript
var cohort = {
	school: "General Assembly",
	city: "San Francisco",
	course: "Web Development Immersive",
	courseId: "WDI29",
	classroom: "8",
	students: [{
		id: 0,
		lastName: "Girouard",
		firstName: "Zeb",
		githubUsername: "zebgirouard"
	}, {
		id: 1,
		lastName: "Barela",
		firstName: "John",
		githubUsername: "jpbarela"
	}]
}


```


> Check: Think/Pair/Share
> 
-  With a partner, consider the following questions:
	- How many of the properties in `cohort` are Strings? 
 	- How many of the properties are Arrays?
 	- If there is an array, what data type(s) are the elements inside?

<!--The `cohort` object is a grouping of key & value pairs (known as properties) that describe our class.  
  
```javascript 
school: "General Assembly"
```
In the line above, `school` is the **key** and `"General Assembly"` is the **value**.
 
To access a property, we can use dot-notation or bracket-notation on the key to have the corresponding value returned.
 
 ```javascript
 var GA = cohort.school; //General Assembly
 ```

 ```javascript
 var GA = cohort["school"]; //General Assembly
 ```
 
Now the variable `GA` is assigned to the string `General Assembly`.  

How about if we want to access all the cohort's students?

 ```javascript
 var students = cohort.students; //students
 ```
The `cohort.students` array is now accessible by using `students` instead.
Declaring variables and defining them as portions of a larger object helps us create readable and maintainable code.  
-->

*We can assume that an Object is a collection of properties (key & value pairs) that all have some sort of relationship, connected logically to one another.*  

> Instructor Note: CFU: Fist-to-five on Object properties, methods

***

<a name="object-review-practice"></a>
## Independent Practice: Objects (5 mins)
- Add some more properties that would fit into an object describing our cohort (address, floor number, instructors, etc).
- Try to access your new properties from the console to make sure they work.

If everything worked out, you should have a fully functioning `cohort` object, only now with even MORE properties with us to play with!  






<!--@sarahholden possible Check for understanding/Mini-lab:
Lab: Model a Hero

What features do batman and wonderWoman share? Remember to think about attributes and methods when you're modeling. Also take note of what differs between them.

Make a diagram of our Hero entity based on the above objects.-->

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

> Note: We defined a method inside the the Superhero constructor here. JavaScript allows it, but don't do it. We'll see the right way to achieve a near identical and preferred result shortly.


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






##Constructors (25 mins)

For relatively straightforward and small objects, it is perfectly fine to declare them as a variable and define them, as we did with `cohort`.  This is known as a *Literal* object definition.  

###Literal Method and Object.create()

Here's a flower using the *Literal* method:

```javascript
// Literal Object Definition
var flower = {
	color : "red",
	petals : 32,
	smells : true
};
```

We *could* create another flower using `Object.create`. For example:

```javascript
// a rose is a flower
var rose = Object.create(flower);
// but, our rose only has 16 petals
rose.petals = 16;
```

The `rose` will share all characteristics of the original `flower`, except it will have 16 petals because we overwrote that property.

###Independent Practice

Now imagine a specific flower.  Take a few minutes to think of three properties.  Try to use multiple senses to describe it.  Define it as "flower".  Then, use `Object.create()` to make a new type of flower with a couple different properties.  Print your new flower to the console to see what it looks like.

### Constructor Syntax

Now let's explore a flower using the preferred *constructor* syntax:
 
 ```javascript
 // constructor object definition
 // note: constructors are always capitalized by convention
 function Flower() {
 	this.color = "red";
 	this.petals = 32;
 	this.smells= true;
 }
 ```

The constructor method is actually a function that can create unique instances of flower objects every time it is called.  Below, we will create a variable `tulip` that will use the constructor method to create a new object.

```javascript
// the keyword `new` is necessary
var tulip = new Flower();
```

Let us break down a couple concepts introduced with this new line of code:
- The capitalization of `Flower` lets everyone know that `Flower` is an object constructor.  Calling `Flower()` will return a `Flower` object.
- The `new` keyword before our function tells javascript that we are creating a new object that will be independent of any other object.
- We call the flower function, which creates an object with the properties made.  Our object is ready to go!

<img src = http://www.mzephotos.com/wallpapers/roses/red-rose-1024x768.jpg width = 75%>

### Independent Practice

Now, take a few minutes to rewrite your code from before to use the *constructor* syntax.

<!--CFU Fist-to-five on the two ways to create an object -->

<!-- 9:35 -->

###Taking It Further

Accessing the properties of our new `tulip` object is the same as accessing our properties from any other object: we can use either dot or bracket notation.

```javascript
var color = tulip.color; // red
var petalCount = tulip.petals; // 32
var smellsNice = tulip.smells; //true
```

If we wanted to create yet ANOTHER flower, all we have to do is call our function just like we did above.  This time, lets make an object called `lily`.

```javascript
var lily = new Flower();
```

We can access the properties of `lily` in the same manner as we did with `tulip`.

```javascript
var color = lily.color; // red
var petalCount = lily.petals; // 32
var smellsNice = lily.smells; //true
```

I don't know about you, but I generally like my lilies yellow. I have also never heard of a lily with 32 petals, holy smokes!  Can we change our `lily` object to better reflect my perfect lily? You bet!

```javascript
// Changing object property values
lily.color = 'yellow';
lily.petals = 6;
```

That's more like it!  To change the value of the lily object properties. We simply access them with dot or bracket notation.  We then follow with an equals and a new appropriate value.  Couldn't be easier!

<img src = https://seniorhikerphotos.files.wordpress.com/2012/06/lilysarina12052301.jpg width = 75%>

##Object Methods
<!-- 9:45 -->
One of the most powerful features of Javascript Objects are Methods.  Methods are *"functions"* that are predefined and built into an object.  We all know and love `Array` methods like `forEach()`, `map()`, `filter()`, and `reduce()`; these are all Methods of the Array object.  We use arrays so much that Javascript automagically creates them from an Array constructor without us having to instantiate them with `new` like we did above with the flowers.  Thanks, Javascript!

Lets make a simple method in the flower object that outputs to the console whenever we call it.

```javascript
function Flower() {
    this.color = "red";
    this.petals = 32;
    this.smells= true;
    // Demonstrates a simple method in an object
    this.bloom = function() {
        console.log("Look at me!");
    };
}
```

We now have a method inside our flower object called `bloom`.

There's an issue with the above code. If we create multiple flowers we don't care if the attributes `color`, `petal`, and `smells` all have different properties. It makes sense for these properties to be different and customizable for each flower. However, all flowers could share the `bloom` method. What we want to avoid is creating an entirely new `bloom` method every time we make a new flower.

```javascript
var lily = new Flower();
var rose = new Flower();

lily.bloom === rose.bloom // false
```

But we want their bloom methods to be the same!

##Prototypes

<!-- Do Object.getPrototypeOf(lily), same with "rose", then wrap that in Object.getPrototypeOf() 
Fist-to-five on this
-->

<!-- 9:55 -->

By adding the method `bloom` to the constructor's **prototype** we can enable all flowers to share a `bloom` method, or any other method for that matter! The prototype is simply the object that can be referenced by all the flower instances.

```javascript
function Flower() {
    this.color = "red";
    this.petals = 32;
    this.smells= true;
}

Flower.prototype = {
  bloom: function() {
    console.log("Look at me!");
  }
}
```

Now try running the same test to see if both flowers share the same `bloom` method.

```javascript
var lily = new Flower();
var rose = new Flower();

lily.bloom === rose.bloom // true
```

###Benefits
<!-- 10:05 -->
- Less wasted memory
- Single source of truth

>What if we edit the prototype *after* the flower instances have been created? Will they update their behavior accordingly?

<!-- Pass out flowers -->

###More methods
<!-- 10:30 -->
Let's add some more methods to the flower constructor.

```javascript
function Flower() {
    this.color = "red";
    this.petals = 32;
    this.smells= true;
}

Flower.prototype = {
  bloom: function() {
    console.log("Look at me!");
  },
  smellsGood: function() {
  // use `this` to access the instance's attributes
    if (this.smells) {
      return 'This flower smells amazing!';
    } else {
      return 'What a noxious weed!';
    }
  },
  describe: function() {
    console.log("This flower is " + this.color + ".");    
  }
}
```
Methods can also access properties within the object with the `this` identifier rather than using dot or bracket notation.

###Quick Challenge - Wilt & water
<!-- 10:35 -->
- Create a wilt() method that decrements each flower by one petal. :(
- Create a water() method that increments each flower by one petal. :)

##Customization
<!-- 10:45 -->
Wouldn't it be nice if at the moment we instantiate a flower we could also define its properties?

```javascript
var chrysanthemum = new Flower("pink", 65, false);
```

Such that the `chrysanthemum` is pink with 65 petals and doesn't smell good.

<details>
<summary>Challenge: how could we refactor the original flower constructor to accomplish this?</summary>

```javascript
function Flower(color, petals, smells) {
    this.color = color;
    this.petals = petals;
    this.smells = smells;
}
```
</details>

##Modeling Flowers
<!-- 10:55 -->
<!--CFU Make an object that describes the flower you have in front of you using Object.create(); -->

Take 10 minutes to create a flower instance based on the flower on your table, using Object.create(). Decide amongst your
tablemates the type of flower, the flower's main color, number of petals, and whether or not it smells pretty. Think up some other possible properties or methods and add them too!

<!--CFU make an object that describes your neighbor's flower with a Constructor function -->

Take another 5 minutes to create a flower instance based on your neighbor's flower, using a Constructor function.

...

<!-- 11:10 -->

Now we should have a flower instance for each of our actual flowers.

Let's source the best new properties that were created on their constructors and integrate them into a universal flower constructor.

<!--CFU Think-pair-share, think of three good ones, and say one so you have a backup -->

##Cross-Pollination

<!-- 11:15 -->

Now that we are awesome Flower experts, let's try our hand at cross pollinating two flower objects. Cross pollinating is beyond the realm of an individual flower and could therefore live on the Flower constructor itself. Another examples of this would be `create`, `new`, or `destroy`. These are all *meta* actions of a flower; a flower cannot create itself! They are called **static methods**.

<!-- CFU (as class), how might we declare this method?  Think-pair-share -->

To exemplify this let's create a static method (also sometimes refered to as a class method) called `crossPollinate` as opposed to the instance methods we've been making (e.g. `bloom`)
- The method will take two flower instances as arguments.    
- Return a new flower intance that is a mix of both "parent" colors. (i.e. red, yellow = "red-yellow"; we don't care about the color wheel).
- Make the new petal count an average between the two parents' petal counts.
- The smellPretty gene is recessive, unfortunately. This means that a flower will smell pretty IF and only IF both flowers smell pretty.  

<details>
<summary>Example solution</summary>

```javascript
// constructor
function Flower(color, petals, smells) {
    this.color = color;
    this.petals = petals;
    this.smells = smells;
}

// static methods
Flower.crossPollinate = function(momFlower, dadFlower) {
  var color = momFlower.color + "-" + dadFlower.color;
  var petals = (momFlower.petals + dadFlower.petals) / 2;
  var smells = momFlower.smells && dadFlower.smells;
  var babyFlower = new Flower(color, petals, smells);
  return babyFlower;
}

// instance methods
Flower.prototype = {
  bloom: function() {
    console.log("Look at me!");
  },
  smellsGood: function() {
    if (this.smells) {
      return 'This flower smells amazing!';
    } else {
      return 'What a noxious weed!';
    }
  },
  describe: function() {
    // Demonstrates use of local object variables
    // use `this` to access the instance's attributes
    console.log("This flower is " + this.color + ".");    
  }
}


var lily = new Flower("blue", 32, true);
var rose = new Flower("green", 12, true);

var rily = Flower.crossPollinate(rose, lily);

rily.smellsGood();
```

</details>

<!--11:30 -->

**Thought experiment:** *Maybe we create a different intermediary object, called Bee, which would facilitate cross-pollination and return a new flower? Flowers don't just bash their heads together and make new flowers in the real world, they need bees!  What are some methods we could assign to a Bee object?*


##Closing Thoughts
<!-- 11:40 -->

<!-- Closing: Almost everything in Javascript either is an object or inherits from an object.  As you walk around the outside world, start thinking "how could I put that think in JSON notation?".  What properties do people on the train have?  What about the train itself?  That's how most Javascript developers think, to one degree or another.  I want to create a game, or an app, how would I model all my objects? -->

* Why is using a prototype useful?
* Would you typically put the methods or attributes in the prototype?
* When would we use static methods?



<a name="introduction"></a>
## Introduction: Topic (# mins)

<a name="introduction"></a>
## Introduction: Topic (# mins)

<a name="introduction"></a>
## Introduction: Topic (# mins)

<a name="introduction"></a>
## Introduction: Topic (# mins)



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
	- JS Circuits - Constructor Notation - [Student Directory](https://generalassembly.wistia.com/medias/cjdt6hhkfz)
	- JS Circuits - Objects Past, Present & Future - [Date Object](https://generalassembly.wistia.com/medias/ga9vu35oz6)
	- JS Circuits - [Constructor vs. Literal Notation](https://generalassembly.wistia.com/medias/86ik38eakk)
	- [OOP Intro](https://generalassembly.wistia.com/medias/lahxav6p4z)
	- [OOP Case Study](https://generalassembly.wistia.com/medias/0bgiqqwd68)
	- [OOP Case Study #2](https://generalassembly.wistia.com/medias/lwjshtw79q)
- Readings
	- MDN - [Intro to OOP](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript)
	- [Object Oriented Analysis and Design with Applications, by Grady Booch and others](http://www.goodreads.com/book/show/424923.Object_Oriented_Analysis_and_Design_with_Applications)
	- [Great lecture notes](https://atomicobject.com/resources/oo-programming/introduction-motivation-for-oo)
	- [OOP in JS from JavascriptIsSexy](http://javascriptissexy.com/oop-in-javascript-what-you-need-to-know/)
	- [Javascript, The Good Parts](http://www.goodreads.com/book/show/2998152-javascript)
	- [Practical Object Oriented Design in Ruby, by Sandi Metz](http://www.poodr.com/)
- Decks

> Instructor Note: When possible, provide a brief description of Additional Resources, classifying whether it is for advanced or beginner students.  
