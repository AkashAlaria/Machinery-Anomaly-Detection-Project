# Machinery Anomaly Detection for Preventive Maintenance

## Description
This project aims to develop a machine learning model for machinery anomaly detection to enable preventive maintenance. The goal is to identify instances when machinery is in a failure state, which would require maintenance or repair actions to prevent further issues or breakdowns.

The project utilizes the MetroPT dataset, which contains sensor data collected from metro trains in Porto, Portugal. The dataset includes various measurements related to the trains' operations and maintenance.

## Dataset
The MetroPT dataset consists of 1516948 data points collected at 1Hz from February to August 2020 and is described by 15 features from 7 analog and 8 digital sensors.

## Preprocessing
The dataset is preprocessed by handling missing values, dropping unnecessary columns, and converting data types. A crucial step is creating a target variable called 'Status' that indicates whether the machinery is in a failure state (1) or not (0). This is done by analyzing predefined failure time intervals, where the data samples falling within those intervals are labeled as failures (Status = 1), and the rest are labeled as normal operation (Status = 0).

The dataset is then split into positive (failure) and negative (non-failure) samples. To balance the classes, the negative samples are under-sampled to match the number of positive samples.

## Model Development
The project explores various machine learning models, including:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Naive Bayes (Gaussian, Multinomial, and Bernoulli)
- Random Forest
- Support Vector Machines (SVM)
- Long Short-Term Memory (LSTM) neural networks

These models are trained and evaluated using metrics like accuracy, precision, recall, F1-score, and confusion matrices.

## Hyperparameter Tuning
The code performs hyperparameter tuning for some models, such as Random Forest and SVM, using techniques like RandomizedSearchCV and grid search to optimize their performance.

## Usage
The project includes a Streamlit application for easy deployment and interaction. The application allows users to input sensor data and obtain predictions from the trained model. It also provides data visualization and information about the project and dataset.

To run the application, execute the `main.py` script.

## Contributors
- Aranyak Karan
- Sparsh Baliyan
- Akash Alaria
- Jaskirat Singh Bagga
