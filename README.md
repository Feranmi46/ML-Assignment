# California Housing Dataset Analysis

## Overview
This project explores, cleans, and analyzes the California Housing dataset. The dataset contains information about housing prices and related features such as location, number of rooms, and median income. The goal of this analysis is to build predictive models for estimating house prices using various regression algorithms.

## Steps Performed

### 1. Data Exploration and Cleaning
- Loaded the dataset and checked for missing values.
- Found 207 missing values in the `total_bedrooms` column and replaced them with the median value.
- Analyzed the correlation between features using a heatmap.
- Explored the impact of the categorical feature `ocean_proximity` on house prices.
- One-hot encoded `ocean_proximity` for numerical representation.

### 2. Data Splitting
- Defined independent variables (`X`) and the target variable (`y` - median house value).
- Split the dataset into **training (80%)** and **testing (20%)** sets.

### 3. Regression Models Applied
We implemented five regression algorithms:
- **Linear Regression**
- **Ridge Regression**
- **Lasso Regression**
- **Random Forest Regressor**
- **Gradient Boosting Regressor**

### 4. Model Performance Evaluation
We used three key metrics to evaluate model performance:
- **Mean Absolute Error (MAE)**: Measures the average absolute difference between actual and predicted values.
- **Mean Squared Error (MSE)**: Penalizes larger errors more than MAE.
- **R-Squared Score (R²)**: Measures how well the model explains the variance in the data.

### 5. Results
| Model               | MAE        | MSE          | R² Score  |
|--------------------|------------|------------|------------|
| Linear Regression | 50,670.74  | 4.91e+09  | 0.625  |
| Ridge Regression  | 50,680.63  | 4.91e+09  | 0.625  |
| Lasso Regression  | 50,670.88  | 4.91e+09  | 0.625  |
| Random Forest     | **31,639.37** | **2.40e+09** | **0.816**  |
| Gradient Boosting | 38,248.03  | 3.12e+09  | 0.762  |

**Best Model:** Random Forest Regressor with the highest R² score (0.816) and lowest error.

## Key Takeaways
- **`median_income`** was the most significant predictor of house prices.
- **Random Forest performed the best**, followed by Gradient Boosting.
- **Linear models (Linear, Ridge, Lasso)** had similar performance but were outperformed by ensemble methods.

## Next Steps
- Tune hyperparameters for Random Forest and Gradient Boosting for better performance.
- Try feature engineering (e.g., creating new ratios, log transformations).
- Use cross-validation techniques to further validate model performance.

## Technologies Used
- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn)
- **Jupyter Notebook** for exploratory analysis

## Author
This project was conducted as part of a machine learning analysis on the California Housing dataset.

