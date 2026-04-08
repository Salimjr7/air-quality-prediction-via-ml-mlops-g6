================================================================================
        PREDICTING AIR QUALITY FOR SUSTAINABLE URBAN LIVING
        A Comparative Study of Classical and Deep Learning Models
================================================================================

  Submitted by : Group 6
  Course       : Introduction to Machine Learning 
  Instructor   : Mr. Tesfaye M.
  Date         : May 26, 2026 G.C.
  Institution  : AASTU / Software Engineering

================================================================================
  PROJECT OVERVIEW
================================================================================

This project develops and compares five machine learning regression models for
predicting the Air Quality Index (AQI) in four major Turkish cities: Istanbul,
Ankara, Izmir, and Bursa. The models evaluated are:

    1. K-Nearest Neighbors Regression   (KNN)
    2. Linear Regression                (LR)
    3. Support Vector Regression        (SVR)
    4. Long Short-Term Memory Network   (LSTM)
    5. CNN-LSTM Hybrid Network          (CNN-LSTM)

The best-performing model was Linear Regression with a test R² of 72.28%,
demonstrating that classical approaches can outperform deep learning when the
dataset is structured, moderate in size, and exhibits near-linear feature
relationships.

================================================================================
  REPOSITORY CONTENTS
================================================================================

  air_quality_prediction.ipynb       Main Jupyter Notebook containing the
                                      complete ML pipeline: data loading,
                                      EDA, preprocessing, model training,
                                      evaluation, visualizations, and a
                                      live prediction interface.

  16_air_quality_prediction.csv       Dataset used for training and testing.
                                      1,460 records | 6 columns | 4 cities
                                      No missing values | No duplicates

  
  documentation.pdf                 PDF version of the full project report.
                                      Recommended for reading — renders
                                      consistently on all devices.

  results/
    model_comparison.png              Grouped bar chart comparing MAE, MSE,
                                      RMSE, and R² across all five models.
    training_accuracy.png             Bar chart of training R² scores.
    testing_accuracy.png              Bar chart of testing R² scores.
    predictions_vs_actual.png         Line plot of all model predictions
                                      overlaid against actual AQI values.
    actual_vs_predicted_scatter.png   Scatter plots (actual vs predicted)
                                      for each of the five models.
    aqi_distribution.png              Histogram of AQI distribution with
                                      EPA category band overlays.
    correlation_heatmap.png           Pearson correlation heatmap of all
                                      engineered features.
  
  mlflow_screenshots/                 dashboard screenshot

  README.txt                          This file.

================================================================================
  DATASET DESCRIPTION
================================================================================

  File    : 16_air_quality_prediction.csv
  Rows    : 1,460
  Columns : 6

  Columns:
    date            - Date of observation       (YYYY-MM-DD format)
    location        - City name                 (Istanbul / Ankara / Izmir / Bursa)
    pm2.5           - Fine particulate matter   (µg/m³, continuous)
    pm10            - Coarse particulate matter (µg/m³, continuous)
    temperature     - Ambient temperature       (°C, continuous)
    predicted_aqi   - Air Quality Index         (Target variable, continuous)

  AQI Statistics:
    Mean   : 44.49
    Std    : 9.54
    Min    : 15.00
    Max    : 78.93
    Range  : Mostly "Good" (0–50) and "Moderate" (51–100) EPA categories

================================================================================
  HOW TO RUN THE NOTEBOOK
================================================================================

  REQUIREMENTS
  ------------
  Python 3.8 or higher is recommended. The following packages must be
  installed before running the notebook:

    pip install numpy pandas matplotlib seaborn scikit-learn tensorflow keras

  Or install all at once:

    pip install numpy pandas matplotlib seaborn scikit-learn tensorflow keras jupyter

  STEPS TO RUN
  ------------
  1. Place the notebook and dataset in the same folder:

       /your-folder/
           air_quality_new_dataset.ipynb
           16_air_quality_prediction.csv

  2. Launch Jupyter Notebook or JupyterLab:

       jupyter notebook
         -- or --
       jupyter lab

  3. Open "air_quality_new_dataset.ipynb" from the Jupyter file browser.

  4. Run all cells in order:
       Kernel → Restart & Run All

  5. Expected total runtime: approximately 3–6 minutes depending on
     hardware (LSTM and CNN-LSTM training takes the longest).

  LIVE PREDICTION (Section 9)
  ---------------------------
  To test the system with your own values, scroll to Section 9 of the
  notebook and modify these five variables in the cell:

       INPUT_PM25        = 35.0       # PM2.5 value (µg/m³)
       INPUT_PM10        = 65.0       # PM10  value (µg/m³)
       INPUT_TEMPERATURE = 22.0       # Temperature (°C)
       INPUT_CITY        = 'Ankara'   # Istanbul / Ankara / Izmir / Bursa
       INPUT_DATE        = '2024-03-15'

  Re-run the cell to get instant predictions from all five models along
  with the EPA health category classification.

================================================================================
  EPA AQI CLASSIFICATION REFERENCE
================================================================================

  AQI Range    Category                      Health Implication
  ---------    ---------------------------   ------------------------------
  0  – 50      Good                          Air quality is satisfactory
  51 – 100     Moderate                      Acceptable; some risk for sensitive
  101 – 150    Unhealthy for Sensitive Groups Sensitive groups may be affected
  151 – 200    Unhealthy                      Everyone may experience effects
  201 – 300    Very Unhealthy                 Health alert for all groups
  301 – 500    Hazardous                      Emergency conditions

================================================================================
  NOTES FOR THE INSTRUCTOR
================================================================================

  - All code is original and written specifically for this dataset.
  - The notebook is fully commented with markdown explanations between
    every section to support readability and academic presentation.
  - The documentation follows a standard five-chapter academic structure
    and is written to be plagiarism-free.
  - The results/ folder contains pre-generated charts so outputs can be
    reviewed without re-running the notebook.
  - The live prediction cell in Section 9 makes the system interactive
    and demonstrates real-world applicability beyond academic evaluation.

================================================================================
  CONTACT
================================================================================

  For questions regarding this submission, please contact:
   Robel Ermiyas |robelermiyas7@gmail.com

================================================================================
                          END OF README
================================================================================