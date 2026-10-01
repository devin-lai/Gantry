# Supported tools and measurement limits

Gantry is a native macOS application for **macOS 13 or later**, with a universal
Apple silicon and Intel binary. The following describes the build 79 reader
families, not a promise that every future agent release uses the same formats.

| Tool | Local records Gantry understands | Main limits |
| --- | --- | --- |
| Claude Code | Sessions, usage, cached quota, instructions, skills, agents, MCP, hooks, plugins, and recorded timing. | Quota is cached. Some sessions omit API timing or leave context growth unexplained. |
| Codex | Local session database and rollout files, recorded usage and quota, instructions, skills, agents, MCP, and supported settings. | Database and rollout coverage can differ. Missing or unreadable sources can make totals partial. |
| Cursor | Local configuration, rules, skills, agents, MCP, hooks, and plugins where present. | Gantry does not index Cursor chat usage or quota in this build. |
| Gemini CLI | Local chats and supported configuration, instructions, extensions, and MCP inventory. | No quota coverage is claimed. Fields depend on the local chat format. |
| OpenCode | Local session database and supported configuration, instructions, agents, skills, and MCP inventory. | Recorded fields vary. No quota coverage is claimed. |
| Copilot CLI | Local session database and supported instructions, skills, agents, plugins, hooks, and MCP inventory. | Coverage varies by record format. No quota coverage is claimed. |

## How to interpret the measurements

**Quota** comes from values the agent cached locally; it can be out of date.
Window attribution is a proxy based on recorded sessions. Providers do not
publish the full token-to-subscription-limit weighting.

**Token and context estimates** are labelled as estimates. Recorded total
context can exceed the sum of components Gantry can identify. Gantry leaves the
remainder unattributed; complete context-timeline accuracy is not established.

**Costs** are API-rate estimates where the local usage and model can be read.
They are not subscription invoices, charges made by Gantry, or guaranteed
savings.

**Timing** uses recorded agent measurements or an active MCP benchmark. A slow
server does not establish that every session is slow. HTTP benchmarking is on
demand; stdio benchmarking follows your welcome-screen or Settings choice.

**Missing data** can reflect unreadable files, denied folder access, unsupported
formats, or absent records. Gantry labels source problems and incomplete totals.
It does not query provider accounts to fill gaps.

**Performance** depends on history size, the Mac, and the source format. Large
transcripts can take longer to index or open. Cross-device performance and
complete compatibility with future agent versions are not established.
