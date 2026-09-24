# 拾光 Shiguang v0.1.15 · ExFAT 项目删除与传输反馈

**历史版本 / Historical release** · 修复 ExFAT 外接盘上项目彻底删除的限制；区分拾光回收站与系统废纸篓，并改进失败重试。优化传输百分比居中和动效。

**[下载本版本 DMG · Apple Silicon Mac](https://github.com/Sorasukiawa/shiguang/releases/download/v0.1.15/Shiguang_0.1.15_aarch64.dmg)** · [安装指南](https://getshiguang.pages.dev/guides/) · [全部版本](https://github.com/Sorasukiawa/shiguang/blob/main/VERSIONS.md)

<strong>历史版本提示：</strong>本页下载固定为此版本。若已安装的旧版没有更新通道，请结束任务、退出 App 后用目标版本 DMG 手动升级。

<details><summary>繁體中文 · ExFAT 專案刪除與傳輸回饋</summary>

修正 ExFAT 外接碟上的專案徹底刪除限制；區分拾光回收站與系統垃圾桶，改善失敗重試。優化傳輸百分比的置中與動效。

僅提供 Apple Silicon macOS 免費測試版，採用 ad-hoc 簽署，尚無 Apple Developer ID 簽署或公證。DMG 供手動安裝；重要素材請保留原卡及另一份可靠備份。

</details>

<details><summary>English · ExFAT project deletion & progress</summary>

Fixes permanent project deletion on external ExFAT volumes, distinguishes Project Trash from the macOS Trash, and improves retry after failure. Transfer percentages and motion are refined.

Apple Silicon macOS free beta only. This build is ad-hoc signed, without Apple Developer ID signing or notarization. Use the DMG for manual installation, and keep the original card plus another reliable backup for important media.

</details>

<details><summary>日本語 · ExFAT 上の削除と転送表示</summary>

外付け ExFAT ボリュームでのプロジェクト完全削除を修正。拾光内のゴミ箱と macOS のゴミ箱を区別し、失敗後の再試行を改善。転送率の配置と動きも調整しました。

Apple Silicon macOS 向けの無料ベータ版のみです。ad-hoc 署名で、Apple Developer ID 署名と公証はありません。手動インストールには DMG を使い、大切な素材は元カードと別の信頼できるバックアップを残してください。

</details>

<details><summary>详细发布记录（简体中文）</summary>

拾光是一款面向摄影师、摄像师、个人创作者与摄影摄像团队的本地拷卡、双备份、校验与项目归档工具。

这次更新重点修复了外接 ExFAT 工作盘上的项目删除，并重新梳理项目记录与素材文件的回收逻辑；传输页的进度显示也同步完成优化。

> [!IMPORTANT]
> 拾光目前仍是免费内测版。处理重要素材时，请保留原始存储卡，并确认至少还有一份可靠备份后再格式化卡片。

## 项目删除更安全

- 普通项目第一次删除时，现在只会进入“拾光回收站”，项目文件夹和素材仍保留在原位置。
- 只有从“拾光回收站”执行彻底删除时，才可以选择保留文件，或将整个项目文件夹和素材移到 macOS 系统废纸篓。
- 修复 ExFAT 外接盘删除项目时可能出现 `Operation not supported (os error 45)` 的问题。
- 改进删除中断与重试流程：尚未完成的系统废纸篓操作会保留可重试状态，不会被误判为删除成功，也不会错误恢复成活动项目。
- 提升旧版本删除状态的兼容性，减少项目文件看起来“直接消失”的情况。
- 简体中文、繁体中文、英文和日文界面现在会明确区分“拾光回收站”与“系统废纸篓”，文件最终去向更清楚。

## 传输进度显示优化

- 修复一位数、两位数百分比在传输界面中视觉偏右的问题，数字与百分号现在保持真正居中。
- 数值变化时采用柔和的模糊翻页动效，连续更新更顺滑。
- 未变化的数字与百分号保持清晰稳定。
- 继续支持 macOS“减弱动态效果”设置。

## 删除安全边界

- 默认移入拾光回收站不会移动或删除原项目文件夹和素材。
- 选择处理项目文件夹时，只处理该项目的根目录，并移入系统废纸篓，不会直接抹除。
- 归档盘和第二备份盘不会随项目删除而被处理。
- 如果项目盘、卷身份或目录归属无法确认，拾光会保留项目记录和现场，优先避免误删。

## 升级方式

如果已经安装 v0.1.14：

1. 打开拾光的“设置”页面。
2. 选择“检查更新”。
3. 确认下载并安装 v0.1.15。

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
