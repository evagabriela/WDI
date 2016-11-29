# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) jQuery vs. JavaScript (60 mins)
<!--
ID NEEDED: Following the morning exercise template here, but think it might be useful to have a little more structure. Let me know if this should be formatted differently!
-->
## Overview
- In this morning's session, we'll be we'll be exploring the difference between jQuery and JavaScript and the benefits to using the jQuery library, vs. "Plain Vanilla" JavaScript.

## Independent Practice - jQuery vs. JavaScript (15 mins)
- Research the difference between jQuery and JavaScript. 
- See if you can find at least two benefits of using each

## Introduction (5 mins)
Today, you’ll learn about one of the most powerful tools in JavaScript: jQuery.

We'll see how jQuery simplifies common web development tasks and ensures that our code works in different browsers.

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4738/Slide-3-jQuery.svg" width="250px">

We’ll also take a look at how we can leverage jQuery to improve our workflow and write code that is clear and concise.

Plus, we’ll see how jQuery helps us manipulate the DOM, allowing us to perform complex manipulations while using less code.


Let's start by diving into a few of the benefits of jQuery.


## First Benefit: Cross-Browser Compatibility (10 mins)

<br>

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4740/Slide-5-Benefit-1.svg" width="300px">

jQuery solves many cross-browser compatibility issues.

When writing regular, or "plain vanilla" JavaScript, different browsers (Chrome, Safari, Firefox, Internet Explorer, etc.) handle the code in different ways.

As a result, code works differently in different browsers, and, in some cases, won’t work at all.


#### Fallback Code
Because of this, developers often have to write "fallback" code for different browsers.

For example, in Internet Explorer (IE) versions 5-8, an event object is not automatically passed to event handler functions as it is in other browsers.

Instead, it’s available as a child of the window object, which requires developers to write fallback code.

So, how do we deal with the fact that, in IE 5-8, the event object is not automatically passed to event handler functions like it is in other browsers?

To get around this discrepancy, we would need to provide an extra check and some "fallback" code in case the event object is not available:

