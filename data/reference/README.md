# MTL-XF-029 — Reference mappings

References support the approved [model and cohort](../README.md). Do not assume a mapping exists solely because entity names look similar.

Required acquisition checks: Fallback history: https://files.digital.nhs.uk/B6/2403F9/HES%20MAR%20data%20Apr%202018%20to%20Mar%202025.csv . Fallback 2025/26: https://files.digital.nhs.uk/F1/007ED5/HES%20MAR%202025-26%20M13.csv . Description workbook: https://files.digital.nhs.uk/74/C31B84/Hospital%20Episode%20Statistics%20Monthly%20Activity%20Report%2C%20March%202026%20-%20Dashboard%20Data%20Descriptions.xlsx . Confirm units, measure types, grain, snapshots and schema compatibility before combining.

For each mapping record source/version, licence, key, definition, valid dates, uniqueness, relationship cardinality, unmatched coverage and responsible domain steward. Quantify every unmapped category/entity. Keep totals distinct from components and do not multiply fact rows through many-to-many crosswalks.

Analyst-created groupings and eligibility thresholds are labelled project assumptions. If they affect case selection, show their effect in [the scenario comparison](../../project/ACCEPTANCE_CRITERIA.md). Candidate raw field names or download references in the source register still require actual version validation.
