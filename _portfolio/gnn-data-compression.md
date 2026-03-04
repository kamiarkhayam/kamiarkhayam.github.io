---
title: "Precision-Guaranteed GNN-Based Predictive Compression for Large-Scale Infrastructure Data"
collection: portfolio
permalink: /project/gnn-precision-compression
excerpt: "Graph neural network framework for prediction-based compression with explicit decompression error guarantees across large-scale spatio-temporal datasets."
---

## Overview

Developed a precision-controlled predictive compression framework leveraging Graph Neural Networks (GCNs) to reduce storage requirements of large-scale spatio-temporal infrastructure data while guaranteeing user-defined decompression accuracy.

The method replaces traditional transform-based compression with a learned spatio-temporal prediction engine that selectively stores only high-error data points.

---

## Technical Architecture

- Global one-step-ahead predictive model trained across all monitoring nodes  
- Graph Convolutional Network (3 layers × 64 hidden dimensions) :contentReference 
- Sequence length: 4 timesteps for spatio-temporal context :contentReference
- Delaunay triangulation–based graph construction (spatial datasets) :contentReference
- k-Nearest Neighbor graph (pattern-similarity–based traffic dataset) :contentReference
- Iterative threshold-controlled predictive discard algorithm (Algorithm 1) :contentReference
- Explicit decompression error bound enforcement  

Loss function: Mean Squared Error  
Evaluation metrics: MAE, MSE, compression ratio, parameter count  

GCN achieved highest accuracy with only ~4.7k parameters compared to millions for CNN/LSTM models

---

## Key Capabilities

- Direct control over maximum decompression error  
- Real-time or post-collection compression applicability  
- Low-parameter model footprint for storage-efficient deployment  
- Reduced error accumulation via threshold-based reset logic
- Superior compression ratio compared to WT, DCT, PCA, and other DL models

---

## Datasets Evaluated

**1. NREL Solar PV Generation (U.S., 5,000+ plants, 5-min resolution)**
**2. Caltrans Traffic Speeds (700 sensors, 5-min resolution)**
**3. ComEd Energy Consumption (≈22,000 zip-code nodes, 30-min resolution)** 

Each dataset spans 1–2 years and includes thousands of monitoring locations.

---

## Empirical Impact

- Discarded up to 78% of datapoints at selected thresholds (traffic dataset example)
- Achieved compression ratios as low as 0.22 while maintaining bounded error
- Consistently outperformed wavelet transform (WT), discrete cosine transform (DCT), PCA, and deep learning baselines
- Demonstrated robustness across heterogeneous infrastructure domains  

Results confirm that spatio-temporal graph modeling materially improves predictive compression efficiency compared to both classical and sequence-only deep learning approaches.

---

## Engineering Deliverables

- PyTorch implementation of GCN-based compression framework  
- Modular graph-construction utilities  
- Multi-architecture benchmarking pipeline (GCN, GT, CNN, LSTM, MLP)  
- Threshold-controlled compression engine  
- Reproducibility scripts and dataset preprocessing modules  

---

## Relevance

Positions graph learning as a storage-efficiency technology for smart infrastructure systems, where sensor density and sampling frequency increasingly challenge data management capabilities.

Framework bridges machine learning, infrastructure analytics, and systems-level storage optimization.

---

## Related Publication

Khayambashi, K., & Alemazkoor, N. (2024).  
Graph neural networks for precision-guaranteed compression of large-scale data.  
*IEEE International Conference on Big Data.*

[View Publication](/publication/2024-ieee-gnn-compression)
