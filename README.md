# CO-Injection-Rate-Optimization
A machine learning repository for predicting CO₂ Injection Rates for Carbon Capture and Storage

# Overview

This project focuses on predicting the CO2 injection rate using historical data. The dataset contains various sensor readings such as pressure, temperature, and CO2 vent rate, along with timestamps. The project utilizes machine learning techniques, particularly XGBoost, to analyze and forecast CO2 injection rates over time.

Dataset

The dataset includes:

Time-based data with timestamps.

Sensor readings including wellhead pressure, temperature, and CO2 vent rate.

Derived features such as interaction terms and rolling means.

Files:

CO2_Injection_rate_train.csv: Training data.

CO2_Injection_rate_test.csv: Test data.

Preprocessing Steps

Handling DateTime:

Converted Date Time to a datetime format.

Extracted hour, day, month, year, day_of_week, and weekend indicators.

Missing Values:

Forward-filled missing values.

Feature Engineering:

Created interaction features (e.g., pressure * temperature).

Computed rolling mean of CO2 vent rate.

Derived mean pressure values by weekend/weekday.

Model Training

Algorithm: XGBoost Regressor.

Validation: TimeSeriesSplit.

Hyperparameter Tuning: GridSearchCV.

Evaluation Metrics

Mean Squared Error (MSE)

Mean Absolute Error (MAE)

R-Squared Score (R²)

Dependencies

Install the necessary libraries using:

pip install pandas numpy matplotlib seaborn xgboost scikit-learn

Usage

Run the preprocessing and model training script:

python train_model.py

Author

[Rahan Fardin Amio]

