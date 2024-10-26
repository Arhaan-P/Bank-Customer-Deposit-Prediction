# Bank Customer Deposit Prediction

This repository contains a data science project focused on predicting whether a bank customer will make a term deposit based on key demographic and financial features. This project was part of **Data Quest 2024**, a data science competition held at **VIT Chennai**. Leveraging machine learning, this project identifies patterns in customer behavior, helping optimize marketing strategies for future campaigns.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Modeling and Evaluation](#modeling-and-evaluation)
- [Results](#results)
- [Conclusion](#conclusion)
- [Future Enhancements](#future-enhancements)

## Project Overview

Predicting customer deposits is crucial for banks to tailor marketing campaigns, allocate resources efficiently, and enhance customer engagement. This project applies machine learning techniques to predict deposit likelihood and understand key influencing factors, offering actionable insights for customer segmentation.

## Dataset

The dataset (`bank.csv`) includes 17 columns with customer demographic and financial attributes:

| Column       | Description                                |
|--------------|--------------------------------------------|
| **age**      | Customer's age                             |
| **job**      | Job type                                   |
| **marital**  | Marital status                             |
| **education**| Education level                            |
| **default**  | Has credit in default? (yes/no)            |
| **balance**  | Average yearly balance (in euros)          |
| **housing**  | Has a housing loan? (yes/no)               |
| **loan**     | Has a personal loan? (yes/no)              |
| **contact**  | Contact communication type                 |
| **day**      | Last contact day                           |
| **month**    | Last contact month                         |
| **duration** | Last contact duration (seconds)            |
| **campaign** | Contacts during current campaign           |
| **pdays**    | Days since last campaign contact           |
| **previous** | Previous contacts before campaign          |
| **poutcome** | Outcome of the previous campaign           |
| **deposit**  | Target variable: deposit made (yes/no)     |

## Data Preprocessing

- **Encoding**: Transformed categorical variables using label encoding and one-hot encoding.
- **Scaling**: Scaled numerical features for consistent model performance.
- **Class Imbalance**: Addressed imbalance in the target variable to improve model robustness.

## Exploratory Data Analysis

Through visualizations and statistical summaries, we explored correlations, distributions, and trends across features. This analysis helped uncover patterns, such as the impact of account balance, job type, and previous campaign outcomes on deposit decisions.

## Modeling and Evaluation

We evaluated several classification models, including Logistic Regression, Decision Trees, and Random Forests. The XGBoost model delivered the best performance with:

- **Training Accuracy**: 95.68%
- **Testing Accuracy**: 84.90%
- **F1 Score**: 0.85

### Key Metrics:

| Model              | Training Accuracy | Testing Accuracy | F1 Score |
|--------------------|-------------------|------------------|----------|
| **XGBoost**        | 95.68%            | 84.90%          | 0.85     |

## Results

The XGBoost model performed robustly, achieving an F1 score of 0.85 on the test set. This score reflects a well-balanced approach to identifying both deposit-making and non-deposit-making customers accurately.

## Conclusion

The project demonstrates the power of machine learning in predicting customer deposit behavior, providing valuable insights for campaign management. By leveraging features like customer balance, contact type, and previous campaign results, banks can better target potential depositors.

## Future Enhancements

- **Hyperparameter Tuning**: Optimize XGBoost and explore alternative parameter settings.
- **Additional Features**: Experiment with derived or engineered features for better prediction accuracy.
- **Deployment**: Develop a web app or API to facilitate easy predictions for new data.
