# Business Requirements Document (BRD)
## LendFast — Application Conversion Optimisation Engagement

---

| Field | Detail |
|---|---|
| Document Title | Business Requirements Document |
| Project Name | LendFast Application Conversion Optimisation |
| Version | 0.1 — Draft |
| Status | In Progress |
| Prepared By | Geethika|
| Reviewed By | [To be assigned] |
| Date Created | August 2026 |
| Last Updated | August 2026 |

---

## Document Control

| Version | Date | Author | Changes |
|---|---|---|---|
| 0.1 | August 2026 | Geethika| Initial draft — Executive Summary |

---

## Table of Contents

1. Executive Summary
2. Business Objectives *(to be completed)*
3. Problem Statement *(to be completed)*
4. Project Scope *(to be completed)*
5. Stakeholder Register *(to be completed)*
6. Current State Overview *(to be completed)*
7. Assumptions and Constraints *(to be completed)*
8. Dependencies *(to be completed)*
9. Functional Requirements *(to be completed)*
10. Non-Functional Requirements *(to be completed)*
11. KPIs and Success Metrics *(to be completed)*
12. Risk Summary *(to be completed)*
13. Acceptance Criteria *(to be completed)*
14. Approvals *(to be completed)*

---

## 1. Executive Summary

LendFast, a digital consumer lending company, is facing critically
low application conversion rates. With an average abandonment rate
of [X]% against an industry benchmark of 63% (Signicat, 2025), the
majority of users who initiate a loan application do not complete it
— directly reducing funded loan revenue and elevating customer
acquisition costs that compress margin on each loan disbursed.

The urgency of this problem is compounded by the company's growth
obligations. Having raised $12 million in Series A funding 18 months
ago, LendFast faces investor expectations of consistent revenue
growth. The cost per funded loan has been increasing steadily while
net revenue has remained flat — a trajectory that is unsustainable
without a significant improvement in application completion rates.

This engagement will address the conversion gap through a structured
two-phase approach. Phase one will conduct a rigorous data analysis
to identify primary drop-off points across the seven-step application
process and validate initial hypotheses around document upload
friction, device-type disparities, and segment-specific barriers.
Phase two will translate findings into targeted interventions across
user experience, process design, and trust-building mechanisms,
developed in consultation with Sales, Finance, Operations, and
Compliance stakeholders. In parallel, three immediate low-cost
interventions — a pre-application document checklist, proactive
in-application support, and regulatory trust signals at the document
upload step — will be implemented to accelerate early conversion
improvements during the analysis period.

LendFast currently has approximately 45,000 registered users of whom
an estimated [X]% have completed a loan application, representing
the active revenue-generating customer base. The remaining registered
users represent a pool of warm leads who demonstrated intent by
initiating an application but did not complete it. Converting these
existing users requires zero additional acquisition spend — making
conversion optimisation the highest return investment available to
the business at this stage. This engagement targets an application
completion rate of 45–50% within six months of implementation,
consistent with improvements achieved by comparable fintech platforms
following UX and process redesign (Titan: 31% to 78% post-redesign).
As a secondary effect, reduced friction and improved user experience
are expected to strengthen brand trust and support organic user
growth — though these effects fall outside the measurable scope of
this engagement.

---

*Sections 2–14 will be completed progressively through the engagement.
Each section will be reviewed and approved by relevant stakeholders
before the document is finalised.*

---

*Document version: 0.1 — Draft*
*Prepared by: [Your Name] — Junior BA/DA*
*Project: LendFast Conversion Optimisation Engagement*
*Status: In Progress*

---

## 2. Business Objectives

The following objectives define the strategic outcomes this engagement
is designed to achieve. Each objective is aligned to a specific
stakeholder group and serves as the foundation for all requirements,
recommendations, and success metrics defined in subsequent sections.

Objectives are stated as strategic intent without numeric targets.
Measurable targets are defined in Section 11 — KPIs and Success Metrics.

---

**Objective 1 — Conversion and Revenue Growth**
*(Primary stakeholder: CEO)*

Increase the rate of loan application completion among registered
users to grow the revenue-generating customer base without additional
acquisition spend.

---

**Objective 2 — Operational Efficiency**
*(Primary stakeholder: Operations Head)*

Reduce operational cost and processing time associated with incomplete
applications by improving application completion quality and reducing
manual follow-up requirements.

---

**Objective 3 — User Experience and Trust**
*(Primary stakeholder: End Users / indirect — all stakeholders)*

Establish LendFast as a trusted and accessible digital lending platform
by delivering a transparent, intuitive, and frictionless application
experience that competes effectively with incumbent financial institutions.

---

**Objective 4 — Regulatory Compliance**
*(Primary stakeholder: Compliance Officer)*

Ensure all application process improvements maintain full adherence
to regulatory requirements including KYC, AML, and federal lending
obligations, protecting the company from regulatory and reputational
risk.

---

**Objective 5 — Marketing Intelligence**
*(Primary stakeholder: Sales and Marketing Head)*

Enable targeted and efficient allocation of marketing spend by
identifying the user segments, acquisition channels, and device
types that produce the highest application completion rates —
informing Sales and Marketing decisions on where to concentrate
customer acquisition investment.

---

**Objective 6 — Financial Risk Protection**
*(Primary stakeholder: Finance Head)*

Ensure that application process improvements do not increase fraud
exposure, degrade applicant pipeline quality, or generate additional
downstream processing burden for Finance and Risk teams.

---

### Objectives to Stakeholder Mapping

| Objective | Primary Stakeholder | Secondary Stakeholders |
|---|---|---|
| 1 — Conversion and Revenue Growth | CEO | Sales & Marketing, Finance |
| 2 — Operational Efficiency | Operations Head | Finance, Development |
| 3 — User Experience and Trust | End Users | CEO, Sales & Marketing |
| 4 — Regulatory Compliance | Compliance Officer | Finance, Legal |
| 5 — Marketing Intelligence | Sales & Marketing Head | CEO, Operations |
| 6 — Financial Risk Protection | Finance Head | Compliance, Operations |


