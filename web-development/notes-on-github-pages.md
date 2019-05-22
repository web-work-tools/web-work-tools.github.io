---
title: GitHub Pages—Starter Pack
description: Publishing a Website via GitHub pages is free, and easy. Here's everything you need to get going, in one place.
image: "https://infominer.id/images/gh-pages-starter-pack.png"
redirect_from:
  - notes.html
  - notes-on-github-pages.html
  - research/notes-on-github-pages.html
  - web-work/gh-pages-starter-pack.html
permalink: gh-pages-starter-pack.html
---

I love github for its support of open source information exchange, free and easy web-publishing. 

As a content creator, it's super valuable to be able to publish my own web-pages. 

Github makes it easy to get started, with the click of a button, you can have a web-page live, requiring only markdown skills (that anyone can learn on the go).

Each feature you want to enable requires a little more learning, and GitHub Pages is set up so that if you decide to, you can gradually progress from content creator to web-developer. 

If you don’t want to think about web-development, and simply want your markdown files to look beautiful once published, github pages can help you do that too.


![](/images/gh-pages-starter-pack.png)

## Contents

* [Introduction](#introduction)
  * [Getting Started](#getting-started-)
  * [Besides the Theme Chooser](#besides-the-theme-chooser-)
* [Resources](#resources-)
  * [Markdown](#markdown)
  * [GitHub Pages](#github-pages-)
  * [Jekyll](#jekyll-)
  * [Themes](#themes-)
    * [Hydejack](#hydejack-)
    * [Minimal Mistakes](#minimal-mistakes)
  * [Front Matter](#front-matter-)
  * [Jekyll-SEO-Tag](#jekyll-seo-tag-)
  * [Open Graph - Favicons and More](#open-graph---favicons-and-more-)
  * [Twitter](#twitter-)
  * [Comments](#comments-)
  * [Other Customizations](#other-customizations-)
  * [Content Creation](#content-creation)
* [Advance](#advance-)
  * [HTML - CSS](#html---css-)
  * [Liquid](#liquid-)
  * [Git](#git-)
  * [SSH](#ssh-)
  * [Data](#data)


## Introduction

![](../images/gh-jekyll.png)

I'm just a newb that created this resource to help myself. 

Corrections, suggestions, tips, and links would be all appreciated.

Github pages runs Jekyll, which runs Kramdown, which is a super powerful markdown engine. Jekyll takes your repository, which contains a combination of configuration files and content, and translates it all into a proper web-page.

Github pages can be used, like, 4 different ways. It’s versitile, but can be confusing.

The simplest way to use pages is to choose one of the <a href="https://pages.github.com/themes/" target="_blank">official GitHub pages themes</a>. Just go into your repository settings:

![](https://i.imgur.com/sw4Iann.png)

All you really need to do is select a branch and it will begin publishing your repository. Then choose a method to publish. Brand-newbs go with the theme chooser.

The first web-page for a given account must be names like so: `username.github.io`. For example, the repository for my personal page is called `infominer33.github.io`.

Every other repository you own can also be made into its own web-page, that will published off of your user page. All you do is go up there and select where you want pages to build from, and you're ready to go. 

so [github.com/infominer33/DIDecentralized](https://github.com/infominer33/DIDecentralized) is published at [infominer.id/DIDecentralized](https://infominer.id/DIDecentralized), because I have a custom domain. Otherwise it would be found at, [infominer33.github.io/DIDecentralized](https://infominer.id/DIDecentralized).

## Getting Started [**^**](#contents)

If you used the theme chooser, all you need to do is edit README.md, and your web-page is re-built from the contents of your GitHub repository every few minutes.

**Create an index.md**

Although pages will build an index.html from your readme.md, pages will not behave as expected if you try to do any configuration or additional optimization with only readme.md.

in that index.md you need to include front matter:

```
---
layout: default
---
```

*\*afaikt - isn't always necessary, but doesn't hurt, and at least one theme wouldn't build without some proper front matter.


## Besides the Theme Chooser [**^**](#contents)

There are other ways that pages can work too. You should be able to run any theme that is set up to support remote themes. However, you have to pay attention to the themes and find ones that are in active development.

You can also run any Gem based theme from your page too. Basically Gem files are packages that contain all of the files necessary for building your site, and keep your repository directory un-cluttered. Then, if you want to change a file that's in the gem, you just create the directory and pur the file where it goes, and configure as you wish. 

I'm still a bit confused about that part, but gems do help you build pages locally to test features before deploying them....

>Q: How can I get started with gem-packaged themes? / Do I need to package my theme into a gem?
>
>Gem-packaged themes are just an advanced option and in addition they are in development for (real world) experiments (e.g. think v0.1 as stated by the Ben Balter - the lead designer / manager / dev at GitHub).
>
>Thus, to conclude do NOT read too much into the official themes docs e.g. as the only or "right" way to design a theme. Just (continue to) use "classic" themes - there are hundreds to learn from and once you have mastered "classic" themes you can "graduate" to the master class, that is, using gem-packaged themes.
-[github.com/planetjekyll/awesome-jekyll-themes](https://github.com/planetjekyll/awesome-jekyll-themes)

I understand what they're saying, but I feel kind of the opposite. I got used to pages, first with the theme chooser, then with gem-based (offering more configurability, but keeping configuration files I don't need or understand out of sight untill needed.) Then again, I didn't really understand my options when I started.

These classic themes are just files and folders, everything where you can see it. I don't know if that's what I would have chosen when I first started.. but it's definitely what I need now. 

According to planetjekyll, these are all "classic" themes: [https://drjekyllthemes.github.io](https://drjekyllthemes.github.io)

## Resources [**^**](#contents)


### Markdown

* <a href="https://guides.github.com/features/mastering-markdown/" target="_blank">Mastering Markdown</a>
* <a href="https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet" target="_blank">Markdown Cheet-Sheet</a>


### Github Pages [**^**](#contents)

* [Github Pages Community Forum](https://github.community/t5/GitHub-Pages/bd-p/pages)
* [Configuring a Publishing Source for GitHub Pages](https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages)
* [help.github.com - User, Organization, and Project Pages](https://help.github.com/en/articles/user-organization-and-project-pages)
* <a href="http://ragupappu.com/2015/04/22/setup-website-using-github-pages-and-jekyll/" target="_blank">http://ragupappu.com/2015/04/22/setup-website-using-github-pages-and-jekyll/</a>
* <a href="https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-3-Local-development-with/ba-p/2292" target="_blank">Getting started with GitHub Pages: Part 3 -- Local development with GitHub Pages</a>
* <a href="https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-4-Customizing-your-Pages/ba-p/4058" target="_blank">Getting started with GitHub Pages: Part 4 -- Customizing your Pages site</a>
* <a href="https://help.github.com/en/articles/adding-jekyll-plugins-to-a-github-pages-site" target="_blank">Adding Jekyll Plugins to a GitHub Pages Site - help.github.com</a>
* <a href="https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll" target="_blank">Setting up You GitHub Pages Site Locally with Jekyll</a>
* <a href="https://github.community/t5/GitHub-Pages/bd-p/pages" target="_blank">GitHub Pages —github.community</a>
* <a href="https://pages.github.com/versions/" target="_blank">https://pages.github.com/versions/</a>
* <a href="https://help.github.com/en/articles/creating-a-custom-404-page-for-your-github-pages-site" target="_blank">Creating Custom 404 page</a>
* <a href="https://help.github.com/en/articles/redirects-on-github-pages" target="_blank">Jekyll Redirect Plugin</a>
* [Clearing Up Confusion around Baseurl](https://byparker.com/blog/2014/clearing-up-confusion-around-baseurl/)




### Jekyll [**^**](#contents)

* <a href="https://github.com/planetjekyll" target="_blank">planetjekyll</a>
  * <a href="https://github.com/planetjekyll/awesome-jekyll" target="_blank">planetjekyll/awesome-jekyll</a>
  * <a href="https://github.com/planetjekyll/awesome-jekyll-plugins" target="_blank">planetjekyll/awesome-jekyll-plugins</a>
* <a href="https://devhints.io/jekyll" target="_blank">Jekyll - Cheat Sheet</a>
* [Jekyll Community Forum](http://talk.jekyllrb.com/)
* <a href="https://github.com/jekyll/jekyll/blob/master/README.markdown" target="_blank">/jekyll/jekyll/blob/master/README.markdown</a>
* <a href="https://jekyllrb.com/docs/plugins/installation/" target="_blank">jekyllrb.com/docs/plugins/installation/</a>
* <a href="https://jekyllrb.com/docs/pagination/" target="_blank">Jekyll - Pagination Docs</a>
* <a href="https://jekyllrb.com/tutorials/navigation/" target="_blank">Jekyll - Navigation Tutorial</a>


### Themes [**^**](#contents)

I'll say now, if you are new to web-development, best to start off trying out a few of the Github Pages official themes. Once installed, I cloned those repos locally so its easier to see how everything works. Then, if I want to configure a file that's not in my repository, I have a copy nearby. You can grab the `_layouts/default.html`, put it in your repo, and get a feel for how configuring that template shapes your entire site. But then you configure individual pages, and categories, perhaphs, to display differently. 

* <a href="https://pages.github.com/themes/" target="_blank">pages.github.com/themes/</a> - official 
* [drjekyllthemes.github.io](https://drjekyllthemes.github.io) (classic 'files and folders')
* <a href="https://github.com/planetjekyll/awesome-jekyll-themes" target="_blank">planetjekyll/awesome-jekyll-themes</a> (gem-based)
* <a href="https://github.blog/2017-11-29-use-any-theme-with-github-pages/" target="_blank">github.blog/2017-11-29-use-any-theme-with-github-pages/</a> -Howto Remote themes.
* [http://themes.jekyllrc.org/](http://themes.jekyllrc.org/)
* [ChristopherA/simplest-github-page](https://github.com/ChristopherA/simplest-github-page)
* [ChristopherA/jekyll-remote_theme-test](https://github.com/ChristopherA/jekyll-remote_theme-test) - a working example of a remote theme.
* [projectpages.github.io/project-pages/](https://projectpages.github.io/project-pages/)
* [prose/starter](https://github.com/prose/starter)
* [forked.yannick.io](http://forked.yannick.io) - Find maintained forks of your favorite GitHub repos.


#### Hydejack [**^**](#contents)

![](https://imgur.com/UvYd77Dl.png)

* <a href="https://github.com/qwtel/hydejack/" target="_blank">/qwtel/hydejack/</a>
* [/qwtel/hydejack-starter-kit](https://github.com/qwtel/hydejack-starter-kit)
* <a href="https://hydejack.com/docs/print/" target="_blank">Hydejack Print Documentation</a>
* <a href="http://nickengmann.com/Documentation.pdf" target="_blank">Hydejack Documentation.pdf</a>
* <a href="https://github.com/qwtel/hydejack/blob/master/docs/advanced.md" target="_blank">Hydejack Advanced</a>


If you don't want to think too much about web-development, try [Hydejack](https://hydejack.com). It's build with everything you need to create a beatiful responsive web-page, with plenty of options and configurations supported. It's a free version of a more robust commercial option. But it's easy to set up, and works great. That's what this page is running atm. 

The only problem is that it has some proprietary code. So it's not 100% customizable. Then again, that keeps you from getting in and screwing things up. 

#### Minimal Mistakes  [**^**](#contents)
![](https://i.imgur.com/Ua8hFx8.png)

I had a problem getting this one to work the first time I tried, and probably wouldn't have bothered w hydejack if I had. It's the most popular pages theme for a reason. However, there will be more of a learning curve to fully configure it, compared with hydejack.

I've just installed minimal mistakes in the SourceCrypto, and am going to learn to master that one. In the meantime, hydejack is *Mobile First*, and the most beautiful -out of box- theme that I've found.

It can be a pain trying to figure out themes, especially if you don't clean out all old files before trying a new theme. Which happened to me, and added to a lot of frustration that I could not understand.


### Front Matter [**^**](#contents)

* <a href="https://jekyllrb.com/docs/front-matter/" target="_blank">Front Matter</a>
* <a href="http://simpleprimate.com/blog/front-matter" target="_blank">YAML front matter in Jekyll</a>
* <a href="https://idratherbewriting.com/documentation-theme-jekyll/mydoc_yaml_tutorial" target="_blank">YAML tutorial in the context of Jekyll</a>


### Jekyll-SEO-Tag [**^**](#contents)

* <a href="https://help.github.com/en/articles/search-engine-optimization-for-github-pages" target="_blank">Search Engine Optimization for Github Pages - help.github.com</a>
* <a href="https://github.com/jekyll/jekyll-seo-tag" target="_blank">/jekyll/jekyll-seo-tag</a>
* <a href="https://github.com/pmarsceill/jekyll-seo-gem" target="_blank">/pmarsceill/jekyll-seo-gem</a>
* <a href="https://github.com/meedan/meedan.code/commit/a9ad6e794fffd35035aa7e5bfb1200a34fe0e479" target="_blank">Override default jekyll-seo-tag template</a>
* <a href="https://blog.webjeda.com/optimize-jekyll-seo/" target="_blank">Tips to Optimize Jekyll SEO</a>
* [blog.webjeda.com/optimize-jekyll-seo/#6-open-graph-and-twitter-cards-in-jekyll](https://blog.webjeda.com/optimize-jekyll-seo/#6-open-graph-and-twitter-cards-in-jekyll)


### Open Graph - Favicons and More [**^**](#contents)

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

### Twitter [**^**](#contents)

* <a href="https://cards-dev.twitter.com/validator" target="_blank">Twitter Card Validator</a>
* <a href="https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards" target="_blank">About Cards - developer.twitter.com</a>
* [https://github.com/jekyll/jekyll-mentions/](https://github.com/jekyll/jekyll-mentions/)

### Comments [**^**](#contents)
* [Github Issues for Blog Comments](http://artsy.github.io/blog/2017/07/15/Comments-are-on/)
* [A repo you can use to work-around GH issue comment request limmits.](https://github.com/orta/gh-commentify)
* [Various ways you can add comments to your static site](https://darekkay.com/blog/static-site-comments/)
* [Add comments to your jekyll powered blog](https://github.com/damieng/jekyll-blog-comments)
* [Setting up Staticman Server](https://www.flyinggrizzly.net/2017/12/setting-up-staticman-server/)

### Other Customizations [**^**](#contents)

* [Adding Custom Google Search](https://digitaldrummerj.me/blogging-on-github-part-7-adding-a-custom-google-search/)
* [digitaldrummerj.me/categories/jekyll](https://digitaldrummerj.me/categories/jekyll/)
* [Social Media Share Bar](https://mycyberuniverse.com/social-media-share-bar-jekyll-blog-website.html)
* [Validating Links and Images](https://digitaldrummerj.me/jekyll-validating-links-and-images/)
* [Jekyll-Target-Blank](https://keith-mifsud.me/projects/jekyll-target-blank)
* [https://github.com/jekyll/jekyll-mentions/](https://github.com/jekyll/jekyll-mentions/)
* [Github Flavored Emoji for Jekyll](https://github.com/jekyll/jemoji)
* [longqian.me/](http://longqian.me/) -Metamask Donation Button.
* <a href="https://superdevresources.com/share-buttons-jekyll/" target="_blank">https://superdevresources.com/share-buttons-jekyll/</a>
* [How to Create an Open-Source Directory on GitHub Pages](https://webdesign.tutsplus.com/tutorials/how-to-create-an-open-source-directory-on-github-pages--cms-26225)
* [Embed files from a github repository onto your page.](http://gist-it.appspot.com/)
* [idleberg/Creative-Commons-Markdown](https://github.com/idleberg/Creative-Commons-Markdown)
* [Redirecting GitHub Pages after a repository move](https://gist.github.com/domenic/1f286d415559b56d725bee51a62c24a7)
* [gjtorikian/html-proofer](https://github.com/gjtorikian/html-proofer) - you got broken links bruh
* [Elasticsearch for Jekyll](https://blog.omc.io/elasticsearch-for-jekyll-part-1-ab456ac7c093)
* [hacking-routing-component-jekyll/](https://www.sitepoint.com/hacking-routing-component-jekyll/)


### Content Creation [**^**](#contents)

Here's some tools to make content creation a little easier.

* [nacyot/awesome-opensource-documents](https://github.com/nacyot/awesome-opensource-documents)
* [neutraltone/awesome-stock-resources](https://github.com/neutraltone/awesome-stock-resources)
* [shime/creative-commons-media](https://github.com/shime/creative-commons-media)
* [Canva Infographic Creator](https://www.canva.com/create/infographics/)
* [easel.ly](http://www.easel.ly/) - free create infographics
* [Amara](http://amara.org/en/) - create captions for YouTube videos.
* [Content Strategy Tool](https://builtvisible.com/content-strategy-helper/) - Find inspiration for your content marketing topics 
* [Copyscape](http://www.copyscape.com/) - track if your content is being plagiarized.
* [Google Public Data](http://www.google.com/publicdata/directory) - content research, infographics, and more.
* [Google SERP Snippet Optimization Tool](http://www.seomofo.com/snippet-optimizer.html) - see how your snippet may appear in search results. 
* [infogr.am](https://infogr.am/) - create infographics and data visualizations
* [Text Cleaner](http://www.textcleanr.com/) - cleans up all kinds of text formatting when copying and pasting between applications.
* [wordle](http://www.wordle.net/) - word cloud generator
* [Yahoo Pipes](http://pipes.yahoo.com/pipes/)
combines feeds "into content and other magical creations". 
* [Piktochart](http://piktochart.com/) - visualization generator.
* [Wistia](http://wistia.com/) - SEO-friendly video hosting. 
* [https://www.pcjs.org](https://www.pcjs.org)
* [https://www341.lunapic.com/editor/](https://www341.lunapic.com/editor/)
* [What You Can Do With Gists on Github?](https://www.labnol.org/internet/github-gist-tutorial/28499/)
* [https://polyglot.untra.io/](https://polyglot.untra.io/)


## Advance [**^**](#contents)

### HTML - CSS [**^**](#contents)

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

### Kramdown [**^**](#contents)

* <a href="https://kramdown.gettalong.org/" target="_blank">kramdown.gettalong.org</a>
* [Kramdown - Syntax](https://kramdown.gettalong.org/syntax.html)



### Liquid [**^**](#contents)

<img src="https://i.imgur.com/jMtd9WR.png"/>

* <a href="https://simpleit.rocks/ruby/jekyll/templates/jekyll-variables-and-liquid-template-tags-cheatsheet/" target="_blank">Jekyll Variables and Liquid Template Tags-Cheatsheet</a>
* <a href="https://learn.cloudcannon.com/jekyll/introduction-to-liquid/" target="_blank">Introduction to Liquid for Jekyll</a>
* <a href="https://blog.webjeda.com/jekyll-liquid/" target="_blank">https://blog.webjeda.com/jekyll-liquid/</a>

### Git [**^**](#contents)

* <a href="https://gist.github.com/davfre/8313299" target="_blank">davfre/git_cheat-sheet.md</a>
* <a href="https://education.github.com/git-cheat-sheet-education.pdf" target="_blank">education.github.com - GIT CHEAT SHEET</a>
* <a href="https://chris.beams.io/posts/git-commit/" target="_blank">Writing Effective Commits</a>
* [www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
* [Git CheetSheet](https://github.com/jonathancross/jc-docs/blob/master/Git-CheatSheet.md)
* [Working with Remotes](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes)
* [managing-commit-signature-verification](https://help.github.com/en/articles/managing-commit-signature-verification)
* [mnyrop/swc-materials/blob/master/git.md](https://github.com/mnyrop/swc-materials/blob/master/git.md)

### SSH [**^**](#contents)

* <a href="https://help.github.com/en/articles/connecting-to-github-with-ssh" target="_blank">Connecting to GitHub with SSH</a>
* <a href="https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent" target="_blank">Generating a new SSH key and adding it to the SSH agent</a>
* <a href="https://help.github.com/en/enterprise/2.15/user/articles/adding-a-new-ssh-key-to-your-github-account" target="_blank">Adding a new SSH key to your GitHub Account</a>
* <a href="https://medium.freecodecamp.org/manage-multiple-github-accounts-the-ssh-way-2dadc30ccaca" target="_blank">How to manage multiple GitHub accounts on a single machine with SSH keys</a>

## Data [**^**](#contents)

* [jekyllrb.com/docs/datafiles/](https://jekyllrb.com/docs/datafiles/)
* [providing-yaml-driven-xml-json-and-atom-using-jekyll-and-github](https://apievangelist.com/2016/09/19/providing-yaml-driven-xml-json-and-atom-using-jekyll-and-github/)
* [google-spreadsheet-to-yaml-on-jekyll/](http://kinlane.com/2016/10/11/google-spreadsheet-to-yaml-on-jekyll/)
* [using-github-repos-and-jekyll-as-a-data-store/](http://kinlane.com/2016/08/15/using-github-repos-and-jekyll-as-a-data-store/)
* [https://github.com/ashmaroli/jekyll-data](https://github.com/ashmaroli/jekyll-data)
* [how-to-easily-use-airtable-data-in-jekyll](https://community.airtable.com/t/how-to-easily-use-airtable-data-in-jekyll/3925)
* [mnyrop/pagemaster](https://github.com/mnyrop/pagemaster)
* [https://minicomp.github.io/wax/reuse/](https://minicomp.github.io/wax/reuse/)
* [http://marii.info/wax_docs/](http://marii.info/wax_docs/)
* [http://marii.info/annotate/](http://marii.info/annotate/)
* [/dr-jekyll-and-mr-hyde/chart-board-visualization](https://www.litcharts.com/lit/dr-jekyll-and-mr-hyde/chart-board-visualization)
* [d3js-visualizations-using-yaml-and-jekyll/](https://apievangelist.com/2016/09/20/d3js-visualizations-using-yaml-and-jekyll/)
* [project-management/jupyter-notebook-on-jekyll/](https://www.linode.com/docs/applications/project-management/jupyter-notebook-on-jekyll/)
* [managing-data-with-jekyll/](https://www.chenhuijing.com/blog/managing-data-with-jekyll/)
* [simple-apis-with-jekyll-and-github-with-data-manag](https://dzone.com/articles/simple-apis-with-jekyll-and-github-with-data-manag)
* [18F/jekyll-get](https://github.com/18F/jekyll-get)
* [how-i-created-a-simple-dbms-using-github-jekyll-prose-and-heroku/](http://fabian-kostadinov.github.io/2015/02/04/how-i-created-a-simple-dbms-using-github-jekyll-prose-and-heroku/)
* [contrafabulists-lessons.github.io/google-sheet-to-github-website/](https://contrafabulists-lessons.github.io/google-sheet-to-github-website/)
* [integrating-autogenerated-content-into-your-documentation-site-using-swagger-and-jekyll](https://www.enigma.com/blog/integrating-autogenerated-content-into-your-documentation-site-using-swagger-and-jekyll)
* [execute-millions-of-sql-statements-in-milliseconds-in-the-browser-with-webassembly-and-web-workers](https://hackernoon.com/execute-millions-of-sql-statements-in-milliseconds-in-the-browser-with-webassembly-and-web-workers-3e0b25c3f1a6)
* [alternativeto.net/software/heroku/?license=free](https://alternativeto.net/software/heroku/?license=free)

---

see:

* [Web Work Resources](https://infominer.id/web-work)

