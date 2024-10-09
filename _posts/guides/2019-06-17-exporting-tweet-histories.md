---
layout: page-fullwidth
title: "Twitter Data: Mine, Export, Explore, Publish"
teaser: "Export your tweets to CSV, filter in a spreadsheet and publish."

categories: ["content creation", "guides"]
tags: ["twitter"]
header: no
image:
  title: twitter-history-export.jpg
  thumb: twitter-history-export.jpg

permalink: /content-creation/twitter-export-csv/
canonical_url: https://web-work-tools.github.io/content-creation/twitter-export-csv/
modified: 2020-11-07T22:22:22-23:00

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

At the start of 2018, I began retweeting all the most valuable information I found on twitter, as part of a learning process. Then, I would periodically scroll back and manually paste the links into the channels of a discord server, organized by category.

The problem with that, is if you are scrolling through your history, it has to load, and it's easy to miss that particualr tweet where I know I left off.

Once I gave up scrolling my twitter history manually, I used a share button integration with discord, to directly send a given link to the proper channel. 

Now I'm taking a break from twitter, transitioning from discord to spreadsheets, and in the process of consolidating a few years of link collecting on a variety of subjects. I have a lot to organize between 4 twitter accounts, a dozen discord servers where I collected\organized links, and a variety of other sources....

## What do?

I started out using a web-app to grab my timeline, and then sort through them using CSV. More recently I got into python, where it's pretty simple to build a script that will grab tweets based on a variety of queries.

For now this is just a collection of links from my research trying to figure out how to manage twitter in some sane way. Once I get a work-flow set up, I will share some of my own work here too.

## Twitter History Export

