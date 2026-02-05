$$$$ Quantitative Volatility Prediction Using Linear Regression
#####Project Overview

This project applies linear regression to a quantitative finance problem: predicting future market volatility using engineered statistical features from historical EUR/USD forex data.
Instead of predicting prices (which is common), the model focuses on volatility, a core concept in quantitative trading and risk management.

### Dataset Used

Asset: EUR/USD (Forex)

Source: Yahoo Finance

Frequency: Daily

Time Period: 2020 – 2024

Access Method: yfinance Python library

Raw Dataset Columns

Open

High

Low

Close

Volume

The dataset is downloaded directly inside the Jupyter notebook, so no manual CSV upload is required.

##### Feature Engineering (Quantitative Indicators)

The following quantitative features were engineered from the price data:
Feature	Description
Return	Daily percentage change in closing price
Rolling Mean (5 days)	Short-term price trend
Rolling Std Dev (5 days)	Historical volatility
Lagged Return	Previous day return (momentum signal)
🎯 Target Variable

Future Volatility:
5-day rolling standard deviation of returns, shifted one day ahead

This allows the model to predict next-day volatility using current market information.

🧠 Model Used

Algorithm: Linear Regression

Library: scikit-learn

Why Linear Regression?

Simple and interpretable

Common baseline model in quantitative research

Allows coefficient-based financial interpretation

### Workflow:
Download EUR/USD historical data
Clean and preprocess time-series data
Engineer quantitative features
Split data into training and testing sets
Train linear regression model
Evaluate model performance
Interpret coefficients
Visualize predicted vs actual volatility

### Model Evaluation:
The model is evaluated using:
Mean Squared Error (MSE)
R² Score
Volatility is inherently difficult to predict; therefore, interpretability and signal behavior are prioritized over high R² values.

###Results Visualization:
The project includes a scatter plot comparing:
Actual volatility
Predicted volatility
This helps visually assess model performance and prediction dispersion.

#### Key Insights:
Lagged returns and rolling volatility contribute significantly to future volatility
Linear regression provides interpretable coefficients for financial analysis
The project demonstrates how traditional statistical models can be applied to financial time series

#### Technologies Used:
Python,Jupyter Notebook ,NumPy ,Pandas,Matplotlib,scikit-learn,yfinance


###Future Improvements:
Add Ridge and Lasso regression for regularization
Experiment with multiple rolling window sizes
Compare performance with non-linear models
Extend to other currency pairs or assets
Convert volatility prediction into a trading signal

#### How to Run the Project:
Clone the repository
Open the notebook in Jupyter or Google Colab
Install dependencies
pip install yfinance scikit-learn

