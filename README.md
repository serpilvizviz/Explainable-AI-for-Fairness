# Explainable AI for Fairness: SHAP, LIME, and GSHAP Evaluation

This repository accompanies the research paper titled:  
**"XAI for Fairness of Machine Learning Models: An Evaluation of SHAP, LIME, and GSHAP"**

## Overview

This project evaluates how well modern Explainable AI (XAI) methods such as SHAP, LIME, and GSHAP can provide fair, reliable, and robust explanations—particularly in high-stakes scenarios involving demographic subgroups.  

We focus on:
- Subgroup-level explanation using GSHAP’s intergroup difference mode.
- Comparison of explanation strength between SHAP, LIME, and GSHAP.
- Adversarial fooling attacks that manipulate explanations without changing model predictions.

## Research Questions

This study addresses the following core research questions:

1. **Subgroup Fairness:** Can GSHAP provide stronger explainability than SHAP and LIME in identifying biases across demographic subgroups?
2. **Multi-Attribute Subgroups:** Can intergroup explanation techniques be extended to capture more complex subgroup structures?
3. **Adversarial Robustness:** Are these explanation methods vulnerable to manipulation without affecting prediction accuracy?
4. **Explanation Integrity:** How do explanations change when artificial, non-influential features are introduced?

## Datasets

The following publicly available datasets were used:
- **Adult Income** dataset from UCI
- **COMPAS** dataset by ProPublica

These datasets contain sensitive attributes such as race, gender, and prior criminal history, making them ideal for fairness-based XAI evaluations.

## Methods

- **SHAP** (KernelSHAP): Used for local and global feature attribution.
- **LIME**: Used for local surrogate explanations with Logistic Regression.
- **GSHAP**: A generalized form of SHAP that allows intergroup difference explanations.  
  We extended this method to analyze fairness across multidimensional subgroups.

## Adversarial Fooling

Inspired by recent work, we implemented fooling experiments that minimize group disparities in explanations while preserving model accuracy. We demonstrate how:
- SHAP and LIME can be manipulated easily,
- GSHAP also remains vulnerable despite its theoretical strengths.

