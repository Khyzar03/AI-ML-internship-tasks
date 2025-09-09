End-to-End ML Pipeline for Customer Churn Prediction

Objective of the Task

The objective of this task was to design and implement a production-ready machine learning pipeline using the Scikit-learn Pipeline API for predicting customer churn. The pipeline should include all essential steps: preprocessing, model training, hyperparameter tuning, and exporting the final pipeline for reusability in production environments.

Methodology / Approach

Dataset
Used the Telco Customer Churn Dataset.

Target variable: Churn (Yes → 1, No → 0).

Removed irrelevant column (customerID).

Data Preprocessing
Identified categorical and numerical features.
Applied StandardScaler to numerical features.
Applied OneHotEncoder to categorical features using ColumnTransformer.
Pipeline Construction
Built separate pipelines for Logistic Regression and Random Forest classifiers.
Each pipeline combined preprocessing and classification in a single reusable object.
Hyperparameter Tuning
Used GridSearchCV with 5-fold cross-validation.
Tuned key parameters such as:
Logistic Regression: C, solver, penalty

Random Forest: n_estimators, max_depth, min_samples_split


Model Evaluation
Evaluated models on the test set using accuracy and classification report (precision, recall, F1-score).
Compared Logistic Regression and Random Forest to identify the best-performing model.


Model Export
Saved the best pipeline (preprocessing + classifier) using Joblib for future deployment.


Key Results or Observations
Logistic Regression achieved a good baseline performance with relatively fast training time.
Random Forest generally outperformed Logistic Regression in terms of accuracy and F1-score, showing better capability in handling non-linear relationships and feature interactions.
The pipeline structure ensured that preprocessing and model training were integrated seamlessly, reducing the risk of data leakage.
The best model (Random Forest in this case) was successfully saved as a .joblib file (churn_prediction_pipeline.joblib), making it directly reusable in production without retraining.


Conclusion
The task successfully demonstrated how to build an end-to-end ML pipeline using Scikit-learn. By combining preprocessing, model training, hyperparameter tuning, and model export into one pipeline, the solution ensures reproducibility, scalability, and production-readiness. This approach can be extended to other classification tasks beyond churn prediction.