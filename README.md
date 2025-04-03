# Employee Attrition Prediction

## Project Summary

This project aims to predict employee attrition using a logistic regression model. The dataset contains various employee attributes which are used to predict whether an employee will leave the company.

## Data Preprocessing

I performed several data preprocessing steps to prepare the dataset for modeling:

- **Encoding Categorical Features:** Categorical variables were encoded to numerical values using techniques like label encoder.
- **Handling Missing Data:** Any missing values in the dataset were imputed or removed based on the situation.
- **Scaling Numerical Features:** I used feature scaling to normalize the numerical features for model training.
- **Class Imbalance:** The dataset exhibited a class imbalance, with fewer employees leaving the company compared to those who stayed. To address this, I applied **SMOTE (Synthetic Minority Over-sampling Technique)** to generate synthetic examples of the minority class.

## Modeling

I trained a logistic regression model on the preprocessed data. The model was evaluated using the following metrics:

- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**

While the model performed well on the majority class, it struggled with the minority class (employees at risk of leaving). To address this, I adjusted the decision threshold, which resulted in an improvement in recall for the minority class (increased to 0.46).

## Challenges & Learnings

The main challenge encountered was handling the **class imbalance**, a common issue in real-world datasets. However, by applying techniques like **SMOTE** and adjusting the **decision threshold**, I was able to improve the model's performance on the minority class.

Key learnings:
- **SMOTE** can be useful in handling class imbalance by creating synthetic samples for the minority class.
- **Threshold adjustment** is an effective way to improve recall, especially when predicting the minority class.

## Next Steps / Future Improvements

- Experiment with other machine learning models, such as **decision trees** or **random forests**, to compare performance and select the best model.
- Fine
