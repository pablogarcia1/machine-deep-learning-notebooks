# 🪙 Bitcoin Clustering Analysis (2020–2024)
**Author: Jose Pablo Garcia Meza**

This project applies **unsupervised machine learning** techniques to analyze Bitcoin (`BTC-USD`) historical data (price and volume) from 2020 to 2024.  
The goal is to identify market patterns (e.g., bull runs, sideways movements, bear markets) using clustering algorithms.

---

## 📊 Dataset
- Source: [Yahoo Finance](https://finance.yahoo.com/)
- Asset: **BTC-USD**
- Interval: Daily data (`1d`)
- Time range: `2020-01-01` → `2024-01-01`
- Features used:
  - `Price` (closing price in USD)
  - `Volume` (trading volume)

---

## ⚙️ Preprocessing
1. Download historical BTC data with `yfinance`.
2. Select and rename features (`Price`, `Volume`).
3. Standardize with `StandardScaler`.
4. Remove outliers using the **IQR rule**.
5. Apply logarithmic transformations to reduce skewness.

---

## 🤖 Clustering Methods

### 1. K-Means
- Applied with **3 clusters**.
- Optimal number of clusters selected using the **Elbow Method**.
- Captures **bull runs, sideways markets, and bear trends**.

### 2. DBSCAN
- Density-based clustering.
- Highlights outliers effectively.
- Sensitive to `eps` and `min_samples` hyperparameters.
- Hyperparameter tuning performed via manual search and grid search with **silhouette score**.

---

## 📈 Visualizations
- **Price vs Volume clustering**
- **BTC Price over time with cluster assignments**
- **Comparison of KMeans and DBSCAN results**

Examples:

- Clustering with KMeans:  
  ![KMeans clustering](assets/kmeans.png)

- Clustering with DBSCAN:  
  ![DBSCAN clustering](assets/dbscan.png)

---

## 🔧 Hyperparameter Tuning
For DBSCAN:
- Grid search on:
  - `eps ∈ [0.001, 1]`
  - `min_samples ∈ {15, 20, 30}`
- Best combination selected using **silhouette score**.

---

##
