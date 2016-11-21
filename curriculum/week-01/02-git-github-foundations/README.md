
# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Git and Github Foundations (90 mins)

| Timing | Type | Topic |
| --- | --- | --- |
| 5 mins | [Opening](#opening) | Why Version Control? |
| 10 mins | [Introduction](#introduction) | Version Control |
| 25 mins | [Demo](#demo) | Git Configuration and Skills |
| 10 mins | [Independent Practice](#ind-practice) | Topic |
| 25 mins | [Demo](#demo) |Git Skills Continued |
| 15 mins | [Conclusion](#conclusion) | Review of Key Terms |

### LEARNING OBJECTIVES
**After this lesson, you will be able to:**  

- Understand basic git commands like init, add, commit, push, pull and clone  
- Distinguish between local and remote repositories   
- Create, copy, merge, and delete local and remote repositories & branches using git commands  
- Describe how branching and merging allows for collaboration during development   
- Fetch changes from a remote without merging them into your own
- Fork and clone remote repositories  
- Differentiate between navigating the file system using the command line vs. the GUI  

---
<a name="opening"></a>
## Opening (5 mins)

Students should split into pairs or small groups and spend a few minutes discussing the following questions: Assuming that version control systems did not exist, how would you:

* Share your source code with other developers?
* Collaborate with other developers?
* Manage multiple versions of a software product?
    - Free vs. Paid
    - Basic vs. Premium
    - 2.x vs. 3.x

Follow activity with a brief recap of student discussions.

***

<a name="introduction"></a>
## Intro to New Material: Version Control (10 mins)

### What is Version Control?

* Version Control is the management of changes to documents, computer programs, web sites, and other collections of information.
* Version Control provides:
    - a database containing a history of changes to a set of files
    - a set of commands for managing that database

### What is Version Control Good For?

* Manage Changes Over Time  
    - Save various points in the development of your work  
    - See the history of your work  
    - Go "Back In Time" to see previous versions of your work  
    - Manage multiple versions of a software project  
* Sharing & Collaboration  
    - Share your work with others  
    - Work effectively as a team on a single project  
    - Allow others to modify your work in a controlled way  
    - Make multiple changes to a project in parallel  
    - Merge parallel changes in a controlled way  
* Experimentation  
    - Experiment with various ideas and either keep or discard your experiments  
    - Keep multiple changes isolated until they are ready to be integrated  

***

<a name="demo"></a>
## Demo: Git Configuration and Skills (25 mins)

As a class, we are going to walk through key Git skills that you will need to be successful in this course. Some of the goals of this session include:  

* Check our GIT configuration

* Develop our GIT Skills  
    - Create a Local GIT repo  
    - Add files  
    - Make commits  
    - Check the repo status  
    - View history  
    - Time travel  

### Part 1 - Setup

Check the GIT Version:  
```
$ which git
$ git --version
```

If you don't have git installed via brew, you should do so now:
```
brew install git            # use brew to install latest version of git    
which git                   # should return "/usr/local/bin/git"
```

Check your GIT Config:
```
$ git config --list
$ git config user.name
```

Set your identity:
```
$ git config --global user.name "John Doe"    
$ git config --global user.email johndoe@example.com
```

Set your default editor:
```
$ git config --global core.editor "subl -n -w"
```

### Part 2 - Creating a repo
Create a new local GIT repository:

```
$ cd ~/ga/wdi/exercises/learning-git
$ mkdir sample1  
$ cd sample1  
$ git init
```

* What just happened?
* Did your Shell Prompt change?

### Part 3 - Our first commit

Add some files:
```
$ touch README.md hello.txt  
$ git status                  # What is an untracked file?
$ git add -A                  # Now the files are in the stage
$ git status
```

Commit the changes:
```
$ git commit -m "Added 2 files."
$ git status
$ git log
```

> Instructor Note:  On the whiteboard, draw a diagram of the following:
- working area  
- stage  
- git repository (.git)  

<!-- SME Needed: Insert File Status Lifecycle Image -->
![Github lifecycle](assets/picture.jpg)

<!-- SME Needed: Insert Basic Git Workflow Image -->

### Part 4: More Commits, and Viewing the History

Edit hello.txt and commit the following changes.

Modify a file:
```
$ echo "Hello, World" >> hello.txt
$ git status
```

We now see a "modified" file, but nothing is staged.
Let's add our changes to the stage:
```
$ git add .
$ git status
```

Now our changes are staged and we can do a commit:
```
$ git commit -m "Fixed hello.txt"
```

Let's view the repo history:
```
  $ git log
```

* Notice all of the info in the log.
* In what order are the commits displayed?

***

<a name="ind-practice"></a>
## Independent Practice: Changes and Commits (10 mins)
Make some very simple changes to your file and commit them. Be sure to check your status and history as you go.

* Suggested changes:
    - Hello General Assembly
    - Hello WDI
    - Hello GIT

> Instructor Note: Leave a couple minutes to demo the solution.


<a name="demo"></a>
## Demo: Git Skills Continued (25 minutes)

### Part 5: Cherry Picking:
Demo the editing of multiple files but only adding one of them to the stage.
```
git add file1   
git commit  
git status  
git log
```

### Part 6: Checking out a Previous Version:

To see the old version:
```
git log  
git checkout <hash_of_previous_commit>
cat hello.txt  
```

To look at the history:
```
git log  
```
* Note: by default the log command only shows up to the current commit we are on

To see all of the commits:
```
git log --all --decorate
```
* Note: what is HEAD and master?  

To return to the most recent version (two options):
```
git checkout master  

# or

git checkout <hash_of_most_recent_commit>  
```

### Part 7: Diffing
View unstaged differences:
```
git diff  

# or  

git diff filename  
```

View staged differences  
```
git diff --staged

# or  

git diff --staged filename
```

### Part 8: Rolling Back Changes
Un-stage changes to a file  
```
git reset filename  
git status  
```

Discarding changes (reverting to the committed version):
```
git checkout filename  
git status
```  
***

<a name="conclusion"></a>
## Conclusion (15 mins)
* Review Git Terminology:
    - repository - a collection of related commits that form a directed acyclic graph
    - commit - a snapshot of the working tree at a giving time (along with a message of what changed)
    - the index (stage) - a staging area where we list changes we want to commit
    - branch - a set of commits that form a linear progression of changes
    - master - the default name for the "main" development branch
    - tag - an optional label on a commit
    - HEAD - what is currently checked out
    - working area - the directory and subdirectories containing the files we are currently working on
* Review Questions:  
    - Can someone tell me what a GIT Repository is?
    - What are some key components of a GIT repo?
    - Can someone describe an important GIT command (get several responses from students)

***

### ADDITIONAL RESOURCES
- [Git Cheat Sheet](https://raw.githubusercontent.com/ATL-WDI-Curriculum/local-and-remote-git/master/images/Git-Cheat-Sheet.png)
- Readings
    - [Git Documentation](https://git-scm.com/documentation)
    - [Forking on Github](https://help.github.com/articles/fork-a-repo/)
    - [Syncing a fork](https://help.github.com/articles/syncing-a-fork/)

- Videos
    - [Lynus Travalds on Git](https://www.youtube.com/watch?v=4XpnKHJAok8)
