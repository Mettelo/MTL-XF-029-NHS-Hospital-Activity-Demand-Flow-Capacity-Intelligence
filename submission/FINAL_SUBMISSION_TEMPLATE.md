# MTL-XF-029 — Final submission: NHS Hospital Activity, Demand, Flow & Capacity Pressure Intelligence

Complete in the team repository as `submission/FINAL_SUBMISSION.md`. This is a template, not delivery evidence. Replace prompts with actual links/results; never invent approvals, hashes or test outcomes.

## Team and version

- Team repository, name and member GitHub accounts:
- Named delivery owners and independent reviewers:
- Reviewed master specification URL/commit:
- Final commit/tag and submission date:
- Delivery start/end dates:
- Declaration: simulated confidential-client engagement using official public/open data; no real-client employment, endorsement or privileged access claimed.

## Business answer

**Decision owner:** Director of Hospital Planning & Service Transformation  
**Decision:** Which hospital activity streams show sustained change requiring planning investigation, and what capacity, waiting-list and workforce evidence is still needed to diagnose service pressure?

State the answer, confidence, principal limitation, proposed investigation and responsible stakeholder role. Explain how it fits the monthly hospital activity planning review.

## Scope and data support

Link approved core/extension contract and source-to-deliverable matrix. Record actual source versions, retrieval UTC, licences, checksums, schema/grain, periods, exclusions and freeze sign-off. Document any required supplement/fallback, why activated, what it replaces and how overlap is handled. Explicitly list unsupported mandatory requirements as blockers and optional items as unavailable with reasons.

## Delivery evidence

| Deliverable | Artefact / owner / reviewer / status |
| --- | --- |
| D1 — Discovery & requirements | To complete |
| D2 — Sources, governance & cohort contract | To complete |
| D3 — Reproducible model & ingestion | To complete |
| D4 — Quality, source reconciliation & exceptions | To complete |
| D5 — Governed metric catalogue | To complete |
| D6 — Domain assessment | To complete |
| D7 — Investigation framework & scenarios | To complete |
| D8 — Decision-support BI | To complete |
| D9 — Assurance & simulated UAT | To complete |
| D10 — Technical & operational handover | To complete |
| D11 — Executive briefing & presentation | To complete |
| D12 — Contribution & delivery record | To complete |

## Project-specific success

1. Every required output states its precise activity unit and whether the input is monthly or cumulative. — evidence/status: To complete.
2. National core results remain usable without provider data or an outpatient extension. — evidence/status: To complete.
3. Every capacity hypothesis identifies the missing bed, workforce, waiting-list or case-mix evidence. — evidence/status: To complete.

## Five findings and investigation recommendation

For each business question link quantitative evidence, scope, comparison, magnitude, uncertainty and limitation. Include up to ten supported cases with reason codes, baseline/alternative position, missing evidence, operational owner and next review. Explain how scenario changes affect the recommendation and include an evidence-insufficient case.

## Acceptance and testing

| Criterion | Pass/fail / evidence / reviewer |
| --- | --- |
| AC1 | To complete |
| AC2 | To complete |
| AC3 | To complete |
| AC4 | To complete |
| AC5 | To complete |
| AC6 | To complete |
| AC7 | To complete |
| AC8 | To complete |
| AC9 | To complete |
| AC10 | To complete |
| AC11 | To complete |
| AC12 | To complete |

| Domain test | Actual result / evidence / tester / reviewer |
| --- | --- |
| DT1 — Reconcile five month/stream values and inspect cumulative versus monthly status. | To complete |
| DT2 — Test financial-year reset when deriving increments from cumulative values. | To complete |
| DT3 — Show a missing month invalidates a twelve-month total. | To complete |
| DT4 — Verify dashboard labels preserve episodes/spells/attendances and contain no inferred occupancy or A&E waiting metric. | To complete |
| DT5 — Cumulative snapshots are 100, 160 and 210 in one financial year | To complete |
| DT6 — Financial-year cumulative total resets from 900 to 100 | To complete |
| DT7 — Two fallback files overlap for a reporting period | To complete |
| DT8 — No provider identifier exists in the core file | To complete |
| DT9 — Outpatient attendance is absent from verified MAR fields | To complete |
| DT10 — A chart shows rising episode counts | To complete |

Link expected outcomes in [the master acceptance criteria](https://github.com/Mettelo/MTL-XF-029-NHS-Hospital-Activity-Demand-Flow-Capacity-Intelligence/blob/main/project/ACCEPTANCE_CRITERIA.md) or a retained copy tied to the reviewed specification commit. Record all additional BI/filter tests, five source checks, five BI reconciliations, defect severity/disposition and accepted limitations. Synthetic test values must be labelled synthetic.

## Reproducibility and executive delivery

- Environment/dependencies, input manifest and clean run steps:
- Independent reviewer/date/duration/output-equivalence evidence:
- Refresh/fallback/change procedure and known failure modes:
- Dashboard/free review instructions and static export:
- Maximum two-page briefing and 15–20 minute presentation:
- Proposed benefit measures and actual measured rerun time; no invented before/after savings:

## Contributions and review

Link `CONTRIBUTIONS.md` and every member's authored artefacts, reviews, issues/PRs/commits and presentation/handover work. Record simulated panel reviewers/date/decision only after the review occurs. Include unresolved limitations and approved scope changes; do not claim real operational outcomes.
