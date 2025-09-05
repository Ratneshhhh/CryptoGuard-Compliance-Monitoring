# 🛡️ CryptoGuard – Compliance Monitoring System

**Simulating Post-Onboarding Compliance for Virtual Asset Providers**

[![Power BI](https://img.shields.io/badge/-Power%20BI-black?style=for-the-badge&logo=powerbi&logoColor=yellow)](https://powerbi.microsoft.com/)
[![SQL](https://img.shields.io/badge/-SQL-blue?style=for-the-badge&logo=postgresql&logoColor=white)](https://en.wikipedia.org/wiki/SQL)
[![Excel](https://img.shields.io/badge/-Excel-107C41?style=for-the-badge&logo=microsoft-excel&logoColor=white)](https://www.microsoft.com/en/microsoft-365/excel)

---

### 📌 Project Overview

CryptoGuard simulates a **real-world post-onboarding compliance system** for a crypto exchange, covering:

- Sanctions & PEP screening
- Rule-based AML alert generation
- EDD case creation & SLA monitoring
- Dynamic risk scoring
- CDD refresh scheduling
- Regulator-friendly reporting

---

### 🧩 Tech Stack

| Tool       | Usage                                                                 |
|------------|------------------------------------------------------------------------|
| **Excel**  | Reference tables (Country Risk, Thresholds), staging data, triage     |
| **SQL**    | Rules engine, materialized alerts, case creation, CDD/EDD views       |
| **Power BI** | Dashboard with KPIs, alert tables, SLA metrics, and EDD queues       |

Star schema was used for data modeling (fact and dimension separation).

---

### 🗂️ Dataset Structure (Synthetic Data)

#### 📁 Excel Staging Tables
- **KYC.csv** – Customer_ID, Risk Score, PEP/Sanction Flags, Onboarding Date
- **Transactions.csv** – Txn_ID, Sender/Receiver, Wallets, Amount, Timestamp
- **Sanctions.csv** – Sanctioned Wallet Addresses
- **Reference Tables** – Country Risk, Currency Rates, Thresholds

#### 🛠️ Key Triage Logic
- High-Value, Cross-Border, PEP/Adverse party detection
- Risk bucket scoring (Low / Medium / High)
- Derived fields for alert rules

---

### 📌 AML Rule Logic in SQL

- **Sanctions_Hit**: Direct match
- **PEP_HV_CrossBorder**: PEP involved + high-value or cross-border
- **Structuring/Smurfing**: Multiple similar or funnel transactions
- **Velocity_Burst**: Rapid fire patterns
- **High-Risk Corridor**: Country pair flow ≥ threshold
- **SLA Calculation**: Severity-based deadline assignment

---

### 📊 Power BI Dashboard

- 📌 **Executive Summary**: Totals, open alerts, SLA breaches, flagged %
- 🔍 **Analyst Workbench**: Drill-through to alert + transaction context
- 🌍 **Corridors & Geo Flow**: Heatmaps & matrices for high-risk paths
- 🧾 **EDD & Case Tracking**: Overdue queue, decisions, top case reasons

---

### 📝 Deliverables

- `Excel/` – Cleaned staging data + triage logic
- `SQL/` – All rule views, alerts, cases, risk scoring
- `PowerBI/` – Dashboard pages (screenshots or .pbix)
- `Reports/` – Sample monthly summary PDF, case snapshots

---

### 📅 Next Steps (In Progress)
- ✅ Excel triage
- ⏳ SQL scripting
- ⏳ Power BI dashboard build
- ⏳ Documentation upload

---

### 📌 Author

📇 **Ratnesh Yadav**  
🔗 [ratneshyadav.net](https://ratneshyadav.net) | [LinkedIn](https://www.linkedin.com/in/ratneshhhh)

---

> ⚠️ Note: This project uses **entirely synthetic data** for simulation purposes and is not tied to any real customer or organization.
