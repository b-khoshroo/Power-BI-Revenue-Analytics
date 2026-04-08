# <p align = "center"> Power-BI-Revenue-Analytics</p>

## Project Overview
This repository contains an end-to-end Power BI business intelligence solution designed to analyze revenue streams, project profitability, and operational support efficiency. The project transitions raw, fragmented data into a structured <b>Star Schema</b> model, powered by a library of <b>26 custom DAX measures</b> to drive executive decision-making.
<br></br>
## Technical Workflow
### 1. Data Transformation (Power Query)
The transformation layer focused on converting system-generated values into business-friendly dimensions:
* <b>Cleaning & Normalization</b>: Performed extensive trimming, cleaning, and data type conversions (e.g., converting IDs from numbers to text to prevent aggregation).
* <b>Ambiguity Resolution</b>: Renamed overlapping columns, such as distinguishing "Contracted MRR" from "Actual MRR," to ensure calculation accuracy.
* <b>Calendar Table Logic</b>: Validated and streamlined the Date dimension, removing redundant keys to optimize model performance.

### 2. Data Modeling
The model is built on a <b>Star Schema</b> architecture:
* <b>Fact Tables</b>: ProjectSales, SubscriptionRevenue, and SupportTickets.
* <b>Dimension Tables</b>: Customer, Employee, Office, and Date.
* <b>Relationship Integrity</b>: Utilized bridge tables (e.g., BridgeEmployeeProject) and bi-directional filters where necessary to capture complex many-to-many relationships.
  
![Data Model](<Visuals/Data Model.png>)

### 3. DAX Analytics Library
The project features 26 sophisticated measures categorized by business function:
* <b>Financial & Revenue</b>: YTD tracking, Profit Margins, and Target Gap analysis.
* <b>Subscription and Recurring Revenue (SaaS Metrics)</b>: Month-over-Month MRR Growth % and Annual Recurring Revenue (ARR).
* <b>Human Capital and Project Operations</b>: Cross-functional collaboration ratios and employee participation rates.
* <b>Support and Operational Service</b>: Ticket concentration by project and average resolution aging.
<br></br>
## Key Visualizations & Insights
### Executive Financial Health
* <b>Insight</b>: Real-time tracking of YTD Revenue and Profit Margins allows for immediate assessment of fiscal health against a target milestone.
### SaaS Revenue Momentum
* <b>Insight</b>: The Total Actual MRR Growth visual identifies critical inflection points in subscription momentum, providing a deeper look into revenue velocity beyond static totals.
### Historical Revenue Context
* <b>Insight</b>: By visualizing Actual MRR Prior Month, the model provides a 5-year historical baseline to validate growth trends and seasonal performance.
<br></br>
## Governance & Scalability
To ensure long-term viability, the project implements:
* <b>Sustainable Schema Design</b>: Supports the addition of new departments or projects without requiring a model rebuild.
* <b>DAX Optimization</b>: Used variables (VAR) to reduce processing load and improve report responsiveness.
* <b>Documentation</b>: All measures include rich metadata and logic descriptions for transparency.

