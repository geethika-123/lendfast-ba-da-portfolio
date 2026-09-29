# UAT Test Cases
## LendFast — Application Conversion Optimisation Engagement

---

| Field | Detail |
|---|---|
| Document Title | User Acceptance Testing — Test Cases |
| Project Name | LendFast Application Conversion Optimisation |
| Version | 0.1 — Draft |
| Status | In Progress |
| Prepared By | Geethika Vissapragada |
| Date | September 2026 |
| BRD Reference | BRD_lendfast.md — Section 9 |

---

## About This Document

This document contains UAT test cases for the LendFast application
conversion optimisation project. Test cases are written by the BA
and executed by designated UAT testers — business representatives
and end user proxies — not by the development or QA team.

UAT validates that delivered functionality meets business requirements
as defined in the BRD. It is the final gate before go-live.

---

## UAT Scope

The following functional requirements are in scope for UAT:

| FR | Requirement | Primary UAT Stakeholder |
|---|---|---|
| FR-01 | Pre-application document checklist | Operations / End user representative |
| FR-02 | Document upload validation and error messaging | Operations / End user representative |
| FR-03 | Session progress save | End user representative |
| FR-04 | Credit check transparency message | Compliance Officer |
| FR-05 | Compliance and licence badges at Step 6 | Compliance Officer |
| FR-06 | Proactive chat support trigger | Operations / End user representative |
| FR-08 | Self-employed user pathway | Self-employed user representative |
| FR-09 | Incomplete applicant re-engagement notification | Marketing team |
| FR-10 | Application progress indicator | End user representative |

**Out of UAT scope:**
FR-07 (Telemetry data capture) — validated through technical
testing by QA and Data Engineering teams. Not a user-facing
feature requiring business stakeholder sign-off.

---

## Severity Definitions

| Severity | Definition | Go-live Impact |
|---|---|---|
| Critical | System completely broken for this scenario. User cannot proceed. Business process blocked or regulatory violation. | Blocks go-live — fix immediately |
| High | Major functionality broken. Significant user impact. Workaround may exist but is not acceptable for production. | Fix before go-live |
| Medium | Functionality partially works. User experience degraded but core process still functions. | Fix before go-live — lower urgency |
| Low | Minor issue. Minimal user impact. Cosmetic or edge case. | Log and fix in future release |

---

## Test Case Format

Each test case contains:
- **Test ID** — unique identifier in format UAT-FR[XX]-[NNN]
- **Requirement Reference** — FR number being tested
- **Test Type** — Happy Path / Negative Path / Edge Case
- **Test Scenario** — specific situation being tested
- **Preconditions** — conditions that must be true before test runs
- **Test Steps** — numbered actions the tester performs
- **Expected Result** — what the system must do
- **Actual Result** — filled during test execution
- **Pass / Fail** — filled during test execution
- **Severity** — filled only if test fails
- **Defects Detected** — defect ID if raised
- **Requirement Tracing** — acceptance criteria reference from BRD

---

## FR-01: Pre-Application Document Checklist

**Requirement:** The system must display a checklist of all required
documents and information before the user begins the application.
The Start Application button must not be accessible until the user
has acknowledged the checklist.

**Acceptance Criteria Reference:** AC-01a — BRD Section 9, FR-01

**Requirements Clarification Note:** AC-01a requires the complete
checklist to be "fully displayed and acknowledged" but does not
specify how the system ensures all items are viewed before
acknowledgement on mobile devices. This gap was identified during
UAT test case design and should be resolved with the development
team before implementation begins. Recommendation: implement a
scroll-to-confirm mechanism on mobile where the acknowledgement
option activates only after the user has scrolled through all items.

---

### UAT-FR01-001 — Happy Path (Desktop)

| Field | Detail |
|---|---|
| Test ID | UAT-FR01-001 |
| Requirement Reference | FR-01 |
| Test Type | Happy Path |
| Test Scenario | A registered user navigates to the loan application page on desktop. The document checklist is displayed before the Start Application button. User acknowledges the checklist and proceeds to Step 1. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has not previously started an application. FR-01 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast application on desktop browser
2. Log in with registered user credentials
3. Navigate to the loan application page
4. Observe the screen before clicking anything
5. Click the Start Application button without acknowledging the checklist
6. Acknowledge the checklist by clicking the acknowledgement checkbox
7. Click the Start Application button

**Expected Result:**
- Document checklist is displayed on page load before Start Application button is accessible
- Start Application button is non-functional or greyed out before checklist acknowledgement (Step 5)
- After acknowledgement, Start Application button becomes active and navigates user to Step 1 (Step 7)

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-01a — BRD Section 9, FR-01 |
| Tester Name | |
| Test Date | |

---

### UAT-FR01-002 — Negative Path (Desktop)

| Field | Detail |
|---|---|
| Test ID | UAT-FR01-002 |
| Requirement Reference | FR-01 |
| Test Type | Negative Path |
| Test Scenario | A registered user attempts to proceed to the application without acknowledging the document checklist. The system must prevent access to Step 1. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has not previously started an application. FR-01 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast application on desktop browser
2. Log in with registered user credentials
3. Navigate to the loan application page
4. Observe the screen before clicking anything
5. Click the Start Application button without acknowledging the checklist

**Expected Result:**
- Document checklist is displayed on page load
- Start Application button remains non-functional when checklist is not acknowledged
- Clicking the Start Application button without acknowledgement produces no navigation — user remains on the checklist page
- Button remains visually inactive (greyed out or disabled)

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-01a — BRD Section 9, FR-01 |
| Tester Name | |
| Test Date | |

---

### UAT-FR01-003 — Edge Case (Acknowledgement Trigger Failure)

| Field | Detail |
|---|---|
| Test ID | UAT-FR01-003 |
| Requirement Reference | FR-01 |
| Test Type | Edge Case |
| Test Scenario | A registered user correctly acknowledges the checklist but the Start Application button fails to activate due to a system trigger failure. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has not previously started an application. FR-01 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate to the loan application page
4. Observe the document checklist displayed
5. Acknowledge the checklist by clicking the acknowledgement checkbox or button
6. Observe the Start Application button state
7. Attempt to click Start Application button

**Expected Result:**
- After acknowledging the checklist, Start Application button becomes active and functional
- If button remains inactive after acknowledgement, this constitutes a defect — system has failed to register the acknowledgement trigger correctly

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-01a — BRD Section 9, FR-01 |
| Tester Name | |
| Test Date | |

---

### UAT-FR01-004 — Edge Case (Mobile Rendering)

| Field | Detail |
|---|---|
| Test ID | UAT-FR01-004 |
| Requirement Reference | FR-01 |
| Test Type | Edge Case |
| Test Scenario | A registered mobile user navigates to the loan application page. The document checklist items may be hidden below the fold. The system must ensure all items are visible and acknowledged before the Start Application button becomes accessible. |
| Preconditions | User is registered with valid credentials. User is accessing from a mobile device. User has not previously started an application. FR-01 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on mobile browser or mobile device
2. Log in with registered credentials
3. Navigate to the loan application page
4. Without scrolling, observe how many checklist items are visible on screen
5. Note whether all items are visible or whether some are hidden below the fold
6. Scroll down to verify if remaining items appear
7. Acknowledge the checklist
8. Attempt to click Start Application button

**Expected Result:**
- All checklist items are visible to the user either without scrolling or through a scroll-to-confirm mechanism
- The acknowledgement option activates only after the user has viewed all checklist items
- Start Application button becomes accessible only after acknowledgement of the complete checklist
- If any items are hidden and acknowledgement is possible without viewing them, this constitutes a defect

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-01a — BRD Section 9, FR-01 |
| Tester Name | |
| Test Date | |

---

## FR-02 through FR-10: Test Cases

*To be completed. Test cases for FR-02, FR-03, FR-04, FR-05,
FR-06, FR-08, FR-09, and FR-10 follow the same structure as
FR-01 above. Each requirement requires a minimum of:*

- *One happy path test case*
- *One negative path test case*
- *One or more edge cases based on requirement complexity*

*FR-02, FR-06, and FR-10 require separate mobile test cases
given EDA confirmation that mobile users complete at 12.1%
versus desktop at 29.0% — a 16.9pp gap concentrated at
document upload and form completion steps.*

---

## UAT Sign-off

The following stakeholders must sign off before go-live is approved:

