# Day 5 — Phase 3 Project Planning: CardioML

## Overview

Day 5 marks the transition into Phase 3 of the AI/ML training program.

The selected project is **CardioML — Cardiac Patient Monitoring System**. The project will be developed and improved across the upcoming Phase 3 sprints.

---

## Project

**CardioML — Cardiac Patient Monitoring System**

CardioML is a machine-learning project focused on analyzing cardiac patient data and building classification models for heart disease prediction.

The project uses the **Heart Disease UCI dataset**.

The dataset includes patient health and clinical features such as:

- Age
- Gender
- Height
- Weight
- Systolic blood pressure
- Diastolic blood pressure
- Cholesterol
- Glucose
- Smoking
- Alcohol consumption
- Physical activity

The target variable is:

- `cardio` — indicates the presence of cardiovascular disease.

---

## Problem Statement

CardioML aims to develop a reliable machine-learning workflow for analyzing cardiac patient data and predicting the presence of cardiovascular disease.

The project will be improved through systematic data analysis, preprocessing, model development, evaluation, interpretation, and deployment preparation.

---

# Definition of Done

The final CardioML project should include:

- A clean and documented Jupyter Notebook covering the complete ML workflow.
- Proper data preprocessing and feature engineering.
- A trained and evaluated machine-learning model.
- Reported performance metrics.
- Model comparison and validation.
- Model interpretability and meaningful insights.
- Saved model artifacts.
- A working deployment.
- A clean GitHub repository.
- A professional README.
- `requirements.txt`.
- Technical documentation and final project presentation.

---

# Sprint 1 Plan

## Sprint 1 Goal

> Establish a clear and reproducible machine-learning foundation for CardioML and prepare the project for further model improvement in the upcoming sprints.

---

## Sprint 1 Focus

- Review the existing project structure.
- Validate the dataset and preprocessing workflow.
- Review the current baseline models.
- Identify areas for model improvement.
- Organize the project structure.
- Document the current state of the project.
- Define the next development steps.

---

## Sprint 1 Backlog

| Task | Description | Priority |
|---|---|---|
| Dataset Review | Review dataset structure, features, target, and data quality | High |
| EDA Review | Validate exploratory analysis and identify additional insights | High |
| Preprocessing Review | Verify cleaning, missing values, encoding, and scaling | High |
| Baseline Review | Review baseline model performance | High |
| Model Improvement | Identify possible improvements for the next sprint | Medium |
| Documentation | Organize project documentation and GitHub structure | Medium |

---

# Acceptance Criteria

Each task should satisfy the following criteria:

- The notebook runs without errors.
- Results are clearly documented using Markdown.
- Code is committed to the appropriate Git branch.
- Commit messages clearly describe the implemented changes.
- A Pull Request is created before merging when applicable.
- Model results and metrics are recorded.
- Changes are reproducible.
- The completed task contributes directly to the Sprint Goal.

---

# Phase 3 Roadmap

## Week 6 — Model Development

Focus on improving the current machine-learning solution.

### Planned Work

- Feature engineering
- Model comparison
- Hyperparameter tuning
- Cross-validation
- Performance improvement

### Expected Outcome

An improved and validated classification model.

---

## Week 7 — Advanced Analysis

Focus on understanding model behavior and extracting deeper insights.

### Planned Work

- Feature importance
- Model interpretability
- Error analysis
- Additional evaluation
- Insight extraction

### Expected Outcome

A better understanding of model behavior, important features, and errors.

---

## Week 8 — Productization

Focus on preparing CardioML for real-world usage.

### Planned Work

- Finalize the ML pipeline.
- Save the trained model.
- Build the application interface.
- Connect the model to the application.
- Prepare deployment requirements.

### Expected Outcome

A working application that can use the trained model to generate predictions.

---

## Week 9 — Final Delivery

Focus on finalizing and presenting the complete project.

### Planned Work

- Final testing
- Deployment verification
- README improvement
- Technical write-up
- GitHub cleanup
- Final presentation

### Expected Outcome

A complete, documented, reproducible, and deployed CardioML project.

---

# GitHub Workflow

The project will follow a feature-branch workflow.

```text
main
  │
  ├── feature/sprint-1
  │
  ├── feature/model-improvement
  │
  ├── feature/advanced-analysis
  │
  └── feature/deployment

Each feature should be developed separately, committed with a descriptive message, reviewed through a Pull Request when required, and then merged into the main branch.

Dataset
   ↓
Data Understanding
   ↓
EDA
   ↓
Data Cleaning & Preprocessing
   ↓
Baseline Model
   ↓
Model Evaluation
   ↓
Model Improvement
   ↓
Model Interpretation
   ↓
Final Model
   ↓
Deployment
   ↓
Final Documentation

Project Risks & Considerations

The following risks should be monitored throughout Phase 3:

Class imbalance.
Overfitting.
Data leakage.
Poor generalization.
Choosing a model based only on accuracy.
Inconsistent preprocessing between training and deployment.
Deployment and dependency issues.
Current Status
Week 5
 CardioML project selected.
 Project planning documented.
 Sprint 1 goal defined.
 Sprint 1 backlog defined.
 Acceptance criteria defined.
 Mentor sign-off.
Phase 3
 Dataset review
 EDA review
 Preprocessing review
 Baseline model review
 Model improvement
 Advanced analysis
 Model interpretation
 Deployment
 Final documentation
Tools
Python
Pandas
NumPy
Scikit-learn
Matplotlib
Jupyter Notebook
Git
GitHub
Final Project Outcome

At the end of Phase 3, CardioML should provide:

A trained and evaluated machine-learning classification model.
A documented end-to-end ML workflow.
Model comparison and validation.
Model interpretation and meaningful insights.
Saved model artifacts.
A working deployed application.
A clean GitHub repository.
Complete project documentation.


Note: 
This README will serve as the main roadmap for CardioML throughout Phase 3.

The plan can be updated during future sprints based on project results, mentor feedback, and technical requirements.
