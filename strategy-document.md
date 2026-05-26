# Strategy Document: Google Fiber

**Proposer:** Emma Santiago, Hiring Manager  
**Status:** Draft

---

## Sign-off Matrix

| Name | Team / Role | Date |
|------|-------------|------|
| Ahmad Daniel | BI Analyst | 22/05/2026 |

---

## Datasets

**Primary dataset:** market_1, market_2, market_3  
**Secondary dataset:** N/A

---

## User Profiles

*Who is the intended audience for this dashboard? How do you expect them to use it?*

| Name | Role |
|------|------|
| Emma Santiago | Hiring Manager |
| Keith Portone | Project Manager |
| Minna Rah | Lead BI Analyst |
| Ian Ortega | BI Analyst |
| Sylvie Essa | BI Analyst |

---

## Dashboard Functionality

| Dashboard Feature | Request |
|-------------------|---------|
| **Reference dashboard** | Build a new dashboard to explore the number of repeat callers and their problem types in three different market cities. |
| **Access** | Read-only access provided to all user profiles listed in this document. |
| **Scope** | Fields include: `date`, `market`, `problem_type`, `contact_n`, `contact_n_#` |
| **Date filters and granularity** | Filters applicable for: Week, Month, Quarter. Granularity: Charts with detailed metrics should allow click-through to view specific underlying information. |

---

## Metrics and Charts

### Chart 1 — Repeat Calls by First Date

| Feature | Detail |
|---------|--------|
| **Chart title** | Repeat calls by first date |
| **Chart type** | Table |
| **Dimensions** | Day of initial call, subsequent repeat calls |
| **Metrics** | Contact count |

---

### Chart 2 — Market and Problem Type of First Repeat Calls

| Feature | Detail |
|---------|--------|
| **Chart title** | Market and Problem Type of First Repeat Calls |
| **Chart type** | Bar chart |
| **Dimensions** | Call type, market, contact_n_1 |
| **Metrics** | Contact count |

---

### Chart 3 — Calls by Market and Type

| Feature | Detail |
|---------|--------|
| **Chart title** | Calls by Market and Type |
| **Chart type** | Table |
| **Dimensions** | Market, call type, day |
| **Metrics** | Contact count |

---

### Chart 4 — Repeats by Week, Month, and Quarter

| Feature | Detail |
|---------|--------|
| **Chart title** | Repeats by Week, Month, and Quarter |
| **Chart type** | Bar chart |
| **Dimensions** | Date, contact |
| **Metrics** | Date |
