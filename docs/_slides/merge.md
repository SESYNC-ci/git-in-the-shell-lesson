---
---

## Merging

An essential component of the centralized workflow is the ability to merge commit histories that have diverged. Each fork in the log has to be re-integrated, and git does this automatically through merging.

===

~~~
git commit -am 'add important info to README.md'
~~~
{:.input}

~~~
[master %hash%] amazing
 1 file changed, 1 insertion(+), 1 deletion(-)
~~~
{:.output}

===

Merge commit's most commonly arise when a commit shows up on GitHub that isn't in your local clone. Create this situation using the GitHub editor.

![]({{ site.baseurl }}/images/atlassian_merge.svg){:width="30%"}  
*[Image][using-branches] by Atlassian / [CC BY]*
{:.captioned}

===

~~~
git push
~~~
{:.input}

~~~
To https://github.com/%username%/test.git
 ! [rejected]        master -> master (fetch first)
 error: failed to push some refs to 'https://github.com/%username%/test.git'
 hint: Updates were rejected because the remote contains work that you do
 hint: not have locally. This is usually caused by another repository pushing
 hint: to the same ref. You may want to first integrate the remote changes
 hint: (e.g., 'git pull ...') before pushing again.
 hint: See the 'Note about fast-forwards' in 'git push --help' for details.
~~~
{:.output}

Take a moment to read the message -- it gives a good explanation of what just happened.

===

## Take the Hint!

~~~
git pull
~~~
{:.input}

~~~
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/%username%/test
   15bc488..26c2dcd  master     -> origin/master
   Auto-merging README.md
   Merge made by the 'recursive' strategy.
    README.md | 1 +
	 1 file changed, 1 insertion(+)
~~~
{:.output}

The message tells you about any changes made by this **merge commit**, which seamlessly integrates changes to the same file by multiple authors.
