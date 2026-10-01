# LendFast — Application Conversion Optimisation
### Business Analysis + Data Analysis Portfolio Project | Fintech

---

## The Business Problem

LendFast is a digital consumer lending startup that raised $12 million
in Series A funding and built a mobile-first personal loan platform.
Eighteen months after launch, the company had acquired 45,000 registered
users but was losing the majority of them before they completed a loan
application — directly suppressing revenue and failing to meet investor
growth expectations.

The CEO's initial hypothesis: the application is too long.

This project demonstrates how a structured BA and DA engagement
challenges that hypothesis, identifies the real root causes through
data analysis, and defines targeted requirements to close the
conversion gap.

---

## Key Findings

EDA confirmed the CEO's hypothesis was wrong. Application length
is not the primary driver of abandonment. The data revealed four
specific, addressable friction points:

| Finding | Metric | Status |
|---|---|---|
| Overall completion rate | 18.2% vs 37.0% industry benchmark | 18.8pp gap |
| Step 6 (Document Upload) drop-off | 66.8% — highest of any step | H4 Confirmed |
| Mobile vs desktop completion gap | 12.1% vs 29.0% — 16.9pp gap | H5 Confirmed |
| Self-employed vs employed gap at Step 2 | 32.6% vs 9.8% — 22.8pp gap | H2 Confirmed |
| Poor credit vs good credit at Step 5 | 28.6% vs 5.9% — 22.7pp gap | H3 Partially Confirmed |
| Loan amount effect on Step 4 | Flat across all ranges | H6 Rejected |

Step 6 alone accounts for 46.5% of all abandonment in the entire
funnel — 894 users lost at document upload out of 2,350 application
starts. The recommended interventions target this point directly.

---

## What This Project Demonstrates

**Business Analysis skills:**
- Problem framing and hypothesis generation before data is examined
- Stakeholder analysis with influence and interest mapping
- Business Requirements Document (BRD) — 14 sections, production quality
- Functional and non-functional requirements with measurable acceptance criteria
- User stories in Agile format mapped to functional requirements across four user types
- Gap analysis — current state vs future state across four dimensions
- Risk analysis written from a BA perspective with mitigation and contingency
- KPI definition mapped to six business objectives with stakeholder accountability
- UAT test cases — 54 test cases across nine functional requirements with severity definitions and requirements clarification notes

**Data Analysis skills:**
- Synthetic dataset generation — 2,350 records with realistic segment-based dropout probabilities
- Data quality assessment — eight checks including MNAR analysis, duplicate detection, and data leakage identification
- Funnel analysis — step-level drop-off rates and survival analysis
- Segmentation analysis — device type, employment status, credit score band, loan amount range
- Hypothesis validation — nine hypotheses tested and formally confirmed, rejected, or marked inconclusive
- Visualisation — funnel charts, segmentation bar charts, time distribution analysis

---

## Key Deliverables

