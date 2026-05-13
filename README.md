# Forecasting Traffic Accidents Using Holt-Winters Time Series Models (ATUS 1997–2024)
This project analyzes and forecasts traffic accident trends in Mexico using historical data from the ATUS dataset (1997–2024). T

# Objectives
The goal is to identify temporal patterns such as trend and seasonality, and to generate accurate forecasts for future periods using time series modeling techniques.

# Technologies Used
- Python
- Pandas
- Matplotlib
- Statsmodels
- Scikit-learn

# Dataset
- Time range: 1997–2024
- Frequency: Monthly
- Structure: Year, Month, Accidents
- Source: INEGI. Statistics on road traffic accidents in urban and suburban areas.
- URL: https://www.inegi.org.mx/sistemas/olap/proyectos/bd/continuas/transporte/accidentes.asp?s=est&c=13159&proy=atus_accidentes
- Public dataset: https://drive.google.com/file/d/1kDaeJ8YWsDm1B5zPJQ9RjhkafH68mKnd/view?usp=sharing

# Methodology
- Data Preprocessing
Resolved encoding issues (UTF-8 with BOM)
Cleaned and structured data into a time series format
Converted dates to a proper datetime index with monthly frequency (MS)
Handled outliers, particularly the April 2020 anomaly, using seasonal imputation

- Exploratory Data Analysis
Visualized the full time series to identify trend and seasonality
Detected strong seasonal patterns with peaks at the end of each year
Identified structural breaks (e.g., 2020 due to external factors)

- Modeling
Applied the Holt-Winters additive model
Captured level, trend, and seasonal components
Optimized smoothing parameters automatically

- Model Evaluation
The model was evaluated using the following metrics:
  * MAE (Mean Absolute Error): 836.57
  * MSE (Mean Squared Error): 1,383,451
  * MAPE (Mean Absolute Percentage Error): 2.82%
  * These results indicate a high level of accuracy in modeling the time series.

# Forecast Results
Generated forecasts for 2025 using the fitted model showed that the series maintains a consistent seasonal behavior over time. The results indicate that higher accident rates are expected during the final months of the year, following the historical trend observed in previous periods.

# Key Insights
The time series exhibits strong and stable seasonality
The model effectively captures recurring monthly patterns
External shocks (e.g., 2020) introduce anomalies but do not significantly affect overall performance
The model demonstrates robustness and reliability for forecasting

# Conclusion
The Holt-Winters additive model proved to be an effective approach for modeling and forecasting traffic accident data with strong seasonal characteristics. The low forecasting error (MAPE ≈ 2.8%) highlights the model’s accuracy and suitability for real-world applications.
This methodology can be extended to other domains such as demand forecasting, financial analysis, and operational planning.
