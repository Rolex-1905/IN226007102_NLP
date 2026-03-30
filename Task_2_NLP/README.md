# Data Science Internship – February 2026  
## NLP Task 2 – Sentiment Analysis using NLP Pipeline & ML Models

---

## Intern Details  

**Name:** Neeraj  
**Intern ID:** IN226007102  
**Module:** NLP (Natural Language Processing)  
**Organization:** Innomatics Research Labs  

---

## Project Description  

This assignment focuses on building a **complete end-to-end Sentiment Analysis system** using real-world text data.  

The goal is to understand how raw text is preprocessed, transformed into numerical features, and used to train machine learning models that can classify sentiment as **Positive** or **Negative**.

The solution is implemented using **Python in a Jupyter Notebook**, following a clean and modular approach.

---

## Dataset  

**Source:** IMDb Movie Reviews Dataset  
**Size:** 50,000 reviews  
**Labels:** Positive / Negative (balanced — 25,000 each)  
**Link:** [IMDb Dataset on Kaggle](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)

---

## Pipeline Flow  
```
Raw Data → Preprocessing → Feature Engineering → Model Training → Evaluation → Comparison
```

---

## Concepts Implemented  

- Text Normalization (lowercasing, whitespace cleaning)
- HTML Tag Removal (critical for IMDb data)
- Special Character and Punctuation Removal
- Tokenization
- Stopword Removal
- Lemmatization
- Bag of Words (BoW) Vectorization
- TF-IDF Vectorization
- Machine Learning Classification Models
- Model Evaluation using Accuracy, Precision, Recall, F1 Score

---

## Features Implemented  

### 🔹 NLP Preprocessing Pipeline  

A reusable `preprocess()` function was developed that applies the following steps in order:

1. Lowercase the text  
2. Remove HTML tags (e.g., `<br />`)  
3. Remove special characters and punctuation  
4. Tokenize into individual words  
5. Remove stopwords  
6. Lemmatize tokens to base word forms  

---

### 🔹 Feature Engineering  

Text was converted into numerical features using two approaches:

- **Bag of Words (BoW)** – counts word occurrences using `CountVectorizer`  
- **TF-IDF** – weights words by importance using `TfidfVectorizer`  

Both were evaluated against all models for comparison.

---

### 🔹 Model Building  

Three machine learning models were trained and evaluated:

| Model | Type |
|-------|------|
| Logistic Regression | Linear Classifier |
| Naive Bayes | Probabilistic Classifier |
| Decision Tree | Tree-based Classifier |

---

### 🔹 Model Evaluation  

Each model was evaluated using:
- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**

Results were compared across both TF-IDF and BoW vectorizers.

---

## Key Results  

| Model | Vectorizer | Accuracy |
|-------|------------|----------|
| Logistic Regression | TF-IDF | ~89% |
| Naive Bayes | TF-IDF | ~86% |
| Decision Tree | TF-IDF | ~72% |

> **Best Model:** Logistic Regression with TF-IDF

---

## Comparison & Insights  

**Best Vectorizer: TF-IDF**  
TF-IDF outperforms BoW because it assigns higher weights to rare but informative words while down-weighting common words.

**Best Model: Logistic Regression**  
Logistic Regression performs best on sparse, high-dimensional text features. It is also interpretable and fast to train.

**Trade-offs:**  
- Naive Bayes — fastest training, competitive accuracy, good for quick results  
- Logistic Regression — best accuracy, slightly slower  
- Decision Tree — most interpretable but overfits on text data  

---

## Technologies Used  

- Python  
- Jupyter Notebook  
- NLTK  
- Scikit-learn  
- Pandas  
- Regular Expressions (`re`)  

---

## File Structure  
```
Task_2_NLP/
│
└── sentiment_analysis.ipynb   ← Main notebook with all code and outputs
```

---

## How to Run  

1. Clone the repository  
2. Open `sentiment_analysis.ipynb` in Jupyter Notebook or Google Colab  
3. Run all cells from top to bottom  
4. The dataset will be downloaded automatically in Cell 2  

---

## Conclusion  

This project demonstrates a complete NLP pipeline for sentiment classification.  
By combining proper preprocessing, feature engineering, and model comparison, the system achieves strong performance on real-world movie review data.  

The implementation highlights how text cleaning quality and vectorization choice directly impact model accuracy.

---

## 📝 Author  

**Neeraj**  
Innomatics Research Labs — Data Science Internship, February 2026
