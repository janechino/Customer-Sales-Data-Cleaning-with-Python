# Customer Sales Prediction and Analysis (Customer-Sales-Data-Cleaning-with-Python)
## Overview
This Python script is designed to process and analyze customer sales data from multiple CSV files, including transactional data and shopping behavior insights. It performs data wrangling, predictive modeling, and generates visualizations to assist in understanding customer behavior, sales performance, and customer retention rates.

The script leverages machine learning models for sales prediction (regression) and subscription status classification (classification). It also includes exploratory data analysis (EDA) to generate key insights, such as revenue by gender and subscription status, as well as customer retention metrics.

# Libraries Used
The script utilizes the following libraries:

pandas: For data manipulation and cleaning.

numpy: For numerical operations.

matplotlib.pyplot: For plotting graphs and visualizations.

seaborn: For enhanced data visualizations.

sklearn: For machine learning models and performance evaluation.


# File Structure
The following datasets are used in the analysis:

Q1: Customer sales data containing individual transaction details.

Q2: Updated shopping behavior data, including payment methods and shipping types.

Q9: Data on customer purchase amounts and behaviors.

These files are loaded from the local directory.

# Script Workflow
## STEP ONE: Install & Import Necessary Libraries
The required libraries (pandas, numpy, matplotlib, seaborn, and sklearn) are imported to facilitate data manipulation, analysis, and visualization.

## STEP TWO: Upload Customer Sales Data
The datasets (Q1, Q2, Q9) are loaded using pd.read_csv() from the local machine's file path.

## STEP THREE: Data Wrangling
Subscription Status Transformation: The subscription status column is updated with appropriate labels ("Normal" for "Not Subscribed" and "Member" for "Subscribed").

Date Conversion: The purchase date is converted to a datetime format, and components such as year, month, day, and day of the week are extracted.

Season Assignment: Each purchase is mapped to its respective season based on the month.

Column Renaming: Columns are renamed for consistency across the datasets.

Data Standardization: Gender, payment methods, subscription status, and sales channels are standardized across datasets.

Dropping Unnecessary Columns: Irrelevant columns are dropped to streamline the data.

Combining Data: Data from all datasets is concatenated into a single dataframe for analysis.

## STEP FOUR: Preprocessing
Missing values (NA) are dropped, and duplicate records are removed.

Categorical columns are encoded using LabelEncoder() to prepare data for machine learning models.

The features (X) and target variables (Y) are split for sales prediction and subscription classification.

Data is scaled using StandardScaler().

## STEP FIVE: Predictive Modeling
Sales Prediction (Regression): A linear regression model is trained to predict the total revenue based on customer features.

Subscription Status Classification (Classification): A Random Forest classifier is trained to predict whether a customer is subscribed or not.

The models are evaluated using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), R² score for regression, and accuracy, classification report for classification.

## STEP SIX: Descriptive Analysis
Customer Retention: The customer retention rate (percentage of members) is calculated and displayed in a pie chart.

Revenue by Gender & Subscription Status: A grouped summary of revenue by gender and subscription status is generated, followed by a bar plot visualization.

# Output
Sales Prediction Performance: The performance metrics (MAE, MSE, R²) for the sales prediction model.

Subscription Prediction Performance: Accuracy and classification report for the subscription status prediction model.

Customer Retention Pie Chart: A visual representation of customer retention based on subscription status.

Revenue Summary: A detailed summary of revenue by gender and subscription status.

Revenue Bar Plot: A bar plot showing the total revenue broken down by gender and subscription status.
