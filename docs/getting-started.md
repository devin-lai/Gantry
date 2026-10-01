# Get started with Gantry

Requires **macOS 13 Ventura or later**, on Apple silicon or Intel. You do not
need a Gantry account or an API key to inspect local records. At least one
supported coding agent with local records makes the app useful.

## Install

1. Get the DMG and `SHA256SUMS.txt` from the [official Releases page](https://github.com/devin-lai/Gantry/releases) for the published preview.
2. Compare the DMG's checksum with the value in the release notes or checksum file:

   ```sh
   shasum -a 256 ~/Downloads/Gantry-1.0.0-build79-public-preview.dmg
   ```

3. Open the disk image and drag Gantry into Applications.
4. Eject the disk image and open Gantry from Applications.

Build 79's public preview has an ad-hoc signature and is not notarized
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
- Use **⌘K** to jump, **⌘R** to refresh, and **⌘Z** to undo the last supported file change.

Missing records or unsupported measurements are expected for some tools. Check
[coverage](compatibility.md) before interpreting an empty view as a problem.

## Updates

Build 79 does not check a remote update feed. Watch the repository's **Releases**
notifications and replace the app manually when a newer published build is
available. Ad-hoc builds may ask for protected-folder access again after an
update.

## Report a problem

Use **Help → Diagnostic Report** to generate a local report. Review and redact
it before pasting anything into a [bug report](https://github.com/devin-lai/Gantry/issues/new?template=bug_report.yml).
Never share credentials, full transcripts, private prompts, or unredacted paths.

## Uninstall

Quit Gantry and move the app from Applications to the Trash. If you also remove
`~/Library/Application Support/Gantry`, you remove its index and edit backups;
keep those backups if you may need to restore a change. Its preferences are at
`~/Library/Preferences/ai.branovo.gantry.plist`. Removing the app does not undo
changes you previously chose to apply to agent configuration.
