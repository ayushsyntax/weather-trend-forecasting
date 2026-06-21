# Weather Trend Forecasting Project Report

> **PM Accelerator Mission:** *To help professionals identify their value, stand out, and advance their careers to land dream Product Management jobs.*

## 1. Project Overview
This report summarizes the methodology and findings of the End-to-End Machine Learning Assessment using the Global Weather Repository. The objective was to clean, preprocess, and model meteorological data to establish baseline predictive performance.

## 2. Methodology
- **Data Preprocessing**: Missing numerical values were imputed via median and categorical values via mode. Extreme precipitation values were capped using an Interquartile Range (IQR) method (1.5x) to limit outlier influence.
- **Feature Engineering**: Extracted temporal features from timestamps. Categorical features were encoded for machine learning compatibility. Standard scaling was applied to all numerical inputs.
- **Forecasting Models**: Evaluated `Linear Regression`, `Random Forest`, `XGBoost`, and a `Voting Regressor` Ensemble.
- **Advanced Analysis**: Applied `Isolation Forest` for multivariate anomaly detection and `XGBoost` for feature importance extraction.

## 3. Results and Metrics
- **Performance**: The `XGBoost` model achieved the strongest test-set performance, yielding an R² score of ~0.985.
- **Feature Importance**: `feels_like_celsius` accounted for >90% of the model's predictive weight, functioning as a highly correlated proxy for the target variable `temperature_celsius`. Humidity (~6%) was the only other notable contributor.
- **Anomaly Detection**: `Isolation Forest` successfully flagged 1% of the dataset as statistical outliers (primarily points exhibiting extreme pressure/temperature variance).

## 4. Limitations
- Feature importance is dominated by `feels_like_celsius`.
- Isolation Forest detects statistical anomalies only, which may not correspond to physical severe weather events without domain labeling.
- Environmental correlations (e.g., wind speed and PM2.5) do not imply causation.
- Results are limited specifically to the spatiotemporal distribution of the dataset used in this project.
