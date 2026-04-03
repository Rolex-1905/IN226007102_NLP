# Data Science Internship – February 2026  
## NLP Task 4 – Fine-Tuning BERT for Sentiment Classification (IMDB Dataset)

---

## Intern Details  

**Name:** Neeraj  
**Intern ID:** IN226007102  
**Module:** NLP (Natural Language Processing)  
**Organization:** Innomatics Research Labs  

## Overview
This project implements fine-tuning of a pre-trained BERT model for binary sentiment classification using the IMDB Movie Reviews dataset. Multiple experiments are conducted to analyze how different fine-tuning strategies affect model performance.

---

## Dataset
- Source: IMDB Movie Reviews Dataset
- Size Used: 5000 samples (subset for faster training)
- Task: Binary Classification (Positive = 1, Negative = 0)

---

## Methodology

### 1. Data Preprocessing
- Removed HTML tags
- Removed special characters
- Converted text to lowercase
- Removed extra whitespace

### 2. Data Splitting
- Train: 70%
- Validation: 15%
- Test: 15%

### 3. Tokenization
- Model: bert-base-uncased tokenizer
- Max Length: 128
- Padding and truncation applied

### 4. Model
- Model: bert-base-uncased
- Framework: PyTorch
- Head: Sequence Classification (2 labels)

---

## Training Configuration
- Optimizer: AdamW
- Learning Rate: 2e-5
- Batch Size: 16
- Epochs: 2

---

## Experiments

### Experiment 1: Frozen BERT
- All BERT layers frozen
- Only classifier layer trained
- Purpose: Evaluate BERT as a feature extractor

### Experiment 2: Fine-Tuning Last 2 Layers
- Last 2 encoder layers + classifier trained
- Remaining layers frozen
- Purpose: Partial adaptation to dataset

### Experiment 3: Full Fine-Tuning
- All layers trainable
- Purpose: Full model adaptation

---

## Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

---

## Results Summary
Performance improves as more layers are fine-tuned.

- Frozen BERT: Lowest performance due to no adaptation
- Last 2 Layers: Better performance with moderate training cost
- Full Fine-Tuning: Best performance with highest computational cost

---

## Key Observations
- Fine-tuning significantly improves model performance
- Partial fine-tuning offers a balance between speed and accuracy
- Full fine-tuning yields best results but requires more resources

---
