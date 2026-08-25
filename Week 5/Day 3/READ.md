# Day 3 — Dimensionality Reduction with PCA

## Overview

Day 3 focused on **Dimensionality Reduction** using **Principal Component Analysis (PCA)**.

The goal was to understand why high-dimensional data can be difficult to work with, how PCA transforms original features into principal components, and how explained variance can be used to evaluate the information retained after dimensionality reduction.

The Titanic dataset was used for the practical implementation.

## Learning Objectives

* Explain the curse of dimensionality and why dimensionality reduction is useful.
* Apply PCA to reduce the dimensions of a dataset.
* Understand principal components and variance.
* Interpret explained variance ratio and cumulative explained variance.
* Determine how many components are needed to retain approximately 95% of the variance.
* Reduce the dataset to two components for visualization.
* Understand the trade-off between dimensionality reduction and information loss.

## Dataset

The numerical features used for PCA were:

* `Pclass`
* `Age`
* `SibSp`
* `Parch`
* `Fare`

Missing values were handled before applying PCA, and all features were standardized using `StandardScaler`.

## Methodology

### 1. Data Preparation

The selected numerical features were extracted from the Titanic dataset.

Missing values were replaced using the median of each feature.

### 2. Feature Scaling

`StandardScaler` was applied before PCA because PCA is variance-based and features with larger numerical ranges could otherwise have a greater influence on the result.

### 3. PCA and Explained Variance

PCA was first fitted using all available components to examine how much variance each component explained.

The explained variance ratios were:

| Component | Explained Variance |
| --------- | -----------------: |
| PC1       |             39.08% |
| PC2       |             27.59% |
| PC3       |             13.94% |
| PC4       |             12.15% |
| PC5       |              7.24% |

The first four components retained approximately **92.76%** of the total variance.

To retain approximately **95%** of the variance, all five components were required.

### 4. Two-Component PCA

For visualization, PCA was applied with two components.

The first two components retained:

**66.67% of the total variance**

This reduced the original five-dimensional feature space to two dimensions.

## Visualization

A 2D scatter plot was created using:

* Principal Component 1 on the x-axis
* Principal Component 2 on the y-axis

The visualization provides a simpler representation of the dataset while retaining approximately 66.67% of its variance.

## Results and Interpretation

The first principal component explained approximately **39.08%** of the variance, while the second explained approximately **27.59%**.

Together, they captured approximately **66.67%** of the total variance.

This demonstrates that PCA can reduce the dimensionality of the dataset while preserving a substantial amount of its variation.

However, approximately **33.33%** of the variance was not represented by the first two components. Therefore, the two-component representation is mainly useful for visualization rather than preserving all of the information in the original dataset.

Another trade-off is interpretability. Principal components are combinations of the original features, so they are less directly interpretable than the original variables.

## Key Takeaways

* PCA is a dimensionality reduction technique based on variance.
* Features should be scaled before applying PCA.
* Explained variance helps determine how much information is retained.
* The first two components retained 66.67% of the variance in this dataset.
* Approximately 95% variance required all five components.
* PCA can make high-dimensional data easier to visualize, but reducing dimensions can result in information loss and lower interpretability.

## Tools Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* StandardScaler
* PCA

## Files

* `Day_3_PCA_Dimensionality_Reduction.ipynb`
* `README.md`
