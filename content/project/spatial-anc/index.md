---
title: Spatial Active Noise Control via Virtual Acoustic Sensing
organization: ME791 Course Project | Guide: Prof. Sripriya Ramamoorthy, IIT Bombay
date: 2026-03-01
date_end: 2026-05-31
draft: false
summary: Virtual sensing framework for Spatial Active Noise Control using 4 remote microphones and an ObsTasNet deep observation-filter on 400 simulated acoustic scenes, achieving 12.6x faster pressure estimation.
tags:
  - Acoustic Signal Processing
  - Spatial ANC
  - ObsTasNet
  - Deep Learning
  - Virtual Sensing
  - Wave Physics
---

Engineered an advanced spatial acoustic signal processing framework enabling Active Noise Control (ANC) in unmonitored spatial zones without requiring intrusive physical microphones at human ear locations.

### Technical Innovations & Experiments
* **Virtual Sensing Framework Formulation**:
  - Addressed the fundamental spatial constraint of ANC where physical sensors cannot be placed inside the human ear canal or head volume during active operation.
  - Reconstructed the acoustic pressure field at target virtual microphone positions using pressure measurements streamed from a sparse array of **4 remote physical microphones**.
* **ObsTasNet Deep Observation-Filter**:
  - Adapted and trained an **ObsTasNet** (Time-domain Audio Separation Network) observation-filter on **400 rigorously simulated 3D acoustic room environments** exhibiting varying reverberation times (\(T_{60}\)) and reflection coefficients.
  - Learned the spatio-temporal Green's function transfer mapping between physical and virtual monitoring positions directly from raw pressure time-series.
* **Inference Speedup & Benchmarking**:
  - Benchmarked against classical analytical kernel interpolation and boundary element methods (BEM).
  - Achieved a **12.6× acceleration** in virtual microphone pressure estimation latency, meeting the hard real-time latency thresholds necessary for stable adaptive feedback anti-noise generation.
