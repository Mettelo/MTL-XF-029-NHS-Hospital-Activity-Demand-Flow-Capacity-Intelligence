# MTL-XF-029 — Data workspace and support gate

## Core contract

Retain the agreed combined April 2018–March 2026 CSV as the intended input, subject to identity validation. The official March 2026 release separately lists historical 2018/19–2024/25 and 2025/26 M13 MAR CSVs; register these as a two-file fallback if the agreed combined file cannot be validated. Core analysis is at the verified national activity-stream grain. Provider detail and outpatient fields must be confirmed in the acquired MAR schema before inclusion.

## Optional work

Provider/catchment comparison requires a registered provider-level source; outpatient metrics require verified MAR fields or a separately registered provisional-HES source. A&E waiting times, bed occupancy, unmet demand and capacity sufficiency are outside the activity core. Scope must not be silently shifted to another NHS series.

## Acquisition state

No raw data is uploaded by this update. Official documentation checks are recorded in [SOURCE_REGISTER.md](SOURCE_REGISTER.md). File payloads, full schemas, bytes/checksums and final reuse/freeze approvals remain pending where stated. Keep publication-level evidence distinct from acquired-file evidence.

## Required source-to-deliverable matrix

Before analysis, create a row per headline measure/required comparison:

`requirement_id | deliverable_id | metric | core_or_extension | source_id | actual_field_or_sheet | valid_grain | coverage | unit_denominator | metadata_evidence | support_status | owner | decision`

Allowed support statuses: documentation-supported; payload-verified; unsupported; optional-not-activated. “Documentation-supported” alone is insufficient for a completed data freeze. If a mandatory field is absent, block its output and resolve the source or approved scope; do not fabricate values or silently waive the requirement.

## Controlled preparation

1. Use registered exact URLs and inspect actual content type, archive members or sheets.
2. Record version, resolved URL, separate retrieval timestamps, bytes, SHA-256 and licence evidence.
3. Approve the actual cohort and scope matrix at G1.
4. Preserve original bytes; transform into curated facts with documented types, keys, hierarchies and joins.
5. Account for retained/excluded/quarantined rows and quantify all mapping gaps.
6. Reconcile five source values and execute [DT1–DT10](../project/ACCEPTANCE_CRITERIA.md).

## Model and measures

Reporting month × activity stream × published measure × available provider/geography/category × revision status. Spell, episode, admission, attendance and patient measures are distinct. If data is cumulative, derive monthly increments only within the same valid financial-year series.

The core contract above controls conditional dimensions. Metric formulas have one authoritative home: [DELIVERABLES.md](../project/DELIVERABLES.md). Do not create another incompatible formula copy in the data README.

## Data areas

- [Raw snapshots](raw/README.md): unmodified source bytes only when later authorised and permitted.
- [Reference data](reference/README.md): category/entity/period mappings with version and cardinality.
- [Metadata](metadata/README.md): manifest, dictionary, methodology, lineage and support/freeze decisions.

**Specific control:** Unconfirmed combined-file provenance or cumulative/snapshot handling could invalidate every downstream activity comparison.
