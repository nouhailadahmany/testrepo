# Schema: MARTS

## Summary
- Tables: 5
- Columns: 128
- Constraints present: false
- Notes: No constraints returned for this schema (views).

## Table classification
| Table | Type | Classification | Confidence | Key candidates | Notes |
|---|---|---|---|---|---|
| V_CAMPAIGN_ROI | VIEW | FACT | medium |  | Aggregated KPIs (TOTAL_, ROAS, CTR_PCT, CVR_PCT). |
| V_CUSTOMER_360 | VIEW | DIMENSION | medium | CUSTOMER_ID | Customer profile with aggregated measures (TOTAL_*). |
| V_INVENTORY_HEALTH | VIEW | FACT | medium |  | Inventory measures + derived status. |
| V_PRODUCT_PERFORMANCE | VIEW | FACT | medium | PRODUCT_ID | Product performance aggregates (NET_REVENUE_EUR, GROSS_PROFIT_EUR, UNIQUE_CUSTOMERS). |
| V_SALES_PERFORMANCE | VIEW | FACT | medium |  | Sales reporting view with measures and breakdown attributes. |

## Relationships
None detected/provided.

## Transformation patterns
### aggregation
- TOTAL_IMPRESSIONS
- TOTAL_CLICKS
- TOTAL_CONVERSIONS
- TOTAL_SPEND
- TOTAL_REVENUE_ATTRIBUTED
- TOTAL_ORDERS
- TOTAL_UNITS
- TOTAL_SPEND_EUR
- AVG_ORDER_VALUE_EUR
- UNIQUE_CUSTOMERS

### date
- FULL_DATE
- LAST_ORDER_DATE
- FIRST_ORDER_DATE
- YEAR
- MONTH_NAME
- QUARTER_NAME

### flags
- IS_ACTIVE
- IS_NEWSLETTER
- IS_OUT_OF_STOCK
- IS_LOW_STOCK
- IS_RETURNED
