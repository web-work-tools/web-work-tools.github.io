---
layout: page-fullwidth
title: "Hugo Starter Kit"
teaser: "Tutorials, Themes, Sortcodes and More!"

categories: ['JAMStack']
tags: ['Hugo']

header: no
image:
  title: "hugo-starter-kit.png"

redirect_from:
  - /hugo-starter-kit
  - /hugo-starter-kit/
permalink: /jamstack/hugo-starter-kit/
modified: 2019-06-15T22:22:22-23:00
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


* [Interview with Bjørn Erik Pedersen, Hugo lead developer](https://www.thenewdynamic.org/article/2017-10-03-interview-hugo-lead-developer/)

## Official Resources

* [Quickstart](https://gohugo.io/getting-started/quick-start/)
* [GoHugo](https://gohugo.io)
* [Documentation](https://gohugo.io/documentation/)
* [Forum](https://discourse.gohugo.io)
* https://gohugo.io/tools/starter-kits/
* [Golang](https://golang.org/) - the language HUGO is built with
  * [Golang Templates](https://golang.org/pkg/text/template/)
* [Configure](https://gohugo.io/getting-started/configuration/) - all the cool config.toml settings you never knew!
* [Syntax Highlighting](https://gohugo.io/content-management/syntax-highlighting/)
* [Page Bundles](https://gohugo.io/content-management/page-bundles/)
* [Permalink Configuration Values:](https://gohugo.io/content-management/urls/#permalink-configuration-values)

```
[Permalinks]
  # | :year        | the 4-digit year                           |
  # | :month       | the 2-digit month                          |
  # | :monthname   | the name of the month                      |
  # | :day         | the 2-digit day                            |
  # | :weekday     | the 1-digit day of the week (Sunday = 0)   |
  # | :weekdayname | the name of the day of the week            |
  # | :yearday     | the 1- to 3-digit day of the year          |
  # | :section     | the content's section                      |
  # | :sections    | the content's sections hierarchy           |
  # | :title       | the content's title                        |
  # | :slug        | the content's slug (or title, if no slug)  |
  # | :filename    | the content's filename (without extension) |

  # Examples
  posts = "/:filename/"
  # post = "/:year/:month/:title/"
  notes = "/notes/:filename/"
```

## Publishing Websites Via Hugo

* [budparr/awesome-hugo](https://github.com/budparr/awesome-hugo/)
* [Make A Hugo Blog from Scratch](https://zwbetz.com/make-a-hugo-blog-from-scratch/)
* [Hugo Asset Pipeline](https://blog.carlmjohnson.net/post/2017/hugo-asset-pipeline/)
* [Hosting Hugo on Netlify - Insanely Fast Deploys](https://www.netlify.com/blog/2015/07/30/hosting-hugo-on-netlifyinsanely-fast-deploys/)


## Using different versions of Hugo:

* [Netlify Plus Hugo .20 and beyond](https://www.netlify.com/blog/2017/04/11/netlify-plus-hugo-0.20-and-beyond/)
  >Until yesterday, if you wanted to use a new version of Hugo on Netlify, you had two options. The first one was to wait for us to install it on our build servers and work around name collisions. Although it was not complicated, you can see by reading this blog post, it’s not very sustainable. The second option was to add the version of the Hugo binary you wanted to use to your repository. Since Hugo is a static binary, this is a very convenient solution if you want to manage it yourself.
  >
  >Starting today, if you want to use a specific new version of Hugo on Netlify, you only need to set the environment variable HUGO_VERSION with the version number you want to use. If it’s a valid release number, we’ll install it for you and use that version. You don’t have to wait for us, or manage binaries yourself. For example, if you want to use Hugo 0.20 right now, you can go to your site’s settings (Build and Deploy, Build Environment Variables section) and set HUGO_VERSION to 0.20 in your environment.

Basically, if you use netlify it will build with whatever version you tell it to. Otherwise you need to install specific versions locally. You can just drop the binary of the version you need in the root of that projects repository.

### Tutorials

* [zwbetz.com - hugo](https://zwbetz.com/tags/hugo/)
* [willschenk.com - hugo](https://willschenk.com/tags/hugo/)
* [https://regisphilibert.com/tags/hugo/](https://regisphilibert.com/tags/hugo/)
* [Hugo Static Site Tutorials](https://kodify.net/hugo-static-site-tutorials/)
* [Undocumented asset pipelines, Starter-Kits and Boilerplates](https://discourse.gohugo.io/t/undocumented-asset-pipelines-starter-kits-and-boilerplates/8423)

![](https://imgur.com/udN9Kcs.png)

* [Hugo Video Turorials](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpOnyRlyS-liKL5ReHDcj4G3)
  >This course covers the basics of using Hugo - Static Site Generator. Work your way through the videos and we'll teach you everything you need to know to create a professional and scalable website or blog!

### Hugo Variables and Templating

* [Site Variables](https://gohugo.io/variables/site/)
* [Page Variables](https://gohugo.io/variables/page/)


## Internal Templates

Hugo ships with a group of boilerplate templates that cover the most common use cases for static websites.

* [The Internal Templates](https://gohugo.io/templates/internal/#the-internal-templates) 

### Twitter Cards

* [Internal Templates: Twitter Cards](https://gohugo.io/templates/internal/#configure-twitter-cards)

I guess the creators of hugo don't use twitter much... since I couldn't get interal includes to work. Or probably I am borked.. anyways.

```html
    {% raw %}
    <!-- Twitter Cards-->
    <!-- Twitter summary card with large image must be at least 280x150px -->
    <meta name="twitter:card" content="summary_large_image"/>
    <meta name="twitter:image:src" content="{{ with .Params.images }}{{ . }}{{ else }}{{ .Site.Params.images }}{{ end }}"/>
    <!-- Twitter Card data -->
    <meta name="twitter:title" content="{{ .Title }}"/>
    <meta name="twitter:description" content="{{ with .Description }}{{ . }}{{ else }}{{if .IsPage}}{{ .Summary }}{{ else }}{{ with .Site.Params.description }}{{ . }}{{ end }}{{ end }}{{ end }}"/>
    {{ with .Site.Social.twitter }}<meta name="twitter:site" content="@{{ . }}"/>{{ end }}
    {{ with .Site.Social.twitter_domain }}<meta name="twitter:domain" content="{{ . }}"/>{{ end }}
    {% endraw %}
```

I still use their params, but coocked up my own based from theirs and something I had in my head.

You can verify this works at [web-work.tools/indieweb](https://web-work.tools/indieweb):

![](https://imgur.com/CGtUwEI.png)

Now I just have to design a header image that fits with twitter dimensions, or set it up to look for an og:image, incase I use a thinner banner image.

**Params for config.toml**

```toml
[params]
  description = "Text about my cool site"
  images = ["site-feature-image.jpg"]
```

**Front Matter Post Variables**

```toml
description = "Text about this post"
images = ["post-cover.png"]
title = "Post title"
```

## Hugo Shortcodes

* [Content Management - Shortcodes](https://gohugo.io/content-management/shortcodes/)
* [parsiya/Hugo-Shortcodes](https://github.com/parsiya/Hugo-Shortcodes)
* [Hugo Shortcode Pack](https://geekthis.net/post/hugo-shortcode-pack/) <-has pdf support via third party.

## Themes

* [github.com/search?q=hugo+theme](https://github.com/search?q=hugo+theme)
* [themes.gohugo.io](https://themes.gohugo.io/)
* [Migrating From Jekyll HPSTR theme to Hugo HPSTR theme](https://web-work.tools/migrate-jekyll-hpstr-hugo/)
  * [mikeymop/minimal-mistakes-hugo/](https://github.com/mikeymop/minimal-mistakes-hugo/) - I see there is also a minimal mistakes hugo theme, so I'll have to try that sometime :)

### Academic

If you are somewhat familiar with Jekyll already, you may want to jumping right in with Academic Pages. It's not exactly simple, but its versatile.

![](https://imgur.com/JpASy3c.png)

I tried [github.com/search?q=hugo+theme](https://github.com/search?q=hugo+theme), and found that Academic has a toooon of stars. More even than the repository for all of hugos themes in one place !!!

![](https://imgur.com/25btYyt.png)

There is a one click fork\deploy with GitHub\GitLab Pages and Netlify.

Seriously just click a button, it creates the repo and publishes it for you. 

* [Academic Install](https://sourcethemes.com/academic/docs/install/)
  >You can choose from one of the following four methods to install:
    >- one-click install using your web browser (recommended)
    >- install on your computer using Git with the Command Prompt/Terminal app
    >- install on your computer by downloading the ZIP files
    >- install on your computer with RStudio
* [Writing content with Markdown, LaTeX, and Shortcodes](https://sourcethemes.com/academic/docs/writing-markdown-latex/)
* [Getting Started With the Page Builder](https://sourcethemes.com/academic/docs/page-builder/) - Learn Academic's widget system.
* [Academic Tips](https://lmyint.github.io/post/hugo-academic-tips/)
* [Display Jupyter Notebooks with Academic](https://sourcethemes.com/academic/docs/jupyter/)
* [Creating a Course or Documentation](https://sourcethemes.com/academic/docs/managing-content/#create-a-course-or-documentation)
* [Academic - Migrate From Jekyll](https://sourcethemes.com/academic/docs/migrate-from-jekyll/)

### Learn

![](https://imgur.com/mZfWUqyl.png)

Another documentation theme, I think a bit simpler than Academic.

* [matcornic/hugo-theme-learn](https://github.com/matcornic/hugo-theme-learn)
  * [learn.netlify.com](https://learn.netlify.com/en/)

## Related Posts

All this started a few months ago when I began creating an [awesome list](https://github.com/DIDecentralized) on github, then got into publishing via GitHub Pages.

* [GitHub Pages Starter Pack](https://web-work.tools/jamstack/github-pages-starter-pack//)
* [GitHub Pages Extended Resources](https://web-work.tools/github-pages-extended-resources/)
* [Static Site Generators](https://web-work.tools/static-site-generators) (just a start)
* [Migrating From Jekyll HPSTR theme to Hugo HPSTR theme](https://web-work.tools/migrate-jekyll-hpstr-hugo/)
* [Command Line - Git - SSH - BASH](https://web-work.tools/command-line-git-ssh/)

</div>