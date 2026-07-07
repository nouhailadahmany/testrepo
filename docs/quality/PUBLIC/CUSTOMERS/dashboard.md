# Enterprise Quality Dashboard — PUBLIC.CUSTOMERS

## Executive Metrics

| Metric | Value |
|---|---:|
| Rows | 12,543 |
| Overall score | 93 |
| Completeness | 95 |
| Uniqueness | 100 |
| Validity | 90 |
| Consistency | 88 |
| Duplicate rows | 12 |
| PII columns | 2 |
| Last updated | 2026-07-06T17:42:51Z |
| Max lag (hrs) | 4 |

## Quality Trend Summary

Freshness timeline provided (date-grain):

```mermaid
gantt
title PUBLIC.CUSTOMERS Refresh Timeline (LAST_UPDATED)
dateFormat  YYYY-MM-DD
axisFormat  %Y-%m-%d
section Observed Refresh Days
2026-07-02 :done, d1, 2026-07-02, 1d
2026-07-03 :done, d2, 2026-07-03, 1d
2026-07-04 :done, d3, 2026-07-04, 1d
2026-07-05 :done, d4, 2026-07-05, 1d
2026-07-06 :done, d5, 2026-07-06, 1d
```

(ASCII fallback)

```
2026-07-02 | █
2026-07-03 | █
2026-07-04 | █
2026-07-05 | █
2026-07-06 | █
```

## Operational Highlights

- **Duplicates:** 12 duplicate rows detected on dedupe key(s): `CUSTOMER_ID`.
- **Null risk:** `PHONE` null rate is **7.13%** (flagged > 5%).
- **PII:** `EMAIL`, `PHONE` flagged as sensitive; ensure masking / access controls.
- **Freshness:** Flag indicates refreshed within SLA; last observed update `2026-07-06T17:42:51Z`.
