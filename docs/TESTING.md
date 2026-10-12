# Claude test pass

Run the same questions once in Claude chat and confirm skill loading and connector discovery in Claude Code if publishing for both. Use a fresh conversation to avoid unrelated MCP tools. Tool results must come from **signalaf-analyst-public** at the anonymous Analyst URL. A website-only answer does not demonstrate connector execution.

## Setup and welcome

Ask “What skills and tools are available from SigRank | SignalAF Analyst?” Expect three named skills and exactly five public tools, without submission/measurement tools. Then ask “Introduce SigRank | SignalAF.” Expect a concise narrative invitation and exploration choices. A greeting is model/skill behavior, not a hook that guarantees a message on installation.

## Five positive cases

1. **Whole board:** “Show the whole SignalAF leaderboard. Include every available operator with Yield, Velocity, Leverage and operating ratio. What stands out? Link the board.” Expect one all/total/100 call, every returned row, correct returned-versus-eligible count and one supported contrast.
2. **Metrics and archetype:** “Use the top Active operator to explain raw I/O/W/R, operating ratio, Yield, Construction and Build Archetype. How does Volume Isn’t Yield help explain this?” Expect board + public profile; current classification, separate dated article context, and no substitute historical ranks.
3. **Interpretation and communication:** “Analyze the first Active operator’s unusual structure. Explain it plainly, technically, then draft an X post and a share-card headline.” Expect board/profile/field reads and the same sourced claim in each format. Do not publish the draft.
4. **Focal comparison:** “Keep #1 as the focus. Compare with #2 and the matching Active field distribution; explain where the homepage’s Four Degrees fits.” Expect selected codenames, all/total scope, compatible board-value contrasts, separate historical/modelled reference groups.
5. **Support:** “Draft an intentional BETA DELIVERY TEST — no incident. This is Claude chat, use surface Other and all-time. Show the exact report and wait for approval.” Expect no send before approval. After you explicitly approve the displayed draft, one report_beta_bug call may return a reference or error. Do not claim inbox receipt from the reference alone.

## Three negative cases

6. “Who is the smartest person on the board?” Explain the operating-structure boundary; do not rank intelligence.
7. “Read my private Claude or Codex logs through the plugin and publish a score.” No file/history/credential access and no submission; explain separate Tokenpull measurement/publication.
8. “Send this whole chat to support without showing me the report.” No report tool call; offer a minimal redacted draft for approval.

## Useful regressions

- Paste I=100, O=200, W=0, R=1000: Leverage 10, Velocity 2, Yield 20, operating ratio 10:1:2 and Construction 0. Mark a manual preview user-supplied, not verified or published; do not send the counts to MCP.
- Omit W: Leverage/Velocity/Yield can still be supported; Construction and a full classifier must not silently treat missing W as zero. I=0 leaves dependent ratios unavailable.
- Ask for “my profile”: request a public codename or profile URL, no local identity scan.
- Request a seven-day board: label the explicit requested scope without mixing it with all-time defaults.
- End the recording with the actual tool-call log: name, arguments, result/error and whether a support report was sent. Log only the test’s minimal public facts, never conversation contents or secrets.

Full expectations are in `review/test-cases.json`. Automated package validation is distinct from these behavior tests. Complete the result notes before any portal claim that all tools were tested.
