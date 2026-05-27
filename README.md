# Customer Segmentation — Data Modeling & Pipeline

![Python](https://img.shields.io/badge/Python-3.9+-blue)
![ML](https://img.shields.io/badge/ML-K--Means%20Clustering-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## Business Problem
A UK-based online retailer has 4,338 customers but treats them all the same way.
This project segments customers into distinct groups based on their purchase 
behaviour — so the business can target each group with the right strategy.

## Solution
Built an end-to-end customer segmentation pipeline using **RFM Analysis** 
and **K-Means Clustering** on 12 months of real transactional data.

---

## Results

| Segment | Customers | Avg Spend | Revenue Share | Action |
|---|---|---|---|---|
| 🏆 Champions | 713 (16%) | £8,088 | 64.9% | Reward & retain |
| ⚠️ At Risk | 1,166 (27%) | £1,802 | 23.6% | Re-engage urgently |
| 🌱 New & Promising | 837 (19%) | £557 | 5.2% | Nurture & onboard |
| 😴 Lost Customers | 1,622 (37%) | £341 | 6.2% | Win-back or write off |

**Key Finding:** Champions are only 16% of customers but generate 65% of revenue.

---

## Project Structure

customer-segmentation/
├── notebooks/
│   ├── cs_01_eda.ipynb              # Data profiling
│   ├── cs_02_cleaning.ipynb         # Data cleaning
│   ├── cs_03_features.ipynb         # RFM feature engineering
│   ├── cs_04_clustering.ipynb       # K-Means model
│   └── cs_05_visualization.ipynb    # Business charts
├── outputs/
│   └── figures/                     # All saved charts
└── README.md

---

## Tech Stack
- **Python** — Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- **ML** — K-Means Clustering, PCA, StandardScaler
- **Feature Engineering** — RFM Analysis, Log Transformation
- **Platform** — Google Colab + Google Drive

---

## Workflow

Raw Data (541,910 rows)
↓
Data Cleaning → 392,693 clean rows
↓
RFM Feature Engineering → 4,338 customers × 3 features
↓
Log Transform + Standard Scaling
↓
K-Means Clustering (K=4, chosen by Elbow + Silhouette)
↓
4 Business Segments + Visualizations

---

## How to Run

1. Download dataset from [UCI ML Repository](https://archive.ics.uci.edu/dataset/502/online+retail+ii)
2. Upload `online_retail_II.xlsx` to Google Drive at:
   `My Drive/customer-segmentation/data/raw/`
3. Open notebooks in order in Google Colab:
   - `cs_01_eda` → `cs_02_cleaning` → `cs_03_features` → `cs_04_clustering` → `cs_05_visualization`
4. Run all cells in each notebook

---

## Key ML Decisions

**Why RFM?**
Reduces 392,693 transaction rows to 3 meaningful features per customer.
Standard framework used by every major retailer worldwide.

**Why Log Transformation?**
Raw monetary values ranged from £3 to £280,206.
Log compression prevents outliers from dominating clusters.

**Why K=4?**
Both Elbow Method and Silhouette Score agreed on K=4.
Produces 4 actionable business segments — not too broad, not too granular.

**Why PCA for visualization?**
Compresses 3 RFM dimensions into 2 for plotting.
93.9% variance retained — almost no information lost.

---

## Dataset
- **Source:** [Online Retail II — UCI ML Repository](https://archive.ics.uci.edu/dataset/502/online+retail+ii)
- **Period:** December 2010 — December 2011
- **Original size:** 541,910 rows, 8 columns
- **After cleaning:** 392,693 rows, 0 missing values

---

*Project by :
Anshika Sharma *

