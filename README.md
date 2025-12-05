📊 Model Performance Comparison

This repository documents the development and comparison of four distinct modeling approaches for Binary Sentiment Classification (Positive/Negative) on a large corpus of IMDb movie reviews. We benchmark Traditional Machine Learning (ML) models against Modern Deep Learning (DL) architectures to determine the optimal balance of performance, complexity, and computational cost.

🥇 Final Test Results Summary

The performance of all four primary models is summarized below, based on their final test set evaluation.

Model Type,Feature Extraction,Architecture,Test Accuracy,Test F1-Score,Complexity
SOTA DL,Subword Tokenization,Fine-tuned BERT,0.8915,0.89,Highest
Traditional ML,"CountVectorizer (BoW, N-grams)",Logistic Regression,0.8909,0.89,Low
Sequential DL,Word2Vec Embeddings,Bi-directional LSTM,0.8862,0.89,High
Probabilistic ML,"TfidfVectorizer (TF-IDF, N-grams)",Multinomial Naive Bayes,0.8712,0.87,Lowest
Shallow DL,GloVe Embeddings (Frozen),Multi-Filter 1D CNN,0.8243,0.82,Medium
