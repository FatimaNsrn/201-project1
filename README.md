# 📊 Model Performance Comparison

This repository documents the development and comparison of four distinct modeling approaches for Binary Sentiment Classification (Positive/Negative) on a large corpus of IMDb movie reviews. We benchmark Traditional Machine Learning (ML) models against Modern Deep Learning (DL) architectures to determine the optimal balance of performance, complexity, and computational cost.

## Key Objectives

Implement robust text preprocessing and feature engineering techniques.

Establish a strong ML baseline using classic count and frequency-based vectorization (BoW, TF-IDF).

Develop a custom CNN model utilizing static GloVe embeddings.

Fine-tune the state-of-the-art BERT model for maximum accuracy.

Provide a clear, quantitative comparison of all models.

## 💾 Dataset and Preprocessing

The project uses a clean, pre-processed version of the IMDb movie review dataset, split into training (40,000 reviews) and testing (10,000 reviews) sets.

<img width="519" height="111" alt="image" src="https://github.com/user-attachments/assets/e85fb595-31a1-4d55-8212-8f5d9390440a" />

## Standard Preprocessing

All models were trained on text data that underwent the following steps:

HTML Tag Removal (e.g., <br />).

Lowercasing.

Punctuation and Special Character Removal.

Whitespace Standardization.


## 🥇 Final Test Results Summary

The performance of all four primary models is summarized below, based on their final test set evaluation.

<img width="731" height="364" alt="image" src="https://github.com/user-attachments/assets/6be59cd6-0870-493e-8d72-897564ccf0a3" />

### 1. Traditional ML Baseline: Logistic Regression
   
This model serves as a powerful, interpretable baseline. It relies on explicit feature engineering using Bag-of-Words (BoW) with Count Vectors for unigrams and bigrams

<img width="854" height="487" alt="image" src="https://github.com/user-attachments/assets/e126f025-7c3d-40a1-bfc5-d6ea839e8a8d" />

### 2. Sequential Deep Learning: Bi-directional LSTM
   
This model explores recurrent networks for sentiment classification, using Word2Vec embeddings trained specifically on the training corpus. The use of a Bi-directional LSTM allows the model to process contextual information both forward and backward through the sentence, improving sequence understanding.

<img width="854" height="207" alt="image" src="https://github.com/user-attachments/assets/181f35f2-9765-4233-add9-f343469cbd8e" />

### 3. Shallow Deep Learning: Multi-Filter 1D CNN

This CNN uses parallel 1D convolutional layers with different kernel sizes (3, 4, 5) to act as variable-length n-gram detectors. It leverages frozen GloVe embeddings (100d) to utilize external semantic knowledge.

### 4. SOTA Deep Learning: Fine-tuned BERT
   
The project's highest-performing model, based on the bert-base-uncased transformer. Fine-tuning allows the model to adapt its deep, pre-trained contextual knowledge directly to the sentiment task.

<img width="828" height="111" alt="image" src="https://github.com/user-attachments/assets/f7d2a78e-aaac-41e8-8418-d850a9b7d7e6" />

💻 Running the Project

Please see the individual code files in the repository for specific installation and execution instructions for each model environment (PyTorch for BERT/LSTM, TensorFlow for CNN, and Scikit-learn for ML Baselines).
