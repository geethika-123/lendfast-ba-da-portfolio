# User Stories
## LendFast — Application Conversion Optimisation Engagement

---

| Field | Detail |
|---|---|
| Document Title | User Stories |
| Project Name | LendFast Application Conversion Optimisation |
| Version | 1.0 |
| Status | Draft |
| Prepared By | Geethika |
| Date | August 2026 |
| BRD Reference | BRD_lendfast.md — Section 9 (Functional Requirements) |

---

## About This Document

User stories translate functional requirements into Agile-ready
sprint tasks written from the user's perspective. Each story
describes who needs something, what they need, and why it matters.

Acceptance criteria for each user story are defined in the BRD
Section 9 under the corresponding functional requirement reference.

Non-functional requirements (NFR-01 through NFR-06) are not
represented as user stories. They are enforced through Definition
of Done criteria applied to every sprint deliverable and through
dedicated technical backlog tasks for performance testing, security
audits, and accessibility compliance.

---

## User Types

| User Type | Description |
|---|---|
| Loan Applicant | A registered LendFast user completing a personal loan application |
| Self-Employed Applicant | A loan applicant whose employment status is self-employed |
| Data Analyst | Internal team member responsible for EDA and performance monitoring |
| Marketing Team Member | Internal team member managing re-engagement campaigns |

---

## User Stories

---

**US-01: Pre-Application Document Checklist**

| Field | Detail |
|---|---|
| FR Reference | FR-01 |
| Priority | High |
| Status | Confirmed |

*As a loan applicant,*
*I want to see a checklist of all required documents before I begin the application,*
*so that I can prepare all required documents in advance and complete the application without interruption.*

Notes: Checklist must be displayed and acknowledged before the Start Application button becomes accessible on all device types.

---

**US-02: Document Upload Validation and Error Messaging**

| Field | Detail |
|---|---|
| FR Reference | FR-02 |
| Priority | High |
| Status | Confirmed |

*As a loan applicant,*
*I want to see the upload status of my documents and receive a clear message if the upload fails,*
*so that I know immediately whether my upload was successful and what to do if it fails.*

Notes: Must cover both success and failure scenarios. Failure message must include specific reason and actionable next steps — not a generic error code.

---

**US-03: Session Progress Save**

| Field | Detail |
|---|---|
| FR Reference | FR-03 |
| Priority | High |
| Status | Confirmed |

*As a loan applicant,*
*I want my application progress to be automatically saved if my session ends unexpectedly,*
*so that I do not need to re-enter all my information if a technical glitch occurs or I need to reopen the application.*

Notes: Save must be triggered automatically — the user should not need to manually save. Progress must be fully restored on next login including all previously entered field values.

---

**US-04: Credit Check Transparency Message**

| Field | Detail |
|---|---|
| FR Reference | FR-04 |
| Priority | High |
| Status | Confirmed |

*As a loan applicant,*
*I want to see a clear message explaining how the credit check will be conducted before I give consent,*
*so that I am not worried about a hard credit inquiry negatively impacting my credit score.*

Notes: Message must appear before the consent checkbox at Step 5. Must clearly state that only a soft credit pull is conducted and credit score will not be affected.

---

**US-05: Compliance and Licence Badges**

| Field | Detail |
|---|---|
| FR Reference | FR-05 |
| Priority | High |
| Status | Confirmed |

*As a loan applicant,*
*I want to see LendFast's regulatory compliance certifications and government-approved licences before I upload my sensitive documents,*
*so that I feel confident my personal and financial information is protected and will not be misused.*

Notes: Badges must be visible at Step 6 before the upload button is accessible. Must include specific regulatory references — not generic trust language.

---

**US-06: Proactive Chat Support**

| Field | Detail |
|---|---|
| FR Reference | FR-06 |
| Priority | High |
| Status | Confirmed |

*As a loan applicant,*
*I want a chat support prompt to appear when I am struggling at any step,*
*so that I can get immediate help without having to search for a support contact and can continue my application with confidence.*

