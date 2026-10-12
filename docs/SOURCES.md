# Sources and official references

Checked 2026-10-10. The exact source OpenAI archive and SHA256 are recorded in `review/source-provenance.json`. Runtime methodology and article links remain in the analyst skill’s references; no new classifier, metric, source population or favored operator was added.

| Information | Where to find it |
| --- | --- |
| Frozen Analyst instructions, welcome, support, eight teaching guides | This package’s `skills/`; provenance records match each file to OpenAI 0.1.31 |
| Anonymous public tools | https://analyst.signalaf.com/api/plugins/sigrank/mcp; read-only discovery snapshot in `review/mcp-tools-snapshot.json` |
| Website implementation and shared Analyst server | https://github.com/SunrisesIllNeverSee/sigrank-app |
| Separate measurement/submission implementation | https://github.com/SunrisesIllNeverSee/sigrank-mcp; not connected by this package |
| Current method and ten archetypes | https://signalaf.com/methodology, https://signalaf.com/metrics, https://signalaf.com/wiki#archetypes; prefer actual returned classifier version |
| Article interpretation | `skills/sigrank-analyst/references/methodology-and-articles.md` links the current articles and explains their cohort/date boundaries |
| Website board | https://signalaf.com/board/all; live tool-returned board URL is authoritative for each call |
| Claude layout and testing | https://claude.com/docs/plugins/build |
| Manifest and listing fields | https://code.claude.com/docs/en/plugins/manifest-reference |
| Host component support | https://claude.com/docs/plugins/platform-support |
| Repository validation | https://claude.com/docs/plugins/pre-submission-checklist |
| Plugin submission | https://claude.com/docs/plugins/submit |
| Both connector and bundle | https://claude.com/docs/directory/publish |
| Connector quality and submission | https://claude.com/docs/connectors/building/review-criteria and https://claude.com/docs/connectors/building/submission |

The ZIP is for Claude installation; public bundle submission reads a GitHub repository. Published requirements and portal behavior can change; use the linked official pages and actual validation results at submission time.
