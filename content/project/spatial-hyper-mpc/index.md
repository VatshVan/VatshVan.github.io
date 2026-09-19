---
title: Spatial Hyper-MPC with Neural Policy Distillation
organization: ME444 Course Project | Guide: Prof. Seshu Pasumarthy, IIT Bombay
date: 2026-03-01
date_end: 2026-04-30
draft: false
summary: Hybrid Neural-MPC controller for 6-DOF active suspension using OSQP and Joint EKF. Distilled a 40-step MPC into a 4,736-parameter neural policy via 20k expert trajectories, reducing peak angular velocities up to 3x.
tags:
  - Autonomous Controls
  - Model Predictive Control
  - Neural Policy Distillation
  - OSQP Solver
  - Joint EKF
  - 6-DOF Vehicle Dynamics
---

Engineered an ultra-fast, high-dimensional control framework for active vehicle suspension systems subjected to aggressive spatial road disturbances.

### Technical Architecture & Innovations
* **Formulation of 6-DOF Dynamic Suspension System**: Modeled full vehicle vertical, pitch, and roll dynamics coupled with non-linear actuator constraints and road profile kinematics.
* **Hybrid Neural-MPC Controller**:
  - Implemented an online Model Predictive Controller formulated as a convex Quadratic Program (QP) solved via the `OSQP` solver.
  - Coupled an online **Joint Extended Kalman Filter (EKF)** to estimate unmeasured chassis states and dynamic tire normal forces in real time.
* **Neural Policy Distillation for Real-Time Inference**:
  - Distilled a computationally demanding 40-step horizon MPC into a compact **4,736-parameter deep neural policy network** trained over **20,000 expert simulation trajectories** using behavioral cloning and DAgger.
  - Reduced solver latency from 15ms (unsuitable for high-frequency chassis stabilization) to under **0.3ms**, enabling microsecond-level execution.
* **Rigorous Benchmarking**: Validated against extensively tuned Multi-Input Multi-Output (MIMO) PID baselines across 3 standardized terrain profiles, demonstrating up to **3× reduction in peak angular velocities** (pitch and roll).
