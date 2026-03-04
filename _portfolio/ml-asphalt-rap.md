---
title: "Machine Learning–Based Performance Prediction for High-RAP Asphalt Mixtures"
collection: portfolio
permalink: /project/ml-balanced-mix-design
excerpt: "Regression-based machine learning framework for predicting rutting, cracking, and moisture resistance of asphalt mixtures and identifying feasible design regions under traffic-level constraints."
---

## Overview

Developed a machine learning framework to predict the performance of asphalt mixtures containing reclaimed asphalt pavement (RAP) and other alternative materials.

The objective was to replace time-consuming laboratory trial-and-error procedures with predictive regression models capable of estimating key performance indicators and identifying feasible material combinations that satisfy Balanced Mix Design (BMD) performance requirements under different traffic levels.

---

## Technical Architecture

The modeling framework benchmarks several regression algorithms for predicting asphalt mixture performance:

- Feed-Forward Neural Network (FNN)  
- Generalized Linear Model (GLM)  
- Support Vector Regression (SVR)  
- Gaussian Process Regression (GPR)

Input features represent mixture composition, including proportions of reclaimed asphalt pavement, crumb rubber, and waste engine oil. Target outputs correspond to key performance indicators used in balanced mix design, including cracking resistance, rutting resistance, and moisture susceptibility.

Models were trained using experimental performance data from multiple asphalt mixture designs and evaluated using held-out validation datasets.

---

## Model Development Strategy

Each model underwent structured hyperparameter tuning to identify configurations that balance predictive accuracy and model stability. Because the dataset size was limited, tuning relied on controlled grid-search exploration rather than aggressive automated optimization.

Model performance was evaluated using mean relative error on unseen testing data. Among the candidate models, Gaussian Process Regression demonstrated the strongest predictive performance and was selected for subsequent design-space analysis.

---

## Feasible Design Space Identification

The trained model was used to explore the asphalt mixture design space across a wide range of material proportions.

A structured grid search was performed across the mixture composition domain. For each candidate mixture, predicted performance metrics were evaluated against traffic-dependent thresholds for rutting resistance, cracking tolerance, and moisture susceptibility.

Mixture combinations were then classified as satisfactory or unsatisfactory according to Balanced Mix Design criteria. Boundary points separating these regions were extracted and used to construct smooth surfaces defining the feasible material design domain.

This process converts discrete laboratory measurements into a continuous predictive design space that can guide mixture optimization.

---

## Empirical Contribution

The framework demonstrates how machine learning can enhance asphalt mixture design by:

- Transforming limited laboratory test data into a predictive design space  
- Identifying feasible material combinations that satisfy performance constraints  
- Reducing the need for extensive trial-and-error laboratory testing  
- Enabling rapid screening of sustainable material blends containing recycled components  

---

## Engineering Deliverables

- Multi-model regression benchmarking pipeline  
- Gaussian Process Regression prediction model  
- Mixture design-space exploration workflow  
- Feasible-region boundary extraction algorithm  
- Statistical analysis framework for material influence evaluation  

---

## Relevance

Balanced Mix Design requires evaluating multiple competing performance criteria across complex material combinations. Data-driven prediction frameworks can significantly accelerate this process by identifying promising mixture compositions before laboratory testing.

This project demonstrates how machine learning can support sustainable pavement engineering by enabling efficient design of asphalt mixtures incorporating recycled materials.

---

## Related Publication

Khorshidi, M., Goli, A., Orešković, M., Khayambashi, K., & Ameri, M. (2023).  
*Performance evaluation of asphalt mixtures containing different proportions of alternative materials.*  
Sustainability, 15(18), 13314.

[View Publication](https://doi.org/10.3390/su151813314)
