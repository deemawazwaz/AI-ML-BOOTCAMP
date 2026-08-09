# Week 4 - Day 1: Train / Validation / Test Splits

## Overview

Today we moved beyond the simple train/test workflow used in Week 3 and introduced a three-way split: training, validation, and test.

The main question was:

> How can we tune a model without accidentally using the test set to make our decisions?

## What We Did

- Loaded the Titanic dataset.
- Separated features (`X`) from the target (`y`).
- Created a reproducible 60/20/20 train/validation/test split.
- Trained Decision Tree models with different `max_depth` values.
- Used the validation set to select the best hyperparameter.
- Evaluated the selected model on the test set only after the model choice was finalized.
- Visualized the relationship between tree depth and validation accuracy.

## Results

The best validation performance was achieved with:

- `max_depth = 2`
- Validation Accuracy = **67.86%**
- Final Test Accuracy = **60.71%**

## Key Insight

The validation set is used for model development and tuning, while the test set must remain untouched until the final evaluation.

Using the test set repeatedly during development can lead to overly optimistic results because our decisions become influenced by information from the test data.

## Why This Matters for Machine Learning

A model is not evaluated only by how well it performs on data we have already used to make decisions.

The real goal is to estimate how well it will perform on unseen data.

Keeping the test set isolated gives us a more honest estimate of generalization performance.

## Tools

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Jupyter Notebook
- Git & GitHub