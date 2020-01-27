---
layout: page-fullwidth
title: "Static Site Generators"
teaser: "Resources on Static Site Generators(SSG) - Beyond Jekyll."
subheadline: "Configuration files, layouts and templates, and all the content you create."

categories: ['JAMStack']

header:
  image_fullwidth: "devopedia-static-site-generators.jpg"
  caption: "Devopedia.org"
  caption_url: "https://devopedia.org/static-site-generators"

image:
  thumb: "devopedia-static-site-generators.jpg"

permalink: /jamstack/static-site-generators/
redirect_from:
  - /static-site-generators/
modified: 2019-06-15T11:12:13-23:00
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


## What is a Static Site Generator (SSG)?

There are some configuration files, layouts and templates, and all of the content you create. So.. the trick is to find something that runs nicely on your system and that you can figure out how to operate.

This page is where I keep track of info on the various SSG that I'm experienced with, as I begin to understand the stack surrounding them.

## General

* [pinceladasdaweb/Static-Site-Generators](https://github.com/pinceladasdaweb/Static-Site-Generators)
* [staticsitegenerators.net](https://staticsitegenerators.net)
* [https://www.staticgen.com/](https://www.staticgen.com/)
  * [I tried Hugo, Jekyll and Gatsby](https://news.ycombinator.com/item?id=17952234)
* [JAMstack templates](https://templates.netlify.com)
  > Find the perfect place to begin a new JAMstack site. Deploy a template site to Netlify with just one click. The site’s code will automatically populate as a new folder in your Git repository so you can explore, edit, and update so it works for you. All for free.



## Jekyll and GitHub Pages

Jekyll is the SSG built into GitHub, covered on the following pages:

* [Github Pages Starter Pack](/jamstack/github-pages-starter-pack/)
* [Using A Static Site Generator other than Jekyll](https://help.github.com/en/articles/using-a-static-site-generator-other-than-jekyll)

## Hugo

* [Hugo Starter Kit](/jamstack/hugo-starter-kit/)

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



## Related Posts

* [Learn HTML CSS and Associated Markup Languages](https://web-work.tools/jamstack/html-css/)
* [Content Creation](https://web-work.tools/content-creation/)
* [GitHub Pages Extended Resources](https://web-work.tools/jamstack/github-pages-extended-resources/)
* [Static Site Generators](https://web-work.tools/jamstack/static-site-generators/)
* [Migrating from Jekyll HPSTR to Hugo HPSTR theme](https://web-work.tools/jamstack/jekyll-hpstr-hugo-theme/)
* [Command Line - Git - SSH - BASH](https://web-work.tools/jamstack/terminal-basics-git-ssh/)

</div>