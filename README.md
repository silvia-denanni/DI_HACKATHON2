# Job Market Insights Dashboard Predictions

## Overview
This project provides an in-depth analysis of job market data, focusing on salary prediction and identifying key trends within various industries. It leverages machine learning models to predict `normalized_salary` based on job-related features, offering valuable insights for job seekers, employers, and market analysts.

## Problem Solved
The primary problem addressed by this project is the lack of clear, data-driven insights into salary expectations across different job roles and industries. By building and evaluating multiple regression models, this project aims to:
*   **Demystify Salary Expectations**: Provide predicted salary ranges based on job attributes.
*   **Identify High-Paying Sectors**: Highlight industries with the highest average salaries.
*   **Understand Job Market Dynamics**: Analyze factors influencing job applications and overall market trends.
*   **Evaluate Predictive Models**: Compare the effectiveness of different machine learning algorithms for salary prediction.

## Features

### Data Loading and Preprocessing
*   Loads job market data from an Excel file (`Job Market Insights Dashboard.xlsx`).
*   Initial inspection of data shape, columns, and basic statistics.
*   Handles missing values in critical columns like `application_url` and `description`.

### Exploratory Data Analysis (EDA)
*   Identifies the top and bottom 5 industries based on mean `normalized_salary`.
*   Calculates mean job listing posting and expiry times.
*   Analyzes the most and least applied-for industries.

### Machine Learning Models for Salary Prediction
The project trains and evaluates several regression models to predict `normalized_salary`:

1.  **Linear Regression Model N1**: Predicts salary using `state` (LabelEncoded) and `title` (TF-IDF vectorized) features.
2.  **Random Forest Regressor Model**: Serves as a comparison to Linear Regression N1, using the same feature set.
3.  **Linear Regression Model N2**: Predicts salary using `state`, `industry_type`, and `formatted_work_type` (all LabelEncoded) features.
4.  **Gradient Boosting Regressor Model**: Serves as a comparison to Linear Regression N2, using the same feature set.
5.  **Linear Regression Model with One-Hot Encoded Features**: Predicts salary using `state`, `industry_type`, and `formatted_work_type` (all One-Hot Encoded) features.

### Model Evaluation and Comparison
*   Evaluates each model using R-squared (R2) score, Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE).
*   Provides a side-by-side comparison of all trained models to assess their performance.
*   Offers insights into why certain models perform better or worse and suggests next steps for improvement.

## How to Run It (on someone else’s computer)

To replicate and run this project on your local machine, follow these steps:

### Prerequisites
*   Python 3.x
*   `pip` (Python package installer)

### Installation
1.  **Clone the repository**:
    ```bash
    git clone https://github.com/your-username/Job-Market-Insights.git
    cd Job-Market-Insights
    ```
    *(Note: Replace `your-username/Job-Market-Insights.git` with the actual GitHub repository URL once available.)*

2.  **Create a virtual environment (recommended)**:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install dependencies**:
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn openpyxl
    ```

### Data
*   Place your `Job Market Insights Dashboard.xlsx` file in the root directory of the cloned repository, or update the `pd.read_excel()` path in the notebook to point to your data file.

### Execution
1.  **Open the Jupyter Notebook (or Google Colab)**:
    You can open the `.ipynb` file using Jupyter Notebook or JupyterLab.
    ```bash
    jupyter notebook
    ```
    Navigate to `Job Market Insights Dashboard Predictions.ipynb` and open it.

2.  **Run all cells**: Execute all cells in the notebook sequentially. This will load the data, perform EDA, train the models, and display the evaluation results.

