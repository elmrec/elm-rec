---
title: "Events"
permalink: /events/
layout: archive
author_profile: false
---

{% assign sorted_posts = site.posts | where_exp: "post", "post.categories contains 'Events'" | sort: "date" | reverse %}

<div class="entries-{{ page.entries_layout | default: 'list' }}">
  {% for post in sorted_posts %}
    {% include archive-single.html type=page.entries_layout %}
  {% endfor %}
</div>