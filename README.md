# E-Commerce User Behavior Analysis

## 1. Project Overview

This project analyzes user behavior for an e-commerce platform using Python for data processing  and Tableau for visualization. 
The analysis focuses on:

📈 User activity trends (DAU, WAU, MAU)

🔄 Funnel conversion analysis

📊 Retention rate tracking

💡 Business insights based on user engagement patterns
Note: The dataset is synthetic test data with evenly distributed events, meaning results are idealized 
compared to real-world scenarios.


## 2. Dataset

- Format: CSV (synthetic data)
- Main columns: user_id, event, timestamp
- Event types:
    1. page_view
    2. product_view
    3. add_to_cart
    4. purchase


## 3. Analysis Stages


### Stage 1 – Data Loading & Cleaning
- Loaded dataset using Pandas
- Converted timestamps to datetime format
- Checked for missing values and duplicates
- Verified column data types

### Stage 2 – Data Exploration
- Checked dataset size and structure
- Identified unique event types and time range
- Counted unique users per event type

### Stage 3 – Aggregated Metrics
Calculated:
- Daily Active Users (DAU)
- Weekly Active Users (WAU)
- Monthly Active Users (MAU)

### Stage 4 – Funnel & User Activity Analysis
Funnel Analysis
**Steps Analyzed**: `page_view → product_view → add_to_cart → purchase`

| Step          | Unique Users | Conversion Rate |
|---------------|--------------|-----------------|
| page_view     | 1000         | 100%            |
| product_view  | 1000         | 100%            |
| add_to_cart   | 1000         | 100%            |
| purchase      | 1000         | 100%            |

**Interpretation**:  
- All steps have identical user counts and conversion rates (100%).  
- This suggests the dataset is synthetic or uniformly distributed.  
- In real-world data, we would expect drop-offs at each stage.

**User Activity Trends**:
- DAU: ~300 users/day, stable with minor fluctuations.
- WAU: ~910–940 users/week, consistent week-to-week.
- MAU: 1000 users/month (all users active monthly).

### Stage 5 – Retention Analysis

**First 30-Day Retention Rate Table**:
- Calculated daily retention rates for first 30 days after each user's first activity.
- Exported results to CSV (retention_rate_first_30_days.csv).

**Key Observations**:
- Retention rates gradually declined over time.
- Day 1 retention close to 100% due to synthetic data consistency.
- Real-world data would typically show sharper drops.

**Summary Retention Table**:
- Calculated overall retention rates across different periods.
- Saved to retention_summary_table.csv.

### Stage 6 – Data Export
Exported files:
- retention_summary_table.csv – Summary retention metrics
- retention_rate_first_30_days.csv – Detailed daily retention rates

### Stage 7 – Visualization
**Python Charts**:

📊 Funnel Chart (Matplotlib)

📈 DAU Trend Line Chart

🔥 Retention Heatmap

**Tableau Dashboard**:
- Funnel visualization
- DAU/WAU/MAU trend
- Retention heatmap
- Filterable interactive dashboard

View Tableau Dashboard link https://public.tableau.com/app/profile/mindy.chen3731/viz/CustomerSegmentationRetentionDashboard/Story1 

## 4. Business Insights
Even though the dataset is synthetic, this workflow demonstrates:
1. Conversion Tracking – Funnel analysis helps identify drop-off points in user journeys.
2. User Engagement Trends – DAU/WAU/MAU trends reveal engagement stability or growth.
3. Retention Optimization – Retention data helps target re-engagement campaigns.
4. Scalability – Same process can be applied to real-world datasets for actionable insights.

📂 Files in This Repo
ecommerce_analysis.py – Main Python analysis script
retention_summary_table.csv – Summary retention metrics
retention_rate_first_30_days.csv – Detailed daily retention rates
(Tableau dashboard link to be added)

