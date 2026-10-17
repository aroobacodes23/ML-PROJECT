Project Proposal — Customer Churn Prediction

1- Problem statement:
Customer churn occurs when a customer stops using a service. This project will explore customer information and prepare a machine-learning workflow to predict whether a customer will churn.

2- Dataset:
The project uses customer_churn_1000.csv, containing 1,000 rows and 12 columns. It includes numeric fields (such as Age, Tenure, Support Calls, Payment Delay and Total Spend) and categorical fields (Gender, Subscription Type and Contract Length). The dataset has no missing values in the supplied 1,000 rows.

3- Prediction target and task:
* Target: Churn (0 = no churn, 1 = churn, based on the dataset's coding).
* Task type: Binary classification.
* Proposed primary success metric: F1-score, because it balances precision and recall and can be informative if the churn classes are not perfectly balanced. Accuracy and class distribution will also be reported.

4- Preparation plan
CustomerID will be excluded from model features because it is an identifier rather than a meaningful customer behaviour feature. A stratified train/test split will be used. Numeric features will be imputed with the median and scaled; categorical features will be imputed with the most frequent value and one-hot encoded. These transformations will be fitted only on training data through a scikit-learn Pipeline and ColumnTransformer to avoid data leakage.

5- Outliers, imbalance and limitations
Potential numeric outliers will be identified using the IQR rule and reviewed rather than automatically deleted, since unusual customer behaviour may be valid. The target distribution will be checked for class imbalance. Dataset provenance and licensing should be verified with the instructor before submission; they are not specified by the supplied CSV alone.