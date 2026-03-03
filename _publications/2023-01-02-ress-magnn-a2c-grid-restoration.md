---
title: "GNN-based Multi-Agent Reinforcement Learning for Power Distribution Recovery"
collection: publications
category: manuscripts
permalink: /publication/2025-magnn-a2c-ress
excerpt: "Topology-aware multi-agent reinforcement learning framework for scalable post-hurricane power distribution restoration."
date: 2025-01-01
venue: "Reliability Engineering & System Safety"
paperurl: "https://github.com/kamiarkhayam/ma-gnn-a2c-grid-restoration"
citation: "Khayambashi, K., Hasnat, M. A., & Alemazkoor, N. (2025). GNN-based multi-agent reinforcement learning for power distribution recovery. Reliability Engineering & System Safety."
---
This paper introduces **MAGNN-A2C**, a graph neural network–enhanced multi-agent reinforcement learning framework for post-hurricane power distribution system restoration. The approach models each repair crew as an autonomous agent operating under a centralized-training–decentralized-execution paradigm, enabling scalable and coordinated repair sequencing in large distribution networks.

A graph convolutional encoder captures grid topology and component interdependencies, allowing agents to prioritize structurally critical repairs that accelerate network re-energization. The learning objective minimizes cumulative Value of Lost Load (VoLL), directly linking repair decisions to socioeconomic outage impacts.

Evaluation on a real-world-scale case study of Galveston Island (>16,000 nodes) demonstrates consistent improvement over rule-based and genetic algorithm baselines, including:

- 18–23% reduction in cumulative outage cost  
- Faster recovery trajectories and higher resilience metrics  
- Strong generalization to unseen storm tracks and damage patterns  

Ablation studies confirm that both the GNN-based state representation and the A2C learning algorithm are essential to performance gains, highlighting the importance of topology-aware coordination in large-scale restoration planning.

**Methods:** Multi-agent reinforcement learning (A2C), graph neural networks (GCN), centralized training with decentralized execution (CTDE), stochastic restoration simulation  

[Code](https://github.com/kamiarkhayam/ma-gnn-a2c-grid-restoration)
