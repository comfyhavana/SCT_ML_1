# Ames House Price Prediction

## Project Overview
This project implements a machine learning model to predict residential property sales prices using the Ames Housing dataset. By utilizing feature engineering and a Linear Regression architecture, the model establishes a baseline for estimating real estate values based on core structural dimensions.

## Dataset
The dataset utilized is the Ames Housing dataset, commonly associated with competitive machine learning benchmarks. It contains 81 explanatory variables describing various aspects of residential homes.

## Feature Engineering
To optimize the Linear Regression model and prevent sparsity issues, specific structural columns were aggregated into comprehensive metrics. Missing values within these selected features were handled via median imputation to ensure data integrity during training.

The model relies on the following engineered features:
* **`Total_Area`**: An aggregation of above-grade living area (`GrLivArea`) and total basement square footage (`TotalBsmtSF`).
* **`Total_Baths`**: A weighted calculation of all property bathrooms, combining above-grade and basement full/half baths.
* **`BedroomAbvGr`**: The total number of bedrooms located above the basement level.

## Model Architecture & Evaluation
A standard **Linear Regression** algorithm was trained using an 80/20 train-validation split. 

**Validation Performance Metrics:**
* **R² Score:** 0.7205
* **Interpretation:** The model successfully explains 72.05% of the variance in house prices using only the three engineered spatial features (Area, Bedrooms, Bathrooms).

## Technologies Used
* **Python 3**
* **Pandas:** Data manipulation, aggregation, and imputation.
* **NumPy:** Mathematical operations and RMSE calculations.
* **Scikit-Learn:** Model building (`LinearRegression`), data splitting (`train_test_split`), and evaluation metrics (`r2_score`, `mean_squared_error`).
* **Matplotlib:** Visualization of actual versus predicted price distributions.

## Usage

1. Clone the repository.
2. Ensure `train.csv` and `test.csv` are located in the root directory.
3. Install the required dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib