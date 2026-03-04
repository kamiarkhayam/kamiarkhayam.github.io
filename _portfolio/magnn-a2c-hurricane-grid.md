---
title: "MAGNN-A2C: Graph Neural Network–Based Multi-Agent Reinforcement Learning for Post-Hurricane Grid Restoration"
collection: portfolio
permalink: /project/magnn-a2c-hurricane-restoration
excerpt: "Topology-aware multi-agent reinforcement learning framework for scalable power distribution system restoration after hurricanes."
---

## Overview

Developed a reinforcement learning framework for optimizing post-hurricane power distribution system restoration.

The approach treats repair crews as coordinated decision-making agents and uses graph neural networks to capture the topology of the power grid. The resulting system learns restoration strategies that prioritize repairs based on their system-wide impact on connectivity, load recovery, and outage costs.

Rather than solving a single large optimization problem for each disaster scenario, the framework learns reusable restoration policies that can guide real-time repair sequencing.

---

## Technical Architecture

The framework integrates three main components:

- **Multi-agent reinforcement learning (MARL)** to model parallel repair crews operating across the network  
- **Graph neural networks (GNNs)** to encode grid topology and spatial dependencies between components  
- **Advantage Actor–Critic (A2C)** learning with centralized training and decentralized execution  

A simulation environment models hurricane hazards, infrastructure damage, and restoration dynamics. Agents interact with this environment to learn coordinated repair policies that reduce outage impacts while respecting operational constraints.

The reward function is based on **Value of Lost Load (VoLL)**, allowing the model to prioritize repairs that restore high-impact loads and critical infrastructure.

---

## Key Capabilities

- Topology-aware repair prioritization through graph-based state representation  
- Coordinated decision-making across multiple repair crews  
- Adaptive restoration strategies that respond to evolving grid conditions  
- Reusable policies enabling rapid post-disaster decision support  
- Integration of economic outage impact into restoration planning  

---

## Case Study

The framework was evaluated on the Galveston, Texas, power distribution system exposed to hurricane hazards.

The simulation environment incorporates:

- Hurricane wind-field modeling and infrastructure fragility assessment  
- Probabilistic component damage and repair-time modeling  
- Sequential restoration dynamics with multiple repair crews  
- Sector-based electricity demand and outage impact valuation  

This environment allows restoration strategies to be evaluated using resilience metrics such as service restoration trajectories, cumulative outage cost, and unserved energy.

---

## Empirical Impact

The learned restoration policy consistently outperforms conventional restoration approaches.

Key outcomes include:

- Reduced cumulative outage costs during hurricane recovery scenarios  
- Faster restoration of electricity service across affected communities  
- Improved recovery trajectories and reduced unserved energy  
- Robust performance across different crew sizes and storm scenarios  

The model also generalizes well to unseen damage patterns and alternative storm tracks, indicating that it learns structural restoration principles rather than scenario-specific repair sequences.

---

## Engineering Deliverables

- High-fidelity post-disaster restoration simulation environment  
- Multi-agent reinforcement learning training framework  
- Graph neural network encoder for grid topology representation  
- Benchmark comparison pipeline including heuristic and evolutionary methods  
- Reproducible experimental workflow for restoration policy evaluation  

---

## Relevance

Efficient restoration strategies are increasingly important as extreme weather events intensify and grid infrastructure faces growing reliability challenges.

This project demonstrates how reinforcement learning and graph-based modeling can support scalable decision-making for infrastructure recovery, enabling utilities to deploy repair crews more effectively and accelerate community recovery after major disruptions.

---

## Related Publication

Khayambashi, K., Hasnat, M. A., & Alemazkoor, N.  
*A Graph Neural Network–based Multi-agent Reinforcement Learning Model for Efficient Power Distribution System Recovery After Hurricanes.*  
Under review at **Reliability Engineering & System Safety**.
