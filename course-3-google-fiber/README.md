# Course 3: Decisions, Decisions — Dashboards and Reports
## Google Fiber — Repeat Calls BI Dashboard

**Status:** ✅ Complete  
**Scenario:** Google Fiber  
**Deliverable type:** Interactive Tableau Dashboard + Executive Summary

---

## Overview

In this final course, I transformed the consolidated target table from Course 2 into a fully interactive BI dashboard published on Tableau Public. The dashboard enables Google Fiber call center leadership to self-serve insights about repeat customer call trends — without needing to request custom reports from the BI team.

This course brought together all three stages of the BI workflow:
- **Plan** (Course 1) → Requirements and strategy documents
- **Build** (Course 2) → SQL pipeline and target table
- **Visualize** (Course 3) → Interactive dashboard and executive summary

---

## Live Dashboard

🔗 **[View on Tableau Public → [Tableau Public URL here](https://public.tableau.com/views/GoogleFiberRepeatCallsDashboardGoogleBICertificate/RepeatCalls?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)]**

---

## Business Problem

Google Fiber's customer service call center needed to understand how often customers call back after their first inquiry. Leadership needed a self-serve tool to explore repeat call trends by market, problem type, and time period — to improve first-call resolution rates and customer satisfaction.

**Primary question answered:**  
*How often are customers repeatedly contacting the customer service team, and what factors drive those repeat calls?*

---

## Dashboard Structure

The final workbook contains **7 worksheets** organized into **4 dashboards**, accessible through a single "Repeat Calls" navigation view.

### Worksheets

| Sheet | Type | Purpose |
|-------|------|---------|
| Repeats by Month | Bar chart | All 8 contact columns grouped by quarter and month |
| Table | Text table | Raw repeat call counts by date |
| Table - Market and Type | Text table | Cross-reference by market and problem type with totals |
| Day 1 - Graph - Market and Type | Bar chart | Day 1 repeat call volume by market and problem type |
| % Day 0 Repeats by Day of Week | Bar chart | % of initial calls by weekday — reveals Monday peak |
| % Day 0 by Market and Type | Bar chart | Day 0 call share by market and problem type |
| % Day 1 by Market and Type | Bar chart | Day 1 repeat call share by market and problem type |

### Dashboards

| Dashboard | Sheets Included | Insight Focus |
|-----------|----------------|---------------|
| Dashboard 1 | Table + Table - Market and Type | Raw data exploration |
| Dashboard 2 | Repeats by Month + Day 1 Graph | Volume trends |
| Dashboard 3 | Repeats by Month + % Day 0 by Day of Week | Day of week patterns |
| Dashboard 4 | % Day 0 + % Day 1 by Market and Type | Market and type comparison |

---

## Key Insights

1. **Monday is peak call day** — consistently ~18% of weekly call volume across all months, with Sunday the lowest at ~8–9%
2. **market_1 dominates volume** — 45,333 initial contacts vs 4,389 for market_2 and 15,217 for market_3
3. **type_2 and type_5 drive the most repeat calls** — technician troubleshooting and internet/wifi issues are harder to resolve in a single call
4. **Initial contacts run 10–15x higher than Day 1 repeats** — most issues are resolved on first contact, but the absolute repeat volume warrants targeted action

---

## Deliverables

| File | Description |
|------|-------------|
| [Google_Fiber_Executive_Summary.pdf](Google_Fiber_Executive_Summary.pdf) | Full executive summary covering business need, methods, dashboard capabilities, results, and next steps |
| [Dashboard link]([https://public.tableau.com](https://public.tableau.com/views/GoogleFiberRepeatCallsDashboardGoogleBICertificate/RepeatCalls?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)) | Live Tableau Public dashboard |

---

## Low-Fidelity Mockup

Before building, a low-fidelity mockup was created to plan the dashboard layout and chart types. The mockup defined:
- 5 chart panels across 4 dashboards
- Filter strategy (market, problem type, date range, day of week)
- Tab navigation structure for the final "Repeat Calls" view

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Google BigQuery | UNION ALL pipeline to consolidate 3 market tables |
| Tableau Public | Dashboard design, development, and publication |
| Python / ReportLab | Executive Summary PDF generation |

---

## Reflection

The biggest lesson from Course 3 was that **dashboard design is a communication exercise, not a technical one**. Every chart choice — bar vs table, absolute counts vs percentages, day-level vs month-level — was made by asking "what decision does this help the stakeholder make?" rather than "what looks impressive?"

The percentage-based views (% Day 0 by Market, % Day 0 by Day of Week) were particularly valuable because they revealed patterns that raw counts obscure — Monday's dominance and market_3's relatively higher repeat rate both only became visible when normalised.

---

*This completes the Google Business Intelligence Certificate end-of-course project portfolio.*  
*[Course 1](../course-1-google-fiber/) · [Course 2](../course-2-google-fiber/) · Course 3*
