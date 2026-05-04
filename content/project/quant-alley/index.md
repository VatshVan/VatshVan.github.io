---
title: Chicago Quant Alley Trading Simulator and Optimizer
tags:
  - Crypto Derivatives
  - Options Trading
  - Multi-Armed Bandits
  - Backtesting
organization: Web and Coding CLub (Seasons of Code Program)
date: 2025-01-05
date_end: 2025-01-07
draft: false
# image:
#   filename: featured.svg
#   focal_point: Smart
#   preview_only: false
---

Designed and implemented a modular Python-based framework for developing, simulating, and optimizing algorithmic trading strategies in cryptocurrency markets.
This end-to-end system comprises three core modules:
* Historical Data Acquisition: Integrated with Delta Exchange API to fetch granular tick-level and order book data for futures and options.
* Event-Driven Simulation Engine: Built a high-fidelity backtester that models slippage, transaction costs, and execution mechanics. Supports both directional and complex derivatives strategies.
* Strategy Optimization: Leveraged Multi-Armed Bandit (MAB) algorithms to efficiently navigate the parameter search space, improving convergence and robustness of strategies.
* Showcased strategies included a dynamic trend-following system and a multi-leg options volatility strategy. Delivered performance analytics including Sharpe, Sortino, max drawdown and trade logs for each backtest iteration.
* Project GitHub: github.com/VatshVan/Chicago-Quant-Alley-Crypto-Trading-Simulator-Strategy-Optimizer