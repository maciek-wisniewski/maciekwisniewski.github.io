---
layout: default
title: Academic Portfolio
permalink: /
---
{% assign publication_years = "2026,2025,2024,2023" | split: "," %}
{% assign sorted_news = site.data.news | sort: "date" | reverse %}
{% assign sorted_blog = site.data.blog.posts | sort: "date" | reverse %}

<main class="site-main">
  <section id="home" class="section hero">
    <p class="eyebrow">Academic Portfolio</p>
    <h1>Modern research website powered by Jekyll + JSON</h1>
    <p class="lead">This template follows your README structure and renders core sections from modular data files.</p>
    <div class="hero-actions">
      <a class="btn btn-primary" href="#research">Explore Research</a>
      <a class="btn btn-ghost" href="#contact">Contact</a>
    </div>
  </section>

  <section id="news" class="section card">
    <div class="section-head">
      <h2>News</h2>
      <p>Latest scientific updates and announcements.</p>
    </div>
    <div class="stack-list">
      {% for item in sorted_news %}
      <article class="stack-item {% if item.featured %}featured{% endif %}">
        <p class="meta">{{ item.date }} · {{ item.type }}</p>
        <h3>{{ item.title }}</h3>
        <p>{{ item.description }}</p>
        {% if item.link %}
        <a href="{{ item.link }}">{{ item.link }}</a>
        {% endif %}
      </article>
      {% endfor %}
    </div>
  </section>

  <section id="bio" class="section card">
    <div class="section-head">
      <h2>Bio</h2>
      <p>Detailed personal and professional biography.</p>
    </div>
    <div class="two-col">
      <div>
        <h3>Professional profile</h3>
        <p>Replace this content with your biography, institution, career timeline, and current research mission.</p>
      </div>
      <div>
        <h3>Interests</h3>
        <ul>
          <li>Computational biology and AI-driven discovery</li>
          <li>Reproducible research engineering</li>
          <li>Interdisciplinary collaboration</li>
        </ul>
      </div>
    </div>
  </section>

  <section id="research" class="section card">
    <div class="section-head">
      <h2>Research</h2>
      <p>Projects and publications managed via JSON files.</p>
    </div>

    <h3 id="research-projects">Projects</h3>
    <div class="grid">
      {% for project in site.data.projects %}
      <article class="project-card">
        <p class="meta">{{ project.duration }} · {{ project.status }}</p>
        <h4>{{ project.title }}</h4>
        <p>{{ project.description }}</p>
        {% if project.tags %}
        <p class="tags">{{ project.tags | join: " · " }}</p>
        {% endif %}
      </article>
      {% endfor %}
    </div>

    <h3 id="research-publications">Articles / Publications</h3>
    {% for year in publication_years %}
    {% assign bucket = site.data.publications[year] %}
    {% if bucket and bucket.publications %}
    <div class="pub-year">
      <h4>{{ bucket.year }}</h4>
      <ol>
        {% for pub in bucket.publications %}
        <li>
          <strong>{{ pub.title }}</strong><br>
          {{ pub.authors | join: ", " }}<br>
          <em>{{ pub.journal }}</em> ({{ pub.year }}){% if pub.doi %}, DOI: {{ pub.doi }}{% endif %}
        </li>
        {% endfor %}
      </ol>
    </div>
    {% endif %}
    {% endfor %}
  </section>

  <section id="teaching" class="section card">
    <div class="section-head">
      <h2>Teaching</h2>
      <p>Current and previous courses with philosophy and supervision.</p>
    </div>
    <p>{{ site.data.teaching.teaching.teaching.intro }}</p>
    <p><strong>Teaching philosophy:</strong> {{ site.data.teaching.teaching.teaching.philosophy }}</p>
    <div class="supervision">
      <span>PhD: {{ site.data.teaching.teaching.teaching.supervision.phd_students }}</span>
      <span>Master: {{ site.data.teaching.teaching.teaching.supervision.master_students }}</span>
      <span>Undergraduate: {{ site.data.teaching.teaching.teaching.supervision.undergraduate_projects }}</span>
    </div>
    <div class="grid">
      {% for course in site.data.teaching.teaching.courses %}
      <article class="course-card">
        <p class="meta">{{ course.semester }} · {{ course.level }}</p>
        <h3>{{ course.title }}</h3>
        <p>{{ course.description }}</p>
        <p>{{ course.institution }} · {{ course.schedule }}</p>
        <p><code>{{ course.content }}</code></p>
      </article>
      {% endfor %}
    </div>
  </section>

  <section id="blog" class="section card">
    <div class="section-head">
      <h2>Blog</h2>
      <p>Personal blog posts and insights.</p>
    </div>
    <div class="stack-list">
      {% for post in sorted_blog %}
      <article class="stack-item {% if post.featured %}featured{% endif %}">
        <p class="meta">{{ post.date }} · {{ post.read_time }}</p>
        <h3>{{ post.title }}</h3>
        <p>{{ post.excerpt }}</p>
        {% if post.tags %}
        <p class="tags">{{ post.tags | join: " · " }}</p>
        {% endif %}
        <p><code>{{ post.content }}</code></p>
      </article>
      {% endfor %}
    </div>
  </section>

  <section id="contact" class="section card">
    <div class="section-head">
      <h2>Contact</h2>
      <p>Professional contact information and inquiry form.</p>
    </div>
    <div class="two-col">
      <div>
        <p><strong>Email:</strong> your.email@institution.edu</p>
        <p><strong>Institution:</strong> Your University</p>
        <p><strong>Department:</strong> Your Department</p>
      </div>
      <form class="contact-form">
        <label>Name<input type="text" name="name" placeholder="Your name"></label>
        <label>Email<input type="email" name="email" placeholder="you@example.com"></label>
        <label>Message<textarea name="message" rows="4" placeholder="Your message"></textarea></label>
        <button type="button" class="btn btn-primary">Send inquiry</button>
      </form>
    </div>
  </section>
</main>
