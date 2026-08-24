# Day 2: DBSCAN & Hierarchical Clustering

## Overview

This project is part of Week 5 of the AI & Machine Learning Bootcamp.

The focus of Day 2 is exploring clustering methods beyond K-Means.
The notebook applies DBSCAN and Hierarchical Clustering to the Titanic
dataset and compares their results with the K-Means clustering results
from Day 1.

---

## Learning Objectives

By completing this notebook, I was able to:

- Understand the limitations of K-Means clustering.
- Apply DBSCAN to identify clusters and noise points.
- Understand the role of `eps` and `min_samples` in DBSCAN.
- Build and interpret a hierarchical clustering dendrogram.
- Select a cut height to determine the number of clusters.
- Compare K-Means, DBSCAN, and Hierarchical Clustering.

---

## Dataset

The Titanic dataset was used for this analysis.

The following numerical features were selected:

- `Pclass`
- `Age`
- `SibSp`
- `Parch`
- `Fare`

Missing values were handled using the median of each feature.

---

## Data Preprocessing

Before applying the clustering algorithms:

1. Numerical features were selected.
2. Missing values were filled using the median.
3. Features were scaled using `StandardScaler`.

Scaling is important because clustering algorithms such as DBSCAN and
Hierarchical Clustering rely on distances between observations.

---

# DBSCAN Clustering

## What is DBSCAN?

DBSCAN is a density-based clustering algorithm.

Unlike K-Means, DBSCAN:

- Does not require specifying the number of clusters in advance.
- Can identify irregularly shaped clusters.
- Can detect noise and outliers.
- Labels noise points with `-1`.

The main parameters used were:

- `eps = 0.5`
- `min_samples = 5`

## DBSCAN Results

The model identified:

- **10 clusters**
- **126 noise points**

The noise points represent observations that do not belong to sufficiently
dense regions of the dataset.

---

# Hierarchical Clustering

Hierarchical clustering creates a hierarchy of clusters by progressively
merging similar observations.

The clustering process was visualized using a dendrogram.

## Dendrogram

The dendrogram shows how observations and groups are progressively merged
based on their distance.

A cut height of:

```text
20 was selected based on the structure of the dendrogram.

Hierarchical Clustering Results

Using a cut height of 20, the algorithm produced:

4 clusters

The visualization displays the resulting cluster assignments using
Pclass and Age.

Comparison of Clustering Methods
Method	Result	Strength	Limitation
K-Means	3 clusters	Simple and efficient	Requires choosing the number of clusters
DBSCAN	10 clusters and 126 noise points	Detects noise and does not require predefined clusters	Sensitive to parameter selection
Hierarchical Clustering	4 clusters	Shows hierarchical relationships using a dendrogram	Can be slower with large datasets
Conclusion

The three clustering methods produced different results because each
algorithm uses a different approach to identify patterns in the data.

K-Means is useful when the approximate number of clusters is known and
the data contains relatively compact groups.

DBSCAN is useful when detecting noise and outliers is important. In this
analysis, it identified 10 clusters and 126 noise points without requiring
the number of clusters to be specified in advance.

Hierarchical Clustering provided a different perspective by showing the
nested structure of the data through a dendrogram. Using a cut height of
20 resulted in 4 clusters.

Overall, the choice of clustering method depends on the structure of the
data and the goal of the analysis.

Tools Used
Python
Pandas
NumPy
Scikit-learn
SciPy
Matplotlib
Jupyter Notebook