---
header:
  overlay_color: "#00f"
  overlay_filter: "0.35"
  overlay_image: /images/blueprints-letters.jpg
  og_image: /images/dispatches-card.jpg
title: Dispatches of a Trust Architect
cover: false
permalink: /dispatches/
redirect_from: /dispatches.html
classes:
- wide
description: Dispatches of a Trust Architect contains Christopher Allen's conversations with other trust architects.
sidebar:
  nav: subpages
---

Dispatches of a Trust Architect is a series of articles by [Life with Alacrity author](http://www.lifewithalacrity.com/) and Blockchain Commons founder Christopher Allen that engages in dialogue with other trust architects and their articles, panels, talks, and other discussions about trust, coercion, privacy, censorship, and other issues with digital architectures.

<ul>
  {% for post in site.categories.Dispatches %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.date | date: '%B %d, %Y' }}: {{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

<font size="-1">_Header image by <a href="https://pixabay.com/users/elasticcomputefarm-1865639/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1474454">ElasticComputeFarm</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1474454">Pixabay</a>._</font>
