---
layout: post
title: "Migrating from Jekyll HPSTR to Hugo."
description: "Everything you need to know, from Jekyll-HPSTR to HPSTR-Hugo."
tags: [hpstr, jekyll, hugo, theme, migration]
image:
  thumb: /images/jkyll-hpstr-hugo.png
  feature: jkyll-hpstr-hugo.png
modified: 2019-06-01T13:15:59-23:00
permalink: /mission-statement/
published: false
---

I'm want to learn Hugo, and I want to use the Hugo version HPSTR theme, and it seems like this is the perfect opportunity to figure it out... 

While I'm at it, might as well record the process. Hopefully it will help a few people along the way.

## Comparing Sitemaps HPSTR Jekyll vs Hugo
* [mmistakes.github.io/hpstr-jekyll-theme/theme-setup/](https://mmistakes.github.io/hpstr-jekyll-theme/theme-setup/)

### Jekyll
![](https://imgur.com/EBIdUUo.png)

### Hugo
![](https://imgur.com/nnI1lou.png)


What we're going to do is make a test branch of our repository... so we can see about getting hugo to run over there, and if successful then we'll learn how to merge this test branch back over.

## Checkout test branch

Use the command `git checkout -b` will allow you to create a local branch for testing.

I will call my new branch `test-hugo` so the command will be like so:

`git checkout -b test-hugo`

### Some git basics for newbs like me.

* [Git Branching and Merging](https://git-scm.com/book/id/v2/Git-Branching-Basic-Branching-and-Merging)

Git keeps track of all your files, but not just the files, but everything in the repository. 

Every commit, git remembers.

It's simple enough to say "yes yes I know"

However, it really boggled my mind the first time I did it locally, because I didn't realize how incredible git actually is.

I can change to a branch or another point in the history of this repository, and git tucks away the one I'm working on... and the whole directory changes and like wait... 

>where did all my files just go? 

Then when you push to GitHub they keep a copy too.. but git is really awesome beyond github. If it was invented today we would call it a blockchain :rofl:

but you don't need github at all, and I'm learning that a significant portion of git repositories are never exposed to the public. 

`git checkout -b` is just the same as creating a new directory, copy pasting the repo files there to test, and testing it out there. Except git makes it look like magic, and keeps track of your progress!

* [More Git Resources](https://infominer.id/web-work/github-pages-starter-pack/#git) >>

## Out with the Old

Anything that I didn't personally customize is gone from the repository. I just kept my posts, pages, some data files that I will figure out if I use it here later, and the config.yml that I will grab some lines from too. 


**HPSTR-Hugo Directory Structure**
![](https://imgur.com/nnI1lou.png)


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

One time, as part of the instructions it had me clone a direcotry of 100 themes, which Hugo can use from the commandline, so you dont' have to fork a theme over and over, every time you need it.

That's a great feature, but I was lost.

Migrating from an existing theme to the same one on Hugo simplified a couple things for me, and I feel on the right track. I'm confident enough to be writing this before having completed it once already.

```
$ mkdir themes
$ cd themes
$ git clone https://github.com/dldx/hpstr-hugo-theme.git hpstr
```

So now, I have themes as a subdirectory in the root directory of this site `/web-work/themes/` and I'll just plug away.



## Content

>[Posts are stored in the content directory](https://dldx.org/hpstr-hugo-theme/theme-setup/#adding-new-content:b8b08bb87737c3c5c8e714d4f8821e60). By default, only content in the `content/posts` will show up in the `All Posts` section, however, you can link to other sections manually. For example, if you create a post at `gallery/photo1.md`, your post will appear both under the home page and under /gallery.



In Hugo, much like [MkDocs](https://infominer.id/web-work/static-site-generators/#mkdocs), it's all about your directory structure.

```
.
└── content
    └── about
    |   └── _index.md  // <- https://example.com/about/
    ├── posts
    |   ├── firstpost.md   // <- https://example.com/posts/firstpost/
    |   ├── happy
    |   |   └── ness.md  // <- https://example.com/posts/happy/ness/
    |   └── secondpost.md  // <- https://example.com/posts/secondpost/
    └── quote
        ├── first.md       // <- https://example.com/quote/first/
        └── second.md      // <- https://example.com/quote/second/
```

* [content-management/organization/](https://gohugo.io/content-management/organization/)
  >Hugo 0.32 announced page-relative images and other resources packaged into Page Bundles.
  >
  >These terms are connected, and you also need to read about [Page Resources](https://gohugo.io/content-management/page-resources/) and [Image Processing](https://gohugo.io/content-management/image-processing/) to get the full picture.
  ![](/1-featured-content-bundles.png)
  >The illustration shows 3 bundles. Note that the home page bundle cannot contain other content pages, but other files (images etc.) are fine.

![](https://imgur.com/c2VcZkh.png)

So now you can see how my content directory is structured. I'm saving that sample post 