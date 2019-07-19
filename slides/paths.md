---
---

## Files under version control

A scripted pipeline relies heavily on plain text files (the scripts),
but may include different file types for figures or even some
data.
 
 - Any file in the directory that is under version control is
   monitored for differences from the committed state of the
   project.
 - Files must be added to at least one commit before they are
   tracked.

===

## Not under version control

The most common pipeline integration is shared data storage, which is
either too large to include or not a flat file.

- Local area network file share (e.g. Z:\\\\...)
- Cloud storeage (e.g. Dropbox, Google Drive)
- Database (e.g. lab PostgreSQL server)

===

## Path to shared data

The best practice is to create of shortcut to a location outside the repository
for data files, and only reference the shortcut in code. For example,
use R's `file.symlink` command to create a fake folder
as a relative path inside your repository.


~~~r
file.symlink(
  from = /path/to/data,
  to = 'data'
)
~~~
{:.text-document title="{{ site.data.lesson.handouts[0] }}"}

===

## Ignoring Files

If you appear to have data files in a subdirectory, git will offer to track them.
You can tell git to ignore these or other files with a special "dot" file:

~~~bash
data/**
~~~
{:.text-document title=".gitignore"}
