---
layout: page
title: Release Process
permalink: /new-additions/release-process/index.html
parent: new-additions
---
Recent changes to the Chicago Design System.
<ol class="index-ol">
{% for page in site.new-additions %}
    {% if page.parent == "release-process" %}
        <ol>
            <li> <h1 class="index-link"> <a href="{{ page.url | prepend: site.baseurl }}"> {{ page.title }} </a> </h1> </li>
            <li class = "index-description"> {{page.description}} </li> 
        </ol>
        {% endif %}
    {% endfor %}
</ol>