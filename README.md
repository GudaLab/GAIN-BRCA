# GAIN-BRCA
GAIN-BRCA: A graph-based explainable AI framework for breast cancer subtype classification based on multi-omics

A graph-based explainable AI framework called GAIN-BRCA leverages multi-omics datasets to classify TCGA-breast cancer subtypes based on PAM50. The omics interaction among the gene expression, DNA methylation, and microRNA was the basis for omics integration. The gene expression is controlled by methylation and miRNA interaction with the gene. This biological relationship was used to integrate the multi-omics datasets.

## GAIN-BRCA Workflow
![Picture1](https://github.com/user-attachments/assets/27dd7683-89d1-4d35-ba41-aa614811a6ea)

# Requirements
•	Tensorflow (>= 2.9.1)
•	Keras (>= 2.9.0)
•	Python (>= 3.8.10)
•	Scikit-learn (>=1.2.1)
•	Basic Python packages: numpy, pandas, math

## Usage
Clone the repository or download source code files and prepare breast cancer multi-omics datasets as per the dataset/Input folder. Edit the directory path in GAIN-BRCA.py to the input files and run. The final accuracy will be as an output of the ANN model trained on GAIN-BRCA based integrated omics after the successful execution of the command.

## Contact
Please contact japatel@unmc.edu if you have any inquiries or issues.
