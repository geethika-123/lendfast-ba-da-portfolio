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
  (Signicat, 2025) — meaning nearly two in three users who start an
  application never finish it
- **70% of financial institutions** reported losing prospective clients
  due to slow or complex onboarding in 2025, up from 48% in 2023
  (Fenergo, 2025)
- Abandoned KYC processes alone strip **$3.3 billion annually** from
  the global banking sector (Fenergo, 2025)
- **73% of users abandon financial apps during onboarding** due to
  poor UX design (McKinsey, 2024)
- **38% of new customers leave mid-onboarding** if the process takes
  too long (Deloitte, 2025)
- Identity verification and document upload steps are the **single
  most common drop-off point** across fintech platforms (INSART, 2026)
- One fintech organisation discovered that **more than 60% of qualified
  borrowers** were abandoning applications before submission
  (The Office Gurus, 2025)
- Titan, a fintech platform, increased onboarding completion from
  **31% to 78%** after a UX redesign — proving the problem is solvable

---

## Company Background

**Company:** LendFast Financial Technologies Ltd.
**Sector:** Fintech — Digital Consumer Lending
**Product:** Mobile-first personal loan platform
**Launch date:** 18 months prior to this engagement
**Registered users:** 45,000
**Geographic market:** United States
**Regulatory environment:** Subject to federal lending regulations
(Truth in Lending Act, Equal Credit Opportunity Act), KYC/AML
requirements, and state-level lending licence obligations

LendFast offers fully digital personal loans ranging from $1,000 to
$50,000 with instant credit decisions and 24-hour fund disbursement
for approved applicants. The platform was built to compete with
incumbent banks on speed, convenience, and digital experience.

Monthly application starts have grown from 800 in Month 1 to
approximately 6,200 in Month 18. However, the volume of completed
applications has not grown proportionally, creating a widening gap
between acquisition investment and funded loan revenue.

---

## The Business Problem

### What the CEO Stated

In a project kickoff meeting, the CEO stated:

> "Our conversion rate is terrible. We're getting thousands of people
> starting loan applications every month but most of them drop off
> before completing. We think the application is too long. Can you
> look into this and tell us what we need to fix?"

### What This Actually Means

The CEO's statement contains one fact and one hypothesis.

**The fact:** A significant proportion of users who start the
application do not complete it.

**The hypothesis:** The cause is application length.

This hypothesis is unvalidated. Industry research suggests that
application abandonment in digital lending is driven by multiple
factors beyond length alone. A rigorous analysis is required to
determine which factors are driving abandonment at LendFast
specifically — and at which steps — before any recommendations
are made.

---

## The Application Flow

LendFast's current personal loan application consists of seven
sequential steps:

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
| CEO | Revenue growth — more completions = more funded loans |
| Sales & Marketing Head | Conversion rate justifies customer acquisition cost |
| Finance Head | Application completeness prevents fraud; regulatory adherence |
| Operations Head | Fewer incomplete applications = less manual follow-up |
| Compliance Officer | KYC, AML, and lending regulation — non-negotiable |
| Development Team | Clear scoped requirements — avoids rework and scope creep |
| End Users | Transparency, ease, speed, and trust in the platform |

---

## Hypotheses

All hypotheses were developed through structured problem framing
before any data was examined. They are ordered from primary to
secondary based on predicted confirmation likelihood.

### Primary Hypotheses

**Hypothesis 1 — Step 2 and 3 friction (information availability)**

I believe Steps 2 and 3 have higher drop-off rates than Steps 1
and 4 because those steps require specific details — such as
employer information and income figures — that users may not have
readily available during a mobile application session.

I will test this by calculating the drop-off rate at each
individual step and comparing Steps 2 and 3 against the overall
average drop-off rate across all steps. If Steps 2 and 3 exceed
the average by more than 10 percentage points, the hypothesis
is supported.

---

**Hypothesis 2 — Self-employed user friction**

I believe self-employed users have higher drop-off rates at
Steps 2 and 3 compared to employed users because certain fields
— such as employer name, employer contact, and fixed income range
— do not apply to self-employed applicants or require information
they cannot provide in a standard format.

I will test this by comparing the drop-off rate at Steps 2 and 3
between self-employed and employed users using the
employment_status field. If the self-employed drop-off rate at
either step exceeds the employed drop-off rate by more than 20
percentage points, the hypothesis is supported.

*Note: This hypothesis is tested after Hypothesis 1 is confirmed.
If Steps 2 and 3 do not show elevated overall drop-off, this
segmentation becomes less relevant.*

---

**Hypothesis 3 — Credit score fear at Step 5**

I believe users with poor or fair credit score bands have higher
drop-off rates at Step 5 than users with good or excellent bands
due to fear of credit score impact from a hard inquiry — even
when LendFast only conducts a soft pull at this stage.

I will test this by comparing Step 5 drop-off rates segmented by
credit_score_band. If poor and fair credit bands exceed good and
excellent bands by more than 15 percentage points at Step 5, the
hypothesis is supported.

