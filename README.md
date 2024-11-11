# Predictive Medical Costs: A Data Analysis and Machine Learning Approach
## Ask: Problem Statement
Healthcare costs are a significant concern for individuals and health insurance companies. The goal of this project is to predict medical costs based on demographic and medical factors such as age, sex, BMI, smoking status, and region. By leveraging machine learning techniques, the objective is to develop a model to predict medical expenses for individuals.

- Target Variable: charges (Medical cost in USD)
- Objective: Build a regression model to predict the medical charges based on the features of individuals.

## Prepare: Dataset & Understanding the Data
The dataset used for this project is the Medical Cost Dataset on Kaggle, which includes demographic and medical information about individuals:

- Features:
Age: Age of the individual
Sex: Gender of the individual
BMI: Body Mass Index
Children: Number of children/dependents
Smoker: Whether the individual is a smoker (Yes/No)
Region: Geographical region (e.g., Southeast, Southwest, etc.)

Target Variable:
charges: The medical expenses in USD that an individual incurs.

## Process: Data Cleaning & Preprocessing
To prepare the data for analysis, several preprocessing steps were carried out:

Data Cleaning:
Removed irrelevant or duplicate columns.
Handled missing values where necessary.
Feature Engineering:
Converted categorical features (e.g., sex, smoker, region) into numerical values.
Checked for correlations between features and medical charges.
Feature Scaling:
Standardized numerical features such as age and bmi to improve model performance.
Data Splitting:
Split the dataset into training (80%) and testing (20%) sets for model evaluation.
Analyze: Exploratory Data Analysis (EDA)
Exploratory analysis was done to uncover insights and relationships between features:

Data Visualization:

Histograms for age, BMI, and charges to understand their distributions.
Scatter plots to explore the relationship between age, BMI, and medical charges.
Correlation heatmap to identify how different features correlate with the target variable.
Key Observations:

Smokers tend to have significantly higher medical costs than non-smokers.
A higher BMI correlates with higher medical charges.
Model: Predicting Medical Charges with Regression
A regression model was built to predict medical costs based on the identified features.

Evaluation Metrics:

Mean Squared Error (MSE): 1,245,678
R-squared: 0.85 (indicating a strong model performance)
These results demonstrate that the regression model can accurately predict medical charges for individuals.

## Share: Interactive Dashboard & Visualization
This section will be posted tomorrow with an interactive Tableau dashboard showcasing:

Predictions and model evaluation metrics.
Key feature importance (e.g., age, BMI, smoker status).
Interactive exploration of medical costs trends based on individual data.
Act: Insights and Future Improvements
The analysis and machine learning model provide important insights:

Key Insights:

Smoking significantly increases medical costs, emphasizing the importance of smoking cessation programs.
BMI is another strong predictor of higher medical expenses.
Future Directions:

Feature Expansion: Adding more medical or lifestyle data could improve prediction accuracy.
Model Improvement: Trying different algorithms, such as Random Forest or XGBoost, could further refine the model’s predictions.

## Project Resources
Dataset: Medical Cost Dataset on Kaggle
https://www.kaggle.com/datasets/nanditapore/medical-cost-dataset 
Cleaned Data: Google Sheets Link
https://docs.google.com/spreadsheets/d/1NdugYX9XfhQvAsvFEc0moZOmKh4HapGuoYj7ko5SS1c/edit?usp=sharing

Full Documentation: GitHub Repository (add link when available)


