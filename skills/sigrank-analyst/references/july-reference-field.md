# July 2026 reference field — proof of concept

The [historical leaderboard](https://signalaf.com/board/history) is frozen as of July 31, 2026. It contains 1,642 profiles: 1,626 seeded from public tokscale numbers and 16 recorded as real. Its source manifest identifies commit `4c610df9a78a6c396e0404d6e776919ac11c40c5`, blob `1a24939623ea0a8efeaaa68ba0e5818c684f7203`, and snapshot generation time `2026-07-31T12:09:09.303Z`.

## Why this field matters

Use this reference cohort to demonstrate the scoring approach across a larger set of profiles, explore how token-flow patterns differ, and compare archived operators, distributions and hypothetical positions. It is a proof-of-concept comparison surface. Its size does not establish a representative population, independently validated measurements, predictive performance or proof of the scoring model. Seeded public-number profiles are not verified first-party submissions.

The live production board serves operators submitting their own data. Keep its placements and statistics separate from this frozen reference cohort. Do not silently combine the two populations.

## Current access and supported claims

- The existing four Analyst read tools query the current board; none currently accepts `dataset="july_2026"`. That selector is proposed, not available. `window="all"` is a current-board aggregation window.
- When public browsing is available, open the exact archive page. State filters, sort metric, row coverage and source date. A paginated page does not prove the whole field was retrieved. Do not calculate full-field percentiles from one visible page or use current `get_field_stats` for archive statistics.
- Preserve archived values and explicit missingness. Do not silently recompute historical metrics using a newer ruleset, assume every optional pillar exists, or label a derived quantity as published.
- For user-provided counts, keep analysis in the conversation and respect the manual-preview guide. A position against July is hypothetical, not submission, publication, a verified placement or a live rank. Exact placement requires the complete relevant cohort and explicit sorting/tie rules; otherwise explain the comparison without inventing a rank.
- Charts may depict archived distributions, composition or comparisons when source values and coverage are available. One frozen snapshot is not a time series and cannot establish growth or causal improvement.

Suggested label: **July 2026 Reference Field — Proof of Concept · Frozen July 31, 2026**. Accompany numerical results with the selected cohort size and seeded/real composition. Keep archive rank distinct from a row's position after filtering or sorting.

For the implementation proposal, see [archive integration design](../../../docs/JULY-REFERENCE-FIELD.md).
