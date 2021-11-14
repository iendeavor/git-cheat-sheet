Git Fundamental Cheat Sheet [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
===============
<hr>
<p align="center">
    <img alt="Git" src="./Img/git-logo.png" height="190" width="455">
</p>
<hr>

Git Cheat Sheet English
===============
### Index
* [Set Up](#setup)
* [Create](#create)
* [Local Changes](#local-changes)
* [Commit History](#commit-history)
* [Branches & Tags](#branches--tags)
* [Update & Publish](#update--publish)
* [Merge & Rebase](#merge--rebase)

<hr>

## Setup

##### Set a name that is identifiable for credit when review version history:
```
$ git config --global user.name “[firstname lastname]”
```

##### Set an email address that will be associated with each history marker:
```
$ git config --global user.email “[valid-email]”
```

<hr>

## Create

##### Clone an existing repository:

There are two ways:

Via SSH

```
$ git clone ssh://user@domain.com/repo.git
```

Via HTTP

```
$ git clone http://domain.com/user/repo.git
```

<hr>

## Local Changes

##### Changes in working directory:
```
$ git status
```

##### Changes to tracked files:
```
$ git diff
```

##### See changes/difference of a specific file:
```
$ git diff <file>
```

##### Add some changes in &lt;file&gt; to the next commit:
```
$ git add -p <file>
```

##### Commit with message:
```
$ git commit -m 'message here'
```

##### Change last commit:<br>
<em><sub>Don't amend published commits!</sub></em>

```
$ git commit -a
```

<hr>

## Commit History

##### Show all commits, starting with newest (it'll show the hash, author information, date of commit and title of the commit):
```
$ git log
```

##### Show all the commits(it'll show just the commit hash and the commit message):
```
$ git log --oneline
```

##### Show changes over time for a specific file:
```
$ git log <file>
```

##### Show Reference log:
```
$ git reflog show
```

<hr>

## Move / Rename

##### Rename a file:

Rename Index.txt to Index.html

```
$ git mv Index.txt Index.html
```

<hr>

## Branches & Tags

##### List all local branches:
```
$ git branch
```

##### Switch HEAD branch:
```
$ git checkout <branch>
```

##### Checkout single file from different branch
```
$ git checkout <branch> -- <filename>
```

##### Switch to the previous branch, without saying the name explicitly:
```
$ git checkout -
```

##### Create a new branch based on your current HEAD:
```
$ git branch <new-branch>
```

##### Mark `HEAD` with a tag:
```
$ git tag <tag-name>
```

##### List all tags:
```
$ git tag
```

<hr>

## Update & Publish

##### Add new remote repository, named &lt;remote&gt;:
```
$ git remote add <remote> <url>
```

##### Download all changes from &lt;remote&gt;, but don't integrate into HEAD:
```
$ git fetch <remote>
```

##### Get all changes from HEAD to local repository without a merge:
```
$ git pull --rebase <remote> <branch>
```

##### Publish local changes on a remote:
```
$ git push <remote> <branch>
```

##### Publish your tag:
```
$ git push <remote> <tag>
```
<hr>

## Merge & Rebase

##### Merge branch into your current HEAD:
```
$ git merge <branch>
```

##### Rebase your current HEAD onto &lt;branch&gt;:<br>
<em><sub>Don't rebase published commit!</sub></em>

```
$ git rebase <branch>
```

##### Abort a rebase:
```
$ git rebase --abort
```

##### Continue a rebase after resolving conflicts:
```
$ git rebase --continue
```

##### Use your editor to manually solve conflicts and (after resolving) mark file as resolved:
```
$ git add <resolved-file>
```

##### Squashing commits:
```
$ git rebase -i <commit-just-before-first>
```

Now replace this,

```
pick <commit_id>
pick <commit_id2>
pick <commit_id3>
```

to this,

```
pick <commit_id>
squash <commit_id2>
squash <commit_id3>
```
<hr>
