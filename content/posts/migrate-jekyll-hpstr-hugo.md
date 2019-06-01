---
type: post
title: "Migrating from Jekyll HPSTR to Hugo."
description: "Everything you need to know, from Jekyll-HPSTR to HPSTR-Hugo."
tags: [hpstr, jekyll, hugo, theme, migration]
image:
  feature: /images/jekyll-hpstr-hugo.png
date: 2019-06-01
excerpt: >
  I've tried to learn Hugo a few different ways, and finally found one that works for me, and I hope will work well for anyone.

  This guide and the accompanying repository should help anyone switching from either Jekyll to Hugo, *or* Hugo to Jekyll.

---

I've tried to learn Hugo a few different ways, and finally found one that works for me, and I hope will work well for anyone.

This guide and the accompanying repository should help anyone switching from either Jekyll to Hugo, *or* Hugo to Jekyll.

I've got two branches of the same exact website except one is run by [Jekyll](https://github.com/infominer33/web-work/tree/hpstr-jekyll) and one is run by [Hugo](https://github.com/infominer33/web-work/tree/test-hugo)!!

That's pretty neat, if you ask me!

I also show examples of the differences between the two, where and how I made changes.

## HPSTR Jekyll vs Hugo 

### Releases

* [mmistakes/hpstr-jekyll-theme](https://github.com/mmistakes/hpstr-jekyll-theme)
* [dldx/hpstr-hugo-theme](https://github.com/dldx/hpstr-hugo-theme/releases)


It turns out that each version was released at the same time, and that they were built together from the very beginning!

The nice thing about `hpstr-hugo-theme` is that its not archived, and if you want to open any [issues](https://github.com/dldx/hpstr-hugo-theme/issues) or [pull-requests](https://github.com/dldx/hpstr-hugo-theme/pulls), that can be done. 

Interestingly, but nice to see, there are currently 0 open pull request or issues in the themes repository.

[![](https://imgur.com/jNTAlGt.png)](https://github.com/mmistakes/hpstr-jekyll-theme/releases)
[![](https://imgur.com/dvapj4y.png)](https://github.com/dldx/hpstr-hugo-theme/releases)

### Commits

![](https://imgur.com/obcGfNc.png)
![](https://imgur.com/KZQODtU.png)

## Which Version of Hugo Should I Run?

Scrolling back through the hugo releases when the HPSTR theme was in active development, I come across:

### [0.16.0 June 6th 2016](https://github.com/gohugoio/hugo/releases?after=v0.16.0)
>Hugo 0.16 is our best and biggest release ever. The Hugo community has outdone itself with continued performance improvements, beautiful themes for all types of sites from project sites to documentation to blogs to portfolios, and increased stability.

### .deb packages for Debian, Ubuntu, etc.
>Hugo has become part of the official Debian and Ubuntu repositories since January 2016!

That's a nice note to find, since I'm an Ubuntu user. 

## [v0.17](https://github.com/gohugoio/hugo/releases/tag/v0.17)

There are numerous options for different platforms, and this version of Hugo was **released in October**, one month after the final release of HPSTR.

>Hugo is going global with our 0.17 release. [...] Adding additional languages to your website is simple and straightforward.
>
>Hugo continues its trend of each release being faster than the last. 

Apparently it's fast enough that people began using hugo's webserver in production, around this time.

>New in 0.17: Available as Snap package
>
>Thanks to the contribution #2443 and guidance from @dholbach, Hugo is now available as a Snap package! (Snaps are a new kind of universal Linux packages.) Check it out at https://uappexplorer.com/app/hugo.hugo-authors
>

Now this is nice because you can get various releases of snap packages through the snap store.

* [askubuntu.com - Can I install multiple copies of a snap-package?](https://askubuntu.com/questions/1026075/can-i-install-multiple-copies-of-a-snap-package)

### Download links for Hugo v0.17

* [go_0.17-64bit.deb](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17-64bit.deb)
* [go_0.17_armhf.deb](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_armhf.deb)
* [go_0.17_FreeBSD-32bit.zip](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_FreeBSD-32bit.zip)
* [go_0.17_FreeBSD-64bit.zip](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_FreeBSD-64bit.zip)
* [go_0.17_freebsd_arm.zip](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_freebsd_arm.zip)
* [go_0.17_i386.deb](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_i386.deb)
* [go_0.17_Linux-32bit.tar.gz](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_Linux-32bit.tar.gz)
* [go_0.17_Linux-64bit.tar.gz](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_Linux-64bit.tar.gz)
* [go_0.17_linux_arm.tar.gz](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_linux_arm.tar.gz)
* [go_0.17_MacOS-32bit.zip](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_MacOS-32bit.zip)
* [go_0.17_MacOS-64bit.zip](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_MacOS-64bit.zip)
* [go_0.17_NetBSD-32bit.zip](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_NetBSD-32bit.zip)
* [go_0.17_NetBSD-64bit.zip](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_NetBSD-64bit.zip)
* [go_0.17_netbsd_arm.zip](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_netbsd_arm.zip)
* [go_0.17_OpenBSD-32bit.zip](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_OpenBSD-32bit.zip)
* [go_0.17_OpenBSD-64bit.zip](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_OpenBSD-64bit.zip)
* [go_0.17_Windows-32bit.zip](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_Windows-32bit.zip)
* [go_0.17_Windows-64bit.zip](https://github.com/gohugoio/hugo/releases/download/v0.17/hugo_0.17_Windows-64bit.zip)

## Test Install

Once it's installed, type I `hugo version` and read:

![](https://imgur.com/0kxcUkf.png)

perfect!!


## Clone the Hugo Theme.

With some pre-requisites out of the way, lets jump in at the first step in the theme setup:

* [Theme Setup - HPSTR Hugo](https://dldx.org/hpstr-hugo-theme/theme-setup/)


```
$ mkdir newProject
$ cd newProject
$ mkdir themes
$ cd themes
$ git clone https://github.com/dldx/hpstr-hugo-theme.git hpstr
```

and you will see `hpster` located in: `/web-work/themes/hpstr`.

## Example Site

Once you have the `newProject/themes/hpstr` you'll find the folder `exampleSite` in the `hpstr` directory. 


Just Copy the contents of `exampleSite` to the root of `newProject`, and test to see if it will run.

`$ hugo`

It should print something like this:

```
Started building sites ...
Built site for language en:
0 draft content
0 future content
0 expired content
10 pages created
0 non-page files copied
15 paginator pages created
9 tags created
0 categories created
total in 100 ms

```

Unless you get that print-out, don't bother changing your whole sites configuration just yet.

Make sure you placed the contents of `exampleSite` into the root of your project directory, and that your directories are structured properly.

If you did everything right and it still won't build, then I would shop around to different releases in that same time period to see if I could get one to work.

Just to be sure! I'll test the server, also, and see that I get a website.

`$ hugo server`

```
Started building sites ...
Built site for language en:
0 draft content
0 future content
0 expired content
10 pages created
0 non-page files copied
15 paginator pages created
9 tags created
0 categories created
total in 61 ms
Watching for changes in /newProject/ {data,content,static,themes}
```

Yay!!!


## Directory Structure HPSTR Jekyll vs Hugo

### [mmistakes.github.io/hpstr-jekyll-theme/theme-setup/](https://mmistakes.github.io/hpstr-jekyll-theme/theme-setup/)
![](https://imgur.com/EBIdUUo.png)

### [hpstr-hugo-theme/theme-setup](https://dldx.org/hpstr-hugo-theme/theme-setup/#setup:b8b08bb87737c3c5c8e714d4f8821e60)
![](https://imgur.com/nnI1lou.png)


## In with the new.

Now, it's simply moving over the content, and swapping out some frontmatter, and configuration formating.

## Content

>[Posts are stored in the content directory](https://dldx.org/hpstr-hugo-theme/theme-setup/#adding-new-content:b8b08bb87737c3c5c8e714d4f8821e60). By default, only content in the `content/posts` will show up in the `All Posts` section, however, you can link to other sections manually. For example, if you create a post at `gallery/photo1.md`, your post will appear both under the home page and under /gallery.


*In Hugo-HPSTR-Theme, it's all about your directory structure.*

![](https://imgur.com/0hsOjV7.png)

You'll notice that your root directory mirrors the themes directory structure, because the theme always keeps a backup file of everything necessary to function.

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

Be sure to change `title:` to `title =` and so forth.

```
[[links]]
title = "Webwork.tools"
url = "/webwork.tools/"

[[links]]
title = "Services"
url = "/services/"

[[links]]
title = "Mostly Free SEO Tools"
url = "/seo-tools/"

[[links]]
title = "GitHub Pages Starter Pack"
url = "/github-pages-starter-pack/"

[[links]]
title = "Practical Public Key Crypto"
url = "/practical-public-key-crypto/"

[[links]]
title = "IndieWeb"
url = "http://infominer.id/indieweb/"

[[links]]
title = "InfoMine"
url = "http://infominer.id/"
```


## Frontmatter

**The main differences**: 
* using `type` rather than `layout`
* using the frontmatter variable `date` to signify publication date, rather than hardcoding it into the title.

### HPSTR-Jekyll

```
---
layout: post
title: "Sample Code Post"
description: "Examples and code for various HPSTR functions."
tags: [samples, code, snippets]
comments: true
link: http://mademistakes.com  
image:
  thumb: /images/pgp-og.png
  feature: pgp-banner.png
  background: triangular.png
modified: 2019-05-30T13:15:59-23:00
permalink: /sample-code/
---
```

### HPSTR-Hugo

```
---
type: post
title: Sample Post
description: "Just about everything you'll need to style in the theme: headings, paragraphs, blockquotes, tables, code blocks, and more."
date: 2011-03-10

tags: [sample post]
image:
  feature: /images//images/abstract-3.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
---
```


## config.toml

Now we are getting places! Next step is to copy the `config.toml` from the root of our example site into the root of our repository. 


This is the final stretch, and we should be good to go 

![](https://imgur.com/za5VOLr.png)

* [Configuring Hugo](http://web.archive.org/web/20161110120102/http://gohugo.io/overview/configuration)


>`contentdir = "content"`\
>`layoutdir = "layouts"`\
>`publishdir = "public"`\
>`builddrafts = false`\
>`baseurl = "http://yoursite.example.com/"`\
>`canonifyurls = true`
>
>`[taxonomies]`\
>`  category = "categories"`\
>`  tag = "tags"`
>
>`[params]`\
>`  description = "Tesla's Awesome Hugo Site"`\
>`  author = "Nikola Tesla"`


## Resources

* [web.archive.org - Installing Hugo v0.17](http://web.archive.org/web/20161110121524/http://gohugo.io/overview/installing)
* [Blogging with Org-Mode and Hugo](http://masayk.github.io/tech/hugo/)
