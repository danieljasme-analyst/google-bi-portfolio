# Course 2: The Path to Insights — Data Models and Pipelines
## Google Fiber — Building the Target Table

**Status:** ✅ Complete  
**Scenario:** Google Fiber  
**Deliverable type:** SQL pipeline + combined target table

---

## Overview

In this course, I moved from planning into the technical phase of the BI project. The goal was to take three separate market datasets and consolidate them into a single target table — the foundation that the Course 3 dashboard will be built on.

This phase mirrors what a real BI professional does before any visualization work begins: understand the raw data, design a pipeline, and produce a clean, analysis-ready dataset for stakeholders.

---

## Business Context

From Course 1, the stakeholders needed a dashboard that could explore repeat call trends across **three market cities**. The data for each city lived in separate tables (`market_1`, `market_2`, `market_3`). Before any dashboard could be built, those tables needed to be combined into one unified dataset.

---

## Dataset Structure

All three source tables share an identical schema — 11 columns, 450 rows each:

| Column | Description |
|--------|-------------|
| `date_created` | Date the initial customer call was made |
| `contacts_n` | Number of contacts on the initial call date |
| `contacts_n_1` | Repeat contacts 1 day after first call |
| `contacts_n_2` | Repeat contacts 2 days after first call |
| `contacts_n_3` | Repeat contacts 3 days after first call |
| `contacts_n_4` | Repeat contacts 4 days after first call |
| `contacts_n_5` | Repeat contacts 5 days after first call |
| `contacts_n_6` | Repeat contacts 6 days after first call |
| `contacts_n_7` | Repeat contacts 7 days after first call |
| `new_type` | Problem type (type_1 through type_5) |
| `new_market` | Market identifier (market_1, market_2, or market_3) |

**Problem type reference:**

| Code | Category |
|------|----------|
| `type_1` | Account management |
| `type_2` | Technician troubleshooting |
| `type_3` | Scheduling |
| `type_4` | Construction |
| `type_5` | Internet and wifi |

---

## Why UNION ALL and not JOIN?

This is an important technical decision worth documenting.

**`UNION ALL`** stacks rows vertically — it combines tables that have the **same columns** into one longer table. This is the right choice here because all three market tables have identical structures and we simply want all rows in one place.

**`JOIN`** combines tables horizontally by matching on a shared key column. This would only apply if the tables had different columns that needed to be linked (e.g. a customer table joined to a call log table via customer ID).

Since `market_1`, `market_2`, and `market_3` all have the exact same 11 columns, `UNION ALL` is the correct and efficient approach.

```
market_1 (450 rows)  ┐
market_2 (450 rows)  ├─ UNION ALL ──► target_table (1,350 rows)
market_3 (450 rows)  ┘
```

---

## SQL Pipeline

The full query is available in [`google_fiber_union_query.sql`](google_fiber_union_query.sql).

```sql
CREATE OR REPLACE TABLE `google-fiber-bi.google_fiber.target_table` AS

SELECT
  date_created, contacts_n, contacts_n_1, contacts_n_2, contacts_n_3,
  contacts_n_4, contacts_n_5, contacts_n_6, contacts_n_7, new_type, new_market
FROM `google-fiber-bi.google_fiber.market_1`

UNION ALL

SELECT
  date_created, contacts_n, contacts_n_1, contacts_n_2, contacts_n_3,
  contacts_n_4, contacts_n_5, contacts_n_6, contacts_n_7, new_type, new_market
FROM `google-fiber-bi.google_fiber.market_2`

UNION ALL

SELECT
  date_created, contacts_n, contacts_n_1, contacts_n_2, contacts_n_3,
  contacts_n_4, contacts_n_5, contacts_n_6, contacts_n_7, new_type, new_market
FROM `google-fiber-bi.google_fiber.market_3`;
```

---

## Output

| File | Description |
|------|-------------|
| [`google_fiber_union_query.sql`](google_fiber_union_query.sql) | BigQuery SQL to create the combined target table |
| [`target_table.csv`](target_table.csv) | The resulting combined dataset — 1,350 rows, 11 columns |

**Verification:** `SELECT COUNT(*) FROM target_table` → **1,350 rows** ✅

---

## Tools Used

- **Google BigQuery** — running the UNION ALL SQL query
- **Tableau Public** — connecting to the target table for dashboard development (Course 3)

> Note: Tableau Public does not support a native BigQuery connector. The target table was exported as a CSV and connected via Tableau's text file connector — a valid and common workflow for Tableau Public users.

---

## Reflection

The key lesson from this course is that **data pipeline decisions have downstream consequences**. Choosing `UNION ALL` over `JOIN` here wasn't just a syntax preference — it was the correct logical choice based on the shape of the data. A wrong choice at this stage would have produced incorrect row counts or missing data that would silently corrupt every chart in the dashboard.

Documenting the *why* behind technical decisions (as done in this README) is a habit that separates junior analysts from senior ones.

---

*Next: [Course 3 — Dashboard design and final BI report](../course-3-google-fiber/)*
