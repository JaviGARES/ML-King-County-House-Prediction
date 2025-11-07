# 🏡 King County House Price Prediction

This project analyzes house sale prices in King County (including Seattle) for the period of **May 2014 to May 2015**. The goal was to determine which property features have the greatest impact on house prices and to build a machine learning model capable of predicting sale prices.

---

## 📊 Dataset Overview

The dataset contains **21 features** describing property characteristics such as size, number of bedrooms, condition, renovation history, location, and more.

**Dataset Source:**  
https://www.kaggle.com/datasets/minasameh55/king-country-houses-aa

**Target Variable:**  
`price` – the sale price of the house.

Example key features:
- `sqft_living`: Interior living space (sqft)
- `grade`: Overall construction and design quality
- `waterfront`: Whether the house has a waterfront view
- `lat` / `long`: Property geographic location

---

## 🔍 Project Steps

### 1. **Data Exploration**
- Checked data structure, distributions, and summary statistics.
- Visualized price distribution and inspected potential outliers.
- Identified correlations and multicollinearity between features.

### 2. **Data Preprocessing**
- Dropped irrelevant columns (`id`, `date`).
- Encoded categorical variable (`zipcode`).
- Removed extreme outliers based on price distribution.
- Created new useful features (feature engineering), including:
  - `house_age`
  - `years_since_renovation`
  - `was_renovated`
  - `total_sqft`
  - `bath_per_bed`
  - `living_lot_ratio`
  - `is_luxury` (price ≥ $650,000)

### 3. **Modeling**
Tested multiple machine learning models:

| Model | Description |
|------|-------------|
| Linear Regression | Baseline model |
| KNN Regressor | Distance-based regression |
| Random Forest Regressor | Decision tree ensemble |
| XGBoost Regressor | Gradient boosting model |

### 4. **Model Improvement**
- Used outlier removal and feature engineering to improve accuracy.
- Applied **RobustScaler** to reduce sensitivity to extreme values.
- Performed **Hyperparameter Tuning** on Random Forest and XGBoost models.

---

## 🏆 Best Model & Key Results

The **best performing model** was: **XGBoost (tuned)**
It achieved:
- **High R² score**
- **Low RMSE**
- **Strong generalization to unseen data**

### 📈 Most Influential Features:
1. **Grade** (construction quality)
2. **Sqft_living**
3. **Location (latitude / longitude)**
4. **Sqft_living15** (neighborhood home size)
5. **Waterfront presence**

---

## 💡 Insights & Recommendations

### For Sellers:
- Improving **home quality (grade)** yields strong value increases.
- Highlight **location advantages** and **living space**.
- Renovations can significantly improve resale value.

### For Buyers:
- Location and construction quality should guide purchase decisions.
- Waterfront and view properties justify their price premium.
- Consider properties with renovation potential.

---

## 📂 Deliverables

- **Jupyter Notebook** containing full data processing and modeling steps.
- **Presentation** summarizing approach and insights.
- **This README.md** explaining workflow and conclusions.

---

## 👥 Team & Collaboration

This project was completed as part of a collaborative analysis simulation to reflect real-world real estate data science workflows.

---