| Stakeholder | Role | Signature | Date |
|---|---|---|---|
| CEO | Executive Sponsor | | |
| Compliance Officer | Regulatory Authority | | |
| Operations Head | Business Representative | | |
| Marketing Head | Re-engagement Owner | | |
| BA Lead | Geethika Vissapragada | | |

---

*Document version: 0.1 — Draft*
*Prepared by: Geethika Vissapragada*
*Project: LendFast Conversion Optimisation Engagement*
*Status: In Progress — FR-01 complete, FR-02 through FR-10 pending*

---

## FR-02: Document Upload Validation and Error Messaging

**Requirement:** The system must verify document format, display
upload progress and status. If upload fails, the system must
display the reason for failure and next steps the user can take
to successfully upload the documents.

**Acceptance Criteria References:**
- AC-02a — Successful upload confirmation — BRD Section 9, FR-02
- AC-02b — Failed upload error message and next steps — BRD Section 9, FR-02

---

### UAT-FR02-001 — Happy Path (Desktop)

| Field | Detail |
|---|---|
| Test ID | UAT-FR02-001 |
| Requirement Reference | FR-02 |
| Test Type | Happy Path |
| Test Scenario | A user at Step 6 uploads a document in the correct format and within the size limit. The system displays upload progress and a success confirmation. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has successfully completed Steps 1 to 5 and is on the document upload screen. A valid PDF or accepted format file under the maximum file size limit is available for upload. FR-02 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate through Steps 1 to 5 using valid test data to reach the document upload screen at Step 6
4. Click the upload button
5. Upload the document with correct format and size
6. Check the status of the display message
7. Proceed to the next step

**Expected Result:**
- Upload progress indicator is displayed while document is uploading
- After successful upload, a confirmation message is displayed indicating the document was received
- The uploaded document name or thumbnail is visible
- Next step button becomes active

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-02a — BRD Section 9, FR-02 |
| Tester Name | |
| Test Date | |

---

### UAT-FR02-002 — Negative Path 1 (Wrong File Format)

| Field | Detail |
|---|---|
| Test ID | UAT-FR02-002 |
| Requirement Reference | FR-02 |
| Test Type | Negative Path |
| Test Scenario | A user at Step 6 uploads a document in an incorrect file format. The system must display a clear error message stating the format is invalid and provide next steps. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has successfully completed Steps 1 to 5. An invalid file format (e.g. .exe or .txt) is available for upload. FR-02 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate through Steps 1 to 5 using valid test data to reach the document upload screen at Step 6
4. Click the upload button
5. Upload a document with incorrect file format
6. Check the status of the display message

**Expected Result:**
- An error message stating the document does not meet format requirements is displayed
- Error message includes specific next steps — for example accepted file formats
- Next step button remains inactive

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-02b — BRD Section 9, FR-02 |
| Tester Name | |
| Test Date | |

---

### UAT-FR02-003 — Negative Path 2 (File Too Large)

| Field | Detail |
|---|---|
| Test ID | UAT-FR02-003 |
| Requirement Reference | FR-02 |
| Test Type | Negative Path |
| Test Scenario | A user at Step 6 uploads a document that exceeds the maximum file size limit. The system must display a clear error message stating the file is too large and provide next steps. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has successfully completed Steps 1 to 5. A valid format file exceeding the maximum file size limit is available for upload. FR-02 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate through Steps 1 to 5 using valid test data to reach the document upload screen at Step 6
4. Click the upload button
5. Upload a document that exceeds the maximum file size
6. Check the status of the display message

**Expected Result:**
- An error message stating the document does not meet size requirements is displayed
- Error message includes specific next steps — for example the maximum file size allowed
- Next step button remains inactive

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-02b — BRD Section 9, FR-02 |
| Tester Name | |
| Test Date | |

---

### UAT-FR02-004 — Edge Case 1 (Success Without Confirmation Message)

| Field | Detail |
|---|---|
| Test ID | UAT-FR02-004 |
| Requirement Reference | FR-02 |
| Test Type | Edge Case |
| Test Scenario | A user at Step 6 successfully uploads a document in correct format and size but receives no confirmation message. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has successfully completed Steps 1 to 5. A valid PDF or accepted format file under the maximum file size limit is available for upload. FR-02 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate through Steps 1 to 5 using valid test data to reach the document upload screen at Step 6
4. Click the upload button
5. Upload the document with correct format and size
6. Check if any display message appears

**Expected Result:**
- A message confirming the document was successfully received must be displayed
- If no message displays, this constitutes a defect — UI functionality is not behaving as intended
- Next step button becomes active

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-02a — BRD Section 9, FR-02 |
| Tester Name | |
| Test Date | |

---

### UAT-FR02-005 — Edge Case 2 (Failure Without Error Message)

| Field | Detail |
|---|---|
| Test ID | UAT-FR02-005 |
| Requirement Reference | FR-02 |
| Test Type | Edge Case |
| Test Scenario | A user at Step 6 uploads an incorrect document (wrong format or size) but receives no error message or reason for failure. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has successfully completed Steps 1 to 5. An invalid file (wrong format or exceeding size limit) is available for upload. FR-02 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate through Steps 1 to 5 using valid test data to reach the document upload screen at Step 6
4. Click the upload button
5. Upload an incorrect document
6. Check if any display message appears
7. Attempt to proceed to next step

**Expected Result:**
- Document upload fails and a message stating the reason for failure must be displayed
- If no message displays, this constitutes a defect — UI functionality is not behaving as intended
- Next step button remains inactive

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-02b — BRD Section 9, FR-02 |
| Tester Name | |
| Test Date | |

---

### UAT-FR02-006 — Edge Case 3 (Network Dropout Mid-Upload)

| Field | Detail |
|---|---|
| Test ID | UAT-FR02-006 |
| Requirement Reference | FR-02 |
| Test Type | Edge Case |
| Test Scenario | A user at Step 6 begins uploading a valid document but loses network connectivity mid-upload. The system must display a network error message and allow retry. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser or mobile device. User has successfully completed Steps 1 to 5. A valid PDF file is available for upload. FR-02 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser or mobile
2. Log in with registered credentials
3. Navigate through Steps 1 to 5 using valid test data to reach the document upload screen at Step 6
4. Click the upload button
5. Begin uploading a valid document
6. Simulate network dropout during upload by disabling wifi or network connection while upload is in progress

**Expected Result:**
- Document upload fails and a message stating "network error" or "connection lost" is displayed
- System allows the user to retry uploading the document once connection is restored
- Next step button remains inactive until a successful upload is confirmed

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-02b — BRD Section 9, FR-02 |
| Tester Name | |
| Test Date | |


---

## FR-03: Session Progress Save

**Requirement:** The system must save user progress when an error
occurs or session times out so that the user can resume from the
same point after restarting the session.

**Acceptance Criteria Reference:** AC-03a — BRD Section 9, FR-03

**Requirements Clarification Note:** FR-03 does not specify expected
system behaviour when a user has two concurrent active sessions on
different devices. For this UAT, the agreed expected behaviour is
"latest save wins" — the most recent session save overwrites the
earlier one. This should be confirmed with the development team
before implementation begins.

**Dependency Note:** UAT-FR03-005 (edge case — incorrect step
restored) relies on FR-07 telemetry data being implemented and
accessible to verify exact save timestamps. FR-07 must be
deployed in the UAT environment before this test case can be executed.

---

### UAT-FR03-001 — Happy Path (Normal Progression)

| Field | Detail |
|---|---|
| Test ID | UAT-FR03-001 |
| Requirement Reference | FR-03 |
| Test Type | Happy Path |
| Test Scenario | A user progresses through the application normally. Session is saved after each step. User can resume from the last completed step after closing and reopening the application. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. FR-03 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate to the loan application page
4. Complete Step 1 and proceed to Step 2
5. Close the browser without logging out
6. Reopen LendFast and log in again
7. Navigate to the loan application page
8. Observe which step the application resumes from

**Expected Result:**
- Application resumes from Step 2 — the last completed step
- All data entered in Step 1 is retained and pre-populated
- User does not need to re-enter any previously completed information

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-03a — BRD Section 9, FR-03 |
| Tester Name | |
| Test Date | |

---

### UAT-FR03-002 — Negative Path 1 (Network Failure — Save Trigger Fails)

| Field | Detail |
|---|---|
| Test ID | UAT-FR03-002 |
| Requirement Reference | FR-03 |
| Test Type | Negative Path |
| Test Scenario | A network failure occurs while the user is filling the application. The session save trigger fails and progress is lost. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has partially completed the application. FR-03 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Complete Steps 1 and 2 with valid data
4. Simulate network failure by disabling wifi or network connection
5. Attempt to proceed to Step 3
6. Restore network connection
7. Log in again and navigate to the application page
8. Observe which step the application resumes from

