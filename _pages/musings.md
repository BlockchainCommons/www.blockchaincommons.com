---
header:
  overlay_color: "#00f"
  overlay_filter: "0.35"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
title: Musings of a Trust Architect
cover: false
classes:
- wide
description: Musings of a Trust Architect contains Christopher Allen's foundational ideas and philosophies behind the technology of Blockchain Commons.
permalink: /musings.html
---

_Musings of a Trust Architect is a series of articles by [Life with Alacrity author](http://www.lifewithalacrity.com/) and Blockchain Commons founder Christopher Allen that lays out some of the foundational ideas and philosophies behind the technology of Blockchain Commons._

<ul>
  {% for post in site.categories.Musings %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.date | date: '%B %d, %Y' }}: {{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

_Header image by <a href="https://pixabay.com/users/elasticcomputefarm-1865639/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1474454">ElasticComputeFarm</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1474454">Pixabay</a>._
