---
type: post
title: "Migrating from Jekyll HPSTR to Hugo."
description: "Everything you need to know, from Jekyll-HPSTR to HPSTR-Hugo."

tags: [hpstr, jekyll, hugo, theme, migration]
image:
  feature: /images/jkyll-hpstr-hugo.png
modified: 2019-06-01
published: false
---

I'm want to learn Hugo, and I want to use the Hugo version HPSTR theme, and it seems like this is the perfect opportunity to figure it out... 

While I'm at it, might as well record the process. Hopefully it will help a few people along the way.


## HPSTR Jekyll vs Hugo 

### Releases

* [mmistakes/hpstr-jekyll-theme](https://github.com/mmistakes/hpstr-jekyll-theme)
* [dldx/hpstr-hugo-theme](https://github.com/dldx/hpstr-hugo-theme/releases)

For some reason, originally, I thought that `dldx/hpstr-hugo-theme` was a more recently maintained version of `mmistakes/hpstr-jekyll-theme`.

It turns out that each version was released at the same time, and that they were built together from the very beginning!

[![](https://imgur.com/NT30edy.png)](https://github.com/mmistakes/hpstr-jekyll-theme/releases)
[![](https://imgur.com/dvapj4y.png)](https://github.com/dldx/hpstr-hugo-theme/releases)

### Commits

![](https://imgur.com/obcGfNc.png)
![](https://imgur.com/KZQODtU.png)

## Which Version of Hugo Should I Run?

Scrolling back through the time period when the HPSTR theme was in active development, I come across:

### 0.16.0 June 6th 2016
>Hugo 0.16 is our best and biggest release ever. The Hugo community has outdone itself with continued performance improvements, beautiful themes for all types of sites from project sites to documentation to blogs to portfolios, and increased stability.

### .deb packages for Debian, Ubuntu, etc.
>Hugo has become part of the official Debian and Ubuntu repositories since January 2016!

That is a nice note to find among the releases of Hugo, since I'm an Ubuntu user. 

## [v0.17](https://github.com/gohugoio/hugo/releases/tag/v0.17)

![](https://imgur.com/1tUE104l.png)


There are options for different platforms, and it was released in october one month after the last release of HPSTR.

I already have a newer version, and am choosing to uninstall it, so the earlier version, hopefully won't conflict.

With ruby\jekyll it is trivial to install and use whichever release you like, at any time. The same could be said for any Python based SSGs.

Though I will probably know a similar solution for hugo soon.

Once it's installed, type I `hugo version` and read:

`Hugo Static Site Generator v0.17 BuildDate: 2016-10-07T10:46:29-04:00`

perfect. if that wasn't successful, I'd check to be sure Hugo was in my path. But that is platform specific, and it's installed. :)

[**More specific installation instructions**](http://web.archive.org/web/20161110121524/http://gohugo.io/overview/installing)
  >Hugo is written in Go with support for multiple platforms.
  >
  >The latest release can be found at Hugo Releases. We currently provide pre-built binaries for  Windows,  Linux,  FreeBSD and  OS X (Darwin) for x64, i386 and ARM architectures.
  >
  >Hugo may also be compiled from source wherever the Go compiler tool chain can run, e.g. for other operating systems including DragonFly BSD, OpenBSD, Plan 9 and Solaris. See [http://golang.org/doc/install/source](http://web.archive.org/web/20161125191343/https://golang.org/doc/install/source) for the full set of supported combinations of target operating systems and compilation architectures.


### Google Search by Date

Now that I'm thinking in the right timespan, and fully realize that newer directions will get me nowhere with this theme. I will try and stick with the guides from that time. 

That's all assuming this is successful :D

## Directory Structure

Now that we've covered some of the backgraound, lets forget about that stuff for a moment, and think about files and folders.

That's what we came to SSG for, right? Ok!

### [mmistakes.github.io/hpstr-jekyll-theme/theme-setup/](https://mmistakes.github.io/hpstr-jekyll-theme/theme-setup/)
![](https://imgur.com/EBIdUUo.png)

### [hpstr-hugo-theme/theme-setup](https://dldx.org/hpstr-hugo-theme/theme-setup/#setup:b8b08bb87737c3c5c8e714d4f8821e60)
![](https://imgur.com/nnI1lou.png)

What we're going to do is make a test branch of our repository... so we can see about getting hugo to run over there, and if successful then we'll learn how to merge this test branch back over.

## Checkout test branch

Use the command `git checkout -b` will allow you to create a local branch for testing.

I will call my new branch `test-hugo` so the command will be like so:

`git checkout -b test-hugo`

### Some git basics for newbs like me

* [Git Branching and Merging](https://git-scm.com/book/id/v2/Git-Branching-Basic-Branching-and-Merging)

Git keeps track of all your files, but not just the files, but everything in the repository. 

Every commit, git remembers.

> "yes yes I know"

However, it really boggled my mind the first time I tried it locally. 

I can change to a branch or another point in the history of this repository, and git tucks away the one I'm working on... and the whole directory changes and like wait... 

>where did all my files just go? 

When you push a repository to GitHub they keep a copy too.. but git is really awesome beyond github. If it was invented today they would call it a blockchain :rofl:

**Git is Magic!** 

it sure felt that way the first time I experienced it, and today still I have a sense of mystery and wonder around Git, thought I know it's technical, and not mystical in nature.

but you don't need github at all, and I'm learning that a significant portion, perhaps a majority, <!--findsource--> of git repositories are never exposed to the public. 

`git checkout -b` is just the same as creating a new directory, copy pasting the repo files there to test, and testing it out there. Except git makes it look like magic, and keeps track of your progress!

* [More Git Resources](https://infominer.id/web-work/github-pages-starter-pack/#git) >>

## Out with the Old

Anything that I didn't personally customize is gone from the test branch. 

**I kept**:
  * posts
  * pages
  * images
  * data files
  * favicon
  * README.md
  * _config.yml 
  * .gitignore


**HPSTR-Hugo Directory Structure**
![](https://imgur.com/nnI1lou.png)
>This should be enough to get a working website!

What I'm thinking is that those folders in the root `assets` directory would be empty unless I'm adding some custom feature.

So I can see that my `_posts` directory will now be called `posts`, and live in the `content` directory. That's simple enough.

### Side-by-Side

![](https://imgur.com/pjmxjDT.png) ![](https://imgur.com/Y9YDq42.png)

The about that  and services folder are just where I'm keeping html and will be moved later. 

Now one part of my directory that looks like Hugo!!! woot! :)


## Clone the Hugo Theme.

With some pre-requisites out of the way, lets jump in at the first step in the theme setup:

* [Theme Setup - HPSTR Hugo](https://dldx.org/hpstr-hugo-theme/theme-setup/)

### BUT FIRST!

**Change to the root of your project's repository.**

Although this is clear by studying the site map, the first few times I tried Hugo, when I started with making a theme directory, I just got confused and gave up.

One time, as part of the instructions it had me begin as the first step to clone a repository of 100+ themes to my home directory, which Hugo can use from the commandline, so you dont' have to fork a theme over and over, every time you need it.

That's a great feature, but I still didn't understand what was going on.

Migrating from an existing theme to the same one on Hugo simplified a couple things for me, and I feel on the right track. I'm confident enough to begin writing as I learn.

```
$ mkdir themes
$ cd themes
$ git clone https://github.com/dldx/hpstr-hugo-theme.git hpstr
```

So now, I have themes as a subdirectory in the root directory of this site `/web-work/themes/` and I'll just plug away.

## Example Site

Once you have the `themes/hpstr` 
Next, you need to configure your site and add some content. We provide a complete example site under the folder exampleSite. All you need to do is copy the contents of that folder into the main hugo site folder so that it looks something like this

## Content

>[Posts are stored in the content directory](https://dldx.org/hpstr-hugo-theme/theme-setup/#adding-new-content:b8b08bb87737c3c5c8e714d4f8821e60). By default, only content in the `content/posts` will show up in the `All Posts` section, however, you can link to other sections manually. For example, if you create a post at `gallery/photo1.md`, your post will appear both under the home page and under /gallery.


*In Hugo-HPSTR-Theme, it's all about your directory structure.*

Luckily we don't have to guess, since there is an `exampleSite` in our `themes/hpstr` directory.

![](https://imgur.com/R8F2D5m.png)


![](https://imgur.com/NJthhWz.png)

So now you can see how my content directory is structured. 

Every directory root has an index and nothing else, currently. 

You'll notice that your root directory mirrors the themes directory structure. 

![](https://imgur.com/83WTq5g.png)



### archetypes/
I entered some tags and categories:

`web-work/themes/hpstr/archetypes/default.md`
```
+++
Description = ""
Tags = ["resources", "web-work"]
Categories = ["howto", "tools"]
menu = "main"
+++
```

## data/ 

**From YAML to TOML**

![](https://imgur.com/83WTq5g.png)


In the `theme` directory is a navigation.yml file, and even awhole `exampleSite` that we can copy over to our root data directory and customize.

![](https://imgur.com/cTxmK7Ql.png)

That's a good start.

## Frontmatter

![](https://imgur.com/LpxVveb.png)

I can see 1 thing is different the date does not include the time, also.

## config.toml

Now we are getting places! Next step is to copy the `config.toml` from the root of our example site into the root of our repository. 


This is the final stretch, and we should be good to go 

![](https://imgur.com/za5VOLr.png)

phew. ok, I feel good. let me rename the config.yml to config.tmp. Not sure if that makes a difference to hugo, but it does to me.


## Extra 
* [bwaycer.github.io/hugo_tutorial.hugo/overview/configuration/](https://bwaycer.github.io/hugo_tutorial.hugo/overview/configuration/)
* [gohugo.io/content-management/archetypes/](https://gohugo.io/content-management/archetypes/)

### Page Bundles

* [content-management/organization/](https://gohugo.io/content-management/organization/)
  >Hugo 0.32 announced page-relative images and other resources packaged into Page Bundles.

As Hugo is just now at 0.32, and this theme port is older, we're not going to pay attn to the latest instructions. Especailly since going to the repo I see no open [issues](https://github.com/dldx/hpstr-hugo-theme/issues) or [pull-requests](https://github.com/dldx/hpstr-hugo-theme/pulls).

