# Results Summary

## Overview

This section summarizes the machine learning results generated during tuberculosis biomarker discovery.

## Baseline Machine Learning Performance

| Model | Accuracy | Precision | Recall | ROC-AUC | Mean CV AUC |
|-------|---------:|----------:|-------:|--------:|------------:|
| Logistic Regression | 0.89 | 0.89 | 0.97 | 0.806 | 0.943 |
| Random Forest | 0.87 | 0.87 | 0.97 | 0.793 | 0.921 |
| SVM | NA | NA | 1.00 | 0.840 | 0.955 |
| XGBoost | NA | NA | NA | 0.923 | NA |
#### *Performance metrics from the baseline Active TB versus Healthy Control classification task. Results provide the foundation for subsequent biomarker prioritization, robustness assessment, and biological interpretation.*

### Key Findings

- All baseline models demonstrated strong discrimination between Active TB and Healthy Controls.
- Logistic Regression achieved the highest overall accuracy (0.89).
- SVM achieved the highest cross-validation performance (Mean CV AUC = 0.955).
- XGBoost achieved the highest test ROC-AUC (0.923).
- Multiple models independently identified overlapping biomarker candidates, supporting biological robustness.

## Biomarker Candidate Identification
Summary of consensus biomarker candidates identified across Logistic Regression, Random Forest, SVM, and XGBoost models. Candidate genes were grouped into Tier 1, Tier 2, and Tier 3 categories based on multi-model support.

## Biomarker Robustness Assessment
[Table 3 from manuscript]

## Biological Interpretation
[Table 2 summary]

## External Validation
Independent external validation was performed using GSE25534 to evaluate biomarker reproducibility, feature alignment, and model generalizability across datasets.