---

## 3. Problem Statement

LendFast, a digital consumer lending platform, is experiencing
critically low application conversion rates with an abandonment
rate of [X]% — significantly exceeding the industry benchmark
of 63% (Signicat, 2025). Despite 45,000 registered users acquired
over 18 months of operations, the revenue-generating customer base
remains at an estimated [X]%, representing a substantial gap between
user acquisition investment and funded loan revenue.

The business impact of this conversion gap is compounded by
LendFast's growth obligations. Having raised $12 million in Series A
funding, the company is not meeting investor expectations for revenue
growth. The cost per funded loan has been increasing steadily while
net revenue margins remain flat — creating a trajectory that is
unsustainable without significant improvement in application
completion rates.

The initial hypothesis presented at project kickoff attributes the
primary drop-off cause to application length. However, preliminary
analysis suggests that multiple contributing factors are likely
driving abandonment across the seven-step application process —
including process friction at document upload, device-type disparities
between mobile and desktop users, segment-specific barriers for
self-employed applicants, and credit score anxiety at the consent
step. Additionally, technical performance factors including
application errors, session timeouts, and upload failures may
represent a further contributing cause that cannot be fully assessed
from the current transactional dataset alone. Structured data
analysis is required to identify and prioritise root causes before
solutions are defined.

This problem statement is bounded to the application completion
journey of existing registered users. The following are explicitly
out of scope: new customer acquisition campaigns and marketing
channel strategy; post-loan-approval operational and servicing
processes; changes to the loan approval criteria, credit risk model,
or compliance frameworks; and core infrastructure or platform
architecture changes. UX and process improvements required to
accelerate conversion are within scope, as is targeted re-engagement
of incomplete applicants based on segmentation findings.


---

## 4. Project Scope

### 4.1 In Scope

The following activities are within the boundary of this engagement.
Each item lists the responsible owner and the tangible deliverable produced.

| Activity | Owner | Deliverable |
|---|---|---|
| Funnel drop-off analysis across all seven application steps | Data Analyst | Step-level drop-off rate report informing requirements definition |
| Segmentation analysis by device type, credit score band, employment status, and loan amount | Data Analyst | Drop-off rates for different market segments enabling targeted re-engagement campaigns |
| Gap analysis comparing current conversion rates against industry benchmarks | BA | Gap analysis document quantifying the difference between current completion rate and industry benchmark, broken down by step, segment, and device type |
| UX and process improvement requirements | BA and UX Designer | Functional requirements document and process flow diagrams specifying UX and workflow changes needed to reduce friction at primary drop-off points |
| Targeted re-engagement of incomplete applicants based on segmentation findings | Sales Head | Segmented re-engagement campaign targeting incomplete applicants by drop-off step and user segment, with measurable conversion targets per segment |
| Technical performance monitoring requirements | Data Analyst | Technical performance monitoring requirements document specifying metrics, thresholds, and alerting criteria for application error rates, session timeouts, and upload failures |

---

### 4.2 Out of Scope

The following are explicitly excluded from this engagement.
Any stakeholder request that falls within these boundaries requires
a separate project initiation.

| Exclusion | Reason |
|---|---|
| New customer acquisition campaigns and marketing channel strategy | This engagement addresses conversion of existing registered users only — acquisition is a separate workstream |
| Post-loan-approval operational and servicing processes | Loan servicing begins after application completion — outside the application funnel boundary |
| Changes to loan approval criteria or credit risk model | Credit model changes require a separate risk and compliance engagement |
| Changes to compliance frameworks or regulatory strategy | Regulatory strategy is owned by the Compliance and Legal teams — outside BA scope |
| Core infrastructure or platform architecture changes | Infrastructure changes require engineering-led engagement with separate budget and timeline |

---

### 4.3 Assumptions

| # | Assumption | If False |
|---|---|---|
| 1 | The dataset is complete and representative of all 45,000 registered users | Missing user records will produce incomplete funnel analysis and unreliable segment findings |
| 2 | Data is recent and captures major seasonal or economic trends across the 18-month period | External contributing factors impacting user decisions cannot be fully assessed |
| 3 | Data accuracy and consistency are maintained without technical logging errors | Faulty data will produce misleading EDA findings and incorrect root cause identification |
| 4 | Brand perception and external reputation are not primary drivers of application abandonment | In-application improvements alone will not achieve the 45–50% completion rate target |
| 5 | The majority of users who started the application had genuine intent to complete a loan application and abandoned due to friction rather than change of mind or competitor switching | The achievable completion rate improvement will be lower than targeted as a proportion of abandonment reflects intentional exit |
| 6 | Regulatory and compliance guidelines remain stable throughout the project implementation timeline | Changes to regulatory requirements will necessitate redesigning recommended processes and workflows |

---

### 4.4 Constraints

| # | Constraint | Implication |
|---|---|---|
| 1 | All recommendations must strictly adhere to existing KYC, AML, and federal lending regulations | No solution that requires regulatory approval or creates compliance risk will be implemented regardless of conversion impact |
| 2 | The loan approval criteria and credit risk model remain fixed boundaries | No application process change may alter who gets approved or how creditworthiness is assessed — any recommendation affecting approval logic requires a separate engagement |
| 3 | All recommendations are constrained to low-to-medium cost interventions consistent with an early-stage fintech's available capital | High-cost infrastructure changes or platform rebuilds are excluded regardless of conversion impact — all budget commitments require Finance Head approval |


---

## 5. Stakeholder Register

The following register documents all stakeholders involved in or
affected by this engagement. Interest and influence ratings inform
engagement strategy. Engagement level determines decision-making
authority. Communication needs define the frequency and channel
of project updates.

**Engagement Level Definitions:**
- **Approve** — must formally sign off before work proceeds
- **Consult** — input sought before decisions are made
- **Inform** — kept updated but not asked for input

**Influence and Interest Scale:**
- **H** — High
- **M** — Medium
- **L** — Low

