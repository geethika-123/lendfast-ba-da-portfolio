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
| Overall application completion rate | 18.2% | ~37% | Signicat, 2025 |
| Industry abandonment rate benchmark | 63% | 63% | Signicat, 2025 |
| Step-level drop-off rates | Step 6: 66.8%, Step 2: 16.5%, Step 3: 14.7%, Step 5: 12.2% | Step 6 below 30% | EDA output |
| Mobile vs desktop completion gap | 16.9pp (mobile 12.1% vs desktop 29.0%) | Within 10pp | EDA output |
| Self-employed completion rate | 12.8% vs employed 19.6% | Within 15pp of employed | EDA output |
| Step 6 drop-off rate | 66.8% | Below 30% | EDA output |
| Average time on application | 19.2 mins (completers: 21.4, abandoned: 18.7) | Under 30 mins | EDA output |

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
| Application completion rate | 18.2% | ~37% | 18.8pp below benchmark |
| Abandonment rate | 81.8% | 63% global average | 18.8pp above benchmark |
| Document upload abandonment | 66.8% at Step 6 | Below 30% | 36.8pp above target |
| Mobile completion vs desktop | 16.9pp gap (12.1% vs 29.0%) | Within 10pp | 6.9pp above target gap |
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
| Overall completion rate | 18.2% → 45–50% | Objective 1 — Conversion and Revenue Growth |
| Step 6 drop-off rate | 66.8% → Below 30% | Objective 3 — User Experience and Trust |
| Mobile completion rate | 12.1% → Within 10pp of desktop | Objective 3 — User Experience and Trust |
| Self-employed completion rate | 12.8% → Within 15pp of employed | Objective 3 — User Experience and Trust |
| Manual follow-up rate | TBD from operations | Below 10% | Objective 2 — Operational Efficiency |
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

---

## 5. Gap Analysis by Dimension

The following gap analysis breaks down the difference between
LendFast's current state and the defined future state across four
dimensions — process, product, data, and capability. Each gap is
traced to specific EDA findings and mapped to the functional
requirements defined in the BRD.

**Baseline metrics established from EDA:**

| Metric | Current State | Future State Target | Gap |
|---|---|---|---|
| Overall completion rate | 18.2% | 45–50% | 26.8–31.8pp below target |
| Industry benchmark gap | 18.8pp below | At benchmark | 18.8pp to close |
| Step 6 drop-off rate | 66.8% | Below 30% | 36.8pp above target |
| Mobile completion rate | 12.1% | Within 10pp of desktop | 16.9pp gap |
| Self-employed completion | 12.8% | Within 15pp of employed | 6.8pp gap |
| Step 5 poor credit drop-off | 28.6% | Below 15% | 13.6pp above target |

---

### 5.1 Process Gap

The process gap represents failures in how the seven-step application
is designed and sequenced — independent of the technology that
delivers it.

**Gap P1 — No pre-application guidance**

Current state: Users are presented with Step 1 immediately upon
clicking the loan application button with no prior indication of
what information or documents will be required. Users encounter
document upload requirements for the first time at Step 6 — after
investing time completing five preceding steps.

Future state: Users receive a complete document checklist before
Step 1 begins, enabling them to prepare required documents in advance
and make an informed decision about whether to start the application.

Evidence: Step 6 drop-off of 66.8% — the highest of any step — is
consistent with users being unprepared for document upload
requirements. The absence of pre-application guidance is the most
likely process cause.

Gap: Pre-application guidance does not exist. Full gap.
BRD Reference: FR-01 — Pre-application document checklist.

---

**Gap P2 — No alternative pathway for self-employed users**

Current state: Steps 2 and 3 are designed exclusively for salaried
employment. Fields require employer name, job title, employment start
date, and fixed monthly income — none of which apply to self-employed
applicants with variable income and no formal employer.

Future state: Self-employed users encounter an adaptive pathway at
Steps 2 and 3 with fields appropriate to their employment situation —
business name, income range, income source type, and supporting
documentation guidance for variable income.

