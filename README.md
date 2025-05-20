This project analyzes Algerian market price data to predict price spreads between lower and upper bounds, providing insights into market volatility and price variations across different product categories.

## Project Overview

The Algerian Market Price Spread Prediction project implements a data science workflow to analyze and predict price spreads in the Algerian market. The project covers:

1. Data Cleaning & Preprocessing
2. Exploratory Data Analysis (EDA)
3. Machine Learning Model Development


## Dataset

The dataset contains information about various products in the Algerian market with the following key columns:

- `lowerBound`: Minimum observed price for a product
- `upperBound`: Maximum observed price for a product
- `price`: Average or standard price for a product
- `category`: Product category (e.g., fruits, vegetables, etc.)
- `month`: Month when the price data was collected
- `spread`: Calculated price spread (target variable)

The spread is defined as: `(upperBound - lowerBound) / lowerBound` and represents the relative price range for each product.

## Workflow

### 1. Data Cleaning

- Calculated the spread between upper and lower price bounds
- Handled infinity values that resulted from division operations
- Removed or replaced NaN values to ensure data quality
- Verified data cleanliness with statistical checks

### 2. Feature Selection & Engineering

- Selected relevant features for model training: `lowerBound`, `upperBound`, `price`, `category`, and `month`
- Processed categorical variables using one-hot encoding

### 3. Model Development

We implemented a **Random Forest Regressor** to predict price spreads with the following specifications:
- 100 decision trees (`n_estimators=100`)
- Standard train-test split (80% training, 20% testing)
- Categorical features encoded using pandas `get_dummies` functionality

### 4. Model Evaluation

The model was evaluated using multiple metrics:
- Root Mean Squared Error (RMSE)
- R² Score (coefficient of determination)

Additionally, visualizations were created to assess:
- Actual vs Predicted spread values
- Feature importance analysis to identify key factors influencing price spread

## Key Insights

- The model effectively captures the relationship between product attributes and price spreads
- Important features determining price spread were identified through feature importance analysis
- The approach handles the challenges of working with financial market data, including outliers and variable relationships


## Conclusion

The Random Forest Regression model provides valuable insights for understanding and predicting price spreads in the Algerian market. This information could be useful for market analysts, retailers, and consumers seeking to understand price volatility and make informed decisions
This was my first ML project so i will appreciate any guidance, an article will be coming soon about my research ;)
