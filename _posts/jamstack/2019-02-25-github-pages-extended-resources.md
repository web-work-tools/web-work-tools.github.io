---
layout: page-fullwidth
title: "GitHub Pages-Extended Resources"
teaser: "Publishing a Website via GitHub pages is free, and easy. Everything you need to publish in one place."
tags: ['jekyll', 'github pages', 'ssg']
categories: ['jamstack']

header: no

image:
  title: "github-pages-extended-resources.png"
  thumb: "github.png"

redirect_from: 
  - /github-pages-extended-resources/
permalink: /jamstack/github-pages-extended-resources/
modified: 2019-06-16T15:59:13-23:00
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


* Continued from [**Github Pages Starter Pack**](/jamstack/github-pages-starter-pack/).

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

<a href="https://web-work.tools/indieweb-resources/" class="btn btn-success">web-work.tools/indieweb-resources</a>

* [indieweb.org](https://indieweb.org)
* [Micropub](https://indieweb.org/Micropub)
* [IndieAuth](https://indieweb.org/IndieAuth)
* [miklb/jekyll-indieweb](https://github.com/miklb/jekyll-indieweb)
* [Static Site Generators & the IndieWeb](https://www.growdigital.org/posts/static-site-generators-the-indieweb/)
* [Jekyll and the Indieweb](http://wordius.com/jekyll-and-the-indieweb/)
* [Implementing the Indieweb on a static website](https://vincentp.me/articles/2018/11/14/20-00/) - Sending and receiving Webmentions and Micropub on a static site
* [voxpelli/webpage-micropub-to-github/](https://github.com/voxpelli/webpage-micropub-to-github/)

