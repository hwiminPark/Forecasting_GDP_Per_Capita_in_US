# GDP Per Capita Forecasting

## Project Overview
This project aims to forecast GDP per capita for the US using historical macroeconomic data. Accurate GDP forecasting is crucial for businesses and policymakers as it provides insights into future economic conditions, which can influence investment decisions, market strategies, and economic policies. By leveraging a combination of traditional and machine learning techniques, this project seeks to predict GDP per capita one year ahead, offering valuable foresight into economic trends. The analysis integrates a range of economic indicators, such as unemployment rates, inflation, and consumer confidence, to create a comprehensive predictive model.

## Data
- **Dataset Source:** 
  - [FRED](https://fred.stlouisfed.org/)
  - [CENSUS](https://www.census.gov/)
  - [OECD](https://www.oecd.org/)
  - [Conference Board](https://www.conference-board.org/)
- **Description:** The dataset spans from 2002 to 2022 and includes the following features:
  - **DATE:** Start date of the month
  - **UNRATE (%):** Unemployment rate
  - **CONSUMER CONF INDEX:** Consumer Confidence Index
  - **PPI-CONST MAT.:** Producer Price Index - Construction Materials
  - **CPIALLITEMS:** Consumer Price Index - All Items
  - **INFLATION (%):** Inflation rate
  - **MORTGAGE INT. MONTHLY AVG (%):** Average mortgage interest rate
  - **GDP PER CAPITA:** GDP per capita (target variable)
  - **QUARTERLY REAL GDP:** Real GDP by quarter
  - **QUARTERLY GDP GROWTH RATE (%):** GDP growth rate by quarter
  - **CSUSHPISA:** S&P/Case-Shiller U.S. National Home Price Index

- **Preprocessing:**
  - **Data Cleaning:** Addressed missing values and performed data transformations.
  - **Feature Engineering:** Applied time series feature engineering techniques including:
    - Differencing
    - Lag features
    - Rolling features
    - Seasonal decomposition

## Methodology
- **Exploratory Data Analysis (EDA):**
  - **Sweetviz Report:** Generated comprehensive insights into data distribution and relationships.
  - **GDP Over Time:** Visualized GDP trends.
  - **Seaborn Pairplot:** Analyzed pairwise relationships between features.
  - **Seasonal Decomposition Plot:** Examined seasonal patterns in GDP.
  - **Autocorrelation Plot:** Assessed persistence and seasonality.
  - **Cluster Analysis:** Identified four distinct clusters representing different macroeconomic conditions.

- **Modeling**
  - **Train-Test Split:** Divided data into training and testing sets.
  - **Model Selection:**
    - **TensorFlow/Keras Models:** Initial models showed high RMSE and did not capture the upward trend.
    - **Random Forest:** Outperformed TensorFlow models with better accuracy and lower RMSE.
  - **Hyperparameter Tuning:** Used Keras Tuner to optimize TensorFlow model parameters.

- **Feature Importance**
  - Analyzed the importance of features using permutation importance. Time-series features derived from GDP and CPI were identified as the most influential.

- **Error Analysis**
  - **Residual Analysis:** Identified patterns and outliers in model predictions.
  - **Model Comparison:** Compared TensorFlow and Random Forest models, highlighting the superior performance of Random Forest.

## Results
- **Model Performance:** Random Forest provided the most accurate predictions with lower RMSE compared to TensorFlow models.
- **Key Insights:**
  - **Feature Influence:** Time-series features from GDP and CPI were identified as critical predictors of GDP per capita.
  - **Model Performance:** Random Forest proved more reliable in capturing trends and providing accurate forecasts compared to TensorFlow models.
  - **Seasonal Patterns:** The GDP data showed strong seasonal effects, highlighting the importance of accounting for these variations in predictions.

## Additional Resources
- **Detailed Write-Up:** [View Article](https://scribe.rip/@jazzed_olivine_llama_204/forecasting-gdp-per-capita-a-data-science-journey-4e959d20d3cc)
- **PDF Version of Jupyter Notebook:** [View PDF](https://drive.proton.me/urls/CEGZKN3158#lFDT9lFI6SDA)
