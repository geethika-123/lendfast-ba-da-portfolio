# LendFast — Case Brief
## BA + DA Portfolio Project | Fintech Digital Lending

---

## About This Document

This case brief establishes the business context, real-world grounding,
and analytical scope for the LendFast portfolio project. It is the
foundation document that all subsequent BA and DA deliverables reference.
Every problem statement, requirement, and recommendation in this project
traces back to this brief.

---

## Industry Context — Why This Problem Is Real

Digital lending application abandonment is not a fictional problem
invented for this case study. It is one of the most documented and
costly challenges in fintech.

**The scale of the problem:**

- The average fintech onboarding drop-off rate is **63%** globally
  (Signicat, 2025)
- **70% of financial institutions** reported losing prospective clients
  due to slow or complex onboarding in 2025, up from 48% in 2023
  (Fenergo, 2025)
- Abandoned KYC processes strip **$3.3 billion annually** from the
  global banking sector (Fenergo, 2025)
- **73% of users abandon financial apps during onboarding** due to
  poor UX design (McKinsey, 2024)
- **38% of new customers leave mid-onboarding** if the process takes
  too long (Deloitte, 2025)
- Identity verification and document upload are the **single most
  common drop-off point** across fintech platforms (INSART, 2026)
- Titan increased onboarding completion from **31% to 78%** after
  UX redesign — proving the problem is solvable

---

## Company Background

**Company:** LendFast Financial Technologies Ltd.
**Sector:** Fintech — Digital Consumer Lending
**Product:** Mobile-first personal loan platform
**Launch date:** 18 months prior to this engagement
**Registered users:** 45,000
**Geographic market:** United States
**Regulatory environment:** Truth in Lending Act, Equal Credit
Opportunity Act, KYC/AML requirements, state lending licences

LendFast offers fully digital personal loans from $1,000 to $50,000
with instant credit decisions and 24-hour disbursement. Monthly
application starts have grown from 800 in Month 1 to approximately
6,200 in Month 18. However, completed applications have not grown
proportionally — creating a widening gap between acquisition
investment and funded loan revenue.

---

## The Business Problem

### What the CEO Stated

> "Our conversion rate is terrible. We're getting thousands of people
> starting loan applications every month but most of them drop off
> before completing. We think the application is too long. Can you
> look into this and tell us what we need to fix?"

### What This Actually Means

The CEO's statement contains one fact and one hypothesis.

**The fact:** A significant proportion of users who start the
application do not complete it.

**The hypothesis:** The cause is application length — unvalidated.

Industry research suggests abandonment is driven by multiple factors.
A rigorous analysis is required before any recommendations are made.

---

## Business Objectives

Six objectives were developed through structured stakeholder analysis,
mapped to each primary stakeholder group.

**Objective 1 — Conversion and Revenue Growth** *(CEO)*
Increase the rate of loan application completion among registered
users to grow the revenue-generating customer base without additional
acquisition spend.

**Objective 2 — Operational Efficiency** *(Operations Head)*
Reduce operational cost and processing time associated with incomplete
applications by improving completion quality and reducing manual
follow-up requirements.

**Objective 3 — User Experience and Trust** *(End Users)*
Establish LendFast as a trusted and accessible digital lending
platform by delivering a transparent, intuitive, and frictionless
application experience that competes effectively with incumbent
financial institutions.

**Objective 4 — Regulatory Compliance** *(Compliance Officer)*
Ensure all application process improvements maintain full adherence
to KYC, AML, and federal lending obligations, protecting the company
from regulatory and reputational risk.

**Objective 5 — Marketing Intelligence** *(Sales and Marketing Head)*
Enable targeted and efficient allocation of marketing spend by
identifying user segments, acquisition channels, and device types
that produce the highest completion rates — informing where to
concentrate customer acquisition investment.

**Objective 6 — Financial Risk Protection** *(Finance Head)*
Ensure that application process improvements do not increase fraud
exposure, degrade applicant pipeline quality, or generate additional
downstream processing burden for Finance and Risk teams.

---

## The Application Flow

| Step | Name | Content | Risk Level |
|---|---|---|---|
| 1 | Personal Details | Name, address, date of birth | Low |
| 2 | Employment Information | Employer name, job title, start date | Medium |
| 3 | Income Verification | Monthly income, income source | Medium |
| 4 | Loan Amount and Purpose | Amount requested, loan purpose | Low |
| 5 | Credit Check Consent | Soft credit pull authorisation | High |
| 6 | Document Upload | Payslips, bank statements, ID | Very High |
| 7 | Review and Submit | Final summary before submission | Low |

---

## Stakeholder Map

| Stakeholder | Primary Interest |
|---|---|
| CEO | Revenue growth — completions = funded loans |
| Sales & Marketing Head | Conversion rate justifies CAC |
| Finance Head | Pipeline quality, fraud prevention, compliance |
| Operations Head | Fewer incomplete applications = less manual work |
| Compliance Officer | KYC, AML, lending regulation — non-negotiable |
| Development Team | Clear scoped requirements — no scope creep |
| End Users | Transparency, ease, speed, trust |

---

## Engagement Scope

### In Scope

- Analysis of the application completion funnel across all seven steps
- Identification of primary drop-off points and root causes
- Segmentation analysis by device type, credit score band,
  employment status, and loan amount
- Gap analysis between current completion rate and industry benchmark
- UX and process improvement requirements
- Targeted re-engagement of incomplete applicants based on
  segmentation findings
- Technical performance monitoring requirements

### Out of Scope

- New customer acquisition campaigns and marketing channel strategy
- Post-loan-approval operational and servicing processes
- Changes to loan approval criteria or credit risk model
- Changes to compliance frameworks or regulatory strategy
- Core infrastructure or platform architecture changes

---

