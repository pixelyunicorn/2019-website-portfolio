# [victor.horse](http://victor.horse)

Built with Jekyll and hosted on GitHub Pages. Created for 2018's #May1Reboot event to showcase my most recent work.

## Content Structure

| Directory |  |
| --- | --- |
| ````_work/```` | Portfolio projects. |
| ````pages/```` | Site content. |
| ````media/```` | Images, pdfs, and other misc static content. |

### Blog Posts

**Blog posts can be easily edited and managed online via http://prose.io/#user/repo.**

Put published posts in ````_work```` and unpublished posts in ````_drafts````.

The first part of the file starts & ends with three dashes. This is your yaml configuration.

Then comes the markdown. Cheatsheet here: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

````markdown
---
title: Hack Club
permalink: /hackclub

web: https://wayback.archive.org/web/20171101000000*/hackclub.com
web-display: HackClub.com (Archived)

tagline: Hack Together!
description: Landing page empowering students to start coding clubs
lead: A nonprofit founded by Forbes 30 Under 30’s Zach Latta, <strong>Hack Club</strong> brings student-led coding clubs to high schools across the world. I worked with Hack Club to create a new homepage and design system that demonstrates how coding is for everyone.

tags: [ design, dev, education, foundation, website, 2016 ]
deliverables: [ Frontend, Design, Writing ]
technologies: [ Rails, Foundation, Sass, Sketch ]

accent: "#E43143"
accent-light: "#FFDEE2"
header-text: white
pattern: patterns/hackclub-10.svg

# Optional webpage screenshot display
screenshots: true
screenshots-desktop: screenshots/hackclub-homepage-d.png
screenshots-mobile: screenshots/hackclub-homepage-m.png

# Optional photo display
photos:
  - [ codeday/voculus.svg, caption ]
  - [ codeday/vtrophy.svg, caption ]
  - [ codeday/vphone.svg, caption ]
---

You can start typing content here. <b>HTML is supported</b> and so is **markdown syntax.**
Try to use bold text and refrain from using _italics_ whenever possible.

Below are your headers, use them sparingly.

## Header 2

### Header 3

Images are pretty easy.

![Image description for screen readers go here: Fluffle Puff!](/media/guests/flufflepuff-avatar.png)

So are links: [Click here for Google!](http://google.com/)

> I am a quote
> - Maud Pie

You can make tables too, if you're inclined.

| Column Header 1 | Column Header 2 |
| -- | -- |
| Hi! | You get the point |
| Yo! | What's up? |

Lists are easy, just number or bullet them appropriately, like this:

- Item 1
- Item 2

1. Item 1
2. Item 2

You can embed anything by copying and pasting an embed code:
<iframe width="560" height="315" src="https://www.youtube.com/embed/rMFWc_FMhqs"
frameborder="0" allowfullscreen></iframe>

````

### Pages

Like posts, but also supports markdown ````.md```` or html ````.html````. I reccomend using html.

````markdown
---
layout: page # page (default) or blank (have to manually define container and content areas)
title: Philadelphia
subtitle: A guide to the City of Brother Love! # optional
permalink: /philly/
redirect_from: /philadelphia/ # optional if you are redireccting from an old url
cover: # may be used in the future
---

Start typing content here!
````

## Development Structure

| Directory |  |
| --- | --- |
| ````_includes/```` | Contents of < head >, navigation, and footer. |
| ````_layouts/```` | Page layout templates. |
| ````_sass/```` | Partial stylesheets. Modify _site.scss for site styles. |
| ````css/```` | Stylesheet compiler, don't touch this file. |
| ````icons/```` | Icon font! See icons/demo.html for a full list. |
| ````img/```` | Static assets necessary to display the site. |

| File |  |
| --- | --- |
| ````404.html/```` | 404 page. Easter egg, maybe? |
| ````CNAME```` | Sets up a CNAME record for the domain the site is on. |
| ````_config.yml```` | Site settings and commonly used phrases.  |
| ````_prose.yml```` | Configuration for [prose.io](http://prose.io/).  |
| ````feed.xml```` | RSS feed for blog posts. |
| ````robots.txt```` | Bot access settings, please change before deploying to production. |

## Running the site locally

Make sure you have ruby installed, then...

````bash
cd cutie

# install gems (first time only)
bundle install

# run server on localhost:4000. SCSS and page content compiled automatically on save.
bundle exec jekyll serve --port 4000 --watch --incremental
````
