# Credit Risk Analysis Report

# Overview of the Analysis

In this analysis, I built and evaluated a logistic regression model to predict the credit risk associated with loans based on historical lending data. The primary purpose of the analysis was to assess the ability of the model to classify loans as either **healthy (0)** or **high-risk (1)**, based on the available features in the dataset.

The dataset provided financial information from a peer-to-peer lending platform, where each loan was labeled as either a **healthy loan** (loan_status = 0) or **high-risk loan** (loan_status = 1). My goal was to predict the **loan_status** for new loan applicants.

The main variables used for prediction were various borrower and loan attributes, which could include features like income, credit score, loan amount, term, etc. After preparing the data by reading the file and splitting it into **training** and **testing** sets, I trained the logistic regression model using the training set and evaluated it on the testing set.

The machine learning process included:
1. **Data Preprocessing**: I cleaned the data, created feature and label sets, and split the data into training and testing subsets.
2. **Model Training**: I trained a **logistic regression** model using the training data.
3. **Model Evaluation**: I used **confusion matrix**, **classification report**, and metrics like **accuracy**, **precision**, and **recall** to assess model performance.
4. **Model Interpretation**: I interpreted the model's ability to predict both healthy and high-risk loans.

I used **LogisticRegression** for this challenge, which is a classification algorithm suitable for binary classification problems like this one.

---

# Results

* **Logistic Regression Model**:
    - **Accuracy**: **99%**  
    The model correctly predicted the loan status for 99% of the samples, which shows it performs well overall.
    
    - **Precision (Class 0 - Healthy Loan)**: **1.00**  
    The model perfectly predicted healthy loans when it classified a loan as healthy.
    
    - **Recall (Class 0 - Healthy Loan)**: **0.99**  
    The model successfully identified 99% of the healthy loans from the total healthy loans in the dataset.
    
    - **Precision (Class 1 - High-Risk Loan)**: **0.84**  
    When the model predicted a loan as high-risk, it was correct 84% of the time.
    
    - **Recall (Class 1 - High-Risk Loan)**: **0.94**  
    The model identified 94% of the high-risk loans correctly, which is strong but leaves room for improvement.
    
    - **F1-Score (Class 1)**: **0.89**  
    The F1-score reflects a balanced trade-off between precision and recall for high-risk loans.

---

# Summary

The **logistic regression model** demonstrated **high overall accuracy (99%)** and strong recall for both healthy loans (0.99) and high-risk loans (0.94). Precision was exceptionally high for healthy loans (1.00), but slightly lower for high-risk loans (0.84), indicating room for improvement in minimizing **false positives** (i.e., healthy loans misclassified as high-risk).

In terms of performance:
- The model performs best in predicting healthy loans with both high precision and recall.
- However, the model could still be optimized to improve the precision for high-risk loans, as it sometimes misclassifies healthy loans as high-risk, leading to **false positives**.

### **Recommendation**:
Given the high accuracy and strong recall for high-risk loans, I recommend using this **logistic regression model** for loan risk prediction, with the suggestion to further fine-tune the model to improve its precision for high-risk loans. Future improvements could include adjusting the decision threshold or exploring alternative models to see if performance can be enhanced further. 

