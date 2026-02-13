---
layout: page
title: RapidDock
permalink: /research/projects/rapid-docking/
back_url: /research/
eyebrow: Research Project
subtitle: Accelerating protein-ligand docking with geometric deep learning.
---
{% assign project = site.data.projects | where: "id", "rapid-docking" | first %}
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
