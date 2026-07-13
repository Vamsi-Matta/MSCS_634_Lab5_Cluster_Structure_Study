# MSCS_634_Lab5_Cluster_Structure_Study

## Clustering Techniques Using DBSCAN and Hierarchical Clustering

### Student Information
- **Name:** Vamshi Matta
- **Course:** MSCS 634 – Advanced Big Data and Data Mining
- **Lab Assignment:** Lab 5
- **Dataset:** Wine Dataset (Scikit-learn)

---

# Overview

The purpose of this lab was to explore and compare two unsupervised machine learning techniques:

1. Agglomerative Hierarchical Clustering
2. Density-Based Spatial Clustering of Applications with Noise (DBSCAN)

Both algorithms were implemented using the Wine dataset from the Scikit-learn library. The lab focused on understanding how different clustering techniques form groups, how parameter selection affects clustering outcomes, and how clustering quality can be evaluated using multiple metrics and visualizations.

---

# Dataset Description

The Wine dataset contains chemical analysis measurements obtained from three different wine cultivars.

### Dataset Characteristics
- Number of observations: 178
- Number of features: 13
- Number of classes: 3
- Missing values: None
- Duplicate records: None

Since clustering algorithms are distance-based, all numerical features were standardized using Z-score normalization before model development.

---

# Tasks Performed

The following activities were completed during this lab:

### Data Preparation and Exploration
- Loaded the Wine dataset.
- Explored the dataset using:
  - `head()`
  - `info()`
  - `describe()`
- Checked for missing values and duplicate records.
- Standardized all numerical features.
- Applied Principal Component Analysis (PCA) for visualization.

### DBSCAN Clustering
- Implemented DBSCAN clustering.
- Tested multiple values of:
  - `eps`
  - `min_samples`
- Evaluated:
  - Number of clusters
  - Number of noise points
  - Silhouette Score
  - Homogeneity Score
  - Completeness Score
- Visualized clusters and noise observations.

### Hierarchical Clustering
- Applied Agglomerative Hierarchical Clustering.
- Tested multiple values of `n_clusters`.
- Calculated:
  - Silhouette Score
  - Homogeneity Score
  - Completeness Score
- Generated cluster visualizations.
- Constructed and interpreted a dendrogram.

### Comparison and Analysis
- Compared both algorithms using:
  - Silhouette Score
  - Homogeneity Score
  - Completeness Score
  - Noise handling capability
- Created comparison tables and charts.

---

# Key Insights

- Standardization significantly improved clustering performance by placing all features on comparable scales.
- DBSCAN successfully identified dense regions and isolated observations as noise.
- The values of `eps` and `min_samples` strongly influenced DBSCAN results.
- Hierarchical Clustering provided an interpretable representation of cluster relationships through the dendrogram.
- Different clustering algorithms produced different group structures because they use different definitions of similarity.
- Multiple evaluation metrics were necessary because a single metric does not fully describe clustering quality.

---

# Challenges Faced

One of the main challenges was selecting appropriate DBSCAN parameters. Small changes in `eps` or `min_samples` sometimes resulted in significantly different cluster formations and noise levels.

Another challenge was determining the most suitable number of hierarchical clusters. Multiple cluster counts had to be evaluated before selecting the final model.

---

# Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- SciPy

---

# Conclusion

This lab provided practical experience with two important unsupervised learning techniques. Hierarchical Clustering offered strong interpretability through dendrogram analysis, while DBSCAN demonstrated the advantages of density-based clustering and noise detection.

The results showed that selecting an appropriate clustering algorithm depends on the characteristics of the dataset, the presence of noise, and the objectives of the analysis.