# PCBert-Kla: An Efficient Prediction Method for Lysine Lactylation Sites Based on BERT and Fusion of Physicochemical Features

## Overview

**PCBert-Kla** is a novel computational tool designed to identify **lysine lactylation (Kla)** sites in proteins. By leveraging **ProtBert**, a protein-specific BERT-based language model, and integrating multiple **physicochemical features**, PCBert-Kla offers state-of-the-art accuracy, robustness, and generalization in Kla site prediction.

## Key Features

- **Protein Sequence Representation**: PCBert-Kla utilizes the **ProtBert** model, a pre-trained BERT-based model for protein sequences, to extract deep features from protein sequences, improving prediction accuracy for Kla sites.
  
- **Fusion of Physicochemical Features**: The model integrates a wide range of physicochemical properties of proteins, including:
  - Molecular Weight Calculation
  - Isoelectric Point Calculation
  - Amino Acid Composition Analysis
  - Secondary Structure Content Prediction
  - Hydrophobicity Calculation
  - Net Charge Calculation

  These features enrich the model's ability to predict Kla sites by considering both sequence and structural characteristics of proteins.

## Installation

To get started with PCBert-Kla, clone the repository:

```bash
git clone https://github.com/ZhangHongqi215/PCBert-Kla.git
cd PCBert-Kla
```

## Data

The dataset includes protein sequences in **csv** format. These sequences are processed to extract relevant features, which are then used for training and evaluating the model.

### Dataset Files

- `train.csv`: Training dataset containing labeled protein sequences.
- `test.csv`: Test dataset for model evaluation.

## How to Run

1. **Prepare the Data**:
   Place your protein sequence data in the `data/` directory. You can download or upload your own dataset in **FASTA** format.

2. **Run the Notebook**:
   Open and run the `PCBert-Kla.ipynb` notebook in Jupyter Notebook or JupyterLab.

3. **Model Training and Evaluation**:
   The notebook will guide you through training the model and evaluating its performance on the test dataset. The results will include metrics such as accuracy, precision, recall, and F1 score.


## Model Architecture

The PCBert-Kla model consists of the following components:

1. **ProtBert Encoder**: A pre-trained BERT model specialized for protein sequences. It encodes the protein sequences into dense vector representations.

2. **Physicochemical Feature Integration**: The model integrates various physicochemical features such as molecular weight, isoelectric point, and secondary structure content to improve prediction capabilities.

3. **Attention Mechanism**: An attention mechanism in the fully connected layers enables the model to focus on the most relevant features, improving accuracy and interpretability.

4. **Fully Connected Layers**: The model employs several fully connected layers to perform classification, with dropout for regularization and batch normalization for stability.

## Evaluation

PCBert-Kla has demonstrated superior performance in predicting Kla sites, as measured by several metrics, including:

- **Accuracy**: The percentage of correctly predicted Kla sites.
- **Precision**: The fraction of true Kla site predictions among all predicted Kla sites.
- **Recall**: The fraction of actual Kla sites that are correctly predicted.
- **F1 Score**: The harmonic mean of precision and recall.
