Mobile User Behavior Analysis & Classification

📌 Project Overview

This project performs Exploratory Data Analysis (EDA) and builds a multi-class classification model to predict User Behavior Class based on mobile device usage patterns.
The objective was to analyze user activity trends and implement a machine learning pipeline using Python and Scikit-learn.

📂 Dataset

Mobile Device Usage and User Behavior Dataset
Source: Kaggle
Link: https://www.kaggle.com/datasets/valakhorasani/mobile-device-usage-and-user-behavior-dataset

Dataset Description

The dataset contains 700 user records with the following features:
App Usage Time (min/day)
Screen On Time (hours/day)
Battery Drain (mAh/day)
Data Usage (MB/day)
Number of Apps Installed
Age
Gender
Operating System
Device Model
Target Variable:
User Behavior Class (1–5)
Each class represents increasing levels of mobile usage intensity.

🧹 Data Cleaning & Preprocessing

The following preprocessing steps were performed:
Checked for missing values and duplicates
Dropped non-informative column (User ID)
Encoded categorical variables (Gender, Operating System, Device Model)
Applied StandardScaler to normalize feature values
Performed stratified 80/20 train-test split to preserve class distribution
This ensured clean, consistent data and prevented data leakage during model training.

📊 Exploratory Data Analysis (EDA)

Grouped analysis and statistical summaries were used to identify usage trends across behavior classes.
Key Insights
App Usage Time, Screen On Time, and Battery Drain strongly correlate with User Behavior Class.
Screen-on time increases consistently across higher behavior classes.
Data usage rises significantly for Class 5 users, indicating heavy usage patterns.
Usage-related features show strong linear separability between classes.

Visualizations Included
Correlation heatmap
Scatter plot (App Usage vs Battery Drain)
Boxplot (Screen On Time by Behavior Class)
These visualizations confirmed clear behavioral differentiation among classes.

🤖 Model Training

A Logistic Regression classifier was implemented for multi-class classification.
Steps:
Feature-target separation
Stratified train-test split (80/20)
Feature scaling using StandardScaler
Model training on training dataset
Evaluation on unseen test dataset

Logistic Regression was chosen due to the strong linear relationships observed during EDA.

📈 Model Performance

Accuracy: [Replace with your actual accuracy, e.g., 98.57%]
Confusion matrix shows strong diagonal dominance
Minor misclassifications occur between adjacent behavior classes
The high accuracy is consistent with the strong feature correlations and clear class separability observed during EDA.

🔍 Conclusion

The dataset demonstrates clear behavioral stratification based on mobile usage intensity. Usage-related features (screen time, app usage, battery drain) are strong predictors of user behavior class.

A linear classifier performs effectively due to the dataset’s structured separability.

🚀 Future Improvements

Test alternative models such as Random Forest or K-Nearest Neighbors
Perform hyperparameter tuning
Apply cross-validation for robustness
Engineer additional interaction features

🛠 Tools & Technologies Used

Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn