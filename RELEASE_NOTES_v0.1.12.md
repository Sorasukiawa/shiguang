# 拾光 Shiguang v0.1.12 · 项目分组与窗口交互

**历史版本 / Historical release** · 修复项目分组菜单被裁切；改进窗口缩放布局、跨分组卡片动画、键盘焦点与减弱动态效果。

**[下载本版本 DMG · Apple Silicon Mac](https://github.com/Sorasukiawa/shiguang/releases/download/v0.1.12/Shiguang_0.1.12_aarch64.dmg)** · [安装指南](https://getshiguang.pages.dev/guides/) · [全部版本](https://github.com/Sorasukiawa/shiguang/blob/main/VERSIONS.md)

<strong>历史版本提示：</strong>本页下载固定为此版本。若已安装的旧版没有更新通道，请结束任务、退出 App 后用目标版本 DMG 手动升级。

<details><summary>繁體中文 · 專案分組與視窗互動</summary>

修正專案分組選單被裁切；改善視窗縮放版面、跨分組卡片動效、鍵盤焦點及減弱動態效果。

僅提供 Apple Silicon macOS 免費測試版，採用 ad-hoc 簽署，尚無 Apple Developer ID 簽署或公證。DMG 供手動安裝；重要素材請保留原卡及另一份可靠備份。

</details>

<details><summary>English · Groups & window layout</summary>

Fixes clipped project-group menus and improves responsive window layout, card movement between groups, keyboard focus, and reduced-motion behavior.

Apple Silicon macOS free beta only. This build is ad-hoc signed, without Apple Developer ID signing or notarization. Use the DMG for manual installation, and keep the original card plus another reliable backup for important media.

</details>

<details><summary>日本語 · グループとウィンドウ操作</summary>

プロジェクトのグループメニューが欠ける問題を修正。ウィンドウサイズ変更時のレイアウト、グループ間のカード移動、キーボードフォーカス、動きを減らす設定を改善しました。

Apple Silicon macOS 向けの無料ベータ版のみです。ad-hoc 署名で、Apple Developer ID 署名と公証はありません。手動インストールには DMG を使い、大切な素材は元カードと別の信頼できるバックアップを残してください。

</details>

<details><summary>详细发布记录（简体中文）</summary>

拾光是一款面向摄影师、摄像师、个人创作者与摄影摄像团队的本地拷卡、双备份、校验与项目归档工具。

v0.1.12 主要优化项目页的分组操作和动态表现，让窗口缩放、整理项目与切换分组更加稳定、自然。

## 本次更新

### 分组操作菜单不再被遮挡

- 修复自建分组右侧“三个点”菜单被项目列表底部裁切的问题。
- 菜单会根据窗口剩余空间自动向上或向下展开，并始终与窗口边缘保持安全距离。
- 窗口缩放、页面滚动时，菜单会继续跟随对应的分组按钮。

### 窗口缩放更加平稳

- 重新整理项目工具栏的响应式布局。
- 调整 App 窗口大小时，标题、搜索、状态和分组控件不再突然换位。
- 项目卡片的可用宽度会随窗口连续变化，减少突兀的界面跳动。

### 项目换组动画更加自然

- 优化切换分组时项目卡片跨列、跨行移动的轨迹。
- 动画速度更从容，并取消不自然的回弹效果。
- 打开菜单等无关操作不会重新触发整组项目卡片动画。

### 键盘操作改进

- 使用键盘打开分组操作菜单后，焦点会自动进入第一个可用操作。
- 按下 `Escape` 可关闭菜单，并将焦点返回原来的“三个点”按钮。
- 系统开启“减弱动态效果”时，会自动停用大幅位置动画。

## 升级方式

如果已经安装 v0.1.11：

1. 打开拾光的“设置”页面。
2. 选择“检查更新”。
3. 确认下载并安装 v0.1.12。

为保护正在处理的素材，拷卡或项目归档进行中不会执行安装和重启。请等待任务结束后再更新。

如果 App 内暂时没有显示更新，也可以退出拾光，从本 Release 下载 DMG，将新版“拾光”拖入“Applications / 应用程序”并替换旧版本。已有项目记录和设置会继续保留。

## 下载与首次打开

当前公开安装包适用于搭载 Apple M 系列芯片的 Mac。

本内测包使用 ad-hoc 签名，尚未使用 Apple Developer ID 签名，也未经过 Apple 公证。macOS 可能在首次启动时拦截：

1. 只从本仓库的 Releases 下载 DMG。
2. 将“拾光”拖入“Applications / 应用程序”。
3. 正常打开一次；如果系统拦截，请关闭提示。
4. 前往“系统设置 → 隐私与安全性”，确认应用为“拾光”后选择“仍要打开”。

请勿关闭 Gatekeeper，也不要为来源不明的安装包绕过系统保护。

> 拾光目前仍处于免费内测阶段。处理重要素材时，请保留原始存储卡，并确认至少还有一份可靠备份后再格式化卡片。

## 反馈

如果遇到问题，欢迎通过本仓库的 Issues 反馈。建议附上拾光版本、macOS 版本、Mac 芯片型号、复现步骤和必要截图；提交前请遮挡客户名称、项目名称和本地路径等敏感信息。

本公开仓库用于提供官方安装包、版本说明和问题反馈，不包含拾光源代码。

</details>

---

<strong>安装与文件：</strong>本版仅提供 Apple Silicon macOS。DMG 用于手动安装；同页的 `Shiguang_aarch64.app.tar.gz`、`.sig` 和 `latest.json` 供应用内更新使用。本版为 ad-hoc 签名，未获 Apple Developer ID 签名或 Apple 公证。GitHub 自动生成的 Source code 归档只是公开资料，不含拾光 App 源码，也不是安装包。

重要素材请保留原始卡和另一份可靠备份，确认副本后再格式化。问题请提交至 [Issues](https://github.com/Sorasukiawa/shiguang/issues)，不要上传原始素材、客户资料或私密路径。