![](http://circuits-assets.generalassemb.ly/prod/asset/4742/Slide-9-Code-Block.svg)


Here, you can see how our "fallback" code still allows us to access the event object in IE 5-8.

![](http://circuits-assets.generalassemb.ly/prod/asset/4743/Slide-10-Code-Block-Annotated.svg)


Obviously, it’s a bit of a hassle to constantly consider all of the different ways various browsers will handle your JavaScript.

#### Feature Detection
Luckily, jQuery is here to make your life much, much easier.

When we use jQuery, we don't need to write fallback code because it automatically deals with the inconsistent ways browsers handle events.

To do this, jQuery uses feature detection to decipher the best way to complete a task. So, if a feature is available in a browser, it uses that feature. Otherwise, it will test to see if the browser supports the next best option and use that approach instead.

This allows us to write code without having to worry how it's handled from browser to browser.


## Second Benefit: Familiar Syntax (5 mins)

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4744/Slide-13-Benefit-2.svg" width="300px">

By this point, you might have noticed that JavaScript’s syntax can be a bit tricky to read, write, and remember.

For example, writing out `document.getElementById('important')` to find an element with the id important means creating a lot of code for a relatively simple task.

The jQuery library solves this by providing us with the `jQuery` function, which selects elements using our friendly CSS selector syntax.

It looks like this:

```js
jQuery('#important');
```

We'll take a deeper look at this syntax later today, but for now just focus on getting an overview.

Here again, we are finding the element with the ID `important`. Notice how, within the parentheses, we use the same syntax we would use to select an element with the ID `important` in CSS: `#important`

It’s a lot easier than `document.getElementById('important')`, right?

You can also use a `$` instead of writing out jQuery in the selector.

For example, `jQuery('#important')` can be written as `$('#important')`, with the `<div class="col" acting as the `jQuery` object.

```js
jQuery('#important') == $('important')
```

Let’s take a look at some more examples of selecting elements.

See how our jQuery selectors (all highlighted in red) resemble the selectors in our CSS (also highlighted in red)?

It makes for a much friendlier, more accessible system.

![](http://circuits-assets.generalassemb.ly/prod/asset/4747/Slide-16-Chart.svg)


And that's just the tip of the iceberg. We can use _any_ of the selectors we know and love from CSS as our jQuery selectors.

_Note: In the previous examples we used single quotations, but you can use double quotations if you like. It is simply a style preference, and it’s completely up to you._


## Third Benefit: More Concise Code (10 mins)

<img src="http://circuits-assets.generalassemb.ly/prod/asset/4746/Slide-16-Benefit-3.svg" width="300px">


You probably already noticed this as we were walking through browser compatibility and familiar syntax, but one of the biggest benefits of jQuery is that it allows us to make our code much more concise.


Just how does jQuery do it? Let’s watch a [video](https://generalassembly.wistia.com/medias/qb34u4qxc1) to learn more.


There are even more ways jQuery can help us keep our code concise.

#### Method Chaining

jQuery allows us to chain methods together to accomplish our goals, making our code shorter and easier to understand.

We'll cover this more in a later lesson, but for now, just take a look at an example:


##### JavaScript

First, let's change the class name of the li to _task-complete_.

```js
document.getElementsByTagName('li')[0].className = 'task-complete';
```

Then, let's change the background color of the li to _blue_.

```js
document.getElementsByTagName('li')[0].style.backgroundColor = "blue";
```


##### jQuery

Here, we can change the class name of the li to _task-complete_ and the background color to _blue_ — all in one line of code!

```js
$('li').addClass('task-complete').css('background-color', 'blue');
```


By using the list item, we’re able to get as much out of one line of jQuery as we are out of two lines of JavaScript!

When we have multiple methods updating an element at once, it’s called **method chaining**. Again, this is something we'll take a deeper dive into in a later lesson.

#### Updating Multiple Elements at Once

Another way that jQuery allows us to shorten our code and improve our workflow is by making it infinitely easier to update multiple elements at once.

Let’s take a look and compare:

##### JavaScript

![](http://circuits-assets.generalassemb.ly/prod/asset/4748/Slide-24-JS-Code.svg)

Here, we first had to select all elements with the class circle, and then loop through those elements to update each individually.

##### jQuery

![](http://circuits-assets.generalassemb.ly/prod/asset/4749/Slide-24b-jQuery.svg)

Here, we selected all elements with the class _circle_ and updated them all at once.

Pretty cool, huh?

## Benefits of Plain Vanilla JavaScript (10 mins)
You might be wondering, is there ever a time when you should use "plain vanilla" JavaScript over jQuery in your project?

Let’s compare the benefits of both methods:

![](http://circuits-assets.generalassemb.ly/prod/asset/5140/Slide-25-Benefits.svg)


The main benefits of using pure JavaScript are its speed and performance.

#### Speed

jQuery is a huge library. And, even if you’re not using _all_ of the features available, you still have to load in the entire library. jQuery adds another ~30kb to your response, which can slow the time it takes for a page to load.

This isn’t usually too big of a worry, but for large-scale projects, it's something to keep in mind. On some networks (and in some countries), using jQuery could mean adding a few more milliseconds to your load time.


#### Performance

It can be easy to misuse jQuery.

For example, using jQuery's each loop (which we'll cover in a future lesson) instead of pure JavaScript for loops can sometimes be unnecessary and could have a negative impact on performance.

When working on a project, it's always worthwhile to think through the most efficient way to achieve a task. Don’t worry—when we cover methods that may be easily misused in future lessons, we'll be sure to highlight their proper use cases.


## Conclusion (5 mins)

In this lesson, we took a look at some of the major benefits that using jQuery can have on our workflow.

Let's take a look at this [video](https://generalassembly.wistia.com/medias/rlslgthvo3) summarizing the benefits of using jQuery.

Hopefully all of this has gotten you excited about harnessing the power of jQuery while working on your own projects.

In the next lesson, we'll dig in and begin to write with jQuery. Are you ready?