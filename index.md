---
layout: default
title: Home
---
{% capture readme_content %}{% include_relative README.md %}{% endcapture %}

<main class="site-wrap">
  <header class="hero">
    <p class="eyebrow">GitHub Pages</p>
    <h1>{{ site.title }}</h1>
    <p class="subtitle">This page is generated from <code>README.md</code>.</p>
  </header>

  {% assign normalized = readme_content | strip %}
  {% if normalized == "" %}
  <section class="card">
    <h2>Add your content</h2>
    <p>Your <code>README.md</code> is currently empty. Add Markdown there and this page will render it automatically.</p>
  </section>
  {% else %}
  <article class="card markdown-body">
    {{ readme_content | markdownify }}
  </article>
  {% endif %}
</main>
