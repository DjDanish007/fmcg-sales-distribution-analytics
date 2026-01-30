# BRD (Lite) – FMCG Sales & Distribution Analytics Dashboard

## 1. Document Control
| Item | Details |
|------|---------|
| Document Title | BRD (Lite) – FMCG Sales & Distribution Analytics Dashboard |
| Version | 1.0 |
| Prepared By | Solution Analyst (Portfolio Project) |
| Date | 2025-01-XX |
| Status | Draft |

---

## 2. Purpose
The purpose of this document is to define the business requirements for an **ERP-inspired FMCG Sales & Distribution Analytics Dashboard**. The dashboard provides consolidated visibility into sales performance, distributor activity, targets, and product insights to support management decision-making.

This BRD is a simplified version (Lite) designed to demonstrate enterprise-level requirement thinking.

---

## 3. Business Context
In large FMCG organizations, sales and distribution operations generate large volumes of data across:
- ERP systems (SAP / Oracle / ERPNext)
- Distributor order management systems
- Manual reporting spreadsheets

Due to fragmented reporting, leadership often experiences:
- delays in performance visibility
- inconsistent KPI calculations
- limited insight into distributor productivity and regional gaps

A unified dashboard is required to improve visibility and decision speed.

---

## 4. Objectives
### 4.1 Business Objectives
- Provide **single view of truth** for sales & distribution performance
- Enable quick identification of:
  - regional underperformance
  - distributor inactivity
  - target achievement gaps
  - top / bottom SKUs
- Standardize KPI definitions for sales review meetings

### 4.2 Project Objectives
- Build a lightweight dashboard using ERP-style datasets
- Provide supporting documentation:
  - business problem
  - KPI definition
  - business insights and scenarios

---

## 5. Stakeholders
| Stakeholder | Role |
|------------|------|
| Sales Manager | Reviews sales performance and target achievement |
| Distribution Head | Tracks distributor activity and coverage gaps |
| Finance Controller | Uses sales visibility for financial tracking (future) |
| Area Sales Officer (ASO) | Monitors territory-wise distributor performance |
| Solution Analyst | KPI design, reporting logic, governance |

---

## 6. Scope

### 6.1 In Scope
- Dashboard UI with KPI cards, charts, and tables
- ERP-inspired datasets:
  - Distributor master
  - Product (SKU) master
  - Sales order transactions
  - Monthly targets
- KPI calculations and reporting logic
- Business insights documentation

### 6.2 Out of Scope (Current Version)
- Real-time ERP integration
- ETL pipeline / data warehouse automation
- User authentication / role-based access control
- Inventory module and receivables module (planned enhancements)
- Mobile application version

---

## 7. Functional Requirements (FR)

### FR-01: KPI Summary Cards
**Description:** Dashboard shall display KPI cards for key performance measures.  
**KPIs:** Total Sales Value, Total Orders, Sales vs Target (%), Active Distributors  
**Priority:** High

---

### FR-02: Sales Trend Visualization
**Description:** Dashboard shall display sales trend by date (daily).  
**Chart Type:** Line chart  
**Priority:** High

---

### FR-03: Region-wise Sales Performance
**Description:** Dashboard shall display sales by region for comparison.  
**Chart Type:** Bar chart / table  
**Priority:** High

---

### FR-04: Distributor Performance Table
**Description:** Dashboard shall list distributors with sales contribution and status.  
**Fields:** Distributor Name, Region, Status, Sales Value  
**Priority:** High

---

### FR-05: SKU Performance Insights
**Description:** Dashboard shall show top and bottom SKUs by sales value.  
**Priority:** Medium

---

### FR-06: Filters (Optional / Enhancement)
**Description:** Dashboard may provide filters to analyze by region, distributor, SKU.  
**Priority:** Medium (Future Enhancement)

---

## 8. Non-Functional Requirements (NFR)

### NFR-01: Usability
Dashboard must be easy to understand for non-technical stakeholders with clean layout and clear KPIs.

### NFR-02: Performance
Dashboard should load within 3–5 seconds on a standard laptop using demo datasets.

### NFR-03: Maintainability
KPI logic should be modular and documented for easy enhancement.

### NFR-04: Data Privacy
All data used must be simulated and should not include real company information.

---

## 9. Data Requirements

### 9.1 Data Sources (Demo)
| File | Type | Description |
|------|------|-------------|
| distributors.csv | Master | Distributor list, status, region |
| products.csv | Master | SKU list, category, pack size, unit price |
| sales_orders.csv | Transaction | Daily sales orders with net value |
| targets.csv | Planning | Monthly targets by region |

### 9.2 Key Data Fields
- DistributorID, DistributorName, Region, Status
- ProductID, ProductName, Category
- OrderID, OrderDate, Quantity, NetValue

---

## 10. Reporting Requirements
The dashboard must support:
- Daily sales monitoring
- Region-wise comparison
- Distributor productivity tracking
- Sales vs target measurement
- SKU performance analysis

---

## 11. Assumptions & Dependencies
### Assumptions
- All transactions are valid and represent completed sales
- Targets are provided monthly by region
- Region mapping remains consistent across datasets

### Dependencies
- Correct dataset formatting
- Chart rendering library (e.g., Chart.js)

---

## 12. Risks & Mitigation
| Risk | Impact | Mitigation |
|------|--------|------------|
| Inconsistent master data | Wrong reporting | Data validation rules / checks |
| KPI misinterpretation | Wrong decisions | KPI definition document + governance |
| Over-simplified demo data | Reduced realism | Expand dataset gradually |

---

## 13. Acceptance Criteria
The solution will be accepted when:
- Dashboard displays all core KPIs accurately
- KPI definitions are documented and aligned with output
- Business insights are generated from the data
- Repo includes professional documentation and screenshots

---

## 14. Future Enhancements
- Add inventory coverage and dispatch performance
- Add outstanding receivables and credit control
- Add territory-level view (ASO / route plan)
- Implement SQL backend + API layer
- Publish Power BI version for enterprise reporting
