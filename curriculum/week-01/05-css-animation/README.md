# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) CSS Animation (90 mins)

| Timing | Type | Topic |
| --- | --- | --- |
| 10 mins | [Introduction](#introduction) | CSS Animations |
| 30 mins | [Independent Practice](#ind-practice-research) | Research Transforms, Transitions, and Animations |
| 45 min | [Independent Practice](#ind-practice) | Topic |
| 5 min | [Conclusion](#conclusion) |Topic |

### LEARNING OBJECTIVES
- Utilize browser compatibility techniques like vendor prefixes, the SHIV, and meta tags
- Describe the importance of prefixing CSS properties
- Use properties like transition and transform to change element properties
- List the types of properties that can / can't be animated
- Describe the purpose and syntax of css keyframes
- List and describe the purpose of the animation properties
- Compare & contrast using CSS and JS for animations

***

<a name="introduction"></a>
## Introduction: CSS Animations (10 mins)

Today we'll be covering 3 major topics, each somewhat related:
- CSS Transforms (2D)
- CSS Transitions
- CSS Animations

###Vocabulary
**Transforms** are a set of CSS properties that take a an element and transform it's shape, e.g. rotating it, scaling it, skewing it, etc.

**Transitions** let us tell the browser how to change a property over time. For example, if the height of an element changes (due to a :hover selector, for example), we can tell the browser to change the height gradually over 1 second.

**Animations** are similar to transitions, in that they let us have properties change over time, but they give us more control over how those changes happen. For example, we have more control over how the animation repeats, change between multiple values at once, etc.

*Prefixing* - If you're using chrome, you won't need to prefix any properties for this lesson, but in general, it's a good idea to check [Can I Use](http://caniuse.com/) to see if you need to use prefixes to support most users. For CSS Animations, you should use prefixes to ensure support for Safari, IE, and other browsers.

The easiest way to do this is with [prefix free](http://leaverou.github.io/prefixfree/).

***

<a name="ind-practice-research"></a>
## Independent Practice: Research Transforms, Transitions, and Animations (40 mins)
Breakout into groups of four. Each group will have 20 minutes to prepare a short explanation / demo of their assigned topic. Your demos should take no longer than 5 minutes.

| Group | Topic
| --- | --- |
| 1 | CSS Transforms (No animation) |
| 2 | CSS Transitions |
| 3 | CSS Animations (basic keyframes and syntax) |
| 4 | CSS Animations (timing functions) |
| 5 | CSS Animations (iterations / repeats / direction ) |

***

<a name="ind-practice"></a>
## Independent Practice: Animate it! (45 minutes)
Implement as many of the following exercises as you can in the time allotted. Feel free to work with a partner!

- [CSS Accordion](https://github.com/ga-wdi-exercises/css-accordion)
<!-- INSTRUCTOR NEEDED: it'd be great if we could find a more real-world example to replace DolphinCat. -->
- [DolphinCat!](https://github.com/ga-wdi-exercises/dolphin-cat-css-animations)
- [Clock](https://github.com/ga-wdi-exercises/clock-bro)

### Bonus
Look at the following transitions and animations examples, try to re-create them from scratch using as little starter code as possible.

<!-- INSTRUCTOR NEEDED: it might be valuable to create code similar to these examples, so we're not just linking the students out to so many options. I think that overwhelms them. Then, we could move these links to Additional Resources.  -->
- [Animated Buttons](http://tympanus.net/Tutorials/AnimatedButtons/index4.html)
- [Image Hover Effects](http://tympanus.net/Tutorials/OriginalHoverEffects/)
- [Solar System in CSS](http://neography.com/experiment/circles/solarsystem/)
  - [*solution*](http://neography.com/journal/our-solar-system-in-css3/)

***

<a name="conclusion"></a>
## Conclusion (5 mins)
#### CSS vs JS Animations
CSS Animations are easy and mostly compatible, so they're often a good choice for basic animation needs. For anything more complex, such as animation that depends on user input, you'll need to use Javascript. There are good libraries for animation, including jQuery UI, and [GSAP (Greensock Animation Platform)](http://greensock.com/gsap).

***

### ADDITIONAL RESOURCES
#### Videos
- [CSS Animation](https://www.youtube.com/watch?v=9RfHG3K8U_Q&index=31&list=PLdnONIhPScST0Vy4LrIZiYKpFNoxgyH7J)
- [CSS Transitions](https://www.youtube.com/watch?v=Xu3SrQhtBqw&index=30&list=PLdnONIhPScST0Vy4LrIZiYKpFNoxgyH7J)
- [CSS Transform](https://www.youtube.com/watch?v=Gu-HBBZLyjg&index=29&list=PLdnONIhPScST0Vy4LrIZiYKpFNoxgyH7J)
