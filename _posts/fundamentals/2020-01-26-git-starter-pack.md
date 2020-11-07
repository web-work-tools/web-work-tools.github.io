---
layout: page-fullwidth
title: "Git Starter Pack"
teaser: "Curated collection of info for using the Git Version Control System."

categories: ['JAMStack','Fundamentals']
tags: ['git']

header: no
image:
  title: "Git_session.png"
  caption: "commons.wikimedia.org/wiki/File:Git_session.svg"
  caption_url: "https://commons.wikimedia.org/wiki/File:Git_session.svg"

date: 2020-01-27
permalink: /git-starter-pack/

---
<div class="row">
<div class="medium-4 medium-push-8 columns" markdown="1">
<div class="panel radius" markdown="1">
**Table of Contents**
{: #toc }
*  TOC
{:toc}
</div>
</div><!-- /.medium-4.columns -->



<div class="medium-8 medium-pull-4 columns" markdown="1">
{% include _improve_content.html %}


## Origin and History

* [A Git Origin Story](https://www.linuxjournal.com/content/git-origin-story)
  > A look at Linux kernel developers' various revision control solutions through the years, Linus Torvalds' decision to use BitKeeper and the controversy that followed, and how Git came to be created.
  > 
  > Originally, Linus Torvalds used no revision control at all. Kernel contributors would post their patches to the Usenet group, and later to the mailing list, and Linus would apply them to his own source tree. Eventually, Linus would put out a new release of the whole tree, with no division between any of the patches. The only way to examine the history of his process was as a giant diff between two full releases. 
* [10 Years of Git: An Interview with Git Creator Linus Torvalds](https://www.linuxfoundation.org/blog/2015/04/10-years-of-git-an-interview-with-git-creator-linus-torvalds/)
  > Torvalds: I really never wanted to do source control management at all and felt that it was just about the least interesting thing in the computing world (with the possible exception of databases ;^), and I hated all SCM’s with a passion. But then BitKeeper came along and really changed the way I viewed source control. BK got most things right and having a local copy of the repository and distributed merging was a big deal. The big thing about distributed source control is that it makes one of the main issues with SCM’s go away – the politics around “who can make changes.” BK showed that you can avoid that by just giving everybody their own source repository. But BK had its own problems, too; there were a few technical choices that caused problems (renames were painful), but the biggest downside was the fact that since it wasn’t open source, there was a lot of people who didn’t want to use it. So while we ended up having several core maintainers use BK – it was free to use for open source projects – it never got ubiquitous. So it helped kernel development, but there were still pain points.
* [10 Years of Git - Atlassian](https://www.atlassian.com/git/articles/10-years-of-git) - timeline
  > 10 years ago Linus Torvalds started writing code for a new distributed version control system on a Sunday and only a mere few days later, the world was given the gift of Git. Git has helped teams big and small work faster while becoming more distributed and has left its mark with cheap local branching, easier code review, flexible work flows and so much more. Over the last decade Git has seen exponential growth and has become the most popular version control system today. Take a walk down memory lane to see how Git has evolved over the years and join us in celebrating the history of Git.
* [Linus Torvalds Invented Git, But He Pulls No Patches With GitHub](https://www.wired.com/2012/05/torvalds-github/)
  > Linus Torvalds keeps a copy of his Linux kernel project on GitHub, the wildly popular code-hosting website. But there's a caveat. If you try to send him a patch or a bug-fix via GitHub, he'll tell you to take a hike.
* [History of Git](https://hackaday.com/2017/05/11/history-of-git/)
  > Git is one of those tools that is so simple to use, that you often don’t learn a lot of nuance to it. You wind up cloning a repository from the Internet and that’s about it. If you make changes, maybe you track them and if you are really polite you might create a pull request to give back to the project. But there’s a lot more you can do. For example, did you know that Git can track collaborative Word documents? Or manage your startup files across multiple Linux boxes?

## Getting Started with Git Fundamentals

* [How to undo (almost) anything with Git](https://github.blog/2015-06-08-how-to-undo-almost-anything-with-git/)
  > One of the most useful features of any version control system is the ability to “undo” your mistakes. In Git, “undo” can mean many slightly different things.
  > 
  > When you make a new commit, Git stores a snapshot of your repository at that specific moment in time; later, you can use Git to go back to an earlier version of your project.
* [Most commonly used git tips and tricks.](http://git.io/git-tips)
* [Working with Remotes](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes)
  > To be able to collaborate on any Git project, you need to know how to manage your remote repositories. Remote repositories are versions of your project that are hosted on the Internet or network somewhere. You can have several of them, each of which generally is either read-only or read/write for you.
* [Writing Effective Commits](https://chris.beams.io/posts/git-commit/)
  > If you haven’t given much thought to what makes a great Git commit message, it may be the case that you haven’t spent much time using git log and related tools. 
* [managing-commit-signature-verification](https://help.github.com/en/articles/managing-commit-signature-verification)
  > You can sign your work locally using GPG or S/MIME. GitHub will verify these signatures so other people will know that your commits come from a trusted source. GitHub will automatically sign commits you make using the GitHub web interface.

>Outside of GitHub and its imitators, most contributors to a project don’t have a published version of their repository online at all, skipping that step and saving some time. - [What is a Fork?](https://drewdevault.com/2019/05/24/What-is-a-fork.html)

### Cheat Sheets

* [davfre/git_cheat-sheet.md](https://gist.github.com/davfre/8313299)
  > `git status` list which (unstaged) files have changed
  > `git diff` list (unstaged) changes to files
  > `git log` list recent commits
* [education.github.com - GIT CHEAT SHEET](https://education.github.com/git-cheat-sheet-education.pdf)
* [Git CheetSheet](https://github.com/jonathancross/jc-docs/blob/master/Git-CheatSheet.md)
  > Git can be challenging to learn and often makes the easy complicated in its attempt to make the complicated easy. This is a collection of notes, aliases, shortcuts and explanations that help me to survive.

```
git add --update # stages only the files which are already tracked and not new
git commit --amend     # Change previous commit message and / or add staged files.
git show --name-status # Show diff of previous commit
git log --stat # Show latest changes committed
git checkout [BRANCH NAME] # To switch to a particular branch
git checkout -b [BRANCH NAME] # To CREATE a new branch
git remote set-url origin git@github.com:jonathancross/pics.jonathancross.com.git # Allow git push via ssh without password
git remote -v  # Show the remotes that are configured: https://help.github.com/articles/fork-a-repo/
```

### Create Test Branch + Merge Changes

This is a little walkthru I made for myself when [trying out a Hugo theme](/jamstack/jekyll-hpstr-hugo-theme/) for this website. I made a test branch for the new theme, and merged the changes merged the changes to master, once I had it running.

* [Git Branching and Merging](https://git-scm.com/book/id/v2/Git-Branching-Basic-Branching-and-Merging)

Use the command `git checkout -b` will allow you to create a local branch for testing.

I called the new branch `test-hugo`:

`git checkout -b test-hugo`

`git checkout -b` creates a duplicate of your repository isolated from your working project, so you can test out and break things without effecting your working product.

* [Merging changes back to the master branch](https://stackoverflow.com/questions/5601931/what-is-the-best-and-safest-way-to-merge-a-git-branch-into-master)


```
git checkout master
git pull origin master
git merge test
git push origin master
```

### Submodules
* [Git Tools - Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules) - so you can pull other git repos into your project
* [Git Submodule Tips](https://gist.github.com/ChristopherA/23ff68d549d990cc7cbbfaacdde4b2ef)
* [Atlassian- Git Submodules](https://www.atlassian.com/git/tutorials/git-submodule)
* [Mastering Git submodules](https://medium.com/@porteneuve/mastering-git-submodules-34c65e940407)
* [Git Submodules Revisited](https://dev.to/dwd/git-submodules-revisited-1p54) - [ycombinator thread](https://news.ycombinator.com/item?id=17055919)
* [Update Git submodule to latest commit on origin](https://stackoverflow.com/questions/5828324/update-git-submodule-to-latest-commit-on-origin/5828396#5828396)
* [Working with Submodules](https://github.blog/2016-02-01-working-with-submodules/)
* [Using submodules in Git - Tutorial](https://www.vogella.com/tutorials/GitSubmodules/article.html)
* [How To: Merge a Git submodule into its main repository](https://medium.com/walkme-engineering/how-to-merge-a-git-submodule-into-its-main-repository-d83a215a319c)
* [Pulling submodule’s history into the main repository — Debiania](https://blog.debiania.in.ua/posts/2017-07-06-pulling-submodule-s-history-into-the-main-repository.html)
  > If you ever decide to somehow fold a Git submodule into the main repository, you’ll definitely end up reading [this Stack Overflow answer](https://stackoverflow.com/questions/1759587/un-submodule-a-git-submodule/) on or [that blog post by Lucas Jenß](http://x3ro.de/2013/09/01/Integrating-a-submodule-into-the-parent-repository.html). But for whatever reason, both of these limit themselves to actions that don’t modify history. Yet if this restriction is lifted, a few more possibilities will emerge.

## Resources

[Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
  > Gitflow Workflow is a Git workflow design that was first published and made popular by Vincent Driessen at nvie. The Gitflow Workflow defines a strict branching model designed around the project release. This provides a robust framework for managing larger projects.  

[git-annex](https://git-annex.branchable.com/)
  > git-annex allows managing files with git, without checking the file contents into git. While that may seem paradoxical, it is useful when dealing with files larger than git can currently easily handle, whether due to limitations in memory, time, or disk space.

* [The entire Pro Git book](https://git-scm.com/book/en/v2) -written by Scott Chacon and Ben Straub
* [Learn Enough Git to Be Dangerous](https://www.learnenough.com/git-tutorial/getting_started)
* [Atlassian -Getting Git Right](https://www.atlassian.com/git)
* [guides.github.com - Git Handbook](https://guides.github.com/introduction/git-handbook/)


</div>