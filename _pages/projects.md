---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---


{% include base_path %}

{% assign grouped_projects = site.projects | group_by: "categories" %}

{% for group in grouped_projects %}
  <h2>{{ group.name }}</h2>
  <div class="project-grid">
    {% for post in group.items %}
      {% include archive-single.html %}
    {% endfor %}
  </div>
{% endfor %}
