# 拾光 Shiguang v0.1.11 · 免费内测与应用内更新

**历史版本 / Historical release** · 首次免费内测：相机卡识别、双目标拷贝、三档校验、MHL 与报告、项目预设和归档流程；修复中文输入法确认候选时误创建项目。

**[下载本版本 DMG · Apple Silicon Mac](https://github.com/Sorasukiawa/shiguang/releases/download/v0.1.11/Shiguang_0.1.11_aarch64.dmg)** · [安装指南](https://getshiguang.pages.dev/guides/) · [全部版本](https://github.com/Sorasukiawa/shiguang/blob/main/VERSIONS.md)

**历史版本提示：**本页下载固定为此版本。若已安装的旧版没有更新通道，请结束任务、退出 App 后用目标版本 DMG 手动升级。

<details><summary>繁體中文 · 免費測試與 App 內更新</summary>

首個免費測試版：記憶卡辨識、雙目的地轉存、三種驗證方式、MHL 與報告、專案預設和封存流程；修正中文輸入法確認候選字時誤建專案。

僅提供 Apple Silicon macOS 免費測試版，採用 ad-hoc 簽署，尚無 Apple Developer ID 簽署或公證。DMG 供手動安裝；重要素材請保留原卡及另一份可靠備份。

</details>

<details><summary>English · Free beta & in-app updates</summary>

The first free beta brings camera-card ingest, two-destination copying, three verification modes, MHL and reports, project presets, and archiving. It fixes accidental project creation when confirming a Chinese IME candidate.

Apple Silicon macOS free beta only. This build is ad-hoc signed, without Apple Developer ID signing or notarization. Use the DMG for manual installation, and keep the original card plus another reliable backup for important media.

</details>

<details><summary>日本語 · 無料ベータとアプリ内更新</summary>

最初の無料ベータ版では、カード取り込み、二つの保存先、三段階の検証、MHL とレポート、プロジェクト設定とアーカイブに対応。中国語 IME の候補確定で誤ってプロジェクトが作成される問題を修正しました。

Apple Silicon macOS 向けの無料ベータ版のみです。ad-hoc 署名で、Apple Developer ID 署名と公証はありません。手動インストールには DMG を使い、大切な素材は元カードと別の信頼できるバックアップを残してください。

</details>

<details><summary>详细发布记录（简体中文）</summary>

拾光是面向**摄影师、摄像师及摄影摄像团队**的本地拷卡、双备份、校验与项目归档工具。v0.1.11 是对外试用的免费内测版，希望让个人创作者和团队都能以更清晰、更可追溯的方式管理每一次素材交接。

## 本次提供的安装包

- **macOS · Apple Silicon**（Apple M 系列芯片）DMG
- 当前尚未提供 Intel Mac 或 Windows 公开安装包

## 核心能力

- 自动识别存储卡中的照片、视频与音频素材，支持按项目日期和自选日期筛选。
- 按项目预设、机位和卷号自动路由，同时支持“全部文件”与“仅素材”范围。
- 从源卡只读一次，同时写入工作盘与第二备份盘。
- 提供不校验、快速校验和完整校验三档策略；完整校验会重读目标文件并与源素材的 xxHash64 比对。
- 生成 MHL 校验清单和 HTML / TXT 拷卡报告，保留每次拷卡的项目、卡片、机位和校验记录。
- 识别已拷过的卡片，重新拷卡时只补新增或缺失文件。
- 支持失败文件补拷、中断恢复、任务期间防休眠和校验通过后自动弹卡。
- 提供项目预设、项目状态、拷卡时间线与完整校验归档。
- 支持简体中文、繁体中文、English、日本語，以及浅色 / 深色主题。

## v0.1.11 重点改进

- 修正使用中文输入法输入英文项目名时，候选确认的回车键可能误创建项目的问题。
- 将设置中“拍摄日边界”统一为带 AM / PM 的 12 小时制，并收紧时间后的多余空间。
- 新增应用内检查更新；发现新版时只提醒，拷卡或归档进行中不会安装并重启。
- 完善更新下载进度与多语错误提示；当前公开内测只使用 GitHub 更新源。
- 在“设置 → 关于”新增 GitHub 内测反馈入口，只预填应用版本与系统类型，不读取项目、本地路径或素材。

## 安装前请知道

### 1. 尚未做 Developer ID 签名与公证

这一内测包尚未使用 Apple Developer ID 签名，也未经 Apple 公证。请仅从 [Sorasukiawa/shiguang](https://github.com/Sorasukiawa/shiguang) 的 Releases 下载。把应用拖入“Applications / 应用程序”后，如 macOS 拦截首次启动，请前往 **系统设置 → 隐私与安全性**，核对应用名称后选择“仍要打开”。

无需关闭 Gatekeeper，也不建议通过命令行全局降低系统安全级别。

### 2. APFS 推荐，ExFAT 目标盘会先检查

在 macOS 内测版中，**APFS 是工作盘、第二备份盘和归档目标盘的推荐格式**。ExFAT 也可以作为目标，但拾光会先检查能否安全写入；无法确认时会在复制素材前停止。ExFAT 相机卡可以直接作为只读素材来源，无需为了使用拾光而格式化已有硬盘。

### 3. 自动更新说明

v0.1.11 首次支持应用内检查更新。如果应用内没有显示新版或更新失败，仍可从 Releases 手动下载 DMG 替换安装。

## 内测安全建议

- 第一次试用请选择可复制的测试素材，或保留原卡与已知可靠的旧备份流程。
- 拷卡结束后先检查报告，人工打开抽查关键照片或视频，并确认至少两份副本可用。
- 在所有检查完成前，不要格式化或复用原始相机卡。
- 如遇异常，请先停止后续操作并保留源卡，再提交反馈。

## 反馈

欢迎在 [GitHub Issues](https://github.com/Sorasukiawa/shiguang/issues) 提交 Bug 或交互建议。请附上拾光版本、macOS 版本、Mac 芯片型号、盘符格式和重现步骤；发布截图前请遮挡客户名称、项目名称与本地路径，不要上传原始素材或客户资料。

---

本仓库仅发布拾光的官方安装包、说明与反馈，不包含源代码，也不构成开源授权。

</details>

---

**安装与文件：**本版仅提供 Apple Silicon macOS。DMG 用于手动安装；同页的 `Shiguang_aarch64.app.tar.gz`、`.sig` 和 `latest.json` 供应用内更新使用。本版为 ad-hoc 签名，未获 Apple Developer ID 签名或 Apple 公证。GitHub 自动生成的 Source code 归档只是公开资料，不含拾光 App 源码，也不是安装包。

重要素材请保留原始卡和另一份可靠备份，确认副本后再格式化。问题请提交至 [Issues](https://github.com/Sorasukiawa/shiguang/issues)，不要上传原始素材、客户资料或私密路径。
