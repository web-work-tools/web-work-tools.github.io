---
layout: post
title: "GitHub Pages-Starter Pack"
description: "Publishing a Website via GitHub pages is free, and easy. Everything you need to get going in one place + extended resources."
tags: [jekyll, github-pages, resources, web-publishing]
modified: 2019-06-16T15:59:13-23:00
permalink: /github-pages-starter-pack/

redirect_from: 
  - /gh-pages-starter-pack/
  - /github-pages-starter-pack

image:
  feature: github-pages-jekyll-starter-pack.png
  thumb: /images/github.png
---


Github makes it easy to get started, with the click of a button, you can have a web-page live, requiring only markdown skills (that anyone can learn on the go).

Each feature you want to enable requires a little more learning, and GitHub Pages is set up so that if you decide to, you can gradually progress from content creator to web-developer. 

If you don’t want to think about web-development, and simply want your markdown files to look beautiful once published, github pages can help you do that too.


![](https://i.imgur.com/mN5sBdg.png)

I first started playing around with GitHub to make an [awesome-list](https://github.com/infominer33/awesome-decentralized-id), in November. 

The number of technical subjects I've begun to learn, thanks to github, is incredible. Publishing via github-pages is really empowering.

![](https://imgur.com/oin0Ir8.png)

## Related Resources

* [Command Line - Git - SSH - BASH](https://web-work.tools/command-line-git-ssh/)
* [Content Creation](https://web-work.tools/content-creation/)
* [Learn HTML CSS and Associated Markup Languages](https://web-work.tools/learn-html-css/)
* [GitHub Pages Extended Resources](https://web-work.tools/github-pages-extended-resources/)
* [Static Site Generators](https://web-work.tools/static-site-generators/)
* [Migrating from Jekyll HPSTR to Hugo HPSTR theme](https://web-work.tools/migrate-jekyll-hpstr-hugo/)


## Introduction

I'm just a newb that created this resource to help myself. It does take a lot of work to create bigger projects like, however it's really simple to create a blog, or a homepage.

Corrections, suggestions, tips, and links would be all appreciated.


![](https://web-work.tools/images/gh-pages-starter-pack.png)


Github pages runs Jekyll, which uses [Kramdown](https://kramdown.gettalong.org/quickref.html) to transform yaml, markdown, and a number of related languages into proper html.

## Getting Started

The simplest way to use pages is to choose one of the <a href="https://pages.github.com/themes/" target="_blank">official GitHub pages themes</a>. Just go into your repository settings:

![](https://i.imgur.com/sw4Iann.png)

All you really need to do is select a branch and it will begin publishing your repository. Then choose a method to publish. Brand-newbs go with the theme chooser.

The first repository for your web-page must be named like so: `username.github.io`. For example, the repository for my personal page is called `infominer33.github.io`.  Simply create a new repository, and if your github username is `@awesomesauce` then you would create a new directory named `awesomesauce.github.io`.

Every other repository you own can also be made into its own web-page, that will published off of your user page, with the same name following your domain. So if you have a repository called, `/Dynomite` and you go into settings select pages to publish from the master branch, then that page will be found at `https://awesomesauce.github.io/Dynomite`.

so [github.com/didecentral/didecentral.github.io](https://github.com/didecentral/didecentral.github.io) is published at [decentralized-id.com](https://decentralized-id.com), because I have a custom domain. But it can still be found at, [infominer33.github.io/DIDecentralized](https://decentralized-id.com).

### Domains

Namecheap supports BTC purchases, so I'm including their github how-to here. If you know of other crypto-friendly domain providers, lmk in the issues.

* [https://help.github.com/en/articles/using-a-custom-domain-with-github-pages](https://help.github.com/en/articles/using-a-custom-domain-with-github-pages)
* [Using Custom Domain for Github Pages](https://medium.com/@hossainkhan/using-custom-domain-for-github-pages-86b303d3918a)
* [namecheap.com - how-do-i-link-my-domain-to-github-pages](https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages)


## Besides the Theme Chooser

It's time for an update, since I previously didn't really understand all of the options very well.

There are a few ways to use GitHub Pages. How many? 

I'll list the ones that I can think of:

* [Gem Themes](#gem-based-themes)
  * [GitHub Supported](#github-supported)
  * [Everything Else](#everything-else)
* [Remote Themes](#remote-themes)
* Files and Folders (Classic)

## Gem Based Themes

Gem files are packages that contain all of the files necessary for building your site, and keep your repository directory un-cluttered. Then, if you want to change a file that's in the gem, you just create the directory and pur the file where it goes, and configure as you wish. 

* [planetjekyll/awesome-jekyll-themes](https://github.com/planetjekyll/awesome-jekyll-themes)
  >Q: How can I get started with gem-packaged themes? / Do I need to package my theme into a gem?
  >
  >Gem-packaged themes are just an advanced option and in addition they are in development for (real world) experiments (e.g. think v0.1 as stated by the Ben Balter - the lead designer / manager / dev at GitHub).
  >
  >Thus, to conclude do NOT read too much into the official themes docs e.g. as the only or "right" way to design a theme. Just (continue to) use "classic" themes - there are hundreds to learn from and once you have mastered "classic" themes you can "graduate" to the master class, that is, using gem-packaged themes.  


### GitHub [Supported](https://pages.github.com/themes/)

GitHub Pages Supports the following gem themes:

* Architect
* Cayman
* Dinky
* Hacker
* Leap day
* Merlot
* Midnight
* Minima
* Minimal
* Modernist
* Slate
* Tactile
* Time machine

### Everything Else

You can use any gem based theme that you want. However, *GitHub* won't build those for you.

You must build them locally, and tell jekyll to build to the `docs` directory, which you may have noticed as an option in your repository settings, and github will publish that directory. However, for user or organization pages, you can only publish from the master directory.

So this will only work for projects other than your homepage, or your organizations homepage.

Simply add the following line to your `_config.yml`

```yml
destination: docs
```

Then add the gem and the source, also add any plugins you are using, such as in this example:

```
source 'https://rubygems.org'
gem "minimal-mistakes-jekyll"

gem "jekyll-paginate"
gem "jekyll-sitemap"
gem "jekyll-gist"
gem "jekyll-feed"
gem "jemoji"
gem "jekyll-include-cache"
```

then from the root of your project directory, on your local command-line:

`bundle install`
`bundle exec jekyll serve`

And you can view your updates to the project locally, before sending them over to github.

Even if you don't use this install method, you should use the same steps to build locally, regardless.

* [bundler.io](https://bundler.io/)
* [Adding a Gem to your Gemfile - help.github.com](https://help.github.com/en/articles/adding-a-jekyll-theme-to-your-github-pages-site#adding-your-theme-as-a-gem-to-your-gemfile)

## Remote Themes

This makes it simpler to keep your source files up to date. However, it is slower than using gems to build locally
  
   * [github.blog/2017-11-29-use-any-theme-with-github-pages/](https://github.blog/2017-11-29-use-any-theme-with-github-pages/)
   * [Jekyll Remote Theme](https://github.com/benbalter/jekyll-remote-theme)
    
   ```
   plugins:
     - jekyll-remote-theme

   remote_theme: benbalter/retlab
   ```

Essentially, if you're just editing files on github, you should just add those lines to your _config.yml along w an index file and Jekyll should build your site.


## Classic Themes

These classic themes are just files and folders, everything where you can see it (and should be forkable to create working websites).


* [drjekyllthemes.github.io](https://drjekyllthemes.github.io) (classic 'files and folders')
* [ChristopherA/simplest-github-page](https://github.com/ChristopherA/simplest-github-page)
* [prose/starter](https://github.com/prose/starter)
* [https://github.com/kinlane/beforeeighteen](https://github.com/kinlane/beforeeighteen) (template for presentation style pages.)


## Github Pages

* [Github Pages Community Forum](https://github.community/t5/GitHub-Pages/bd-p/pages)
* <a href="https://pages.github.com/versions/" target="_blank">https://pages.github.com/versions/</a> - These plugins can be used via gh-pages.
* [Configuring a Publishing Source for GitHub Pages](https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages)
* [help.github.com - User, Organization, and Project Pages](https://help.github.com/en/articles/user-organization-and-project-pages)
* <a href="http://ragupappu.com/2015/04/22/setup-website-using-github-pages-and-jekyll/" target="_blank">http://ragupappu.com/2015/04/22/setup-website-using-github-pages-and-jekyll/</a>
* <a href="https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll" target="_blank">Setting up You GitHub Pages Site Locally with Jekyll</a>
  * <a href="https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-3-Local-development-with/ba-p/2292" target="_blank">-- Local development with GitHub Pages</a>
* <a href="https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-4-Customizing-your-Pages/ba-p/4058" target="_blank">Getting started with GitHub Pages: Part 4 -- Customizing your Pages site</a>
* [Clearing Up Confusion around Baseurl](https://byparker.com/blog/2014/clearing-up-confusion-around-baseurl/)


## Jekyll

![](https://web-work.tools/images/gh-jekyll.png)

* <a href="https://github.com/jekyll/jekyll/blob/master/README.markdown" target="_blank">Jekyll README</a>
* <a href="https://github.com/planetjekyll" target="_blank">planetjekyll</a>
  * <a href="https://github.com/planetjekyll/awesome-jekyll" target="_blank">planetjekyll/awesome-jekyll</a>
* <a href="https://devhints.io/jekyll" target="_blank">Jekyll - Cheat Sheet</a>
* [Jekyll Community Forum](http://talk.jekyllrb.com/)
* <a href="https://jekyllrb.com/docs/pagination/" target="_blank">Jekyll - Pagination Docs</a>
* <a href="https://jekyllrb.com/tutorials/navigation/" target="_blank">Jekyll - Navigation Tutorial</a>
* [https://wiredcraft.com/blog/make-jekyll-fast](https://wiredcraft.com/blog/make-jekyll-fast)
* [Jekyll - Static Site Generator | Tutorial](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB)
  > This course covers the basics of using Jekyll - Static Site Generator. Work your way through the videos and we'll teach you everything you need to know to create a professional and scalable website or blog!
  [![](https://i.imgur.com/IoU70pW.png)](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB)
* [Run a Specific Version of Bundler](https://makandracards.com/makandra/9741-run-specific-version-of-bundler)
  * Can get older themes to work if you use the right verion of bundler (found in gemfile.lock).
* [benbalter/jekyll-style-guide](https://github.com/benbalter/jekyll-style-guide)

## Jekyll Themes

I'll say now, if you are new to web-development, best to start off trying out a few of the [official GitHub Pages Themes](https://pages.github.com/themes/). 

Once installed, I cloned those repos locally so its easier to see how everything works. Then, if I want to configure a file that's not in my repository, I have a copy nearby. You can grab the `_layouts/default.html`, put it in your repo, and get a feel for how configuring that template shapes your entire site. But then you configure individual pages, and categories, perhaphs, to display differently. 

### Finding Themes
* <a href="https://github.com/planetjekyll/awesome-jekyll-themes" target="_blank">planetjekyll/awesome-jekyll-themes</a> (gem-based)
* [http://themes.jekyllrc.org/](http://themes.jekyllrc.org/)
* [jekyll-theme-showcase-share-your-jekyll-themes/1382](https://webcache.googleusercontent.com/search?q=cache:http://talk.jekyllrb.com/t/jekyll-theme-showcase-share-your-jekyll-themes/1382)
* [**forked.yannick.io**](http://forked.yannick.io) - **Find maintained forks of your favorite GitHub repos.**

The problem is that all of these websites are not exactly up to date. Many of the themes listed above were written for older versions of Jekyll. 

Choosing a theme is very personal to your needs, also.

### Found Themes

I'm keeping track of themes that catch my eye:

* [projectpages.github.io/project-pages/](https://projectpages.github.io/project-pages/)
  * [project-pages/wiki](https://github.com/projectpages/project-pages/wiki)
* [bradleytaunt/lightspeed](https://github.com/bradleytaunt/lightspeed)
* [Just the Docs](https://pmarsceill.github.io/just-the-docs/)
* [era.yayd.in/jekyll-bulma/](https://era.yayd.in/jekyll-bulma/)
* [https://ndrewtl.github.io/airspace-jekyll/](https://ndrewtl.github.io/airspace-jekyll/)
  * [ndrewtl/airspace-jekyll/](https://github.com/ndrewtl/airspace-jekyll/)
* [deanattali.com/beautiful-jekyll/](https://deanattali.com/beautiful-jekyll/)
* [github/personal-website](https://github.com/github/personal-website)
  > Code that'll help you kickstart a personal website that showcases your work as a software developer.
* [Documentation Theme Jekyll](https://idratherbewriting.com/documentation-theme-jekyll)
  ![](https://imgur.com/7UjPtdAl.png)



### Hydejack

![](https://i.imgur.com/3ZY5FI7.png)

* <a href="https://infominer.id/qwtel/hydejack/" target="_blank">/qwtel/hydejack/</a>
* [/qwtel/hydejack-starter-kit](https://github.com/qwtel/hydejack-starter-kit)
* <a href="https://hydejack.com/docs/print/" target="_blank">Hydejack Print Documentation</a>
* <a href="http://nickengmann.com/Documentation.pdf" target="_blank">Hydejack Documentation.pdf</a>
* <a href="https://github.com/qwtel/hydejack/blob/master/docs/advanced.md" target="_blank">Hydejack Advanced</a>


If you don't want to think too much about web-development, try [Hydejack](https://hydejack.com). It's build with everything you need to create a beatiful responsive web-page, with plenty of options and configurations supported. It's a free version of a more robust commercial option. But it's easy to set up, and works great.

The only problem is that it is not open source. So it's not 100% customizable. Then again, that keeps you from getting in and screwing things up. -->

### Minimal Mistakes
Minimal Mistakes is the most popular theme for Github Pages, and with good cause. It creates gorgeous web-sites right out the box, and with some fine tuning is beautiful indeed. You can find pretty much everything you need to run Minimal Mistakes in the Quickstart Guide, Sample Posts and Collections, along with their corresponding files on Github.

* [minimal-mistakes/docs/quick-start-guide](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)
* [Sample Posts](https://mmistakes.github.io/minimal-mistakes/year-archive/)
* [Sample Collections](https://mmistakes.github.io/minimal-mistakes/collection-archive/)
* [mmistakes/minimal-mistakes](https://github.com/mmistakes/minimal-mistakes)
  ![](https://i.imgur.com/Ua8hFx8.png)
    * [Minimal Mistakes remote theme starter](https://github.com/mmistakes/mm-github-pages-starter)
    * [mmistakes/minimal-mistakes-algolia-search](https://github.com/mmistakes/minimal-mistakes-algolia-search) - reference if you have problems enabling search.
* [mmistakes/jekyll-theme-unit-test](https://github.com/mmistakes/jekyll-theme-unit-test)
* [Minimal Mistakes Navigation Examples](https://github.com/mmistakes/minimal-mistakes/blob/master/docs/_data/navigation.yml)
* [Minimal Mistakes - Post Archive with Feature Rows](https://mmistakes.github.io/minimal-mistakes/post-archive-feature-rows/) [[source]](https://github.com/mmistakes/minimal-mistakes/blob/master/docs/_pages/post-archive-feature-rows.html)
* [minimal-mistakes/markup-syntax-highlighting/](https://mmistakes.github.io/minimal-mistakes/markup-syntax-highlighting/)

### Other themes by [@mmistakes](https://github.com/mmistakes):

I've just listed what repositories most fit my use cases, you might want to browse through his [github portfolio](https://github.com/mmistakes), yourself.

#### Made Mistakes
* [mademistakes.com](https://mademistakes.com/) -Michael Rose's Homepage
  * [mmistakes/made-mistakes-jekyll](https://github.com/mmistakes/made-mistakes-jekyll)
   ![](https://imgur.com/0yW4S0h.png)


#### So Simple

* [So Simple Theme](https://mmistakes.github.io/so-simple-theme/)
  * [mmistakes/so-simple-theme](https://github.com/mmistakes/so-simple-theme)
    ![](https://imgur.com/uS54JQp.png)

#### Basically Basic

* [Basically Basic](https://mmistakes.github.io/jekyll-theme-basically-basic/)
  * [mmistakes/jekyll-theme-basically-basic](https://github.com/mmistakes/jekyll-theme-basically-basic)
  * [mmistakes/jekyll-theme-basically-basic-algolia-search](https://github.com/mmistakes/jekyll-theme-basically-basic-algolia-search)
    ![](https://imgur.com/OPflMe7.png)

#### Skinny Bones
* [Skinny Bones](https://mmistakes.github.io/skinny-bones-jekyll/)
  * [mmistakes/skinny-bones-jekyll](https://github.com/mmistakes/skinny-bones-jekyll)
    ![](https://imgur.com/HKZKkfKl.png)


#### Hpstr

This site currently runs on Hpstr, but it is archived, and doesn't support modern features of jekyll such as baseurl, nor can I get jekyll-redirect-from to work with it.

I will try migrating this to the Hugo port of this theme, which i believe is maintained. It's been nice trying out though, and I've got a few I'd like to look at anyway.

* [Hpstr](https://mmistakes.github.io/hpstr-jekyll-theme/)
  * [mmistakes/hpstr-jekyll-theme](https://github.com/mmistakes/hpstr-jekyll-theme)
  ![](https://imgur.com/G9eWy3ol.png)



## Setup


**Create an index.md**

Although pages will build an index.html from your readme.md, pages will not behave as expected if you try to do any configuration or additional optimization with only readme.md.

in that index.md you need to include front matter:

```
---
layout: default
---
```

There is a plugin that builds index files from all the readme.md files of your repository.. but it has trouble creating an index.html from your repositories primary README.md.


### Front Matter

* <a href="https://jekyllrb.com/docs/front-matter/" target="_blank">Front Matter</a>
* <a href="http://simpleprimate.com/blog/front-matter" target="_blank">YAML front matter in Jekyll</a>
* <a href="https://idratherbewriting.com/documentation-theme-jekyll/mydoc_yaml_tutorial" target="_blank">YAML tutorial in the context of Jekyll</a>


### Layouts

Layouts are preconfigured page templates. When I started, it was too much to think about layouts, and I would use "single" and "page". Now that I am using blog posts.. (because they populate your RSS feed, and increases their portability) I'm also using the Home layout:

![](https://imgur.com/ikX9wF6l.png)

* [https://jekyllrb.com/docs/step-by-step/04-layouts/](https://jekyllrb.com/docs/step-by-step/04-layouts/)
* [documentation-theme-jekyll/tag_special_layouts.html](https://idratherbewriting.com/documentation-theme-jekyll/tag_special_layouts.html)

I'm wondering if I can move these documentation theme layouts, or even this post index from hpstr over to minimal-mistakes... probably so... except maybe there is custom css.. and I really haven't taken the time to figure that out, yet.

### Collections 
* [https://jekyllrb.com/docs/collections/](https://jekyllrb.com/docs/collections/)
* [http://stories.upthebuzzard.com/jekyll_notes/](http://stories.upthebuzzard.com/jekyll_notes/)
  * [using-jekyll-collections.html](http://stories.upthebuzzard.com/jekyll_notes/2017-02-15-using-jekyll-collections.html)
  * [prev-and-next-within-a-jekyll-collection.html](http://stories.upthebuzzard.com/jekyll_notes/2017-02-19-prev-and-next-within-a-jekyll-collection.html)
  * [sort-order-of-jekyll-collections.html](http://stories.upthebuzzard.com/jekyll_notes/2017-02-19-sort-order-of-jekyll-collections.html)
  * [accessing-jekyll-collection-details-from-a-post.html](http://stories.upthebuzzard.com/jekyll_notes/2017-02-19-accessing-jekyll-collection-details-from-a-post.html)

### Plugins
* <a href="https://jekyllrb.com/docs/plugins/installation/" target="_blank">jekyllrb.com/docs/plugins/installation/</a>
* <a href="https://github.com/planetjekyll/awesome-jekyll-plugins" target="_blank">planetjekyll/awesome-jekyll-plugins</a>
* [Jekyll-Target-Blank](https://keith-mifsud.me/projects/jekyll-target-blank)
* [https://github.com/jekyll/jekyll-mentions/](https://github.com/jekyll/jekyll-mentions/)
* [Github Flavored Emoji for Jekyll](https://github.com/jekyll/jemoji)
* <a href="https://help.github.com/en/articles/adding-jekyll-plugins-to-a-github-pages-site" target="_blank">Adding Jekyll Plugins to a GitHub Pages Site - help.github.com</a>
* <a href="https://help.github.com/en/articles/creating-a-custom-404-page-for-your-github-pages-site" target="_blank">Creating Custom 404 page</a>
* [Implemented the "Edit this page" feature. jekyll#3495](https://github.com/delftswa2014/jekyll/commit/e109555aa0533148c53200e63d1e60a3acf67e74)
* <a href="https://help.github.com/en/articles/redirects-on-github-pages" target="_blank">Jekyll Redirect Plugin</a>

Use `redirect_from: internal/url` to change the location you are publishing, but keep old links.
Use `redirect_to: https://external.url` to send visitors somewhere else (perhaps you want it to live on another site, but not lose your valuable links :)
{: .notice }



## Related Resources

* [Learn HTML CSS and Associated Markup Languages](https://web-work.tools/learn-html-css/)
* [Content Creation](https://web-work.tools/content-creation/)
* [GitHub Pages Extended Resources](https://web-work.tools/github-pages-extended-resources/)
* [Static Site Generators](https://web-work.tools/static-site-generators/)
* [Migrating from Jekyll HPSTR to Hugo HPSTR theme](https://web-work.tools/migrate-jekyll-hpstr-hugo/)
* [Command Line - Git - SSH - BASH](https://web-work.tools/command-line-git-ssh/)
