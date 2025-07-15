# Project 2: Medical Cost Prediction: Multiple Linear Regression Analysis

![medical_cost_prediction_2](https://github.com/user-attachments/assets/53c86b81-9bfa-4095-9fea-08bded92787a)

:large_blue_diamond: Project Objective:     
 - This project analyzes a public dataset of medical insurance costs from Kaggle to identify the key factors that drive expenses.
 - The goal is to build an accurate and interpretable regression model that can predict a person's annual insurance charges based on their demographic and health-related attributes.

:star2: Key Skills & Tools
 - Data Cleaning & Manipulation: Pandas, NumPy
 - Data Visualization: Matplotlib, Seaborn
 - Statistical Modeling: Statsmodels (Ordinary Least Squares), SciPy (Hypothesis Testing)
 - Machine Learning: Scikit-learn (Train-Test Split, Model Evaluation)
 - Core Competencies: Exploratory Data Analysis (EDA), Feature Engineering (Log Transforms, Interaction & Polynomial Terms), Predictive Modeling, Model Diagnostics.

:herb: Analysis & Key Findings
 - The analysis involved EDA, hypothesis testing, and an iterative model-building process to achieve the most accurate and reliable results.

:herb: Foundational Analysis & Outlier Investigation:
 - A two-sample t-test confirmed that smokers have significantly higher medical charges than non-smokers (p < 0.001), establishing smoking as the most critical predictive variable.
 - Outlier analysis revealed that nearly all high-cost charges belonged to smokers. These data points were retained as they represented legitimate, high-cost scenarios rather than data errors.

:herb: Iterative Model Development & Diagnostics:
 - A baseline OLS regression model was built, which achieved an R-squared of 0.75. However, diagnostic plots revealed that the model's residuals violated the assumptions of normality and homoscedasticity.
 - A log transformation was applied to the charges variable, which successfully corrected these violations and improved the model's fit.

:herb: Key Predictive Factors & Interactions:
 - The final model was enhanced by incorporating key features identified in the EDA, including a significant interaction term between BMI and smoking status and a polynomial term for age.
 - BMI-Smoker Interaction: The model shows that the effect of BMI on costs is far more severe for smokers. For each one-unit increase in BMI, a smoker's charges increase by approximately 4.9%, while the effect for non-smokers is negligible.
 - Non-Linear Age Effect: Costs increase with age but do so at a decreasing rate, highlighting a non-linear relationship.

:herb: Final Model Performance:
 - The final, refined model demonstrates strong predictive power, explaining 78.4% of the variance (Adjusted R-squared) in the log of medical charges.
 - When evaluated on unseen test data, the model achieved a Root Mean Squared Error (RMSE) of ~$7,486.

:bulb: Business Application
 - This predictive model offers significant value for an insurance provider by:
 - Improving Risk Assessment: Accurately pricing insurance premiums based on an individual's key attributes, particularly the combined risk of smoking and high BMI.
 - Informing Wellness Programs: Quantifying the financial impact of smoking and obesity, providing a strong business case for targeted wellness and smoking cessation programs to reduce long-term costs.
