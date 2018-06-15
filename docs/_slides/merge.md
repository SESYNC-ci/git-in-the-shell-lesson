---
---

## Merging

An essential component of the centralized workflow is the ability to merge commit histories that have diverged. Each fork in the log has to be re-integrated, and git does this automatically through merging.

===

~~~
git add <path>
git commit -m 'feel the learn'
~~~
{:.input}

~~~
[master <sha>] feel the learn
 5 files changed, 955 insertions(+)
~~~
{:.output}

===

Merge commits most commonly arise when a commit shows up on GitHub that isn't in your local clone. Such as the current situation.

![]({{ site.baseurl }}/images/atlassian_merge.svg){:width="50%"}  
*[Image][using-branches] by Atlassian / [CC BY]*
{:.captioned}

===

Even though these changes do not conflict, GitHub won't allow you to push. Take a moment to read the message, it gives a good explanation of what has happened.

~~~
git push
~~~
{:.input}

~~~
To https://github.com/<username>/<repo>.git
 ! [rejected]        master -> master (fetch first)
 error: failed to push some refs to 'https://github.com/<username>/<repo>.git'
 hint: Updates were rejected because the remote contains work that you do
 hint: not have locally. This is usually caused by another repository pushing
 hint: to the same ref. You may want to first integrate the remote changes
 hint: (e.g., 'git pull ...') before pushing again.
 hint: See the 'Note about fast-forwards' in 'git push --help' for details.
~~~
{:.output}

===

## Merge Locally

The **origin** does not even attempt to reconcile diverging commit histories; it does
not matter that the diverging commits affect separate files. In order to preserve
the repo, the contributor is always responsible for "overseeing" the merge on a local **clone**.

===

## Take the Hint!

~~~
git pull
~~~
{:.input}

~~~
remote: Counting objects: <progress>
remote: Compressing objects: <progress>
remote: <stats>
Unpacking objects: <progress>
From https://github.com/<username>/<repo>
   <sha>..<sha>  master     -> origin/master
   Auto-merging README.md
   Merge made by the 'recursive' strategy.
    README.md | 1 +
	 1 file changed, 1 insertion(+)
~~~
{:.output}

The message tells you about any changes made by this **merge commit**, which seamlessly integrates changes to the same file by multiple authors.

[using-branches]: https://www.atlassian.com/git/tutorials/
