---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---


{% include base_path %}

{% assign grouped_projects = site.projects | group_by: "categories" %}

{% for group in grouped_projects reversed%}
  {% assign clean_name = group.name | replace: '[', '' | replace: ']', '' | replace: '"', '' %}
  <h2>{{ clean_name }}</h2>
  <div class="project-grid">
    {% for post in group.items %}
<div style="display:flex; align-items:flex-start; gap:20px; margin-bottom:30px;">
  {% if post.header.teaser %}
    <a href="{{ post.url | relative_url }}">
      <img src="{{ post.header.teaser | relative_url }}" alt="{{ post.title }}"
           style="width:220px; height:auto; border-radius:8px; flex-shrink:0;">
    </a>
  {% endif %}

  <div style="flex:1;">
    <h3 style="margin-top:0;">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    {{ post.excerpt | markdownify }}
    {% if post.tags %}
      <p style="font-size:0.9em; color:#777;">{{ post.tags | join: " • " }}</p>
    {% endif %}
  </div>
</div>
      <!-- {% include archive-single.html %} -->
    {% endfor %}
  </div>
{% endfor %}
