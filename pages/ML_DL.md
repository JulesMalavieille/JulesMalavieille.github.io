---
layout: single
title: "Machine learning and Deep learning projects"
permalink: pages/ML_DL/
---

## Phytoplankton classification 
This self-initiated project aimed to strengthen my skills in machine learning and deep learning. The goal was to train and compare several supervised learning methods on spectrophotometric data of phytoplankton in order to predict their size class.

We implemented and compared four models: logistic regression, random forest, XGBoost, and a multi-layer perceptron (MLP). Hyperparameters for each method were optimized via cross-validation. Model performance was evaluated using accuracy on size class. 

The best results were achieved by XGBoost, closely followed by the random forest. The MLP also performed well despite the small dataset, but did not surpass the ensemble methods. Logistic regression achieved the lowest accuracy, as expected given its linear nature.
