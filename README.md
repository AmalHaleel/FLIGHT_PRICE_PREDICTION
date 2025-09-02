# FLIGHT_PRICE_PREDICTION

  Overview

This project predicts flight ticket prices using Machine Learning regression models.
It includes data preprocessing, feature engineering, model training, and evaluation with multiple algorithms.
The final model, Random Forest Regressor, achieved an R² score of 0.9477, explaining ~95% of the price variance.

  Dataset

Rows: 10,683
Target: Price (flight fare)
Features: Airline, Source, Destination, Route, Total_Stops, Duration, Date_of_Journey, Additional_Info, etc.
Preprocessed to handle missing values, inconsistent formats, and feature extraction from dates/times.

  Approach

Data Preprocessing

Handled missing values (Route, Total_Stops).

Standardized text (e.g., "No Info" → "No info").

Extracted Day, Month, Year, Dep_Hour, Arrival_Hour, Duration_mins.

Derived features: is_weekend, is_overnight.

Feature Engineering & Encoding

Converted categorical features with OneHotEncoding.

Scaled numerical features where needed.

Used ColumnTransformer and Pipeline for clean preprocessing.


  Modeling

Trained multiple regression models:

Linear Regression

Random Forest Regressor

XGBoost Regressor

Ridge Regression

  Evaluation Metrics:

R² score, Cross-Validation

 Visualizations:

Predicted vs Actual prices, Error distribution, Feature importance.

  Results
 
Model	R² Score	CV Mean Score
Linear Regression	0.7017	–
Random Forest Regressor	0.9477	0.9463
XGBoost Regressor	0.9477	–
Ridge Regression	0.9477	–

Conclusion
Flight prices are strongly influenced by duration, number of stops, airline, and travel month.
Random Forest provided the best performance, explaining ~95% of price variance.
The model can be extended by including seasonal data, holiday schedules, and demand patterns for further improvement.
Best Model: Random Forest Regressor (R² = 0.9477)


