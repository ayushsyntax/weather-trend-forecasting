# Weather Trend Forecasting Assessment

> **PM Accelerator Mission:** *To help professionals identify their value, stand out, and advance their careers to land dream Product Management jobs.*

## Project Overview
This repository contains the completion of the PM Accelerator Tech Assessment for Weather Trend Forecasting. It involves comprehensive analysis and predictive modeling using the "Global Weather Repository" dataset. The project fulfills both the Basic and Advanced assessment requirements, focusing on descriptive observations and baselining model performance.

## Dataset
- **Source**: Global Weather Repository
- **Description**: Daily weather observations across multiple countries and cities, including standard meteorological data (temperature, precipitation, wind, pressure) and environmental air quality indices.

## Methodology
- **Data Cleaning & Preprocessing**: Missing numerical values were imputed via median and categorical values via mode. Extracted temporal features from timestamps.
- **Outlier Handling**: Utilized IQR (Interquartile Range) capping to handle extreme outliers in precipitation.
- **Scaling**: Standard scaling was applied to continuous features to optimize gradient-based learning.
- **Modeling**: Evaluated multiple models including Linear Regression, Random Forest, XGBoost, and an Ensemble Voting Regressor.
- **Advanced Techniques**: Employed Isolation Forest for anomaly detection and geospatial libraries for mapping continental climates.

## Results
- The XGBoost model achieved the highest test-set performance with an R² score of ~0.985.
- Continent-level aggregations clearly highlighted spatial temperature distributions.
- Air quality metrics (like PM2.5) exhibited statistically significant negative correlations with wind speed.

## Key Findings
- **Forecasting is highly accurate**: Tree-based models (XGBoost) strongly predict test-set weather.
- **Feature Dominance**: The model relies almost entirely on `feels_like_celsius`.
- **Anomalies can be flagged**: Statistical algorithms isolated extreme multi-variate atmospheric readings.
- **Environment correlation**: Lower wind speeds correlate with reduced air quality.

## Project Limitations
- Feature importance is dominated by `feels_like_celsius`.
- Isolation Forest detects statistical anomalies only.
- Correlations do not imply causation.
- Results are limited to the dataset used in this project.

## Repository Structure
```text
weather-trend-forecasting/
├── README.md
├── requirements.txt
├── .gitignore
├── data/
│   └── GlobalWeatherRepository.csv
├── notebooks/
│   ├── 01_weather_forecasting.ipynb
│   └── 02_advanced_analysis.ipynb
├── outputs/
│   └── figures/
├── reports/
│   └── project_report.md
└── presentation/
    └── Weather_Trend_Forecasting_Consulting.pptx
```

## Installation & How To Run

1. **Clone the repository:**
   ```bash
   git clone <your-repo-link>
   cd weather-trend-forecasting
   ```

2. **Create a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Notebooks:**
   Start Jupyter Notebook to explore the code interactively:
   ```bash
   jupyter notebook
   ```

## Demo Video
[Link to Demo Video will be inserted here]
