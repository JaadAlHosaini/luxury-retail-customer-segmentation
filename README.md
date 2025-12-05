# Luxury Retail Customer Segmentation using K-Means

This project performs customer segmentation for a luxury retail environment inspired by brands such as Dior, Sephora, and Louis Vuitton.  
The goal is to group customers into meaningful behavioral segments based on their spending, shopping frequency, recency, and product preferences.

## Project Overview

Customer segmentation is essential for luxury brands to understand:

- High-value VIP shoppers  
- Beauty and skincare loyalists  
- Occasional but high-ticket buyers  
- Price-sensitive or low-frequency segments  

By using K-Means clustering, we uncover distinct groups of customers to support targeted marketing, personalized recommendations, and loyalty programs.

---

## Dataset

A synthetic luxury retail dataset was generated containing:

**Demographics**
- Customer ID  
- Age  
- Gender  
- Country  

**Shopping Behavior**
- Total annual spending  
- Number of purchases  
- Visit frequency  
- Recency (days since last purchase)  
- Favorite product category  

**Engineered Features**
- Average basket size  
- Annual spending  
- Normalized spending (0–1 scale)  
- Recency score (0–1 scale)

The dataset contains 3000 customers.

---

## Feature Engineering and Preprocessing

Steps included:

1. Selection of numerical and categorical features  
2. One-hot encoding for categorical variables  
3. Scaling using StandardScaler  
4. Building the final feature matrix for clustering  

---

## Choosing the Number of Clusters (k)

K-Means was run for k = 2 to 10.  
Silhouette scores were compared:

| k | Silhouette Score |
|---|------------------|
| 2 | 0.325 |
| 3 | 0.213 |
| **4** | **0.235** |
| 5 | 0.211 |
| 6 | 0.218 |
| 7 | 0.216 |
| 8 | 0.206 |
| 9 | 0.190 |
| 10 | 0.172 |

Although k = 2 had the highest score, it is not useful for business segmentation.  
Therefore, k = 4 was selected as the optimal balance between quality and interpretability.

---

## Visualizations

### PCA 2D Scatter Plot  
Shows cluster separation in two principal components.

### Spending vs. Frequency  
Identifies buying patterns such as:
- High spenders with high frequency  
- Low spenders with low frequency  

### Cluster Profile Heatmap  
Compares average spending, visits, purchases, and recency across segments.

---

## Business Insights (k = 4)

Each cluster was analyzed based on:
- Size and share of total customers  
- Average spending levels  
- Shopping frequency  
- Recency of visits  
- Top country and category  
- Revenue contribution  

Example insight:

> Cluster 0 represents high-spending luxury shoppers who purchase frequently and have strong preference for makeup and skincare categories. This group contributes a significant share of the total revenue and should be targeted with VIP loyalty programs.

These insights can guide:
- Marketing strategy  
- Personalized recommendations  
- Loyalty reward tiers  
- Inventory planning  

---

## Tech Stack

- Python  
- Pandas / NumPy  
- Scikit-Learn  
- Matplotlib / Seaborn  
- Google Colab  

---

## Files Included

- `customer_segmentation.ipynb` – Full notebook  
- Visualizations (PCA, scatter plots, heatmaps)  
- Generated dataset used for clustering  
- README (this file)

---

## Conclusion

This project demonstrates the use of unsupervised learning to extract meaningful customer segments for luxury retail brands.  
The insights produced can help optimize marketing efforts, improve customer engagement, and increase revenue.

This project is suitable for roles in:

- Data Science  
- Business Analytics  
- Machine Learning  
- MIS  
- Retail Analytics  
