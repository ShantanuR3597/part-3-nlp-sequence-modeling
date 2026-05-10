# Part 3: NLP and Sequence Modeling Mini Project

## Problem Statement

The objective of this project is to build a Natural Language Processing (NLP) pipeline for customer support sentiment classification. The project compares traditional text vectorization techniques with sequence-based deep learning approaches.

The goal is to understand how text data is converted into numerical format and how sequence models such as LSTMs process textual information.

---

# Dataset

The dataset contains customer support messages with sentiment labels.

## Dataset Features

- ticket_id
- channel
- customer_message
- sentiment_label
- word_count
- urgent_flag

## Sentiment Classes

- Positive
- Neutral
- Negative

---

# Task 1: Dataset Understanding

The dataset contains 1500 customer support messages.

## Key Observations

- The dataset contains three sentiment classes: positive, neutral, and negative.
- The sentiment distribution is relatively balanced.
- The average customer message length is approximately 12.7 words.
- Customer messages include refund requests, payment issues, account updates, and support feedback.

---

# Task 2: Text Preprocessing

The text preprocessing pipeline included:

- Lowercasing text
- Removing special characters and numbers
- Tokenization
- Removing stopwords
- Creating cleaned text messages

## Observation

The preprocessing steps reduced noise in the text data and improved the quality of input features for machine learning and deep learning models.

---

# Task 3: Text Vectorization

TF-IDF vectorization was used to convert text into numerical feature vectors.

## Observation

- TF-IDF transformed customer messages into meaningful numerical representations.
- 146 text features were generated from the cleaned dataset.
- Label Encoding converted sentiment categories into numerical labels.

---

# Task 4: Baseline Model

A Logistic Regression model was used as the baseline machine learning model.

## Steps Performed

- Train-test split
- TF-IDF vectorization
- Logistic Regression training
- Prediction and evaluation

## Results

- Testing Accuracy: 100%
- Strong classification performance across all sentiment classes.

## Evaluation

The confusion matrix showed perfect classification performance with no major misclassifications.

---

# Task 5: Sequence Model (LSTM)

An LSTM-based sequence model was created for sentiment classification.

## Sequence Modeling Steps

- Tokenization
- Sequence conversion
- Padding sequences
- Train-test split
- Embedding layer
- LSTM layer
- Dense output layer

## LSTM Architecture

- Embedding Layer
- LSTM Layer
- Dense Softmax Output Layer

## Results

- LSTM Testing Accuracy: 100%
- Very low testing loss
- Stable convergence during training

## Observations

The LSTM model successfully captured contextual relationships and sequential dependencies between words.

---

# Task 6: Attention and Transformer Reflection

## Why RNNs Struggle

Traditional RNNs struggle with long-term dependencies because earlier information weakens over time.

## How LSTMs Help

LSTMs use memory cells and gating mechanisms to retain important contextual information.

## Attention Mechanism

Attention allows models to focus on important words within a sequence.

## Importance of Transformers

Transformers process text more efficiently using self-attention and are widely used in modern NLP and Generative AI systems.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow / Keras
- NLTK
- Matplotlib
- Seaborn

---

# Repository Structure

```plaintext
part-3-nlp-sequence-modeling/

│── README.md
│── notebook.ipynb
│── requirements.txt

│── results/
│   ├── model_evaluation.png
│   └── sample_predictions.txt
```

---

# Conclusion

This project demonstrated both traditional NLP techniques and sequence-based deep learning methods for sentiment classification. Logistic Regression with TF-IDF and the LSTM sequence model both achieved strong performance on the dataset. The project also highlighted the importance of sequence learning, attention mechanisms, and transformers in modern NLP applications.
