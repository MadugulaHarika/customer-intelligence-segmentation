📊 Customer Intelligence & Advanced RFM Segmentation
🚀 Project Overview

This project performs end-to-end Customer Intelligence Analysis using:

Rule-based RFM Segmentation

Machine Learning (KMeans Clustering)

Revenue contribution analysis

Strategic business recommendations

The goal is to identify high-value customers, detect churn risks, and provide data-driven marketing strategies.

🎯 Business Problem

Retail businesses struggle to:

Identify high lifetime value customers

Detect customers at risk of churn

Allocate marketing budgets efficiently

Convert mid-tier customers into loyal buyers

This project addresses these challenges using structured behavioral segmentation and machine learning validation.

🛠️ Tech Stack

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

Jupyter Notebook

Git & GitHub

📂 Project Structure
customer-intelligence-segmentation/
│
├── data/
│   └── Online Retail.xlsx
│
├── notebooks/
│   ├── 01_EDA.ipynb
│   └── 02_RFM_and_ML_Segmentation.ipynb
│
├── README.md
└── .gitignore
🔎 Phase 1: Exploratory Data Analysis (EDA)
Data Cleaning Performed

Removed negative quantities (canceled transactions)

Removed duplicates

Handled missing Customer IDs

Created Revenue column

Key Findings

Revenue is concentrated among a small group of customers

Significant number of inactive buyers

Presence of transaction cancellations

High variance in customer purchase frequency

📊 Phase 2: RFM Segmentation (Rule-Based)
RFM Metrics

Recency – Days since last purchase

Frequency – Number of transactions

Monetary – Total customer spend

Customers were segmented into:

Champions

Potential Loyalists

Loyal Customers

At Risk

Lost Customers

New Customers

💰 Revenue Contribution Insights

Champions (~11% of customers) generate ~50% of total revenue.

Potential Loyalists represent the largest customer base (~47%).

At Risk customers contribute significant revenue (~11%).

Lost customers contribute minimal revenue (~3%).

Revenue is heavily concentrated among a small high-value segment, demonstrating a strong Pareto distribution.

🤖 Phase 3: Machine Learning Segmentation (KMeans)

To validate rule-based segmentation, KMeans clustering was applied.

ML Pipeline

Log transformation to reduce skewness

Standard scaling

Elbow method to determine optimal clusters (k = 4)

KMeans clustering

Cluster interpretation

ML Cluster Interpretation
ML Segment	Behavioral Pattern
High Value Customers	Very recent, high frequency, high spend
At Risk Customers	Previously active, declining recency
Regular Customers	Moderate frequency and spend
Lost Customers	Inactive, low frequency, low spend
RFM vs ML Comparison

Strong alignment for Champions and Lost segments.

ML revealed that some “Potential Loyalists” were behaviorally closer to At Risk or Lost groups.

Demonstrates limitations of static threshold-based segmentation.

This dual approach strengthens analytical validity.

📈 Key Strategic Insights

A small percentage of customers drive disproportionate revenue.

Over 60% of customers fall into At Risk or Lost categories (churn risk).

Potential Loyalists represent the largest growth opportunity.

Retention-focused strategies are more impactful than acquisition-heavy approaches.

🎯 Business Recommendations
Segment	Strategy
High Value	Loyalty rewards and exclusive benefits
At Risk	Targeted discounts and reactivation campaigns
Regular	Upselling and cross-selling
Lost	Low-cost win-back campaigns
🚀 Future Improvements

Add Silhouette Score for cluster validation

Add PCA visualization for cluster separation

Build interactive dashboard (Power BI or Streamlit)

Explore churn prediction modeling

📌 Project Status

Data Cleaning & EDA ✅

RFM Segmentation ✅

Revenue Analysis ✅

Machine Learning Clustering ✅

Cluster Validation & Visualization (Next Phase)

💡 Conclusion

This project demonstrates how combining rule-based analytics with machine learning can provide deeper behavioral segmentation, improve marketing precision, and optimize revenue strategies.

It transforms raw transaction data into actionable customer intelligence.