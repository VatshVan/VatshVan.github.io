---
title: "Regime-Aware Portfolio Optimization"
organization: "Summer of Quant, Quant Club | IIT Bombay"
date: 2026-06-01
date_end: 2026-07-31
draft: false
summary: "Built a regime-switching portfolio optimizer combining Gaussian HMMs, Random Forest meta-models, and convex allocation across 503 equities with Purged 5-Fold CV and 250+ alpha features."
tags:
  - "Quantitative Finance"
  - "Hidden Markov Models"
  - "Convex Optimization"
  - "CUSUM Sampling"
  - "Triple Barrier Method"
  - "Purged K-Fold CV"
---

Developed an institutional-grade, regime-switching portfolio optimization system designed to dynamically adapt asset allocations across shifting market volatility and macroeconomic regimes.

### Core Mathematical & Algorithmic Contributions
* **Regime Identification with HMMs**: Trained Gaussian Hidden Markov Models (HMMs) on multi-asset macro and price time-series to classify latent market regimes (e.g., Low Volatility Trending, High Volatility Mean-Reverting, Crisis/Liquidity Contraction).
* **Event-Driven Labeling Framework**: Replaced arbitrary fixed-time horizon returns with financial ML standards:
  - Implemented **CUSUM filter sampling** to detect structural regime changes and information arrival events.
  - Employed the **Triple Barrier Method** with volatility-normalized dynamic thresholds to assign path-dependent trade labels (Profit-Take, Stop-Loss, Expiry).
* **High-Dimensional Factor Space**: Engineered **250+ alpha features** spanning cross-sectional price momentum, realized volatility term structures, volume profiles, and macroeconomic factor spaces.
* **Leakage Mitigation & Cross-Validation**: Addressed temporal autocorrelation and lookahead bias across a **503-equity S&P universe** using **Purged 5-Fold Cross-Validation**, **1% embargoes**, and sequential bootstrapping to preserve statistical independence.
* **Convex Capital Allocation**: Integrated Random Forest meta-models with convex portfolio optimization (Markowitz mean-variance with Ledoit-Wolf shrinkage covariance and CVaR tail-risk constraints).
