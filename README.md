# **HR Analytics - Employee Attrition & Performance**

## **Introduction**
This project aims to predict employee attrition using various machine learning models. The dataset includes features such as employee demographics, job satisfaction, and performance metrics. The goal is to help HR professionals identify employees at risk of leaving and take proactive measures to improve retention.

## **Data Collection**
The dataset used in this project is sourced from [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset). It contains detailed employee information, including:
- **Employee Demographics**: Age, gender, marital status
- **Job-Related Data**: Job satisfaction, performance rating, job role
- **Work Environment**: Workload, benefits, work-life balance
- **Company Performance**: Business unit, revenue contribution

## **Objective**
- The main objective of this project is to predict employee attrition based on various employee characteristics. 
- By applying machine learning techniques, we aim to identify the primary factors leading to employee turnover and predict future attrition.

## **Methodology**

### **EDA (Exploratory Data Analysis)**
- Performed EDA to understand the dataset and uncover hidden patterns:
- Analyzed feature distributions (e.g., age, job satisfaction, tenure).
- Identified and handled missing values.
- Visualized feature correlations with attrition using heatmaps and bar plots.

### **Feature Engineering**
To improve model performance, I applied the following feature engineering techniques:
- Encoding Categorical Features: Converted categorical variables (e.g., job role, department) into numerical values using one-hot encoding and label encoding.\
- Scaling Numerical Features: Applied MinMaxScaler to normalize numerical features.
- Handling Class Imbalance: Used **SMOTE** (Synthetic Minority Over-sampling Technique) to generate synthetic examples for the minority class (employees who left).

### **Model Selection**
 - Trained a logistic regression model on the preprocessed data.
 - While the model performed well on the majority class, it struggled with the minority class (employees at risk of leaving).
 - Adjusted the decision threshold, which resulted in an improvement in recall for the minority class

## **Model Evaluation**
Model performance was evaluated using:
- **Accuracy**: To measure the proportion of correct predictions.
- **Precision, Recall, F1-Score**: To assess model effectiveness in predicting attrition (positive class).

## Challenges & Learnings
Challenges:
- Class Imbalance: The dataset had significantly fewer attrition cases compared to retained employees, leading to biased predictions.
- Feature Selection: Some features had low correlation with attrition and were removed for better performance.

Key Learnings:
- SMOTE effectively balances datasets by creating synthetic minority class samples.
- Threshold tuning can significantly improve recall for imbalanced datasets.
- Feature scaling is crucial for models like logistic regression

## Next Steps / Future Improvements

- Experiment with other machine learning models, such as **decision trees** or **random forests**, to compare performance and select the best model.
- Fine-tune hyperparameters for better generalization.
