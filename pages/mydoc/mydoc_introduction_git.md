---
title: Introduction to git
tags: [git]
sidebar: mydoc_sidebar
last_updated: Mar 30, 2022
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

## Repositories and branches

A Git repository (repo) is your project; the collection of files that make up the source code. Any changes made within the repo is tracked by branches.

A branch is essentially a timeline of events to your project. Multiple branches can exist within a repo, and it's possible for a branch to be created from an existing branch (called **branching**) or for one branch to **merge** into another. This feature allows for developers to concurrently work in their own environment before merging their work into a main/master branch.

A typical collaboration structure that uses Git involves a repo with a main/master branch and multiple feature branches. The main branch is the production branch; it is the branch with the most stable changes and ready for deployment. Feature branches are branched from the main branch or other feature branches. They're meant to add a new feature for the main branch and could have unstable changes. Once a feature branch is stable, it's then merged into the main branch.

### Checkout

You can only view one branch at a time. When you're switching between branches, that's called <a href="#" data-toggle="tooltip" data-original-title="{{site.data.glossary.checkout}}">checking out</a> a branch. When you do that, the files in your working directory updates to reflect what's within the checked out branch.

## GitHub

GitHub is a free repository-hosting service. You can create or publish a repository and it'll be hosted on the cloud. This allows for anybody anywhere to collaborate with your project.

GitHub also has other features that extends Git, such as creating [issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues), [pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests), automation with [actions](https://docs.github.com/en/actions), and a lot more.
## Pushing and pulling

To synchronize with the remote repository's branches, you'll want to push and pull. Pushing uploads your branch's changes to the remote branch, while pulling downloads from the remote branch.

Sometimes, there will be merge conflicts when pushing/pulling. This is when Git is unable to figure out how to merge your changes and requires your help. There are multiple tools to resolve conflicts; for using VSCode, see [here](mydoc_git_and_vscode.html#merging-and-resolving-conflicts).

{% include links.html %}