---
layout: page-fullwidth
title: "Twitter Data: Mine, Export, Explore, Publish"
teaser: "Export your tweets to CSV, filter in a spreadsheet and publish."

tags: ["How-To"]
categories: ["Content Creation"]

header: no
image:
  title: twitter-history-export.jpg
  thumb: twitter-history-export.jpg

redirect_from:
  - export-tweets-csv/
permalink: /content-creation/twitter-export-csv/
canonical_url: https://web-work.tools/content-creation/twitter-export-csv/
modified: 2019-06-18T22:22:22-23:00

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

Now I'm taking a break from twitter, transitioning from discord to spreadsheets, and in the process of consolidating a few years of link collecting on a variety of subjects. I have a lot to organize between 4 twitter accounts, a dozen discord servers where I organized links on different subjects, and a variety of other sources....

**What do?**

# Export Tweets to CSV

So, this is the hard part. Finding a *free* app that will get as many tweets as you need.

For now, I know [vicinitas.io](https://www.vicinitas.io/free-tools/download-user-tweets) allows you to download up to 3200 tweets to csv, which was enough for me.

In the future, this page will fill with everything related to exporting and publishing content from twitter.

From there, I threw the CSV in Libre Office Calc (an ok free version of Excell). I was able to filter the 3200 tweets to include only those related to identity.

I am going to share more about how, exactly, I make the content from csv. In the meantime:

## Resources

This is a game changer! While searching for resources to add in this post, I found [rob-murray/jekyll-twitter-plugin](https://github.com/rob-murray/jekyll-twitter-plugin)!!!
{: .notice}

* [twitterdev/tweet-updates](https://github.com/twitterdev/tweet-updates) - This repository contains information about the updates to Tweet formats for attachments and simplified replies. -[developer.twitter.com - tweet updates](https://developer.twitter.com/en/docs/tweets/tweet-updates.html)
* [hridaydutta123/awesome-twitter-tools](https://github.com/hridaydutta123/awesome-twitter-tools)

## Twitter Related Gists
* [yanofsky/tweet_dumper.py](https://gist.github.com/yanofsky/5436496) - A script to download all of a user's tweets into a csv
* [arikfr/export_lists.py](https://gist.github.com/arikfr/58e491e0cdbe36a9e48c) - Simple script to export Twitter lists to CSV]
* [vickyqian/twitter crawler.txt](https://gist.github.com/vickyqian/f70e9ab3910c7c290d9d715491cde44c) - A Python script to download all the tweets of a hashtag into a csv

## Twitter GitHub Repos

* [kennethreitz/twitter-scraper](https://github.com/kennethreitz/twitter-scraper) - Scrape the Twitter Frontend API without authentication. 
*  [rtweet.info](https://rtweet.info)
  * [mkearney/rtweet](https://github.com/mkearney/rtweet) - bird R client for interacting with Twitter's [stream and REST] APIs
  * [mkearney/rtweet-workshop](https://github.com/mkearney/rtweet-workshop)
  * [hrbrmstr/21-recipes]() - An R/rtweet edition of [Matthew A. Russell's Python Twitter Recipes Book](https://rud.is/books/21-recipes/)
* [twintproject/twint](https://github.com/twintproject/twint) - An advanced Twitter scraping & OSINT tool written in Python that doesn't use Twitter's API, allowing you to scrape a user's followers, following, Tweets and more while evading most API limitations.
* [taspinar/twitterscraper](https://github.com/taspinar/twitterscraper) - Scrape Twitter for Tweets
* [AdrienGuille/TweetStreamer](https://github.com/AdrienGuille/TweetStreamer) - A command line tool for collecting tweets via Twitter's public streaming API
* [DocNow/twarc](https://github.com/DocNow/twarc) - A command line tool (and Python library) for archiving Twitter JSON
* [Jefferson-Henrique/GetOldTweets-python](https://github.com/Jefferson-Henrique/GetOldTweets-python) - A project written in Python to get old tweets, it bypass some limitations of Twitter Official API.
* [jennybc/scream](https://github.com/jennybc/scream) - Get replies and quotes of a tweet
* [snovvcrash/tweetlord](https://github.com/snovvcrash/tweetlord) - bird Twitter profile dumper (downloader) with authorization swapping
* [Datamine/Archive-Tweets](https://github.com/Datamine/Archive-Tweets) - Archive and Delete Liked and Posted Tweets


## Cross-posting
* [renatolond/mastodon-twitter-poster](https://github.com/renatolond/mastodon-twitter-poster) - Crossposter to post statuses between Mastodon and Twitter

## Bots - Code

* [freeCodeCamp/100DaysOfCode-twitter-bot](https://github.com/freeCodeCamp/100DaysOfCode-twitter-bot) - Twitter bot for #100DaysOfCode [@_100DaysOfCode](https://twitter.com/_100DaysOfCode)
* [bonzanini/Book-SocialMediaMiningPython](https://github.com/bonzanini) - Companion code for the book "Mastering Social Media Mining with Python
* [botwiki/botwiki.org](https://github.com/botwiki/botwiki.org) - Tutorials, articles, datasets and other resources for creating useful, interesting, artistic and friendly online bots. 
* [huginn/huginn](https://github.com/huginn/huginn) - Create agents that monitor and act on your behalf. Your agents are standing by! 

## Clean Feed

* [MikeMcQuaid/TwitterDelete](https://github.com/MikeMcQuaid/TwitterDelete) - Delete your old, unpopular tweets. 

## Nerd Stuff

* [mattdodge/Tweet-2-RSS](https://github.com/mattdodge/Tweet-2-RSS)
* [vzqzac/twgitbot](https://github.com/vzqzac/twgitbot) - A node.js bot that checks a github repo changes and tweets it to your Twitter account 
* [Kikobeats/fetch-timeline-cli]() - Fetch Twitter user's timeline from your terminal zap. 
  * [kikobeats.github.io/fetch-timeline-cli/](https://kikobeats.github.io/fetch-timeline-cli/)


## Data

* [tylerpearson/twitter-most-followed-scripts](https://github.com/tylerpearson/twitter-most-followed-scripts) - Scripts to find the most commonly followed Twitter accounts by a group of people [tmf.tylerp.me](http://tmf.tylerp.me)
  * [tylerpearson/twitter-most-followed-site](https://github.com/tylerpearson/twitter-most-followed-site)
* [tylerpearson/twitter-bio-analyzer-script](https://github.com/tylerpearson/twitter-bio-analyzer-script)
* [justinlittman/twitter-scraper](https://github.com/justinlittman/twitter-scraper) - A tool for scraping tweet ids from the Twitter website.
* [geofurb/Ornitholog](https://github.com/geofurb/Ornitholog) - Open-source Twitter collection and archiving tool for tracking specific topics and collecting bulk data.
* [motazsaad/tweets-collector](https://github.com/motazsaad/tweets-collector) - Collect tweets (tweets corpus) using Twitter API. Collection can be based on hashtags, keywords, geographical location


## Templates

* [HoussemDellai/social-media-templates](https://github.com/HoussemDellai/social-media-templates) - Provides templates for using Twitter, Youtube, Instagram, Flickr, Foursquare and Eventbrite API with Xamarin Forms.
