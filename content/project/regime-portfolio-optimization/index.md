---
title: "Regime-Aware Portfolio Optimization"
organization: "Summer of Quant, Quant Club | IIT Bombay"
date: 2026-06-01
draft: false
summary: "Built a regime-switching portfolio optimizer combining Gaussian HMMs, Random Forest meta-models and convex allocation across 503 equities."
tags:
  - "Quantitative Finance"
  - "Hidden Markov Models"
  - "Convex Optimization"
  - "CUSUM Sampling"
---

### Executive Overview
Integrated Gaussian Hidden Markov Models (HMMs), Random Forest meta-models and convex portfolio optimization across 503 equities (2018–2024).

### Key Methodological Innovations
* **CUSUM Sampling & Triple Barrier Method**: Sampled informative event timestamps, filtering microstructural noise with 5-day horizon and 1.5x dynamic ATR thresholds.
* **Purged 5-Fold Cross-Validation**: Implemented with 1% embargo periods preventing information leakage.
* **Regime-Conditional Allocation**: Transitioned dynamically between Maximum Sharpe (bullish) and Hierarchical Risk Parity (high-volatility).
