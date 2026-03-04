---
title: "Hybrid Chance-Constrained Optimal Power Flow Using Enhanced Multi-Fidelity Graph Neural Networks"
collection: portfolio
permalink: /project/hcc-opf-emf-gnn
excerpt: "Surrogate-accelerated chance-constrained optimal power flow framework combining multi-fidelity graph neural networks with hybrid constraint validation under renewable and load uncertainty."
---

## Overview

Developed a hybrid chance-constrained optimal power flow (HCC-OPF) framework that integrates enhanced multi-fidelity graph neural networks (EMF-GNN) as surrogate AC power flow solvers under uncertain electricity demand and renewable generation.

Probabilistic optimal power flow typically requires thousands of nonlinear AC simulations, which limits scalability for uncertainty-aware planning and operations. The proposed framework addresses this challenge by using graph-based surrogate models to approximate power flow results while selectively invoking the exact AC solver when constraints approach critical thresholds.

This hybrid design preserves computational efficiency while maintaining operational reliability.

---

## Technical Architecture

The framework integrates multi-fidelity machine learning with reliability-aware optimization.

### Multi-Fidelity Graph Neural Network Surrogate

- Low-fidelity graph model trained on DC power flow simulations  
- High-fidelity graph model trained on AC power flow results  
- Residual learning architecture that corrects low-fidelity predictions  
- Graph message passing that captures electrical interactions across network topology  

This multi-fidelity structure improves both prediction accuracy and data efficiency compared to single-fidelity neural surrogates.

### Hybrid Constraint Validation

To ensure safe optimization results, a hybrid correction mechanism monitors surrogate predictions during optimization.

When predicted operating points approach constraint boundaries, the exact AC solver is invoked to validate and correct the solution. This strategy prevents surrogate approximation errors from causing operational violations while preserving most computational gains.

---

## Key Capabilities

- Scalable chance-constrained optimal power flow under uncertainty  
- Surrogate-accelerated AC power flow evaluation using graph neural networks  
- Multi-fidelity learning that reduces high-fidelity training data requirements  
- Hybrid validation mechanism that preserves constraint reliability  
- Robust performance under topology changes and contingency scenarios  

---

## Experimental Evaluation

The framework was evaluated on several IEEE benchmark transmission systems under uncertainty in electricity demand and renewable generation.

Test scenarios included correlated stochastic sampling of loads and renewable output as well as N-1 contingency conditions. Performance was compared against traditional AC-based optimization and single-fidelity machine learning surrogates.

---

## Empirical Impact

Results demonstrate significant improvements in both computational efficiency and solution reliability.

Key outcomes include:

- Improved surrogate accuracy compared with single-fidelity graph models  
- Near-identical optimal cost distributions relative to exact AC-based solutions  
- Substantial reduction in constraint violation probability through hybrid validation  
- Robust performance under topology perturbations and contingency scenarios  
- Minimal increase in optimization time compared to purely surrogate-based methods

These results show that hybrid surrogate optimization can enable scalable probabilistic OPF without compromising operational constraints.

---

## Engineering Deliverables

- Enhanced multi-fidelity GNN architecture for AC power flow approximation  
- Hybrid chance-constrained OPF optimization framework  
- Surrogate training and evaluation pipeline using PyTorch Geometric  
- Monte Carlo simulation workflow for uncertainty-driven OPF analysis  
- Reproducible implementation and open-source repository  

https://github.com/kamiarkhayam/HCCOPF-using-EMFGNN

---

## Relevance

Modern power systems face increasing uncertainty due to renewable generation variability and growing electrification demand. Operational planning tools must therefore evaluate large numbers of stochastic scenarios while maintaining strict reliability constraints.

This framework demonstrates how graph-based surrogate modeling and hybrid optimization can support scalable probabilistic OPF, enabling faster and more reliable decision-making for future power systems.

---

## Publication

Khayambashi, K., Hasnat, M. A., & Alemazkoor, N.  
*Hybrid Chance-Constrained Optimal Power Flow Under Load and Renewable Generation Uncertainty Using Enhanced Multi-Fidelity Graph Neural Networks.*  
Journal of Machine Learning for Modeling and Computing, 5(4):53–76 (2024).
