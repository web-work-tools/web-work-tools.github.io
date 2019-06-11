---
type: post
title: "Infominer's GitHub Portfolio and HowTo"
description: "How to make a Portfolio for your GitHub repositories with `github/personal-website`"
date: 2019-05-27
tags: [github, repositories, open source, portfolio, github-pages]
summary: "Now there is a simple way to create a GitHub style portfolio for your github repositories!"
aliases:
  - /posts/make-a-github-portfolio/
  - /make-a-github-portfolio/
slug: /make-a-github-portfolio/
image:
  feature: /images/infominer33-github-portfolio.jpeg
  thumb: /images/infominer33-github-portfolio.jpeg
  og_image: infominer33-github-portfolio.jpeg
  credit: Check it Out!
  creditlink: https://infominer.id/repo-portfolio
---

![](https://web-work.tools/images/infominer33-github-portfolio.jpeg)

I learned of this cool project from [@bmann](https://twitter.com/bmann). I've been wanting a simple way to make a page like this for a while!

It's really nice to have a place to keep track, because I'm always forgetting how many I even manage!

It might seem intimidating to hear, "Just Fork It!" 

However, you'll see that it's not much more complex than that.

## Step 1

Fork this repository:

* [github/personal-website](https://github.com/github/personal-website)

## Step 2

Go to settings and select publish from master branch:


![](https://imgur.com/UAhVvRPl.png)

## Step 3

If you already have a web-page, then maybe you aren't reading this.. If you don't, then you must name the repository the same as your name on github. So my first website's repository name is [infominer33.github.io](https://github.com/infominer33/infominer33.github.io) since my github username is infominer33. Now it publishes to `infominer.id` (but also `infominer33.github.io`) because I have a custom domain, and every other repository I publish is a branch of that first domain.

Since I already have a primary webpage, I change my repository name to `repo-portfolio`. That way, it lives at:

* [infominer.id/repo-portfolio](https://infominer.id/repo-portfolio/)


![](https://imgur.com/yL5BaNxl.png)


## Step 4

On github pages, `_config.yml` lives in the root directory of each webpage, this is where you can fine tune settings which repositories display:

```

projects:
  sort_by: pushed
  # sort_by options:
  #   - pushed
  #   - stars
  limit: 12
  exclude:
    archived: false
    forks: false
    projects:
      - pub-yes
      - yest
      - archive-crypto
      - yest-the-docs
      - bahamas-crypto

```


you can also configure social media accounts.

```
social_media:
  website: https://infominer.id/
  keybase: infominer
  telegram: infominer33
  twitter: infominer33
  # behance: your_username
  # dribbble: your_username
  # facebook: your_username
  # hackerrank: your_username
  # instagram: your_username
  # linkedin: your_username
  # mastodon: your_username
  # medium: your_username
  # stackoverflow: your_user_id
  # unsplash: your_username
  # vk: your_username
  # youtube: your_username
```
and topics of interest:

```

topics:
  - name: Bitcoin
    web_url: https://github.com/topics/bitcoin
    image_url: https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/bitcoin/bitcoin.png

  - name: Decentralized Identity
    web_url: https://github.com/topics/decentralized-identity
    image_url: https://infominer.id/DIDecentralized/assets/icons/didicon.png

```

Cool beans, right?

There are also blog features, although I'm not sure I'll blog there... who knows!?!?

I haven't looked through the [issues](https://github.com/github/personal-website/issues), or [pull-requests](https://github.com/github/personal-website/pulls) yet to see what folk are working on, or tried to tweak any of the quirks I've noticed..

If you want to learn more about GitHub Pages, check out:



<figure class="full">
	<img src="https://web-work.tools/images/gh-pages-starter-pack.png" alt="">
	<figcaption><a href="https://web-work.tools/github-pages-starter-pack/"><b>GitHub Pages - Starter Pack:Extended Resources</b></a></figcaption>
</figure>

