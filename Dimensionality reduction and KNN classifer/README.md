#Dimensionality Reduction and K-Nearest Neighbor Classifier

## Dataset
- **File used:** `WisconsinDiagnosticBreastCancer.csv`

## Tasks Completed

### Part A: Data Preparation
- Split the dataset into:
  - **Training (60%)** → `WDBC Train.csv`  
  - **Validation (20%)** → `WDBC Validation.csv`  
  - **Testing (20%)** → `WDBC Test.csv`  
---
### Part B: Standardization
- Applied **Standardization**:  
  $$
  x_{new} = \frac{x - \mu}{\sigma}
  $$
---

### Part C: Principal Component Analysis (PCA)
   - Performed PCA on training data.  
   - PCA with **2 components (l = 2):**
     - Saved as `WDBC PCA2 Train.csv`, `WDBC PCA2 Validation.csv`, `WDBC PCA2 Test.csv`  
   - PCA with **10 components (l = 10):**
     - Saved as `WDBC PCA10 Train.csv`, `WDBC PCA10 Validation.csv`, `WDBC PCA10 Test.csv`  

---

### Part D: K-Nearest Neighbor (KNN) Classification on Original Data
- Implemented **KNN** classifier with K = 1, 7, 11.  
- Evaluated using:
  - Confusion Matrix  
  - Accuracy  
  - Precision  
  - Recall  
  - F1-score  
- Selected the best K and evaluated on test data.  
---


