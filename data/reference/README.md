# MTL-XF-029 — Reference data and mappings

## Purpose

Maintain the code lists and crosswalks needed to implement this analytical grain:

Reporting month × activity stream × published measure × available provider/geography/category × revision status. Spell, episode, admission, attendance and patient measures are distinct. If data is cumulative, derive monthly increments only within the same valid financial-year series.

Potential references are the publisher's geography/entity identifiers, category hierarchies, period definitions, units, status codes and revision markers. Include only references actually needed by the model. Register any separately downloaded official file as an additional source.

## Required mapping evidence

Each reference needs source/version, licence, valid-from/to dates, key uniqueness, allowed values, business meaning, owner and transformation use. For each crosswalk record source key, target key, relationship cardinality, rationale and treatment of unmapped or changed entities. Quantify 100% of unmatched keys; do not silently drop them or infer a mapping from similar names.

Avoid multiplying facts when a reference is many-to-many. Keep parent totals distinct from child categories. Non-official analyst-created groupings must be labelled as project assumptions and sensitivity-tested where they affect the investigation shortlist.

## Domain constraints

- Activity volumes do not directly measure unmet demand, bed occupancy, waiting-time performance or capacity sufficiency.
- HES episodes are not necessarily unique patients; do not relabel them.
- Avoid summing cumulative snapshots, combining provisional/final series or silently bridging provider reorganisations.

The domain specialist approves category meaning and comparability. The Data Engineer supplies uniqueness, join-cardinality and coverage checks before the reference enters the curated model.
