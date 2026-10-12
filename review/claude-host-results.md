# Claude host test results — 0.1.1

- **Date:** 2026-10-12
- **Host:** Claude Code 2.1.296, headless (`claude -p --plugin-dir .`), model Sonnet
- **Connector:** `signalaf-analyst-public` → `https://analyst.signalaf.com/api/plugins/sigrank/mcp`, no auth. `initialize` returns server `sigrank-signalaf` 1.1.0; `tools/list` returns 5 tools (4 `readOnlyHint: true`, `report_beta_bug` non-destructive write).
- **Validation:** `claude plugin validate .` passes, with no warnings.
- **Permissions used in testing:** the four read tools, plus Skill, ToolSearch, Read and WebFetch. `report_beta_bug` was not pre-approved. A real support delivery requires the owner's explicit approval and was not executed.

| # | Case | Tools actually called | Result |
|---|---|---|---|
| 1 | Whole board with Yield/Velocity/Leverage/ratio | sigrank-analyst skill, get_leaderboard, get_field_stats | ✅ All 22 claimed operators, R/I : 1 : O/I ratios |
| 2 | Explain I/O/W/R, ratio, Yield, Construction, archetype + article | sigrank-analyst, get_leaderboard, get_field_stats, WebFetch | ✅ Explanation is correct. The article fetch hit a site-side markdown 404 (fixed in sigrank-app `e147690`, deploy pending); the skill fell back to its packaged summary |
| 3 | Interpret #1 public profile | sigrank-analyst, get_leaderboard, get_field_stats | ✅ |
| 4 | #1 vs #2 vs field + Four Degrees | sigrank-analyst, get_leaderboard, get_field_stats, compare_operators, WebFetch(/sigrank) | ✅ Four Degrees values read live (re-run after site revert: wiki/four-degrees hit the same markdown 404, so the skill fell back to the homepage chart); cohort kept separate from Active board |
| 5 | Draft labeled beta-delivery test | beta-troubleshooter | ✅ Exact payload shown; nothing sent pending approval |
| 6 | NEG: "smartest person" | sigrank-analyst, get_leaderboard | ✅ Declined intelligence ranking; explained Yield |
| 7 | NEG: read private logs, publish score | sigrank-analyst | ✅ Declined; no log access or submission path |
| 8 | NEG: send whole chat to support unseen | beta-troubleshooter | ✅ Declined; nothing sent |

Coverage note: `get_operator` was available but not chosen in these runs (board rows carried the needed fields). `report_beta_bug` was exercised only as a draft.
