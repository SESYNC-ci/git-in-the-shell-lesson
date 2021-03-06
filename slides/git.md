---
---

## Git in the Shell

The namesake of GitHub is the command-line utility `git`. It performs
the clone, push, pull, and merge procedures just mentioned, and many
more.

When using `git` from the command line, you issue commands through
the Unix shell. These commands have their own special syntax. 
If you aren't familiar with Unix shell commands, you might want to 
look at [this lesson from Software Carpentry](https://swcarpentry.github.io/shell-novice/).
Or check out [explainshell.com](https://explainshell.com/), which is a
handy tool that gives you the help text associated with specific shell
commands, including `git` commands.
{:.notes}

===

### Note on terminology and configuration

As of October 1, 2020, all new repositories created on GitHub will have a default branch
called `main`. Previously, the default name was `master`. The [change](https://github.com/github/renaming) was
made to promote inclusive language in the version control world. SESYNC is planning to update 
the GitLab server to match this new default. However, the git client will still
default to `master` if you create a repository locally, unless you configure it as
described below.
You should also be aware that any documentation, tutorial, or StackOverflow
post written before 2020 will assume your default branch is called `master`. 
{:.notes}

We recommend setting the default branch name for new repositories you create 
locally to `main`. Enter the following into your terminal prompt. 

~~~bash
git config --global init.defaultBranch main
~~~
{:.input title="Terminal"}

This option is available for git version 2.28 or later.

===

The software has no GUI of its own, and works through commands always beginning with `git` given in the shell. 
For example, the command to turn the "current folder" into a git repo is `git init`.
You would run `git init` locally from an existing folder containing project code.

~~~bash
cd <path to directory>
git init
~~~
{:.input title="Terminal"}

===

Add files to git's watchlist with the "add" command. This action is also known as "staging" files.

~~~bash
git add <path to files>
git status
~~~
{:.input title="Terminal"}

You can stage all files that have been modified since the last commit with `git add .`.
{:.notes}

===

"Commit" updates the added (staged) files in a newly labeled version of your project's history.


~~~bash
git commit -m "initial commit"
~~~
{:.input title="Terminal"}

~~~bash
*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: empty ident name (for <(null)>) not allowed
~~~
{:.output style="display: block;"}

The above error message appears if you have not yet configured your local machine with
your GitHub user credentials.
{:.notes}

===

Every commit needs an author. Follow git's instructions, using a
real email address so your commits can be associated with your
GitHub account, and try again.


~~~bash
git commit -m "initial commit"
git status
~~~
{:.input title="Terminal"}

Now, author information will be associated with any commits you make.
This is a one-time configuration for each computer on which you use git.
{:.notes}

Saving, staging, and committing are each separate steps, none of which imply any
of the others. This may seem like a hassle, but is a good thing! As your project
grows larger, you will frequently save changes you don't want to commit: staging
lets you choose what changes get packaged into a commit.
{:.notes}

===

## Look at the Log

Version control gives you access to the state of the repository at any previous commit. View this history in the log.


~~~bash
git log
~~~
{:.input title="Terminal"}

~~~bash
commit <sha>
Author: <author>
Date:   <datetime>

    initial commit
~~~
{:.output style="display: block;"}

===

## Exercise 1

Edit your committed file with some small, breaking change. Create a second commit that includes this change, and make sure it shows up in the log.

===

## Revert

Let's investigate the most recent commit.


~~~bash
git show
~~~
{:.input title="Terminal"}
~~~
commit <sha>
Author: <author>
Date:   <datetime>

    <message>

<diff>
~~~
{:.output style="display: block;"}

===

The <sha>, or however many digits of it are needed, provides a unique label for
each commit. Use "revert" to undo the changes introduced in a specified commit.


~~~bash
git revert --no-edit <sha>
~~~
{:.input title="Terminal"}
~~~
[main <sha>] Revert <message>
 1 file changed, 1 insertion(+), 1 deletion(-)
~~~
{:.output style="display: block;"}
