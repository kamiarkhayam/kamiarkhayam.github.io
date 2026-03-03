---
title: "Machine Learning–Based Performance Prediction for High-RAP Asphalt Mixtures"
collection: portfolio
permalink: /project/ml-balanced-mix-design
excerpt: "Regression-based machine learning framework for predicting rutting, cracking, and moisture resistance of asphalt mixtures and identifying feasible design regions under traffic-level constraints."
---

## Overview

Developed a machine learning prediction framework to model performance behavior of asphalt mixtures containing reclaimed asphalt pavement (RAP), crumb rubber (CR), waste engine oil (WEO), and steel slag (SS).

The objective was to replace exhaustive laboratory trial-and-error with data-driven regression models capable of predicting key performance indicators and identifying allowable material combinations that satisfy traffic-dependent thresholds under Balanced Mix Design (BMD) requirements.

---

## Technical Architecture

Four regression models were implemented and benchmarked:

- Feed-Forward Neural Network (FNN)
- Generalized Linear Model (GLM)
- Support Vector Regression (SVR)
- Gaussian Process Regression (GPR)

**Input features**
- RAP content (%)
- CR content (%)
- WEO content (%)

**Target outputs**
- Cracking Tolerance Index (CTindex)
- Flow Number (FN)
- Tensile Strength Ratio (TSR)

Model training used performance data from 44 mixture designs.

---

## Model Development Strategy

### Hyperparameter Tuning

Each model underwent structured tuning:

- **FNN**: number of hidden layers, neurons, epochs, batch size, regularization coefficient  
- **GLM**: regularization strength  
- **SVR**: kernel type, penalty parameter, tube width  
- **GPR**: kernel selection (linear + radial basis), variance and length-scale grid search  

To prevent overfitting due to limited dataset size, tuning avoided aggressive automated optimizers and relied on controlled grid search.

Model selection metric:
- Mean Relative Error (MRE) on held-out test data

---

## Selected Model: Gaussian Process Regression

Gaussian Process Regression (GPR) demonstrated superior predictive accuracy while explicitly capturing predictive uncertainty.

Advantages of GPR in this application:

- Strong performance with small datasets  
- Nonlinear response surface modeling  
- Probabilistic prediction capability  
- Smooth interpolation across material design space  

GPR was therefore selected for final feasible-region identification.

---

## Feasible Design Space Identification

After training, a structured grid search was performed across the 3D material input space:

- RAP ∈ [0–75%]  
- CR ∈ [0–15%]  
- WEO ∈ [0–15%]  

For each grid point:

1. Predicted CTindex, FN, and TSR were computed  
2. Predictions were evaluated against established traffic-level thresholds  
3. Points were classified as **satisfactory** or **unsatisfactory**

Boundary points separating these regions were extracted and used to:

- Fit second-order polynomial surfaces  
- Construct 3D performance boundary planes  

These surfaces define admissible material combinations that satisfy:

- FN ≥ 190 (10–30M ESALs)  
- FN ≥ 740 (>30M ESALs)  
- CTindex ≥ 110  
- TSR ≥ 0.8  

This converts discrete lab results into a continuous performance-feasible material domain.

---

## Statistical Sensitivity Analysis

A paired t-test framework was implemented to quantify the relative influence of:

- RAP  
- CR  
- WEO  

on prediction residuals for FN, CTindex, and TSR.

This analysis identified which alternative material most strongly influenced each performance metric, enhancing interpretability beyond black-box regression.

---

## Engineering Deliverables

- Multi-model regression benchmarking pipeline  
- Custom GPR implementation with kernel tuning  
- Structured hyperparameter selection protocol  
- 3D feasible-region extraction algorithm  
- Polynomial boundary surface fitting module  
- Statistical material influence analysis framework  

---

## Empirical Contribution

- Transformed 44 laboratory mixture designs into a continuous predictive design space  
- Reduced dependence on iterative experimental trials  
- Provided explicit performance-feasible material boundaries under traffic constraints  
- Integrated machine learning directly into Balanced Mix Design methodology  

---

## Relevance

Demonstrates how probabilistic regression models can be embedded into infrastructure material design workflows to:

- Accelerate mixture optimization  
- Quantify uncertainty  
- Enable rapid screening of sustainable material combinations  

Framework bridges pavement engineering and data-driven modeling, providing a scalable pathway toward intelligent mix design under sustainability constraints.

---

## Related Publication

Khorshidi, M., Goli, A., Orešković, M., Khayambashi, K., & Ameri, M. (2023).  
Performance evaluation of asphalt mixtures containing different proportions of alternative materials.  
*Sustainability, 15(18), 13314.*

[View Publication](https://doi.org/10.3390/su151813314)
