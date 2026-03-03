---
title: "Multi-Fidelity Graph Neural Networks for Efficient Power Flow Analysis"
collection: portfolio
permalink: /project/mf-gnn-powerflow
excerpt: "Residual multi-fidelity GNN framework for scalable probabilistic power flow under high-dimensional renewable and load uncertainty."
---

## Overview

Developed a residual multi-fidelity Graph Neural Network (MF-GNN) framework to accelerate AC power flow analysis under high-dimensional uncertainty in load and renewable generation.

The framework addresses two key bottlenecks in modern probabilistic power flow:

1. Computational burden of repeated nonlinear AC simulations.
2. Large high-fidelity data requirements for training deep learning surrogates.

By fusing low-cost DC simulations with high-fidelity AC simulations through a residual graph-based architecture, the proposed MF-GNN achieves higher accuracy with significantly reduced data-generation cost.

Published in *Electric Power Systems Research* (2024).

---

## Technical Architecture

### 1. Graph-Based Power System Representation

- Buses modeled as nodes.
- Transmission lines modeled as edges.
- Node features:
  - Active/reactive demand
  - Active generation (including distributed renewables)
  - Voltage setpoint
- Adjacency matrix explicitly incorporated into learning.

Three WL-GNN layers (64 hidden units each) with sum aggregation were used.

---

### 2. Multi-Fidelity Residual Structure

**Low-Fidelity GNN (LF-GNN)**
- Trained on DC power flow data.
- Predicts phase angles only.
- MSE loss on DC phase angle outputs.

**High-Fidelity GNN (HF-GNN)**
- Takes LF phase angle estimates + voltage magnitude baseline.
- Learns residual corrections to AC solution.
- Predicts:
  - Voltage magnitude
  - Phase angle
- Residual learning reduces approximation complexity.

This design allows:
- Smaller high-fidelity dataset
- Reduced overfitting
- Improved generalization to unseen topologies

---

## Experimental Design

Tested on IEEE benchmark systems:

- 9-bus
- 14-bus
- 30-bus
- 118-bus
- 2383-bus Polish system

Uncertainty modeling:

- Active/reactive demand ~ Gaussian (5% std of mean)
- Distributed renewable generation at load buses
- High-dimensional correlated sampling
- ACPF = high-fidelity
- DCPF = low-fidelity

Training setup:

- 70% training / 20% validation / 10% testing
- 1000 epochs
- Adam optimizer (lr = 0.001)
- NVIDIA RTX 4090 GPU
- Hyperparameter search via Optuna

---

## Key Quantitative Results

### 1. Accuracy Improvement

MF-GNN consistently outperformed:

- Single-fidelity GNN (SF-GNN)
- Local DNN
- Global DNN
- Support Vector Regression
- Multi-Fidelity NN (MF-NN)

Example MAE reductions (scaled ×10⁻³):

**IEEE 118-bus**
- Voltage magnitude:
  - MF-GNN: 0.687
  - SF-GNN: 1.194
- Phase angle:
  - MF-GNN: 6.379
  - SF-GNN: 6.940

With exact DCPF input:
- Voltage magnitude MAE reduced to 0.312
- Phase angle MAE reduced to 0.392

---

### 2. Data Efficiency & Computational Savings

MF-GNN trained with:
- 6000 high-fidelity + 12,000 low-fidelity samples

Achieved higher accuracy than:
- SF-GNN trained with 28,000 high-fidelity samples

Training data generation time:
- MF-GNN: 38.2 s
- SF-GNN: 127.4 s  
→ 70% reduction in computational cost

For Polish 2383-bus system:
- MF-GNN data generation: 61 s
- SF-GNN data generation: 1470 s  
→ >95% reduction

---

### 3. Model Compactness

For Polish 2383-bus system:

| Model | Trainable Parameters | Inference Time |
|-------|----------------------|----------------|
| MF-GNN | 70,148 | 0.00023 s |
| MF-NN | 159,084,321 | 0.02227 s |

MF-GNN uses >2000× fewer parameters and is ~100× faster at inference.

---

### 4. Robustness to Topology Perturbation

Under single-line outages:

**IEEE 118-bus (scaled ×10⁻³)**  
Voltage magnitude MAE:
- MF-GNN: 0.910
- SF-GNN: 1.255

Phase angle MAE:
- MF-GNN: 9.559
- SF-GNN: 10.023

Residual multi-fidelity structure improves contingency robustness.

---

### 5. Generalization to Unseen Grid Topologies

Trained on:
- 9, 14, 30, 118-bus systems

Tested on:
- 24-bus and 39-bus systems (unseen)

MF-GNN consistently outperformed SF-GNN, demonstrating improved cross-topology generalization due to:

- Graph-structured learning
- Reduced overfitting in residual HF component
- Multi-fidelity data enrichment

---

## Engineering Contributions

- Residual multi-fidelity GNN architecture for AC power flow.
- Scalable probabilistic power flow surrogate under high-dimensional uncertainty.
- Robust to topology perturbations.
- Generalizes to unseen grid structures.
- Orders-of-magnitude parameter reduction compared to dense multi-fidelity NN.
- Open-source code and dataset provided.

---

## Relevance

Advances surrogate modeling for:

- Probabilistic power flow
- Renewable integration analysis
- High-dimensional uncertainty quantification
- Contingency screening
- Real-time grid analytics

Directly supports scalable reliability analysis for modern power systems with deep renewable penetration and electrification growth.

---

## Publication

Taghizadeh, M., Khayambashi, K., Hasnat, M. A., & Alemazkoor, N.  
Multi-fidelity graph neural networks for efficient power flow analysis under high-dimensional demand and renewable generation uncertainty.  
Electric Power Systems Research, 237 (2024) 111014.
