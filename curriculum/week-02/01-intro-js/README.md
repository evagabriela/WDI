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


Let’s see what it takes to add JavaScript to your HTML.

HTML renders line by line, so it’s important to think about where we’ll place our JS.









First, we'll need to create a JavaScript file. The process is similar to creating any other file, we just want to use a .js extension for JS. Common names for JavaScript files are main.js and script.js.









On larger sites, we'll want to house all of our JavaScript files in a folder to them organized. It's common to call this folder “js” or “scripts.”









Just like we need to add a `<link>` tag when we want to tell our browser where it can find the CSS files associated with our HTML page, we need to add a `<script>` tag to let the browser know where it can find the page’s associated JS files.

We recommend you include your JS files right before the closing `</body>` tag in your HTML code.





![](http://circuits-assets.generalassemb.ly/prod/asset/5058/Slide-67-Order.svg)









If you have multiple JS files that depend on one another, it matters what order you place them in your HTML.

Because HTML is parsed by the browser from the top down, any **libraries** (define on the next slide) we add to our project must appear above any other JS files using these libraries.

If not, the JS script will crash when it tries to use any methods defined in that library, because it won’t know those methods exist.









A **library** is a file that contains pre-written code you can download and include in your project.

It allows you to take code that other developers have written and use its functionality code so you don't always have to write everything from scratch.

We'll be working closely with the jQuery library later in this course.









Now, make sure your JS file is hooked up to your HTML correctly:



![](http://circuits-assets.generalassemb.ly/prod/asset/5059/Slide-54.png)


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

