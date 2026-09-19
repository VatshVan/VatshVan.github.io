---
title: Inverse Elasticity Physics-Informed Neural Network (PINN)
organization: ME218 Course Project | Guide: Prof. Sripriya Ramamoorthy, IIT Bombay
date: 2026-03-01
date_end: 2026-04-30
draft: false
summary: Direct Hybrid Collocation PINN estimating Young's modulus fields across 3 Additive Manufacturing lattice specimens. Unified 8 DIC anchors with 10,000+ Sobol points enforcing 2D Cauchy Momentum PDEs.
tags:
  - Machine Learning
  - Physics-Informed Neural Networks
  - Cauchy Momentum PDE
  - Inverse Problems
  - Sobol Collocation
  - Continuum Mechanics
---

Formulated and implemented a physics-informed deep learning architecture to solve the ill-posed inverse elasticity problem of reconstructing spatially varying material properties from sparse experimental surface measurements.

### Methodology & Mathematical Framework
* **Direct Hybrid Collocation Architecture**: Designed a deep neural network that represents displacement (\(u, v\)), stress (\(\sigma_{xx}, \sigma_{yy}, \sigma_{xy}\)), strain (\(\varepsilon\)), and the spatially distributed Young's modulus field (\(E(x,y)\)) across 3 distinct Additively Manufactured (AM) lattice specimens.
* **PDE-Constrained Multi-Objective Optimization**:
  - Embedded the governing **2D Cauchy Momentum balance equations** (\(\nabla \cdot \boldsymbol{\sigma} + \mathbf{b} = \mathbf{0}\)) directly into the neural network loss function using automatic differentiation.
  - Formulated a **7-objective composite loss** balancing boundary conditions, constitutive Hookean stress-strain relationships, and PDE residual compliance.
* **Sparse Anchor Fusion & Sampling**: Unified **8 Digital Image Correlation (DIC)** experimental anchor measurement zones with **10,000+ Sobol low-discrepancy collocation points** distributed across the domain interior to guide convergence without requiring destructive interior slicing.
* **Results**: Successfully reconstructed continuous modulus degradation gradients and identified local defect concentrations in 3D-printed meta-materials with high spatial fidelity.
