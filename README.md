# Biomedical ML for Tuberculosis Biomarker Discovery

## Project Overview

This project applies machine learning and explainable artificial intelligence (XAI) techniques to identify transcriptional biomarkers associated with active tuberculosis (TB) in human blood gene expression datasets. The goal is to discover biologically meaningful gene signatures capable of distinguishing Active TB from Healthy Controls while maintaining model interpretability and supporting downstream biological investigation.

The study combines multiple machine learning algorithms, SHAP explainability analysis, consensus feature selection, biological interpretation, and external validation planning to create a robust biomarker discovery workflow.

---

## Scientific Motivation

Tuberculosis remains one of the leading infectious causes of death worldwide. Early and accurate diagnosis is essential for disease control, yet conventional diagnostic approaches may be limited by sensitivity, infrastructure requirements, or turnaround time.

Host transcriptomic biomarkers provide an opportunity to identify disease-associated immune signatures directly from patient gene expression profiles. However, many machine learning studies emphasize predictive performance without sufficient biological interpretation or validation.

This project addresses that gap by integrating:

* Machine learning classification
* Consensus biomarker prioritization
* SHAP explainability
* Biological interpretation
* External validation planning

to identify biomarker candidates that are both statistically robust and biologically meaningful.

---

## Objectives

The primary objectives of this project were to:

1. Develop machine learning models capable of distinguishing Active TB from Healthy Controls.
2. Identify candidate biomarkers using multiple feature selection approaches.
3. Evaluate model interpretability using SHAP explainability analysis.
4. Prioritize biologically relevant biomarker panels.
5. Assess biomarker robustness through consensus evaluation.
6. Establish an external validation workflow for independent dataset assessment.

---

## Dataset Description

### Discovery Dataset

**GSE19491**

* Platform: Illumina HumanHT-12 v3.0 Expression BeadChip
* Organism: Human
* Phenotypes:

  * Active Tuberculosis
  * Latent Tuberculosis
  * Healthy Controls

For Phase 1 analyses, the primary classification task focused on:

**Active TB vs Healthy Controls**

### External Validation Dataset

**GSE25534**

Used as an independent cohort for feature alignment, biomarker reproducibility assessment, and future model generalizability evaluation.

---

## Machine Learning Workflow

![Machine Learning Workflow](results/figures/Figure_0_ML_Workflow.png)

*Figure 0. End-to-end machine learning workflow used for tuberculosis biomarker discovery and biological interpretation.*
## Key Results

### Baseline Model Performance

| Model               | Accuracy | Precision | Recall | ROC-AUC |
| ------------------- | -------- | --------- | ------ | ------- |
| Logistic Regression | 0.89     | 0.89      | 0.97   | 0.806   |
| Random Forest       | 0.87     | 0.87      | 0.97   | 0.793   |
| SVM                 | NA       | NA        | 1.00   | 0.840   |
| XGBoost             | NA       | NA        | NA     | 0.923   |

### Major Findings

* All baseline models demonstrated strong discrimination between Active TB and Healthy Controls.
* Logistic Regression achieved the highest overall accuracy (0.89).
* SVM achieved the strongest cross-validation performance (Mean CV AUC = 0.955).
* XGBoost achieved the highest test ROC-AUC (0.923).
* Multiple models independently identified overlapping biomarker candidates, supporting biomarker robustness.

---

## Consensus Biomarker Panel

### Tier 2 – Biologically Prioritized Biomarkers

| Gene   | Biological Role                    |
| ------ | ---------------------------------- |
| GBP1P1 | Interferon-stimulated response     |
| NSMAF  | TNF / immune stress signaling      |
| OSM    | Inflammatory cytokine signaling    |
| PARP14 | Immune regulation / STAT signaling |
| STAT1  | Interferon signaling               |

### Tier 1 – Multi-Model Consensus Biomarkers

* CLEC4GP1
* CPN2
* DOC2B
* F7
* KNSTRN
* PDE4DIP
* RNA28S5

### Combined Reduced Panel

The final reduced biomarker panel consisted of 12 candidate genes combining consensus machine learning support and biological relevance.

---

## Biological Insights

Biological interpretation revealed strong enrichment for:

* Interferon-mediated immune responses
* TNF-associated inflammatory signaling
* Cytokine-mediated immune regulation
* Host-defense and antimicrobial pathways

STAT1 emerged as a particularly compelling biomarker due to its central role in interferon-responsive transcriptional programs. Additional candidates including GBP1P1, PARP14, NSMAF, and OSM demonstrated convergence of machine learning support, SHAP importance, and biological plausibility.

Together, these findings suggest that active tuberculosis is characterized by coordinated activation of interferon and inflammatory signaling pathways that can be detected through host transcriptional signatures.

---

## Explainability Analysis

Model interpretability was assessed using SHAP (SHapley Additive exPlanations).

SHAP analysis identified multiple immune-associated genes among the strongest contributors to model predictions and provided quantitative evidence supporting biomarker prioritization.

### ROC Curve Comparison

![ROC Curve Comparison](results/figures/Figure_1_ROC_Curves.png)

### SHAP Summary Plot

![SHAP Summary Plot](results/figures/Figure_3_SHAP_Summary.png)

Additional visualizations are available in:

- results/figures/Figure_2_CV_Comparison.png
- results/figures/Figure_4_SHAP_Importance.png

## External Validation

Independent validation was initiated using GSE25534.

Completed activities include:

* External dataset selection
* Phenotype label generation
* External biomarker panel creation
* Feature alignment
* Platform compatibility verification

Final validation modeling and performance metrics remain pending reconstruction following notebook loss caused by a power interruption. The validation workflow will be rerun to restore quantitative performance estimates and complete the model generalizability assessment.

---

## Repository Structure

```text
data/
docs/
notebooks/
reports/
results/
  ├── figures/
  ├── models/
  └── tables/
src/
```

---

## Future Work

Planned extensions include:

* Reconstruction of external validation analyses
* Active TB vs Latent TB classification
* Hybrid TB classification models
* Pathway enrichment analysis
* Single-cell RNA-seq integration
* Cell-type mapping of biomarker candidates
* Advanced model comparison and robustness assessment

---

## Author

**Abdulrahman S. Hammond**

Biomedical Scientist | Immunology | Tuberculosis Research | Machine Learning

Project Status: Active Development
