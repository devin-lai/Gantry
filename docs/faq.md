# Frequently asked questions

### Is Gantry open source?

No. This repository contains public documentation, feedback, and binary
releases. The application source remains private. GitHub-generated source
archives contain this repository's documentation and artwork, not the app
implementation. Install the DMG from a published release.

### Is it free?

Official binaries are free for personal, non-commercial use. Business,
employer, and client use requires separate permission. See [LICENSE](../LICENSE).

### Do I need all six agents?

No. Start with one supported tool that has local records. Different agents
expose different measurements; see [compatibility](compatibility.md).

### Does it replace my coding agent?

No. Gantry is a companion dashboard for inspecting local records and supported
configuration. Keep using your existing coding tool. Start with one question in
the [workflow guide](workflows.md).

### Does the Chinese README mean the app has a Chinese interface?

The Chinese README is translated documentation. It does not promise a localized
application interface. [Read the Chinese introduction.](../README.zh-CN.md)

### Does Gantry need my API keys or provider login?

There is no Gantry login or API-key setup for local inspection. If you choose
to benchmark an MCP server, that server can use credentials already in its
configuration or environment. Gantry does not log in to provider accounts to
fetch billing or quota data.

### Does it upload my prompts?

It does not upload session history to a Gantry service. Active MCP benchmarks
can start configured servers or contact chosen HTTP endpoints, and those
services can make their own requests. Read [PRIVACY.md](../PRIVACY.md).

### Will it change my agent setup automatically?

Supported file changes require you to apply a previewed action and create a
backup. Scanning maintains Gantry's own local index. Automatic MCP benchmarking,
if you enable it, starts configured servers. File cleanup and process quitting
are separate actions with separate recovery limits.

### Why does a quota or cost number differ from the provider?

Quota is a locally cached reading. Costs are estimates at API rates rather than
your subscription bill. Missing fields, stale records, and provider accounting
rules can all produce differences.

### Why does macOS block the preview?

Build 79's public preview is ad-hoc signed and not notarized by Apple.
See the [installation guide](getting-started.md) for verification and first-launch
steps. Do not interpret a checksum as notarization.

### Can I help without access to the source?

Yes: describe a reproducible bug, suggest a useful workflow, or improve the
public documentation. See [CONTRIBUTING.md](../CONTRIBUTING.md). Share links to the
official release rather than redistributing the binary.