Notes: Proactive trigger activates after 60 seconds of inactivity at any step. Must also be available on-demand via a visible help button. Chat must be staffed or have an intelligent response system — not a dead link.

---

**US-07: Telemetry Data Capture**

| Field | Detail |
|---|---|
| FR Reference | FR-07 |
| Priority | High |
| Status | Confirmed |

*As a data analyst,*
*I want all user events, errors, and timestamps to be automatically captured and stored in a database throughout the application process,*
*so that I can conduct exploratory data analysis to identify friction points and validate hypotheses about user behaviour.*

Notes: Events must include step completions, field skips, page load errors, session timeouts, and upload failures. Each event must carry a user identifier and precise timestamp. Data must be accessible via the analytics dashboard.

---

**US-08: Self-Employed User Pathway**

| Field | Detail |
|---|---|
| FR Reference | FR-08 |
| Priority | Low |
| Status | Provisional — pending Hypothesis 2 validation |

*As a self-employed loan applicant,*
*I want to see fields that are relevant to my employment situation at Steps 2 and 3,*
*so that I can accurately represent my income and employment status without being forced to fit into fields designed for salaried employees.*

Notes: Pathway is triggered when user selects self-employed as employment status. Must replace standard employer name and fixed income fields with appropriate alternatives. Implementation pending EDA confirmation of Hypothesis 2.

---

**US-09: Incomplete Applicant Re-Engagement Notification**

| Field | Detail |
|---|---|
| FR Reference | FR-09 |
| Priority | High |
| Status | Provisional — pending segmentation analysis findings |

*As a marketing team member,*
*I want the system to automatically send targeted re-engagement notifications to users who abandoned the application,*
*so that we can recover incomplete applications and increase conversion without additional customer acquisition spend.*

Notes: Notification must only trigger when abandonment is user-initiated — not when a technical failure caused the session to end. Must be segmented by drop-off step and user type to enable personalised messaging. Implementation pending segmentation analysis findings.

---

**US-10: Application Progress Indicator**

| Field | Detail |
|---|---|
| FR Reference | FR-10 |
| Priority | Low |
| Status | Provisional — pending mobile drop-off confirmation |

*As a loan applicant,*
*I want to see a progress indicator showing how many steps I have completed and how many remain throughout the application,*
*so that I know how much of the application is left and feel confident enough to continue rather than abandon.*

Notes: Must be visible on all device types throughout the entire application journey. Must update in real time as the user progresses through each step. Implementation pending EDA confirmation of mobile drop-off hypothesis.

---

## User Stories Summary

| ID | Title | User Type | FR Reference | Priority | Status |
|---|---|---|---|---|---|
| US-01 | Pre-Application Document Checklist | Loan Applicant | FR-01 | High | Confirmed |
| US-02 | Document Upload Validation and Error Messaging | Loan Applicant | FR-02 | High | Confirmed |
| US-03 | Session Progress Save | Loan Applicant | FR-03 | High | Confirmed |
| US-04 | Credit Check Transparency Message | Loan Applicant | FR-04 | High | Confirmed |
| US-05 | Compliance and Licence Badges | Loan Applicant | FR-05 | High | Confirmed |
| US-06 | Proactive Chat Support | Loan Applicant | FR-06 | High | Confirmed |
| US-07 | Telemetry Data Capture | Data Analyst | FR-07 | High | Confirmed |
| US-08 | Self-Employed User Pathway | Self-Employed Applicant | FR-08 | Low | Provisional |
| US-09 | Incomplete Applicant Re-Engagement | Marketing Team Member | FR-09 | High | Provisional |
| US-10 | Application Progress Indicator | Loan Applicant | FR-10 | Low | Provisional |

---

*Document version: 1.0*
*Prepared by: Geethika
*Project: LendFast Conversion Optimisation Engagement*
*Status: Draft — pending stakeholder review*
