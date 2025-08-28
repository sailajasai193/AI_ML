#  Regression with Single Input Variable  


##Problem Statement
Given the dataset **AirQuality.csv** containing various air pollution indicators, the task is to **predict CO concentration (mg/m³)** using regression models with **only one input feature**:  
- `PT08.S1(CO)` → Tin oxide sensor response (nominally CO targeted).  

---

##  Dataset Details
- **Input Variable:** `PT08.S1(CO)`  
- **Output Variable:** `CO` (mg/m³)  
- Other columns (ignored in this lab): NMHC, C6H6(GT), NOx, NO2, O3 sensor responses, Temperature, Humidity, etc.  

---


### 1. Data Splitting
- Dataset divided into:
  - **60% Training**  
  - **20% Validation**  
  - **20% Test**  

---

### 2. Linear Regression
- Built a linear regression model with `PT08.S1(CO)` as independent variable.  
- **Plots:**
  - Best fit line on training data.  
  - Scatter plot of **Actual vs Predicted CO** on test data.  
---

### 3. Polynomial Curve Fitting
- Models trained with polynomial degrees **p = 2, 3, 4, 5**.  
- **Best Model:** Polynomial degree **5**  
  - Test RMSE: **0.7307**  

---

### 4. Neural Network (PyTorch)
- Built a feed-forward neural network with:
  - Input: 1 neuron  
  - Hidden Layer: Sigmoid activation, varied hidden neurons (8, 16, 32, 64)  
  - Output: 1 neuron  
  - Loss: Mean Squared Error (MSE)  
  - Optimizer: Stochastic Gradient Descent (SGD)  
- **Plot:** Training Loss vs Epochs for the best neural network.  

---

##  Summary
- **Simple Linear Regression** achieved a test RMSE of **0.7546**.  
- **Polynomial Regression (degree 5)** improved test RMSE to **0.7307**.  
- **Neural Network (64 hidden neurons)** achieved the best performance with test RMSE **0.7494**.  
- Polynomial regression slightly outperformed linear regression and neural network in this dataset.  
---
