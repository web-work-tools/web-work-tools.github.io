---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: 'feature.jpg'
widget1:
  title: "GitHub Pages Starter Pack"
  url: '/jamstack/github-pages-starter-pack/'
  image: github-pages.jpeg
  text: 'Publishing a Website via GitHub pages is free, and easy. Everything you need to get your first site off the ground and extended resources..'
widget2:
  title: "Tools and Resources for Content Creation"
  url: 'https://github.com/Phlow/feeling-responsive'
  image: content-thumb.jpeg
  text: 'Here, I keep track of all types of information guides and tools related to content creation.'
widget3:
  title: "100's of SEO Tools Organized by Category"
  url: '/seo/tools/'
  image: webwork-tools.png
  text: "You'll be hard pressed to find a more extensive collection of SEO tools, with an assortment of links for additional resources."
#
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
#callforaction:
#  url: #https://tinyletter.com/feeling-responsive
#  text: #Inform me about new updates and features ›
#  style: #alert
permalink: /
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---
