# Workflow
## Overview

This project follows a structured machine learning workflow for tuberculosis biomarker discovery using human transcriptomic datasets.

The workflow begins with transcriptomic data acquisition and preprocessing, followed by feature selection, machine learning model development, explainability analysis, biological interpretation, and independent external validation.

## Workflow Diagram
GSE19491
    ↓
Data Cleaning
    ↓
Probe Annotation
    ↓
Gene Mapping
    ↓
Feature Selection
    ↓
Machine Learning Models
    ↓
SHAP Explainability
    ↓
Biological Interpretation
    ↓
External Validation (GSE25534)


## Step 1: Data Acquisition
#### Input Dataset
- GSE19491
- Human whole-blood transcriptomic dataset
- Active TB, Latent TB, and Healthy Controls

#### Objective

Establish the primary dataset for biomarker discovery and model development.


## Step 2: Data Cleaning
#### Activities
- Parse expression files
- Verify sample labels
- Handle missing values
- Quality-control checks

#### Output

Clean expression matrix suitable for downstream analysis.


## Step 3: Probe Annotation
#### Activities
- Import GPL6947 annotation data
- Map probe identifiers to gene symbols
- Remove probes lacking valid annotations

#### Output

Annotated probe-level dataset.


## Step 4: Gene Mapping
#### Activities
- Aggregate probes to gene-level features
- Resolve duplicate mappings
- Generate gene-level expression matrix

#### Output

Gene-level expression dataset


## Step 5: Feature Selection
#### Activities
- Logistic Regression importance analysis
- Random Forest importance analysis
- Support Vector Machine feature evaluation
- Consensus biomarker identification
- XGBoost feature importance analysis

#### Output

Tiered biomarker candidate panels.


## Step 6: Machine Learning Models
#### Models Evaluated
- Logistic Regression
- Random Forest
- Support Vector Machine
- XGBoost

#### Evaluation
- Accuracy
- Precision
- Recall
- ROC-AUC
- Cross-validation

#### Output

Model performance benchmarks.


## Step 7: SHAP Explainability
#### Activities
- SHAP value computation
- Global feature importance analysis
- Local prediction interpretation

#### Output

Interpretable model explanations.


## Step 8: Biological Interpretation
#### Activities
- Literature review
- Immune pathway assessment
- Functional interpretation of biomarkers

#### Output

Biologically informed candidate gene signatures.


## Step 9: External Validation
#### Validation Dataset
- GSE25534
#### Activities
- Feature alignment
- External performance evaluation
- Biomarker reproducibility assessment

#### Output

Independent validation of discovered biomarkers.


## Final Deliverables
- Reproducible analysis workflow
- Machine learning benchmark comparison
- Explainable biomarker panel
- External validation results
- Technical report
- Public GitHub portfolio repository

