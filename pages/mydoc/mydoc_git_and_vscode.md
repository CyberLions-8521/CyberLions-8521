---
title: Using Git and VSCode
tags: [vscode, git]
sidebar: mydoc_sidebar
last_updated: Mar 30, 2022
summary: "VSCode provides integrated support for Git. With additional benefits like extensions, it's much easier to use the controls by VSCode than inputting commands."
permalink: mydoc_git_and_vscode.html
folder: mydoc
---

## Source Control

VSCode has built-in support for Git ([so long you have installed it](mydoc_install_git.md)) which is usually easier to use than using the command line. You can access the majority of controls through the **source control** tab.

{:refdef: style="text-align: center"}
![Source Control Tab](images/source_control_circle.png)
{: refdef}

{% include tip.html content="The number next to the icon indicates the number of files changed in your current repository." %}

## Opening a repository

If VSCode is not in a repository, the source control menu will show options to open a folder with a repository or to clone one from GitHub.

{:refdef: style="text-align: center"}
![Source Control Init Options](images/source_control_open_repo.png)
{: refdef}

{% include important.html content="If these options are grayed out, you probably don't have Git installed. [Install Git through this guide](mydoc_install_git.md)." %}

More often you'll be choosing the latter option. By choosing this option, VSCode will ask you to log into your GitHub account. Afterwards, the command palette will open with a list of your GitHub repositories. You can also type in the name of the author and/or repository. Press enter or click a repo to clone it.

If you have downloaded a repo already, or want to make a local repo before publishing it, then use the former option. If you open a folder *without* a repo, you'll have an option to initialize one. You'll also have the option to publish it to GitHub.

## Checking out branches

You can use the <a href="#" data-toggle="tooltip" data-original-title="{{site.data.glossary.statusbar}}">status bar</a> to quickly <a href="#" data-toggle="tooltip" data-original-title="{{site.data.glossary.checkout}}">check out</a> another branch. Look for the button with branch icon (same icon used for Source Control) and the currently checked out branch's name, and click on it. A dropdown will appear allowing you to select your branch to check out, both from your local repo and the remote repo (prefixed with origin/).

You may alternatively use the source control tab. In the tab, press the 3 dots to access the dropdown, then press `Checkout to...`. Similarly, a dropdown will appear for you to select a branch to checkout to.

## Staging and committing

When you edit, add, or delete files, the name of the file will be colored and a status letter will appear to the right of it. These will also be shown under Source Control > Changes.

{:refdef: style="text-align: center"}
![Source Control Changes](images/source_control_changes.png)
{: refdef}

**M**: Modified. The file's contents were changed from the last commit.<br>
**D**: Deleted. The file was removed.<br>
**U**: Untracked. Means the file was not tracked by the repo before, so it's likely a new file.

If you click on the files in the source control, it will open the difftool - a comparison tool that displays the modifications from the previous commit to the current change. If you hover over the files, there will be 3 options: opening the file, discarding the change, and <a href="#" data-toggle="tooltip" data-original-title="{{site.data.glossary.stage}}">staging</a> the change. Hovering over the dropdown will have a <a href="#" data-toggle="tooltip" data-original-title="{{site.data.glossary.stash}}">stash</a> changes option in place of opening the file option.

## Pushing and pulling

You may push/pull either from the <a href="#" data-toggle="tooltip" data-original-title="{{site.data.glossary.statusbar}}">status bar</a> or source control tab.

After making a local commit, or if the remote branch changes, the status bar's synchronize changes button will update with a downarrow and uparrow. Clicking it will push/pull changes.

The source control tab has a dropdown accessible through the 3 dots. Accessing it shows `Push` and `Pull` as some of the elements. Clicking it will also push/pull changes.

## Fetching

You may fetch from the source control dropdown menu in `Push, Pull > Fetch`. You can also enable automatic fetching by accessing your VSCode settings and setting Git: Autofetch to true.

## Merging and resolving conflicts

{% include links.html %}