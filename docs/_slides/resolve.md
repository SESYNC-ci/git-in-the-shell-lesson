---
---

## Merge Conflicts

Diverging commits that do not affect the same files, or affect different lines within a file, can usually be merged
automatically. That's what happened in the previous example where everything happened in sequence. First, the owner committed
and pushed, then the collaborator pulled, committed, and pushed, then the owner pulled again. 
But if both owner and collaborator modify the same file simultaneously, git cannot safely merge the commits because 
it has no way of knowing which version to use. If git cannot safely merge commits, it guides you through conflict resolution.
{:.notes}

A "merge conflict" will arise when two contributors change a line of text. For example, if you both add a project description.

===

The owner adds a description under "# About" in the local clone. Meanwhile the collaborator adds a description under "# About" using the GitHub editor in the owner's repository.

~~~markdown
# About

...
~~~
{:.text-document title="README.md"}

===

The owner commits his or her change, but receives an error message from git when attempting to pull.

~~~bash
git pull
~~~
{:.input title="Terminal"}
~~~bash
CONFLICT (content): Merge conflict in <path>
Automatic merge failed; fix conflicts and then commit the result.
~~~
{:.output}

===

Any conflicted region is fenced off in the named files with conflict markers 
and must be manually tidied up.

`<<<<<<<` indicates the beginning of your version of the conflicted section,
then `=======` indicates the beginning of your neighbor's version, which ends
with `>>>>>>>`.
{:.notes}

~~~markdown
<<<<<<< HEAD:master
 ...
=======
 ...
>>>>>>>
~~~
{:.text-document title="README.md"}

===

Follow all the instructions in the original message (or ask again with a 
`git status`):

~~~bash
git status
~~~
{:.input title="Terminal"}
~~~bash
You have unmerged paths.
 (fix conflicts and run "git commit")
 
Unmerged paths:
 (use "git add <file>..." to mark resolution)
~~~
{:.output}

*Important note*: If you find resolving merge conflicts confusing, the best way to avoid them is to **pull before you push**!
That means always pull the most recent version of the repo from the remote before making changes. 
That way, merge conflicts will only occur if you and your collaborator(s) are working on the code at the exact same time.
{:.notes}

===

## Exercise 4

Switch roles with your neighbor and repeat both Exercise 3 and the steps above to
introduce and resolve a merge conflict.
