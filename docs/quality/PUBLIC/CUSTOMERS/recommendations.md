# Recommendations — RETAIL_DWH.PUBLIC.CUSTOMERS

## Highest-impact actions
1. Reduce `PHONE` null rate (currently 7.13%)
   - Confirm if PHONE is required; if yes, enforce capture at source or backfill from trusted systems.
   - Add alerting rule for PHONE null% > 5%.

2. Investigate `EMAIL` null-rate spike
   - Validate upstream changes, ingestion filters, and recent application/schema releases.

3. PII controls
   - Ensure EMAIL/PHONE are masked in non-prod and restricted in prod.

## Monitoring
- Track daily null rates for EMAIL and PHONE.
- Track duplicates on `CUSTOMER_ID` (current duplicates: 12 rows; rate 0.001).

## Notes
- Overall table quality is considered **GOOD**.
- Monitoring recommended for PHONE null rate.
