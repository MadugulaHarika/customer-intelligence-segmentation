# Customer Revenue Intelligence System  
### RFM Segmentation + Machine Learning Clustering

---

## Executive Summary

This project develops a Customer Revenue Intelligence framework using RFM (Recency, Frequency, Monetary) analysis and KMeans clustering to segment customers based on purchasing behavior.

The analysis identifies high-value customers, churn-risk segments, and revenue concentration patterns.  
The final output translates machine learning results into actionable business strategies.

This project demonstrates the complete analytics lifecycle:

Data Cleaning → Feature Engineering → Segmentation → Model Validation → Visualization → Revenue Impact Analysis → Strategic Recommendations

---

## Business Problem

Retail businesses often treat all customers equally, leading to inefficient marketing spend and missed revenue opportunities.

Key questions addressed:

- Who are the highest revenue-driving customers?
- Which customers are at risk of churn?
- How concentrated is revenue across segments?
- How can segmentation inform targeted strategies?

---

## Dataset Overview

Transactional retail dataset containing:

- Invoice details
- Customer ID
- Purchase dates
- Quantity
- Unit price

Customer-level features were engineered from transaction-level data.

---

## Data Preparation

Performed:

- Removal of cancelled transactions
- Filtering negative quantities
- Handling missing Customer IDs
- Creation of total transaction amount

Ensured data integrity before feature engineering.

---

## Feature Engineering: RFM Metrics

Each customer was summarized using:

- **Recency** – Days since last purchase  
- **Frequency** – Total number of transactions  
- **Monetary** – Total revenue generated  

These features capture behavioral purchasing patterns.

---

## Rule-Based Segmentation (Baseline)

Customers were first segmented using quantile-based RFM scoring.

This provided an interpretable, business-driven segmentation baseline before applying machine learning.

---

## Machine Learning Segmentation

### Model Used
KMeans Clustering

### Preprocessing
- StandardScaler applied to RFM features

### Number of Clusters
4

---

## Model Validation

### Silhouette Score
0.3363

This indicates moderate but meaningful separation between clusters.

In real-world retail behavioral data, perfect separation is uncommon due to overlapping purchasing patterns.

---

## PCA Visualization

Principal Component Analysis (PCA) was used to reduce RFM features to two dimensions for visualization.

The PCA projection demonstrated:

- Clear structural grouping
- Meaningful cluster separation
- Expected overlap between adjacent behavioral segments

This supports clustering validity visually.

---

## Cluster Profiling

Average RFM values revealed four distinct behavioral segments:

### 1. Champions
- Most recent purchases
- Highest transaction frequency
- Highest monetary contribution
- Core revenue drivers

### 2. Regular Customers
- Moderate recency and spending
- Strong upselling opportunity

### 3. New / Low Value
- Recently acquired
- Low monetary contribution
- Nurturing potential

### 4. At Risk
- Long time since last purchase
- Low frequency and spending
- High churn probability

---

## Revenue Contribution Analysis

Total revenue contribution by segment:

- Champions: 5.79M
- Regular Customers: 2.11M
- At Risk: 0.54M
- New / Low Value: 0.45M

### Key Insight

Champions generate the majority of total revenue.

Revenue is highly concentrated within a relatively smaller high-value segment, highlighting the importance of retention-focused strategies.

---

## Strategic Business Recommendations

- Implement loyalty programs for Champions  
- Develop upselling campaigns for Regular Customers  
- Create onboarding engagement flows for New customers  
- Launch targeted reactivation campaigns for At Risk customers  

---

## Advanced Components Implemented

- RFM feature engineering
- Rule-based segmentation
- KMeans clustering
- Silhouette score validation
- PCA dimensionality reduction
- Cluster profiling
- Revenue contribution quantification
- Business translation of ML outputs

---

## Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook
- Git & GitHub

---

## Project Impact

This project demonstrates the ability to:

- Translate raw transaction data into customer intelligence
- Apply unsupervised machine learning appropriately
- Validate clustering performance
- Convert model outputs into business strategy
- Communicate insights in executive-ready format

---

## Author

Madugula Harika  
Data Science | Customer Analytics | Machine Learning