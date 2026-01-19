# Sampling Techniques on Credit Card Fraud Analysis

## Overview
This project demonstrates the impact of different sampling techniques on a highly imbalanced credit card fraud dataset. The objective is to balance the dataset, apply multiple sampling strategies, train various machine learning models, and analyze how sampling affects model accuracy.

---

## Objective
- To handle class imbalance in a credit card transaction dataset  
- To apply five different sampling techniques  
- To evaluate five machine learning models  
- To compare results using accuracy tables and graphs  

---

## Dataset Description
- Dataset: Credit Card Fraud Dataset  
- Source: GitHub  
- Target Column: `Class`  
  - `0` – Non-Fraud Transaction  
  - `1` – Fraud Transaction  

The dataset is highly imbalanced, with fraud transactions being significantly fewer than non-fraud transactions.

---

## Methodology

### Step 1: Data Loading
The dataset is loaded using the Pandas library and initial analysis is performed to understand the class imbalance.

### Step 2: Data Balancing
The dataset is first balanced using random undersampling by selecting an equal number of non-fraud transactions to match the fraud transactions.

### Step 3: Sampling Techniques
After balancing, the following five sampling techniques are applied:

- **Sampling1 – Simple Random Sampling:**  
  Random selection of samples from the balanced dataset.

- **Sampling2 – Systematic Sampling:**  
  Samples are selected at fixed intervals.

- **Sampling3 – Stratified Sampling:**  
  Sampling is performed while maintaining class proportions.

- **Sampling4 – Cluster Sampling:**  
  The dataset is divided into clusters, and samples are selected from specific clusters.

- **Sampling5 – Bootstrap Sampling:**  
  Sampling is performed with replacement to generate a new dataset.

---

## Machine Learning Models Used
Five machine learning models are trained on each sampling technique:

- **M1:** Logistic Regression  
- **M2:** Decision Tree  
- **M3:** Random Forest  
- **M4:** K-Nearest Neighbors (KNN)  
- **M5:** Support Vector Machine (SVM)  

The dataset is split into training and testing sets using stratified train-test split.

---

## Evaluation Metric
- **Accuracy** is used as the evaluation metric.
- Accuracy represents the percentage of correctly classified transactions.

---

## Results

### Accuracy Table

| Model | Sampling1 | Sampling2 | Sampling3 | Sampling4 | Sampling5 |
|------|----------|----------|----------|----------|----------|
| M1 | 100.00 | 66.67 | 100.00 | 100.00 | 100.00 |
| M2 | 50.00 | 33.33 | 0.00 | 100.00 | 100.00 |
| M3 | 100.00 | 33.33 | 33.33 | 66.67 | 100.00 |
| M4 | 100.00 | 33.33 | 0.00 | 66.67 | 83.33 |
| M5 | 100.00 | 33.33 | 33.33 | 66.67 | 66.67 |

---

## Result Graphs
Two graphs are generated to visualize the experimental results:

1. **Model-wise Accuracy Comparison:**  
   Compares the performance of each machine learning model across all sampling techniques.

2. **Average Accuracy per Sampling Technique:**  
   Shows the average accuracy achieved by each sampling method.

Both graphs are saved as image files and included in the repository.

---

## Observations
- Sampling techniques significantly affect model performance  
- Some models achieve high accuracy due to overfitting on small balanced datasets  
- No single sampling technique performs best for all models  

---

## Conclusion
This experiment highlights the importance of handling class imbalance in fraud detection problems. Different sampling techniques lead to varying model performance, emphasizing the need for careful selection of sampling strategies before training machine learning models.

