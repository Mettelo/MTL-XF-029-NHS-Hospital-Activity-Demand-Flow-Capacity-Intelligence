# MTL-XF-029 — Governance and decision controls

This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

## Authority and accountability

**Director of Hospital Planning & Service Transformation** owns business scope, prioritisation assumptions, accepted analytical limitations and investigation recommendations. The Mettelo review panel owns programme acceptance. Operational responsibilities are in [business context](BUSINESS_CONTEXT.md); delivery-role artefacts are in [the project brief](PROJECT_BRIEF.md).

The Data Governance Analyst approves source identity, metadata, licence evidence and field support. The Data Engineer owns transformations and reruns. Domain specialists approve interpretation; a distinct reviewer checks critical calculations and executes or reviews DT1–DT10. Combining delivery roles does not remove review accountability.

## Stage gates

| Gate | Accountability | Required review |
| --- | --- | --- |
| G1 — scope/source, end Week 2 | Business Analyst + Data Governance Analyst + domain specialist | Approve actual period, geography, grain, required input and field support in a source-to-deliverable matrix. Official release, split-file fallback links and description resource verified; agreed combined-file identity, MAR field availability and snapshot compatibility pending. Unsupported mandatory outputs remain blocked, not quietly reclassified as completed. |
| G2 — model/metrics, end Week 4 | Data Engineer + domain specialist + independent reviewer | Approve row accounting, keys, hierarchy, join cardinality, five source reconciliations and all core metric definitions. |
| G3 — analytical decision review, end Week 6 | Director of Hospital Planning & Service Transformation + operational stakeholders | Compare supported streams using same-month year-on-year changes and a declared baseline index, requiring at least three contiguous comparable monthly flows for persistence. Show a recent baseline and, where valid, a pre-pandemic comparator separately. The investigation list may contain fewer than ten streams and is never padded with invented provider cases. Retain an evidence-insufficient case and a manual review route. |
| G4 — release, end Week 8 | Simulated Mettelo panel + independent reviewer | Accept D1–D12 only after ten executed domain tests, five BI reconciliations, clean rerun evidence and resolution of all critical/high defects. |

## Data/source control

Use the [source register](../data/SOURCE_REGISTER.md) as the authoritative evidence record. Preserve agreed URLs and explicitly label new required references, supplements and fallbacks. Record each actual file's resolved URL, retrieval UTC, release, scope, bytes, checksum and licence notices. Public access alone is not proof of unrestricted redistribution. No raw-data upload is part of this update.

Freeze input files only after the source-to-deliverable matrix passes; retain original bytes in an approved location and never overwrite a snapshot. A fallback must have a documented activation reason, compatible coverage and version-selection rule. Do not stack overlapping combined and fallback inputs.

## Domain interpretation

- Activity volumes do not directly measure unmet demand, bed occupancy, waiting-time performance or capacity sufficiency.
- HES episodes are not necessarily unique patients; do not relabel them.
- Avoid summing cumulative snapshots, combining provisional/final series or silently bridging provider reorganisations.

**Primary risk:** Unconfirmed combined-file provenance or cumulative/snapshot handling could invalidate every downstream activity comparison.

The [metric contract](DELIVERABLES.md) and [domain tests](ACCEPTANCE_CRITERIA.md) govern calculations. Thresholds/weights that are project choices must be labelled as such, with baseline and alternative scenarios; they are not official service standards. No automatic allocation or regulatory/professional certification is implied.

## Core and extension change control

Provider/catchment comparison requires a registered provider-level source; outpatient metrics require verified MAR fields or a separately registered provisional-HES source. A&E waiting times, bed occupancy, unmet demand and capacity sufficiency are outside the activity core. Scope must not be silently shifted to another NHS series.

Every source/scope change records requester, date, reason, old/new requirement, coverage/schema impact, affected KPIs/artefacts/tests, owner, reviewer and decision. Missing mandatory evidence blocks the dependent release; it is not resolved by relabelling a promised deliverable unavailable. Optional models need a naive baseline, appropriate holdout, leakage checks, uncertainty and a named reviewer.

## Reuse, information and repository controls

Never commit secrets, private correspondence or unnecessary personal details. Preserve suppression and publication notices. Check screenshots and exports for permitted publication. The team repository must be under Mettelo with individual member accounts, evidence-linked contributions and reviews. Record environment, manifest and final commit/tag so reviewers can reproduce results without paid-only access. Accurately describe verified participation; do not claim real-client employment, endorsement, operational adoption or achieved savings.
