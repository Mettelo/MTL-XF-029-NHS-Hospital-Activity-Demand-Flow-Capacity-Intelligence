# MTL-XF-029 — Required deliverables

**Commissioned decision:** Which hospital activity streams show sustained change requiring planning investigation, and what capacity, waiting-list and workforce evidence is still needed to diagnose service pressure?

All locations below refer to the team's delivery repository. The master repository defines the requirements and contains no completed analysis. Owners are assigned from [the project roles](PROJECT_BRIEF.md).

## D1 — Discovery & decision requirements

**Due:** Week 1  
**Team artefact location:** `docs/01-discovery/`

Decision statement; stakeholder map; as-is reporting to investigation-review process; at least eight prioritised requirements. Answer these questions: How have elective and non-elective activity changed across comparable months? How does outpatient activity differ from admitted care? Where are sustained changes visible relative to a declared baseline? What do pandemic effects, revisions and provider changes do to the interpretation? What additional beds, waiting-list and workforce evidence is required before a capacity decision?

**Acceptance evidence:** All requirements have an owner, priority, deliverable and test ID; domain analyst approves scope.

## D2 — Governed sources & cohort

**Due:** Week 2  
**Team artefact location:** `docs/02-data-governance/; data/`

Freeze the agreed HES Monthly Activity Report historical CSV for April 2018–March 2026. Inspect provisional/final status, monthly versus year-to-date measures and actual provider/geographic dimensions. Use only supported breakdowns; this is the final HES project, replacing the earlier A&E concept. Register exact files, metadata, licences, checksums, coverage and critical fields; record rejection of unavailable dimensions.

**Acceptance evidence:** 100% of inputs registered; no claimed freeze until acquisition evidence exists.

## D3 — Reproducible analytical model

**Due:** Week 3  
**Team artefact location:** `src/; sql/; docs/03-data-model/`

Reporting month × activity stream × published measure × available provider/geography/category × revision status. Spell, episode, admission, attendance and patient measures are distinct. If data is cumulative, derive monthly increments only within the same valid financial-year series. Deliver load, type checks, hierarchy handling, lineage, exclusions and environment instructions.

**Acceptance evidence:** A second member regenerates equivalent curated outputs from identical inputs; no unexplained duplicate analytical keys.

## D4 — Quality & reconciliation

**Due:** Week 3  
**Team artefact location:** `docs/04-data-quality/; tests/`

Profile missingness, suppression, valid values, keys and join coverage. Reconcile five month/stream values and inspect cumulative versus monthly status. Test financial-year reset when deriving increments from cumulative values. Show a missing month invalidates a twelve-month total. Verify dashboard labels preserve episodes/spells/attendances and contain no inferred occupancy or A&E waiting metric.

**Acceptance evidence:** Every input row is accounted for as retained, excluded or quarantined; five published cells reconcile within declared rounding.

## D5 — KPI catalogue

**Due:** Week 4  
**Team artefact location:** `docs/05-kpi-catalogue/`

Define all 8 measures listed below with formula, grain, denominator, unit, source fields, exclusions, owner, refresh and limitations.

**Acceptance evidence:** 100% headline metrics trace to source fields and tested transformations; conditional unavailable measures are explicitly marked.

## D6 — Domain analytical assessment

**Due:** Week 5  
**Team artefact location:** `analysis/; docs/06-analysis/`

Build separate elective, non-elective and outpatient trajectories with source-specific units and reporting status. Compare recent activity with a declared pre-pandemic and/or recent baseline; identify sustained changes over at least three months.

**Acceptance evidence:** At least five evidence-backed findings state period, population, comparison, magnitude, uncertainty and limitation; negative findings count.

## D7 — Investigation decision framework

**Due:** Week 6  
**Team artefact location:** `docs/07-decision-framework/`

Create up to ten stream/provider investigation cases only where provider data exists, otherwise stream-level cases; separate activity evidence from capacity hypotheses. Record eligibility, thresholds, weights if used, reason codes and manual review triggers.

