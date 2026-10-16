# MTL-XF-029 — Source register and verification record

**Project:** NHS Hospital Activity, Demand, Flow & Capacity Pressure Intelligence  
**Documentation review:** 16 October 2026  
**State:** official documentation checked; acquired-file validation and freeze approval pending.  
**Steward:** Data Governance Analyst, with the project domain specialist.

## Source/cohort decision

Retain the agreed combined April 2018–March 2026 CSV as the intended input, subject to identity validation. The official March 2026 release separately lists historical 2018/19–2024/25 and 2025/26 M13 MAR CSVs; register these as a two-file fallback if the agreed combined file cannot be validated. Core analysis is at the verified national activity-stream grain. Provider detail and outpatient fields must be confirmed in the acquired MAR schema before inclusion.

**Outside core:** Provider/catchment comparison requires a registered provider-level source; outpatient metrics require verified MAR fields or a separately registered provisional-HES source. A&E waiting times, bed occupancy, unmet demand and capacity sufficiency are outside the activity core. Scope must not be silently shifted to another NHS series.

## Official publication and methodology references

| Official reference | URL |
| --- | --- |
| Official March 2026 M13 release and data descriptions | https://digital.nhs.uk/data-and-information/publications/statistical/provisional-monthly-hospital-episode-statistics-for-admitted-patient-care-outpatient-and-accident-and-emergency-data/april-2025---march-2026-m13 |

References above were inspected for this revision. They establish only the evidence described below; they are not a completed file acquisition, licence clearance or signed freeze.

## Verification findings

The official release describes provisional data and country-level publication coverage. Its resource list separates historical MAR data to March 2025 from a 2025/26 M13 CSV and also lists distinct provisional-HES, provider and description resources. It does not establish that the previously agreed combined URL has identical fields or coverage; treat that identity as pending, not a confirmed failure.

**Field/reference mapping and acquisition instructions:** Fallback history: https://files.digital.nhs.uk/B6/2403F9/HES%20MAR%20data%20Apr%202018%20to%20Mar%202025.csv . Fallback 2025/26: https://files.digital.nhs.uk/F1/007ED5/HES%20MAR%202025-26%20M13.csv . Description workbook: https://files.digital.nhs.uk/74/C31B84/Hospital%20Episode%20Statistics%20Monthly%20Activity%20Report%2C%20March%202026%20-%20Dashboard%20Data%20Descriptions.xlsx . Confirm units, measure types, grain, snapshots and schema compatibility before combining.

**Remaining status:** Official release, split-file fallback links and description resource verified; agreed combined-file identity, MAR field availability and snapshot compatibility pending.

## Exact copyable file URLs

Original agreed URLs are retained. Entries labelled required supplement/reference or fallback are explicit changes from the initial pack. Do not silently replace an input with a newer release.

### S1 — Agreed combined MAR CSV — identity still pending

```text
https://files.digital.nhs.uk/7C/B29FFA/HES%20MAR%20data%20Apr%202018%20to%20Mar%202026.csv
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

### F1 — Registered fallback history — use only after identity/scope decision

```text
https://files.digital.nhs.uk/B6/2403F9/HES%20MAR%20data%20Apr%202018%20to%20Mar%202025.csv
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. This is a controlled fallback, not an instruction to stack it with the original combined file.

### F2 — Registered fallback 2025/26 M13 — paired with F1

```text
https://files.digital.nhs.uk/F1/007ED5/HES%20MAR%202025-26%20M13.csv
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. This is a controlled fallback, not an instruction to stack it with the original combined file.

### R1 — Required MAR description workbook

```text
https://files.digital.nhs.uk/74/C31B84/Hospital%20Episode%20Statistics%20Monthly%20Activity%20Report%2C%20March%202026%20-%20Dashboard%20Data%20Descriptions.xlsx
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Reference metadata; match its version to the analytical input.

## File validation and licence record

For every actually used input record:

`source_id, role_core_reference_fallback_extension, original_url, resolved_url, retrieved_utc, actual_release, filename, bytes, sha256, format, sheets_or_members, rows, geography, period_start, period_end, grain, schema_version, methodology_evidence, licence_notice, attribution, redistribution_conditions, approved_by, approval_date`

Retain the relevant publication/file notices, including exceptions and third-party conditions. Do not assume all publishers use the same licence. A stated publication licence does not remove the need to check file-specific terms. Keep unverified values pending; never invent a hash or approval.

## Support and freeze decision

Complete the [source-to-deliverable matrix](README.md). The domain specialist verifies actual grain, units, period comparability and supported metrics; the steward verifies identity and reuse terms. Required missing fields block dependent core outputs. Every activated extension is separately registered. Where a fallback is used, record why, which original it replaces, overlap handling and impact on outputs.

If an agreed URL fails, seek the same official archived release and record evidence. A browser format limitation does not prove a file is unavailable, and a successful page fetch does not prove payload integrity. Preserve the frozen version and metadata in the approved location so future website changes do not silently alter the cohort.
