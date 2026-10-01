# Four ways to start with Gantry

[Download and install](getting-started.md) · [Supported tools](compatibility.md) · [Back to the overview](../README.md)

Start with one supported coding agent that has local records. Read the welcome
screen before enabling automatic stdio MCP benchmarking. Keeping it disabled
lets you explore the inventory and recorded evidence first.

## 1. Check your quota runway

**For Claude Code and Codex users with locally cached quota records.**

1. Open **Overview** and find the available quota windows.
2. Check the source freshness, remaining quota, and reset time together.
3. Use the menu bar view if you want to keep the available quota readings nearby.

Use this to decide whether to start another session or check the provider's
usage page. Gantry reads local cached values, so a missing or stale reading is
not a live statement of your account balance. It does not ask you to log in to
your provider.

## 2. Understand what loads before your first prompt

**For users with project instructions, skills, rules, or MCP configuration.**

1. Open **Inventory** and inspect the items Gantry found for your agent and project.
2. Look at instruction files, skills, agent definitions, and MCP schemas, including their sources and available estimates.
3. Where your agent records startup context, compare that measurement with the identifiable configuration components.

Use this to review a setup that has grown over time. An inventory item is not
proof that the agent used it in every session. Estimates and recorded totals
can differ, and Gantry leaves unexplained context unattributed.

## 3. Investigate a slow MCP server

**For users who have configured an MCP server.**

1. Find the server in **Inventory** and inspect the available status and timing evidence.
2. If you want a fresh measurement, choose an active benchmark for that server.
3. Review initialization and tool-list timings. Compare with recorded session timing where your agent provides it.

An active benchmark can launch a stdio server or contact a chosen HTTP endpoint.
That server can use credentials from its configuration or environment and make
network requests. Only run a server you intend to execute. A single measurement
does not establish how every future session will perform.

## 4. Review a setup finding before changing anything

**For users with a finding in Doctor.**

1. Open **Doctor** and select a finding relevant to your setup.
2. Read the evidence and the proposed next step.
3. For a supported file edit, inspect the exact change before applying it. Gantry creates a local backup.
4. Use the app's Undo or **⌘Z** if you want to revert the supported edit.

Use this to make a deliberate configuration change. Not every finding has an
automatic fix. File removal uses the Trash, and process stopping has different
recovery limits; neither should be interpreted as a file edit that ⌘Z can restore.

## Something is missing?

Check [tool coverage](compatibility.md), the relevant folder permissions, and
whether your agent has produced local records. **⌘R** refreshes the workspace;
**⌘K** helps you jump to the relevant section or item.

If the supported records still do not appear, [report the issue](https://github.com/devin-lai/Gantry/issues/new?template=bug_report.yml)
with your Gantry build, macOS version, agent version, and a small reproducible
example. Review and redact any diagnostics before sharing them. Do not attach
full session transcripts or credentials.
