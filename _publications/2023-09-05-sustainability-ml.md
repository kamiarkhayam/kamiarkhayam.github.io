---
title: "Performance Evaluation of Asphalt Mixtures Containing Different Proportions of Alternative Materials"
collection: publications
category: manuscripts
permalink: /publication/2023-ml-asphalt-performance
date: 2023-09-05
venue: "Sustainability"
paperurl: "https://www.mdpi.com/2071-1050/15/18/13314"
citation: "Khorshidi, M., Goli, A., Orešković, M., Khayambashi, K., & Ameri, M. (2023). Performance evaluation of asphalt mixtures containing different proportions of alternative materials. Sustainability, 15(18), 13314."
---
Published in *Sustainability* (2023).

This study integrates experimental pavement engineering with machine learning–based predictive modeling to identify optimal compositions of reclaimed asphalt pavement (RAP), crumb rubber (CR), waste engine oil (WEO), and steel slag (SS) under balanced mix design constraints.

A total of 44 mixture designs were experimentally evaluated across three performance metrics:

- Cracking resistance (CTindex)
- Rutting resistance (Flow Number)
- Moisture damage resistance (TSR)

Machine learning models were then developed to learn nonlinear relationships between material composition and performance thresholds. Four regression techniques were compared:

- Feed-forward neural networks (FNN)
- Generalized linear models (GLM)
- Support vector regression (SVR)
- Gaussian process regression (GPR)

Gaussian Process Regression (GPR) demonstrated the lowest mean relative error and superior uncertainty handling. Rather than relying solely on deterministic predictions, the framework quantified performance variability and enabled probabilistic identification of feasible material regions.

A grid-search over the multi-dimensional material space (RAP–CR–WEO) was performed using trained ML models to:

- Predict performance across untested combinations  
- Identify feasible regions satisfying ESAL-based thresholds  
- Fit polynomial boundary surfaces separating acceptable vs. unacceptable performance  

This approach transformed a combinatorial materials problem into a continuous optimization surface, enabling rapid screening of sustainable asphalt designs without exhaustive laboratory testing.

Key ML Contributions:

- Data-driven surrogate modeling of multi-material pavement systems  
- Comparative evaluation of nonlinear regression techniques  
- Uncertainty-aware GPR modeling for performance prediction  
- 3D feasible-region surface fitting for engineering decision support  

This work demonstrates how machine learning can accelerate sustainable infrastructure material design by replacing discrete trial-and-error experimentation with predictive performance mapping.
