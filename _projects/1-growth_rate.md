---
title: "Estimating the Cosmological Growth Rate from Peculiar Velocity Correlations"
excerpt: "
Built a statistical inference framework to estimate the cosmological growth rate parameter $$f\\sigma_8$$ from galaxy peculiar velocity correlations.  Automated data loading, binning, and Monte Carlo uncertainty propagation across 100+ realisations using NumPy and SciPy. Implemented a $$\\chi^2$$-based  model fitting via iminuit and produced publication-ready data visualizations, validating results against ΛCDM predictions."
collection: projects
tags: [Python, Statistics, Cosmology, Data Analysis, Visualization]
---

## Summary
Developed a full data analysis and inference pipeline to estimate the local cosmological growth rate $$f\sigma_8$$ using galaxy peculiar velocity correlations from the Cosmicflows-4 catalog. The project integrated observational data processing, statistical modeling, Monte Carlo uncertainty propagation, and $$\chi^2$$-based parameter inference.

## Tech Stack
Python, NumPy, Pandas, SciPy, iminuit, Matplotlib, tqdm, HDF5, HPC

## Highlights
* Designed an end-to-end pipeline for loading, filtering, and binning large-scale galaxy catalogs (>$$10^4$$ galaxies).
* Computed two-point velocity correlation functions $$\Psi_1$$, $$\Psi_2$$ using vectorized NumPy operations and Monte Carlo error propagation (100+ realizations).
* Implemented custom statistical fitting routines with $$\chi^2$$ minimization (via Minuit) to infer $$f\sigma_8$$ and its uncertainty.
* Compared fitted results across cosmic environments (voids, filaments, knots) and validated them against ΛCDM predictions.
* Produced publication-ready visualizations of velocity correlation functions and parameter fits.

**Publication:**  
Dupuy A., Courtois H. M., Kubik B. (2019). *An estimation of the local growth rate from Cosmicflows peculiar velocities.*  
*Monthly Notices of the Royal Astronomical Society*, 486(1), 440–448.  
[doi:10.1093/mnras/stz901](https://doi.org/10.1093/mnras/stz901) · [arXiv:1901.03530](https://arxiv.org/abs/1901.03530)

<p align="center">
  <img src="/images/fig_growth_rate.png" width="80%">
</p>

*Figure: Comparison of the inferred growth rate (blue point) with ΛCDM predictions (black curve) and other observational probes. Computed using custom $$\chi^2$$ fitting on Cosmicflows-3 velocity data.*
