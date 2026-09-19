---
title: "Chicago Quant Alley: Crypto Trading Simulator & Optimizer"
organization: "Seasons of Code, Web and Coding Club | IIT Bombay"
date: 2025-05-01
date_end: 2025-07-31
draft: false
summary: "Engineered a mid-frequency Bitcoin options/futures simulator with slippage modeling, async ccxt API execution, dynamic strike selection, and Multi-Armed Bandit hyperparameter optimization."
tags:
  - "Quantitative Finance"
  - "Crypto Derivatives"
  - "Options Trading"
  - "Multi-Armed Bandits"
  - "Async CCXT"
  - "Backtesting Engine"
---

Designed and deployed a modular, high-throughput Python framework for developing, simulating, and systematically optimizing quantitative trading strategies in cryptocurrency derivative markets.

### Architecture & System Modules
* **Asynchronous Market Data Pipeline**: Built an event-driven data ingestion layer integrating with the **Delta Exchange API** and `ccxt` async routines to capture granular tick-level trades, order book depth, and implied volatility surfaces with minimal latency.
* **Realistic Execution Simulation**: Formulated a simulation engine that faithfully replicates market microstructure frictions:
  - Models non-linear market impact, dynamic slippage, and tiered taker/maker fee schedules.
  - Implements realistic order queue priority and partial fill mechanics for limit orders.
* **Dynamic Options Lifecycle & Greeks Management**: Engineered dynamic strike selection and continuous risk monitoring covering real-time portfolio Greeks (Delta, Gamma, Vega, Theta), margin utilization, automated roll strategies, and drawdown controls.
* **Multi-Armed Bandit (MAB) Strategy Tuning**: Deployed Upper Confidence Bound (UCB) and Thompson Sampling algorithms to optimize strategy hyperparameters, balancing exploration of parameter regimes with exploitation of top-performing parameter sets for rapid convergence.
* **Repository**: [GitHub: Chicago-Quant-Alley](https://github.com/VatshVan/Chicago-Quant-Alley-Crypto-Trading-Simulator-Strategy-Optimizer)