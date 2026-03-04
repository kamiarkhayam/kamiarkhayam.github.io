---
title: "Leveraging Hyperscale Data Centers as Restoration Anchors for Grid Resilience"
collection: portfolio
permalink: /project/data-center-restoration-anchors
excerpt: "Graph Neural Network–based reinforcement learning framework for integrating hyperscale data centers into post-disaster distribution system restoration."
---

## Overview

Developed a resilience-oriented restoration framework that treats selected hyperscale data centers as coordinated infrastructure assets rather than passive electricity loads during extreme weather disruptions.

The framework integrates distribution reconfiguration, survivability constraints, and Graph Neural Network–based reinforcement learning to quantify how large controllable loads can accelerate community recovery without compromising internal reliability.

---

## Technical Architecture

- Distribution network reconfiguration under uncertain damage and repair timelines  
- Explicit modeling of behind-the-meter data center resources (UPS, storage, controllable load)  
- Survivability-constrained restoration optimization  
- Graph Neural Network–based reinforcement learning for scalable policy learning  
- Scenario-based hurricane outage modeling with stochastic repair processes  
- Value of Lost Load (VoLL)–weighted objective formulation  

Restoration environment models:

- Benchmark distribution test feeders with hurricane-driven line failures  
- Time-varying component availability and access constraints  
- Critical-facility prioritization (hospitals, water systems, emergency services)  
- Coordinated load restoration subject to data center operational envelopes  
- Resilience metrics including VoLL-weighted unserved energy, time-to-restore critical loads, and restoration trajectory performance  

---

## Key Capabilities

- Topology-aware GNN encoder for structured network state representation  
- Joint optimization of community recovery objectives and data center survivability constraints  
- Learning-based restoration policy scalable to large distribution networks  
- Explicit quantification of resilience trade-offs across restoration strategies  
- Integration of digital infrastructure into distribution-level emergency operations modeling  

---

## Case Study Configuration

**Network:** Benchmark distribution test systems with hurricane-induced damage scenarios  
**Hazard modeling:** Stochastic line failures and repair-time distributions  
**Operational constraints:** Data center backup duration, load flexibility bounds, survivability thresholds  
**Objective:** Minimize VoLL-weighted unserved energy while preserving anchor facility integrity  

---

## Empirical Impact

- Reduced VoLL-weighted unserved energy relative to conventional restoration strategies  
- Accelerated restoration of critical community loads under severe outage scenarios  
- Identified operational regimes where data center flexibility improves system recovery without degrading internal reliability  
- Quantified resilience value relative to self-preservation-only restoration strategies  

Results demonstrate that hyperscale digital infrastructure can function as programmable restoration assets rather than passive high-load stressors.

---

## Engineering Deliverables

- Distribution restoration simulation environment with stochastic damage modeling  
- GNN-based reinforcement learning restoration agent  
- Data center operational constraint modules  
- Scenario-generation and Monte Carlo evaluation pipeline  
- Resilience metric computation and benchmarking framework  

---

## Relevance

Reframes hyperscale data centers from grid stressors to resilience-enabling infrastructure under extreme events.

Framework bridges reinforcement learning, distribution system restoration, and digital infrastructure planning to support utilities facing rapid AI-driven load growth and increasing climate risk.

---

## Related Publication

Khayambashi, K., & Alemazkoor, N.  
Leveraging hyperscale data centers to support power system reliability and resilience.  
*In preparation.*
