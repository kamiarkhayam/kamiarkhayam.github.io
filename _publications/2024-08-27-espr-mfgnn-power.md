---
title: "Multi-Fidelity Graph Neural Networks for Efficient Power Flow Analysis Under High-Dimensional Demand and Renewable Generation Uncertainty"
collection: publications
category: manuscripts
permalink: /publication/2024-mfgnn-powerflow-epsr
date: 2024-12-01
venue: "Electric Power Systems Research"
paperurl: "https://www.sciencedirect.com/science/article/abs/pii/S0378779624009003"
citation: "Taghizadeh, M., Khayambashi, K., Hasnat, M. A., & Alemazkoor, N. (2024). Multi-fidelity graph neural networks for efficient power flow analysis under high-dimensional demand and renewable generation uncertainty. Electric Power Systems Research, 237, 111014."
---
This paper introduces a residual multi-fidelity graph neural network (MF-GNN) framework for fast and accurate probabilistic power flow analysis in modern grids with high renewable penetration and stochastic load variation.

The proposed architecture integrates:
- A low-fidelity GNN trained on DC power flow simulations  
- A high-fidelity GNN trained on AC power flow simulations  
- A residual learning mechanism that predicts only the correction between DC and AC solutions  

By fusing inexpensive DC simulations with limited AC simulations, the framework significantly reduces training cost while improving voltage magnitude and phase angle prediction accuracy.

Extensive experiments on IEEE 9-, 14-, 30-, 118-, and 2383-bus systems demonstrate:

- Lower mean absolute error than single-fidelity GNNs  
- Strong robustness under N-1 line contingency scenarios  
- Improved generalization to unseen grid topologies  
- Substantial computational savings compared to high-fidelity-only training  

The model leverages graph structure explicitly, enabling scalability across varying grid sizes while maintaining strong predictive performance under high-dimensional uncertainty.

**Methods:** Multi-fidelity learning, graph neural networks (WL-GNN), probabilistic power flow, DC/AC data fusion, residual learning  

[Paper]({{ page.paperurl }}) | [Code](https://www.sciencedirect.com/science/article/abs/pii/S0378779624009003)
