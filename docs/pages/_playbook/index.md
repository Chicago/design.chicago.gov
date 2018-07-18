---
layout: page
title: Playbook
permalink: /playbook/index.html
description: Our complete design process.
---

{% assign parts = page.permalink | split: '/' %}
{% assign keyIndex = parts.size | minus: 2 %}
{% assign endURL = parts[keyIndex] %}

<ol class="index-ol">
{% assign links = site.playbook | where: "parent",endURL | sort: 'position' %}
    {% for link in links %}
      <ol>
        <li> <h2 class="index-link"> <a href="{{ link.url | prepend: site.baseurl }}"> {{ link.title }} </a> </h2> </li>
        <li class = "index-description"> {{link.description}} </li> 
      </ol>
      {% endfor %}
</ol>