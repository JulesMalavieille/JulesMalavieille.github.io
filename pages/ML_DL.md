---
layout: single
title: "Machine learning and Deep learning projects"
permalink: pages/ML_DL/
---

## Phytoplankton classification 
This self-initiated project aimed to strengthen my skills in machine learning and deep learning. The goal was to train and compare several supervised learning methods on spectrophotometric data of phytoplankton in order to predict their size class.

We implemented and compared four models: logistic regression, random forest, XGBoost, and a multi-layer perceptron (MLP). Hyperparameters for each method were optimized via cross-validation. Model performance was evaluated using accuracy on size class. 

The best results were achieved by XGBoost, closely followed by the random forest. The MLP also performed well despite the small dataset, but did not surpass the ensemble methods. Logistic regression achieved the lowest accuracy, as expected given its linear nature.

Download the full report : <a href="/assets/projet_ML_DL.pdf" class="btn btn--primary" target="_blank">📥 Download the full report</a>

See the code on the Github page of the project : <a href="https://github.com/JulesMalavieille/Phytoplankton-classification" class="btn btn--primary" target="_blank">🔗 View Project on GitHub</a> 


## Species occurrence modeling

This self-initiated project aimed to develop and validate a machine learning pipeline for predicting marine species occurrence from environmental data, with a particular focus on methodological rigor and ecological consistency. A key challenge addressed in this work was the absence problem inherent to presence-only datasets, which required the careful generation of pseudo-absence data based on ecological niche assumptions.

Environmental variables (e.g. temperature, salinity, oxygen, bathymetry) were combined with species occurrence records to construct a labeled dataset. A Random Forest classifier was trained to estimate the probability of species presence, with particular attention paid to data preprocessing, class balance, and model interpretability. Model performance was evaluated using standard classification metrics and ecological coherence checks rather than accuracy alone.

Beyond raw predictive performance, this project emphasized the robustness and realism of the predictions, including the spatial structure of probabilities and their consistency with known species ecology. The final output included both pointwise predictions and spatial probability maps, designed to be interpretable and usable for applied contexts such as ecological studies or decision support.

Download the full report : <a href="/assets/Modele_occurence.pdf" class="btn btn--primary" target="_blank">📥 Download the full report</a>

See the code on the Github page of the project : <a href="https://github.com/JulesMalavieille/Prevision-teleost-presence-" class="btn btn--primary" target="_blank">🔗 View Project on GitHub</a> 