Evidence: Self-employed users abandon at Step 2 at 32.6% versus
9.8% for employed users — a 22.8 percentage point gap exceeding the
20pp confirmation threshold. H2 confirmed.

Gap: Self-employed pathway does not exist. Full gap.
BRD Reference: FR-08 — Self-employed user pathway (elevated to
confirmed high priority from EDA findings).

---

**Gap P3 — No session progress save**

Current state: If a user's session ends unexpectedly — browser crash,
device shutdown, network failure — all entered information is lost.
Returning users must restart the application from Step 1.

Future state: Application progress is automatically saved at each
step. Returning users resume from the last completed step without
re-entering information.

Evidence: 302 users across the dataset have multiple application
attempts — 15.7% of unique users started more than one application.
Without session save, each restart represents a complete restart
from Step 1, compounding abandonment across attempts.

Gap: Session progress save does not exist in the UI. Full gap.
BRD Reference: FR-03 — Session progress save.

---

### 5.2 Product Gap

The product gap represents features and trust signals that the
current application lacks — things the platform should provide to
users but currently does not.

**Gap PR1 — No credit check transparency at Step 5**

Current state: Step 5 presents a credit check consent checkbox
without explaining the nature of the credit check. Users familiar
with hard credit inquiries — which negatively impact credit scores
and remain visible to future lenders — may assume a hard pull is
conducted and abandon rather than risk score damage.

Future state: A clear message appears before the consent checkbox
stating explicitly that only a soft credit pull is conducted and
the user's credit score will not be affected.

Evidence: Poor credit users abandon at Step 5 at 28.6% versus
5.9% for good credit users — a 22.7pp gap. Fair credit users at
18.9% also show elevated abandonment. H3 partially confirmed.
The differential by credit band is consistent with credit anxiety
as the mechanism — users with lower scores have more reason to fear
credit check consequences.

Gap: Credit check transparency message does not exist. Full gap.
BRD Reference: FR-04 — Credit check transparency message.

---

**Gap PR2 — No trust signals at Step 6**

Current state: Step 6 asks users to upload sensitive financial
documents — payslips, bank statements, and government-issued ID —
to a platform they may have encountered for the first time, with
no visible regulatory compliance badges, security certifications,
or licence verification displayed at the point of maximum trust
sensitivity.

Future state: Regulatory compliance badges, security certifications,
and licence verification are prominently displayed at Step 6 before
the upload button is accessible, providing users with visible
evidence that the platform is regulated and their data is protected.

Evidence: Step 6 drop-off of 66.8% — concentrated at the exact
point where trust is most critical. Mobile Step 6 drop-off of
approximately 77% suggests that mobile users, who cannot easily
research the platform while on the application screen, are
particularly affected by the absence of trust signals.

Gap: Compliance and trust signals do not exist at Step 6. Full gap.
BRD Reference: FR-05 — Compliance and licence badges at Step 6.

---

**Gap PR3 — No proactive support at friction points**

Current state: No support mechanism activates when a user pauses
or struggles at any application step. Users who encounter confusion
or uncertainty must either find a contact method themselves or
abandon. The only support available is reactive — after abandonment
has already occurred.

Future state: A proactive chat support trigger activates
automatically when a user pauses for more than 60 seconds at any
step, offering immediate assistance before abandonment occurs.

Evidence: Step 6 66.8% drop-off and Step 2 16.5% drop-off both
represent high-friction points where real-time support would have
the highest intervention value. 302 users with multiple attempts
demonstrate that abandonment is not always a permanent decision —
proactive support at the moment of hesitation could convert
abandonments into completions.

Gap: Proactive support does not exist. Full gap.
BRD Reference: FR-06 — Proactive chat support trigger.

---

**Gap PR4 — No document upload validation or feedback**

Current state: When a user uploads a document at Step 6, no upload
progress indicator is displayed. If the upload fails — wrong file
format, file too large, network timeout — no clear error message
or recovery path is provided. Users cannot confirm whether their
upload succeeded without proceeding to the next screen.

