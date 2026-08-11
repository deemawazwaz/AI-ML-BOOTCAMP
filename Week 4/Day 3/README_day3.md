# Day 3 — Bias-Variance & Diagnosing Model Fit

## Overview

Today focused on understanding how machine learning models can fail because
they are either too simple or too complex.

Instead of evaluating models only by their final score, the goal was to
diagnose their behavior using training and validation performance.

## Topics Covered

- Underfitting and high bias
- Overfitting and high variance
- Bias-variance trade-off
- Training vs. validation performance
- Model complexity and decision-tree depth
- Regularization
- Ridge (L2)
- Lasso (L1)

## Practical Work

A Decision Tree classifier was deliberately made very deep to demonstrate
overfitting. The model achieved a training F1-score of 1.00 while its
validation F1-score was approximately 0.456, producing a large gap of
approximately 0.544.

A very shallow tree with `max_depth=1` was then tested. It achieved a
training F1-score of approximately 0.586 and a validation F1-score of
approximately 0.406, showing behavior consistent with underfitting.

Several tree depths were compared to observe how model complexity affects
training and validation performance.

## Model Complexity Results

The experiments showed that increasing tree depth generally increased
training performance, while validation performance did not improve at
the same rate.

At `max_depth=10`, the validation F1-score reached approximately 0.444,
but the training-validation gap increased to approximately 0.495.

At `max_depth=5`, the validation F1-score was approximately 0.383 with
a smaller gap of approximately 0.203, demonstrating a more balanced
level of model complexity.

## Regularization

Ridge and Lasso regression were also explored to understand how
regularization controls model complexity.

### Ridge

- RMSE: 0.746
- R²: 0.576

### Lasso

- RMSE: 0.783
- R²: 0.532

Ridge performed better in this experiment based on both RMSE and R².
However, this result is dataset-dependent and does not imply that Ridge
is always superior to Lasso.

## Key Takeaway

The main lesson of this day was that model performance must be evaluated
in terms of both accuracy and generalization.

A model with an extremely high training score may simply be memorizing
the training data, while a model with low scores on both training and
validation data may be too simple.

The goal is to find an appropriate level of complexity that captures
useful patterns while maintaining good performance on unseen data.