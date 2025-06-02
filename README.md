# 🏡 Ames Housing Price Prediction

This project focuses on regression analysis of the Ames Housing Dataset, aiming to predict house sale prices (`SalePrice`) based on a wide variety of features.

---

## 📂 Overview

The dataset includes over 70 features such as:

- Total square footage  
- Year built, number of bathrooms, garage info  
- Neighborhood, house style  
- Overall condition and quality  

---

## 📊 Models Used

The project compares performance across multiple regression models:

- Linear Regression  
- RidgeCV  
- Random Forest Regressor  
- XGBoost  
- Kernel Ridge Regression  
- Stacking ensembles:  
  - RandomForest + XGBoost  
  - RidgeCV + XGBoost  

---

## ⚙️ Evaluation Metrics

All models are evaluated using 4‑fold cross‑validation (`KFold`) on the following metrics:

- MAE — Mean Absolute Error  
- RMSE — Root Mean Squared Error  

---

## 🔍 Cross-Validation Results

| Model                   | Mean MAE | Mean RMSE |
|-------------------------|----------|-----------|
| Linear Regression       | ~19,100  | ~28,560   |
| RidgeCV                 | ~19,000  | ~28,550   |
| Random Forest           | ~15,165  | ~22,139   |
| XGBoost                 | ~14,356  | ~21,168   |
| Kernel Ridge            | ~22,676  | ~32,965   |
| Stacking (RF + XGB)     | ~16,060  | ~23,819   |
| Stacking (Ridge + XGB)  | ~14,173  | ~20,958   |

---

## 🔥 Top Features (Feature Importance)

Feature importance was extracted using RandomForest and XGBoost. The top features contributing to prediction include:

- OverallQual  
- GrLivArea  
- TotalBsmtSF  
- GarageCars  
- YearBuilt  
- etc.  

---

## 📈 Visualizations

### 🔷 Correlation Heatmap

![Correlation Heatmap](images/feature_correlation_heatmap.png)

### 🏘 Sale Price by Neighborhood

![Sale Price by Neighborhood](images/saleprice_neighborhood_boxplot.png)

### 📊 Histogram: Overall Condition

![Overall Condition Histogram](images/overall_condition.png)

### 📊 Histogram: Overall Quality

![Overall Quality Histogram](images/overall_quality_hist.png)

---

## 💾 Dataset

Data used:  
📎 [Ames Housing Dataset on Kaggle](https://www.kaggle.com/code/devraai/ames-housing-eda-prediction)

---

## 🧰 Installation

To run the project locally:

```bash
pip install -r requirements.txt
