---
layout: post
title: Migrating from Jekyll HPSTR to Hugo
description: Everything you need to know, from Jekyll-HPSTR to HPSTR-Hugo
tags: [hpstr, jekyll, hugo, theme, migration]
date: 2019-06-01
redirect_from:
  - /migrate-jekyll-hpstr-hugo
  - /migrate-jekyll-hpstr-hugo/
  - /from-jekyll-hpstr-to-hugo
permalink: /from-jekyll-hpstr-to-hugo/

image:
  thumb: /images/jekyll-hpstr-hugo.png
  feature: jekyll-hpstr-hugo.png
---


I've tried to learn Hugo a few different ways, and finally found one that works for me, and I hope will work well for anyone.

This guide and the accompanying repository should help anyone switching from either Jekyll to Hugo, *or* Hugo to Jekyll.

I've got two branches of the same exact website except one is run by [Jekyll](https://github.com/webwork-tools/webwork-tools.github.io/tree/hpstr-jekyll) and one is run by [Hugo](https://github.com/webwork-tools/webwork-tools.github.io/tree/test-hugo)!!

That's pretty neat, if you ask me!

I also show examples of the differences between the two, where and how I made changes.

## Why

1. `mmistakes/hpstr-jekyll-theme` is archived, and you can no longer submit issues or pull-requests.
2. Hugo has a lot of support from the development community, and is growing quickly in features and popularity.
3. It can be really hard finding working jekyll themes.
4. There are a lot of awesome Hugo themes that generally seem to be operational.
5. I know of some indieweb themes.
6. `/themes/` directory allows for easy testing and switching between new themes.

## HPSTR Jekyll vs Hugo 

I'm looking through different releases of Hugo to see which will run HPSTR, since its an old theme and won't run in the newest version. If you have a newer suggestion, feel free to shout out. I will also find out what the options are.

### Releases

