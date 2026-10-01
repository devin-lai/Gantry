# Build 79 public-preview artifact audit

Audited on **October 1, 2026**. This note applies only to the exact artifact
identified below; it is not a certification of all future builds or all runtime
behavior.

| Item | Result |
| --- | --- |
| File | `Gantry-1.0.0-build79-public-preview.dmg` |
| Version | Gantry 1.0.0, build 79 |
| Size | 15,052,667 bytes |
| SHA-256 | `be048354167d135f18dfdc19b5dadfe7c29d3c24d95045f0c61e9ef6e5033243` |
| Architectures | Apple silicon (arm64) and Intel (x86_64) |
| Minimum macOS | 13.0 |
| App signature | Valid ad-hoc signature; no signing certificate or Apple team identifier |
| Debugger entitlement | Disabled |
| Notarization | Not notarized by Apple |
| Update feed | No address configured |

## Scope and findings

The mounted bundle, disk-image filesystem, uncompressed image bytes, binary
strings, property lists, signature, entitlements, resources, and extended
attributes were inspected. Pattern scans and Gitleaks found no credentials or
personal build paths in this candidate. Apparent token substrings in compiled
symbol names and random compressed-image bytes were reviewed as false positives.

The image contains the app, an Applications shortcut, installation notes, the
personal-use license, and privacy notes. No source files, dSYM bundles,
provisioning profiles, private keys, account databases, personal session
transcripts, or developer configuration files are included.

Private debug symbols and local symbol-table entries were stripped from a
separate distribution copy, then the app was re-signed with debugger access
disabled. All **74 file-backed Mach-O sections** across both architectures match
the original executable's section bytes. The stripped app launched successfully
in an isolated empty-data smoke check. That check does not establish full feature
coverage, Intel runtime behavior, or performance on every supported Mac.

Automated scans cannot prove the absence of every possible secret. The checksum
identifies this audited file; it does not authenticate the publisher or represent
Apple notarization. See [installation guidance](getting-started.md).
