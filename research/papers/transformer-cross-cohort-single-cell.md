---
layout: page
title: Transformer Models for Cross-Cohort Single-cell Annotation
permalink: /research/papers/transformer-cross-cohort-single-cell/
back_url: /research/
eyebrow: Paper
subtitle: Publication details
---
{% assign bucket = site.data.publications["2024"] %}
{% assign pub = bucket.publications | where: "id", "transformer-cross-cohort-single-cell" | first %}
<p><strong>Authors:</strong> {{ pub.authors | join: ", " }}</p>
<p><strong>Venue:</strong> {{ pub.journal }} ({{ pub.year }})</p>
<p><strong>DOI:</strong> {{ pub.doi }}</p>
<p>{{ pub.abstract }}</p>
<p><strong>Keywords:</strong> {{ pub.keywords | join: ", " }}</p>
<p><a class="inline-link" href="{{ pub.pdf_url }}" target="_blank" rel="noopener noreferrer">PDF</a></p>
<p><a class="inline-link" href="{{ pub.code_url }}" target="_blank" rel="noopener noreferrer">Code</a></p>
