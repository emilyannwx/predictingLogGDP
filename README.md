# predictingLogGDP



## Project Overview

This project focuses on predicting the Log GDP per capita using the World Happiness Report (WHR) dataset. The objective is to develop a supervised learning regression model that can predict Log GDP based on various socioeconomic factors. Predicting Log GDP is crucial as it provides insights into which factors significantly influence economic growth, allowing governments and organizations to design policies or offer consulting services that enhance these factors, ultimately improving public welfare and economic stability.

## Data and Features

### Original Features:

- **Life ladder**
- **GINI index**
- **Social support**
- **Healthy life expectancy at birth**
- **Freedom to make life choices**
- **Generosity**
- **Perceptions of corruption**
- **GINI household income index**
- **Positive affect**
- **Negative affect**

### Selected Features:

- **Happiness** (Life ladder)
- **Support** (Social support)
- **Life** (Healthy life expectancy at birth)

### Feature Selection Process:

After analyzing the correlation between each feature and Log GDP, the following features were removed due to weak correlation:

* **Freedom to make life choices**
* **Generosity**
* **Perceptions of corruption**
* **Positive affect**
* **Negative affect**

### Data Preparation:

Renamed all features for clarity.
Dropped missing values to ensure data quality.
Standardized the data to maintain consistency in scale across all features.

## Model Selection
The model used for prediction is a **Multiple Linear Regression** model. The dataset was split into training and testing sets, with the model fitted on the training data and evaluated on the test data. The model's performance was assessed using the following metrics:

**Root Mean Square Error (RMSE)**: 0.45

**R-squared (R²) Score**: 0.80

## Regularization

To further refine the model, **Lasso Regression (L1 Regularization)** was applied. The coefficients obtained from the Lasso model are:

**Happiness**: 0.191853

**Support**: 0.160538

**Life**: 0.604768

These results indicate that all selected features contribute meaningfully to the prediction of Log GDP.

## Conclusion

Both the Multiple Linear Regression model and the Lasso Regression model yielded identical RMSE and R² scores. This consistency suggests that the chosen features—Happiness, Support, and Life—are indeed relevant and significant in predicting Log GDP. This model can be used by governments and organizations to identify and enhance factors that drive economic growth.

