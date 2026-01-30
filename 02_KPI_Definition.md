# KPI Definition – FMCG Sales & Distribution Analytics Dashboard

## 1. Purpose
This document defines the key KPIs used in the FMCG Sales & Distribution Analytics Dashboard. These KPIs represent typical performance measures used in enterprise FMCG organizations for sales reviews and distribution monitoring.

---

## 2. KPI List (High Level)
| KPI Category | KPI Name |
|-------------|----------|
| Sales | Total Sales Value |
| Sales | Total Orders |
| Sales | Average Order Value |
| Target | Sales vs Target (%) |
| Distribution | Active Distributors |
| Distribution | Inactive Distributors |
| Regional | Region-wise Sales Contribution |
| Product | Top SKUs by Sales Value |
| Product | Bottom SKUs by Sales Value |

---

## 3. KPI Definitions (Detailed)

### KPI 01: Total Sales Value
- **Definition:** Total net sales value for the selected period.
- **Formula:** `SUM(NetValue)`
- **Data Source:** `sales_orders.csv`
- **Business Use:** Measures overall sales performance.

---

### KPI 02: Total Orders
- **Definition:** Total number of sales orders recorded in the selected period.
- **Formula:** `COUNT(OrderID)`
- **Data Source:** `sales_orders.csv`
- **Business Use:** Tracks sales activity volume and order flow.

---

### KPI 03: Average Order Value (AOV)
- **Definition:** Average net value per order.
- **Formula:** `Total Sales Value / Total Orders`
- **Data Source:** `sales_orders.csv`
- **Business Use:** Indicates order size and revenue per transaction.

---

### KPI 04: Sales vs Target (%)
- **Definition:** Achievement percentage of sales compared to target.
- **Formula:** `(Actual Sales Value / Target Value) * 100`
- **Data Source:**  
  - Actual: `sales_orders.csv`  
  - Target: `targets.csv`
- **Business Use:** Core KPI for management to monitor target achievement.

---

### KPI 05: Active Distributors
- **Definition:** Count of distributors currently active.
- **Formula:** `COUNT(DistributorID WHERE Status='Active')`
- **Data Source:** `distributors.csv`
- **Business Use:** Helps track coverage and operational distributor base.

---

### KPI 06: Inactive Distributors
- **Definition:** Count of distributors currently inactive.
- **Formula:** `COUNT(DistributorID WHERE Status='Inactive')`
- **Data Source:** `distributors.csv`
- **Business Use:** Identifies risk of territory gaps and sales loss.

---

### KPI 07: Region-wise Sales Contribution
- **Definition:** Sales value split by region.
- **Formula:** `SUM(NetValue) GROUP BY Region`
- **Data Source:** `sales_orders.csv`
- **Business Use:** Helps management compare performance across regions.

---

### KPI 08: Top SKUs by Sales Value
- **Definition:** SKUs generating the highest sales value.
- **Formula:** `SUM(NetValue) GROUP BY ProductID ORDER BY DESC`
- **Data Source:**  
  - Sales: `sales_orders.csv`  
  - SKU Info: `products.csv`
- **Business Use:** Identifies revenue-driving products and supports promotions.

---

### KPI 09: Bottom SKUs by Sales Value
- **Definition:** SKUs generating the lowest sales value.
- **Formula:** `SUM(NetValue) GROUP BY ProductID ORDER BY ASC`
- **Data Source:**  
  - Sales: `sales_orders.csv`  
  - SKU Info: `products.csv`
- **Business Use:** Supports rationalization, bundle strategy, and market push.

---

## 4. KPI Notes / Governance
- All KPIs use **NetValue** as the primary revenue measure.
- Data is designed in an ERP-like structure:
  - **Master Data:** distributors, products
  - **Transactions:** sales orders
  - **Planning:** targets
- KPIs can be expanded later to include:
  - Order Fulfillment Rate
  - Outstanding Receivables
  - Stock Coverage Days
  - Discount / Scheme Impact
