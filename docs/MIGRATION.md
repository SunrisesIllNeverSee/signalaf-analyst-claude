# Claude adaptation record

Prepared 2026-10-10 from the exact submitted OpenAI archive `signalaf-analyst-0.1.31-public-review.zip`, SHA256 c0ece8fc238a6ebc28591000326b9ccfff7c475265b8ab00893fa24a31f1f907. The source archive is unchanged. OpenAI 0.1.31 is in review according to the owner; no OpenAI submission was modified to prepare this package.

The Claude release starts its independent sequence at **0.1.0**. Internal name `signalaf-analyst` and visible identity **SigRank | SignalAF Analyst** are retained. The MCP key and HTTPS endpoint are the same anonymous Analyst connection. No website, database, scoring, MCP tool, or deployment change is included.

## Packaging changes

- Use `.claude-plugin/plugin.json`, with Claude’s supported display, icon, policy-link and metadata fields. Use root `.mcp.json` with `type: http`. Default component discovery loads the skills and connector once.
- Carry over the existing section-sign artwork and all three skills plus eight analyst references. Per-file hashes are in `review/source-provenance.json`.
- Adapt the welcome’s supported-host sentence; update the analyst’s endpoint reference to the isolated hostname.
- Replace Codex-only local identity lookup with explicit public-codename lookup. Remove the local identity script and its tests from the Claude package. Related reference sentences now describe the same boundary. No local usage analysis is introduced.
- Describe Claude surfaces in beta triage. The shared tool accepts ChatGPT, Codex, Website, Other; use **Other** for Claude and spell out chat/Cowork/Claude Code in the report’s summary or steps.
- Retain five positive and three negative cases, changing only the host-specific beta case and private-log prompt. Cases are plain review documentation, not a claim of completed Claude execution.
- Use the existing upstream MIT license. Replace OpenAI-specific roadmap/submission/history documents with this Claude README and handoff documentation; preserve runtime methodology and narrative in the skills.

There are no local MCP servers, measurement collectors, submission routes, hooks, agents, model settings, userConfig prompts, credentials, or app ownership bindings in this package. It changes no metric formula, archetype rule, board preference, or operator emphasis.


## 0.1.1 (2026-10-12)

- Four Degrees of Leverage now referenced at its stable URL https://signalaf.com/wiki/four-degrees (the homepage placement varies with site redesigns). No metric, rule or tool change.
- Added marketplace manifest and README install line; set `repository`.
- Claude host test results recorded in `review/claude-host-results.md`.


## 0.1.2 (2026-10-14)

- Publisher name changed from "SignalAF" to "SigRank SignalAF Analyst" in `plugin.json` and `marketplace.json` (the directory's name check flagged "SignalAF" as close to an unrelated listing).
- Removed `displayName`, `documentationUrl`, `supportUrl` and `termsOfServiceUrl` from `plugin.json`; the directory's validator reported them as fields it doesn't read. Those links are entered in the directory submission form instead. `privacyPolicyUrl` is kept because the directory asks for it explicitly. No skill, connector or metric change.
