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

> *Note: Feature names were anonymized for the project.*

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

---

## 🤖 Modeling & Evaluation

Several classification models were tested, compared, and tuned:

- Logistic Regression
- Random Forest Classifier
- Gradient Boosting (XGBoost)
- Support Vector Machine (SVM)

**Evaluation Metrics:**

- Accuracy
- Precision / Recall
- F1-Score
- ROC-AUC Curve

Models were evaluated on a hold-out validation set to avoid overfitting.

---

## 🏆 Results Summary

- The best-performing model achieved **over 90% accuracy**, with strong precision and recall scores.
- Feature importance analysis provided insights into which variables influenced hiring decisions the most.

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/job-candidate-ml.git
   cd job-candidate-ml
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch the notebook:
   ```bash
   jupyter notebook
   ```

4. Open `notebook_43.ipynb` and run all cells sequentially.

---

## 📦 Requirements

- Python 3.8+
- pandas
- numpy
- matplotlib / seaborn
- scikit-learn
- xgboost
- jupyter

> All packages can be installed via `requirements.txt`.

---

## 👤 Author

**[Your Full Name]**  
23 y/o Computer Science student passionate about AI, data, and real-world applications of machine learning.

---

## 🙌 Acknowledgements

Thanks to our course instructor **Ron [Last Name]** for guidance and structure throughout this project.
