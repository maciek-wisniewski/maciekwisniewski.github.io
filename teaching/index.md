---
layout: page
title: Teaching
permalink: /teaching/
eyebrow: Teaching
subtitle: Courses with dedicated subpages.
---
<p>{{ site.data.teaching.teaching.teaching.intro }}</p>
<p><strong>Teaching philosophy:</strong> {{ site.data.teaching.teaching.teaching.philosophy }}</p>

<div class="supervision">
  <span>PhD: {{ site.data.teaching.teaching.teaching.supervision.phd_students }}</span>
  <span>Master: {{ site.data.teaching.teaching.teaching.supervision.master_students }}</span>
  <span>Undergraduate: {{ site.data.teaching.teaching.teaching.supervision.undergraduate_projects }}</span>
</div>

<div class="grid">
  {% for course in site.data.teaching.teaching.courses %}
  <article class="course-card {% if course.featured %}featured{% endif %}">
    <p class="meta">{{ course.semester }} · {{ course.level }}</p>
    <h3><a href="{{ course.url | relative_url }}">{{ course.title }}</a></h3>
    <p>{{ course.description }}</p>
    <p>{{ course.institution }} · {{ course.schedule }}</p>
    <a class="inline-link" href="{{ course.url | relative_url }}">Open course page</a>
  </article>
  {% endfor %}
</div>
