# WEATHER TREND FORECASTING

![Python](https://img.shields.io/badge/Python-3.x-black?style=flat-square&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-black?style=flat-square&logo=jupyter&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-scikit--learn%20%7C%20XGBoost-black?style=flat-square)

> **PM Accelerator Mission:** *To help professionals identify their value, stand out, and advance their careers to land dream Product Management jobs.*

---

## TABLE OF CONTENTS
- [PROJECT OVERVIEW](#project-overview)
- [DATASET](#dataset)
- [TECH STACK](#tech-stack)
- [METHODOLOGY](#methodology)
- [KEY FINDINGS & RESULTS](#key-findings--results)
- [PROJECT LIMITATIONS](#project-limitations)
- [REPOSITORY STRUCTURE](#repository-structure)
- [INSTALLATION](#installation)

---

## PROJECT OVERVIEW
This repository contains the completion of the PM Accelerator Tech Assessment for Weather Trend Forecasting. It involves comprehensive analysis, data storytelling, and predictive modeling using historical global weather data.

The project fulfills both the Basic and Advanced assessment requirements by focusing on descriptive observations, baseline model performance, and advanced techniques such as anomaly detection and spatial analysis.

## DATASET
- **Source:** Global Weather Repository
- **Description:** Daily weather observations across multiple countries and cities. Features include standard meteorological data (temperature, precipitation, wind speed, atmospheric pressure) and environmental indices (air quality, UV index).

## TECH STACK
This project leverages the following core libraries:
- **Data Manipulation:** `pandas`, `numpy`
- **Machine Learning:** `scikit-learn` (Linear Regression, Random Forest, Isolation Forest), `xgboost`
- **Data Visualization:** `matplotlib`, `seaborn`
- **Geospatial & Utils:** `pycountry-convert`

## METHODOLOGY
Our approach is divided into two main notebooks, moving from basic assessment to advanced analysis:

1. **Data Cleaning & Preprocessing:**
   - Imputed missing numerical values via the median and categorical values via the mode.
   - Extracted temporal features (Year, Month, Day) from timestamps.
2. **Outlier Handling:**
   - Utilized IQR (Interquartile Range) capping to handle extreme outliers in precipitation, preventing skew in our linear models.
3. **Scaling:**
   - Standard scaling was applied to continuous features to optimize gradient-based learning.
4. **Modeling:**
   - Evaluated multiple models including a Baseline Linear Regression, Random Forest, XGBoost, and an Ensemble Voting Regressor.
5. **Advanced Techniques:**
   - Employed Isolation Forests for multivariate anomaly detection (identifying extreme weather events).
   - Mapped continental climate zones and correlated environmental factors with weather stagnation.

## KEY FINDINGS & RESULTS

| CATEGORY | INSIGHT |
|---|---|
| **Forecasting Accuracy** | Tree-based models (XGBoost & Random Forest) heavily outperformed linear baselines, achieving a test-set R² score of ~0.985. |
| **Feature Dominance** | The model relies almost entirely on `feels_like_celsius` to predict ambient temperature, with humidity and UV index acting as secondary drivers. |
| **Anomaly Detection** | Statistical algorithms successfully isolated extreme atmospheric readings (e.g., severe low-pressure / high-temperature combinations). |
| **Environmental Impact** | Lower wind speeds (atmospheric stagnation) showed a statistically significant correlation with reduced air quality and visibility. |

## PROJECT LIMITATIONS
- **Feature Redundancy:** Feature importance is dominated by `feels_like_celsius`, which is mathematically derived from the target variable (`temperature_celsius`).
- **Anomaly Detection Limits:** The Isolation Forest detects statistical anomalies only; it does not confirm meteorological significance without domain expert review.
- **Causation vs. Correlation:** Observed correlations (like wind vs. air quality) do not inherently imply causation.
- **Dataset Scope:** Results are limited to the temporal and geographical scope of the provided dataset.

## REPOSITORY STRUCTURE
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

## INSTALLATION

1. **Clone the repository:**
   ```bash
   git clone <your-repo-link>
   cd weather-trend-forecasting
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv venv
   # Windows: venv\Scripts\activate
   # macOS/Linux: source venv/bin/activate
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Notebooks:**
   ```bash
   jupyter notebook
   ```
