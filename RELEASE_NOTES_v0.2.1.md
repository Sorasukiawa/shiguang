[简体中文](#简体中文) | [繁體中文](#繁體中文) | [English](#english) | [日本語](#日本語)

## 简体中文

拾光 v0.2.1 继续免费内测。本版强化拷贝校验，并新增可查询、导出的任务报告。

- **校验更明确：**快速校验会完整回读每份目标文件并比较 XXH64；完整校验还会独立重读源文件。设备无法绕开系统缓存时，结果会如实标明。
- **任务报告：**拷卡、文件拷贝、项目素材导入、本地归档和网络归档的结果可按项目、日期、类型及状态筛选；可导出单任务或选中任务的离线 HTML、A4 多页 PDF。报告包含逐目标状态、可得的校验结果、失败信息与备注，支持四语言和隐藏完整路径。
- **中断记录：**任务或 App 意外退出后，遗留的活跃结果会标为中断；旧记录缺少的时间、校验结果等仍显示为未知，不会推断成功。
- **慢盘响应：**拷卡预检使用独立数据库连接；等待存储设备检查时，不再占用其他页面共用的数据库连接。

仅支持 Apple Silicon macOS。公开 v0.2.0 用户可在设置中检查更新；执行中的拷卡、文件拷贝或归档任务会阻止安装。更新前请结束重要任务，并保留原始素材及另一份可靠备份。

本版仍为 ad-hoc 签名，未取得 Apple Developer ID 签名或公证。隔离验收覆盖原生 PDF、实体 U 盘和独立 SMB 故障；其中一次 272 MiB SMB 恢复耗时 419 秒。实体介质上的拷卡与本地归档失败重试已通过界面验证，并确认新旧作业关联。

## 繁體中文

拾光 v0.2.1 繼續免費內測。本版強化複製驗證，並新增可查詢、匯出的工作報告。

- **驗證更明確：**快速驗證會完整重讀每份目的地檔案並比對 XXH64；完整驗證還會另外重讀來源檔案。裝置無法繞過系統快取時，結果會如實標示。
- **工作報告：**記憶卡轉存、檔案複製、專案素材匯入、本機封存與網路封存的結果，可依專案、日期、類型及狀態篩選；可將單一或選取的工作匯出為離線 HTML、A4 多頁 PDF。報告包含各目的地狀態、可取得的驗證結果、失敗資訊與備註，支援四種語言和隱藏完整路徑。
- **中斷記錄：**工作或 App 意外結束後，遺留的進行中結果會標為中斷；舊記錄缺少的時間、驗證結果等仍顯示為未知，不會推定成功。
- **慢速磁碟回應：**記憶卡轉存預檢使用獨立資料庫連線；等待儲存裝置檢查時，不再佔用其他頁面共用的連線。

僅支援 Apple Silicon macOS。公開 v0.2.0 使用者可在設定中檢查更新；進行中的記憶卡轉存、檔案複製或封存工作會阻止安裝。更新前請結束重要工作，保留原始素材與另一份可靠備份。

本版仍採用 ad-hoc 簽署，未取得 Apple Developer ID 簽署或公證。隔離驗收涵蓋原生 PDF、實體 USB 隨身碟和獨立 SMB 故障；其中一次 272 MiB SMB 復原耗時 419 秒。實體媒體上的記憶卡轉存與本機封存失敗重試已透過介面驗證，並確認新舊工作關聯。

## English

Shiguang v0.2.1 continues the free beta. This release strengthens copy verification and adds searchable, exportable task reports.

- **Clearer verification:** Quick verification fully rereads every destination file and compares XXH64 hashes. Full verification also rereads the source independently. Results disclose when a device cannot bypass the system cache.
- **Task reports:** Filter camera-card offloads, file copies, project media imports, local archives, and network archives by project, date, type, and status. Export one or several selected tasks as offline HTML or multipage A4 PDF. Reports show each destination's status, available verification evidence, failures, and notes, with four-language support and an option to hide full paths.
- **Interrupted work:** Active results left by an unexpected task or app exit are recorded as interrupted. Missing times and verification results in older records remain unknown rather than being inferred as successful.
- **Slow-drive responsiveness:** Card-offload preflight uses a separate database connection, leaving the connection shared by other pages available while storage checks wait.

Apple Silicon macOS only. Users of public v0.2.0 can check for updates in Settings. Running offload, file-copy, or archive jobs prevent installation. Finish important jobs and keep the original media plus another reliable backup before upgrading.

This build remains ad-hoc signed, without Apple Developer ID signing or notarization. Isolated validation covered native PDFs, a physical USB drive, and an independent SMB session; one 272 MiB SMB recovery took 419 seconds. Failed card offloads and local archives were retried through the UI on physical media, with the new jobs linked to the earlier attempts.

## 日本語

拾光 v0.2.1 は無料ベータ版の更新です。コピーの検証を強化し、検索・書き出しができるタスクレポートを追加しました。

- **検証の明確化：**高速検証では各保存先ファイルを最後まで読み直し、XXH64 を比較します。完全検証では元ファイルも別途読み直します。装置でシステムキャッシュを回避できない場合、そのことを結果に表示します。
- **タスクレポート：**メモリーカードの取り込み、ファイルコピー、プロジェクトへの素材追加、ローカルアーカイブ、ネットワークアーカイブの結果を、プロジェクト・日付・種類・状態で絞り込めます。単一または選択した複数のタスクを、オフライン HTML または複数ページの A4 PDF に書き出せます。保存先ごとの状態、確認できた検証結果、失敗内容、メモを記録し、4 言語とフルパスの非表示に対応します。
- **中断の記録：**タスクや App が予期せず終了した場合、残った実行中の結果は中断として記録します。古い記録に存在しない時刻や検証結果は、成功と推測せず不明のまま表示します。
- **低速ドライブへの対応：**カード取り込みの事前確認に専用のデータベース接続を使い、ストレージの確認待ち中も他の画面が共有する接続を占有しません。

Apple Silicon 搭載 macOS 専用です。公開版 v0.2.0 の利用者は設定から更新を確認できます。取り込み、ファイルコピー、アーカイブの実行中は更新をインストールできません。更新前に重要な処理を終え、元の素材ともう一つの信頼できるバックアップを保管してください。

このビルドは引き続き ad-hoc 署名で、Apple Developer ID 署名および公証はありません。分離した環境でネイティブ PDF、実機 USB メモリー、独立した SMB 接続の障害を検証しました。そのうち 272 MiB の SMB 復旧には 419 秒かかりました。実機メディアでカード取り込みとローカルアーカイブの失敗後の再試行を UI から検証し、新旧ジョブの関連付けも確認しました。
