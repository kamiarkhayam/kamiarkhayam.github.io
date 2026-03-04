---
title: "Probabilistic Energy Transition Modeling Framework"
collection: portfolio
permalink: /project/energy-transition-uncertainty
excerpt: "Probabilistic energy transition planning framework integrating capacity expansion modeling, hierarchical Monte Carlo simulation, and machine learning surrogates."
---

## Overview

Developed a probabilistic modeling framework for evaluating long-term energy transition strategies under deep technological, economic, institutional, and climate uncertainty.

The framework couples deterministic capacity expansion optimization with hierarchical Monte Carlo simulation and neural surrogate modeling to characterize the full distribution of possible system outcomes rather than a single optimal pathway. This approach enables identification of the structural uncertainties that most strongly influence long-term transition costs and infrastructure investment decisions.

---

## Technical Architecture

The framework integrates power system planning with modern uncertainty quantification methods:

- Capacity expansion modeling using **TEMOA**
- Hierarchical nested Monte Carlo simulation separating structural and stochastic uncertainty
- Neural network surrogate models to accelerate large-scale scenario exploration
- Global sensitivity analysis using variance-based Sobol indices
- Parallelized computing workflow for large ensemble evaluation

Uncertainties are represented in two layers. Structural (epistemic) uncertainties capture unknown future conditions such as fuel prices, technology costs, demand growth, and hurricane frequency changes. Stochastic (aleatoric) uncertainties represent natural variability including weather, storm occurrence, infrastructure damage, and restoration duration.

---

## Key Capabilities

- Joint modeling of structural and stochastic uncertainty in long-term energy planning  
- Risk-distribution estimation rather than single deterministic cost outcomes  
- Surrogate-accelerated exploration of high-dimensional planning spaces  
- Identification of dominant uncertainty drivers influencing system costs  
- Computational framework enabling large-scale probabilistic scenario analysis  

---

## Case Study

The framework was applied to the **Puerto Rico power system**, which faces simultaneous decarbonization challenges and significant climate risk exposure.

Scenarios evaluate alternative transition pathways including:

- Business-as-usual development  
- High-renewable deployment  
- Fully decarbonized electricity systems  

The model evaluates system evolution through mid-century while accounting for hurricane impacts, infrastructure damage, and restoration costs.

---

## Empirical Impact

The analysis shows that uncertainty in climate risk and institutional effectiveness can strongly influence long-term transition costs.

Key findings include:

- Renewable and fully decarbonized pathways have a **38–41% probability of being less costly than business-as-usual** when uncertainty is considered.  
- Changes in **hurricane frequency and intensity emerge as the dominant drivers of system cost variance.**  
- Institutional and operational inefficiencies represent a second major source of uncertainty in transition outcomes.  
- A high-dimensional uncertainty space collapses to a small set of influential drivers that determine most system cost variability.

These results demonstrate that transition planning outcomes depend heavily on uncertainty assumptions rather than deterministic optimization results alone.

---

## Engineering Deliverables

- Integrated TEMOA–Monte Carlo probabilistic modeling workflow  
- Neural surrogate modeling pipeline for scenario acceleration  
- Global sensitivity analysis toolkit for uncertainty decomposition  
- Parallelized simulation infrastructure for large ensemble evaluation  
- Reproducible scenario configuration and analysis scripts  

---

## Relevance

Deep decarbonization planning increasingly requires explicit treatment of uncertainty, particularly in climate-exposed power systems.

This framework integrates capacity expansion modeling, climate risk analysis, and machine learning acceleration to support robust energy transition planning under uncertainty.

---

## Related Publication

Khayambashi, K., Clarens, A. F., Shobe, W. M., & Alemazkoor, N. (2025).  
*Identifying key uncertainties in energy transitions: A Puerto Rico case study.*  
Nature Communications, 16(1), 9064.

[View Publication](/publication/2025-nature-uncertainty)
