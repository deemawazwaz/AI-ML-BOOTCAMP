# Week 5 — Day 1: Unsupervised Learning & K-Means

## Overview

Day 1 focuses on unsupervised learning and K-Means clustering.
The goal is to discover hidden patterns and groups in data without
using a target variable.

## Learning Objectives

- Understand supervised vs. unsupervised learning.
- Understand how clustering works.
- Apply K-Means clustering.
- Choose the number of clusters using the Elbow Method.
- Evaluate clusters using the Silhouette Score.
- Visualize and interpret the resulting clusters.

## Dataset

For the practical exercise, the Titanic dataset was used.

The following numerical features were used for clustering:

- Pclass
- Age
- SibSp
- Parch
- Fare

The `Survived` variable was not used during clustering because K-Means
is an unsupervised learning algorithm.

## Data Preprocessing

The following preprocessing steps were performed:

1. Selected relevant numerical features.
2. Checked for missing values.
3. Filled missing values using the median.
4. Standardized the features using `StandardScaler`.

Feature scaling is important because K-Means relies on distance
calculations.

## K-Means Clustering

K-Means groups observations into a predefined number of clusters.

The algorithm repeatedly assigns observations to their nearest
centroid and updates the centroid based on the assigned observations
until the clusters stabilize.

## Choosing the Number of Clusters

### Elbow Method

K-Means was evaluated for values of `k` from 1 to 10 using inertia.
The Elbow Method was used to identify a suitable range of cluster
values.

### Silhouette Score

The Silhouette Score was calculated for three candidate values:

| k | Silhouette Score |
|---|------------------:|
| 2 | 0.407 |
| 3 | 0.438 |
| 4 | 0.413 |

The highest score was obtained with:

**k = 3**

Therefore, the final K-Means model used three clusters.

## Cluster Interpretation

### Cluster 0

- Average Pclass: 2.72
- Average Age: 24.54
- Average SibSp: 0.29
- Average Parch: 0.23
- Average Fare: 13.57

This cluster mainly represents younger passengers with lower-fare
tickets and relatively low family-related values.

### Cluster 1

- Average Pclass: 1.11
- Average Age: 42.10
- Average SibSp: 0.47
- Average Parch: 0.43
- Average Fare: 86.96

This cluster represents older passengers who generally traveled in
higher-class and higher-fare tickets.

### Cluster 2

- Average Pclass: 3.00
- Average Age: 20.32
- Average SibSp: 3.50
- Average Parch: 3.29
- Average Fare: 41.47

This cluster represents younger passengers with substantially higher
family-related values, suggesting larger family groups.

## Visualization

A 2D scatter plot was created to visualize the clusters using
standardized `Pclass` and `Age`.

The visualization also includes the K-Means centroids.

## Key Takeaways

- Unsupervised learning can discover patterns without labeled targets.
- K-Means is a distance-based clustering algorithm.
- Feature scaling is important before applying K-Means.
- The Elbow Method helps evaluate suitable values of `k`.
- The Silhouette Score provides a quantitative measure of cluster quality.
- `k = 3` achieved the highest Silhouette Score among the tested values.
- The resulting clusters showed different passenger characteristics
  based on class, age, family-related variables, and fare.

## Notebook

The complete implementation is available in:

`Day_1_KMeans_Clustering.ipynb`

## Tools

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook