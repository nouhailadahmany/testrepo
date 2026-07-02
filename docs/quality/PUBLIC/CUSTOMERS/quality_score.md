# Quality Score — RETAIL_DWH.PUBLIC.CUSTOMERS

## Summary

A lightweight score computed from available signals in the payload.

## Inputs used
- Null rates (EMAIL, PHONE)
- Duplicate count (CUSTOMER_ID)
- Freshness status
- Rule violations / anomalies counts

## Score (heuristic)

| Component | Result |
|---|---|
| Freshness | Healthy |
| Duplicates | 0 on CUSTOMER_ID |
| Null health | EMAIL 18.2%, PHONE 42.7% |
| Exceptions | 1 violation, 1 anomaly |

**Overall:** Needs attention (driven primarily by PHONE null rate and EMAIL null spike)
