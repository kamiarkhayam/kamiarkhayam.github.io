---
title: "GCAM–CDR Coupled Uncertainty Framework"
collection: portfolio
permalink: /project/gcam-cdr-power-uq
excerpt: "Probabilistic integrated assessment modeling framework coupling carbon dioxide removal deployment with power-sector evolution under deep uncertainty."
---

## Overview

Developed a probabilistic planning framework that couples carbon dioxide removal (CDR) deployment with electricity-sector evolution under deep technological, resource, and policy uncertainty.

The approach integrates the **GCAM-USA integrated assessment model** with large-scale Monte Carlo simulation, neural surrogate modeling, and variance-based sensitivity analysis. Rather than producing a single deterministic decarbonization pathway, the framework characterizes the full distribution of possible system outcomes and identifies the key drivers shaping long-term energy transitions.

---

## Technical Architecture

The framework integrates integrated assessment modeling with modern uncertainty quantification methods:

- **GCAM-USA** state-level integrated assessment modeling  
- Structured Monte Carlo sampling across a high-dimensional uncertainty space  
- Automated scenario generation and batch model execution  
- Neural network surrogate models for computational acceleration  
- Variance-based **Sobol Global Sensitivity Analysis** to identify dominant drivers of system uncertainty  

Neural surrogate models approximate GCAM outputs, enabling large-scale sensitivity analysis that would otherwise be computationally prohibitive with the full integrated assessment model.

---

## Key Capabilities

- Explicit coupling of **CDR deployment pathways and electricity-sector evolution**  
- Representation of uncertainty in technology costs, deployment timing, and resource availability  
- Modeling of cross-sector resource competition (e.g., biomass, land, storage capacity)  
- Probabilistic characterization of energy system futures rather than deterministic forecasts  
- Identification of dominant uncertainty drivers through global sensitivity analysis  

This approach reduces a large parameter space to a smaller set of decision-relevant uncertainties that shape system evolution.

---

## Case Study

The framework was applied to decarbonization planning for **Virginia’s energy system** using GCAM-USA.

The analysis evaluates how different CDR technologies interact with the electricity sector under uncertainty. Technologies represented include direct air capture, bioenergy with carbon capture and storage (BECCS), enhanced rock weathering, and other emerging carbon removal approaches.

Electricity system evolution is modeled simultaneously, capturing changes in renewable generation, thermal capacity, and storage deployment as CDR demand evolves.

---

## Empirical Findings

The analysis reveals that uncertainty in **CDR technology emergence and deployment timing** becomes a dominant driver of long-term electricity system evolution.

Key insights include:

- Mid-century carbon removal deployment varies widely across plausible futures.  
- Electricity system expansion can increase substantially under high CDR demand scenarios.  
- Resource constraints such as biomass availability and land use become cross-sector bottlenecks.  
- Once CDR demand uncertainty is introduced, traditional drivers such as generator capital costs play a smaller role in determining system outcomes.

Overall, the study shows that decarbonization planning must account for uncertainty in negative-emissions technologies because these uncertainties propagate directly into electricity system investment decisions.

---

## Engineering Deliverables

- Automated GCAM scenario generation and batch execution workflow  
- Monte Carlo simulation framework for integrated assessment modeling  
- Neural surrogate modeling pipeline for large-scale scenario exploration  
- Global sensitivity analysis toolkit for identifying key uncertainty drivers  
- Reproducible modeling workflow and open-source repository  

https://github.com/kamiarkhayam/gcam-cdr-power-uq

---

## Relevance

Energy transition planning increasingly depends on uncertain negative-emissions technologies. This framework provides a computationally tractable method for evaluating how those uncertainties reshape electricity system evolution.

The approach bridges **integrated assessment modeling, machine learning acceleration, and uncertainty quantification**, enabling more robust decarbonization planning under deep uncertainty.

---

## Related Publication

Khayambashi, K., Javadi, P., Fuhrman, J., Clarens, A. F., & Alemazkoor, N.  
*The Coupled Uncertainty of Carbon Removal and the Power Sector in Decarbonization Planning for Virginia.*  
In preparation.
