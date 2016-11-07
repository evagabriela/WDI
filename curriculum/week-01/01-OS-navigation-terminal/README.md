
---

# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) OS Navigation Using the Terminal (120 mins)

| Timing | Type | Topic |
| --- | --- | --- |
| 5 min | [Opening](#opening) | Opening |
| 10 min | [Why the CLI?](#why-the-cli) | Command Line vs. GUI |
| 25 min | [The Basics of the CLI](#cli-basics) |CLI Basics |
| 10 min | Break | |
| 25 min | [Paths](#paths) |Absolute vs. Relative Paths |
| 25 min | [Common Commands](#common-commands) |Common commands |
| 10 min | [WDI Environment](#wdi-environment) |Environment Setup |
| 5 min | [Conclusion](#conclusion) |Conclusion |

### LEARNING OBJECTIVES
*After this lesson, you will be able to:*


- Compare and contrast CLIs with GUIs.
- Explain how command line usage can increase efficiency.
- Describe the anatomy of a command: statements, flags and arguments.
- Explain what a path is and why the 'current path' is important in the CLI.
- Explain the difference between absolute and relative paths.
- List common commands to
	- View the path of the current directory
	- View the contents of a directory
	- Navigate to different directories
	- Manage files and directories
- List unsafe commands
- Setup your working directory / environment for WDI.

### STUDENT PRE-WORK
*Before this lesson, you should already be able to:*

- Navigate his/her computer using Finder
- Have exposure to the command line from Fundamentals



### INSTRUCTOR PREP
*Before this lesson, instructors will need to:*

- Gather materials needed for class
- Complete Prep work required
- Review the instructions for setting up the WDI Environment and tailor to suit the needs of your specific instance.
- Tailor instructions for submitting HW

***

<a name="opening"></a>
## Opening (5 mins)
- Review current lesson objectives



**Turn & Talk:** Given your exposure to the Command Line in the pre-work and Installfest, spend **2 minutes** discussing and writing down some answers for the following questions with a partner...

* How is the CLI different from the GUI?
* What do you like / dislike about using it?
* Compared to a GUI, in what ways might using the CLI be better or worse for developers?

***

<a name="why-the-cli"></a>
## Why The CLI? (10 mins)

**Speed.** Developers can execute common tasks much faster using the CLI. Features such as tab completion,
command history, piping and more all contribute to this.

> Try a `.txt` file on your computer, first via the GUI, then the CLI using the `touch` command. Which way is quicker?

**Precision.** We can look at the commands we're about to enter and understand exactly what they will do. This allows for...

**Repeatability / Scriptability.** We can easily save commands and re-use them, or even share them with others.

> What you did during Installfest was run a set of scripts that we shared with you!  

**Tools.** There are tons of tools we can use in the CLI to achieve a vast number of tasks. Most of them are built in, but we can also download external ones using services like Homebrew (OSX) and `apt-get` (Linux).

> Tree is an example of a nifty third-party tool. It's useful in visualizing directory structure. Try downloading it by running this in the CLI: `$ brew install tree`.
>
> Tools built for the command line usually follow something called
the ['Unix philosophy'](http://catb.org/esr/writings/taoup/html/#id2807216), meaning each tool should do one thing and do it
well. Complex tasks can be achieved by chaining tools together.  

**Debugging.** Whenever we get an error in the CLI, it will often come with a lot of information that we can use to then debug it. As developers, this preferable to what can often be unhelpful GUI errors, like this...

![](http://coding-journal.com/wp-content/uploads/2013/10/Screen-Shot-2013-10-30-at-12.02.14.png)

> All these benefits aren't necessarily exclusive to the CLI (compared to a traditional GUI), but they tend to be more consistent.





#### DEMO: Hello.txt using GUI vs CLI

> Note: There's nothing wrong with combining the powers of both the CLI and a GUI! We generally won't be writing files in the terminal. We'll be using the Atom GUI. This just highlights that there are efficiencies that can be garnered from knowledge of CLI.

We might be thinking to ourselves, "These differences are negligible! Which in this contrived example, it's a difference of MAYBE 5 seconds. But in the span of our careers as developers, becoming proficient with the command line is extremely important. It will end up saving us lots of time.


> Check: Describe the benefits of using the CLI as a developer vs. using a GUI. Explain how using the command line can increase efficiency.

***
<a name="cli-basics"></a>
## The Basics of CLI (30 mins)

You may already be familiar with some of these concepts, but it's worth reviewing them now, cementing the concepts and getting some more practice in.

#### Everything is a command

First things first, on the command line, everything we enter into the command line is a **command**. When we hit enter, the command is executed.

#### Commands have output and side effects

Some commands have **output**, which is displayed on the screen for us to see.

Examples of commands that have output might be:

* `pwd`
* `ls`
* `cat <filename>`

Other commands primarily exist to have a *side-effect*, or in other words, to make some change, usually on our system. An example might be `touch`, which creates a new file.

Note that often times, a command whose main job is a side effect may not provide any output if it succeeds. If there is an error it will provide output.

Rarely, some commands may provide both an output and side effects.

#### Command Syntax (Flags and Arguments)

    $ ls -als *.png

Commands generally consist of three parts, the command, followed by flags (aka options), and finally arguments.

The **command** is the first 'word', e.g. `ls`, `cd`, or `touch`. It is like the verb, which says generally, 'what do I want to do'.

Next come the **Flags**. Think of these as "options" that tell the command how to do what it's about to do. There may be zero or more options.
* Sometimes you won't be using any options. Other times just one or maybe even more!
* Options usually start with one or two dashes. If the option is a letter, then one dash (e.g., `-a`). If it's a whole word, then two dashes (e.g., `--all`).

> [Here's a list](http://catb.org/esr/writings/taoup/html/ch10s05.html#id2948149) of some single-letter flags you might encounter. This is not an exhaustive list.

Finally come the arguments. These are what you want to do the action to. Usually these are file names, but they could be URLs, or other things.

#### Common Patterns
The commands entered into the CLI are often in one of the following forms..

- `doSomething --how toFiles`
- `doSomething --how sourceFile destinationFile`

Where **doSomething** is, in effect, a verb, **how** an adverb (for example, should the command be executed "verbosely" or "quietly") and **toFiles** an object or objects (typically one or more files) on which the command should act.

> Not all commands follow this pattern, but many do.

Let's take a look at something we did for installfest.

```
$ brew install git
```

> When we type this command and hit enter , we're saying, "Computer, we're about to do something with homebrew. The thing were going to do is install something. What we want to install is git.

#### Independent Practice (Commands, Flags, and Arguments) (5 min)
**Q:** Spend 2 minutes writing down the commands, flags and arguments for each of the below commands:

  1. `$ touch index.html`
  2. `$ ls -al`
  3. `$ cp index.html index2.html`
  4. `$ brew install git`

> Lesson objective: Describe the anatomy of a command: statements, flags and arguments.

> Remember, not all of these have flags and/or arguments.

> Check: Spend 2 - 3 minutes reviewing answers with class

***

<a name="paths"></a>
## Paths (20 mins)
#### What is a 'path'?

A path is the description that tells us (or a computer) where a file or directory is on our computer.

Our terminal (shell) is always working out of a single path at a time. Commands that are run will take action in the current path (directory) unless we tell them to do otherwise.

#### Relative vs Absolute Paths

All paths point to a single file or directory, but we can write paths to be either **relative** or **absolute**.

##### Absolute Paths

An absolute path will always tell us exactly where the file or directory is. An example in the real world would be a mailing address:

```
GA
2nd Floor, Ponce City Market
675 Ponce De Leon Ave NE
Atlanta, GA 30308
USA
Earth
Solar System
Milky Way
```

Absolute paths start with a `/` and go from top down (least specific to more specific):

```bash
/Milky_Way/Solar_System/Earth/USA/San Francisco/CA
```

or a realistic example:

```bash
/Users/joehacker/wdi/lessons/cli-intro
```

The first slash essentially means "start at the root of the computer's file system."

Some absolute paths instead start with a `~`. This is a shortcut to the absolute path of our home directory. So the above absolute path could also be written as

```bash
~/wdi/lessons/cli-intro
```

> On Macs, `~` corresponds to your user directory - `/users/your-mac-username`.


#### Relative Paths

Relative paths are interpreted as starting from the current working directory. They start with anything but a `/` or `~`.

So if we were in our home directory, the path to this lesson's directory could be written in the following ways...

```bash
wdi/lessons/cli-intro                                   # relative
~/wdi/lessons/cli-intro                                 # absolute
/Users/adrianmaseda/wdi/lessons/cli-intro               # absolute
```

If we were in a different folder, then the relative path would point to an entirely different folder/file.

Periods have special meaning when used in relative paths..
* `.`: one dot means "relative to the current directory"
* `..`: two dots means "go up to the parent directory"

So if we're in `~/wdi/lessons`, then the relative path `../projects` means "go up one level to the wdi folder, then down into my `projects` directory.

We can use more than one `..` to go up multiple levels. For example...

This time, if we're in `~/wdi/lessons/cli-intro`, entering `cd ../../projects` would go up two levels to `wdi`, and then down one level into `projects`.

**Q:** Spend two minutes writing out what the following commands are doing in English...
  1. `$ cd ./lessons`
  2. `$ ls ..`
  3. `$ mv ../index.html .`


> Check: Explain what a path is and why the 'current path' is important in the CLI.
> Check: Explain the difference between absolute and relative paths.

## Common Commands (35 mins)

#### Getting Help (5 mins)

There are three general ways to get help with a command.

* Add `--help` or `-h` to the end of the command (e.g., `brew --help`).
* Use the manual -- or `man` -- tool (e.g., `man brew`).
* Google!

The first two options will display text using a program called `less`. Use the arrow keys to navigate. Type `q` to quit.


#### Basic Interface Commands Overview (10 mins)
1. ls [*DIRECTORY*]
	- list contents of a directory
	- common examples
		- `ls -l`
		- `ls -a`
		- `ls -la`
1. pwd
	- show path to current directory
1. mkdir *DIRECTORY*
	- make a directory
1. cd [*DIRECTORY*]
	- change to a different directory
1. touch *FILE*
	- create an empty file
1. mv *SOURCE* *DESTINATION*
	- move a file/directory somewhere else
	- also used for renaming
1. cp *SOURCE* *DESTINATION*
	- copy a file to a destination
1. rmdir *DIRECTORY*
	- remove an empty directory
1. open [-a *PATHTOAPPLICATION*] file
	- open a file


#### Unsafe Commands (10 mins)

### `sudo`

`sudo` -- or "super user do" -- runs the command that follows as the super user (i.e., 'root' or 'admin'). That means your computer will not prevent you from running the command and may not even confirm if this is what you actually want to do. This is of particular concern when the command may have destructive effects.

> Generally, you shouldn't need to run commands with `sudo` in this course. If you're not sure, ask an instructor.

### `rm`

`rm` -- or "remove" -- deletes files with no confirmation. There is no `trash` to recover removed files
from.  So use `rm` with caution.

You should especially use `rm -rf` with caution.

> Based on your knowledge of flags, what does `rm -rf` do?
> Lesson Objective: List unsafe commands

#### Independent Practice - Star Wars! (10 mins)
> Lesson Objective:
  List common commands to
    -  View the path of the current directory
    -  View the contents of a directory
    -  Navigate to different directories
    -  Manage files and directories
***

[Star Wars Lab Instructions](labs/star_wars/README.md)

> Check: Review to make sure students have correct answers for the exercise.

## WDI Environment (10 mins)

#### Directory Structure

Here's the suggested structure for your WDI folder. Please create the following folders if they do not exist.

  * ~/wdi
    * sandbox
    * exercises
    * lessons
    * projects



> Instructor Note: Tailor this to fit the needs of your specific instance of WDI.

***

## Ultimate Time Savers (If Time Allows)

The next three points are reasons not to hold down the arrow or delete keys.

### `ctrl-c`

Cancel whatever you were typing before. Abort!

### `ctrl-e`

Move cursor to the **e**nd of the line.

### `ctrl-a`

Move cursor to the beginning of the line

> a is the beginning of the English alphabet

### The up and down arrows

Cycle through previous commands

### Tab completion

When typing a command that has a file as an argument, like `cd`,
type only the first few letters and hit the TAB key.

### Clear the screen

- ctrl-l
- command-k
- `clear`

## You do: Speed Rounds

Copy and paste each of the following commands into the terminal without
pressing enter.

### 1. Cancel the really long line of text

```
$ kjahlkjhsadlkjfhlaksjdhf asdjkfhlsadjhflkjashdf lasjkhdfjhasd sdjhfjhsgajhgf
```

### 2. Fix the typo at the beginning of the command

```
$ cdd ~/Documents && pwd && ls && ccd -
```

### 3. Fix the typo at the end of the command

```
Same as the previous command
```

***

## Own your terminal (If Time Allows)

#### Styling the default Terminal application
1. [Color your prompt](http://www.cyberciti.biz/faq/bash-shell-change-the-color-of-my-shell-prompt-under-linux-or-unix/)
  - It will be WAY easier to read
2. [Choose a theme](http://apple.stackexchange.com/a/92769)
  - Pick something you like to look at

#### [iTerm2](https://www.iterm2.com/features.html)

Most of the instructors use iTerm2 as a terminal replacement.

My favorite features include:

- A better, more readable font
- Hotkey support (full screen and tabs)
- Unlimited Scroll Back history

***

## Bash Profile Aliases (If Time Allows)

You may have noticed during Installfest that the instructors messed with this file: `~/.bash_profile`.

<details>
  <summary>**Q:** Based on the path, where is this file located?</summary>
  In the home directory (i.e., Users/your-name-here).
</details>

Essentially, we changed the `~/.bash_profile` to make your prompt into a better one!

There will be commands you will find yourself doing frequently. It might become a pain to type out these commands in full all the time. It would be really nice if we could shorten some of these commands... enter aliasing. Aliasing is really quite simple!

Let's open our  `~/.bash_profile` in atom and type in the following...

```
alias greeting="echo 'hello world'"
alias gs='git status'
```

> At this point you may be wondering what exactly "bash" is. Bash is a language we can use to interact with our computer via the shell (via Terminal or some other text-based interface).

#### You Do: Make An Alias

Take the next five minutes to create your own alias and test it. If possible, alias something you think you'll find yourself doing frequently!

***

<a name="conclusion"></a>
## Conclusion (5 mins)
- Review independent practice deliverables
- Recap topics covered in today's lesson and lesson objectives
- Cover homework and/or upcoming tasks




***





### Checks for Understanding

* Why would a developer prefer the command line over a GUI?
* Where can we find help for shell commands?
* Describe 4 bash commands for managing folders and files.
* Describe 2 unsafe commands.
* You are currently in the "code" folder in the below file tree. How would you get to the folder that contains "beach.png" using the command line?

```
home
├── documents
│   └── code
├── photos
│   ├── headshot.jpg
│   └── summer_vacation_2014
│       └── beach.png
└── videos
```

* **BONUS:** Write a command to list only files beginning with your first name. Label the parts of the command.

### Hungry for More?

* `grep`
* `cat`
* `less`
* `find`
* `cal`
* `vim` and `vimtutor`

### Feeling Adventurous?

Bash isn't the only option. Check out zsh (http://code.joejag.com/2014/why-zsh.html) or fish (http://fishshell.com/)

***

### Glossary

*  **Prompt** — is a sequence of (one or more) characters used in a command-line interface to indicate readiness to accept commands. Its intent is to literally prompt the user to take action. A prompt usually ends with one of the characters `$`, `%`, `#`, `:`, `>` and often includes other information, such as the path of the current working directory.

*  **Arguments(Parameters)** — are items of information provided to a program or command when it is started. A program can have many command-line arguments that identify sources or destinations of information, or that alter the operation of the program.

*  **Flags(Options)** — modify the operation of a command; the effect is determined by the command's program. Options follow the command name on the command line, separated by spaces.

*  **Path** - is the description that tells us (or a computer) where a file or folder is on our computer.
***


### ADDITIONAL RESOURCES

- Exercises
	- [Kitchen Organizer](labs/kitchen/README.md)
  - [CLI Gardening](https://github.com/ga-dc/cli_gardening)
	- [Command Line Fu - Challenge](https://github.com/ga-wdi-exercises/command_line_fu)
- Readings
	- [Unix Intro Course](http://www.doc.ic.ac.uk/~wjk/UnixIntro/)
	- [Bash Beginner's Guide](http://www.tldp.org/LDP/Bash-Beginners-Guide/html/)
- Cheat Sheets:
	- https://github.com/0nn0/terminal-mac-cheatsheet/wiki/Terminal-Cheatsheet-for-Mac-%28-basics-%29
	- http://i.imgur.com/1c9y0.png