**Expected Result:**
- If save trigger functioned correctly — application resumes from Step 2 with all data retained
- If save trigger failed — application restarts from Step 1 with no data retained. This constitutes a defect — network failure must not cause loss of previously saved progress
- Owner: Network engineering team

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-03a — BRD Section 9, FR-03 |
| Tester Name | |
| Test Date | |

---

### UAT-FR03-003 — Negative Path 2 (Application Closure — Save Trigger Fails)

| Field | Detail |
|---|---|
| Test ID | UAT-FR03-003 |
| Requirement Reference | FR-03 |
| Test Type | Negative Path |
| Test Scenario | The application closes unexpectedly while the user is filling it. The session save trigger fails and progress is lost. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has partially completed the application. FR-03 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Complete Steps 1 and 2 with valid data
4. Force close the browser abruptly (without normal logout)
5. Reopen LendFast and log in again
6. Navigate to the loan application page
7. Observe which step the application resumes from

**Expected Result:**
- If save trigger functioned correctly — application resumes from Step 2 with all data retained
- If save trigger failed — application restarts from Step 1. This constitutes a defect — abrupt closure must not cause loss of previously saved progress
- Owner: Frontend / Backend development team

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-03a — BRD Section 9, FR-03 |
| Tester Name | |
| Test Date | |

---

### UAT-FR03-004 — Negative Path 3 (Session Timeout — Save Trigger Fails)

| Field | Detail |
|---|---|
| Test ID | UAT-FR03-004 |
| Requirement Reference | FR-03 |
| Test Type | Negative Path |
| Test Scenario | The user's session times out due to inactivity. The session save trigger fails and progress is lost upon return. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has partially completed the application. Session timeout threshold is known and documented. FR-03 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Complete Steps 1 and 2 with valid data
4. Leave the application inactive until session timeout is triggered
5. Log in again after timeout
6. Navigate to the loan application page
7. Observe which step the application resumes from

**Expected Result:**
- If save trigger functioned correctly — application resumes from Step 2 with all data retained
- If save trigger failed — application restarts from Step 1. This constitutes a defect — session timeout must not cause loss of previously saved progress
- Owner: Backend development team

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-03a — BRD Section 9, FR-03 |
| Tester Name | |
| Test Date | |

---

### UAT-FR03-005 — Edge Case 1 (Incorrect Step or Data Restored)

| Field | Detail |
|---|---|
| Test ID | UAT-FR03-005 |
| Requirement Reference | FR-03 |
| Test Type | Edge Case |
| Test Scenario | Session is saved but upon resumption the user is placed at an incorrect step or some previously entered data is missing. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has completed at least two steps. FR-03 and FR-07 (telemetry) are both deployed in UAT environment. Telemetry logs are accessible for verification. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Complete Steps 1, 2, and 3 with valid test data — note exact data entered
4. Close the browser
5. Check telemetry logs to confirm save timestamp and step number recorded
6. Reopen LendFast and log in again
7. Navigate to the loan application page
8. Compare the step the application resumes from against the telemetry log
9. Verify all data entered in Steps 1, 2, and 3 is correctly pre-populated

**Expected Result:**
- Application resumes from Step 4 — the next incomplete step
- All data entered in Steps 1, 2, and 3 is correctly pre-populated
- Telemetry log confirms the save was triggered at the correct step and timestamp
- If step or data does not match telemetry record, this constitutes a defect

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-03a — BRD Section 9, FR-03 |
| Tester Name | |
| Test Date | |

---

### UAT-FR03-006 — Edge Case 2 (Two Concurrent Sessions — Latest Save Wins)

| Field | Detail |
|---|---|
| Test ID | UAT-FR03-006 |
| Requirement Reference | FR-03 |
| Test Type | Edge Case |
| Test Scenario | The same user has two active sessions on different devices simultaneously. Both sessions save progress. The latest save must overwrite the earlier one without data corruption. |
| Preconditions | User is registered with valid credentials. User has access to two different devices (e.g. desktop and mobile). FR-03 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on Device 1 (desktop) and log in
2. Complete Steps 1 and 2 on Device 1
3. Without closing Device 1, open LendFast on Device 2 (mobile) and log in with same credentials
4. Complete Steps 1, 2, and 3 on Device 2 — using different data values to distinguish the sessions
5. Close both devices
6. Reopen LendFast on any device and log in
7. Observe which step and which data the application resumes from

**Expected Result:**
- Application resumes from Step 4 — reflecting the Device 2 session which progressed further
- Data pre-populated matches Device 2 entries — latest save wins
- No data corruption or mixing of data between sessions
- If application resumes from Device 1 state or shows mixed data, this constitutes a defect

**Requirements Clarification Note:** Latest save wins behaviour must
be confirmed with the development team before implementation.
FR-03 does not currently specify concurrent session handling.

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-03a — BRD Section 9, FR-03 |
| Tester Name | |
| Test Date | |


---

## FR-04: Credit Check Transparency Message

**Requirement:** The system must display a message stating that
only a soft credit pull is conducted and the user's credit score
will not be affected, before the credit check consent checkbox
is presented at Step 5.

**Acceptance Criteria Reference:** AC-04a — BRD Section 9, FR-04

**Primary UAT Stakeholder:** Compliance Officer — must verify
exact wording of the transparency message before go-live.
Incorrect disclosure language constitutes a regulatory violation
under the Truth in Lending Act (TILA).

**Critical Note:** Any defect where the transparency message
displays incorrect information — stating a hard credit check
will be conducted or that the user's credit score will be
affected — is classified as Critical severity and blocks
go-live immediately.

---

### UAT-FR04-001 — Happy Path

| Field | Detail |
|---|---|
| Test ID | UAT-FR04-001 |
| Requirement Reference | FR-04 |
| Test Type | Happy Path |
| Test Scenario | A registered user reaches Step 5 of the application. A transparency message stating that only a soft credit pull will be conducted and the user's credit score will not be affected is displayed before the consent checkbox. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has successfully completed Steps 1 to 4. FR-04 feature is deployed in UAT environment. Compliance Officer has approved the exact wording of the transparency message. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate through Steps 1 to 4 using valid test data
4. Observe Step 5 screen before interacting with anything
5. Read the transparency message displayed
6. Verify the consent checkbox is positioned after the message
7. Check the consent checkbox and proceed to Step 6

**Expected Result:**
- A transparency message is displayed before the consent checkbox stating that only a soft credit pull will be conducted
- The message explicitly states the user's credit score will not be affected
- Consent checkbox is positioned after the message — not before it
- After checking the consent checkbox, user can proceed to Step 6

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-04a — BRD Section 9, FR-04 |
| Tester Name | |
| Test Date | |

---

### UAT-FR04-002 — Negative Path (Consent Checkbox Without Transparency Message)

| Field | Detail |
|---|---|
| Test ID | UAT-FR04-002 |
| Requirement Reference | FR-04 |
| Test Type | Negative Path |
| Test Scenario | A registered user reaches Step 5 and is presented with the credit check consent checkbox without any transparency message being displayed. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has successfully completed Steps 1 to 4. FR-04 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate through Steps 1 to 4 using valid test data
4. Observe Step 5 screen before interacting with anything
5. Check whether a transparency message is displayed before the consent checkbox

**Expected Result:**
- Transparency message must be displayed before the consent checkbox is accessible
- If consent checkbox appears without the transparency message, this constitutes a defect — regulatory disclosure requirement is not met
- Compliance Officer must be notified immediately if this defect is found

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | High |
| Defects Detected | |
| Requirement Tracing | AC-04a — BRD Section 9, FR-04 |
| Tester Name | |
| Test Date | |

---

### UAT-FR04-003 — Edge Case 1 (Incorrect Message Content — Critical)

| Field | Detail |
|---|---|
| Test ID | UAT-FR04-003 |
| Requirement Reference | FR-04 |
| Test Type | Edge Case |
| Test Scenario | A registered user reaches Step 5 and a transparency message is displayed but contains incorrect information — stating a hard credit check will be conducted or that the user's credit score will be affected. |
| Preconditions | User is registered with valid credentials. User has successfully completed Steps 1 to 4. FR-04 feature is deployed in UAT environment. Compliance Officer approved message wording is documented for comparison. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate through Steps 1 to 4 using valid test data
4. Observe Step 5 screen
5. Read the transparency message displayed in full
6. Compare exact wording against the Compliance Officer approved message text

