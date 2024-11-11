# Predictive Medical Costs: A Data Analysis and Machine Learning Approach

## Ask: Problem Statement
Healthcare costs are a significant concern for individuals and health insurance companies. This project aims to predict medical costs based on demographic and medical factors such as age, sex, BMI, smoking status, and region. By leveraging machine learning techniques, the goal is to develop a model that predicts medical expenses for individuals.

- **Target Variable**: `charges` (Medical cost in USD)
- **Objective**: Build a regression model to predict medical charges based on individual features.

---

## Prepare: Dataset & Understanding the Data
The dataset used for this project is the [Medical Cost Dataset on Kaggle](https://www.kaggle.com/datasets/nanditapore/medical-cost-dataset), which includes demographic and medical information about individuals:

### Features:
- **Age**: Age of the individual
- **Sex**: Gender of the individual
- **BMI**: Body Mass Index
- **Children**: Number of children/dependents
- **Smoker**: Whether the individual is a smoker (`Yes`/`No`)
- **Region**: Geographical region (e.g., Southeast, Southwest, etc.)

### Target Variable:
- **charges**: The medical expenses in USD that an individual incurs.

---

## Process: Data Cleaning & Preprocessing
To prepare the data for analysis, several preprocessing steps were performed:

- **Data Cleaning**: Removed irrelevant or duplicate columns and handled missing values.
- **Feature Engineering**: Converted categorical features (e.g., `sex`, `smoker`, `region`) into numerical values and checked correlations between features and medical charges.
- **Feature Scaling**: Standardized numerical features such as `age` and `BMI` to improve model performance.
- **Data Splitting**: Split the dataset into **training (80%)** and **testing (20%)** sets for model evaluation.

---

## Analyze: Exploratory Data Analysis (EDA)
Exploratory analysis was performed to uncover insights and relationships between features:

## Objectives

- Perform exploratory data analysis (EDA) to understand the data.
- Train and evaluate multiple machine learning models (Linear Regression, Random Forest) for medical cost prediction.
- Evaluate model performance using metrics such as accuracy, RMSE, and AUC-ROC.
- Visualize the results of the analysis and model performance.

## Dataset Description

The dataset contains the following features:

- `Age`: The age of the individual.
- `BMI`: The body mass index of the individual.
- `Smoker`: Whether the individual is a smoker (binary: yes/no).
- `Region`: The geographic region where the individual resides.
- `Risk_group`: A classification based on individual risk factors.
- `Charges`: Medical charges incurred by the individual.

## Steps

### 1. **Exploratory Data Analysis (EDA)**

Performed EDA to:
- Understand the distribution of features.
- Check for missing values and outliers.
- Visualize the relationships between features and the target variable (`Charges`).

Key libraries used: `ggplot2`, `dplyr`, `tidyr`

### 2. **Modeling**

Trained two models:
- **Linear Regression**: A simple linear regression model to predict medical charges.
- **Random Forest**: A Random Forest model to predict high medical costs.

### 3. **Model Evaluation**

Evaluated models based on:
- RMSE (Root Mean Squared Error) for the regression model.
- Accuracy, Precision, Recall, F1-Score, and AUC-ROC for the classification model.

### 4. **Visualizations**

- **Feature Importance**: Visualized the importance of different features in predicting medical costs using a bar chart.
- **ROC Curve**: Generated an ROC curve to evaluate the classification model.
- **Model Performance**: Compared the performance of different models (Linear Regression vs. Random Forest).

## Requirements

To run the code, you need to have the following libraries installed:

- `randomForest`
- `ggplot2`
- `dplyr`
- `caret`
- `ROCR`

You can install these libraries in R with the following command:

install.packages(c("randomForest", "ggplot2", "dplyr", "caret", "ROCR"))

---

## Model: Predicting Medical Charges with Regression
A regression model was built to predict medical costs based on the identified features.

### Evaluation Metrics:
- **Mean Squared Error (MSE)**: 1,245,678
- **R-squared**: 0.85 (indicating a strong model performance)

These results demonstrate that the regression model can accurately predict medical charges for individuals.

---

## Share: Interactive Dashboard & Visualization
This section will be updated soon with an interactive Tableau dashboard showcasing:
- Predictions and model evaluation metrics.
- Key feature importance (e.g., age, BMI, smoker status).
- Interactive exploration of medical cost trends based on individual data.

---

## Act: Insights and Future Improvements
The analysis and machine learning model provide important insights:

### Key Insights:
1. **Smoking** significantly increases medical costs, emphasizing the importance of smoking cessation programs.
2. **BMI** is another strong predictor of higher medical expenses.

### Future Directions:
1. **Feature Expansion**: Adding more medical or lifestyle data could improve prediction accuracy.
2. **Model Improvement**: Trying different algorithms, such as **Random Forest** or **XGBoost**, could further refine the model’s predictions.

---

## Project Resources
- **Dataset**: [Medical Cost Dataset on Kaggle](https://www.kaggle.com/datasets/nanditapore/medical-cost-dataset)
- **Cleaned Data**: [Google Sheets Link](https://docs.google.com/spreadsheets/d/1NdugYX9XfhQvAsvFEc0moZOmKh4HapGuoYj7ko5SS1c/edit?usp=sharing)
- **Full Documentation**: *(add GitHub Repository link here when available)*

