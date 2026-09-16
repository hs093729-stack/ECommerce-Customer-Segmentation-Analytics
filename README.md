# 🛒 Advanced E-Commerce Customer Segmentation & LTV Analytics

## 📌 Ecosystem Overview
This repository hosts an unsupervised customer lifecycle analytics framework that aggregates and filters over 540,000 lines of messy, real-world transactional records. By engineering Recency, Frequency, and Monetary (RFM) behavioral metrics and correcting heavy financial data skewness, this system maps structural customer groups to drive high-conversion marketing campaign allocations.

## 🛠️ Corporate Tech Stack
* **Data Core:** Python, Pandas, NumPy, Datetime Operations
* **Clustering & Scaling:** Scikit-Learn (K-Means++, StandardScaler, Silhouette Score)
* **Reporting Blueprint:** Matplotlib, Seaborn, Power BI KPI Wireframing

## 🔄 Data Pipeline Architecture
1. **Transaction Sanitization:** Filtered out over 135,000 rows missing unique customer tokens to isolate concrete purchasing tracks; canceled out operational invoice entries containing negative values (returns and damaged stock corrections).
2. **RFM Aggregation:** Processed historical transaction timelines against a modern business snapshot matrix to calculate Recency (days since last purchase), Frequency (distinct invoices), and Monetary Value (total capital spent per customer).
3. **Variance Scaling:** Flattened immense revenue distribution gaps (\$3.75 to \$280K) using Logarithmic Rescaling (`np.log1p`) and standardized parameters via `StandardScaler` to remove distance-mapping bias.
4. **Grid Optimization:** Executed a 1-to-10 cluster WCSS loop, identifying the sharp mathematical elbow bend at exactly **k=3** cohorts.

## 📈 Executive Key Results & Business Value
* **Cohort Segmentation:** Partitioned 4,338 unique global customer lifecycles with a solid **0.3360 Score** into three high-value business groups:
  * **Loyal Champions (776 Users):** Elite purchasers ordering ~13 times with an average spend of **\$7,865**.
  * **Stable Regular Spenders (1,696 Users):** Core transactional users buying every 44 days.
  * **Hibernating / High-Risk (1,866 Users):** Slipping accounts with zero orders in 167 days.
* **Power BI Blueprint:** Designed an enterprise 3-tier layout featuring behavioral scatter matrices and regional slicer drop-downs to translate numbers into clear visual directions.
