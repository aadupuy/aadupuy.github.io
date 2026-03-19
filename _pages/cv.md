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
* March 2022 -- March 2026: Research Fellow at Korea Institute for Advanced Study
  * Designed and implemented a 3D CNN model (V-Net) to reconstruct missing signals from incomplete and noisy data, achieving a correlation coefficient of 0.98 between model predictions and ground truth.
  * Applied models to noisy, real-world data, bridging model development and real data applications.
  * Improved model performance through hyperparameter tuning, dataset refinement, and custom loss design.
  * Built automated preprocessing pipelines for 12,000+ 3D datasets, reducing manual effort.
  * Trained and optimized models on GPU and HPC environments, using SLURM for distributed job scheduling.
  * Communicated results through publications and presentations, and collaborated with international teams.

* March 2019 -- December 2021: Postdoctoral Researcher at Institut de Physique des 2 Infinis, Lyon, France
  * Developed C++ and Python frameworks for large-scale 3D data processing and spatial partitioning of 3D datasets.
  * Applied statistical and regression models in Python  to analyze datasets and estimate key parameters.
  * Designed data preprocessing and cleaning pipelines to improve data consistency and reduce manual effort.
  * Built 2D and 3D visualization tools to explore spatial patterns and communicate results.
  * Collaborated with international teams on data integration, model evaluation.
 
Education
======
* Ph.D in in Astrophysics — Institut de Physique des 2 Infinis & Université Claude Bernard Lyon 1, France, 2018
* M.Sc. in Physics (Astrophysics) — Université Claude Bernard Lyon 1, France & Wuhan University, China, 2015
* B.Sc. in Physics (graduated with Honors) — Université Claude Bernard Lyon 1 & École Normale Supérieure de Lyon, France, 2013

Skills
======
* Machine Learning & Deep Learning: TensorFlow, Keras (deep learning model development), CNNs
* Programming:  Python (NumPy, Pandas, SciPy, Scikit-learn ML workflows), C++, SQL
* Data Processing & Visualization: Matplotlib, PyVista, Paraview, VTK
* Tools: Git, Jupyter Notebook, HPC (GPU training, SLURM job scheduling)

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
