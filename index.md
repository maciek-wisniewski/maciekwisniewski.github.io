---
layout: page
title: Maciej Wisniewski
permalink: /
eyebrow: Home
subtitle: Computational Scientist · AI for Molecular Biology and Toxicology
---
<div class="home-intro">
  {% assign profile_image = site.static_files | where: "path", "/assets/images/profile/maciej-wisniewski.jpg" | first %}
  {% if profile_image %}
  <img class="profile-photo" src="{{ '/assets/images/profile/maciej-wisniewski.jpg' | relative_url }}" alt="Maciej Wisniewski profile photo">
  {% else %}
  <div class="profile-photo-placeholder">
    <p class="photo-label">Profile photo placeholder</p>
    <p class="photo-path"><code>assets/images/profile/maciej-wisniewski.jpg</code></p>
  </div>
  {% endif %}
  <div>
    <p class="home-anchor">I develop machine-learning models and physics-informed methods for molecular dynamics, protein-ligand interactions, and mechanistic toxicity prediction.</p>
    <p>I am a computational researcher working at the intersection of machine learning, molecular dynamics, and systems biology. My work focuses on generative and flow-based models for molecular systems, protein structure and conformational dynamics, and physically grounded modeling for biomolecular data.</p>
    <p><strong>Research interests include:</strong></p>
    <ul>
      <li>Machine learning for molecular dynamics and protein structure</li>
      <li>Flow matching and diffusion models on geometric manifolds</li>
      <li>Protein-ligand and protein-protein interaction modeling</li>
      <li>Physics-informed and energy-based neural networks</li>
    </ul>
    <p>Currently based in Poland, working on independent and collaborative research projects in computational biology and AI-driven molecular modeling.</p>
    <p>See <strong>Research</strong> for ongoing projects and publications, and <strong>Blog</strong> for technical notes and research commentary.</p>
  </div>
</div>

<h2>Sections</h2>
<div class="link-grid">
  <a class="link-card" href="{{ '/news/' | relative_url }}">
    <h3>News</h3>
    <p>Latest scientific updates and announcements.</p>
  </a>
  <a class="link-card" href="{{ '/bio/' | relative_url }}">
    <h3>Bio</h3>
    <p>Detailed personal and professional biography.</p>
  </a>
  <a class="link-card" href="{{ '/research/' | relative_url }}">
    <h3>Research</h3>
    <p>Projects and papers with dedicated detail pages.</p>
  </a>
  <a class="link-card" href="{{ '/teaching/' | relative_url }}">
    <h3>Teaching</h3>
    <p>Course list with separate subpages for each course.</p>
  </a>
  <a class="link-card" href="{{ '/blog/' | relative_url }}">
    <h3>Blog</h3>
    <p>Post list with individual pages for each entry.</p>
  </a>
  <a class="link-card" href="{{ '/contact/' | relative_url }}">
    <h3>Contact</h3>
    <p>Social links and professional contact channels.</p>
  </a>
</div>
