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

===

Add files to git's watchlist with the "add" command

~~~bash
git add <path>
git status
~~~
{:.input}

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
{:.output style="display: block;"}

===

Every commit needs an author. Follow git's instructions, using a
real email address so your commits can be associated with your
GitHub account, and try again.


~~~bash
git commit -m "initial commit"
~~~
{:.input}

===


~~~bash
git status
~~~
{:.input}

===

## Checkout the Log

Version control gives you access to the state of the repository at any previous commit. View this history in the log.


~~~bash
git log
~~~
{:.input}

~~~bash
commit <sha>
Author: <author>
Date:   <datetime>

    initial commit
~~~
{:.output style="display: block;"}

===

## Exercise 1

Edit your commited file with some small, breaking change. Create a second commit that includes this change, and make sure it shows up in the log.

===

## Revert

Let's investigate the most recent commit.


~~~bash
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
{:.output style="display: block;"}

===

The <sha>, or however many digits of it are needed, provides a unique label for
each commit. Use "revert" to undo the changes introduced in a specified commit.


~~~bash
git revert --no-edit <sha>
~~~
{:.input}
~~~
[master <sha>] Revert <message>
 1 file changed, 1 insertion(+), 1 deletion(-)
~~~
{:.output style="display: block;"}