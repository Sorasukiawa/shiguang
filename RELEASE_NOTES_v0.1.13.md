# 拾光 Shiguang v0.1.13 · 项目回收站与状态管理

**历史版本 / Historical release** · 新增项目回收站：普通删除只隐藏项目记录，不移动素材；彻底删除时可选择是否处理项目根目录。修复“仅标记完成”及路径提示稳定性。

**[下载本版本 DMG · Apple Silicon Mac](https://github.com/Sorasukiawa/shiguang/releases/download/v0.1.13/Shiguang_0.1.13_aarch64.dmg)** · [安装指南](https://getshiguang.pages.dev/guides/) · [全部版本](https://github.com/Sorasukiawa/shiguang/blob/main/VERSIONS.md)

<strong>历史版本提示：</strong>本页下载固定为此版本。若已安装的旧版没有更新通道，请结束任务、退出 App 后用目标版本 DMG 手动升级。

<details><summary>繁體中文 · 專案回收站與狀態管理</summary>

新增專案回收站：一般刪除只隱藏專案紀錄，不移動素材；徹底刪除時可選擇是否處理專案根資料夾。修正「僅標記完成」與路徑提示。

僅提供 Apple Silicon macOS 免費測試版，採用 ad-hoc 簽署，尚無 Apple Developer ID 簽署或公證。DMG 供手動安裝；重要素材請保留原卡及另一份可靠備份。

</details>

<details><summary>English · Project Trash & status</summary>

Adds Project Trash. Ordinary removal hides the project record without moving media; permanent deletion offers a separate choice for the project root folder. Also fixes mark-as-complete-only and path notices.

Apple Silicon macOS free beta only. This build is ad-hoc signed, without Apple Developer ID signing or notarization. Use the DMG for manual installation, and keep the original card plus another reliable backup for important media.

</details>

<details><summary>日本語 · プロジェクトのゴミ箱と状態</summary>

プロジェクトのゴミ箱を追加。通常の削除では記録だけを隠し、素材は移動しません。完全削除時にはプロジェクトのルートフォルダーを処理するか選べます。「完了としてマークのみ」とパス表示も修正しました。

Apple Silicon macOS 向けの無料ベータ版のみです。ad-hoc 署名で、Apple Developer ID 署名と公証はありません。手動インストールには DMG を使い、大切な素材は元カードと別の信頼できるバックアップを残してください。

</details>

<details><summary>详细发布记录（简体中文）</summary>

拾光是一款面向摄影师、摄像师、个人创作者与摄影摄像团队的本地拷卡、双备份、校验与项目归档工具。

v0.1.13 增加了更安全的项目删除与恢复流程，并集中修复路径提示和注意说明偶发闪黑、消失的问题。

> [!IMPORTANT]
> 拾光目前仍是免费内测版。处理重要素材时，请保留原始存储卡，并确认至少还有一份可靠备份后再格式化卡片。

## 本次更新

### 新增项目回收站

- 项目卡片菜单现在可以将项目移入回收站，之后可以随时恢复。
- 默认移入回收站只隐藏拾光中的项目记录，不移动、不删除原项目文件夹和素材。
- 彻底删除时可以选择只删除资料库记录，或将整个项目根文件夹移入 macOS 系统废纸篓。
- 归档盘和第二备份盘不会随项目删除而被处理。

### 修复“仅标记完成”

- 修复归档操作中的“仅标记完成”无法使用的问题。
- 该操作现在只更新项目状态，不要求外接项目盘在线，也不会整理目录或移动素材。

### 路径与说明提示更加稳定

- 修复设置和拷卡页面注意号悬停圆形被裁切的问题。
- 注意号不再显示问号光标，键盘操作和辅助说明仍然保留。
- 改善 NAS、百度网盘及长路径状态提示的命中范围和显示位置。
- 修复快速移动鼠标时提示框叠加闪黑、刚出现就消失的问题。
- 同一时刻只保留一个悬停提示，鼠标移入说明框后仍可持续阅读。

## 升级方式

如果已经安装 v0.1.12：

1. 打开拾光的“设置”页面。
2. 选择“检查更新”。
3. 确认下载并安装 v0.1.13。

为保护正在处理的素材，拷卡或项目归档进行中不会执行安装和重启，请等待任务结束后再更新。

如果 App 内暂时没有显示更新，也可以退出拾光，从本 Release 下载 DMG，将新版“拾光”拖入“Applications / 应用程序”并替换旧版本。已有项目记录和设置会继续保留。

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
