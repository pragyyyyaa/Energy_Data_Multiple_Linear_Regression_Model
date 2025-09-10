# Appliance Energy Prediction

## Project Overview
This project aims to predict household appliance energy consumption based on environmental and temporal factors. 
The dataset includes indoor temperature, humidity, and weather data collected over 4.5 months. 
The primary modeling approach used was **Multiple Linear Regression (MLR)**, supported by exploratory data analysis and statistical checks.

---

## Objectives
- Clean and preprocess the dataset.
- Perform Exploratory Data Analysis (EDA).
- Treat outliers using IQR.
- Check multicollinearity using Variance Inflation Factor (VIF).
- Train a Multiple Linear Regression model with stepwise elimination.
- Perform model diagnostics (normality and homoscedasticity of residuals).
- Evaluate results and suggest improvements.

---

## Dataset
- **Source:** Household energy consumption dataset with weather station data (Chièvres, Belgium).  
- **Target Variable:** `Appliances` (energy consumption in Wh).  
- **Features:** Indoor temperature, humidity, and weather station variables.  
- **Final Features Used:** 18 (after dropping insignificant/multicollinear variables).

---

## Methodology
1. Data Cleaning: Dropped irrelevant columns (date), checked null values, duplicates.
2. Outlier Treatment: Used IQR method and clipped extreme values.
3. Scaling: Applied MinMaxScaler for normalization.
4. Exploratory Analysis: Univariate, bivariate, multivariate visualizations (histograms, scatter plots, violin plots, heatmaps, pairplots).
5. Feature Selection: Removed multicollinear variables using VIF.
6. Modeling: Built an MLR model with stepwise feature elimination based on p-values.
7. Diagnostics: Residuals tested for normality & homoscedasticity.

---

## Results
- Final Model included 18 significant predictors.
- **R-squared:** 0.190 → Model explains ~19% of variance.
- **Limitations:** Residual analysis showed heteroscedasticity → Linear regression assumptions not fully met.

---

## Future Work
- Apply advanced regression techniques:
  - Random Forest Regressor
  - Gradient Boosting Regressor
  - Neural Networks
- Improve feature engineering with additional temporal/weather features.

---

## How to Run
1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd appliance-energy-prediction
   ```

2. Install requirements:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook or Python script for analysis.

---

## Author
Submitted by: **Pragya Gupta**  
PGDM-Research & Business Analytics
