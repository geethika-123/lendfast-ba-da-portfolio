# Gap Analysis
## LendFast — Application Conversion Optimisation Engagement

---

| Field | Detail |
|---|---|
| Document Title | Gap Analysis |
| Project Name | LendFast Application Conversion Optimisation |
| Version | 0.1 — Draft |
| Status | In Progress |
| Prepared By | Geethika Vissapragada |
| Date | August 2026 |
| BRD Reference | BRD_lendfast.md |

---

## Document Control

| Version | Date | Author | Changes |
|---|---|---|---|
| 0.1 | August 2026 | Geethika Vissapragada | Initial draft — Introduction and Methodology |

---

## Table of Contents

1. Introduction
2. Methodology
3. Current State Assessment *(to be completed)*
4. Future State Definition *(to be completed)*
5. Gap Analysis
   - 5.1 Process Gap *(to be completed)*
   - 5.2 Product Gap *(to be completed)*
   - 5.3 Data Gap *(to be completed)*
   - 5.4 Capability Gap *(to be completed)*
6. Recommendations Summary *(to be completed)*
7. Prioritisation Matrix *(to be completed)*

---

## 1. Introduction

This gap analysis supports the LendFast Conversion Optimisation
engagement documented in the Business Requirements Document
(BRD_lendfast.md). It assesses the specific gaps between LendFast's
current application completion performance and the targets defined
in BRD Section 11, broken down across four dimensions — process,
product, data, and capability. Quantitative gap measurements marked
[X] will be updated following completion of the exploratory data
analysis phase.

---

## 2. Methodology

An extensive study of the fintech industry was conducted using
financial reports, publications, and research from McKinsey,
Deloitte, Fenergo, and Signicat to establish industry benchmarks
and identify common root causes of application abandonment in
digital lending platforms. All relevant stakeholders were mapped
and structured brainstorming sessions were conducted to generate
nine hypotheses identifying potential root causes of LendFast's
low conversion rates. Basic transactional data from LendFast's
application database was reviewed to understand funnel performance
at a step level. Granular telemetry data — including field-level
interactions, session recordings, and error logs — is not currently
captured at granular level and has been specified as a functional
requirement (FR-07) to enable deeper behavioural understanding of
customers in future iterations. Qualitative research through user
surveys and usability testing is planned following EDA completion
to validate quantitative findings with direct user feedback —
particularly around trust concerns at Step 6 and self-employed
user experience at Steps 2 and 3. Any workflow or process changes
outside of the application completion journey are not considered
within the scope of this analysis. The gap analysis is structured
across four dimensions — process, product, data, and capability —
to ensure gaps are identified at both operational and product levels.

---

*Sections 3–7 will be completed following exploratory data analysis.*
*Quantitative baselines will be established from EDA findings and
incorporated into each section before the document is finalised.*

---

*Document version: 0.1 — Draft*
*Prepared by: Geethika Vissapragada*
*Project: LendFast Conversion Optimisation Engagement*
*Status: In Progress*

---

## 3. Current State Assessment

### 3.1 Application Funnel Performance

*Quantitative baseline metrics will be populated following completion
of the exploratory data analysis phase. The structure below defines
the metrics to be measured and their industry benchmarks.*

| Metric | Current Value | Industry Benchmark | Source |
|---|---|---|---|
| Overall application completion rate | [X]% | ~37% | Signicat, 2025 |
| Industry abandonment rate benchmark | 63% | 63% | Signicat, 2025 |
| Step-level drop-off rates | [X]% per step | TBD | EDA output |
| Mobile vs desktop completion gap | [X]% | TBD | EDA output |
| Self-employed completion rate | [X]% | TBD | EDA output |
| Step 6 drop-off rate | [X]% | TBD | EDA output |
| Average time on application | [X] mins | TBD | EDA output |

*All [X] values to be replaced with actual figures from EDA.*

---

### 3.2 Stakeholder Pain Points

The current low conversion rate creates distinct pain points across
stakeholder groups that extend beyond the immediate revenue impact.

The CEO's primary concern in the current state is the widening gap
between user acquisition investment and funded loan revenue. With
45,000 registered users and a conversion rate of [X]% — significantly
below the 63% industry benchmark — the cost per funded loan has been
rising steadily while net revenue remains flat. This trajectory
directly undermines the growth expectations established at Series A
funding and creates pressure to demonstrate measurable improvement
before the next investor review.

The Finance Head is responsible for budget allocation across various
projects to effectively utilise existing capital funds until the next
funding round. The rising cost per funded loan is increasing the
pressure on already constrained margins, making it more difficult to
justify continued acquisition spend from the current capital base.
These low conversion rates are compressing profit margins and creating
a trajectory that is financially unsustainable without intervention.

The Operations Head faces a high volume of manual follow-up work
generated by incomplete applications. Each abandoned application that
reaches a certain completion threshold creates downstream processing
burden — operators must contact incomplete applicants, chase missing
documents, and manually update records. This interrupts the overall
operational workflow and extends loan processing times beyond the
24-hour disbursement target that LendFast promises customers.

The Sales and Marketing Head has no adequate justification for the
current level of customer acquisition spend given the conversion rate
it produces. With restricted budget and low conversion, extensive
targeted re-engagement campaigns cannot be launched unless revenue
improves significantly — creating a dependency loop where poor
conversion limits the marketing investment needed to address it.

