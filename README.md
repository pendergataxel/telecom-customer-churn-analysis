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

---

# Executive Summary & Strategic Takeaways

## 1. Executive Summary
Customers leaving happens early on because of a rocky onboarding experience, flexible month-to-month plans, bare fiber internet without tech support, and confusing online billing. While about 1 in 4 customers leave overall, most drop out within their first 6 months, especially those without long-term commitments or security add-ons. The best ways to stop this and keep customers around longer are moving people to term contracts, bundling security and support into internet packages, and making payments simple.

---

## 2. Core Synthesis Findings

### Univariate Synthesis: Customer Profile & Strategic Vulnerabilities
- **The Predominant Customer Archetype:** The baseline subscriber is digitally reliant yet uncommitted. Customers subscribe heavily to core connectivity services (90.3% phone, 78.3% internet), but predominantly transacting on flexible month-to-month terms (51.3%) without structured promotional incentives (54.9%).
- **High Risk of Losing Customers:** About 1 in 4 customers leave, and more than half are on month-to-month plans with nothing stopping them from canceling. Most cancellations happen early on, mainly because rivals tempt customers away with better devices and cheaper deals.
- **Bad Service is a Self-Inflicted Problem:** Competitors are the main external threat, but rude staff and poor service cause about a third of all cancellations. This is an internal issue the company can directly fix with better support training.
- **Untapped Upsell Potential:** Most customers are new and haven't spent much yet (under $2,000), but loyal, multi-service users bring in over $11,000. Less than 45% of users buy extra add-ons like security or tech support, so selling these add-ons is an easy way to grow revenue and make it harder for customers to leave.

### Bivariate Synthesis: Churn Drivers & Behavioral Vulnerabilities
- **The Fragile High-Risk Profile:** Attrition concentrates heavily among unanchored, solo subscribers, older demographics, and specific regions. Seniors (65+) and single households churn at the highest rates, while regional hot spots like San Diego see losses nearly 3× the average. Conversely, family ties (marriage and dependents) and number of referrals (2+ referrals) serve as the strongest organic anchors against churn.
- **The Acute Onboarding Cliff:** Customer churn is predominantly an onboarding failure, not a late-stage fatigue. More than half of all exits happen within the first 6 months (53%), with a severe exit spike in Month 1 and a median churn tenure of just 10 months. Acquisition campaigns targeting quick sign-ups (such as Offer E) suffer catastrophic early drop-offs (53% churn) before accounts ever reach lifecycle stability (2+ years).
- **The Premium Service Disconnect:** Customers are not leaving because of heavy network usage, data caps, or billing penalties; they leave because of expensive base pricing without perceived support value. Fiber Optic customers churn at an alarming 40.8%, and churn density spikes sharply between $70 and $100+/month. When expensive internet plans lack value-add services like Online Security or Tech Support, churn doubles to ~40%.
- **Structural Commitment Dictates Retention:** Contract terms and payment friction directly control account longevity. Month-to-month subscribers leave at 45.8%, whereas multi-year commitments eliminate churn (dropping to 2.6% on two-year agreements). Furthermore, friction-heavy payment methods like bank withdrawals and checks experience more than double the churn of credit card autopay (34%–37% vs. 14.4%), compounding early cancellations.
- **Catastrophic Lifetime Value Erosion:** Because attrition occurs so rapidly, churned accounts fail to amortize acquisition costs, exiting with a median total revenue of just $913.40 compared to $2,968.90 for retained accounts. Retaining customers past the initial 6-month threshold and securing long-term contracts unlocks over 3× the cumulative revenue per subscriber.

### Multivariate Synthesis: Churn Drivers & Behavioral Vulnerabilities
- **Contracts Shield Against Price Sensitivity:** Month-to-month users cancel rapidly as bills increase, but contracts keep churn very low below $90. Once bills cross $90, even committed customers start leaving, doubling 1-year churn to ~20%.
- **Fiber Without Add-ons Is a Churn Trap:** Bare fiber optic plans see the worst cancellations, peaking above 50%. Adding either Tech Support or Online Security cuts churn in half, while pairing both drives it down to ~14%. Each extra add-on steadily drops churn from over 60% down to under 10%, yet most fiber users remain dangerously stuck at 0 to 2 add-ons.
- **Digital Billing Sparks Unexpected Exits:** Paperless billing hurts retention across all age groups. The highest churn hits seniors on bank withdrawal (~49%) and anyone pairing paperless billing with mailed checks (~50%), pointing to clear payment friction.
- **Credit Cards Provide the Strongest Floor:** Auto-paying via credit card with paper bills yields the best retention across every demographic, keeping churn as low as 6% to 10% for non-seniors and under 29% for seniors.

---

## 3. Strategic Recommendations & Action Plan

1. **Fix Internal Service Quality:** Competitors take blame, but 1 in 3 exits are driven by poor staff attitude and service issues. Retrain frontline support teams to eliminate self-inflicted losses.
2. **Bundle Fiber with Security & Support:** Stop selling bare fiber optic internet by itself. Include Online Security and Tech Support directly in standard fiber packages to drop cancellations from around 50% down toward 14%.
3. **Tackle the Month 1–6 Tenure Cliff:** Set up direct support for new users during their first 6 months to fix the 53% early drop-off. Push referral perks early on, since getting customers to 2+ referrals creates a solid barrier against leaving.
4. **Target Month-to-Month Users Near $70–$90:** Spot month-to-month customers before their bills cross the $70–$90 range and offer discounts or perks to switch to 1- or 2-year contracts before higher prices push them out.
5. **Streamline Payment Channels & Billing:** Discourage paperless billing, troubleshoot failed payment paths for mailed check users, and push automatic credit card billing.

---

## 4. Potential Improvements for the Future
- **Predictive Churn Modeling:** Train classification models (Logistic Regression, Random Forest, XGBoost) using the high-impact drivers identified in this EDA (contract type, onboarding tenure, fiber add-on depth).
- **Customer Lifetime Value (CLV) Segmentation:** Build an RFM-style (Recency, Frequency, Monetary) segmentation model to prioritize retention campaigns based on cumulative account value rather than just churn risk.
- **A/B Testing Retention Strategies:** Design controlled experiments to test whether auto-bundling Online Security into entry Fiber plans moves the needle on early churn.
- **Billing Friction Deep Dive:** Analyze user interaction and billing logs to uncover the root technical cause behind the high churn spike seen in paperless accounts.