# 拾光 Shiguang v0.1.17 · 品牌更新与拷卡反馈

**历史版本 / Historical release** · 统一暖金色品牌图标；完整校验失败会写入可读报告，加强来源路径与卷号保护，改进项目选择与归档反馈。

**[下载本版本 DMG · Apple Silicon Mac](https://github.com/Sorasukiawa/shiguang/releases/download/v0.1.17/Shiguang_0.1.17_aarch64.dmg)** · [安装指南](https://getshiguang.pages.dev/guides/) · [全部版本](https://github.com/Sorasukiawa/shiguang/blob/main/VERSIONS.md)

<strong>升级例外 / Upgrade exception / 升級例外 / 更新時の注意：</strong>公开 v0.1.17 安装包未配置更新通道。已安装该版的用户须结束任务、退出拾光，再用目标版本的 DMG 手动替换；不要依赖设置页检查更新。 / The public v0.1.17 build has no updater endpoint. Quit after finishing tasks and install the target version's DMG manually. / 公開 v0.1.17 沒有更新通道，請結束工作、退出 App 後使用目標版本 DMG 手動升級。 / 公開 v0.1.17 には更新先がないため、作業終了後にアプリを終了し、目的のバージョンの DMG で手動更新してください。

<details><summary>繁體中文 · 品牌更新與轉存回饋</summary>

統一暖金色品牌圖示；完整驗證失敗會寫入可讀報告，加強來源路徑與卷號保護，改善專案選擇與封存回饋。

已安裝公開 v0.1.17 的使用者，請結束工作並退出 App，再以目標版本的 DMG 手動升級。

僅提供 Apple Silicon macOS 免費測試版，採用 ad-hoc 簽署，尚無 Apple Developer ID 簽署或公證。DMG 供手動安裝；重要素材請保留原卡及另一份可靠備份。

</details>

<details><summary>English · Branding & ingest feedback</summary>

Introduces the warm-gold app identity. Full-verification failures appear in readable reports; source-path and card-number safeguards, project selection, and archive feedback improve.

Users of the public v0.1.17 build must finish tasks, quit the app, and upgrade manually with the target version's DMG.

Apple Silicon macOS free beta only. This build is ad-hoc signed, without Apple Developer ID signing or notarization. Use the DMG for manual installation, and keep the original card plus another reliable backup for important media.

</details>

<details><summary>日本語 · ブランドと取り込み結果</summary>

暖かい金色のブランドアイコンを導入。完全検証の失敗を読めるレポートへ記録し、元カードのパスと番号の保護、プロジェクト選択、アーカイブ表示を改善しました。

公開 v0.1.17 の利用者は作業終了後にアプリを終了し、目的のバージョンの DMG で手動更新してください。

Apple Silicon macOS 向けの無料ベータ版のみです。ad-hoc 署名で、Apple Developer ID 署名と公証はありません。手動インストールには DMG を使い、大切な素材は元カードと別の信頼できるバックアップを残してください。

</details>

<details><summary>详细发布记录（四语言）</summary>

[简体中文](#简体中文) | [繁體中文](#繁體中文) | [English](#english) | [日本語](#日本語)

## 简体中文

拾光是一款面向摄影师、摄像师、个人创作者与摄影摄像团队的本地拷卡、双备份、校验与项目归档工具。

v0.1.17 统一了新的品牌 Logo，并修复了多项可能影响拷卡判断、报告可信度与归档反馈的问题。

> [!IMPORTANT]
> 拾光目前仍是免费内测版。处理重要素材时，请保留原始存储卡，并确认至少还有一份可靠备份后再格式化卡片。

### 本次更新

- 采用全新的暖金色“收光”Logo，App、DMG 与公开下载页使用同一套品牌图标。
- 完整校验发现的问题现在会写入可读报告，避免任务失败时报告看起来仍像成功。
- 加强来源卡异常路径拦截；素材打开或重试前都会再次确认仍在已选存储卡内，避免意外读取卡外文件。
- 连续处理大量同机位存储卡时，卷号目录达到上限后会改用独立安全目录，不会把新卡混入已有目录。
- 拷卡页未选择项目时会明确提示，不再显示伪选中的第一个项目或“正在扫描”。
- 项目归档进度反馈更及时，并在页面恢复后自动重新同步，减少长时间归档时的等待与后台查询。

### 升级与首次打开

如果已经安装 v0.1.16，可以在拾光“设置”页面检查更新。也可以退出拾光，从本 Release 下载 DMG，将新版“拾光”拖入“Applications / 应用程序”并替换旧版。已有项目记录和设置会继续保留。

当前公开安装包仅适用于搭载 Apple M 系列芯片的 Mac。本免费内测包使用 ad-hoc 签名，尚未使用 Apple Developer ID 签名，也未经过 Apple 公证；如果 macOS 拦截首次启动，请前往“系统设置 → 隐私与安全性”，确认应用为“拾光”后选择“仍要打开”。请勿关闭 Gatekeeper。

Intel Mac 与 Windows 版尚未提供公开下载。

## 繁體中文

拾光是一套為攝影師、影像工作者、獨立創作者與影像團隊打造的本機素材轉存、二重備份、檢驗與專案封存工具。

v0.1.17 統一了新的品牌 Logo，並修正多項可能影響轉存判斷、報告可信度與封存回饋的問題。

> [!IMPORTANT]
> 拾光目前仍是免費內測版。處理重要素材時，請保留原始記憶卡，並在確認至少還有一份可靠備份後才格式化卡片。

### 本次更新

- 採用全新的暖金色「收光」Logo，App、DMG 與公開下載頁使用同一套品牌圖示。
- 完整檢驗發現的問題現在會寫入可讀報告，避免工作失敗時報告看起來仍像成功。
- 強化來源記憶卡的異常路徑攔截；素材開啟或重試前都會再次確認仍在已選記憶卡內，避免意外讀取卡外檔案。
- 連續處理大量同機位記憶卡時，卷號資料夾達到上限後會改用獨立安全資料夾，不會把新卡混入既有資料夾。
- 轉存頁尚未選擇專案時會清楚提示，不再顯示假選取的第一個專案或「正在掃描」。
- 專案封存進度回饋更即時，頁面恢復後也會自動重新同步，減少長時間封存時的等待與背景查詢。

### 升級與首次開啟

如果已安裝 v0.1.16，可以在拾光「設定」頁面檢查更新。也可以結束拾光，從本 Release 下載 DMG，將新版「拾光」拖曳到「Applications / 應用程式」並取代舊版。既有專案記錄與設定會繼續保留。

目前公開安裝檔只適用於搭載 Apple M 系列晶片的 Mac。本免費內測版使用 ad-hoc 簽署，尚未使用 Apple Developer ID 簽署，也尚未通過 Apple 公證；若 macOS 阻擋首次開啟，請前往「系統設定 → 隱私權與安全性」，確認應用程式為「拾光」後選擇「強制打開」。請勿關閉 Gatekeeper。

Intel Mac 與 Windows 版尚未提供公開下載。

## English

Shiguang is a local-first media offload, dual-destination backup, verification, and project-archive tool for photographers, filmmakers, independent creators, and production teams.

v0.1.17 introduces the unified new brand mark and fixes several issues that could affect offload decisions, report trustworthiness, and archive feedback.

> [!IMPORTANT]
> Shiguang is still a free beta. Keep the original memory card and confirm at least one other known-good backup before formatting it.

### What changed

- Shiguang now uses the new warm-gold “captured light” mark across the app, DMG, and public download page.
- Full-verification issues now appear in the human-readable report, so a failed job cannot still look successful there.
- Stricter source-card safeguards recheck that media still belongs to the selected card before opening or retrying it, preventing accidental reads outside the card.
- When many cards from one camera position exhaust the numbered folders, the next card uses a separate safe folder instead of being mixed into an existing one.
- The offload screen now clearly asks for a project when none is selected, without showing a false first selection or “Scanning”.
- Project-archive progress updates more promptly and resynchronizes when the page returns, reducing delay and background queries during long archives.

### Upgrade and first launch

If v0.1.16 is already installed, check for updates from Shiguang Settings. You can also quit Shiguang, download the DMG from this Release, and replace the old app in Applications. Existing project records and settings are preserved.

The public installer is available only for Apple Silicon Macs with an Apple M-series chip. This free beta uses ad-hoc signing; it is not signed with an Apple Developer ID and is not notarized by Apple. If macOS blocks the first launch, open System Settings → Privacy & Security, confirm the app is Shiguang, and choose Open Anyway. Do not disable Gatekeeper.

Intel Mac and Windows builds are not publicly available.

## 日本語

拾光は、フォトグラファー、映像制作者、個人クリエイター、制作チーム向けの、ローカルで動作するメディア取り込み・二重バックアップ・検証・プロジェクトアーカイブツールです。

v0.1.17 では新しいブランドロゴを統一し、取り込み判断、レポートの信頼性、アーカイブの進捗表示に関わる複数の問題を修正しました。

> [!IMPORTANT]
> 拾光は引き続き無料ベータ版です。元のメモリーカードを保管し、別の信頼できるバックアップが少なくとも1つ使用できることを確認してから、カードを初期化してください。

### 更新内容

- 新しい暖かなゴールド基調の「光を収める」ロゴを採用し、App、DMG、公開ダウンロードページのブランドアイコンを統一しました。
- 完全検証で見つかった問題を人が読めるレポートにも記録し、ジョブが失敗しているのに成功したように見える状態を防ぎます。
- 元カードの異常なパスをより厳密に検出し、ファイルを開く時や再試行時に素材が選択したメモリーカード内にあることを再確認して、カード外のファイルを誤って読み込むのを防ぎます。
- 同じカメラ位置のカードを大量に連続処理し、番号付きフォルダーが上限に達した場合は、既存フォルダーへ混在させず、新しいカードを独立した安全なフォルダーへ保存します。
- プロジェクト未選択時の取り込み画面に明確な案内を表示し、先頭プロジェクトの見せかけの選択や「スキャン中」表示をなくしました。
- プロジェクトのアーカイブ進捗をよりすばやく反映し、画面に戻った際も自動で再同期するため、長時間のアーカイブ中の待ち時間とバックグラウンド処理を抑えます。

### アップグレードと初回起動

v0.1.16 がインストール済みの場合は、拾光の「設定」からアップデートを確認できます。拾光を終了し、この Release から DMG をダウンロードして、Applications 内の旧版と置き換えることもできます。既存のプロジェクト記録と設定は保持されます。

公開インストーラーは Apple M シリーズチップを搭載した Apple Silicon Mac 専用です。この無料ベータ版は ad-hoc 署名で、Apple Developer ID による署名も Apple の公証もありません。macOS が初回起動をブロックした場合は、「システム設定 → プライバシーとセキュリティ」で対象が拾光であることを確認し、「そのまま開く」を選んでください。Gatekeeper は無効にしないでください。

Intel Mac 版と Windows 版は公開されていません。

---

If you encounter a problem, please use this repository's Issues. Include the Shiguang version, macOS version, Mac chip, reproducible steps, and complete error text. Redact client names, project names, local paths, and other sensitive information before posting.

This public repository provides official installers, release notes, and issue tracking. It does not contain Shiguang source code.

</details>

---

<strong>安装与文件：</strong>本版仅提供 Apple Silicon macOS。DMG 用于手动安装；同页的 `Shiguang_aarch64.app.tar.gz`、`.sig` 和 `latest.json` 供应用内更新使用。本版为 ad-hoc 签名，未获 Apple Developer ID 签名或 Apple 公证。GitHub 自动生成的 Source code 归档只是公开资料，不含拾光 App 源码，也不是安装包。

重要素材请保留原始卡和另一份可靠备份，确认副本后再格式化。问题请提交至 [Issues](https://github.com/Sorasukiawa/shiguang/issues)，不要上传原始素材、客户资料或私密路径。
