# Feature Importance Analysis


# Overview
This repository focuses on building and training a machine learning model, specifically a RandomForestRegressor, to estimate stock levels based on sales, sensor, and timestamp data.

Key Steps:
## 1. Data Preprocessing:
- Importing Libraries: Standard Python libraries like pandas, numpy, and scikit-learn are imported.
- Loading the Dataset: Three datasets (df_sales, df_stock, and df_sensor) are loaded, and unnecessary columns are dropped.
- Understanding the Data: Basic information about the datasets is explored.
## 2. Data Transformation:
- Convert Timestamps: Timestamp columns in all three datasets are converted to datetime format.
- Hourly Timestamps: The timestamps are further converted into hourly intervals.
## 3. Dataset Merging:
- The three datasets are aggregated based on timestamps and product IDs and then merged into a single dataset (merged_df).
## 4. Feature Engineering:
- Additional features are engineered, such as day of the month, day of the week, and hour from the timestamp.
- Dummy variables are created for the 'category' feature using one-hot encoding.
## 5. Model Training:
- The dataset is split into features (X) and the target variable (y), which is the estimated stock percentage.
- A loop runs for K (10) folds to train and evaluate the model.
- Random Forest Regressor and Linear Regression models are used.
## 6. Model Evaluation:
- The mean absolute error (MAE) is calculated for each fold to evaluate model performance.
- The average MAE across all folds is printed as a measure of the model's overall accuracy.
## 7. Feature Importance Analysis:
- Feature importances are calculated using the trained Random Forest Regressor model.
- A bar plot is generated to visualize the relative importance of each feature in predicting stock levels.
3 Results:
The code provides insights into feature importance and model accuracy, offering a foundation for further analysis and improvements.
