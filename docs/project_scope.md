# Project Scope

## Project Title

Biomedical Machine Learning for Tuberculosis Biomarker Discovery Using Human Transcriptomic Data

##Background

Tuberculosis (TB) remains one of the leading infectious causes of mortality worldwide. Although transcriptomic profiling has identified numerous genes associated with disease progression, 
translating these findings into robust and interpretable predictive biomarkers remains challenging. 

Machine learning offers an opportunity to identify biologically meaningful gene signatures while improving diagnostic classification performance.

## Project Objectives

The primary objective of this project is to develop interpretable machine learning models capable of distinguishing active tuberculosis from healthy controls using publicly available human transcriptomic datasets.

Specific objectives include:

- Develop reproducible preprocessing workflows for transcriptomic data.
- Identify candidate biomarkers using multi-model feature selection.
- Compare machine learning algorithms for disease classification.
- Evaluate model stability and generalization.
- Interpret model predictions using explainable AI methods.
- Assess biological relevance of identified biomarkers.
- Validate findings using independent external datasets.

##Research Questions
1. Which transcriptomic features best distinguish active TB from healthy controls?
2. Can reduced biomarker panels achieve performance comparable to larger feature sets?
3. Which machine learning algorithms provide the best balance between predictive performance and interpretability?
4. Are identified biomarkers reproducible in independent datasets?

## Key Components

- Data preprocessing and quality control
- Feature selection and biomarker discovery
- Multi-model machine learning evaluation
- Explainable AI using SHAP
- Biological interpretation of identified genes
- External dataset validation

## Datasets

##Primary Dataset:
GSE19491

Human whole-blood transcriptomic dataset
Active TB, latent TB, and healthy controls
Platform: Illumina HumanHT-12 v3.0

##External Validation Dataset:
GSE25534

Independent human transcriptomic dataset
Used for external validation of discovered biomarkers

##Methodology

##Data Processing
- Quality control
- Probe annotation and gene mapping
- Gene-level feature aggregation
- Missing value handling
- Feature standardization

##Machine Learning Models
- Logistic Regression
- Random Forest
- Support Vector Machine
- XGBoost

##Feature Selection
- Model-specific importance ranking
- Cross-model consensus selection
- Tiered biomarker classification

##Explainability
- SHAP analysis
- Feature contribution analysis
- Biological interpretation

##Validation
- Stratified cross-validation
- ROC analysis
- External dataset validation

##Expected Deliverables
- Reproducible analysis pipeline
- Machine learning benchmark comparison
- Interpretable biomarker panel
- Visualization suite
- Technical report
- Public GitHub portfolio repository

## Technologies
- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- SHAP
- Matplotlib
- Jupyter Notebook

## Current Status

Active development.
