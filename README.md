# Feature Engineering and Selection for Enhanced Model Performance

This repository contains a project that demonstrates feature engineering, feature selection, and model optimization using the California Housing dataset. The goal is to enhance model performance through thoughtful feature creation and selection techniques.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Feature Engineering](#feature-engineering)
- [Feature Selection](#feature-selection)
- [Dimensionality Reduction](#dimensionality-reduction)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Results](#results)
- [Dependencies](#dependencies)
- [How to Run](#how-to-run)
- [Contributing](#contributing)
  

## Introduction

In this project, I focus on enhancing the performance of a machine learning model by carefully engineering new features and selecting the most relevant features from the dataset. The project showcases:
- The creation of meaningful features from existing data.
- The use of feature importance techniques to select key features.
- The application of Principal Component Analysis (PCA) for dimensionality reduction.
- Training and evaluating a Random Forest Regressor with selected features to optimize performance.

## Dataset

The project uses the California Housing dataset from Scikit-Learn, which contains information about various factors affecting housing prices in California.

- **Features**:
  - `MedInc`: Median income in the block group.
  - `HouseAge`: Median house age in the block group.
  - `AveRooms`: Average number of rooms per household.
  - `AveBedrms`: Average number of bedrooms per household.
  - `Population`: Population in the block group.
  - `AveOccup`: Average number of household members.
  - `Latitude`: Block group latitude.
  - `Longitude`: Block group longitude.

- **Target**:
  - `MedHouseVal`: Median house value in the block group.

## Feature Engineering

Two new features were engineered to capture complex relationships in the data:

1. **Income_Age_Interaction**: Interaction between median income and house age (`MedInc * HouseAge`).
2. **HouseAge_PerCap**: Ratio of house age to population (`HouseAge / Population`).

These features were added to the original dataset to provide additional predictive power to the model.

## Feature Selection

Feature importance was evaluated using a Random Forest Regressor to identify the most significant features. The top 5 features based on their importance were selected for training a simplified model, aimed at reducing overfitting and improving generalization.

## Dimensionality Reduction

Principal Component Analysis (PCA) was applied to the dataset to reduce its dimensionality and visualize the underlying structure. The dataset was reduced to 2 principal components for easier visualization.

## Model Training and Evaluation

The project involved training a Random Forest Regressor on:
- The full set of features.
- The top selected features based on feature importance.

Model performance was evaluated using Root Mean Squared Error (RMSE), with the model trained on the top features showing comparable or improved performance.

## Results

- **Top 5 Selected Features**: `MedInc`, `Income_Age_Interaction`, `HouseAge`, `AveRooms`, `AveOccup`.
- **Model RMSE with Top Features**: `X.XX`

> Replace `X.XX` with the actual RMSE from your results.

## Dependencies

- Python 3.x
- pandas
- scikit-learn
- numpy

You can install the required packages via pip:

```bash
pip install pandas scikit-learn numpy
