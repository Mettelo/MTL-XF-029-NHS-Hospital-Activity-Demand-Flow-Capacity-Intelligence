# MTL-XF-029 — Business context

## Organisation and decision owner

**Simulated client:** Confidential NHS Hospital Planning & Service Transformation Directorate. **Accountable executive:** Director of Hospital Planning & Service Transformation. **Review cadence:** monthly hospital activity planning review.

This fictional directorate/board is an engagement scenario, not an assertion of a real client's circumstances. The source data remains official public/open data.

## Business setting and immediate planning need

The simulated hospital planning and service-transformation directorate prepares a monthly activity review for elective and non-elective planning leads. Its first decision is which supported activity streams need a deeper operational evidence request before any capacity response is proposed.

## Business problem

The Director of Hospital Planning & Service Transformation needs to decide which changes in hospital activity warrant a planning investigation. Separate reports can mix episodes, admissions, optional outpatient measures and year-to-date snapshots, making it difficult to tell whether a reported increase is sustained, comparable or explained by revisions.

The consequence is an unclear route from a headline activity movement to the next operational question. Leaders may discuss extra capacity before establishing whether the signal reflects throughput, reporting or case mix. The commission is a verified national activity-stream review that supports a focused request for waiting-list, workforce, bed or pathway evidence. Provider-level action remains conditional on an approved provider source.

## Why the current process is insufficient

The activity pack supplies volumes, but the planning discussion asks why they moved and what response is needed. If the units, monthly/cumulative basis and publication status are hidden, even the starting comparison is uncertain. The replacement must validate the MAR inputs and use a declared baseline before presenting a sustained-change case.

## Stakeholders and decisions

| Simulated stakeholder | Decision / review responsibility |
| --- | --- |
| Director of Hospital Planning & Service Transformation | Accountable for scope, investigation priorities, accepted limitations and final business sign-off. |
| Head of Elective & Non-elective Planning | Review activity change and specify pathway/capacity evidence requests. |
| Outpatient Transformation Lead | Interpret appointment/attendance measures separately from inpatient activity. |
| Hospital Information Steward | Approve HES/MAR definitions, provisional status and geographic coverage. |
| Operational Assurance & Finance Leads | Challenge capacity claims and define additional workforce, bed and cost evidence. |

## Commissioned decision

Which hospital activity streams show sustained change requiring planning investigation, and what capacity, waiting-list and workforce evidence is still needed to diagnose service pressure?

## Practical management use case

At the monthly review, the planning lead opens an elective or non-elective stream with at least three comparable monthly-flow observations showing a sustained change. The Information Steward verifies the unit, publication status and any cumulative-to-monthly derivation, then the lead compares the declared recent or pre-pandemic baseline.

The Director records an activity finding and a separate planning hypothesis. A possible capacity concern becomes a request for bed, workforce and waiting-list evidence with an operational owner; a reporting discontinuity becomes a data-resolution action. The core pack remains national and usable without provider or outpatient extensions. It does not convert activity volumes into a staffing or bed requirement.

## Current-to-target workflow

**Target management handover:** A monthly planning pack containing verified stream trajectories, baseline comparisons, unit/revision diagnostics and a hypothesis-to-evidence action register. Each case must distinguish the observed activity change, possible explanation and additional operational dataset needed to test it.

The meeting's decision record must contain: the selected case and reporting period; the source-backed finding; the decision to investigate, watch, clarify or close; the responsible stakeholder role; the specific additional evidence requested; and the next review point. Add the evidence that would reverse or narrow the recommendation. A watchlist or no-action conclusion is valid when supported; do not fill the shortlist simply to reach ten cases.

## Required analytical response

- Build separate verified elective and non-elective trajectories with source-specific units and reporting status; include outpatient trajectories only when the validated MAR schema supports them or a compatible official extension is registered.
- Compare recent activity with a declared pre-pandemic and/or recent baseline; identify sustained changes over at least three months.
- Create up to ten stream/provider investigation cases only where provider data exists, otherwise stream-level cases; separate activity evidence from capacity hypotheses.

## Measurable project outcomes

1. Every required output states its precise activity unit and whether the input is monthly or cumulative.
2. National core results remain usable without provider data or an outpatient extension.
3. Every capacity hypothesis identifies the missing bed, workforce, waiting-list or case-mix evidence.

## Proposed benefit monitoring

Measure whether every planning case states the correct activity unit and baseline and separates its finding from its capacity hypothesis; target 100%. In simulated UAT, require the user to choose the next evidence request rather than infer beds from volume alone. Reduced waits or improved flow cannot be claimed from this activity analysis.

Record the preparation and review baseline at kickoff, then measure evidence-pack regeneration during the independent rerun. No pre-project time saving or achieved operational benefit is assumed. The eight-week engagement is assessed on the usability and traceability of the decision pack; later service outcomes require separate follow-up.

## Scope and evidence limits

**Core:** Retain the agreed combined April 2018–March 2026 CSV as the intended input, subject to identity validation. The official March 2026 release separately lists historical 2018/19–2024/25 and 2025/26 M13 MAR CSVs; register these as a two-file fallback if the agreed combined file cannot be validated. Core analysis is at the verified national activity-stream grain. Provider detail and outpatient fields must be confirmed in the acquired MAR schema before inclusion.

**Extensions:** Provider/catchment comparison requires a registered provider-level source; outpatient metrics require verified MAR fields or a separately registered provisional-HES source. A&E waiting times, bed occupancy, unmet demand and capacity sufficiency are outside the activity core. Scope must not be silently shifted to another NHS series.

- Activity volumes do not directly measure unmet demand, bed occupancy, waiting-time performance or capacity sufficiency.
- HES episodes are not necessarily unique patients; do not relabel them.
- Avoid summing cumulative snapshots, combining provisional/final series or silently bridging provider reorganisations.

## Risks, mitigations and escalation

- **Interpretation risk:** Unconfirmed combined-file provenance or cumulative/snapshot handling could invalidate every downstream activity comparison. The domain specialist reviews definitions and DT1–DT10 before sign-off.
- **Source risk:** Official release, split-file fallback links and description resource verified; agreed combined-file identity, MAR field availability and snapshot compatibility pending. The steward records unresolved items at G1; mandatory gaps block dependent outputs.
- **Decision risk:** prioritisation assumptions may affect which cases appear. Show alternative scenarios, excluded cases and evidence that could change a recommendation.
- **Delivery risk:** limited time or skills can leave undocumented manual steps. Assign a second-member rerun and retain contribution/review evidence throughout the eight weeks.

## Evidence chain

Stakeholder requirement → registered source and valid cohort → governed field/metric → tested transformation → reconciled finding → scenario reason code → investigation owner/evidence request → simulated UAT and sign-off.

Every major recommendation must be traceable through this chain.
