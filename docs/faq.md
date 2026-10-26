# Frequently asked questions

### Which file should I install?

Download the DMG from the [official release page](https://github.com/devin-lai/Gantry/releases/latest).
Follow the [installation guide](getting-started.md) to verify it and install Gantry.

### Is it free?

**Completely free, including for commercial use.** Personal projects, business,
employer, and client use are all permitted without charge or separate permission.
This also applies to previously downloaded official releases. See [LICENSE](../LICENSE).

### Do I need all six agents?

No. Start with one supported tool that has local records. Different agents
expose different measurements; see [compatibility](compatibility.md).

### Where did the generated Codex project folders go?

Independent conversations now live in **Sessions → No project**. A shortcut
from Projects takes you there. The conversation's actual working folder stays
in Details; Gantry does not move or delete it to organize the list. When local
metadata cannot establish membership, the session remains **Project not recorded**.

### Can I use 1.3 on macOS 13?

Version 1.3 requires **macOS 14.5 or later**. Earlier releases remain on the
[Releases page](https://github.com/devin-lai/Gantry/releases), with their original
requirements and limitations.

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

### Why does macOS block the download?

Gantry 1.3.0 is ad-hoc signed and not notarized by Apple.
See the [installation guide](getting-started.md) for verification and first-launch
steps. Do not interpret a checksum as notarization.

### Does a handoff note use another model?

No. It assembles recorded session content, labels its sources and cuts, and
copies the result when you ask. It does not generate a new model summary.
Review the note for private content before sharing it.

### Does Gantry commit my files or resume an agent automatically?

Git checks are read-only. Copying a resume command or handoff note does not
execute it. You decide where and how to continue.

### Why are details missing from an older Codex session?

Some sessions are initially indexed from only part of the local rollout.
Use **Load session details** where offered. Files that are missing,
unsupported, malformed, changing, or over the read limits may still be
incomplete. See [compatibility](compatibility.md).

### How can I help?

Describe a reproducible bug, suggest a useful workflow, or improve the
public documentation. See [CONTRIBUTING.md](../CONTRIBUTING.md). Share links to the
official release rather than redistributing the binary.
