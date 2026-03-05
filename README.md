# Credit Card Fraud Detection – Anomaly Detection with KMeans

## Overview
This project demonstrates **anomaly detection** on credit card transactions to identify potential fraudulent activity.  
Credit card fraud is rare: only **0.4% of transactions** are reported as fraudulent, making anomaly detection a suitable approach.

---

## Dataset
- Source: Kaggle (modified version for this project)  
- Each row represents one transaction  
- 30 features including anonymized features and **transaction amount**  
- Dataset is clean: no missing values, no duplicates  

---

## Technologies & Libraries Used
- **Google Colab** – interactive Python environment  
- **Pandas** – data manipulation  
- **NumPy** – numerical operations  
- **scikit-learn**:
  - `StandardScaler` – feature scaling  
  - `KMeans` – clustering for anomaly detection  
  - `set_config` – improved dataframe output  
- **SciPy** – `cdist` to compute distances to cluster centers  
- **Matplotlib & Seaborn** – for visualizations  

---

## Method
1. **Data Scaling:** Standardized all features for fair distance calculations.  
2. **Clustering:** Applied **KMeans** with 3 clusters to group similar transactions.  
3. **Distance Calculation:** Computed each transaction’s distance to the closest cluster center.  
4. **Anomaly Detection:** Transactions above the **99.6th percentile** of distances were flagged as potential fraud.  

---

## Results
- **Total transactions analyzed:** 10,000 *(replace with actual number)*  
- **Anomalies detected (potential fraud):** 40  

### Histogram of Distances to Cluster Centers
<img width="821" height="415" alt="image" src="https://github.com/user-attachments/assets/5a5982b6-b5ae-46c5-98c4-b46e87e88cfd" />

*Red line indicates the anomaly threshold; transactions beyond this line are flagged as potential fraud.*


---

## Conclusion
- KMeans-based anomaly detection successfully highlighted **the most unusual transactions** in the dataset.  
- Flagged transactions can be prioritized for **further investigation**.  
- Demonstrates how **unsupervised learning** can detect rare fraudulent activities in financial data.  

---

## Next Steps / Enhancements
- Compare results with **IsolationForest** for anomaly detection.  
- Apply **PCA** for 2D visualization of clusters and anomalies.  
- Experiment with different **number of clusters** or **percentile thresholds**.  

---

## How to Add Your Images
1. Replace `example_histogram.png` with the actual histogram you plotted using Seaborn.  
2. Add screenshots or tables for the top anomalous transactions to make the README more visual.  
3. Upload the images to your GitHub repo and reference them in the Markdown.

---
for more details text me via farahwadya@gmail.com