Finally, end users are experiencing trust issues driven by the absence
of solid assurance of transparency and compliance throughout the
application. Users encounter no document checklist before starting,
no regulatory badges when sharing sensitive financial information, and
no proactive support when they struggle at complex steps. The result
is an application experience that feels opaque and untrustworthy
compared to established banking platforms.

---

### 3.3 Process Assessment

When a user registers on the LendFast platform and clicks on the loan
application, they are presented with the first step of the application
immediately, with no prior guidance on what information or documents
will be required throughout the process. This creates a fundamental
information asymmetry — users commit time to the application without
knowing what lies ahead, and encounter unexpected requirements at later
steps with no way to prepare.

Steps 2 and 3 — employment information and income verification — are
designed for a standard salaried employment model. Self-employed users,
freelancers, and those with variable income encounter fields that do
not reflect their situation: fixed employer name, standard monthly
income fields, and employment start date requirements that assume
continuous traditional employment. There is no alternative pathway or
field adaptation for non-standard employment types, creating a process
that effectively excludes a significant user segment at these steps.
Additionally, users may not have specific employment details or income
documentation immediately available during a mobile session, causing
abandonment not due to unwillingness but due to information
unavailability.

Step 5 — credit check consent — creates specific anxiety because the
platform does not proactively communicate that only a soft credit pull
will be conducted. Users familiar with hard credit inquiries, which
negatively impact credit scores and remain visible to future lenders,
may hesitate or abandon at this step out of concern. Without a clear
transparency message before the consent checkbox, users are left to
assume the worst-case scenario.

Step 6 — document upload — compounds trust issues with technical
friction. Users are asked to upload sensitive financial documents to a
platform they may have encountered for the first time, with no visible
regulatory compliance badges or licence verification displayed at the
moment of maximum trust sensitivity. No upload progress indicator is
shown, leaving users uncertain whether their upload is processing or
has failed silently. When an upload fails, no clear error message or
recovery path is presented. The combination of trust deficit and
technical opacity at this step makes it the highest-risk abandonment
point in the application.

No application progress indicator is displayed across any step,
leaving users unable to gauge how much of the process remains. This
is particularly damaging in scenarios involving device interruption,
browser crashes, or mobile session timeouts — where users who return
to the application have no clear reference point for where they left
off. Mobile users face additional friction as the interface lacks
device-specific optimisations, making form completion and document
upload significantly more time-consuming than on desktop.

---

### 3.4 Benchmark Comparison

| Dimension | LendFast Current State | Industry Benchmark | Gap |
|---|---|---|---|
| Application completion rate | [X]% | ~37% | [X]pp below benchmark |
| Abandonment rate | [X]% | 63% global average | TBD from EDA |
| Document upload abandonment | [X]% | Highest single step across fintech (INSART, 2026) | TBD |
| Mobile completion vs desktop | [X]% gap | Significant gap typical across fintech | TBD |
| Re-engagement rate | Not implemented | 15–25% industry average | Full gap |
| Proactive support | Not implemented | Standard in leading platforms | Full gap |
| Pre-application checklist | Not implemented | Standard in leading platforms | Full gap |

*Benchmark gaps marked TBD will be quantified following EDA completion.*

---

## 4. Future State Definition

The future state defines where LendFast must be within six months of
full implementation. Each target is specific, measurable, and tied to
a business objective defined in the BRD.

### 4.1 Application Performance Targets

| Metric | Future State Target | Business Objective |
|---|---|---|
| Overall completion rate | 45–50% | Objective 1 — Conversion and Revenue Growth |
| Step 6 drop-off rate | Below 30% | Objective 3 — User Experience and Trust |
| Mobile completion rate | Within 10% of desktop rate | Objective 3 — User Experience and Trust |
| Self-employed completion rate | Within 15% of employed rate | Objective 3 — User Experience and Trust |
| Manual follow-up rate | Below 10% of completed applications | Objective 2 — Operational Efficiency |
| Average processing time | Under 24 hours | Objective 2 — Operational Efficiency |

### 4.2 Capability Targets

| Capability | Current State | Future State |
|---|---|---|
| Pre-application guidance | None | Document checklist displayed before Step 1 |
| Trust signals | None at Step 6 | Regulatory badges and licence verification displayed |
| Proactive support | None | Chat trigger after 60 seconds inactivity at any step |
| Credit check transparency | None | Explicit soft pull message before consent checkbox |
| Session persistence | None confirmed | Automatic progress save on session interruption |
| Telemetry capture | Basic transactional data only | Full event logging with timestamps (FR-07) |
| Self-employed pathway | None | Adaptive fields triggered by employment status |
| Re-engagement | None | Automated notification within 24 hours of abandonment |

### 4.3 Success Definition

The future state is considered achieved when all four acceptance
criteria defined in BRD Section 13 are met — specifically when all
High priority confirmed functional requirements are implemented,
KPI targets are verified by their respective owners, zero compliance
violations are identified, and the CEO and Compliance Officer provide
formal sign-off on delivery.

---

*Sections 5 through 7 — Gap Analysis by Dimension, Recommendations
Summary, and Prioritisation Matrix — will be completed following
exploratory data analysis. Quantitative gaps and recommendation
priorities depend on EDA findings confirming or rejecting the nine
hypotheses documented in the case brief.*

---

*Document version: 0.2 — Sections 1–4 complete*
*Prepared by: Geethika Vissapragada*
*Project: LendFast Conversion Optimisation Engagement*
*Status: In Progress — awaiting EDA for Sections 5–7*
