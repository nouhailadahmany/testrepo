# Recommendations — PUBLIC.CUSTOMERS

## Recommendations

| Priority | Recommendation | Trigger (source data) |
|---|---|---|
| High | Enforce PII governance controls (masking, RBAC, audit) for `EMAIL`, `PHONE` | `pii_columns` + high severity PII flag |
| Medium | Reduce `PHONE` NULL rate; investigate ingestion/collection coverage | `PHONE` null_rate=0.0713 + medium nulls flag + anomaly outlier |
| Low | Review duplicate handling on `CUSTOMER_ID`; confirm upstream dedupe logic | `duplication.duplicate_row_count`=12 |

## Quality Improvements

No data available (no root-cause diagnostics provided beyond flags/anomalies).

## Monitoring Suggestions

- Monitor `PHONE` null rate against expected max (0.05) as indicated in anomaly details.
- Track `EMAIL` null-rate changes (spike noted: +3.2%).

## Governance Recommendations

- Maintain PII inventory for `EMAIL` and `PHONE` and ensure least-privilege access.
