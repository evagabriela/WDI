# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) HTML Forms (90 mins)

| Timing | Type | Topic |
| --- | --- | --- |
| 10 mins | [Introduction](#introduction) | HTML Forms |
| 15 min | [Demo/Codealong](#demo) | Your First Form |
| x min | [Guided Practice](#guided-practice) | Topic |
| x min | [Independent Practice](#ind-practice) | Topic |
| x min | [Conclusion](#conclusion) |Topic |

### LEARNING OBJECTIVES
*After this lesson, you will be able to:*
- Create and style the following HTML elements: checkbox, radio buttons, text area/box, submit button, fieldset, label, and form
- Evaluate the proper usage of HTML form and input options

***

<a name="introduction"></a>
## Introduction: HTML Forms (10 mins)

## Why is this important?
*This workshop is important because:*

Forms are an important way a web application receive user input. The proper use of forms makes it easier to develop accessible websites with a good user experience.

### An Example `<form>` Element (Tag)

```html
<form method="POST" action="/page">
  <input type="text" name="pageName" />
  <input type="submit" value="Create" />
</form>
```

### Attributes

In the opening of the `<form>` tag you can see two attributes: `method` & `action`

- **method**: the HTTP verb (method) that the browser uses to submit the form.
- **action**: the path of the HTTP request page that processes the information submitted via the form.

>A `route` is simply a combination of a method & action. For example `GET '/page'` or `POST '/users'` are both valid routes.

### POST vs GET
#### [POST](http://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html#sec9.5)
- Data is not shown in URL
- Can contain sensitive data
- No size limitations
- Adds information to, or deletes info from a database

 #### [GET](http://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html#sec9.3)
- Short forms (such as search fields)
- Appended to URL in name/value pairs
- Never use for sensitive info!!!
- Useful for form submissions when user wants to bookmark results
***

<a name="demo"></a>
## Codealong: Your First Form (# mins)
### Challenge: Doomed?

Create an html `form` that, on submit, sends the user to "hasthelargehadroncolliderdestroyedtheworldyet.com". Hint: what's the form action? Bonus: Can you change the submit button to say "Are we doomed?".

#### Solution

```html
<form action="http://hasthelargehadroncolliderdestroyedtheworldyet.com" method="GET">
  <input type="submit" value="Are we doomed!?">
</form>
```

**Client / Server Model**

![client/server](assets/clientserver.png)

## Common Inputs

| Field Type | HTML Code | Widget (Control) | Notes |
|:-- |:-- |:-- |:-- |
| plain text | `<input type="text">` | ![<input type="text">][text] | the type attribute can be omitted |
| password field | `<input type="password">` | ![<input type="password">][text] | echoes dots instead of characters |
| text area | `<textarea></textarea>` | ![<textarea></textarea>][area] | a more customizable plain text area |
| checkbox | `<input type="checkbox">` | ![<input type="checkbox">][check] | can be toggled on or off |
| radio button | `<input type="radio">` | ![<input type="radio" name="group"> <input type="radio" name="group">][radio] | can be grouped with other inputs |
| drop-down lists | `<select><option>` | ![<select><option>Option 1</option><option>Option 2</option></select>][select] | [check here for more info](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select) |
| file picker | `<input type="file">` | ![<input type="file">][file] | pops up an “open file” dialog |
| hidden field | `<input type="hidden">` |  | nothing there!
| submit button | `<input type="submit">` | ![<input type="submit">][submit] | activates the form's submission <br/>(a `POST` request or <br/>Javascript action) |

<!-- Images -->
[text]:   assets/text.png
[area]:   assets/textarea.png
[check]:  assets/checkbox.png
[radio]:  assets/radio.png
[select]: assets/option.png
[file]:   assets/file.png
[submit]: assets/submit.png

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
#### Videos
- [HTML Forms](https://www.youtube.com/watch?v=-5tH2qnTnH0&index=16&list=PLdnONIhPScST0Vy4LrIZiYKpFNoxgyH7J)
- Readings

#### Decks
- [HTML Forms Slideshow](assets/forms.pdf)

> Instructor Note: When possible, provide a brief description of Additional Resources, classifying whether it is for advanced or beginner students.  
