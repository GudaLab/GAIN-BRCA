# GAIN-BRCA

A Graph-Based Explainable AI Framework for Breast Cancer Subtype Classification Based on Multi‑Omics

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

\`\`\`bash
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
\`\`\`

## Requirements

- Python ≥ 3.8.10  
- TensorFlow ≥ 2.9.1  
- Keras ≥ 2.9.0  
- scikit-learn ≥ 1.2.1  
- numpy  
- pandas  
- math  

## Data Sources

1. **Clone or Download**  
   \`\`\`bash
   git clone <repository_url>
   \`\`\`
2. **Prepare Input Data**  
   Place the following CSV files into \`dataset/Input/\`:  
   - \`mRNA_NormCount.csv\`  
   - \`miRNA_NormCount.csv\`  
   - \`methyl_NormBeta.csv\`  
   - \`miRNA_mRNA_interaction.csv\`  
   - \`CpG_mRNA_interaction.csv\`  
   - \`dependent_variables.csv\`  
   Datasets available at: https://zenodo.org/records/15175435
3. **Configure Paths**  
   Edit file paths in \`GAIN_BRCA.py\` to match your local directory structure.
4. **Run the Pipeline**  
   \`\`\`bash
   python GAIN_BRCA.py
   \`\`\`
   This will:
   - Import and integrate multi‑omics datasets.  
   - Compute integrated expression values using interaction data.  
   - Train an ANN model with stratified k‑fold cross-validation.  
   - Output prediction accuracy and save probabilities to a CSV file.

## Code Documentation

- **GAIN_BRCA.py**  
  Main script orchestrating data import, integration, and model training.
- **delta_integration.py**  
  - \`int_Delta1(miRNA, mRNA, Int1)\`: Integrates miRNA and mRNA expression.  
  - \`int_Delta2(methyl, mRNA, Int2)\`: Integrates methylation data with mRNA expression.
- **GAIN_BRCA_ANN.py**  
  Implements the ANN model using TensorFlow/Keras: data scaling, cross-validation, training, evaluation, and saving outputs.

## Contact

For questions or issues, please contact:  
Pranav Patel — japatel@unmc.edu  
