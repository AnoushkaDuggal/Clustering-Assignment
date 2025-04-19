# Clustering-Assignment

## Overview

This assignment performs an evaluation of three clustering algorithms — **K-Means**, **Hierarchical Clustering**, and **Mean Shift** — on a UCI dataset. The goal is to study the impact of various preprocessing techniques on clustering performance using internal validation metrics.

---

## Methodology

The analysis involves applying multiple preprocessing strategies:

- No Preprocessing  
- Normalization  
- Standardization  
- PCA (Principal Component Analysis)  
- Standardization + PCA  

Each preprocessing technique is followed by clustering using:

- K-Means (with cluster sizes `k = 3, 4, 5`)  
- Agglomerative (Hierarchical) Clustering (`k = 3, 4, 5`)  
- Mean Shift (auto-detects number of clusters)  

### Evaluation Metrics

Clustering quality is evaluated using the following internal metrics:

- **Silhouette Score**: Measures cohesion and separation; ranges from -1 to 1 (higher is better).
- **Calinski-Harabasz Index**: Indicates within-cluster dispersion; higher values are better.
- **Davies-Bouldin Index**: Represents average similarity between clusters; lower values are better.

---

## Results Summary

### Best Observations

- **K-Means** achieved a **Silhouette score of 1.0** under PCA, indicating excellent separation of clusters.
- **Mean Shift** clustering also produced **perfect Silhouette scores** when combined with PCA.
- **Hierarchical Clustering** yielded optimal scores using PCA and no preprocessing.

### Influence of Preprocessing

- **PCA** significantly improved clustering performance across all methods.
- **Normalization and Standardization** had a positive but moderate effect, especially when followed by PCA.
- The combination **Standardization + PCA** consistently provided strong and balanced performance.

---

## Conclusion

PCA emerged as the most effective preprocessing method, enhancing both the compactness and separability of clusters.  
K-Means clustering, when paired with PCA or Standardization + PCA, showed the most balanced performance across all metrics.  
Mean Shift clustering also demonstrated competitive results, particularly when PCA was applied.  
Hierarchical clustering performed well with PCA but was more sensitive to other preprocessing methods.

These findings support the importance of proper data preprocessing in unsupervised learning tasks, especially clustering.

