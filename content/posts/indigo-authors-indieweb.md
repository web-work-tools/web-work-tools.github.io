---
type: post
title: "Indigo Authors - Indiweb Features"
date: 2019-06-03
categories: ["meta"]
tags: ["options", "indieweb","hugo","front matter"]
slug: /indigo-authors-indieweb/
aliases:
  - /indigo-authors-indieweb/
  - /posts/indigo-authors-indieweb/
summary: >
  "The following classes are used to mark up the author bio for Indieweb parsing: h-card, u-photo, p-name, u-url, rel=me, p-locality, p-country-name, u-email, p-note. I'll be exploring these classes more thoroughly, soon."

---

## Notes from the Editor

I'm noticing that the repository hasn't been recently updated by it's owner, however, I can find some helpful contributions from the community:

* https://github.com/AngeloStavrow/indigo/pulls

*note, I changed the date so it would bump to the top.


## Indigo Authors
The bottom of every page in the theme can optionally show a short biography of the site author, including a profile picture, email link, and location.

<!--more-->

## Setting up the author bio

A set of configuration options are used for displaying the biography.

```
[params]
  Author = "Author Name"
  Avatar = "images/site-logo.svg"
  Biography = "A short description, a few sentences describing the author. Set
               the 'ShowBio' parameter to false to hide this."
  ShowBio = true        

[params.indieWeb]  
    EmailAddress = "email.address@example.com"
    Country = "CountryName"
    City = "CityName"
```

Specifics on each setting item are as follows:

- `Author`: Your name; this is the site author name.
- `Avatar`: The path to your profile picture. By default, it will show the theme's logo (`/static/images/site-logo.svg`).
- `Biography`: Hopefully the placeholder text here is self-explanatory; add a couple of short sentences about yourself here.
- `ShowBio`: If you prefer not to show the author bio, set this to `false`. By default, it's set to `true`.
- `EmailAddress`: The email address at which you can be contacted.
- `Country`: The name of the country in which you live.
- `City`: The name of the city in which you live.

## IndieWeb features

The following classes are used to mark up the author bio for [IndieWeb][indieweb] parsing:

| Element         | Class                       |
| :-------------- | :-------------------------- |
| The author card | `h-card`                    |
| Profile picture | `u-photo`                   |
| Author URL*     | `p-name`, `u-url`, `rel=me` |
| City            | `p-locality`                |
| Country         | `p-country-name`            |
| Email address   | `u-email`                   |
| Biography       | `p-note`                    |

*Author URL is set to the site's base URL.

[indieweb]: https://indieweb.org/

