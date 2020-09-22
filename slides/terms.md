---
---

## What's a GitHub?

![]({% include asset.html path="images/atlassian_workflow.svg" %}){:width="70%"}  
*[Image][comparing-workflows] by Atlassian / [CC BY]*
{:.captioned}

The **origin** is the central copy of the project, a repository that lives on GitHub. Every member of the team uses a **local** copy of the entire project, called a **clone**.

===

![]({% include asset.html path="images/atlassian_pull.svg" %}){:width="60%"}  
*[Image][comparing-workflows] by Atlassian / [CC BY]*
{:.captioned}

Cloning is the initial **pull** of the entire project and all its history. In general, a worker **pulls** the work of other teammates from the **origin** when ready to incorporate their work, and she **pushes** updates to the **origin** when ready to share her own work.

===

A commit is a unit of work: any collection of changes to one or more files in the repository.
A versioned project is like a tree of commits, although the current tree has just one **branch**.
After a worker creates a **clone**, the local copy is viewing the same commit as the **origin**.

Notice that the local and remote (origin) repos are both on a branch called *main* in the diagram
below. This is the default name given to the primary version of the repository.
{:.notes}

![]({% include asset.html path="images/atlassian_clone.png" %}){:width="40%" style="border: none; box-shadow: none;"}  
*[Image][syncing] by Atlassian / [CC BY]*
{:.captioned}

===

When the origin has commits that do not exist in the local repo, it has gotten ahead and a **pull** is required to synchronize state.

![]({% include asset.html path="images/atlassian_after_pull_top.png" %}){:width="60%" style="border: none; box-shadow: none;"}  
*[Image][syncing] by Atlassian / [CC BY]*
{:.captioned}

===

A **pull**, or initially a **clone**, applies commits copied from the **origin** to your local repo, syncing them up
as if you had created identical commits locally.

![]({% include asset.html path="images/atlassian_after_pull_bottom.png" %}){:width="60%" style="border: none; box-shadow: none;"}  
*[Image][syncing] by Atlassian / [CC BY]*
{:.captioned}

===

In the opposite situation, commits created locally are not immediately
synchronized to the **origin**.

![]({% include asset.html path="images/atlassian_after_push_top.png" %}){:width="70%" style="border: none; box-shadow: none;"}  
*[Image][syncing] by Atlassian / [CC BY]*
{:.captioned}

===

A **push** copies local commits to the **origin** and applies them remotely.

![]({% include asset.html path="images/atlassian_after_push_bottom.png" %}){:width="70%" style="border: none; box-shadow: none;"}  
*[Image][syncing] by Atlassian / [CC BY]*
{:.captioned}


[comparing-workflows]: https://www.atlassian.com/git/tutorials/comparing-workflows
[syncing]: https://www.atlassian.com/git/tutorials/syncing/git-pull
[CC BY]: http://creativecommons.org/licenses/by/2.5/au/

