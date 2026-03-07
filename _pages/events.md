---
title: "Community Events"
permalink: /events/
layout: archive
classes: wide
author_profile: false
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/park-header.jpg
  caption: "Join Our Community Events at Elm Road Recreation Ground"
  actions:
    - label: "Join WhatsApp"
      url: "https://chat.whatsapp.com/FZ9KMjIYmGNIgRolTgUVxb"
excerpt: "Discover upcoming events and activities at Elm Road Recreation Ground. From seasonal cleanups to family fun days, there's something for everyone!"
---

{% assign sorted_posts = site.posts | where_exp: "post", "post.categories contains 'Events'" | sort: "date" | reverse %}

<section class="page-intro-panel">
  <p class="page-intro-panel__eyebrow">Events</p>
  <h2>This is the fastest way to see what is happening in and around the park.</h2>
  <p>Use this page to find family events, volunteer sessions, planting days, and community activity organised by FERR. If you want reminders and changes in real time, join the WhatsApp group after browsing here.</p>
</section>

<section class="page-highlights-grid" aria-label="Event archive summary">
  <article class="page-highlights-card">
    <p class="page-highlights-card__eyebrow">In this archive</p>
    <h3>{{ sorted_posts | size }} events</h3>
    <p>Everything from practical volunteer sessions to family-friendly gatherings, kept in one place.</p>
  </article>
  <article class="page-highlights-card">
    <p class="page-highlights-card__eyebrow">Best next step</p>
    <h3>Check the latest listing first</h3>
    <p>The newest event is usually the most relevant one, especially for dates, timings, and what to bring.</p>
  </article>
  <article class="page-highlights-card">
    <p class="page-highlights-card__eyebrow">Stay updated</p>
    <h3>Use WhatsApp for changes</h3>
    <p>Weather, timings, and volunteer plans can move quickly. WhatsApp is where those updates land first.</p>
  </article>
</section>

<div class="entries-{{ page.entries_layout | default: 'list' }}">
  {% for post in sorted_posts %}
    {% include archive-single.html type=page.entries_layout %}
  {% endfor %}
</div>

<section class="page-cta-panel" aria-label="Event follow-up">
  <div>
    <p class="page-cta-panel__eyebrow">After browsing</p>
    <h2>Want to hear about the next event before it reaches the website?</h2>
    <p>Join the community WhatsApp group for reminders, updates, and last-minute changes, or use the contact page if you want to help organise one.</p>
  </div>
  <div class="page-cta-panel__actions">
    <a class="btn btn--success" href="https://chat.whatsapp.com/FZ9KMjIYmGNIgRolTgUVxb">Join WhatsApp</a>
    <a class="btn btn--primary" href="/contact/">Contact FERR</a>
  </div>
</section>
