# Coverage — PUBLIC.CUSTOMERS

## Profiling Coverage

| Area | Status | Evidence |
|---|---|---|
| Row count | ✅ | `row_count` provided |
| Column profiling | ✅ | `identified_columns` provided |
| Null analysis | ✅ | `null_analysis` provided |
| Duplicate analysis | ✅ | `duplication` provided |

## Rule Coverage

| Area | Status | Evidence |
|---|---|---|
| Constraint checks | ⛔ | No explicit constraint outputs provided |
| Duplicate rules | ✅ | Duplicate metrics + dedupe keys provided |
| Validity/domain rules | ⛔ | No invalid-value metrics provided |

## PII Coverage

| Area | Status | Evidence |
|---|---|---|
| PII column detection | ✅ | `pii_columns` provided |
| Risk tiering | ⛔ | Not provided |

## Freshness Coverage

| Area | Status | Evidence |
|---|---|---|
| Timestamp column | ✅ | `freshness.timestamp_column` provided |
| Timeline | ✅ | `freshness.timeline` provided |
| SLA evaluation | ✅ (flag-driven) | "Table refreshed within SLA." |
