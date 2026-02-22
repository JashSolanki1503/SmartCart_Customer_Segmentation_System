# 🛒 SmartCart Customer Segmentation System

## 📌 Project Overview

SmartCart is a growing e-commerce platform serving customers across multiple countries.
Currently, the company uses **generic marketing strategies** for all users, which leads to:

* Inefficient marketing campaigns
* Poor customer targeting
* Missed opportunities to retain high-value customers
* Delayed identification of churn-prone users

This project builds an **Unsupervised Machine Learning-based Customer Segmentation System** to group customers into meaningful clusters based on purchasing behaviour, engagement levels, and loyalty indicators.

---

## 🎯 Project Objective

To develop an intelligent clustering system that:

* Identifies distinct customer segments
* Enables data-driven marketing strategies
* Improves customer retention
* Supports personalized engagement

---

## 📂 Dataset Description

The dataset contains **2240 customer records** with 22 attributes including:

### 1️⃣ Demographics

* Year_Birth
* Education
* Marital_Status
* Income
* Kidhome
* Teenhome
* Dt_Customer

### 2️⃣ Purchase Behaviour (Spending)

* MntWines
* MntFruits
* MntMeatProducts
* MntFishProducts
* MntSweetProducts
* MntGoldProds

### 3️⃣ Purchase Frequency

* NumWebPurchases
* NumCatalogPurchases
* NumStorePurchases
* NumDealsPurchases
* NumWebVisitsMonth

### 4️⃣ Customer Engagement

* Recency
* Complain

---

## 🛠️ Project Workflow

### 1️⃣ Data Cleaning

* Handled missing values using **Median Imputation** (Income was slightly skewed).
* Cleaned categorical inconsistencies.

---

### 2️⃣ Feature Engineering

To improve clustering quality and reduce dimensional noise:

* Created **Age** from Year_Birth
* Created **Customer_Tenure_Days** from Dt_Customer
* Created **Total_Spending** (sum of all product spending)
* Created **Total_Children** (Kidhome + Teenhome)
* Simplified categorical variables (Education & Marital_Status grouping)

👉 Focus: Behaviour-based feature construction.

---

### 3️⃣ Exploratory Data Analysis (EDA)

* Correlation Heatmap
* Feature Distribution Analysis
* Outlier Observations

---

### 4️⃣ Data Preprocessing

* Label Encoding / Category Simplification
* Feature Scaling using StandardScaler
* PCA for 2D & 3D visualization

---

### 5️⃣ Clustering Algorithms Applied

* K-Means Clustering
* Agglomerative (Hierarchical) Clustering
* DBSCAN (Density-Based Clustering)

---

### 6️⃣ Optimal Cluster Selection

Used:

* Elbow Method
* Silhouette Score

Final selection based on:

* Balanced elbow point
* Strong silhouette score
* Business interpretability

For this particular project best Clusturing algorithm is : Agglomerative (Hierarchical) Clustering
because inside this algorithm clustures are well seperated as compare to other clusturing algorithms

---

## 📊 Final Cluster Insights

### 🔵 Cluster 0 – Low Value Browsers

* More children
* High website visits but low purchases
* Low total spending
* Poor response rate

---

### 🟢 Cluster 1 – High Value Loyal Customers

* Fewer children
* High total spending
* High web, catalog & store purchases
* Stable engagement

---

### 🟡 Cluster 2 – Low Spending Family Segment

* More children
* Living alone
* Very low spending
* Low catalog/store purchases

---

### 🔴 Cluster 3 – Premium Responsive Customers

* Very fewer children
* Higher response rate
* High spending
* High purchase frequency

---

## 📈 Key Learnings

* Feature engineering defines cluster quality.
* Scaling is mandatory for distance-based algorithms.
* Outlier detection and removal is crucial in Unsupervised Learning, especially for distance-based algorithms like KMeans, because extreme values can distort centroid positions and lead to incorrect cluster formation.
* Cluster interpretation is more important than algorithm selection.
* Behaviour-based features improve segmentation clarity.

---

## 🚀 Business Impact

This segmentation system can help SmartCart:

* Target high-value customers with loyalty rewards
* Re-engage inactive browsers
* Identify churn-risk customers
* Optimize marketing campaigns

---

## 🧠 Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib & Seaborn
* Scikit-learn
* Scipy for Dendrogram Creation and Computations

---

## 📌 Future Improvements

* Deploy using Streamlit
* Automate cluster prediction for new customers
* Create customer persona dashboard
* Compare advanced clustering methods

---

## 👨‍💻 Author

Jash Solanki
BTech | AI/ML Enthusiast

---

⭐ If you found this project useful, consider giving it a star!
