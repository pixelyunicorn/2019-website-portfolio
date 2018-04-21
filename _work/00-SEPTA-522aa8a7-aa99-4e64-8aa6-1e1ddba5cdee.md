---
title: SEPTA
permalink: /septa

web: http://bolty-scalp.victor.moe/realtime/status/system-status.html
web-display: SEPTA.org (preview)

tagline: Track Yo' Vehicle!
description: A modern status page for a century-old public transit system
lead: With 306.9 million annual trips, the <strong>Southeastern Pennsylvania Transportation Authority (SEPTA)</strong> has a heavily-utilized System Status page that displays critical information for riders, such as real time vehicle locations, detours, delays, and suspensions. They tapped into the experts from the <strong>PennApps Fellows</strong> program to redesign that page for the mobile era.

tags: [ design, dev, react, transit, website, 2016 ]
deliverables: [ Project Management, Frontend ]
technologies: [ React ]
contributors: [ "PennApps Fellows (developers)" ]

accent: "#2B5D94"
accent-light: "#CCEBFF"
header-text: white
pattern: hero-patterns/happy-intersection-05.svg

screenshots: true
screenshots-desktop: screenshots/septa-routes-d.png
screenshots-mobile: screenshots/septa-routes-m.png
---

# Easy to Navigate

We built a single page application that updates dynamically with content provided by SEPTA. The page is familiar to existing users, with a cleaner layout that makes an extensive list of routes easier to navigate.

<blockquote class="accent-light-bg text-center">
	<strong>Main Page</strong>
	<row>
		<column class="no-margin-bottom"><i>Before</i><img src="{{ site.baseurl }}/media/work/septa/home-before.png" alt="Before my rewrite"></column>
		<column class="no-margin-bottom"><i>After</i><img src="{{ site.baseurl }}/media/work/septa/home-after.png" alt="After my rewrite"></column>
	</row>
</blockquote>

<blockquote class="accent-light-bg text-center">
	<strong>Route Display</strong>
	<row>
		<column class="no-margin-bottom"><i>Before: Modal Accordion</i><img src="{{ site.baseurl }}/media/work/septa/route-before.png" alt="Before my rewrite"></column>
		<column class="no-margin-bottom"><i>After: Single Page</i><img src="{{ site.baseurl }}/media/work/septa/route-after.png" alt="After my rewrite"></column>
	</row>
</blockquote>

# Mobile-First Design

The most common use case for the System Status page is for mobile users to track their vehicles in realtime, yet the current website is nowhere close to being optimized for the most common mobile devices on the market. We optimized the page to be mobile friendly with easy-to-find routes and automatic location usage after location permission is granted.

<blockquote class="accent-light-bg text-center">
	<strong>Mobile User Flow</strong>
	<row>
		<column class="no-margin-bottom"><i>Mode Selection</i><img src="{{ site.baseurl }}/media/work/septa/mobile-1.png" alt="Before my rewrite"></column>
		<column class="no-margin-bottom"><i>Route Selection</i><img src="{{ site.baseurl }}/media/work/septa/mobile-2.png" alt="After my rewrite"></column>
		<column class="no-margin-bottom"><i>Status Display</i><img src="{{ site.baseurl }}/media/work/septa/mobile-3.png" alt="After my rewrite"></column>
	</row>
</blockquote>

# Bad Data? No Problem!

Once of the most interesting challenges with this project was working on an [API](https://sidewaysdictionary.com/#/term/api) (data feed) that did not provide data in a developer-friendly format. This API was full of inconsistencies (and typos!) but it was the best form of information that SEPTA had to offer. Thankfully, React makes it easy to iron out these inconsistencies, so strings like `Yes` and `Y` were turned into booleans like `true` as data flows in. [(Don’t believe us? Click here to see it for yourself!)](https://www3.septa.org/api/Alerts/?dataType=jsonp)


<pre>
[{
	"route_id":"bus_route_1",
	"route_name":"1",
	"mode":"Bus",
	"isadvisory":"<strong class="accent-bg">No</strong>",
	"isdetour":"N",
	"isalert":"N",
	"<strong class="accent-bg">issuppend</strong>":"N",
	"last_updated":"Mar 22 2018  3:31PM",
	"<strong class="accent-bg">isSnow</strong>":"N",
	"description":"Parx Casino to 54th-City"
},
</pre>