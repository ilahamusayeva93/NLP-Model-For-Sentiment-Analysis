# NLP Model for Sentiment Analysis

## Overview

This repository contains an R Notebook for sentiment analysis on customer reviews about a restaurant using Natural Language Processing (NLP) techniques. The analysis involves loading and exploring the NLP dataset, data preparation, tokenization, vectorization, model training, evaluation, and interpretation of results.

## Notebook Details

### 1. Load Required Libraries

- **Libraries:** The script loads necessary R libraries for data manipulation, text processing, and modeling, including `tidyverse`, `text2vec`, `caTools`, `glmnet`, and `pROC`.

### 2. Read and Explore Data

- **Data Reading:** The notebook reads a CSV file containing NLP data and displays the first few rows and column names of the dataset.

### 3. Data Preparation

- **Train-Test Split:** The dataset is split into training and testing sets using a seed for reproducibility.

### 4. Tokenization and Vectorization

- **Tokenization:** The training and testing data are tokenized using preprocessor and word tokenizer functions.

- **Vocabulary Creation and Pruning:** A vocabulary is created and pruned based on term counts and document proportions. The pruned vocabulary is displayed, and a vectorizer is created.

- **Document-Term Matrix (DTM):** Document-term matrices are created for both training and testing data.

### 5. Model Training

- **glmnet Classifier:** A glmnet classifier is trained using cross-validation with the training data.

### 6. Model Evaluation on Training Set

- **Maximum AUC:** The notebook displays the maximum Area Under the Curve (AUC) on the training set.

### 7. Tokenization and Vectorization for Testing Set

- **Tokenization and DTM Creation:** The testing data is tokenized, and a document-term matrix is created using the existing vocabulary.

### 8. Model Evaluation on Testing Set

- **Prediction:** Predictions are made on the testing data, and coefficients and feature importance are extracted.

### 9. ROC Analysis and Confusion Matrix

- **ROC Analysis:** Receiver Operating Characteristic (ROC) analysis is performed using the predicted probabilities.

- **Confusion Matrix:** A confusion matrix is displayed for model evaluation on the testing set.

## Dataset Information

### Description

The dataset consists of 1000 customer reviews about a restaurant, with each review labeled binarily (0 for negative, 1 for positive sentiment).

### Analysis Tasks

1. **Data Import:** Import the NLP dataset and get familiarized with it.
2. **Define Preprocessing Function:** Define a preprocessing function for text data.
3. **Define Tokenization Function:** Define a tokenization function for text data.
4. **Modeling:** Train a normal N-fold GLM model.
5. **Predict Model and Remove Stopwords:** Make predictions, remove stopwords, and create a pruned vocabulary.
6. **Create DTM for Training and Testing:** Apply tokenization and vectorization for training and testing with the new pruned vocabulary.
7. **Apply Vectorizer:** Create a vectorizer for the training data.
8. **Interpretation for Model:** Provide interpretation for the trained model.

## How to Use

To replicate the analysis:

1. Ensure you have R and the required libraries installed.
2. Place the "nlpdata.csv" dataset in the same directory as the notebook.
3. Run the notebook in an R environment, considering any specific package dependencies.

## Author

- **Author:** Ilaha Musayeva
- **Date:** 11.04.23


