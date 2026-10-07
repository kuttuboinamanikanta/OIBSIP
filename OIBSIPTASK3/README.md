# Email/SMS Spam Detection with Machine Learning 📧

## Overview
This project builds a Natural Language Processing (NLP) binary classifier to distinguish between spam and legitimate (ham) messages. It is part of the Oasis Infobyte Data Science internship.

## Tech Stack
* **Language:** Python 3.x
* **Libraries:** `pandas`, `scikit-learn`, `nltk`, `matplotlib`, `seaborn`, `wordcloud`
* **Concepts:** Natural Language Processing (NLP), Text Preprocessing, TF-IDF Vectorization, Binary Classification

## Dataset
The model is trained on the classic **SMS Spam Collection Dataset** (sourced from Kaggle). The dataset contains 5,572 text messages labeled as either `ham` or `spam`. 
* **Ham:** ~86.6%
* **Spam:** ~13.4%

## Project Workflow
1. **Data Cleaning:** Dropped empty columns and mapped text labels to binary integers (`spam: 1`, `ham: 0`).
2. **Text Preprocessing Pipeline:** 
   * Converted all text to lowercase.
   * Removed numbers and punctuation using regular expressions.
   * Removed common English stopwords using the `nltk` library to reduce noise.
3. **Data Visualization:** 
   * Plotted class distribution charts.
   * Generated **WordClouds** to visually highlight the most frequent words in spam (e.g., "FREE", "TEXT", "CALL") vs. ham (e.g., "ok", "come", "time").
4. **Feature Extraction:** Used **TF-IDF Vectorizer** to transform the cleaned text into a numerical feature matrix (capped at 3000 max features).
5. **Model Training:** Split the data 80/20 and trained two classifiers:
   * `Multinomial Naive Bayes` (Industry standard for text classification)
   * `Logistic Regression`
6. **Evaluation:** Evaluated models based on Accuracy, Precision, Recall, F1-Score, and Confusion Matrices.

## Key Insights: The Importance of Recall
In spam detection, evaluating a model requires a careful balance between Precision and Recall. While high precision ensures legitimate emails aren't sent to the spam folder, **Recall** is critical because a low recall score means the filter is failing its primary job: catching spam. A robust spam filter must maximize recall to keep inboxes clean without sacrificing the precision needed to protect vital communications.

## How to Run This Project
1. Clone this repository.
2. Install required dependencies:
   ```bash
   pip install pandas scikit-learn nltk matplotlib seaborn wordcloud