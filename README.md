# 🛒 Everything Plus – Customer Segmentation & Churn Analysis

This project analyzes transaction data from **Everything Plus**, an online store for household items.  
Using **Jupyter notebooks** and a **Tableau dashboard**, it explores purchasing behavior, builds **K-Means** customer segments, tests hypotheses, and trains a **predictive churn model**.

🔗 **Live dashboard:** https://public.tableau.com/app/profile/marcela.stephanie.pereira.maris1628/viz/DashboarddeAnlisedeClientes/Dashboard1  
💻 **Repository:** https://github.com/MarcelaMaris/Project-14A-Tripleten-Everything-Plus

---

## 🎯 Objectives
- Clean and prepare transaction data; build customer-level features.  
- Perform **EDA** on order frequency, average ticket, products and revenue.  
- Segment customers with **K-Means** and interpret cluster profiles.  
- Test hypotheses relating behavior to **inactivity (churn)**.  
- Train predictive models (Logistic Regression, Random Forest) to flag churn risk.  
- Share results via an **interactive Tableau dashboard**.

---

## 🧭 Dashboard Features
- **📈 Cluster overview**  
  Bar chart with the number of customers per cluster.

- **🫧 Frequency × Ticket bubble chart**  
  Each point is a customer; bubble size reflects **total spend**.  
  **Slider** for “days since last purchase” highlights potential churn risk.

- **📦 Spend distribution**  
  Histogram of total customer spend (binned), showing concentration at lower values.

- **🔍 Interactivity**  
  Filter by cluster and explore outliers (very high ticket / very high frequency).

---

## 📌 Conclusions
- Most customers have **low frequency** (median = 2 orders) and **moderate average ticket**.  
- **Top-selling items** by volume are not always the **top-revenue** items.  
- **Three segments** (k=3) emerged:  
  - A large “standard” group (low frequency, moderate ticket).  
  - A very small **high-ticket** group (few orders, very high average order value).  
  - A **high-frequency** group (many orders, lower per-order value).  
- Churn models reached **very high metrics** (near 1.00). This may indicate **overfitting or data leakage** and is flagged as a limitation for future work.

---

## 📝 Recommendations
- **Retention campaigns** targeted by segment (e.g., perks for high-frequency, cross-sell for standard group).  
- **Early-warning monitoring** of customers with many days since last purchase.  
- Revisit the **churn definition** (>90 days) and apply **time-based validation** to avoid leakage.  
- Add features (seasonality, product mix, channel) and try **cross-validation / hyperparameter tuning**.

---

## 🛠️ Technologies Used
- **Python**, **Pandas**, **NumPy**, **Matplotlib**, **Seaborn**  
- **scikit-learn**, **Statsmodels**, **SciPy**  
- **Jupyter Notebook** for analysis  
- **Tableau** for the interactive dashboard
