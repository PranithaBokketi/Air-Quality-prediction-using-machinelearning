Air Quality Prediction Using Machine Learning
Project Overview

This project predicts air quality levels using historical air pollution data and machine learning techniques. It uses time-series forecasting with Facebook Prophet to model and forecast pollutant concentration over time.

The goal is to understand data preprocessing for time-series, apply forecasting models, and evaluate prediction performance with visualization.

Dataset

Source: UCI Machine Learning Repository – Air Quality Dataset

Description: Contains hourly averaged responses from an array of chemical sensors, along with meteorological data (Temperature, Humidity, etc.).

Size: ~9358 rows and 15 features

Target Variable: CO(GT) (Carbon Monoxide concentration)

Technologies Used

Language: Python

Platform: Google Colab / Jupyter Notebook

Libraries:

pandas, numpy – Data manipulation

matplotlib, seaborn – Visualization

scikit-learn – Scaling and evaluation metrics

prophet – Time-series forecasting

Steps Implemented
1. Data Preprocessing

Loaded dataset and explored missing values

Replaced invalid values (-200) with NaN

Filled missing numeric values using column mean

Combined Date and Time into a single Datetime column

Removed unnecessary columns (Unnamed: 15, Unnamed: 16)

2. Feature Engineering

Selected target variable: CO(GT)

Scaled features using MinMaxScaler

Prepared data for Prophet by renaming columns:

Datetime → ds

CO(GT) → y

3. Model Development

Split data into training and testing sets

Built Facebook Prophet time-series forecasting model

Predicted future air quality levels

4. Model Evaluation

Metrics used:

MAE (Mean Absolute Error)

RMSE (Root Mean Square Error)

R² Score

Visualized Actual vs Predicted pollutant levels

 Results

Prophet model successfully captured the trend of CO(GT) levels.

Evaluation metrics:

MAE: X.XX  
RMSE: X.XX  
R²: X.XX  


Forecast visualization:

How to Run
Option 1: Google Colab

Open the notebook in Google Colab

Upload AirQualityUCI.csv

Install dependencies:

!pip install prophet


Run all cells

Option 2: Local Jupyter Notebook

Clone the repository:

git clone https://github.com/PranithaBokketi/Air-Quality-prediction-using-machinelearning

Install requirements:

pip install -r requirements.txt


Run the notebook:

jupyter notebook AirQualityPrediction.ipynb

Requirements
pandas
numpy
matplotlib
seaborn
scikit-learn
prophet

Future Enhancements

Compare Prophet with LSTM (RNN-based approach)

Build an interactive dashboard using Streamlit or Plotly

Predict multiple pollutants simultaneously


Author 
BOKKETI PRANITHA
