# 🎯 Job Candidate Acceptance Prediction - ML Final Project

This project is the final submission for my Machine Learning course at university. It tackles a real-world classification problem: **predicting whether a job candidate will be accepted into a high-tech position based on their profile data**. The project demonstrates the full machine learning pipeline, from raw data preprocessing and feature analysis to model training, evaluation, and optimization.

---

## 📊 Project Objective

To build a supervised machine learning model that classifies candidates as either **accepted** or **not accepted** based on historical hiring data.

---

## 📁 Dataset Overview

The dataset consists of tens of thousands of anonymized job candidate records, each containing various numerical and categorical features such as:

- `years_of_experience`
- `previous_salary`
- `A`, `B` (anonymized numerical features)
- `degree_level`
- `field`
- `target` (acceptance label: 1 = accepted, 0 = not accepted)
- and more


---

## 🔧 Preprocessing & Feature Engineering

Significant effort was dedicated to preparing the dataset:

- **Outlier Removal**:  
  - Feature **A**: Removed values > 30 or < -16 based on histogram and box plot analysis.
  - Feature **B**: Removed values > 40 due to right-skewed outliers.
  - `previous_salary`: Removed suspiciously low salaries close to zero.
  
- **Data Cleaning**:  
  - Verified consistency and nulls.
  - Removed erroneous or misleading records.
  
- **Visualization**:  
  - Histograms and box plots used to understand feature distributions.
  - `.describe()` method applied for statistical summary.
- **Data Conversion**:
  - Some data was non-numerical yet was still creatively utilized to evaluate the best model.

---

## 🤖 Modeling & Evaluation

Several classification models were tested, compared, and tuned:

- Logistic Regression
- Random Forest Classifier
- KNN Model
- Multi Layer Perceptron

**Evaluation Metric**: ROC-AUC Curve

Models were evaluated on a hold-out validation set to avoid overfitting.

---

## 🏆 Results Summary

- The best-performing model (the Random Forest Classifier) achieved AUC score of 0.86 when tested with unknown data.
- Feature importance analysis provided insights into which variables influenced hiring decisions the most.

---

## 👤 Author

**[Netanel Druyan]**  
23 y/o Computer Science student passionate about AI, data, and real-world applications of machine learning.

---
## Acknowledgements

Huge thanks to Naama Tanchuma for collaborating and orginizing the project report file.