* [mmistakes/hpstr-jekyll-theme](https://github.com/mmistakes/hpstr-jekyll-theme)
* [dldx/hpstr-hugo-theme](https://github.com/dldx/hpstr-hugo-theme/releases)


It turns out that each version was released at the same time, and that they were built together from the very beginning!

The nice thing about `hpstr-hugo-theme` is that its not archived, and if you want to open any [issues](https://github.com/dldx/hpstr-hugo-theme/issues) or [pull-requests](https://github.com/dldx/hpstr-hugo-theme/pulls), that can be done. 

Interestingly, but nice to see, there are currently 0 open pull request or issues in the themes repository.

[![](https://imgur.com/jNTAlGt.png)](https://github.com/mmistakes/hpstr-jekyll-theme/releases)
[![](https://imgur.com/dvapj4y.png)](https://github.com/dldx/hpstr-hugo-theme/releases)


### Root Directories

![](https://imgur.com/obcGfNc.png)
![](https://imgur.com/KZQODtU.png)


## Using different versions of Hugo:

* [Netlify Plus Hugo .20 and beyond](https://www.netlify.com/blog/2017/04/11/netlify-plus-hugo-0.20-and-beyond/)
  >Until yesterday, if you wanted to use a new version of Hugo on Netlify, you had two options. The first one was to wait for us to install it on our build servers and work around name collisions. Although it was not complicated, you can see by reading this blog post, it’s not very sustainable. The second option was to add the version of the Hugo binary you wanted to use to your repository. Since Hugo is a static binary, this is a very convenient solution if you want to manage it yourself.
  >
  >Starting today, if you want to use a specific new version of Hugo on Netlify, you only need to set the environment variable HUGO_VERSION with the version number you want to use. If it’s a valid release number, we’ll install it for you and use that version. You don’t have to wait for us, or manage binaries yourself. For example, if you want to use Hugo 0.20 right now, you can go to your site’s settings (Build and Deploy, Build Environment Variables section) and set HUGO_VERSION to 0.20 in your environment.

Basically, if you use netlify it will build with whatever version you tell it to. Otherwise you need to install specific versions locally. You can just drop the binary of the version you need in the root of that projects repository.

## Which Version of Hugo Should I Run?

Scrolling back through the hugo releases when the HPSTR theme was in active development, I come across:

### [0.16.0 June 6th 2016](https://github.com/gohugoio/hugo/releases?after=v0.16.0)
>Hugo 0.16 is our best and biggest release ever. The Hugo community has outdone itself with continued performance improvements, beautiful themes for all types of sites from project sites to documentation to blogs to portfolios, and increased stability.

### .deb packages for Debian, Ubuntu, etc.
>Hugo has become part of the official Debian and Ubuntu repositories since January 2016!

That's a nice note to find, since I'm an Ubuntu user. 

## [v0.17](https://github.com/gohugoio/hugo/releases/tag/v0.30) - October 2016

There are numerous options for different platforms, and this version of Hugo was released in October, one month after the final release of HPSTR.

>Hugo is going global with our 0.17 release. [...] Adding additional languages to your website is simple and straightforward.
>
>Hugo continues its trend of each release being faster than the last. 

Apparently it's fast enough that people began using hugo's webserver in production, around this time.

>New in 0.17: Available as Snap package
>
>Thanks to the contribution #2443 and guidance from @dholbach, Hugo is now available as a Snap package! (Snaps are a new kind of universal Linux packages.) Check it out at https://uappexplorer.com/app/hugo.hugo-authors
>

### [Download links for Hugo v0.17](https://github.com/gohugoio/hugo/releases/tag/v0.17)

Now that I have Hugo working, lets see how far I can go in Hugo versions.


## [v0.30.1](https://github.com/gohugoio/hugo/releases/tag/v0.30.1) - Oct 16, 2017

>Hugo 0.30 is the Race Car Edition. Hugo is already very very fast, but much wants more. So we added Fast Render Mode. It is hard to explain, so start the Hugo development server with hugo server and start editing. Live reloads just got so much faster! The "how and what" is discussed at length in other places, but the short version is that we now re-render only the parts of the site that you are working on.

This is a big release, so I'm going to look ahead for the closest bug-fixes, but avoid any feature releases.

## [v0.31.1](https://github.com/gohugoio/hugo/releases/tag/v0.31.1) -  Nov 27, 2017

So.. there's another big release after this, at the start of 2018, but I think I'll stick with this one. It's a year after HPSTR completed its development. I think we'll be good here, and I want to get to know Hugo better before changing things up too much.

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

This part, I can't figure out.

I don't understand why `.Title` is not `.title`.

I'm pretty sure I need to add 

`<meta name="twitter:site" content="{{ .site }}">`

but I didn't have success with that yet.

```
<!-- Twitter Cards -->
<meta name="twitter:title" content="{{ .Title }}">
<meta name="twitter:description" content="{{ with .Description }}{{ . }}{{ else }}{{ $.Site.Params.subtitle }}{{ end }}">
{{ with .Site.Params.owner.twitter }}<meta name="twitter:creator" content="{{ . }}">{{ end }}
{{ if isset ($.Scratch.Get "Params") "image" }}
    {{ $imageparams := index ($.Scratch.Get "Params") "image" }}
    {{ with $imageparams.thumb }}
        <meta name="twitter:card" content="summary">
        <meta name="twitter:image" content="{{ . | absURL }}">
    {{ else }}
        <meta name="twitter:card" content="summary_large_image">
        <meta name="twitter:image" content="{{ $imageparams.feature | absURL }}">
    {{ end }}
{{ end }}
```

I also added these lines to my config.toml

```

[twitter]
  card = "summary_image_large"
  site = "@infominer33"
  title =  "web-work.tools: Independent Web-Work and Skyscraper Publishing."
  description = "Resources for Independent Webworkers: Web-Publishing, SEO, Static Site Generators, Ubuntu, Research Driven Content."
  image = "/images/web-work-tools.png"
```

I think some of those are supurfulous but it doesn't matter if I use extra, as long as I get all the right values in.

![](https://imgur.com/e6egggQ.png)


## Test Branches

I've switched over to the Indieweb Hugo Theme, Indigo, a testament to how easy it is, here on Hugo.
* https://github.com/webwork-tools/webwork-tools.github.io/tree/test-hugo
* https://github.com/webwork-tools/webwork-tools.github.io/tree/hpster-jekyll
* [AngeloStravrow/indigo](https://github.com/AngeloStavrow/indigo)


## Resources

* https://sourcethemes.com/academic/docs/migrate-from-jekyll/
* [web.archive.org - Installing Hugo - Dec, 2017](http://web.archive.org/web/20171209165059/http://gohugo.io/getting-started/installing)
* [web.archive.org - Using Hugo - Dec,2017](http://web.archive.org/web/20171211175036/http://gohugo.io/getting-started/usage)
* [Creating a Test Branch and Merging changes back to Master](https://web-work.tools/posts/branches-git/)
* [Goodbye Jekyll - Hello Hugo](https://www.jvt.me/posts/2019/01/04/goodbye-jekyll-hello-hugo/)

## Other Hugo Themes

* https://github.com/EmielH/tale-hugo

## Over the Rainbow
* [Blogging with Org-Mode and Hugo](http://masayk.github.io/tech/hugo/)

## Related Posts

* [Learn HTML CSS and Associated Markup Languages](https://web-work.tools/learn-html-css/)
* [Content Creation](https://web-work.tools/content-creation/)
* [GitHub Pages Extended Resources](https://web-work.tools/github-pages-extended-resources/)
* [Static Site Generators](https://web-work.tools/static-site-generators/)
* [Migrating from Jekyll HPSTR to Hugo HPSTR theme](https://web-work.tools/migrate-jekyll-hpstr-hugo/)
* [Command Line - Git - SSH - BASH](https://web-work.tools/command-line-git-ssh/)
