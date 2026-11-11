<div align="center">
  <img src="assets/gantry-icon.png" width="96" alt="Gantry's teal octopus mascot">
  <h1>Gantry</h1>
  <p><strong>Pick up where your last agent left off.</strong></p>
  <p>Your local AI coding workspace for <strong>Claude Code, Codex, Cursor, and more</strong>.<br>Find past sessions, see what changed, and carry project decisions across Claude Code and Codex.</p>
  <p>
    <a href="https://github.com/devin-lai/Gantry/releases/download/v2.0.0/Gantry-2.0.0.dmg"><img src="https://img.shields.io/badge/Download_for_macOS-v2.0.0-168577?style=for-the-badge&amp;logo=apple&amp;logoColor=white" alt="Download Gantry 2.0.0 for macOS"></a>
  </p>
  <p><strong>Native macOS · Apple silicon &amp; Intel · macOS 14.5+<br>Completely free, including for commercial use · No Gantry account · No analytics telemetry</strong></p>
  <p>Ad-hoc signed; <strong>not notarized by Apple</strong>. <a href="docs/getting-started.md">First-launch instructions</a>.</p>
  <p><strong>English</strong> · <a href="README.zh-CN.md">简体中文</a></p>
  <p>
    <a href="#project-memory-in-200">What's new</a> ·
    <a href="#why-gantry">Why Gantry</a> ·
    <a href="docs/workflows.md">Try a workflow</a> ·
    <a href="docs/compatibility.md">Supported tools</a> ·
    <a href="https://github.com/devin-lai/Gantry/issues/new/choose">Feedback</a>
  </p>
</div>

## Project Memory in 2.0.0

Switch from Claude Code to Codex and bring the decisions that matter with you. With the opt-in **Project Memory** pilot, connected agents can recall saved decisions and lessons in enabled projects. You choose which notes can appear at session startup and can preview the exact text first.

- **Keep the right context in reach.** Save a decision, import selected Claude Code notes, or review what an agent saved. Keep useful notes available for recall and disable outdated ones.
- **See what the next session received.** Where local records provide the evidence, Gantry shows startup text and memory calls alongside the conversation. Optional work notes can provide a short excerpt of how the previous session ended.
- **Get back to the work itself.** Search a past conversation, inspect recorded file changes and Git status, and resume supported sessions in Terminal. Check cached quota and diagnose MCP configuration from the same Mac app.

**Try it in one project.** In **Projects → Review projects…**, choose **Turn on…**, then open **Connect agents…** in that project's **Project Memory** card to preview the setup. [Project Memory walkthrough](docs/getting-started.md#try-project-memory) · [2.0.0 release notes](https://github.com/devin-lai/Gantry/releases/tag/v2.0.0)

