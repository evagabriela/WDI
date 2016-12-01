# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) CSS Selector Basics (90 mins)

| Timing | Type | Topic |
| --- | --- | --- |
| 5 mins | [Opening](#opening) | CSS |
| 20 mins | [Intro to New Material](#introduction) | What is CSS? |
| 15 mins | [Demo](#guided-practice) | CSS Tools of the Trade |
| 45 mins | [Independent Practice](#ind-practice) | CSS Challenges |
| 5 mins | [Conclusion](#conclusion) |Review and Questions |

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
## Opening: (5 mins)
- Review the purpose of HTML
- Remind students CSS references HTML

***

<a name="introduction"></a>
## Intro to New Material: What is CSS? (30 mins)

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

These styles are called inherent or initial styles. Adding CSS is all about overriding these initial styles to create a customized, beautiful web page. CSS is powerful! Consider the incredible diversity of design in [these websites](http://www.mezzoblue.com/zengarden/alldesigns/) with the exact same HTML, but different CSS.

You can accomplish [a lot with very little](http://jgthms.com/web-design-in-4-minutes/) using CSS. If you want to go the extra mile, you can accomplish some [seriously amazing things](http://codepen.io/). This lesson is a step towards building a working knowledge of CSS and solidifying what you learned in the pre-work. Your goal isn't to memorize the 500+ CSS properties– it’s to get an idea of what you can accomplish with CSS and know how to research what you don’t.

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

**Note** Because IDs can override classes, they can make a codebase more difficult to maintain when it scales. Using classes in your CSS is preferred; it will help with the scalability of your design, and help you write cleaner code. IDs will become more useful in JavaScript.


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
- The `font-size` of `1em` in `p {}` will be overridden by the `font-size` of `2em` in `.intro {}`
- The `font-size` of `2em` in `.intro {}` will be overridden by the `font-size` of `0` in `.hidden {}` and
- The `font-size` of `0` in `.hidden {}` will be overridden by the `font-size` of `0` in `#highlight {}`
- A `font size` of `3em` will render

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

> Check for Understanding: Describe which selectors override which (element, class, id).

#### Special Selectors
Selectors can be more complex than just an element, class, or ID. In fact, Special Selectors may be preferable over using classes in some cases.

##### Multiple Selector
Applies the same declaration block to more than one element.

```css
h1, h2 {}
```
- Styles all `<h1>` and `<h2>` tags


##### Tag Qualified Selector
Specifying elements with an applied class
_Example 1_

```css
a.visible {}
```

- Styles only anchor tags with the "visible" class: ```<a class="visible"></a>```. Will not style any other elements with the applied visible class like ```<p class="visible"></p>``` or ```<img class="visible">```.

_Example 2_
```css
.profile.minimized {}
```
Styles all tags that have both the "profile" and "minimized" classes applied: `<div class="profile minimized"></div>`

**Best Practice Check**: What’s the best way to work– with tag qualifiers or without?
A: In short, be consistent. Using a class *without* a tag qualifier is a more scalable way to work, because it’s less specific. Remember that classes are meant to style a number of elements– not just one.

If you choose to use Qualified Tag Selectors, be sure it’s the simplest approach and you have a good reason for doing so. Here’s an example of a tag qualifier that’s not helpful:

```css
div#hero {}
```
Although this code will work, there's only ever going to be one tag with an ID of "hero" since IDs are unique. It’s simpler to write `#hero {}`.


##### Descendant Selectors
Filter out tags based on their ancestors.

```css
main p {}
  ```
- Styles all `<p>` tags that are descendants of `<main>` tags:

```html
<main>
    <p></p>
</main>

and
<main>
    <section>
        <p></p>
    </section>
</main>
```
Be sure you don’t overuse Descendant Selectors, because they can slow down your page. Although we read them left to right (select `<main>` then `<p>`) the browser reads them right to left. First, the browser selects all `<p>` tags and then selects only those inside `<main>`.

Below is an example of how not use Descendant Selectors. You can imagine Descendant Selectors becoming overwhelming for the browser:
`main section ul li a{ }`

As a general rule, limit the number of selectors to 3, and consider making classes as an alternative.

##### Direct Child Selectors
Filters out first-generation child tags only.

```css
main > p {}
```

Styles all `<p>` tags that are direct, first-generation descendants of `<main>` tags.
```html
<main>
     <p></p>
  </main>
```

  *Will not* style children that aren't direct descendants, like this ‘grandchild’ `<p>`:
```html
<main>
     <section>
         <p></p>
     </section>
  </main>
```

##### Adjacent Sibling Selectors:
Filters sibling tags that appear in a stated order, and styles the second sibling.

```css
h2 + p {}
```

Styles any `<p>` that follows an `<h2>`.
```html
<section>
    <h2></h2>
    <p></p>
</section>
```

*Will not* style an element that isn’t adjacent:
```html
<section>
        <h2></h2>
    <h3></h3>
      <p></p>
  </section>
```
  *Will not* style an element that isn’t a sibling:
```html
<section>
        <h2></h2>
    <div>
      <p></p>
    </div>
  </section>
```

##### Universal Selector:
Selects all tags on the page *without* using ancestry.

`* { margin:0; }`

Styles *every single* tag on the page without using inheritance. So if any tags that appear on your page do not have a `margin` declaration of their own, their `margin` will be `0`.  
**Note**: This is a very powerful selector, and can slow down your page if not used properly. Read more about Universal Selectors here.  


> Check: Label the following special selectors:
> p + p  |  p > a  |  section p

***

<a name="demo"></a>
## Demo: CSS Tools of the Trade (15 mins)

### Tools of the Trade
Oftentimes, dealing with CSS can be a pain. Getting a web page to look the way you want will take a lot of experimentation, iteration, and patience as you’re learning the most efficient ways to code. Here are some great resources to help you master CSS!

The [CSS Validator](http://jigsaw.w3.org/css-validator/#validate_by_input) is a tool into which you can copy and paste your CSS, and it'll tell you precisely what's wrong with it. We expect you to validate your CSS during this course.

[The Chrome Element Inspector](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/?hl=en) allows you to look at a specific element on a page, and see exactly which CSS rules are being applied to it. You can also turn rules on and off, modify rules, and create new rules– which makes experimenting within the Inspector a fast way to fine-tune your design. Note: these edits don’t change your file, and will reset when you refresh the page.

>Instructor Note: Briefly walk through each of the tools above.
 ***

### Research & Debugging
The purpose of this class isn't for you to walk away being an expert in all things CSS. That takes months of tolerating many unexpected, sometimes counter-intuitive results. The goal is for you to be exposed to all the things that can be accomplished with CSS. If they're on your radar, you can continue to work with and expand your skillset.
What should you do if something is unfamiliar?
Read it like English. CSS is intended to be readable.
Look it up! If you don't know what box-sizing means, Google ‘css box-sizing’.
Even professional developers rely heavily on sites like Stack Overflow in their day-to-day workflow. Why? There’s simply too much to memorize, and too many unique situations to encounter. This is what’s great about being a programmer! Nothing is ever new, even if you’ve done it dozens of times.
So don’t feel like an amateur when you’re Googling for answers– feel like a pro!

***

<a name="ind-practice"></a>
## Independent Practice: CSS Challenges (45 minutes)

>Instructor Note: This can be done independently or in groups.

Navigate to [codepen](http://codepen.io/) and complete the following tasks:  
#### List some common element properties that can be styled  
- Create an html page with a p tag and some placeholder text  
- Change its text color to a hex value that you choose from http://color.adobe.com  
- Give it a background color  
- Make the size of the text larger  
- Change its font family to a sans-serif font  
- Make the text bold  
- Center the text  

#### Describe ids and classes. Explain when should we use which.  
- Add two more p tags.  
- Give one p tag an id  
- Give the other two p tags the same class  
- Use just the ids and classes to style p tag with the id differently from the ones with a class  

#### Describe "The Cascade"
- Create a p tag within a section tag    
- Put some text in the section tag, but outside the p tag  
- Put some text in the p tag  
- Style just the section tag to give its text some color  
- Note that the p tag has also been affected  

#### Describe how to combine various selectors
- Create a rule for all p tags that also have a class of active  
- For this rule, make the text bold  
- Add an active class to a few of your p tags  
- Create a rule for all div tags that also have a class of active  
- For this rule, make the text very large  
- Create a div tag with the class of active  

#### Describe Specificity
- Create a rule for the tag with an id of blue  
- Set the text color for this rule to blue  
- On the next line of your css file, create a rule for all tags with classes of red  
- Set the text color for this rule to red  
- In your HTML, create a span tag with both an id of blue and a class of red  
- Note that the color of the span tag should be blue  

> Check: Were students able to create the desired deliverable(s)? Did it meet all necessary requirements / constraints?  Ask students to share their challenges with the class.

***

<a name="conclusion"></a>
## Conclusion (5 mins)
- In the independent practice, which rules felt the most challenging? Why?
- Imagining a site you visit often, what are some examples of content where special selectors might be useful?
- Is there a special selector you **wish** existed?

***


### Hungry for more?
#### Exercises
* [CSS Animal-Style](exercises/animal-style)
* [CSS Color Box](exercises/color-box)
* [CSS Diner](http://flukeout.github.io/)

#### Readings  
* [Shay Howe's HTML/CSS Guide](http://learn.shayhowe.com/)  
* [30 CSS Selectors You Must Memorize](http://code.tutsplus.com/tutorials/the-30-css-selectors-you-must-memorize--net-16048)  
* [Specifics on CSS Specificity](https://css-tricks.com/specifics-on-css-specificity/)  
* [CSS Specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)  
* [Typography/Web Fonts](http://practicaltypography.com/typography-in-ten-minutes.html )  

#### Tools and References
* [CSS Specificity Calculator](http://specificity.keegan.st/)
* [Web Design in 4 Minutes](http://jgthms.com/web-design-in-4-minutes/)
* [CSS Visual Reference](http://cssreference.io/)
* [LearnLayout.com](http://learnlayout.com/)
    - A great interactive tutorial that details CSS' many properties and quirks.  
* [Mozilla Developer Network CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)  
    - Like W3Schools, but in much more detail.    
    - [Universal Selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Universal_selectors)  
* [CanIUse.com](http://caniuse.com/)
    - Search for a CSS property (or HTML, or JS), and it'll tell you on which web browsers it functions.  
* [CSS Validator](https://jigsaw.w3.org/css-validator/#validate_by_input)
    - Copy and paste your CSS in here and it tells you what's wrong with it.  
* [Codrops](http://tympanus.net/codrops/css_reference/)  
* [Codepen](http://codepen.io/)  
* [Mezzoblue](http://www.mezzoblue.com/zengarden/alldesigns/)  


#### Videos
* [Intro to CSS](https://www.youtube.com/watch?v=xWiT2TWCFjc&list=PLdnONIhPScST0Vy4LrIZiYKpFNoxgyH7J&index=3)
* [CSS Foundations: 1 of 2](https://www.youtube.com/watch?v=aLtWccm8Ayo&list=PLae1he6d1WImFXtLgPt7MDAx6k6iP59EW&index=107)
* [CSS Foundations: 2 of 2](https://www.youtube.com/watch?v=A9Mn2UoUW-k&index=115&list=PLae1he6d1WImFXtLgPt7MDAx6k6iP59EW)
* [CSS Colors, Backgrounds, and Font Basics](https://www.youtube.com/watch?v=UMMHsQPmfug&list=PLdnONIhPScST0Vy4LrIZiYKpFNoxgyH7J&index=4)
* [CSS Selectors](https://www.youtube.com/watch?v=g0Aq2kP5-CY&list=PLdnONIhPScST0Vy4LrIZiYKpFNoxgyH7J&index=5)
* [CSS Family Selectors](https://www.youtube.com/watch?v=Zudl-fCDSdM&index=14&list=PLdnONIhPScST0Vy4LrIZiYKpFNoxgyH7J)
* [CSS Attribute Selectors](https://www.youtube.com/watch?v=PuF0drOMN3E&list=PLdnONIhPScST0Vy4LrIZiYKpFNoxgyH7J&index=15)
* [CSS Pseudo Selectors: 1 of 4](https://www.youtube.com/watch?v=O9dpZj4XWmA&list=PLae1he6d1WImFXtLgPt7MDAx6k6iP59EW&index=113)
* [CSS Pseudo Selectors: 2 of 4](https://www.youtube.com/watch?v=sd8xY2jUXpc&index=112&list=PLae1he6d1WImFXtLgPt7MDAx6k6iP59EW)
* [CSS Pseudo Selectors: 3 of 4](https://www.youtube.com/watch?v=c-AsuaboyeI&index=111&list=PLae1he6d1WImFXtLgPt7MDAx6k6iP59EW)
* [CSS Pseudo Selectors: 4 of 4](https://www.youtube.com/watch?v=s7hM9RDgkRY&list=PLae1he6d1WImFXtLgPt7MDAx6k6iP59EW&index=114)
* [CSS Pseudo Selectors: Links](https://www.youtube.com/watch?v=YMZGPqNDn_s&list=PLdnONIhPScST0Vy4LrIZiYKpFNoxgyH7J&index=17)
* [CSS Pseudo Selectors: Children](https://www.youtube.com/watch?v=tMCahu7H-fA&index=18&list=PLdnONIhPScST0Vy4LrIZiYKpFNoxgyH7J)
* [CSS Pseudo Selectors: nth-child](https://www.youtube.com/watch?v=yFmwjX9oGt8&index=19&list=PLdnONIhPScST0Vy4LrIZiYKpFNoxgyH7J)
