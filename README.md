# Explainable and Adaptive Machine Learning for Fraud Risk Detection

Code, experimental results, and reproducibility materials for the research paper:

**“Explainable and Adaptive Machine Learning for Fraud Risk Detection in Bangladesh’s Digital Banking Ecosystem”**

**Author:** Md Najmus Swaqeeb  
**Conference:** 11th Annual Banking Conference 2026, Bangladesh Institute of Bank Management (BIBM), Dhaka, Bangladesh  
**Presented:** 28 October 2026  
**Preprint:** [arXiv:2610.39556](https://arxiv.org/abs/2610.39556)

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
- Precision: 0.7330
- Recall: 0.4236
- True positives: 527
- False positives: 192

Platt calibration reduced the test Brier score from **0.114086 to 0.024514**, an improvement of approximately **78.5%**.

The adaptive top-1% policy reduced false positives from **192 to 117**, while recall decreased from **0.4236 to 0.2122**. This demonstrates an operational trade-off between reducing investigation workload and maintaining fraud recall.

## Dataset

The experiments use the publicly available **PaySim synthetic mobile-money fraud dataset**.

The dataset itself is **not included** in this repository.

Users should obtain PaySim separately from its authorized public source and place the dataset in the appropriate local data directory before running the experiments.

## Reproducibility

The cleaned public reproducibility notebook is available at:

`notebooks/BIBM_Fraud_Detection_Reproducibility.ipynb`

Required Python packages are listed in:

`requirements.txt`

Experiment settings and configuration information are available in:

`config/reproducibility_config.json`

The repository also contains the final result tables and figures used to document the experimental findings.

## Repository Contents

- `notebooks/` — cleaned reproducibility notebook
- `results/` — experimental outputs and result tables
- `figures/` — final visualizations
- `config/` — experiment configuration
- `src/` — reusable Python code, where applicable
- `requirements.txt` — required Python packages

## Important Limitations

The results should not be interpreted as direct estimates of fraud prevalence or deployed-model performance in Bangladesh.

Bangladesh provides the application context of the research, while PaySim provides the synthetic experimental benchmark.

The synthetic data also exhibit temporal patterns and changes in fraud frequency across periods. Consequently, relationships learned from time-related features in PaySim may not transfer directly to real banking environments.

Validation using appropriately protected real-world transaction data from Bangladeshi financial institutions across multiple time periods is therefore an important direction for future research.

## Conference

This research was presented at the **11th Annual Banking Conference 2026**, organized by the **Bangladesh Institute of Bank Management (BIBM)**, Dhaka, Bangladesh, on **28 October 2026**.

The conference discussion highlighted the practical relevance of balancing fraud detection with false-positive control and investigation workload, while also emphasizing the importance of future validation using real-world banking data.

## Preprint

The paper is publicly available on arXiv:

**Md Najmus Swaqeeb. “Explainable and Adaptive Machine Learning for Fraud Risk Detection in Bangladesh’s Digital Banking Ecosystem.”**

**arXiv:2610.39556 [cs.LG]**

https://arxiv.org/abs/2610.39556

## Citation

If you use this work, please cite the arXiv preprint:

```bibtex
@article{swaqeeb2026fraud,
  title={Explainable and Adaptive Machine Learning for Fraud Risk Detection in Bangladesh's Digital Banking Ecosystem},
  author={Swaqeeb, Md Najmus},
  journal={arXiv preprint arXiv:2610.39556},
  year={2026}
}
```

## Author

**Md Najmus Swaqeeb**

ORCID: https://orcid.org/0009-0001-0355-8064