**Expected Result:**
- Transparency message matches the Compliance Officer approved wording exactly
- Message states only a soft credit pull is conducted
- Message states the user's credit score will not be affected
- If message states a hard credit check or that the score will be affected, this constitutes a Critical defect — regulatory violation under TILA — go-live is blocked immediately

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | Critical — if incorrect wording is displayed |
| Defects Detected | |
| Requirement Tracing | AC-04a — BRD Section 9, FR-04 |
| Tester Name | |
| Test Date | |

---

### UAT-FR04-004 — Edge Case 2 (Page Refresh Bypasses Transparency Message)

| Field | Detail |
|---|---|
| Test ID | UAT-FR04-004 |
| Requirement Reference | FR-04 |
| Test Type | Edge Case |
| Test Scenario | A user at Step 5 encounters a page load error or session timeout. Upon refreshing the page, the consent checkbox is displayed directly without the transparency message. |
| Preconditions | User is registered with valid credentials. User has successfully completed Steps 1 to 4 and is at Step 5. FR-04 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate through Steps 1 to 4 using valid test data
4. Reach Step 5
5. Simulate page load error by refreshing the browser or triggering a session timeout
6. Observe Step 5 screen after page reload

**Expected Result:**
- After page refresh or session restoration, transparency message must be displayed before the consent checkbox
- Consent checkbox must not be accessible without the transparency message on any page load — including refreshes
- If consent checkbox appears without message after refresh, this constitutes a defect

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-04a — BRD Section 9, FR-04 |
| Tester Name | |
| Test Date | |

---

### UAT-FR04-005 — Edge Case 3 (Message Truncated or Not Fully Visible on Mobile)

| Field | Detail |
|---|---|
| Test ID | UAT-FR04-005 |
| Requirement Reference | FR-04 |
| Test Type | Edge Case |
| Test Scenario | A mobile user reaches Step 5 and the transparency message is truncated, cut off, or not fully visible on the mobile screen. The user cannot read the complete message before being presented with the consent checkbox. |
| Preconditions | User is registered with valid credentials. User is accessing from a mobile device. User has successfully completed Steps 1 to 4. FR-04 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on mobile browser or mobile device
2. Log in with registered credentials
3. Navigate through Steps 1 to 4 using valid test data
4. Reach Step 5 and observe the screen without scrolling
5. Check whether the complete transparency message is visible
6. If message is cut off, scroll down to check if remaining text appears
7. Verify consent checkbox is positioned after the complete message

**Expected Result:**
- Complete transparency message is visible on mobile — either without scrolling or through a clearly indicated scroll mechanism
- Consent checkbox appears only after the complete message is visible and readable
- If message is truncated and consent checkbox is accessible before complete message is read, this constitutes a defect

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-04a — BRD Section 9, FR-04 |
| Tester Name | |
| Test Date | |


---

## FR-05: Compliance and Licence Badges at Step 6

**Requirement:** The system must display the company's regulatory
compliance certifications and government-approved licence information
before the user can access the document upload button at Step 6.

**Acceptance Criteria Reference:** AC-05a — BRD Section 9, FR-05

**Primary UAT Stakeholder:** Compliance Officer — must verify
that correct licence numbers, valid certifications, and accurate
regulatory claims are displayed. Incorrect or expired licence
information constitutes a false regulatory claim.

**Critical Note:** Any defect where an incorrect licence number,
expired certification, or false regulatory claim is displayed
is classified as Critical severity and blocks go-live immediately.

---

### UAT-FR05-001 — Happy Path

| Field | Detail |
|---|---|
| Test ID | UAT-FR05-001 |
| Requirement Reference | FR-05 |
| Test Type | Happy Path |
| Test Scenario | A registered user reaches Step 6. Company regulatory compliance badges and government-approved licence information are displayed before the document upload button is accessible. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has successfully completed Steps 1 to 5. FR-05 feature is deployed in UAT environment. Compliance Officer has verified and approved the licence numbers and certification details to be displayed. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate through Steps 1 to 5 using valid test data
4. Observe Step 6 screen before interacting with anything
5. Verify compliance badges and licence information are displayed
6. Compare displayed licence number and certification details against Compliance Officer approved reference document
7. Attempt to click the upload button
8. Verify upload button is accessible after badges are displayed

**Expected Result:**
- Regulatory compliance badges and government-approved licence information are displayed on page load at Step 6
- Displayed licence number and certification details match the Compliance Officer approved reference exactly
- Upload button is accessible after badges are displayed
- User can proceed to upload documents

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-05a — BRD Section 9, FR-05 |
| Tester Name | |
| Test Date | |

---

### UAT-FR05-002 — Negative Path 1 (Upload Button Accessible Without Badges)

| Field | Detail |
|---|---|
| Test ID | UAT-FR05-002 |
| Requirement Reference | FR-05 |
| Test Type | Negative Path |
| Test Scenario | A registered user reaches Step 6 and the document upload button is accessible without any compliance badges or licence information being displayed. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has successfully completed Steps 1 to 5. FR-05 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate through Steps 1 to 5 using valid test data
4. Observe Step 6 screen before interacting with anything
5. Check whether compliance badges and licence information are displayed
6. Attempt to click the upload button without badges being visible

**Expected Result:**
- Compliance badges and licence information must be displayed before the upload button is accessible
- If upload button is accessible without badges being displayed, this constitutes a defect — trust signals are missing at the highest risk abandonment point
- Compliance Officer must be notified immediately

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | High |
| Defects Detected | |
| Requirement Tracing | AC-05a — BRD Section 9, FR-05 |
| Tester Name | |
| Test Date | |

---

### UAT-FR05-003 — Negative Path 2 (Badge-Upload Button Relationship Failure)

| Field | Detail |
|---|---|
| Test ID | UAT-FR05-003 |
| Requirement Reference | FR-05 |
| Test Type | Negative Path |
| Test Scenario | Compliance badges display correctly but the upload button remains blocked or inaccessible even after badges are fully displayed. The badge-to-button activation relationship has failed. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has successfully completed Steps 1 to 5. FR-05 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate through Steps 1 to 5 using valid test data
4. Observe Step 6 screen
5. Verify compliance badges are fully displayed
6. Attempt to click the upload button after badges have loaded
7. Observe whether upload button responds

**Expected Result:**
- After compliance badges are fully displayed, upload button must become active and accessible
- If upload button remains inactive after badges have loaded, this constitutes a defect — badge-to-button activation trigger has failed
- Owner: Frontend development team

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-05a — BRD Section 9, FR-05 |
| Tester Name | |
| Test Date | |

---

### UAT-FR05-004 — Edge Case 1 (Wrong Licence Number, Expired Certification, or Broken Badge Image)

| Field | Detail |
|---|---|
| Test ID | UAT-FR05-004 |
| Requirement Reference | FR-05 |
| Test Type | Edge Case |
| Test Scenario | A registered user reaches Step 6 and compliance badges display but contain incorrect information — wrong licence number, expired certification date, or broken badge images. |
| Preconditions | User is registered with valid credentials. User has successfully completed Steps 1 to 5. FR-05 feature is deployed in UAT environment. Compliance Officer approved reference document with correct licence numbers and valid certification dates is available for comparison. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate through Steps 1 to 5 using valid test data
4. Observe Step 6 screen
5. Check each compliance badge and licence detail against the Compliance Officer approved reference document
6. Verify certification dates are current and not expired
7. Verify all badge images load correctly without broken image icons

**Expected Result:**
- All licence numbers match the Compliance Officer approved reference exactly
- All certification dates are current and valid
- All badge images load correctly without broken image icons
- Any mismatch in licence number or expired certification constitutes a Critical defect — false regulatory claim, go-live blocked immediately
- Broken badge image constitutes a High severity defect — trust signal is missing

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | Critical — wrong licence or expired cert / High — broken image |
| Defects Detected | |
| Requirement Tracing | AC-05a — BRD Section 9, FR-05 |
| Tester Name | |
| Test Date | |

---

### UAT-FR05-005 — Edge Case 2 (Page Refresh Bypasses Badges)

