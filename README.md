# Retail Demand Forecasting using Machine Learning

## Project Overview

This project focuses on forecasting weekly retail demand using historical sales data and machine learning techniques. Accurate demand forecasting enables retailers to optimize inventory management, reduce stock shortages, minimize overstocking costs, and improve business decision-making.

The project follows a complete data science pipeline, including data ingestion, exploratory data analysis (EDA), data preprocessing, feature engineering, model development, evaluation, and model selection.

Three machine learning models were developed and compared:

* Linear Regression (Baseline Model)
* XGBoost Regressor
* Random Forest Regressor

Hyperparameter tuning was performed on the XGBoost model using **GridSearchCV** with **TimeSeriesSplit** cross-validation to improve forecasting performance.

The models were evaluated using multiple regression metrics, including:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* Mean Absolute Percentage Error (MAPE)
* R² Score
* Weighted Mean Absolute Error (WMAE)

Based on the evaluation results, **XGBoost Regressor** was selected as the best-performing model because it achieved the lowest prediction errors and the highest R² score.

---

# Project Objectives

The primary objectives of this project are:

* Forecast weekly retail sales accurately.
* Analyze historical sales trends and seasonal demand patterns.
* Compare multiple machine learning algorithms.
* Select the most suitable forecasting model based on evaluation metrics.
* Support inventory planning and retail business decision-making.

---

# Technologies Used

## Programming Language

* Python 3.x

## Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost

## Machine Learning Models

* Linear Regression
* XGBoost Regressor
* Random Forest Regressor

## Validation Technique

* TimeSeriesSplit (5-Fold Cross Validation)

---

# Project Folder Structure

```
Retail_Demand_Forecasting/
│
├── data/
│   └── retail_demand_dataset.csv
│
├── notebooks/
│   └── Retail_Demand_Forecasting.ipynb
│
├── reports/
│   ├── Process_Flow_Document.pdf
│   ├── Best_Model_Selection_Report.pdf
│   └── Final_Project_Report.pdf
│
├── results/
│   ├── Model_Evaluation.xlsx
│   ├── Prediction_Results.csv
│   └── Feature_Importance.png
│
├── README.md
└── requirements.txt
```

---

# Dataset Description

The dataset contains historical retail information used for forecasting weekly sales.

Important attributes include:

* Store
* Department
* Date
* Weekly Sales
* IsHoliday
* Temperature
* Fuel Price
* CPI
* Unemployment

Target Variable:

**Weekly Sales**

---

# Data Science Workflow

The project follows the workflow below:

1. Data Ingestion
2. Exploratory Data Analysis (EDA)
3. Data Cleaning & Transformation
4. Feature Engineering
5. Feature Selection
6. TimeSeriesSplit Cross Validation
7. Model Training
8. Hyperparameter Tuning
9. Model Evaluation
10. Performance Comparison
11. Prediction
12. Best Model Selection

---

# Setup Instructions

## Step 1: Clone or Download the Project

Download the project files and place them in a working directory.

---

## Step 2: Install Required Libraries

Install the required Python packages using:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

Or install all dependencies from:

```bash
pip install -r requirements.txt
```

---

## Step 3: Launch Jupyter Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```
Retail_Demand_Forecasting.ipynb
```

---

## Step 4: Load the Dataset

Ensure the dataset is placed inside the **data/** folder.

Example:

```python
import pandas as pd

df = pd.read_csv("data/retail_demand_dataset.csv")
```

---

## Step 5: Run the Notebook

Execute all notebook cells sequentially.

The notebook automatically performs:

* Data loading
* Data validation
* EDA
* Data preprocessing
* Feature engineering
* TimeSeriesSplit cross-validation
* Model training
* Hyperparameter tuning
* Model evaluation
* Prediction generation

---

# How to Reproduce the Results

To reproduce the project results, follow these steps:

1. Install all required Python libraries.
2. Place the dataset inside the **data/** directory.
3. Open the Jupyter Notebook.
4. Execute all cells from top to bottom without skipping any steps.
5. The notebook will:

   * Load and preprocess the dataset.
   * Perform feature engineering.
   * Apply TimeSeriesSplit (5-fold cross-validation).
   * Train the Linear Regression, XGBoost, and Random Forest models.
   * Perform hyperparameter tuning on the XGBoost model.
   * Evaluate all models using MAE, RMSE, MAPE, R² Score, and WMAE.
   * Compare model performance.
   * Select the best-performing model.
   * Generate demand predictions and evaluation outputs.

Following these steps will reproduce the same workflow and comparable results obtained in this project.

---

# Model Evaluation Metrics

The models are evaluated using the following metrics:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* Mean Absolute Percentage Error (MAPE)
* R² Score
* Weighted Mean Absolute Error (WMAE)

These metrics provide a comprehensive assessment of prediction accuracy and model performance.

---

# Best Model

After comparing all developed models, **XGBoost Regressor** was selected as the final forecasting model because it demonstrated:

* Lowest MAE
* Lowest RMSE
* Lowest WMAE
* Highest R² Score
* Excellent ability to capture nonlinear demand patterns

The selected model provides accurate forecasts suitable for retail inventory planning and business decision-making.

---

# Future Improvements

Potential enhancements include:

* Incorporating external features such as weather, public holidays, and competitor pricing.
* Exploring advanced forecasting models such as LightGBM, CatBoost, Prophet, and LSTM.
* Applying advanced hyperparameter optimization techniques such as Optuna or Bayesian Optimization.
* Developing an automated model retraining pipeline.
* Deploying the forecasting model as a web application or REST API for real-time predictions.

---

# Conclusion

This project demonstrates a complete machine learning pipeline for retail demand forecasting, from data preprocessing to model deployment preparation. By comparing multiple regression algorithms and selecting the best-performing model, the project provides an effective solution for forecasting weekly retail sales and supporting inventory management decisions.
