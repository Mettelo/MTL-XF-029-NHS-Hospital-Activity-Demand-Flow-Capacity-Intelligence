# MTL-XF-029 — NHS Hospital Activity, Demand, Flow & Capacity Pressure Intelligence

**Mettelo Project Studio** · Cross-Functional · Master project specification  
**Client:** Confidential NHS Hospital Planning & Service Transformation Directorate  
**Accountable simulated executive:** Director of Hospital Planning & Service Transformation  
**Sector:** NHS / Hospital Activity / Service Planning  
**Team:** 6–8 people · **Window:** 8 weeks  
**Status:** documentation revised; file acquisition and cohort freeze pending  
**Review cadence:** monthly hospital activity planning review

> This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

## Business setting

The simulated hospital planning and service-transformation directorate prepares a monthly activity review for elective and non-elective planning leads. Its first decision is which supported activity streams need a deeper operational evidence request before any capacity response is proposed.

## Business problem

The Director of Hospital Planning & Service Transformation needs to decide which changes in hospital activity warrant a planning investigation. Separate reports can mix episodes, admissions, optional outpatient measures and year-to-date snapshots, making it difficult to tell whether a reported increase is sustained, comparable or explained by revisions.

The consequence is an unclear route from a headline activity movement to the next operational question. Leaders may discuss extra capacity before establishing whether the signal reflects throughput, reporting or case mix. The commission is a verified national activity-stream review that supports a focused request for waiting-list, workforce, bed or pathway evidence. Provider-level action remains conditional on an approved provider source.

## Commissioned decision

> Which hospital activity streams show sustained change requiring planning investigation, and what capacity, waiting-list and workforce evidence is still needed to diagnose service pressure?

## Practical use

At the monthly review, the planning lead opens an elective or non-elective stream with at least three comparable monthly-flow observations showing a sustained change. The Information Steward verifies the unit, publication status and any cumulative-to-monthly derivation, then the lead compares the declared recent or pre-pandemic baseline.

The Director records an activity finding and a separate planning hypothesis. A possible capacity concern becomes a request for bed, workforce and waiting-list evidence with an operational owner; a reporting discontinuity becomes a data-resolution action. The core pack remains national and usable without provider or outpatient extensions. It does not convert activity volumes into a staffing or bed requirement.

**Management handover:** A monthly planning pack containing verified stream trajectories, baseline comparisons, unit/revision diagnostics and a hypothesis-to-evidence action register. Each case must distinguish the observed activity change, possible explanation and additional operational dataset needed to test it.

The full [business context](project/BUSINESS_CONTEXT.md) sets out stakeholders, decisions, evidence limits and proposed benefit measures.

## What must be delivered

1. Build separate verified elective and non-elective trajectories with source-specific units and reporting status; include outpatient trajectories only when the validated MAR schema supports them or a compatible official extension is registered.
2. Compare recent activity with a declared pre-pandemic and/or recent baseline; identify sustained changes over at least three months.
3. Create up to ten stream/provider investigation cases only where provider data exists, otherwise stream-level cases; separate activity evidence from capacity hypotheses.

The complete D1–D12 pack includes discovery, source governance, ingestion/model, quality, metric catalogue, analysis, investigation scenarios, BI, assurance/UAT, independent handover, executive briefing and contribution evidence. A dashboard by itself does not satisfy the commission.

## Fixed core and optional work

**Core:** Retain the agreed combined April 2018–March 2026 CSV as the intended input, subject to identity validation. The official March 2026 release separately lists historical 2018/19–2024/25 and 2025/26 M13 MAR CSVs; register these as a two-file fallback if the agreed combined file cannot be validated. Core analysis is at the verified national activity-stream grain. Provider detail and outpatient fields must be confirmed in the acquired MAR schema before inclusion.

**Extensions:** Provider/catchment comparison requires a registered provider-level source; outpatient metrics require verified MAR fields or a separately registered provisional-HES source. A&E waiting times, bed occupancy, unmet demand and capacity sufficiency are outside the activity core. Scope must not be silently shifted to another NHS series.

Source support is checked at the Week 2 gate. A required output is blocked until its fields and cohort are verified; it cannot pass acceptance through a generic “data unavailable” disclaimer. An explicitly optional extension may remain unavailable with a reason. See [exact source URLs and verification evidence](data/SOURCE_REGISTER.md).

## Measurable project outcomes

1. Every required output states its precise activity unit and whether the input is monthly or cumulative.
2. National core results remain usable without provider data or an outpatient extension.
3. Every capacity hypothesis identifies the missing bed, workforce, waiting-list or case-mix evidence.

All headline metrics require field lineage; five source values and five BI measures must reconcile. DT1–DT10 must be executed, a second member must reproduce the core outputs, and no critical/high defect may remain. These assess delivery quality; real-world savings or service improvement are not claimed.

## Investigation rules

Compare supported streams using same-month year-on-year changes and a declared baseline index, requiring at least three contiguous comparable monthly flows for persistence. Show a recent baseline and, where valid, a pre-pandemic comparator separately. The investigation list may contain fewer than ten streams and is never padded with invented provider cases.

- Activity volumes do not directly measure unmet demand, bed occupancy, waiting-time performance or capacity sufficiency.
- HES episodes are not necessarily unique patients; do not relabel them.
- Avoid summing cumulative snapshots, combining provisional/final series or silently bridging provider reorganisations.

## Team and stakeholder ownership

Director of Hospital Planning & Service Transformation approves business scope and the investigation recommendation. The Business Analyst, Data Governance Analyst, Data Engineer and BI Developer work with the specialist roles in the [project brief](project/PROJECT_BRIEF.md). Assign individual owners at kickoff and record substantive work and independent reviews in `CONTRIBUTIONS.md`.

## Delivery plan

Weeks 1–2: decision requirements and verified cohort. Weeks 3–4: model, reconciliation and metric definitions. Weeks 5–6: analytical findings, alternative investigation scenarios and BI draft. Weeks 7–8: simulated UAT, independent rerun, executive briefing and handover.

## Start here

1. [Project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. [D1–D12 deliverables and metric contracts](project/DELIVERABLES.md).
3. [AC1–AC12 and DT1–DT10 acceptance tests](project/ACCEPTANCE_CRITERIA.md).
4. [Governance and sign-off](project/GOVERNANCE.md).
5. [Data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw](data/raw/README.md), [reference](data/reference/README.md) and [metadata](data/metadata/README.md) guidance.
6. [Team repository standard](submission/TEAM_REPOSITORY_STANDARD.md), [submission guide](submission/SUBMISSION_GUIDE.md) and [final template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master repository holds the Mettelo-controlled specification. Create `MTL-XF-029-<team-name>` under the **Mettelo GitHub organisation** and add every member's individual account. Delivery analysis, code, tests, BI and contribution evidence belong in that team repository. Use issues, branches, meaningful commits, PRs and reviews where practical.

The required master areas are `project/`, `data/` (including raw/reference/metadata guidance) and `submission/`; [the documentation index](project/README.md) explains their authority and current revision.

**Mettelo — Built for What’s Next**