Future state: The system displays upload progress, confirms
successful upload, and provides specific error messages with
actionable recovery steps when upload fails.

Evidence: Step 6 mobile drop-off of approximately 77% is
significantly higher than desktop at 51%. Document upload on
mobile is inherently more friction-prone — files may be harder
to locate, upload speeds may be slower, and error recovery without
clear guidance is more difficult on a small screen.

Gap: Document upload validation and feedback does not exist.
Full gap.
BRD Reference: FR-02 — Document upload validation and error
messaging.

---

### 5.3 Data Gap

The data gap represents information LendFast currently does not
capture that is required for ongoing analysis, performance
monitoring, and future optimisation.

**Gap D1 — No granular telemetry data**

Current state: LendFast captures basic transactional data —
application start, step reached, completion status, and demographic
fields. No granular event-level data is captured — field-level
interactions, page load times, upload attempt counts, error
occurrences, or session recordings.

Future state: All user events are logged with timestamps —
step completions, field interactions, page load events, upload
attempts, errors, and session timeouts. This data enables
identification of specific technical friction points and
distinguishes voluntary abandonment from technically forced
abandonment.

Evidence: H9 (technical performance as abandonment cause) cannot
be assessed from the current dataset. The ambiguity in
time_on_application_mins — which could reflect friction or
voluntary pausing — cannot be resolved without event-level data.

Gap: Granular telemetry infrastructure does not exist. Full gap.
BRD Reference: FR-07 — Telemetry data capture.

---

**Gap D2 — Insufficient historical data for seasonal analysis**

Current state: 18 months of application data — six quarters —
is available for analysis. This is insufficient to identify
genuine seasonal patterns and distinguish them from random
variation or LendFast's own marketing spend changes during
the growth period.

Future state: Minimum 36 months of data enables reliable seasonal
analysis. Quarterly completion rate patterns can be compared
across two full annual cycles to confirm or reject seasonal
effects.

Evidence: H7 inconclusive — quarterly completion rates ranged
from 16.3% to 21.2% with no identifiable pattern across six
quarters. The 2023Q3-Q4 peak cannot be confirmed as seasonal
without a second annual cycle for comparison.

Gap: Partial gap — data exists but volume is insufficient for
seasonal analysis. Gap closes naturally over time.
BRD Reference: Monitoring requirement — no specific FR. Recommend
re-analysis at 36-month mark.

---

**Gap D3 — No re-engagement tracking infrastructure**

Current state: When a user abandons the application, no system
exists to track that abandonment, segment the user by drop-off
point, or trigger a re-engagement communication. The 302 returning
users in the dataset restarted organically — not through any
systematic re-engagement effort.

Future state: Abandoned applications trigger an automated
re-engagement notification within 24 hours, segmented by
drop-off step and user type. Re-engagement conversion rates
are tracked and optimised over time.

Evidence: 302 users with multiple application attempts —
15.7% of unique users — demonstrate willingness to return.
A systematic re-engagement capability would convert more of
these voluntary returners and potentially recover users who
abandoned without returning organically.

Gap: Re-engagement infrastructure does not exist. Full gap.
BRD Reference: FR-09 — Incomplete applicant re-engagement
notification.

---

### 5.4 Capability Gap

The capability gap represents organisational capabilities LendFast
currently lacks to implement and sustain the recommended changes.

**Gap C1 — No segmentation-based marketing capability**

Current state: LendFast's marketing spend is not segmented by
application drop-off behaviour, device type, or employment status.
The 302 returning users who restarted organically represent an
untapped re-engagement opportunity that is not being systematically
exploited. Marketing budget is allocated to new user acquisition
without optimisation based on which segments convert at higher rates.

Future state: EDA findings enable targeted marketing — mobile
users who dropped at Step 6 receive trust-focused messaging,
self-employed users receive documentation guidance, poor credit
users receive transparency messaging about the soft pull process.
Marketing spend is allocated toward segments and channels that
produce the highest completion rates.

