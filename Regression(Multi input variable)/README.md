# Regression with Multi-Input Variables  


## Problem Statement
The objective of this lab is to **predict CO concentration (mg/m³)** from the **AirQuality.csv** dataset using:  
1. Multiple Linear Regression  
2. Polynomial Regression  
3. Neural Network (PyTorch)  
---


### 1. Multiple Linear Regression (All 12 Features)  
- Built a regression model using all features.  

---

### 2. Polynomial Regression (All 12 Features)  
- Trained polynomial regression models with **degrees 2, 3, 4, 5**.  
- **RMSE Results (Validation):**  
  - Degree 2 → **0.4118**  
  - Degree 3 → **0.4097**  Best  
  - Degree 4 → 3.6963 (Overfitting)  
  - Degree 5 → 42.5004 (Severe Overfitting)  
- **Best Model:** Degree **3** polynomial regression  
  - Test RMSE: **0.4530**  

---

### 3. Neural Network (All 12 Features, PyTorch)  
- Built a **feed-forward neural network** with:  
  - Input Layer → 12 neurons  
  - Hidden Layer → Sigmoid activation, tested with [8, 16, 32, 64] neurons  
  - Output Layer → 1 neuron (regression output)  
  - Loss: MSE  
  - Optimizer: SGD  

- **Best Model (64 hidden neurons):**  
  - Test RMSE: **0.6910**  

---

## Summary
- **Linear Regression:** Test RMSE = **0.4812**  
- **Polynomial Regression (Degree 3):** Test RMSE = **0.4530** → **Best overall**  
- **Neural Network (64 hidden neurons):** Test RMSE = **0.6910**  .  

---
