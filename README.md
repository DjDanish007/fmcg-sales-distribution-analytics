# Fmcg-sales-distribution-analytics
ERP-inspired FMCG Sales &amp; Distribution analytics dashboard showcasing KPIs, distributor performance, targets, and business insights using simulated enterprise data.

FMCG Sales & Distribution Analytics Dashboard
📌 Overview

This project demonstrates an ERP-inspired FMCG Sales & Distribution Analytics Dashboard designed to provide business stakeholders with actionable visibility into sales performance, distributor efficiency, targets, and regional trends.

The solution simulates real-world FMCG enterprise data flows and focuses on business decision-making, not just visualization.

🎯 Business Problem

In large FMCG organizations, sales and distribution data often exists across multiple systems (ERP, distributor portals, manual reports), resulting in:

Delayed management visibility

Poor distributor performance tracking

Limited insight into sales vs targets

Reactive decision-making

Management requires a single, easy-to-understand analytical view to monitor performance and take timely actions.

💡 Solution Approach

This dashboard acts as a lightweight analytical layer on top of ERP-style datasets, enabling:

Monitoring of key sales and distribution KPIs

Identification of high- and low-performing distributors

Regional sales trend analysis

Sales vs target tracking

The solution is intentionally kept simple, scalable, and business-centric, reflecting how analytical dashboards are often designed in enterprise FMCG environments.

📊 Key KPIs Covered

Total Sales Value

Sales vs Target (%)

Distributor Performance (Active / Inactive)

Region-wise Sales Contribution

Top & Bottom Performing Distributors

SKU-level Sales Insights

Outstanding Sales Trends (simulation)

🗂️ Data Model (ERP-Inspired)

The project uses structured CSV files to simulate ERP transactional and master data:

Distributors – Distributor master data

Products (SKUs) – FMCG product master

Sales Orders – Daily transactional sales data

Targets – Monthly / regional sales targets

This structure mirrors real ERP concepts such as master data, transactions, and reporting layers.

🛠️ Tools & Technologies

HTML5

CSS3

JavaScript

Chart.js

CSV (ERP-style datasets)

No backend or database is required for the current version.

📁 Project Structure
fmcg-sales-distribution-analytics
│
├── data
│   ├── distributors.csv
│   ├── products.csv
│   ├── sales_orders.csv
│   └── targets.csv
│
├── dashboard
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── docs
│   ├── 01_Business_Problem.md
│   ├── 02_KPI_Definition.md
│   └── 03_Business_Insights.md
│
└── README.md

🧠 Business Insights (Sample)

Identification of regions with declining sales trends

Early warning for distributor inactivity

Target achievement gaps by region

SKU concentration risk in specific markets

These insights reflect typical FMCG sales review discussions at regional and national levels.

🚀 Future Enhancements

Region, distributor, and SKU-level filters

Power BI / Tableau version

Backend integration (SQL / API)

Role-based views (Sales Manager, Distribution Head)

Automated data refresh

👤 Author

Dilnawaz sajid
Solution Analyst – FMCG
Expertise in ERP-driven sales, distribution, and analytics solutions.

📌 Disclaimer

All data used in this project is simulated and intended purely for demonstration and learning purposes. No real company data is used.
