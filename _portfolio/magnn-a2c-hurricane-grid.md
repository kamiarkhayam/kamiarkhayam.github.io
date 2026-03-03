---
title: "Topology-Aware Multi-Agent Reinforcement Learning for Post-Hurricane Grid Recovery"
collection: projects
permalink: /project/magnn-a2c-grid-restoration
excerpt: "Graph Neural Network–based multi-agent reinforcement learning framework for scalable, topology-aware power distribution system recovery after hurricanes."
---

This project develops a scalable multi-agent reinforcement learning framework for optimizing post-hurricane power distribution system restoration under complex network interdependencies and limited repair resources.

The system integrates:

• Multi-Agent Markov Decision Process formulation for repair sequencing  
• Graph Neural Network encoder for topology-aware state representation  
• Centralized Training with Decentralized Execution (CTDE) architecture  
• Advantage Actor–Critic (A2C) learning with Generalized Advantage Estimation  
• High-fidelity hurricane hazard simulation and fragility-based damage modeling  
• Stochastic repair-time modeling with multi-crew coordination  

The restoration environment models:

• >16,000-node real-world distribution network (Galveston Island, TX) :contentReference[oaicite:0]{index=0}  
• Hurricane wind-field simulation and component fragility sampling  
• Sector-specific Value of Lost Load (VoLL) modeling  
• Sequential, parallel crew dispatch with evolving network connectivity  
• Resilience metrics including cumulative VoLL cost, unserved energy, time-to-80% restoration, and recovery-curve area  

Key technical contributions include:

• First real-world-scale validation of a GNN-enhanced multi-agent RL framework for distribution restoration  
• Explicit encoding of network topology to capture global re-energization pathways  
• Demonstration of scalability beyond small test feeders  
• Robust generalization to unseen storm tracks and damage realizations  

Impact:

• 18–23% reduction in cumulative outage cost relative to rule-based and genetic algorithm baselines  
• ~$70–$120 million avoided economic losses per major hurricane  
• Reduction in unserved energy from 182–275 GWh (baselines) to 117 GWh  
• Faster restoration trajectories with significantly higher recovery-curve area  
• Deployment-time inference faster than heuristic baselines after one-time offline training  

The framework follows a train-once–deploy-many paradigm: several hours of offline training produce a reusable policy capable of real-time restoration decision support.

## Related Publication

Khayambashi, K., Hasnat, M. A., & Alemazkoor, N.  
GNN-based multi-agent reinforcement learning for power distribution recovery.  
*Reliability Engineering & System Safety.*

## Code Repository

[GitHub – MAGNN-A2C Grid Restoration](https://github.com/kamiarkhayam/ma-gnn-a2c-grid-restoration)
