### A Graph-Based Explainable AI Framework for Breast Cancer Subtype Classification Based on Multi‑Omics

---

## Table of Contents

- [Overview](#overview)
- [Workflow](#workflow)
- [File Structure](#file-structure)
- [Requirements](#requirements)
- [Data Sources](#data-sources)
- [Code Documentation](#code-documentation)
- [Contact](#contact)


## Overview

- **GAIN-BRCA** leverages multi‑omics datasets to classify TCGA breast cancer subtypes based on PAM50.
- Integrates gene expression, DNA methylation, and microRNA data via their biological interactions.
- Models regulatory relationships where gene expression is influenced by methylation and miRNA interactions.
- Employs a graph‑based explainable AI framework for enhanced integration and prediction.

## Workflow

![GAIN-BRCA Workflow](https://github.com/user-attachments/assets/f07b3481-a831-40ec-874e-558af3c8e2e9)
*Figure: GAIN-BRCA analysis pipeline.*

## File Structure

```bash
GAIN-BRCA/
├── GAIN_BRCA.py
├── delta_integration.py
├── GAIN_BRCA_ANN.py
└── dataset/
    └── Input/
        ├── mRNA_NormCount.csv
        ├── miRNA_NormCount.csv
        ├── methyl_NormBeta.csv
        ├── miRNA_mRNA_interaction.csv
        ├── CpG_mRNA_interaction.csv
        └── dependent_variables.csv
