Project Overview

OmniStep Footwear is a global retailer operating across 6 international markets. This project analyzes a dataset of over 30,000 transactions (generating $9.08M+ in revenue) to identify regional operational bottlenecks, assess omnichannel customer behavior, and evaluate the true financial impact of aggressive promotional markdowns.

Business Problem

The executive team needed actionable visibility into three core areas:

Profitability Leakage: Are 30%+ discount campaigns actually driving volume, or just eroding margins?

Customer Misalignment: How do income levels dictate preferred sales channels and payment methods?

Operational Gaps: Which global regions and product sizes are underperforming, causing inventory imbalances?

 Data Architecture & Methodology

To ensure enterprise-grade performance and scalability, the raw flat-file dataset was heavily modeled before any visualizations were built.

ETL & Data Lineage: Utilized Power Query to isolate raw data into a non-loading staging table, creating a pristine pipeline for downstream transformations.

Star Schema Design: Refactored flat transaction records into a fully normalized Star Schema, generating integer surrogate keys for Dim_Product and Dim_Order_Context to maximize the VertiPaq engine's compression and filtering speeds.

Dynamic Time-Intelligence: Built a boundary-locked Dim_Calendar table using DAX MIN/MAX variables to guarantee future-proof chronological reporting.

Modular DAX: Created a dedicated Measures table housing custom iterator functions (SUMX) to calculate advanced metrics like Discount Elasticity Index and Revenue Retention Rate.

 Key Strategic Insights

The Margin Illusion: Analysis of the Discount Elasticity Index revealed that pushing markdowns to 30% in the Running category actually decreased unit volume (from 2,640 down to 2,471 units). The strategy recommendation is to cap discounts at 20% to prevent margin dilution without sacrificing market share.

Geographic Variances: The UAE emerged as the highest-performing market ($1.55M Net Revenue), while localized bottlenecks in Pakistan ($1.46M) require immediate supply chain audits.

Inventory Velocity: Global demand is heavily skewed toward Size 7 footwear. Supply chain procurement should optimize production runs toward this high-velocity profile while tightening Size 8 inventory buffers to reduce holding costs.

 Tech Stack

Tool: Power BI Desktop

Data Transformation: Power Query (M)

Modeling & Calculations: DAX

Design: Custom JSON Theme (Matte Grey & Athletic Accents)
