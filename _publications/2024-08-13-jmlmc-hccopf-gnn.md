---
title: "Hybrid Chance-Constrained Optimal Power Flow Under Load and Renewable Generation Uncertainty Using Enhanced Multi-Fidelity Graph Neural Networks"
collection: publications
category: manuscripts
permalink: /publication/2024-hccopf-emfgnn
date: 2024-01-01
venue: "Journal of Machine Learning for Modeling and Computing"
paperurl: "https://www.dl.begellhouse.com/journals/558048804a15188a,6ea623526214d90d,70b2b005471fa9c2.html"
citation: "Khayambashi, K., Hasnat, M. A., & Alemazkoor, N. (2024). Hybrid chance-constrained optimal power flow under load and renewable generation uncertainty using enhanced multi-fidelity graph neural networks. Journal of Machine Learning for Modeling and Computing, 5(4), 53–76."
---
Published in *Journal of Machine Learning for Modeling and Computing* (2024).

This work introduces a hybrid chance-constrained optimal power flow (HCC-OPF) framework that integrates enhanced multi-fidelity graph neural networks (EMF-GNN) as fast and accurate surrogate power flow solvers under high-dimensional load and renewable generation uncertainty.

The proposed EMF-GNN architecture fuses low-fidelity DC power flow simulations with high-fidelity AC simulations through a residual multi-fidelity structure, significantly reducing training cost while improving voltage magnitude and phase angle prediction accuracy across IEEE benchmark systems.

To ensure operational reliability, a hybrid optimization mechanism selectively invokes the exact AC power flow solver near constraint thresholds, preventing surrogate-induced constraint violations while preserving computational efficiency.

Extensive experiments on IEEE 9-, 14-, 30-, and 118-bus systems demonstrate:

- Improved surrogate accuracy compared to single-fidelity and prior multi-fidelity GNN models  
- Reduced constraint violation probability under uncertainty  
- Robust performance under N-1 security contingencies  
- Significant computational speedup relative to full AC-based chance-constrained OPF  

**Methods:** Multi-fidelity graph neural networks, chance-constrained optimization, hybrid surrogate-based OPF, Monte Carlo uncertainty modeling, N-1 contingency analysis  

[Paper]({{ page.paperurl }}) | [Code](https://github.com/kamiarkhayam/HCCOPF-using-EMFGNN)
