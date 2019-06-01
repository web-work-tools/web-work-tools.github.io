---
type: post
title: "Creating a Test Branch and Merging back the Changes"
description: "Used while testing the hugo build of the HPSTR theme."
tags: [hpstr, jekyll, hugo, theme, migration]
image:
  feature: /images/Git_branches_fork.png
  credit: "Bunyk - Українська"
  creditlink: "https://commons.wikimedia.org/wiki/File:Git_branches_fork.svg"
date: 2019-05-31
aliases:
  - /branches-git/
---

I made a test branch for the swapping jekyll for hugo article, and then merged the changes back to master, once I had it running.

## Checkout test branch

Use the command `git checkout -b` will allow you to create a local branch for testing.

I will call my new branch `test-hugo` so the command will be like so:

`git checkout -b test-hugo`

## Some git basics for newbs like me

* [Git Branching and Merging](https://git-scm.com/book/id/v2/Git-Branching-Basic-Branching-and-Merging)

Git keeps track of all your files, but not just the files, but everything in the repository. 

Every commit, git remembers.

> "yes yes I know"

However, it really boggled my mind the first time I tried it locally. 

I can change to a branch or another point in the history of this repository, and git tucks away the one I'm working on... and the whole directory changes and like wait... 

>where did all my files just go? 

When you push a repository to GitHub they keep a copy too.. but git is really awesome beyond github. If it was invented today they would call it a blockchain :rofl:

### Git is Magic!

it sure feels that way, especially the first time I realized what it was doing. I still have a sense of wonder and mystery around Git.

You probably knowbut you don't need github at all, and I'm learning that a significant portion, of git repositories are never exposed to the public. 

>Outside of GitHub and its imitators, most contributors to a project don’t have a published version of their repository online at all, skipping that step and saving some time. - [What is a Fork?](https://drewdevault.com/2019/05/24/What-is-a-fork.html)

`git checkout -b` is just the same as creating a new directory, copy pasting the repo files there to test, and testing it out there. Except git makes it look like magic, and keeps track of your progress!

* [More Git Resources](https://infominer.id/web-work/github-pages-starter-pack/#git) >>

## [Merging changes back to the master branch](https://stackoverflow.com/questions/5601931/what-is-the-best-and-safest-way-to-merge-a-git-branch-into-master)


```
git checkout master
git pull origin master
git merge test
git push origin master
```
