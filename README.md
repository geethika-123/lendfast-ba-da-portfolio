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

## What This Project Demonstrates

**Business Analysis skills:**
- Problem framing and hypothesis generation before data is examined
- Stakeholder analysis with influence and interest mapping
- Business Requirements Document (BRD) — 14 sections, production quality
- Functional and non-functional requirements with acceptance criteria
- User stories in Agile format mapped to functional requirements
- Risk analysis written from a BA perspective with mitigation and contingency
- KPI definition mapped to business objectives and stakeholder accountability

**Data Analysis skills** *(in progress — see project status below)*:
- Exploratory data analysis on application funnel data
- Step-level drop-off rate calculation
- Segmentation analysis by device type, employment status, and credit score band
- Hypothesis validation against real data
- Power BI dashboard for stakeholder reporting

---

## Deliverables

### Complete

| Document | Description |
|---|---|
| [Case Brief](01_problem_framing/case_brief.md) | Industry-grounded problem statement with real fintech abandonment statistics, nine hypotheses with testing methods, and pre-data recommendations |
| [Business Requirements Document](02_ba_documents/BRD_lendfast.md) | Full 14-section BRD covering objectives, scope, stakeholder register, functional and non-functional requirements, KPIs, risk summary, and acceptance criteria |
| [User Stories](02_ba_documents/user_stories.md) | Ten Agile user stories mapped to functional requirements, covering four distinct user types |

### In Progress

| Deliverable | Description |
|---|---|
| EDA Notebook | Python exploratory data analysis — funnel drop-off rates and segmentation |
| Segmentation Analysis | Drop-off rates by device type, employment status, credit score band |
| Gap Analysis Document | Current state vs future state with root cause breakdown |
| As-Is Process Flow | Seven-step application process mapped in current state |
| To-Be Process Flow | Redesigned process incorporating recommended improvements |
| Power BI Dashboard | Stakeholder-facing conversion funnel and KPI tracking dashboard |
| Impact Analysis | Business impact assessment of each recommended change |

---

## Project Structure

```
lendfast-ba-da-portfolio/
│
├── README.md
│
├── 01_problem_framing/
│   └── case_brief.md              # Problem statement, hypotheses, industry context
│
├── 02_ba_documents/
│   ├── BRD_lendfast.md            # Full Business Requirements Document
│   └── user_stories.md            # Agile user stories for all functional requirements
│
├── 03_data_analysis/              # Coming soon
│   ├── lendfast_data.csv
│   ├── EDA_lendfast.ipynb
│   └── segmentation_analysis.ipynb
│
├── 04_process_flows/              # Coming soon
│   ├── asis_process_flow.png
│   └── tobe_process_flow.png
│
├── 05_requirements/               # Coming soon
│   └── gap_analysis.md
│
├── 06_impact_risk/                # Coming soon
│   └── impact_analysis.md
│
└── 07_dashboard/                  # Coming soon
    ├── lendfast_dashboard.pbix
    └── dashboard_screenshot.png
```

---

## The Analytical Approach

This project follows the correct BA sequence — hypotheses before data,
problem framing before solutions, stakeholder alignment before
requirements.

Nine hypotheses were developed before any data was examined:

- **Primary:** Step 6 (document upload) has the highest single-step
  drop-off rate driven by document unavailability and trust concerns
- **Primary:** Mobile users complete at significantly lower rates than
  desktop users
- **Primary:** Self-employed users abandon at Steps 2 and 3 at higher
  rates than employed users
- **Primary:** Poor and fair credit score users drop off at Step 5
  due to fear of hard credit inquiry impact
- **Secondary:** Higher loan amounts correlate with higher Step 4
  drop-off due to fear of rejection

Each hypothesis has a defined test method and confirmation threshold.
EDA findings will either confirm or reject each one — and recommendations
will only be finalised after confirmation.

This approach prevents the most common BA mistake: building solutions
for the wrong problem.

---

## Industry Context

This case is grounded in real fintech data:

- Average fintech onboarding abandonment rate: **63%** (Signicat, 2025)
- Financial institutions losing clients to complex onboarding: **70%**
  (Fenergo, 2025)
- Annual cost of abandoned KYC processes globally: **$3.3 billion**
  (Fenergo, 2025)
- Titan (fintech): improved onboarding completion from **31% to 78%**
  after UX redesign

LendFast is a fictional company. The problem, the data structure,
and the analytical approach reflect real challenges faced by digital
lending platforms today.

---

## Project Status

| Phase | Status |
|---|---|
| Problem framing and hypothesis generation | ✅ Complete |
| Business Requirements Document | ✅ Complete |
| User Stories | ✅ Complete |
| SQL revision and EDA preparation | 🔄 In progress |
| Data generation and EDA | ⏳ Upcoming |
| Process flows and gap analysis | ⏳ Upcoming |
| Power BI dashboard | ⏳ Upcoming |

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


---

*This project is actively being developed. The BA documentation
phase is complete. The DA phase begins following SQL revision.*
