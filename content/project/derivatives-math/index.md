---
title: Mathematics of Derivative Pricing & Risk Neutral Valuation
organization: Summer of Science, Maths & Physics Club | IIT Bombay
date: 2025-05-01
date_end: 2025-07-31
draft: false
summary: Theoretical derivation and computational implementation of the Black-Scholes PDE, martingale pricing, Greeks sensitivity analysis, and Monte Carlo option pricing engines in Python.
tags:
  - Quantitative Finance
  - Black-Scholes PDE
  - Stochastic Calculus
  - Greeks Sensitivity
  - Martingale Pricing
  - Monte Carlo Simulation
---

A comprehensive theoretical and computational investigation into continuous-time mathematical finance, asset pricing models, and risk-neutral valuation frameworks.

### Mathematical Exploration & Computational Implementations
* **Stochastic Calculus & Black-Scholes Formulation**: Derived the Black-Scholes Partial Differential Equation (PDE) via geometric Brownian motion dynamics and dynamic replication under the absence of arbitrage. Applied the Feynman-Kac theorem to solve the PDE under risk-neutral equivalent martingale measures (\(\mathbb{Q}\)).
* **Numerical Pricing Engines**:
  - Implemented high-performance vectorized Monte Carlo pricing engines with antithetic variate variance reduction for exotic and path-dependent options.
  - Implemented binomial lattice models (Cox-Ross-Rubinstein) and finite-difference PDE schemes for American-style early exercise boundary determination.
* **Sensitivity Analysis & Payoff Engineering**: Computed full analytical and numerical Greeks (\(\Delta, \Gamma, \mathcal{V}, \Theta, \rho\)) across implied volatility smiles and time-to-maturity surfaces.
* **Hedging Strategies**: Simulated dynamic delta and gamma hedging portfolios under discrete rebalancing intervals to measure residual hedging slippage and gamma risk.
* **Repository**: [GitHub: Mathematics_Of_Pricing_Derivatives](https://github.com/VatshVan/Mathematics_Of_Pricing_Derivatives)
* **Project Report**: [Google Drive Technical Report](https://drive.google.com/file/d/1f_SgJi7vGpL9-7TIhU96r7zdb4itlnQH/view?usp=sharing)
