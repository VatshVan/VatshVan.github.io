---
title: "Mathematics of Derivative Pricing: Theory and Computational Implementation"
publication: "SSRN Electronic Journal (Pre-Print ID: 6439720) & IIT Bombay"
date: 2025-07-15
draft: false
summary: "Rigorous investigation into stochastic calculus, Black-Scholes PDE derivation, equivalent martingale measures, Greeks sensitivity analysis, and Monte Carlo option pricing engines."
url_ssrn: "https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6439720"
ssrn_id: "6439720"
orcid: "0009-0001-7236-8213"
author_ssrn: "https://papers.ssrn.com/sol3/cf_dev/AbsByAuth.cfm?per_id=10485196"
url_pdf: "https://drive.google.com/file/d/1f_SgJi7vGpL9-7TIhU96r7zdb4itlnQH/view?usp=sharing"
tags:
  - "SSRN Pre-print"
  - "Black-Scholes PDE"
  - "Stochastic Calculus"
  - "Martingale Pricing"
  - "Monte Carlo Simulation"
  - "Greeks Sensitivity"
---

### Abstract
This technical monograph explores the mathematical foundations and computational realization of modern derivative pricing. Beginning with discrete binomial lattices and Brownian motion kinematics, we derive the fundamental Black-Scholes partial differential equation under non-arbitrage principles and Feynman-Kac representations. We formulate numerical schemes using both vectorized Monte Carlo methods with antithetic variate variance reduction and finite-difference PDE solvers for early-exercise American options. Complete Python workflows evaluate Greeks surfaces and delta-hedging performance under realistic volatility and transaction frictions.

---

### Publication & Pre-print Details
* **SSRN Pre-print**: [https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6439720](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6439720) (Abstract ID: `6439720`)
* **SSRN Author Profile**: [Vatsh Van on SSRN (Author ID: 10485196)](https://papers.ssrn.com/sol3/cf_dev/AbsByAuth.cfm?per_id=10485196)
* **Author ORCID**: [0009-0001-7236-8213](https://orcid.org/0009-0001-7236-8213)
* **Primary Affiliation**: Department of Mechanical Engineering & Centre for Machine Intelligence and Data Science (CMInDS), Indian Institute of Technology Bombay
* **Full Technical Report (PDF)**: [View on Google Drive](https://drive.google.com/file/d/1f_SgJi7vGpL9-7TIhU96r7zdb4itlnQH/view?usp=sharing)
* **Open-Source Code**: [GitHub Repository `Mathematics_Of_Pricing_Derivatives`](https://github.com/VatshVan/Mathematics_Of_Pricing_Derivatives)

---

### Theoretical Architecture & Mathematical Formulations

#### 1. Stochastic Calculus & Itô's Lemma
Under a filtered probability space \((\Omega, \mathcal{F}, (\mathcal{F}_t)_{t \ge 0}, \mathbb{P})\), the asset price \(S_t\) follows geometric Brownian motion (GBM):
$$ dS_t = \mu S_t dt + \sigma S_t dW_t $$
Applying Itô's formula to a twice continuously differentiable derivative pricing function \(V(S_t, t)\):
$$ dV = \left( \frac{\partial V}{\partial t} + \mu S \frac{\partial V}{\partial S} + \frac{1}{2}\sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} \right) dt + \sigma S \frac{\partial V}{\partial S} dW_t $$

#### 2. Risk-Neutral Valuation & Black-Scholes PDE
By constructing a self-financing delta-hedged portfolio \(\Pi_t = V_t - \Delta_t S_t\) with \(\Delta_t = \frac{\partial V}{\partial S}\), the stochastic \(dW_t\) term vanishes:
$$ \frac{\partial V}{\partial t} + r S \frac{\partial V}{\partial S} + \frac{1}{2}\sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} - rV = 0 $$

#### 3. Numerical Implementations
* **Vectorized Monte Carlo Simulation**: Antithetic variates variance reduction achieving \(\mathcal{O}(1/\sqrt{N})\) convergence across 1,000,000 paths.
* **Finite-Difference Solvers**: Crank-Nicolson implicit-explicit discretization for American put options with free boundary conditions.
* **Greeks Surfaces**: Exact closed-form and finite-difference evaluations of Delta (\(\Delta\)), Gamma (\(\Gamma\)), Vega (\(\nu\)), Theta (\(\Theta\)), and Rho (\(\rho\)).
