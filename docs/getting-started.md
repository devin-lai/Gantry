# Get started with Gantry

Requires **macOS 14.5 Sonoma or later**, on Apple silicon or Intel. You do not
need a Gantry account or an API key to inspect local records. At least one
supported coding agent with local records makes the app useful.

## Install

1. Get `Gantry-1.3.2.dmg` and `SHA256SUMS.txt` from the [official 1.3.2 release](https://github.com/devin-lai/Gantry/releases/tag/v1.3.2).
2. Compare the DMG's checksum with the value in the release notes or checksum file:

   ```sh
   shasum -a 256 ~/Downloads/Gantry-1.3.2.dmg
   ```

3. Open the disk image and drag Gantry into Applications.
4. Eject the disk image and open Gantry from Applications.

Gantry 1.3.2 has an ad-hoc signature and is not notarized
by Apple. A checksum identifies the downloaded bytes; it does not establish
Apple's approval or the publisher's identity. If macOS blocks the app, verify
the download and decide whether you trust it, then use **System Settings →
Privacy & Security → Open Anyway** after the attempted launch. Follow
[Apple's first-launch guidance](https://support.apple.com/en-us/102445).

## Your first minute

- Read the welcome screen and choose whether Gantry may benchmark stdio MCP servers automatically. You can keep it off and benchmark later.
- Allow access to relevant folders if you want Gantry to inspect those projects.
- Start with **Overview** for quota, context, and findings, then **Doctor** for the evidence and next steps.
- Open **Inventory** for skills and MCP servers, **Sessions** for recorded usage, or **Live Runtime** for running processes.
- In **Sessions**, type to filter titles and projects; press **Return** to search conversation contents. Open a result to read the passage and use **Copy resume command** where supported.
- Review **Changed files** and current Git status, or use **Copy handoff note** to prepare for another session. Check copied notes for private content before sharing.
- For older Codex conversations, **Load session details** can recover recorded endings, edits, and commands, with progress and cancellation.
- Open **Agents** and select a tool and working directory to inspect capabilities for that context.
- Use **⌘K** to jump, **⌘R** to refresh, and **⌘Z** to undo the last supported file change.

Missing records or unsupported measurements are expected for some tools. Check
[coverage](compatibility.md) before interpreting an empty view as a problem.
For a concrete place to start, [choose one of six workflows](workflows.md).

## Updates

Gantry 1.3.2 checks for updates when you choose **Help → Check for Updates**,
or weekly if you explicitly opt in. It opens a release download in your browser;
it never downloads or installs updates automatically. You can also watch this
repository's **Releases** notifications. Ad-hoc builds may ask for protected-folder
access again after an update.

Before upgrading, check that your Mac runs macOS 14.5 or later. Quit Gantry,
open the 1.3.2 DMG, and replace Gantry in Applications. Keep Gantry's Application
Support folder if you want to retain its index and edit backups.
[Read what's new in 1.3.2.](releases/1.3.2.md)

## Report a problem

Use **Help → Diagnostic Report** to generate a local report. Review and redact
it before pasting anything into a [bug report](https://github.com/devin-lai/Gantry/issues/new?template=bug_report.yml).
Never share credentials, full transcripts, private prompts, or unredacted paths.

## Uninstall

Quit Gantry and move the app from Applications to the Trash. If you also remove
`~/Library/Application Support/Gantry`, you remove its index and edit backups;
keep those backups if you may need to restore a change. Its preferences are at
`~/Library/Preferences/github.devin-lai.gantry.plist`. Removing the app does not undo
changes you previously chose to apply to agent configuration.
