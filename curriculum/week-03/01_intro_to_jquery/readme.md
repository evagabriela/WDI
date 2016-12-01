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

In this lesson, you’ll learn about one of the most powerful tools in JavaScript: jQuery.

We'll see how jQuery simplifies common web development tasks and ensures that our code works in different browsers.




![](http://circuits-assets.generalassemb.ly/prod/asset/4738/Slide-3-jQuery.svg)

We’ll also take a look at how we can leverage jQuery to improve our workflow and write code that is clear and concise.

Plus, we’ll see how jQuery helps us manipulate the DOM, allowing us to perform complex manipulations while using less code.

![](http://circuits-assets.generalassemb.ly/prod/asset/4738/Slide-3-jQuery.svg)



Let's start by diving into a few of the benefits of jQuery.

![](http://circuits-assets.generalassemb.ly/prod/asset/4739/Slide-4-Benefits.svg)


## First Benefit: Cross-Browser Compatibility

![](http://circuits-assets.generalassemb.ly/prod/asset/4740/Slide-5-Benefit-1.svg)


jQuery solves many cross-browser compatibility issues.

When writing regular, or "plain vanilla" JavaScript, different browsers (Chrome, Safari, Firefox, Internet Explorer, etc.) handle the code in different ways.

As a result, code works differently in different browsers, and, in some cases, won’t work at all.




Because of this, developers often have to write "fallback" code for different browsers.

For example, in Internet Explorer (IE) versions 5-8, an event object is not automatically passed to event handler functions as it is in other browsers.

Instead, it’s available as a child of the window object, which requires developers to write fallback code.




Before we move forward, let’s get a quick refresher on what we learned about event objects in Unit 5.

Event objects allow us to access information about an event that has just occurred.




For example, say we wanted to discover the target of the event, or what type of event.

Was it a click event? A mouse-over?

The event object would allow us to easily find this information.




In the example below, the event object allows us see that we are preventing the browser from refreshing the page — its default behavior — when we click on an anchor.



![](http://circuits-assets.generalassemb.ly/prod/asset/4741/Slide-7-Code-Block.svg)


So, how do we deal with the fact that, in IE 5-8, the event object is not automatically passed to event handler functions like it is in other browsers?






To get around this discrepancy, we would need to provide an extra check and some "fallback" code in case the event object is not available:



![](http://circuits-assets.generalassemb.ly/prod/asset/4742/Slide-9-Code-Block.svg)




Here, you can see how our "fallback" code still allows us to access the event object in IE 5-8.



![](http://circuits-assets.generalassemb.ly/prod/asset/4743/Slide-10-Code-Block-Annotated.svg)


Obviously, it’s a bit of a hassle to constantly consider all of the different ways various browsers will handle your JavaScript.

Luckily, jQuery is here to make your life much, much easier.




When we use jQuery, we don't need to write fallback code because it automatically deals with the inconsistent ways browsers handle events.

To do this, jQuery uses feature detection to decipher the best way to complete a task. So, if a feature is available in a browser, it uses that feature. Otherwise, it will test to see if the browser supports the next best option and use that approach instead.

This allows us to write code without having to worry how it's handled from browser to browser.




## Second Benefit: Familiar Syntax

![](http://circuits-assets.generalassemb.ly/prod/asset/4744/Slide-13-Benefit-2.svg)




By this point, you might have noticed that JavaScript’s syntax can be a bit tricky to read, write, and remember.

For example, writing out `document.getElementById('important')` to find an element with the id important means creating a lot of code for a relatively simple task.




The jQuery library solves this by providing us with the `jQuery` function, which selects elements using our friendly CSS selector syntax.




It looks like this:

`jQuery('#important');`

Here again, we are finding the element with the ID `important`. Notice how, within the parentheses, we use the same syntax we would use to select an element with the ID `important` in CSS: `#important`

It’s a lot easier than `document.getElementById('important')`, right?






You can also use a `<div class="col" instead of writing out jQuery in the selector.

For example, `jQuery('#important')` can be written as `$('#important')`, with the `<div class="col" acting as the `jQuery` object.




    jQuery('#important') == $('important')




Let’s take a look at some more examples of selecting elements.






See how our jQuery selectors (all highlighted in red) resemble the selectors in our CSS (also highlighted in red)?

It makes for a much friendlier, more accessible system.



![](http://circuits-assets.generalassemb.ly/prod/asset/4747/Slide-16-Chart.svg)


And that's just the tip of the iceberg. We can use _any_ of the selectors we know and love from CSS as our jQuery selectors.

_Note: In the previous examples we used single quotations, but you can use double quotations if you like. It is simply a style preference, and it’s completely up to you._




## Third Benefit: More Concise Code

![](http://circuits-assets.generalassemb.ly/prod/asset/4746/Slide-16-Benefit-3.svg)


You probably already noticed this as we were walking through browser compatibility and familiar syntax, but one of the biggest benefits of jQuery is that it allows us to make our code much more concise.




Just how does jQuery do it? Let’s watch a video to learn more:



There are even more ways jQuery can help us keep our code concise.

jQuery allows us to chain methods together to accomplish our goals, making our code shorter and easier to understand.

We'll cover this more in Lesson 4, but for now, just take a look at an example:




## JavaScript

First, let's change the class name of the li to _task-complete_.

`document.getElementsByTagName('li')[0].className = 'task-complete';`

Then, let's change the background color of the li to _blue_.

`document.getElementsByTagName('li')[0].style.backgroundColor = "blue";`


## jQuery

Here, we can change the class name of the li to _task-complete_ and the background color to _blue_ — all in one line of code!

`$('li').addClass('task-complete').css('background-color', 'blue');`


By using the list item, we’re able to get as much out of one line of jQuery as we are out of two lines of JavaScript!




Let's look at that line of jQuery again:



    $('li').addClass('task-complete').css('background-color', 'blue');

Here, we added a class and changed the background color in one line.

When we have multiple methods updating an element at once, it’s called **method chaining**. Again, this is something we'll take a deeper dive into in Lesson 4.




Another way that jQuery allows us to shorten our code and improve our workflow is by making it infinitely easier to update multiple elements at once.




Let’s take a look and compare:

## JavaScript

![](http://circuits-assets.generalassemb.ly/prod/asset/4748/Slide-24-JS-Code.svg)

Here, we first had to select all elements with the class circle, and then loop through those elements to update each individually.

## jQuery

![](http://circuits-assets.generalassemb.ly/prod/asset/4749/Slide-24b-jQuery.svg)

Here, we selected all elements with the class _circle_ and updated them all at once.

Pretty cool, huh?




You might be wondering, is there ever a time when you should use "plain vanilla" JavaScript over jQuery in your project?

Let’s compare the benefits of both methods:

![](http://circuits-assets.generalassemb.ly/prod/asset/5140/Slide-25-Benefits.svg)


The main benefits of using pure JavaScript are its speed and performance.

## Speed

jQuery is a huge library. And, even if you’re not using _all_ of the features available, you still have to load in the entire library. jQuery adds another ~30kb to your response, which can slow the time it takes for a page to load.

This isn’t usually too big of a worry, but for large-scale projects, it's something to keep in mind. On some networks (and in some countries), using jQuery could mean adding a few more milliseconds to your load time.




## Performance

It can be easy to misuse jQuery.

For example, using jQuery's each loop (which we'll cover in a future lesson) instead of pure JavaScript for loops can sometimes be unnecessary and could have a negative impact on performance.

When working on a project, it's always worthwhile to think through the most efficient way to achieve a task. Don’t worry—when we cover methods that may be easily misused in future lessons, we'll be sure to highlight their proper use cases.




In this lesson, we took a look at some of the major benefits that using jQuery can have on our workflow.

![](http://circuits-assets.generalassemb.ly/prod/asset/4751/Slide-28-Benefits.svg)


## Benefit #1

We saw how "plain vanilla" JavaScript is often handled differently by different browsers, and how jQuery solves many of those cross-browser compatibility issues.

When using jQuery, we can rest assured that our code will function similarly in different browsers, which will save countless hours of tedious browser testing.




## Benefit #2

We also saw how jQuery's syntax for selecting elements closely resembles the CSS-style syntax we already know and love:

Selecting an element by its ID in JavaScript:

`document.getElementById('important')`

Selecting an element by its ID in jQuery:

`$('#important')`

Much easier, right?




## Benefit #3

Finally, we took a look at how jQuery's syntax can make our code much more concise. One line of jQuery can accomplish something that would require multiple lines of JavaScript.

Here are just a few of the areas where jQuery will allow us to write less code:

*   Selecting elements
*   Writing methods
*   Achieving multiple tasks with one element
*   Updating multiple elements at once




Hopefully all of this has gotten you excited about harnessing the power of jQuery while working on your own projects.

In the next lesson, we'll dig in and begin to write with jQuery. Are you ready?



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
