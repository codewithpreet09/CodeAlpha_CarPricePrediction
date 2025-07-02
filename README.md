# CodeAlpha_CarPricePrediction 
# Car Price Prediction

This project focuses on building a machine learning model to predict car selling prices based on various features. The goal is to demonstrate a typical machine learning workflow, including data loading, preprocessing, feature engineering, model training, and evaluation.

## Dataset

The project uses the "car data.csv" dataset, which contains information about various cars, including their selling price, present price, driven kilometers, fuel type, selling type, transmission, owner, and manufacturing year.

## Project Steps

The following steps were performed in this project:

1.  **Data Loading and Initial Inspection:** The dataset was loaded into a pandas DataFrame. Missing values were checked (and none were found in this dataset).
2.  **Data Preprocessing (One-Hot Encoding):** Categorical features (`Car_Name`, `Fuel_Type`, `Selling_type`, `Transmission`) were converted into a numerical format using one-hot encoding to make them suitable for the machine learning model. The `drop_first=True` argument was used to avoid multicollinearity.
3.  **Feature Engineering:** A new feature, `no_of_years`, was created to represent the age of the car by subtracting the `Year` from the `current_year` (set to 2020).
4.  **Data Splitting:** The data was split into training and testing sets using `train_test_split` from scikit-learn. The `Selling_Price` was set as the target variable (`y`), and all other relevant features were used as predictors (`X`). The `Year` and `current_year` columns were dropped from the features as `no_of_years` was created.
5.  **Model Training:** A Linear Regression model from scikit-learn was initialized and trained on the training data (`X_train`, `y_train`).
6.  **Model Evaluation:** The trained model was evaluated on the test data (`X_test`, `y_test`) using common regression metrics:
    *   Mean Absolute Error (MAE)
    *   Mean Squared Error (MSE)
    *   R-squared (R2)

## Results

The Linear Regression model achieved the following evaluation metrics on the test set:

*   **Mean Absolute Error (MAE):**  2.0365174789895226
*   **Mean Squared Error (MSE):**   9.22109039145135
*   **R-squared (R2):**   0.5997023481939774


## Technologies Used

*   Python
*   Pandas
*   Scikit-learn

## How to Run the Code

1.  Download the `car data.csv` dataset.
2.  Open the provided Jupyter Notebook or Colab notebook.
3.  Ensure you have the necessary libraries installed (`pandas`, `sklearn`).
4.  Run the cells sequentially to load the data, preprocess, engineer features, train the model, and evaluate its performance.

---