| Stakeholder | Interest | Influence | Engagement | Communication | Key Concern |
|---|---|---|---|---|---|
| CEO | H | H | Approve | Weekly executive steering meetings | Whether conversion improvements will deliver the revenue growth needed to meet Series A investor expectations |
| Sales & Marketing Head | H | M | Consult | Fortnightly progress reports with ad-hoc updates when segmentation findings are available | Maximising conversion return on each marketing spend |
| Finance Head | H | M | Consult | Weekly executive meetings | Effective utilisation of capital funds without increasing fraud exposure or downstream processing costs |
| Operations Head | M | L | Inform | Fortnightly progress reports | Uninterrupted loan processing workflow with no additional bottlenecks from process changes |
| Compliance Officer | H | H | Approve | Weekly executive meetings | Ensuring all process changes meet KYC, AML, and federal lending regulatory requirements |
| Development Team | M | L | Inform + targeted Consult | Requirements documentation at milestones — ad-hoc consultation for technical feasibility questions | Clear, scoped requirements with no mid-sprint scope changes |
| End Users | H | L | Inform | Through improved product experience post-implementation — no direct project communication required | Transparent, frictionless, and trustworthy loan application experience |

---

### Key Stakeholder Insights

**Two High/High stakeholders — CEO and Compliance Officer**

These are the two stakeholders whose sign-off is non-negotiable.
Every recommendation must satisfy both — the CEO's growth objectives
and the Compliance Officer's regulatory requirements. Where these
two interests conflict, regulatory requirements take precedence
as a non-negotiable constraint (see Section 4.4).

**Finance Head as gatekeeper**

Despite Medium influence, Finance holds effective veto power over
any recommendation that increases fraud exposure or budget
commitments beyond approved capital. All cost implications must
be cleared with Finance before recommendations are presented
to the CEO for approval.

**End Users as the ultimate measure**

End users have no direct project influence but represent the
ultimate measure of success. Every recommendation is evaluated
against whether it reduces friction and builds trust for the
end user — the person completing the application at 10pm on
their phone with documents they may not have immediately available.


---

## 6. Current State Overview

This section documents how LendFast operates today — the existing
application process, current performance, known system characteristics,
and confirmed pain points — before any changes are made. This is the
as-is baseline that the gap analysis, process flows, and requirements
will reference throughout the engagement.

---

### 6.1 Current Application Process

LendFast provides users a web application where they can sign up
with email or phone verification and start filling an application
for a personal loan. Each user completes up to seven sequential
sections of information covering personal details, employment and
income status, loan amount and purpose declaration, and document
upload to verify financial credibility. The application process
adheres to KYC, AML, and federal lending obligations throughout.

| Step | Name | User Action | System Action |
|---|---|---|---|
| 1 | Personal Details | Enters name, address, date of birth | Validates format and checks for duplicate accounts |
| 2 | Employment Information | Enters employer name, job title, start date | Stores employment data for income verification |
| 3 | Income Verification | Enters monthly income and income source | Flags inconsistencies for manual review |
| 4 | Loan Amount and Purpose | Selects loan amount and purpose | Generates indicative loan terms |
| 5 | Credit Check Consent | Authorises soft credit pull | Initiates credit bureau API call |
| 6 | Document Upload | Uploads payslips, bank statements, photo ID | Validates file format and initiates document verification |
| 7 | Review and Submit | Reviews application summary and submits | Routes completed application to underwriting queue |

---

### 6.2 Current Performance Metrics

After raising $12 million in Series A funding and 18 months of
operation, LendFast has acquired 45,000 registered users. Despite
significant growth in user acquisition, the primary performance
indicator — application completion rate — stands at [X]% against
an industry benchmark of 63%, representing the core operational
gap this engagement addresses.

The business consequence of this conversion gap is significant.
Revenue generation has not grown proportionally with user acquisition.
The cost per funded loan has been rising continuously while net
profit margins remain flat — creating a trajectory that does not
meet investor growth expectations.

*Note: All baseline metrics marked [X] will be populated following
completion of the exploratory data analysis phase.*

| Metric | Current Value | Industry Benchmark | Source |
|---|---|---|---|
| Application completion rate | [X]% | ~37% | Signicat, 2025 |
| Step-level drop-off rates | [X]% per step | TBD | EDA output |
| Mobile vs desktop completion gap | [X]% | TBD | EDA output |
| Self-employed completion rate | [X]% | TBD | EDA output |
| Cost per funded loan | Rising — exact figure TBD | TBD | Finance team |
| Monthly application starts | ~6,200 | N/A | CEO kickoff |

---

### 6.3 Current Systems and Tools

Based on the product description, LendFast's application is assumed
to operate on a cloud-based platform with third-party integrations
for credit bureau access at Step 5 and document verification at
Step 6. Specific vendors, integration architecture, and system
constraints are to be confirmed with the Development team before
technical feasibility of recommendations can be assessed.

**Dependency:** Current technology stack details
**Owner:** Development Team Lead
**Required by:** [Date — to be agreed at project kickoff]

---

### 6.4 Known Pain Points

**Confirmed pain points — established before data analysis:**

1. Application drop-off rate significantly exceeds the industry
   benchmark — confirmed by the CEO at project kickoff meeting.

2. Incomplete applications generate manual follow-up workload for
   the Operations team — confirmed through stakeholder mapping.

**Hypothesised pain points — pending data validation:**

Additional pain points have been hypothesised based on industry
research and stakeholder input. These are documented in full in
the project case brief and will be validated or rejected through
the data analysis phase. Confirmed pain points will be incorporated
into this section following EDA completion.


---

## 7. Assumptions and Constraints

*Assumptions and constraints are documented in Section 4 —
Project Scope (Sections 4.3 and 4.4). They are maintained
there to keep all scope-related information consolidated
in one section for stakeholder reference.*

*See Section 4.3 for all six project assumptions.*
*See Section 4.4 for all three project constraints.*

---

