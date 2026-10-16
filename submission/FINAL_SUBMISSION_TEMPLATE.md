# MTL-XF-029 — Final submission: NHS Hospital Activity, Demand, Flow & Capacity Pressure Intelligence

Complete this template in your team repository as `submission/FINAL_SUBMISSION.md`. Replace prompts with evidence; leave unavailable items explicitly unavailable with reasons. This template itself is not completed delivery evidence.

## Team and version

- Team repository URL:
- Team name and individual GitHub accounts:
- Final commit/tag and submission date:
- Master specification URL and reviewed commit:
- Delivery dates:
- Named role owners and independent reviewers:
- Engagement declaration: simulated confidential-client engagement using official public/open data; no real-client employment, endorsement or privileged access claimed.

## Commissioned decision

Which hospital activity streams show sustained change requiring planning investigation, and what capacity, waiting-list and workforce evidence is still needed to diagnose service pressure?

State the answer, confidence, principal limitation and proposed investigation action.

## Actual cohort and provenance

Agreed boundary: Freeze the agreed HES Monthly Activity Report historical CSV for April 2018–March 2026. Inspect provisional/final status, monthly versus year-to-date measures and actual provider/geographic dimensions. Use only supported breakdowns; this is the final HES project, replacing the earlier A&E concept.

Record actual frozen files/versions, manifest/checksums, source-register link, licence evidence, retrieval timestamp, schema/coverage validation, inclusions/exclusions and approved deviations. Do not mark acquisition complete without evidence.

## Evidence index

| Deliverable | Artefact link | Owner / reviewer | Status / limitation |
| --- | --- | --- | --- |
| D1 — Discovery & decision requirements | To complete | To complete | To complete |
| D2 — Governed sources & cohort | To complete | To complete | To complete |
| D3 — Reproducible analytical model | To complete | To complete | To complete |
| D4 — Quality & reconciliation | To complete | To complete | To complete |
| D5 — KPI catalogue | To complete | To complete | To complete |
| D6 — Domain analytical assessment | To complete | To complete | To complete |
| D7 — Investigation decision framework | To complete | To complete | To complete |
| D8 — BI decision-support product | To complete | To complete | To complete |
| D9 — Independent assurance & UAT | To complete | To complete | To complete |
| D10 — Technical & operational handover | To complete | To complete | To complete |
| D11 — Executive recommendation | To complete | To complete | To complete |
| D12 — Contribution & delivery record | To complete | To complete | To complete |

## Governed measures

| Required measure | Definition/source/test link | Result / unavailable reason |
| --- | --- | --- |
| Elective activity | To complete | To complete |
| Non-elective activity | To complete | To complete |
| Outpatient activity | To complete | To complete |
| Year-on-year activity change | To complete | To complete |
| Trailing twelve-month activity | To complete | To complete |
| Activity mix | To complete | To complete |
| Baseline index | To complete | To complete |
| Revision/coverage flag | To complete | To complete |

## Business questions and five findings

1. How have elective and non-elective activity changed across comparable months?
2. How does outpatient activity differ from admitted care?
3. Where are sustained changes visible relative to a declared baseline?
4. What do pandemic effects, revisions and provider changes do to the interpretation?
5. What additional beds, waiting-list and workforce evidence is required before a capacity decision?

For each question record the finding, quantitative evidence, period/grain, comparison, uncertainty, limitation and artefact link. Record an evidenced gap where the data cannot answer it.

## Investigation shortlist and sensitivity

Provide up to ten supported cases. For each: entity/segment, signal and magnitude, eligibility, reason code, scenario membership, proposed investigation, responsible role, missing evidence and review trigger. Compare at least two scenarios and explain membership/rank changes. Include a case where evidence is insufficient for action.

## Acceptance and assurance

| Criterion | Pass/fail / evidence / reviewer |
| --- | --- |
| AC1 (D1) | To complete |
| AC2 (D2) | To complete |
| AC3 (D3) | To complete |
| AC4 (D4) | To complete |
| AC5 (D4–D5) | To complete |
| AC6 (D5) | To complete |
| AC7 (D6) | To complete |
| AC8 (D7) | To complete |
| AC9 (D8) | To complete |
| AC10 (D9) | To complete |
| AC11 (D10–D11) | To complete |
| AC12 (D12) | To complete |

Record at least ten executed UAT scenarios, expected/actual results, defect severity/disposition and five reconciled BI measures. Mandatory cases:

1. Reconcile five month/stream values and inspect cumulative versus monthly status.
2. Test financial-year reset when deriving increments from cumulative values.
3. Show a missing month invalidates a twelve-month total.
4. Verify dashboard labels preserve episodes/spells/attendances and contain no inferred occupancy or A&E waiting metric.

## Reproducible handover

- Environment/tool versions and dependencies:
- Input snapshot location and checksum verification:
- Clean run instructions and output locations:
- Independent rerun reviewer/date/duration/results:
- Reconciliation evidence and permitted rounding:
- Refresh/change process and known failure modes:

## Executive delivery

- Two-page briefing link:
- Presentation link and 15–20 minute duration:
- Dashboard/free access instructions and static export:
- Recommendations, missing evidence, responsible roles and next review:

## Contributions

For every member link authored artefacts, review work, issues/PRs/commits and presentation/handover contribution. Link `CONTRIBUTIONS.md`; commit count alone is insufficient.

## Limitations and review decision

- Activity volumes do not directly measure unmet demand, bed occupancy, waiting-time performance or capacity sufficiency.
- HES episodes are not necessarily unique patients; do not relabel them.
- Avoid summing cumulative snapshots, combining provisional/final series or silently bridging provider reorganisations.

Add actual limitations, optional extensions, unresolved accepted issues and their impacts. Record simulated panel review date, reviewers and decision only after review occurs. Do not claim real operational savings or outcome improvements.
