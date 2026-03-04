---
title: "Multi-Fidelity Graph Neural Networks for Efficient Power Flow Analysis"
collection: portfolio
permalink: /project/mf-gnn-powerflow
excerpt: "Residual multi-fidelity graph neural network framework enabling scalable probabilistic power flow analysis under high-dimensional renewable and load uncertainty."
---

## Overview

Developed a multi-fidelity Graph Neural Network (MF-GNN) framework to accelerate AC power flow analysis under high-dimensional uncertainty in electricity demand and renewable generation.

Probabilistic power flow traditionally requires thousands of nonlinear AC simulations, which becomes computationally expensive for large systems. The proposed framework addresses this challenge by combining inexpensive DC simulations with a residual graph-based learning architecture that approximates high-fidelity AC results.

This approach significantly reduces the amount of expensive simulation data required while maintaining high predictive accuracy.

---

## Technical Architecture

The framework represents the power grid as a graph and learns system behavior using a residual multi-fidelity architecture.

### Graph-Based Power System Representation

- Buses represented as graph nodes  
- Transmission lines represented as edges  
- Node features include load, generation, and voltage operating conditions  
- Graph message passing captures electrical interactions across the network  

### Multi-Fidelity Residual Learning

The model consists of two coordinated learning stages:

- **Low-fidelity model:** trained on DC power flow simulations to predict baseline system behavior.  
- **High-fidelity model:** learns residual corrections to approximate full AC power flow results.

By learning the difference between low- and high-fidelity simulations, the model reduces approximation complexity and improves generalization while requiring far fewer high-fidelity training samples.

---

## Key Capabilities

- Scalable surrogate modeling for probabilistic AC power flow  
- Significant reduction in required high-fidelity simulation data  
- Graph-based learning that captures power system topology  
- Robust performance under uncertainty in load and renewable generation  
- Improved generalization to unseen network configurations  

---

## Experimental Evaluation

The framework was evaluated using multiple IEEE benchmark systems ranging from small test networks to large transmission systems.

Uncertainty scenarios included variations in electricity demand and distributed renewable generation. The model was trained using a combination of DC and AC simulation data and compared against several machine learning baselines, including dense neural networks and single-fidelity graph models.

---

## Empirical Impact

Results demonstrate consistent improvements in accuracy, data efficiency, and computational performance.

Key outcomes include:

- Significant accuracy improvement compared to single-fidelity GNN and dense neural network surrogates  
- Accurate prediction of voltage magnitude and phase angle under high-dimensional uncertainty  
- Up to **70% reduction in high-fidelity training data requirements**  
- **Orders-of-magnitude reduction in model size** compared with dense multi-fidelity neural networks  
- **Sub-millisecond inference time**, enabling rapid probabilistic power flow evaluation  

The residual multi-fidelity architecture also improves robustness under topology perturbations such as line outages.

---

## Engineering Deliverables

- Multi-fidelity graph neural network architecture for power flow analysis  
- Probabilistic power flow surrogate modeling pipeline  
- Dataset generation workflow combining AC and DC simulations  
- Benchmark evaluation framework for uncertainty-driven grid analysis  
- Reproducible code and experimental datasets  

---

## Relevance

Efficient probabilistic power flow analysis is essential for modern power systems with high renewable penetration and increasing operational uncertainty.

This project demonstrates how multi-fidelity learning and graph-based modeling can dramatically reduce computational costs while preserving accuracy, enabling scalable reliability analysis and real-time grid analytics.

---

## Publication

Taghizadeh, M., Khayambashi, K., Hasnat, M. A., & Alemazkoor, N.  
*Multi-fidelity graph neural networks for efficient power flow analysis under high-dimensional demand and renewable generation uncertainty.*  
Electric Power Systems Research, 237 (2024), 111014.
