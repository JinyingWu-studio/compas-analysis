# COMPAS Analysis (Python Implementation)

## Purpose
This project reproduces the ProPublica COMPAS analysis using Python. The goal is to examine potential racial bias in COMPAS risk scores.

## Methods
- Data cleaning and filtering
- Exploratory data analysis (EDA)
- Logistic regression modeling
- Confusion matrix evaluation
- Fairness analysis using FPR and FNR across racial groups

## Libraries Used
- pandas
- numpy
- matplotlib
- seaborn
- statsmodels

## How to Run
1. Open the Jupyter notebook (`Lecture_01_alignment-2.ipynb`)
2. Run all cells from top to bottom
3. The analysis will reproduce all results and figures

## Notes
The analysis follows the same conceptual workflow as the original R implementation but is fully implemented in Python.

## Explainability Extension (Assignment 2)

This extension adds explainability methods to the COMPAS analysis, including:

- **LIME** for local, interpretable explanations of individual predictions  
- **SHAP** for both global (feature importance) and local (waterfall) explanations  
- **DiCE (Counterfactual Explanations)** to show how minimal changes in features can flip predictions  

We compare explanations for a Black defendant and a White defendant with similar predicted risks to examine how model decisions differ across individuals.

These results highlight that even when predicted risks are similar, the underlying feature contributions and counterfactual changes can differ, raising potential fairness concerns.