Evidence: Device type segmentation confirms mobile users complete
at 12.1% versus desktop at 29.0%. Employment status segmentation
confirms self-employed users complete at 12.8% versus employed
at 19.6%. These segment-level completion rate differences enable
precision targeting that does not currently exist.

Gap: Segmentation-based marketing capability does not exist.
Full gap — requires both the FR-09 infrastructure and the
analytical findings from this EDA to implement.
BRD Reference: FR-09, KPI-05 — Re-engagement conversion rate.

---

**Gap C2 — No fraud exposure baseline**

Current state: No baseline measurement of fraudulent application
rate exists prior to implementing process changes. Without a
pre-implementation baseline, it will be impossible to determine
whether recommended UX simplifications increase fraud exposure
after implementation.

Future state: A fraud detection baseline is established before
any process changes are implemented. Post-implementation fraud
rates are compared against baseline to confirm that conversion
improvements have not compromised pipeline quality.

Evidence: BRD Risk R-05 identifies compliance conflicts as a
medium-rated risk. Without a fraud baseline, the Finance Head
cannot assess whether FR-01 (document checklist) or FR-08
(self-employed pathway) changes the fraud profile of completed
applications.

Gap: Fraud baseline measurement capability does not exist.
Partial gap — fraud data likely exists in loan servicing systems
but has not been integrated into this analysis.
BRD Reference: KPI-06 — Fraud and financial risk metrics.


---

## 6. Recommendations Summary

Recommendations are ordered by priority — determined by the number
of users affected, the strength of EDA confirmation, and
implementation complexity. All recommendations are traced to
confirmed EDA findings and mapped to functional requirements
defined in the BRD.

---

### Tier 1 — Implement Immediately
*Highest user impact. Directly confirmed by EDA. Low to medium
implementation complexity.*

---

**R1: Add a Pre-Application Document Checklist**
*FR-01 | Step 6 | 894 users lost | H4 Confirmed*

Before a user starts the application, display a clear checklist
of every document they will need — payslips, bank statements, and
photo ID. The Start Application button should only become accessible
after the user acknowledges the checklist.

Why it matters: 894 users — 38% of all application starters —
abandon at Step 6 document upload. The most likely cause is users
arriving at Step 6 unprepared, having invested time in five
preceding steps without knowing documents would be required.
A checklist at the start eliminates this surprise entirely at
near-zero implementation cost.

Expected impact: Reduction in Step 6 drop-off rate from 66.8%
toward the 30% target by ensuring users who start the application
are prepared to complete it.

---

**R2: Show Upload Progress and Clear Error Messages at Step 6**
*FR-02 | Step 6 | 894 users lost | H4 and H5 Confirmed*

When a user uploads a document, show a progress bar while the
upload processes and display a clear confirmation when it succeeds.
If the upload fails, tell the user exactly why — wrong file format,
file too large, network timeout — and give them specific steps to
fix it and try again.

Why it matters: Mobile users drop off at Step 6 at approximately
77% — 26 percentage points higher than desktop users at 51%.
Document upload on mobile is inherently more friction-prone.
Without upload feedback, users cannot confirm whether their upload
worked, creating uncertainty that drives abandonment — particularly
on mobile where retrying is more difficult.

Expected impact: Reduction in mobile Step 6 drop-off through
improved upload transparency and error recovery. Contributes to
closing the 16.9pp mobile vs desktop completion gap.

---

**R3: Display Regulatory Badges and Licence Verification at Step 6**
*FR-05 | Step 6 | 894 users lost | H4 Confirmed*

At Step 6, before the upload button is accessible, prominently
display LendFast's regulatory compliance certifications,
government-approved lending licence, and data security standards.
Users should see clear evidence that the platform is regulated
and their documents are protected before uploading sensitive
financial information.

Why it matters: Step 6 asks users to upload payslips, bank
statements, and government ID to a platform they may have
encountered for the first time. Without visible trust signals,
users have no basis for confidence that their sensitive data is
safe. This is a low-cost intervention — trust badges require no
backend changes — with direct impact on the highest drop-off point
in the funnel.

