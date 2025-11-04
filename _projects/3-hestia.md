---
title: "Anisotropic Satellite Accretion onto the Local Group with HESTIA"
excerpt: "Analyzed high-resolution cosmological simulations (HESTIA suite) to study the directional accretion of satellites onto the Milky Way and Andromeda galaxies. Extracted velocity shear and tidal tensors, traced satellite infall trajectories, and identified large-scale anisotropies aligned with the cosmic web."
collection: projects
tags: [Python, NumPy, Pandas, Astrophysics, Tensor Analysis, Cosmological Simulations, Visualization]
---

## Summary
This project investigates how the cosmic web channels matter onto galaxies in the Local Group. Using the HESTIA constrained simulations, I developed a full analysis pipeline to identify and quantify the anisotropy of satellite accretion around the Milky Way and Andromeda. The study compares satellite infall directions with the eigenvectors of the local velocity shear and tidal tensors, revealing a strong alignment with the axis of slowest collapse ($$\vec{e}_3$$), implying that satellite accretion is guided by the surrounding filamentary structure of the cosmic web.

## Tech Stack
Python 3, NumPy, h5py, Matplotlib, Astropy, pandas, Jupyter

## Highlights
* Extracted and diagonalized 3D velocity shear and tidal tensors from HESTIA simulation snapshots.
* Computed eigenvectors ($$\vec{e}_1$$, $$\vec{e}_2$$, $$\vec{e}_3$$) of each tensor field to characterize local flow anisotropy.
* Developed Python scripts for large-scale tensor field analysis and trajectory extraction.
* Quantified alignment statistics between satellite infall vectors and cosmic web eigenframes, distinguishing between early and late accretion epochs.
* Visualized directional distributions on Aitoff projections and generated 3D renderings of the local velocity field.
* Published results demonstrating that Local Group satellites are funneled along coherent large-scale structures of the cosmic web.

**Publication:**  
Dupuy A., Libeskind N. I., Hoffman Y., Courtois H. M., Gottlöber S., Grand R. J. J., Knebe A., Sorce J. G., Tempel E., Tully R. B., Vogelsberger M., Wang P. (2022). *Anisotropic satellite accretion on to the Local Group with HESTIA.* 
*Monthly Notices of the Royal Astronomical Society*, 516(3), 4576–4584. 
[doi:10.1093/mnras/stac2486](https://doi.org/10.1093/mnras/stac2486) · [arXiv:2208.14648](https://arxiv.org/abs/2208.14648)


<p align="center">
  <img src="/images/fig_hestia.png" width="120%">
</p>

*Figure: Aitoff projection showing the sky distribution of satellite infall directions in supergalactic coordinates. The background map encodes the probability density of infall positions. Circles and labels mark the principal axes ($$\vec{e}_1$$, $$\vec{e}_2$$, $$\vec{e}_3$$) of the local velocity shear tensor. The red cross represents the mean infall direction, aligned with $$\vec{e}_3$$, indicating that satellites are preferentially accreted along the axis of slowest collapse.*