## Hypotheses

All hypotheses were developed through structured problem framing
before any data was examined.

### Primary Hypotheses

**Hypothesis 1 — Step 2 and 3 friction**
I believe Steps 2 and 3 have higher drop-off rates than Steps 1
and 4 because those steps require specific details — employer
information and income figures — that users may not have readily
available during a mobile application session.
*Test: Compare drop-off rate at each step against overall average.
Confirmed if Steps 2 and 3 exceed average by more than 10
percentage points.*

**Hypothesis 2 — Self-employed user friction**
I believe self-employed users have higher drop-off rates at Steps
2 and 3 compared to employed users because fields like employer
name and fixed income range do not apply to their situation.
*Test: Compare drop-off rates at Steps 2 and 3 between
self-employed and employed users. Confirmed if self-employed
exceeds employed by more than 20 percentage points.*

**Hypothesis 3 — Credit score fear at Step 5**
I believe users with poor or fair credit score bands have higher
drop-off rates at Step 5 than users with good or excellent bands
due to fear of credit score impact from a hard inquiry.
*Test: Compare Step 5 drop-off rates by credit_score_band.
Confirmed if poor and fair bands exceed good and excellent by
more than 15 percentage points.*

**Hypothesis 4 — Document upload as primary drop-off**
I believe Step 6 has the highest single-step drop-off rate because
document upload requires files users may not have immediately
available and raises trust concerns about sharing sensitive data
with a new platform.
*Test: Compare individual step drop-off rates across all seven
steps. Confirmed if Step 6 has the highest rate.*
*Prediction: HIGH confidence — consistent with industry research.*

**Hypothesis 5 — Mobile device friction**
I believe mobile users have significantly higher drop-off rates
than desktop users, particularly at Steps 6 and 7, because
document upload and form completion are more difficult on
small screens.
*Test: Compare completion rates between mobile, desktop, and
tablet using device_type. Confirmed if mobile completion rate
is more than 15 percentage points below desktop.*
*Prediction: HIGH confidence.*

### Secondary Hypotheses

**Hypothesis 6 — Loan amount and drop-off**
I believe users requesting higher loan amounts drop off at Step 4
at higher rates due to fear of rejection or uncertainty about
interest rates and total repayment costs.
*Test: Segment drop-off rates at Step 4 by loan_amount_requested
value ranges.*

**Hypothesis 7 — Seasonal variation**
I believe drop-off rates show quarterly variation due to external
economic conditions influencing applicant confidence.
*Test: Calculate completion rates by quarter using
application_start_date.*
*Prediction: LOW confidence — only 18 months of data insufficient
to distinguish seasonal patterns from marketing spend changes.*

**Hypothesis 8 — Time on application as friction signal**
I believe users who abandon in under 10 minutes encountered an
early barrier while users spending over 30 minutes faced
procedural friction or document unavailability.
*Test: Compare average time_on_application_mins between
completers and non-completers. Identify users below 10 minutes
and above 30 minutes and check step reached.*

**Hypothesis 9 — Technical performance as abandonment cause**
I believe a measurable proportion of abandonment is caused by
technical failures — application errors, session timeouts, and
upload failures — rather than user choice. This cannot be
assessed from the current transactional dataset alone and
requires telemetry data for validation.
*Test: Analyse time_on_application_mins at technically complex
steps as a proxy indicator. Full validation requires error logs
and session recording data not currently available.*

---

## Pre-Data Recommendations

**Recommendation 1 — Pre-application document checklist**
Display a clear checklist of all required documents before Step 1
begins so users know what to prepare before investing time in
the application.

**Recommendation 2 — Trust signals at Step 6**
Add regulatory compliance badges, security certifications, and
licence verification at Step 6 where trust concerns are highest.

**Recommendation 3 — Proactive support trigger**
Implement a proactive chat support trigger at Step 6 that
activates when a user pauses for more than 60 seconds —
addressing confusion before abandonment occurs.

---

## Success Definition

| Metric | Baseline | Target | Timeline |
|---|---|---|---|
| Overall completion rate | TBD from data | 45–50% | 6 months |
| Step 6 drop-off rate | TBD from data | Below 30% | 6 months |
| Mobile completion rate | TBD from data | Within 10% of desktop | 6 months |
| Self-employed completion rate | TBD from data | Within 15% of employed | 6 months |

---

## Data Available for Analysis

| Field | Description |
|---|---|
| user_id | Unique applicant identifier |
| application_start_date | Date the application was initiated |
| step_reached | Furthest step completed (1–7) |
| loan_amount_requested | Requested loan value in USD |
| employment_status | employed / self-employed / unemployed / student |
| credit_score_band | poor / fair / good / excellent |
| device_type | mobile / desktop / tablet |
| application_completed | yes / no |
| loan_approved | yes / no / null |
| time_on_application_mins | Total minutes spent on application |

---

## Known Data Limitations

- No error logs or telemetry data available — technical failures
  cannot be distinguished from voluntary abandonment
- time_on_application_mins is ambiguous — long times may indicate
  friction or voluntary interruption
- 18 months of data is insufficient to confirm seasonal causation
- No acquisition channel data available — cannot link completion
  rates to specific marketing sources

---

## References

- Fenergo (2025). KYC and Onboarding Abandonment Report.
- Signicat (2022). The Battle to Onboard.
- McKinsey & Company (2024). Fintech UX and Customer Acquisition.
- Deloitte (2025). Retail Banking Customer Onboarding Study.
- INSART (2026). The Anatomy of Trust in Fintech UX.
- Fintactix (2025). Reducing Loan Application Abandonment.

---

*Document version: 3.0*
*Prepared by: [Geethika]*
*Project: LendFast Conversion Optimisation Engagement*
*Status: Foundation document — approved for project use*
