---
---

## Create a GitHub Repository

1. Sign in or create a GitHub account.

2. Create a [personal access token][pat].

**IMPORTANT**: As of August 2021, a personal access token is now required to authenticate
pushing to a remote repo. The link above is to a GitHub documentation page
with very detailed instructions on how to navigate to the settings page where
you can generate a token. When you are prompted to select the scopes 
(permissions) to give the token, check the box marked `repo`.
After you generate the token, save it in a safe 
place; you will need it in a moment. The best place to save it long-term is 
a password manager such as [LastPass](https://www.lastpass.com).
{:.notes}

===

3\. Create a new repository on your GitHub page.

===

![]({% include asset.html path="images/new_repo-1.png" %}){:width="50%"}  
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
~~~
{:.input title="Terminal"}

===

Push your commit up to the **origin**.

**IMPORTANT**: When you are prompted to enter your password, **paste your personal access token** 
into the prompt, *not* the password that you use to sign in to GitHub.com in your browser. 
On Windows you will need to use `Shift`+`Insert` or right-click to paste, because `Ctrl`+`V` 
will not work in a terminal window.
{:.notes}

~~~
git push
~~~
{:.input title="Terminal"}
~~~
Username for 'https://github.com': <username>
Password for 'https://<username>@github.com': 
Counting objects: <progress>
Delta compression using up to 4 threads.
Compressing objects: <progress>
Writing objects: <progress>
<stats>
remote: Resolving deltas: <progress>
To 'https://github.com/<username>/<repo>.git'
   <sha>..<sha>  main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
Counting objects: <progress>
~~~
{:.output}

===

Take a look at the repository on GitHub.

- There is a space for files
- There is a suggestion to create a `README.md`, a project summary in Markdown.
- You are looking at a branch called **main**.
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

As you go, utilize the Preview tab to see the result of rendering your Markdown to HTML.

[pat]: https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token
