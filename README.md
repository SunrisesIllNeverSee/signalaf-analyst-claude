# SigRank | SignalAF Analyst

![SigRank section-sign logo](assets/icon.png)

**Performative stats and benchmarks for AI users, not models.**  
**AI Operator Leaderboard**

Models have benchmarks; here, AI operators take the spotlight. Explore the whole live SignalAF board, discover distinctive operating patterns, and find other builders through shared statistics. Use the metrics to understand how fresh input, output, cache creation, and cache reuse combine into a token cascade.

**Tokenpull measures → SigRank evaluates → SignalAF publishes.**

This is a separate Claude release, version **0.1.1**, adapted from the submitted OpenAI **0.1.31** package. It supports Claude chat, Cowork, and Claude Code through three skills and one public remote connector.

## Install

In Claude Code:

```sh
/plugin install signalaf-analyst --marketplace SunrisesIllNeverSee/signalaf-analyst-claude
```

## Try it

1. Upload the supplied ZIP in Claude: Customize → Plugins → Add → Upload plugin.
2. Open the plugin’s Connectors tab and add/connect **signalaf-analyst-public**. Its server is `https://analyst.signalaf.com/api/plugins/sigrank/mcp`. Choose **No sign in** if Claude asks about authentication. No SignalAF account, API key, or Supabase client is required.
3. Start a fresh chat and ask: “Introduce SigRank | SignalAF, then show the whole live Active board and explain one interesting contrast.”

For local Claude Code testing from this directory:

```sh
claude plugin validate .
claude --plugin-dir .
```

The plugin identifier is `signalaf-analyst`; its skill names are `get-started`, `sigrank-analyst`, and `beta-troubleshooter`. Skills load by relevance. No forced startup hook or guaranteed automatic greeting is claimed; ask for an introduction to exercise the welcome.

Claude Code 2.1.281 or later recognizes the directory icon and policy-link fields. Older versions can load the package but their validator warns about those fields; use current Claude Code for a strict validation run. Validated with Claude Code 2.1.x on 2026-10-12 (see `review/claude-host-results.md`).

## Explore

- “Show the whole live Active board. Include Yield, Velocity, Leverage, and operating ratio.”
- “Explain the top operator’s four token pillars and Build Archetype.”
- “Compare the first operator with a peer and the matching field distribution.”
- “Explain why volume and Yield tell different stories.”
- “Help me understand my pasted aggregate token counts and a hypothetical board position.”

The default board is **Active / Total / All-time**. An explicit request for a different supported period is handled separately. Current ranks and names come from the tools, not bundled examples. The welcome and explanations adapt to the question’s tone and depth. Archetypes describe operating patterns. Metrics describe observable AI operating structure, not intelligence, productivity, work quality, or personality.

## What connects and runs

The only bundled connection is the anonymous Analyst MCP on **analyst.signalaf.com**. Claude calls four public read tools: `get_leaderboard`, `get_operator`, `compare_operators`, and `get_field_stats`. A fifth tool, `report_beta_bug`, sends a minimal report to **hello@signalaf.com** through SignalAF’s existing support service, only after you approve its displayed contents.

The plugin contains Markdown skills, JSON configuration, and artwork. It starts no local service, installs no dependencies, and has no hooks or executable helpers. It does not read identity files, usage logs, Claude memory, chat history, credentials, or account telemetry. To find your public profile, supply a public codename or SignalAF profile URL.

Local measurement uses Tokenpull. Enrollment, score uploads, and board submissions belong to the separate SigRank submission system. This package does not connect that system. A pasted-count analysis stays in the conversation; selecting SignalAF’s separate paste-preview website sends the numbers you enter there to that website, as its guide explains.

## Privacy policy

Public lookups send the requested board filters or public codenames to SignalAF. Private prompts, chat transcripts, raw logs, signing keys, and identity files are not requested or attached to support reports. A user-supplied reply email is optional. Approved support reports are delivered through the existing Resend email service to hello@signalaf.com; temporary IP-based rate limiting uses Upstash. Support retains reports while open and personal details for 90 days after closure, with earlier deletion available by emailing support. Retention cleanup is an owner-operated inbox process, not a bundled automation.

See the published [privacy policy](https://signalaf.com/privacy), [terms](https://signalaf.com/terms), [support](https://signalaf.com/support), and [product documentation](https://signalaf.com/plugin). These describe SignalAF’s handling; Anthropic’s handling of your Claude conversation is governed by your Claude service terms and settings.

## Release and review

This ZIP is ready for local installation and testing. Directory submission uses a GitHub repository and Claude’s developer portal. See [submission steps](docs/SUBMISSION.md), [test prompts](docs/TESTING.md), [release provenance](docs/MIGRATION.md), and [validation status](docs/VALIDATION.md). Claude host behavior and portal checks must be completed before claiming the release has passed Claude review. The existing OpenAI recording is supporting material, not proof of Claude behavior.

License: MIT, preserving the existing SignalAF repository license and copyright notice.
