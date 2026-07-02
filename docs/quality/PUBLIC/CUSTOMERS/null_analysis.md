# Null Analysis — RETAIL_DWH.PUBLIC.CUSTOMERS

| Column | Nullable | Null % | Notes |
|---|---:|---:|---|
| CUSTOMER_ID | false | 0.0% | Primary identifier; should remain non-null |
| EMAIL | true | 18.2% | Consider whether EMAIL is optional for all customer types |
| PHONE | true | 42.7% | Above threshold; see rule violations |
