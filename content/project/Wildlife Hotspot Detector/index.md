---
title: Wildlife Hotspot Detector
tags:
  - Active Learning
  - Feature Engineering
  - Supervised Learning
date: 2025-10-01
date_end: 2025-11-20
organization: Programming in Data Science (Course Project under Prof. Vinay Kulkarni)
draft: false
# image:
#   filename: featured.svg
#   focal_point: Smart
#   preview_only: false
---

* Engineered feature vectors (HOG, GLCM) to isolate texture variance, distinguishing signal from background
* Quantified feature importance via Random Forest ranking, reducing 750+ dimensions to maximize signal fidelity
* Architected Active Learning loops via Uncertainty Sampling, utilizing SMOTE to resolve class imbalance
* Optimized XGBoost hyperparameters via GridSearchCV, achieving 0.85 F1 on highly skewed datasets