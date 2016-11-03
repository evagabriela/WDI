---
title: WDI Fundamentals Review
duration: "1:00"
creator:
    name: Mike Hopper
    city: Atlanta
---
# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) WDI Fundamentals Review (60 mins)

| Timing | Type | Topic |
| --- | --- | --- |
| 5 min | [Opening](#opening) | Topic |
| x min | [Install Sublime Text](#install-sublime) | Installation |
| x min | [Text Editor Overview](#guided-practice) | Topic |
| x min | [Independent Practice](#ind-practice) | Topic |
| x min | [Conclusion](#conclusion) |Topic |

### LEARNING OBJECTIVES
*After this lesson, you will be able to:*

- Explain the difference between text files and binary files
- Installing Sublime Text 3 using brew cask
- Modify the configuration of Sublime to set the theme, font, tab settings, etc.
- Launch Sublime from the command line
- Use Find to search the current file or all of the files
- Change the layout to 2up, 3up, 4up, etc.
- Install Package Control
- Using Package Control to install other Sublime plugins
- Use cool Sublime editing tricks such as:
  - select and edit several lines at once
  - select and edit in "column mode"
  - move the selected line up or down
- Use keyboard shortcuts to save time


<!-- can you expand on this? -->

### STUDENT PRE-WORK
*Before this lesson, you should already be able to:*

- Be familiar with how to create and edit files in Sublime Text.

### INSTRUCTOR PREP
*Before this lesson, instructors will need to:*

- Gather materials needed for class
- Complete Prep work required
- Prepare any specific instructions

---
<a name="opening"></a>
## Opening (5 mins)
- Review current lesson objectives
- Include Hook / Real-world Relevance (why the content from this lesson is useful or important)

The main purpose of this lesson is to for you to get comfortable with the
Sublime editor, including how to configure it, install plugins, and get
*greedy* about discovering faster, more efficient ways of editing files.

![VI or Sublime](to-vi-or-not-to-vi.png)


***




## Install Sublime Text (10 min)

#### Install Homebrew

Copy and Paste into your terminal window:

```bash
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

#### Install Sublime (Using Brew and Cask)

Copy and Paste into your terminal window:

```bash
brew tap caskroom/cask
brew tap caskroom/versions
brew cask install sublime-text
```


## Text Editor Overview

#### What is a Text Editor?
* Provides an interface for viewing and modifying text files
* Text files are files containing human readable text
* Encoded via ASCII or Unicode characters
* There are different *kinds* of text editors:
    - terminal / command line: vim, emacs, nano
    - window based: Sublime, TextMate, Notepad++

#### Modern Text Editors
* Can open a file or a directory
* Can understand context:
    - context sensitive help
    - may highlight errors or bad practices in your code
    - adapt to different file formats
    - provide syntax highlighting

* extensions & plugins - used to add additional features to the editor

#### Types of Text Files
* Plain text
* Markdown
* CSV
* Various Programming Languages
    - HTML
    - CSS
    - JavaScript
    - Ruby
    - BASH
    - SQL
* Each programming language has a set of rules, keywords, operators, and syntax

#### Sublime Text
* multi-platform (OS X, Windows, Linux)
* popular (widely used for web development)
* free to try (though you will be nagged to purchase it)
* extensible (we can add functionality via plugins)

#### Sublime Versions
* You will want to be sure that you have installed Sublime Text **3**



## Using Sublime
#### Launching Sublime

To open sublime, simply click the icon in the Dash or Launchpad.
Or just type `subl` in a terminal.

To open Sublime with a specific file, we can use the command line again,
but this time passing in a file name:

```bash
mkdir recipes
subl recipes/veggie_soup.txt
```

#### Project mode

Real-world software projects often involve _many_ files organised into
folders. It is handy to be able to see all the files in our project when
working in our text editor. Sublime makes this easy as it supports a
project mode. To use this we simply pass a directory instead of a file:

```bash
subl recipes
```
or...

```bash
cd recipes
subl .
```

Notice that the sidebar now has a folders section that shows all the files
and folders in the project. Clicking on a folder expands the view to show its
contents.

#### Take a Tour of the Sublime Editor Window Components

* Menu
* Sidebar
* Open files via tabs
    - can rearrange tabs
    - can change layout of tabs - `Alt-Command-<Number>`
* Edit pane
* Ruler
* Minimap
* Footer
    - Line #, Column #
    - White Space Mode
    - File Type

#### Find (Search)

* You can search a single file or all of the open files
* You can search case sensitive or case insensitive
* You can search using regular expressions (we will talk about those later)

#### Settings and themes

`cmd + ,` allows you to access the sublime's preferences.

It opens this file as a JSON object (we will learn all about JSON in the next
few weeks).  It basically presents the settings as a series of keys and values
- you can add keys/values, and/or modify the existing values to fit your
personal preferences.

**For now, add the following:**

```json
{
    "draw_white_space": "all",
    "ensure_newline_at_eof_on_save": true,
    "fade_fold_buttons": false,
    "font_face": "Menlo",
    "font_size": 20,
    "highlight_line": true,
    "highlight_modified_tabs": true,
    "indent_to_bracket": true,
    "line_padding_bottom": 1,
    "line_padding_top": 1,
    "open_files_in_new_window": false,
    "rulers":
    [
        78
    ],
    "soda_classic_tabs": true,
    "soda_folder_icons": true,
    "tab_size": 2,
    "translate_tabs_to_spaces": true,
    "trim_trailing_white_space_on_save": true,
    "word_separators": "./\\()\"'-:,.;<>~!@#%^&*|+=[]{}`~?",
    "word_wrap": "false"
}
```

We can change the colour scheme sublime uses by going to `preferences/color scheme` and selecting one of the themes. I recommend **Sunburst** or **Dawn**. When you select a scheme it changes all of the syntax highlighting colors.



## Package Control

Sublime works with a lot of plugins, and we will install new plugins almost every week. Before, you had to download the package manually and add it to Sublime's plugins folder. Now there is a package manager for Sublime, which works a bit like brew; you ask for a package and sublime will install it for you.

In short, Sublime is highly customisable, you can play around by editing your user settings and by installing plugins. We will do this using *Package Control*.

Follow the instructions [here](https://packagecontrol.io/installation#st3) to install *Package Control*.
Note that there is a difference in the instructions between ST2 and ST3. 

#### Install Some Plugins!

Now we will use *Package Control* to install the following plugins:

1. Advanced New File
	- We can test out the plugin by creating a new file:
		- Create a New File (AdvancedNewFile plugin):   `Alt-Command-N`
2. Sidebar Enhancements (only available for ST3)
	- Now when you right click on any folder or file in the sidebar, you'll see a whole list of options for what you can do with the files.
3. Emmet
	- Emmet provides us with a whole range of autocomplete shortcuts for writing HTML.




## Guided Practice

In this code along we will create some files via the command line and then
edit them in Sublime.




## References


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
	- [Sublime Practice](https://www.shortcutfoo.com/app/dojos/sublime-text-2-mac)
- Videos
	- [Sublime Youtube videos](https://www.youtube.com/playlist?list=PLLnpHn493BHEYF4EX3sAhVG2rTqCvLnsP)
- Readings
	- [Efficiency With Sublime Text](http://thunderboltlabs.com/blog/2013/11/19/efficiency-with-sublime-text-and-ruby/)
	- [Scotch.io Tutorials](https://scotch.io/tag/sublime-text)
	- [Sublime Text Keyboard Shortcuts](http://www.wdtutorials.com/2013/06/23/sublime-text-keyboard-shortcuts-cheat-sheet-win-os-x-and-linux#.VT2F161Viko)

- Decks

> Instructor Note: When possible, provide a brief description of Additional Resources, classifying whether it is for advanced or beginner students.  

