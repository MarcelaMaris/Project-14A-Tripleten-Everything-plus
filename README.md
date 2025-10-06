# 🛒 Everything Plus – Customer Segmentation & Churn Analysis

This project uses transactional data from Everything Plus to identify behavioral patterns, segment customers, and predict churn risk — enabling data-driven retention strategies and targeted marketing actions.
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
- Most customers have **low purchase frequency** (median = 2) and **moderate average ticket**, indicating a predominantly occasional buyer base.
- **Volume leaders ≠ Revenue leaders**: the top-selling items by units were not always the ones generating the most revenue, highlighting cross-selling and pricing opportunities.
- Customer segmentation (K=3) revealed three clear profiles:
  - 🟦 **Standard group** (majority): low frequency, moderate ticket — stable but not high-value.
  - 🟥 **High-ticket group**: very small, few orders but extremely high AOV — potentially corporate buyers or outliers.
  - 🟩 **High-frequency group**: loyal and frequent buyers with lower AOV — ideal for loyalty or upselling campaigns.
- Predictive churn models achieved **exceptionally high performance (F1 ≈ 1.00)**. While this shows strong patterns in the data, it also raises concerns about **potential overfitting or data leakage**, especially around churn definition.
- **Behavior alone wasn’t strongly correlated with churn** in hypothesis tests, but machine learning captured complex combinations of features that were predictive.

---

## 📝 Recommendations
- **Targeted retention campaigns per segment**  
  - 🟩 High-frequency: loyalty perks, subscription offers, early access.  
  - 🟦 Standard: cross-selling and personalized recommendations.  
  - 🟥 High-ticket: dedicated account management and premium services.
  
- **Early churn warning system**  
  Monitor “days since last purchase” continuously and trigger proactive re-engagement actions for at-risk customers.

- **Refine churn definition and validation**  
  Use rolling windows or survival analysis to define inactivity more robustly, and adopt **time-based validation** to avoid data leakage.

- **Feature engineering**  
  Enrich the model with seasonality, product mix, acquisition channel, or region to improve accuracy and generalization.

- **Model monitoring and retraining**  
  Reassess churn models periodically as customer behavior and business strategy evolve.

- **Experimentation layer**  
  Test retention actions on at-risk segments and measure uplift, closing the loop between prediction and marketing effectiveness.


---
## 💡 Key Business Impact
- Identified distinct customer segments for **personalized marketing**.  
- Built a churn prediction model to **prioritize retention efforts**.  
- Highlighted strategic opportunities in product mix and pricing.  
- Delivered insights through a **Tableau dashboard** for easy business adoption.


---

## 🛠️ Tech Stack
- **Data Analysis**: Python, Pandas, NumPy, Matplotlib, Seaborn  
- **Statistical Testing**: Statsmodels, SciPy  
- **Machine Learning**: scikit-learn (K-Means, Logistic Regression, Random Forest)  
- **Visualization**: Tableau, Jupyter Notebook

