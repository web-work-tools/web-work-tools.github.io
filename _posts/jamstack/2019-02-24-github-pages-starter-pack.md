---
layout: page-fullwidth
title: "GitHub Pages-Starter Pack + Extended Resources"
teaser: "Publishing a Website via GitHub pages is free, and easy. Everything you need to get going in one place plus extended resources."

categories: ['JAMStack']
tags: ['Jekyll', 'GitHub Pages','GitHub']

header: no
image: 
  title: "gh-pages-starter-pack.png"
  caption: "Extended Resources"
  caption_url: /jamstack/github-pages-extended-resources/
  thumb: "github.png"

permalink: /jamstack/github-pages-starter-pack/
modified: 2020-11-06T15:59:13-23:00
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

I started collecting links in a text file, back when I first started to use GitHub pages. There were many resources available on how to use jekyll, but not so many on how to use GitHub pages.

Github makes it easy to get started web-publishing. With the click of a button, you can have a simple web-page live, requiring only [markdown](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf) skills, that anyone can learn on the go.

I started out clicking on GitHub's GUI, and each new feature I wanted to enable required a little more learning, and GitHub Pages is set up so that, if you decide to, you can gradually progress from content creator to web-developer. 

If you don’t want to think about web-development, and simply want your markdown files to look beautiful once published, github pages can help you do that too.

The number of technical subjects I've begun to learn is incredible, thanks to GitHub and it's dedicated community of open-source creators.

## Getting Started

