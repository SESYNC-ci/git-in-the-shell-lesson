---
---

## Git in the Shell

The namesake of GitHub is the command-line utility `git`. It performs
the clone, push, pull, and merge procedures just mentioned, and many
more.

===

The software has no GUI of it's own, and works through commands always beginning with "git " given in the shell. The comamnd to turn the "current folder" into a git repo is:

~~~bash
git init
~~~
{:.input}

~~~bash
Initialized empty Git repository in ~/handouts/.git/
Commit your changes with a descriptive but short commit message.
~~~
{:.output}

===

Add files to git's watchlist with the "add" command

~~~bash
git add README.md
git status
~~~
{:.input}

~~~bash
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   README.md

Untracked files:
~~~
{:.output}

===

"Commit" updates the added files in a newly labeled version of your project's history.

~~~bash
git commit -m "initial commit"
~~~
{:.input}

~~~bash
*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: empty ident name (for <(null)>) not allowed
~~~
{:.output}

===

Every commit needs an author. Follow git's instructions, using a
real email address so your commits can be associated with your
GitHub account, and try again.

~~~bash
git commit -m "initial commit"
~~~
{:.input}

~~~bash
[master (root-commit) <sha>] initial commit
 1 file changed, 10 insertions(+)
 create mode 100755 README.md
~~~
{:.output}

===

~~~bash
git status
~~~
{:.input}

~~~bash
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	CONTRIBUTING.md
	data/
	handouts.Rproj
	worksheet-1.R
	worksheet-2.R
	worksheet-3.R
	worksheet-4.R

nothing added to commit but untracked files present (use "git add" to track)
~~~
{:.output}

===

## Checkout the Log

Version control gives you access to the state of the repository at any previous commit. View this history in the log.

~~~
git log
~~~
{:.input}

~~~
commit <sha>
Author: <author>
Date:   <datetime>

    initial commit
~~~
{:.output}

===

## Exercise 1

Introduce a second commit that messes up your README.md or another file. Make sure it shows up in the log.

===

## Revert

Let's investigate the most recent commit.

~~~
git show
~~~
{:.input}

~~~
commit <sha>
Author: <author>
Date:   <datetime>

    <message>

<diff>
~~~
{:.output}

===

The <sha>, even just the first few digits at this stage, are unique to each commit. Use "revert" to undo the changes introduced in a specified commit.

~~~
git revert --no-edit <sha>
~~~
{:.input}

~~~
[master <sha>] Revert <message>
 1 file changed, 1 insertion(+), 1 deletion(-)
~~~
{:.output}
