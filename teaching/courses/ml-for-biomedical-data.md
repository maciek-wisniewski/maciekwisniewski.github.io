---
layout: page
title: Machine Learning for Biomedical Data
permalink: /teaching/courses/ml-for-biomedical-data/
back_url: /teaching/
eyebrow: Course
subtitle: Graduate course detail
---
{% assign course = site.data.teaching.teaching.courses | where: "id", "ml-for-biomedical-data" | first %}
<p class="meta">{{ course.semester }} · {{ course.year }} · {{ course.level }}</p>
<p><strong>Institution:</strong> {{ course.institution }}</p>
<p><strong>Schedule:</strong> {{ course.schedule }}</p>
<p><strong>Room:</strong> {{ course.room }}</p>
<p><strong>Credits:</strong> {{ course.credits }} · <strong>Students:</strong> {{ course.students }}</p>
<p>{{ course.description }}</p>

<h2>Course overview</h2>
<p>Hands-on modeling of high-dimensional biomedical datasets with robust validation, interpretability, and reproducibility standards.</p>
