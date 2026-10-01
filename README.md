# Python-Telecom-Customer-Churn-Analysis

Exploratory data analysis (EDA) of a 504,000-customer telecom dataset in Python, focused on **who churns and why**, using pandas, Matplotlib and Seaborn in a Jupyter Notebook.

## Dataset
`telecom_customer_churn_big.csv.gz`: 504,000 rows × 14 columns.

| Column | Description |
|---|---|
| customer_id, gender, age, city | Customer profile |
| signup_date, tenure_months | Account history |
| contract_type, internet_service, payment_method, paperless_billing | Plan and billing |
| support_calls | Number of support calls |
| monthly_charges, total_charges | Billing amounts |
| churn | Target (Yes / No) |

**Data quality notes:** missing values in `age` (~15k), `city` (~10k), `monthly_charges` (~7.5k) and `total_charges` (~10k), plus ~4,000 duplicate `customer_id` rows, handled during cleaning.

## What the analysis covers
- Data cleaning (missing values, duplicates, date parsing)
- Feature engineering: `churn_flag`, `tenure_group`, `age_group`
- Churn rate by contract, internet service, payment method, tenure, age and city
- Box plots of monthly charges and support calls by churn
- Correlation heatmap and a contract × internet service churn heatmap

## Key findings
- Overall churn is **34.3%**.
- **Month-to-month** contracts churn at ~49%, versus ~19.6% (one year) and ~11.8% (two year).
- **Fiber** customers churn most (~45%), versus DSL ~28% and no internet ~19%.
- Churned customers pay more (avg ~₹888 vs ~₹773 monthly), make more support calls (2.2 vs 1.4) and have shorter tenure (~30 vs ~40 months).
- Payment method and paperless billing show almost no effect on churn.
- Highest-risk segment: **month-to-month + Fiber (~63% churn)**.

## Tools
Python · pandas · NumPy · Matplotlib · Seaborn · Jupyter

## Author
**Ginish Kumar** (GinishTech) · [GitHub](https://github.com/GinishTech) · [LinkedIn](https://linkedin.com/in/ginish-kumar-544b2a1b4)
