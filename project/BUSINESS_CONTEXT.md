# MTL-XF-029 — Business context

## Organisation and pressure

**NHS Hospital Activity, Demand, Flow & Capacity Pressure Intelligence.** An NHS planning directorate needs to understand how elective/non-elective activity, admissions and outpatient demand are changing over time and which areas show sustained pressure rather than short-term variation. This will support operational and service-planning reviews.

The simulated sponsor, Confidential NHS Hospital Planning & Service Transformation Directorate, must decide where to direct limited analytical and service-review attention. Its starting problem is an inconsistent view of nhs hospital activity, demand, flow & capacity pressure intelligence: totals, rates, periods and categories can lead users to different conclusions without a common definition. The engagement supplies an evidence base; it does not assume the client has already suffered a quantified failure.

## Current process and its consequences

Analysts retrieve official tables independently, prepare local summaries and discuss headline differences in management meetings. Without a shared cohort and definition register, revisions, incomparable denominators and missing coverage can pass into recommendations. The consequence is an investigation shortlist that cannot be explained or reproduced, rather than a verified estimate of financial loss.

## Required decision process

1. Confirm the reporting cohort and available dimensions.
2. Review governed metrics and quality exceptions before interpreting patterns.
3. Compare like-for-like trends and segment evidence against the questions below.
4. Challenge at least two prioritisation scenarios and document changes in shortlisted cases.
5. Assign a responsible role, evidence-gathering action and review point to every proposed investigation.

**Decision:** Which hospital activity streams show sustained change requiring planning investigation, and what capacity, waiting-list and workforce evidence is still needed to diagnose service pressure?

## Business questions and evidence

| Question | Expected evidence |
| --- | --- |
| How have elective and non-elective activity changed across comparable months? | Reconciled trend/segment table and diagnostic chart with period, grain, denominator and source references. |
| How does outpatient activity differ from admitted care? | Reconciled trend/segment table and diagnostic chart with period, grain, denominator and source references. |
| Where are sustained changes visible relative to a declared baseline? | Segment or coverage assessment stating which comparisons are supported. |
| What do pandemic effects, revisions and provider changes do to the interpretation? | Sensitivity or scope audit showing what changes the interpretation. |
| What additional beds, waiting-list and workforce evidence is required before a capacity decision? | Investigation plan with missing evidence, owner and decision-review trigger. |

## Intended management use

- Build separate elective, non-elective and outpatient trajectories with source-specific units and reporting status.
- Compare recent activity with a declared pre-pandemic and/or recent baseline; identify sustained changes over at least three months.
- Create up to ten stream/provider investigation cases only where provider data exists, otherwise stream-level cases; separate activity evidence from capacity hypotheses.

The BI executive view starts with the commissioned question, reporting period and coverage. Users inspect a diagnostic view before reading the investigation shortlist. Every case records the signal, its magnitude, uncertainty, alternative explanations, evidence still needed and a next-step owner. The final briefing must explain at least one case where the evidence is insufficient for action.

## Measures of project value

Success means a repeatable review with five supported findings, five reconciled dashboard measures, two compared decision scenarios, ten UAT scenarios and a reproducible handover. Teams may propose a future operational baseline and improvement target, but must label these as proposed measures rather than achieved benefits. No observed savings or service improvement can be claimed from this simulated engagement alone.

## Interpretation and evidence limits

- Activity volumes do not directly measure unmet demand, bed occupancy, waiting-time performance or capacity sufficiency.
- HES episodes are not necessarily unique patients; do not relabel them.
- Avoid summing cumulative snapshots, combining provisional/final series or silently bridging provider reorganisations.

## Dependencies and risks

- Source/schema validation may narrow the scope: record an explicit impact decision rather than inventing fields.
- Data revisions may alter findings: preserve immutable source manifests and rerun comparisons.
- Small, suppressed or non-comparable segments may distort ordering: apply eligibility rules and show excluded cases.
- Local context or operational records may be missing: attach an evidence request to the relevant recommendation.

The domain roles in [the brief](PROJECT_BRIEF.md) own interpretation; the simulated review panel owns decisions.
