# Predictive Medical Costs: A Data Analysis and Machine Learning Approach  

This case study explores a data-driven approach to predicting medical costs using demographic, lifestyle, and derived factors such as BMI category, age group, smoker status, family size, risk group, and cost ranges. Using the **Medical Cost Dataset** from Kaggle, the project involved data cleaning, feature engineering, exploratory analysis, and building machine learning models—specifically Linear Regression and Random Forest—to forecast medical expenses. The analysis highlights key cost drivers such as smoking, BMI, and risk group, emphasizing preventive healthcare's role in reducing expenses. This work demonstrates how predictive modeling can provide actionable insights to address healthcare cost challenges effectively.

---

## Table of Contents  

1. [**Ask: Problem Statement**](#1-ask-problem-statement)  
2. [**Prepare: Dataset & Understanding the Data**](#2-prepare-dataset--understanding-the-data)  
3. [**Process: Data Cleaning & Preprocessing**](#3-process-data-cleaning--preprocessing)  
4. [**Analyze: Exploratory Data Analysis (EDA)**](#4-analyze-exploratory-data-analysis-eda)  
5. [**Model: Predicting Medical Charges with Regression**](#5-model-predicting-medical-charges-with-regression)  
6. [**Share: Interactive Dashboard & Visualization**](#6-share-interactive-dashboard--visualization)  
7. [**Act: Insights and Future Improvements**](#7-act-insights-and-future-improvements)  
8. [**Project Resources**](#8-project-resources)  

---

## 1. Ask: Problem Statement  

Healthcare costs are a significant concern for individuals and insurance companies. This project aims to predict medical costs based on demographic, lifestyle, and derived factors such as age, BMI, smoking status, and new categorical features. By leveraging machine learning techniques, the goal is to develop a model that predicts medical expenses for individuals.  

- **Target Variable**: `charges` (Medical cost in USD)  
- **Objective**: Build a regression model to predict medical charges based on individual features and engineered categories.  

---

## 2. Prepare: Dataset & Understanding the Data  

The dataset used for this project is the [Medical Cost Dataset on Kaggle](https://www.kaggle.com/datasets/nanditapore/medical-cost-dataset), which includes demographic and medical information about individuals.  

### Features:  
- **Age**: Age of the individual  
- **Sex**: Gender of the individual  
- **BMI**: Body Mass Index  
- **Children**: Number of children/dependents  
- **Smoker_binary**: Encoded smoker status into `0` (Non-smoker) and `1` (Smoker).
- **Region**: Geographical region (e.g., Southeast, Southwest, etc.)  

### Derived Features:  
1. **BMI_category**: Categorized BMI into `Underweight`, `Normal`, `Overweight`, and `Obese`.  
2. **Age_category**: Grouped ages into categories such as `Young`, `Middle-aged`, and `Senior`.  
3. **Smoker**: Whether the individual is a smoker (`Yes`/`No`)   
4. **Family_size**: Derived from the `children` column into categories like `No children` and `Large family`.  
5. **Risk_group**: Categorized individuals into `Low-risk`, `Medium-risk`, and `High-risk` based on smoking and BMI.  
6. **Cost_ranges**: Grouped medical charges into ranges such as `Low`, `Medium`, and `High`.  

### Target Variable:  
- **charges**: The medical expenses in USD that an individual incurs.  

---

## 3. Process: Data Cleaning & Preprocessing  

To prepare the data for analysis, several preprocessing steps were performed:  

1. **Data Cleaning**: Removed irrelevant or duplicate columns and handled missing values.  
2. **Feature Engineering**:  
   - Derived new features like `BMI_category`, `Age_category`, and `Risk_group`.  
   - Converted categorical features (`sex`, `smoker`, `region`) and derived features into numerical values.  
   - Checked correlations between features and medical charges.  
3. **Feature Scaling**: Standardized numerical features such as `age` and `BMI` to improve model performance.  
4. **Data Splitting**: Divided the dataset into **training (80%)** and **testing (20%)** sets for model evaluation.  

---

## 4. Analyze: Exploratory Data Analysis (EDA)  

Exploratory analysis was performed to uncover insights and relationships between original and derived features.  

### Objectives:  
- Understand data distribution and relationships.  
- Identify significant predictors of medical costs.  
- Visualize the data using histograms, scatterplots, bar charts, and correlation heatmaps.  

Key Findings from EDA:  
1. Smokers incur **significantly higher medical costs** than non-smokers.  
2. Individuals categorized as **Obese** have higher average costs than those in lower BMI categories.  
3. **High-risk groups**, as defined by the risk group feature, represent the highest average medical charges.  

Key Libraries: `ggplot2`, `dplyr`, `tidyr`.  

---

## 5. Model: Predicting Medical Charges with Regression  

Two models were trained to predict medical costs based on the identified features:  

### Models Trained:  
1. **Linear Regression**:  
   - **RMSE**: 5521.50  
   - **MAE**: 3742.80  
   - **R-squared**: 0.761  

2. **Random Forest**:  
   - **RMSE**: 5514.34  
   - **MAE**: 3944.00  
   - **R-squared**: 0.754  

### Key Takeaways:  
- Both models performed comparably, with **Linear Regression** slightly outperforming Random Forest in R-squared.  
- **Smoker_binary**, **BMI_category**, and **Risk_group** were identified as the most significant predictors of higher medical costs.  
![predictive model](https://github.com/user-attachments/assets/7659bec1-71b1-429c-9f2f-fa777e39694a)
![BMI vs Charges by Risk Group](https://github.com/user-attachments/assets/bc4b9230-6b28-4190-8d33-1a8c5b0b4c22)

---

## 6. Share: Interactive Dashboard & Visualization  

An interactive **Tableau Dashboard** is under development to showcase:  
- Predictions and model evaluation metrics.  
- Key feature importance, including derived categories like `Risk_group` and `BMI_category`.  
- Interactive exploration of medical cost trends based on user-selected features.  
![Dashboard 1 (7)](https://github.com/user-attachments/assets/6e67d2b6-bfbb-4fca-bf67-37dab0b11b03)
[Interactive Tableau Dashboard](https://public.tableau.com/views/PredictiveMedicalCost/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
---

## 7. Act: Insights and Future Improvements  

### Key Insights:  
1. **Smoking** is a significant factor contributing to higher medical costs, emphasizing the need for robust tobacco control initiatives and smoking cessation programs.
2. High-risk individuals consistently incur higher medical charges, highlighting the importance of targeted interventions and preventive care strategies.
3. Categorical features like `BMI category` and `Risk group` provide valuable insights into medical cost patterns, simplifying model interpretation and enabling more actionable insights.

### Future Directions:  
1. **Feature Expansion**: Incorporate additional relevant features, such as family history, lifestyle factors, and socioeconomic status, to enhance model accuracy and predictive power.
Explore advanced feature engineering techniques, such as feature interaction and transformation, to capture complex relationships within the data.
2. **Model Improvement**:  
   - Experiment with advanced algorithms like **XGBoost** or **Neural Networks**.  
   - Optimize existing models using hyperparameter tuning.  
3. **Dashboard Refinement**: Enhance visualizations to improve user interaction and insights delivery.

---
## 8. Project Resources  

- **Dataset**: [Medical Cost Dataset on Kaggle](https://www.kaggle.com/datasets/nanditapore/medical-cost-dataset)  
- **Cleaned Data**: [Google Sheets Link](https://docs.google.com/spreadsheets/d/1NdugYX9XfhQvAsvFEc0moZOmKh4HapGuoYj7ko5SS1c/edit?usp=sharing)
- **Tableau Dashboard**: [Interactive Tableau Dashboard](https://public.tableau.com/views/PredictiveMedicalCost/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
