# Data-Analysis-in-Fraud-Detection-
🏦 Fraud Detection Analysis - InterUni Datathon 2024 This repository contains the solution and code developed for the InterUni Datathon 2024 hosted by Skyline Financial Services. The project focuses on building a machine learning model to detect fraudulent users and identifying the key drivers behind fraudulent behavior to minimize revenue loss.

🏆 Achievement: Achieved 97% accuracy on the test dataset.

📖 Project Overview
Skyline Financial Services faced a significant dip in revenue due to undetected fraudulent activity. The goal of this project was to analyze transactional and demographic data to:

Detect Fraud: Build a robust predictive model to identify fraudulent transactions in real-time.

Explain Drivers: Uncover the root causes and behavioral patterns associated with fraud.

Prevent Future Loss: Provide actionable insights for risk management strategies.

🛠️ Tech Stack & Skills Demonstrated
Languages: Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn)

Data Processing:

Feature Engineering:

Geospatial Analysis: Mapped coordinates (Lat/Lon) to cities and created a LocationMatch feature to detect location spoofing/mismatches.

Time Analysis: Converted transaction times (e.g., "14:30:00") into numerical values (seconds) to help the model detect patterns, such as whether fraud occurs more often at specific times of the day.

Text Cleaning: Processed Currency columns (removing symbols) and standardized categorical data (e.g., DeviceType, TransactionLocation).

Handling Imbalanced Data: Addressed the class imbalance (Fraud vs. Non-Fraud) inherent in financial datasets.

Machine Learning Models:

Logistic Regression

K-Nearest Neighbors (KNN)

Support Vector Classifier (SVC)

Random Forest Classifier (Best Performing Model)

Gradient Boosting Classifier

Model Evaluation: Optimized for F1-Score due to the imbalanced nature of fraud data.

📊 Key Insights & Feature Engineering
During the exploratory data analysis (EDA) and feature engineering phase, several key patterns emerged:

Withdrawals are High Risk: Withdrawal transaction types accounted for the vast majority of fraud cases compared to payments or transfers.

Location Mismatches: A custom feature LocationMatch was created to verify if the user's registered location matched the transaction location. Mismatches were highly correlated with fraud.

Temporal Patterns: Fraudulent activity showed distinct patterns related to the time of transaction (TransactionTime).

🚀 Methodology
Data Cleaning: * Cleaned inconsistent data in Age (e.g., negative ages) and Gender.

Standardized city names (e.g., "Mel", "MLB" -> "Melbourne").

Converted currency strings to float values.

Feature Selection:

Calculated correlation matrices to identify the most predictive features.

Selected top 7 features: TransactionTime, TransactionType, TransactionAmount, TransactionLocation, TransactionMonth, LocationMatch, NumDependents.

Model Training & Selection:

Tested multiple algorithms including Logistic Regression, KNN, and SVC.

Random Forest proved to be the superior model, balancing bias and variance effectively for this dataset.

Hyperparameter tuning was performed to optimize n_estimators, max_depth, and split criteria.

🏆 Results

Best Model: Random Forest Classifier 

Test Accuracy: 97%

Correlation between the fraud and other features: TransactionTime (-0.49) and TransactionType (0.45) show the strongest correlations, indicating that when a transaction occurs and its method (e.g., withdrawals) are the top indicators of fraud.


Key Metric: High F1-Score indicating a strong balance between Precision and Recall, crucial for minimizing false positives in fraud detection. 

📂 Repository Structure
├── FinalVersion_Datathon (FINAL).ipynb/             # Jupyter Notebooks for EDA and Modeling
└── README.md              # Project documentation


🤝 Collaboration
This project was a collaborative effort.


Collaboration
This project was a collaborative effort where we split tasks to maximize efficiency. My primary contributions included:

Data Cleaning Strategy: I write the logic to identify and remove duplicates and filter out outliers (e.g., negative ages, extreme values) to ensure a clean dataset for the team.

Model Development: I led the model testing phase, evaluating various algorithms (Logistic Regression, KNN, SVC) and identifying Random Forest as the optimal solution for this specific dataset.

Model Optimization: Tuned hyperparameters to achieve the 97% accuracy benchmark.

Feature Engineering: Developed the geospatial logic to correlate transaction locations with user home locations.

Data Cleaning: Collaborated with team members to standardize "dirty" categorical variables (e.g., inconsistent city names and device types).

Note: This project was submitted as part of the InterUni Datathon 2024.
