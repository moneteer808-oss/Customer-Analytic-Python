# Superstore RFM Customer Segmentation (Python)

This project performs customer segmentation using the RFM (Recency, Frequency, Monetary) framework on the Superstore dataset.  
It demonstrates end-to-end analytical workflow including data cleaning, feature engineering, segmentation logic, visualization, and business interpretation.

This repository is part of a structured learning portfolio that progresses from foundational analytics (R), to feasibility studies (predictive modeling), to implementation in Python.

---

## Portfolio Context

### 1. Foundation Project (R)
**Superstore RFM Customer Segmentation (R)**  
Initial implementation in R that introduced the segmentation methodology.  
GitHub:  
https://github.com/moneteer808-oss/Superstore-RFM-Customer-Segmentation

### 2. Feasibility Study
**Superstore Predictive Customer Analytics**  
Exploration using R to determine predictive modeling opportunities and limitations based on the Superstore dataset.  
GitHub:  
https://github.com/moneteer808-oss/Superstore-Predictive-Customer-Analytics

### 3. Tool Comparison
**RFM Customer Segmentation – Python (Basic Version)**  
A simple version comparing R vs Python workflows before developing this improved, polished version.  
GitHub:  
https://github.com/moneteer808-oss/RFM-Customer-Segmentation-Python

This current repository represents the refined, production-ready Python version.

---

## Project Objectives

1. Clean and prepare the Superstore dataset for customer-level analysis.  
2. Calculate RFM metrics for each unique customer.  
3. Assign R, F, and M scores using quantile-based ranking.  
4. Generate composite RFM scores and segment customers.  
5. Visualize customer distributions and segment performance.  
6. Provide actionable business insights for retention and revenue growth.

---

## Data Source

Superstore Dataset (Kaggle)  
Used for educational and non-commercial purposes.  
Source:  
https://www.kaggle.com/datasets/vivek468/superstore-dataset-final/data

---

## Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- LightGBM  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  

---

## Repository Structure

├── data/
│   └── Superstore.csv                # Raw dataset (excluded from repo if too large)
│
├── notebooks/
│   └── RFM_Segmentation.ipynb        # Full analysis notebook
│
├── output/
│   ├── rfm_table.csv                 # Final computed RFM table
│   ├── segment_summary.csv           # Customer segment summary
│   └── visuals/                      # Charts and plots
│
├── README.md                         # Project documentation
└── requirements.txt                  # Python dependencies

---

## Methodology

### 1. Data Cleaning
- Convert date fields to datetime  
- Handle missing values  
- Standardize column names  
- Filter out invalid or negative sales/quantity records  

### 2. RFM Calculation
- **Recency**: Days since last purchase  
- **Frequency**: Number of unique purchase transactions  
- **Monetary**: Total revenue contributed by the customer  

### 3. RFM Scoring
- Apply quantile ranking (1–5) to each RFM dimension  
- Higher score = stronger customer attribute  

Example:  
`R_score + F_score + M_score = RFM_Score (3–15)`

### 4. Segmentation Logic
Segments include:
- Champions  
- Loyal Customers  
- Potential Loyalists  
- At-Risk  
- Hibernating  
- Needs Attention  
- Lost  

### 5. Visualization
- RFM heatmaps  
- Revenue contribution by segment  
- Customer count by segment  
- Scatterplots (Monetary vs Frequency)

### 6. Business Insights
- Identify top-value customers for retention  
- Detect declining customers for reactivation  
- Optimize low-value segments

---

## Key Results (Example)

| Segment              | Customers | Avg_Future_Spend | Churn_Rate |
|----------------------|-----------|------------------|------------|
| Champions            | 105       | $540             | 21%        |
| Loyal Customers      | 65        | $695             | 28%        |
| At Risk              | 99        | $605             | 29%        |
| Potential Loyalists  | 51        | $514             | 24%        |
| Needs Attention      | 96        | $645             | 24%        |

---

## How to Run This Project

# create virtual environment
python3 -m venv venv

# activate
source venv/bin/activate

# install dependencies
pip install -r requirements.txt

# run notebook
jupyter notebook
---

## Future Improvements

- Clustering-based segmentation (KMeans, GMM)  
- Churn prediction using machine learning  
- Build dashboard in Power BI or Looker Studio  
- Add marketing recommendations per segment  

---

## License
This project is for educational purposes only.  
Dataset rights belong to the original Kaggle publisher.