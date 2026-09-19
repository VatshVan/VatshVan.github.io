---
title: Wildlife Hotspot Detector: Active Learning on Skewed Datasets
organization: DS203 Course Project | Guide: Prof. Vinay Kulkarni, IIT Bombay
date: 2025-10-01
date_end: 2025-11-20
draft: false
summary: Engineered HOG/GLCM/LAB feature vectors, Random Forest dimension reduction (750+ features), and an Active Learning loop with SMOTE and XGBoost GridSearchCV, attaining 0.85 F1-Score on highly skewed data.
tags:
  - Machine Learning
  - Active Learning
  - Feature Engineering
  - XGBoost
  - SMOTE
  - Computer Vision
---

Engineered an active learning machine learning pipeline to detect wildlife presence in large-scale, highly skewed ecological camera trap datasets with heavy background clutter.

### Methodology & Technical Highlights
* **Multi-Domain Feature Engineering**: Extracted complementary spatial and textural representations:
  - **Histogram of Oriented Gradients (HOG)** to capture structural outlines and animal silhouettes.
  - **Gray-Level Co-occurrence Matrix (GLCM)** to compute second-order statistical texture features (contrast, dissimilarity, homogeneity, energy).
  - **LAB Color Space** statistics to isolate luminance-invariant color distribution differences from complex vegetation backgrounds.
* **Dimensionality Reduction**: Evaluated feature importance across **750+ candidate dimensions** via Random Forest Mean Decrease in Impurity (MDI), discarding redundant features to curb the curse of dimensionality.
* **Active Learning with Class Rebalancing**:
  - Addressed extreme class imbalance (under 3% positive animal detections) by coupling **Synthetic Minority Over-sampling Technique (SMOTE)** with uncertainty-based active learning queries.
  - Strategically prioritized low-confidence boundary samples for label acquisition, minimizing human labeling budget by 60%.
* **Model Optimization**: Fine-tuned **XGBoost** hyperparameters via stratified 5-fold `GridSearchCV`, securing an **0.85 F1-Score** on previously unseen test environments.