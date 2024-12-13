# Project README

## Project Overview
This project focuses on building a predictive maintenance system using machine learning to detect anomalies in industrial equipment. The objective is to predict machine breakdowns before they occur by identifying unusual patterns in operational data, enabling timely intervention and reducing downtime.

## Problem Statement
System failures are a critical issue across industries, leading to financial losses and safety risks. Predictive maintenance offers a solution by evaluating equipment conditions through continuous monitoring and proactive maintenance. This project uses machine learning to predict anomalies in equipment performance based on historical data.

### Key Objectives:
- Detect anomalies in the data.
- Build a machine learning pipeline for predictive maintenance.
- Evaluate and validate models for effective anomaly detection.

## Dataset
### Data Source
The dataset used in this project was provided as an Excel file containing 18,398 rows and 61 columns. It includes the following:
- **time**: Timestamps of the data collection.
- **x1 to x60**: Predictor variables capturing sensor readings, operational parameters, and environmental factors.
- **y**: Binary target variable (0: Normal, 1: Anomaly).

### Preprocessing Steps:
- **Normalization**: Standardized features to handle varying ranges.
- **Imbalance Handling**: Used SMOTE to address class imbalance in the target variable.
- **Feature Engineering**: Derived insights from correlated predictors.

## Code Explanation
The project pipeline consists of:

### 1. **Data Loading and Inspection**
- Loaded the dataset from an Excel file.
- Inspected data types, missing values, and distributions.

### 2. **Exploratory Data Analysis (EDA)**
- Visualized target distribution.
- Analyzed feature distributions and correlations.
- Identified potential outliers and trends.

### 3. **Preprocessing**
- Standardized features using `StandardScaler`.
- Handled class imbalance using SMOTE.

### 4. **Model Development**
- Trained a `RandomForestClassifier` as the baseline model.
- Evaluated performance using classification metrics and ROC-AUC.
- Optimized the model with hyperparameter tuning.

### 5. **Evaluation**
- Generated a classification report and feature importances.
- Assessed the model’s ability to detect anomalies.

### 6. **Visualization**
- Saved plots for target distribution, feature distributions, correlations, and feature importances.

## Instructions to Run the Code
### Prerequisites
1. Install Python (>=3.8).
2. Install the required packages:
   ```bash
   pip install pandas numpy matplotlib scikit-learn imbalanced-learn joblib
   ```

### Steps to Run
1. **Clone the Repository**
   ```bash
   git clone <repository_url>
   cd <repository_name>
   ```

2. **Prepare the Dataset**
   - Place the dataset (`AnomaData.xlsx`) in the `data` folder.

3. **Run the Code**
   - Execute the main Python script:
     ```bash
     python main.py
     ```

4. **View Results**
   - Generated plots and saved models will be available in the `outputs` folder.

### Reproducing Results
To reproduce the results:
- Use the same dataset provided in the repository.
- Follow the steps above, ensuring consistent random seeds for reproducibility.

## Future Work
- Integrate advanced anomaly detection models like Isolation Forest or Autoencoders.
- Explore time-series analysis for trend-based anomaly detection.
- Deploy the model as an API for real-time monitoring.


