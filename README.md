<p align="center">
  <img src="assets/walmart-sales-forecasting-banner.png" alt="Walmart Sales Forecasting Project Banner" width="100%">
</p>


# Walmart Sales Forecasting

A time-series analysis and sales forecasting project focused on exploring historical Walmart weekly sales, identifying seasonal patterns, and evaluating forecasting models across multiple stores.

## Technologies Used

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy">
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=plotly&logoColor=white" alt="Matplotlib">
  <img src="https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge" alt="Seaborn">
  <img src="https://img.shields.io/badge/Statsmodels-3B6EA8?style=for-the-badge" alt="Statsmodels">
  <img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="Scikit-learn">
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter Notebook">
</p>

## Quick Navigation
<p align="center">
  <a href="#project-overview"><img src="https://img.shields.io/badge/Overview-1F6FEB?style=for-the-badge" alt="Overview"></a>
  <a href="#objectives"><img src="https://img.shields.io/badge/Objectives-1F6FEB?style=for-the-badge" alt="Objectives"></a>
  <a href="#methodology"><img src="https://img.shields.io/badge/Methodology-1F6FEB?style=for-the-badge" alt="Methodology"></a>
  <a href="#visualizations"><img src="https://img.shields.io/badge/Visualizations-1F6FEB?style=for-the-badge" alt="Visualizations"></a>
  <a href="#model-performance"><img src="https://img.shields.io/badge/Model_Results-1F6FEB?style=for-the-badge" alt="Model Results"></a>
  <a href="#getting-started"><img src="https://img.shields.io/badge/Getting_Started-1F6FEB?style=for-the-badge" alt="Getting Started"></a>
  <a href="#connect-with-me"><img src="https://img.shields.io/badge/Connect-1F6FEB?style=for-the-badge" alt="Connect"></a>
</p>

## Project Overview

Retail sales forecasting helps businesses understand demand patterns and make better inventory, staffing, and operational decisions.

This project analyzes Walmart weekly sales data across **45 stores**, explores sales trends and holiday effects, and compares statistical forecasting models to evaluate their performance on historical sales data.

## Objectives

- Perform exploratory data analysis (EDA) on weekly sales data.
- Identify seasonal trends and patterns in retail sales.
- Analyze correlations between numerical variables.
- Investigate potential outliers using the Interquartile Range (IQR) method.
- Build and evaluate time-series forecasting models.
- Compare ARIMA, ARIMAX, and Seasonal Naive forecasting approaches.

## Tech Stack

- **Language:** Python
- **Data Analysis:** NumPy, Pandas
- **Visualization:** Matplotlib, Seaborn
- **Time-Series Modeling:** Statsmodels
- **Model Evaluation:** Scikit-learn
- **Environment:** Google Colab / Jupyter Notebook

## Project Structure

```text
walmart-sales-forecasting/
├── assets/
│   ├── arimax-vs-seasonal-naive.png
│   ├── monthly-sales-seasonality.png
│   └── total-sales-forecast.png
├── .gitignore
├── README.md
├── requirements.txt
└── walmart_sales_forecasting.ipynb
```

## Methodology

1. **Data Preparation:** Load, inspect, and prepare the historical sales data for analysis.
2. **Exploratory Data Analysis:** Examine sales distributions, correlations, outliers, and seasonal trends.
3. **Feature Analysis:** Investigate the relationship between sales, holidays, and other available variables.
4. **Forecasting:** Develop ARIMA, ARIMAX, and Seasonal Naive models.
5. **Model Evaluation:** Compare forecast predictions with actual sales using RMSE and MAPE.
6. **Multi-Store Analysis:** Examine combined weekly sales forecasts across the 45 stores.

## Visualizations

### 1. Monthly Sales Seasonality

Explores how average weekly sales vary across months and helps identify seasonal sales patterns.

![Average Weekly Sales by Month](assets/monthly-sales-seasonality.png)

### 2. Forecast Model Comparison

Compares ARIMAX and Seasonal Naive predictions against actual sales over the evaluated test period.

![ARIMAX vs Seasonal Naive Forecast](assets/arimax-vs-seasonal-naive.png)

### 3. Total Weekly Sales Forecast

Visualizes the combined weekly sales forecast across all 45 stores.

![Total Weekly Sales Forecast Across All Stores](assets/total-sales-forecast.png)

## Model Performance

The following are the evaluation results recorded during the project analysis. Lower RMSE and MAPE values indicate better predictive performance on the evaluated data.

| Model | RMSE | MAPE |
|---|---:|---:|
| ARIMA (1,0,1) | ~304K | ~11.0% |
| Seasonal Naive | ~94K | ~5.2% |
| ARIMAX — Holiday Weeks 47–52 | ~100K | ~5.1% |
| ARIMAX — Weeks 1–4 and 47–52 | ~106K | ~5.7% |

*Note: These results correspond to the evaluated periods and configurations. Model performance may vary across stores and test windows.*

## Key Findings

- Weekly sales exhibit seasonal variation, making time-series analysis useful for retail forecasting.
- The Seasonal Naive model performed substantially better than the evaluated ARIMA model on the reported metrics.
- ARIMAX provided a way to incorporate additional explanatory variables, including holiday-related information.
- Forecasting performance should be evaluated against a suitable baseline rather than assuming a more complex model is always better.
- Correlation does not establish causation, and statistical outliers may represent genuine retail events rather than data errors.

## Getting Started

### Prerequisites

- Python 3.10 or a compatible Python environment
- Jupyter Notebook or Google Colab
- The dataset required by the notebook

### Run on Google Colab

1. Open the notebook in Google Colab.
2. Upload or connect the required dataset.
3. Install any missing dependencies listed in `requirements.txt`.
4. Run the notebook cells in order.

### Run Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/YOUR_USERNAME/walmart-sales-forecasting.git
   ```

2. Move into the project directory:

   ```bash
   cd walmart-sales-forecasting
   ```

3. Create and activate a virtual environment:

   ```bash
   python -m venv .venv
   ```

   On Windows:

   ```bash
   .venv\Scripts\activate
   ```

   On Linux/macOS:

   ```bash
   source .venv/bin/activate
   ```

4. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

5. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

6. Open `walmart_sales_forecasting.ipynb` and run the cells in sequence.

## Limitations

- Forecast accuracy depends on the selected test period, available historical data, and model assumptions.
- Statistical convergence warnings may occur for certain store-level ARIMAX models.
- Holiday effects and correlations should not be interpreted as proof of causation.
- Results from historical data do not guarantee future sales performance.

## Future Improvements

- Tune forecasting model parameters systematically.
- Investigate additional time-series models and forecasting baselines.
- Perform consistent validation across individual stores.
- Explore additional explanatory variables where suitable data is available.

## Author

**Samarth Boraste**  
## Connect with Me

<p align="center">
  <a href="https://www.linkedin.com/in/samarthb77/">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin" alt="Connect on LinkedIn" />
  </a>
  <a href="https://github.com/samarthboraste">
    <img src="https://img.shields.io/badge/GitHub-Follow-black?style=for-the-badge&logo=github" alt="Follow on GitHub" />
  </a>
</p>

*This project was developed for learning and practical exploration of retail sales analysis and time-series forecasting.*
