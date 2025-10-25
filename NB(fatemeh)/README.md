# Sentiment Analysis with Naive Bayes and Combined Features

## Overview
This project performs **sentiment analysis** on IMDB movie reviews using a **Naive Bayes classifier**. The approach combines **TF-IDF text features** with **statistical/style features** to capture both word-level information and review-level characteristics.

---

## Dataset
- IMDB movie reviews from the **HuggingFace `datasets` library**
- Columns:
  - `review` → text of the review
  - `label` → sentiment (0 = positive, 1 = negative)
- Split:
  - 40,000 reviews for training
  - 10,000 reviews for testing

---

## Feature Engineering

### 1. Text Features
- Tokenized reviews
- Vectorized using **TF-IDF** to capture word importance

### 2. Statistical / Style Features
- **Number of exclamation marks (`!`)**: Indicates emphasis or strong emotion.  
- **Number of question marks (`?`)**: Can reflect confusion, sarcasm, or rhetorical questions.  
- **Number of ellipsis (`...` or `…`)**: Often used for pauses, hesitation, or dramatic effect.  
- **Number of all-caps words**: Words written entirely in uppercase (length ≥ 2) can emphasize certain opinions or feelings. 

> TF-IDF vectors and statistical features are **combined into a single feature matrix** for each review.

---

## Model
- **Classifier:** Naive Bayes
- Trained on the **combined feature matrix** (TF-IDF + statistical features)
- Evaluation metrics:
  - **Accuracy**
  - **Confusion matrix**
  - **Classification report** (precision, recall, F1-score)

---

## Summary
- The combination of **TF-IDF and statistical features** allows the model to capture both textual content and stylistic cues.
- Demonstrates a simple and effective **feature engineering + classical ML pipeline** for sentiment analysis.