**Acceptance evidence:** Every shortlisted case has metrics, rationale, owner and evidence gaps; at least two scenarios compared; fewer than ten is valid where evidence is insufficient.

## D8 — BI decision-support product

**Due:** Draft Week 6; final Week 7  
**Team artefact location:** `dashboard/`

Executive overview answering 'Which hospital activity streams show sustained change requiring planning investigation, and what capacity, waiting-list and workforce evidence is still needed to diagnose service pressure?' plus diagnostic and data-quality views; visible periods, units, denominator notes, resettable filters and accessible labels.

**Acceptance evidence:** Five headline measures reconcile; every filter tested; export screenshots/PDF plus reproducible build or free access instructions.

## D9 — Independent assurance & UAT

**Due:** Week 7  
**Team artefact location:** `docs/08-assurance-uat/`

At least ten scenarios including the four project-specific tests below; requirement-to-test matrix, expected/actual evidence, defect log and simulated stakeholder feedback.

**Acceptance evidence:** No unresolved critical/high defect; accepted lower-severity limitations have a named reviewer and explicit impact.

## D10 — Technical & operational handover

**Due:** Week 8  
**Team artefact location:** `docs/09-technical-handover/`

Clean setup, architecture, frozen input manifest, run/refresh steps, output checks, troubleshooting and change-control process for NHS Hospital Activity, Demand, Flow & Capacity Pressure Intelligence.

**Acceptance evidence:** Another member reproduces the core outputs without undocumented edits and records environment, duration and discrepancies.

## D11 — Executive recommendation

**Due:** Week 8  
**Team artefact location:** `deliverables/`

Maximum two-page briefing and 15–20 minute presentation: commissioned decision, five findings, investigation shortlist, sensitivity, missing evidence, responsibilities and next review.

**Acceptance evidence:** Every quantitative claim links to an artefact/metric; no unsupported causal, policy or operational guarantee.

## D12 — Contribution & delivery record

**Due:** Weekly; final Week 8  
**Team artefact location:** `CONTRIBUTIONS.md; delivery issues/PRs`

Record who delivered and reviewed each MTL-XF-029 work package, including domain, governance, engineering, BI and assurance contributions.

**Acceptance evidence:** Every member links to substantive artefacts and review/presentation evidence; commit count alone is insufficient.

## Required KPI definitions

| Metric | Required definition / calculation |
| --- | --- |
| Elective activity | Publisher-defined elective admissions/spells/episodes, labelled precisely with measure. |
| Non-elective activity | Publisher-defined non-elective activity using a separate compatible category. |
| Outpatient activity | Published attendances/appointments by available type; keep distinct from admitted care. |
| Year-on-year activity change | 100 × (monthly activity / corresponding prior-year month − 1), with positive comparable base. |
| Trailing twelve-month activity | Sum of twelve genuine contiguous monthly flows; never sum year-to-date cumulative values. |
| Activity mix | 100 × compatible activity component / matching stream total; do not divide outpatient attendances by inpatient episodes. |
| Baseline index | 100 × current activity / declared comparable baseline; label pandemic and reporting breaks. |
| Revision/coverage flag | Available valid months and provisional/final status by stream; display missingness and provider continuity. |

For every metric record business purpose, formula, source fields, grain, unit, numerator/denominator, exclusions, suppression, zero-base behaviour, owner, refresh and test evidence. Do not populate conditional metrics from invented fields.

## Mandatory domain scenarios

1. Reconcile five month/stream values and inspect cumulative versus monthly status.
2. Test financial-year reset when deriving increments from cumulative values.
3. Show a missing month invalidates a twelve-month total.
4. Verify dashboard labels preserve episodes/spells/attendances and contain no inferred occupancy or A&E waiting metric.

## Review gates

Week 2: cohort and source approval. Week 4: model, DQ and metrics approval. Week 6: analytical and decision-framework review. Week 8: UAT, independent rerun and final panel review. Record reviewer, date, artefact version and decision at every gate.