| Field | Detail |
|---|---|
| Test ID | UAT-FR05-005 |
| Requirement Reference | FR-05 |
| Test Type | Edge Case |
| Test Scenario | A user at Step 6 encounters a page load error or session timeout. Upon refreshing, the upload button is displayed directly without compliance badges being shown. |
| Preconditions | User is registered with valid credentials. User has successfully completed Steps 1 to 5 and is at Step 6. FR-05 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate through Steps 1 to 5 using valid test data
4. Reach Step 6
5. Simulate page load error by refreshing the browser or triggering a session timeout
6. Observe Step 6 screen after page reload
7. Check whether compliance badges are displayed before upload button

**Expected Result:**
- After page refresh or session restoration, compliance badges must be displayed before the upload button is accessible
- Upload button must not be accessible on any page load — including refreshes — without badges being displayed first
- If upload button appears without badges after refresh, this constitutes a defect

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-05a — BRD Section 9, FR-05 |
| Tester Name | |
| Test Date | |

---

### UAT-FR05-006 — Edge Case 3 (Badges Broken or Not Visible on Mobile)

| Field | Detail |
|---|---|
| Test ID | UAT-FR05-006 |
| Requirement Reference | FR-05 |
| Test Type | Edge Case |
| Test Scenario | A mobile user reaches Step 6 and compliance badges either fail to load, display as broken images, or are not fully visible on the mobile screen. |
| Preconditions | User is registered with valid credentials. User is accessing from a mobile device. User has successfully completed Steps 1 to 5. FR-05 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on mobile browser or mobile device
2. Log in with registered credentials
3. Navigate through Steps 1 to 5 using valid test data
4. Reach Step 6 and observe the screen
5. Check whether all compliance badges load correctly without broken image icons
6. Check whether all badge text and licence information is fully visible on the mobile screen
7. Scroll if necessary to verify complete badge visibility
8. Attempt to access the upload button

**Expected Result:**
- All compliance badges load correctly on mobile without broken image icons
- All badge text and licence information is fully readable on the mobile screen
- Upload button is accessible only after badges are fully visible
- Broken badge images on mobile constitute a High severity defect
- Badge text cut off or not readable on mobile constitutes a Medium severity defect

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-05a — BRD Section 9, FR-05 |
| Tester Name | |
| Test Date | |


---

## FR-06: Proactive Chat Support Trigger

**Requirement:** The system must display a proactive chat support
prompt when a user is inactive for more than 60 seconds at any
application step. A help button must also be visible at all times
allowing users to initiate chat on demand.

**Acceptance Criteria References:**
- AC-06a — Proactive trigger: chat prompt appears after 60 seconds
  inactivity — BRD Section 9, FR-06
- AC-06b — Reactive trigger: chat prompt appears when help button
  is clicked — BRD Section 9, FR-06

**Primary UAT Stakeholder:** Operations Head and End User
Representative.

**Requirements Clarification Note 1 — Chat Support Type:**
FR-06 does not specify whether chat support is live human,
bot-only, or hybrid. Agreed implementation for LendFast is
Option C — bot first with option to escalate to a human agent
on request. Development team must confirm this architecture
before implementation begins.

**Requirements Clarification Note 2 — Escalation Chain:**
FR-06 does not define the resolution path when neither the bot
nor a human agent can resolve a user's issue. Recommended
minimum: offer a callback or email follow-up with a reference
number. This operational process must be defined before go-live.

---

### UAT-FR06-001 — Happy Path 1 (Proactive Trigger — 60 Second Inactivity)

| Field | Detail |
|---|---|
| Test ID | UAT-FR06-001 |
| Requirement Reference | FR-06 |
| Test Type | Happy Path |
| Test Scenario | A registered user pauses or remains inactive for more than 60 seconds at any application step. A chat support prompt is displayed offering assistance. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has started the application and is at any step. FR-06 feature is deployed in UAT environment. Chat support (bot with human escalation) is active and available. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate to any application step
4. Stop all interactions and remain inactive for 65 seconds
5. Observe whether a chat support prompt appears
6. Interact with the chat prompt
7. Verify chat is functional and responsive

**Expected Result:**
- A chat support prompt appears after 60 seconds of inactivity
- Prompt offers assistance relevant to the current step
- Chat is functional — bot responds to user queries
- Option to escalate to human agent is available on request
- User can dismiss the prompt and continue the application without disruption

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-06a — BRD Section 9, FR-06 |
| Tester Name | |
| Test Date | |

---

### UAT-FR06-002 — Happy Path 2 (Reactive Trigger — Help Button)

| Field | Detail |
|---|---|
| Test ID | UAT-FR06-002 |
| Requirement Reference | FR-06 |
| Test Type | Happy Path |
| Test Scenario | A registered user clicks the help button at any application step. A chat support prompt is displayed immediately offering assistance. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has started the application and is at any step. FR-06 feature is deployed in UAT environment. Chat support is active and available. Help button is visible on screen. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate to any application step
4. Locate the help button on screen
5. Click the help button
6. Observe whether chat prompt appears immediately
7. Interact with the chat prompt
8. Verify chat is functional and responsive

**Expected Result:**
- Help button is visible at all times during the application
- Chat prompt appears immediately upon clicking the help button
- Chat is functional — bot responds to user queries
- Option to escalate to human agent is available on request
- User can dismiss the chat and continue the application

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-06b — BRD Section 9, FR-06 |
| Tester Name | |
| Test Date | |

---

### UAT-FR06-003 — Negative Path 1 (Chat Prompt Fails to Display After Inactivity)

| Field | Detail |
|---|---|
| Test ID | UAT-FR06-003 |
| Requirement Reference | FR-06 |
| Test Type | Negative Path |
| Test Scenario | A registered user remains inactive for more than 60 seconds at an application step but no chat support prompt appears. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has started the application and is at any step. FR-06 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate to any application step
4. Stop all interactions and remain inactive for 90 seconds
5. Observe whether a chat support prompt appears

**Expected Result:**
- Chat support prompt must appear within 60 seconds of inactivity
- If no prompt appears after 90 seconds of inactivity, this constitutes a defect — proactive trigger has failed
- Users at high-friction steps (Steps 2, 3, and 6) are at highest risk of abandonment without proactive support

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | High |
| Defects Detected | |
| Requirement Tracing | AC-06a — BRD Section 9, FR-06 |
| Tester Name | |
| Test Date | |

---

### UAT-FR06-004 — Negative Path 2 (Chat Prompt Fails to Display on Help Button Click)

| Field | Detail |
|---|---|
| Test ID | UAT-FR06-004 |
| Requirement Reference | FR-06 |
| Test Type | Negative Path |
| Test Scenario | A registered user clicks the help button at any application step but no chat prompt appears. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has started the application and is at any step. FR-06 feature is deployed in UAT environment. Help button is visible on screen. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate to any application step
4. Click the help button
5. Observe whether a chat prompt appears

**Expected Result:**
- Chat prompt must appear immediately upon clicking the help button
- If no prompt appears after clicking help button, this constitutes a defect — reactive trigger has failed
- User has no support mechanism available — abandonment risk increases

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | High |
| Defects Detected | |
| Requirement Tracing | AC-06b — BRD Section 9, FR-06 |
| Tester Name | |
| Test Date | |

---

### UAT-FR06-005 — Edge Case 1 (Bot Fails to Resolve Issue — Human Escalation)

| Field | Detail |
|---|---|
| Test ID | UAT-FR06-005 |
| Requirement Reference | FR-06 |
| Test Type | Edge Case |
| Test Scenario | A user interacts with the chat bot but the bot is unable to provide a correct answer or resolve the user's issue. The system must offer escalation to a human agent. |
| Preconditions | User is registered with valid credentials. User has started the application and is at any step. FR-06 feature is deployed in UAT environment. Chat bot and human escalation are both active. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate to any application step
4. Trigger chat support via inactivity or help button
5. Submit a query that the bot cannot resolve — for example a complex income verification question
6. Observe whether the bot offers escalation to a human agent
7. Request human agent escalation
8. Verify human agent joins the chat

**Expected Result:**
- When bot cannot resolve the issue, an option to escalate to a human agent is offered
- Human agent joins the chat within a defined response time
- If bot fails to offer escalation or human agent is unavailable with no alternative offered,
  this constitutes a defect
- Minimum acceptable fallback: offer callback or email follow-up with reference number

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-06b — BRD Section 9, FR-06 |
| Tester Name | |
| Test Date | |

---

### UAT-FR06-006 — Edge Case 2 (Chat Trigger Fires During Active User Interaction)

