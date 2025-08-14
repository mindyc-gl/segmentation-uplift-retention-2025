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
