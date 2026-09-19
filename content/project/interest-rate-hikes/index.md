---
title: Effects of Interest Rate Hikes on Financial Markets & Vasicek Modeling
organization: FINSEARCH, Finance Club | IIT Bombay
date: 2026-06-01
date_end: 2026-07-31
draft: false
summary: Empirical analysis of 20+ years of RBI monetary policy tightening cycles and simulation of bond price sensitivity and yield curves using the Vasicek short-rate model.
tags:
  - Quantitative Finance
  - Fixed Income
  - Vasicek Model
  - Macroeconomics
  - Monetary Policy
  - Stochastic Rates
---

Empirical macro-financial research analyzing the transmission mechanism of central bank monetary policy tightening cycles onto domestic equity and sovereign debt markets.

### Research Scope & Methodological Framework
* **Empirical RBI Policy Analysis**: Curated and synthesized **20+ years of Reserve Bank of India (RBI) monetary policy decisions**, identifying structural tightening regimes (repo rate hikes), liquidity absorption mechanisms (CRR/SLR adjustments), and their corresponding macroeconomic drivers (CPI inflation surges, currency depreciations, fiscal deficits).
* **Yield Curve & Term Structure Modeling**:
  - Implemented the **Vasicek one-factor short-rate model** (\(dr_t = a(b - r_t)dt + \sigma dW_t\)) capturing mean-reverting interest rate dynamics.
  - Calibrated model parameters (\(a, b, \sigma\)) via Maximum Likelihood Estimation (MLE) against historical interbank call money rates.
* **Bond Price Sensitivity & Duration Analysis**:
  - Simulated theoretical sovereign zero-coupon and coupon-bearing bond yield curves under various policy rate trajectory paths.
  - Evaluated effective duration and convexity shifts to assess market portfolio vulnerability during rate hike cycles.
