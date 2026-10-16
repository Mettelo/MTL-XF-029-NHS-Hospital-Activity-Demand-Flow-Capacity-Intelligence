# MTL-XF-029 — Data workspace

## Required sources and cohort

NHS England HES Monthly Activity Report, full historical series Apr 2018–Mar 2026. It is a single 22 MB CSV, much more durable and reproducible than relying on monthly A&E file URLs.

Freeze the agreed HES Monthly Activity Report historical CSV for April 2018–March 2026. Inspect provisional/final status, monthly versus year-to-date measures and actual provider/geographic dimensions. Use only supported breakdowns; this is the final HES project, replacing the earlier A&E concept.

[Source register and exact URLs](SOURCE_REGISTER.md)

**Current state:** specification only. No raw datasets have been downloaded or uploaded in this build. Expected size, row count and history statements from the earlier agreement require verification against the actual files. Do not mark the cohort frozen until the manifest and metadata are complete.

## Controlled acquisition and preparation

1. Read [SOURCE_REGISTER.md](SOURCE_REGISTER.md); use the exact agreed URLs and official publisher documentation.
2. Validate that the response is the expected CSV/ODS/XLSX/ZIP rather than an error page. Inspect archive contents and sheet names where relevant.
3. Record resolved URL, UTC retrieval, release, coverage, filename, bytes, SHA-256 and licence evidence. Log discrepancies before changing sources.
4. Preserve original bytes in an approved immutable snapshot; later upload only where instructed and redistribution is permitted.
5. Record source fields, types, valid values, suppression, units and publisher methodology in [metadata](metadata/README.md).
6. Implement the analytical grain below, verify keys/cardinality and account for excluded/quarantined records.
7. Reconcile at least five published measures and create curated outputs reproducibly in the team repository.

## Analytical grain

Reporting month × activity stream × published measure × available provider/geography/category × revision status. Spell, episode, admission, attendance and patient measures are distinct. If data is cumulative, derive monthly increments only within the same valid financial-year series.

## Required metric contract

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

## Mandatory quality risks

- Activity volumes do not directly measure unmet demand, bed occupancy, waiting-time performance or capacity sufficiency.
- HES episodes are not necessarily unique patients; do not relabel them.
- Avoid summing cumulative snapshots, combining provisional/final series or silently bridging provider reorganisations.

1. Reconcile five month/stream values and inspect cumulative versus monthly status.
2. Test financial-year reset when deriving increments from cumulative values.
3. Show a missing month invalidates a twelve-month total.
4. Verify dashboard labels preserve episodes/spells/attendances and contain no inferred occupancy or A&E waiting metric.

## Folder ownership

- [raw](raw/README.md): unmodified approved source snapshots; guidance only at present.
- [reference](reference/README.md): governed code lists, hierarchies and crosswalks.
- [metadata](metadata/README.md): source notices, schema, glossary, lineage and manifest evidence.

Curated data, processing code, logs and test results belong in the team delivery repository. Preserve a reproducible boundary between source inputs and generated products. Do not add personal, confidential or paid-source data.
