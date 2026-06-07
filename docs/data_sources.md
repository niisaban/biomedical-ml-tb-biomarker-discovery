## Data Sources
## Overview

This project uses publicly available human transcriptomic datasets from the NCBI Gene Expression Omnibus (GEO) to develop and validate machine learning models for tuberculosis biomarker discovery.

The datasets were selected to support both model development and independent external validation.

## Dataset Summary

| Dataset | Purpose | Platform |
|----------|----------|----------|
| GSE19491 | Model development and feature discovery | Illumina HumanHT-12 v3.0 |
| GSE25534 | External validation | Illumina HumanHT-12 platform |

## Primary Development Dataset

## GSE19491

#### Source
- Repository: NCBI Gene Expression Omnibus (GEO)
- Accession: GSE19491

#### Role
Model development and biomarker discovery

#### Description
GSE19491 is a human whole-blood transcriptomic dataset containing samples from:

- Active Tuberculosis (TB)
- Latent Tuberculosis Infection (LTBI)
- Healthy Controls

#### Platform
- Illumina HumanHT-12 v3.0 Expression BeadChip
- GEO Platform: GPL6947

#### Project Usage
This dataset was used for:

- Data preprocessing
- Probe-to-gene mapping
- Feature selection
- Machine learning model training
- Cross-validation
- SHAP explainability analysis
- Biomarker panel development

## External Validation Dataset

# GSE25534

#### Source
- Repository: NCBI Gene Expression Omnibus (GEO)
- Accession: GSE25534

#### Role
Independent external validation

#### Description
GSE25534 is an independent human transcriptomic dataset used to evaluate the reproducibility and generalizability of biomarkers identified from the primary development dataset.

#### Project Usage
This dataset was used for:

- Feature alignment validation
- External model assessment
- Biomarker reproducibility evaluation

# Data Processing Notes

The following preprocessing steps were performed before model development:

1. Probe annotation and gene mapping.
2. Removal of probes lacking valid gene symbols.
3. Gene-level aggregation of expression values.
4. Feature alignment between development and validation datasets.
5. Quality control and consistency checks.
6. Preparation of machine learning-ready matrices.

# Data Availability

All datasets used in this project are publicly available through the NCBI Gene Expression Omnibus (GEO).

Researchers wishing to reproduce this work should obtain the datasets directly from GEO and follow the preprocessing workflow documented in this repository.

# Reproducibility

The repository does not redistribute raw GEO datasets.

Instead, it provides:

- Processing workflows
- Analysis notebooks
- Feature selection procedures
- Modeling pipelines
- Validation workflows

to support reproducibility while preserving data provenance.

