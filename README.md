# Time-Series Analysis and Forecasting of U.S. Retail Sales

## Project Overview
This project analyzes and forecasts monthly U.S. retail sales using classical time-series models. The goal is to compare different modeling approaches and identify the most accurate method for capturing both trend and seasonality in real-world economic data.

Retail sales are a key indicator of consumer behavior and overall economic activity. Accurate forecasting helps support business planning, demand estimation, and strategic decision-making.

---

## Dataset
- **Source:** Federal Reserve Economic Data (FRED)  
- **Series ID:** MRTSSM44000USN  
- **Frequency:** Monthly  
- **Time Range:** January 1992 – October 2025  
- **Observations:** 406  

The dataset exhibits a strong upward trend and clear seasonal patterns, making it well-suited for time-series modeling.

---

## Methodology

### 1. Exploratory Data Analysis
- Visualized the original time series to identify trend and seasonality  
- Applied **Box-Cox transformation** to stabilize variance  
- Performed **first-order differencing** and **seasonal differencing**  
- Analyzed **ACF and PACF plots** to guide model selection  

---

### 2. Models Implemented

#### Baseline Model
- **Seasonal Naive**  
  - Assumes values repeat from the same period in the previous year  
  - Serves as a benchmark for comparison  

#### Advanced Models
- **ETS (Error-Trend-Seasonal)**  
- **SARIMA (Seasonal ARIMA)**  
- **Regression with ARMA errors**  

These models represent different approaches:
- smoothing-based methods (ETS)  
- parametric time-series models (SARIMA)  
- regression + time-series residual modeling  

---

### 3. Model Evaluation

Models were evaluated using:

- **RMSE (Root Mean Squared Error)**  
- **MAE (Mean Absolute Error)**  
- **MAPE (Mean Absolute Percentage Error)**  

Residual diagnostics were conducted using:
- **ACF of residuals**
- **Ljung-Box tests** to check independence  

---

## 📈 Results

| Model | Performance |
|------|------------|
| Seasonal Naive | Captures seasonality but fails to model upward trend |
| SARIMA | Improves fit and captures temporal structure |
| Regression + ARMA | Adds flexibility with explanatory components |
| **ETS (Best)** | Achieves lowest forecast error and best alignment with actual data |

 **Final Model: ETS**

- Lowest overall prediction error  
- Effectively captures both **trend and seasonal patterns**  
- Provides stable and reliable forecasts on the test set  

---

## Key Insights

- Baseline models are insufficient for data with strong trends  
- Proper transformation and differencing are critical for stationarity  
- Model comparison is essential — performance varies significantly  
- ETS is highly effective for real-world economic time series  

---

## Tools & Technologies

- **Language:** R  
- **Libraries:** forecast, ggplot2  
- **Techniques:** Time-series modeling, statistical diagnostics, model comparison  

---

## Project Structure
time-series-retail-forecasting/
├── data/
├── code/
├── report/
├── slides/


---

## 🚀 Future Improvements

- Incorporate external variables (e.g., economic indicators)  
- Explore machine learning-based forecasting models  
- Analyze structural breaks (e.g., COVID-19 impact)  
- Build automated forecasting pipelines for real-time updates  

---

## Author

**Yunelle Teng**  
Applied Data Science @ University of Chicago  
