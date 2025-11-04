---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---


{% include base_path %}

{% assign grouped_projects = site.projects | group_by: "categories" %}

{% for group in grouped_projects %}
  {% assign clean_name = group.name | replace: '[', '' | replace: ']', '' | replace: '"', '' %}
  <h2>{{ clean_name }}</h2>
  <div class="project-grid">
    {% for post in group.items %}
      {% include archive-single.html %}
    {% endfor %}
  </div>
{% endfor %}
