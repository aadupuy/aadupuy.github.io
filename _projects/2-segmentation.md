---
title: "3D Segmentation of the Cosmic Velocity Field into Gravitational Basins"
excerpt: "Developed a high-performance C++ framework using VTK and MPI to segment the 3D cosmic velocity field into dynamically coherent regions ('watersheds'). This method identifies attractors, repellers and their respective gravitational basin by tracing streamlines through the velocity field, providing a physically motivated map of the large-scale structure of the Universe."
collection: projects
tags: [C++, VTK, MPI, HDF5, Eigen, Scientific Computing, Cosmology, Visualization]
---

## Summary
Designed and implemented a fully parallelized C++ codebase for cosmic flow analysis and segmentation of large-scale 3D cosmological fields. The method partitions the cosmic velocity field into gravitational basins using streamline integration and a watershed algorithm, providing a physically consistent way to define superclusters such as Laniakea and large repulsive regions.

## Tech Stack
C++14, VTK 9.4, MPI, Eigen3, HDF5, Python (post-processing)

## Highlights
* Implemented streamline tracing and watershed segmentation in C++ using the VTK visualization toolkit for 3D vector field processing.
* Integrated MPI parallelization for distributed execution on HPC clusters, supporting large velocity cubes (up to $$~512^3$$ voxels).
* Used Eigen for numerical operations and HDF5 for efficient I/O of 3D simulation and observational data.
* Developed modular code structure (filters.cpp, segmentation.cpp, streamlines.cpp, io.cpp) with CMake build system.
* Visualized segmented basins in 3D (interactive VTK renderings using Paraview or PyVista in Python + Vimeo or Sketchfab exports).
* Applied to both simulated and observational datasets from the Cosmicflows program to reveal the structure of nearby superclusters.

**Related publications:**  
Dupuy A., Courtois H. M., Dupont F., Denis F., Graziani R., Copin Y., Pomarède D., Libeskind N., Carlesi E., Tully R. B., Guinet D. (2019). *Partitioning the Universe into gravitational basins using the cosmic velocity field.* 
*Monthly Notices of the Royal Astronomical Society: Letters*, 489(1), L1–L6. 
[doi:10.1093/mnrasl/slz115](https://doi.org/10.1093/mnrasl/slz115) · [arXiv:1907.06555](https://arxiv.org/abs/1907.06555)

Courtois H. M., Kraan-Korteweg R. C., Dupuy A., Graziani R., Libeskind N. I. (2019). *A kinematic confirmation of the hidden Vela supercluster.* 
*Monthly Notices of the Royal Astronomical Society: Letters*, 490(1), L57–L61. 
[doi:10.1093/mnrasl/slz146](https://doi.org/10.1093/mnrasl/slz146) · [arXiv:1909.08875](https://arxiv.org/abs/1909.08875)

Dupuy A., Courtois H. M., Libeskind N. I., Guinet D. (2020). *Segmenting the Universe into dynamically coherent basins.* 
*Monthly Notices of the Royal Astronomical Society*, 493(3), 3513–3520. 
[doi:10.1093/mnras/staa536](https://doi.org/10.1093/mnras/staa536) · [arXiv:2002.06814](https://arxiv.org/abs/2002.06814)

Dupuy A., Courtois H. M. (2023). *Dynamic cosmography of the local Universe: Laniakea and five more watershed superclusters.* 
*Astronomy & Astrophysics*, 678, A176.
[10.1051/0004-6361/202346802](https://doi.org/10.1051/0004-6361/202346802) · [arXiv:2305.02339](https://arxiv.org/abs/2305.02339)

**Related Github repository:** [Dynamic Cosmography of the Local Universe](https://github.com/aadupuy/dynamic_cosmography)

<p align="center">
  <img src="/images/fig_segmentation.png" width="70%">
</p>

*Figure: Animated visualization of the cosmic velocity field segmentation (see [Vimeo link](https://vimeo.com/305959931/b85e36f10a)). This figure shows the relation between high-density peaks (in red) and streamlines of the peculiar velocity field in a ΛCDM simulation constrained to the Local Universe. Regions of high streamline density (yellow) trace cosmic filaments connecting clusters. Two automatically partitioned volumes are highlighted: the red mesh corresponds to a simulated Coma supercluster, and the blue mesh indicates a basin of repulsion.*