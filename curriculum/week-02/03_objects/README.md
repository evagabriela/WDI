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

> Instructor Note: Use instructor notes to talk directly to instructors. Otherwise, write out lesson directions and materials in a student-facing voice.

Check: Ask students to define, explain, or recall any **general** prior concepts or tools.

***

<a name="introduction"></a>
## Introduction: Topic (# mins)


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
