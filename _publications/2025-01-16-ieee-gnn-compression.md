---
title: "Graph Neural Networks for Precision-Guaranteed Compression of Large-Scale Data"
collection: publications
category: manuscripts
permalink: /publication/2024-ieee-bigdata-gnn-compression
excerpt: "GNN-based prediction framework enabling direct control over decompression error for large-scale spatio-temporal data."
date: 2024-12-01
venue: "IEEE International Conference on Big Data"
paperurl: "https://ieeexplore.ieee.org/abstract/document/10825665"
citation: "Khayambashi, K., & Alemazkoor, N. (2024). Graph neural networks for precision-guaranteed compression of large-scale data. <i>Proceedings of the IEEE International Conference on Big Data</i>."
---
Published in *IEEE International Conference on Big Data* (2024).

Rapid expansion of smart infrastructure has led to massive volumes of spatio-temporal data that challenge storage and transmission systems. Traditional lossy compression techniques often lack explicit control over reconstruction error, while prediction-based methods struggle to scale across large, spatially distributed networks.

This work introduces a prediction-based compression framework using Graph Neural Networks (GNNs) that guarantees a user-defined decompression error threshold. A single global model is trained to perform one-step-ahead predictions across thousands of spatially connected nodes, discarding data points when prediction error remains below a specified tolerance and retaining only high-error observations.

The method is evaluated on three large-scale datasets:

- U.S. solar PV generation data (>5,000 plants, 5-minute resolution)
- California traffic sensor data (700 stations, 2023)
- ComEd smart meter data (~22,000 spatial units, 2 years)

Results show that GNN-based compression consistently achieves lower compression ratios than traditional methods (WT, DCT, PCA) and other deep learning architectures while maintaining strict error guarantees. The approach demonstrates strong scalability and parameter efficiency, making it suitable for real-time smart infrastructure applications.

**Keywords:** predictive compression, graph neural networks, spatio-temporal modeling, smart infrastructure, big data  

[Paper]({{ page.paperurl }}) | [Code](https://github.com/kamiarkhayam/BigData-Compression-GNN)
