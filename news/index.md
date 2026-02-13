---
layout: page
title: News
permalink: /news/
eyebrow: News
subtitle: Latest scientific updates and announcements.
---
{% assign items = site.data.news | sort: "date" | reverse %}
<div class="stack-list">
  {% for item in items %}
  <article class="stack-item {% if item.featured %}featured{% endif %}">
    <p class="meta">{{ item.date }} · {{ item.type }}</p>
    <h3><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h3>
    <p>{{ item.description }}</p>
    <a class="inline-link" href="{{ item.url | relative_url }}">Read update</a>
  </article>
  {% endfor %}
</div>
