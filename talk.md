## Setup 

```bash
# You should set these two:
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

# Optional, but recommended:
git config --global color.ui "auto"

# Optionally, pick one editor to use: 
git config --global core.editor "nano"        # Default, if you do nothing.
git config --global core.editor "gedit -w -s" # Recommended option.
git config --global core.editor "vim"  
git config --global core.editor "emacs"  
```

Setup up a GitHub account if you don't already have one:
[www.github.com](www.github.com)

Note: Give people time to get settled. They should run this if have they time.



# Disclaimer:
I tend to talk really fast when I get excited, may use magical shortcuts
and hotkeys without thinking about it,
so if I do something you don't understand:

**PLEASE** tell me to
"slow down and explain yourself!"

Note: That being said, I like to keep things informal so please
      ask questions during the talk.



# Git and Github
## Introduction to Source Control
[Michael Sergio](www.github.com/michaelsergio)

Note: Show of hands
  * Range: Seniors, Juniors, Sophmores, Freshman, Grads, CS,SE,non majors?
  * How many have used Git before. Github?
  * Worked on coding projects together.



## Problem 1:
You have code that works.

Now you have to implement a new feature.

After changing a few things, nothing works anymore.

What do you do?

Note: 
That's what the Undo button is for.
But what about code from 6 months ago.
Even 6 hours ago. 6 minutes ago - new feature.
Concept of revision may be good here. Working on multiple copies of code.



## Problem 2:
You're working on a project with someone.

You make some changes. 

How do you give those changes back?

Note: USB, Dropbox.




## Possible Solutions to Problem 2.
Carrier Pidgeon (RFC 1149)

Dropbox

Sneakernet - USB

```bash
Never underestimate the bandwidth of a station wagon full 
of tapes hurtling down the highway.
                                    - Andrew S. Tanenbaum
```

How do you put the data back together so that it works?

Note: A Standard for the Transmission of IP Datagrams on Avian Carriers



## Better Tools - A History
1974 Douglas McIlroy writes diff for Unix 5th Edition.

```diff
--- /path/to/original''timestamp''
+++ /path/to/new''timestamp''
@@ -1,3 +1,9 @@
+This is an important +notice! It should therefore be located at
+the beginning of this document!
+
This part of the document has stayed the same from version to
@@ -5,16 +11,10 @@
be shown if it doesn't change.  Otherwise, that would not be helping to
-compress the size of the changes.
-
-This paragraph contains
-text that is outdated.
-It will be deleted in the
-near future.
+compress anything.
```

1985 Larry Wall writes patch for sending diffs through networks.

Note: Not a new problem.
      diff can also be called a delta. or a difference in files. 
      patch takes those diff files and updates your current files.
      In 1985 networks, you didn't want to send a whole file.



## History 
* 1972 **SCSS**  - Source Code Control System *- Bell Labs*
* 1982 **RCS**   - Revision Control System
* 1986 **CVS**   - Concurrent Versions System 
* 2000 **SVN**   - Subversion
* 2002 **DCVS**  - Distributed Concurrent Versions System
* 2005 **Bazaar**
* 2005 **Mercurial**
* 2005 **Git**

Note: These terms are used interchangeably now a days.
      But what happened in 2005 with all these 



## Problem 3 
You're in charge of a project used by millions of users.

You receive thousands of patches per release.

You don't trust everyone.

You're Finnish.



## What doesn't work
Centralized Workflow

![[centralized]](img/centralized.png)

**Push** and **Pull** from Central Repository

Note: Define Repository of code.
      Define: **push, pull**. 
      Not a bad model. Used by SVN.
      Problem: Who decides merges?




## Distributed Workflow
![[Integration model]](img/integration-manager.png)

1. Developer **pulls** a fork from the Blessed Repo.
2. Developer **commits** changes to private repo.
3. Developer **pushes** to their own public repo.
4. Integration Manager **pulls** from each developers public repo.
5. When well tested, manager **pushes** back to blessed repo.

Note: Every developer has their own separate **branch**.
  