* [Want to analyse your tweets? How to import Twitter JSON data exports into Excel - ZDNet](https://www.zdnet.com/article/want-to-analyse-your-tweets-how-to-import-twitter-json-data-exports-into-excel/)
  > It turns out that Twitter is using a non-standard version of JSON lists for its exports, and you're going to need to make a quick change to the file it delivers if you want to be able to use your data in any analytical tooling. If you've been on Twitter as long as I have, that can mean editing at the very least a 100GB plus file (in my case two) to remove the text Twitter has added to the start of what would otherwise be a relatively normal list formatted set of JSON documents. You'll need a decent text editor to make the changes. I recommend something like Visual Studio Code, which can happily load very large text files.
* [Show HN: Search your Twitter history with Algolia - Hacker News](https://github.com/saasify-sh/twitter-search) - [Hacker News](https://news.ycombinator.com/item?id=22842542)
  > Instantly search across your entire Twitter history with a beautiful UI powered by Algolia.

## Twitter API

* [Use Cases, Tutorials, & Documentation - Twitter Developer](https://developer.twitter.com/en)
  > The following examples demonstrate how Twitter developer products can be used to build solutions across a diverse set of use cases. Preview the data that is returned by our endpoints.
* [Standard search API — Twitter Developers](https://developer.twitter.com/en/docs/tweets/search/api-reference/get-search-tweets)
  > To learn how to use [Twitter Search](https://twitter.com/search) effectively, please see the [Standard search operators](https://developer.twitter.com/en/docs/tweets/search/guides/standard-operators) page for a list of available filter operators. Also, see the [Working with Timelines](https://developer.twitter.com/en/docs/tweets/timelines/guides/working-with-timelines) page to learn best practices for navigating results by `since_id` and `max_id`.
* [Standard operators - Docs - Twitter Developer](https://developer.twitter.com/en/docs/twitter-api/v1/rules-and-filtering/overview/standard-operators)
  > The best way to build a standard query and test if it’s valid and will return matched Tweets is to first try it at [twitter.com/search](https://twitter.com/search). As you get a satisfactory result set, the URL loaded in the browser will contain the proper query syntax that can be reused in the standard search API endpoint.
  * [Automate Getting Twitter Data in Python Using Tweepy and API Access > Customizing Twitter Queries](https://www.earthdatascience.org/courses/use-data-open-source-python/intro-to-apis/twitter-data-in-python/#customizing-twitter-queries)
    > if you search for climate+change, Twitter will return all tweets that contain both of those words (in a row) in each tweet. [...]
    > `new_search = "climate+change -filter:retweets"`
* [GET statuses/oembed - Docs - Twitter Developer](https://developer.twitter.com/en/docs/twitter-api/v1/tweets/post-and-engage/api-reference/get-statuses-oembed)
  > The oEmbed endpoint allows customization of the final appearance of an Embedded Tweet by setting the corresponding properties in HTML markup to be interpreted by Twitter's JavaScript bundled with the HTML response by default. The format of the returned markup may change over time as Twitter adds new features or adjusts its Tweet representation.

### Collections

* [About collections - Docs - Twitter Developer](https://developer.twitter.com/en/docs/twitter-api/v1/tweets/curate-a-collection/overview/about_collections)
  > Use these methods to browse Collections, whether by ID, those owned by a specific user, or those containing a specific Tweet.
  > 
  > These methods allow you to create, modify, or delete a collection on behalf of the currently authenticated user.
  > 
  > Collections are meant to be shared with the world, on and off Twitter. To that end, [embedded timelines](https://dev.twitter.com/web/embedded-timelines) have been expanded to support [embedded collections](https://dev.twitter.com/web/embedded-timelines/collection). Use the [widget configurator](https://twitter.com/settings/widgets/new/custom) to prepare your collections for syndication and receive the simple HTML & JavaScript embed code for your site.
* [Response structures when Querying Collections - Docs - Twitter Developer](https://developer.twitter.com/en/docs/twitter-api/v1/tweets/curate-a-collection/overview/response_structures)
  > The Collections API responds with data structures that often depart from the objects you traditionally encounter in the Twitter API.
* [Overview - Docs - Twitter Developer](https://developer.twitter.com/en/docs/twitter-for-websites/timelines/overview)
  > Embedded timelines are an easy way to embed Tweets on your website in a compact, linear view. Display the latest Tweets from a Twitter account, lists, or your curated collections.
* [Creating a Twitter Collection via API - by Lauren Fratamico - Medium](https://medium.com/@lauren.fratamico/creating-a-twitter-collection-via-api-1378ecfe20df)
  > This tutorial goes through how to create and add to collections via python3, and the code can be seen in a gist [here](https://gist.github.com/fratamico/0a56a342d483882ec1d5fb451676d5ae).

### Tweepy (python)

* [tweepy.api — Twitter API wrapper — tweepy 3.9.0](http://docs.tweepy.org/en/latest/api.html)
  > This page contains some basic documentation for the Tweepy module.
* [Extended Tweets — tweepy 3.9.0 documentation](http://docs.tweepy.org/en/latest/extended_tweets.html)
  > When using extended mode, the `text` attribute of Status objects returned by `tweepy.API` methods is replaced by a `full_text` attribute, which contains the entire untruncated text of the Tweet. The `truncated` attribute of the Status object will be `False`, and the `entities` attribute will contain all entities. Additionally, the Status object will have a `display_text_range` attribute, an array of two Unicode code point indices, identifying the inclusive start and exclusive end of the displayable content of the Tweet.

#### Scripts

* [How I automatically created a Twitter List of FreeCodeCampers in 5 minutes](https://www.freecodecamp.org/news/how-i-automatically-created-a-twitter-list-of-freecodecampers-in-5-minutes-425f0b922118/)
  > We are going to create a Python script that will automatically search Twitter for individuals who use the **#freeCodeCamp** hashtag and add them to a Twitter list of “FreeCodeCampers”. [Twitter lists](https://help.twitter.com/en/using-twitter/twitter-lists) are a way to curate a group of individuals on Twitter and collect all of their tweets in a stream, without having to follow each individual accounts. Twitter lists can contain up to 5,000 individual Twitter accounts.
* [yanofsky/tweet_dumper.py](https://gist.github.com/yanofsky/5436496)
  > A script to download all of a user's tweets into a csv
* [arikfr/export_lists.py](https://gist.github.com/arikfr/58e491e0cdbe36a9e48c) 
  > Simple script to export Twitter lists to CSV
* [vickyqian/twitter crawler.txt](https://gist.github.com/vickyqian/f70e9ab3910c7c290d9d715491cde44c) 
  > A Python script to download all the tweets of a hashtag into a csv
* [freeCodeCamp/100DaysOfCode-twitter-bot](https://github.com/freeCodeCamp/100DaysOfCode-twitter-bot) - Automated twitter list creation based on hashtag
  > Twitter bot for #100DaysOfCode [@_100DaysOfCode](https://twitter.com/_100DaysOfCode)
* [tylerpearson/twitter-most-followed-scripts](https://github.com/tylerpearson/twitter-most-followed-scripts) 
  >  Scripts to find the most commonly followed Twitter accounts by a group of people [tmf.tylerp.me](http://tmf.tylerp.me)
* [tylerpearson/twitter-bio-analyzer-script](https://github.com/tylerpearson/twitter-bio-analyzer-script)
  > Ruby script to find the most common words in the bios of the accounts a user follows on Twitter
* [justinlittman/twitter-scraper](https://github.com/justinlittman/twitter-scraper) - A tool for scraping tweet ids from the Twitter website.
* [MikeMcQuaid/TwitterDelete](https://github.com/MikeMcQuaid/TwitterDelete) - Delete your old, unpopular tweets. 
* [bonzanini/Book-SocialMediaMiningPython](https://github.com/bonzanini) - Companion code for the book "Mastering Social Media Mining with Python

### R Tweet

*  [rtweet.info](https://rtweet.info)
  * [mkearney/rtweet](https://github.com/mkearney/rtweet) - bird R client for interacting with Twitter's [stream and REST] APIs
  * [mkearney/rtweet-workshop](https://github.com/mkearney/rtweet-workshop)
  * [hrbrmstr/21-recipes](https://github.com/hrbrmstr/21-recipes) - An R/rtweet edition of [Matthew A. Russell's Python Twitter Recipes Book](https://rud.is/books/21-recipes/)

## Apps

* [botwiki/botwiki.org](https://github.com/botwiki/botwiki.org) - Tutorials, articles, datasets and other resources for creating useful, interesting, artistic and friendly online bots. 
* [huginn/huginn](https://github.com/huginn/huginn) - Create agents that monitor and act on your behalf. Your agents are standing by! 
* [geofurb/Ornitholog](https://github.com/geofurb/Ornitholog) - Open-source Twitter collection and archiving tool for tracking specific topics and collecting bulk data.
* [motazsaad/tweets-collector](https://github.com/motazsaad/tweets-collector) - Collect tweets (tweets corpus) using Twitter API. Collection can be based on hashtags, keywords, geographical location
* [vicinitas.io - Download User Tweets](https://www.vicinitas.io/free-tools/download-user-tweets) 
* [hridaydutta123/awesome-twitter-tools](https://github.com/hridaydutta123/awesome-twitter-tools)
* [kennethreitz/twitter-scraper](https://github.com/kennethreitz/twitter-scraper) - Scrape the Twitter Frontend API without authentication. 
* [twintproject/twint](https://github.com/twintproject/twint) - An advanced Twitter scraping & OSINT tool written in Python that doesn't use Twitter's API, allowing you to scrape a user's followers, following, Tweets and more while evading most API limitations.
* [taspinar/twitterscraper](https://github.com/taspinar/twitterscraper) - Scrape Twitter for Tweets
* [AdrienGuille/TweetStreamer](https://github.com/AdrienGuille/TweetStreamer) - A command line tool for collecting tweets via Twitter's public streaming API
* [DocNow/twarc](https://github.com/DocNow/twarc) - A command line tool (and Python library) for archiving Twitter JSON
* [Jefferson-Henrique/GetOldTweets-python](https://github.com/Jefferson-Henrique/GetOldTweets-python) - A project written in Python to get old tweets, it bypass some limitations of Twitter Official API.
* [jennybc/scream](https://github.com/jennybc/scream) - Get replies and quotes of a tweet
* [snovvcrash/tweetlord](https://github.com/snovvcrash/tweetlord) - bird Twitter profile dumper (downloader) with authorization swapping
* [Datamine/Archive-Tweets](https://github.com/Datamine/Archive-Tweets) - Archive and Delete Liked and Posted Tweets
* [The Best Twitter Search Tricks - Digital Inspiration](https://www.labnol.org/internet/twitter-search-tricks/13693/)
  > The [Twitter Archiver](https://www.labnol.org/internet/save-twitter-hashtag-tweets/6505/) and the [Twitter Bots](https://www.labnol.org/internet/write-twitter-bot/27902/) app fire each time a new tweet is found that match your search query. You can write simple search queries (like `#Oscars`) or more complex query (like `obama min_retweets:10 filter:news`) that uses one or more Twitter’s advanced search operators.

## Re-Publishing Twitter Content

* [Twitter’s Developer Policies for Researchers, Archivists, and Librarians - by Justin Littman - On Archivy - Medium](https://medium.com/on-archivy/twitters-developer-policies-for-researchers-archivists-and-librarians-63e9ba0433b2)
  > I have long maintained that one of the most significant barriers to Twitter research and archiving are [Twitter’s Developer Policies](https://developer.twitter.com/en/developer-terms/policy). This barrier takes the form of not only the restrictions contained in the policies, but the ambiguity of the documents themselves.
* [Set up Twitter for Websites - Docs - Twitter Developer](https://developer.twitter.com/en/docs/twitter-for-websites/javascript-api/guides/set-up-twitter-for-websites)
  > The easiest way to create a Twitter for Websites widget — a Tweet button, Follow button, embedded Tweet or timeline — is to use our configuration tools at [publish.twitter.com](https://publish.twitter.com/) then copy and paste the generated HTML code into the template or widget area for your site.
* [Display requirements – Twitter Developers - Twitter Developer](https://developer.twitter.com/en/developer-terms/display-requirements)
  > If you follow these guidelines merely to display a Tweet, you may not need to contact Twitter for any additional display or trademark permissions. However, you may still want to submit your proposed use and context for Twitter review. (Note that, in some cases, permission from the original content creator may still be necessary, as Twitter does not provide permission to use third party/user content.)
* [rob-murray/jekyll-twitter-plugin](https://github.com/rob-murray/jekyll-twitter-plugin)
  > A Liquid tag plugin for the Jekyll blogging engine that embeds Tweets, Timelines and more from Twitter API
* [tylerpearson/twitter-most-followed-site](https://github.com/tylerpearson/twitter-most-followed-site)
    > Jekyll site to display the results generate by the scripts in the [Twitter Most Followed repo](https://github.com/tylerpearson/twitter-most-followed-scripts).

## Nerd Stuff

* [mattdodge/Tweet-2-RSS](https://github.com/mattdodge/Tweet-2-RSS)
* [vzqzac/twgitbot](https://github.com/vzqzac/twgitbot) - A node.js bot that checks a github repo changes and tweets it to your Twitter account 
* [Kikobeats/fetch-timeline-cli](https://github.com/Kikobeats/fetch-timeline-cli) - Fetch Twitter user's timeline from your terminal zap. 
  * [kikobeats.github.io/fetch-timeline-cli/](https://kikobeats.github.io/fetch-timeline-cli/)
* [renatolond/mastodon-twitter-poster](https://github.com/renatolond/mastodon-twitter-poster) - Crossposter to post statuses between Mastodon and Twitter
