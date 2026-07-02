# Recommendations — RETAIL_DWH.PUBLIC.CUSTOMERS

## Highest-impact actions
1. **Reduce PHONE null rate (42.7%)**
   - Confirm whether PHONE is truly optional. If not, enforce capture at source or backfill from trusted systems.
   - Add a rule with an agreed threshold (e.g., null% ≤ 10%) and alerting.

2. **Investigate EMAIL null spike (+15%)**
   - Check upstream changes, ingestion filters, and recent schema/application releases.
   - Compare null% by load batch/date if available.

3. **PII controls**
   - Ensure EMAIL/PHONE are masked in non-prod and restricted in prod.

## Suggested rules to add
- `PHONE` null percentage ≤ threshold.
- `CUSTOMER_ID` uniqueness (no duplicates).
