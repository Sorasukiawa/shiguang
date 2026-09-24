# 拾光 Shiguang v0.1.16 · 更灵活的素材目录

**历史版本 / Historical release** · 新项目可选“简单存放”或“按卡分开”，内置预设加入 LOGO 目录；拷卡前必须明确选择项目。已有项目的目录规则不会自动改变。

**[下载本版本 DMG · Apple Silicon Mac](https://github.com/Sorasukiawa/shiguang/releases/download/v0.1.16/Shiguang_0.1.16_aarch64.dmg)** · [安装指南](https://getshiguang.pages.dev/guides/) · [全部版本](https://github.com/Sorasukiawa/shiguang/blob/main/VERSIONS.md)

<strong>历史版本提示：</strong>本页下载固定为此版本。若已安装的旧版没有更新通道，请结束任务、退出 App 后用目标版本 DMG 手动升级。

<details><summary>繁體中文 · 更靈活的素材資料夾</summary>

新專案可選「簡單存放」或「按卡分開」，內建預設加入 LOGO 資料夾；轉存前必須明確選擇專案。現有專案的資料夾規則不會自動變更。

僅提供 Apple Silicon macOS 免費測試版，採用 ad-hoc 簽署，尚無 Apple Developer ID 簽署或公證。DMG 供手動安裝；重要素材請保留原卡及另一份可靠備份。

</details>

<details><summary>English · Flexible media folders</summary>

New projects can use a simpler media layout or separate folders per card. Built-in presets add a LOGO folder, and ingest requires an explicit project choice. Existing project layouts do not change automatically.

Apple Silicon macOS free beta only. This build is ad-hoc signed, without Apple Developer ID signing or notarization. Use the DMG for manual installation, and keep the original card plus another reliable backup for important media.

</details>

<details><summary>日本語 · 素材フォルダーの選択肢</summary>

新規プロジェクトで簡単な保存方法かカード別フォルダーを選択可能に。標準設定に LOGO フォルダーを追加し、取り込み前にプロジェクトの明示的な選択を必須にしました。既存プロジェクトの構成は自動変更しません.

Apple Silicon macOS 向けの無料ベータ版のみです。ad-hoc 署名で、Apple Developer ID 署名と公証はありません。手動インストールには DMG を使い、大切な素材は元カードと別の信頼できるバックアップを残してください。

</details>

<details><summary>详细发布记录（简体中文）</summary>

拾光是一款面向摄影师、摄像师、个人创作者与摄影摄像团队的本地拷卡、双备份、校验与项目归档工具。

v0.1.16 让新项目的素材目录更灵活，并进一步减少拷卡时的误操作。

> [!IMPORTANT]
> 拾光目前仍是免费内测版。处理重要素材时，请保留原始存储卡，并确认至少还有一份可靠备份后再格式化卡片。

## 本次更新

- 新建项目时可以选择“简单存放”或“按卡分开”。
- “简单存放”会将同一机位的素材集中存放，减少不必要的文件夹层级。
- “按卡分开”会为每张存储卡建立 R01、R02 等独立目录，避免不同卡片的素材混在一起。
- 视频、照片和混合项目的内置预设统一增加独立的 `LOGO` 素材目录。
- 拷卡页只有在明确选择项目后才会准备拷贝，不再自动绑定列表中的第一个项目。
- 项目回收站名称已简化为“回收站”，仍与 macOS“系统废纸篓”明确区分。
- 优化素材存放方式的切换反馈，并继续支持 macOS“减弱动态效果”。

## 兼容与安全

- 已有项目继续沿用原来的素材目录规则，不会因为升级自动改变现有文件夹结构。
- 如果项目结构信息缺失或异常，拾光会先停止拷卡，不会猜测保存位置。

## 升级方式

如果已经安装 v0.1.15，可以在拾光“设置”页面检查更新。拷卡或项目归档进行中不会执行安装和重启。

也可以退出拾光，从本 Release 下载 DMG，将新版“拾光”拖入“Applications / 应用程序”并替换旧版。已有项目记录和设置会继续保留。

## 下载与首次打开

当前公开安装包仅适用于搭载 Apple M 系列芯片的 Mac。Intel Mac 与 Windows 版尚未提供公开下载。

本内测包使用 ad-hoc 签名，尚未使用 Apple Developer ID 签名，也未经过 Apple 公证。如果 macOS 拦截首次启动，请前往“系统设置 → 隐私与安全性”，确认应用为“拾光”后选择“仍要打开”。

请勿关闭 Gatekeeper，也不要为来源不明的安装包绕过系统保护。

## 反馈

如果遇到问题，欢迎通过本仓库的 Issues 反馈。建议附上拾光版本、macOS 版本、Mac 芯片型号、复现步骤和必要截图；提交前请遮挡客户名称、项目名称和本地路径等敏感信息。

本公开仓库用于提供官方安装包、版本说明和问题反馈，不包含拾光源代码。

</details>

---

<strong>安装与文件：</strong>本版仅提供 Apple Silicon macOS。DMG 用于手动安装；同页的 `Shiguang_aarch64.app.tar.gz`、`.sig` 和 `latest.json` 供应用内更新使用。本版为 ad-hoc 签名，未获 Apple Developer ID 签名或 Apple 公证。GitHub 自动生成的 Source code 归档只是公开资料，不含拾光 App 源码，也不是安装包。

重要素材请保留原始卡和另一份可靠备份，确认副本后再格式化。问题请提交至 [Issues](https://github.com/Sorasukiawa/shiguang/issues)，不要上传原始素材、客户资料或私密路径。
