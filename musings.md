---
title: "Musings of an Architect"
cover: false
hide_description: true
permalink: /musings.html
---

_Musings of an Architect is a series of articles by [Life with Alacrity author](http://www.lifewithalacrity.com/) and Blockchain Commons founder Christopher Allen that lays out some of the foundational ideas and philosophies behind the technology of Blockchain Commons._

<ul>
  {% for post in site.categories.Musings %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.date }}: {{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
