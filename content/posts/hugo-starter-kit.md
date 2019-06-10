---
type: post
title: "Hugo Starter Kit"
description: "Resources for Publishing with Hugo via Git-Hub/Lab Pages."
tags: [resources, hugo, static site generators, webpub]
image:
  feature: /images/hugo-starter-kit.png
date: 2019-06-06
summary: "I've begun organizing resources around using the Hugo Static Site Generator. Official Resources, Tutorials, Themes, Sortcodes and More!"
aliases:
  - /posts/hugo-starter-kit/
  - /hugo-starter-kit/
slug: /hugo-starter-kit/
---


![](https://webwork.tools/images/hugo-starter-kit.png)

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

* https://zwbetz.com/tags/hugo/ 
* https://willschenk.com/tags/hugo/ 
* [https://regisphilibert.com/tags/hugo/](https://regisphilibert.com/tags/hugo/)
* [Hugo Static Site Tutorials](https://kodify.net/hugo-static-site-tutorials/)
* https://discourse.gohugo.io/t/undocumented-asset-pipelines-starter-kits-and-boilerplates/8423

![](https://imgur.com/udN9Kcs.png)

* [Hugo Video Turorials](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpOnyRlyS-liKL5ReHDcj4G3)
  >This course covers the basics of using Hugo - Static Site Generator. Work your way through the videos and we'll teach you everything you need to know to create a professional and scalable website or blog!

## Hugo Shortcodes

* https://gohugo.io/content-management/shortcodes/
* https://github.com/parsiya/Hugo-Shortcodes
* https://geekthis.net/post/hugo-shortcode-pack/ <-has pdf support via third party.

## Themes

* [github.com/search?q=hugo+theme](https://github.com/search?q=hugo+theme)
* [themes.gohugo.io](https://themes.gohugo.io/)
* [Migrating From Jekyll HPSTR theme to Hugo HPSTR theme](https://webwork.tools/migrate-jekyll-hpstr-hugo/)

### Academic

If you are somewhat familiar with Jekyll already, you may want to jumping right in with Academic Pages. It's not exactly simple, but its versatile.

![](https://imgur.com/JpASy3c.png)

I tried [github.com/search?q=hugo+theme](https://github.com/search?q=hugo+theme), and found that Academic has a toooon of stars. More even than the repository for all of hugos themes in one place !!!

![](https://imgur.com/25btYyt.png)

There is a one click fork\deploy with GitHub\GitLab Pages and Netlify.

Seriously just click a button, it creates the repo and publishes it for you. 

* https://sourcethemes.com/academic/docs/install/
* [Writing content with Markdown, LaTeX, and Shortcodes](https://sourcethemes.com/academic/docs/writing-markdown-latex/)
* [Getting Started With the Page Builder](https://sourcethemes.com/academic/docs/page-builder/) - Learn Academic's widget system.
* https://lmyint.github.io/post/hugo-academic-tips/
* [Display Jupyter Notebooks with Academic](https://sourcethemes.com/academic/docs/jupyter/)
* [Creating a Course or Documentation](https://sourcethemes.com/academic/docs/managing-content/#create-a-course-or-documentation)

### Learn

![](https://imgur.com/mZfWUqyl.png)

Another documentation theme, I think a bit simpler than Academic.

* https://github.com/matcornic/hugo-theme-learn
  * https://learn.netlify.com/en/



## Related Posts

All this started a few months ago when I began creating an [awesome list](https://github.com/DIDecentralized) on github, then got into publishing via GitHub Pages.

* [GitHub Pages Starter Pack](https://webwork.tools/github-pages-starter-pack/)
* [GitHub Pages Extended Resources](https://webwork.tools/github-pages-extended-resources/)
* [Static Site Generators](https://webwork.tools/static-site-generators) (just a start)
* [Migrating From Jekyll HPSTR theme to Hugo HPSTR theme](https://webwork.tools/migrate-jekyll-hpstr-hugo/)
* [Command Line - Git - SSH - BASH](https://webwork.tools/command-line-git-ssh/)
