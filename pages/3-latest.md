---
layout: default
title: Latest
permalink: /latest/
---

**Follow our latest updates**
=============================

{% for post in site.posts %}
<div class="news-tile">
  <hr />
  <div class="row py-vw1">
    <div class="col-md-2 text-center">
      {% if post.date > site.time %}
        <p class="date future-date">{{ post.date | date: "%B %d, %Y"}}</p>
      {% else %}
        <p class="date">{{ post.date | date: "%B %d, %Y"}}</p>
      {% endif %}
    </div>
    <div class="col-md-10">
      <h2><a class="plain" href="{{ post.url }}">{{ post.title }}</a></h2>
      {% if post.event_title %}
        <p>{{ post.event_title }}</p>
      {% else %}
        <p>{{ post.excerpt }}</p>
      {% endif %}
    </div>
  </div>
</div>
{% endfor %}
