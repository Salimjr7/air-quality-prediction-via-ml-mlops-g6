# Predicting Air Quality for Sustainable Urban Living

A comparative machine learning project that predicts the Air Quality Index (AQI) for major Turkish cities using classical regression models and deep learning approaches. The notebook compares K-Nearest Neighbors, Linear Regression, Support Vector Regression, LSTM, and a CNN-LSTM hybrid to show how model choice affects performance on structured environmental data.

The best result in this project came from Linear Regression, which achieved a test R2 of 72.28%. That outcome is a useful reminder that simpler models can outperform deeper architectures when the dataset is moderate in size and the relationships are close to linear.

## What’s Inside

- `air_quality_prediction.ipynb` - the full ML workflow, including data loading, exploratory data analysis, preprocessing, model training, evaluation, visualizations, and a live prediction section.
- `16_air_quality_prediction.csv` - the dataset used for training and testing.
- `results/` - charts comparing model performance, predictions, AQI distribution, and feature correlations.
- `mlflow_screenshots/` - dashboard screenshots captured during experimentation.
- `Project Documentation.pdf` - the full project report.

## Dataset Overview

- Rows: 1,460
- Columns: 6
- Cities: Istanbul, Ankara, Izmir, Bursa
- Features: date, location, pm2.5, pm10, temperature, predicted_aqi

## Models Compared

1. K-Nearest Neighbors Regression
2. Linear Regression
3. Support Vector Regression
4. LSTM
5. CNN-LSTM Hybrid

## How to Run

1. Place the notebook and dataset in the same folder.
2. Install the required packages:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow keras jupyter
```

3. Launch Jupyter:

```bash
jupyter noteboo
```

4. Open `air_quality_prediction.ipynb` and run all cells in order.

The live prediction section lets you test custom PM2.5, PM10, temperature, city, and date values to generate AQI predictions and EPA category labels.

## Project Goal

This repository is intended to support academic evaluation and practical experimentation with AQI forecasting. It combines a clean comparison of classical and neural models with visual outputs that make the results easy to review.
