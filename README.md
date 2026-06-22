# 🌤️ Weather Trend Forecasting

[![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-orange?style=flat-square&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Machine Learning](https://img.shields.io/badge/Machine%20Learning-scikit--learn%20%7C%20XGBoost-yellow?style=flat-square)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

> **PM Accelerator Mission:** *To help professionals identify their value, stand out, and advance their careers to land dream Product Management jobs.*

---

## 📑 Table of Contents
- [Project Overview](#-project-overview)
- [Dataset](#-dataset)
- [Tech Stack](#-tech-stack)
- [Methodology](#-methodology)
- [Key Findings](#-key-findings)
- [Project Limitations](#-project-limitations)
- [Repository Structure](#-repository-structure)
- [Installation](#-installation)
- [Demo Video](#-demo-video)
- [Submission Checklist](#-submission-checklist)
- [Author Info](#-author-info)
- [License](#-license)

---

## 🎯 Project Overview
Welcome to the **Weather Trend Forecasting** project! This repository contains the complete submission for the **PM Accelerator Tech Assessment (Product Management)**. The project focuses on data storytelling, comprehensive analysis, and predictive modeling using historical global weather data to generate actionable insights and robust temperature forecasts.

## 📊 Dataset
The dataset utilized in this project is the **[Global Weather Repository](https://www.kaggle.com/datasets/nelgiriyewithana/global-weather-repository)** available on Kaggle.

- **Size:** 148,515 rows × 41 features
- **Source:** Kaggle
- **Scope:** Global weather metrics ranging from temperature and humidity to wind speeds and air quality.

## 🛠️ Tech Stack
This project leverages a modern data science tech stack:
- **Languages:** Python
- **Data Manipulation:** `pandas`, `numpy`
- **Machine Learning:** `scikit-learn` (Linear Regression, Random Forest, Isolation Forest, StandardScaler, VotingRegressor), `XGBoost`
- **Data Visualization:** `matplotlib`, `seaborn`

## 🧪 Methodology
The project is divided into two comprehensive Jupyter Notebooks, progressively moving from basic exploratory data analysis to advanced machine learning models.

### 1. `01_weather_forecasting.ipynb` (Basic)
- **Data Cleaning:** Handled missing values, standardized formats, and optimized data types.
- **Exploratory Data Analysis (EDA):** Visualized distributions, identified correlations, and explored seasonality.
- **Baseline Modeling:** Trained initial Linear Regression and Random Forest models to establish a performance baseline.

### 2. `02_advanced_analysis.ipynb` (Advanced)
- **Anomaly Detection:** Utilized **Isolation Forest** to identify extreme weather events.
- **Climate Analysis:** Deep dive into broader climate trends and seasonal patterns.
- **Feature Importance:** Analyzed which variables contribute most to accurate temperature predictions.
- **Spatial Analysis:** Explored geographical variations in weather patterns.
- **Advanced Modeling:** Implemented **XGBoost** and ensemble methods for optimized forecasting.

## 📈 Key Findings

| Metric/Insight | Result | Details |
| --- | --- | --- |
| **Best Model** | **XGBoost** | **R² = 0.985, RMSE = 1.18, MAE = 0.43** |
| **Model Improvement** | **43% Reduction** | 43% RMSE reduction compared to the baseline Linear Regression model. |
| **Anomalies Detected** | **1,485 Events** | Detected extreme weather events comprising 1% of the data using Isolation Forest. |

## ⚠️ Project Limitations
- **Circular Feature Issue:** The dataset includes a `feels_like_celsius` feature, which acts as a circular reference (leakage) when predicting actual temperature. While it artificially inflates model accuracy, mitigating this required careful feature selection in advanced modeling stages.

## 📂 Repository Structure
```text
weather-trend-forecasting/
├── data/
│   └── GlobalWeatherRepository.csv  # Dataset (Not included in repo, download from Kaggle)
├── notebooks/
│   ├── 01_weather_forecasting.ipynb # Basic EDA & Baseline Models
│   └── 02_advanced_analysis.ipynb   # Advanced Modeling & Anomaly Detection
├── outputs/                         # Generated plots and tables
├── presentation/                    # Slide decks or presentation materials
├── reports/                         # Final reports
├── requirements.txt                 # Project dependencies
├── .gitignore
└── README.md                        # Project documentation
```

## ⚙️ Installation

To run this project locally, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ayushsyntax/weather-trend-forecasting.git
   cd weather-trend-forecasting
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python -m venv venv
   # On Windows
   venv\Scripts\activate
   # On Mac/Linux
   source venv/bin/activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Download the Dataset:**
   - Download the dataset from [Kaggle](https://www.kaggle.com/datasets/nelgiriyewithana/global-weather-repository).
   - Place the CSV file in the `data/` directory.

5. **Run the Notebooks:**
   ```bash
   jupyter notebook
   ```

## 🎥 Demo Video
Watch the project walkthrough and demo here:
**[YouTube Demo Video](https://youtu.be/CqGPecOg9YA)**


## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
