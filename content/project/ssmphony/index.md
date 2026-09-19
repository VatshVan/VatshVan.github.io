---
title: "SSMphony: Linear-Complexity Audio Generation with Mamba & State Space Models"
organization: Independent Research
date: 2025-01-01
draft: false
summary: Explored linear-complexity State Space Models (SSM) and Mamba architectures for long-horizon audio synthesis, overcoming the quadratic attention bottlenecks of standard Transformer architectures.
tags:
  - Deep Learning
  - State Space Models
  - Mamba
  - Audio Generation
  - Linear Attention
  - Sequence Modeling
---

Explored modern State Space Models (SSMs) and selective structured state space architectures (Mamba) for continuous long-context audio and waveform synthesis.

### Technical Focus & Architectures
* **Overcoming Quadratic Bottlenecks**: Standard transformer-based autoregressive audio synthesis suffers from \(O(L^2)\) computational complexity, making high-sample-rate audio generation memory-prohibitive.
* **Continuous-Time State Space Discretization**: Formulated continuous state space dynamics:
  \[
  h'(t) = \mathbf{A} h(t) + \mathbf{B} x(t), \quad y(t) = \mathbf{C} h(t) + \mathbf{D} x(t)
  \]
  discretized via Zero-Order Hold (ZOH) to yield parallelizable convolutional training and \(O(1)\) recurrent inference per step.
* **Selective State Representation**: Leveraged input-dependent selection mechanisms to selectively propagate or filter out audio frequency bands, achieving high acoustic fidelity with sub-quadratic memory scaling.