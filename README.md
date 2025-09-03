# MLDP-Project
(MLDP) is a Year 2 module in TP. It introduces the fundamentals of machine learning principles and practices. It covers a range of machine learning models and algorithmic machine learning methods, such as supervised learning.


### What was the purpose of this MLDP Project?

- Save manual effort in cleaning, preparing, and analyzing large datasets.
- Ensure fair model selection by comparing algorithms systematically.
- Deploy a trustworthy model (Random Forest) that can generalize to unseen data, providing actionable insights for businesses or organizations.

In short: the pipeline is meant to bridge the gap between raw data and practical, real-world predictions so decisions can be made more accurately and efficiently.


### What is happening in my Pipeline?
**1. Data Preparation**
- Loaded dataset using Pandas.
- Conducted random sampling to inspect data.
- Removed white spaces and handled string formatting.
- Checked for duplicates → displayed and removed them.
- Basic EDA (shape, columns, first/last rows, dataset size).
- Missing values analysis → created indicator columns to track them.

**2. Exploratory Data Analysis (EDA)**
- Visualized class distribution with bar charts and pie charts.
- Used groupby to summarize categorical features (e.g., income by race).
- Box plots for numerical distributions.
- Explored relationships between categorical features and income levels.
- Identified and removed redundancy:
  - Education vs. education_num → high multicollinearity detected.
  - Dropped one feature to avoid duplication.

**3. Feature Engineering**
- Encoding categorical features (Ordinal, One-Hot where needed).
- Combined related features into more meaningful attributes.
- Extracted important categorical breakdowns (e.g., marital-status, relationship).
- Saved processed dataset to modified-dataset.csv.

**4. Model Training & Validation**
- Split into train/test sets using train_test_split.
- Defined print_metrics function for evaluation (Accuracy, Precision, Recall, F1, ROC AUC).
- Applied K-Fold Cross Validation to get robust results.
- Hyperparameter tuning with GridSearchCV for:
  - Random Forest
  - KNN
  - Decision Tree
  - SVM

**5. Model Comparison & Results**
- Best Performing Model: Random Forest
- Cross-validated accuracy: ~0.861
- Final test accuracy: 0.8621
- Precision: 0.7887 (highest)
- Recall: 0.5994
- F1 Score: 0.6811 (highest)
- ROC AUC: 0.7735 (highest)

Random Forest outperformed all other models consistently across metrics.

**6. Deployment Preparation** 
- Saved trained Random Forest model and scaler using joblib for reuse.
- Set up pipeline structure for future predictions.


### End-to-End Flow
Raw dataset → Cleaning & Deduplication → EDA & Feature Engineering → Train/Test Split → Cross-validation & Hyperparameter Tuning → Model Selection → Save Best Model (Random Forest).
