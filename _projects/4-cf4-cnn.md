---
title: "Revealing Hidden Cosmic Flows through the Zone of Avoidance with Deep Learning"
excerpt: "Built a 3D convolutional neural network (V-Net) to reconstruct dark-matter density and gravitational potential from incomplete galaxy peculiar velocity data. Achieved high correlation ($$r = 0.98$$) between predicted and true (simulated) fields, accurately recovering known cosmic structures such as the Great Attractor. Produced interactive 3D visualizations and automated data preprocessing pipelines for training on 12,000+ samples using TensorFlow and HPC GPUs."
collection: projects
tags: [Python, TensorFlow, Deep Learning, 3D CNN, Astrophysics, Cosmology, Data Reconstruction, PyVista, Matplotlib]
---

## Summary
This project introduces a deep-learning framework to reconstruct the 3D dark matter and velocity fields in the Zone of Avoidance (ZOA) — a region of the sky obscured by the Milky Way where traditional surveys are incomplete. Using a 3D V-Net convolutional neural network, trained on cosmological simulations (A-SIM), the model learns to infer both the dark matter density and gravitational potential from sparse galaxy peculiar velocity data. The derived velocity field accurately recovers known hidden structures, including the Great Attractor, confirming the model’s ability to map cosmic flows in regions with missing observations.

## Tech Stack
Python 3, TensorFlow, NumPy, h5py, Matplotlib, PyVista, tqdm, HDF5, HPC (NVIDIA A100 GPUs)

## Methods Overview
* Data: Used the Cosmicflows-4 galaxy catalog (17,000+ galaxies) and constructed CF4-like mock catalogs drawn from the A-SIM cosmological N-body simulation.
* Inputs: Galaxy number density ($$N_\mathrm{gal}$$) and mean radial peculiar velocity ($$V\mathrn{pec}$$) on 3D grids ($$128^3$$ voxels, 160 Mpc/h cube).
* Targets: Dark matter density ($$\rho$$) and gravitational potential ($$\phi$$) fields, smoothed to 1.25 Mpc/h resolution.
* Model: 3D V-Net CNN with encoder–decoder structure and reflection padding; trained separately for $$\rho$$ and $$\phi$$ prediction using MSE loss.
* Optimization: Used Adam optimizer with a triangular cyclic learning rate ($$10^{-7}–10^{-5}$$) over 200 epochs; training on dual NVIDIA A100 GPUs (80 GB).
* Validation: 11,512 total training samples (1,264 validation); performance tested on unseen mocks and statistical realizations of corrected CF4 data.

## Highlights
* Constructed a scalable 3D CNN for volumetric cosmological data (input tensor shape: $$2 \times 128 \times 128 \times 128$$).
* Predicted both density and potential fields, then derived the full 3D peculiar velocity field via physical gradients.
* Achieved Pearson r = 0.98 between predicted and true gravitational potential fields on validation data.
* Validated reconstructions through bulk flow statistics and cross-checks with independent observations.
* Recovered known clusters and voids in the ZOA, including the Great Attractor at $$(l, b) = (308.4°, 29.0°), cz \sim 4960 km/s)$$.
* Produced interactive 3D visualizations with PyVista, publicly viewable on Sketchfab, and 2D skymaps with Matplotlib.

**Publication:**  
Dupuy A., Jeong D., Hong S. E., Hwang H. S., Kim J., Courtois H. M. (Accepted, 2025). *Revealing Hidden Cosmic Flows through the Zone of Avoidance with Deep Learning.*  
*The Astrophysical Journal*, (in press). 
arXiv (coming soon)

<p align="center">
  <img src="/images/fig_cnn.png" width="100%">
</p>

*Figure: Comparison between the true and predicted three-dimensional fields from the trained convolutional neural network (CNN). The top row shows the dark matter density field and the bottom row shows the gravitational potential field. Left panels correspond to the ground truth from simulations, while right panels show the CNN predictions for a randomly selected validation sample. All panels represent the same SGX–SGY slice (−15 < SGZ < 15 Mpc/h). Arrows indicate the derived velocity field from each potential field, highlighting the network’s ability to recover coherent cosmic flows consistent with the underlying large-scale structure.*
