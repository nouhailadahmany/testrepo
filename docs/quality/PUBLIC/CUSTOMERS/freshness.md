# Freshness — PUBLIC.CUSTOMERS

## Freshness Metrics

| Metric | Value |
|---|---|
| Timestamp column | `LAST_UPDATED` |
| Last updated | `2026-07-06T17:42:51Z` |
| Max lag hours | 4 |

## Freshness Timelines

Provided timeline (daily):

```mermaid
gantt
title PUBLIC.CUSTOMERS Observed Update Days
dateFormat  YYYY-MM-DD
axisFormat  %Y-%m-%d
section Updates
2026-07-02 :done, u1, 2026-07-02, 1d
2026-07-03 :done, u2, 2026-07-03, 1d
2026-07-04 :done, u3, 2026-07-04, 1d
2026-07-05 :done, u4, 2026-07-05, 1d
2026-07-06 :done, u5, 2026-07-06, 1d
```

## Staleness Warnings

| Status | Detail |
|---|---|
| No staleness warning emitted | Quality flag indicates: "Table refreshed within SLA." |

## Update Recency Analysis

| Field | Value |
|---|---|
| Min observed `LAST_UPDATED` | 2026-05-01T08:12:11Z |
| Max observed `LAST_UPDATED` | 2026-07-06T17:42:51Z |
