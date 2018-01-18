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

The best practice is to create of shortcut to shared data
files, and reference the local shortcut in code. For example,
use the `ln` command in the shell to create a fake folder
as a relative path inside your repository.

~~~bash
mkdir "~/Google Drive"
ln -s cloud "~/Google Drive/"
~~~
{:.input}

===

## Ignore Exclusions

~~~bash
data/**
cloud/**
~~~
{:.text-document title=".gitignore"}
