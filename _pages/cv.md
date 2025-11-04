---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---


{% include base_path %}

Work experience
======
* March 2022 -- Present: Research Fellow at Korea Institute for Advanced Study
  * Duties

* March 2019 -- December 2021: Postdoctoral Researcher at Institut de Physique des 2 Infinis, Lyon, France
  * Duties
 
Education
======
* Ph.D in in Astrophysics — Institut de Physique des 2 Infinis & Université Claude Bernard Lyon 1, France, 2018
* M.Sc. in Physics (Astrophysics) — Université Claude Bernard Lyon 1, France & Wuhan University, China, 2015
* B.Sc. in Physics (graduated with Honors) — Université Claude Bernard Lyon 1 & École Normale Supérieure de Lyon, France, 2013

Skills
======
* Programming & data analysis: Python (NumPy, Pandas, Scikit-learn), C++, SQL
* Machine & deep learning: TensorFlow, Keras, CNNs
* Data visualization: Matplotlib, PyVista
* Tools & software: Jupyter Notebook, Git, LaTeX

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
