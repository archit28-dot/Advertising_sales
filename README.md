# Advertising Sales Prediction with Linear Regression

This notebook demonstrates the process of building and evaluating a Linear Regression model to predict sales based on advertising spend across different media channels (TV, Radio, Newspaper).

## Project Overview

The goal of this project is to understand the relationship between advertising expenditure and sales, and to develop a predictive model that can estimate future sales based on marketing budgets.

## Dataset

The dataset used for this project is `Advertising.csv`, which contains information on advertising budgets for TV, radio, and newspaper, along with corresponding sales figures.

## Key Steps

1.  **Data Loading and Exploration**: The dataset is loaded using pandas, and initial exploratory data analysis (EDA) is performed through scatter plots and pair plots to visualize relationships between features and sales.
2.  **Data Preprocessing**: The features (`X`) and target variable (`y`) are separated. The data is then split into training and testing sets to evaluate the model's performance on unseen data.
3.  **Model Training**: A `LinearRegression` model from `sklearn` is initialized and trained on the training data.
4.  **Model Evaluation**: The trained model's performance is assessed using common regression metrics: Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE). Residual plots are also used to check the model's assumptions.
5.  **Coefficients Analysis**: The coefficients of the linear regression model are inspected to understand the impact of each advertising medium on sales.
6.  **Model Persistence**: The trained model is saved to a file (`sales_model.joblib`) using `joblib` for future use, and then reloaded to demonstrate its functionality.

## Model Performance

After training, the model achieved the following performance metrics on the test set:

*   **Mean Absolute Error (MAE)**: `1.21` (approximately)
*   **Mean Squared Error (MSE)**: `2.30` (approximately)
*   **Root Mean Squared Error (RMSE)**: `1.52` (approximately)

The average sales value in the dataset is `14.02`, indicating that the RMSE is relatively low compared to the mean sales, suggesting a reasonable predictive accuracy.

## Model Coefficients

The coefficients indicate the estimated change in sales for a one-unit increase in advertising spend, holding other factors constant:

*   **TV**: `0.0458`
*   **Radio**: `0.1885`
*   **Newspaper**: `-0.0010`

This suggests that radio advertising has the highest positive impact on sales, followed by TV. Newspaper advertising shows a very small negative coefficient, implying a negligible or slightly negative impact within this model.

## How to Run the Notebook

1.  Ensure you have `numpy`, `pandas`, `matplotlib`, `seaborn`, and `scikit-learn` installed.
2.  Download the `Advertising.csv` dataset and place it in the same directory as the notebook.
3.  Run all cells in the notebook sequentially.
