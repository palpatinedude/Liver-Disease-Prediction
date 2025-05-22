Liver Disease Classification Using Machine Learning
===================================================

Overview
--------
This project analyzes the Indian Liver Patient Dataset (ILPD) using machine learning classifiers to predict whether a patient has a liver disease or not. It implements:
- Naive Bayes
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)

The project includes:
- Preprocessing
- Model training and evaluation
- Hyperparameter tuning
- Statistical testing (t-test)
- Feature selection
- Performance comparison

Dataset
-------
Source: Indian Liver Patient Dataset (ILPD)

Attributes:
- age, sex, d1 to d8: Patient demographic and medical information
- healthyornotliver: Target class (1 = Liver disease, 2 = No liver disease)

Features
--------
- Data Preprocessing:
  - Column renaming and label encoding (e.g., sex → numerical)
  - Handling missing values using column-wise means
  - Normalization using MinMaxScaler (range [-1, 1])

- Classifier Training:
  - Gaussian Naive Bayes
  - K-Nearest Neighbors (with hyperparameter tuning)
  - Support Vector Machine (C and gamma optimization)

- Model Evaluation:
  - Accuracy
  - Precision
  - Recall (Sensitivity)
  - Specificity
  - Geometric Mean
  - Confusion Matrix
  - Classification Report
  - Execution Time
  - 5-Fold Cross-Validation

- Model Comparison:
  - Evaluation based on metrics and execution time
  - Reports best-performing and fastest model

- Hyperparameter Tuning:
  - SVM: Linear search for optimal C and gamma
  - KNN: Optimal K based on best training accuracy

- Feature Importance:
  - t-tests for feature significance
  - Irrelevant features dropped based on p-values
  - Retraining and evaluation with reduced feature set

Dependencies
------------
Ensure the following Python packages are installed:

    pip install pandas numpy scikit-learn matplotlib researchpy scikit-learn-intelex

How to Run
----------
1. Make sure the dataset `Indian Liver Patient Dataset (ILPD).csv` is present in the same directory.
2. Run the script:

    python healthy_liver_prediction.py


Notes
-----
- The script handles preprocessing and normalization automatically.
- The evaluation uses both holdout and cross-validation methods.
- Final model performance is based on reduced feature set using statistical testing.

