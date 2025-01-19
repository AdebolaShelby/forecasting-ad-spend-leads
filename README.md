# Forecasting Cost and Leads for 2025

## Overview

This project uses historical data to forecast monthly ad spend (Cost) and generated leads for the year 2025. The analysis incorporates advanced feature engineering and machine learning models to provide accurate predictions. The results are visualized in a combined bar and line chart to illustrate the distribution of forecasted costs and leads.
![alt text](forecasted_monthly_costs_and_leads.png)

Steps

1. Data Loading and Cleaning

* The dataset (combined_lead_export_data.csv) is loaded and cleaned to ensure consistency.

* Cost values are converted to numeric by removing symbols and formatting.

* Months are ordered and represented numerically for modeling purposes.

2. Feature Engineering

* Additional features are created to enhance the predictive power of the model:

* Cyclic Features: Month_sin and Month_cos to represent the cyclical nature of months.

* Lagged Features: Previous month's Cost and Leads.

* Rolling Averages: 3-month and 6-month rolling averages for both Cost and Leads.

3. Model Training

* Two separate Random Forest Regressor models are trained to forecast Cost and Leads using data from 2023 and 2024.

* Features include:

    * Year

    * Month_Num

    * Month_sin, Month_cos

    * Lagged and rolling averages for Cost and Leads

4. Forecasting for 2025

* Forecasts are generated for each month of 2025.

* A 10% growth factor is applied to both cost and lead forecasts to account for expected growth.

5. Visualization

* Forecasted costs are represented as a bar chart.

* Forecasted leads are overlaid as a line chart for clear comparison.

* Dual y-axes are used for proper scaling of both metrics.

## How to Use

* Ensure the required Python libraries are installed:

    * pip install pandas numpy matplotlib scikit-learn

* Place the dataset combined_lead_export_data.csv in the project directory.

* Run the Python script to generate the forecast and visualize the results.

## Output

The output chart displays:

* Blue bars: Forecasted monthly ad spend (Cost).

* Orange line: Forecasted monthly leads.

## File Structure

* combined_lead_export_data.csv: Input data.

* forecast_2025_analysis.py: Python script for forecasting and visualization.

