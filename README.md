# Energy Price Forecasting with Machine Learning (Prophet)

### Project Overview
In this project, I developed a Time Series Forecasting model using Meta's `Prophet` library in Python to predict the wholesale energy spot prices in the Colombian market for the next 90 days. 

### Business Value
Predictive analytics allows energy traders, large consumers, and grid operators to anticipate market behavior, optimize purchasing strategies, and mitigate financial risks associated with extreme price volatility. By moving from descriptive to predictive analysis, businesses can make proactive rather than reactive decisions.

### Technical Execution & Tools
* **Language:** Python
* **Libraries:** `prophet`, `pandas`, `matplotlib`
* **Data Source:** Historical daily spot prices from XM (Sinergox) - 2021 to 2026.
* **Model Configuration:** I implemented a `logistic` growth model. To align the mathematical output with real-world market constraints, I applied a logical floor (`floor = 0` COP/kWh) and a capacity ceiling (`cap = 4000` COP/kWh). This prevents the algorithm's confidence intervals from predicting impossible negative prices, ensuring business logic is maintained.

### Key Insights from the Forecast
1. **Accurate Historical Mapping:** The model effectively captured the extreme price volatility and spikes driven by the 2023-2024 "El Niño" climate phenomenon (represented by the black dots).
2. **Short-Term Trend Stabilization:** For the forecasted 90-day period in 2026, the central tendency line (dark blue) indicates a stabilization of spot prices at lower levels, assuming no anomalous climate or grid events occur.
3. **Uncertainty Margin:** The light blue shaded area represents the confidence interval, highlighting the inherent volatility of a hydro-dominated energy matrix.

---
### Visualization
<img width="1189" height="690" alt="image" src="https://github.com/user-attachments/assets/179f2a52-c3d6-41ea-ae7f-36b292dc10ef" />