| Field | Detail |
|---|---|
| Test ID | UAT-FR06-006 |
| Requirement Reference | FR-06 |
| Test Type | Edge Case |
| Test Scenario | The proactive chat prompt appears while the user is actively typing or interacting with a form field — not during a genuine pause. The trigger fires incorrectly and interrupts the user. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User is actively filling a form field at any application step. FR-06 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate to any application step with a text input field
4. Begin typing slowly in a form field — pausing between keystrokes
5. Continue slow interaction for 65 seconds without fully stopping
6. Observe whether chat prompt appears during active interaction

**Expected Result:**
- Chat prompt must not appear while the user is actively interacting with any form field
- 60-second inactivity timer must reset on any user interaction — including keystrokes, mouse movements, and field clicks
- If chat prompt appears during active interaction, this constitutes a defect — proactive trigger logic is incorrectly calibrated

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | Medium |
| Defects Detected | |
| Requirement Tracing | AC-06a — BRD Section 9, FR-06 |
| Tester Name | |
| Test Date | |

---

### UAT-FR06-007 — Edge Case 3 (Chat Prompt Obscures Form Fields on Mobile)

| Field | Detail |
|---|---|
| Test ID | UAT-FR06-007 |
| Requirement Reference | FR-06 |
| Test Type | Edge Case |
| Test Scenario | A mobile user encounters the proactive chat prompt which obscures form fields or cannot be easily dismissed, creating additional friction instead of reducing it. |
| Preconditions | User is registered with valid credentials. User is accessing from a mobile device. User has started the application and is at any step. FR-06 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on mobile browser or mobile device
2. Log in with registered credentials
3. Navigate to any application step
4. Remain inactive for 65 seconds to trigger proactive chat prompt
5. Observe whether the chat prompt obscures any form fields
6. Attempt to dismiss the chat prompt
7. Verify form fields are fully accessible after dismissing the prompt

**Expected Result:**
- Chat prompt on mobile must not obscure active form fields
- Chat prompt must be easily dismissable with a single tap
- After dismissing the prompt, all form fields must be fully accessible and no data previously entered must be lost
- If prompt obscures fields or cannot be dismissed easily, this constitutes a Medium severity defect

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-06a — BRD Section 9, FR-06 |
| Tester Name | |
| Test Date | |


---

## FR-08: Self-Employed User Pathway

**Requirement:** The system must display a separate pathway at
Step 2 for self-employed users with fields appropriate to their
employment situation — business name, income type, income range,
and supporting documentation guidance — instead of standard
employer name, job title, and fixed salary fields.

**Acceptance Criteria Reference:** AC-08a — BRD Section 9, FR-08

**Primary UAT Stakeholder:** Self-employed user representative.

**Note:** FR-08 covers Step 2 only. Step 3 income verification
for self-employed users is addressed separately. Verification
of whether a user is genuinely self-employed cannot be validated
at the point of form submission — this is confirmed during
downstream loan processing when documents are reviewed.

**EDA Evidence:** Self-employed users abandon at Step 2 at 32.6%
versus 9.8% for employed users — a 22.8pp gap confirming H2.
FR-08 is elevated from provisional low priority to confirmed
high priority based on this finding.

---

### UAT-FR08-001 — Happy Path

| Field | Detail |
|---|---|
| Test ID | UAT-FR08-001 |
| Requirement Reference | FR-08 |
| Test Type | Happy Path |
| Test Scenario | A registered self-employed user reaches Step 2. A separate self-employed subsection is displayed with relevant fields. User completes self-employed fields and proceeds to Step 3. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has successfully completed Step 1. Employment status selected as self-employed. FR-08 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Complete Step 1 with valid personal details
4. Reach Step 2 and select self-employed as employment status
5. Observe whether a separate self-employed subsection appears
6. Verify self-employed fields are displayed — business name, income type, income range, documentation guidance
7. Verify standard employed fields — employer name, job title, fixed salary — are not displayed or are disabled
8. Complete all self-employed fields with valid test data
9. Proceed to Step 3

**Expected Result:**
- Selecting self-employed triggers a separate subsection with fields relevant to self-employment
- Standard employed fields are not displayed or are disabled when self-employed is selected
- All required self-employed fields are present — business name, income type, income range
- User can complete self-employed fields and proceed to Step 3 without friction

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-08a — BRD Section 9, FR-08 |
| Tester Name | |
| Test Date | |

---

### UAT-FR08-002 — Negative Path (Incomplete Employment Details)

| Field | Detail |
|---|---|
| Test ID | UAT-FR08-002 |
| Requirement Reference | FR-08 |
| Test Type | Negative Path |
| Test Scenario | A registered user reaches Step 2 and attempts to proceed without completing either the employed or self-employed subsection. The system must prevent progression until one complete subsection is filled. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has successfully completed Step 1. FR-08 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Complete Step 1 with valid personal details
4. Reach Step 2
5. Leave all employment fields empty
6. Attempt to proceed to Step 3

**Expected Result:**
- System prevents progression to Step 3 when no employment subsection is completed
- An error message or validation prompt is displayed indicating that employment details must be provided
- User remains on Step 2 until at least one complete subsection is filled

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | High |
| Defects Detected | |
| Requirement Tracing | AC-08a — BRD Section 9, FR-08 |
| Tester Name | |
| Test Date | |

---

### UAT-FR08-003 — Edge Case 1 (Self-Employed Pathway Not Displayed)

| Field | Detail |
|---|---|
| Test ID | UAT-FR08-003 |
| Requirement Reference | FR-08 |
| Test Type | Edge Case |
| Test Scenario | A self-employed user reaches Step 2 and selects self-employed as employment status but only the standard employed subsection is displayed. No separate self-employed pathway appears. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has successfully completed Step 1. FR-08 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Complete Step 1 with valid personal details
4. Reach Step 2 and select self-employed as employment status
5. Observe whether a self-employed subsection appears
6. Check whether only the standard employed section is displayed

**Expected Result:**
- Selecting self-employed must trigger the self-employed subsection
- If only standard employed fields appear with no self-employed pathway, this constitutes a defect — the conditional display logic has failed
- Self-employed users are forced into fields that do not reflect their situation — replicating the exact friction H2 confirmed

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | High |
| Defects Detected | |
| Requirement Tracing | AC-08a — BRD Section 9, FR-08 |
| Tester Name | |
| Test Date | |

---

### UAT-FR08-004 — Edge Case 2 (Wrong or Missing Fields in Self-Employed Section)

| Field | Detail |
|---|---|
| Test ID | UAT-FR08-004 |
| Requirement Reference | FR-08 |
| Test Type | Edge Case |
| Test Scenario | The self-employed subsection displays but contains wrong fields — such as employer name or employer details — instead of the correct self-employment fields like business name and income type. Or required self-employment fields are missing entirely. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has successfully completed Step 1. FR-08 feature is deployed in UAT environment. Reference list of required self-employed fields is documented for comparison. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Complete Step 1 with valid personal details
4. Reach Step 2 and select self-employed as employment status
5. Observe which fields are displayed in the self-employed subsection
6. Compare displayed fields against the required self-employed field list — business name, income type, income range, documentation guidance
7. Check whether any standard employed fields — employer name, job title, fixed salary — appear in the self-employed subsection

**Expected Result:**
- Self-employed subsection displays: business name, income type, income range, and documentation guidance
- Standard employed fields — employer name, job title, fixed salary — do not appear in the self-employed subsection
- If wrong fields appear or required fields are missing, this constitutes a High severity defect — self-employed users cannot accurately represent their situation

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | High — if wrong or missing fields |
| Defects Detected | |
| Requirement Tracing | AC-08a — BRD Section 9, FR-08 |
| Tester Name | |
| Test Date | |

---

### UAT-FR08-005 — Edge Case 3 (Both Subsections Simultaneously Active)

| Field | Detail |
|---|---|
| Test ID | UAT-FR08-005 |
| Requirement Reference | FR-08 |
| Test Type | Edge Case |
| Test Scenario | A user selects self-employed at Step 2 but both the employed and self-employed subsections remain active and editable simultaneously — allowing the user to fill fields in both sections. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser or mobile device. User has successfully completed Step 1. FR-08 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Complete Step 1 with valid personal details
4. Reach Step 2 and select self-employed as employment status
5. Observe whether the employed subsection is disabled or hidden
6. Attempt to enter data in the employed subsection fields
7. Check whether the system allows data entry in both subsections simultaneously

**Expected Result:**
- Selecting self-employed must disable or hide the employed subsection
- User must not be able to enter data in both subsections simultaneously
- If both subsections remain active, this constitutes a defect — conditional display logic has failed and data integrity is at risk
- Particularly important on mobile where rendering issues may cause both sections to appear active

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | Medium |
| Defects Detected | |
| Requirement Tracing | AC-08a — BRD Section 9, FR-08 |
| Tester Name | |
| Test Date | |


