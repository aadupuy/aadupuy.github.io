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
  * Analyzed large-scale cosmological datasets to study the density and velocity fields of the local Universe.
  * Developed and trained deep learning models (3D CNNs / V-Net) in Python and TensorFlow for cosmic field reconstruction, including mock data generation for training samples and 3D visualizations.
  * Conducted statistical analysis and model fitting (chi-square minimization, growth rate parameter estimation, bulk flow measurement) on peculiar velocity surveys.
  * Produced 2D and 3D visualizations (interactive & publication ready) of density, velocity fields, and gravitational basins.
  * Collaborated internationally, co-authored multiple peer-reviewed publications and delivered research talks at international conferences and workshops on cosmology.

* March 2019 -- December 2021: Postdoctoral Researcher at Institut de Physique des 2 Infinis, Lyon, France
  * Conducted large-scale data analysis of velocity and density fields using Python (NumPy, Pandas, Matplotlib).
  * Developed 3D methods in C++ for cosmic structure segmentation, streamline tracing, and velocity field modeling to study the dynamics of the local Universe.
  * Implemented data processing and automation pipelines for HI observations (GBT) integrated into the Cosmicflows-4 catalog.
  * Applied statistical analyzes and model fitting (chi-square minimization, parameter estimation) to measure the growth rate of large-scale structures.
  * Published results in peer-reviewed journals (A&A, MNRAS) and collaborated with international research teams.
  * Delivered presentations and talks at international conferences and workshops on cosmology and large-scale structures.
 
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
