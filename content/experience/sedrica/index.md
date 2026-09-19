---
title: "Controls & State Estimation Engineer"
organization: "SeDriCa (UMIC) - IIT Bombay"
company: "Unmesh Mashruwala Innovation Cell [UMIC]"
location: "IIT Bombay"
date: 2025-09-01
draft: false
summary: "Engineering India's first Level 5 autonomous car. Developing 100 Hz HyperMPC on LibTorch-Acados for 1/10 F1TENTH racing and Joint EKF RTK GNSS/IMU localization for a full-scale vehicle."
image:
  filename: "images.jpg"
  focal_point: "Smart"
  preview_only: false
tags:
  - "Autonomous Vehicles"
  - "HyperMPC @ 100 Hz"
  - "LibTorch-Acados C++"
  - "Joint EKF"
  - "RTK GNSS & IMU Fusion"
  - "Level 5 Autonomy"
---

Contributing to **SeDriCa**, IIT Bombay's premier autonomous vehicle tech team of 30+ students under the guidance of **Prof. Archak Mittal**, developing India's first Level 5 self-driving car customized for Indian road and traffic dynamics.

### F1TENTH Autonomous Racing | Autonomous Controls
* **Learned-Dynamics HyperMPC Runtime**: Engineering a high-performance `LibTorch`-`Acados` C++ runtime to deploy learned-dynamics HyperMPC at an ultra-low-latency **100 Hz control loop** on a 1/10-scale autonomous racecar.
* **GRU-Based Parameter Adaptation**: Developing a Gated Recurrent Unit (`GRU`) hyper-network architecture with B-spline control encoding to dynamically learn horizon-varying vehicle model parameters and tire friction coefficients under aggressive cornering maneuvers.

### Autonomous Golf Cart | Localization & State Estimation
* **Autonomous Localization Stack**: Building an end-to-end outdoor localization framework ensuring decimeter-level navigation precision using high-precision **RTK GNSS** receivers.
* **Joint Extended Kalman Filter (EKF)**: Formulating and deploying a Joint EKF that fuses high-rate IMU accelerometer and gyroscope telemetry with RTK GNSS positions to provide drift-free estimates of vehicle 6-DOF pose, linear velocity, and heading in real time.
* **Environmental Awareness & Perception Integration**: Collaborated with perception sub-teams on LiDAR point cloud registration and obstacle bounding box integration for real-time trajectory re-planning.