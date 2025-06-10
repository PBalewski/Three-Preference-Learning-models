# Comparative Analysis of 3 Preference Learning models with Interpretability

**Authors:** PBalewski, vasia-korz
**Date:** may 2025  

## Introduction

This project focuses on the **(binary) sorting problem**, where we compare models that classify alternatives into ordered categories based on multiple monotonic criteria. The aim is to assess the performance, interpretability, and behavior of different models trained on the same dataset.

The following goals were addressed:

- Implement and compare various sorting models
- Evaluate model performance (Accuracy, F1 score, AUC)
- Explain individual predictions and model decisions
- Analyze user preferences inferred from model parameters
- Assess criteria influence and presence of thresholds or dependencies

---

## Dataset

**Dataset Used:** Computer Hardware  
**Source:** https://archive.ics.uci.edu/dataset/29/computer+hardware

**Dataset Overview:**
- Number of alternatives: 209
- Number of classes: 4 - changed to 2
- Number of criteria: 6

**Criteria**: 
1. MYCT: machine cycle time in nanoseconds
2. MMIN: minimum main memory in kilobytes
3. MMAX: maximum main memory in kilobytes
4. CACH: cache memory in kilobytes
5. CHMIN: minimum channels in units
6. CHMAX: maximum channels in units


## Models Trained

Three models were developed and evaluated as part of the analysis:

1. **XGBoost**  
   A Decision Tree-based, interpretable baseline model.

2. **ANN-UTADIS**  
   A neural-based MCDA approach designed to preserve interpretability.

3. **Feedforward Neural Network**  
   A deeper model using multiple hidden layers and nonlinear activations.

All models were trained on the same training/test split to ensure fair comparison.

---

## Evaluation Metrics

Each model was assessed using:

- **Accuracy**
- **F1 Score**
- **AUC (Area Under Curve)**

Additional model-specific metrics, confusion matrices, and ROC curves are available in the report folder.

---

## Experiments and Analysis

### Decision Explanations for 3 Alternatives

Three test examples were analyzed to explore:

- What *minimal change* in a single criterion value would change the classification
- Theoretical calculation based on model parameters
- Validation using space sampling

### Interpretation of the Models

Using global analysis tools, we investigated:

- Influence and ranking of the criteria
- Detection of preference thresholds and indifference regions
- Identification of user preferences
- Monotonicity and interactions between criteria

Techniques applied:

- **Partial Dependence Plots (PDP)**
- **Permutation Feature Importance (PFI)**
- **Global Surrogate Models**

---