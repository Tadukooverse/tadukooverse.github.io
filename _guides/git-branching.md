---
title: Git Branching Guide
blurb: How we use Git branches at Tadukooverse.
developer: true
---
The basic guideline for Git branches is that every release and GitHub issue currently being developed should have its own branch. Also, when a branch is merged into another successfully, it should be 
deleted.

To be more specific, when starting development on a new release, a new branch should be made off of master and be named like ```<version>-SNAPSHOT``` (e.g. ```0.2-Alpha-SNAPSHOT```). This branch 
will be treated like the "release candidate" branch for the release, and should only contain completed features at all times. When you create this branch, update the version strings in Maven and 
commit that change to the new branch. From this point, all development on this release should happen in branches off of this main one.

**Note**: If you're making a minor or patch release on an old version, you would branch off of the appropriate release tag instead of branching off of master, but the naming and further process 
would be the same. (e.g. if Alpha v.0.2 is out and we need to make Alpha v.0.1.1 for some bug fixes, you'd branch off the tag for Alpha v.0.1 instead of branching off master).

When starting development on a new issue, a new branch should be made off of the appropriate "release candidate" branch and be named like ```<release candidate branch name>-<issue name>``` 
(e.g. ```0.2-Alpha-SNAPSHOT-Tadukoo-Look-&-Feel```). In most cases, this branch will be the branch you develop on.

**Note**: If the issue is an Epic (an issue composed of multiple sub-issues), this branch will be treated like a "release candidate" for the issue, and should only contain completed sub-issues 
at all times. The sub-issues would branch off of the Epic's branch, and will be treated as normal development branches.

When development on an issue is completed, create a pull request back to the version's (or Epic's) release candidate branch (after updating your branch to it). Once the pull request is approved 
and merged, the issue's branch may be deleted.

When development of a new release is completed, create a pull request back to master. Once the pull request is approved, delete the branch and create a new GitHub release, creating a proper tag 
for the release. This tag will be used for branching off that version in the future if needed.
