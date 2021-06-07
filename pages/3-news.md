---
layout: default
title: News
permalink: /news/
---

**News** at ELLIS Heidelberg
=========================

<hr class="hr-primary">
{% for post in site.posts %}
<div class="row">
  <div class="col-2 text-center">
    <p class="date">{{ post.date | date: "%B %d, %Y"}}</p>
  </div>
  <div class="col-10">
    <h2><a class="plain" href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt }}</p>
  </div>
  {% if forloop.last != true %}
  <div class="col-12">
    <hr>
  </div>
  {% endif %}
</div>
{% endfor %}