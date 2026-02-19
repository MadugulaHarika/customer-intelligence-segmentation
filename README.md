# AI-Powered Customer Intelligence & Revenue Optimization System

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn (planned)
- Jupyter Notebook

---

## Project Structure
1. Project Objective

The objective of this project is to build an end-to-end customer intelligence system using retail transaction data to:

- Perform customer segmentation
- Analyze revenue behavior
- Prepare for churn modeling
- Enable revenue optimization strategies

2. Dataset Overview

- Dataset: Online Retail Transaction Data
- Source: UCI Machine Learning Repository
- Initial Rows: 541,909
- Columns: 8
- Unique Customers: 4,372
- Granularity: Transaction-level (each row represents one product in an invoice)

3. Initial Data Observations
Missing Values
- Description: 1,454 missing
- CustomerID: 135,080 missing (~25%)
CustomerID is critical for customer-level analysis.

Negative Quantities
- 3,836 cancelled invoices (InvoiceNo starting with "C")
- 1,336 rows had negative quantities without cancellation prefix
- These rows lacked CustomerID, Description, and UnitPrice
- Likely system adjustments or corrupted entries

4. Data Cleaning Decisions
To prepare data for customer intelligence modeling:
- Removed rows with missing CustomerID
    Required for segmentation and churn modeling
- Removed rows with Quantity ≤ 0
    Represent returns, cancellations, or system adjustments

After cleaning:
- Final Rows: 397,924

5. Feature Engineering
Created new feature:
TotalPrice = Quantity × UnitPrice
This represents revenue per transaction and is critical for:
- RFM analysis
- Revenue optimization
- Customer segmentation