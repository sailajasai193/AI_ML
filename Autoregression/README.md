#  Autoregression  

##  Problem Statement  
 given a dataset **daily_covid_cases.csv** containing the **7-day rolling average of new Covid-19 cases in India** recorded daily from **30th Jan 2020 to 2nd Oct 2021**.  
The goal is to analyze temporal patterns and build **AutoRegression (AR) models** to forecast Covid-19 cases.  
---

##  Dataset Description  
- **Columns:**  
  - Date → Index of each day  
  - new_cases → 7-day rolling average of confirmed Covid-19 cases  
  
- **Train-Test Split:**  
  - 65% → Training (first wave till early 2021)  
  - 35% → Testing (covers the **second wave**)  

---
###  1. Autocorrelation Analysis  
- Plotted **line plot of daily cases vs date** → captured **first wave (Aug 2020)** and **second wave (May 2021)**.  
- Generated a **1-day lagged sequence** and computed:  
  - Pearson correlation coefficient: **0.9991** → very strong correlation.  
- Plotted **ACF (AutoCorrelation Function)** up to 60 lags → correlation decreases gradually with lag.  
---

### 2. AR(5) Model  
- Built an **AR(5) model** using training data.  

###  3. Optimal Lag using ACF Heuristic  
- Condition: `abs(AutoCorrelation) > 2 / sqrt(T)` where `T = training data size`.  
- Optimal lag found = **60**.  
- **AR(60) Model Performance:**  
- RMSE = **1860.87**  
- MAPE ≈ **2.02%**  
- Performance was **slightly worse than AR(15)**. 

##  Summary   
- **AR(15) model** gave the **best results** with **RMSE = 1699.23** and **MAPE = 1.50%**.  
- Very high lags (like 60) did not improve performance.  
- AutoRegression models effectively captured Covid-19 case trends across both waves.  
