# 🏠 House Price Prediction Model

## Overview:

This project implements a machine learning model to predict house prices based on various property features. The model uses XGBoost (Extreme Gradient Boosting) with careful feature engineering and preprocessing to achieve accurate price predictions.

## Dataset

The dataset used in this project is from Kaggle. You can find the original dataset here:  
[Kaggle House Price Dataset](https://www.kaggle.com/datasets/shivachandel/kc-house-data)

The dataset contains house sale prices for King County (Seattle, WA area) with the following key features:
- Bedrooms, bathrooms, square footage
- Location information (zip codes)
- Property age and renovation history
- Waterfront status, views, and condition
- And other relevant property characteristics

## Features

The model includes several engineered features to improve prediction accuracy:
- House age (current year - year built)
- Renovation status (whether the property has been renovated)
- Years since last renovation
- Living area to lot size ratio
- Price per square foot
- Total rooms (bedrooms + bathrooms)
- Basement presence indicator
- Month when the property was sold

## Model Architecture

The pipeline consists of:
1. **Preprocessing**:
   - One-hot encoding for categorical features (month sold)
   - Ordinal encoding for zip codes
   - Numerical features passed through unchanged

2. **Regression Model**:
   - XGBoost regressor with 200 estimators
   - Learning rate of 0.1
   - Maximum tree depth of 6

## Performance

The model achieves the following metrics on the test set:
- **R² Score**: 0.6724
- **Mean Squared Error**: 27685176236.743435
- **Mean Absolute Error**: 100126.8193048326

## Requirements

- Python 3.6+
- pandas
- scikit-learn
- xgboost

## Future Improvements

- Hyperparameter tuning for better performance
- Additional feature engineering
- Experiment with different models
- Address potential data quality issues
- Add more comprehensive evaluation metrics

  
