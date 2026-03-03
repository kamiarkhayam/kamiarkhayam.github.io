---
title: "Probabilistic Energy Transition Modeling Framework"
collection: portfolio
permalink: /project/energy-transition-uncertainty
excerpt: "Large-scale hierarchical Monte Carlo and neural surrogate framework for uncertainty-aware energy transition planning."
---

This project develops a scalable probabilistic modeling framework for evaluating long-term energy transition strategies under high-dimensional technological, economic, institutional, and climate uncertainty.

The system integrates:

• Deterministic capacity expansion modeling using TEMOA  
• Hierarchical nested Monte Carlo simulation  
• 5,000 epistemic realizations × 1,000 aleatoric realizations  
• Hurricane damage and outage cost modeling  
• Deep neural network surrogate modeling (>93% predictive accuracy)  
• Sobol-based global sensitivity analysis  
• Parallelized high-performance computation  

The probabilistic engine explicitly separates uncertainty layers:

• Epistemic uncertainties (fuel prices, technology CAPEX/O&M, demand growth, hurricane frequency/intensity change, organizational inefficiency)  
• Aleatoric uncertainties (weather variability, hurricane occurrence, component damage, restoration time)  
• Full cost propagation including operational cost, damage restoration cost, and outage economic impact  

Case study configuration:

• Region: Puerto Rico 2050 power system :contentReference[oaicite:0]{index=0}  
• Transition scenarios: Business-as-usual (BAU), Fully Renewable (FR), Fully Decarbonized (FD)  
• Time horizon: Multi-period capacity expansion to 2050  
• 36 representative time slices per year for renewable variability  

Key technical contributions include:

• First large-scale integration of epistemic and aleatoric uncertainty in energy transition cost planning  
• Explicit modeling of organizational inefficiency as a systemic uncertainty driver  
• Surrogate-accelerated global sensitivity analysis in high-dimensional planning space  
• Identification of dominant uncertainty sources rather than full-dimensional brute-force exploration  

Impact:

• Demonstrated 38–41% probability that renewable/decarbonized pathways can be less costly than business-as-usual under uncertainty  
• Identified hurricane frequency change as the dominant driver (>50%) of total cost variance  
• Revealed organizational inefficiency as the second largest cost-uncertainty driver  
• Reduced high-dimensional cost evaluation to a small set of dominant decision-relevant uncertainties  
• Enabled computationally tractable sensitivity analysis across millions of simulated realizations  

The framework follows a design-once–analyze-many paradigm: deterministic optimization defines system architecture, while nested Monte Carlo and surrogate modeling quantify risk distributions and dominant uncertainty drivers.

## Related Publication

Khayambashi, K., Clarens, A. F., Shobe, W. M., & Alemazkoor, N. (2025).  
Identifying key uncertainties in energy transitions: A Puerto Rico case study.  
*Nature Communications*, 16(1), 9064.  

[View Publication](/publication/2025-nature-uncertainty)
