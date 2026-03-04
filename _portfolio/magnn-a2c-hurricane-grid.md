---
title: "MAGNN-A2C: Graph Neural Network–Based Multi-Agent Reinforcement Learning for Post-Hurricane Grid Restoration"
collection: portfolio
permalink: /project/magnn-a2c-hurricane-restoration
excerpt: "Topology-aware multi-agent reinforcement learning framework for scalable, coordinated power distribution system restoration after hurricanes."
---

## Overview

Developed a scalable multi-agent reinforcement learning framework (MAGNN-A2C) for optimizing post-hurricane power distribution system restoration.

The framework models each repair crew as an autonomous agent and integrates Graph Neural Networks (GNNs) with Advantage Actor–Critic (A2C) learning under a centralized-training–decentralized-execution paradigm to learn coordinated, topology-aware repair policies.

---

## Technical Architecture

- Multi-Agent Markov Decision Process (MAMDP) formulation  
- Graph Convolutional Network (2 layers, 64 hidden dimensions) for topology-aware state encoding  
- Decentralized actor networks (one per repair crew)  
- Centralized critic with global graph pooling  
- Centralized Training, Decentralized Execution (CTDE)  
- Advantage Actor–Critic (A2C) optimization with Generalized Advantage Estimation (GAE)  
- Stochastic hurricane hazard simulation (Holland wind model + decay modeling)  
- Fragility-based component damage assessment (poles, substations, towers)  
- Stochastic repair time sampling (lognormal, normal, truncated distributions)  
- Value of Lost Load (VoLL)–weighted restoration objective  

Environment scale:

- Real-world distribution system: Galveston Island, Texas  
- 16,037 nodes and 16,834 edges  
- 15,679 wooden poles, 268 concrete poles, 81 transmission towers, 9 substations  

---

## Key Capabilities

- Topology-aware repair prioritization using GNN message passing  
- Explicit multi-crew coordination through MARL formulation  
- Learning reusable restoration policies (train-once–deploy-many)  
- Economic-impact–aware optimization via VoLL-weighted rewards  
- Scalable restoration over large real-world distribution networks  
- Robust generalization to unseen hurricane tracks and damage patterns  

---

## Case Study Configuration

**Region:** Galveston Island, Texas  
**Hazard modeling:** Synthetic Category 3 hurricane (track + intensity), fragility-based damage  
**Evaluation horizon:** 720 hours (30 days)  
**Comparison baselines:**  
- Rule-based restoration heuristic  
- Decentralized genetic algorithm (GA)  

**Crew configurations tested:** 8, 10, and 12 repair crews  

---

## Empirical Impact

- 18–23% reduction in cumulative outage cost relative to baselines  
- $70–120M avoided socio-economic losses per major hurricane  
- Aurc (area under recovery curve): 0.768 vs 0.637 (rule-based) and 0.454 (GA)  
- Total unserved energy reduced to 116.9 GWh (vs 182.7 and 275 GWh)  
- Time to restore 80% load reduced to 353.9 hours (vs 356.8 and 524.7 hours)  
- Faster inference than rule-based heuristic (≈30–40 s vs 60–70 s per episode)  

Policy generalized successfully to:

- Randomized damage realizations  
- Perturbed storm tracks (±10 km, ±5° bearing)  
- Weaker Category 2 storms  

Results demonstrate that topology-aware multi-agent coordination materially improves recovery speed, outage impact, and resilience metrics without increasing operational decision time.

---

## Engineering Deliverables

- High-fidelity restoration simulation environment  
- Hurricane hazard generation and fragility-based damage pipeline  
- Multi-agent RL training framework (PyTorch + PyTorch Geometric)  
- GNN encoder with partitioned decentralized actors  
- Baseline benchmarking suite (rule-based, GA, PPO variants, encoder ablations)  
- Reproducible evaluation pipeline with resilience metric tracking  

---

## Relevance

Establishes a scalable, topology-aware decision-support framework for post-disaster grid restoration.

Bridges reinforcement learning, graph representation learning, infrastructure resilience modeling, and real-world-scale distribution system operations to support utilities facing increasingly severe hurricane risk.

---

## Related Publication

Khayambashi, K., Hasnat, M. A., & Alemazkoor, N.  
A Graph Neural Network-based Multi-agent Reinforcement Learning Model for Efficient Power Distribution System Recovery After Hurricanes.  
*Reliability Engineering & System Safety (under review).*
