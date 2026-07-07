# Data Quality — RETAIL_DWH.PUBLIC.CUSTOMERS

**Database:** RETAIL_DWH  
**Schema:** PUBLIC  
**Table:** CUSTOMERS  
**Rows (profiled):** 12,543

## Dashboard

| Area | Status / Highlights | Report |
|---|---|---|
| Freshness | **Healthy** (last update: `2026-07-01 08:15:00`) | [freshness](./freshness.md) |
| Nulls | EMAIL nulls **18.2%**; PHONE nulls **42.7%** | [null analysis](./null_analysis.md) |
| Duplicates | CUSTOMER_ID duplicates: **0** | [duplicates](./duplicates.md) |
| PII | Detected PII columns: **EMAIL, PHONE** | [pii](./pii.md) |
| Rule violations | 1 finding | [rule violations](./rule_violations.md) |
| Anomalies | 1 detected | [anomalies](./anomalies.md) |
| Business usage | Dimension; joined with SALES, ORDERS | [business usage](./business_usage.md) |
| Coverage | Column coverage snapshot | [coverage](./coverage.md) |
| Overall quality | Computed score + drivers | [quality score](./quality_score.md) |

## Contents
- [dashboard](./dashboard.md)
- [profiling](./profiling.md)
- [null analysis](./null_analysis.md)
- [duplicates](./duplicates.md)
- [freshness](./freshness.md)
- [quality score](./quality_score.md)
- [rule violations](./rule_violations.md)
- [column health](./column_health.md)
- [pii](./pii.md)
- [anomalies](./anomalies.md)
- [business usage](./business_usage.md)
- [coverage](./coverage.md)
- [recommendations](./recommendations.md)
