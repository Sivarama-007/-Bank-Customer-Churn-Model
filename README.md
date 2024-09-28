# Bank Customer Churn Prediction
# Overview:
This project was completed as part of the YBI Foundation Data Science with Python internship, focusing on predicting customer churn in a bank using various machine learning techniques.

# Learning Objectives:
Data Encoding: Employed techniques like one-hot encoding to transform categorical variables into a format suitable for machine learning models.

Feature Scaling: Implemented scaling methods such as Min-Max scaling and standardization to normalize numerical features, ensuring optimal model performance.

Handling Imbalanced Data:

Random Under Sampling: Addressed class imbalance by randomly reducing the number of instances in the majority class.
Random Over Sampling: Balanced the dataset by duplicating instances from the minority class using random sampling techniques.
## Objective
The primary objective of this project is to predict whether a bank customer will churn (leave the bank) based on various demographic, financial, and behavioral data. This helps the bank take proactive measures to retain valuable customers.

## Data Source
Bank Churn Modelling CSV
The dataset used for this project contains customer information such as:
- Credit score
- Geography
- Gender
- Age
- Tenure
- Balance
- Number of products
- Has credit card or not
- Is active member or not
- Estimated salary
- Churn status (target variable)

The dataset includes both churned and non-churned customers. 
dataset

## Project Workflow
### 1. Data Import and Exploration
We begin by importing and exploring the dataset to understand the distribution of key variables and check for any missing or inconsistent data.

### 2. Data Visualization
Visualizations were created to analyze the relationship between variables, such as:
- Churn rate based on geography
- Impact of credit score and balance on customer churn
- Distribution of active members vs. non-active members

### 3. Data Preprocessing
To prepare the data for modeling, several preprocessing steps were applied:
- Handling missing values (if any)
- Encoding categorical variables (e.g., `Geography`, `Gender`)
- Normalizing numerical variables
- Addressing class imbalance using Random Undersampling and Oversampling techniques

### 4. Model Training
The following models were trained to predict customer churn:
- **Support Vector Classifier (SVC)** 
- **Random Forest Classifier**
- **Logistic Regression**
  
Each model was evaluated using **Random Undersampling** and **Random Oversampling** techniques to address class imbalance. Hyperparameter tuning was also performed for optimal performance.

### 5. Model Evaluation
The models were evaluated based on precision, recall, F1-score, and accuracy. Below are some key evaluation metrics:

#### Baseline Model (Without Sampling):
| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.85      | 0.99   | 0.91     | 2414    |
| 1     | 0.82      | 0.26   | 0.39     | 586     |

#### After Random Undersampling:
| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.73      | 0.75   | 0.74     | 627     |
| 1     | 0.73      | 0.71   | 0.72     | 596     |

#### After Random Oversampling:
| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.97      | 0.86   | 0.91     | 2379    |
| 1     | 0.88      | 0.97   | 0.92     | 2399    |

**Final Model Results After Hyperparameter Tuning:**
- **Accuracy**: 80%
- **Precision (Churn)**: 0.49
- **Recall (Churn)**: 0.41
- **F1-Score (Churn)**: 0.45

### 6. Prediction
The final model was used to predict churn on unseen test data, providing the probability of customer churn for each instance.

## Conclusion
Through this project, we successfully built a model to predict bank customer churn. The model helps to identify customers who are likely to churn, enabling the bank to take proactive actions. With further hyperparameter tuning and feature engineering, the model's performance could be further improved, especially for predicting the minority class (churned customers).

## Setup Instructions
To run this project on your local machine:
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Bank-Customer-Churn-Model.git


