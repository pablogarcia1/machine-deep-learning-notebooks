# Credit Card Customers Clustering with PCA & K-Means

This project performs **unsupervised learning** to segment credit card customers based on their spending behavior.  
The analysis uses **Principal Component Analysis (PCA)** for dimensionality reduction and **K-Means clustering** for customer segmentation.

---

## Project Overview
The dataset `CC GENERAL.csv` contains anonymized customer credit card data.  

Steps performed:
1. **Data Preprocessing**
   - Removed the `CUST_ID` column (identifier).  
   - Filled missing values in `MINIMUM_PAYMENTS` and `CREDIT_LIMIT` with the median.  
   - Standardized features using `StandardScaler`.  

2. **Dimensionality Reduction (PCA)**
   - Applied PCA to reduce dimensionality while retaining ~90% of the variance.  
   - Chose the optimal number of components automatically.  
   - Visualized explained variance with a cumulative variance plot.  

3. **Clustering**
   - Applied **K-Means** with 4 clusters.  
   - Added cluster labels back to the dataset.  

4. **Cluster Interpretation**
   - Computed **summary statistics (mean & std)** for each cluster.  
   - Created scaled profiles to highlight relative differences across clusters.  
   - Plotted clusters on the first two PCA components.  
   - Evaluated clustering quality using **Silhouette Score**.  
   - Built **customer profiles** with selected features:  
     - `BALANCE`, `BALANCE_FREQUENCY`, `PURCHASES`, `CREDIT_LIMIT`, `MINIMUM_PAYMENTS`.  
   - Heatmap visualization of average customer profiles per cluster. 