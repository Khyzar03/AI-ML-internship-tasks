Task Objective
Use the UCI Heart Disease dataset to make a binary assessment of a person's heart disease risk.



Utilized Dataset
Kaggle's Heart Condition  Age, sex, kind of chest pain, cholesterol, fasting blood sugar, exercise-induced angina, ST depression, slope, CA, thal, and so on are typical columns in the UCI dataset.  Goal: goal (1 denotes illness, 0 denotes no illness).


Models Used

Scaling and one-hot encoding in logistic regression (pipeline).
To prevent overfitting, use a decision tree with a moderate depth.

Key Findings & Results

Use the printouts to report the accuracy and ROC-AUC (for example, "LogReg: Acc=0.85, AUC=0.90; Tree: Acc=0.83, AUC=0.87"—your figures will differ).
The balance of TPs, FPs, and FNs is displayed in the confusion matrix.
The model with a higher AUC typically performs better overall, according to the ROC Curve, which visually compares the two models.
The following are common top features: thal/slope, exercise-induced angina (exang), ST depression (oldpeak), maximal heart rate (thalach), and type of chest pain (cp).  The features that were most important to you during your run are displayed in your feature-importance tables.