# Course 1: Foundations of Business Intelligence
## Google Fiber — Call Center Repeat Call Dashboard

**Status:** ✅ Complete  
**Scenario:** Google Fiber  
**Deliverable type:** BI Project Planning Documents

---

## Overview

In this course, I completed the planning phase of a BI project for the Google Fiber call center team. This involved gathering stakeholder requirements, defining project scope and success criteria, and establishing a dashboard strategy — all before writing a single line of code or touching any data.

This phase is often underestimated by junior BI professionals, but it's where projects succeed or fail. Getting alignment on requirements upfront prevents costly rework later.

---

## Business Problem

The Google Fiber customer service call center wanted to understand **how often customers call back after their first inquiry**. If a customer has to call multiple times to resolve a single issue, it signals a failure in first-call resolution — which hurts both customer satisfaction and operational efficiency.

**Primary question to answer:**  
*How often are customers repeatedly contacting the customer service team, and which markets and problem types are driving the most repeat calls?*

---

## Stakeholders

| Name | Role |
|------|------|
| Emma Santiago | Hiring Manager (Client/Sponsor) |
| Keith Portone | Project Manager |
| Minna Rah | Lead BI Analyst |
| Ian Ortega | BI Analyst |
| Sylvie Essa | BI Analyst |

---

## Dataset Context

The data used in this project is a fictionalized, pre-anonymized version of actual Google Fiber call center data. Key structural details:

- **Markets:** `market_1`, `market_2`, `market_3` — three different city service areas
- **Problem types:**
  - `Type_1` — Account management
  - `Type_2` — Technician troubleshooting
  - `Type_3` — Scheduling
  - `Type_4` — Construction
  - `Type_5` — Internet and wifi
- **Call structure:** `contacts_n` = initial contact date; `contacts_n_6` = repeat call 6 days after first contact (7-day tracking window)

---

## Deliverables

| Document | Description |
|----------|-------------|
| [Stakeholder Requirements Document](documents/stakeholder-requirements.md) | Captures who the stakeholders are, what they need, and the primary business question |
| [Project Requirements Document](documents/project-requirements.md) | Defines purpose, dependencies, prioritized requirements, SMART success criteria, compliance, and roll-out plan |
| [Strategy Document](documents/strategy-document.md) | Establishes dashboard functionality, metrics, chart specifications, and stakeholder sign-off |

---

## Key Decisions Made

1. **Repeat call definition:** A repeat call is any contact by the same customer within a 7-day window of their initial call — this is based on the dataset's `contacts_n` column structure.
2. **Scope:** Three charts minimum — repeat calls by first contact date, by market and problem type, and by time period (week/month/quarter).
3. **Access:** Read-only for all listed stakeholders; no PII exposed (data is pre-anonymized).

---

## Reflection

The most important skill practiced in this course was **asking the right questions before starting**. In a real BI role, jumping straight to building a dashboard without documented requirements leads to misaligned deliverables and wasted time. The three planning documents here serve as a contract between the BI team and the stakeholders.

---

*Next: Course 2 — Data schema design and ETL pipeline*
