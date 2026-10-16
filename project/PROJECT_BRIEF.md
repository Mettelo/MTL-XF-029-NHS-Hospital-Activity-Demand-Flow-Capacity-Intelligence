# MTL-XF-029 — Project brief

## Engagement

This is a **simulated confidential-client engagement** using official public/open data. The client label is fictional and intentionally anonymous. Do not imply a real external Mettelo customer, employment by that client, privileged access or confidential source data. Public source statistics remain public; the engagement framing does not make them confidential.

**Simulated sponsor:** Confidential NHS Hospital Planning & Service Transformation Directorate. **Duration:** 8 weeks. **Team:** 6–8 members. **Track:** Cross-Functional. **Sector:** NHS / Hospital Activity / Service Planning.

## Commission

Which hospital activity streams show sustained change requiring planning investigation, and what capacity, waiting-list and workforce evidence is still needed to diagnose service pressure?

**NHS Hospital Activity, Demand, Flow & Capacity Pressure Intelligence.** An NHS planning directorate needs to understand how elective/non-elective activity, admissions and outpatient demand are changing over time and which areas show sustained pressure rather than short-term variation. This will support operational and service-planning reviews.

## Outcomes and boundaries

- Build separate elective, non-elective and outpatient trajectories with source-specific units and reporting status.
- Compare recent activity with a declared pre-pandemic and/or recent baseline; identify sustained changes over at least three months.
- Create up to ten stream/provider investigation cases only where provider data exists, otherwise stream-level cases; separate activity evidence from capacity hypotheses.

Deliver evidence for a management investigation decision, with an auditable shortlist of up to ten cases and at least two alternative prioritisation scenarios. Do not manufacture a full shortlist where the data supports fewer cases. Findings may conclude that evidence is insufficient.

**Data boundary:** Freeze the agreed HES Monthly Activity Report historical CSV for April 2018–March 2026. Inspect provisional/final status, monthly versus year-to-date measures and actual provider/geographic dimensions. Use only supported breakdowns; this is the final HES project, replacing the earlier A&E concept.

**Model boundary:** Reporting month × activity stream × published measure × available provider/geography/category × revision status. Spell, episode, admission, attendance and patient measures are distinct. If data is cumulative, derive monthly increments only within the same valid financial-year series.

**Out of scope:** real operational deployment, confidential case-level data, guaranteed savings/outcome improvements, paid-source dependencies and automatic allocation of services or funding. Optional modelling or enriched sources must not delay or replace the core D1–D12 pack.

## Users and acceptance owners

- Simulated sponsor/review panel: approves commissioned question, changes and final investigation recommendation.
- Domain service/planning user: checks whether diagnostic evidence supports the proposed review action.
- Data steward: verifies source/version, licence, definitions, quality and retention evidence.
- BI user: tests overview, drill-down, filters and limitations.
- Independent reviewer: verifies calculations, rerun and requirement-to-test traceability.

These are simulated stakeholder roles, not claims of access to a real organisation.

## Work allocation

| Accountable role | Project responsibility and evidence |
| --- | --- |
| Business Analyst / Delivery Lead | Own the commissioned decision for Confidential NHS Hospital Planning & Service Transformation Directorate; record at least eight prioritised requirements, each linked to a deliverable and test; maintain weekly scope and decision logs. |
| Data Governance Analyst | Register every 029 input and critical field; approve the frozen cohort, licence evidence, glossary and 100% headline-KPI lineage before analysis. |
| Data Engineer | Implement the stated 029 analytical grain, ingestion and exclusions; deliver a clean rerun with row-count/checksum evidence and no unexplained key duplicates. |
| BI Developer | Build executive, diagnostic and quality views for the commissioned decision; reconcile at least five 029 dashboard measures and test every visible filter. |
| NHS Activity & Performance Analyst | Approve activity units and revision status, and reconcile five month/stream measures. |
| Hospital Planning & Operations Analyst | Write up to ten activity investigation cases with missing bed, workforce and waiting-list evidence. |
| Clinical Data Assurance Analyst | Test cumulative resets, provider continuity and distinction between episodes and patients. |

At kickoff, replace role ownership with named team members and record review partners in `CONTRIBUTIONS.md`. Multiple roles per member are permitted, but critical calculations need a reviewer distinct from their author.

## Working stages

1. Week 1: agree at least eight requirements and define expected decisions.
2. Week 2: inspect actual file schemas, establish available coverage and approve cohort freeze.
3. Week 3: implement and reconcile analytical facts, keys and exclusions.
4. Week 4: approve the 8-measure KPI catalogue and denominator rules.
5. Week 5: complete five supported findings and domain comparisons.
6. Week 6: compare two decision scenarios, produce the investigation shortlist and BI draft.
7. Week 7: execute ten or more assurance/UAT scenarios, including project-specific edge cases.
8. Week 8: independent rerun, executive briefing, presentation and final handover.

## Sign-off

Follow [D1–D12](DELIVERABLES.md) and [AC1–AC12](ACCEPTANCE_CRITERIA.md). Approve only with reproducible evidence, no unresolved critical/high defects and transparent conditional-data limitations. A change in source availability must be logged; do not silently substitute a newer release.
