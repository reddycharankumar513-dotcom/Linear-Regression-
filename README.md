# Simple Linear Regression on California Housing Data

## Project Overview

This project demonstrates a simple linear regression model using real California housing data.

The objective is to fit a regression model, evaluate its performance, analyze the residuals, and interpret the model coefficients in simple terms.

## Dataset

The project uses the California Housing dataset available through `scikit-learn`.

- **Feature:** `MedInc` - median income in the area, measured in tens of thousands of dollars.
- **Target:** `MedHouseVal` - median house value, measured in hundreds of thousands of dollars.
- **Model:** Simple Linear Regression

Only one feature is used because the objective is to demonstrate simple linear regression.

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Project Workflow

1. Load the California Housing dataset.
2. Select Median Income as the predictor.
3. Select Median House Value as the target.
4. Split the data into training and testing sets.
5. Fit a Linear Regression model.
6. Generate predictions.
7. Calculate RMSE and R².
8. Plot the regression line.
9. Calculate and visualize residuals.
10. Interpret the intercept and coefficient.
11. Discuss model limitations.

## Files

- `simple_linear_regression.ipynb` - Complete notebook containing the model, plots, evaluation, residual analysis, and interpretation.
- `requirements.txt` - Python dependencies required to run the notebook.
- `README.md` - Project documentation and setup instructions.

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/simple-linear-regression.git
cd simple-linear-regression
```

### 2. Create a virtual environment

Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

macOS/Linux:

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Open `simple_linear_regression.ipynb` and run the cells from top to bottom.

## Model

The notebook fits the simple linear regression equation:

`MedHouseVal = intercept + coefficient × MedInc`

### Coefficient Interpretation

The coefficient represents the expected change in predicted median house value associated with a one-unit increase in the Median Income feature.

Because `MedInc` is measured in tens of thousands of dollars and `MedHouseVal` is measured in hundreds of thousands of dollars, the units should be considered when interpreting the coefficient.

### Intercept Interpretation

The intercept is the model's predicted median house value when Median Income is zero. This has limited practical meaning because a zero median income is not representative of the observed data.

## Residual Analysis

Residuals are calculated as:

`Residual = Actual Value - Predicted Value`

The notebook includes:

- A residuals-versus-predicted-values scatter plot.
- A residual distribution histogram.
- A written discussion of the residual pattern.

The residuals are generally centered around zero but show substantial spread. This indicates that median income explains part of the variation in house values, while other factors also contribute to house prices.

## Evaluation Metrics

The notebook reports:

- **RMSE (Root Mean Squared Error):** measures the typical size of prediction errors in the target's units.
- **R² (R-squared):** measures the proportion of variation in the target explained by the model.

The exact values are generated when the notebook is executed.

## Limitations

This is intentionally a simple model using only one predictor. House values depend on many factors, so Median Income alone cannot fully explain the variation in house prices.

A multiple linear regression model using additional housing features could provide a more complete analysis.

## Assignment Requirements Covered

- [x] Model fitted on real data
- [x] Residuals plotted and discussed
- [x] Coefficients interpreted in words
- [x] Notebook with fitted model and interpretation
- [x] README with instructions for running the project
