# Time Series Analysis of Furniture and Office Supplies Sales

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)
- [Visualization](#visualization)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Overview

This project focuses on time series analysis and forecasting of sales data for two categories: Furniture and Office Supplies. The dataset is obtained from a retail store, containing sales data from 2014 to 2017. The project uses SARIMA and Prophet models to forecast future sales, analyze trends, and detect seasonality.

## Features

- **Data Preprocessing**: Cleans and processes sales data for Furniture and Office Supplies.
- **Time Series Decomposition**: Breaks down the sales data into trend, seasonal, and residual components.
- **SARIMA Modeling**: Uses SARIMA (Seasonal AutoRegressive Integrated Moving Average) model to forecast sales for Furniture.
- **Prophet Modeling**: Uses Facebook's Prophet model to forecast both Furniture and Office Supplies sales.
- **Sales Forecasting**: Predicts future sales for both Furniture and Office Supplies over a period of 36 months.
- **Trend Comparison**: Compares the sales trends and forecasts of Furniture and Office Supplies.

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- statsmodels
- fbprophet
- itertools

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/time-series-sales-forecasting.git
   cd time-series-sales-forecasting
   ```

2. **Create a Virtual Environment**

   ```bash
   python -m venv venv
   ```

3. **Activate the Virtual Environment**

   - On Windows:

     ```bash
     venv\Scripts\activate
     ```

   - On macOS/Linux:

     ```bash
     source venv/bin/activate
     ```

4. **Install Required Packages**

   ```bash
   pip install -r requirements.txt
   ```

5. **Install fbprophet (Prophet)**

   ```bash
   pip install prophet
   ```

## Usage

1. **Run the Jupyter Notebook**

   Open the notebook to follow the steps, or run the Python script to view the time series analysis and forecasting results:

   ```bash
   jupyter notebook
   ```

2. **Input Data**

   The dataset used is a retail store dataset containing sales data from 2014 to 2017 for Furniture and Office Supplies.

## Data Preprocessing

- Load and clean the dataset by removing irrelevant columns.
- Convert `Order Date` into `datetime` format.
- Group sales data by month using `resample` function.
- Separate data for Furniture and Office Supplies.
  
## Modeling

- **SARIMA (Seasonal ARIMA) Model**: 
  - We use SARIMA for forecasting Furniture sales.
  - Multiple combinations of parameters were tested using grid search to identify the optimal model.
  - The model with the lowest AIC (Akaike Information Criterion) value is chosen.
  
- **Prophet Model**:
  - Facebook's Prophet model is used to forecast both Furniture and Office Supplies sales.
  - It provides flexible handling of trend changes and seasonality detection over the time series.

## Visualization

- **Sales Trends**: Visualize the sales trends of both Furniture and Office Supplies.
- **Time Series Decomposition**: Decompose the time series into trend, seasonal, and residual components.
- **Forecasting**: Plot the forecasts and confidence intervals for both categories.
- **Comparison**: Compare Furniture and Office Supplies sales forecasts and trends.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Prophet](https://facebook.github.io/prophet/) for providing the forecasting model.
- [Statsmodels](https://www.statsmodels.org/stable/index.html) for SARIMA modeling.
- [Matplotlib](https://matplotlib.org/) and [Pandas](https://pandas.pydata.org/) for visualization and data manipulation.
