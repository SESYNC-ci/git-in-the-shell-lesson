---
---

## Git in the Shell

The namesake of GitHub is the command-line-utility `git`. It performs
the clone, push, pull, and merge procedures just mentioned, and many
more.

===

~~~bash
git init .
~~~
{:.input}

~~~bash
Initialized empty Git repository in ~/handouts/.git/
Commit your changes with a descriptive but short commit message.
~~~
{:.output}

===

Add paths to git's watchlist, and then commit the current "version"
to your project's long history.

~~~bash
git add README.md
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

Every commit needs an author. Follow git's instructions, using a real email address so your
commits can be associated with your GitHub account, a bit later on.

===

~~~bash
git commit -m "initial commit"
~~~
{:.input}

~~~bash
[master (root-commit) 248b03e] initial commit
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

Version control gives you access to the state of the repository at any commit. To view the history, look at the log.

~~~
git log
~~~
{:.input}

~~~
commit 0517b3b2258e6cce76770646f175dc8abfe9e148
Merge: 8612809 26c2dcd
Author: Ian Carroll <icarroll@sesync.org>
Date:   Tue Jul 26 14:53:22 2016 -0400

    Merge branch 'master' of https://github.com/itcarroll/test
	
commit 8612809b6eeea263a853783cf4c37a6862a31d22
Author: Ian Carroll <icarroll@sesync.org>
Date:   Tue Jul 26 13:48:57 2016 -0400

    amazing
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
commit 8612809b6eeea263a853783cf4c37a6862a31d22
Author: Ian Carroll <icarroll@sesync.org>
Date:   Fri Jun 24 13:48:57 2016 -0400

    amazing
	
diff --git a/README.md b/README.md
index 521cb5d..24a865d 100644
--- a/README.md
+++ b/README.md
@@ -1,4 +1,4 @@
-# Welcome to My Project
+# Welcome to My Amazing Project

This project does the following:
 + nothing
~~~
{:.output}

===

~~~
git revert --no-edit 8612
~~~
{:.input}

~~~
[master b0aaef0] Revert "amazing"
 1 file changed, 1 insertion(+), 1 deletion(-)
~~~
{:.output}
