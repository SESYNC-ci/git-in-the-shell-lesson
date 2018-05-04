---
---

## Create a GitHub Repository

1. Sign in or create a GitHub account.

2. Create a new repository on your GitHub page.

===

![]({{ site.baseurl }}/images/new_repo-1.png){:width="50%"}  
{:.captioned}

1. Give the repo a name
1. Add a short "tag line" to jog your memory
1. Do not check the box or add anything

===

## Empty repository

You have created an empty repository. The quick start information provides clues
on how to see your first commits.

===

## Configure your clone

To push and pull from your local repo to GitHub, you must configure your local
repo with the URL of the remote repo. By convention, we call the central copy
the "origin".

~~~
git remote add origin <URL>
git push
~~~
{:.text-document title="{{ site.handouts[0] }}"}

===

Push your commit up to the **origin**.

~~~
Username for 'https://github.com': <username>
Password for 'https://<username>@github.com': 
Counting objects: 9, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 2.10 KiB | 1.05 MiB/s, done.
Total 9 (delta 6), reused 0 (delta 0)
remote: Resolving deltas: 100% (6/6), completed with 6 local objects.
To <url>
   <sha>..<sha>  master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.Counting objects: 3, done.
~~~
{:.output}

===

Take a look at the repository on GitHub.

- There is a space for files
- There is a suggestion to create a `README.md`, a project summary in Markdown.
- You are looking at a branch called "master".
- The commit history is available from the top bar.
- The "Clone or download" button provides a URL.

===

## GitHub Editor

The online editor is good for quick-n-easy fixes, and for working on documentation. Its a bad place to modify code, because it's not tested before reaching the origin. It's great for creating a project README.

===

## Exercise 2

Create a new file called "README.md" and add the following content on separate lines with a blank line in between.

1. A title, preceded by `#` (the markdown "level 1" heading)
1. A "About" section, preceded by `##` (the markdown "level 2" heading)
1. A "Contributors" section, preced by `##`
1. Your name, preceded by `-` (the markdown bulleted list)

As you go, utilize the Preview tab to se the result of rendering your Markdown to HTML.
