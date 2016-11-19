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

> Instructor Note: Use instructor notes to talk directly to instructors. Otherwise, write out lesson directions and materials in a student-facing voice.

Check: Ask students to define, explain, or recall any **general** prior concepts or tools.

***

<section>

<div class="slide-grid">

<div class="col-centered">

In order to create interactive and responsive sites, we'll often want to update the DOM based on our user's actions.

For example, when a user clicks on our site’s menu icon, a sidebar menu should slide out from the side of the page. Or, if a user types an incorrect format into a form field, that field should become outlined in red.

These actions are called **events**.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col">

Take a look at this GIF.

Here, we can see a cursor scroll over to the hamburger menu on the top left, where a sidebar menu appears

</div>

<div class="col">

<center>![](http://circuits-assets.generalassemb.ly/prod/asset/4723/click_1.gif)</center>

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

JavaScript is different than most other programming languages because it is designed specifically to work in the event-driven environment of a browser window.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

JS is not just executed line by line and then forgotten. When a browser loads HTML and CSS, it then uses its interpreter to run your JavaScript.

Once your JS has fully loaded, it lives in the background of your browser window, waiting and listening for any event triggers you’ve programmed.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

As its name implies, in event-driven programming, the flow of a program is driven by events.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

This means:

*   The program continually "waits" or listens for events to occur.

*   There are many kinds of events, such as clicking, tabbing into a form field, pressing a computer key down or letting a computer key up, scrolling, resizing the browser window, etc. We'll take a look at some of these events later in this lesson.

*   The event acts as a “trigger,” which calls, or runs, a function.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Event loops are an important part of event-driven programming.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

The browser is continually checking to see if an event has occurred. When it does happen, the event loop uses a trigger function to identify which code to run.

So, if someone clicks on a menu option, what should the program do?

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

It should run an event handler.

These are pieces of code that will run once an event occurs. If someone clicks on a button or menu option, the event handler kicks in.

![](http://circuits-assets.generalassemb.ly/prod/asset/4616/Slide-8-Event-Loop.svg)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

There are many benefits of working within an event-driven system.

For one, when you’re programming around events, coding becomes somewhat intuitive (i.e., you wait for user take an action, and then you **respond** to that action).

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Let’s look at another example in the GIF below.

Here we are **waiting for the user to scroll**. When the user does scroll, we run a function that changes the background color of the navigation bar (nav) and fixes its position so that it "sticks" to the top of the screen.

![](http://circuits-assets.generalassemb.ly/prod/asset/4656/Slide-10.gif)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

So, how do we set up, or write, event handlers?

We mentioned previously that we can set up **event handlers** in our scripts that will listen, or wait, for an event to occur and then trigger a function.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

The syntax for setting up an event handler looks like this:

![](http://circuits-assets.generalassemb.ly/prod/asset/5363/Slide-12-Element.svg)

`element` - refers to the DOM node with which we want to tie the event. For example, if we want to trigger an event when the user clicks on a button, the element would be that button element.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

The syntax for setting up an event handler looks like this:

![](http://circuits-assets.generalassemb.ly/prod/asset/4618/Slide-13-Dot.svg)

`.` - ties the method on the right hand side (addEventListener) with the element on the left hand side.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

The syntax for setting up an event handler looks like this:

![](http://circuits-assets.generalassemb.ly/prod/asset/4619/Slide-14-addEventListener.svg)

`addEventListener()` - is the method we will use to tie an event listener to an element.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

The syntax for setting up an event handler looks like this:

![](http://circuits-assets.generalassemb.ly/prod/asset/5138/Slide-15-nameOfEvent.svg)

`'nameOfEvent'` - is of the event for which we want to listen. For example, maybe we want to wait until the user triggers a 'click' event.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

The syntax for setting up an event handler looks like this:

![](http://circuits-assets.generalassemb.ly/prod/asset/5139/Slide-16-functionToRun.svg)

`'functionToRun'` - is the name of the function we want to run when the event occurs. When we pass a function as an argument to another function, like we are here, this is what is referred to as a **callback function**.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

_Note that there are no parentheses after the function name._  
( `functionToRun` not `functionToRun()` )

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Let's take a look at an example of an event handler:

    // Let's set up a function that will be triggered when the event occurs.
    var alertUser = function () {
      alert('Button has been clicked!');
    }

    // Next let's find the element we want to tie
    //the event to and save it to a variable.
    var button = document.querySelector('button');

    // Finally let's set up an event handler.
    // When the user clicks on the button,
    // the alertUser function will run.
    button.addEventListener('click', alertUser);

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

There are many events that can trigger a function. Here are a few:

</div>

![](http://circuits-assets.generalassemb.ly/prod/asset/4622/Slide-18-Chart.svg)

'focus' - When the user clicks or tabs into a form field and it receives focus 'blur' - When the user clicks or hits tab away from a form field and it loses focus

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

To start, we'll look at another example of an event handler.

Say we've created a simple form that allows users to subscribe to our email newsletter.

When the user tabs or clicks away from the email input field, we want to make sure the user has entered a value in the field.

Move on to the next slide to take a look at the code for our email newsletter.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-small">

Here, we have a simple HTML snippet of an email form.

</div>

<div class="col-large">

<center>![](http://circuits-assets.generalassemb.ly/prod/asset/4623/Slide-20-HTML.svg)</center>

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-small">

The form contains an input field where the user can enter an email address, a button for submitting the form, and a paragraph with the id _message_ that currently does not have any text inside of it.

</div>

<div class="col-large">

<center>![](http://circuits-assets.generalassemb.ly/prod/asset/4623/Slide-20-HTML.svg)</center>

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-small">

Our stylesheet (on the right side of the image) is also very basic.

All we have is a class _error_, which will give a solid red border to any elements that have the _error_ class.

</div>

<div class="col-large">![](http://circuits-assets.generalassemb.ly/prod/asset/4624/Slide-21-CSS.svg)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Take a look at the code for our email newsletter:

</div>

![](http://circuits-assets.generalassemb.ly/prod/asset/4625/Slide-22-JS.svg)</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

On the right, we've added our JS using event handlers.

</div>

![](http://circuits-assets.generalassemb.ly/prod/asset/4625/Slide-22-JS.svg)</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Let's take a look at what the page looks like when the user hits tab or clicks away from the email field without entering any information.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col">

The email input now has the _error_ class, giving the input field a red border.

We've also added a message in the paragraph with the id _message_ alerting the user they need to enter an email address.

</div>

<div class="col">![](http://circuits-assets.generalassemb.ly/prod/asset/4626/Slide-24-Email-Form.svg)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

It’s time to test yourself.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col">

      Red
      Blue
      Yellow

</div>

<div class="col">

    function turnRed () {
      document.querySelector('body').style.backgroundColor = "red";
    }
    function turnBlue () {
      document.querySelector('body').style.backgroundColor = "blue";
    }
    function turnYellow () {
      document.querySelector('body').style.backgroundColor = "yellow";
    }

</div>

<div class="col-centered">

How would we add event handlers to:

Run the turnRed function when the #red element is clicked?

Answer:

    document.querySelector('#red').addEventListener('click', turnRed);

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col">

      Red
      Blue
      Yellow

</div>

<div class="col">

    function turnRed () {
      document.querySelector('body').style.backgroundColor = "red";
    }
    function turnBlue () {
      document.querySelector('body').style.backgroundColor = "blue";
    }
    function turnYellow () {
      document.querySelector('body').style.backgroundColor = "yellow";
    }

</div>

<div class="col-centered">

How would we add event handlers to:

Run the turnBlue function when the #blue element is clicked?

Answer:

    document.querySelector('#blue').addEventListener('click', turnBlue);

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col">

      Red
      Blue
      Yellow

</div>

<div class="col">

    function turnRed () {
      document.querySelector('body').style.backgroundColor = "red";
    }
    function turnBlue () {
      document.querySelector('body').style.backgroundColor = "blue";
    }
    function turnYellow () {
      document.querySelector('body').style.backgroundColor = "yellow";
    }

</div>

<div class="col-centered">

How would we add event handlers to:

Run the turnYellow function when the #yellow element is clicked?

Answer:

    document.querySelector('#yellow').addEventListener('click', turnYellow);

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

In this lesson, we learned how we can react to our users' actions when they visit our site.

We saw how we can harness JavaScript's event handling to wait until the user takes an action — like clicking on a button or scrolling down the page — and then run a block of code, or a function, when this event occurs.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

In the next lesson, we'll dive even deeper into handling events. This will allow us to further control the flow of events on our sites.

</div>

</div>

</section>





<section>

<div class="slide-grid">

<div class="col-centered">

In the last lesson we took a look at how we can program events to occur automatically, or wait until our users do something and then run some code in response.

Now we’re going to take a closer look at events, and see how we can run multiple functions when one occurs.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Let’s start off by talking more about event handler callbacks.

As we saw in a previous unit, the keyword `this` refers to the object that "owns" the function that the executed code runs within.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

It’s important to remember that when we have a method that is inside an object, `this` refers to the object that contains that method.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

For example, in the function below, `this` refers to the object that contains the makeNoise method, rover.

    var rover = {
      name: 'Rover',
      species: 'dog',
      breed: 'Golden Retreiver',
      noise: 'bark',
      makeNoise: function () {
        console.log(this.noise);
      }
    }

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

However, when a callback function is executed within the context of an event handler, it is the element (the DOM node) that owns the context.

So in this case, `this` will refer to the element that we selected when we set up our event handler.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Let’s look at an example where we’ll change the background color of a circle from blue to red, just by clicking on it:

![](http://circuits-assets.generalassemb.ly/prod/asset/4627/Slide-7a-HTML-JS.svg)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Let’s look at an example where we’ll change the background color of a circle from blue to red, just by clicking on it:

![](http://circuits-assets.generalassemb.ly/prod/asset/4628/Slide-7b-HTML-JS-Annotated.svg)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Here when we click on the circle and trigger the turnRed function, `this` will refer to the element with the class `circle` within the `turnRed` function.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Here’s what that looks like in action:

![](http://circuits-assets.generalassemb.ly/prod/asset/4629/Slide-8.gif)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Alright, but why use the keyword `this`:

`this.style.backgroundColor = "red";`

Instead of just writing:

`document.querySelector('.circle').style.backgroundColor = "red";`</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Well, let's imagine that there are several circles on our page:

And we only want the `.circle` that we just clicked to have the updated red background color. That is where the `this` keyword really becomes useful.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Let’s take a look:

    //Select all elements with the class .circle on the page
      var circles = document.querySelectorAll('.circle');

    //loop through each .circle element and add an event handler.
      for (var i = 0; i < circles.length; i++) {
        circles[i].addEventListener('click', turnRed);
      }

      function turnRed () {
        this.style.backgroundColor = "red";
      }

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Here we are adding an event handler to each element with the class `.circle`.

When an element with the `.circle` class gets clicked, the `turnRed` function will be called; within that `turnRed` function, `this` will only refer to the `.circle` that triggered the `turnRed` function and not to any of the other circles.

So now only the background color of the circle **we just clicked** will be changed to red.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Let's see this in action:

![](http://circuits-assets.generalassemb.ly/prod/asset/4630/Slide-11.gif)

See how we are only adding the style attribute to the circle we are currently clicking on (i.e., the one that triggered the callback function)? Pretty cool, huh?

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Now it’s your turn to test yourself.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

      Blue Jeans
      Denim
      Chambray
      Dark Wash
      Light Wash

How could we write code that would change the text of any list item that is clicked to "Forever!"? Start by writing code to select all list items on the page.

Click on the next slide to reveal the answer when you’re ready.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Did your code look something like this?

    var listItems = document.querySelectorAll('li');

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Now loop through each list item and add a handler that runs a function called _sayForever_.

Click on the next slide to reveal the answer when you’re ready.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Here’s the answer:

    for (var i = 0; i < listItems.length; i++) {
      listItems[i].addEventListener('click', sayForever);
    }

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Now you need to define a _sayForever_ function. From within the function it should change the innerHTML of the item that was just clicked to _“Forever!”_.

(Hint: make sure to use the _this_ keyword)

Click on the next slide to reveal the answer when you’re ready.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Ready? Here’s the answer:

    function sayForever () {
      this.innerHTML = "Forever!";
    }

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

There may be instances where we want to trigger multiple functions when an event occurs.

For example, maybe when our user clicks the "submit" button we want to run a function that will check to see if the form is valid and call another function that will display a "loading" icon.

In a case like this, we’d have multiple event handlers for one event.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

To trigger multiple functions, first define the functions that you want to be called when our event occurs.

For example, on the next slide, we define two functions: showLoadingIcon() and checkEmailInput().

</div>

</div>

</section>

<section>

<div class="slide-grid">

    function showLoadingIcon() {
      document.getElementById('loading').style.display = "block";
    }
    function checkEmailInput() {
      var emailInputField = document.querySelector('input');
        // Check to see whether the user has entered a value to the email field.
        if (emailInputField.value.length === 0) {
          // If the email field is blank, display a message to the user.
          document.getElementById('message').innerText = 'Please enter an email address.'
          // Add an error class to the input field that will give it a red border.
          emailInputField.className = 'error';
        } else {
          // Otherwise, clear out the error message.
          document.getElementById('message').innerText = '';
          // Remove the error class from the input field
          emailInputField.className = '';
        }
    }

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Alternatively, you could write something like this, which should still get the point across:

</div>

    function showLoadingIcon() {
      // Code to show the loading icon
    }

    function checkEmailInput() {
      // Code that checks to see if the user entered an email address
      // And adds a red border to the input and an error message if not.
    }

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

We’ll then need to define a third function, which will contain the previous two functions:

    function submitForm() {
      showLoadingIcon();
      checkEmailInput();
    }

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Finally, we’ll assign that third function as the event handler:

</div>

    document.getElementById('submit').addEventListener('click', submitForm);

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Lets recap the steps before we move on:

1.  Start with input and button elements.

3.  Attach an event listener to the button.

5.  Invoke two functions within the event handler.

*   The first function showed the loading icon.
*   The second function validated the email address.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Now that we've gotten the hang of writing event handlers, let’s talk a bit about the event object.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

When an event occurs, we might want to find out some information about it.

For example, which element did the user interact with that caused the event? What type of event was it? A click event? A mouseover?

Luckily, we can use the event object to obtain this kind of information.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

So how do we gain access to the event object?

First, we will need to pass the event object as a parameter.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Take a look at this example:

![](http://circuits-assets.generalassemb.ly/prod/asset/4631/Slide-25-Code.svg)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Let's break this down a bit:

![](http://circuits-assets.generalassemb.ly/prod/asset/4632/Slide-26-Annotated.svg)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Now if we simply use whichever parameter name we chose (in our case “e”) from within the function, we have access to the event object.

Take a look at what the event object looks when you log it to the console, and notice all of the properties we have available to us as part of the event object:

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">![](http://circuits-assets.generalassemb.ly/prod/asset/4633/Slide-27-Codeblock.svg)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

We'll take a look at a few of these properties in the following slides, but for now just note how much information about the event the event object holds.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

We can use dot notation to access those properties, just like we did in Unit 4:

</div>

    document.querySelector('a').addEventListener('click', turnBlue);

      function turnBlue (e) {
        // To access a property of the event object, we can use dot notation:
          var target = e.target;

          // Log the target to the console
          console.log(target);

          document.querySelector('body').style.backgroundColor = "blue";
    }

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Here we are accessing the target of the event by using dot notation `e.target`. We are then logging the target to the console.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Let's take a look at what we see in the console:

<a href="#">Turn Blue</a>

Aha! That's the target of the event, or the element we clicked on that caused the event to fire.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Or maybe we want to find out what type of event it was. We can find that out by using the type property. Here we are accessing the type of event using `e.type`. Take a look:

</div>

    document.querySelector('a').addEventListener('click', turnBlue);

    function turnBlue (e) {
      // To access a property of the event object, we can use dot notation:
      var typeOfEvent = e.type;

      // Log the type to the console
      console.log(typeOfEvent);

      document.querySelector('body').style.backgroundColor = "blue";
    }

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

And here's what we see in the console: `click`

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Now let’s discuss another important use of the event object—**Prevent Default**.

As you may be able to tell from its name, prevent default allows us to prevent the default behavior of an event.

Some events, like clicking on a link or submitting a form, are meant to take a user to another page.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-small">

Like in the example to the right — when an anchor is clicked, the default action will take the user to another page.

If no URL is specified, the page will simply load at the top.

</div>

<div class="col-large">  

<center>![](http://circuits-assets.generalassemb.ly/prod/asset/4635/Slide-34.gif)</center>

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-small">

But maybe when a user clicks on a link or submits a form, we don't want to take them to another page.

We want to make some text appear instead.

</div>

<div class="col-large">  

<center>![](http://circuits-assets.generalassemb.ly/prod/asset/4635/Slide-34.gif)</center>

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

To do that, we could type:

</div>

    // Here we are adding a click event to the first anchor on the page.
      // When the anchor is clicked, we will run the addMessage function.

      document.querySelector('a').addEventListener('click', addMessage);

      function addMessage () {
        // When the addMessage function runs, we will display a message   for the user.
        document.querySelector('.message').innerHTML = 'A message for the user!';
    }

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-small">

Our message is added at the bottom like we had intended, but we don't want the page to jump to the top!

</div>

<div class="col-large">![](http://circuits-assets.generalassemb.ly/prod/asset/4635/Slide-34.gif)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

We want to override the default functionality of a link, and have a message appear instead of taking the user to another page.

But as you saw in the GIF, when the user clicks on an anchor that doesn’t have a specified URL, the page jumps up to the top.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

To prevent this default behavior, we can use the `preventDefault()` method:

</div>

    document.querySelector('a').addEventListener('click', addMessage);

    function addMessage (e) {
    // Now we are preventing the default behavior, using the event object and the .preventDefault() method.
      e.preventDefault();
      document.querySelector('.message').style.display = 'block';
    }

<div class="col-centered">

Here again, we’re passing the event object as a parameter to our callback function.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Notice how within the function, we called the preventDefault method on the event object using dot notation:

`e.preventDefault();`</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-small">

Let's take a look at the result:

</div>

<div class="col-large">![](http://circuits-assets.generalassemb.ly/prod/asset/4636/Slide-37.gif)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

You'll often use this method when you have anchors or submit buttons on a page that you want to provide with some JavaScript functionality, instead of having them take you to another page.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Now that we have a good feel for what the event object is, let's go ahead and look at a concept that is central to event handling in JavaScript: event flow.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

We've seen in the past that HTML elements can be nested inside other HTML elements. When we say "nested", we mean that one element can wrap another element.

Take a look at a quick refresher:

    Popular memes for 2016

      Hotline Bling
      Katy Perry's Left Shark
      Lil Mama Crying
      Pizza Rat
      What's Good?

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Here we have a `ul` that is wrapping five `li`. Each `li`, in turn, is wrapping an anchor.

In other words, we could say that each `a` is nested inside of an `li`, and each `li` is nested inside the `ul`.

    Popular memes for 2016

      Hotline Bling
      Katy Perry's Left Shark
      Lil Mama Crying
      Pizza Rat
      What's Good?

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

When we hover over an anchor and click on it, JS can trigger any events that are tied to the anchor, as well as any events that are tied to any elements the `a` is nested within (i.e., the `li` it sits within, the `ul` it is also nested within).

If we zoom out a bit and remember the DOM tree, we will remember that our `ul` is nested inside the `body`, which is nested inside the `html`, which is nested inside the document object.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Events that are bound to any of these elements will trigger when we click on the `a`.

![](http://circuits-assets.generalassemb.ly/prod/asset/5152/Screen_Shot_2016-08-08_at_10.02.00_AM.png)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

The order in which these events fire is called **event flow**.

**Event bubbling** is when the event starts at the most specific element node and then flows outwards towards the least specific node.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col">

<center>![](http://circuits-assets.generalassemb.ly/prod/asset/4637/Slide-42-Event-Bubbling.svg)</center>

</div>

<div class="col">

Here the event will start at the `a`, the most specific node, and then work its way outward, triggering any events that might be tied to the `li`, then the `ul`, then the `body`, then finally, the `document` (in this case, the HTML doc).

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Why does this matter?

Understanding event flow comes into play when the code has event handlers that are tied to the element that triggers the event and any of its ancestors or descendants.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col">

Take a look at our example from before. We've gone ahead and tied an event handler to the `a`, `li`, `ul`, `body` and `document` elements that appends a paragraph element to the body that states "[element name] has been clicked"

</div>

<div class="col">![](http://circuits-assets.generalassemb.ly/prod/asset/4638/Slide-45.gif)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Notice in the previous slide the order in which those messages are appended to the body: "Anchor has been clicked" is appended first, and "Document has been clicked" is appended last, since the events are flowing outwards from the most specific element.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

The key concept here is that events are triggered not only for the element that we tie the event handler to, but also for any elements that element is nested inside of.

The flow in which these events happens is from the most specific element to the least specific element (outwards in the diagram).

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Now let’s talk about `stopPropagation()`.

There may be instances where we don't want an event to bubble up to its ancestors.

If we want to stop this behavior, we can use the event object's `stopPropagation()` method to prevent this bubbling.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Let’s take a look:

</div>

    function addAnchorMessage (e) {
      e.stopPropagation();
      document.querySelector('body').appendChild = 'Anchor has been clicked';

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Here again we pass in the event object as a parameter, “e”.

We then access the `stopPropagation()` method using dot notation. This prevents the event from bubbling up to any ancestors.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col">

Now when we click on an anchor, we don't see messages being appended for each ancestor element since those events are no longer being triggered:

</div>

<div class="col">![](http://circuits-assets.generalassemb.ly/prod/asset/4639/Slide-50.gif)</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

This is just one more helpful use of the event object!

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Now you understand a bit more about event flow and how multiple event handlers may be triggered on any ancestor elements.

We took a look at how the flow of events happens—from the most specific, or target, element outwards to the least specific ancestor element.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Having a grasp on this flow will be immensely helpful in the future when you’re working on complex interactions and trying to understand the order in which events will happen.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

We’ve covered quite a bit in this lesson.

We took a look at how we can trigger multiple functions on one event by calling each function from within a callback function.

We also saw how we can use the keyword this to access the individual element that caused an event to fire.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

We learned that we can gain access to the event object by passing it in as a parameter to a callback function. This gives us access to the properties and methods tied to the event object from within that callback function.

And finally, we saw how events flow from the most specific element to the least specific element.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Up until this point we've been writing things out in "plain vanilla" JavaScript.

In the next lesson we'll take a look at how we can harness the power of jQuery to write JavaScript that will work in different browsers, in a much friendlier syntax.

</div>

</div>

</section>

<section>

<div class="slide-grid">

<div class="col-centered">

Take a peek and get excited to meet your new best friend, jQuery:

![](http://circuits-assets.generalassemb.ly/prod/asset/4640/Slide-54-JS-jQ.svg)</div>

</div>

</section>

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

