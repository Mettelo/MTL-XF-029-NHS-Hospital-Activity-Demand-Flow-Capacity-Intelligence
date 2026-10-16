# MTL-XF-029 — Metadata, lineage and freeze evidence

Metadata makes nhs hospital activity, demand, flow & capacity pressure intelligence reproducible. This folder currently contains guidance; no acquisition manifest or source sign-off is claimed.

## Required records after acquisition

- Source manifest: source ID, exact/resolved URL, retrieval UTC, actual release, filename, bytes, SHA-256, archive members/sheets and coverage.
- Publisher methodology and licence/attribution evidence with provenance and retrieval date.
- Schema and field dictionary: name, type, meaning, units, key role, missing/suppression markers and valid values.
- Business glossary and critical data elements, with named steward and approved definitions.
- Grain, hierarchy and join-cardinality documentation.
- Field-level lineage from raw fields through transformations to each headline metric/dashboard measure.
- Quality profile, row-accounting reconciliation, exclusions, unresolved exceptions and their decision impact.
- Freeze approval, change log and later revision comparisons.

## Model contract

Reporting month × activity stream × published measure × available provider/geography/category × revision status. Spell, episode, admission, attendance and patient measures are distinct. If data is cumulative, derive monthly increments only within the same valid financial-year series.

## Metric definition coverage

- Elective activity: Publisher-defined elective admissions/spells/episodes, labelled precisely with measure.
- Non-elective activity: Publisher-defined non-elective activity using a separate compatible category.
- Outpatient activity: Published attendances/appointments by available type; keep distinct from admitted care.
- Year-on-year activity change: 100 × (monthly activity / corresponding prior-year month − 1), with positive comparable base.
- Trailing twelve-month activity: Sum of twelve genuine contiguous monthly flows; never sum year-to-date cumulative values.
- Activity mix: 100 × compatible activity component / matching stream total; do not divide outpatient attendances by inpatient episodes.
- Baseline index: 100 × current activity / declared comparable baseline; label pandemic and reporting breaks.
- Revision/coverage flag: Available valid months and provisional/final status by stream; display missingness and provider continuity.

Every listed metric needs source fields, transformation/formula, valid grain, unit, numerator/denominator, exclusions, zero/missing behaviour, refresh expectation, owner and test reference. Mark conditional metrics unavailable if the actual source cannot support them.

Store actual evidence only; never invent publisher schema, a completed licence review, a checksum or a stakeholder approval. See [source register](../SOURCE_REGISTER.md) and [acceptance criteria](../../project/ACCEPTANCE_CRITERIA.md).
