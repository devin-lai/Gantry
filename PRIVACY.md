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
Preferences are stored in `~/Library/Preferences/github.devin-lai.gantry.plist`.
macOS may ask for access to Desktop, Documents, or Downloads when recorded
projects are located there. Some measurements may be incomplete if access is
denied.

Recorded file edits add file paths and change metadata to the local index;
Gantry does not keep the patches or edited file contents as part of that
changed-file list. **Load session details** deliberately reads more of a
selected local Codex conversation and caches the resulting metadata.

## Project Memory pilot

Project Memory is opt-in per project. For Git repositories, it stores memories in local Git metadata and shares them across linked worktrees. Outside Git it uses a local `.memopier` folder. You choose which Claude Code notes to import, which agents to connect, and which memories to approve for session startup.

Connected Claude Code and Codex sessions can receive approved startup text or request saved memories. The connected agent may send that context to its model provider under its own settings and privacy policy. Optional work notes are off by default. When enabled, they retain recorded session endings, prompts, final reports, and changed-file metadata locally within size limits for later retrieval. Work notes can contain private session content. Gantry must be running to write them. Folder exclusions and the global work-note switch control collection.

**Continue in Claude Code/Codex** previews an editable prompt naming a saved work note, then copies that prompt or starts a new interactive terminal session when you choose. The receiving connected agent can retrieve the note through the pickup tool. Launch and pickup activity counts stay local; those measurements do not contain prompt or work-note text.

## Changes and active operations

Supported configuration edits are previewed and backed up before writing. Files
removed through cleanup go to the Trash. A stopped process cannot be restored
with file Undo.

Gantry can ask an installed agent CLI for its version and inspect running
processes. MCP benchmarking can launch configured stdio servers and, on demand,
contact configured HTTP servers. Servers may use their configuration,
environment variables, or credentials and may make their own network requests.
Choose your benchmarking preference on the welcome screen or in Settings.

Git checks use read-only status, tracked-file, and history queries in relevant
checkouts. They do not commit or modify repository contents, and can be turned
off in Settings. **Copy handoff note** places recorded session content on the
clipboard only when requested. That text can include private prompts, replies,
commands, and paths; review it before pasting into another app or service.

## Updates and reports

Gantry checks its update feed on `raw.githubusercontent.com` when you
request a check, or weekly only after you opt in. The request carries no Gantry
version, identifier, or cookie; GitHub can receive ordinary connection information,
including your IP address. Gantry does not automatically download or install updates.
Opening provider help or usage links opens that provider's website in a browser.

Diagnostic reports are generated locally. Gantry does not submit them for you.
Read and redact a report before sharing: shortened home paths can still contain
private project names or error details. Screenshots can reveal private session
titles, paths, account labels, and usage figures.

GitHub, linked websites, and any MCP services you run have their own privacy
policies. The screenshots in this repository use synthetic demo data and have
nonessential metadata removed.
