---
layout: page
title: Documentation
permalink: /docs/
---

# Documentation

Welcome to the {{ site.title }} Documentation pages!


<div class="section-index">
    <hr class="panel-line">
    {% assign sorted = site.docs | sort: 'date' | reverse %}
    {% for doc in sorted  %}
    <div class="entry">
    <h3><a href="{{ doc.url | prepend: site.baseurl }}">{{ doc.title }}</a></h3>
    <span class="post-date">{{ doc.date | date: "%B %d, %Y" }}</span><br>
    <p>{{ doc.description }}</p>
    </div>{% endfor %}
</div>
