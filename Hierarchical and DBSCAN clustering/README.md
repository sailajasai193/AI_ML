#  Hierarchical and DBSCAN Clustering  


##  Problem Statement  
We are given the **Iris dataset (Iris.csv)** containing **150 samples**, each with **4 attributes**:  
- Sepal Length, Sepal Width, Petal Length, Petal Width (cm).  
- Class label (Species: *Iris-setosa, Iris-versicolor, Iris-virginica*).  

### Tasks  
2. Perform **Agglomerative Hierarchical Clustering** with different linkage methods.  
3. Plot **dendrogram** and determine the optimal number of clusters.  
4. Perform **DBSCAN clustering** with different parameter combinations.    

---

### 1. Data Preprocessing and Dimensionality Reduction  
- Normalized dataset using `StandardScaler`.  
- Applied **PCA → 2 principal components**.  
- Saved reduced dataset as **iris_dataset_2D.csv**.  
- Visualized the 2D dataset with species labels.  

---

###  2. Hierarchical (Agglomerative) Clustering  
- Applied clustering with **n_clusters = 3** using different linkages:  

| Linkage   | Purity Score |
|-----------|--------------|
| Ward      | **0.8067** |
| Complete  | 0.6800 |
| Average   | 0.6667 |
| Single    | 0.6667 |

- **Ward linkage** gave the **highest purity (0.8067)**.  
- Plotted **dendrogram** (threshold=6) → **optimal clusters = 5**.  
- For `n_clusters=5`, purity score = **0.8067** (same as Ward 3-clusters).  
---

###  3. DBSCAN Clustering  
- **Default parameters:** `eps=0.5`, `min_samples=5`  
  - Purity Score = **0.6800**  

- **Comparison with other methods (k=3):**  
  - K-Means: 0.6667  
  - Agglomerative (Ward): **0.8067**  
  - DBSCAN: 0.6800  

- **Parameter tuning:**  
  - Tried combinations of `eps ∈ {0.5, 1.0}` and `min_samples ∈ {4, 10}`.  
  - Results:  

| eps | min_samples | n_clusters | Purity |
|-----|-------------|------------|--------|
| 0.5 | 4           | 2          | **0.6783** |
| 0.5 | 10          | 2          | 0.6769 |
| 1.0 | 10          | 2          | 0.6735 |
| 1.0 | 4           | 2          | 0.6644 |

---

##  Results Summary  

| Algorithm        | Optimal Params | Purity Score |
|------------------|----------------|--------------|
| **K-Means**      | k = 3          | 0.6667 |
| **K-Medoids**    | k = 4 (Lab 11) | 0.84 |
| **Agglomerative**| Ward, k = 3    | **0.8067** |
| **DBSCAN**       | eps=0.5, min_samples=4 | 0.6783 |

---

## Conclusion  
- **Agglomerative (Ward linkage)** achieved the **highest purity (0.8067)** among hierarchical methods.  
- **K-Medoids (Lab 11)** gave even higher purity (**0.84**) compared to DBSCAN and K-Means.  
- **DBSCAN** struggled with the Iris dataset due to overlapping clusters and parameter sensitivity.  
- **Optimal clusters = 5** (from dendrogram), but purity remained similar to 3-cluster case.  

---
