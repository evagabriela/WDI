# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) CSS Selector Basics (90 mins)

| Timing | Type | Topic |
| --- | --- | --- |
| x min | [Introduction](#introduction) | What is CSS? |
| x min | [Demo/Codealong](#demo) | Topic |
| x min | [Guided Practice](#guided-practice) | Topic |
| x min | [Independent Practice](#ind-practice) | Topic |
| x min | [Conclusion](#conclusion) |Topic |

### LEARNING OBJECTIVES
*After this lesson, you will be able to:*
- Style all elements of a particular HTML element on a web page 
- Style copy elements using font-weight, font-size, color, line-height, letter-spacing, text-transform, text-decoration, text-align
- Understand best practice for specificity and cascading
- Understand why external CSS sheets are better than inline styles
- Describe the syntactical and functional relationship between selectors, properties, and values 
- Use special selectors (descendant, adjacent sibling, direct child, universal)
- Apply a set of styles to elements based on pseudo-classes (:hover, :active, :visited, :even, :odd, :nth-child, :first-of-type, :last-of-type) 
- Apply styles to specific elements using classes and IDs
- Apply styles using the Desktop Down method


### STUDENT PRE-WORK
*Before this lesson, you should already be able to:*
- Write HTML that gets rendered as a document in the browser 
- Use HTML tags to add content to a webpage: h1 - h6, p, a, img, ul/ol
- Use HTML tags to define groups of content: header, main, section, article, aside, figure, figcaption, footer
- Pass The Validator without errors


### INSTRUCTOR PREP
*Before this lesson, instructors will need to:*
- Be ready to assess students' levels of understanding of HTML


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
## Introduction: What is CSS? (# mins)

#### Overview
Cascading Style Sheets (CSS) transform the content on your page into a well-designed website. While HTML's purpose is to define what content *is*; CSS's purpose is to define how content should *look*.


### Initial Styles
Keep in mind that even without CSS, your site has design. It’s not very *good* design, but design decisions have been made nonetheless. What styles can you identify?

- White background
- Black color
- Times New Roman font
- Left text alignment
- Bold headers
- Blue, underlined links
- Round, solid black bullets for list items
- Predetermined font sizes
- Predetermined margin & padding
- Predetermined display (inline vs block)

These styles are called inherent or initial styles. Adding CSS is all about overwriting these initial styles to create a customized, beautiful web page. CSS is powerful! Consider the incredible diversity of design in ![these websites](http://www.mezzoblue.com/zengarden/alldesigns/) with the exact same HTML, but different CSS.

You can accomplish ![a lot with very little](http://jgthms.com/web-design-in-4-minutes/) using CSS. If you want to go the extra mile, you can accomplish some ![seriously amazing things](http://codepen.io/). This lesson is a step towards building a working knowledge of CSS and solidifying what you learned in the pre-work. Your goal isn't to memorize the 500+ CSS properties– it’s to get an idea of what you can accomplish with CSS and know how to research what you don’t.

Keep in mind you don’t have to be a designer to be good at CSS, but you do have to be detail-oriented and thoughtful about your code. When it comes time to show off your projects after this course, the first thing most prospective employers will see is your styling. And as we all know, first impressions are incredibly important.


### Review: Structure of CSS
A CSS file is composed of many rules. Each rule governs the appearance of certain elements. A style rule looks like this:

```css
selector {
    property:value;
    property:value;
    property:value;
}
```

Everything inside the curly braces is called the "declaration block." Individual property and value pairs are called “declarations.” 


### Review: Classes and IDs
Sometimes just targeting an element is not enough. We can target other attributes of elements in our selectors.

*Classes*: used for repeatable styles used multiple times within one page or many
```html
<div class="col-2"></div>
```
```css
.col-2 {}
```

*IDs*: used for elements on a page that occur only once– each id on a page must be unique
```html
<div id="hero"></div>
```
```css
#hero {}
```

*Note*
Because IDs can override classes, they can make a codebase more difficult to maintain when it scales. Using classes in your CSS is preferred; it will help with the scalability of your design, and help you write cleaner code. IDs will become more useful in JavaScript.


### Specificity Within The Cascade 
Some properties of elements are passed down to their children. In general:
- Properties dealing with text are inherited by their children
- Properties dealing with spacing are not inherited by their children

View the full property table ![here](https://www.w3.org/TR/CSS2/propidx.html).

When an element is being styled by more than one rule, the browser calculates which rule is more specific and applies that rule’s styles. In general:
- Class rules will override element selector rules;
- If two classes are applied, the second class will override the first; and
- An ID will override both a class and element selector.

Special Selectors *can* override both classes and IDs in certain situations– so choose your methods carefully and keep your code dry.

Consider the following code: 

```html
<p class="intro hidden" id="highlight"></p>
```
```css
p { font-size: 1em; }
.intro { font-size: 2em; }
.hidden { font-size: 0; }
#highlight { font-size: 3em; }
```

This is not an example of efficient code, but it will help demonstrate the cascade. Here's how the code above will be calculated:
- The ```font-size``` of ```1em``` in ```p {}``` will be overridden by the ```font-size``` of ```2em``` in ```.intro {}```;
- The ```font-size``` of ```2em``` in ```.intro {}``` will be overridden by the ```font-size``` of ```0``` in ```.hidden {}```; and
- The ```font-size``` of ```0``` in ```.hidden {}``` will be overridden by the ```font-size``` of ```0``` in ```#highlight {}```;
- A ```font size``` of ```3em``` will render


Keep in mind, specificity can work to your advantage because of inheritance! If you put all the shared styles for all paragraph tags in p {} and put more specific styles in classes, your code will be efficient and non-repetitive.

Consider an updated version of the previous example: 
```html
<p class="intro visible" id="highlight"></p>
```
```css
p { font-size: 1em; }
.intro { color: #333; }
.visible { visibility: visible; }
#highlight { background-color: #ffff00; }
```

The result? All of these styles will be applied, because the same property is not being called with a different value.

#### Special Selectors
Selectors can be more complex than just an element, class, or ID. In fact, Special Selectors may be preferable over using classes in some cases.

*Multiple Selector*: applies the same declaration block to more than one element
```css
h1, h2 {}
```
- Styles all <h1> and <h2> tags


*Tag Qualified Selector*: specifying elements with an applied class
_Example 1_
```css
a.visible {}
```
- Styles only anchor tags with the "visible" class: ```<a class="visible"></a>```. Will not style any other elements with the applied visible class like ```<p class="visible"></p>``` or ```<img class="visible">```.

_Example 2_
```css
.profile.minimized {}
```
Styles all tags that have both the "profile" and "minimized" classes applied: ```<div class="profile minimized"></div>```


*Best Practice Check*: What’s the best way to work– with tag qualifiers or without?
In short, be consistent. Using a class *without* a tag qualifier is a more scalable way to work, because it’s less specific. Remember that classes are meant to style a number of elements– not just one.

If you choose to use Qualified Tag Selectors, be sure it’s the simplest approach and you have a good reason for doing so. Here’s an example of a tag qualifier that’s not helpful:

```css
div#hero {}
```
Although this code will work, there's only ever going to be one tag with an ID of "hero" since IDs are unique. It’s simpler to write ```#hero {}```.


Descendant Selectors: filter out tags based on their ancestors
main p {}
Styles all <p> tags that are descendants of <main> tags.
<main>
    <p></p>
</main>

and
<main>
    <section>
        <p></p>
    </section>
</main>
Be sure you don’t overuse Descendant Selectors, because they can slow down your page. Although we read them left to right (select <main> then <p>) the browser reads them right to left. First, the browser selects all <p> tags and then selects only those inside <main>. 

Below is an example of how not use Descendant Selectors. You can imagine Descendant Selectors becoming overwhelming for the browser:
main section ul li a{ }


As a general rule, limit the number of selectors to 3, and consider making classes as an alternative.


Direct Child Selectors: filters out first-generation child tags only

main > p {}
Styles all <p> tags that are direct, first-generation descendants of <main> tags.
<main>
     <p></p>
  </main>

  *Will not* style children that aren't direct descendents, like this ‘grandchild’ <p> :
<main>
     <section>
         <p></p>
     </section>
  </main>



Adjacent Sibling Selectors: filters sibling tags that appear in a stated order, and styles the second sibling

h2 + p {}

Styles any <p> that follows an <h2>.

<section>
    <h2></h2>
    <p></p>
</section>


*Will not* style an element that isn’t adjacent :
<section>
        <h2></h2>
    <h3></h3>
      <p></p>
  </section>

  *Will not* style an element that isn’t a sibling :
<section>
        <h2></h2>
    <div>
      <p></p>
    </div>
  </section>


Universal Selector: selects all tags on the page *without* using ancestry

* { margin:0; }
Styles *every single* tag on the page without using inheritance. So if any tags that appear on your page do not have a margin declaration of their own, their margin will be 0.  
Note: This is a very powerful selector, and can slow down your page if not used properly. Read more about Universal Selectors here.  


> Check: Insert 1-2 guiding questions to ensure students are comprehending the material.

***

<a name="demo"></a>
## Demo / Codealong: Topic (# mins)
Walk through a codealong or demonstration of something.

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

> Check: By this point, students should be able to write out or code their own methods / functions / arguments / etc.

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

<a name="ind-practice"></a>
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
- Decks

> Instructor Note: When possible, provide a brief description of Additional Resources, classifying whether it is for advanced or beginner students.  

