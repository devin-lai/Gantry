<div align="center">
  <img src="assets/gantry-icon.png" width="96" alt="Gantry's teal octopus mascot">
  <h1>Gantry</h1>
  <p><strong>Know your quota. Understand your context. Fix your setup.</strong></p>
  <p>A native macOS dashboard for <strong>Claude Code, Codex, and your other AI coding tools</strong>.</p>
  <p>
    <a href="https://github.com/devin-lai/Gantry/releases/download/v1.0.0-build79-preview/Gantry-1.0.0-build79-public-preview.dmg"><img src="https://img.shields.io/badge/Download_for_macOS-Public_preview-168577?style=for-the-badge&amp;logo=apple&amp;logoColor=white" alt="Download Gantry for macOS — build 79 public preview"></a>
  </p>
  <p><strong>macOS 13+ · Apple silicon &amp; Intel · Free for personal, non-commercial use</strong></p>
  <p>This preview is ad-hoc signed and <strong>not notarized by Apple</strong>. <a href="docs/getting-started.md">Read the first-launch instructions.</a></p>
  <p><strong>English</strong> · <a href="README.zh-CN.md">简体中文</a></p>
  <p>
    <a href="#why-gantry">Why Gantry</a> ·
    <a href="#choose-your-first-workflow">Try a workflow</a> ·
    <a href="docs/compatibility.md">Supported tools</a> ·
    <a href="https://github.com/devin-lai/Gantry/releases/tag/v1.0.0-build79-preview">Release notes</a> ·
    <a href="https://github.com/devin-lai/Gantry/issues/new/choose">Feedback</a>
  </p>
</div>

![Gantry Overview: quota runway, setup findings, live sessions, and context insights](assets/overview-dark.png)

*Screenshots use synthetic demo data. Numbers illustrate the interface; appearance and available measurements vary by build and agent.*

## Why Gantry

Your coding setup is spread across session logs, instruction files, skills, hooks, and MCP servers. Gantry brings that local evidence into one workspace so you can see what needs attention and decide what to change.

Use Gantry alongside **Claude Code · Codex · Cursor · Gemini CLI · OpenCode · Copilot CLI**. Start with one agent; no migration or Gantry account is needed. **Coverage differs:** quota is available for Claude Code and Codex; Cursor coverage is configuration inventory, without chat usage or quota in this build. [See the complete coverage table.](docs/compatibility.md)

| When this happens… | Open Gantry to… |
| --- | --- |
| **“I'm close to my limit.”** | See cached Claude Code and Codex quota windows, reset times, freshness, and pace. Keep a compact view in the menu bar. |
| **“What loads before I even type?”** | Inspect instructions, rules, skills, agent definitions, and MCP schemas, with token estimates and recorded startup context where available. |
| **“Something in my setup feels slow.”** | Inspect MCP startup and tool-list timings, plus recorded API, tool, and hook time. |
| **“Which configuration should I change?”** | Follow Doctor findings to the evidence, preview supported file edits, and keep a local backup for Undo. |

## Choose your first workflow

After [installing](docs/getting-started.md), pick the question that brought you here:

| Start here | What to try |
| --- | --- |
| **Check quota runway** | Open **Overview** and check the quota source's freshness before planning your next session. |
| **Understand startup context** | Open **Inventory** to inspect what your project and agent configuration contribute. |
| **Investigate a slow MCP server** | Inspect available timing evidence; choose an active benchmark only if you want to run the configured server. |
| **Review one setup finding** | Open **Doctor**, inspect the evidence, and preview a supported change before applying it. |

[Walk through these four workflows →](docs/workflows.md)

## Inspect. Preview. Undo.

Gantry's Doctor connects a finding to the evidence and a next step. Supported file edits show the exact change and create a backup before writing. Undo is available in the app and with **⌘Z**. Removing a file uses the Trash; stopping a process has its own recovery limits.

<details>
  <summary><strong>See Doctor in action</strong> — skills, MCP servers, and hooks</summary>

![Gantry Doctor: prioritized findings for skills, MCP servers, and hooks](assets/doctor-light.png)

*Synthetic demo data; available findings depend on your configuration and build.*

</details>

You can also explore **Projects** and **Sessions** for recorded usage and API-rate cost estimates, or **Live Runtime** for agent and MCP processes, CPU, and memory. **⌘K** jumps to a project, session, skill, server, or section; **⌘R** refreshes the workspace.

## Local data. No Gantry account.

Gantry indexes records already on your Mac and keeps its index and backups locally. It has no Gantry account or analytics telemetry. Session data is not uploaded to a Gantry service.

MCP benchmarking is an active operation: it can launch configured servers or contact an HTTP endpoint you choose. Those servers can use their configured credentials and make their own network requests. You choose whether automatic stdio benchmarking is enabled during welcome or in Settings. [Read the privacy details.](PRIVACY.md)

## Download and first launch

**Requires macOS 13 Ventura or later, on Apple silicon or Intel.**

[Download the build 79 public preview](https://github.com/devin-lai/Gantry/releases/download/v1.0.0-build79-preview/Gantry-1.0.0-build79-public-preview.dmg) · [Release notes and checksum](https://github.com/devin-lai/Gantry/releases/tag/v1.0.0-build79-preview). To hear about new builds, use **Watch → Custom → Releases** on this repository. Build 79 has no built-in update feed.

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

## Help another agent user find Gantry

Found a bug? [Send a report](https://github.com/devin-lai/Gantry/issues/new?template=bug_report.yml). Have a workflow Gantry could improve? [Describe it](https://github.com/devin-lai/Gantry/issues/new?template=feature_request.yml). Please remove secrets, private paths, and confidential prompts from anything you share.

If Gantry is useful to you, **star this repository** and share [the repository link](https://github.com/devin-lai/Gantry) with someone who uses a supported coding tool. [Short descriptions and sharing guidance](docs/share.md) make it easier to explain what it does. Documentation corrections and translations are welcome; the application source remains private. [How to contribute](CONTRIBUTING.md) · [Report a sensitive security issue privately](SECURITY.md).

## License

**Free for personal, non-commercial use only.** Gantry is proprietary software. This public repository hosts documentation, feedback, and binary releases; the application's source code is closed-source. Commercial, employer, and client use requires separate permission. See [LICENSE](LICENSE).

Gantry is an independent application and is not affiliated with the makers of the supported coding tools.
