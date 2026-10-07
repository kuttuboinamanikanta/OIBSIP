# Iris Flower Classification Project 🌸

## Overview
This project is an end-to-end Machine Learning classification workflow built in Python. The objective is to train a model to accurately identify the species of an Iris flower (*Setosa, Versicolor, or Virginica*) based on four physical measurements: sepal length, sepal width, petal length, and petal width.

## Tech Stack
* **Language:** Python 3.x
* **Environment:** Jupyter Notebook
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Machine Learning:** `scikit-learn`

## Dataset
The project utilizes the classic **Iris Dataset**, originally published by Ronald Fisher in 1936. It is loaded directly via `sklearn.datasets.load_iris()`. The dataset contains 150 samples (50 for each of the three species) and has no missing values.

## Project Workflow
1. **Exploratory Data Analysis (EDA):** Checked data types, null values, and basic statistics.
2. **Data Visualization:** Generated boxplots and pairplots to visualize feature distributions and class separability.
3. **Feature Selection Analysis:** Identified that *Petal Length* and *Petal Width* are the most highly discriminative features.
4. **Model Training:** Split the data (80% training / 20% testing) and trained two classifiers:
   * Logistic Regression
   * Random Forest Classifier
5. **Model Evaluation:** Evaluated both models using Accuracy Scores, Confusion Matrices, and Classification Reports.

## Key Findings & Conclusion
* **Feature Importance:** The `Setosa` species is perfectly linearly separable from the others using just petal measurements.
* **Best Model:** **Logistic Regression** was declared the optimal model for this specific task. 
* **Justification:** While both models achieved near-perfect accuracy on the test set, Logistic Regression was chosen because the data is largely linearly separable. Using a complex ensemble method like Random Forest on such a simple dataset is computationally unnecessarily and prone to overfitting, whereas Logistic Regression is fast, mathematically simple, and highly interpretable.

## How to Run This Project Locally
1. Clone this repository to your local machine.
2. Ensure you have Python installed.
3. Install the required libraries by running:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn jupyter
