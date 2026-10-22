# Insurance Policy Persistency & Claims Performance Analysis

An end-to-end analytics project using **SQL, Power Query, DAX and Power BI** on an insurance portfolio (no real customer data).

**Business questions:** Which channels and products keep customers? Where do claims run late, and does it cost renewals? Which active policies are at risk of lapsing?

## Data (simulated, as of 30 Sep 2026)
6,500 policies | 4,800 customers | 45,521 payments | 8,286 renewals | 1,542 claims | 1,232 feedback records | 6 products (Life, Motor, Health, Property)

## What I did
1. **SQL (SQLite):** 12 queries using joins, CTEs, window functions and conditional aggregation: renewal rate, early surrender, claims vs SLA, delay causes, sentiment, payment behaviour, lapse-risk list.
2. **Power Query:** typed 7 tables, built `Days_To_Settle` and `Delayed` flag with custom columns.
3. **Data model + DAX:** date table, star-style relationships, measures for renewal rate, early surrender rate, % claims delayed, avg days to settle, avg rating, missed-payment %.
4. **Power BI report (4 pages):** Executive Summary, Claims Performance, Root Cause & Retention, Management Summary.

## Key findings
- Renewal rate drops from **82.8%** after an on-time claim to **70.5%** after a delayed claim.
- Customer rating: **4.16** (on-time claims) vs **2.17** (delayed claims).
- **Bancassurance** has the weakest renewal rate (**73.7%**) and the highest missed-payment rate (~10%).
- **Property claims** breach SLA most often (55.8%); top causes are assessor delays and missing documents.
- Savings Plan early surrender is 13.4% vs 6.2% for Term Life.

*These show association, not proven causation.*

## Files
- `sql/` : schema and the 12 analysis queries
- `data/` : CSV files and `insurance.db`
- `report/` : dashboard PDF and `.pbix`
- `screenshots/` : report pages

Author: Daniel Aiyede | datascienceportfol.io/aiyedeo
