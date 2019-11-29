---
layout: page-fullwidth
title: "Infominer's GitHub Portfolio and HowTo"
teaser: "How to make a Portfolio for your GitHub repositories with `github/personal-website`"

categories: ["Content Creation"]
tags: ["github", "how to"]

header: no
image:
  title: "infominer33-github-portfolio.jpeg"
  caption: "infominer.id/repo-portfolio"
  caption_url: "https://infominer.id/repo-portfolio"

redirect_from: 
 # - /make-a-github-portfolio/
permalink: /content-creation/github-portfolio/
modified: 2019-05-28T13:15:59-23:00
---

I haven't played with this in a while, but I suspect I need to do something in that portfolio to freshen up its view. All the same, I have the steps I took to get this far, right here:

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
    image_url: https://decentralized-id.com/assets/icons/didicon.png

```

Cool beans, right?

There are also blog features, although I'm not sure I'll blog there... who knows!?!?

I haven't looked through the [issues](https://github.com/github/personal-website/issues), or [pull-requests](https://github.com/github/personal-website/pulls) yet to see what folk are working on, or tried to tweak any of the quirks I've noticed..

If you want to learn more about GitHub Pages, check out:



<figure class="full">
	<img src="https://web-work.tools/images/gh-pages-starter-pack.png" alt="">
	<figcaption><a href="https://web-work.tools/jamstack/github-pages-starter-pack//"><b>GitHub Pages - Starter Pack:Extended Resources</b></a></figcaption>
</figure>

