# CO2-Injection-Rate-Optimization
A machine learning repository for predicting CO₂ Injection Rates for Carbon Capture and Storage

## Overview

This project focuses on predicting the CO2 injection rate using historical data. The dataset contains various sensor readings such as pressure, temperature, and CO2 vent rate, along with timestamps. The project utilizes machine learning techniques, particularly XGBoost, to analyze and forecast CO2 injection rates over time.

## Dataset

The dataset includes:

1. Time-based data with timestamps.

2. Sensor readings including wellhead pressure, temperature, and CO2 vent rate.

3. Derived features such as interaction terms and rolling means.

## Files:

1. CO2_Injection_rate_train.csv: Training data.

2. CO2_Injection_rate_test.csv: Test data.

## Preprocessing Steps

### Handling DateTime:

1. Converted Date Time to a datetime format.

2. Extracted hour, day, month, year, day_of_week, and weekend indicators.

### Missing Values:

1. Forward-filled missing values.

### Feature Engineering:

1. Created interaction features (e.g., pressure * temperature).

2. Computed rolling mean of CO2 vent rate.

3. Derived mean pressure values by weekend/weekday.

### Model Training

1. Algorithm: XGBoost Regressor.

2. Validation: TimeSeriesSplit.

3. Hyperparameter Tuning: GridSearchCV.

4. Evaluation Metrics: Mean Squared Error (MSE), R-Squared Score (R²)

### Install the necessary libraries using:
```
pip install pandas numpy matplotlib seaborn xgboost scikit-learn
```

Run the preprocessing and model training script:

```
python train_model.py
```

Author

Rahan Fardin Amio
