# Tax Reconciliation & Lodgement Performance Dashboard

**Power BI · Power Query · DAX · Data Modelling**

A Power BI dashboard built for a professional accounting environment to reconcile tax lodgement data between two systems — the Australian Taxation Office (ATO) and an internal practice management platform (XPM) — and to monitor lodgement compliance and outstanding debt.

> **Note:** All data in this project has been anonymized for confidentiality. Client names and values have been modified, while the underlying analytical structure has been preserved.

---

## Context

Accounting firms managing large client portfolios need to reconcile what's recorded internally against what's lodged with the ATO. Mismatches between systems can hide missed lodgements, untracked debt, or data entry errors — all of which carry compliance risk.

This project was built to:
- Identify inconsistencies between internal records (XPM) and ATO data
- Monitor lodgement compliance and performance over time
- Surface outstanding obligations and concentrated risk among clients
- Give the practice a single, interactive view to support decision-making

## What I did

- Cleaned and standardized multi-source data from ATO and XPM
- Built reconciliation logic to identify clients present in one system but missing from the other
- Designed KPIs for lodgement performance and outstanding debt
- Modeled relationships and built DAX measures to support dynamic, cross-filtered analysis
- Developed two interactive dashboard pages with slicers and navigation buttons, allowing users to drill into client-level detail and explore trends by period, region, and tax type

## Dashboard

### 1. Company Overview
High-level view of client distribution, lodgement status, and outstanding debt across the practice.

![Company Overview](screenshots/company_overview.png)

**Highlights:**
- 1.6K total clients across 5 entity types (individuals/sole traders, companies, trusts, SMSFs, other)
- 1.14K tax returns on the lodgement list, with 371 outstanding 2025 lodgements
- $4.54M in total ATO debt, concentrated heavily in Queensland-based clients
- Debt is concentrated among a small number of clients, visible in the Top 5 Debtors view

### 2. Lodgement Issues and Exceptions
Reconciliation view identifying discrepancies between systems and tracking lodgement performance over time.

![Lodgement Issues and Exceptions](screenshots/lodgement_issues.png)

**Highlights:**
- 112 unmatched clients identified between ATO and XPM (36 ATO-only, 76 XPM-only)
- Monthly on-time vs. late lodgement performance, segmented by tax type (ITR, CTR, TRT, SMSF, FBT, PTR, AS, CURNN)
- Average lodgement timing of -5.20 days (early/late), with a slicer to explore performance by tax type
- Late lodgements peak around mid-year reporting periods

## Key Insights

- Individual traders/sole traders represent the largest client segment by far
- Significant reconciliation gaps exist between ATO and internal system records — 112 clients didn't match cleanly between the two
- Lodgement delays are not evenly distributed; they spike in specific reporting months
- Outstanding debt is concentrated among a handful of clients rather than spread evenly across the portfolio

## Tools & Techniques

| Area | Tools |
|---|---|
| Data cleaning & transformation | Power Query |
| Data modelling | Power BI (star schema, relationships) |
| Calculations & KPIs | DAX |
| Visualization & interactivity | Power BI (slicers, bookmarks, navigation buttons) |

## Repository Structure

```
├── Tax_Reconciliation_Dashboard.pbix   # Power BI source file
├── Company_Overview.pdf                # One-page project summary
├── screenshots/
│   ├── company_overview.png
│   └── lodgement_issues.png
└── README.md
```

---

**Cesar Pazo** — Data Analyst, Melbourne, Australia
📧 cesaralberto.pazo@gmail.com
