---
title: "Probabilistic Energy Transition Modeling Framework"
collection: portfolio
permalink: /project/energy-transition-uncertainty
excerpt: "Hierarchical Monte Carlo and neural surrogate framework for uncertainty-aware long-term energy transition planning under compound technological and climate risk."
---

## Overview

Developed a scalable probabilistic modeling framework for evaluating long-term energy transition strategies under high-dimensional technological, economic, institutional, and climate uncertainty.

The framework couples deterministic capacity expansion optimization with hierarchical nested Monte Carlo simulation and neural surrogate modeling to quantify full-system cost risk distributions and identify dominant uncertainty drivers.

---

## Technical Architecture

- Deterministic capacity expansion modeling using TEMOA  
- Hierarchical nested Monte Carlo structure  
- 5,000 epistemic realizations × 1,000 aleatoric realizations  
- Explicit separation of uncertainty layers  
- Hurricane damage and outage economic impact modeling  
- Deep neural network surrogate (>93% predictive accuracy)  
- Sobol-based global sensitivity analysis  
- Parallelized high-performance computation  

Uncertainty layers:

- **Epistemic uncertainties:** fuel prices, technology CAPEX/O&M, demand growth, hurricane frequency and intensity change, organizational inefficiency  
- **Aleatoric uncertainties:** weather variability, hurricane occurrence, component damage, restoration time  
- Full propagation of operational cost, restoration cost, and outage economic impact  

---

## Key Capabilities

- Joint modeling of structural (epistemic) and stochastic (aleatoric) uncertainties  
- Risk-distribution estimation rather than single-point cost comparison  
- Surrogate-accelerated sensitivity analysis in high-dimensional planning space  
- Identification of dominant variance drivers without brute-force exploration  
- Design-once–analyze-many computational paradigm  

---

## Case Study Configuration

**Region:** Puerto Rico power system (planning horizon to 2050)  
**Scenarios:** Business-as-usual (BAU), Fully Renewable (FR), Fully Decarbonized (FD)  
**Time structure:** Multi-period capacity expansion with 36 representative time slices per year  
**Objective:** Long-run total system cost under uncertainty  

---

## Empirical Impact

- 38–41% probability that renewable or fully decarbonized pathways outperform business-as-usual in total cost under uncertainty  
- Hurricane frequency change identified as dominant cost-variance driver (>50% of total variance)  
- Organizational inefficiency identified as second-largest uncertainty contributor  
- Reduced high-dimensional uncertainty space to a small set of decision-relevant drivers  
- Enabled computationally tractable evaluation across millions of simulated realizations  

Results demonstrate that long-term energy transition outcomes are driven more by structural uncertainty assumptions rather than deterministic optimization outputs alone.

---

## Engineering Deliverables

- Integrated TEMOA–Monte Carlo probabilistic workflow  
- Neural surrogate training and inference pipeline  
- Global sensitivity analysis implementation  
- Parallel computing framework for large-scale realization sampling  
- Reproducibility scripts and scenario configuration modules  

---

## Relevance

Positions uncertainty quantification as a core planning requirement for deep decarbonization pathways, particularly in climate-exposed island grids.

Framework bridges capacity expansion modeling, climate risk analytics, and high-dimensional uncertainty decomposition to support robust long-term energy policy design.

---

## Related Publication

Khayambashi, K., Clarens, A. F., Shobe, W. M., & Alemazkoor, N. (2025).  
Identifying key uncertainties in energy transitions: A Puerto Rico case study.  
*Nature Communications*, 16(1), 9064.

[View Publication](/publication/2025-nature-uncertainty)