Expected impact: Reduction in Step 6 drop-off through increased
user confidence at the moment of maximum trust sensitivity.

---

**R4: Trigger Proactive Chat Support When Users Pause**
*FR-06 | All steps | H4 and H1 Confirmed*

When a user pauses for more than 60 seconds at any application
step, automatically display a chat support prompt offering
assistance. The prompt should be specific to the step the user
is on — not a generic help message. A help button should also
be visible at all times so users can initiate support on demand.

Why it matters: 894 users abandon at Step 6 and 647 users abandon
at Steps 2 and 3. Users who pause at these high-friction steps
are signalling hesitation — not necessarily a decision to leave.
Proactive support at the moment of hesitation intercepts abandonment
before it occurs. Reactive support — available only after a user
has already left — recovers very few users.

Expected impact: Conversion of a measurable proportion of
hesitation-driven abandonments into completions at Steps 2, 3,
and 6 — the three highest drop-off points in the funnel.

---

**R5: Create a Separate Application Pathway for Self-Employed Users**
*FR-08 | Steps 2 and 3 | 647 users lost | H2 Confirmed — 22.8pp gap*

When a user selects self-employed as their employment status,
automatically show fields relevant to self-employment — business
name, income type, income range — instead of standard employer
name, job title, and fixed salary fields. Provide guidance on
what documentation self-employed users can use to verify income
when standard payslips are not available.

Why it matters: Self-employed users abandon at Step 2 at 32.6%
versus 9.8% for employed users — a 22.8 percentage point gap
confirmed by EDA. 537 self-employed users attempted the
application. Their completion rate of 12.8% is the lowest of
any employment group — lower than even unemployed users (20.0%)
who face similar field friction. The current application is
built for salaried employment and effectively excludes a
significant and growing user segment.

Expected impact: Reduction in self-employed drop-off at Steps
2 and 3 toward the employed user baseline, recovering an
estimated 120+ additional completions from the self-employed
segment alone.

---

### Tier 2 — Implement After Tier 1
*Confirmed by EDA. Lower user volume than Tier 1 but
high-confidence finding.*

---

**R6: Display a Clear Soft Credit Check Message at Step 5**
*FR-04 | Step 5 | 186 users lost | H3 Partially Confirmed*

Before the credit check consent checkbox at Step 5, display a
clear message stating that LendFast conducts only a soft credit
pull — meaning the user's credit score will not be affected and
the check will not appear on their credit file. The message should
be specific and reassuring, not buried in terms and conditions.

Why it matters: Poor credit users abandon at Step 5 at 28.6%
versus 5.9% for good credit users — a 22.7 percentage point gap.
Fair credit users abandon at 18.9%. Users with lower credit scores
have experienced hard credit checks before and know the
consequences. Without a clear explanation that LendFast uses only
a soft pull, these users reasonably assume the worst and abandon
rather than risk credit score damage. This is a text change —
one of the lowest-cost interventions in the entire recommendation
set.

Expected impact: Reduction in Step 5 drop-off among poor and
fair credit users by addressing a specific, identifiable
psychological barrier with accurate information.

---

### Tier 3 — Infrastructure
*Does not directly address a specific drop-off point but enables
all other recommendations and ongoing improvement.*

---

**R7: Automatically Save Application Progress**
*FR-03 | All steps | 302 returning users identified*

Automatically save a user's progress at each step so that if
their session ends — browser crash, device shutdown, network
failure — they can resume from where they left off when they
return. The saved state should persist for a minimum of 30 days.

Why it matters: 302 users in the dataset started more than one
application — 15.7% of unique users. These returning users
represent demonstrated intent. Without session save, every
return requires a full restart from Step 1 — compounding
abandonment across attempts. Session save converts restarts into
continuations.

Expected impact: Reduction in multi-attempt abandonment. Improved
experience for the 15.7% of users who return after abandonment.

---

**R8: Implement Comprehensive Event Logging and Telemetry**
*FR-07 | All steps | H9 Cannot Be Assessed Without This*

