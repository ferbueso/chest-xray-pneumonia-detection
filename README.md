# Chest X-ray Pneumonia Detection  
This repository contains a deep learning project focused on detecting pneumonia from chest X-ray images. It involves exploratory data analysis, data preprocessing, model design and training from scratch, performance optimization, and final evaluation. No pretrained models are used to ensure that all feature extraction and learning is achieved through custom CNN architectures.

## Table of Contents

- [Dataset Citation](#dataset-citation)  
- [Overview](#overview)  
- [Data Preprocessing](#data-preprocessing)  
- [Modeling](#modeling)  
- [Evaluation Metrics](#evaluation-metrics)  
- [Results](#results)  

## Dataset Citation  
Mooney, P. (2018). Chest X-Ray Images (Pneumonia) [Dataset]. Kaggle.  
🔗 [https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)

## Overview  

The goal of this project is to develop a deep learning model to classify chest X-ray images as either pneumonia or normal. The project follows these key steps:

1. Exploratory data analysis to understand the dataset  
2. Data cleaning and preparation for deep learning pipelines  
3. Training a baseline convolutional neural network (CNN)  
4. Improving the model architecture and training procedure  
5. Final evaluation on a held-out test set  

## Data Preprocessing  

The dataset is structured into separate folders for training, validation, and testing. Preprocessing steps included:

- Loading and normalizing image data  
- Applying data augmentation techniques to improve generalization (random flips, rotations)  
- Implementing a custom PyTorch dataset class and data loaders  
- Ensuring strict separation between training, validation, and test data  
- Fixing random seeds for reproducibility

## Modeling  

Two main models were developed:

1. **Baseline CNN Model**  
   - Shallow architecture trained from scratch  
   - Used as a performance benchmark  

2. **Improved CNN Model**  
   - Enhanced architecture with additional convolutional blocks  
   - Incorporated data augmentation, dropout and early stopping

📊 Training runs were logged using [Weights & Biases](https://wandb.ai/).

## Evaluation Metrics  

To assess model performance comprehensively, the following metrics were used:

- **Accuracy**: Overall correctness of predictions  
- **Precision**: Proportion of predicted pneumonia cases that were correct  
- **Recall**: Proportion of actual pneumonia cases correctly identified  
- **F1-score**: Harmonic mean of precision and recall  
- **Confusion Matrix**: Detailed breakdown of model predictions  

## Results  

| Model           | Accuracy | F1 Score | Notes                                     |
|----------------|----------|----------|--------------------------------------------|
| Baseline CNN   | 95.9%    | 0.97     | Trained from scratch                       |
| Improved CNN   | 93.5%    | 0.95     | Data augmentation, dropout, early stopping |

🧪 Final evaluation was done only once on the test set to prevent data leakage and ensure fair reporting.
