# FMCG-company-Supply-Chain-Management-ML-project-for-shipment-optimization
Supply Chain Optimization using Regression &amp; Machine Learning | FMCG Optimum Shipment Prediction | EDA, OLS, Random Forest, Gradient Boosting

## Overview
This project addresses supply chain inefficiencies in an FMCG company operating in the instant noodles market. The company faced demand-supply mismatches across warehouses, leading to excess inventory in some regions and stock shortages in others.

The goal of this project is to use historical operational data to build predictive models that improve shipment planning and optimize supply chain performance.

---

## Objective
- Predict shipment volume (`product_wg_ton`)
- Identify key drivers impacting supply chain efficiency
- Provide actionable business recommendations

---

## Dataset
- **Rows:** 25,000  
- **Columns:** 24  
- **Time Period:** Last 3 months  
- **Target Variable:** `product_wg_ton`  

### Key Features:
- Warehouse details (location, size, ownership)
- Operational metrics (transport issues, breakdowns, storage issues)
- Market factors (competitors, distributors, retail shops)

---

## Exploratory Data Analysis (EDA)
- Univariate and Bivariate Analysis
- Correlation heatmap
- Outlier detection

### Key Findings:
- Strong correlation between `storage_issue_reported_l3m` and shipment volume (possible data leakage)
- Urban areas receive higher shipments despite most warehouses being in rural areas
- Transport issues negatively impact shipment volume

---

## Data Preprocessing
- Removed irrelevant columns (`Ware_house_ID`, `WH_Manager_ID`)
- Handled missing values:
  - Mean (numerical features)
  - Mode (categorical features)
- Outlier treatment applied
- Created dummy variables for categorical features
- Train-test split: 70:30

---

## Models Implemented

### Linear Regression (OLS)
- Multicollinearity handled using VIF
- Removed high p-value variables
- **R² Score:** ~0.985
- Good generalization (no overfitting)

---

###  Advanced Models
- Random Forest
- Gradient Boosting
- Bagging

### Final Model: Gradient Boosting
- **R² Score:** 0.994  
- **MAPE:** 4.35%  
- Best performance after hyperparameter tuning

---

## Model Evaluation
- RMSE, MAE, MAPE
- Residual analysis
- Assumption testing:
  - Linearity
  - Normality
  - Homoscedasticity

---

## Key Insights
- Transport issues significantly reduce shipment volume
- Warehouse breakdowns negatively impact operations
- Temperature-controlled warehouses increase shipments
- Government-certified warehouses (A+) perform better
- Storage issues are a major influencing factor

---

## Business Recommendations

### Logistics Optimization
- Improve routing and reduce transport disruptions

### Infrastructure Upgrade
- Invest in warehouse maintenance and monitoring systems

### Temperature Control
- Enhance temperature-regulated storage facilities

### Demand-Based Expansion
- Increase capacity in high-demand zones (Zone 6)

### Distribution Strategy
- Use rural warehouses for storage
- Use urban warehouses for distribution

### Certification Improvement
- Upgrade warehouses to higher government certification levels

---

## Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Statsmodels
