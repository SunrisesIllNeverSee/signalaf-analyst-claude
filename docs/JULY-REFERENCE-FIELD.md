# July reference field: Analyst integration design

Status: proposed, not implemented. Documented 2026-11-19T19:08:02Z at the owner's request. Scope: documentation only; no connector release or backend change.

## Product intent

Make the frozen July 2026 cohort a first-class proof-of-concept comparison surface. Its 1,642 profiles let people explore the scoring approach across a larger historical population, contrast token-flow patterns and contextualize hypothetical inputs. Keep that role distinct from the live production leaderboard. The cohort has 1,626 seeded public-tokscale profiles and 16 real profiles; neither size nor seeded metrics alone prove representativeness or validate the model.

## Proposed interface

Extend `get_leaderboard`, `get_operator`, `compare_operators` and `get_field_stats` with an explicit dataset selector, provisionally `dataset="live" | "july_2026"`. Preserve live defaults and existing behavior. A historical dataset selection is independent of a current-board window. Reject incompatible live-only windows or filters for July instead of ignoring them or falling back to live data. Update connector input/output schemas and tool descriptions together.

Reuse the application's `getHistoricalBoard()` in `lib/history/board-2026-07-31.ts`, archived entry types and comparison helpers. It loads bundled frozen JSON and does not query Supabase. Preserve the original artifact and checksum. The archive's recorded fields and historical metric definitions remain authoritative; do not mutate frozen values to fit live DTOs.

Support bounded pagination, operator search, numeric sorting, explicit platform/category/seed filters, comparisons and statistics for the selected archive population. Return total matching count, returned count, continuation state and stable row IDs. Keep original archived rank separate from filtered/sorted position. Missing data stays missing. Record per-metric sample sizes and exclusion rules for distributions.

Each archive response should identify dataset, frozen date, generation timestamp, source commit/blob/checksum, chosen filters, selected population and seeded/real counts. Historical provenance must not be replaced by live-board provenance or treated as independent verification.

## Charts and hypothetical comparisons

Return bounded, chart-ready numeric rows or distributions with metric names, units, source links, missingness and coverage. The host can render comparison bars, composition plots, histograms or scatterplots. This proposal does not promise an embedded interactive widget or time-series history.

Hypothetical placement is a separate capability decision: the current plugin intentionally keeps user-supplied counts out of the remote MCP. Preserve that privacy boundary. Do not add upload parameters under the guise of an archive filter. A local/in-conversation comparison may use a complete compatible public cohort; any later server-side preview needs separately documented consent and data handling. Describe any result as hypothetical, not a production rank or published submission.

## Acceptance checks for a future implementation

- Default calls still use the live board; July requests cannot invoke live database reads or silently substitute current data.
- Archive counts and source integrity match the frozen manifest. Pagination covers every matching row without duplicates, and sort/tie behavior is explicit.
- Search, filters and comparison values agree with the website; missing metrics are not zero-filled. Statistical/chart output records its actual population and per-metric coverage.
- Live and archive results cannot silently be mixed into a single percentile, rank or improvement claim.
- Unsupported archive windows and cross-dataset comparison requests return an explicit limitation.
- Every chart and result labels the July proof-of-concept field and keeps seeded origins distinct from verified first-party submissions.
- User-supplied counts are not transmitted by existing public read tools.

## Rollout boundary

This documentation teaches the current browsing path and defines future tool support. It does not add tools, publish a package, change production or update an installed OpenAI plugin cache. The OpenAI package should receive equivalent guidance in its maintained publication source; this repository is the separate Claude distribution.
