---
title: "Hybrid Chance-Constrained Optimal Power Flow Using Enhanced Multi-Fidelity Graph Neural Networks"
collection: portfolio
permalink: /project/hcc-opf-emf-gnn
excerpt: "Scalable, surrogate-accelerated chance-constrained optimal power flow under high-dimensional load and renewable uncertainty with N-1 security."
---

## Overview

Developed a scalable hybrid chance-constrained optimal power flow (HCC-OPF) framework that integrates enhanced multi-fidelity graph neural networks (EMF-GNN) as surrogate AC power flow solvers under correlated load and renewable generation uncertainty.

The framework addresses two fundamental challenges in probabilistic OPF:
1. Computational burden from repeated AC power flow evaluations.
2. Constraint violation risk introduced by surrogate approximation errors.

A hybrid correction mechanism selectively activates the exact AC solver near critical constraint thresholds to ensure reliability.

Full publication: Journal of Machine Learning for Modeling and Computing (2024).

---

## Technical Architecture

### 1. Enhanced Multi-Fidelity GNN (EMF-GNN)

- Low-fidelity block (TagConv) trained on DC power flow data.
- High-fidelity block (k-GNN / GraphConv) trained on AC power flow data.
- Residual learning architecture:
  - HF network predicts voltage magnitude and phase residuals.
- Embedding transfer from LF to intermediate HF layers.
- Mean Squared Error loss on voltage magnitude and phase angle.
- Trained using PyTorch + PyTorch Geometric (RTX 4090 GPU).

Training design:
- LF dataset size = 2× HF dataset.
- 6000 high-fidelity samples identified as elbow point.
- 40% more HF data provided to single-fidelity baseline for fair comparison.

---

## Case Studies

Tested on IEEE benchmark systems:

- 9-bus
- 14-bus
- 30-bus
- 118-bus

Uncertainty modeling:
- Load: 60%–140% of baseline
- Renewable generation: 5%–15% of total generation
- Correlated multivariate Gaussian sampling
- 200 Monte Carlo trials per case
- N-1 generator and line contingencies

---

## Key Empirical Results

### Surrogate Accuracy (Power Flow Estimation)

Compared to single-fidelity GNN:

- Case 14 voltage magnitude MSE reduced from 1.45E-06 to 6.78E-07.
- Case 118 voltage magnitude MSE reduced from 1.03E-02 to 1.78E-03.
- Phase angle errors consistently reduced across all cases.

Multi-fidelity architecture improves both:
- Estimation accuracy
- Training data efficiency

---

### OPF Performance Under Uncertainty

Using EMF-GNN within HCC-OPF:

**Objective Function Relative Error**
- Case 30 reduced from 0.44 (SF-GNN) to 0.17.
- Case 118 reduced from 0.10 to 0.08.

**Distribution Similarity (Jensen–Shannon Divergence)**
- Case 118 reduced from 0.03 to 0.02.
- Case 14 reduced from 0.16 to 0.14.

Surrogate-based OPF achieves near-identical cost distributions compared to exact AC solver across 200 trials.

---

### Hybrid Correction Impact (Case 118)

Compared to fully surrogate-based CC-OPF:

| Metric | Surrogate-Only | Hybrid (Proposed) |
|--------|----------------|------------------|
| Constraint violation probability | 0.23 | 0.06 |
| Objective MRE | 0.11 | 0.03 |
| JSD | 0.08 | 0.02 |
| Iteration time (s) | 33.02 | 96.37 |
| Total optimization time (s) | 1554.21 | 1635.21 |

Constraint violation probability reduced by ~74%  
Objective error reduced by ~73%  
Total optimization time increased by only ~5%

Hybrid mechanism improves reliability without sacrificing scalability.

---

### N-1 Security Performance

Under random generator and line outages:

- Case 30 objective MRE reduced from 0.27 to 0.18.
- Case 118 objective MRE reduced from 0.103 to 0.097.
- Error levels remain stable despite topology perturbations.

Demonstrates robustness of topology-aware GNN under contingency shifts.

---

## Engineering Contributions

- Residual multi-fidelity GNN architecture for AC power flow.
- Surrogate-accelerated chance-constrained OPF.
- Hybrid constraint validation mechanism.
- Scalable performance across 9–118 bus systems.
- Monte Carlo + PSO optimization under correlated uncertainty.
- Open-source implementation:
  https://github.com/kamiarkhayam/HCCOPF-using-EMFGNN

---

## Relevance

Bridges:

- Probabilistic power system optimization  
- Graph-based deep learning  
- Multi-fidelity surrogate modeling  
- Reliability-aware hybrid optimization  

Enables real-time or near real-time OPF under renewable uncertainty while preserving operational constraint integrity.

---

## Publication

Khayambashi, K., Hasnat, M. A., & Alemazkoor, N.  
Hybrid Chance-Constrained Optimal Power Flow Under Load and Renewable Generation Uncertainty Using Enhanced Multi-Fidelity Graph Neural Networks.  
Journal of Machine Learning for Modeling and Computing, 5(4):53–76 (2024).
