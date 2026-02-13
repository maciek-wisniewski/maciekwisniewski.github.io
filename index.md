---
layout: page
title: Maciej Wisniewski
permalink: /
eyebrow: Home
subtitle: Computational Scientist · AI for Molecular Biology and Toxicology
hero_wide: true
---
<div class="home-intro">
  <div class="profile-frame" id="profile-frame">
    <img class="peptide-asset" src="{{ '/assets/images/profile/peptide-asset-1.png' | relative_url }}" alt="" aria-hidden="true">
    {% assign profile_image = site.static_files | where: "path", "/assets/images/profile/maciej-wisniewski.jpg" | first %}
    {% if profile_image %}
    <img class="profile-photo" src="{{ '/assets/images/profile/maciej-wisniewski.jpg' | relative_url }}" alt="Maciej Wisniewski profile photo">
    {% else %}
    <div class="profile-photo-placeholder">
      <p class="photo-label">Profile photo placeholder</p>
      <p class="photo-path"><code>assets/images/profile/maciej-wisniewski.jpg</code></p>
    </div>
    {% endif %}
  </div>
  <div class="home-text">
    <p class="home-anchor">I develop machine-learning models and physics-informed methods for Molecular Dynamics Simulations, protein-ligand interactions and biomolecular complexes.</p>
    <p>I am a computational researcher working at the intersection of machine learning, bioinformatics, and pharmacy. My work focuses on generative and flow-based models for molecular systems, protein structure and conformational dynamics, and physically grounded modeling for biomolecular data.</p>
    <p><strong>Research interests include:</strong></p>
    <ul>
      <li>Explainable Deep Learning</li>
      <li>Flow Matching and Diffusion models algorythms</li>
      <li>Protein-ligand and protein-protein interaction modeling</li>
      <li>Physics-informed and energy-based neural networks</li>
    </ul>
    <p>Currently based in Poland, working on independent and collaborative research projects in computational biology and AI-driven molecular modeling.</p>
  </div>
</div>

<h2>Explore the site</h2>
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

<script>
  (function () {
    var frame = document.getElementById('profile-frame');
    if (!frame) return;

    frame.addEventListener('mouseenter', function () {
      frame.classList.add('is-peptide-active');
    });

    frame.addEventListener('mouseleave', function () {
      frame.classList.remove('is-peptide-active');
    });
  }());
</script>
