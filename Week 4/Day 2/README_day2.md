# Day 2 — Cross-Validation

## Overview

This day focused on cross-validation as a more reliable way to estimate
machine learning model performance than relying on a single validation split.

## Topics Covered

- Why a single validation split can be misleading
- k-Fold Cross-Validation
- 5-Fold Cross-Validation
- `cross_val_score`
- Mean F1-score
- Standard deviation
- Stratified K-Fold Cross-Validation
- Preserving class distribution during classification
- Comparing standard and stratified cross-validation

## Practical Work

A Decision Tree classifier was evaluated using:

- A single validation split
- Standard 5-Fold Cross-Validation
- Stratified 5-Fold Cross-Validation

The results were visualized and interpreted to understand both model
performance and stability across different folds.

## Key Results

### Single Validation Split

F1-score: **0.383**

### Standard 5-Fold Cross-Validation

Mean F1-score: **0.361**

Standard deviation: **0.072**

### Stratified 5-Fold Cross-Validation

Mean F1-score: **0.350**

Standard deviation: **0.136**

## Key Takeaway

Cross-validation provides a more reliable estimate of model performance
by evaluating the model across multiple subsets of the training data.

For classification problems, Stratified K-Fold is particularly useful
because it preserves the class distribution across the folds.

The results also demonstrate why both the mean and standard deviation
should be considered when evaluating model performance.