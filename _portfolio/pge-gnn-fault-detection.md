---
title: "Temporal Graph Neural Networks for Failure and Cause Prediction in Transmission Networks"
collection: portfolio
permalink: /project/pge-temporal-gnn-failure-prediction
excerpt: "Utility-scale graph learning framework for structure-level failure localization and cause prediction across large transmission networks."
---

## Overview

Developed temporal Graph Neural Network (GNN) models for large-scale transmission infrastructure in collaboration with Pacific Gas and Electric Company (PG&E).

The project focuses on transforming raw asset inventories, span connectivity data, and historical outage records into graph-structured datasets to enable structure-level failure localization and cause prediction under highly imbalanced, real-world operational conditions.

The framework supports proactive reliability planning by shifting from reactive failure analysis to predictive, topology-aware risk assessment.

---

## Technical Contributions

### 1. Scalable Graph Construction Pipeline

Designed and implemented a utility-scale graph-building engine that converts raw utility records into structured power-grid graphs:

- Nodes: transmission structures (poles/towers)  
- Edges: physical spans connecting structures  
- Node features: design attributes, age, environmental exposure layers, insulator aggregates  
- Edge features: conductor properties, span geometry  

Constructed event-level graph instances with shared topology and event-specific failure labels, enabling temporal train/validation/test splits aligned with operational timelines.

---

### 2. Multi-Task Temporal GNN Modeling

Developed multi-task learning architectures to jointly perform:

- **Node-level failure localization** (identify failed structure within large graph)  
- **Graph-level failure cause classification** (≈10–12 operational cause categories)

Core modeling components:

- Graph Attention Network (GATv2) backbone  
- Temporal data splits based on outage timestamps  
- Pointer-style localization objective to handle extreme class imbalance  
- Candidate-set sampling using k-hop neighborhoods  
- Class-balanced and focal-style losses for rare-event learning  

Designed topology-aware evaluation metrics including Recall@k and graph-distance-to-true-failure to reflect operational usefulness rather than naive accuracy.

---

### 3. Coarse-Graph and Feature Selection Experiments

Implemented supernode-based coarse graph representations to:

- Study information bottlenecks under aggregation  
- Perform distance-aware soft labeling  
- Evaluate top-k performance across reduced graph resolutions  

This experimentation quantified trade-offs between computational efficiency and spatial localization precision.

---

### 4. Asset Lifecycle and Insulator Analytics

Developed analytical modules to examine:

- Insulator replacement vs addition detection  
- Age distribution and material evolution trends  
- Data currency validation across decades of records  

Generated lifecycle summaries and structured reports to inform graph feature engineering and reliability insights.

---

### 5. Connectivity and GIS-Based Network Analytics

Conducted large-scale graph diagnostics:

- Connected component analysis  
- Degree distributions and structural bottleneck identification  
- Temporal failure trend analysis  
- OpenStreetMap-based interactive GIS visualization of structures and failure clusters  

Enabled domain experts to interpret learned patterns in spatial and network context.

---

## Impact

- Converted heterogeneous utility asset records into scalable graph datasets with ~10⁵ nodes per network instance  
- Enabled structure-level predictive failure localization under extreme class imbalance  
- Integrated topology-aware metrics aligned with utility operational decision-making  
- Provided interpretable spatial analytics linking network structure to failure patterns  
- Supported transition toward predictive reliability planning and early-warning systems  

---

## Relevance

Demonstrates deployment of advanced graph machine learning in real-world utility operations.

Bridges:

- Infrastructure asset analytics  
- Graph deep learning  
- Temporal failure modeling  
- GIS-based network interpretation  
- Reliability engineering for large-scale power systems  

Establishes a reusable blueprint for graph-based predictive maintenance in critical infrastructure networks.
