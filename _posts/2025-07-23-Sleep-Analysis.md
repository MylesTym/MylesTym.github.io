---
title: Sleep Health ML Analysis
date: 2025-07-23
---

# Sleep Health ML

![Main project image](assets/main-image.png)

This project builds, evaluates, and compares machine learning classification models to predict sleep health outcomes using structured health and behavioral data. The dataset includes variables such as age, BMI, physical activity levels, stress levels, and reported sleep disorders.

The objective is to assess the viability of automated classification models in identifying individuals at risk for poor sleep health or sleep-related conditions, using supervised learning techniques applied to real-world categorical and numeric health indicators.

## Objectives

- Clean and prepare the dataset for supervised learning tasks.
- Engineer features related to sleep quality and health indicators.
- Train multiple machine learning models for binary and multiclass classification.
- Evaluate model performance using standard classification metrics.
- Interpret model outputs to determine feature influence and predictive value.

## Methods and Tools

- **Language:** Python 3.11
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn
- **Environment:** Jupyter Notebook
- **Models Used:** Logistic Regression, K-Nearest Neighbors, Decision Tree, Random Forest, Support Vector Machine
- **Evaluation Metrics:** Accuracy, Precision, Recall, F1 Score, Confusion Matrix

## Project Structure

```text
Sleep-Health-ML/
├── data/                # Raw and preprocessed datasets
├── notebooks/           # Jupyter notebooks for EDA and modeling
├── assets/              # Images and visualizations
├── requirements.txt     # Python package dependencies
└── README.md            # Project documentation

## Key Outcomes

- Decision Tree and Random Forest models yielded the highest performance in multiclass classification tasks.
- Stress and physical activity were among the most influential variables in predicting sleep disorders.
- Preprocessing and feature selection significantly improved model stability and interpretability.

## Repository

GitHub Repository: [https://github.com/MylesTym/Sleep-Health-ML](https://github.com/MylesTym/Sleep-Health-ML)

## Author

Myles Tym  
[GitHub Profile](https://github.com/MylesTym)

## Disclaimer

This project is provided solely for educational and demonstration purposes. It is not intended to deliver medical guidance or clinically accurate health analysis. The included models and results should not be used to make health-related decisions and do not substitute professional healthcare consultation.
