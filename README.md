# Series Analyzer

A Python-based tool for analyzing time series data using various statistical methods.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [API Documentation](#api-documentation)
6. [Contributing](#contributing)
7. [License](#license)

## Introduction

The Series Analyzer is a Python package designed to analyze time series data using various statistical methods. It provides an easy-to-use interface for performing common time series analysis tasks, including trend detection, seasonality analysis, and forecasting.

## Features

- Time series decomposition into trend, seasonal, and residual components
- Statistical tests for stationarity (Augmented Dickey-Fuller test)
- Autocorrelation and partial autocorrelation plots
- ARIMA model implementation for time series forecasting
- Support for multiple time series datasets

## Installation

To install the Series Analyzer package, run the following command:
bash pip install git+https://github.com/RohanDebnath24/Series-Analyzer.git

## Usage

Here's a basic example of how to use the Series Analyzer:


python from series_analyzer import SeriesAnalyzer

# Load your dataset
df = pd.read_csv('your_time_series_data.csv')

# Initialize the analyzer
analyzer = SeriesAnalyzer(df)

# Perform time series decomposition
trend, seasonal, residual = analyzer.decompose()

# Check for stationarity
result = analyzer.stationarity_test() print(f"Is stationary: {result}")

# Generate an ARIMA forecast
forecast = analyzer.arima_forecast(steps=30)


## API Documentation

The Series Analyzer provides several key methods:

- `__init__(self, df)`: Initializes the analyzer with a pandas DataFrame containing time series data.
- `decompose()`: Performs time series decomposition using STL decomposition.
- `stationarity_test()`: Runs the Augmented Dickey-Fuller test to check for stationarity.
- `autocorrelation_plot()`: Generates an autocorrelation plot.
- `partial_autocorrelation_plot()`: Generates a partial autocorrelation plot.
- `arima_forecast(steps)`: Creates an ARIMA model and generates a forecast for the specified number of steps.

For full documentation, including method parameters and return types, please see the [API Reference](docs/api.md).

## Contributing

Contributions are welcome! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



