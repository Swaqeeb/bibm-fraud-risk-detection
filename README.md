# Explainable and Adaptive Machine Learning for Fraud Risk Detection

Code, experimental results, and reproducibility materials for the research paper:

**“Explainable and Adaptive Machine Learning for Fraud Risk Detection in Bangladesh’s Digital Banking Ecosystem”**

**Author:** Md Najmus Swaqeeb  
**Status:** Presented at the 11th Annual Banking Conference 2026, Bangladesh Institute of Bank Management (BIBM), Dhaka, Bangladesh, 28 October 2026.

**Preprint:** Submitted to arXiv; permanent arXiv identifier pending.

## Overview

This project investigates transaction-level fraud-risk detection using machine learning, probability calibration, explainable AI, and adaptive risk prioritization.

The experimental evaluation uses the PaySim synthetic mobile-money dataset. PaySim is used as a reproducible benchmark and is not a dataset of Bangladeshi banking or mobile financial service transactions.

## Models

The study evaluates:

- Logistic Regression
- Random Forest
- XGBoost
- LightGBM

The strongest fixed-threshold model was Clean XGBoost.

## Methodology

The project includes:

- Chronological train/validation/test splitting
- Leakage-conscious historical feature engineering
- Validation-based threshold selection
- Probability calibration using Platt scaling
- SHAP-based global and local explainability
- Adaptive top-1% risk prioritization within 24-step windows

## Main Results

Clean XGBoost achieved:

- F1-score: 0.5369
- PR-AUC: 0.5658
- ROC-AUC: 0.9068

Platt calibration reduced the test Brier score from 0.114086 to 0.024514.

The adaptive top-1% policy reduced false positives from 192 to 117, while recall decreased from 0.4236 to 0.2122.

## Dataset

The experiments use the publicly available **PaySim** synthetic mobile-money fraud dataset.

The dataset itself is not included in this repository.

## Repository Contents

- `results/` — experimental outputs and tables
- `figures/` — final visualizations
- `notebooks/` — reproducibility notebooks
- `src/` — reusable Python code
- `config/` — experiment configuration

## Important Note

The results should not be interpreted as direct estimates of fraud prevalence or deployed-model performance in Bangladesh. Bangladesh is the application context of the research, while PaySim provides the synthetic experimental benchmark.

## Conference

Accepted for presentation at the **11th Annual Banking Conference 2026**, organized by the **Bangladesh Institute of Bank Management (BIBM)**.
