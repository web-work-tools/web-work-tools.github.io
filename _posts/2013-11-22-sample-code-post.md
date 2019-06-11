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

published: false
---

This is just a copy paste of useful code from the posts that come w the theme.

## Link Posts

This theme supports **link posts**, made famous by John Gruber. To use, just add `link: http://url-you-want-linked` to the post's YAML front matter and you're done.

## Background Image

> "Sample post with a background image CSS override."

Here be a sample post with a custom background image. To utilize this "feature" just add the following YAML to a post's front matter.

```yaml
image:
  background: filename.png
```

This little bit of YAML makes the assumption that your background image asset is in the `/images` folder. If you place it somewhere else or are hotlinking from the web, just include the full http(s):// URL. Either way you should have a background image that is tiled.

If you want to set a background image for the entire site just add `background: filename.png` to your `_config.yml` and BOOM --- background images on every page!

<div xmlns:cc="https://creativecommons.org/ns#" xmlns:dct="https://purl.org/dc/terms/" about="https://subtlepatterns.com" class="notice">Background images from <span property="dct:title">Subtle Patterns</span> (<a rel="cc:attributionURL" property="cc:attributionName" href="https://subtlepatterns.com">Subtle Patterns</a>) / <a rel="license" href="https://creativecommons.org/licenses/by-sa/3.0/">CC BY-SA 3.0</a></div>

## GitHub Gist Embed

An example of a Gist embed below.

{% gist mmistakes/6589546 %}

## Video Embeds

<iframe width="560" height="315" src="//www.youtube.com/embed/SU3kYxJmWuQ" frameborder="0"></iframe>

Video embeds are responsive and scale with the width of the main content block with the help of [FitVids](http://fitvidsjs.com/).

```html
<iframe width="560" height="315" src="//www.youtube.com/embed/SU3kYxJmWuQ" frameborder="0"></iframe>
```

Here are some examples of what a post with images might look like. If you want to display two or three images next to each other responsively use `figure` with the appropriate `class`. Each instance of `figure` is auto-numbered and displayed in the caption.

## Figures (for images or video)

### One Up

<figure>
	<a href="https://farm9.staticflickr.com/8426/7758832526_cc8f681e48_b.jpg"><img src="https://farm9.staticflickr.com/8426/7758832526_cc8f681e48_c.jpg" alt=""></a>
	<figcaption><a href="https://www.flickr.com/photos/80901381@N04/7758832526/" title="Morning Fog Emerging From Trees by A Guy Taking Pictures, on Flickr">Morning Fog Emerging From Trees by A Guy Taking Pictures, on Flickr</a>.</figcaption>
</figure>

### Two Up

Apply the `half` class like so to display two images side by side that share the same caption.

```html
<figure class="half">
	<img src="/images/image-filename-1.jpg" alt="">
	<img src="/images/image-filename-2.jpg" alt="">
	<figcaption>Caption describing these two images.</figcaption>
</figure>
```

And you'll get something that looks like this:

<figure class="half">
	<a href="https://placehold.it/1200x600.jpg"><img src="https://placehold.it/600x300.jpg" alt=""></a>
	<a href="https://placehold.it/1200x600.jpg"><img src="https://placehold.it/600x300.jpg" alt=""></a>
	<img src="https://placehold.it/600x300.jpg" alt="">
	<img src="https://placehold.it/600x300.jpg" alt="">
	<figcaption>Two images.</figcaption>
</figure>

### Three Up

Apply the `third` class like so to display three images side by side that share the same caption.

```html
<figure class="third">
	<a href="https://placehold.it/1200x600.jpg"><img src="https://placehold.it/600x300.jpg" alt=""></a>
	<a href="https://placehold.it/1200x600.jpg"><img src="https://placehold.it/600x300.jpg" alt=""></a>
	<a href="https://placehold.it/1200x600.jpg"><img src="https://placehold.it/600x300.jpg" alt=""></a>
	<figcaption>Caption describing these three images.</figcaption>
</figure>
```

And you'll get something that looks like this:

<figure class="third">
	<a href="https://placehold.it/1200x600.jpg"><img src="https://placehold.it/600x300.jpg" alt=""></a>
	<a href="https://placehold.it/1200x600.jpg"><img src="https://placehold.it/600x300.jpg" alt=""></a>
	<a href="https://placehold.it/1200x600.jpg"><img src="https://placehold.it/600x300.jpg" alt=""></a>
	<a href="https://placehold.it/1200x600.jpg"><img src="https://placehold.it/600x300.jpg" alt=""></a>
	<a href="https://placehold.it/1200x600.jpg"><img src="https://placehold.it/600x300.jpg" alt=""></a>
	<a href="https://placehold.it/1200x600.jpg"><img src="https://placehold.it/600x300.jpg" alt=""></a>
	<figcaption>Three images.</figcaption>
</figure>

### Alternative way

Another way to achieve the same result is to include `gallery` Liquid template. In this case you
don't have to write any HTML tags – just copy a small block of code, adjust the parameters (see below)
and fill the block with any number of links to images. You can mix relative and external links.

Here is the block you might want to use: ( can't make local captures to work.)

```liquid
{% raw %}{% capture images %}
	https://web-work.tools/images/abstract-10.jpg
	https://web-work.tools/images/abstract-11.jpg
	http://upload.wikimedia.org/wikipedia/en/2/24/Lenna.png
{% endcapture %}
{% include gallery images=images caption="Test images" cols=3 %}{% endraw %}
```

Parameters:

- `caption`: Sets the caption under the gallery (see `figcaption` HTML tag above);
- `cols`: Sets the number of columns of the gallery.
Available values: [1..3].

It will look something like this:

{% capture images %}
	https://web-work.tools/images/abstract-10.jpg
	https://web-work.tools/images/abstract-11.jpg
	https://upload.wikimedia.org/wikipedia/commons/6/6c/Lenna_0.1_SP_Noise_3x3_VecMed_L1.png
{% endcapture %}
{% include gallery images=images caption="Test images" cols=3 %}
