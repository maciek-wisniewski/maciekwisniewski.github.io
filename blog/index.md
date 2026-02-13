---
layout: page
title: Blog
permalink: /blog/
eyebrow: Blog
subtitle: Posts with dedicated subpages.
---
{% assign posts = site.data.blog.posts | sort: "date" | reverse %}
<div class="stack-list">
  {% for post in posts %}
  <article class="stack-item {% if post.featured %}featured{% endif %}">
    <p class="meta">{{ post.date }} · {{ post.read_time }}</p>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p>{{ post.excerpt }}</p>
    {% if post.tags %}<p class="tags">{{ post.tags | join: " · " }}</p>{% endif %}
    <a class="inline-link" href="{{ post.url | relative_url }}">Read post</a>
  </article>
  {% endfor %}
</div>
