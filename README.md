# MTL-XF-029 — NHS Hospital Activity, Demand, Flow & Capacity Pressure Intelligence

**Mettelo Project Studio** · Cross-Functional · Master specification  
**Client:** Confidential NHS Hospital Planning & Service Transformation Directorate  
**Sector:** NHS / Hospital Activity / Service Planning  
**Status:** Pre-launch; documentation ready, data acquisition/freeze pending  
**Recommended team:** 6–8 people · **Delivery window:** 8 weeks  
**Master repository:** `Mettelo/MTL-XF-029-NHS-Hospital-Activity-Demand-Flow-Capacity-Intelligence`

> This is a **simulated confidential-client engagement** using official public/open data. The client label is fictional and intentionally anonymous. Do not imply a real external Mettelo customer, employment by that client, privileged access or confidential source data. Public source statistics remain public; the engagement framing does not make them confidential.

## Business challenge

**NHS Hospital Activity, Demand, Flow & Capacity Pressure Intelligence.** An NHS planning directorate needs to understand how elective/non-elective activity, admissions and outpatient demand are changing over time and which areas show sustained pressure rather than short-term variation. This will support operational and service-planning reviews.

Current reporting fragments the evidence needed for a repeatable management review. The team must explain which signals are reliable, which comparisons are valid and where further investigation is needed. No budget, operational failure or improvement outcome is asserted as an observed client fact.

## Commissioned decision

> Which hospital activity streams show sustained change requiring planning investigation, and what capacity, waiting-list and workforce evidence is still needed to diagnose service pressure?

The product supports a simulated stakeholder review. A dashboard alone is insufficient: the recommendation must be traceable to governed definitions, a reproducible model, reconciled analysis and a transparent investigation framework.

## Business questions

- How have elective and non-elective activity changed across comparable months?
- How does outpatient activity differ from admitted care?
- Where are sustained changes visible relative to a declared baseline?
- What do pandemic effects, revisions and provider changes do to the interpretation?
- What additional beds, waiting-list and workforce evidence is required before a capacity decision?

## Approved data and cohort

NHS England HES Monthly Activity Report, full historical series Apr 2018–Mar 2026. It is a single 22 MB CSV, much more durable and reproducible than relying on monthly A&E file URLs.

Freeze the agreed HES Monthly Activity Report historical CSV for April 2018–March 2026. Inspect provisional/final status, monthly versus year-to-date measures and actual provider/geographic dimensions. Use only supported breakdowns; this is the final HES project, replacing the earlier A&E concept.

Exact copyable URLs and acquisition gates are in [SOURCE_REGISTER.md](data/SOURCE_REGISTER.md). No raw data is uploaded by this build. Source coverage and size statements inherited from the agreement are expected values until controlled acquisition verifies them; current URLs are not a substitute for a frozen file manifest.

## What the team must build

1. Build separate elective, non-elective and outpatient trajectories with source-specific units and reporting status.
2. Compare recent activity with a declared pre-pandemic and/or recent baseline; identify sustained changes over at least three months.
3. Create up to ten stream/provider investigation cases only where provider data exists, otherwise stream-level cases; separate activity evidence from capacity hypotheses.

Produce the full D1–D12 delivery pack: discovery, governance, ingestion/model, quality, KPI catalogue, analysis, decision framework, BI, assurance/UAT, handover, executive briefing and contribution record. [Deliverables](project/DELIVERABLES.md) defines locations, dates and evidence for each.

## Core measures

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

## Cross-functional ownership

| Accountable role | Project responsibility and evidence |
| --- | --- |
| Business Analyst / Delivery Lead | Own the commissioned decision for Confidential NHS Hospital Planning & Service Transformation Directorate; record at least eight prioritised requirements, each linked to a deliverable and test; maintain weekly scope and decision logs. |
| Data Governance Analyst | Register every 029 input and critical field; approve the frozen cohort, licence evidence, glossary and 100% headline-KPI lineage before analysis. |
| Data Engineer | Implement the stated 029 analytical grain, ingestion and exclusions; deliver a clean rerun with row-count/checksum evidence and no unexplained key duplicates. |
| BI Developer | Build executive, diagnostic and quality views for the commissioned decision; reconcile at least five 029 dashboard measures and test every visible filter. |
| NHS Activity & Performance Analyst | Approve activity units and revision status, and reconcile five month/stream measures. |
| Hospital Planning & Operations Analyst | Write up to ten activity investigation cases with missing bed, workforce and waiting-list evidence. |
| Clinical Data Assurance Analyst | Test cumulative resets, provider continuity and distinction between episodes and patients. |

Roles may be combined by a smaller team, but each responsibility needs a named owner. A different member reviews critical calculations and final evidence wherever practical.

## Interpretation rules

- Activity volumes do not directly measure unmet demand, bed occupancy, waiting-time performance or capacity sufficiency.
- HES episodes are not necessarily unique patients; do not relabel them.
- Avoid summing cumulative snapshots, combining provisional/final series or silently bridging provider reorganisations.

## Measurable success

- All source files and transformations have provenance and licence evidence; approved inputs have SHA-256 manifests.
- All headline metrics have tested definitions and source-field lineage.
- At least five published values and five dashboard measures reconcile with declared source rounding.
- At least five findings address the business questions and quantify materiality.
- Up to ten investigation cases have evidence, reason codes, owners and limitations; at least two priority scenarios are compared.
- At least ten UAT scenarios pass or have explicitly accepted low-impact limitations; no critical/high defect remains.
- A second member reproduces the core outputs from the same frozen inputs.

These are delivery acceptance thresholds, not promises of real-world service improvement. See [acceptance criteria](project/ACCEPTANCE_CRITERIA.md).

## Delivery sequence

Weeks 1–2: decision requirements, source inspection and freeze approval. Weeks 3–4: model, reconciliation and KPI definitions. Weeks 5–6: analysis, investigation framework and BI draft. Weeks 7–8: UAT, independent rerun, briefing and handover.

## Start here

1. Read the [project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. Review [deliverables](project/DELIVERABLES.md), [acceptance criteria](project/ACCEPTANCE_CRITERIA.md) and [governance](project/GOVERNANCE.md).
3. Inspect the [data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw guidance](data/raw/README.md), [reference guidance](data/reference/README.md) and [metadata guidance](data/metadata/README.md).
4. Create `MTL-XF-029-<team-name>` under the **Mettelo GitHub organisation**, add each member's individual account and follow the [team repository standard](submission/TEAM_REPOSITORY_STANDARD.md).
5. Use the [submission guide](submission/SUBMISSION_GUIDE.md) and [final submission template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master holds the challenge specification. Teams deliver their analysis and artefacts in their own Mettelo organisation repository. Do not submit team work by replacing this master specification. Use issues, branches, meaningful commits, PRs and reviews to demonstrate actual collaboration.

## Specification map

```text
README.md
project/README.md
project/PROJECT_BRIEF.md
project/BUSINESS_CONTEXT.md
project/DELIVERABLES.md
project/ACCEPTANCE_CRITERIA.md
project/GOVERNANCE.md
data/README.md
data/SOURCE_REGISTER.md
data/raw/README.md
data/reference/README.md
data/metadata/README.md
submission/README.md
submission/TEAM_REPOSITORY_STANDARD.md
submission/SUBMISSION_GUIDE.md
submission/FINAL_SUBMISSION_TEMPLATE.md
```

**Mettelo — Built for What’s Next**
