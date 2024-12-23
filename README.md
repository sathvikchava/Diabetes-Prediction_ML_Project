# Diabetes Prediction Using Machine Learning

---

## Overview
This project leverages machine learning to predict diabetes based on health, lifestyle, and demographic data from the CDC Diabetes Health Indicators dataset. By combining exploratory data analysis (EDA), robust preprocessing techniques, and multiple predictive models, we aim to provide data-driven insights for early diabetes detection and prevention.

---

## Table of Contents
1. [Objective](#objective)
2. [Dataset](#dataset)
3. [Methodology](#methodology)
4. [Results](#results)
5. [Technologies Used](#technologies-used)
6. [Contributors](#contributors)

---

## Objective
Diabetes, a chronic global health issue, affects millions and poses significant medical and economic burdens. This project seeks to:
- Predict diabetes using machine learning.
- Identify key factors influencing diabetes risk.
- Demonstrate the role of data science in healthcare innovation.

---

## Dataset
- **Source**: [CDC Diabetes Health Indicators Dataset](https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators)
- **Size**: 253,680 records, 22 features.
- **Key Features**:
  - Health indicators (BMI, blood pressure, cholesterol).
  - Lifestyle factors (physical activity, diet, smoking).
  - Demographics (age, income, education).

---

## Methodology
### 1. Data Cleaning
The raw dataset was prepared for analysis through systematic preprocessing:
1. **Importing Data**: The dataset was loaded and reviewed for structure and content.
2. **Handling Missing Values**: 
   - The dataset was analyzed using `df.isnull().sum()`, and it was confirmed that there were no missing values.
3. **Categorical Variables**:
   - Variables such as `Age`, `Education`, `GenHlth`, and others were transformed using one-hot encoding.
   - This conversion made the data suitable for machine learning algorithms.
4. **Numerical Variables**:
   - Features like `BMI` were standardized using `StandardScaler` to ensure consistency in scale.
5. **Final Dataset**:
   - The cleaned dataset consisted of 104 features, with categorical variables expanded through encoding.

---

### 2. Exploratory Data Analysis (EDA)
EDA was conducted to uncover patterns, distributions, and relationships in the data:
1. **Dataset Overview**:
   - The dataset includes 253,680 rows and 22 columns.
   - Key predictors include health indicators (BMI, blood pressure) and lifestyle factors (physical activity, diet).
2. **Target Variable Distribution**:
   - The target variable, `Diabetes_binary`, is highly imbalanced:
     - 90% of entries indicate no diabetes.
     - 10% indicate diabetes.
   - Imbalance highlights challenges in predicting diabetic cases.
3. **Numerical Feature Analysis**:
   - Histograms of features like `BMI`, `MentHlth`, and `PhysHlth` revealed right-skewed distributions.
   - Most individuals fall within normal BMI ranges, with fewer in underweight or overweight categories.
4. **Correlation Analysis**:
   - Strong positive correlations with `Diabetes_binary`: General Health, High Blood Pressure, BMI.
   - Negative correlations: Fruits/Vegetable intake, physical activity, and higher income.
   - Heatmaps visualized relationships, highlighting significant predictors.
5. **Key Findings**:
   - General health, high blood pressure, and BMI are critical predictors of diabetes risk.
   - Lifestyle factors such as healthy eating and physical activity reduce the likelihood of diabetes.

---

### 3. Modeling
- **Algorithms Used**: Logistic Regression, Random Forest, AdaBoost.
- Implemented cross-validation for stable and reliable results.
- Evaluated models on metrics like accuracy, precision, recall, and F1 scores.

---

## Results
- **Model Performance**:
  - Logistic Regression: **86.51% Accuracy**
  - Random Forest: **85.94% Accuracy**
  - AdaBoost: **86.44% Accuracy**
- **Key Insights**:
  - Strong predictors include BMI, general health, and blood pressure.
  - Lifestyle factors (e.g., fruit/vegetable intake) are inversely related to diabetes risk.
  - Challenges remain in improving recall for diabetic cases due to class imbalance.

---

## Technologies Used
- **Programming Language**: Python
- **Libraries**:
  - Data Processing: `pandas`, `numpy`
  - Visualization: `matplotlib`, `seaborn`
  - Machine Learning: `scikit-learn`
- **Tools**: Jupyter Notebook

---
