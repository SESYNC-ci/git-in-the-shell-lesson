---
---

## What's a GitHub?

![]({{ site.baseurl }}/images/atlassian_workflow.svg){:width="70%"}  
*[Image][comparing-workflows] by Atlassian / [CC BY]*
{:.captioned}

The **origin** is the central copy of the project, a repository that lives on GitHub. Every member of the team uses a **local** copy of the entire project, called a **clone**.

===

![]({{ site.baseurl }}/images/atlassian_pull.svg){:width="60%"}  
*[Image][comparing-workflows] by Atlassian / [CC BY]*
{:.captioned}

Cloning is the initial **pull** of the entire project and all its history. In general, a worker **pulls** the work of other teammates from the **origin** when ready to incorporate their work, and she **pushes** updates to the **origin** when ready to share her own work.

===

A commit is a unit of work: any collection of changes to one or more files in the repository.
A versioned project is like a tree of commits, although the current tree has just one **branch**.
After a worker creates a **clone**, the local copy is viewing the same commit as the **origin**.

![]({{ site.baseurl }}/images/atlassian_clone.png){:width="40%" style="border: none; box-shadow: none;"}  
*[Image][syncing] by Atlassian / [CC BY]*
{:.captioned}

===

A **pull**, or initially a **clone**, applies commits copied from the **origin** to your local repo, syncing them up.

![]({{ site.baseurl }}/images/atlassian_after_pull_top.png){:width="60%" style="border: none; box-shadow: none;"}  
*[Image][syncing] by Atlassian / [CC BY]*
{:.captioned}

===

A **pull**, or initially a **clone**, applies commits copied from the **origin** to your local repo, syncing them up.

![]({{ site.baseurl }}/images/atlassian_after_pull_bottom.png){:width="60%" style="border: none; box-shadow: none;"}  
*[Image][syncing] by Atlassian / [CC BY]*
{:.captioned}

===

A **push** copies local commits to the **origin** and applies them remotely.

![]({{ site.baseurl }}/images/atlassian_after_push_top.png){:width="70%" style="border: none; box-shadow: none;"}  
*[Image][syncing] by Atlassian / [CC BY]*
{:.captioned}

===

A **push** copies local commits to the **origin** and applies them remotely.

![]({{ site.baseurl }}/images/atlassian_after_push_bottom.png){:width="70%" style="border: none; box-shadow: none;"}  
*[Image][syncing] by Atlassian / [CC BY]*
{:.captioned}


[comparing-workflows]: https://www.atlassian.com/git/tutorials/comparing-workflows
[syncing]: https://www.atlassian.com/git/tutorials/syncing/git-pull
[CC BY]: http://creativecommons.org/licenses/by/2.5/au/
