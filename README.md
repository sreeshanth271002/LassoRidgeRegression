# Linear vs Ridge vs Lasso Regression

## Overview

This project compares three regression approaches on the California Housing dataset:

- Linear Regression
- Ridge Regression
- Lasso Regression

The objective is to understand how L1 and L2 regularization affect model coefficients, overfitting, and prediction performance.

## Dataset

California Housing dataset containing 20,640 observations and 8 input features.

Target:
- `MedHouseVal`

Features:
- `MedInc`
- `HouseAge`
- `AveRooms`
- `AveBedrms`
- `Population`
- `AveOccup`
- `Latitude`
- `Longitude`

## Methodology

1. Checked for missing values
2. Split data into 80% training and 20% testing
3. Standardized the features
4. Trained Linear, Ridge, and Lasso regression models
5. Evaluated using RMSE and R²
6. Used 5-fold cross-validation to tune the regularization parameter `alpha`
7. Compared coefficient shrinkage across different alpha values
8. Evaluated the final models on the held-out test set

## Results

| Model | Test RMSE | Test R² |
|---|---:|---:|
| Linear Regression | 0.745581 | 0.575788 |
| Ridge | 0.745504 | 0.575876 |
| Lasso | 0.745041 | 0.576402 |

Lasso achieved the lowest test RMSE and highest test R² in this experiment, although the improvement over Linear Regression was very small.

## Key Learnings

- Ridge uses L2 regularization and gradually shrinks coefficients.
- Lasso uses L1 regularization and can shrink coefficients exactly to zero.
- Increasing `alpha` increases the strength of regularization.
- Excessive regularization can cause underfitting.
- Regularization does not necessarily improve every dataset.
- Model selection should be based on validation/test performance rather than assuming that a regularized model is always better.

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook / Google Colab
