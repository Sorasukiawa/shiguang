[简体中文](./README.md) | [繁體中文](./README.zh-TW.md) | [English](./README.en.md) | [日本語](./README.ja.md)

<p align="center"><img src="./shiguang-mark.svg" width="88" height="88" alt="Shiguang icon"></p>
<h1 align="center">拾光 Shiguang</h1>
<p align="center"><a href="https://getshiguang.pages.dev/">Website</a> · <a href="https://getshiguang.pages.dev/guides/">User guides</a> · <a href="https://github.com/Sorasukiawa/shiguang/issues">Report an issue</a></p>
<p align="center">Make every media offload verifiable and traceable.</p>
<p align="center">A local-first tool for <strong>photographers, filmmakers, independent creators, and production teams</strong>, covering media offload, dual-destination backup, verification, and project archive workflows.</p>

> [!IMPORTANT]
> Shiguang is currently a **free beta**. Keep the original memory card and confirm at least one other known-good backup before formatting it. Do not use this beta as the only safeguard for important media.

## Download

### v0.1.18 · Apple Silicon Mac

The current public beta is available only for an Apple Silicon Mac with an Apple M-series chip. Intel Mac and Windows builds are not yet available for public download.

- [Download Shiguang v0.1.18 DMG](https://github.com/Sorasukiawa/shiguang/releases/tag/v0.1.18)
- [View all releases](https://github.com/Sorasukiawa/shiguang/releases)

If you are unsure which chip your Mac uses, open ** → About This Mac** and check the Chip field.

## What changed in v0.1.18

- Project lists and details show loading, failure, and retry states. Slow disk queries no longer block task-progress initialization, and failed refreshes preserve the existing list.
- Preset read failures preserve the original file. In-memory presets change only after saving succeeds, and unchanged presets are no longer rewritten on every launch.
- NAS archives gain persistent task records, re-verification of the original plan, and a new-task recovery entry after failure. Expandable history identifies each attempt's folder.
- MHL manifests now handle required fields and special characters correctly. Interrupted-job checks, resumed-copy feedback, and dual-destination result descriptions are clearer.
- Stalled update downloads time out. Invalidated packages can be checked again, and stale notices are removed. Installation and restart remain blocked during offload or archiving.
- Project details fit smaller windows better, with improved layout transitions and page language declarations for all four languages.

The public v0.1.16 → v0.1.18 upgrade passed download, installation, and automatic restart checks from Settings on this Mac. The public v0.1.17 build has no update channel and cannot upgrade from Settings: finish running jobs, quit Shiguang, and replace it using this Release’s DMG. v0.1.18 includes the update channel. Project records, settings, and custom presets were preserved in this upgrade; the built-in video preset gained its photo-media route. First installation on a clean Mac remains unverified.

## What Shiguang does

| Capability | Description |
| --- | --- |
| Card detection | Recognizes common photo, video, and audio media, then organizes files by shoot date, camera position, and reusable project preset |
| Safe media offload | Selects a safe write protocol for each destination; existing files are never overwritten, and interrupted remnants are preserved and reported |
| Dual-destination backup | Reads the camera card once while writing to a working drive and a second backup drive |
| Verification | Quick verification checks readability and size; full verification rereads destination files and compares xxHash64 values with the source media |
| Reports and duplicate prevention | Produces MHL and human-readable reports, remembers completed cards, and copies only new or missing files during a follow-up offload |
| Projects and presets | Creates projects from reusable folder templates for originals, selects, deliverables, audio, and production files |
| Project archive | Runs full verification during archival, keeps the project record and chain of custody, and does not automatically delete local media |

## Understanding verification

- **No verification:** Relies only on whether the write operation reports an error. It is the fastest option and is not suitable for important media.
- **Quick verification:** Checks that every file exists, can be read, and has the expected byte size. This detects missing files and obvious truncation.
- **Full verification:** Rereads every byte from each destination, recalculates xxHash64, and compares it with the source hash captured during copying. Use this for important shoots and dual-destination backup workflows.

Here, xxHash64 detects whether copied content is identical; it is not authentication or a cryptographic signature. Even after verification passes, open and spot-check critical media and confirm that at least two copies are usable before formatting a camera card.

## First launch on macOS

The v0.1.18 beta is not signed with an Apple Developer ID and is not notarized by Apple. macOS may therefore block its first launch:

1. Download the DMG only from the [Sorasukiawa/shiguang](https://github.com/Sorasukiawa/shiguang) Releases page.
2. Open the DMG and drag Shiguang into **Applications**.
3. Try opening Shiguang normally once. If macOS blocks it, close the warning.
4. Open **System Settings → Privacy & Security**, confirm that the blocked app is Shiguang, and choose **Open Anyway**.

You do not need to disable Gatekeeper. Never bypass system protection for a package from an unknown source.

## Drive compatibility

- **APFS is recommended for working drives, second backup drives, and archive destinations.**
- **ExFAT can also be a destination, but it must first pass Shiguang's safety capability probe.** Shiguang verifies volume identity, exclusive creation, and durable volume writes. If safety cannot be established, it refuses the copy before writing media instead of falling back to an overwrite-prone path.
- **An ExFAT camera card can be used directly as a read-only source** and is not subject to the destination-drive probe.

APFS and ExFAT use different safe-write strategies, but neither path overwrites an existing file. Shiguang does not ask you to format a source card or an existing working drive; do not change the format of the only medium holding your media merely to test the beta.

## Privacy and network access

- Media scanning, copying, verification, and project records are processed locally by default.
- Shiguang does not upload your photos or videos to a Shiguang server.
- If you choose a NAS or a third-party sync folder as a destination, subsequent network transfer or cloud synchronization is handled by that system or provider.
- When automatic update checks are enabled, the app contacts the official update source. It only notifies you of an update and does not install one during an offload or archive operation.

## Report a beta issue

Open an [Issue](https://github.com/Sorasukiawa/shiguang/issues) with your Shiguang version, macOS version, Mac chip, source and destination drive formats, reproducible steps, and the complete error text. Screenshots are helpful, but redact client names, project names, and local paths first.

Do not upload original media, client information, private paths, or other sensitive data to an Issue.

## About this repository

This is Shiguang's public repository for **official installers, user documentation, release notes, and user feedback**.

**This repository does not contain the Shiguang source code. It provides no open-source license and grants no right to modify or redistribute the source code.**
