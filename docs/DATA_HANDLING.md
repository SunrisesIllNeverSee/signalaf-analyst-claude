# Prepared data-handling notes

These are factual handoff notes for portal answers; the publisher confirms them in the actual form.

| Path | Data and handling |
| --- | --- |
| Public reads | Board filters and public codenames go to the declared Analyst MCP; public operator records and aggregate counts return. Public profile identifiers are still data about people and should not be described as “no personal data ever.” |
| Manual preview | A user may voluntarily provide aggregate counts in Claude. They are not sent to the Analyst MCP. Visiting and using the separate SignalAF paste page sends the entered numbers to that website; describe this distinction. |
| Beta report | Approved summary, reproduction steps, expected/actual behavior, surface, relevant window, and optional user-supplied reply email/version/tool. Never attach credentials, raw logs, private telemetry or the chat. |
| Delivery | SignalAF uses Resend to deliver the report to hello@signalaf.com. The sending user sees a reference or error. Claude surfaces map to Other in the current schema. |
| Rate limiting | Existing server temporarily uses IP-based Upstash rate limits, with one-hour expiry; IP is not attached to the support email. |
| Retention | Reports stay while open; personal details are retained for 90 days after closure, with earlier deletion requested at hello@signalaf.com. Owner-operated email cleanup; no bundled retention worker. |
| Local access | None. This package has no local identity resolver, log collector, shell hook, or account connection. It does not query Claude memory/history. |

Service links: [privacy](https://signalaf.com/privacy), [terms](https://signalaf.com/terms), [support](https://signalaf.com/support). The server and these policies are shared with the submitted OpenAI Analyst; this package does not change them. Age-audience and legal acknowledgements remain publisher decisions; they are not inferred from the statistics use case.
