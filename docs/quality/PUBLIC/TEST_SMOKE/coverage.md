# Coverage — PUBLIC.TEST_SMOKE

## Profiling Coverage

| Area | Status | Evidence |
|---|---|---|
| Row count | ✅ | `row_count` provided |
| Column profiling | ⛔ | `identified_columns` empty |
| Null analysis | ✅ | `null_analysis` provided |
| Duplicate analysis | ⛔ | `duplication` empty |

## Rule Coverage

| Area | Status | Evidence |
|---|---|---|
| Constraint checks | ⛔ | No explicit constraint outputs provided |
| Duplicate rules | ⛔ | No duplication metrics provided |
| Validity/domain rules | ⛔ | No invalid-value metrics provided |

## PII Coverage

| Area | Status | Evidence |
|---|---|---|
| PII column detection | ✅ | `pii_columns` provided (empty list) |
| Risk tiering | ⛔ | Not provided |

## Freshness Coverage

| Area | Status | Evidence |
|---|---|---|
| Timestamp column | ⛔ | Not provided |
| Timeline | ⛔ | Not provided |
| SLA evaluation | ⛔ | Not provided |
