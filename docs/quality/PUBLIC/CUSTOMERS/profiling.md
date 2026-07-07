# Profiling — PUBLIC.CUSTOMERS

## Row Counts

| Metric | Value |
|---|---:|
| Row count | 12,543 |

## Null Analysis (per provided null_analysis)

| Column | Null count | Null rate |
|---|---:|---:|
| EMAIL | 234 | 0.0187 |
| PHONE | 894 | 0.0713 |
| COUNTRY | 4 | 0.0003 |
| LAST_UPDATED | 0 | 0.0 |

## Duplicate Analysis

| Metric | Value |
|---|---|
| Duplicate row count | 12 |
| Duplicate rate | 0.001 |
| Dedupe keys | `CUSTOMER_ID` |

Examples (dedupe key values):

| CUSTOMER_ID |
|---:|
| 4128 |
| 9911 |

## Profiling Metrics (identified columns)

| Column | Data type | Description | Distinct count | Min | Max | Sample values |
|---|---|---|---:|---|---|---|
| CUSTOMER_ID | NUMBER | Unique customer identifier | 12,543 | 1 | 12,543 | 1001, 1002, 1003 |
| EMAIL | VARCHAR | Customer email address | 11,874 | — | — | john.smith@email.com, alice@email.com |
| PHONE | VARCHAR | Customer phone number | 11,234 | — | — | +33612345678, +33687654321 |
| COUNTRY | VARCHAR | Country of residence | 18 | — | — | France, Germany, Spain |
| LAST_UPDATED | TIMESTAMP_NTZ | Timestamp of last update | 12,401 | 2026-05-01T08:12:11Z | 2026-07-06T17:42:51Z | — |
