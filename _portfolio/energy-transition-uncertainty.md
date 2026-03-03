---
title: "Probabilistic Energy Transition Modeling Framework"
collection: portfolio
permalink: /project/energy-transition-uncertainty
excerpt: "Large-scale Monte Carlo and neural surrogate framework for uncertainty-aware energy transition planning."
date: 2025-01-01
---

## Overview

Designed and implemented a scalable probabilistic modeling framework to evaluate long-term energy transition strategies under deep technological and climate uncertainty.

The framework integrates deterministic capacity expansion modeling with nested uncertainty propagation and machine learning–based surrogate acceleration.

---

## Technical Architecture

- Capacity expansion modeling using **TEMOA**
- Nested Monte Carlo simulation  
  - 5,000 epistemic realizations  
  - 1,000 aleatoric realizations per scenario  
- Hurricane damage and outage cost modeling  
- Deep neural network surrogate training (>93% predictive accuracy)
- Sobol-based global sensitivity analysis
- Parallelized computation for high-dimensional scenario evaluation

---

## Key Capabilities

- Explicit separation of epistemic vs. aleatoric uncertainty  
- Quantification of distributional system cost outcomes  
- Identification of dominant cost drivers in high-dimensional planning space  
- Computational tractability via learned surrogate approximation  

---

## Case Study

**Region:** Puerto Rico 2050 power system  
**Scenarios:**  
- Business-as-usual  
- Fully renewable  
- Fully decarbonized  

**Outputs Generated:**  
- Operational cost distributions  
- Damage cost distributions  
- Outage cost distributions  
- Global sensitivity indices  

---

## Engineering Deliverables

- TEMOA configuration modules  
- Monte Carlo simulation engines  
- Surrogate training scripts (PyTorch)  
- Sensitivity analysis modules  
- Full reproducibility documentation  

---

## Relevance

Demonstrates integration of optimization, uncertainty quantification, and machine learning to enable risk-aware infrastructure planning at scale.

---

## Related Publication

Khayambashi, K., Clarens, A. F., Shobe, W. M., & Alemazkoor, N. (2025).  
Identifying key uncertainties in energy transitions: A Puerto Rico case study.  
*Nature Communications*, 16(1), 9064.

[View Publication](/publication/2025-nature-uncertainty)