## 8. Dependencies

Dependencies are external conditions or deliverables that
this engagement relies on but does not control. If a dependency
is not met, the associated project activities are blocked until
it is resolved.

| # | Dependency | Owner | Risk if Unmet |
|---|---|---|---|
| 1 | Dataset completeness and accuracy depends on the data collection methods and systems used by LendFast over the 18-month period | Development Team / Data Engineering | EDA findings will be unreliable and root cause identification may be incorrect — invalidating all subsequent recommendations |
| 2 | Credit bureau API and document verification service integrations remain stable and accessible throughout the implementation period | Third-party vendors (names TBD from Development team consultation) | Step 5 and Step 6 recommendations may require redesign if integration specifications change |
| 3 | CEO and Compliance Officer approval of final recommendations is required before any UX or process changes can be implemented | CEO and Compliance Officer | Implementation is blocked regardless of recommendation quality — project timeline extends until approval is secured |
| 4 | Functional requirements definition cannot begin until comprehensive data analysis is completed | Data Analyst | Subsequent process and workflow designs and suggested implementations cannot be completed within the 6-month timeframe |

---

### Dependency Resolution Plan

| # | Dependency | Resolution Action | Target Date |
|---|---|---|---|
| 1 | Dataset quality | Data quality assessment as first EDA activity — flag issues before full analysis begins | Week 1 of data analysis phase |
| 2 | API integrations | Confirm vendor details and integration stability with Development team during technology stack consultation | Prior to requirements definition |
| 3 | Stakeholder approval | Schedule CEO and Compliance Officer review session as final milestone before implementation begins | Month 4 of engagement |
| 4 | EDA completion | Data analysis must be completed and findings validated before requirements workshops begin | Prior to requirements definition phase |


---

## 9. Functional Requirements

Functional requirements describe specific behaviours and capabilities
the system must have to meet business needs. They answer: what must
the system do?

**Priority Definitions:**
- **High** — Required for launch. Directly addresses primary business objective.
- **Medium** — Important but not launch-blocking. Addresses secondary objectives.
- **Low** — Desirable. Addresses edge cases or segment-specific needs.

**Status Definitions:**
- **Confirmed** — Required regardless of EDA findings.
- **Provisional** — Pending EDA validation. Will be confirmed or removed
  following data analysis phase.

---

### Confirmed Requirements

---

**FR-01: Pre-Application Document Checklist**

| Field | Detail |
|---|---|
| Description | The system must display a checklist of all required documents and information before the user begins the application |
| Trigger | When user navigates to the loan application landing page |
| Priority | High |
| Status | Confirmed |

*Acceptance Criteria:*

```
AC-01a:
Given the user is accessing the application on any device type
When the application landing page loads
Then the complete document checklist must be fully displayed 
and acknowledged by the user before the Start Application 
button becomes accessible
```

---

**FR-02: Document Upload Validation and Error Messaging**

| Field | Detail |
|---|---|
| Description | The system must verify document format, display upload progress and status. If upload fails, the system must display the reason for failure and next steps the user can take to successfully upload |
| Trigger | When user clicks the upload document button at Step 6 |
| Priority | High |
| Status | Confirmed |

*Acceptance Criteria:*

```
AC-02a:
Given the user clicks the upload button on any device
When the document is uploaded successfully
Then a confirmation message with upload status must be displayed

AC-02b:
Given the user clicks the upload button on any device
When the document upload fails
Then the system must display the reason for failure and 
specific next steps the user can take to resolve the issue
```

---

**FR-03: Session Progress Save**

| Field | Detail |
|---|---|
| Description | The system must save user progress when an error occurs or session times out so that the user can resume from the same point after restarting the session |
| Trigger | When the application closes unexpectedly or an error is logged |
| Priority | High |
| Status | Confirmed |

*Acceptance Criteria:*

```
AC-03a:
Given a user is signed in and actively filling the application
When the application closes with any error or session timeout
Then an automatic save must be triggered and all entered 
information must be retained when the user logs in again
```

---

**FR-04: Credit Check Transparency Message**

| Field | Detail |
|---|---|
| Description | The system must display a message stating that a hard credit check will not be conducted and the user's credit score will not be affected by this process |
| Trigger | When the application reaches Step 5 |
| Priority | High |
| Status | Confirmed |

*Acceptance Criteria:*

```
AC-04a:
Given the user reaches Step 5 of the application
When the credit check consent screen loads
Then a message must be displayed before the consent 
checkbox stating that the user's credit score will 
not be affected by this credit check
```

---

**FR-05: Compliance and Licence Badges at Step 6**

| Field | Detail |
|---|---|
| Description | The system must display the company's regulatory compliance adherence and government-approved licence information before the user uploads any sensitive documents |
| Trigger | When user reaches Step 6 and before the upload button is accessible |
| Priority | High |
| Status | Confirmed |

*Acceptance Criteria:*

```
AC-05a:
Given the user reaches the document upload page
When Step 6 loads
Then compliance badges and licence verification information 
must be displayed before the user can access the upload button
```

---

**FR-06: Proactive Chat Support Trigger**

| Field | Detail |
|---|---|
| Description | The system must provide a proactive chat support trigger that activates when a user shows signs of friction during the application process |
| Trigger | When user pauses for more than 60 seconds at any step OR when user clicks the help button |
| Priority | High |
| Status | Confirmed |

*Acceptance Criteria:*

```
AC-06a:
Given a user is actively filling the application
When the user remains inactive on any step for more than 
60 seconds
Then a chat support prompt must appear offering assistance

AC-06b:
Given a user is actively filling the application
When the user clicks the help button at any step
Then a chat support interface must be displayed immediately
```

---

**FR-07: Telemetry Data Capture**

| Field | Detail |
|---|---|
| Description | The system must record all telemetry data including errors, event logs, user journey paths, and timestamps to enable analysis of user behaviour and identification of technical friction points |
| Trigger | Whenever any user event occurs within the application |
| Priority | High |
| Status | Confirmed |

