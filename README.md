# Loan Risk Prediction Model - README

## Overview of the Analysis
This project involves a dataset provided by a bank, containing information on 77,536 loans, pre-classified as Healthy (0) or High-Risk (1). Notably, the dataset comprises 75,036 healthy loans and 2,500 high-risk ones, indicating a significant imbalance that could impact model performance.

Key features used for predictions include:
- Loan Size
- Interest Rate
- Borrower's Income
- Debt to Income Ratio
- Number of Accounts
- Derogatory Marks
- Total Debt

The goal is to predict whether a loan is low-risk or high-risk using these features. We employed a linear regression model, dividing the main dataset into training (75%) and testing (25%) segments. Feature scaling was applied to enhance accuracy due to varying numerical magnitudes across features.

## Results
The training and testing models performed similarly, suggesting good generalization and effectiveness in handling new/ unseen data. The imbalance in the dataset did not significantly impact performance, possibly due to data standardization in preprocessing.

**Training Model Performance:**
- Precision: Healthy Loans (1.00), High-Risk Loans (0.86)
- Recall: Healthy Loans (0.99), High-Risk Loans (0.98)
- Accuracy: 0.99
- F1-Score, Macro Avg, Weighted Avg also provided

**Testing Model Performance:**
- Precision: Healthy Loans (1.00), High-Risk Loans (0.84)
- Recall: Healthy Loans (0.99), High-Risk Loans (0.98)
- Accuracy: 0.99
- F1-Score, Macro Avg, Weighted Avg also provided

Both models showed high recall for high-risk loans, detecting 98% of them. Precision for high-risk loans was 86% in training and 84% in testing, indicating that 12-16% of loans labeled as high-risk were actually healthy.

## Summary
The evaluation of our machine learning models for predicting loan risk demonstrates promising but nuanced results. The models display impressive accuracy, precision, and recall in both training and testing, with particularly strong performance in identifying high-risk loans. However, a deeper analysis suggests a need for caution in the practical application of these models.

**Model Performance**
*High Recall:* Both models exhibit a high recall rate for high-risk loans (98%), indicating their effectiveness in identifying most of the high-risk loans. This feature of the model is crucial in minimizing potential defaults.
*Precision Concerns:* The precision of the model, while good, indicates room for improvement. With a precision of 86% for training and 84% for testing, there's a significant probability (14-16%) that healthy loans could be misclassified as high-risk.

**Recommendations**

*Conditional Adoption with Supplementary Measures:* While the model's ability to identify high-risk loans makes it a valuable tool, its adoption should come with supplementary measures. Due to the potential for misclassifying healthy loans as high-risk, additional review processes for loans flagged as high-risk by the model are advisable.
*Importance of Reducing False Positives:* Efforts should be directed towards improving the model's precision to reduce the rate of false positives. This could involve further tuning of the model, exploring alternative modeling techniques, or implementing a secondary review mechanism for loans identified as high-risk.
*Aligning with Business Risk Strategy:* The decision to prioritize either recall or precision should align with the bank's risk tolerance and operational capacity. If the implications of falsely identifying a loan as high-risk are significant, a balanced approach or a more conservative model might be warranted.

**Final Thoughts**

While the model shows a strong ability to identify high-risk loans, its adoption should be approached with caution due to the risk of misclassification. Continual monitoring and refinement of the model are essential to ensure its effectiveness and alignment with the bank's risk management goals. The recommendation includes a dual approach: leveraging the model's strengths while actively mitigating its limitations through additional checks or model adjustments. 
