---
layout: page
title: Projects
permalink: /projects/
description:
nav: true
nav_order: 3
display_categories: []
horizontal: false
---

<!-- _pages/projects.md -->

<p class="project-gallery-intro">
  Here are some projects I have worked on for coursework and explored out of curiosity. Select a project to learn more or view its related paper.
</p>

{% assign sorted_projects = site.projects | sort: "importance" %}

<div class="project-gallery">
  {% for project in sorted_projects %}
    <article class="project-showcase-card">
      <div class="project-card-heading">
        <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
      </div>

      <a
        class="project-card-visual{% unless project.preview %} project-card-visual-placeholder{% endunless %}"
        href="{{ project.url | relative_url }}"
        aria-label="View {{ project.title }}"
      >
        {% if project.preview %}
          <img src="{{ project.preview | relative_url }}" alt="{{ project.preview_alt | default: project.title }}" loading="lazy">
        {% else %}
          <span>Project image coming soon</span>
        {% endif %}
      </a>

      <div class="project-card-body">
        <div class="project-card-meta">{{ project.period }} · {{ project.context }}</div>
        <p>{{ project.summary }}</p>

        <div class="project-card-links">
          <a href="{{ project.url | relative_url }}"><i class="fa-solid fa-arrow-right" aria-hidden="true"></i> Details</a>
          {% for link in project.links %}
            <a href="{{ link.url | relative_url }}"><i class="{{ link.icon }}" aria-hidden="true"></i> {{ link.label }}</a>
          {% endfor %}
        </div>
      </div>
    </article>

{% endfor %}

</div>