| Document | Description | Status |
|---|---|---|
| [Case Brief](01_problem_framing/case_brief.md) | Industry-grounded problem statement, nine hypotheses, pre-data recommendations | ✅ Complete |
| [BRD](02_ba_documents/BRD_lendfast.md) | 14-section Business Requirements Document with EDA-updated baselines | ✅ Complete |
| [User Stories](02_ba_documents/user_stories.md) | 10 Agile user stories across four user types | ✅ Complete |
| [Gap Analysis](02_ba_documents/gap_analysis.md) | 7-section gap analysis with recommendations and prioritisation matrix | ✅ Complete |
| [UAT Test Cases](02_ba_documents/uat_test_cases.md) | 54 test cases across nine FRs with severity definitions | ✅ Complete |
| [EDA Notebook](03_data_analysis/EDA_lendfast.ipynb) | Python EDA — funnel analysis, segmentation, hypothesis validation | ✅ Complete |
| [Dataset](03_data_analysis/lendfast_applications.csv) | Synthetic dataset — 2,350 records, 12 columns | ✅ Complete |
| As-Is Process Flow | Current seven-step application process mapped in Draw.io | ⏳ Upcoming |
| To-Be Process Flow | Redesigned process incorporating recommendations | ⏳ Upcoming |
| Power BI Dashboard | Executive-facing conversion funnel and KPI tracking | ⏳ Upcoming |
| Impact Analysis | Business impact estimates per confirmed recommendation | ⏳ Upcoming |
| [Dashboard](https://datastudio.google.com/s/tvNzMVINxaY) | Looker Studio — 4 pages, executive summary, segmentation, KPI tracking, hypothesis scorecard | ✅ Complete |
---

## Project Structure

```
lendfast-ba-da-portfolio/
│
├── README.md
│
├── 01_problem_framing/
│   └── case_brief.md              # Problem statement, 9 hypotheses, industry context
│
├── 02_ba_documents/
│   ├── BRD_lendfast.md            # Full 14-section BRD — updated with EDA findings
│   ├── user_stories.md            # 10 Agile user stories across 4 user types
│   ├── gap_analysis.md            # 7-section gap analysis with prioritisation matrix
│   └── uat_test_cases.md          # 54 UAT test cases across 9 functional requirements
│
├── 03_data_analysis/
│   ├── lendfast_applications.csv  # Synthetic dataset — 2,350 records
│   └── EDA_lendfast.ipynb         # EDA notebook — funnel, segmentation, hypotheses
│
├── 04_process_flows/              # Upcoming
│   ├── asis_process_flow.png
│   └── tobe_process_flow.png
│
└── 07_dashboard/                  # Upcoming
    ├── lendfast_dashboard.pbix
    └── dashboard_screenshot.png
```

---

## The Analytical Approach

This project follows the correct BA sequence — hypotheses before data,
problem framing before solutions, stakeholder alignment before requirements.

Nine hypotheses were developed before any data was examined. Each had
a defined test method and confirmation threshold. EDA findings confirmed,
rejected, or marked inconclusive each hypothesis — and requirements were
only finalised after confirmation.

### Hypothesis Scorecard

| ID | Hypothesis | Outcome |
|---|---|---|
| H1 | Steps 2 and 3 have above-average drop-off | ✅ Confirmed |
| H2 | Self-employed users abandon more at Steps 2 and 3 | ✅ Confirmed — 22.8pp gap |
| H3 | Poor/fair credit users abandon more at Step 5 | ✅ Partially Confirmed |
| H4 | Step 6 has the highest single-step drop-off | ✅ Confirmed — 66.8% |
| H5 | Mobile users complete at lower rates than desktop | ✅ Confirmed — 16.9pp gap |
| H6 | Higher loan amounts drive Step 4 abandonment | ❌ Rejected — flat pattern |
| H7 | Seasonal variation in completion rates | ⚠ Inconclusive — insufficient data |
| H8 | Time on application as friction signal | ❌ Rejected — ambiguous signal |
| H9 | Technical performance as abandonment cause | 🔍 Cannot assess — telemetry required |

This approach prevents the most common BA mistake: building solutions
for the wrong problem.

---

## Top Three Recommendations

Based on confirmed EDA findings, three interventions are recommended
for immediate implementation:

**1. Pre-application document checklist (FR-01) and upload validation (FR-02)**
Step 6 loses 894 users — 46.5% of all abandonment. Users arrive at
document upload unprepared. A checklist before Step 1 and clear upload
feedback at Step 6 directly address the primary abandonment point.

**2. Self-employed user pathway (FR-08)**
Self-employed users abandon at Step 2 at 32.6% versus 9.8% for employed
users. Standard employer fields don't accommodate variable income.
An adaptive pathway recovers an estimated 120+ additional completions
from self-employed users alone.

**3. Credit check transparency message (FR-04)**
Poor credit users abandon at Step 5 at 28.6% versus 5.9% for good
credit users. A one-line message stating that only a soft credit pull
is conducted is a near-zero-cost intervention for a confirmed friction point.

---

## Industry Context

This case is grounded in real fintech research:

- Average fintech onboarding abandonment rate: **63%** (Signicat, 2025)
- Financial institutions losing clients to complex onboarding: **70%** (Fenergo, 2025)
- Annual cost of abandoned KYC processes globally: **$3.3 billion** (Fenergo, 2025)
- Titan (fintech): improved onboarding completion from **31% to 78%** after UX redesign

LendFast is a fictional company. The problem, the data structure,
and the analytical approach reflect real challenges faced by digital
lending platforms today.

---

## Project Status

| Phase | Status |
|---|---|
| Problem framing and hypothesis generation | ✅ Complete |
| Business Requirements Document (14 sections) | ✅ Complete |
| User Stories (10 stories, 4 user types) | ✅ Complete |
| Gap Analysis (7 sections, prioritisation matrix) | ✅ Complete |
| UAT Test Cases (54 cases, 9 FRs) | ✅ Complete |
| Synthetic dataset generation | ✅ Complete |
| EDA notebook — funnel and segmentation analysis | ✅ Complete |
| Hypothesis validation | ✅ Complete |
| As-Is and To-Be process flows | ⏳ Upcoming |
| Power BI dashboard | ✅ Complete |
| Impact analysis | ⏳ Upcoming |

---

## About

**Geethika Vissapragada**
Business Analyst | Data Analyst | AI for Industrial Operations

Background in mechanical engineering and power plant operations
(APGENCO, 2017–2021) with expertise in operational data analysis,
KPI dashboards, reliability metrics, and stakeholder reporting.
Transitioning into AI-focused BA and DA roles where industrial
domain knowledge is a differentiator.

- LinkedIn: [linkedin.com/in/geethika-vissapragada](https://www.linkedin.com/in/geethika-vissapragada/)
- Kaggle: [kaggle.com/geethika123](https://www.kaggle.com/geethika123)
- PowerOps AI Agent: [github.com/geethika-123/powerops-ai-agent](https://github.com/geethika-123/powerops-ai-agent)

