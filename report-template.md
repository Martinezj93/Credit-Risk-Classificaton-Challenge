# Module 12 Report Template

## Overview of the Analysis

* The objective of this analysis is to construct a regression model capable of assessing the creditworthiness of borrowers.
* The dataset used for this analysis comprises historical lending data obtained from a peer-to-peer lending services company. 
* The analysis focuses on determining the loan status, categorizing it as either healthy or at risk, which serves as the dependent variable (y value).
* The independent variables (x values) encompass loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, and derogatory marks.
* The analysis process involves several steps. Initially, the dataset is divided into training and test sets. Next, the dependent and independent variables are defined. A logistic regression model is then created and trained using the original dataset. This trained model is subsequently utilized for making predictions. Lastly, the performance of the model is evaluated.
* Two distinct logistic regression models are developed. The first model employs the original dataset, while the second model utilizes a randomly oversampled dataset to mitigate imbalances. The results of both models are compared using the scikit-learn library to assess their respective performances.

## Results

* Machine Learning Model 1:

   * Precision: For the "Healthy Loan" class (label 0), the precision is 1.00, which means that all the instances predicted as "Healthy Loan" are indeed true. For the "High-Risk Loan" class (label 1), the precision is 0.87, indicating that 87% of the instances predicted as "High-Risk Loan" are true positives.

  * Recall: For the "Healthy Loan" class (label 0), the recall is 1.00, meaning that the model correctly identifies all instances of "Healthy Loan." For the "High-Risk Loan" class (label 1), the recall is 0.89, indicating that the model captures 89% of the actual "High-Risk Loan" instances.

  * Accuracy: Accuracy measures the overall correctness of the model's predictions. In this case, the accuracy is 0.99, which means that the model correctly predicts the label for 99% of the instances in the dataset.

  Overall, the logistic regression model appears to perform very well in predicting both the "Healthy Loan" (label 0) and "High-Risk Loan" (label 1) classes. It achieves a high precision, recall, and F1-score for the "Healthy Loan" class, indicating accurate predictions and capture of all instances. For the "High-Risk Loan" class, the model has a slightly lower precision, recall, and F1-score but still performs well, capturing a high percentage of actual high-risk loans while maintaining a good balance between precision and recall. The overall accuracy of the model is 99%, indicating a high level of correctness in its predictions.

* Machine Learning Model 2:

  * Precision: For the "Healthy Loan" class (0), the precision is 1.00, indicating that all the predicted healthy loans are correct. For the "High-Risk Loan" class (1), the precision is 0.87, suggesting that 87% of the predicted high-risk loans are correct.

  * Recall: For the "Healthy Loan" class (0), the recall is 1.00, indicating that all the healthy loans are correctly identified. For the "High-Risk Loan" class (1), the recall is 1.00, meaning that all the high-risk loans are correctly identified.

  * Accuracy: Accuracy is the overall proportion of correctly classified instances. In this case, the accuracy is 1.00, meaning that the logistic regression model accurately predicts both the "Healthy Loan" and "High-Risk Loan" labels.

  Overall, the logistic regression model demonstrates excellent performance in predicting both the "Healthy Loan" (0) and "High-Risk Loan" (1) labels. It achieves high precision, recall, and F1-score for both classes, indicating that it effectively distinguishes between healthy and high-risk loans. The overall accuracy of 1.00 further confirms the model's capability to make accurate predictions.

## Summary

The analysis compares the performance of two logistic regression models: one trained on the original dataset and the other trained on a randomly oversampled dataset. The results suggest the following:

For the "Healthy Loan" class (0), both models exhibit exceptional performance. They achieve a precision, recall, and F1-score of 1.00, indicating that all healthy loans are correctly identified.

For the "High-Risk Loan" class (1), the model trained on the original dataset achieves a precision of 0.87, recall of 1.00, and an F1-score of 0.93. The oversampled model also attains a recall of 1.00, indicating that all high-risk loans are correctly identified.

Considering these findings, it appears that the model trained on the original dataset performs better in terms of precision for the high-risk loans, while both models exhibit excellent performance for healthy loans.

The choice of the model to use depends on the specific problem and priorities. If the emphasis is on correctly identifying high-risk loans (class 1), the model trained on the original dataset could be preferred. On the other hand, if equal importance is placed on predicting both healthy (class 0) and high-risk loans, both models perform well, and either could be suitable.