*Acceptance Criteria:*

```
AC-07a:
Given a user starts the application
When any event occurs — including step completion, field 
skipping, extended time on a field, page load errors, 
or session timeouts
Then the event must be logged with a corresponding 
timestamp and user identifier
```

---

### Provisional Requirements
*(Pending EDA validation — will be confirmed or removed 
following data analysis phase)*

---

**FR-08: Self-Employed User Pathway**

| Field | Detail |
|---|---|
| Description | The system must display a separate sub-section for self-employed users with fields relevant to variable income and self-employment documentation |
| Trigger | When the user selects employment status as self-employed at Step 2 |
| Priority | Low |
| Status | Provisional — pending Hypothesis 2 validation |

*Acceptance Criteria:*

```
AC-08a:
Given the user reaches Step 2 of the application
When the user selects employment status as self-employed
Then a separate sub-section must be displayed with fields 
relevant to self-employed applicants replacing standard 
employer and fixed income fields
```

---

**FR-09: Incomplete Applicant Re-Engagement Notification**

| Field | Detail |
|---|---|
| Description | The system must send a re-engagement notification to users who abandon the application without completing it, targeted by segment and step of abandonment |
| Trigger | When a user closes or abandons the application without completion and no technical failure event is recorded |
| Priority | High |
| Status | Provisional — pending segmentation analysis findings |

*Acceptance Criteria:*

```
AC-09a:
Given a user starts the application
When the user closes or abandons the application 
without completing it and no system error is recorded
Then a re-engagement notification must be sent to the 
user's registered email address within 24 hours of 
abandonment
```

---

**FR-10: Application Progress Indicator**

| Field | Detail |
|---|---|
| Description | The system must display a progress indicator showing the current step and total steps remaining throughout the application process on all device types |
| Trigger | When the user clicks the Start Application button |
| Priority | Low |
| Status | Provisional — pending mobile drop-off confirmation |

*Acceptance Criteria:*

```
AC-10a:
Given a user has started the application on any device
When the user progresses through each step
Then a progress indicator must be visible showing 
the current step number and total steps remaining 
throughout the entire application process
```

---

### Functional Requirements Summary

| ID | Title | Priority | Status |
|---|---|---|---|
| FR-01 | Pre-Application Document Checklist | High | Confirmed |
| FR-02 | Document Upload Validation and Error Messaging | High | Confirmed |
| FR-03 | Session Progress Save | High | Confirmed |
| FR-04 | Credit Check Transparency Message | High | Confirmed |
| FR-05 | Compliance and Licence Badges at Step 6 | High | Confirmed |
| FR-06 | Proactive Chat Support Trigger | High | Confirmed |
| FR-07 | Telemetry Data Capture | High | Confirmed |
| FR-08 | Self-Employed User Pathway | Low | Provisional |
| FR-09 | Incomplete Applicant Re-Engagement Notification | High | Provisional |
| FR-10 | Application Progress Indicator | Low | Provisional |


---

## 10. Non-Functional Requirements

Non-functional requirements define the quality attributes of the
system — not what it does but how well it does it. Every NFR
contains a specific measurable standard that can be verified
through testing or monitoring.

---

**NFR-01: Availability**

| Field | Detail |
|---|---|
| Description | The system must maintain 99.9% uptime during peak application hours (8am to 11pm local time) |
| Priority | High |
| Rationale | LendFast loses applicants permanently when the platform is unavailable mid-application. A 0.1% downtime allowance equates to approximately 8.7 hours of acceptable downtime per year — consistent with fintech industry standards |
| Measurement | Uptime monitored via system health dashboard. Monthly availability report reviewed by Operations Head. Alerts triggered when availability drops below threshold |

---

**NFR-02: Performance**

| Field | Detail |
|---|---|
| Description | The system must load each application step within 3 seconds on a standard mobile connection and within 1.5 seconds on desktop |
| Priority | High |
| Rationale | Page load latency beyond 3 seconds on mobile significantly increases abandonment rates. Given that LendFast's primary users access via mobile, mobile performance is the primary standard |
| Measurement | Page load times tracked via telemetry data (FR-07). Alerts triggered when average load time exceeds threshold. Reviewed weekly by Development team |

---

**NFR-03: Security**

| Field | Detail |
|---|---|
| Description | The system must implement AES-256 encryption for all data at rest and TLS 1.2 or higher for all data in transit to prevent data leakage and information misuse |
| Priority | High |
| Rationale | The application processes sensitive personal, financial, and identity data. Any data breach causes direct monetary loss to users and severe reputational and regulatory damage to LendFast |
| Measurement | Quarterly security audits and penetration testing. All data access attempts logged and reviewed monthly. Authentication and authorisation protocols audited quarterly |

---

**NFR-04: Compliance**

| Field | Detail |
|---|---|
| Description | The system must strictly adhere to KYC, AML, Truth in Lending Act (TILA), and Equal Credit Opportunity Act (ECOA) requirements throughout all application process stages |
| Priority | High |
| Rationale | LendFast processes financial transactions that are subject to federal and state regulation. Non-compliance creates legal liability, regulatory penalties, and loss of operating licence — existential risks for an early-stage fintech |
| Measurement | Quarterly compliance audits conducted with Compliance Officer. Any process change reviewed for regulatory impact before implementation. Zero tolerance threshold — 100% compliance required |

---

**NFR-05: Usability**

| Field | Detail |
|---|---|
| Description | The system must meet WCAG 2.1 accessibility standards and the average application completion time must not exceed 30 minutes across all device types |
| Priority | High |
| Rationale | Drop-off rates are highly influenced by ease of use. Users from different backgrounds and technical abilities interact with the platform — if the application itself feels too complex, users will switch to competitors before reaching the approval stage |
| Measurement | Average time per step and overall completion time tracked via telemetry data (FR-07). WCAG 2.1 compliance verified through accessibility audit. Completion time benchmarked monthly against the 30-minute target |

---

**NFR-06: Scalability**

