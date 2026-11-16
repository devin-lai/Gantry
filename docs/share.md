# Share Gantry with another agent user

![Gantry 2.1.0 with synthetic demo data](../assets/overview-light-2.1.0.png)

[Repository](https://github.com/devin-lai/Gantry) · [Gantry 2.1.0](https://github.com/devin-lai/Gantry/releases/tag/v2.1.0) · [简体中文介绍](../README.zh-CN.md)

## A short description

> Switch agents. Keep the thread. Gantry is a native Mac workspace for Claude Code, Codex, Cursor, and more. Find past conversations, review changes, and continue in Claude Code or Codex with an editable handoff. Local-first and free for personal and commercial use. macOS 14.5+.

## A release introduction

> Claude Code finished the implementation. Want Codex to review it? Gantry 2.1.0 helps you find that session and launch the next one in the same project with a prompt you control. Continuation uses optional saved work notes and connected agents. A refreshed Overview, clearer Projects, cached quota, and MCP diagnostics keep the surrounding setup in view. Apple silicon and Intel. No Gantry account or analytics telemetry.

## 简短介绍

> 切换助手，接着做。Gantry 2.1.0 将 Claude Code、Codex、Cursor 等工具的本地会话放进原生 Mac 工作台。找回对话、查看改动，用可编辑的交接提示词启动下一次 Claude Code 或 Codex 会话。续接需要自愿开启的工作笔记、已连接的助手与目标 CLI。个人与商业用途均免费，macOS 14.5+。

Share the official repository or release link so readers get the current download, checksum, license, and first-launch instructions together. This release is ad-hoc signed and not notarized by Apple; link to the [installation guide](getting-started.md).

## Keep the claims accurate

- Continuation opens a new session and asks the receiving agent to retrieve a saved note. It needs enabled work notes, an available note, a connected receiving agent, and the target CLI.
- Project Memory remains an opt-in pilot. Startup context requires approval. Connected agents may send received context to their model providers.
- Tool coverage varies. Quota is supported for Claude Code and Codex; Cursor includes desktop history and search, with usage, cost, and quota unavailable.
- Quotas are cached readings and costs are API-rate estimates. They are not invoices or promises of savings. Recorded file changes do not capture every shell side effect.
- Gantry is free for personal and commercial use. The public repository hosts documentation and downloads; application source remains closed-source. See [LICENSE](../LICENSE) for branding and reuse terms.
- The screenshots use synthetic data and have nonessential metadata removed. Never share private session content, credentials, account identifiers, or unredacted diagnostics.
