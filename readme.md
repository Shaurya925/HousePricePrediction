# House Price Prediction using XGBoost

## Overview

This project predicts house prices using machine learning techniques. The dataset was preprocessed, explored, and multiple models were trained and compared to select the best-performing model.

The target variable (`SalePrice`) was highly skewed, so a logarithmic transformation was applied to improve model performance.

The final model was an XGBoost Regressor optimized using GridSearchCV.

## Dataset

* Source: Kaggle House Prices Dataset
* Rows: 1460
* Original Features: 81
* Final Features after preprocessing: 191

## Project Workflow

### 1. Data Cleaning

* Handled missing values
* Dropped columns with excessive missing values
* Removed unnecessary features

### 2. Exploratory Data Analysis (EDA)

* Analyzed target variable distribution
* Checked correlations
* Identified important features

### 3. Feature Engineering

* Log transformed `SalePrice`
* One-hot encoded categorical variables
* Performed train-test split

### 4. Model Building

Models trained:

1. Linear Regression
2. Random Forest Regressor
3. XGBoost Regressor

### 5. Hyperparameter Tuning

GridSearchCV was used to optimize the XGBoost model.

## Model Performance

| Model             | R² Score |
| ----------------- | -------- |
| Linear Regression | 0.774    |
| Random Forest     | 0.886    |
| XGBoost           | 0.900    |
| Tuned XGBoost     | 0.904    |

Final Model:

* Algorithm: XGBoost Regressor
* R² Score: 0.904
* RMSE: 0.134

## Feature Importance

Top contributing features:

* OverallQual
* ExterQual
* GarageCars
* CentralAir
* GrLivArea

## Visualizations

* SalePrice distribution
* Correlation heatmap
* Actual vs Predicted plot
* Residual plot
* Feature importance plot

## Files

```text
house_price_model.pkl
feature_columns.pkl
house_price_prediction.ipynb
README.md
requirements.txt
```

## How to Run

### Clone repository

```bash
git clone <repository-url>
cd house-price-prediction
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run notebook

```bash
jupyter notebook
```

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* Joblib

## Future Improvements

* Build a Streamlit web application
* Deploy the model
* Save preprocessing pipeline
* Add prediction API

## Author

Shaurya Kumar
