<div align="center">
  <img src="assets/gantry-icon.png" width="112" alt="Gantry's teal octopus mascot">
  <h1>Gantry</h1>
  <p><strong>See what your AI coding agents load, spend, and run.</strong></p>
  <p>A native macOS workspace for quota, context, MCP diagnostics, and fixes you can undo.</p>
  <p>
    <a href="https://github.com/devin-lai/Gantry/releases/download/v1.0.0-build79-preview/Gantry-1.0.0-build79-public-preview.dmg">Download Gantry for macOS</a> ·
    <a href="docs/getting-started.md">Get started</a> ·
    <a href="https://github.com/devin-lai/Gantry/issues/new/choose">Report a bug or suggest a feature</a>
  </p>
  <p>
    <img src="https://img.shields.io/badge/macOS-13%2B-242938?logo=apple&amp;logoColor=white" alt="macOS 13 or later">
    <img src="https://img.shields.io/badge/Apple_silicon_%26_Intel-supported-168577" alt="Apple silicon and Intel">
    <img src="https://img.shields.io/badge/personal_use-free-168577" alt="Free for personal use">
    <img src="https://img.shields.io/badge/source-proprietary-626B75" alt="Proprietary source">
  </p>
</div>

![Gantry Overview: quota runway, setup findings, live sessions, and context insights](assets/overview-dark.png)

*Screenshots use synthetic demo data. Numbers illustrate the interface; appearance and available measurements vary by build and agent.*

## Your agents have a lot going on. Get one clear view.

A quota window is running low. A skill never makes it into context. An MCP server takes too long to start. A hook slows every turn. Gantry brings the local evidence together so you can see what needs attention and decide what to change.

Use it alongside **Claude Code, Codex, Cursor, Gemini CLI, OpenCode, and Copilot CLI**. You can start with just one agent. [Coverage differs by tool.](docs/compatibility.md)

| What you want to know | What Gantry helps you inspect |
| --- | --- |
| **How much quota is left?** | Locally cached Claude Code and Codex quota windows, reset times, freshness, and pace, with a compact menu bar view and optional notifications. |
| **What loads before my first prompt?** | Instruction files, rules, skills, agent definitions, and MCP schemas, with token estimates and measured startup context where sessions record it. |
| **Why does this setup feel slow?** | MCP initialization and tool-list timings, plus API, tool, and hook time where agents record those measurements. |
| **What should I fix first?** | Doctor findings ranked by priority, with evidence and supported local changes you can preview before applying. |
| **What is running right now?** | Agent processes and MCP children, CPU and memory use, live session context where available, and orphaned servers. |
| **Where did the tokens go?** | Project and session views with recorded usage, context timelines, and clearly labelled API-rate cost estimates. |

## Inspect. Preview. Undo.

Gantry's Doctor connects a finding to the evidence and a next step. Supported file edits show the exact change and create a backup before writing. Undo is available in the app and with **⌘Z**. Removing a file uses the Trash; stopping a process has its own recovery limits.

![Gantry Doctor: prioritized findings for skills, MCP servers, and hooks](assets/doctor-light.png)

Inventory brings skills, sub-agents, MCP servers, rules, commands, hooks, and plugins into one place. **⌘K** jumps to a project, session, skill, server, or section; **⌘R** refreshes the workspace.

## Local data. No Gantry account.

Gantry indexes records already on your Mac and keeps its index and backups locally. It has no Gantry account or analytics telemetry. Session data is not uploaded to a Gantry service.

MCP benchmarking is an active operation: it can launch your configured servers or contact an HTTP server you choose. Those servers can make their own network requests. The welcome screen asks about automatic stdio benchmarking; you can change the choice in Settings. [Read the privacy details.](PRIVACY.md)

## Download and first launch

**Requires macOS 13 Ventura or later, on Apple silicon or Intel.**

[Download the build 79 public preview](https://github.com/devin-lai/Gantry/releases/download/v1.0.0-build79-preview/Gantry-1.0.0-build79-public-preview.dmg) · [Release notes and checksum](https://github.com/devin-lai/Gantry/releases/tag/v1.0.0-build79-preview). Watch **Releases** to hear when a newer build is available.

1. Download the DMG from this repository's Releases page.
2. Open it and drag **Gantry** into **Applications**.
3. Open Gantry and follow the welcome screen. It detects supported local agent folders.

The build 79 public preview is **ad-hoc signed and not notarized by Apple**. macOS may block its first launch. After verifying the release checksum and deciding to trust the download, use **System Settings → Privacy & Security → Open Anyway**. [Installation, checksum verification, and uninstall instructions.](docs/getting-started.md)

## Know what the numbers mean

- Quota readings come from local agent records. They can be stale and do not replace the provider's usage page.
- API-rate cost is an estimate from recorded usage and pricing, not your subscription bill.
- Context components include estimates; a timeline can leave unexplained usage unattributed.
- When a source is missing, unreadable, or incomplete, Gantry labels the limitation. Features depend on what each agent records.
- Gantry helps you inspect configuration; it cannot guarantee lower spending, faster models, or better answers.

[Supported tools and limits](docs/compatibility.md) · [Frequently asked questions](docs/faq.md) · [Build 79 artifact audit](docs/build79-audit.md)

## Help make Gantry more useful

Found a bug? [Send a report](https://github.com/devin-lai/Gantry/issues/new?template=bug_report.yml). Have a workflow Gantry could improve? [Describe it](https://github.com/devin-lai/Gantry/issues/new?template=feature_request.yml). Please remove secrets, private paths, and confidential prompts from anything you share.

If Gantry helps you understand your setup, **star this repository** so other agent users can find it, and share the repository link with someone who could use it. Feedback and documentation improvements are welcome; the application source remains private.

## License

**Free for personal, non-commercial use only.** Gantry is proprietary software. This public repository hosts documentation, feedback, and binary releases; the application's source code is closed-source. Commercial, employer, and client use requires separate permission. See [LICENSE](LICENSE).

Gantry is an independent application and is not affiliated with the makers of the supported coding tools.
