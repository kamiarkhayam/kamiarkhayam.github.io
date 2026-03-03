---
title: "GCAM–CDR Coupled Uncertainty Framework"
collection: portfolio
permalink: /project/gcam-cdr-power-uq
excerpt: "Large-scale probabilistic integrated assessment modeling framework coupling carbon dioxide removal and power-sector evolution under deep uncertainty."
---

## Overview

Developed an integrated probabilistic planning framework that couples carbon dioxide removal (CDR) deployment with electricity sector evolution under deep technological, resource, and policy uncertainty.

The framework combines a state-level Integrated Assessment Model (GCAM-USA) with large-ensemble Monte Carlo simulation, neural surrogate acceleration, and variance-based Global Sensitivity Analysis to move beyond deterministic decarbonization forecasting.

Full manuscript: :contentReference[oaicite:0]{index=0}

---

## Technical Architecture

- State-level Integrated Assessment Modeling using **GCAM-USA**
- High-dimensional uncertainty space (>70 uncertain parameters)
- Latin Hypercube Sampling for structured Monte Carlo input generation
- Automated XML modification and parallel GCAM execution
- Deep Neural Network surrogate models (entity embeddings + ReLU layers)
- 5-fold cross-validation with early stopping
- Sobol variance-based Global Sensitivity Analysis (SALib + Saltelli sampling)

**Simulation scale**
- Thousands of full GCAM runs
- 2020–2050 dynamic-recursive horizon
- Multi-technology time-series outputs (generation + sequestration)

Average surrogate fidelity:
- Mean R² ≈ 0.75  
- Wind R² = 0.98  
- Rock Weathering R² = 0.93  

---

## Key Capabilities

- Explicit modeling of CDR–power sector feedbacks
- Representation of technology emergence timing uncertainty
- Resource competition modeling (biomass, land, storage)
- Probabilistic portfolio evolution instead of single-path forecasts
- Identification of dominant uncertainty drivers via Sobol indices
- Dimensionality reduction from 70+ parameters to ~8 primary drivers

---

## Case Study

**Region:** Commonwealth of Virginia  
**Model:** GCAM-USA (state resolution)  
**Planning Horizon:** 2020–2050  

**CDR Technologies Modeled:**
- DACCS (natural gas + electricity variants)
- BECCS (multiple biomass pathways)
- Enhanced Rock Weathering (ERW)
- Biochar
- Direct Ocean Removal (DOR)

**Electricity Portfolio Modeled:**
- Solar (utility + rooftop)
- Wind (onshore + offshore)
- Nuclear
- Natural Gas
- Coal
- Storage technologies

---

## Empirical Findings

- Mid-century sequestration uncertainty spans from minimal removal to multi-megaton deployment.
- Electricity system size variance expands significantly under high-DACCS futures.
- CDR technology emergence timing dominates system-level uncertainty.
- Generator capital cost assumptions exert secondary influence once CDR demand uncertainty is incorporated.
- Biomass availability and land constraints emerge as structural cross-sector bottlenecks.
- System variance collapses to a small set of influential variables, enabling targeted uncertainty management.

Primary structural insight:
> Power-sector uncertainty becomes demand-driven by CDR rollout timing rather than supply-driven by generation cost assumptions.

---

## Engineering Deliverables

- GCAM automation engine for batch scenario execution
- Monte Carlo orchestration workflow (Python)
- Surrogate modeling pipeline (PyTorch)
- Sensitivity analysis toolkit (SALib integration)
- Reproducible dataset and open-source repository:
  https://github.com/kamiarkhayam/gcam-cdr-power-uq

---

## Relevance

Demonstrates integration of:

- Integrated Assessment Modeling  
- Deep uncertainty quantification  
- Machine learning surrogate acceleration  
- Cross-sector infrastructure coupling  

Framework generalizes to other states, national contexts, or sector-coupled decarbonization studies requiring computationally tractable probabilistic analysis.

---

## Related Publication

Khayambashi, K., Javadi, P., Fuhrman, J., Clarens, A. F., & Alemazkoor, N.  
The Coupled Uncertainty of Carbon Removal and the Power Sector in Decarbonization Planning for Virginia.  
In preparation / Under review.
