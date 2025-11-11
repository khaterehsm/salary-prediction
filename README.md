# salary-prediction
Data Science project (GlassDoor Jobs Salary Prediction)

---

# project overview
This project predicting the job salarie for job postings based on various features like job title, rating, location, etc. The goal is to support businesses and job seekers in making informed decisions about salary expectations.
This repository contains a single Jupyter notebook (`Salary-Prediction-main.ipynb`) that demonstrates the end-to-end process for predicting salaries from job postings. The notebook includes data ingestion, cleaning, exploratory data analysis (EDA), feature engineering, model training (regression and classification variants), and evaluation.

---

## 🗂 Data 
- If you have the CSV, place it into data/ as df.csv.
- Main raw fields used: Job Title, Location, Salary Estimate, Rating, and derived: Min_salary, Max_salary, Average_salary, State, normalized Job Title.

---

## 🧹 Data cleaning & feature engineering (what I did)
- Removed invalid salary entries (e.g., -1, hourly salaries).  
- Parsed salary text (`$`, K, ranges) and created Min_salary, Max_salary, Average_salary.  
- Extracted State from location strings and cleaned inconsistent entries.  
- Normalized Job Title (mapping similar titles to canonical forms).  
- Trimmed outliers using quantiles (e.g., 1% / 99%) to reduce extreme values impact.  
These steps are implemented inside the notebook with commented code blocks.

---

## 📊 Exploratory Data Analysis (EDA)
Key EDA performed:
- Distribution of average salaries (histogram + KDE).  
- Boxplot to find outliers and salary spread.  
- Correlation heatmap between numeric features.  
- Top states / job titles by job count and average salary.  
(See the notebook Salary_Prediction.ipynb for visualizations and interpretive notes.)

---

## 🤖 Modeling
Models trained and evaluated:
- Linear Regression (baseline regression)    
- (Optional) Classification experiments after target binning (if converting salary to classes) used Logistic Regression, KNN, DecisionTree, RandomForest for classification.

Evaluation metrics reported (regression): MAE.  
For classification experiments: accuracy, precision, recall, f1-score and confusion matrix are reported.
A small predict_example.py (or example cell in the notebook) demonstrates how to load the model and make predictions.

