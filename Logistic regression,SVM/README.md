# Logistic Regression and Support Vector Machines  

## Dataset: Wisconsin Diagnostic Breast Cancer (WDBC)  

1. **Original Dataset**  
   - `WDBC_Train.csv`, `WDBC_Validation.csv`, `WDBC_Test.csv`  
---

## Parts Implemented  

### Part A: Logistic Regression (Original Data)  
- Implemented using `sklearn.linear_model.LogisticRegression`.  
- Plotted **feature importance** from learned weight vector.  
- Evaluated using:  
  - Confusion Matrix  
  - Accuracy, Precision, Recall, F1-score  

### Part B: SVM with Linear Kernel (Original Data)  
- Implemented using `sklearn.svm.SVC(kernel='linear')`.  
- Plotted **weight vector distribution**.  

---

### Part C: SVM with Gaussian (RBF) Kernel (Original Data)  
- Implemented using `sklearn.svm.SVC(kernel='rbf')`.  
- Tuned parameters **C** and **γ (gamma)**.  

---

### Part D: SVM with Polynomial Kernel (Original Data)  
- Implemented using `sklearn.svm.SVC(kernel='poly', degree=3)`.  
- Tuned **C, γ, degree**.  
  
---

## Performance Summary (Original Data)  

| Model                     | Validation Accuracy | Test Accuracy |
|----------------------------|---------------------|---------------|
| Logistic Regression        | 92.98%             | 94.73%        |
| SVM (Linear Kernel)        | 97.36%             | 95.61%        |
| SVM (Gaussian / RBF)       | 85.08%             | 92.98%        |
| SVM (Polynomial Kernel)    | 86.84%             | 92.98%        |

---

