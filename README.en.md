[简体中文](./README.md) | [繁體中文](./README.zh-TW.md) | [English](./README.en.md) | [日本語](./README.ja.md)

<p align="center"><img src="./shiguang-icon.png" width="112" height="112" alt="Shiguang"></p>
<h1 align="center">Shiguang</h1>
<p align="center">Card offload · File copy · Project media import</p>
<p align="center"><a href="https://github.com/Sorasukiawa/shiguang/releases/download/v0.2.0/Shiguang_0.2.0_aarch64.dmg"><strong>Download v0.2.0 · Apple Silicon Mac</strong></a><br>Free beta · 简体中文 / 繁體中文 / English / 日本語 · Light and dark themes</p>
<p align="center"><a href="https://getshiguang.pages.dev/">Website & interactive demo</a> · <a href="https://getshiguang.pages.dev/guides/">User guides</a> · <a href="./RELEASE_NOTES_v0.2.0.md">Release notes</a> · <a href="https://github.com/Sorasukiawa/shiguang/issues">Report an issue</a></p>

<p align="center"><img src="https://raw.githubusercontent.com/Sorasukiawa/shiguang/328fb3cb25479f3d4c1dd1c168fa28d315e95f55/shiguang-overview.svg" width="100%" alt="Shiguang: Copy. Organize. Verify."></p>

## Choose a workflow for your media

| What you want to do | How Shiguang helps |
| --- | --- |
| **Copy files and folders** · New in v0.2.0 | Select or drop files from Finder and copy to one or more destinations, preserving hierarchy, hidden files and empty directories |
| **Bring existing media into a project** · New in v0.2.0 | Drop onto a project card or project details; map photos, video, audio and project files to their folders |
| **Offload a camera card** | Identify media and organize by shoot date, camera and preset; read once while writing to a working drive and a backup drive |
| **Organize and archive** | Reuse folder templates, archive with full verification and keep project records without automatically deleting local media |

### From dropping files to checking results

1. **Choose a source:** Add files, folders or camera-card media.
2. **Review the plan:** Check file count, size, destination space, folder mapping and verification.
3. **Copy and check:** Follow persistent task progress, completed results and failed files.
4. **Fill the gaps:** Recheck destinations and retry only unfinished files or copies.

## A more complete workflow in v0.2.0

- **Check before writing:** Catch overlapping paths, nested destinations and insufficient combined space on a shared volume; confirm destination identity.
- **Never overwrite existing files:** Report name conflicts and keep partial output distinct from completed copies.
- **Recover each destination independently:** One drive can finish while another disconnects. Reconnect to fill missing copies.
- **Recover after restarting the app:** Task receipts preserve completed results across forced exits, full disks and interrupted record commits.
- **Protect APFS destinations:** Stop writing if a volume detaches or is replaced, avoiding the local directory behind its former mount point.
- **Keep the original offload tools:** Dual backups, three verification modes, MHL and readable reports, duplicate prevention, project templates and archiving.

[v0.2.0](https://github.com/Sorasukiawa/shiguang/releases/tag/v0.2.0) · [All releases](https://github.com/Sorasukiawa/shiguang/releases) · [Complete v0.2.0 release notes](./RELEASE_NOTES_v0.2.0.md)

## Before you download

Available as a **free beta for Apple Silicon macOS only**. Intel Mac and Windows builds are not yet available for public download. Check your chip under ** → About This Mac**. Public v0.1.19 users can check for updates in Settings; updates do not install during offload, file copy or archiving.

> [!IMPORTANT]
> This build is ad-hoc signed, without Apple Developer ID signing or Apple notarization. Keep original cards and another reliable backup until copies are checked. Do not use the beta as the only safeguard for important media.

Validated scenarios include synthetic files, isolated databases, native Finder drag and drop, and forced disconnection of APFS disk images. This does not establish compatibility with every physical USB device, NAS failure mode or third-party sync service.

## Understanding verification

- **No verification:** Relies only on whether the write operation reports an error. It is the fastest option and is not suitable for important media.
- **Quick verification:** Checks that every file exists, can be read, and has the expected byte size. This detects missing files and obvious truncation.
- **Full verification:** Rereads every byte from each destination, recalculates xxHash64, and compares it with the source hash captured during copying. Use this for important shoots and dual-destination backup workflows.

Here, xxHash64 detects whether copied content is identical; it is not authentication or a cryptographic signature. Even after verification passes, open and spot-check critical media and confirm that at least two copies are usable before formatting a camera card.

## First launch on macOS

The v0.2.0 beta is not signed with an Apple Developer ID and is not notarized by Apple. macOS may therefore block its first launch:

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
