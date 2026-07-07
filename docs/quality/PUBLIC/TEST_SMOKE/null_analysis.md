# Null Analysis — PUBLIC.TEST_SMOKE

## Null Percentage Charts

```mermaid
xychart-beta
title "Null Rate by Column (PUBLIC.TEST_SMOKE)"
x-axis ["COL_A"]
y-axis "Null rate" 0 --> 0.10
bar [0.05]
```

(ASCII fallback)

```
COL_A | █████░░░░░ 5.00%
```

## Null Severity Rankings

Severity rules (deterministic):
- High: >= 10%
- Medium: >= 5% and < 10%
- Low: > 0% and < 5%
- None: 0%

| Rank | Column | Null rate | Severity |
|---:|---|---:|---|
| 1 | COL_A | 0.05 | Medium |

## Column Completeness Analysis

| Column | Completeness (1 - null_rate) |
|---|---:|
| COL_A | 0.95 |