---

## FR-09: Incomplete Applicant Re-Engagement Notification

**Requirement:** When a user abandons the application without
completing it, the system must send a targeted re-engagement
notification within 24 hours to encourage the user to return
and complete the application.

**Acceptance Criteria Reference:** AC-09a — BRD Section 9, FR-09

**Primary UAT Stakeholder:** Marketing Team — owns re-engagement
campaign performance and KPI-05.

**Requirements Clarification Note:** FR-09 does not specify how
the system distinguishes between user-initiated abandonment and
session termination due to technical failure. The system must
not trigger re-engagement notifications for sessions that ended
due to technical failure — only for genuine user-initiated
abandonment. Development team must define the detection mechanism
before implementation begins.

---

### UAT-FR09-001 — Happy Path (Abandonment Triggers Email Within 24 Hours)

| Field | Detail |
|---|---|
| Test ID | UAT-FR09-001 |
| Requirement Reference | FR-09 |
| Test Type | Happy Path |
| Test Scenario | A registered user starts the application and abandons it intentionally by closing the browser or navigating away. A re-engagement email is triggered and delivered within 24 hours. |
| Preconditions | User is registered with a valid email address. User has started but not completed the application. FR-09 feature is deployed in UAT environment. Email delivery system is active. Test email monitoring tool is available to verify receipt. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Start the loan application and complete at least one step
4. Close the browser or navigate away from the application intentionally
5. Wait 24 hours
6. Check the registered email inbox for a re-engagement notification

**Expected Result:**
- A re-engagement email is delivered to the user's registered email address within 24 hours of abandonment
- Email content is relevant to the step at which the user abandoned
- Email contains a direct link to resume the application
- Email does not trigger if the user completes the application before the 24-hour window

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-09a — BRD Section 9, FR-09 |
| Tester Name | |
| Test Date | |

---

### UAT-FR09-002 — Negative Path (Email Delivery Failure)

| Field | Detail |
|---|---|
| Test ID | UAT-FR09-002 |
| Requirement Reference | FR-09 |
| Test Type | Negative Path |
| Test Scenario | The system correctly detects user abandonment and triggers the re-engagement notification but the email fails to deliver — due to an invalid email address, bounced delivery, or spam filter blocking. |
| Preconditions | User is registered with an invalid or test email address that will cause delivery failure. User has abandoned the application. FR-09 feature is deployed in UAT environment. Email delivery logs are accessible. |

**Test Steps:**

1. Register a test user with an invalid or bounced email address
2. Start the loan application and complete at least one step
3. Abandon the application intentionally
4. Wait 24 hours
5. Check email delivery logs to confirm whether the system detected abandonment and triggered the notification
6. Verify delivery status in the email system logs

**Expected Result:**
- System detects abandonment and triggers the notification correctly
- Email delivery fails due to invalid address or bounce
- System logs the delivery failure with a timestamp and reason
- Failed delivery is flagged for review — Marketing team should be notified of undeliverable addresses
- If system neither detects abandonment nor logs a delivery attempt, this constitutes a defect

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | Medium |
| Defects Detected | |
| Requirement Tracing | AC-09a — BRD Section 9, FR-09 |
| Tester Name | |
| Test Date | |

---

### UAT-FR09-003 — Edge Case 1 (User Returns and Completes Within 24 Hours)

| Field | Detail |
|---|---|
| Test ID | UAT-FR09-003 |
| Requirement Reference | FR-09 |
| Test Type | Edge Case |
| Test Scenario | A user abandons the application but returns and completes it within the 24-hour notification window. No re-engagement email must be triggered since the application is now complete. |
| Preconditions | User is registered with a valid email address. User has abandoned the application. FR-09 feature is deployed in UAT environment. Test email monitoring tool is available. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Start the loan application and complete at least one step
4. Abandon the application intentionally
5. Return to the application within 12 hours and complete all seven steps
6. Wait 24 hours from the original abandonment
7. Check the registered email inbox

**Expected Result:**
- No re-engagement email is triggered after the user completes the application
- System must cancel the scheduled notification when completion is detected
- If a re-engagement email is delivered after completion, this constitutes a defect

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | Medium |
| Defects Detected | |
| Requirement Tracing | AC-09a — BRD Section 9, FR-09 |
| Tester Name | |
| Test Date | |

---

### UAT-FR09-004 — Edge Case 2 (No Email Triggered After 24 Hours)

| Field | Detail |
|---|---|
| Test ID | UAT-FR09-004 |
| Requirement Reference | FR-09 |
| Test Type | Edge Case |
| Test Scenario | A user genuinely abandons the application but no re-engagement email is triggered or delivered within 24 hours. |
| Preconditions | User is registered with a valid email address. User has abandoned the application. FR-09 feature is deployed in UAT environment. Test email monitoring tool is available. Email delivery logs are accessible. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Start the loan application and complete at least one step
4. Abandon the application intentionally
5. Wait 26 hours
6. Check registered email inbox
7. Check email delivery logs to determine whether a notification was triggered

**Expected Result:**
- Re-engagement email must be delivered within 24 hours of abandonment
- If no email is received after 26 hours and delivery logs show no trigger, this constitutes a defect — re-engagement system has failed to detect abandonment or schedule the notification

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | High |
| Defects Detected | |
| Requirement Tracing | AC-09a — BRD Section 9, FR-09 |
| Tester Name | |
| Test Date | |

---

### UAT-FR09-005 — Edge Case 3 (Email Triggers Due to Technical Glitch)

| Field | Detail |
|---|---|
| Test ID | UAT-FR09-005 |
| Requirement Reference | FR-09 |
| Test Type | Edge Case |
| Test Scenario | A user's session ends due to a technical failure — server error, network drop, or system crash — not due to intentional abandonment. A re-engagement email is incorrectly triggered. |
| Preconditions | User is registered with a valid email address. User has an active application session. FR-09 feature is deployed in UAT environment. Backend session logs are accessible to distinguish technical failure from user-initiated closure. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Start the loan application and complete at least one step
4. Simulate a technical failure — server error or forced network disconnection
5. Wait 24 hours
6. Check registered email inbox
7. Check backend session logs to confirm the session ended due to technical failure

**Expected Result:**
- No re-engagement email must be triggered when session ended due to technical failure
- Backend logs must distinguish between technical failure and user-initiated abandonment
- If re-engagement email is triggered for a technically-failed session, this constitutes a defect — system cannot distinguish user behaviour from technical failure
- This gap must be resolved through backend session event logging before FR-09 is deployed

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | Medium |
| Defects Detected | |
| Requirement Tracing | AC-09a — BRD Section 9, FR-09 |
| Tester Name | |
| Test Date | |

---

### UAT-FR09-006 — Edge Case 4 (Multiple Emails Triggered Within 24 Hours)

| Field | Detail |
|---|---|
| Test ID | UAT-FR09-006 |
| Requirement Reference | FR-09 |
| Test Type | Edge Case |
| Test Scenario | A user abandons the application and receives multiple re-engagement emails within the 24-hour window due to a trigger duplication error. |
| Preconditions | User is registered with a valid email address. User has abandoned the application. FR-09 feature is deployed in UAT environment. Test email monitoring tool is available. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Start the loan application and complete at least one step
4. Abandon the application intentionally
5. Wait 24 hours
6. Check registered email inbox for number of re-engagement emails received

**Expected Result:**
- Exactly one re-engagement email must be delivered within the 24-hour window
- If more than one email is received, this constitutes a defect — trigger duplication error
- Multiple emails create user frustration and erode trust in the platform

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | Medium |
| Defects Detected | |
| Requirement Tracing | AC-09a — BRD Section 9, FR-09 |
| Tester Name | |
| Test Date | |

---

### UAT-FR09-007 — Edge Case 5 (Email Triggers After Application Completion)

| Field | Detail |
|---|---|
| Test ID | UAT-FR09-007 |
| Requirement Reference | FR-09 |
| Test Type | Edge Case |
| Test Scenario | A user completes the full application but still receives a re-engagement email — potentially causing confusion about whether the application was successfully submitted. |
| Preconditions | User is registered with a valid email address. User has successfully completed and submitted the application. FR-09 feature is deployed in UAT environment. Test email monitoring tool is available. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Complete all seven steps of the application and submit
4. Wait 24 hours
5. Check registered email inbox for any re-engagement notification

