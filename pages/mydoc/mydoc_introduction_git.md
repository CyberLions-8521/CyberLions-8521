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

## Using VSCode and Git

VSCode has built-in support for Git ([so long you have installed it](mydoc_install_git.md)) which is usually easier to use than using the command line. You can access the majority of controls through the **source control** tab.

{:refdef: style="text-align: center"}
![Source Control Tab](images/source_control_circle.png)
{: refdef}

{% include tip.html content="The number next to the icon indicates the number of files changed in your current repository." %}

### Opening a repository

If VSCode is not in a repository, the source control menu will show options to open a folder with a repository or to clone one from GitHub.

{:refdef: style="text-align: center"}
![Source Control Init Options](images/source_control_open_repo.png)
{: refdef}

{% include important.html content="If these options are grayed out, you probably don't have Git installed. [Install Git through this guide](mydoc_install_git.md)." %}

More often you'll be choosing the latter option. By choosing this option, VSCode will ask you to log into your GitHub account. Afterwards, the command palette will open with a list of your GitHub repositories. You can also type in the name of the author and/or repository. Press enter or click a repo to clone it.

If you have downloaded a repo already, or want to make a local repo before publishing it, then use the former option. If you open a folder *without* a repo, you'll have an option to initialize one. You'll also have the option to publish it to GitHub.

### Staging and committing

When you edit, add, or delete files, the name of the file will be colored and a status letter will appear to the right of it. These will also be shown under Source Control > Changes.

{:refdef: style="text-align: center"}
![Source Control Changes](images/source_control_changes.png)
{: refdef}

**M**: Modified. The file's contents were changed from the last commit.<br>
**D**: Deleted. The file was removed.<br>
**U**: Untracked. Means the file was not tracked by the repo before, so it's likely a new file.

If you click on the files in the source control, it will open the difftool - a comparison tool that displays the modifications from the previous commit to the current change. If you hover over the files, there will be 3 options: opening the file, discarding the change, and <a href="#" data-toggle="tooltip" data-original-title="{{site.data.glossary.stage}}">staging</a> the change. Hovering over the dropdown will have a <a href="#" data-toggle="tooltip" data-original-title="{{site.data.glossary.stash}}">stash</a> changes option in place of opening the file option.

{% include links.html %}