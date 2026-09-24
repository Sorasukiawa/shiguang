# 拾光 Shiguang v0.1.14 · 缺失目录与删除流程修复

**历史版本 / Historical release** · 修复项目目录已缺失、文件处理失败或目录状态变化时的删除流程；无法确认磁盘与目录归属时会停止，而不是猜测删除。调整设置页更新信息布局。

**[下载本版本 DMG · Apple Silicon Mac](https://github.com/Sorasukiawa/shiguang/releases/download/v0.1.14/Shiguang_0.1.14_aarch64.dmg)** · [安装指南](https://getshiguang.pages.dev/guides/) · [全部版本](https://github.com/Sorasukiawa/shiguang/blob/main/VERSIONS.md)

<strong>历史版本提示：</strong>本页下载固定为此版本。若已安装的旧版没有更新通道，请结束任务、退出 App 后用目标版本 DMG 手动升级。

<details><summary>繁體中文 · 缺失資料夾與刪除流程修正</summary>

修正專案資料夾已缺失、檔案處理失敗或資料夾狀態變更時的刪除流程；無法確認磁碟及資料夾歸屬時會停止，不會猜測刪除。調整更新資訊版面。

僅提供 Apple Silicon macOS 免費測試版，採用 ad-hoc 簽署，尚無 Apple Developer ID 簽署或公證。DMG 供手動安裝；重要素材請保留原卡及另一份可靠備份。

</details>

<details><summary>English · Missing-folder deletion fixes</summary>

Fixes deletion when a project folder is missing, file handling fails, or folder state changes. Deletion stops when disk or folder identity cannot be confirmed. Also adjusts the update panel layout.

Apple Silicon macOS free beta only. This build is ad-hoc signed, without Apple Developer ID signing or notarization. Use the DMG for manual installation, and keep the original card plus another reliable backup for important media.

</details>

<details><summary>日本語 · 不明なフォルダーと削除の修正</summary>

プロジェクトフォルダーが見つからない、ファイル処理が失敗する、状態が途中で変わる場合の削除処理を修正。ディスクやフォルダーの識別を確認できなければ削除を停止します。更新画面の配置も調整しました。

Apple Silicon macOS 向けの無料ベータ版のみです。ad-hoc 署名で、Apple Developer ID 署名と公証はありません。手動インストールには DMG を使い、大切な素材は元カードと別の信頼できるバックアップを残してください。

</details>

<details><summary>详细发布记录（简体中文）</summary>

拾光是一款面向摄影师、摄像师、个人创作者与摄影摄像团队的本地拷卡、双备份、校验与项目归档工具。

v0.1.14 是一次项目删除流程的数据安全与更新体验修复，解决项目目录已经缺失时“删除项目和文件”无法完成、删除期间目录状态变化可能导致判断不一致，以及设置页更新信息排版错位的问题。

> [!IMPORTANT]
> 拾光目前仍是免费内测版。处理重要素材时，请保留原始存储卡，并确认至少还有一份可靠备份后再格式化卡片。

## 本次修复

### 项目目录已经缺失时可以安全完成删除

- 修复项目文件夹已被移动或删除后，勾选“同时处理项目文件夹和素材”会一直停在删除确认框的问题。
- 只有确认原项目盘在线且目录确实属于该项目时，拾光才会清理这类卡住的项目记录。
- 原项目盘未连接、磁盘身份变化、出现无法确认归属的同名目录或目录状态异常时，操作会立即停止，不会猜测性删除。
- 项目根目录已经缺失时，只保留继续识别该项目所需的最少记录，不会保存素材内容或额外生成素材清单。

### 删除失败后的状态更加清楚

- “移入拾光回收站”和“处理项目文件夹”仍是两个独立阶段。
- 如果第一阶段已经成功、第二阶段失败，确认框现在会切换到真实的“彻底删除”状态并显示对应错误，不再看起来像按钮没有反应。
- 用户勾选的“同时处理项目文件夹和素材”会继续保留。
- 再次尝试时只重试失败的文件处理阶段，不会重复执行移入回收站。

### 目录状态变化时会重新确认

- 如果项目目录在删除过程中重新出现，拾光会重新检查最新状态，不会继续沿用过期判断。
- 只有确认属于当前项目的目录才会移入 macOS 系统废纸篓。
- 无法确认目录归属时会停止操作并保留记录。

### 设置页更新信息排版更清楚

- “当前版本”与更新状态、安装按钮改为稳定的顶部对齐，不再被多行更新说明挤到中间。
- 版本说明改为下方独立的全宽信息行，避免右对齐导致的窄列换行与末尾孤字。
- 更新状态可以在空间不足时安全截断，安装按钮仍保持完整、可操作。

## 删除安全边界

- 默认移入拾光回收站不会移动或删除原项目文件夹和素材。
- 选择处理项目文件夹时，只处理该项目的根目录，并移入系统废纸篓，不会直接抹除。
- 归档盘和第二备份盘不会随项目删除而被处理。
- 如果项目盘或目录状态无法确认，拾光会保留项目记录和现场，优先避免误删。

## 升级方式

如果已经安装 v0.1.13：

1. 打开拾光的“设置”页面。
2. 选择“检查更新”。
3. 确认下载并安装 v0.1.14。

为保护正在处理的素材，拷卡或项目归档进行中不会执行安装和重启，请等待任务结束后再更新。

如果 App 内暂时没有显示更新，也可以退出拾光，从本 Release 下载 DMG，将新版“拾光”拖入“Applications / 应用程序”并替换旧版。已有项目记录和设置会继续保留。

## 下载与首次打开

当前公开安装包仅适用于搭载 Apple M 系列芯片的 Mac。Intel Mac 与 Windows 版尚未提供公开下载。

本内测包使用 ad-hoc 签名，尚未使用 Apple Developer ID 签名，也未经过 Apple 公证。macOS 可能在首次启动时拦截：

1. 只从本仓库的 Releases 下载 DMG。
2. 将“拾光”拖入“Applications / 应用程序”。
3. 正常打开一次；如果系统拦截，请关闭提示。
4. 前往“系统设置 → 隐私与安全性”，确认应用为“拾光”后选择“仍要打开”。

请勿关闭 Gatekeeper，也不要为来源不明的安装包绕过系统保护。

## 反馈

如果遇到问题，欢迎通过本仓库的 Issues 反馈。建议附上拾光版本、macOS 版本、Mac 芯片型号、复现步骤和必要截图；提交前请遮挡客户名称、项目名称和本地路径等敏感信息。

本公开仓库用于提供官方安装包、版本说明和问题反馈，不包含拾光源代码。

</details>

---

<strong>安装与文件：</strong>本版仅提供 Apple Silicon macOS。DMG 用于手动安装；同页的 `Shiguang_aarch64.app.tar.gz`、`.sig` 和 `latest.json` 供应用内更新使用。本版为 ad-hoc 签名，未获 Apple Developer ID 签名或 Apple 公证。GitHub 自动生成的 Source code 归档只是公开资料，不含拾光 App 源码，也不是安装包。

重要素材请保留原始卡和另一份可靠备份，确认副本后再格式化。问题请提交至 [Issues](https://github.com/Sorasukiawa/shiguang/issues)，不要上传原始素材、客户资料或私密路径。
