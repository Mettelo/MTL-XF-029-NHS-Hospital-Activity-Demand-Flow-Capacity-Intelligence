# MTL-XF-029 — Project brief

This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

**Client:** Confidential NHS Hospital Planning & Service Transformation Directorate. **Decision owner:** Director of Hospital Planning & Service Transformation. **Team:** 6–8. **Duration:** 8 weeks. **Review:** monthly hospital activity planning review.

## Business problem and commission

The simulated hospital planning and service-transformation directorate prepares a monthly activity review for elective and non-elective planning leads. Its first decision is which supported activity streams need a deeper operational evidence request before any capacity response is proposed.

The Director of Hospital Planning & Service Transformation needs to decide which changes in hospital activity warrant a planning investigation. Separate reports can mix episodes, admissions, optional outpatient measures and year-to-date snapshots, making it difficult to tell whether a reported increase is sustained, comparable or explained by revisions.

The consequence is an unclear route from a headline activity movement to the next operational question. Leaders may discuss extra capacity before establishing whether the signal reflects throughput, reporting or case mix. The commission is a verified national activity-stream review that supports a focused request for waiting-list, workforce, bed or pathway evidence. Provider-level action remains conditional on an approved provider source.

> Which hospital activity streams show sustained change requiring planning investigation, and what capacity, waiting-list and workforce evidence is still needed to diagnose service pressure?

**Required management handover:** A monthly planning pack containing verified stream trajectories, baseline comparisons, unit/revision diagnostics and a hypothesis-to-evidence action register. Each case must distinguish the observed activity change, possible explanation and additional operational dataset needed to test it.

See [the management use case](BUSINESS_CONTEXT.md#practical-management-use-case) for how the review meeting uses this evidence.

## Core deliverable boundary

Retain the agreed combined April 2018–March 2026 CSV as the intended input, subject to identity validation. The official March 2026 release separately lists historical 2018/19–2024/25 and 2025/26 M13 MAR CSVs; register these as a two-file fallback if the agreed combined file cannot be validated. Core analysis is at the verified national activity-stream grain. Provider detail and outpatient fields must be confirmed in the acquired MAR schema before inclusion.

**Optional / out of core:** Provider/catchment comparison requires a registered provider-level source; outpatient metrics require verified MAR fields or a separately registered provisional-HES source. A&E waiting times, bed occupancy, unmet demand and capacity sufficiency are outside the activity core. Scope must not be silently shifted to another NHS series.

File availability does not prove dimensional support. Before analytical build, the team completes the source→field→metric→deliverable matrix in [data guidance](../data/README.md). Missing mandatory support blocks the gate and requires an approved official replacement or scope decision.

## Analytical model

Reporting month × activity stream × published measure × available provider/geography/category × revision status. Spell, episode, admission, attendance and patient measures are distinct. If data is cumulative, derive monthly increments only within the same valid financial-year series.

The source contract above controls where a general grain description is conditional. Do not create dimensions absent from the approved input.

## Objectives

1. Every required output states its precise activity unit and whether the input is monthly or cumulative.
2. National core results remain usable without provider data or an outpatient extension.
3. Every capacity hypothesis identifies the missing bed, workforce, waiting-list or case-mix evidence.

## Business questions

1. How have elective and non-elective activity changed across comparable months?
2. How does outpatient activity differ from admitted care?
3. Where are sustained changes visible relative to a declared baseline?
4. What do pandemic effects, revisions and provider changes do to the interpretation?
5. What additional beds, waiting-list and workforce evidence is required before a capacity decision?

## Cross-functional delivery model

| Delivery role | Required project contribution |
| --- | --- |
| Business Analyst / Delivery Lead | Map the monthly hospital activity planning review, document eight prioritised user requirements and maintain requirement→deliverable→test links; Director of Hospital Planning & Service Transformation owns business approval. |
| Data Governance Analyst | Own the MTL-XF-029 source/metadata register, cohort decision, licence evidence and 100% headline-measure lineage; resolve the specific risk: Unconfirmed combined-file provenance or cumulative/snapshot handling could invalidate every downstream activity comparison. |
| Data Engineer | Implement the declared facts, keys, hierarchy and join controls; account for every source row and deliver a second-member reproducible run at the chosen MTL-XF-029 scope. |
| BI Developer | Implement the monthly hospital activity planning review overview, diagnostic and quality pages; reconcile five measures and ensure cohort/extension warnings survive filters and export. |
| NHS Activity & Performance Analyst | Approve activity units and revision status, and reconcile five month/stream measures. |
| Hospital Planning & Operations Analyst | Write up to ten activity investigation cases with missing bed, workforce and waiting-list evidence. |
| Clinical Data Assurance Analyst | Test cumulative resets, provider continuity and distinction between episodes and patients. |

Assign named team members and review partners at kickoff; roles may be combined, but a distinct member must review critical calculations and perform the final clean rerun. The executive and operational stakeholder roles are specified in [business context](BUSINESS_CONTEXT.md).

## Required investigation approach

Compare supported streams using same-month year-on-year changes and a declared baseline index, requiring at least three contiguous comparable monthly flows for persistence. Show a recent baseline and, where valid, a pre-pandemic comparator separately. The investigation list may contain fewer than ten streams and is never padded with invented provider cases.

## Milestones and acceptance

| Gate | Reviewers | Evidence / decision |
| --- | --- | --- |
| G1 — scope/source, end Week 2 | Business Analyst + Data Governance Analyst + domain specialist | Approve actual period, geography, grain, required input and field support in a source-to-deliverable matrix. Official release, split-file fallback links and description resource verified; agreed combined-file identity, MAR field availability and snapshot compatibility pending. Unsupported mandatory outputs remain blocked, not quietly reclassified as completed. |
| G2 — model/metrics, end Week 4 | Data Engineer + domain specialist + independent reviewer | Approve row accounting, keys, hierarchy, join cardinality, five source reconciliations and all core metric definitions. |
| G3 — analytical decision review, end Week 6 | Director of Hospital Planning & Service Transformation + operational stakeholders | Compare supported streams using same-month year-on-year changes and a declared baseline index, requiring at least three contiguous comparable monthly flows for persistence. Show a recent baseline and, where valid, a pre-pandemic comparator separately. The investigation list may contain fewer than ten streams and is never padded with invented provider cases. Retain an evidence-insufficient case and a manual review route. |
| G4 — release, end Week 8 | Simulated Mettelo panel + independent reviewer | Accept D1–D12 only after ten executed domain tests, five BI reconciliations, clean rerun evidence and resolution of all critical/high defects. |

D1–D12 are defined in [deliverables](DELIVERABLES.md). AC1–AC12 and DT1–DT10 are defined in [acceptance criteria](ACCEPTANCE_CRITERIA.md). No real production deployment, automatic funding/service allocation, private-client data or paid-source dependency is required.
