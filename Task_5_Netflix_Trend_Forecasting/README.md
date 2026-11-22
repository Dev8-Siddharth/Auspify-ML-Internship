# Task 5: Netflix Trend Forecasting Model (Time Series)

## 📌 Project Overview
This is Task 5 of the Auspify Technologies Machine Learning Internship. The objective is to forecast future Netflix content release trends based on historical data. This is an **Advanced Time Series Forecasting** problem.

## 🛠️ Tech Stack
- **Python 3**
- **Pandas & NumPy:** Data manipulation and aggregation.
- **Statsmodels:** ARIMA (AutoRegressive Integrated Moving Average) modeling.
- **Matplotlib:** Time series visualization.

## 🧠 Methodology
1. **Data Preprocessing & The "2021 Trap":**
   - Aggregated the total count of Movies and TV Shows released per year.
   - **Critical Engineering Decision:** We discovered that the dataset contained incomplete data for 2021 (a data collection artifact). We truncated the data at 2020 to prevent the model from learning a false "crash" trend. We also filtered out pre-2000 data to focus on the streaming era.
2. **Exploratory Data Analysis (EDA):**
   - Visualized the exponential growth of Movies from 2010-2017, followed by a slight decline.
   - Observed the steady, linear growth of TV Shows.
3. **ARIMA Modeling:** 
   - Trained two separate ARIMA(1,1,1) models: one for Movies and one for TV Shows.
   - The (1,1,1) parameters represent Auto-Regressive (using past values), Integrated (differencing to remove trends), and Moving Average (using past errors).
   - Forecasted the next 3 years (2021, 2022, 2023) for both content types.

## 📊 Business Insights (The Strategic Pivot)
This dual-forecast reveals a critical business insight:
- **Movies:** Forecasted to decline from ~457 (2021) to ~412 (2023).
- **TV Shows:** Forecasted to grow from ~473 (2021) to ~541 (2023).
- **The Crossover:** By 2022, TV Show production is predicted to overtake Movie production. Netflix is strategically pivoting from one-off films toward episodic, binge-able content that drives long-term subscriber retention.

## 📸 Output Screenshots
*(See the Screenshots folder in this directory)*
- Cleaned Historical Release Trends (2000-2020)
- Dual ARIMA Forecast Visualization (Movies vs TV Shows)