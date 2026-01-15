# Sentiment Analysis on Movie Reviews

This project focuses on **binary sentiment analysis** for movie reviews, classifying each review as **positive** or **negative**.  
It was developed as part of an **NLP course** to compare classical machine learning models with deep learning and Transformer-based approaches.

---

## Problem Definition

Sentiment Analysis aims to identify the emotional polarity of a text.

Example:
That was terrible" → Negative

---

## Dataset

| Attribute | Description |
|---------|------------|
| Dataset Name | imdb-movie-reviews |
| Source | Hugging Face |
| Total Samples | 50,000 reviews |
| Training Set | 40,000 |
| Test Set | 10,000 |
| Labels | Positive / Negative |
| Distribution | Balanced |

---

## Preprocessing

The following preprocessing steps were applied before training the models:

1. Removal of HTML tags  
2. Removal of punctuation  
3. Lowercasing all text  
4. Text vectorization (TF-IDF / Bag of Words / Tokenization depending on model)

---

## Models and Methodology

### Classical Machine Learning Models

| Model | Methodology |
|-----|------------|
| Naive Bayes (TF-IDF) | Multinomial Naive Bayes trained on TF-IDF vectors extracted from cleaned text. |
| Naive Bayes + Stylistic Features | TF-IDF features combined with stylistic cues such as punctuation counts, capitalization, and ellipses. |
| Logistic Regression | Logistic Regression trained using Bag-of-Words (CountVectorizer) representation. |

---

### Deep Learning Models

| Model | Methodology |
|-----|------------|
| CNN + GloVe | CNN with parallel convolution filters (3,4,5), max-pooling, and pretrained 100-dim GloVe embeddings. |
| BiLSTM + Word2Vec | Bidirectional LSTM using Word2Vec embeddings trained on the dataset, with dropout and dense layers. |

---

### Transformer-Based Model

| Model | Methodology |
|-----|------------|
| BERT (bert-base-uncased) | Fine-tuned pretrained BERT model using AdamW optimizer for sentiment classification. |

---

## Results

| Model | Test Accuracy | Key Observations |
|-----|--------------|----------------|
| Naive Bayes (TF-IDF) | 0.85 | Strong baseline; fast and stable |
| Logistic Regression | 0.89 | High accuracy but sensitive to feature sparsity |
| CNN + GloVe | 0.82 | Effective feature extraction with embeddings |
| BiLSTM + Word2Vec | 0.88 | Captures sequential dependencies well |
| BERT | 0.89 | Best overall performance with contextual understanding |


---

## Analysis

- **Naive Bayes** showed strong baseline performance with good generalization.
- **Stylistic features** did not significantly improve classification accuracy.
- **Logistic Regression** overfitted due to high-dimensional sparse features.
- **CNN + GloVe** demonstrated stable learning and effective feature extraction.
- **BiLSTM** captured sequential dependencies but showed mild overfitting.
- **BERT** achieved the best overall performance, leveraging pretrained contextual representations.

---

## Conclusion

The experiments show a clear progression from classical models to deep learning and Transformer-based approaches.  
While simpler models generalize well, pretrained models such as **BERT** provide the strongest performance for sentiment analysis tasks.