Log every user event throughout the application — step
completions, field interactions, page load times, upload attempts,
errors, and session timeouts — with precise timestamps and user
identifiers. Store this data in a queryable format accessible
to the analytics team.

Why it matters: H9 (technical performance as abandonment cause)
cannot be assessed from the current transactional dataset.
Without event-level telemetry, the team cannot distinguish
friction-driven abandonment from technical failure, cannot
identify specific fields causing hesitation, and cannot measure
the effectiveness of implemented recommendations with precision.
Telemetry is the data infrastructure that makes all future
analysis more powerful.

Expected impact: Enables validation of H9, supports ongoing
optimisation of all Tier 1 and Tier 2 interventions, and
provides the event-level data required for a complete
understanding of user behaviour throughout the funnel.

---

### Tier 4 — Provisional
*Pending further validation or dependent on Tier 3 infrastructure.*

---

**R9: Send Targeted Re-Engagement Notifications to Incomplete Applicants**
*FR-09 | All steps | Provisional — pending segmentation infrastructure*

Within 24 hours of abandonment, automatically send a personalised
re-engagement notification to users who started but did not
complete an application. The message should be tailored to the
step at which the user abandoned — a user who stopped at Step 6
should receive a different message than one who stopped at Step 2.

Why it matters: 302 users in the dataset returned organically
without any re-engagement prompt. A systematic re-engagement
capability would recover additional users who abandoned without
returning on their own — converting warm leads at zero acquisition
cost. This recommendation requires the telemetry infrastructure
from R8 to implement effectively.

Expected impact: Recovery of a measurable proportion of
abandoned applications through targeted re-engagement. Industry
re-engagement conversion rates for digital lending average
15–25% of contacted users.

---

**R10: Add a Progress Indicator Showing Steps Completed**
*FR-10 | All steps | Provisional — pending mobile drop-off confirmation*

Display a progress indicator throughout the application showing
the user's current step and total steps remaining. The indicator
should be visible on all device types and update in real time
as the user progresses.

Why it matters: Users who cannot see how much of the application
remains may abandon due to uncertainty about time commitment —
particularly on mobile where the application feels longer due to
the additional friction of smaller screens and slower uploads.
A progress indicator sets clear expectations and reduces
abandonment driven by uncertainty rather than genuine objection.

Expected impact: Marginal reduction in abandonment across all
steps through improved expectation management. Particularly
relevant for mobile users where application length perception
is most distorted.


---

## 7. Prioritisation Matrix

Recommendations are scored across three dimensions to produce a
priority ranking that balances user impact, evidence strength,
and implementation effort.

---

### Scoring Methodology

**Impact Score (1–5) — based on users lost from EDA:**

| Users Lost | Score |
|---|---|
| 800+ | 5 |
| 500–799 | 4 |
| 300–499 | 3 |
| 100–299 | 2 |
| Under 100 or infrastructure | 1 |

**Evidence Strength (0.4–0.9) — based on EDA confirmation status:**

| Evidence Type | Score |
|---|---|
| Directly confirmed by EDA — gap exceeds pre-defined threshold | 0.9 |
| Partially confirmed — pattern exists but below threshold | 0.7 |
| Pre-data recommendation supported by industry research | 0.6 |
| Provisional — insufficient data or dependent on infrastructure | 0.4 |

**Effort Score (1–4) — based on estimated implementation weeks:**

| Implementation Weeks | Score |
|---|---|
| 1 week | 1 |
| 2–3 weeks | 2 |
| 3–4 weeks | 3 |
| 4–6 weeks | 4 |

**Priority Score = (Impact × Evidence Strength) / Effort**

Higher score = implement first.

---

### Scoring Table

