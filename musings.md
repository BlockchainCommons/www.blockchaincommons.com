---
cover: false
hide_description: true
permalink: /musings.html
---
<ul>
  {% for post in site.categories.musings %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