Before you start using Jekyll or any other [static site generators](https://web-work.tools/jamstack/static-site-generators/), it's helpful to understand how GitHub pages works.

![](https://user-images.githubusercontent.com/44134283/98421763-15ce8900-2058-11eb-93fe-969403fb4fee.png)

In your repository settings you'll find various options of where to publish your site from.

![image](https://user-images.githubusercontent.com/44134283/98423000-4d8b0000-205b-11eb-80d4-1e7503b70800.png)

Whichever of those options you choose, you can drop an index.html in the root of whatever location you chose in the above settings, and that site will be published.

### Repository Naming Conventions

The first repository for your web-page must be named like so: `username.github.io`. For example, the repository for my personal page is called `infominer33.github.io`.  Simply create a new repository, and if your github username is `@awesomesauce` then you would create a new directory named `awesomesauce.github.io`.

Every other repository you own can also be made into its own web-page, that will published off of your user page, with the same name following your domain. So if you have a repository called, `/Dynamite` and you go into settings select pages to publish from the master branch, then that page will be found at `https://awesomesauce.github.io/Dynamite`.

So [github.com/didecentral/didecentral.github.io](https://github.com/didecentral/didecentral.github.io) is published at [decentralized-id.com](https://decentralized-id.com), because I have a custom domain. But it can still be found at, [infominer33.github.io/DIDecentralized](https://decentralized-id.com).

Following these steps, so far, is all without jekyll, just html, css, and javascript. 

### Classic Themes

You can install 'classic themes' simply by copying (or forking) their repository to a space you control, and change them by editing their files manually. These are just files and folders, with everything where you can see it.

* [drjekyllthemes.github.io](https://drjekyllthemes.github.io) (classic 'files and folders')
* [ChristopherA/simplest-github-page](https://github.com/ChristopherA/simplest-github-page)
* [prose/starter](https://github.com/prose/starter)
* [kinlane/beforeeighteen](https://github.com/kinlane/beforeeighteen) (template for presentation style pages.)

### Resources

* [Github Pages Community Forum](https://github.community/t5/GitHub-Pages/bd-p/pages)
* [https://pages.github.com/versions/](https://pages.github.com/versions/) - These plugins can be used via gh-pages.
* [Configuring a Publishing Source for GitHub Pages](https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages)
* [help.github.com - User, Organization, and Project Pages](https://help.github.com/en/articles/user-organization-and-project-pages)
* [Getting started with GitHub Pages: Part 4 -- Customizing your Pages site](https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-4-Customizing-your-Pages/ba-p/4058)
* [Clearing Up Confusion around Baseurl](https://byparker.com/blog/2014/clearing-up-confusion-around-baseurl/)

## Jekyll

What separates 'classic themes' from jekyll themes is a configuration file called `_config.yml`. This lets jekyll know how to build your site, and it lets github know it can be built. 

![](https://web-work.tools/images/gh-jekyll.png)

* [Jekyll README](https://github.com/jekyll/jekyll/blob/master/README.markdown)
* [Jekyll Configuration options](https://jekyllrb.com/docs/configuration/options/)
* [Jekyll - Cheat Sheet](https://devhints.io/jekyll)
* [Jekyll Community Forum](http://talk.jekyllrb.com/)
* [Jekyll - Pagination Docs](https://jekyllrb.com/docs/pagination/)
* [Jekyll - Navigation Tutorial](https://jekyllrb.com/tutorials/navigation/)
* [Jekyll - Static Site Generator - Tutorial](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB) Youtube Playlist (2017)
* [GitHub Pages and Jekyll](https://www.youtube.com/playlist?list=PLWzwUIYZpnJuT0sH4BN56P5oWTdHJiTNq) - These videos teach you how to use GitHub Pages to create and manage websites, docs, and Jekyll blogs (2020)
* [planetjekyll](https://github.com/planetjekyll)
  * [planetjekyll/awesome-jekyll](https://github.com/planetjekyll/awesome-jekyll)

### Official GitHub Pages Themes

The simplest way to use jekyll\github-pages is to choose one of the [official GitHub pages themes](https://pages.github.com/themes/). 

![](https://i.imgur.com/sw4Iann.png)

Those basic github themes are mostly for developers who want a page to put up for a software project, or anyone who just wants a basic blog to get started learning. Using the theme chooser, you can get started writing blogs immediately, and begin learning the basics of how jekyll sites are configured. 

Once installed, I cloned those repos locally so its easier to see how everything works. Then, if I want to configure a file that's not in my repository, I have a copy nearby. You can grab the `_layouts/default.html`, put it in your repo, and get a feel for how configuring that template shapes your entire site. But then you configure individual pages, and parts of your site to display differently. 

GitHub Pages has [the following themes](https://pages.github.com/themes/) built in, you can begin learning with a few clicks:

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

After you've learned the ropes, it's easy to bring any content you created to a new theme.

#### ¡!Create an index.md¡!

Although pages will build an index.html from your readme.md, pages will not behave as expected if you try to do any configuration or additional optimization with only readme.md.

In that index.md you need to include front matter:

```
---
layout: default
---
```

There is a plugin that will builds index files from all the readme.md files of your repository.. but it has trouble creating an index.html from your repositories primary README.md.


### Finding Jekyll Themes

There are tons of themes available for Jekyll... it's just not neccessarily easy to figure out how to use them, when you're first learning. Especially because they've all been built with\for different versions of Jekyll.

After I find a theme I like, I fork it and then go to settings and choose master, docs, or gh-pages, depending on how the site is designed, to make sure it's working. I've spent a lot of time configuring themes I didn't verify I could get running first. Don't do that :) 

* [github.com/topics/jekyll-theme](https://github.com/topics/jekyll-theme)
* [planetjekyll/awesome-jekyll-themes](https://github.com/planetjekyll/awesome-jekyll-themes) (gem-based)
* [themes.jekyllrc.org](http://themes.jekyllrc.org/)
* [Jekyll Theme Showcase](http://talk.jekyllrb.com/t/jekyll-theme-showcase-share-your-jekyll-themes/1382)
* [techgaun.github.io/active-forks](https://techgaun.github.io/active-forks) - Find active forks of your favorite GitHub repos.

### Minimal Mistakes

When I was first looking for a jekyll theme, I couldn't get away from this theme in google search results, and had a lot of trouble getting others to work. Minimal Mistakes is probably the most robust and reliable jekyll theme available.

Not only that, it has **excellent** documentation! You can find pretty much everything you need to run Minimal Mistakes in the Quickstart Guide, Sample Posts and Collections, along with their corresponding files on Github.

Minimal Mistakes is forkable to create a working site, and its a gem-based theme.

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

I have my own demo site with lots of detailed instructions on how I set them up, you can check out here: [web-work.tools/minimal-mistakes/](https://web-work.tools/minimal-mistakes/)

### Other Jekyll Themes I Like

Here are some themes that have caught my eye, and I know they work.

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

#### Themes by [@mmistakes](https://github.com/mmistakes):

* [So Simple Theme](https://mmistakes.github.io/so-simple-theme/) - [Source](https://github.com/mmistakes/so-simple-theme)
* [Basically Basic](https://mmistakes.github.io/jekyll-theme-basically-basic/) - [source](https://github.com/mmistakes/jekyll-theme-basically-basic) - [with algolia](https://github.com/mmistakes/jekyll-theme-basically-basic-algolia-search)
* [Skinny Bones](https://mmistakes.github.io/skinny-bones-jekyll/) - [source](https://github.com/mmistakes/skinny-bones-jekyll)
* [Hpstr](https://mmistakes.github.io/hpstr-jekyll-theme/) - [source](https://github.com/mmistakes/hpstr-jekyll-theme)

## Setup

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

* [Configuring a custom domain for your GitHub Pages site](https://help.github.com/en/articles/using-a-custom-domain-with-github-pages)
* [Using Custom Domain for Github Pages](https://medium.com/@hossainkhan/using-custom-domain-for-github-pages-86b303d3918a)
* [namecheap.com - How do I link my domain to GitHub Pages](https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages)

## Customizations

* [Justin James - Jekyll Category](https://digitaldrummerj.me/categories/jekyll/)
* [Social Media Share Bar](https://mycyberuniverse.com/social-media-share-bar-jekyll-blog-website.html)
* [Validating Links and Images](https://digitaldrummerj.me/jekyll-validating-links-and-images/)
* [longqian.me/](http://longqian.me/) -Metamask Donation Button.
* [Simple Share buttons for Jekyll blog](https://superdevresources.com/share-buttons-jekyll/)
* [Embed files from a github repository onto your page.](http://gist-it.appspot.com/)
* [Redirecting GitHub Pages after a repository move](https://gist.github.com/domenic/1f286d415559b56d725bee51a62c24a7)
* [Hacking a Routing Component in Jekyll](https://www.sitepoint.com/hacking-routing-component-jekyll/)
* [Multiple Authors for the Same Post](https://github.com/mmistakes/minimal-mistakes/issues/1341#issuecomment-505660670)
* [Setup GitHub Pages "gh-pages" branch and "master" branch as subfolders of a parent project folder ("grandmaster").](https://gist.github.com/chrisjacob/833223)
* [13 Steps to a Faster Jekyll Website](https://wiredcraft.com/blog/make-jekyll-fast)
* [benbalter/jekyll-style-guide](https://github.com/benbalter/jekyll-style-guide)

### Comments
* [Github Issues for Blog Comments](http://artsy.github.io/blog/2017/07/15/Comments-are-on/)
* [A repo you can use to work-around GH issue comment request limmits.](https://github.com/orta/gh-commentify)
* [Various ways you can add comments to your static site](https://darekkay.com/blog/static-site-comments/)
* [Add comments to your jekyll powered blog](https://github.com/damieng/jekyll-blog-comments)
* [Setting up Staticman Server](https://www.flyinggrizzly.net/2017/12/setting-up-staticman-server/)
  * [new feature! added comments to this *static* website](https://www.edwinwenink.xyz/posts/18-comments/)
* [Going static part 2: static comments](https://mademistakes.com/articles/jekyll-static-comments/)
  * [Improving static comments with Jekyll & Staticman](https://mademistakes.com/articles/improving-jekyll-static-comments/)

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
* [jekyll/jekyll-seo-tag](https://github.com/jekyll/jekyll-seo-tag)
* [pmarsceill/jekyll-seo-gem](https://github.com/pmarsceill/jekyll-seo-gem)
* [Override default jekyll-seo-tag template](https://github.com/meedan/meedan.code/commit/a9ad6e794fffd35035aa7e5bfb1200a34fe0e479)
* [Tips to Optimize Jekyll SEO](https://blog.webjeda.com/optimize-jekyll-seo/)
* [10 Must do Jekyll SEO optimizations](https://blog.webjeda.com/optimize-jekyll-seo/#6-open-graph-and-twitter-cards-in-jekyll)

### Open Graph, Twitter Cards, Favicons and More

* [Open Graph Tags, Twitter Cards, Rich Pins](https://warfareplugins.com/open-graph-tags-twitter-cards-rich-pins/)
* [A basic tutorial on "How to get the most out of embeds?" for a discord-friendly website!](https://www.reddit.com/r/discordapp/comments/82p8i6/a_basic_tutorial_on_how_to_get_the_most_out_of/) (supports og values)
  * [DiscordApp Developers - Channel Embed Limits](https://discordapp.com/developers/docs/resources/channel#embed-limits)
* [Check how other apps see your site](https://debug.iframely.com/) - Debug your URLs against oEmbed, Twitter Cards, Open Graph and Iframely specs
* [realfavicongenerator.net](https://realfavicongenerator.net) 
  > The strict minimum for the master picture is 70x70. Your picture is 225x225, which is ok. However, it is recommended to use a picture of at least 260x260. If you still want to use your picture, some of the derivated favicons will not be generated, such as the high resolution tile for Windows 8 / IE 11.
* [ogp.me](http://ogp.me) - Open Graph Webpage (really good resource for Facebook and beyond. (great links at bottom.)
* [developers.google.com - Breadcrumbs](https://developers.google.com/search/docs/data-types/breadcrumb)
  ![](https://i.imgur.com/TWbbVhn.png)
* [Googles guide to enhancing your site's metadata](https://developers.google.com/search/docs/guides/enhance-site)
* [Twitter Card Validator](https://cards-dev.twitter.com/validator)
* [About Cards - developer.twitter.com](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards)
* [https://github.com/jekyll/jekyll-mentions/](https://github.com/jekyll/jekyll-mentions/)

## Gem Based Themes

Gem files are ruby packages that contain all of the files necessary for building your site, allowing you to keep your repository un-cluttered, and keeps your site up to date, when the gems developer makes updates. 

If you want to change a file that's in the gem, you just create the directory and put the file where it goes, to configure as you wish. 

* [Using Jekyll gem-based themes on Github Pages](https://4brunu.github.io/blog/2017/01/29/using-jekyll-gem-based-themes-on-github-pages)
* [planetjekyll/awesome-jekyll-themes](https://github.com/planetjekyll/awesome-jekyll-themes)

Until [GitHub Actions](https://github.com/marketplace/actions/jekyll-actions) were introduced, you needed to [Install jekyll](https://jekyllrb.com/docs/installation/) and build them locally, to the `docs` directory, which you may have noticed as an option in your repository settings. 

For user or organization pages, you can only publish from the master directory. So, this will only work for projects other than your homepage, or your organizations homepage. 

Although that's consistant with everything I've read, in practice I've found that after forking minimal mistakes, and setting up the gemfile, it will build the site for me. So I think having the entire project in my master, not relying on the gem, jekyll will build the site from master. (see `decentralized-id/decentralized-id.github.io`'s: ['_config.yml'](https://github.com/Decentralized-ID/decentralized-id.github.io/blob/master/_config.yml)) and [`gemfile`](https://github.com/Decentralized-ID/decentralized-id.github.io/blob/master/_config.yml) for reference) 

There's also using the [gh-pages](https://gist.github.com/chrisjacob/1086274/382ef1ccc22b57b9b1f0e3a362b39e806b9ba04c) branch, but that's getting a little more technical.

Until you've set up a few different sites, and figure out the ins and outs, it will take some tinkering to figure it out.

### Build with Jekyll Locally

You will find that GitHub error messages are not very descriptive. Buidling your site locally is the best way to figure out why GitHub Pages can't build your site.

#### _config.yml

You can set the destination in your `_config.yml`, otherwise jekyll will build to the `_site` directory, which is usually added to your `.gitignore` file.

```yml
destination: docs
```

If you're publishing from the `docs` directory, be sure and don't add that to your `.gitignore`, since you want your website uploaded to GitHub to be published..

#### Gemfile

Then add the gem and its source, also add any plugins you are using:

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

#### Install and Build the Site

Hopefully you have [installed `git`](/git-starter-pack/), by now. You'll need that to push any local changes to GitHub.

* [Install jekyll](https://jekyllrb.com/docs/installation/) 
* [Install bundler](https://bundler.io/)

Then use bundler to install the theme

`bundle update`

`bundle install`

Build gives an error message if the build fails

`bundle exec jekyll build`

Serve builds and "serves" a local browsable copy

`bundle exec jekyll serve`

Trace gives details on errors (but won't always show your problem)

`bundle exec jekyll build --trace`

Verbose... you get the idea.

`bundle exec jekyll build --verbose`

### Resources

* [bundler.io](https://bundler.io/)
* [Setting up You GitHub Pages Site Locally with Jekyll](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll)
  * [Local development with GitHub Pages](https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-3-Local-development-with/ba-p/2292)
* [Adding a Gem to your Gemfile - help.github.com](https://help.github.com/en/articles/adding-a-jekyll-theme-to-your-github-pages-site#adding-your-theme-as-a-gem-to-your-gemfile)
* [Run a Specific Version of Bundler](https://makandracards.com/makandra/9741-run-specific-version-of-bundler)
  * Can get older themes to work if you use the right verion of bundler (found in gemfile.lock).
* [gjtorikian/html-proofer](https://github.com/gjtorikian/html-proofer) - you got broken links bruh

### Remote Themes

This makes it simpler to keep your source files up to date. However, it is much slower than using gems to build locally (which only really matters if your site has a lot of content).
  
* [github.blog/2017-11-29-use-any-theme-with-github-pages/](https://github.blog/2017-11-29-use-any-theme-with-github-pages/)
* [Jekyll Remote Theme](https://github.com/benbalter/jekyll-remote-theme)
    
```
plugins:
  - jekyll-remote-theme

remote_theme: benbalter/retlab
```

Essentially, if you're just editing files on github, you should just add those lines to your _config.yml along w an index file and Jekyll should build your site.

## Technical

### Liquid

<img src="https://i.imgur.com/jMtd9WR.png"/>

* [Shopify - Liquid](http://shopify.github.io/liquid/tags/control-flow/)
* [Jekyll Variables and Liquid Template Tags-Cheatsheet](https://simpleit.rocks/ruby/jekyll/templates/jekyll-variables-and-liquid-template-tags-cheatsheet/)
* [Introduction to Liquid for Jekyll](https://learn.cloudcannon.com/jekyll/introduction-to-liquid/)
* [How to use Liquid Syntax in Jekyll?](https://blog.webjeda.com/jekyll-liquid/)

### Data

* [Data Files - jekyllrb](https://jekyllrb.com/docs/datafiles/)
* [Working with Jekyll data example site](https://billraymond.github.io/jekyll-data-example/) - [BillRaymond/jekyll-data-example](https://github.com/BillRaymond/jekyll-data-example)
  * [Working with Jekyll Data: Part 1 (slides only)](https://www.youtube.com/watch?v=7Jj-KX40iTE&feature=youtu.be&list=PLWzwUIYZpnJuT0sH4BN56P5oWTdHJiTNq) 
  * [Working with Jekyll Data Part 2: Built-in data](https://www.youtube.com/watch?v=d9obuvg3ReA&feature=youtu.be&list=PLWzwUIYZpnJuT0sH4BN56P5oWTdHJiTNq)
  * [Working with Jekyll Data, Part 3: Custom Data](https://www.youtube.com/watch?v=kKU-lMv5OZM&feature=youtu.be&list=PLWzwUIYZpnJuT0sH4BN56P5oWTdHJiTNq)
* [Accessing static files in Jekyll](https://mademistakes.com/notes/static-files/)
* [ashmaroli/jekyll-data](https://github.com/ashmaroli/jekyll-data)
* [How to easily use Airtable Data in Jekyll](https://community.airtable.com/t/how-to-easily-use-airtable-data-in-jekyll/3925)
* [mnyrop/pagemaster](https://github.com/mnyrop/pagemaster)
* [WAX - Reuse](https://minicomp.github.io/wax/reuse/)
  > Wax is inspired by FAIR data principles, and as such strives to make its collections findable, accessible, interoperable and reusable.
  > 
  > The demo site comes with a specific _include called interactive_metadata_table to help you make pages like this one complete with interactive DataTables and downloadable CSVs of collection metadata.
  * [Wax - Annotate](http://marii.info/annotate/)
* [Display Jupyter Notebooks with Jekyll](https://www.linode.com/docs/applications/project-management/jupyter-notebook-on-jekyll/)
* [Managing data with Jekyll](https://www.chenhuijing.com/blog/managing-data-with-jekyll/)
* [18F/jekyll-get](https://github.com/18F/jekyll-get)
* [HOW I CREATED A SIMPLE DBMS USING GITHUB, JEKYLL, PROSE AND HEROKU](http://fabian-kostadinov.github.io/2015/02/04/how-i-created-a-simple-dbms-using-github-jekyll-prose-and-heroku/)
* [Google Sheet To Github Website Lesson](https://contrafabulists-lessons.github.io/google-sheet-to-github-website/)

### JSON

* [A JSON content feed for Jekyll](https://natelandau.com/a-json-feed-for-jekyll/)
* [Counting and JSON output in Jekyll](http://www.cagrimmett.com/til/2016/05/20/json-output-in-jekyll.html)
* [Jekyll — Convert Full YAML Front-matter to XML/JSON](https://stackoverflow.com/questions/16889512/jekyll-convert-full-yaml-front-matter-to-xml-json)
* [Inlining JSON in a Jekyll Liquid Template](https://mrcoles.com/inlining-json-jekyll-liquid-template/)
* [Jekyll JSON API](https://www.techiediaries.com/how-to-use-jekyll-like-a-pro-output-data-as-json/)
* [JSON Feed Viewer](https://json-feed-viewer.herokuapp.com/feed/?url=https%3A%2F%2Fndarville.com%2Ffeed.json)

### API Evangelist 

* [WHAT IS OPENAPI?](https://kinlane.github.io/what-is-openapi/) - OpenAPI is a YAML / JSON specification for describing the surface area of web APIs.
* [Simple APIs With Jekyll and Github With Data Managed via Google Spreadsheets](https://dzone.com/articles/simple-apis-with-jekyll-and-github-with-data-manag)
* [Providing YAML driven XML, JSON, and Atom using Jekyll And Github](https://apievangelist.com/2016/09/19/providing-yaml-driven-xml-json-and-atom-using-jekyll-and-github/)
* [Google Spreadsheet To YAML On Jekyll](http://kinlane.com/2016/10/11/google-spreadsheet-to-yaml-on-jekyll/)
* [Using Github Repos And Jekyll As A Data Store](http://kinlane.com/2016/08/15/using-github-repos-and-jekyll-as-a-data-store/)
* [My Github Micro Tool Base](https://kinlane.github.io/github-micro-tool/)
* [OpenApi Toolbox Api Evangelist - Docs](http://openapi.toolbox.apievangelist.com/documentation/)
* [kinlane/OpenAPI-Specification](https://github.com/kinlane/OpenAPI-Specification)

### Automation

You can use GitHub actions or other CI to build your site automatically when you push to the repository and\or on a schedule. There are many other possibilities for creating content automatically based on web-events, and using staticman for forms that do more than just comments.

* [Alternatives to Heroku](https://alternativeto.net/software/heroku/?license=free)
* [benbalter/jekyllbot](https://github.com/benbalter/jekyllbot) - Listens for GitHub post-recieve service hooks messages, runs jekyll, and pushes the results back to GitHub. 
* [automate-github-pages-ifttt-glitch.html](https://webrender.net/2017/11/23/automate-github-pages-ifttt-glitch.html)
* [GH Pages Actions](https://michaelcurrin.github.io/code-cookbook/recipes/ci-cd/github-actions/workflows/jekyll/gh-pages-actions.html)
* [Huginn](https://github.com/huginn/huginn) - Create agents that monitor and act on your behalf. Your agents are standing by!
* [Staticman](https://staticman.net/)
* [eduardoboucas/staticman](https://github.com/eduardoboucas/staticman)

## Indieweb

This is beyond the scope of a GitHub pages post, but I can't help but adding a few links to indieweb. If you are publishing a personal blog, independent from an enterprise, then you are part of the indieweb.

<a href="https://web-work.tools/indieweb/" class="btn btn-success">web-work.tools/indieweb/</a>

* [indieweb.org](https://indieweb.org)
* [Micropub](https://indieweb.org/Micropub)
* [IndieAuth](https://indieweb.org/IndieAuth)
* [miklb/jekyll-indieweb](https://github.com/miklb/jekyll-indieweb)
* [Static Site Generators & the IndieWeb](https://www.growdigital.org/posts/static-site-generators-the-indieweb/)
* [Jekyll and the Indieweb](http://wordius.com/jekyll-and-the-indieweb/)
* [Implementing the Indieweb on a static website](https://vincentp.me/articles/2018/11/14/20-00/) - Sending and receiving Webmentions and Micropub on a static site
* [voxpelli/webpage-micropub-to-github/](https://github.com/voxpelli/webpage-micropub-to-github/)

</div>