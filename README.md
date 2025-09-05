# CryptoGuard – Compliance Monitoring

[![](https://img.shields.io/badge/Power%20BI-Analytics-green)](https://powerbi.microsoft.com/) 
[![](https://img.shields.io/badge/SQL-Staging%20%26%20Rules-blue)](https://en.wikipedia.org/wiki/SQL) 
[![](https://img.shields.io/badge/Excel-Data%20Prep-yellow)](https://www.microsoft.com/en-us/microsoft-365/excel) 
[![](https://img.shields.io/badge/AML-Risk%20Detection-red)](https://en.wikipedia.org/wiki/Anti-money_laundering) 
[![](https://img.shields.io/badge/Crypto-Compliance-purple)](https://en.wikipedia.org/wiki/Cryptocurrency) 
[![](https://img.shields.io/badge/Project-In%20Progress-lightgrey)]()

A compliance simulation project to replicate **post-onboarding KYC/AML monitoring** in a crypto exchange using synthetic data. The project spans **Excel, SQL, and Power BI**, simulating ongoing screening, transaction monitoring, alert generation, SLA tracking, and EDD triggers.

---

## 🔍 Objective

To simulate the daily compliance activities in a virtual asset service provider (VASP), focusing on:

- Ongoing PEP and sanctions screening after onboarding
- Risk-based monitoring of transactions via SQL rules
- Case management with alert lifecycle and SLA deadlines
- Scheduling CDD reviews and triggering EDD cases

---

## 🗂️ Project Structure

- **Excel Staging Workbook**: Synthetic datasets (KYC, Transactions, Sanctions, Country Risk, Currency Rates, Thresholds) + triage logic (risk scoring, flags, QC).
- **SQL Layer**: 
  - Staging tables: `dim_customer`, `fact_transaction`, `dim_sanctions`, `ref_thresholds`, `ref_country_risk`
  - Rules engine using SQL views for alert scenarios (sanction hit, PEP, high-value, smurfing, structuring, etc.)
  - Materialized `alerts`, `cases`, `cdd_refresh`, and `edd_triggers`
- **Power BI Report**: 4-page interactive dashboard covering alerts, SLA, risk profiles, corridors, and case queues.
- **Documentation**: Monthly summary sample and case snapshots for reporting use.

---

## 🛠️ Tools & Technologies

- **Excel**: Data creation, enrichment, triage columns, and dynamic scoring logic
- **SQL**: Rules engine for AML alerts, staging pipelines, SLA & EDD logic
- **Power BI**: Dashboards for compliance overview, case resolution, and alert monitoring
- **Domain Frameworks**: FATF guidelines, sanctions monitoring, proximity tracing, CDD/EDD best practices

---

## 📊 Live Power BI Dashboard

🚧 *In Progress*  
Will include:

- Executive Summary with KPIs
- Open/closed case tracking
- EDD queue and SLA breaches
- Corridor maps and alert distributions
- Drill-throughs for alert-level transaction history

---

## 🚨 Key Features

- **SQL-Based AML Rule Engine**:
  - `Sanctions Hit`, `Sanctions Proximity`, `PEP High Value`, `Cross-Border`
  - `Structuring`, `Smurfing`, `Velocity Burst`, `High-Risk Corridors`
- **Dynamic Risk Score Calculation** (Excel):
  - Combines PEP/Sanction/Geo risk for triaging customers
- **Case & Alert Management**:
  - SLA-based lifecycle monitoring for each alert
  - Case consolidation for multi-alert customers
- **EDD Triggering Engine**:
  - Auto-identification of customers needing enhanced due diligence

---

## ✅ Outcome

This end-to-end simulation enables:

- Realistic compliance analysis workflow tailored for the crypto sector
- Visibility into evolving customer risk with data-driven refresh schedules
- Proactive AML detection with minimal false positives using dynamic scoring
- Dashboard-driven investigations with full alert/case context and SLA tracking

---

## 📎 Related Links

- [Crypto Risk Tiering Excel (KYC, TXN, Sanctions)](https://github.com/Ratneshhhh/CryptoGuard-Compliance-Monitoring/tree/main/excel)
- [Power BI Dashboard (Coming Soon)](https://github.com/Ratneshhhh/CryptoGuard-Compliance-Monitoring)
- [Monthly Summary & Case Snapshots](https://github.com/Ratneshhhh/CryptoGuard-Compliance-Monitoring/tree/main/docs)

---
