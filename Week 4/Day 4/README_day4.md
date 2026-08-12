# Day 4 — Feature Engineering & Hyperparameter Tuning

## Overview

Today focused on improving a machine learning workflow through feature engineering and systematic hyperparameter tuning.

The Titanic dataset was used with a Random Forest classifier.

The main question was:

> Can better features and better model settings improve model performance?

## Feature Engineering

Two new features were created:

* **FamilySize**: combines `SibSp` and `Parch`, including the passenger.
* **IsAlone**: indicates whether the passenger was travelling alone.

```python
df["FamilySize"] = df["SibSp"] + df["Parch"] + 1
df["IsAlone"] = (df["FamilySize"] == 1).astype(int)
```

These features were created to provide the model with more meaningful information about family relationships.

## Data Split

The dataset was divided into:

* Training: 250 samples
* Validation: 84 samples
* Test: 84 samples

A fixed `random_state=42` was used for reproducibility.

The test set was kept separate until the final evaluation.

## Baseline Model

A Random Forest was trained before tuning.

**Baseline Validation F1: 0.473**

This score was used as the reference point for evaluating the effect of hyperparameter tuning.

## Hyperparameter Tuning

`GridSearchCV` with 5-fold cross-validation was used to systematically search for better Random Forest settings.

Parameters tested:

* `n_estimators`: 50, 100, 200
* `max_depth`: 3, 5, 10, None
* `min_samples_split`: 2, 5, 10

This resulted in 180 model fits.

### Best Parameters

```text
n_estimators = 100
max_depth = 10
min_samples_split = 10
```

**Best Cross-Validation F1: 0.463**

**Tuned Validation F1: 0.453**

The tuned model did not outperform the baseline validation score of 0.473. This demonstrates that hyperparameter tuning does not guarantee better performance.

## Feature Importance

| Feature     | Importance |
| ----------- | ---------: |
| Fare        |     0.3065 |
| PassengerId |     0.2353 |
| Age         |     0.2140 |
| FamilySize  |     0.0639 |
| Pclass      |     0.0512 |
| SibSp       |     0.0449 |
| Parch       |     0.0423 |
| IsAlone     |     0.0418 |

Among the engineered features, `FamilySize` was more important than `IsAlone`.

`PassengerId` also showed relatively high importance. Since it is an identifier rather than a meaningful passenger characteristic, this result should be interpreted cautiously.

Feature importance indicates contribution to model decisions, not causation.

## Final Test Evaluation

After completing feature engineering and hyperparameter tuning, the final model was evaluated on the held-out test set.

**Final Test F1: 0.538**

The test set was not used during model selection or hyperparameter tuning and was evaluated only at the end.

## Key Takeaways

* Feature engineering can provide additional information to a model.
* Creating new features does not automatically improve performance.
* Hyperparameters are settings chosen before training.
* `GridSearchCV` provides a systematic way to tune hyperparameters using cross-validation.
* The tuned model did not outperform the baseline on the validation set.
* The test set should remain untouched until final evaluation.
* Feature importance should be interpreted carefully and does not imply causation.

The main lesson is that machine learning improvement should be based on evidence. Every feature and model decision should be tested to determine whether it actually improves generalization.