![Gantry's Project Memory review with the exact startup context preview](assets/project-memory-2.0.0.png)

*Project Memory with synthetic examples. Startup context requires your approval.*

## Why Gantry

Your coding tools already keep useful evidence on your Mac. Gantry brings the scattered conversations, instructions, skills, hooks, and MCP configuration into one place.

| Your question | What Gantry brings into view |
| --- | --- |
| **“Where did I leave off?”** | Searchable conversations, recorded endings, changed files, current Git state, and copyable handoff notes. |
| **“Which decisions should carry forward?”** | Opt-in Project Memory with reviewable startup notes and on-demand recall for Claude Code and Codex. |
| **“How much quota is left?”** | Cached Claude Code and Codex quota windows, reset times, freshness, and pace, including a menu bar view. |
| **“What loads before my first prompt?”** | Instructions, rules, skills, agent definitions, and MCP schemas, with estimates and recorded context where available. |
| **“Why is this MCP server failing?”** | Configuration, executable, working-directory, environment, initialization, and tool-list outcomes from Gantry's checks. |
| **“What should I change?”** | Doctor findings linked to evidence, previews for supported file edits, local backups, and Undo. |

Use Gantry alongside **Claude Code · Codex · Cursor · Antigravity · OpenCode · Copilot CLI**. Start with one tool; keep your existing workflow.

**Coverage varies.** Quota is available for Claude Code and Codex. Cursor supports desktop conversation history, search, and configuration inventory; its usage, cost, and quota are unavailable. A configuration marked available is not proof that an agent loaded it. [See coverage and limits.](docs/compatibility.md)

<details>
  <summary><strong>See the Gantry workspace</strong></summary>

![Gantry Overview with local quotas, sessions, and setup findings](assets/overview-1.3.2-light.png)

*Overview in 1.3.2 with synthetic demo data.*

</details>

## Try it with a recent session

1. [Download and install Gantry](docs/getting-started.md). Read the welcome screen and choose your MCP benchmarking preference.
2. Open **Sessions** and select a recent conversation. Type to filter titles and projects; press **Return** to search conversation content.
3. Review the recorded ending and changed files. Where offered, use **Load session details**, **Copy handoff note**, or **Copy resume command**.

For configuration work, start with **Agents** and choose the tool and project you care about. For quota, start with **Overview**.

**⌘K** jumps to an item · **⌘F** finds search in Sessions · **⌘R** refreshes · **⌘Z** undoes a supported file edit.

[Explore six practical workflows →](docs/workflows.md)

<details>
  <summary><strong>See Doctor in action</strong> — inspect the evidence before changing your setup</summary>

![Gantry Doctor: prioritized configuration findings for skills, MCP servers, and hooks](assets/doctor-1.3.0-light.png)

*Synthetic demo data. Available findings depend on your setup. File removal uses the Trash; stopping a process cannot be undone with file Undo.*

</details>

## Local records. Your choice of action.

Gantry keeps its index and edit backups on your Mac. There is no Gantry account, no analytics telemetry, and no upload of session history to a Gantry service. Read-only Git checks show the current state of recorded changed files; they do not commit or modify your repository.

MCP checks are active operations: they can launch configured servers or contact chosen HTTP endpoints. Those servers can use their own credentials and make network requests. You choose whether automatic stdio benchmarking is enabled. Handoff notes go to your clipboard when you copy them; review them before sharing.

Project Memory is stored locally. Connected agents may send memory context they receive to their model providers. [Privacy details](PRIVACY.md)

## Download and first launch

[**Download Gantry-2.0.0.dmg**](https://github.com/devin-lai/Gantry/releases/download/v2.0.0/Gantry-2.0.0.dmg) · [Release notes and SHA-256](https://github.com/devin-lai/Gantry/releases/tag/v2.0.0)

Requires **macOS 14.5 Sonoma or later**, on Apple silicon or Intel. Open the DMG and drag **Gantry** into **Applications**.

This release is **ad-hoc signed and not notarized by Apple**. After checking the checksum and deciding to trust the download, follow the [first-launch instructions](docs/getting-started.md) if macOS blocks it. A checksum identifies the file; it does not authenticate its publisher.

Use **Help → Check for Updates** when you choose, opt into weekly checks in Settings, or select **Watch → Custom → Releases** on this repository. Updates are installed manually.

## Know what the numbers mean

Quota readings are cached and may be stale. Costs are API-rate estimates, not subscription bills. Context components may be estimated or unattributed. Missing or unreadable records limit what Gantry can show. Changed-file lists cover recorded edit tools; they do not capture every shell-command side effect or establish who owns a change.

[Supported tools and limits](docs/compatibility.md) · [FAQ](docs/faq.md)

## Help shape Gantry

[Ask a question](https://github.com/devin-lai/Gantry/discussions/categories/q-a) or
[share an idea](https://github.com/devin-lai/Gantry/discussions/categories/ideas).
The maintainer aims to answer questions and review ideas weekly, on a best-effort
basis; there is no guaranteed response time. Use [Feedback](https://github.com/devin-lai/Gantry/issues/new/choose)
to choose between discussions and issue forms.

[Report a bug](https://github.com/devin-lai/Gantry/issues/new?template=bug_report.yml), [suggest a workflow](https://github.com/devin-lai/Gantry/issues/new?template=feature_request.yml), or improve the documentation and translations. Remove credentials, private paths, and confidential prompts from public reports.

If Gantry helps you get back to work, **star this repository** so others can find it, and [share the official link](docs/share.md) with another coding-agent user.

[Contributing](CONTRIBUTING.md) · [Report a security issue privately](SECURITY.md)

## License

**Completely free, including for commercial use.** Use Gantry for personal projects, at work, or with clients without charge or separate permission. See [LICENSE](LICENSE).

This public repository contains downloads, documentation, and release assets. The Gantry application source remains closed-source.

Gantry is independent and is not affiliated with the makers of the supported coding tools.