## Linux Workflow
![[Dictator model]](img/benevolent-dictator.png)
For the Linux Kernel, different sub-systems have their own maintainers:
networking, CPU, power, all the various drivers, etc...

Note: You have the same structure as a distributed workflow but with more
      social structure.



## Why Use A Distributed System?
Must get **forking** and **merging** right

Otherwise everything falls apart.



## Development Workflow
![[simple-workflow]](img/main-dev-branch.png)



## Development Workflow
![[feature branch]](img/feature-dev.png)



![[full branch workflow]](img/branches.png)
Note: No title on this slide




# Got It? 
# Good.
# Lets do it!



### https://github.com/michaelsergio/purrfect



## Pull Request
https://github.com/blog/1124-how-we-use-pull-requests-to-build-github
Note: How GitHub uses GitHub internally.


## Staging
![[staging]](img/staging.png)




## Git Ettiquite
* If it’s not in source control, it doesn't exist!
* Commit early, commit often!
* Always look at your changes before committing them.
* Compilation output does not belong in source control. Use .gitignore files!
* Remember the axe-murderer when writing commit messages.



## Applications of GitHub
* Package Mangers
* Continious Integration
* Discover new projects and tools.
* Click Explore on the GitHub main page for more.
* https://github.com/explore



## Beyond Code 
* [Supports Viewing of Maps](https://github.com/blog/1528)
* [Supports 3D models](http://github.com/blog/1465)
* Books
* German Law - bundestag
* https://github.com/showcases
Note: Ruby Gems, Cocapods, Node packages



## Continuous Integration
You should not ever edit code directly on a server!

Push code to a remote service.

Have it tested and deployed automatically.

Etsy deploys more than 50 times a day.

Note: Etsy uses Jenkins as CI tool.



## Git is a tool
### Professionals Invest in their tools!
Learn your Unix tools, your Text Editor, your Source Control, your scripting
languages.

Don't be afraid!

"Civilised tool for a civilized age" -  some guy on the internet
Note: You may not always use the same tool.



## Why do we use version control?
To protect us from ourselves.
Note: Software is complex, every part is moving at once. Always use it!



# Appendix
Note: Add anything else that doesn't fit below.



## Contributing Ettique
* Pay attention to style guides used.
* Always include a README.md!
* Your README should always include how to build and run your project.
Note: CommonMark 



## Software Licenses
[TLDR Legal](https://tldrlegal.com/)
Note: As a professional you should know the basic differences.



## Why is Git so fast?
### It's a DAG
Directed Acyclic Graph
Note: Learn your data structures!



# Questions?



## References
* [Coming from SVN](http://merrigrove.blogspot.com/2014/02/why-heck-is-git-so-hard-places-model-ok.html)
* [Git is a DAG](http://eagain.net/articles/git-for-computer-scientists/)
* [20 GitTips](http://www.javaworld.com/article/2113465/developer-tools-ide/git-smart-20-essential-tips-for-git-and-github-users.html)



## Tutorials
* [Stanford Git Tutorial](http://www-cs-students.stanford.edu/~blynn/gitmagic/ch02.html#_saving_state)
* [Git Architecture](http://aosabook.org/en/git.html)
* [Learn Git Branching](http://pcottle.github.io/learnGitBranching/)

* [Fundamentals](http://gitimmersion.com/index.html)
* [Walkthorugh](http://think-like-a-git.net/)



## Books
* [Pragmatic Guide to Git - Good Intro](http://pragprog.com/book/pg_git/pragmatic-guide-to-git)
* [Git SCM - Online, Free, Up-to-date](http://git-scm.com/book/en/v2)
* [Pragamtic Programmer - Classic for every developer](http://www.amazon.com/The-Pragmatic-Programmer-Journeyman-Master/dp/020161622X)



### Links
[History of SCM](http://en.wikipedia.org/wiki/History_of_software_configuration_management)



# Giveaway!
Note: Homework, do it right now.
      If you have a side project in mind or an idea, go to your GH page.
      Create a new repo. Does it have a name, name it now. Otherwise use the
      default repo name it gives you.
      By the end of the week, start something.



