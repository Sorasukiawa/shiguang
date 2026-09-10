[简体中文](#简体中文) | [繁體中文](#繁體中文) | [English](#english) | [日本語](#日本語)

## 简体中文

拾光是一款面向摄影师与影像团队的本地拷卡、双备份、校验与项目归档工具。v0.1.18 继续免费内测，重点改进任务恢复、项目读取、预设保护和更新体验。

### 本次更新

- 项目列表和详情增加读取、失败与重试反馈；慢盘查询不再阻塞任务进度初始化，刷新失败时保留已有列表。
- 加强预设保护：读取失败保留原文件，保存成功后再更新内存；未改变的预设不会在每次启动时重写。
- NAS 归档增加持久任务记录、原计划复验和失败后的新任务入口；历史记录可以展开并定位各次尝试的文件夹。
- 修正 MHL 清单的必填字段和特殊字符处理，并改进中断任务检查、补拷反馈与双目标结果说明。
- 更新下载停滞时会超时返回；失效更新包可重新检查，旧提醒随候选失效撤下。拷卡或归档期间仍禁止安装与重启。
- 改善项目详情在小窗口中的排布、窗口切换动效和四语言页面声明。

### 升级与当前范围

已完成公开 v0.1.16 → v0.1.18 的设置页下载、安装和自动重启验收。公开 v0.1.17 缺少更新通道，无法从设置页升级，请结束任务并退出拾光后，使用本页 DMG 替换旧版。0.1.18 已接入更新通道。项目记录、设置和自定义预设在本次升级中保持；内置视频预设补齐照片素材路由。全新 Mac 的首次安装仍待验收。

当前仅提供 Apple Silicon Mac 版本，继续使用 ad-hoc 签名，尚无 Apple Developer ID 签名或 Apple 公证。Intel Mac 和 Windows 版尚未提供。若系统拦截首次打开，可在「系统设置 → 隐私与安全性」确认应用后选择「仍要打开」。

NAS 已验证部分正常归档与中断恢复场景，但仍观察到 SMB 断连，底层原因尚未解决；百度同步目录的本地归档与手动云端回读不代表自动同步隔离已完成。重要素材请保留原卡及另一份可靠备份，勿仅依赖内测版或据此删除源素材。

## 繁體中文

拾光是一套面向攝影師與影像團隊的本機素材轉存、二重備份、檢驗與專案封存工具。v0.1.18 繼續免費內測，著重改善工作復原、專案讀取、預設保護與更新體驗。

### 本次更新

- 專案清單與詳情新增讀取、失敗及重試回饋；慢速磁碟查詢不再阻塞工作進度初始化，重新整理失敗時保留既有清單。
- 強化預設保護：讀取失敗時保留原檔，儲存成功後才更新記憶體；未變更的預設不會在每次啟動時重寫。
- NAS 封存新增持久工作記錄、原計畫重新檢驗及失敗後建立新工作的入口；可展開歷史記錄並定位各次嘗試的資料夾。
- 修正 MHL 清單的必填欄位及特殊字元處理，改善中斷工作檢查、補拷回饋與雙目標結果說明。
- 更新下載停滯時會逾時返回；失效更新包可重新檢查，舊提醒會隨候選失效撤下。轉存或封存期間仍禁止安裝與重新啟動。
- 改善小視窗的專案詳情排版、視窗切換動效與四語言頁面宣告。

### 升級與目前範圍

已完成公開 v0.1.16 → v0.1.18 的設定頁下載、安裝與自動重新啟動驗收。公開 v0.1.17 缺少更新通道，無法從設定頁升級，請結束工作並退出拾光後，使用本頁 DMG 取代舊版。0.1.18 已接入更新通道。專案記錄、設定與自訂預設在此次升級中保持；內建影片預設補齊照片素材路由。全新 Mac 的首次安裝仍待驗收。

目前只提供 Apple Silicon Mac 版本，仍使用 ad-hoc 簽署，尚無 Apple Developer ID 簽署或 Apple 公證。Intel Mac 與 Windows 版尚未提供。若系統阻擋首次開啟，可在「系統設定 → 隱私權與安全性」確認應用程式後選擇「強制打開」。

NAS 已驗證部分正常封存與中斷復原情境，但仍觀察到 SMB 斷線，底層原因尚未解決；百度同步目錄的本機封存與手動雲端回讀不代表自動同步隔離已完成。重要素材請保留原卡與另一份可靠備份，勿僅依賴內測版或據此刪除來源素材。

## English

Shiguang is a local media offload, dual-destination backup, verification, and project-archive tool for photographers and production teams. v0.1.18 continues the free beta, with improvements to recovery, project loading, preset protection, and updates.

### What changed

- Project lists and details show loading, failure, and retry states. Slow disk queries no longer block task-progress initialization, and failed refreshes preserve the existing list.
- Preset read failures preserve the original file. In-memory presets change only after saving succeeds, and unchanged presets are no longer rewritten on every launch.
- NAS archives gain persistent task records, re-verification of the original plan, and a new-task recovery entry after failure. Expandable history identifies each attempt's folder.
- MHL manifests now handle required fields and special characters correctly. Interrupted-job checks, resumed-copy feedback, and dual-destination result descriptions are clearer.
- Stalled update downloads time out. Invalidated packages can be checked again, and stale notices are removed. Installation and restart remain blocked during offload or archiving.
- Project details fit smaller windows better, with improved layout transitions and page language declarations for all four languages.

### Upgrade and current scope

The public v0.1.16 → v0.1.18 upgrade passed download, installation, and automatic restart checks from Settings on this Mac. The public v0.1.17 build has no update channel and cannot upgrade from Settings: finish running jobs, quit Shiguang, and replace it using this Release’s DMG. v0.1.18 includes the update channel. Project records, settings, and custom presets were preserved in this upgrade; the built-in video preset gained its photo-media route. First installation on a clean Mac remains unverified.

Only Apple Silicon Macs are supported by this release. The app uses ad-hoc signing, without an Apple Developer ID signature or Apple notarization. Intel Mac and Windows builds are not available. If macOS blocks the first launch, confirm the app in System Settings → Privacy & Security and choose Open Anyway.

Some normal NAS archive and interruption-recovery scenarios have passed, but SMB disconnections remain unresolved. Local archiving to a Baidu sync folder and manual cloud round trips do not establish automatic-sync isolation. Keep the original card and another reliable backup for important media; do not rely solely on this beta or use these results as permission to delete source media.

## 日本語

拾光は、フォトグラファーと制作チーム向けの、ローカルで動作する素材取り込み・二重バックアップ・検証・プロジェクトアーカイブツールです。v0.1.18 も無料ベータ版として、タスク復旧、プロジェクト読み込み、プリセット保護、更新操作を改善しました。

### 更新内容

- プロジェクト一覧と詳細に読み込み・失敗・再試行の状態を表示します。低速ディスクへの問い合わせがタスク進捗の初期化を妨げず、再読み込みに失敗しても既存の一覧を保持します。
- プリセットの読み込み失敗時は元のファイルを保持し、保存成功後にメモリー上の値を更新します。変更のないプリセットは起動のたびに書き換えません。
- NAS アーカイブに永続タスク記録、元の計画の再検証、失敗後の新規タスク作成を追加しました。履歴を展開して、各試行のフォルダーを確認できます。
- MHL マニフェストの必須項目と特殊文字の処理を修正し、中断タスクの確認、補完コピーの表示、二重保存の結果説明を改善しました。
- 更新ダウンロードの停止時はタイムアウトします。無効になった更新パッケージは再確認でき、古い通知も取り下げられます。取り込み・アーカイブ中は引き続きインストールと再起動を禁止します。
- 小さなウィンドウでの詳細表示、レイアウト遷移、4言語のページ言語宣言を改善しました。

### アップグレードと現在の範囲

公開版 v0.1.16 → v0.1.18 について、この Mac の設定画面からダウンロード・インストール・自動再起動を確認しました。公開版 v0.1.17 は更新先が未設定のため、設定画面からは更新できません。タスクと拾光を終了し、この Release の DMG で旧版を置き換えてください。0.1.18 には更新先を設定済みです。プロジェクト記録・設定・カスタムプリセットは保持され、内蔵の動画プリセットには写真素材の保存先が追加されました。新しい Mac への初回インストールは未検証です。

本リリースは Apple Silicon Mac 専用です。ad-hoc 署名を使用しており、Apple Developer ID 署名および Apple 公証はありません。Intel Mac 版と Windows 版は提供していません。初回起動がブロックされた場合は、「システム設定 → プライバシーとセキュリティ」で対象を確認し、「そのまま開く」を選択できます。

NAS の正常なアーカイブと中断復旧の一部は検証済みですが、SMB 切断は未解決です。Baidu 同期フォルダーへのローカル保存と手動のクラウド往復確認は、自動同期の分離完了を意味しません。重要な素材は元のカードと別の信頼できるバックアップを保管し、ベータ版だけに依存したり、これらの結果を理由に元の素材を削除したりしないでください。

---

Please report problems through this repository's Issues. Include the app version, macOS version, Mac chip, steps to reproduce, and error text. Remove private project names, paths, and client information before posting.
