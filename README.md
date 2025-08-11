# 🛍️ Customer Segmentation Using RFM Analysis in E-Commerce

## 📌 Introduction
In e-commerce, understanding customer purchasing behavior is key to driving personalized marketing strategies and improving overall customer retention.  
**RFM Analysis** — based on **Recency, Frequency, and Monetary value** — is a proven method to segment customers according to their transaction patterns, enabling data-driven business decisions.

This project applies **RFM Analysis** on transactional data from an e-commerce platform to identify distinct customer groups and recommend tailored engagement strategies for each.

---

## 🎯 Project Objectives
- **Customer Segmentation** – Group customers based on RFM scores using clustering techniques.  
- **Actionable Insights** – Identify the characteristics of each segment and propose targeted marketing strategies.  
- **Visualization** – Use **PCA (Principal Component Analysis)** to visualize customer clusters in a reduced-dimensional space.  

---

## 📊 Dataset Overview
- **Source**: E-commerce transactional dataset  
- **Columns**: `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`  
- **Size**: 541,909 rows × 8 columns  
- **Period**: 1-year transactional data  

**Data Cleaning Steps**:  
- Removed rows with missing `CustomerID` and `Description`.  
- Converted `InvoiceDate` to datetime format.  
- Removed negative quantities (returns) when appropriate.  

---

## 🛠️ Methodology

### **1. Feature Engineering**
- **Total Spending** = `Quantity × UnitPrice`  
- Extracted date components (year, month, day) from `InvoiceDate`.

### **2. RFM Metrics**
- **Recency** – Days since last purchase.  
- **Frequency** – Total number of transactions.  
- **Monetary** – Total amount spent.  

### **3. Scaling & Clustering**
- Scaled features using **StandardScaler**.  
- Determined optimal clusters using **Elbow Method**.  
- Applied **K-Means Clustering (k=3)**.  

### **4. Evaluation**
- **Silhouette Score**: `0.60` → Good cluster separation.  
- Visualized clusters using **PCA (2 components)**.  

---

## 📌 Results & Insights

### **Cluster 0** – Dormant/Low-Value Customers  
- **Recency**: ~246 days  
- **Frequency**: Low  
- **Monetary**: Low  
- **Strategy**: Reactivation campaigns, discounts, awareness offers.  

### **Cluster 1** – Loyal & Moderate Spenders  
- **Recency**: ~40 days  
- **Frequency**: Moderate  
- **Monetary**: Moderate  
- **Strategy**: Upselling, loyalty rewards, personalized recommendations.  

### **Cluster 2** – High-Value/VIP Customers  
- **Recency**: ~4 days  
- **Frequency**: Very high  
- **Monetary**: Very high  
- **Strategy**: VIP perks, exclusive offers, personal account management.  

---

## 📈 Visualizations
- **Sales Trends** – By month, top customers, top countries.  
- **RFM Distribution** – Understanding customer value patterns.  
- **PCA Scatterplot** – Cluster visualization in reduced dimensions.  

---

## 🧩 Tech Stack
- **Python** – Data cleaning, analysis, visualization  
- **Libraries**:  
  - `pandas`, `numpy` – Data manipulation  
  - `matplotlib`, `seaborn` – Visualization  
  - `scikit-learn` – Scaling, clustering, PCA, evaluation  

---
