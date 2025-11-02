# 🌍 Forecasting Tourism Flows: Predictive Analytics (Mexico–USA)

## 📖 Project Overview
This project focuses on **forecasting short-term U.S. tourist arrivals to Mexico** using real-world tourism and macroeconomic data.  
The objective is to help tourism stakeholders **anticipate seasonal demand**, **optimize resource allocation**, and **make data-driven strategic decisions**.

The analysis compares several forecasting models to identify the most accurate and reliable approach for predicting quarterly tourism flows. Emphasis is placed on combining **statistical soundness**, **interpretability**, and **real-world applicability**.

---

## 🧩 Data Sources
- **`dataTour.Rdata`** – Contains quarterly tourism flow data between 20 destination countries and their five main origin countries.  
  - Each destination includes:
    - 5 origin country columns  
    - A **Total** column  
    - A **Difference** column representing arrivals from other origins  

- **`IMFdata.Rdata`** – Provides macroeconomic indicators for 46 countries, such as:
  - GDP growth  
  - Purchasing Power Parity (PPP)  
  - Inflation rates  
  - Other key economic factors  

These datasets enable the exploration of both **seasonal patterns** and **economic influences** on tourism flows.

---

## ⚙️ Methodology
Multiple forecasting models were developed and compared to evaluate short-term prediction accuracy:

1. **Seasonal Naïve Model** – Baseline model capturing consistent quarterly seasonality.  
2. **Exponential Smoothing (ETS)** – Captures level, trend, and seasonal effects (notably ETS(A,Ad,A)).  
3. **Autoregressive Lag Model (AR)** – Models temporal dependencies in tourist arrivals.  
4. **Lag Model with Seasonal Dummies** – Enhances AR models with quarter-specific seasonal adjustments.  
5. **Macroeconomic Regression Model** – Incorporates U.S. GDP growth and Mexico’s PPP to link economic indicators with tourism flows.

### Evaluation Metrics
- **Root Mean Squared Error (RMSE)**  
- **Mean Absolute Error (MAE)**  

Models were trained and validated using historical data up to **2018**, with **2019** serving as the out-of-sample test period.

---

## 📊 Key Findings
- The **Seasonal Naïve model** achieved the **lowest RMSE and MAE** across both validation and test datasets.  
- The **ETS(A,Ad,A)** model effectively captured trends but showed mild overfitting on the test period.  
- **Autoregressive** and **Lag + Dummy** models provided good fit during training but lacked generalization power.  
- The **Macroeconomic regression model** offered valuable interpretability but produced higher errors for short-term predictions.  

### ✅ Conclusion
Tourism flows between the **U.S. and Mexico** show **strong, stable seasonal patterns**.  
The **Seasonal Naïve model** is the **most reliable, interpretable, and operationally efficient** method for short-term forecasting.  

ETS and regression models remain useful for **long-term trend monitoring** and **policy scenario analysis**, providing context on how economic changes influence tourism.

---

## 🧠 Tools & Technologies
- **Language:** R  
- **Techniques:** Time Series Forecasting (ETS, AR, Regression)  
- **Evaluation Metrics:** RMSE, MAE  
- **Validation Strategy:** Train–Validation–Test Split  
- **Visualization:** R packages for time series diagnostics and forecasting visualization  

---

## 📈 Practical Applications
This analysis supports:
- Forecasting **seasonal tourism demand** between the U.S. and Mexico  
- **Optimizing resource allocation** (staffing, infrastructure, marketing)  
- Integrating **macroeconomic indicators** for strategic planning  
- Enhancing **data-driven decision-making** in tourism management  

