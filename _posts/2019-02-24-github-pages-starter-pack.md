---
layout: post
title: "GitHub Pages-Starter Pack"
description: "Publishing a Website via GitHub pages is free, and easy. Everything you need to get going in one place + extended resources."
tags: [jekyll, github-pages, resources, web-publishing]
modified: 2019-05-30T15:59:13-23:00
permalink: github-pages-starter-pack/
canonical_url: 'https://infominer.id/web-work/github-pages-starter-pack/'
redirect_from: gh-pages-starter-pack/
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

## Introduction

I'm just a newb that created this resource to help myself. It does take a lot of work to create bigger projects like, however it's really simple to create a blog, or a homepage.

Corrections, suggestions, tips, and links would be all appreciated.

**Note:** this page is just for Jekyll\GHPages. I'm making new pages for the other stuff like [static site generators besides jekyll](https://infominer.id/web-work/static-site-generators/), and [content creation](https://infominer.id/web-work/content-creation/).

![](https://infominer.id/web-work/images/gh-pages-starter-pack.png)


Github pages runs Jekyll, which runs [Kramdown](https://kramdown.gettalong.org/quickref.html), which can transform yaml, markdown, and a number of related languages into proper html.

Github pages can be used, like, 4 different ways. It’s versitile, but can be confusing.

The simplest way to use pages is to choose one of the <a href="https://pages.github.com/themes/" target="_blank">official GitHub pages themes</a>. Just go into your repository settings:

![](https://i.imgur.com/sw4Iann.png)

All you really need to do is select a branch and it will begin publishing your repository. Then choose a method to publish. Brand-newbs go with the theme chooser.

The first repository for your web-page must be named like so: `username.github.io`. For example, the repository for my personal page is called `infominer33.github.io`.  Simply create a new repository, and if your github username is `@awesomesauce` then you would create a new directory named `awesomesauce.github.io`.

Every other repository you own can also be made into its own web-page, that will published off of your user page, with the same name following your domain. So if you have a repository called, `/Dynomite` and you go into settings select pages to publish from the master branch, then that page will be found at `https://awesomesauce.github.io/Dynomite`.

so [github.com/infominer33/DIDecentralized](https://github.com/infominer33/DIDecentralized) is published at [infominer.id/DIDecentralized](https://infominer.id/DIDecentralized), because I have a custom domain. But it can still be found at, [infominer33.github.io/DIDecentralized](https://infominer.id/DIDecentralized).

### Domains

Namecheap supports BTC purchases, so I'm including their github how-to here. If you know of other crypto-friendly domain providers, lmk in the issues.

* [https://help.github.com/en/articles/using-a-custom-domain-with-github-pages](https://help.github.com/en/articles/using-a-custom-domain-with-github-pages)
* [Using Custom Domain for Github Pages](https://medium.com/@hossainkhan/using-custom-domain-for-github-pages-86b303d3918a)
* [namecheap.com - how-do-i-link-my-domain-to-github-pages](https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages)


## Getting Started

If you used the theme chooser, all you need to do is edit README.md, and your page is built instantly when you save a commit to the repository.

**Create an index.md**

Although pages will build an index.html from your readme.md, pages will not behave as expected if you try to do any configuration or additional optimization with only readme.md.

in that index.md you need to include front matter:

```
---
layout: default
---
```

There is a plugin that builds index files from all the readme.md files of your repository.. but it has trouble creating an index.html from your repositories primary README.md.



## Besides the Theme Chooser


1. Remote Themes.

   This is supposed to be the easy route, and makes it simpler to keep your source files up to date. 
  
   * [github.blog/2017-11-29-use-any-theme-with-github-pages/](https://github.blog/2017-11-29-use-any-theme-with-github-pages/)
   * [Jekyll Remote Theme](https://github.com/benbalter/jekyll-remote-theme)
    
   ```
   plugins:
     - jekyll-remote-theme

   remote_theme: benbalter/retlab
   ```

   Essentially, if you're just editing files on github, you should just add those lines to your _config.yml along w an index file and Jekyll should build your site.



2. You can also run any Gem based theme from your page. Gem files are packages that contain all of the files necessary for building your site, and keep your repository directory un-cluttered. Then, if you want to change a file that's in the gem, you just create the directory and pur the file where it goes, and configure as you wish. 

   * [planetjekyll/awesome-jekyll-themes](https://github.com/planetjekyll/awesome-jekyll-themes)
     >Q: How can I get started with gem-packaged themes? / Do I need to package my theme into a gem?
     >
     >Gem-packaged themes are just an advanced option and in addition they are in development for (real world) experiments (e.g. think v0.1 as stated by the Ben Balter - the lead designer / manager / dev at GitHub).
     >
     >Thus, to conclude do NOT read too much into the official themes docs e.g. as the only or "right" way to design a theme. Just (continue to) use "classic" themes - there are hundreds to learn from and once you have mastered "classic" themes you can "graduate" to the master class, that is, using gem-packaged themes.  
     >
     >I understand what they're saying, but I feel kind of the opposite. I used the theme chooser and remote\gem themes to begin learning. Then again, I didn't really understand my options when I started.

3. These [classic themes](#classic) are just files and folders, everything where you can see it (and should be forkable to create working websites)

## Moved

Running out of space on this page ;) 

**NOTE:** The following resources are specifically for github-pages\jekyll *compatible* themes. Anything requiring a local build will now live on another page:

### Static Site Generators Other Than Jekyll

<a href="https://infominer.id/web-work/static-site-generators/" class="btn btn-success">Static Site Generators</a>

### Content Creation

<a href="https://infominer.id/web-work/content-creation/" class="btn btn-primary">Content Creation</a>

## Fundamentals

<a href="https://lab.github.com/" class="btn btn-info">GitHub Learning Lab</a>

### Markdown

* [Kramdown - QuickRef Guide](https://kramdown.gettalong.org/quickref.html)
* <a href="https://guides.github.com/features/mastering-markdown/" target="_blank">Mastering Markdown</a>
* <a href="https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet" target="_blank">Markdown Cheet-Sheet</a>

### Github Pages

* [Github Pages Community Forum](https://github.community/t5/GitHub-Pages/bd-p/pages)
* <a href="https://pages.github.com/versions/" target="_blank">https://pages.github.com/versions/</a> - These plugins can be used via gh-pages.
* [Configuring a Publishing Source for GitHub Pages](https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages)
* [help.github.com - User, Organization, and Project Pages](https://help.github.com/en/articles/user-organization-and-project-pages)
* <a href="http://ragupappu.com/2015/04/22/setup-website-using-github-pages-and-jekyll/" target="_blank">http://ragupappu.com/2015/04/22/setup-website-using-github-pages-and-jekyll/</a>
* <a href="https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll" target="_blank">Setting up You GitHub Pages Site Locally with Jekyll</a>
  * <a href="https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-3-Local-development-with/ba-p/2292" target="_blank">-- Local development with GitHub Pages</a>
* <a href="https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-4-Customizing-your-Pages/ba-p/4058" target="_blank">Getting started with GitHub Pages: Part 4 -- Customizing your Pages site</a>
* [Clearing Up Confusion around Baseurl](https://byparker.com/blog/2014/clearing-up-confusion-around-baseurl/)


### Jekyll

![](https://infominer.id/web-work/images/gh-jekyll.png)

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

### Themes

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

### Classic

* [drjekyllthemes.github.io](https://drjekyllthemes.github.io) (classic 'files and folders')
* [indieweb/blank-gh-site](https://github.com/indieweb/blank-gh-site)
* [ChristopherA/simplest-github-page](https://github.com/ChristopherA/simplest-github-page)
* [prose/starter](https://github.com/prose/starter)
* [https://github.com/kinlane/beforeeighteen](https://github.com/kinlane/beforeeighteen) (template for presentation style pages.)


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

* [Hpstr](https://mmistakes.github.io/hpstr-jekyll-theme/)
  * [mmistakes/hpstr-jekyll-theme](https://github.com/mmistakes/hpstr-jekyll-theme)
  ![](https://imgur.com/G9eWy3ol.png)

## Setup

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
{: .notice--info}



## Other Customizations
* [digitaldrummerj.me/categories/jekyll](https://digitaldrummerj.me/categories/jekyll/)
* [Social Media Share Bar](https://mycyberuniverse.com/social-media-share-bar-jekyll-blog-website.html)
* [Validating Links and Images](https://digitaldrummerj.me/jekyll-validating-links-and-images/)
* [longqian.me/](http://longqian.me/) -Metamask Donation Button.
* <a href="https://superdevresources.com/share-buttons-jekyll/" target="_blank">https://superdevresources.com/share-buttons-jekyll/</a>
* [Embed files from a github repository onto your page.](http://gist-it.appspot.com/)
* [Redirecting GitHub Pages after a repository move](https://gist.github.com/domenic/1f286d415559b56d725bee51a62c24a7)
* [hacking-routing-component-jekyll/](https://www.sitepoint.com/hacking-routing-component-jekyll/)
* [How-to-build-a-lowtech-website](https://solar.lowtechmagazine.com/2018/09/how-to-build-a-lowtech-website/)

### Comments
* [Github Issues for Blog Comments](http://artsy.github.io/blog/2017/07/15/Comments-are-on/)
* [A repo you can use to work-around GH issue comment request limmits.](https://github.com/orta/gh-commentify)
* [Various ways you can add comments to your static site](https://darekkay.com/blog/static-site-comments/)
* [Add comments to your jekyll powered blog](https://github.com/damieng/jekyll-blog-comments)
* [Setting up Staticman Server](https://www.flyinggrizzly.net/2017/12/setting-up-staticman-server/)
  * [new feature! added comments to this *static* website](https://www.edwinwenink.xyz/posts/18-comments/)
* [https://mademistakes.com/articles/jekyll-static-comments/](https://mademistakes.com/articles/jekyll-static-comments/)
  * [https://mademistakes.com/articles/improving-jekyll-static-comments/](https://mademistakes.com/articles/improving-jekyll-static-comments/)

### Search

* [Elasticsearch for Jekyll](https://blog.omc.io/elasticsearch-for-jekyll-part-1-ab456ac7c093)
* [Adding Custom Google Search](https://digitaldrummerj.me/blogging-on-github-part-7-adding-a-custom-google-search/)
* [github.com/algolia/jekyll-algolia](https://github.com/algolia/jekyll-algolia)
* [community.algolia.com/jekyll-algolia/blog.html](https://community.algolia.com/jekyll-algolia/blog.html)
* [https://www.algolia.com/doc/](https://www.algolia.com/doc/)



## SEO

* [Use Jekyll like a pro: Improving SEO](https://codeburst.io/use-jekyll-like-a-pro-improving-seo-c8cfb81781b7)

### Jekyll-SEO-Tag

* <a href="https://help.github.com/en/articles/search-engine-optimization-for-github-pages" target="_blank">Search Engine Optimization for Github Pages - help.github.com</a>
* <a href="https://github.com/jekyll/jekyll-seo-tag" target="_blank">/jekyll/jekyll-seo-tag</a>
* <a href="https://github.com/pmarsceill/jekyll-seo-gem" target="_blank">/pmarsceill/jekyll-seo-gem</a>
* <a href="https://github.com/meedan/meedan.code/commit/a9ad6e794fffd35035aa7e5bfb1200a34fe0e479" target="_blank">Override default jekyll-seo-tag template</a>
* <a href="https://blog.webjeda.com/optimize-jekyll-seo/" target="_blank">Tips to Optimize Jekyll SEO</a>
* [blog.webjeda.com/optimize-jekyll-seo/#6-open-graph-and-twitter-cards-in-jekyll](https://blog.webjeda.com/optimize-jekyll-seo/#6-open-graph-and-twitter-cards-in-jekyll)


### Open Graph - Favicons and More

* <a href="https://warfareplugins.com/open-graph-tags-twitter-cards-rich-pins/" target="_blank">Open Graph Tags, Twitter Cards, Rich Pins</a>
* <a href="https://www.reddit.com/r/discordapp/comments/82p8i6/a_basic_tutorial_on_how_to_get_the_most_out_of/" target="_blank">A basic tutorial on "How to get the most out of embeds?" for a discord-friendly website!</a> (supports og values)
  * <a href="https://discordapp.com/developers/docs/resources/channel#embed-limits" target="_blank">discordapp.com/developers/docs/resources/channel#embed-limits</a>
* <a href="https://iframely.com/debug" target="_blank">https://iframely.com/debug</a>
* [realfavicongenerator.net](https://realfavicongenerator.net) 
  > The strict minimum for the master picture is 70x70. Your picture is 225x225, which is ok. However, it is recommended to use a picture of at least 260x260. If you still want to use your picture, some of the derivated favicons will not be generated, such as the high resolution tile for Windows 8 / IE 11.
* <a href="http://ogp.me" target="_blank">ogp.me</a> - Open Graph Webpage (really good resource for Facebook and beyond. great links at bottom.)
* [developers.google.com - Breadcrumbs](https://developers.google.com/search/docs/data-types/breadcrumb)
  ![](https://i.imgur.com/TWbbVhn.png)
* [Googles guide to enhancing your site's metadata](https://developers.google.com/search/docs/guides/enhance-site)



### Twitter

* <a href="https://cards-dev.twitter.com/validator" target="_blank">Twitter Card Validator</a>
* <a href="https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards" target="_blank">About Cards - developer.twitter.com</a>
* [https://github.com/jekyll/jekyll-mentions/](https://github.com/jekyll/jekyll-mentions/)


## Bug Testing

Buidling your site locally is the best way to figure out why it's not publishing correctly via GitHub.

You must set up your gemfile specifically for each theme.

* [Install bundler](https://bundler.io/)

then prepare bundler for your project:

     bundle update

     bundle install

Build gives an error message if the build fails

     bundle exec jekyll build

Serve builds and "serves" a local browsable copy

     bundle exec jekyll serve

Trace gives details on errors (but won't always show your problem)

     bundle exec jekyll build --trace

Verbose... you get the idea.

     bundle exec jekyll build --verbose


### Proofers

* [gjtorikian/html-proofer](https://github.com/gjtorikian/html-proofer) - you got broken links bruh

### Linters

coming soon....

## Technical Deets

### HTML - CSS

* <a href="https://htmldog.com/guides/html/beginner/" target="_blank">htmldog.com - HTML5 and CSS Beginner Tutorials</a> 
* <a href="https://www.w3schools.com/w3css/w3css_sidebar.asp" target="_blank">/w3css/w3css_sidebar.asp</a>
* <a href="https://www.w3.org/wiki/The_web_standards_model_-_HTML_CSS_and_JavaScript" target="_blank">The_web_standards_model_-_HTML_CSS_and_JavaScript</a>
* <a href="https://developer.mozilla.org/en-US/docs/Learn" target="_blank">Learn web development - developer.mozilla.org</a>
* <a href="https://codepen.io/maziarzamani/pen/eJKGvj" target="_blank">Flat CSS Sidebar</a>
* <a href="https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML" target="_blank">The Head - Metadata in HTML</a>
* <a href="https://metatags.io" target="_blank">https://metatags.io</a>
* [https://htmlcolorcodes.com/color-chart/](https://htmlcolorcodes.com/color-chart/)
* [rtable](https://dbushell.com/2016/03/04/css-only-responsive-tables/)
* <a href="https://unicode-table.com/en/#miscellaneous-symbols-and-pictographs" target="_blank">unicode-table.com/#miscellaneous-symbols-and-pictographs</a> 
* [katex](https://khan.github.io/KaTeX/)
* [Viewport and Media Queries](https://docs.google.com/presentation/d/1rmxwWa9P6_xHqonmh5ONXRS-jPc5XKbnv99Rjkhe04s/present?slide=id.i0)

### Kramdown

* <a href="https://kramdown.gettalong.org/" target="_blank">kramdown.gettalong.org</a>
* [Kramdown - Syntax](https://kramdown.gettalong.org/syntax.html)

### Liquid

<img src="https://i.imgur.com/jMtd9WR.png"/>

* [shopify.github.io/liquid/tags/control-flow/](http://shopify.github.io/liquid/tags/control-flow/)
* <a href="https://simpleit.rocks/ruby/jekyll/templates/jekyll-variables-and-liquid-template-tags-cheatsheet/" target="_blank">Jekyll Variables and Liquid Template Tags-Cheatsheet</a>
* <a href="https://learn.cloudcannon.com/jekyll/introduction-to-liquid/" target="_blank">Introduction to Liquid for Jekyll</a>
* <a href="https://blog.webjeda.com/jekyll-liquid/" target="_blank">https://blog.webjeda.com/jekyll-liquid/</a>

### Git

* <a href="https://gist.github.com/davfre/8313299" target="_blank">davfre/git_cheat-sheet.md</a>
* <a href="https://education.github.com/git-cheat-sheet-education.pdf" target="_blank">education.github.com - GIT CHEAT SHEET</a>
* <a href="https://chris.beams.io/posts/git-commit/" target="_blank">Writing Effective Commits</a>
* [www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
* [Git CheetSheet](https://github.com/jonathancross/jc-docs/blob/master/Git-CheatSheet.md)
* [Working with Remotes](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes)
* [managing-commit-signature-verification](https://help.github.com/en/articles/managing-commit-signature-verification)
* [mnyrop/swc-materials/blob/master/git.md](https://github.com/mnyrop/swc-materials/blob/master/git.md)
* [Git-Tools-Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules) - so you can pull other git repos into your project


### SSH

* <a href="https://help.github.com/en/articles/connecting-to-github-with-ssh" target="_blank">Connecting to GitHub with SSH</a>
* <a href="https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent" target="_blank">Generating a new SSH key and adding it to the SSH agent</a>
* <a href="https://help.github.com/en/enterprise/2.15/user/articles/adding-a-new-ssh-key-to-your-github-account" target="_blank">Adding a new SSH key to your GitHub Account</a>
* <a href="https://medium.freecodecamp.org/manage-multiple-github-accounts-the-ssh-way-2dadc30ccaca" target="_blank">How to manage multiple GitHub accounts on a single machine with SSH keys</a>

### Data

* [https://mademistakes.com/notes/static-files/](https://mademistakes.com/notes/static-files/)
* [jekyllrb.com/docs/datafiles/](https://jekyllrb.com/docs/datafiles/)
* [https://github.com/ashmaroli/jekyll-data](https://github.com/ashmaroli/jekyll-data)
* [how-to-easily-use-airtable-data-in-jekyll](https://community.airtable.com/t/how-to-easily-use-airtable-data-in-jekyll/3925)
* [mnyrop/pagemaster](https://github.com/mnyrop/pagemaster)
* [https://minicomp.github.io/wax/reuse/](https://minicomp.github.io/wax/reuse/)
* [http://marii.info/wax_docs/](http://marii.info/wax_docs/)
* [http://marii.info/annotate/](http://marii.info/annotate/)
* [project-management/jupyter-notebook-on-jekyll/](https://www.linode.com/docs/applications/project-management/jupyter-notebook-on-jekyll/)
* [managing-data-with-jekyll/](https://www.chenhuijing.com/blog/managing-data-with-jekyll/)
* [18F/jekyll-get](https://github.com/18F/jekyll-get)
* [how-i-created-a-simple-dbms-using-github-jekyll-prose-and-heroku/](http://fabian-kostadinov.github.io/2015/02/04/how-i-created-a-simple-dbms-using-github-jekyll-prose-and-heroku/)
* [contrafabulists-lessons.github.io/google-sheet-to-github-website/](https://contrafabulists-lessons.github.io/google-sheet-to-github-website/)
* [execute-millions-of-sql-statements-in-milliseconds-in-the-browser-with-webassembly-and-web-workers](https://hackernoon.com/execute-millions-of-sql-statements-in-milliseconds-in-the-browser-with-webassembly-and-web-workers-3e0b25c3f1a6)
* [https://github.blog/2012-06-12-github-data-challenge-winners/](https://github.blog/2012-06-12-github-data-challenge-winners/)

### JSON

* [A JSON content feed for Jekyll](https://natelandau.com/a-json-feed-for-jekyll/)
* [Counting and JSON output in Jekyll](http://www.cagrimmett.com/til/2016/05/20/json-output-in-jekyll.html)
* [Jekyll — Convert Full YAML Front-matter to XML/JSON](https://stackoverflow.com/questions/16889512/jekyll-convert-full-yaml-front-matter-to-xml-json)
* [Inlining JSON in a Jekyll Liquid Template](https://mrcoles.com/inlining-json-jekyll-liquid-template/)
* [Jekyll JSON API](https://www.techiediaries.com/how-to-use-jekyll-like-a-pro-output-data-as-json/)
* [JSON Feed Viewer](https://json-feed-viewer.herokuapp.com/feed/?url=https%3A%2F%2Fndarville.com%2Ffeed.json)


### Automation

* [alternativeto.net/software/heroku/?license=free](https://alternativeto.net/software/heroku/?license=free)
* [integrating-autogenerated-content-into-your-documentation-site-using-swagger-and-jekyll](https://www.enigma.com/blog/integrating-autogenerated-content-into-your-documentation-site-using-swagger-and-jekyll)
* [benbalter/jekyllbot](https://github.com/benbalter/jekyllbot) - Listens for GitHub post-recieve service hooks messages, runs jekyll, and pushes the results back to GitHub. 
* [automate-github-pages-ifttt-glitch.html](https://webrender.net/2017/11/23/automate-github-pages-ifttt-glitch.html)

### API Evangelist 

Not sure how much of this is useful, but I'll save for further examination.

* [simple-apis-with-jekyll-and-github-with-data-manag](https://dzone.com/articles/simple-apis-with-jekyll-and-github-with-data-manag)
* [providing-yaml-driven-xml-json-and-atom-using-jekyll-and-github](https://apievangelist.com/2016/09/19/providing-yaml-driven-xml-json-and-atom-using-jekyll-and-github/)
* [google-spreadsheet-to-yaml-on-jekyll/](http://kinlane.com/2016/10/11/google-spreadsheet-to-yaml-on-jekyll/)
* [using-github-repos-and-jekyll-as-a-data-store/](http://kinlane.com/2016/08/15/using-github-repos-and-jekyll-as-a-data-store/)
* [kinlane.github.io/github-micro-tool/](https://kinlane.github.io/github-micro-tool/)
* [openapi.toolbox.apievangelist.com/documentation/](http://openapi.toolbox.apievangelist.com/documentation/)
* [kinlane.github.io/what-is-openapi/](https://kinlane.github.io/what-is-openapi/)
* [d3js-visualizations-using-yaml-and-jekyll/](https://apievangelist.com/2016/09/20/d3js-visualizations-using-yaml-and-jekyll/)
* [https://github.com/kinlane/OpenAPI-Specification](https://github.com/kinlane/OpenAPI-Specification)


### Indieweb

<a href="https://infominer.id/indieweb" class="btn btn-success">infominer.id/indieweb</a>

* [indieweb.org](https://indieweb.org)
* [Micropub](https://indieweb.org/Micropub)
* [IndieAuth](https://indieweb.org/IndieAuth)
* [miklb/jekyll-indieweb](https://github.com/miklb/jekyll-indieweb)
* [Static Site Generators & the IndieWeb](https://www.growdigital.org/posts/static-site-generators-the-indieweb/)
* [Jekyll and the Indieweb](http://wordius.com/jekyll-and-the-indieweb/)
* [Implementing the Indieweb on a static website](https://vincentp.me/articles/2018/11/14/20-00/) - Sending and receiving Webmentions and Micropub on a static site
* [voxpelli/webpage-micropub-to-github/](https://github.com/voxpelli/webpage-micropub-to-github/)