**Expected Result:**
- No re-engagement email must be triggered for a completed and submitted application
- If a re-engagement email is received after completion, this constitutes a Medium severity defect
- Mitigation: if this defect is found, add a note to the email stating "please ignore this notification if you have already completed your application" before go-live as a temporary workaround

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | Medium — if email triggers after completion |
| Defects Detected | |
| Requirement Tracing | AC-09a — BRD Section 9, FR-09 |
| Tester Name | |
| Test Date | |


---

## FR-10: Application Progress Indicator

**Requirement:** The system must display a progress indicator
throughout the application showing the user's current step and
total steps remaining. The indicator must be visible on all
device types and update in real time as the user progresses
through each step.

**Acceptance Criteria Reference:** AC-10a — BRD Section 9, FR-10

**Primary UAT Stakeholder:** End User Representative.

---

### UAT-FR10-001 — Happy Path

| Field | Detail |
|---|---|
| Test ID | UAT-FR10-001 |
| Requirement Reference | FR-10 |
| Test Type | Happy Path |
| Test Scenario | A registered user progresses through the application from Step 1 to Step 7. The progress indicator is visible at every step and updates correctly in real time as the user advances. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. FR-10 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate to the loan application page
4. Observe the progress indicator at Step 1
5. Complete Step 1 and proceed to Step 2
6. Observe the progress indicator updates to reflect Step 2
7. Continue through Steps 3 to 7 — observing the indicator at each step
8. Submit the application at Step 7
9. Observe the final state of the progress indicator

**Expected Result:**
- Progress indicator is visible at every step from Step 1 to Step 7
- Indicator correctly reflects the current step number and total steps remaining at each stage
- Indicator updates in real time as user advances to each new step
- At Step 7 submission, indicator reflects completion of all steps

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-10a — BRD Section 9, FR-10 |
| Tester Name | |
| Test Date | |

---

### UAT-FR10-002 — Negative Path 1 (Progress Indicator Fails to Display)

| Field | Detail |
|---|---|
| Test ID | UAT-FR10-002 |
| Requirement Reference | FR-10 |
| Test Type | Negative Path |
| Test Scenario | A registered user progresses through the application but the progress indicator fails to display at any step. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. FR-10 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate to the loan application page
4. Observe the screen at Step 1 for the presence of a progress indicator
5. Complete Step 1 and proceed to Step 2
6. Observe whether a progress indicator is present at Step 2

**Expected Result:**
- Progress indicator must be visible at every step
- If no progress indicator is displayed at any step, this constitutes a defect — the feature has failed to render
- Users cannot gauge remaining application length — abandonment risk increases

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | Medium |
| Defects Detected | |
| Requirement Tracing | AC-10a — BRD Section 9, FR-10 |
| Tester Name | |
| Test Date | |

---

### UAT-FR10-003 — Negative Path 2 (Progress Indicator Shows Wrong Step)

| Field | Detail |
|---|---|
| Test ID | UAT-FR10-003 |
| Requirement Reference | FR-10 |
| Test Type | Negative Path |
| Test Scenario | A registered user progresses through the application and the progress indicator displays but shows an incorrect step number — for example showing Step 3 when the user is actually on Step 5. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. FR-10 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Navigate to the loan application page
4. Complete Steps 1 through 4 using valid test data
5. Reach Step 5
6. Observe the progress indicator and verify it shows Step 5

**Expected Result:**
- Progress indicator must show the correct current step number at every stage
- If indicator shows a step number different from the actual current step, this constitutes a defect — real-time update logic has failed
- Incorrect step display misleads users about their progress and may cause premature abandonment

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | Medium |
| Defects Detected | |
| Requirement Tracing | AC-10a — BRD Section 9, FR-10 |
| Tester Name | |
| Test Date | |

---

### UAT-FR10-004 — Edge Case 1 (Wrong Step Displayed After Page Reload or Session Timeout)

| Field | Detail |
|---|---|
| Test ID | UAT-FR10-004 |
| Requirement Reference | FR-10 |
| Test Type | Edge Case |
| Test Scenario | A user at Step 5 encounters a page reload or session timeout. Upon returning, the progress indicator resets to Step 1 or shows an incorrect step despite the user's session being saved correctly. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has completed Steps 1 to 4 and is at Step 5. FR-10 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Complete Steps 1 to 4 using valid test data and reach Step 5
4. Note the current step shown on the progress indicator
5. Refresh the page or simulate a session timeout
6. Log in again and navigate to the application
7. Observe the step shown on the progress indicator after returning

**Expected Result:**
- Progress indicator must correctly reflect the last completed step after page reload or session restoration
- If indicator resets to Step 1 or shows a step other than Step 5, this constitutes a defect — persistence failure between the session save and the progress indicator
- Note: this test case is dependent on FR-03 session save being correctly implemented

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | Medium |
| Defects Detected | |
| Requirement Tracing | AC-10a — BRD Section 9, FR-10 |
| Tester Name | |
| Test Date | |

---

### UAT-FR10-005 — Edge Case 2 (Progress Indicator Fails to Update on Backward Navigation)

| Field | Detail |
|---|---|
| Test ID | UAT-FR10-005 |
| Requirement Reference | FR-10 |
| Test Type | Edge Case |
| Test Scenario | A user on Step 5 navigates backwards to Step 3 to correct previously entered information. The progress indicator remains at Step 5 instead of updating to reflect the user's current position at Step 3. |
| Preconditions | User is registered with valid credentials. User is accessing from a desktop browser. User has completed Steps 1 to 5. FR-10 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on desktop browser
2. Log in with registered credentials
3. Complete Steps 1 to 5 using valid test data
4. Note the progress indicator shows Step 5
5. Navigate backwards to Step 3 using the back button or step navigation
6. Observe the progress indicator after landing on Step 3

**Expected Result:**
- Progress indicator must update to reflect the user's current position when navigating backwards
- If indicator remains at Step 5 while user is on Step 3, this constitutes a defect — real-time update logic does not handle backward navigation
- Note: indicator should reflect current position not highest completed step —
  this distinction must be confirmed with development team before implementation

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | Low |
| Defects Detected | |
| Requirement Tracing | AC-10a — BRD Section 9, FR-10 |
| Tester Name | |
| Test Date | |

---

### UAT-FR10-006 — Edge Case 3 (Progress Indicator Rendering on Mobile)

| Field | Detail |
|---|---|
| Test ID | UAT-FR10-006 |
| Requirement Reference | FR-10 |
| Test Type | Edge Case |
| Test Scenario | A mobile user progresses through the application but the progress indicator is not visible, is partially hidden, or does not render correctly on a mobile screen. |
| Preconditions | User is registered with valid credentials. User is accessing from a mobile device. FR-10 feature is deployed in UAT environment. |

**Test Steps:**

1. Open LendFast on mobile browser or mobile device
2. Log in with registered credentials
3. Navigate to the loan application page
4. Observe the progress indicator at Step 1 — check visibility and correct rendering
5. Complete Step 1 and proceed to Step 2
6. Verify progress indicator updates correctly on mobile screen
7. Continue through at least three steps checking indicator visibility at each

**Expected Result:**
- Progress indicator is fully visible on mobile screen without being cut off or hidden
- Indicator updates correctly on mobile as user progresses through steps
- If indicator is not visible or does not render correctly on mobile, this constitutes a Medium severity defect — mobile users who cannot see their progress are at higher abandonment risk

| Field | Detail |
|---|---|
| Actual Result | |
| Pass / Fail | |
| Severity | |
| Defects Detected | |
| Requirement Tracing | AC-10a — BRD Section 9, FR-10 |
| Tester Name | |
| Test Date | |

---

## UAT Sign-off

The following stakeholders must sign off on UAT completion
before go-live is approved. Sign-off confirms that all test
cases in scope have been executed, all Critical and High
severity defects have been resolved, and the delivered
solution meets the business requirements as defined in the BRD.

| Stakeholder | Role | Signature | Date |
|---|---|---|---|
| CEO | Executive Sponsor | | |
| Compliance Officer | Regulatory Authority | | |
| Operations Head | Business Representative | | |
| Marketing Head | Re-engagement Owner | | |
| BA Lead | Geethika Vissapragada | | |

---

*Document version: 1.0 — Complete*
*Prepared by: Geethika Vissapragada*
*Project: LendFast Conversion Optimisation Engagement*
*Status: Complete — FR-01 through FR-10 (excluding FR-07)*
*Total test cases: 54*

