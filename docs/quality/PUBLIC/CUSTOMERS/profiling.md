# Profiling — RETAIL_DWH.PUBLIC.CUSTOMERS

**Row count:** 12,543

## Columns

| Column | Type | Description | Distinct | Min | Max | Sample values |
|---|---|---|---:|---|---|---|
| CUSTOMER_ID | NUMBER | Unique customer identifier | 12,543 | 1 | 12,543 | 1001, 1002, 1003 |
| EMAIL | VARCHAR | Customer email address | 11,874 | — | — | john.smith@email.com, alice@email.com |
| PHONE | VARCHAR | Customer phone number | 11,234 | — | — | +33612345678, +33687654321 |
| COUNTRY | VARCHAR | Country of residence | 18 | — | — | France, Germany, Spain |
| LAST_UPDATED | TIMESTAMP_NTZ | Timestamp of last update | 12,401 | 2026-05-01T08:12:11Z | 2026-07-06T17:42:51Z | — |

## Duplication (key)

| Key columns | Duplicate rows | Duplicate rate |
|---|---:|---:|
| CUSTOMER_ID | 12 | 0.001 |
