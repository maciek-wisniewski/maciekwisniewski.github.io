---
layout: page
title: Introduction to Bioinformatics and Computational Genomics
permalink: /teaching/courses/intro-to-bioinf-and-comp-genomics/
back_url: /teaching/
eyebrow: Course
subtitle: Undergraduate course detail
---
{% assign course = site.data.teaching.teaching.courses | where: "id", "intro-to-bioinf-and-comp-genomics" | first %}
<p class="meta">{{ course.semester }} · {{ course.year }} · {{ course.level }}</p>
<p><strong>Institution:</strong> {{ course.institution }}</p>
<p><strong>Schedule:</strong> {{ course.schedule }}</p>
<p><strong>Room:</strong> {{ course.room }}</p>
<p><strong>Credits:</strong> {{ course.credits }} · <strong>Students:</strong> {{ course.students }}</p>
<p>{{ course.description }}</p>

<h2>Learning objectives</h2>
<ul>
  <li>Build reproducible biomolecular analysis pipelines</li>
  <li>Apply statistical methods to sequencing datasets</li>
  <li>Communicate computational results clearly</li>
</ul>
