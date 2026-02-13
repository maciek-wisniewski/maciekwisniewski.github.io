---
layout: page
title: SingleCell Foundation Model
permalink: /research/projects/single-cell-foundation/
back_url: /research/
eyebrow: Research Project
subtitle: Transfer learning for single-cell transcriptomic annotation.
---
{% assign project = site.data.projects | where: "id", "single-cell-foundation" | first %}
<p class="meta">{{ project.duration }} · {{ project.status }}</p>
<p>{{ project.detailed_description }}</p>
<p><strong>Funding:</strong> {{ project.funding }}</p>
<p><strong>Collaborators:</strong> {{ project.collaborators | join: ", " }}</p>
<p><strong>Keywords:</strong> {{ project.tags | join: ", " }}</p>

<h2>Key achievements</h2>
<ul>
  {% for achievement in project.key_achievements %}
  <li>{{ achievement }}</li>
  {% endfor %}
</ul>

<p><a class="inline-link" href="{{ project.github_repo }}" target="_blank" rel="noopener noreferrer">GitHub repository</a></p>
<p><a class="inline-link" href="{{ project.website }}" target="_blank" rel="noopener noreferrer">Project website</a></p>