| Field | Detail |
|---|---|
| Description | The system must support at least 10,000 concurrent users during peak hours (8am to 11pm local time) and scale horizontally and vertically to accommodate a growing user base |
| Priority | Medium |
| Rationale | LendFast has grown from 800 to 6,200 monthly application starts in 18 months. Conversion improvements and organic growth will further increase concurrent usage. The system must handle traffic spikes during marketing campaigns without performance degradation |
| Measurement | Transactions per second (TPS), active user sessions, response time under load, and CPU/memory/disk consumption monitored via infrastructure dashboard. Load testing conducted before major releases |

---

### Non-Functional Requirements Summary

| ID | Category | Key Standard | Priority |
|---|---|---|---|
| NFR-01 | Availability | 99.9% uptime during peak hours | High |
| NFR-02 | Performance | 3 sec mobile / 1.5 sec desktop page load | High |
| NFR-03 | Security | AES-256 at rest / TLS 1.2 in transit | High |
| NFR-04 | Compliance | KYC, AML, TILA, ECOA adherence | High |
| NFR-05 | Usability | WCAG 2.1 / 30-min completion target | High |
| NFR-06 | Scalability | 10,000 concurrent users at peak | Medium |


---

## 11. KPIs and Success Metrics

KPIs measure whether business objectives are achieved over time.
All baseline values marked [X] will be populated following
completion of the exploratory data analysis phase.

---

**KPI-01: Application Completion Rate**

| Field | Detail |
|---|---|
| Business Objective | Objective 1 — Conversion and Revenue Growth |
| Metric | Percentage of users who start the application and complete all seven steps |
| Baseline | [X]% — to be established from EDA |
| Target | 45–50% within 6 months of implementation |
| Timeline | 6 months post-implementation |
| Measurement Method | Monthly calculation: completed applications ÷ total application starts. Tracked via Power BI dashboard |
| Owner | CEO — reviewed in weekly executive meetings |

---

**KPI-02: Operational Processing Efficiency**

| Field | Detail |
|---|---|
| Business Objective | Objective 2 — Operational Efficiency |
| Metric 1 | Average time from application submission to loan decision in hours |
| Target 1 | Under 24 hours — consistent with LendFast's disbursement promise |
| Measurement Method 1 | Average time calculated from application submission timestamp to loan decision timestamp |
| Metric 2 | Percentage of completed applications requiring manual follow-up |
| Target 2 | Below 10% of completed applications |
| Measurement Method 2 | Number of applications requiring manual follow-up ÷ total applications processed |
| Timeline | 6 months post-implementation |
| Owner | Operations Head — reviewed in weekly executive meetings |

---

**KPI-03: User Experience and Trust Metrics**

| Field | Detail |
|---|---|
| Business Objective | Objective 3 — User Experience and Trust |
| Metric 1 | Step 6 drop-off rate |
| Baseline 1 | [X]% — to be established from EDA |
| Target 1 | Below 30% within 6 months |
| Measurement Method 1 | Number of applications dropped at Step 6 ÷ total incomplete applications |
| Metric 2 | Chat support continuation rate |
| Baseline 2 | [X]% — to be established post FR-06 implementation |
| Target 2 | Above 60% continuation rate after chat engagement |
| Measurement Method 2 | Number of users who engaged with chat and subsequently completed the application ÷ total users who engaged with chat |
| Timeline | 6 months post-implementation |
| Owner | BA and UX Designer — tracked via Power BI dashboard |

---

**KPI-04: Regulatory Compliance Rate**

| Field | Detail |
|---|---|
| Business Objective | Objective 4 — Regulatory Compliance |
| Metric | Percentage of processed applications meeting all compliance requirements |
| Baseline | [X]% — to be established from compliance audit |
| Target | 100% — zero tolerance threshold |
| Timeline | Ongoing — monitored continuously |
| Measurement Method | Number of applications failing regulatory requirements ÷ total successfully processed applications. Tracked via compliance dashboard |
| Owner | Compliance Officer — reviewed quarterly |

---

**KPI-05: Re-Engagement Conversion Rate**

| Field | Detail |
|---|---|
| Business Objective | Objective 5 — Marketing Intelligence |
| Metric | Percentage of incomplete applicants who complete the application after receiving targeted re-engagement communication |
| Baseline | [X]% — to be established after FR-09 implementation |
| Target | At least 25% increase within 6 months of implementation |
| Timeline | 6 months post-implementation |
| Measurement Method | Total applications completed after receiving re-engagement notifications ÷ total incomplete applications contacted. Tracked via Power BI dashboard |
| Owner | Sales and Marketing Head |

---

**KPI-06: Fraud and Financial Risk Metrics**

| Field | Detail |
|---|---|
| Business Objective | Objective 6 — Financial Risk Protection |
| Metric 1 | Percentage increase in fraudulent applications post-implementation |
| Target 1 | Must not exceed 10% increase from baseline |
| Measurement Method 1 | (Fraud applications post-implementation − fraud applications pre-implementation) ÷ fraud applications pre-implementation |
| Metric 2 | Overall fraudulent application rate |
| Baseline 2 | [X]% — to be established from EDA |
| Target 2 | At least 20% below industry standard fraud rate |
| Measurement Method 2 | Total fraud applications ÷ total completed or submitted applications |
| Timeline | 6 months post-implementation |
| Owner | Finance Head — reviewed monthly |

---

### KPI Summary Table

| ID | KPI Name | Primary Metric | Target | Owner |
|---|---|---|---|---|
| KPI-01 | Application Completion Rate | Completion rate | 45–50% | CEO |
| KPI-02 | Operational Processing Efficiency | Processing time / Manual follow-up rate | <24 hrs / <10% | Operations Head |
| KPI-03 | User Experience and Trust | Step 6 drop-off / Chat continuation | <30% / >60% | BA and UX Designer |
| KPI-04 | Regulatory Compliance Rate | Compliance adherence | 100% | Compliance Officer |
| KPI-05 | Re-Engagement Conversion Rate | Re-engagement completion | 25% increase | Sales and Marketing Head |
| KPI-06 | Fraud and Financial Risk | Fraud rate change / Overall fraud rate | <10% increase / 20% below industry | Finance Head |


