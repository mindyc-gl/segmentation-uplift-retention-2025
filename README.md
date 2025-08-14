1. Data overview
- Rows: 74,817
- Columns: 7
- UserID, SessionID, Timestamp, EventType, ProductID, Amount, Outcome

 Data types:
 UserID (int), SessionID (int), Timestamp (object → should be converted to datetime),  EventType (object), ProductID (object), Amount (float), Outcome (object)

2. Missing values
- ProductID: 42,704 missing
- Amount: 64,135 missing
- Outcome: 64,135 missing
- The other columns have 0 missing values.

3. Uniqueness
- UserID: 1,000 unique
- SessionID: 10 unique
- Timestamp: almost all unique (likely each event has its own time)
- EventType: 7 unique
- ProductID: 8,747 unique
- Amount: 10,682 unique
- Outcome: 1 unique value (this is suspicious — might not be useful unless it has meaningful distribution in context)

Stage 3 – User Activity & Funnel Analysis
Funnel Analysis

Steps Analyzed: page_view → product_view → add_to_cart → purchase

Result:

Step	Unique Users	Conversion Rate
page_view	1000	100%
product_view	1000	100%
add_to_cart	1000	100%
purchase	1000	100%

Interpretation:
All steps have identical user counts and conversion rates (100%).
This indicates that every user in the dataset performed all four actions.
This is unusual in real-world data and suggests your current dataset is test or synthetic data with uniform distribution.
In a real dataset, we would expect a drop at each stage as some users don’t progress to the next step.

Daily, Weekly, Monthly Active Users

Daily Active Users (DAU):

Average ~300 users per day.

Peak ~340 users, lowest ~175 users (likely incomplete data at the end of the dataset).

Relatively stable over time with slight fluctuations.

Weekly Active Users (WAU):

Around ~910–940 users per week.

Very consistent week-to-week, no strong upward or downward trend.

Monthly Active Users (MAU):

Always 1000 users, meaning all users were active in each month (again indicating synthetic dataset).

DAU Trend Visualization

Shows a stable pattern of daily usage without significant growth or decline.

A sharp drop at the very end likely due to incomplete last-day data.
