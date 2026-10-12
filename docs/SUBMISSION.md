# Submit the Claude release

Package preparation is complete; Claude host testing and directory submission are separate steps. Use the same paid Claude account/organization for the connector and bundle. Current official guidance requires a remote server listing as well as a bundle listing when you own both. [Directory publishing](https://claude.com/docs/directory/publish)

## 1. Install and test

Upload the ZIP through Customize → Plugins → Add → Upload plugin. Connect its remote entry with No sign in. Run the five positive and three negative cases in `review/test-cases.json`; record actual tool calls and results. Exercise an approved, explicitly labeled support delivery test if you intend to attest all five tools were executed. The prior OpenAI test and video do not establish Claude execution. [Package testing](https://claude.com/docs/plugins/build)

## 2. Publish the source

Put the **contents** of this package at the root of a dedicated GitHub repository, with `.claude-plugin/plugin.json` directly below that root. A dedicated repository avoids bringing website dependencies and unrelated files into review. Select the intended owner; connect the GitHub account to Claude and confirm push access. The repository may be private during preparation but must be public before the listing goes live. The `repository` manifest field is intentionally omitted until an actual source URL exists. [Plugin submission](https://claude.com/docs/plugins/submit)

## 3. Submit the connector

Open https://claude.ai/directory/manage → Submit new → MCP connector. Enter the exact anonymous HTTPS endpoint from `.mcp.json`. Use No authentication. Reuse the prepared listing, company, support and privacy values in `review/listing.json`. Explain reviewer access: no credentials, populated public board, connect and run the public tools. Provide actual test evidence. Current tools declare top-level titles and read/write hints; have the portal confirm their interpretation. The support tool is a non-destructive write requiring approved contents. If Claude flags its annotations, record the finding for a coordinated server change rather than silently changing the endpoint while OpenAI review is active. [Connector submission](https://claude.com/docs/connectors/building/submission)

## 4. Submit the bundle

Submit new → Plugin bundle. Enter the actual repository, leave the plugin path empty for a root package, and select the intended tracked branch/tag. Validate that commit, resolve actual blocking findings, check the listing and data handling, then review the policy acknowledgements. Pair it with the same-organization connector using the identical server URL. [Bundle requirements](https://claude.com/docs/plugins/pre-submission-checklist)

## 5. Finish as publisher

The owner verifies the final publisher/organization, data-handling answers, intended age audience and compliance acknowledgements, then submits. No claims of legal compliance, reviewer credentials, completed Claude tests, or approval are prefilled as attestations. Publication is a later action once the applicable review permits it. Name/slug availability and portal validation are pending.

This package is text/tools, without an interactive MCP App. Do not claim it has an interactive dashboard or apply MCP App carousel requirements as if that feature existed. The existing YouTube walkthrough may be included as OpenAI supporting context; record a Claude run if a Claude-specific demo is requested.