---

## 12. Risk Summary

A risk is a future event that may negatively affect the delivery
or outcomes of this engagement. Risks are assessed by likelihood
and impact and managed proactively through mitigation and
contingency planning.

**Risk Rating Matrix:**
- High/High = Critical — immediate mitigation required
- High/Medium or Medium/High = High — active monitoring required
- Medium/Medium = Medium — periodic review required
- Low/anything = Low — log and monitor

---

**R-01: Hypothesis Failure and Missed Root Causes**

| Field | Detail |
|---|---|
| Description | The hypotheses formulated during problem framing may not be confirmed by data analysis, or significant drivers of application abandonment may have been missed entirely. Recommendations built on unconfirmed or incomplete hypotheses will fail to address actual root causes — resulting in UX and process changes that do not move completion rate KPIs despite correct implementation |
| Likelihood | Medium — industry research supports the primary hypotheses but LendFast-specific data may reveal unexpected patterns |
| Impact | High — if root causes are misidentified, the entire recommendation set requires redesign, extending the timeline and consuming additional budget |
| Risk Rating | High |
| Mitigation | Apply structured hypothesis testing methodology during EDA — confirm or reject each hypothesis explicitly before defining requirements. Maintain a provisional requirements category (as established in Section 9) so that unconfirmed hypotheses do not drive implementation until data validates them |
| Owner | BA and Data Analyst |
| Contingency | If EDA rejects primary hypotheses, conduct supplementary qualitative research — user interviews or support ticket analysis — to identify actual drop-off drivers before requirements are revised |

---

**R-02: Data Quality Issues or Missing Data**

| Field | Detail |
|---|---|
| Description | The dataset provided may contain incomplete records, logging errors, or inconsistent field values that undermine the reliability of EDA findings. If step_reached values are incorrectly logged due to technical failures, funnel analysis will produce misleading drop-off rates. If key segments are underrepresented, segmentation analysis will generate biased recommendations |
| Likelihood | Medium — data quality issues are common in early-stage fintech platforms where logging infrastructure may not have been a priority during rapid growth |
| Impact | High — unreliable data produces incorrect root cause identification, invalidating all downstream requirements and recommendations |
| Risk Rating | High |
| Mitigation | Conduct a data quality assessment as the first EDA activity before any analysis begins. Document completeness, accuracy, and consistency issues. Flag any fields with more than 5% missing values or suspected logging errors before proceeding |
| Owner | Data Analyst |
| Contingency | If data quality is insufficient for reliable analysis, escalate to Development team to identify logging gaps and request a corrected dataset. Supplement with industry benchmarks where LendFast-specific data is unreliable |

---

**R-03: Stakeholder Misalignment During Project**

| Field | Detail |
|---|---|
| Description | Competing priorities among stakeholders may emerge during the engagement — particularly between the Sales and Marketing Head seeking maximum conversion through process simplification and the Finance Head and Compliance Officer requiring application completeness and regulatory adherence. Unresolved conflicts may delay sign-off, dilute recommendations, or result in a solution that satisfies no stakeholder fully |
| Likelihood | Medium — two High/High stakeholders (CEO and Compliance Officer) have non-overlapping primary concerns. The CEO's growth objective and the Compliance Officer's regulatory mandate will create tension at specific recommendation review points |
| Impact | Medium — misalignment delays implementation and may require requirements to be renegotiated, extending the timeline |
| Risk Rating | Medium |
| Mitigation | Establish a formal stakeholder review process at the end of each project phase. Present recommendations with explicit compliance impact assessments so Finance and Compliance concerns are addressed before CEO approval is sought. Use the stakeholder register communication plan (Section 5) to ensure no stakeholder is surprised by a recommendation |
| Owner | BA — escalate to CEO as project sponsor if misalignment cannot be resolved at working level |
| Contingency | If stakeholder conflict blocks progress, convene a formal conflict resolution session chaired by the CEO as executive sponsor. Document agreed trade-offs in a decision log with sign-off from all parties |

---

**R-04: Budget Overrun**

| Field | Detail |
|---|---|
| Description | The scope of UX and process improvements required may exceed the allocated capital budget, particularly if data analysis reveals that multiple high-impact changes are needed simultaneously. Development costs for features like proactive chat support (FR-06), telemetry infrastructure (FR-07), and re-engagement systems (FR-09) may individually be within budget but collectively exceed the available allocation |
| Likelihood | Medium — LendFast is an early-stage fintech with constrained capital. The constraint in Section 4.4 limits recommendations to low-to-medium cost interventions but cumulative implementation costs may still exceed expectations |
| Impact | Medium — budget overrun forces prioritisation decisions that may result in high-impact requirements being deferred, reducing the likelihood of achieving KPI targets within 6 months |
| Risk Rating | Medium |
| Mitigation | Prioritise requirements by ROI at the point of implementation planning — implement High priority confirmed requirements first (FR-01 through FR-07) before provisional requirements. Obtain Finance Head cost approval for each implementation phase before work begins rather than seeking approval for the full scope at once |
| Owner | Finance Head — BA responsible for flagging scope cost implications |
| Contingency | If budget is insufficient for full implementation, present a phased delivery plan to the CEO and Finance Head — immediate low-cost interventions in Phase 1, data-dependent requirements in Phase 2 after Phase 1 ROI is demonstrated |

---

**R-05: Compliance Conflicts Blocking Recommendations**

