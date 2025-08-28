 Outlier Detection, Standardization, Normalization and Correlation of Data

**Dataset Used:** `landslide_data_original.csv`

This dataset contains sensor readings (temperature, humidity, pressure, rain, etc.) collected from 10 locations in the Mandi district, Himachal Pradesh.

---

## Problem Statement 1 (Compulsory)

### 1. Outlier Detection
- Identified **outliers** using the IQR method:  
  \[
  (Q1 - 1.5 \times IQR) < x < (Q3 + 1.5 \times IQR)
  \]  
- Replaced outliers with the **median** of the attribute.  
- Plotted boxplots again to compare before and after outlier correction.  

---

### 2. Correlation
- Computed **Pearson’s** and **Spearman’s** correlation coefficients for all attribute pairs  
- Visualized correlations using a **heatmap**.  
- Chose **`rain`** as the target attribute:  
  - Found correlations of `rain` with all other attributes (Pearson & Spearman).  
---

### 3. Standardization and Normalization
- Performed **Min-Max Normalization**:
  - Range (0–1) without using inbuilt libraries.  
  - Range (0–20) without using inbuilt libraries.  
  - Repeated the same using **Scikit-learn (`MinMaxScaler`)**.  
- Performed **Standardization**:
  - Applied formula:  
    \[
    x_{new} = \frac{x - \mu}{\sigma}
    \]  
  - Repeated using **Scikit-learn (`StandardScaler`)**.  
- Compared correlation results between **raw**, **normalized**, and **standardized** datasets.  

---

## Tools & Libraries Used
- Python (Pandas, NumPy, Matplotlib, Seaborn)  
- Scikit-learn (for normalization & standardization)  

---

## Outputs
- **Outlier-corrected file:** `landslide_data_corrected.csv`  
- Normalized datasets (0–1, 0–20 ranges)  
- Standardized dataset  
- Multiple plots for data analysis  
