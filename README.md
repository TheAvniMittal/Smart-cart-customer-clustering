# SmartCart Customer Clustering

Segmenting 2,240 retail customers into 4 actionable groups using KMeans & Agglomerative Clustering with PCA visualization, to drive targeted marketing decisions.

**Live Demo:** [theavnimittal.github.io/Smart-cart-customer-clustering](https://theavnimittal.github.io/Smart-cart-customer-clustering/)

![Python](https://img.shields.io/badge/Python-3.9+-blue?style=flat-square)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-orange?style=flat-square)
![pandas](https://img.shields.io/badge/pandas-2.x-green?style=flat-square)
![matplotlib](https://img.shields.io/badge/matplotlib-3.x-red?style=flat-square)

---

## Problem Statement

Understanding customer behavior is key to personalized marketing. This project segments customers based on demographics, purchase history, and spending habits — revealing distinct groups that can guide business decisions like targeted promotions, inventory planning, and loyalty programs.

---

## Dataset

**File:** `data/smartcart_customers.csv`

| Feature | Description |
|---|---|
| `Income` | Annual household income |
| `Recency` | Days since last purchase |
| `MntWines`, `MntFruits`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds` | Spending per category |
| `NumCatalogPurchases`, `NumStorePurchases` | Purchase channel behavior |
| `Year_Birth`, `Education`, `Marital_Status`, `Kidhome`, `Teenhome` | Demographics |

---

## ML Pipeline

| Step | Method |
|---|---|
| Missing value handling | Median imputation |
| Feature engineering | Age, customer tenure, total spending, family size |
| Encoding | OneHotEncoder (Education, Marital Status) |
| Scaling | StandardScaler |
| Dimensionality reduction | PCA — 3 components |
| Optimal K selection | Elbow Method + Silhouette Score |
| Clustering | KMeans & Agglomerative Clustering (Ward linkage) |

---

## Cluster Profiles

| Cluster | Label | Profile | Recommended Action |
|---|---|---|---|
| 0 | Budget shoppers | Low income, low spending | Value deals & discounts |
| 1 | Premium buyers | High income, high spending | Upsell premium products |
| 2 | Catalog buyers | Mid income, catalog-heavy | Targeted catalog campaigns |
| 3 | Disengaged | High recency, low activity | Win-back offers |

---

## Project Structure

```
smart-cart-customer-clustering/
│
├── README.md
├── requirements.txt
├── .gitignore
├── index.html                        # Live dashboard (GitHub Pages)
│
├── data/
│   └── smartcart_customers.csv
│
├── notebooks/
│   └── clustering_system.ipynb
│
└── outputs/
    └── cluster_summary.csv
```

---

## How to Run

```bash
# 1. Clone the repo
git clone https://github.com/theavnimittal/Smart-cart-customer-clustering.git
cd Smart-cart-customer-clustering

# 2. Install dependencies
pip install -r requirements.txt

# 3. Place the dataset
# Add smartcart_customers.csv inside the data/ folder

# 4. Open the notebook
jupyter notebook notebooks/clustering_system.ipynb
```

---

## Tech Stack

- **Python 3.9+**
- **scikit-learn** — KMeans, Agglomerative Clustering, PCA, StandardScaler, OneHotEncoder
- **pandas** — data wrangling and feature engineering
- **matplotlib / seaborn** — visualization
- **kneed** — automated elbow point detection

---

## License

MIT License