| Field | Detail |
|---|---|
| Description | One or more confirmed functional requirements may be identified as non-compliant during the Compliance Officer's implementation review — requiring recommendations to be redesigned or removed. For example, pre-application disclosure requirements under ECOA or TILA may restrict how document checklists or credit check messaging can be presented, conflicting with UX improvement recommendations |
| Likelihood | Low — requirements were designed with compliance constraints in mind and reviewed against known regulatory obligations. However, edge cases in regulatory interpretation may surface during formal compliance review |
| Impact | High — if a High priority confirmed requirement (FR-01 through FR-07) is blocked by compliance, the associated KPI target may not be achievable within the 6-month timeline |
| Risk Rating | Medium |
| Mitigation | Involve the Compliance Officer in requirements review before finalisation — not only at the end of the engagement. Flag any requirement that touches data disclosure, consent, or document handling for early compliance review. Reference Constraint 1 (Section 4.4) at every requirements review session |
| Owner | Compliance Officer — BA responsible for facilitating early compliance review |
| Contingency | If a requirement is blocked, immediately identify a compliant alternative that achieves the same business objective. Escalate to CEO if no compliant alternative exists and the KPI target is materially affected |

---

**R-06: Timeline Delays from Dependency Chain**

| Field | Detail |
|---|---|
| Description | The engagement has a sequential dependency chain — EDA must complete before requirements are finalised, requirements must be approved before development begins, and CEO and Compliance Officer sign-off must be obtained before implementation starts. A delay at any point in this chain cascades through all subsequent phases, compressing the implementation window and making the 6-month KPI target unachievable |
| Likelihood | Medium — data quality issues (R-02), stakeholder misalignment (R-03), or compliance conflicts (R-05) could each independently delay the dependency chain |
| Impact | High — a compressed implementation window means fewer recommendations are implemented before the 6-month measurement point, reducing the likelihood of achieving completion rate targets |
| Risk Rating | High |
| Mitigation | Track dependency resolution against the dates defined in Section 8 Dependency Resolution Plan. Flag delays to the CEO immediately — do not absorb timeline slippage silently. Run parallel workstreams where dependencies allow — for example, NFR definition and process flow design can proceed in parallel with EDA |
| Owner | BA — weekly timeline review in executive steering meetings |
| Contingency | If timeline slippage is confirmed, present a revised delivery plan to the CEO with adjusted KPI measurement dates. Do not maintain the original 6-month KPI target if implementation was compressed — revise targets to reflect actual implementation timeline |

---

### Risk Summary Table

| ID | Risk | Likelihood | Impact | Rating | Owner |
|---|---|---|---|---|---|
| R-01 | Hypothesis failure and missed root causes | Medium | High | High | BA and Data Analyst |
| R-02 | Data quality issues or missing data | Medium | High | High | Data Analyst |
| R-03 | Stakeholder misalignment | Medium | Medium | Medium | BA |
| R-04 | Budget overrun | Medium | Medium | Medium | Finance Head |
| R-05 | Compliance conflicts blocking recommendations | Low | High | Medium | Compliance Officer |
| R-06 | Timeline delays from dependency chain | Medium | High | High | BA |


---

## 13. Acceptance Criteria

The following conditions must be met for the LendFast Conversion
Optimisation engagement to be formally accepted as successfully
delivered. These criteria are agreed upon by all signatories
in Section 14 before project work begins.

---

The LendFast Conversion Optimisation engagement is considered
successfully delivered when all four of the following conditions
are met:

**Condition 1 — Functional Requirements Delivery**

All High priority confirmed functional requirements (FR-01 through
FR-07) have been implemented and individually verified through
their respective acceptance criteria as defined in Section 9.
Provisional requirements (FR-08 through FR-10) are implemented
only where EDA findings confirm the underlying hypothesis.

**Condition 2 — KPI Achievement**

KPI targets defined in Section 11 are achieved within 6 months
of full implementation. Formal sign-off is obtained from the
designated KPI owner for each metric confirming the target has
been met and sustained for a minimum of one measurement period.

| KPI | Target | Sign-off Owner |
|---|---|---|
| Application completion rate | 45–50% | CEO |
| Operational processing time | Under 24 hours | Operations Head |
| Manual follow-up rate | Below 10% | Operations Head |
| Step 6 drop-off rate | Below 30% | BA and UX Designer |
| Chat continuation rate | Above 60% | BA and UX Designer |
| Compliance adherence rate | 100% | Compliance Officer |
| Re-engagement conversion rate | 25% increase | Sales and Marketing Head |
| Fraud rate change | No more than 10% increase | Finance Head |

**Condition 3 — Compliance Verification**

Zero compliance violations are identified during the implementation
review conducted by the Compliance Officer. All functional
requirements have been assessed against KYC, AML, TILA, and ECOA
requirements before deployment. Any compliance concern raised
during implementation has been resolved and documented.

**Condition 4 — Executive Approval**

Final delivery is formally approved by the CEO as executive sponsor
and the Compliance Officer as regulatory authority. Both signatures
must be present on the Approvals page (Section 14) before the
engagement is officially closed.

---

*Note: If KPI targets are not achieved within the 6-month window
due to timeline delays caused by documented risks (R-01 through
R-06), the measurement timeline will be extended by mutual
agreement between the BA and the CEO rather than the engagement
being considered unsuccessful. Target revision requires formal
sign-off from the CEO.*


---

## 14. Approvals

By signing below, each stakeholder confirms they have reviewed
this Business Requirements Document and agree that it accurately
represents the scope, objectives, requirements, and success
criteria for the LendFast Conversion Optimisation engagement.

Approval signifies agreement to:
- The project scope as defined in Section 4
- The functional and non-functional requirements in Sections 9 and 10
- The KPI targets and measurement methods in Section 11
- The acceptance criteria in Section 13

---

| Role | Name | Signature | Date |
|---|---|---|---|
| CEO (Executive Sponsor) | | | |
| Compliance Officer | | | |
| Finance Head | | | |
| Sales and Marketing Head | | | |
| Operations Head | | | |
| Lead BA | Geethika | | |

---

*This document is version 0.1 — Draft. It will be updated to
version 1.0 — Final upon receipt of all signatures above.*

*Document prepared by: [Your Name] — Junior BA/DA*
*Project: LendFast Conversion Optimisation Engagement*
*Date: August 2026*

