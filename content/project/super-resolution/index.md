---
title: Single Image Super Resolution with Deep Residual Networks
organization: ME228 Course Project | Guide: Prof. Neeraj Kumbhakarna, IIT Bombay
date: 2026-03-01
date_end: 2026-04-30
draft: false
summary: Enhanced Deep Super-Resolution (EDSR) with 32 residual blocks and PyTorch AMP. Achieved 34.84 dB PSNR and 0.939 SSIM on DIV2K, and 37.47 dB PSNR benchmarking SRCNN on Sen2Venus satellite imagery.
tags:
  - Deep Learning
  - Computer Vision
  - Super Resolution
  - EDSR
  - PyTorch AMP
  - Satellite Imagery
---

Engineered high-performance convolutional architectures for high-fidelity single image super-resolution (SISR), with applications ranging from photographic benchmarks to satellite earth observation.

### Technical Implementation & Results
* **Deep Residual Network Architecture (EDSR)**:
  - Constructed an Enhanced Deep Super-Resolution model utilizing **32 deep residual blocks** with removed batch normalization layers to preserve range flexibility and reduce memory overhead.
  - Employed sub-pixel convolution (pixel-shuffle) layers for efficient spatial feature upsampling.
* **Mixed-Precision Training & Memory Optimization**:
  - Leveraged **PyTorch Automatic Mixed Precision (AMP)** (FP16/FP32) to double training throughput while maintaining numerical stability.
  - Implemented dynamic spatial patch tiling during backpropagation and inference, effectively bounding peak VRAM allocation to prevent out-of-memory errors on large input tensors.
* **Benchmark Performance**:
  - Trained over **290,000 iterations** using an \(L_1\) pixel-loss objective, attaining a **34.84 dB PSNR** and **0.939 SSIM** on the standard **DIV2K** validation dataset.
  - Implemented and benchmarked an **SRCNN** on the **Sen2Venus** high-resolution satellite imagery dataset, achieving **37.47 dB PSNR** in reconstructing non-linear high-frequency spatial features from low-resolution multi-spectral bands.
