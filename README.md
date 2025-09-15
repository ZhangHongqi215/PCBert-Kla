# PCBert-Kla: An Efficient Prediction Method for Lysine Lactylation Sites Based on BERT and Fusion of Physicochemical Features

## Overview

**PCBert-Kla** is a novel computational tool designed to identify **lysine lactylation (Kla)** sites in proteins. By leveraging **ProtBert**, a protein-specific BERT-based language model, and integrating multiple **physicochemical features**, PCBert-Kla offers state-of-the-art accuracy, robustness, and generalization in Kla site prediction.

PCBert-Kla combines the power of deep learning and protein-specific language models with the incorporation of key protein properties to predict Kla sites effectively. It outperforms existing methods in terms of predictive performance and generalization.

## Key Features

- **Protein Sequence Representation**: PCBert-Kla utilizes the **ProtBert** model, a pre-trained BERT-based model for protein sequences, to extract deep features from protein sequences, improving prediction accuracy for Kla sites.
  
- **Fusion of Physicochemical Features**: The model integrates a wide range of physicochemical properties of proteins, including:
  - Molecular weight
  - Isoelectric point
  - Amino acid composition
  - Secondary structure content
  - Hydrophobicity
  - Charge distribution

  These features enrich the model's ability to predict Kla sites by considering both sequence and structural characteristics of proteins.

- **Attention Mechanism**: PCBert-Kla incorporates an attention mechanism in the fully connected layers, which allows the model to automatically select the most relevant features for Kla site prediction, further improving its accuracy and robustness.

- **State-of-the-art Performance**: PCBert-Kla demonstrates exceptional accuracy and generalization capabilities, outperforming existing methods in Kla site prediction across multiple performance metrics.

## Installation

To get started with PCBert-Kla, clone the repository and install the necessary dependencies:

```bash
git clone https://github.com/ZhangHongqi215/PCBert-Kla.git
cd PCBert-Kla
```

## Data

The dataset includes protein sequences in **FASTA** format. These sequences are processed to extract relevant features, which are then used for training and evaluating the model.

### Dataset Files

- `upTrain.fasta`: Training dataset containing labeled protein sequences.
- `upTest.fasta`: Test dataset for model evaluation.

### Data Format

- Each sequence in the dataset is in **FASTA** format, where each sequence is labeled with the Kla site information.
- The sequences are processed to extract the necessary features before being fed into the model for training.

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
