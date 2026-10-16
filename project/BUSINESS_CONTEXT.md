# MTL-XF-029 — Business context

## Organisation and decision owner

**Simulated client:** Confidential NHS Hospital Planning & Service Transformation Directorate. **Accountable executive:** Director of Hospital Planning & Service Transformation. **Review cadence:** monthly hospital activity planning review.

This fictional directorate/board is an engagement scenario, not an assertion of a real client's circumstances. The source data remains official public/open data.

## Business problem

The planning directorate must decide which activity streams warrant investigation when volumes differ from prior periods. Episodes, admissions and outpatient attendances are not interchangeable, and monthly values may be confused with year-to-date snapshots. Rising activity could reflect throughput, coding, case mix or demand; it does not on its own prove that bed capacity is insufficient.

## Why the current process is insufficient

The current scenario relies on separately prepared reports without a common source/metric contract. The material failure to prevent is specific: Unconfirmed combined-file provenance or cumulative/snapshot handling could invalidate every downstream activity comparison.

This creates uncertainty over which cases need investigation and which comparisons should be rejected. No quantified loss, backlog, budget deficit or service failure is invented as a client fact.

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

At the monthly meeting, the Director reviews a three-month sustained change in elective or non-elective activity and compares it with the declared baseline. The Information Steward checks whether the measure is a true monthly flow and whether a revision explains the change. The planning team then requests waiting-list, workforce or bed evidence before diagnosing a capacity constraint. Provider-specific recommendations appear only if the approved file actually contains valid provider detail.

## Current-to-target workflow

1. **Before review:** analyst registers the approved files, coverage and definitions; steward checks the cohort and unresolved exceptions.
2. **At review:** Director of Hospital Planning & Service Transformation opens the overview, then inspects diagnostics and the underlying eligible population before considering a case.
3. **Challenge:** the relevant stakeholder compares the alternative scenario and asks whether the signal survives missingness, comparability and denominator checks.
4. **Action:** each accepted case records investigation type, responsible service role, missing evidence, next review and what finding would reverse the recommendation.
5. **Follow-up:** the next monthly hospital activity planning review records evidence received and the decision, without claiming the analytical signal itself caused an improvement.

## Required analytical response

- Build separate elective, non-elective and outpatient trajectories with source-specific units and reporting status.
- Compare recent activity with a declared pre-pandemic and/or recent baseline; identify sustained changes over at least three months.
- Create up to ten stream/provider investigation cases only where provider data exists, otherwise stream-level cases; separate activity evidence from capacity hypotheses.

## Measurable project outcomes

1. Every required output states its precise activity unit and whether the input is monthly or cumulative.
2. National core results remain usable without provider data or an outpatient extension.
3. Every capacity hypothesis identifies the missing bed, workforce, waiting-list or case-mix evidence.

## Proposed benefit monitoring

At kickoff, record a baseline review process and propose measures for: time to regenerate the agreed evidence pack; proportion of agenda recommendations with a complete evidence chain; and proportion of accepted investigations with a role owner and next review. The target for recommendation traceability and ownership is 100%; regeneration time is measured during the independent rerun, with no fabricated pre-project baseline or claimed reduction. These are proposed management measures, not achieved service benefits.

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
