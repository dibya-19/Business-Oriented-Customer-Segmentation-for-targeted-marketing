# Business-Oriented Customer Segmentation using Unsupervised Machine Learning for Targeted Marketing

> **Identifying meaningful customer segments using K-Means Clustering and Principal Component Analysis (PCA) to enable data-driven marketing and business decision-making.**

---

## Project Overview

Customer segmentation is a fundamental business strategy that helps organizations understand differences in customer purchasing behavior. Instead of treating every customer equally, businesses can group customers with similar characteristics and design personalized marketing strategies.

In this project, I developed an end-to-end customer segmentation pipeline using the **Wholesale Customers Dataset** from the UCI Machine Learning Repository. By applying **Exploratory Data Analysis (EDA)**, **Log Transformation**, **Feature Scaling**, **Principal Component Analysis (PCA)**, and **K-Means Clustering**, the project identifies meaningful customer groups and translates the results into actionable business insights.

---

## Business Problem

Wholesale businesses often use the same marketing strategy for every customer despite significant differences in purchasing behavior.

This leads to:

- Inefficient promotional campaigns
- Poor inventory planning
- Lower customer engagement
- Reduced profitability

The goal of this project is to identify distinct customer segments based on purchasing patterns and provide business recommendations for targeted marketing.

---

## Dataset

**Source:** UCI Machine Learning Repository

**Dataset:** Wholesale Customers Dataset

### Features Used

- Fresh
- Milk
- Grocery
- Frozen
- Detergents_Paper
- Delicassen

> *Channel* and *Region* were excluded from clustering to focus on spending behavior.

---

## Project Workflow

```text
Business Understanding
        │
        ▼
Data Exploration (EDA)
        │
        ▼
Data Cleaning
        │
        ▼
Log Transformation
        │
        ▼
Feature Scaling (StandardScaler)
        │
        ▼
Principal Component Analysis (PCA)
        │
        ▼
K-Means Clustering
        │
        ▼
Elbow Method
        │
        ▼
Silhouette Score
        │
        ▼
Cluster Profiling
        │
        ▼
Business Insights & Recommendations
```

---

## Exploratory Data Analysis

The exploratory analysis revealed:

- Highly right-skewed spending distributions
- Presence of genuine high-value customers (outliers)
- Strong positive correlation among Milk, Grocery, and Detergents_Paper
- Different purchasing patterns across product categories

These observations guided the preprocessing strategy before clustering.

---

## Data Preprocessing

The following preprocessing techniques were applied:

- Log Transformation (`log1p`) to reduce skewness
- StandardScaler for feature standardization
- Principal Component Analysis (PCA) for dimensionality reduction

PCA retained approximately **92% of the dataset's variance** using the first four principal components.

---

## Clustering Methodology

The project uses **K-Means Clustering** because it:

- Efficiently groups similar observations
- Works well with standardized numerical features
- Produces interpretable customer segments

The optimal number of clusters was determined using:

- Elbow Method
- Silhouette Score

Final number of clusters:

**K = 3**

---

## Customer Segments

### Cluster 0 – Retail & Grocery Customers

**Characteristics**

- High Milk spending
- High Grocery spending
- High Detergents & Paper spending
- Lower Fresh spending

**Business Strategy**

- Grocery bundles
- Household product promotions
- Loyalty rewards

---

### Cluster 1 – Fresh Food Buyers

**Characteristics**

- High Fresh spending
- High Frozen spending
- Lower Grocery spending

**Business Strategy**

- Seasonal offers
- Fresh produce promotions
- Frozen product bundles

---

### Cluster 2 – High-Value Bulk Buyers

**Characteristics**

- High spending across nearly all product categories

**Business Strategy**

- Premium customer programs
- Volume discounts
- Dedicated account management

---

## Visualizations

The project includes:

- Histograms
- Boxplots
- Correlation Heatmap
- Elbow Curve
- Silhouette Score Analysis
- Cluster Heatmap
- Cluster-wise Bar Chart
- PCA Scatter Plot

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Repository Structure

```text
Customer-Segmentation/
│
├── data/
│   └── Wholesale customers data.csv
│
├── notebooks/
│   └── Customer_Segmentation.ipynb
│
├── images/
│   ├── heatmap.png
│   ├── elbow_curve.png
│   ├── pca_clusters.png
│   └── ...
│
├── report/
│   └── Customer_Segmentation_Report.pdf
│
├── README.md
├── requirements.txt
└── LICENSE
```

---

## Business Impact

The generated customer segments can help businesses:

- Improve customer targeting
- Personalize marketing campaigns
- Optimize inventory management
- Increase customer retention
- Support data-driven business decisions

---

## Future Improvements

Possible future enhancements include:

- Compare K-Means with DBSCAN and Hierarchical Clustering
- Include customer demographic information
- Build an interactive Streamlit dashboard
- Deploy the project as a web application
- Perform real-time customer segmentation

---

## Results

- Successfully identified **3 distinct customer segments**
- Generated business-oriented customer profiles
- Visualized customer groups using PCA
- Produced actionable marketing recommendations

---

## References

- UCI Machine Learning Repository – Wholesale Customers Dataset
- Scikit-learn Documentation
- Pandas Documentation
- NumPy Documentation
- Matplotlib Documentation
- Seaborn Documentation

---

## Author

**Dibya Lochan**

Final Year B.Tech CSE (AI/ML & Data Science)

Feel free to connect with me on LinkedIn and explore more of my projects!

---

⭐ If you found this project useful, consider giving the repository a star!
