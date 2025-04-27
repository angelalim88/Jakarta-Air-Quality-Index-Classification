# Jakarta Air Quality Analysis

## Overview
This project focuses on classifying and predict the Air Quality Index (AQI) in Jakarta, Indonesia, from 2010 to 2023, using the ISPU (Indeks Standar Pencemaran Udara) dataset. The dataset records concentrations of key pollutants, including PM10, PM2.5, SO2, CO, O3, and NO2, from various monitoring stations. The analysis involves data cleaning, exploratory data analysis (EDA), and the application of machine learning models (Random Forest, MLP, and SVM) to classify AQI categories.

**Objectives**:
- Preprocess and clean the dataset to address missing values and inconsistencies.
- Conduct EDA to identify trends and patterns in air quality across Jakarta's monitoring stations.
- Develop and evaluate machine learning models to predict AQI categories (e.g., BAIK, SEDANG) based on pollutant concentrations (PM10, PM2.5, SO2, CO, O3, NO2).
- Support air quality monitoring, inform policy decisions, and raise public awareness about pollution levels in Jakarta.

## Dataset
The dataset (`ispu_dki_all.csv`) contains 4,626 entries with the following columns:
- `tanggal`: Date of measurement (e.g., 2010-01-01)
- `stasiun`: Monitoring station (e.g., DKI1 Bunderan HI)
- `pm10`, `pm25`, `so2`, `co`, `o3`, `no2`: Pollutant concentrations
- `max`: Maximum pollutant value for the day
- `critical`: Pollutant contributing most to the air quality index
- `categori`: Air quality category (BAIK, SEDANG, etc.)

**Data Issues**:
- Significant missing values in `pm25` (3,903 missing, ~84%).
- Minor missing values in `pm10` (160), `so2` (19), `co` (8), `o3` (5), `no2` (8), and `critical` (1).

## Project Structure
The analysis is conducted in a Jupyter Notebook: `Jakarta_Air_Analysis_Richard.ipynb`. The notebook is structured as follows:
1. **Library Imports**: Imports libraries including pandas, numpy, matplotlib, seaborn, scikit-learn, tensorflow, altair, plotly, and imbalanced-learn.
2. **Data Loading**: Loads `ispu_dki_all.csv` and displays the first 10 rows.
3. **Data Cleansing**: Checks for missing values and data types, with a missing value report.
4. **Model Evaluation**: Trains Random Forest, MLP, and SVM models, and visualizes their performance using confusion matrices.

## Model Evaluation
The models were evaluated using the following metric:
- **Confusion Matrix**: Measures the number of correct and incorrect predictions for each AQI category, showing the classification performance of Random Forest, MLP, and SVM models.

![Confusion Matrices](https://github.com/angelalim88/Jakarta-Air-Quality-Index-Classification/blob/main/images/confusion_matrices.png)

## Evaluation Results
The confusion matrices reveal the following:
- **Random Forest**: Performs well in classifying AQI categories, likely due to its robustness with imbalanced data.
- **MLP and SVM**: Show moderate performance but struggle with certain categories, possibly due to data imbalance or feature complexity.

These results indicate that Random Forest is the most reliable model for predicting AQI categories in this dataset, providing a solid foundation for air quality monitoring and policy support.
