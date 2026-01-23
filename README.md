IBM HR Analytics Employee Attrition Prediction
📌 Project Overview

This project builds and compares multiple machine learning models to predict employee attrition using the IBM HR Analytics dataset.
The goal is to identify whether an employee is likely to leave the company based on demographic, job-related, and satisfaction-related features.

Three supervised learning models are implemented and evaluated:

Logistic Regression

Decision Tree Classifier

Random Forest Classifier

The models are compared using F1 Score, which is especially important due to class imbalance in attrition data.

📂 Dataset

Name: IBM HR Analytics Employee Attrition Dataset

Format: CSV

Records: 1470 employees

Target Variable: Attrition (Yes or No)

The dataset contains a mix of numerical and categorical features related to employee demographics, job role, satisfaction, compensation, and work-life balance.

🛠️ Technologies Used

Python

Pandas and NumPy for data handling

Matplotlib and Seaborn for visualization

Scikit-learn for machine learning models and evaluation

Google Colab for execution and file upload

⚙️ Workflow
1. Data Loading

Dataset is uploaded using Google Colab file upload.

CSV file is read into a Pandas DataFrame.

2. Data Exploration

Dataset structure and data types are inspected using info().

Missing values are checked and confirmed to be absent.

Descriptive statistics are generated for numerical features.

3. Data Cleaning

The following columns are removed as they do not contribute meaningful information:

EmployeeCount

Over18

StandardHours

4. Encoding Categorical Variables

All categorical columns are encoded using Label Encoding.

The target variable Attrition is converted into numerical format.

5. Train Test Split

Features and target are separated.

Data is split into:

80 percent training set

20 percent testing set

Stratified sampling is used to preserve class distribution.

6. Feature Scaling

Standardization is applied using StandardScaler.

Scaling is done after train test split to avoid data leakage.

🤖 Models Implemented
Logistic Regression

Used as a baseline model.

Performs well in overall accuracy.

Shows moderate performance on minority class prediction.

Decision Tree Classifier

Simple and interpretable.

Suffers from overfitting.

Lower F1 score compared to other models.

Random Forest Classifier

Ensemble model with 100 decision trees.

Strong performance on majority class.

Lower recall for attrition class due to imbalance.

📊 Model Evaluation

The models are evaluated using:

Confusion Matrix

Precision, Recall, and F1 Score

Classification Report

F1 Score Comparison
Model	F1 Score
Logistic Regression	~0.49
Decision Tree	~0.32
Random Forest	~0.23

A bar chart is generated to visually compare model F1 scores.

🔍 Feature Importance

Feature importance is extracted from the Random Forest model.

Top 15 influential features are visualized using a bar chart.

Common influential features include:

OverTime

JobSatisfaction

Age

MonthlyIncome

TotalWorkingYears

✅ Key Observations

Attrition data is imbalanced, which impacts recall and F1 scores.

Logistic Regression achieves the highest F1 score among tested models.

Random Forest provides valuable insights into feature importance.

Improving minority class prediction would require techniques like SMOTE, class weighting, or threshold tuning.

🚀 Future Improvements

Handle class imbalance using resampling techniques.

Perform hyperparameter tuning using GridSearch or RandomizedSearch.

Try advanced models such as XGBoost or LightGBM.

Use ROC AUC and Precision Recall curves for deeper evaluation.

Deploy the model as a web application or dashboard.

📌 Conclusion

This project demonstrates a complete machine learning pipeline for employee attrition prediction, from data preprocessing to model evaluation and interpretation. It highlights the challenges of imbalanced classification problems and provides a solid foundation for further optimization.
