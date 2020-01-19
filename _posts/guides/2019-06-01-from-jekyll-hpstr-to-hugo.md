---
layout: page-fullwidth
title: "Migrating from Jekyll HPSTR to Hugo"

categories: ['jamstack', 'guides']
tags: ['ssg', 'jekyll', 'hugo', 'github pages']

header: no
image:
  title: "hpstr-hugo-migration.jpg"
  caption: "Everything you need to know, from Jekyll-HPSTR to HPSTR-Hugo"
  thumb: "jekyll-hpstr-hugo.png"

permalink: /jamstack/jekyll-hpstr-hugo-theme/
modified: 2019-11-17T22:22:22-23:00
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

Originally I used the [Jekyll Theme HPSTR](https://github.com/mmistakes/jekyll-theme-hpstr) for this site. I was also trying to learn Hugo, and found there was a [HPSTR Hugo theme](https://themes.gohugo.io/hpstr-hugo-theme/).

I made this guide for switching between them, as a part of my learning experience.

Ideally, this guide and the accompanying repository should help anyone switching from either Jekyll to Hugo, *or* Hugo to Jekyll.

Eventually, I switched back to the Jekyll theme, and now I'm stretching my experience further, with [Feeling Responsive](https://phlow.github.io/feeling-responsive/), which has an ideal UI for the content I create.

I have branches of both the hugo and the jekyll version of this sites old theme, which you can view on github, or even clone and run locally.

* [HPSTR Jekyll Branch](https://github.com/web-work-tools/web-work-tools.github.io/tree/hpstr-jekyll) 
* [HPSTR Hugo Branch](https://github.com/web-work-tools/web-work-tools.github.io/tree/test-hugo)!!


## HPSTR Jekyll vs Hugo 

First, I found which version of hugo it was built for, since its an old theme and won't run in the newest version. 

## Using different versions of Hugo:

* [Netlify Plus Hugo .20 and beyond](https://www.netlify.com/blog/2017/04/11/netlify-plus-hugo-0.20-and-beyond/)
  >Until yesterday, if you wanted to use a new version of Hugo on Netlify, you had two options. The first one was to wait for us to install it on our build servers and work around name collisions. Although it was not complicated, you can see by reading this blog post, it’s not very sustainable. The second option was to add the version of the Hugo binary you wanted to use to your repository. Since Hugo is a static binary, this is a very convenient solution if you want to manage it yourself.
  >
  >Starting today, if you want to use a specific new version of Hugo on Netlify, you only need to set the environment variable HUGO_VERSION with the version number you want to use. If it’s a valid release number, we’ll install it for you and use that version. You don’t have to wait for us, or manage binaries yourself. For example, if you want to use Hugo 0.20 right now, you can go to your site’s settings (Build and Deploy, Build Environment Variables section) and set HUGO_VERSION to 0.20 in your environment.

Basically, if you use netlify it will build with whatever version you tell it to. Otherwise you need to install specific versions locally. You can just drop the binary of the version you need in the root of that projects repository.

### Releases

* [mmistakes/hpstr-jekyll-theme](https://github.com/mmistakes/hpstr-jekyll-theme/releases)
* [dldx/hpstr-hugo-theme](https://github.com/dldx/hpstr-hugo-theme/releases)

It turns out that each version was released at the same time, and that they were built together from the very beginning! The final release was Sep 14, 2016. So I want a version of Hugo not too much newer then that.

## [v0.31.1](https://github.com/gohugoio/hugo/releases/tag/v0.31.1) -  Nov 27, 2017

I tested the theme on this version and it worked well, you may find a newer release will work, but I wouldn't bother, since any new features could break the theme. It's a year after HPSTR completed its development. I think we'll be good here, and I want to get to know Hugo better before changing things up too much.

The next major change introduces page bundles. I wouldn't be surprised if it has a problem with this theme.

## Test Install

* [web.archive.org - Installing Hugo - Dec, 2017](http://web.archive.org/web/20171209165059/http://gohugo.io/getting-started/installing)

Once it's installed, type I `hugo version` and read:

![](https://imgur.com/J2lnKkR.png)

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
title = "web-work.tools"
url = "/web-work.tools/"

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
title = "InfoMine"
url = "http://infominer.xyz/"
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
  feature: abstract-3.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
---
```


## config.toml

Now we are getting places! Next step is to copy the `config.toml` from the root of our example site into the root of our repository. 


This is the final stretch, and we should be good to go 

```

baseurl = "https://web-work.tools"
languageCode = "en-gb"
title = "web-work.tools: Independent Web-Work and Skyscraper Publishing."
theme = "hpstr"
pluralizelisttitles = false
PygmentsCodeFences = true
Paginate = 5
disqusShortname = "hpstrhugo"
publishdir = "docs"
enableEmoji = true
[params]
	subtitle = "Digital Tools for a Digital Transformation."
	[params.author]
		name = "⧉ Infominer"
		avatar = "/images/info-id.png"
		bio = "Full-Time Crypto-Curation and Histories ⧉ #Bitcoin #Blockchain #DecentralizedID ⧉ Research, Publishing, #WebWork #Indieweb ⧉"
		github = "webwork-tools/webwork-tools.github.io"
	[params.image]
	  feature = "/images/web-work-tools.png"



```
* [Configuring Hugo](http://web.archive.org/web/20161110120102/http://gohugo.io/overview/configuration)

>`publishdir = "docs"`

By setting this in our config.toml, we will be able to ask github pages to publish from the docs folder.

## Redirects

One thing that's important to note, if you are switching from Jekyll HPSTR to HPSTR Hugo with me. HPSTR Hugo makes all your posts live in the `/posts/` directory.

If you used to let your blog live at the root of the site, like me, then add aliases, which are how Hugo does redirects.

* [Content Manegement - Aliases](https://gohugo.io/content-management/urls/#aliases)

```
aliases:
  - /title-goes-here/
  - /other-title-too/
```

## One last thing!

It seems like you need to type `hugo` to publish to the docs directory, because `hugo server` doesn't do both, it only does the webserving.. I don't really understand, but that seems to be the case.

## Use a linebreak before each list!

## Twitter Cards

For twitter cards, I use the [minimal-mistakes - _includes/seo.html](https://github.com/mmistakes/minimal-mistakes/blob/master/_includes/seo.html) as a reference for up to date syntax, and update the code that generates it wherever I need (or simply drop it in the includes of jekyll themes).

![](https://imgur.com/e6egggQ.png)


## Test Branches

I've switched over to the Indieweb Hugo Theme, Indigo, a testament to how easy it is, here on Hugo.
* [webwork-tools.github.io/tree/test-hugo](https://github.com/webwork-tools/webwork-tools.github.io/tree/test-hugo)
* [webwork-tools.github.io/tree/hpster-jekyll](https://github.com/webwork-tools/webwork-tools.github.io/tree/hpster-jekyll)
* [AngeloStravrow/indigo](https://github.com/AngeloStavrow/indigo)


## Resources

* [web.archive.org - Installing Hugo - Dec, 2017](http://web.archive.org/web/20171209165059/http://gohugo.io/getting-started/installing)
* [web.archive.org - Using Hugo - Dec,2017](http://web.archive.org/web/20171211175036/http://gohugo.io/getting-started/usage)
* [Creating a Test Branch and Merging changes back to Master](https://web-work.tools/posts/branches-git/)
* [Goodbye Jekyll - Hello Hugo](https://www.jvt.me/posts/2019/01/04/goodbye-jekyll-hello-hugo/)

## Other Hugo Themes

* [/EmielH/tale-hugo](https://github.com/EmielH/tale-hugo)

## Over the Rainbow
* [Blogging with Org-Mode and Hugo](http://masayk.github.io/tech/hugo/)

## Related Posts

* [Hugo Starter Kit](https://web-work.tools/hugo-starter-kit/)
* [Learn HTML CSS and Associated Markup Languages](https://web-work.tools/learn-html-css/)
* [Content Creation](https://web-work.tools/content-creation/)
* [GitHub Pages Extended Resources](https://web-work.tools/github-pages-extended-resources/)
* [Static Site Generators](https://web-work.tools/static-site-generators/)
* [Command Line - Git - SSH - BASH](https://web-work.tools/command-line-git-ssh/)