Mobile User Behavior Analysis & Classification
📌 Project Overview

This project performs Exploratory Data Analysis (EDA) and builds a multi-class classification model to predict User Behavior Class based on mobile device usage patterns.

The objective was to analyze user behavior trends and implement a structured machine learning pipeline using Python and Scikit-learn.

📂 Dataset

Mobile Device Usage and User Behavior Dataset
Source: Kaggle
https://www.kaggle.com/datasets/valakhorasani/mobile-device-usage-and-user-behavior-dataset

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
User Behavior Class (1–5), representing increasing levels of mobile usage intensity.

🧹 Data Cleaning & Preprocessing

The following preprocessing steps were performed:

Checked for missing values and duplicate records
Removed non-informative column (User ID)
Encoded categorical variables (Gender, Operating System, Device Model)
Applied StandardScaler to normalize feature magnitudes
Used stratified 80/20 train-test split to preserve class balance
These steps ensured clean data and prevented data leakage during model training.

📊 Exploratory Data Analysis

Grouped analysis and statistical summaries were performed to identify behavioral patterns across user classes.

Key Insights

App Usage Time, Screen On Time, and Battery Drain show strong positive correlation with User Behavior Class.
Screen-on time increases consistently across higher behavior classes
Data usage rises significantly for heavy users (Class 5).
Usage-related features demonstrate strong linear separability between classes.

Visualizations Included
Correlation heatmap
Scatter plot (App Usage vs Battery Drain)
Boxplot (Screen On Time by Behavior Class)
Barplot

These visualizations confirm clear behavioral segmentation based on usage intensity.

🤖 Model Implementation

Model Used: Logistic Regression (multi-class classification)

Implementation Steps

Feature-target separation
Stratified train-test split (80/20)
Feature scaling using StandardScaler
Model training on training dataset
Evaluation on unseen test dataset
Logistic Regression was selected due to the strong linear relationships observed during EDA.

📈 Model Performance

Accuracy: 100.00% 

The confusion matrix shows strong diagonal dominance, indicating high prediction accuracy across all five behavior classes. Minor misclassifications occur between adjacent behavior classes with slightly overlapping feature distributions.

🔍 Conclusion

The dataset exhibits clear behavioral stratification based on mobile usage intensity. Core usage features such as screen time, app usage, battery drain, and data consumption are strong predictors of user behavior class.
Due to strong linear separability in the dataset, Logistic Regression performs effectively and generalizes well to unseen data.

🚀 Future Improvements

Experiment with alternative models (Random Forest, KNN)
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
