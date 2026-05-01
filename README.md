# COMPAS Analysis (Python Implementation) (Assignment 1)

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

# Disparate Impact Audit (Assignment 3)

This project analyzes fairness in a COMPAS-based prediction model using the cleaned dataset and model from previous assignments.

## What is included
- AIR, ME, and SMD calculations for race and sex
- Intersectional analysis (race × sex)
- FPR and FNR comparison across racial groups
- Two-proportion z-tests for statistical significance
- A grouped bar chart showing FPR and FNR by race
- A short compliance memo summarizing findings

## Key idea
The goal of this assignment is to check whether the model produces different outcomes for different demographic groups.  
We focus on both selection-based metrics (AIR, ME) and error-based metrics (FPR, FNR).

## Files
- `Assignment3.ipynb`: main notebook with all analysis

## Notes
The analysis is based on observational data and results may reflect underlying data bias.  
All results are for educational purposes.

# COMPAS Model Audit（Assignment4)

This project evaluates predictive models using the COMPAS dataset.

The analysis includes:
- Generalization performance
- Distribution shift
- Spurious correlation testing
- Robustness analysis
- Fairness evaluation across subgroups

The goal is to move beyond accuracy and assess model reliability and accountability.

# COMPAS ML Security Audit(Assignment5)

This project analyzes robustness, fairness, and privacy risks using the COMPAS dataset.

## Contents
- PGD Evasion Attack
- Poisoning with Fairness Monitoring
- Membership Inference Attack

## Key Findings
- AUC may remain stable while fairness degrades
- AIR can reveal hidden subgroup risks
- MI risk is low (AUC ≈ 0.5)

## Author
Jinying Wu
