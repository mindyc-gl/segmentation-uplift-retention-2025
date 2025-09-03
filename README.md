*E-Commerce Customer Segmentation & Retention Analysis*
1. Project Overview

This project analyzes customer behavior on an e-commerce platform using Python for data processing and Tableau for visualization. The focus is on RFM segmentation, customer retention, and revenue contribution to uncover loyalty patterns and churn risks.

Key Objectives

📊 Segment users with RFM (Recency, Frequency, Monetary) analysis

🔄 Track customer retention trends over time

💰 Measure revenue contribution by customer segment

💡 Generate actionable insights for customer engagement strategy

2. Dataset

Format: CSV (synthetic test data)

Main Columns: user_id, event, timestamp

Event Types: page_view, product_view, add_to_cart, purchase

⚠️ Note: Dataset is synthetic with evenly distributed events, so results are idealized compared to real-world scenarios.

3. Analysis Stages

Stage 1 – Data Preparation

Loaded dataset with Pandas

Converted timestamps to datetime

Removed duplicates & checked data types

Stage 2 – RFM Segmentation

Calculated Recency, Frequency, and Monetary scores

Assigned users into segments (e.g., Loyal Customers, Potential Loyalists, VIP, At Risk, Lost Customers)

Stage 3 – Retention Analysis

Calculated retention rates by cohort

Built retention curves to track segment-level user loyalty over time

Stage 4 – Revenue Analysis

Measured revenue contribution by RFM segment

Identified high-value groups vs. churn-risk groups

Stage 5 – Visualization (Tableau)

RFM Bubble Chart → Customer Segmentation

Retention Curve → Retention trends by segment

Revenue Contribution → Which groups drive the most revenue

Segment Movement → How customers shift between segments over time

View Tableau Dashboard link https://public.tableau.com/app/profile/mindy.chen3731/viz/CustomerSegmentationRetentionDashboard/Story1 

4. Business Insights
- Loyal Customers drive the majority of revenue (67.3%) and show strong retention.
- Potential Loyalists are the main growth opportunity, with room to convert into VIPs.
- VIP Customers have the highest per-user spend but need strategies to maintain engagement.
- At Risk & Lost Customers highlight churn risks requiring reactivation efforts.

5. Files in This Repo
ecommerce_analysis.py → Python data processing & RFM calculation
retention_summary_table.csv → Summary of retention metrics
customer_rfm_segments.csv → Exported RFM segmentation results
Tableau Dashboard link (interactive visualization)
