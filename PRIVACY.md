# Privacy and local access

Gantry reads supported coding-agent records on your Mac to show inventory,
usage, configuration findings, and runtime activity. It has no Gantry account
and no analytics telemetry. It does not upload session history to a Gantry
service.

## Files it reads and stores

Depending on which tools you use, Gantry reads local folders such as `~/.claude`,
`~/.codex`, `~/.cursor`, `~/.gemini`, `~/.config/opencode`, `~/.copilot`, and
`~/.agents`, along with agent-referenced projects and configuration files.
These records can include prompts, local paths, usage counters, instructions,
and MCP configuration. Treat them as private.

Gantry keeps its index and backups in `~/Library/Application Support/Gantry`.
Preferences are stored in `~/Library/Preferences/ai.branovo.gantry.plist`.
macOS may ask for access to Desktop, Documents, or Downloads when recorded
projects are located there. Some measurements may be incomplete if access is
denied.

## Changes and active operations

Supported configuration edits are previewed and backed up before writing. Files
removed through cleanup go to the Trash. A stopped process cannot be restored
with file Undo.

Gantry can ask an installed agent CLI for its version and inspect running
processes. MCP benchmarking can launch configured stdio servers and, on demand,
contact configured HTTP servers. Servers may use their configuration,
environment variables, or credentials and may make their own network requests.
Choose your benchmarking preference on the welcome screen or in Settings.

## Updates and reports

Build 79 has no built-in update-feed address, so its Check for Updates action
makes no update request. Download future builds from the official Releases page.
Opening provider help or usage links opens that provider's website in a browser.

Diagnostic reports are generated locally. Gantry does not submit them for you.
Read and redact a report before sharing: shortened home paths can still contain
private project names or error details. Screenshots can reveal private session
titles, paths, account labels, and usage figures.

GitHub, linked websites, and any MCP services you run have their own privacy
policies. The screenshots in this repository use synthetic demo data and have
nonessential metadata removed.
