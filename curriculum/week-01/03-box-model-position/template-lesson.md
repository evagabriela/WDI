---
# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Box Model and Positioning (90 mins)

| Timing | Type | Topic |
| --- | --- | --- |
| x min | [Introduction](#introduction) | Box Model |
| x min | [Demo/Codealong](#demo) | Topic |
| x min | [Guided Practice](#guided-practice) | Topic |
| x min | [Independent Practice](#ind-practice) | Topic |
| x min | [Conclusion](#conclusion) |Topic |

### LEARNING OBJECTIVES
*After this lesson, you will be able to:*
- Use the Box Model to style element borders and structure your page
- Understand the value of box-sizing: border-box; and apply it to the page layout as needed
- Adjust element spacing using padding and margin 
- Describe the difference between block, inline, and inline-block elements
- Explain the difference between and use cases of static, relative, fixed, & absolute positioning

### STUDENT PRE-WORK
*Before this lesson, you should already be able to:*
- Style all elements of a particular HTML element on a web page 
- Understand best practice for specificity and cascading
- Apply styles to specific elements using classes and IDs
- Pass The Validator without errors

---
<a name="opening"></a>
## Opening (10 mins)
- Review pre-work, projects, or exit ticket, if applicable
- Review current lesson objectives
- Reference general course content or topics (e.g. code or concepts that have been used across multiple lessons)
- Include Hook / Real-world Relevance (why the content from this lesson is useful or important)

> Instructor Note: Use instructor notes to talk directly to instructors. Otherwise, write out lesson directions and materials in a student-facing voice.

Check: Ask students to define, explain, or recall any **general** prior concepts or tools.

***

<a name="introduction"></a>
## Introduction: Box Model (5 mins)

All HTML elements can be considered boxes. Even if you see a circle, it's living within a box.

The CSS box model describes this principle - a box wraps around all HTML elements, and it consists of: margins, borders, padding, and the actual content. This model allows us to place a border around elements and space elements in relation to other elements. With CSS properties and values, it is possible to apply specific styles to each of these elements, and change the way they behave and/or display on the page.

#### Layout: Turn & Talk (5 mins)
Install the <a href="https://chrome.google.com/webstore/detail/pesticide-for-chrome/bblbgcheenepgnnajgfpiicnbbdmmooh">Pesiticide Chrome Extension</a>, which visualizes all DOM elements as boxes. Work with a parter to investigate a few different sites using the extension, and discuss how the Box Model might help you to control layout.


***

<a name="demo"></a>
## Demo / Codealong: Box Model (# mins)
Let's write some code to help us visualize the Box Model. Paste the following into Codepen.

```html
<header>
  <h1>Box Model Pro</h1>
  <nav>
    <a href="#">About</a>
    <a href="#">Demo</a>
    <a href="#">Contact</a>
  </nav>
</header>

<div>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iusto commodi aspernatur quae possimus! Veritatis ad libero maiores. Assumenda quae <a href="#">perspiciatis</a> dolore voluptatem porro optio eos, nemo et eligendi, voluptatum necessitatibus.</p>
</div>
```

```css
body{
  font-family:Georgia, serif;
}

header{
  text-align:center;
}

nav a{
  margin:1em;
  text-transform:uppercase;
}

h1{
  font-size:3em;
}

p{
  font-size:1em;
  line-height:1.618em;
}

a{
  font-weight:bold;
  color:inherit;
  text-decoration:none;
}
```

Dynamite! Now, navigate to your dev tools and under the elements tab, hover over each of the elements. What do you notice? A "box" is being highlighted in your browser!

What happens when we drop this code into the CSS file?

```css
* {
    border: 1px solid red !important;
}
```

The universal selector ```*{ }``` is a great way to apply a style to every element on the page *without* using inhertiance. We'll teach you more about this selector in a later lesson. For now, it helps us see the boundaries of different elements. Pay special attention to how much space elements take up on the page, and how that space differs for block and inline elements. 

### Box Model Components
The image below illustrates the box model and what you should have seen in your dev tools:

*INSERT IMAGE*

But what do these different layers mean, and how are they relating to one another?
- Margin: clears an area around the border (or boundaries of the padding if no border); the margin does not have a background color, it is completely transparent
- Border: a border that goes around the padding and content; the border is affected by the background color of the box unless a color is declared
- Padding: clears an area around the content; the space between the content and the border; the padding is affected by the background color of the box
- Content: the content of the box, where text and images appear

Let's get go into some more detail and practice with each of these elements of The Box Model.

*Margin*
The margin is the space around the element. The larger the margin, the more space between our element and the elements around it. We can adjust the margin to move our HTML elements closer to or farther from each other.

Adjusting our margins not only moves our element relative to other elements on the page but also relative to the "walls" of the HTML document. For example, if we declare the width of our ```<div>``` and set its margin to auto, this tells the document to automatically put equal left and right margins on our element. The equal left and right margins calculate based on the width of the document, centering it on the page.

```css
div{
  width:40em;
  margin:4em auto;
}
```

If you want to specify a particular margin, to a particular side, you can do it like this:
```css
div {
  margin-top: /*some value*/
  margin-right: /*some value*/
  margin-bottom: /*some value*/
  margin-left: /*some-value*/
  }
```

You can also set an element's margins all at once using shorthand, which reads clockwise around the content (top, right, bottom, left):

```css
div {
  margin: 1px 2px 3px 4px;
}
```

You'll typically use 1-2 values with the margin property, where 1 value controls all 4 margins and 2 values control the top & bottom, left & right margins respectively. For more on shorthand, read <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties">MDN</a>.

```css
div {
  margin: 40em auto; /*top & bottom margins are 40em; left & right margins are auto*/
}

p {
  margin: 2em; /*all margins 20px*/
}
```

*Border*
The border is the edge of the element. It's what we've been making visible every time we set the border property. You can use shortand for setting ```border```, just like we did with ```margin```. Lets add a border to our ```<div>```:

```css
div{
  width:40em;
  margin:4em auto;
  border: 1px solid #000;
  /*
  border-width:1px;
  border-style:solid;
  border-color:#000; 
  */
}
```

*Padding and Content*
The padding is the spacing between the content and the border. Padding comes in handy for creating space between the text and the border, or using the background color of the box. We can adjust padding to move the border (or boundaries of our box) closer to or farther from the content. Shorthand can be used with padding as well. Let's try out some changes to our ```div``` with the border.

```css
div{
  width:40em;
  margin:4em auto;
  border: 1px solid #000;
  padding:2em;
}
```

Much better! The text is more readable and the page itself has more visual balance. What if our ```div``` has a background color and no border?

```css
div{
  width:40em;
  margin:4em auto;
  /* border: 1px solid #000; */
  padding:2em;
  background:#eee;
}
```

Our container still looks great!

## Refresher: How Display Affects Spacing & Layout (15 mins)
We just learned each HTML element gets its own box to live in. Cool, right? 

As you saw, the outermost box of each element went all the way across the page. This is why, until now, your HTML elements have been sitting on top of one another: by default, they take up the full width of the page. We can change all this with the first positioning property we'll learn, the display property and the four values we can use: inline, block, inline-block, and none.

An inline element has no line break before or after it. This makes the element sit on the same line as another element, but without formatting it like a block. It only takes up as much width as it needs (not the whole line). Inline places all your elements on a single line. The bad news is that it doesn't maintain their "box"ness, so exciting techniques like centering with ```margin:auto;``` are not possible with inline elements.

A block element has some whitespace above and below it and does not tolerate any HTML elements next to it without further styling. This makes the element a block box. It won't let anything sit next to it on the page and takes up the full width.

An inline-block element is _placed_ as an inline element (on the same line as adjacent content), but it _behaves_ as a block element. This makes the element a block box but will allow other elements to sit next to it on the same line.

If you assign ```none``` as the value of the ```display```, this will make the element and its content disappear from the page entirely! However, some browsers 

To illustrate all ```display``` values, consider this HTML:
```html
    <div class="inline">Displays</div>
    <div class="inline">Content</div>
    <div class="inline">in</div>
    <div class="inline">a</div>
    <div class="inline">Row</div>

    <div class="block">Displays</div>
    <div class="block">Content</div>
    <div class="block">Stacked</div>
    <div class="block">Row</div>
    <div class="block">After</div>
    <div class="block">Row</div>

    <div class="inline-block">Displays</div>
    <div class="inline-block">Content</div>
    <div class="inline-block">in</div>
    <div class="inline-block">a</div>
    <div class="inline-block">Row</div>
    <div class="inline-block">with</div>
    <div class="inline-block">Block</div>
    <div class="inline-block">Spacing</div>

    <div class="none">Displays nothing!</div>
```

With this CSS:

```css
div{
  border:1px solid red;
  text-align:center;
}

.inline {
    display: inline;
}

.block {
    display: block;
}

.inline-block {
    display: inline-block;
}

.none{
    display:none
}
```

We would end up with something like this:
<!-- insert image here -->


***

<a name="guided-practice"></a>
## Guided Practice: Topic (# mins)
Solve a problem or apply this topic to a real world scenario. Solving or understanding this scenario should require the use of the current topic (in addition to any prior topics).

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Facere dignissimos totam deleniti architecto porro, nisi. Laudantium repellat animi vero. Illo expedita deserunt officia iure quidem saepe culpa, aut, laborum consequatur.

```ruby
def lorem
  return 'some stuff'
end
```

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Doloribus eligendi nemo eius quo, soluta maxime provident temporibus aperiam eveniet eum. Non, soluta error veritatis pariatur praesentium beatae reprehenderit, numquam quaerat. Lorem ipsum dolor sit amet.

Consectetur adipisicing elit. Facere dignissimos totam deleniti architecto porro, nisi. Laudantium repellat animi vero. Illo expedita deserunt officia iure quidem saepe culpa, aut, laborum consequatur.

```ruby
def another_lorem
  this = some_method(0+2)
  return this.to_json
end
```
> Check: Were students able to successfully solve the problem or complete the task?

***

<!-- <a name="ind-practice"></a>
## Independent Practice: Topic (# minutes)
Use the lesson topic/skill to create a deliverable that meets certain criteria.

> Instructor Note: This can be a pair programming activity or done independently.

Briefly describe the Independent Practice exercise here.  What is the end deliverable?  What skills will it help students practice?  Include a link to the Github folder, which will include a more exhaustive description of the exercise, as well as any code, files or assets for students to download.

> Check: Were students able to create the desired deliverable(s)? Did it meet all necessary requirements / constraints?

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
- Decks -->


