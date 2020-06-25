---
layout: page-fullwidth
title: "GitHub Pages-Starter Pack"
teaser: "Publishing a Website via GitHub pages is free, and easy. Everything you need to get going in one place + extended resources."

categories: ['JAMStack']
tags: ['Jekyll', 'GitHub Pages','GitHub']

header: no
image: 
  title: "gh-pages-starter-pack.png"
  caption: "Extended Resources"
  caption_url: /jamstack/github-pages-extended-resources/
  thumb: "github.png"

permalink: /jamstack/github-pages-starter-pack/
modified: 2019-11-17T15:59:13-23:00
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

I'm just a newb that created this resource to help myself. Github makes it easy to get started web-publishing. With the click of a button, you can have a web-page live, requiring only markdown skills (that anyone can learn on the go).

Each feature you want to enable requires a little more learning, and GitHub Pages is set up so that if you decide to, you can gradually progress from content creator to web-developer. 

If you don’t want to think about web-development, and simply want your markdown files to look beautiful once published, github pages can help you do that too.

The number of technical subjects I've begun to learn is incredible!

Thanks to github and it's dedicated community of open-source creators.

## Getting Started

The simplest way to use pages is to choose one of the [official GitHub pages themes](https://pages.github.com/themes/). Just go into your repository settings:

![](https://i.imgur.com/sw4Iann.png)

All you really need to do is select a branch and it will begin publishing your repository. Then choose a method to publish.

The first repository for your web-page must be named like so: `username.github.io`. For example, the repository for my personal page is called `infominer33.github.io`.  Simply create a new repository, and if your github username is `@awesomesauce` then you would create a new directory named `awesomesauce.github.io`.

Every other repository you own can also be made into its own web-page, that will published off of your user page, with the same name following your domain. So if you have a repository called, `/Dynomite` and you go into settings select pages to publish from the master branch, then that page will be found at `https://awesomesauce.github.io/Dynomite`.

so [github.com/didecentral/didecentral.github.io](https://github.com/didecentral/didecentral.github.io) is published at [decentralized-id.com](https://decentralized-id.com), because I have a custom domain. But it can still be found at, [infominer33.github.io/DIDecentralized](https://decentralized-id.com).

* [Github Pages Community Forum](https://github.community/t5/GitHub-Pages/bd-p/pages)
* [https://pages.github.com/versions/](https://pages.github.com/versions/) - These plugins can be used via gh-pages.
* [Configuring a Publishing Source for GitHub Pages](https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages)
* [help.github.com - User, Organization, and Project Pages](https://help.github.com/en/articles/user-organization-and-project-pages)
* [http://ragupappu.com/2015/04/22/setup-website-using-github-pages-and-jekyll/](http://ragupappu.com/2015/04/22/setup-website-using-github-pages-and-jekyll/)
* [Setting up You GitHub Pages Site Locally with Jekyll](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll)
  * [-- Local development with GitHub Pages](https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-3-Local-development-with/ba-p/2292)
* [Getting started with GitHub Pages: Part 4 -- Customizing your Pages site](https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-4-Customizing-your-Pages/ba-p/4058)
* [Clearing Up Confusion around Baseurl](https://byparker.com/blog/2014/clearing-up-confusion-around-baseurl/)

### GitHub Supported

Those basic github themes are mostly for developers who want a page to put up for a software project, or anyone who just wants a basic blog to get started. This way, you could get started writing blogs immediately, and learn the basics. Later, it's easy to bring those old posts to a new theme.

[GitHub Pages Supports](https://pages.github.com/themes/) the following gem themes:

* [Architect](https://github.com/pages-themes/architect)
* [Cayman](https://github.com/pages-themes/cayman)
* [Dinky](https://github.com/pages-themes/dinky)
* [Hacker](https://github.com/pages-themes/hacker)
* [Leap day](https://github.com/pages-themes/leap-day)
* [Merlot](https://github.com/pages-themes/merlot)
* [Midnight](https://github.com/pages-themes/midnight)
* [Minima](https://github.com/jekyll/minima)
* [Minimal](https://github.com/pages-themes/minimal)
* [Modernist](https://github.com/pages-themes/modernist)
* [Slate](https://github.com/pages-themes/slate)
* [Tactile](https://github.com/pages-themes/tactile)
* [Time machine](https://github.com/pages-themes/time-machine)



### Gem Based Themes

Gem files are ruby packages that contain all of the files necessary for building your site, and keep your repository directory un-cluttered. Then, if you want to change a file that's in the gem, you just create the directory and pur the file where it goes, and configure as you wish. 

* [planetjekyll/awesome-jekyll-themes](https://github.com/planetjekyll/awesome-jekyll-themes)

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

### Remote Themes

This makes it simpler to keep your source files up to date. However, it is slower than using gems to build locally
  
* [github.blog/2017-11-29-use-any-theme-with-github-pages/](https://github.blog/2017-11-29-use-any-theme-with-github-pages/)
* [Jekyll Remote Theme](https://github.com/benbalter/jekyll-remote-theme)
    
```
plugins:
  - jekyll-remote-theme

remote_theme: benbalter/retlab
```

Essentially, if you're just editing files on github, you should just add those lines to your _config.yml along w an index file and Jekyll should build your site.


### Classic Themes

These classic themes are just files and folders, everything where you can see it (and should be forkable to create working websites).

* [drjekyllthemes.github.io](https://drjekyllthemes.github.io) (classic 'files and folders')
* [ChristopherA/simplest-github-page](https://github.com/ChristopherA/simplest-github-page)
* [prose/starter](https://github.com/prose/starter)
* [kinlane/beforeeighteen](https://github.com/kinlane/beforeeighteen) (template for presentation style pages.)

## Jekyll

![](https://web-work.tools/images/gh-jekyll.png)

* [Jekyll README](https://github.com/jekyll/jekyll/blob/master/README.markdown)
* [planetjekyll](https://github.com/planetjekyll)
  * [planetjekyll/awesome-jekyll](https://github.com/planetjekyll/awesome-jekyll)
* [Jekyll - Cheat Sheet](https://devhints.io/jekyll)
* [Jekyll Community Forum](http://talk.jekyllrb.com/)
* [Jekyll - Pagination Docs](https://jekyllrb.com/docs/pagination/)
* [Jekyll - Navigation Tutorial](https://jekyllrb.com/tutorials/navigation/)
* [https://wiredcraft.com/blog/make-jekyll-fast](https://wiredcraft.com/blog/make-jekyll-fast)
* [Jekyll - Static Site Generator | Tutorial](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB) (youtube playlist from 2017), I can't guarantee everything will be perfectly up to date.
* [Run a Specific Version of Bundler](https://makandracards.com/makandra/9741-run-specific-version-of-bundler)
  * Can get older themes to work if you use the right verion of bundler (found in gemfile.lock).
* [benbalter/jekyll-style-guide](https://github.com/benbalter/jekyll-style-guide)

### Jekyll Themes

I'll say now, if you are new to web-development, best to start off trying out a few of the [official GitHub Pages Themes](https://pages.github.com/themes/). 

Once installed, I cloned those repos locally so its easier to see how everything works. Then, if I want to configure a file that's not in my repository, I have a copy nearby. You can grab the `_layouts/default.html`, put it in your repo, and get a feel for how configuring that template shapes your entire site. But then you configure individual pages, and categories, perhaphs, to display differently. 

* [planetjekyll/awesome-jekyll-themes](https://github.com/planetjekyll/awesome-jekyll-themes) (gem-based)
* [themes.jekyllrc.org](http://themes.jekyllrc.org/)
* [Jekyll Theme Showcase](http://talk.jekyllrb.com/t/jekyll-theme-showcase-share-your-jekyll-themes/1382)
* [techgaun.github.io/active-forks](https://techgaun.github.io/active-forks) - Find active forks of your favorite GitHub repos.

The problem is that all of these websites are not exactly up to date. Many of the themes listed above were written for older versions of Jekyll. 

Choosing a theme is very personal to your needs, also.

### Found Themes

I'm keeping track of themes that catch my eye:

* [Type on Strap](https://sylhare.github.io/Type-on-Strap/) - [Source](https://github.com/sylhare/Type-on-Strap)
* [Beautiful Jekyll](http://deanattali.com/beautiful-jekyll) - [Source](https://github.com/daattali/beautiful-jekyll)
* [Feeling Responsive](http://phlow.github.io/feeling-responsive/) - [Source](https://github.com/Phlow/feeling-responsive)
* [Just the Docs](https://pmarsceill.github.io/just-the-docs/)
* [Documentation Theme Jekyll](https://idratherbewriting.com/documentation-theme-jekyll)
* [projectpages.github.io/project-pages/](https://projectpages.github.io/project-pages/)
  * [project-pages/wiki](https://github.com/projectpages/project-pages/wiki)
* [bradleytaunt/lightspeed](https://github.com/bradleytaunt/lightspeed)
* [era.yayd.in/jekyll-bulma/](https://era.yayd.in/jekyll-bulma/)
* [https://ndrewtl.github.io/airspace-jekyll/](https://ndrewtl.github.io/airspace-jekyll/)
  * [ndrewtl/airspace-jekyll/](https://github.com/ndrewtl/airspace-jekyll/)
* [github/personal-website](https://github.com/github/personal-website)
  > Code that'll help you kickstart a personal website that showcases your work as a software developer.
  ![](https://imgur.com/7UjPtdAl.png)
* [polyglot.untra.io](https://polyglot.untra.io/) - multi-lingual publishing.
* [hydecorp/hydejack](https://github.com/hydecorp/hydejack) 
  - [/hydecorp/hydejack-starter-kit](https://github.com/qwtel/hydejack-starter-kit)
  * [Hydejack Documentation.pdf](http://nickengmann.com/Documentation.pdf)
  * [Hydejack Advanced](https://github.com/hydecorp/hydejack/blob/master/docs/advanced.md)

### Minimal Mistakes

When I was first looking for a jekyll theme, it seemed I couldn't get away from this theme in google search results. No wonder, it's stable, creates gorgeous sites right out the box, and has every feature you could want, as a beginner. I see plenty of professional sites built with it, tho I don't always even realize right away.

Not only that, it has **excellent** documentation! You can find pretty much everything you need to run Minimal Mistakes in the Quickstart Guide, Sample Posts and Collections, along with their corresponding files on Github.

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

* [So Simple Theme](https://mmistakes.github.io/so-simple-theme/) - [Source](https://github.com/mmistakes/so-simple-theme)
* [Basically Basic](https://mmistakes.github.io/jekyll-theme-basically-basic/) - [source](https://github.com/mmistakes/jekyll-theme-basically-basic) - [with algolia](https://github.com/mmistakes/jekyll-theme-basically-basic-algolia-search)
* [Skinny Bones](https://mmistakes.github.io/skinny-bones-jekyll/) - [source](https://github.com/mmistakes/skinny-bones-jekyll)
* [Hpstr](https://mmistakes.github.io/hpstr-jekyll-theme/) - [source](https://github.com/mmistakes/hpstr-jekyll-theme)

## Setup
**Create an index.md**

Although pages will build an index.html from your readme.md, pages will not behave as expected if you try to do any configuration or additional optimization with only readme.md.

in that index.md you need to include front matter:

```
---
layout: default
---
```

There is a plugin that will builds index files from all the readme.md files of your repository.. but it has trouble creating an index.html from your repositories primary README.md.


### Front Matter

* [Front Matter](https://jekyllrb.com/docs/front-matter/)
* [YAML front matter in Jekyll](http://simpleprimate.com/blog/front-matter)
* [YAML tutorial in the context of Jekyll](https://idratherbewriting.com/documentation-theme-jekyll/mydoc_yaml_tutorial)


### Layouts

Layouts are preconfigured page templates. When I started, it was too much to think about layouts, and I would use "single" and "page". Now that I am using blog posts.. (because they populate your RSS feed, and increases their portability) I'm also using the Home layout:

![](https://imgur.com/ikX9wF6l.png)

* [https://jekyllrb.com/docs/step-by-step/04-layouts/](https://jekyllrb.com/docs/step-by-step/04-layouts/)
* [documentation-theme-jekyll/tag_special_layouts.html](https://idratherbewriting.com/documentation-theme-jekyll/tag_special_layouts.html)

### Collections 
* [https://jekyllrb.com/docs/collections/](https://jekyllrb.com/docs/collections/)
* [http://stories.upthebuzzard.com/jekyll_notes/](http://stories.upthebuzzard.com/jekyll_notes/)
  * [using-jekyll-collections.html](http://stories.upthebuzzard.com/jekyll_notes/2017-02-15-using-jekyll-collections.html)
  * [prev-and-next-within-a-jekyll-collection.html](http://stories.upthebuzzard.com/jekyll_notes/2017-02-19-prev-and-next-within-a-jekyll-collection.html)
  * [sort-order-of-jekyll-collections.html](http://stories.upthebuzzard.com/jekyll_notes/2017-02-19-sort-order-of-jekyll-collections.html)
  * [accessing-jekyll-collection-details-from-a-post.html](http://stories.upthebuzzard.com/jekyll_notes/2017-02-19-accessing-jekyll-collection-details-from-a-post.html)

### Plugins
* [jekyllrb.com/docs/plugins/installation/](https://jekyllrb.com/docs/plugins/installation/)
* [planetjekyll/awesome-jekyll-plugins](https://github.com/planetjekyll/awesome-jekyll-plugins)
* [Jekyll-Target-Blank](https://keith-mifsud.me/projects/jekyll-target-blank)
* [https://github.com/jekyll/jekyll-mentions/](https://github.com/jekyll/jekyll-mentions/)
* [Github Flavored Emoji for Jekyll](https://github.com/jekyll/jemoji)
* [Adding Jekyll Plugins to a GitHub Pages Site - help.github.com](https://help.github.com/en/articles/adding-jekyll-plugins-to-a-github-pages-site)
* [Creating Custom 404 page](https://help.github.com/en/articles/creating-a-custom-404-page-for-your-github-pages-site)
* [Implemented the "Edit this page" feature. jekyll#3495](https://github.com/delftswa2014/jekyll/commit/e109555aa0533148c53200e63d1e60a3acf67e74)
* [Jekyll Redirect Plugin](https://help.github.com/en/articles/redirects-on-github-pages)

Use `redirect_from: internal/url` to change the location you are publishing, but keep old links.
Use `redirect_to: https://external.url` to send visitors somewhere else (perhaps you want it to live on another site, but not lose your valuable links :)
{: .notice }

### Domains

Namecheap supports BTC purchases, so I'm including their github how-to here. If you know of other crypto-friendly domain providers, lmk in the issues.

* [https://help.github.com/en/articles/using-a-custom-domain-with-github-pages](https://help.github.com/en/articles/using-a-custom-domain-with-github-pages)
* [Using Custom Domain for Github Pages](https://medium.com/@hossainkhan/using-custom-domain-for-github-pages-86b303d3918a)
* [namecheap.com - how-do-i-link-my-domain-to-github-pages](https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages)



## Customizations
* [digitaldrummerj.me/categories/jekyll](https://digitaldrummerj.me/categories/jekyll/)
* [Social Media Share Bar](https://mycyberuniverse.com/social-media-share-bar-jekyll-blog-website.html)
* [Validating Links and Images](https://digitaldrummerj.me/jekyll-validating-links-and-images/)
* [longqian.me/](http://longqian.me/) -Metamask Donation Button.
* [https://superdevresources.com/share-buttons-jekyll/](https://superdevresources.com/share-buttons-jekyll/)
* [Embed files from a github repository onto your page.](http://gist-it.appspot.com/)
* [Redirecting GitHub Pages after a repository move](https://gist.github.com/domenic/1f286d415559b56d725bee51a62c24a7)
* [hacking-routing-component-jekyll/](https://www.sitepoint.com/hacking-routing-component-jekyll/)
* [How-to-build-a-lowtech-website](https://solar.lowtechmagazine.com/2018/09/how-to-build-a-lowtech-website/)
* [Multiple Authors for the Same Post](https://github.com/mmistakes/minimal-mistakes/issues/1341#issuecomment-505660670)

### Comments
* [Github Issues for Blog Comments](http://artsy.github.io/blog/2017/07/15/Comments-are-on/)
* [A repo you can use to work-around GH issue comment request limmits.](https://github.com/orta/gh-commentify)
* [Various ways you can add comments to your static site](https://darekkay.com/blog/static-site-comments/)
* [Add comments to your jekyll powered blog](https://github.com/damieng/jekyll-blog-comments)
* [Setting up Staticman Server](https://www.flyinggrizzly.net/2017/12/setting-up-staticman-server/)
  * [new feature! added comments to this *static* website](https://www.edwinwenink.xyz/posts/18-comments/)
* [https://mademistakes.com/articles/jekyll-static-comments/](https://mademistakes.com/articles/jekyll-static-comments/)
  * [https://mademistakes.com/articles/improving-jekyll-static-comments/](https://mademistakes.com/articles/improving-jekyll-static-comments/)

### Image Galleries



### Search

* [Elasticsearch for Jekyll](https://blog.omc.io/elasticsearch-for-jekyll-part-1-ab456ac7c093)
* [Adding Custom Google Search](https://digitaldrummerj.me/blogging-on-github-part-7-adding-a-custom-google-search/)
* [github.com/algolia/jekyll-algolia](https://github.com/algolia/jekyll-algolia)
* [community.algolia.com/jekyll-algolia/blog.html](https://community.algolia.com/jekyll-algolia/blog.html)
* [https://www.algolia.com/doc/](https://www.algolia.com/doc/)



## SEO

* [Use Jekyll like a pro: Improving SEO](https://codeburst.io/use-jekyll-like-a-pro-improving-seo-c8cfb81781b7)

### Jekyll-SEO-Tag

* [Search Engine Optimization for Github Pages - help.github.com](https://help.github.com/en/articles/search-engine-optimization-for-github-pages)
* [/jekyll/jekyll-seo-tag](https://github.com/jekyll/jekyll-seo-tag)
* [/pmarsceill/jekyll-seo-gem](https://github.com/pmarsceill/jekyll-seo-gem)
* [Override default jekyll-seo-tag template](https://github.com/meedan/meedan.code/commit/a9ad6e794fffd35035aa7e5bfb1200a34fe0e479)
* [Tips to Optimize Jekyll SEO](https://blog.webjeda.com/optimize-jekyll-seo/)
* [blog.webjeda.com/optimize-jekyll-seo/#6-open-graph-and-twitter-cards-in-jekyll](https://blog.webjeda.com/optimize-jekyll-seo/#6-open-graph-and-twitter-cards-in-jekyll)


### Open Graph - Favicons and More

* [Open Graph Tags, Twitter Cards, Rich Pins](https://warfareplugins.com/open-graph-tags-twitter-cards-rich-pins/)
* [A basic tutorial on "How to get the most out of embeds?" for a discord-friendly website!](https://www.reddit.com/r/discordapp/comments/82p8i6/a_basic_tutorial_on_how_to_get_the_most_out_of/) (supports og values)
  * [discordapp.com/developers/docs/resources/channel#embed-limits](https://discordapp.com/developers/docs/resources/channel#embed-limits)
* [https://iframely.com/debug](https://iframely.com/debug)
* [realfavicongenerator.net](https://realfavicongenerator.net) 
  > The strict minimum for the master picture is 70x70. Your picture is 225x225, which is ok. However, it is recommended to use a picture of at least 260x260. If you still want to use your picture, some of the derivated favicons will not be generated, such as the high resolution tile for Windows 8 / IE 11.
* [ogp.me](http://ogp.me) - Open Graph Webpage (really good resource for Facebook and beyond. great links at bottom.)
* [developers.google.com - Breadcrumbs](https://developers.google.com/search/docs/data-types/breadcrumb)
  ![](https://i.imgur.com/TWbbVhn.png)
* [Googles guide to enhancing your site's metadata](https://developers.google.com/search/docs/guides/enhance-site)



### Twitter

* [Twitter Card Validator](https://cards-dev.twitter.com/validator)
* [About Cards - developer.twitter.com](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards)
* [https://github.com/jekyll/jekyll-mentions/](https://github.com/jekyll/jekyll-mentions/)


## Build Local - Bug Testing

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

## Technical


### Liquid

<img src="https://i.imgur.com/jMtd9WR.png"/>

* [shopify.github.io/liquid/tags/control-flow/](http://shopify.github.io/liquid/tags/control-flow/)
* [Jekyll Variables and Liquid Template Tags-Cheatsheet](https://simpleit.rocks/ruby/jekyll/templates/jekyll-variables-and-liquid-template-tags-cheatsheet/)
* [Introduction to Liquid for Jekyll](https://learn.cloudcannon.com/jekyll/introduction-to-liquid/)
* [https://blog.webjeda.com/jekyll-liquid/](https://blog.webjeda.com/jekyll-liquid/)

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

<!--
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
-->

### Indieweb

<a href="https://web-work.tools/indieweb-resources/" class="btn btn-success">web-work.tools/indieweb-resources</a>

* [indieweb.org](https://indieweb.org)
* [Micropub](https://indieweb.org/Micropub)
* [IndieAuth](https://indieweb.org/IndieAuth)
* [miklb/jekyll-indieweb](https://github.com/miklb/jekyll-indieweb)
* [Static Site Generators & the IndieWeb](https://www.growdigital.org/posts/static-site-generators-the-indieweb/)
* [Jekyll and the Indieweb](http://wordius.com/jekyll-and-the-indieweb/)
* [Implementing the Indieweb on a static website](https://vincentp.me/articles/2018/11/14/20-00/) - Sending and receiving Webmentions and Micropub on a static site
* [voxpelli/webpage-micropub-to-github/](https://github.com/voxpelli/webpage-micropub-to-github/)


</div>