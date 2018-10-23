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

~~~markdown
## Collaborators

- <your name>
- My Neighbor
~~~
{:.text-document title="README.md"}

Our aim is to let your project collaborator replace "My Neighbor" with his or
her name.

===

## Commit it with git

Before you can commit changes involving a new file, you have to tell the version control system (that's `git`!) what changes to include.

~~~bash
git add README.md
git commit -m 'just me so far!'
~~~
{:.input title="Terminal"}

===

## Push

Look at the `git status` and notice that your branch is ahead of origin/master! Push those commit(s) to your GitHub repo.

===

## Collaborate!

The first step to collaborative workflows is granting access to the **origin** of your project. Introduce yourself to your neighbor, and decide which of you will be the "owner" and which the "collaborator". The owner will need the collaborator's GitHub username.

===

![]({{ site.baseurl }}/images/repo_collab.png)
{:.captioned}

Add your neighbor as a collaborator!

===

## Exercise 3

As the collaborator on your neighbors repository, you have permission to edit his or her "README.md". Make sure you accept the invitation to collaborate in your email!

The text below shows where you'll see the owner's name if you're looking at the right (not your own). The collaborator should edit the file in the owner's repo, by replacing "My Neighbor" with his or her own name.
{:.notes}

~~~markdown
## Collaborators

- <the owner's name>
- <your name>
~~~
{:.text-document title="README.md"}

Write a meaningful commit message while "saving" your work. Note that on the GitHub editor, there's no distinction between save and commit. The owners should then pull the new commit into their local clone of the project.
{:.notes}
