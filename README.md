# Telecom Customer Retention & Churn Dynamics Analysis

Customer attrition directly impacts recurring revenue and long-term customer lifetime value (LTV). This project conducts an **exploratory data analysis (EDA)** on customer demographics, contract terms, billing tiers, and service adoption patterns across telecom subscribers to answer five strategic questions:

1. **Why are customers leaving?**
2. **What primary factors drive churn?**
3. **At what stage in the customer lifecycle is churn risk highest?**
4. **How can the business expand revenue without increasing churn risk?**
5. **What actionable interventions should the business implement next?**

### Analytical Workflow

To systematically answer these questions, the analysis follows a 4-stage progression:

1. **Data Audit & Cleaning** - Audit data integrity and handle anomalies.
2. **Univariate Analysis** - Establish baseline benchmarks across customer demographics, billing distributions, and overall churn rates.
3. **Bivariate Analysis** - Evaluate individual variables against churn status to isolate primary risk factors and direct churn drivers.
4. **Multivariate Analysis** - Examine interactions between multiple variables to understand compounded churn risk.

### Dataset Overview

* **Source:** Maven Analytics
* **Title:** Telecom Customer Churn Dataset
* **Size:** ~7,000 customer records across 38 features

### Tech Stack & Tools

* **Language:** Python
* **Data Manipulation:** `pandas`, `numpy`
* **Visualization:** `matplotlib`, `seaborn`
