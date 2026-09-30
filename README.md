# 🏦 Bank Customer & Loan Analytics

An end-to-end data analytics project that explores customer behavior, account activity, transactions, and loan performance for a retail bank — from raw MySQL data to Python-based EDA to an interactive Power BI dashboard.

![Executive Overview](https://github.com/sahibsingh25012005-ui/banking-customer-financial-analysis-sql-python-powerbi/blob/main/Images/Executive_overview.png)

---

## 📌 Project Overview

This project analyzes a synthetic banking dataset (~50,000 customers) covering customers, accounts, transactions, loans, and branches. The goal is to uncover actionable insights around customer demographics, account health, transaction behavior, and loan portfolio performance — and present them through a multi-page Power BI dashboard.

**Workflow:**

```
MySQL Database  →  Python (pandas, SQLAlchemy)  →  Data Cleaning & EDA  →  Power BI Dashboard
```

---

## 🗂️ Dataset

Data was sourced from a MySQL database (`bank`) with five core tables:

| Table          | Description                                                        |
|----------------|---------------------------------------------------------------------|
| `customers`    | Demographics — age, gender, city, state, occupation, income, etc.  |
| `accounts`     | Account type, balance, open date, status, branch link              |
| `branches`     | Branch name, city, state, and branch type (Urban/Semi-Urban/Rural) |
| `transactions` | Transaction type, amount, channel, category, merchant category     |
| `loans`        | Loan type, amount, interest rate, term, EMI, status, outstanding   |

**Scale:** ~50K customers · ~50K accounts · ~300K transactions · ~18K loans · 120 branches

---

## 🛠️ Tools & Technologies

- **Python** — `pandas`, `numpy`, `matplotlib`, `seaborn`, `SQLAlchemy`
- **MySQL** — source database for raw and cleaned tables
- **Power BI** — interactive dashboard and visual reporting
- **Jupyter Notebook** — data extraction, cleaning, and exploratory analysis

---

## 🔍 Analysis Workflow

1. **Data Extraction** — Connected to the MySQL `bank` database via SQLAlchemy and loaded all five tables into pandas DataFrames.
2. **Data Exploration** — Profiled each table (`.head()`, `.describe()`, null/duplicate checks) to understand structure and distributions.
3. **Exploratory Data Analysis (EDA)** — Analyzed customer demographics, account balances by type/status, transaction patterns by channel and category, and loan performance by type and status.
4. **Aggregation** — Built summary tables (e.g., loan totals, average interest rates, outstanding amounts by loan type) using `groupby` and `agg`.
5. **Data Export** — Wrote cleaned/aggregated tables back to MySQL (as `*_analysis` tables) and exported them to CSV for use in Power BI.
6. **Dashboarding** — Built a 3-page interactive Power BI report for business-facing insights.

---

## 📊 Power BI Dashboard

The dashboard consists of three pages:

### 1. Executive Overview
High-level KPIs and trends for leadership — total customers, total balance, total/outstanding loan amounts, monthly transaction trends, gender distribution, age-group breakdown, and account balance by branch type/account type. Includes slicers for account type and city.

![Executive Overview](https://github.com/sahibsingh25012005-ui/banking-customer-financial-analysis-sql-python-powerbi/blob/main/Images/Executive_overview.png)

### 2. Customer & Account Analysis
Deep dive into the customer base and account portfolio — average age, balance, income, active/inactive accounts, customer acquisition trend over time, account balance by type, account status distribution, and top branch cities by balance.

![Customer & Account Analysis](https://github.com/sahibsingh25012005-ui/banking-customer-financial-analysis-sql-python-powerbi/blob/main/Images/Customer_and_account_analysis.png)

### 3. Transaction & Loan Analysis
Focus on transactional and lending activity — total transactions and value, loan amount/interest by loan type, transactions by channel, debit vs. credit split, loan status breakdown, a geo map of loan distribution by city, and a detailed customer-level loan table. Includes a year slicer and account-type filter.

![Transaction & Loan Analysis](https://github.com/sahibsingh25012005-ui/banking-customer-financial-analysis-sql-python-powerbi/blob/main/Images/Transaction_and_loan_analysis.png)

---

## 💡 Key Insights

- Average customer is **38 years old** with an average account balance of **₹74.4K** and average annual income of **₹48.9K**.
- **Savings accounts** hold the largest share of total balance (₹2.3bn), followed by Current (₹0.8bn) and Salary (₹0.6bn) accounts.
- **91%** of accounts are Active, with a small share Dormant or Closed.
- Total loan book stands at **₹11.87bn**, with **₹4.34bn** currently outstanding.
- **Personal loans** are the most common loan type by volume (6,288 loans), while **Home loans** carry the highest total outstanding amount.
- The gender split among account holders is nearly even (Male 47%, Female 51%, Other 2%).
- **Mobile Banking** and **UPI** are the leading transaction channels, reflecting a strong digital-first customer base.
- **58%** of loans are Active, with a modest **8.5%** rate of default.

---

## 📁 Repository Structure

```
├── main.ipynb                          # Data extraction, cleaning & EDA notebook
├── bank_customers_loan_analysis.pbix   # Power BI dashboard file
├── Executive_overview.png              # Dashboard screenshot – Page 1
├── Customer_and_account_analysis.png   # Dashboard screenshot – Page 2
├── Transaction_and_loan_analysis.png   # Dashboard screenshot – Page 3
└── README.md
```

---

## 🚀 How to Use

1. Clone this repository.
2. Open `main.ipynb` in Jupyter Notebook to review the data extraction and EDA process (requires a MySQL connection to reproduce end-to-end, or use the exported CSVs directly).
3. Open `bank_customers_loan_analysis.pbix` in **Power BI Desktop** to explore the interactive dashboard.

---

## 👤 Author

Sahib Singh

Aspiring Data Analyst | Python | SQL | Power BI 

Email: (sahibsingh25012005@gmail.com)

LinkedIn: (https://www.linkedin.com/in/sahib-singh-5587ba364/)

GitHub: (https://github.com/sahibsingh25012005-ui)

*Note: This project uses synthetically generated banking data for demonstration purposes only — it does not represent any real financial institution or customer data.*
