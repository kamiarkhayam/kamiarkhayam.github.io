---
title: "Leveraging Hyperscale Data Centers to Support Power System Reliability and Resilience"
collection: portfolio
permalink: /project/data-center-restoration-anchors
excerpt: "Resilience-oriented restoration framework that models hyperscale data centers as active 'restoration anchors' using graph neural network–based reinforcement learning under extreme weather disruptions."
---

## Overview

Developed a resilience-focused modeling framework that redefines hyperscale data centers as active infrastructure assets rather than passive electricity loads.

Rapid growth in AI-driven hyperscale data centers is reshaping grid demand patterns while increasing the consequences of widespread outages under extreme weather. Although these facilities possess behind-the-meter flexibility (UPS systems, battery storage, controllable cooling and computing), current restoration practice treats them as self-protecting loads that disconnect during disturbances.

This project systematically evaluates when and how selected data centers can serve as **restoration anchors** to support post-disaster grid recovery while preserving their own operational survivability constraints :contentReference[oaicite:0]{index=0}.

---

## Technical Contributions

### 1. Resilience-Oriented Restoration Formulation

Formulated a restoration optimization framework that coordinates:

- Distribution network reconfiguration  
- Prioritized community load restoration  
- Data center internal generation and storage availability  
- Uncertain damage and repair conditions  

Modeled data centers as hybrid infrastructure nodes capable of:

- Controlled load modulation  
- Temporary islanded support  
- Coordinated reconnection  

Objective minimizes Value of Lost Load (VOLL)–weighted unserved energy while enforcing data center survivability constraints.

---

### 2. Graph Neural Network–Based Reinforcement Learning

Developed a scalable decision-making policy using:

- Graph-structured representation of distribution networks  
- Node features: load criticality, outage status, topology position  
- Edge features: line availability and switching constraints  
- Embedded data center operational states  

Trained a graph neural network–based reinforcement learning (GNN-RL) agent to generate restoration actions that:

- Reduce unserved critical load  
- Accelerate time-to-restore  
- Avoid compromising data center reliability  

This approach enables adaptive restoration decisions over evolving grid states under uncertainty.

---

### 3. Hurricane-Driven Outage Simulation Studies

Conducted simulation experiments on benchmark distribution systems under extreme weather scenarios:

- Scenario-based line failures and stochastic repair timelines  
- Comparison of three strategies:
  - Conventional restoration  
  - Data center self-preservation only  
  - Coordinated restoration-anchor strategy  

Performance evaluated using:

- VOLL-weighted unserved energy  
- Time-to-restore critical loads  
- Robustness across uncertainty realizations  

---

## Key Findings and Impact

- Demonstrated measurable reduction in outage duration for critical community loads when data centers act as coordinated restoration anchors  
- Quantified resilience gains relative to conventional restoration practices  
- Established operational conditions under which data center support enhances recovery without violating internal reliability requirements  
- Provided structured framework for integrating large digital loads into utility restoration planning  

The project reframes hyperscale data centers from sources of grid stress to programmable resilience resources.

---

## Broader Significance

Highly relevant to national infrastructure planning in the United States, where AI-driven data center expansion is rapidly increasing concentrated demand and outage consequences.

Offers evidence-based guidance for:

- Utilities managing large digital interconnections  
- Policymakers evaluating reliability and resilience standards  
- Infrastructure planners balancing cost, flexibility, and recovery performance  

Supports integration of emerging digital infrastructure into broader critical-infrastructure resilience strategies under increasing climate-driven disruption risks.

---

## Role

Lead Researcher and Primary Author.

Individually responsible for:

- Formulating the resilience-oriented restoration model  
- Developing the GNN-based reinforcement learning policy  
- Designing evaluation metrics (VOLL-weighted unserved energy, restoration time)  
- Conducting hurricane-driven simulation studies  
- Interpreting results in the context of infrastructure planning and grid reliability  

