#Neural Networks (Breast Cancer Classification)
## Dataset: Wisconsin Diagnostic Breast Cancer (WDBC)
### Dataset Variants Used
1. **Standardized Dataset**  
   - `WDBC_Scaled_Train.csv`  
   - `WDBC_Scaled_Validation.csv`  
   - `WDBC_Scaled_Test.csv`  

2. **PCA-transformed Dataset (l = 10 components)**  
   - `WDBC_PCA10_Train.csv`  
   - `WDBC_PCA10_Validation.csv`  
   - `WDBC_PCA10_Test.csv`  

---

## Tasks Performed

### Part A: Neural Network on Standardized Dataset
- Input layer: 30 neurons.  
- Hidden layers: experimented with different **single** and **two-hidden layer** architectures.  
- Output layer: 1 neuron with **sigmoid activation**.  
- Training setup:  
  - Optimizer: **Stochastic Gradient Descent (SGD)**  
  - Loss function: **Sum of Squared Error (SSE)**  
  - Epochs: 1000  

**Architectures Tested**
- **Single hidden layer models:**  
  - [30 → 10 → 1]  
  - [30 → 100 → 1]  
  - [30 → 64 → 1]  
  - [30 → 512 → 1]  

- **Two hidden layer models:**  
  - [30 → 64 → 16 → 1]  
  - [30 → 128 → 32 → 1]  
  - [30 → 256 → 64 → 1]  
  - [30 → 512 → 128 → 1]  


**Training Output**  
- Epoch vs Loss graph plotted for each architecture.  
- Observed decreasing trend in loss (convergence).  
---
### Part B: Neural Network on PCA-transformed Dataset (l = 10)
- Same experiment repeated with PCA-reduced features (10 components).  
- Same architectures tested (single hidden layer & two hidden layers).  
- Performance compared with standardized dataset.  

---

## Example Model (Two-Layer: 128,32)
```python
model = nn.Sequential(
    nn.Linear(30, 128),
    nn.Sigmoid(),
    nn.Linear(128, 32),
    nn.Sigmoid(),
    nn.Linear(32, 1),
    nn.Sigmoid()
)
