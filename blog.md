---
title: Design Office Blog
permalink: /blog/
layout: page
---
<hr>
{% for post in site.posts %}
  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
  <h5>Author: {{ post.author }}</h5>
  <p>{{ post.excerpt }}</p>
  <hr>
{% endfor %}