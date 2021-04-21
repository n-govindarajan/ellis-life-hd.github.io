---
layout: default
title: Events
permalink: /events/
---

ELLIS Heidelberg **events**
===========================

<hr class="hr-primary">
{% for category in site.categories %}
{% if category[0] == "event" %}
{% for post in category[1] %}
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
{% endif %}
{% endfor %}