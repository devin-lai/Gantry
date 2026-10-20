# Supported tools and measurement limits

Gantry is a native macOS application for **macOS 13 or later**, with a universal
Apple silicon and Intel binary. The following describes the 1.2.0 reader
families, not a promise that every future agent release uses the same formats.

| Tool | Local records Gantry understands | Main limits |
| --- | --- | --- |
| Claude Code | Sessions, usage, cached quota, instructions, skills, agents, MCP, hooks, plugins, and recorded timing. | Quota is cached. Some sessions omit API timing or leave context growth unexplained. |
| Codex | Local session database and rollout files, recorded usage and quota, instructions, skills, agents, MCP, and supported settings. | Database and rollout coverage can differ. Missing or unreadable sources can make totals partial. |
| Cursor | Desktop conversation history and search, project discovery, configuration, rules, skills, agents, MCP, hooks, and plugins where present. | Usage, cost, quota, and a terminal resume command are unavailable. Missing or unsupported message records make search partial. |
| Antigravity | Local conversation indexes, readable SQLite conversation stores and JSONL transcripts, usage where recorded, configuration, instructions, skills, and MCP inventory. | Older encrypted conversation files cannot be read. Transcript search needs a readable JSONL transcript. No quota coverage is claimed. Replaces Gemini CLI support in 1.1. |
| OpenCode | Local session database and supported configuration, instructions, agents, skills, and MCP inventory. | Recorded fields vary. No quota coverage is claimed. |
| Copilot CLI | Local session database and supported instructions, skills, agents, plugins, hooks, and MCP inventory. | Coverage varies by record format. No quota coverage is claimed. |

## How to interpret the measurements

**Live states** distinguish Working and Ready for Claude Code and Codex, and
recorded permission waits for Claude Code. Other tools show Running. Optional
notices depend on macOS notification permission and the agent's local records.
Codex approval prompts and questions are not presented as a Waiting state.

**Session details** show recorded endings and commands for Claude Code and
Codex. Claude Code permission-decision counts require records from 2.1.294 or
later. Command review describes recorded tool inputs; it does not establish
what a command changed or provide a security verdict. Older or large Codex
rollouts may initially be read only from their tail. **Load session details**
can recover more of a selected local conversation, with progress, cancellation,
retry, and persistent caching. Missing, unsupported, malformed, changing, or
over-limit records can remain incomplete; Gantry labels those gaps.

**Changed files and handoff** use recorded edit tools from Claude Code, Codex,
Cursor, and Antigravity where supported. They do not capture all shell-command
side effects. Git status is a read-only observation of the checkout now, not
proof of who made a change. A handoff note uses recorded content, labels cuts,
and may contain private text or paths. A resume command is offered only where
supported; Cursor desktop conversations have no terminal resume command.

**Agent capabilities** resolve skills and MCP configuration for the selected
tool and working directory. Configuration availability, Gantry's connection
checks, and verification inside the tool are distinct. Managed policy, account
state, launch overrides, remote environments, and dynamic providers can limit
what local files establish. Supported configuration edits are for specific
Claude Code and Codex controls; the app does not provide universal editors for
every supported tool.

**Quota** comes from values the agent cached locally; it can be out of date.
Window attribution is a proxy based on recorded sessions. Providers do not
publish the full token-to-subscription-limit weighting.

**Token and context estimates** are labelled as estimates. Recorded total
context can exceed the sum of components Gantry can identify. Gantry leaves the
remainder unattributed; complete context-timeline accuracy is not established.

**Costs** are API-rate estimates where the local usage and model can be read.
They are not subscription invoices, charges made by Gantry, or guaranteed
savings. Tail-only Codex records can produce a less complete estimate than a
full detail read.

**Timing** uses recorded agent measurements or an active MCP benchmark. A slow
server does not establish that every session is slow. HTTP benchmarking is on
demand; stdio benchmarking follows your welcome-screen or Settings choice.

**Missing data** can reflect unreadable files, denied folder access, unsupported
formats, or absent records. Gantry labels source problems and incomplete totals.
It does not query provider accounts to fill gaps.

**Performance** depends on history size, the Mac, and the source format. Large
transcripts can take longer to index or open. Cross-device performance and
complete compatibility with future agent versions are not established.
