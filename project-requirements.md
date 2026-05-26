# Project Requirements Document: Google Fiber

**BI Analyst:** Ahmad Daniel  
**Client/Sponsor:** Emma Santiago, Hiring Manager  
**Date:** May 2026

---

## Purpose

As part of the interview process, the Fiber customer service team requested a dashboard using fictional call center data — based on data they use regularly on the job — to gain insights about repeat callers. The team's ultimate goal is to communicate with customers to reduce call volume, increase customer satisfaction, and improve operational optimization. The dashboard should demonstrate an understanding of this goal and provide stakeholders with insights about repeat caller volumes in different markets and the types of problems they represent.

---

## Key Dependencies

The datasets are fictionalized versions of the actual data this team works with. Because of this, the data is already anonymized and approved. Stakeholders will need data access to all datasets so they can explore the steps taken.

**Primary contacts:**
- Emma Santiago — Hiring Manager
- Keith Portone — Project Manager

---

## Stakeholder Requirements (Prioritized)

In order to continuously improve customer satisfaction, the dashboard must help Google Fiber decision-makers understand how often customers have to repeatedly call and what problem types or other factors might be influencing those calls.

| Requirement | Priority |
|-------------|----------|
| A chart or table measuring repeat calls by their first contact date | R — Required |
| A chart or table exploring repeat calls by market and problem type | R — Required |
| Explore repeat caller trends in the three different market cities | R — Required |
| Design charts so stakeholders can view trends by week, month, quarter, and year | R — Required |
| Charts showcasing repeat calls by week, month, and quarter | D — Desired |
| Provide insights into the types of customer issues that generate more repeat calls | D — Desired |

---

## Success Criteria (SMART)

1. **Specific:** BI insights must clearly identify the specific characteristics of repeat calls, including how often customers are repeating calls.
2. **Measurable:** Calls should be evaluated using measurable metrics, including frequency and volume. For example: do customers call with a specific problem more often than others? Which market city experiences the most calls? How many customers are calling more than once?
3. **Action-oriented:** These outcomes must quantify the number of repeat callers under different circumstances to provide the Google Fiber team with insights into customer satisfaction.
4. **Relevant:** All metrics must support the primary question: *How often are customers repeatedly contacting the customer service team?*
5. **Time-bound:** Analyze data that spans at least one year to understand how repeat callers change over time. Exploring data across multiple months will capture peaks and valleys in usage.

---

## User Journeys

The team's ultimate goal is to communicate with customers to reduce call volume and increase customer satisfaction and improve operational optimization. The dashboard should demonstrate an understanding of this goal and provide stakeholders with insights about repeat caller volumes in different markets and the types of problems they represent.

---

## Assumptions

In order to anonymize and fictionalize the data, the datasets use the columns `market_1`, `market_2`, and `market_3` to indicate three different city service areas.

The data lists five problem types:

| Code | Category |
|------|----------|
| Type_1 | Account management |
| Type_2 | Technician troubleshooting |
| Type_3 | Scheduling |
| Type_4 | Construction |
| Type_5 | Internet and wifi |

The dataset records repeat calls over seven-day periods. The initial contact date is listed as `contacts_n`. Subsequent call columns follow the format `contacts_n_[days since first call]`. For example, `contacts_n_6` indicates a call six days after first contact.

---

## Compliance and Privacy

The datasets are fictionalized versions of the actual data this team works with. Because of this, the data is already anonymized and approved. Stakeholders will need data access to all datasets so they can explore the steps taken.

---

## Accessibility

The dashboards should offer text alternatives including large print and text-to-speech options to support users with accessibility needs.

---

## Roll-out Plan

The stakeholders have requested a completed BI tool within **six weeks**.
