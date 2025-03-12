---
title: "Community Events"
permalink: /events/
layout: archive
author_profile: false
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/park-header.jpg
  caption: "Join Our Community Events at Elm Road Recreation Ground"
excerpt: "Discover upcoming events and activities at Elm Road Recreation Ground. From seasonal cleanups to family fun days, there's something for everyone!"
---

{% assign sorted_posts = site.posts | where_exp: "post", "post.categories contains 'Events'" | sort: "date" | reverse %}

<div class="entries-{{ page.entries_layout | default: 'list' }}">
  {% for post in sorted_posts %}
    {% include archive-single.html type=page.entries_layout %}
  {% endfor %}
</div>