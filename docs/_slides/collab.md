---
---

## Working with Collaborators

True collaboration goes deeper than commenting on a final report, but integrated work on a project from start to finish raises workflow challenges.

- Be it data, a script, or a write-up, who has the most up-to-date version?
- Will a teammate's work overwrite any of your own?
- How do I recover the working version of code the PI broke?

Centralized workflows, managed by `git`, help solve these challenges.

===

## Project Integrity

- The **origin** becomes the official up-to-date repo, *even* if your work is a few commits ahead.
- Diverging files are easily reintegrated with a **merge** algorithm.
- The complete project history is available to **checkout**.

Note, version control works really well with text. Non-textual components of your project (e.g. large or binary data) rarely live in a repository. Use cloud storage for more static files and a database for dynamic records.
{:.notes}

===

## Create a new file

Create a new text file as below, adding yourself as the first collaborator.

~~~
## Project Collaborators

- ...
- My neighbor!
~~~
{:.text-document title="collaborators.md"}

Our aim is to let your project collaborator replace "My neighbor!" with his or her name.

===

## Track it with git

Before you can commit changes involving a new file, you have to tell the version control system (that's `git`!) to watch it..

```bash
git add collaborators.md
git commit -m 'just me so far!'
```
{:.input}

===

## Push

Look at the `git status` and notice that your branch is ahead of origin/master! Push those commit(s) to your GitHub repo.

===

## Collaborate!

The first step to collaborative workflows is granting access to the **origin** of your project. Introduce yourself to your neighbor, and ask for his/her GitHub username.

===

![]({{ site.baseurl }}/images/repo_collab.png)
{:.captioned}

Add your neighbor as a collaborator, and accept your neighbor's invitation to collaborate!

===

As a collaborator on your neighbors repository, you have permission to edit their `collaborators.md`.

The text below shows "My Neighbor!" where you should see your neighbor's name. Edit the file in your neighbor's repo, by replacing the remaining "My neighbor!" with your own name.
{:.notes}

~~~
## Project Collaborators

- My neighbor!
- ...
~~~
{:.text-document title="collaborators.md"}

Write a meaningful commit message to save your work.

===

## Integrate your Collaborator's work

If you have no uncommited work in your tracked files, you can pull down the new commit from your neighbor and "fast-forward" your project.

```bash
git pull
```
{:.input}
