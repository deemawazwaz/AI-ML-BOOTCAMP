# Day 4 — t-SNE & Anomaly Detection

## Overview

Day 4 focused on using t-SNE for visualization of high-dimensional data and Isolation Forest for unsupervised anomaly detection.

## Objectives

- Apply t-SNE to visualize high-dimensional data in 2D.
- Understand the difference between PCA and t-SNE.
- Understand anomaly detection and why it is often unsupervised.
- Detect anomalies using Isolation Forest.
- Interpret flagged anomalous points.

## 1. t-SNE Visualization

t-SNE (t-distributed Stochastic Neighbor Embedding) is a dimensionality-reduction technique designed mainly for visualization.

Unlike PCA, which focuses on preserving global variance, t-SNE focuses on preserving local neighborhoods.

### PCA vs t-SNE

| PCA | t-SNE |
|---|---|
| Preserves global variance | Preserves local neighborhoods |
| Useful for compression and visualization | Mainly used for visualization |
| Fast | Slower on large datasets |
| Components have interpretable directions | Axes have no direct meaning |

In this dataset, t-SNE was used to visualize local groupings and reveal structure in the data.

## 2. Anomaly Detection

Anomaly detection identifies observations that differ significantly from the normal pattern of the dataset.

It is commonly unsupervised because anomalous examples are often rare and do not have predefined labels.

## 3. Isolation Forest

Isolation Forest detects anomalies by randomly partitioning the data.

Points that can be isolated quickly are more likely to be anomalies.

```python
from sklearn.ensemble import IsolationForest

iso = IsolationForest(
    contamination=0.05,
    random_state=42
)

preds = iso.fit_predict(X)

# -1 = anomaly
#  1 = normal

4. Results

The Isolation Forest model produced the following results:

Total points: 418
Normal points: 397
Anomalies: 21
Contamination: 0.05

Approximately 5% of the observations were flagged as anomalies.

5. Interpretation

The flagged points represent observations that differ from the general distribution of the dataset.

Possible reasons for being flagged include unusual combinations of feature values or observations that are relatively isolated from the majority of the data.

Conclusion

t-SNE is useful for visually exploring local structure in high-dimensional data, while PCA is more suitable when dimensionality reduction and explained variance are important.

Isolation Forest provides an unsupervised approach for identifying observations that appear unusual without requiring pre-labeled anomaly data.