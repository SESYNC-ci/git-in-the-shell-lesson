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
1. Leave the boxes (including the "README") un-checked

===

## Empty repository

You have created an empty repository. The quick start information provides clues on how to create your first commit.

===

## Configure your clone

To push and pull from your local repo to GitHub, you must configure your local repo with the URL of the remote repo. By convention, we call the central copy the "origin".

~~~
git remote add origin <URL>
~~~
{:.input}

===

Push your commit up to the **origin**.

~~~
git push
~~~
{:.input}

~~~
Username for 'https://github.com': <username>
Password for 'https://<username>@github.com': 
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 353 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/itcarroll/test.git
   %hash%..%hash%  master -> master
~~~
{:.output}

===

Take a look at the repository on GitHub.

- `README.md` is a Markdown file giving basic information about the repository.
- There is a list of files, including a folder for data.
- You are looking at a branch called `master`.
- The commit history is available from the top bar.
- The "Clone or download" button provides a URL.

===

## GitHub Editor

The online editor is good for quick-n-easy fixes, and for working on documentation. Its a bad place to modify code, because it's not tested before reaching the origin.

===

~~~bash
git pull
~~~
{:.input}
