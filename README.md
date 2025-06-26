# 🏡 House Price Prediction with Machine Learning Models and FastAPI

This repository contains a Google Colab notebook that demonstrates the process of building and deploying a house price prediction model using various machine learning algorithms and a FastAPI application. The project covers data loading, exploratory data analysis (EDA), data cleaning and preparation, feature engineering, model training and evaluation, and finally, implementing a simple web application using FastAPI to make predictions.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Machine Learning Models Used](#machine-learning-models-used)
- [Key Steps](#key-steps)
- [Model Evaluation](#model-evaluation)
- [FastAPI Implementation](#fastapi-implementation)
- [How to Run the Notebook](#how-to-run-the-notebook)
- [Author](#author)

## Project Overview

The goal of this project is to predict house prices based on various features of the property. Several regression models are trained and evaluated to determine the best-performing model. The chosen model is then used to build a simple web application using FastAPI that allows users to get a house price prediction by providing the relevant features.

## Dataset

The dataset used in this project is `housing.csv`, downloaded from Kaggle. It contains information about houses, including their price and various attributes.

**Dataset Details:**

- `price`: The target variable, representing the price of the house.
- `area`: The area of the house.
- `bedrooms`: The number of bedrooms.
- `bathrooms`: The number of bathrooms.
- `stories`: The number of stories.
- `mainroad`: A categorical feature indicating whether the house is on a main road ('yes' or 'no').
- `guestroom`: A categorical feature indicating whether there is a guest room ('yes' or 'no').
- `basement`: A categorical feature indicating whether there is a basement ('yes' or 'no').
- `hotwaterheating`: A categorical feature indicating whether there is hot water heating ('yes' or 'no').
- `airconditioning`: A categorical feature indicating whether there is air conditioning ('yes' or 'no').
- `parking`: Shows the number of parking spaces.
- `prefarea`: Shows whether the house is in a preferred area ('yes' or 'no').
- `furnishingstatus`: Shows the furnishing status ('furnished', 'semi-furnished', or 'unfurnished').

## Machine Learning Models Used

The following machine learning regression models were implemented and evaluated:

1.  Linear Regression Model
2.  Random Forest Regressor
3.  Gradient Boosting Regressor
4.  K-Nearest Neighbors Regressor
5.  Support Vector Regressor (SVR)

## Key Steps

1.  **Data Loading:** Loading the `housing.csv` dataset.
2.  **Exploratory Data Analysis (EDA):** Analyzing the data distribution, descriptive statistics, and correlations between features.
3.  **Data Cleaning and Preparation:** Checking for and handling missing values and duplicate data. Standardizing categorical feature values.
4.  **Feature Engineering:** Mapping 'semi-furnished' to 'furnished' in the `furnishingstatus` column and encoding categorical features using Label Encoding.
5.  **Model Training & Evaluation:** Splitting the data, training each of the five models, and evaluating their performance using metrics like Mean Squared Error (MSE), Root Mean Squared Error (RMSE), R-squared (R2), and Mean Absolute Error (MAE).
6.  **Overall Models Evaluation:** Comparing the performance of all trained models using a table and bar charts to identify the best-performing model.
7.  **FastAPI Implementation:** Building a simple web application with a frontend (`index.html` and `index.js`) and a backend (`main.py` logic within the notebook) using FastAPI to serve the best-performing model for predictions. LocalTunnel is used to expose the local server to the internet.

## Model Evaluation

A comparison of the evaluation metrics for each model is provided to determine the best-performing model. The notebook concludes that the **Gradient Boosting Regressor** is the best model for this dataset based on its lower error metrics (MSE, RMSE, MAE) and higher R2 score.

## FastAPI Implementation

A simple web application is built using FastAPI.
-   `index.html`: Provides a user interface to input house features.
-   `index.js`: Handles fetching data from the form and sending a POST request to the FastAPI backend for prediction.
-   The FastAPI backend (`main.py` logic in the notebook) loads the trained Gradient Boosting Regressor model and the label encoders to process the incoming data and return a predicted house price.
-   LocalTunnel is used to create a public URL to access the FastAPI application running in the Colab environment.

## How to Run the Notebook

1.  Open the Colab notebook in Google Colab.
2.  Mount your Google Drive if your dataset and trained models are stored there (as shown in the notebook). Ensure the paths in the notebook match your file locations.
3.  Run all the cells in the notebook sequentially.
4.  The last sections of the notebook set up and run the FastAPI application and LocalTunnel. Follow the instructions in the notebook to access the web application via the provided LocalTunnel URL.

## Author

-   **Ahsan Javed**
-   Email: ahsan.javed1702@gmail.com
-   GitHub: [https://github.com/ahsan-javed-ds](https://github.com/ahsan-javed-ds)
-   LinkedIn: [https://www.linkedin.com/in/ahsan-javed17/](https://www.linkedin.com/in/ahsan-javed17/)
