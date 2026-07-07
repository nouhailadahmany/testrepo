# Rule Violations — RETAIL_DWH.PUBLIC.CUSTOMERS

## Findings (from quality flags)

| Severity | Category | Column | Message |
|---|---|---|---|
| high | pii | EMAIL | Sensitive PII columns detected. |
| medium | nulls | PHONE | PHONE contains more than 5% NULL values. |
| low | duplicates | CUSTOMER_ID | 12 duplicate CUSTOMER_ID values detected. |
| low | freshness | LAST_UPDATED | Table refreshed within SLA. |

## Duplicates
- **Duplicate row count:** 12
- **Duplicate rate:** 0.001
- **Dedupe keys:** CUSTOMER_ID
- **Examples:** CUSTOMER_ID = 4128; 9911