---

**Hypothesis 4 — Document upload as primary drop-off point**

I believe Step 6 has the highest single-step drop-off rate across
all users because document upload requires users to have payslips
and bank statements immediately available and raises trust concerns
about sharing sensitive files with a new and unfamiliar platform.

I will test this by calculating the individual step drop-off rate
for all seven steps and identifying which step has the highest
rate. If Step 6 is the highest, the hypothesis is confirmed.

*Prediction: HIGH confidence this will be confirmed. Industry
research consistently identifies document upload as the primary
abandonment point in digital lending and fintech onboarding.*

---

**Hypothesis 5 — Mobile device friction**

I believe mobile users have a significantly higher drop-off rate
than desktop users, particularly at Steps 6 and 7, because
document upload and detailed form completion are more difficult
and time-consuming on small screens.

I will test this by comparing completion rates between mobile,
desktop, and tablet users using the device_type field. If mobile
completion rate is more than 15 percentage points below desktop
completion rate, the hypothesis is supported.

*Prediction: HIGH confidence this will be confirmed. Uploading
documents and filling detailed forms through a mobile interface
consumes significantly more time and creates more friction than
desktop equivalents.*

---

### Secondary Hypotheses
*(To be investigated during EDA — not primary drivers)*

**Hypothesis 6 — Loan amount and drop-off**

I believe users requesting higher loan amounts drop off at Step 4
at higher rates than users requesting smaller amounts due to fear
of rejection or uncertainty about interest rates and total
repayment costs for large amounts.

I will test this by segmenting drop-off rates at Step 4 across
loan_amount_requested value ranges and comparing against the
overall Step 4 drop-off rate.

---

**Hypothesis 7 — Seasonal variation**

I believe drop-off rates show quarterly variation due to external
economic conditions influencing applicant confidence and urgency.

I will test this by calculating completion rates by quarter using
application_start_date.

*Prediction: LOW confidence this will show meaningful signal.
LendFast has only 18 months of data — insufficient to distinguish
genuine seasonal patterns from the company's own marketing spend
changes or product updates during that period. Seasonal causation
cannot be confirmed from this dataset alone.*

---

**Hypothesis 8 — Time on application as friction signal**

I believe time spent on the application reveals two distinct
friction patterns. Users who abandon in under 10 minutes
encountered an early barrier — an unexpected field or trust
concern — and disengaged quickly. Users who spend over 30 minutes
without completing faced procedural friction — document
unavailability or confusion at a specific step.

I will test this by comparing average time_on_application_mins
between completers and non-completers, and by identifying users
below 10 minutes and above 30 minutes and checking which step
they reached before dropping off.

---

## Pre-Data Recommendations

These recommendations are formed before data analysis based on
structured problem framing and industry research. They will be
validated, refined, or revised once the data analysis is complete.

**Recommendation 1 — Pre-application document checklist**

Display a clear, specific checklist of all required documents
before Step 1 begins. Users should know before investing any time
that they will need payslips, bank statements, and photo ID
available for upload. This directly addresses the most common
cause of Step 6 abandonment — users reaching document upload
unprepared.

**Recommendation 2 — Trust signals at Step 6**

Add regulatory compliance badges, security certifications, and
licence verification displays at Step 6 specifically — the point
where trust concerns are highest. Users who have never used
LendFast before need visible evidence that the platform is
regulated and secure before uploading sensitive financial
documents. This is a low-cost, high-impact intervention.

**Recommendation 3 — Proactive support trigger**

Implement a proactive chat support trigger at Step 6 that
activates when a user pauses for more than 60 seconds. Reactive
support — where users call after abandoning — recovers very few
users. Proactive support in the moment addresses confusion and
document uncertainty before abandonment occurs.

---

## Success Definition

| Metric | Baseline | Target | Timeline |
|---|---|---|---|
| Overall application completion rate | TBD from data | 45–50% | 6 months |
| Step 6 drop-off rate | TBD from data | Below 30% | 6 months |
| Mobile completion rate | TBD from data | Within 10% of desktop | 6 months |
| Self-employed completion rate | TBD from data | Within 15% of employed | 6 months |

*Baseline values will be calculated during data analysis and
updated in this document before the BRD is finalised.*

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
| loan_approved | yes / no / null (if not completed) |
| time_on_application_mins | Total minutes spent on the application |

---

## References

- Fenergo (2025). KYC and Onboarding Abandonment Report.
- Signicat (2022). The Battle to Onboard — European Digital Finance.
- McKinsey & Company (2024). Fintech UX and Customer Acquisition.
- Deloitte (2025). Retail Banking Customer Onboarding Study.
- INSART (2026). The Anatomy of Trust in Fintech UX.
- Lorikeet CX (2026). AI Onboarding in Fintech — Industry Benchmarks.
- Fintactix (2025). Reducing Loan Application Abandonment.

---


*Prepared by: [Geethika]
*Project: LendFast Conversion Optimisation Engagement*
*Status: Approved for use as project foundation*
