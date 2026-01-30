# Business Problem – FMCG Sales & Distribution Analytics Dashboard

## 1. Background / Context
In large FMCG organizations, Sales & Distribution operations involve multiple stakeholders (Sales Team, Distribution, Finance, and Management) and multiple systems (ERP, distributor portals, manual spreadsheets). Due to fragmented reporting, decision-makers often face delays in understanding real-time performance.

This project simulates an **ERP-inspired analytical dashboard** that provides a consolidated view of key Sales & Distribution KPIs using structured master and transactional datasets.

---

## 2. Problem Statement
The organization lacks a single, reliable view to monitor:

- Daily / weekly sales performance
- Sales vs target achievement
- Distributor productivity and inactivity
- Region-wise sales contribution
- SKU-level performance and concentration risks

As a result, leadership decisions become reactive instead of proactive.

---

## 3. Business Objectives
The primary objectives of this solution are:

1. Provide management with a **single analytical view** of Sales & Distribution performance.
2. Enable faster decision-making using **standardized KPIs**.
3. Highlight distributor and regional performance gaps.
4. Improve sales governance by identifying risks (inactive distributors, SKU dependency).
5. Establish a scalable foundation for future integration with ERP / BI systems.

---

## 4. Stakeholders
| Stakeholder | Interest / Use |
|------------|-----------------|
| Sales Manager | Sales trends, achievement vs target, top regions |
| Distribution Head | Distributor activity, coverage gaps |
| Finance Controller | Sales value visibility, potential receivables tracking (future) |
| Area Sales Officer (ASO) | Territory-wise sales monitoring |
| Business Analyst / Solution Analyst | KPI design, reporting logic, data model governance |

---

## 5. Scope

### 5.1 In Scope
- ERP-style dataset structure (master + transactional data)
- Dashboard KPIs and charts:
  - Sales value and trend
  - Sales vs Target
  - Distributor performance
  - Region contribution
  - SKU insights
- Business insight documentation for decision-making

### 5.2 Out of Scope (Current Version)
- Real ERP integration (SAP/Oracle/ERPNext)
- Real-time refresh / ETL pipelines
- Role-based authentication
- Inventory and receivables detailed modules (future enhancement)

---

## 6. Assumptions
- Data is simulated and structured like ERP exports (CSV format).
- Each Sales Order record represents a completed sale transaction.
- Target values are defined monthly by region.
- Region mapping is consistent across distributors and transactions.

---

## 7. Success Criteria
The solution will be considered successful if it:

- Displays key KPIs clearly in a management-friendly layout
- Supports region and distributor performance analysis
- Enables identification of underperformance and key risks within minutes
- Can be extended easily for future ERP/BI integration

---

## 8. Expected Business Value
- Faster sales review meetings (daily/weekly/monthly)
- Early detection of distributor inactivity and regional gaps
- Better target governance and accountability
- Strong foundation for future BI maturity (Power BI / Superset / SQL warehouse)
