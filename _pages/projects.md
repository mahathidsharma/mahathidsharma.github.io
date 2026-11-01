---
layout: page
title: Projects
permalink: /projects/
description: Research projects I have worked on.
nav: true
nav_order: 2
---

<!-- Projects: one list, two cards per row, ordered by the "importance" number (1 shows first) -->
<div class="projects">
  {% assign sorted_projects = site.projects | sort: "importance" %}
  <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
</div>
