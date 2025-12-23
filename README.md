# 👥 Customer Segmentation using PCA & Clustering

Identifying meaningful customer segments from high-dimensional transactional data using PCA, K-Means clustering, Python, and Power BI to support targeted marketing and strategic decision-making.

---

## Table of Contents

- <a href="#overview">Overview</a>
- <a href="#business-problem">Business Problem</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#data-cleaning--preparation">Data Cleaning & Preparation</a>
- <a href="#dimensionality-reduction-pca">Dimensionality Reduction (PCA)</a>
- <a href="#clustering-approach">Clustering Approach</a>
- <a href="#dashboard">Dashboard</a>
- <a href="#how-to-run-this-project">How to Run This Project</a>
- <a href="#key-insights--business-impact">Key Insights & Business Impact</a>
- <a href="#author--contact">Author & Contact</a>

---

<h2><a class="anchor" id="overview"></a>Overview</h2>

This project focuses on customer segmentation using transactional and item-level data to uncover hidden customer behavior patterns.
A complete analytics pipeline was built using Python for data processing, PCA for dimensionality reduction, K-Means for clustering, and Power BI for business visualization.

The goal is to transform complex, high-dimensional purchase data into actionable customer segments for marketing and retention strategies.

---

<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

**Businesses often struggle to understand customer behavior when dealing with large transactional datasets. This project aims to:**
- Identify distinct customer segments based on purchasing behavior
- Reduce noise and redundancy from thousands of item-level features
- Enable targeted marketing instead of one-size-fits-all campaigns
- Support data-driven decisions for customer retention and growth

---

<h2><a class="anchor" id="dataset"></a>Dataset</h2>

**The project uses multiple datasets generated during the pipeline:**
- cleaned_transactions.csv – Cleaned transactional-level data
- item_data.csv – Customer × Item purchase matrix (~2500 features)
- analytical_base_table.csv – Aggregated customer-level metrics
- pca_item_data.csv – PCA-reduced feature set
- customer_segmentation_dashboard.csv – Final dataset for Power BI

Each dataset serves a specific role in the analysis pipeline.

---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- Python (Pandas, NumPy, Scikit-learn)
- PCA (Principal Component Analysis)
- K-Means Clustering
- Matplotlib / Seaborn
- Power BI (Interactive Dashboard)
- Google Colab / Jupyter Notebook
- GitHub

---

<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

```
customer-segmentation/
│
├── README.md
├── .gitignore
├── requirements.txt
│
├── data/
│   ├── cleaned_transactions.csv
│   ├── item_data.csv
│   ├── analytical_base_table.csv
│   ├── pca_item_data.csv
│   └── customer_segmentation_dashboard.csv
│
├── notebooks/
│   └── Customer_Segmentation.ipynb
│
├── dashboard/
│   └── customer_segmentation_dashboard.pbix

```

---

<h2><a class="anchor" id="data-cleaning--preparation"></a>Data Cleaning & Preparation</h2>

- Removed invalid or incomplete transaction records
- Aggregated transaction data at customer level
- Created customer–item purchase matrix
- Standardized features to ensure equal importance
- Prepared analytical base table for business interpretation

---

<h2><a class="anchor" id="dimensionality-reduction-pca"></a>Dimensionality Reduction (PCA)</h2>

**Problem:**
- Item-level data contained ~2500 features, leading to high dimensionality and noise

**Solution:**
- Applied Principal Component Analysis (PCA)
- Reduced features from ~2500 → 300 principal components
- Retained ~80% of total variance

**Important Design Choice:**
- PCA features were used only for clustering
- Business dashboards use interpretable customer metrics instead of PCA components

---

<h2><a class="anchor" id="clustering-approach"></a>Clustering Approach</h2>

- **Algorithm: K-Means Clustering**
- **Input: PCA-transformed features**
- **Objective: Group customers with similar purchasing behavior**

**Why K-Means?**
- Efficient on large datasets
- Suitable for numerical features
- Easy to interpret and deploy
- Each customer is assigned a cluster label, which is later merged with customer-level metrics.

---

<h2><a class="anchor" id="dashboard"></a>Dashboard</h2>

**The Power BI dashboard was built using the final customer-level dataset enriched with cluster labels.**

**Dashboard Highlights:**
- Customer distribution by cluster
- Average spend and purchase frequency per cluster
- High-value vs low-value customer segments
- Interactive filters for cluster-level analysis

📌 PCA components were intentionally excluded from the dashboard to maintain business interpretability.

![Customer Segmentation Dashboard](images/dashboard.png)

---

<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

1. Clone the repository:
```bash
git clone https://github.com/yourusername/customer-segmentation.git
```
2. Install dependencies:
```bash
pip install -r requirements.txt
```
3. Run the notebook:
```bash
- `notebooks/Customer_Segmentation.ipynb`
```

---

<h2><a class="anchor" id="key-insights--business-impact"></a>Key Insights & Business Impact</h2>

- Identified distinct customer segments with varying purchasing behavior
- Highlighted high-value and low-engagement customer groups
- Enabled targeted marketing and personalized campaigns
- Reduced data complexity while preserving meaningful patterns

---

<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

* DEEKSHANT RAHANGDALE *
📧 Email: deekshantrahangdale07@gmail.com
🔗 [LinkedIn](https://www.linkedin.com/in/deekshant-rahangdale-563015256/)  