
# NLP Disaster Tweets Classification - Kaggle Mini-Project

**MSc Computer Science & AI – Deep Learning Peer-Graded Assignment**
Author: Fatih Uenal
Date: June 2025# NLP Disaster Tweets Classification 🚨

**Author:** Fatih Uenal  
**Course:** CU Boulder MSc in Computer Science & AI  
**Project:** Week 4 NLP Mini-Project  
**Date:** 10.06.2025  
**Repository:** [GitHub](https://github.com/FUenal/week4_nlp_mini_project_msc_compsci_final)

---

## 🧠 Project Overview

This mini-project addresses a real-world Natural Language Processing (NLP) task from the [Kaggle "Disaster Tweets" competition](https://www.kaggle.com/competitions/nlp-getting-started). The goal is to build a classifier that determines whether a tweet refers to a real disaster (`target=1`) or not (`target=0`).

Key aspects include:
- Working with noisy, informal language typical of Twitter.
- Preprocessing and cleaning textual data.
- Comparing traditional ML (TF-IDF + Logistic Regression) with deep learning approaches (BiLSTM and BiGRU).

---

## 📁 Dataset

Three files are used:
- `train.csv`: 7,613 labeled tweets (`target` column provided).
- `test.csv`: 3,263 unlabeled tweets for prediction.
- `sample_submission.csv`: Template for Kaggle submission.

Primary features:
- `text`: the tweet content (main input feature)
- `keyword` and `location`: optional features with missing values

---

## 🔍 Exploratory Data Analysis (EDA)

Key insights:
- Balanced classes between disaster and non-disaster tweets.
- Slight difference in tweet lengths by class.
- Significant missing values in `keyword` and `location`.

Preprocessing steps:
- Lowercasing text
- Removing URLs, mentions, hashtags, and special characters
- Handling missing values

---

## 📐 Model Architectures

Three models were built and compared:

### 1. Logistic Regression with TF-IDF (Baseline)
- Simple, interpretable baseline model
- Fast to train
- Used TF-IDF features from raw tweet text

### 2. Bidirectional LSTM
- Learns semantic relationships from sequences
- Embedding + BiLSTM + Dense + Dropout layers

### 3. Bidirectional GRU
- Alternative to LSTM (lighter and faster)
- Achieves comparable performance

All neural models used:
- Custom word embeddings
- Binary cross-entropy loss
- Sigmoid activation in the final layer

---

## 🏁 Results

The notebook includes accuracy scores, confusion matrices, and classification reports for all models. The best performance came from the deep learning models, especially with BiLSTM.

### 📸 Kaggle Submission

![Kaggle Leaderboard Screenshot](kaggle_score.png)

> *(Replace with actual path in your repo.)*

---

## Example Submission File

```csv
id,label
abc123,0
def456,1
ghi789,0
```

---

## Acknowledgments

* Kaggle and the organizers for providing a rich, real-world dataset.
* The MSc Computer Science & AI program for framing this as a hands-on assignment.

---