| FR | Recommendation | Users Lost | Impact | Evidence Strength | Effort (weeks) | Effort Score | Priority Score |
|---|---|---|---|---|---|---|---|
| FR-01 | Pre-application document checklist | 894 | 5 | 0.6 | 1–2 | 1 | 3.00 |
| FR-05 | Compliance badges at Step 6 | 894 | 5 | 0.6 | 1 | 1 | 3.00 |
| FR-02 | Document upload validation | 894 | 5 | 0.6 | 2–3 | 2 | 1.50 |
| FR-04 | Credit check transparency message | 186 | 2 | 0.7 | 1 | 1 | 1.40 |
| FR-06 | Proactive chat support trigger | 1,541 | 5 | 0.6 | 3–4 | 3 | 1.00 |
| FR-08 | Self-employed user pathway | 647 | 4 | 0.9 | 4–6 | 4 | 0.90 |
| FR-03 | Session progress save | 302 | 2 | 0.6 | 3–4 | 3 | 0.40 |
| FR-10 | Application progress indicator | N/A | 1 | 0.4 | 1–2 | 1 | 0.40 |
| FR-09 | Re-engagement notifications | 480 | 3 | 0.4 | 4–6 | 4 | 0.30 |
| FR-07 | Telemetry data capture | N/A | 1 | 0.9 | 4–6 | 4 | 0.23 |

---

### Priority Quadrant — Impact vs Effort

```
HIGH        │ FR-01  FR-05      │ FR-06  FR-08      │
IMPACT      │ (Quick Wins)      │ (Strategic Bets)  │
            │ FR-02  FR-04      │                   │
            │───────────────────│───────────────────│
LOW         │ FR-10             │ FR-03  FR-07      │
IMPACT      │ (Fill-ins)        │ FR-09             │
            │                   │ (Deprioritise)    │
            └───────────────────┴───────────────────┘
                  LOW EFFORT          HIGH EFFORT
```

**Quick Wins (High Impact, Low Effort):**
FR-01, FR-02, FR-04, FR-05 — UI additions and text changes that
directly address the highest drop-off points. Implement in Sprint 1.

**Strategic Bets (High Impact, High Effort):**
FR-06, FR-08 — High confirmed impact but require significant
development investment. Plan carefully, implement in Sprint 2–3.

**Fill-ins (Low Impact, Low Effort):**
FR-10 — Simple UI addition with marginal impact. Implement
opportunistically when development capacity allows.

**Deprioritise (Low Impact, High Effort):**
FR-03, FR-07, FR-09 — Infrastructure requirements. Essential
for long-term capability but do not directly recover users in
the short term. Plan as a separate infrastructure workstream.

---

### Implementation Roadmap

| Sprint | Recommendations | Expected Outcome |
|---|---|---|
| Sprint 1 (Weeks 1–3) | FR-01, FR-04, FR-05 | Address Step 6 trust and Step 5 anxiety — lowest effort, highest evidence strength |
| Sprint 2 (Weeks 3–6) | FR-02, FR-06 | Add upload validation and proactive chat — medium effort, high Step 6 impact |
| Sprint 3 (Weeks 6–10) | FR-08 | Self-employed pathway — confirmed H2, highest evidence strength of all recommendations |
| Sprint 4 (Weeks 10–14) | FR-03, FR-07 | Infrastructure — session save and telemetry — enables ongoing optimisation |
| Sprint 5 (Weeks 14–18) | FR-09, FR-10 | Provisional requirements — re-engagement and progress indicator |

---

### Important Limitation

Evidence strength scores are based on EDA confirmation against
pre-defined thresholds — not formal statistical significance
testing. A production prioritisation exercise would supplement
these scores with chi-square tests and confidence intervals on
segment-level completion rate differences, particularly for
smaller segments such as students (n=91) where sample size
may limit the reliability of observed patterns.

FR-08 (self-employed pathway) ranks sixth by priority score
despite having the highest evidence strength (0.9) due to
its high implementation effort (4–6 weeks). In the stakeholder
prioritisation meeting, this trade-off should be explicitly
presented to the CEO and Finance Head — the confirmed evidence
for FR-08 is stronger than any other recommendation except
FR-07, but the implementation cost is also the highest.
The final ranking between FR-06 and FR-08 should reflect
the organisation's available budget and development capacity.

