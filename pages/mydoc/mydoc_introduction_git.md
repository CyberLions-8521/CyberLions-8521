---
title: Introduction to git
sidebar: mydoc_sidebar
last_updated: Mar 28, 2022
summary: "Git is a distributed version control software. Utilizing the concept of branches, Git allows programmers to work in parallel and collaboratively. GitHub is a cloud-based hosting service for managing Git repositories."
permalink: mydoc_introduction_git.html
folder: mydoc
---

## Version Control System

Source code is *the* big cheese of programmers. It is an accumulation of collective thinking, rigorous testing, and constant refining. As such, it has to be highly protected. Accidental deletion, malicious/naive editors, and bad edits all contribute to that fact.

Version Control System (VCS), software that provides version control, is a solution. Version control is the practice of tracking and managing changes to source code - so, if any mistake was made, changes can be rolled back to an earlier version. Unintended consequences can always be undone to an earlier stage.

Another benefit to version control is collaboration. Often, programmers are working concurrently on their own files of the projects. However, sometimes a programmer may make a change that is incompatible with another programmer's edits. Version control allows investigating each change and resolving any conflicts.

### Distributed Version Control System

Git is a Distributed Version Control System (DVCS), meaning everybody has a copy of the repository. Programmers would <a href="#" data-toggle="tooltip" data-original-title="{{site.data.glossary.clone}}">clone</a> a repo from a central server (e.g. GitHub) and work on their local copy of the repo. After doing their edits, they would <a href="#" data-toggle="tooltip" data-original-title="{{site.data.glossary.push}}">push</a> their changes back to the server for other programmers to see.

The advantage to this compared to a Centralized Version Control System (CVCS) (where there is only one repo) is the following:

1. Programmers can work offline and upload changes whenever they're connected.
2. Any errors on the server will not prevent you from working on the code.
3. If the server's repo is accidentally wiped, then because everybody has a copy, a local repo can just be published back again.

{% include links.html %}