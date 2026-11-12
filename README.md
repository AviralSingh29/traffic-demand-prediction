# UrbanFlow AI — Urban Traffic Demand Forecasting Platform

### Flipkart Gridlock Hackathon 2.0

## Overview

UrbanFlow AI is a machine learning-based urban traffic demand forecasting platform designed to predict traffic demand across Bengaluru's road network.

The project leverages spatio-temporal, environmental, and road-network data to identify traffic demand patterns and generate accurate predictions. The objective is to support data-driven urban mobility planning, congestion management, and intelligent transportation systems.

The solution implements an end-to-end **CatBoost-based regression pipeline**, incorporating exploratory data analysis, data preprocessing, feature engineering, model training, and predictive performance evaluation.

---

## Key Highlights

- Developed a CatBoost-based regression pipeline for urban traffic demand forecasting.
- Performed exploratory data analysis (EDA) to understand spatio-temporal traffic patterns.
- Implemented data preprocessing and feature engineering to extract meaningful predictive information.
- Engineered temporal and geospatial features to capture traffic demand variations.
- Optimized model hyperparameters to improve predictive performance.

---

## Results

### Model Performance

| Metric | Score |
|---|---:|
| Validation R² Score | **0.9436** |
| HackerEarth Public Leaderboard Score | **90.8044** |

### Final Model

**CatBoost Regressor**

- Iterations: 2000
- Depth: 8
- Learning Rate: 0.03
- Loss Function: RMSE

---

## Project Outputs

### Validation Performance

![Validation Performance](images/validation_score.png)

### Feature Importance

![Feature Importance](images/feature_importance.png)

---

## Dataset

### Dataset Size

- Training Samples: 77,299
- Test Samples: 41,778

### Features

- Geohash
- Day
- Timestamp
- RoadType
- NumberofLanes
- LargeVehicles
- Landmarks
- Temperature
- Weather

### Target Variable

- Demand

---

## Exploratory Data Analysis (EDA)

Performed exploratory analysis to understand traffic demand patterns and identify relationships between different features.

Key analysis included:

- Missing value analysis
- Demand distribution analysis
- Weather-wise demand analysis
- Road type analysis
- Lane count analysis
- Geospatial feature analysis

---

## Data Preprocessing

Prepared the dataset for machine learning through data preprocessing and transformation.

Key operations included:

- Data inspection and validation
- Missing value analysis and treatment
- Data type handling
- Categorical feature preparation
- Training and validation data preparation

---

## Feature Engineering

Developed additional predictive features to capture temporal and geographical traffic patterns.

Key engineered features included:

- Hour extraction from timestamps
- Minute extraction from timestamps
- Rush Hour indicator
- Evening Peak indicator
- Geohash Prefix encoding
- Traffic pattern-based temporal features

---

## Model Development

### Algorithm

**CatBoost Regressor**

### Why CatBoost?

- Efficient handling of categorical variables.
- Strong performance on structured and tabular datasets.
- Reduced requirement for extensive categorical preprocessing.
- Built-in regularization to help control overfitting.
- Effective modelling of complex feature relationships.

### Model Hyperparameters

```python
iterations = 2000
depth = 8
learning_rate = 0.03
loss_function = "RMSE"
```

---

## Tech Stack

- **Programming Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Machine Learning:** Scikit-Learn, CatBoost
- **Data Visualization:** Matplotlib
- **Development Environment:** Jupyter Notebook

---

## Key Learnings

- Spatio-temporal feature engineering for traffic forecasting.
- Geospatial feature extraction using Geohash.
- Exploratory data analysis of urban traffic patterns.
- Handling categorical variables using CatBoost.
- Regression modelling and predictive performance evaluation.
- Hyperparameter optimization and model improvement.
- End-to-end machine learning pipeline development.

---

## Repository Structure

```text
traffic-demand-prediction/
│
├── Traffic_Demand_Prediction.ipynb
├── README.md
├── requirements.txt
│
└── images/
    ├── validation_score.png
    ├── feature_importance.png
    └── leaderboard_score.png
```

---

## Project Objective

UrbanFlow AI aims to demonstrate how machine learning and spatio-temporal data analysis can contribute to smarter urban mobility planning by forecasting traffic demand across Bengaluru's road network.

**Developed as part of Flipkart Gridlock Hackathon 2.0.**
