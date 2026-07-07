# Column Health — RETAIL_DWH.PUBLIC.CUSTOMERS

Heuristic health by column based on nulls, uniqueness, and flags.

| Column | Health | Drivers |
|---|---|---|
| CUSTOMER_ID | Good | Uniqueness strong; low duplicate rate (0.1%). |
| EMAIL | Good | Low null rate (1.87%); anomaly spike observed—monitor. |
| PHONE | Fair | Null rate 7.13% (above 5% threshold); outlier anomaly. |
| COUNTRY | Good | Very low null rate (0.03%). |
| LAST_UPDATED | Good | Non-null; supports freshness SLA. |
