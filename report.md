# credit-risk-classification

## Overview of the Analysis
 * Purpose of the Analysis:

    The primary goal of this analysis is to develop machine learning models for predicting loan default risk. By leveraging logistic regression models, we aim to enhance the accuracy of identifying high-risk loans and provide insights into the financial health of borrowers.

 * Financial Information and Prediction Target:
    
    The dataset includes essential financial information such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, total debt, and loan status. The target variable, 'loan_status', indicates whether a loan is healthy (0) or has a high risk of defaulting (1).

 * Value_Counts:
    
    The primary variable we were predicting is loan_status, which represents whether a loan is healthy (0) or has a high risk of defaulting (1). Here is the distribution of loan_status in the dataset:

    * Healthy Loans (0): 75,036 instances
    * High-Risk Loans (1): 2,500 instances

    This distribution indicates a class imbalance, with a significantly larger number of healthy loans compared to high-risk loans. Addressing this imbalance is crucial for developing a robust machine learning model, and we employed resampling techniques, such as random oversampling, to handle this disparity during the analysis.

### Stages of the Machine Learning Process:
 * Data Preprocessing:

    Features were selected and labeled, and the dataset was split into training and testing sets.
    The imbalance in the target variable was addressed using resampling techniques.
 
 * Original Logistic Regression Model:

    A logistic regression model was trained on the original data to establish a baseline performance.
    
    Metrics such as balanced accuracy, precision, and recall were evaluated.
    
 * Logistic Regression Model with Oversampling:

    Random oversampling was applied to address class imbalance in the training data.
    
    A logistic regression model was trained on the oversampled data to assess performance improvements.

### Methods Used:

    Logistic regression models were employed for binary classification, specifically to predict loan default risk.

    Random oversampling using the 'RandomOverSampler' module from the imbalanced-learn library was implemented to tackle the class imbalance in the dataset.

This analysis provides a comprehensive approach to predicting loan default risk, considering both the original dataset and an oversampled version to enhance model performance, especially in identifying high-risk loans

## Results

 * Machine Learning Model 1: Original Logistic Regression
    Balanced Accuracy: 95.2%
    Precision (High-Risk Loans): 85%
    Recall (High-Risk Loans): 91%
 
 * Machine Learning Model 2: Logistic Regression with Oversampling
    Balanced Accuracy: 99.4%
    Precision (High-Risk Loans): 84%
    Recall (High-Risk Loans): 99%

 * Model 1 (Original Logistic Regression):
    Achieves a balanced accuracy of 95.2%, indicating overall good predictive performance.
    High precision (85%) for identifying high-risk loans, emphasizing low false-positive rates.
    High recall (91%) for high-risk loans, indicating effective identification of true positives.

 * Model 2 (Logistic Regression with Oversampling):
    Demonstrates outstanding performance with a balanced accuracy of 99.4% after addressing class imbalance through random oversampling.
    Maintains a solid precision (84%) for high-risk loans, balancing false positives and true positives effectively.
    Remarkable recall (99%) for high-risk loans, minimizing false negatives and capturing a significant proportion of actual high-risk instances.

 The results suggest that Model 2, trained on oversampled data, outperforms Model 1, indicating its effectiveness in identifying high-risk loans while maintaining a high level of overall accuracy.

## Summary
    The logistic regression model with oversampling demonstrates superior performance with a balanced accuracy of 99.4%, excelling in both precision (84%) and recall (99%) for high-risk loans. While the original logistic regression model performed well, the oversampled model showcases improved sensitivity, crucial for identifying high-risk loans. The choice of the model may depend on the specific business objective. If minimizing the risk of missing high-risk loans is paramount, the logistic regression model with oversampling is recommended. However, further consideration should be given based on business priorities and the associated costs of false positives and false negatives