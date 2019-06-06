---
type: post
title: "Static Site Generators"
description: "Resources on Static Site Generators(SSG) - Beyond Jekyll."
date: 2019-05-25
tags: [static site generators, tools, resources, CI\CD]
aliases:
  - /posts/static-site-generators/
  - /static-site-generators/
slug: /static-site-generators/
image:
  feature: /images/devopedia-static-site-generators.jpg
  credit: Devopedia.org
  creditlink: https://devopedia.org/static-site-generators
---

* [Devopedia.org](https://devopedia.org/static-site-generators)
  ![](https://infominer.id/web-work/images/devopedia-static-site-generators.jpg)


Well, now i'm looking into options besides jekyll, to expand my skills, and try out some themes that aren't available for Jekyll.

I'll be honest, if you are new like me, getting jekyll themes to work is tricky. Many of them are not supported anymore.


## What is a Static Site Generator (SSG)?

There are some configuration files, layouts and templates, and then there is all your content that your create. So.. the trick is to find something that runs nicely on your system and that you can figure out how to operate.

I'll have a few general resources at the top and just add as I go, since I'm not ready to learn about too many of them, just yet.

## General

* [Using A Static Site Generator other than Jekyll](https://help.github.com/en/articles/using-a-static-site-generator-other-than-jekyll)
* [pinceladasdaweb/Static-Site-Generators](https://github.com/pinceladasdaweb/Static-Site-Generators)
* [staticsitegenerators.net](https://staticsitegenerators.net)
* [https://www.staticgen.com/](https://www.staticgen.com/)
  * [I tried Hugo, Jekyll and Gatsby](https://news.ycombinator.com/item?id=17952234)


## Hugo

These links have moved to their own page: 

* [Hugo Starter Kit](/hugo-starter-kit/)

## MkDocs

MkDocs has built in search, and in some ways simpler than publishing w jekyll.

For example, you don't need to put frontmatter into every single document.. it will just create a website from markdown files and autogenerate toc based on directory structure.

MkDocs really caught my eye when I saw it running at [EthHub](https://docs.ethhub.io/)

![](https://i.imgur.com/c7Ik39r.png)

* [https://www.mkdocs.org/](https://www.mkdocs.org/)
* [/mkdocs/mkdocs/wiki/MkDocs-Plugins](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Plugins)
* [MkDocs Material Components - Cheat Sheet](https://yakworks.github.io/mkdocs-material-components/cheat-sheet/)
* [mkdocs.readthedocs.io](https://mkdocs.readthedocs.io)
* [mkdocs/mkdocs/wiki/MkDocs-Plugins](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Plugins)
* [mkdocs-awesome-pages-plugin](https://github.com/lukasgeiter/mkdocs-awesome-pages-plugin)
* [mkdocs.plugins/](https://www.wheelodex.org/entry-points/mkdocs.plugins/)
* [metadata-for-markdown-mkdocs/](https://blogs.pjjk.net/phil/metadata-for-markdown-mkdocs/)
* [https://gristlabs.github.io/mkdocs-windmill/](https://gristlabs.github.io/mkdocs-windmill/#)
  * [gristlabs/mkdocs-windmill](https://github.com/gristlabs/mkdocs-windmill)
* [https://python-markdown.github.io/extensions/](https://python-markdown.github.io/extensions/)
  * [Python-Markdown/markdown/wiki/Third-Party-Extensions](https://github.com/Python-Markdown/markdown/wiki/Third-Party-Extensions)
* [https://python-markdown.github.io/extensions/smarty/](https://python-markdown.github.io/extensions/smarty/)

Because MkDocs builds with python, that opens up a whole universe of tools at your disposal. The python markdown extensions are a prime example.

However, basically none of the regular jekyll plugins work with mkdocs, it's a whole universe to its own w Python.


### Now Dev

I don't even know... but it seems pretty dope.

* [https://zeit.co/blog/now-dev](https://zeit.co/blog/now-dev)
* [https://zeit.co/docs/v2/deployments/concepts/lambdas](https://zeit.co/docs/v2/deployments/concepts/lambdas)


### Keybase

![](https://imgur.com/PVUAaAu.png)

Just sayin'... keybase has 250 gigs of free storage you can use to host a website...

you could build gem based sites locally, and keybase will automatically sync the data.




## Thats all for now!

<figure class="full">
	<img src="https://infominer.id/web-work/images/gh-pages-starter-pack.png" alt="">
	<figcaption><a href="https://infominer.id/web-work/github-pages-starter-pack/"><b>GitHub Pages - Starter Pack:Extended Resources</b></a></figcaption>
</figure>

