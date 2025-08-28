#K-Nearest Neighbors, Bayes, and Naive Bayes Classifier  

## Dataset  
- **Diabetic Retinopathy Debrecen Data Set**  
- Prepared into train, validation, and test CSVs   
-  **class label** (0 = No Diabetic Retinopathy, 1 = Diabetic Retinopathy)  

---

## Tasks Performed  
---
### 1. K-Nearest Neighbors (KNN) Classifier  
- Implemented **KNN** with `K = 7`  
- Normalized features using:  

  \[
  x_{new} = \frac{x - \mu}{\sigma}
  \]

- Trained on **training set**, validated on **validation set**  
- Evaluated performance on **test set**  

---
### 3. Bayes Classifier  
- Implemented **Bayes Classifier** assuming conditional independence of features  
- Estimated probabilities from training data  
- Classified test data based on maximum posterior probability  

---

### 4. Naive Bayes Classifier  
- Implemented **Naive Bayes** for categorical/continuous features  
- Used conditional probabilities for each attribute given the class  
- Compared results with **KNN** and **Bayes Classifier**  

---


