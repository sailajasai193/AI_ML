# KMeans and KMediod Clustering  



##  Problem Statement  
given the **Iris flower dataset (Iris.csv)** containing **150 samples** with **4-dimensional features**:    
- Each sample belongs to one of three species: **Iris-setosa, Iris-versicolor, Iris-virginica**.  


---

###  1. Data Preprocessing & Dimensionality Reduction  
- Loaded dataset (`Iris.csv`).  
- Normalized all features using **StandardScaler**.  
- Applied **PCA → 2 principal components**.  
- Saved the reduced dataset as **iris_dataset_2D.csv**.  

---

###  2. K-Means Clustering  
- Applied **K-Means (k=3)** on the reduced dataset.  
- Visualized clusters with **different colors** and **marked cluster centers**.
- used inertia and purity score for evaluation
- Repeated for `k = 2, 4, 6, 10`.  
- **Elbow Method:** Optimal `k = 4`.  
- **Inertia (k=4):** `89.80`.  
- **Purity Score (k=4):** `0.85`.  

---

###  3. K-Medoids Clustering  
- Applied **K-Medoids (k=3)** on PCA-reduced data.  
- Repeated for `k = 2, 4, 6, 10`.  
- **Elbow Method:** Optimal `k = 4`.  
- **Inertia (k=4):** `97.37`.  
- **Purity Score (k=4):** `0.84`.  

---

##  Results Summary  

| Algorithm  | Optimal K | Inertia | Purity Score |
|------------|-----------|---------|--------------|
| **K-Means**   | 4         | 89.80   | 0.85 |
| **K-Medoids** | 4         | 97.37   | 0.84 |

- Both algorithms achieved **high purity (~85%)**.  
- **K-Means performed slightly better** in terms of inertia and purity.  
  

---

##  Conclusion  
- Dimensionality reduction via PCA preserved the class separability of Iris dataset.  
- K-Means and K-Medoids gave **comparable results**, with **K-Means showing slightly better clustering quality**.  
- **Optimal number of clusters = 4**, as determined using the **elbow method**.  

---
