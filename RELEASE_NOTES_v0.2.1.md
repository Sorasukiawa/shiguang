# 拾光 Shiguang v0.2.1 · 校验升级与任务报告

快速校验完整回读每份目标文件；完整校验还会独立重读来源。新增可筛选、导出的 HTML／PDF 任务报告，并改进慢盘预检响应。

**[下载本版本 DMG · Apple Silicon Mac](https://github.com/Sorasukiawa/shiguang/releases/download/v0.2.1/Shiguang_0.2.1_aarch64.dmg)** · [安装指南](https://getshiguang.pages.dev/guides/) · [全部版本](https://github.com/Sorasukiawa/shiguang/blob/main/VERSIONS.md)

**升级提示：**公开 v0.2.0 可从设置检查更新；正在运行的拷卡、文件拷贝或归档任务会阻止安装。升级前请结束重要任务并保留备份。

**已知边界：**NAS／SMB 断连后的恢复可能较慢；本地写入第三方同步目录，不等于云端同步已完成或已验证。

<details><summary>繁體中文 · 驗證升級與工作報告</summary>

快速驗證完整重讀每份目的地檔案；完整驗證還會獨立重讀來源。新增可篩選、匯出的 HTML／PDF 工作報告，並改善慢速磁碟預檢時的回應。

僅提供 Apple Silicon macOS 免費測試版，採用 ad-hoc 簽署，尚無 Apple Developer ID 簽署或公證。DMG 供手動安裝；重要素材請保留原卡及另一份可靠備份。

NAS／SMB 斷線後的復原可能較慢；寫入第三方同步資料夾，不代表雲端同步已完成或已驗證。

</details>

<details><summary>English · Verification & task reports</summary>

Fast verification now rereads every destination file; full verification also independently rereads the source. Searchable HTML/PDF task reports arrive, and slow-disk preflight no longer blocks other pages.

Apple Silicon macOS free beta only. This build is ad-hoc signed, without Apple Developer ID signing or notarization. Use the DMG for manual installation, and keep the original card plus another reliable backup for important media.

Recovery after a NAS/SMB disconnect may be slow. Writing to a third-party sync folder does not establish that cloud synchronization completed or was verified.

</details>

<details><summary>日本語 · 検証の強化と作業レポート</summary>

簡易検証では保存先ファイルをすべて読み直し、完全検証では元ファイルも独立して読み直します。検索・書き出し可能な HTML／PDF 作業レポートを追加し、低速ディスクの事前確認中の応答も改善しました。

Apple Silicon macOS 向けの無料ベータ版のみです。ad-hoc 署名で、Apple Developer ID 署名と公証はありません。手動インストールには DMG を使い、大切な素材は元カードと別の信頼できるバックアップを残してください。

NAS／SMB の切断後は復旧に時間がかかる場合があります。外部同期フォルダーへの書き込みは、クラウド同期の完了や検証を意味しません。

</details>

<img src="https://raw.githubusercontent.com/Sorasukiawa/shiguang/64ca6e5971d1245c2da1a4a3040bed1c13d0fee5/report-v0.2.1-synthetic.png" width="480" alt="v0.2.1 PDF 任务报告示例，全部为合成数据">

*报告示例；全部内容为合成数据。*

<details><summary>详细发布记录（四语言）</summary>

[简体中文](#简体中文) | [繁體中文](#繁體中文) | [English](#english) | [日本語](#日本語)

## 简体中文

拾光 v0.2.1 继续免费内测。本版强化拷贝校验，并新增可查询、导出的任务报告。

- **校验更明确：**快速校验会完整回读每份目标文件并比较 XXH64；完整校验还会独立重读源文件。设备无法绕开系统缓存时，结果会如实标明。
- **任务报告：**拷卡、文件拷贝、项目素材导入、本地归档和网络归档的结果可按项目、日期、类型及状态筛选；可导出单任务或选中任务的离线 HTML、A4 多页 PDF。报告包含逐目标状态、可得的校验结果、失败信息与备注，支持四语言和隐藏完整路径。
- **中断记录：**任务或 App 意外退出后，遗留的活跃结果会标为中断；旧记录缺少的时间、校验结果等仍显示为未知，不会推断成功。
- **慢盘响应：**拷卡预检使用独立数据库连接；等待存储设备检查时，不再占用其他页面共用的数据库连接。

仅支持 Apple Silicon macOS。公开 v0.2.0 用户可在设置中检查更新；执行中的拷卡、文件拷贝或归档任务会阻止安装。更新前请结束重要任务，并保留原始素材及另一份可靠备份。


## 繁體中文

拾光 v0.2.1 繼續免費內測。本版強化複製驗證，並新增可查詢、匯出的工作報告。

- **驗證更明確：**快速驗證會完整重讀每份目的地檔案並比對 XXH64；完整驗證還會另外重讀來源檔案。裝置無法繞過系統快取時，結果會如實標示。
- **工作報告：**記憶卡轉存、檔案複製、專案素材匯入、本機封存與網路封存的結果，可依專案、日期、類型及狀態篩選；可將單一或選取的工作匯出為離線 HTML、A4 多頁 PDF。報告包含各目的地狀態、可取得的驗證結果、失敗資訊與備註，支援四種語言和隱藏完整路徑。
- **中斷記錄：**工作或 App 意外結束後，遺留的進行中結果會標為中斷；舊記錄缺少的時間、驗證結果等仍顯示為未知，不會推定成功。
- **慢速磁碟回應：**記憶卡轉存預檢使用獨立資料庫連線；等待儲存裝置檢查時，不再佔用其他頁面共用的連線。

僅支援 Apple Silicon macOS。公開 v0.2.0 使用者可在設定中檢查更新；進行中的記憶卡轉存、檔案複製或封存工作會阻止安裝。更新前請結束重要工作，保留原始素材與另一份可靠備份。


## English

Shiguang v0.2.1 continues the free beta. This release strengthens copy verification and adds searchable, exportable task reports.

- **Clearer verification:** Quick verification fully rereads every destination file and compares XXH64 hashes. Full verification also rereads the source independently. Results disclose when a device cannot bypass the system cache.
- **Task reports:** Filter camera-card offloads, file copies, project media imports, local archives, and network archives by project, date, type, and status. Export one or several selected tasks as offline HTML or multipage A4 PDF. Reports show each destination's status, available verification evidence, failures, and notes, with four-language support and an option to hide full paths.
- **Interrupted work:** Active results left by an unexpected task or app exit are recorded as interrupted. Missing times and verification results in older records remain unknown rather than being inferred as successful.
- **Slow-drive responsiveness:** Card-offload preflight uses a separate database connection, leaving the connection shared by other pages available while storage checks wait.

Apple Silicon macOS only. Users of public v0.2.0 can check for updates in Settings. Running offload, file-copy, or archive jobs prevent installation. Finish important jobs and keep the original media plus another reliable backup before upgrading.


## 日本語

拾光 v0.2.1 は無料ベータ版の更新です。コピーの検証を強化し、検索・書き出しができるタスクレポートを追加しました。

- **検証の明確化：**高速検証では各保存先ファイルを最後まで読み直し、XXH64 を比較します。完全検証では元ファイルも別途読み直します。装置でシステムキャッシュを回避できない場合、そのことを結果に表示します。
- **タスクレポート：**メモリーカードの取り込み、ファイルコピー、プロジェクトへの素材追加、ローカルアーカイブ、ネットワークアーカイブの結果を、プロジェクト・日付・種類・状態で絞り込めます。単一または選択した複数のタスクを、オフライン HTML または複数ページの A4 PDF に書き出せます。保存先ごとの状態、確認できた検証結果、失敗内容、メモを記録し、4 言語とフルパスの非表示に対応します。
- **中断の記録：**タスクや App が予期せず終了した場合、残った実行中の結果は中断として記録します。古い記録に存在しない時刻や検証結果は、成功と推測せず不明のまま表示します。
- **低速ドライブへの対応：**カード取り込みの事前確認に専用のデータベース接続を使い、ストレージの確認待ち中も他の画面が共有する接続を占有しません。

Apple Silicon 搭載 macOS 専用です。公開版 v0.2.0 の利用者は設定から更新を確認できます。取り込み、ファイルコピー、アーカイブの実行中は更新をインストールできません。更新前に重要な処理を終え、元の素材ともう一つの信頼できるバックアップを保管してください。


</details>

---

**安装与文件：**本版仅提供 Apple Silicon macOS。DMG 用于手动安装；同页的 `Shiguang_aarch64.app.tar.gz`、`.sig` 和 `latest.json` 供应用内更新使用。本版为 ad-hoc 签名，未获 Apple Developer ID 签名或 Apple 公证。GitHub 自动生成的 Source code 归档只是公开资料，不含拾光 App 源码，也不是安装包。

重要素材请保留原始卡和另一份可靠备份，确认副本后再格式化。问题请提交至 [Issues](https://github.com/Sorasukiawa/shiguang/issues)，不要上传原始素材、客户资料或私密路径。
