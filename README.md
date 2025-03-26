Project Overview:
This project explores how customer demographic and financial data can be used to predict whether a customer will subscribe to a term deposit. Using a dataset sourced from UCI's Machine Learning Repository and originally collected through a Portuguese bank's marketing campaigns, we aim to build predictive models that can support smarter, data-driven customer outreach.

Business Objective:
The primary goal is to assist the bank in identifying which clients are most likely to subscribe to a term deposit, so marketing efforts can be focused more effectively. By understanding which features are most predictive of subscription behavior, the bank can improve conversion rates and reduce campaign costs.

Dataset Description:
The dataset contains information on over 40,000 customers, including:

    Client demographics (age, job, marital status, education)
    Financial behavior (housing and personal loans, credit default)
    Contact-related information (contact method, campaign duration)
    Social/economic context (employment variation, consumer confidence)

The target variable is y, indicating whether the client subscribed (yes) or not (no) to the term deposit.

Data Cleaning:

    Replaced ambiguous 'unknown' entries with NaN for key features, then either dropped or re-encoded them depending on the percentage of missing data.
    Handled class imbalance using stratified splitting and class weights.
    Encoded categorical variables using OneHotEncoder.

Modeling:
Four different classification models were trained and evaluated:
   
    Logistic Regression
    K-Nearest Neighbors (KNN)
    Decision Tree Classifier
    Support Vector Machine (SVM)

Hyperparameter tuning was performed using GridSearchCV, and models were compared based on:
   
    Accuracy
    F1 Score
    ROC AUC

Key Findings

    Students, retirees, and university-educated individuals were significantly more likely to subscribe.
    Blue-collar workers, housemaids, and entrepreneurs were less likely to subscribe.
    The presence of 'unknown' values in financial features (e.g., default status) negatively affected model performance.
    The best model (based on balanced metrics) still showed challenges due to class imbalance, prompting future work in oversampling or alternative modeling approaches.

Tools Used

    Python (Pandas, NumPy, scikit-learn, seaborn, matplotlib)
    Jupyter Notebook
    GridSearchCV for hyperparameter tuning
