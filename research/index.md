---
layout: page
title: Research
permalink: /research/
eyebrow: Research
subtitle: Switch between projects and papers.
---
{% assign publication_years = "2026,2025,2024,2023" | split: "," %}
<div class="tab-actions" role="tablist" aria-label="Research tabs">
  <button type="button" class="tab-btn is-active" data-tab-target="projects" aria-selected="true">Projects</button>
  <button type="button" class="tab-btn" data-tab-target="papers" aria-selected="false">Papers</button>
</div>

<section id="tab-projects" class="tab-panel is-active" aria-live="polite">
  <div class="grid">
    {% for project in site.data.projects %}
    <article class="project-card">
      <p class="meta">{{ project.duration }} · {{ project.status }}</p>
      <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
      <p>{{ project.description }}</p>
      {% if project.tags %}<p class="tags">{{ project.tags | join: " · " }}</p>{% endif %}
      <a class="inline-link" href="{{ project.url | relative_url }}">Open project</a>
    </article>
    {% endfor %}
  </div>
</section>

<section id="tab-papers" class="tab-panel" aria-live="polite">
  {% for year in publication_years %}
  {% assign bucket = site.data.publications[year] %}
  {% if bucket and bucket.publications %}
  <div class="pub-year">
    <h3>{{ bucket.year }}</h3>
    <div class="stack-list">
      {% for pub in bucket.publications %}
      <article class="stack-item">
        <h4><a href="{{ pub.url | relative_url }}">{{ pub.title }}</a></h4>
        <p>{{ pub.authors | join: ", " }}</p>
        <p><em>{{ pub.journal }}</em> ({{ pub.year }})</p>
        <a class="inline-link" href="{{ pub.url | relative_url }}">Read paper details</a>
      </article>
      {% endfor %}
    </div>
  </div>
  {% endif %}
  {% endfor %}
</section>

<script>
  (function () {
    var buttons = document.querySelectorAll('.tab-btn');
    var panels = {
      projects: document.getElementById('tab-projects'),
      papers: document.getElementById('tab-papers')
    };

    function activate(tabName) {
      buttons.forEach(function (button) {
        var active = button.getAttribute('data-tab-target') === tabName;
        button.classList.toggle('is-active', active);
        button.setAttribute('aria-selected', active ? 'true' : 'false');
      });

      Object.keys(panels).forEach(function (name) {
        var active = name === tabName;
        panels[name].classList.toggle('is-active', active);
      });
    }

    buttons.forEach(function (button) {
      button.addEventListener('click', function () {
        activate(button.getAttribute('data-tab-target'));
      });
    });
  }());
</script>
