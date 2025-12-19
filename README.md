# Aircraft Price Prediction – Multiple Linear Regression Model

A robust **multiple linear regression model in R** developed to predict aircraft prices using technical and performance specifications.  
This project focuses on identifying the **key drivers of aircraft pricing** while ensuring statistical validity through rigorous diagnostics.

---

## Project Overview

###  Goal
Predict aircraft prices using features such as **engine type, engine power, speed, and wing span**, and identify the most influential pricing factors for aviation stakeholders.

###  Key Achievements
- Achieved **92.5% explained variance (Adjusted R²)** using interaction terms
- Identified **critical predictors**: engine type, cruise speed, and wing span
- Applied rigorous statistical diagnostics:
  - Multicollinearity
  - Heteroscedasticity
  - Outlier and influence analysis

---

##  Dataset

- **Source**: Kaggle  
- **Dataset**: [Aircraft Price Analysis and Prediction Dataset](https://www.kaggle.com/datasets/mehmet0sahinn/aircraft-price-analysis-and-prediction-dataset)

- **Records**: 517 aircraft (after cleaning)  
- **Features**:  
  - 14 quantitative  
  - 2 qualitative  

### Variables

| Type | Description |
|-----|------------|
| **Target** | `price` (USD) |
| **Predictors** | `engine_type` (Jet / Piston / Propjet), `engine_power` (hp), `cruise_speed` (knots), `wing_span` (inches), `range` (nautical miles), and others |

---

##  Usage

### 1️ Open R or RStudio

### 2️ Install required packages
```r
install.packages(c("tidyverse", "car", "MASS", "broom", "GGally"))
```
### 3. Run the analysis
Oopen and execute the RMarkdown notebook:
Aircraft_Price_Prediction.Rmd

---
##  Methodology

1. **Data Cleaning**
   - Removed missing values
   - Standardized measurement units
   - Encoded categorical variables

2. **Exploratory Data Analysis (EDA)**
   - Visualized feature relationships
   - Detected outliers and trends

3. **Feature Engineering**
   - Created interaction terms to improve model performance

4. **Modeling**
   - Built multiple linear regression models
   - Applied stepwise model selection

5. **Model Diagnostics**
   - Checked multicollinearity using Variance Inflation Factor (VIF)
   - Evaluated heteroscedasticity
   - Analyzed residuals and influential points

---
##  Results

#### Best Model

```r
price ~ factor(engine_type) + engine_power + max_speed + cruise_speed +
        stall_speed + all_eng_roc + out_eng_roc +
        takeoff_distance + wing_span + range
```
#### Adjusted R²: 0.9248

#### Key Predictors: Engine type, cruise speed, wing span

#### Main Effects of Engine Type:

- Piston: Aircraft with a piston engine are, on average, $4.4 million cheaper than jets (holding other variables constant).
- Propjet: Aircraft with a propjet engine are $2.8 million cheaper than jets.
### Model Diagnostics:

- Multicollinearity managed (VIF mostly < 5)
- Residuals checked for normality and equal variance

---
## Repository Structure

```text
.
├── notebook/
│   └── Aircraft_Price_Prediction.Rmd   
├── README.md
└── .gitignore

```
---
## Challenges

- Handling missing and inconsistent data
- Addressing multicollinearity among predictors
- Managing outliers and influential points

---
## Team
- Riya Chevli
- Anitha Joseph
- Jincy Thomas
- Joshua Quartey
- Megha Radhakrishnan Sanitha
- Prichelle Lal


