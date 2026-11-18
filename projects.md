---
layout: page
title: Projects
permalink: /projects/
lede: Labs and builds, with the repository linked on each card.
---

{% if site.data.projects.size > 0 %}
<ul class="project-grid">
  {% for project in site.data.projects %}
  <li>
    <a class="project-card" href="{{ project.url }}" target="_blank" rel="noopener noreferrer">
      <h2>{{ project.name }}</h2>
      <p>{{ project.description }}</p>
      {% if project.tags %}
      <ul class="tags">
        {% for tag in project.tags %}
        <li>{{ tag }}</li>
        {% endfor %}
      </ul>
      {% endif %}
      <span class="card-action">View repository<span class="visually-hidden"> (opens in a new tab)</span></span>
    </a>
  </li>
  {% endfor %}
</ul>
{% else %}
<p class="empty">No projects listed yet. Add one in <code>_data/projects.yml</code>.</p>
{% endif %}
