# Data Quality — RETAIL_DWH.PUBLIC.CUSTOMERS

**Database:** RETAIL_DWH  
**Schema:** PUBLIC  
**Table:** CUSTOMERS  
**Rows (profiled):** 12,543

## Dashboard

| Area | Status / Highlights | Report |
|---|---|---|
| Freshness | **Healthy** (last updated: `2026-07-06T17:42:51Z`, SLA max lag: 4h) | [freshness](./freshness.md) |
| Quality score | **93 / 100** (Completeness 95, Uniqueness 100, Validity 90, Consistency 88) | [quality score](./quality_score.md) |
| Nulls | EMAIL nulls **1.87%**; PHONE nulls **7.13%** | [null analysis](./null_analysis.md) |
| Duplicates | Duplicate rows: **12** (dedupe key: CUSTOMER_ID) | [rule violations](./rule_violations.md#duplicates) |
| PII | **PII detected:** EMAIL, PHONE | [pii](./pii.md) |
| Anomalies | 2 detected (PHONE null-rate outlier; EMAIL null-rate spike) | [anomalies](./anomalies.md) |
| Column health | Mixed (PHONE impacted by nulls) | [column health](./column_health.md) |
| Coverage | Column coverage snapshot | [coverage](./coverage.md) |
| Recommendations | Monitoring + remediation actions | [recommendations](./recommendations.md) |

## Contents
- [dashboard](./dashboard.md)
- [profiling](./profiling.md)
- [null analysis](./null_analysis.md)
- [freshness](./freshness.md)
- [quality score](./quality_score.md)
- [rule violations](./rule_violations.md)
- [column health](./column_health.md)
- [pii](./pii.md)
- [anomalies](./anomalies.md)
- [business usage](./business_usage.md)
- [coverage](./coverage.md)
- [recommendations](./recommendations.md)
