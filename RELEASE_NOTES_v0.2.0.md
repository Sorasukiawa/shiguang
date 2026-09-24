# 拾光 Shiguang v0.2.0 · 文件拷贝与项目素材导入

**历史版本 / Historical release** · 新增文件与文件夹多目标拷贝、Finder 拖入及项目素材导入；保留目录层级，提供空间预检、校验、逐目标结果与中断恢复。

**[下载本版本 DMG · Apple Silicon Mac](https://github.com/Sorasukiawa/shiguang/releases/download/v0.2.0/Shiguang_0.2.0_aarch64.dmg)** · [安装指南](https://getshiguang.pages.dev/guides/) · [全部版本](https://github.com/Sorasukiawa/shiguang/blob/main/VERSIONS.md)

**历史版本提示：**本页下载固定为此版本。若已安装的旧版没有更新通道，请结束任务、退出 App 后用目标版本 DMG 手动升级。

<details><summary>繁體中文 · 檔案複製與專案素材匯入</summary>

新增檔案與資料夾的多目的地複製、Finder 拖入與專案素材匯入；保留資料夾層級，提供空間預檢、驗證、各目的地結果與中斷復原。

僅提供 Apple Silicon macOS 免費測試版，採用 ad-hoc 簽署，尚無 Apple Developer ID 簽署或公證。DMG 供手動安裝；重要素材請保留原卡及另一份可靠備份。

</details>

<details><summary>English · File copy & project import</summary>

Adds multi-destination file and folder copying, Finder drag and drop, and project media import. Preserves folder structure and provides capacity preflight, verification, per-destination results, and interruption recovery.

Apple Silicon macOS free beta only. This build is ad-hoc signed, without Apple Developer ID signing or notarization. Use the DMG for manual installation, and keep the original card plus another reliable backup for important media.

</details>

<details><summary>日本語 · ファイルコピーと素材追加</summary>

ファイル／フォルダーの複数保存先へのコピー、Finder からのドラッグ、プロジェクトへの素材追加に対応。階層保持、容量の事前確認、検証、保存先別の結果、中断後の復旧を備えます.

Apple Silicon macOS 向けの無料ベータ版のみです。ad-hoc 署名で、Apple Developer ID 署名と公証はありません。手動インストールには DMG を使い、大切な素材は元カードと別の信頼できるバックアップを残してください。

</details>

![v0.2.0 文件拷贝界面演示，使用示例路径与文件](https://raw.githubusercontent.com/Sorasukiawa/shiguang/64ca6e5971d1245c2da1a4a3040bed1c13d0fee5/file-copy-v0.2.0-demo.png)

*界面流程演示；示例路径与文件。*

<details><summary>详细发布记录（四语言）</summary>

[简体中文](#简体中文) | [繁體中文](#繁體中文) | [English](#english) | [日本語](#日本語)

## 简体中文

拾光 v0.2.0 是一次面向日常素材流转的大版本更新。除了原有的相机卡拷卡流程，现在可以直接拷贝任意文件和文件夹，也可以把已有素材导入指定项目；这一整套新流程继续遵循“不覆盖已有文件、先检查再写入、结果可恢复”的原则。

### 新增：文件拷贝与项目素材导入

- 新增独立的「文件拷贝」页面，可选择或从 Finder 拖入文件、文件夹，并同时写入一个或多个目的地。
- 新增项目素材导入：可从项目卡片、项目详情页或导入弹层加入素材，并按照片、视频、音频、工程文件等类别映射到项目目录。
- 文件夹会保留原有层级、隐藏文件与空目录；开始前会展示来源明细、文件数、总大小、目标可用空间和校验方式。
- 支持不校验、快速校验和完整校验。完整校验会回读每份副本，并用 XXH64 与拷贝时计算的源文件哈希比对。
- 传输任务在页面切换后仍会持续显示，可查看进度、失败文件、打开目标目录，并只重试尚未完成的文件或副本。

### 更可靠的写入与恢复

- 写入前拒绝来源与目的地重叠、目的地互相包含，以及同一存储卷合计空间不足等危险配置。
- 同名文件不会被覆盖；文件和目录使用适合目标文件系统的安全发布流程，异常半成品不会伪装成完成结果。
- 传输收据与项目记录支持跨进程恢复。遇到进程退出、数据库暂时写入失败或发布后未完成记录提交时，可沿最近一次任务继续，避免重复拷贝已完成副本。
- 双目标任务彼此隔离：一个目标失败或掉线时，另一个目标可继续完成；重试只补齐失败目标，并重新确认目标身份和空间。
- 加强 APFS 目标身份保护。目标卷在任务期间被卸载或替换时会失败关闭，避免把素材误写到原挂载点背后的本机目录。
- 补齐磁盘写满、目录发布中断、遗留临时作用域和强退后的恢复处理；未知或无法确认归属的内容会保留并明确报错。

### 界面与交互

- 文件拷贝与项目导入使用新的灰色卡片布局、来源清单、目标区和任务状态反馈，并补齐简体中文、繁體中文、English、日本語四种语言。
- Finder 拖放会按实际落点进入项目卡片、项目详情或文件拷贝页；项目卡片之间的空隙不会误触发导入。
- 修复全 App 分段选择器、开关和步骤条在长距离切换时的动画过冲；从「不校验」直接切到「完整校验」时，滑块会始终停留在轨道内。
- 加载失败、文件选择延迟返回、快速连续点击、项目切换和重试等状态增加了明确反馈与重复提交保护。

### 升级与范围

仅提供 Apple Silicon macOS 版本。公开 v0.1.19 用户可在设置中检查更新；更新不会在拷卡、文件拷贝或归档任务进行时安装。升级前请结束重要任务，并保留原卡和另一份可靠备份。

本版继续使用 ad-hoc 签名，尚无 Apple Developer ID 签名或 Apple 公证。macOS 首次打开时可能需要在「系统设置 → 隐私与安全性」中选择「仍要打开」。本轮验证包含合成文件、隔离数据库、Finder 原生拖放和 APFS 镜像强制掉线；不等同于所有实体 USB 设备、NAS 断连或第三方同步服务均已验证。

## 繁體中文

拾光 v0.2.0 是一次面向日常素材流轉的大版本更新。除了原有的記憶卡轉存流程，現在可以直接複製任意檔案與資料夾，也可以把既有素材匯入指定專案；整套新流程延續「不覆寫既有檔案、先檢查再寫入、結果可復原」的原則。

### 新增：檔案複製與專案素材匯入

- 新增獨立的「檔案拷貝」頁面，可選擇或從 Finder 拖入檔案、資料夾，並同時寫入一個或多個目的地。
- 新增專案素材匯入：可從專案卡片、專案詳情或匯入視窗加入素材，並依照片、影片、音訊、工程檔案等類別對應到專案目錄。
- 資料夾會保留原有層級、隱藏檔案與空目錄；開始前會顯示來源明細、檔案數、總大小、目的地可用空間和驗證方式。
- 支援不驗證、快速驗證與完整驗證。完整驗證會重新讀取每份副本，並以 XXH64 與複製時算出的來源雜湊比對。
- 切換頁面後仍可查看傳輸工作、進度與失敗檔案，也可開啟目標目錄，並只重試尚未完成的檔案或副本。

### 更可靠的寫入與復原

- 寫入前拒絕來源與目的地重疊、目的地彼此包含，以及同一儲存卷合計空間不足等危險設定。
- 不會覆寫同名檔案；檔案與目錄會依目標檔案系統使用安全發布流程，異常半成品不會被標示為完成。
- 傳輸收據與專案記錄支援跨程序復原。程序退出、資料庫暫時無法寫入，或發布後尚未完成記錄提交時，可沿最近一次工作繼續，避免再次複製已完成副本。
- 雙目的地工作彼此隔離：一個目的地失敗或離線時，另一個仍可完成；重試只補齊失敗目的地，並重新確認目的地身分與空間。
- 加強 APFS 目的地身分保護。目的卷在工作期間卸載或被替換時會安全失敗，避免素材誤寫到原掛載點背後的本機目錄。
- 補齊磁碟寫滿、目錄發布中斷、遺留暫存作用域和強制結束後的復原；無法確認歸屬的內容會保留並清楚報錯。

### 介面與互動

- 檔案複製與專案匯入採用新的灰色卡片版面、來源清單、目的地區和工作狀態回饋，並提供简体中文、繁體中文、English、日本語。
- Finder 拖放會依實際落點進入專案卡片、專案詳情或檔案拷貝頁；專案卡片之間的空隙不會誤觸匯入。
- 修正全 App 分段選擇器、開關與步驟列長距離切換時的動畫過衝；從「不校驗」直接切到「完整校驗」時，滑塊會保持在軌道內。
- 載入失敗、檔案選擇延遲回傳、快速連續點擊、專案切換與重試等狀態，新增明確回饋及重複提交保護。

### 升級與範圍

僅提供 Apple Silicon macOS 版本。公開 v0.1.19 使用者可在設定中檢查更新；轉存、檔案複製或封存工作執行時不會安裝更新。升級前請結束重要工作，並保留原卡與另一份可靠備份。

本版繼續採用 ad-hoc 簽署，尚無 Apple Developer ID 簽署或 Apple 公證。macOS 首次開啟時，可能需要在「系統設定 → 隱私權與安全性」中選擇「強制打開」。本輪驗證包含合成檔案、隔離資料庫、Finder 原生拖放與 APFS 映像強制離線；不代表所有實體 USB 裝置、NAS 斷線或第三方同步服務均已驗證。

## English

Shiguang v0.2.0 is a major update for everyday media movement. In addition to the existing camera-card offload workflow, you can now copy arbitrary files and folders or import existing media into a project. The new workflows retain Shiguang's core rules: never overwrite an existing file, validate the plan before writing, and preserve enough state to recover safely.

### New: file copy and project media import

- A new **File Copy** page accepts files and folders selected in the app or dropped from Finder, then copies them to one or more destinations.
- Project media import is available from project cards, project details, and the import dialog. Photos, video, audio, project files, and other categories can be mapped to project folders.
- Folder hierarchy, hidden files, and empty directories are preserved. Before starting, Shiguang shows source details, file count, total size, destination capacity, and the selected verification mode.
- Choose no verification, quick verification, or full verification. Full verification rereads every copy and compares its XXH64 value with the source hash calculated during copying.
- Transfers remain visible while you move between pages. You can inspect progress and failed files, open the destination, and retry only unfinished files or copies.

### Safer writes and recovery

- Preflight checks reject overlapping sources and destinations, nested destinations, and insufficient combined space when several destinations share a volume.
- Existing files are never overwritten. Files and directories use a publication strategy suited to the destination file system, and interrupted partial output is never reported as complete.
- Transfer receipts and project records support recovery across process restarts. If the app exits, the database is temporarily unwritable, or publication finishes before its receipt is committed, recovery continues from the latest task without recopying completed destinations.
- Destinations fail independently. If one destination disconnects or fails, another can finish; retry fills only the missing destination after rechecking its identity and capacity.
- APFS destination identity checks now stay bound to the opened destination root. If a volume is detached or replaced during a transfer, the task fails closed instead of writing into the local directory behind the former mount point.
- Recovery now covers a full disk, interrupted directory publication, owned temporary scopes, and forced process exit. Unknown or unowned remnants are preserved and reported rather than removed.

### Interface and interaction

- File copy and project import use a new card layout with clearer source lists, destinations, action areas, and task feedback, localized in Simplified Chinese, Traditional Chinese, English, and Japanese.
- Finder drops follow the actual target: a project card, project details, or the File Copy page. Gaps between project cards remain neutral and do not open an import by accident.
- Fixed overshooting motion across segmented controls, switches, and the ingest step indicator. Jumping directly from **No verification** to **Full verification** keeps the slider inside its track.
- Loading failures, delayed picker responses, rapid repeated actions, project changes, and retries now provide clearer feedback and stronger duplicate-submission guards.

### Upgrade and support scope

Apple Silicon macOS only. Public v0.1.19 users can check for updates in Settings. Shiguang will not install an update while an offload, file copy, or archive is running. Finish important jobs and keep the original card plus another reliable backup before upgrading.

This build remains ad-hoc signed and is not signed with an Apple Developer ID or notarized by Apple. On first launch, macOS may require **System Settings → Privacy & Security → Open Anyway**. Validation for this release includes synthetic files, isolated databases, native Finder drag and drop, and forced disconnection of APFS disk images. It does not establish compatibility with every physical USB device, NAS failure mode, or third-party sync service.

## 日本語

拾光 v0.2.0 は、日常的な素材移動のための大型アップデートです。従来のメモリーカード取り込みに加え、任意のファイルやフォルダーのコピー、既存素材のプロジェクトへの取り込みに対応しました。新しい処理も「既存ファイルを上書きしない」「書き込み前に計画を確認する」「安全に復旧できる状態を残す」という原則に従います。

### 新機能：ファイルコピーとプロジェクト素材の取り込み

- 新しい「ファイルコピー」画面で、App から選択した項目や Finder からドロップしたファイル／フォルダーを、1つ以上の保存先へコピーできます。
- プロジェクトカード、プロジェクト詳細、取り込みダイアログから既存素材を追加できます。写真、動画、音声、プロジェクトファイルなどの分類をプロジェクト内フォルダーへ割り当てられます。
- フォルダー階層、隠しファイル、空フォルダーを保持します。開始前に、入力元の明細、ファイル数、合計サイズ、保存先の空き容量、検証方式を確認できます。
- 検証なし、高速検証、完全検証に対応。完全検証では各コピーを読み直し、コピー時に計算した元ファイルの XXH64 と比較します。
- 画面を移動しても転送タスクと進捗を確認できます。失敗したファイルの確認、保存先を開く操作、未完了のファイルやコピーだけの再試行が可能です。

### 書き込みと復旧の強化

- 入力元と保存先の重複、保存先同士の包含、同一ボリューム上の複数保存先を合計した空き容量不足を、書き込み前に拒否します。
- 既存の同名ファイルは上書きしません。ファイルとフォルダーは保存先のファイルシステムに適した安全な公開処理を使い、中断した一時出力を完了として扱いません。
- 転送レシートとプロジェクト記録はプロセス再起動後も復旧できます。App の終了、データベースの一時的な書き込み失敗、公開完了後のレシート未確定が起きても、完了済みの保存先を再コピーせず、直近タスクから続行できます。
- 複数の保存先は独立して失敗します。1つが切断または失敗しても別の保存先は完了でき、再試行では身元と空き容量を再確認したうえで不足分だけを補います。
- APFS 保存先の身元確認を、開いた保存先ルートへ固定しました。転送中にボリュームが取り外されたり置き換わったりした場合、元のマウントポイント背後にあるローカルフォルダーへ誤って書き込まず、安全に失敗します。
- 容量不足、フォルダー公開の中断、所有済み一時領域、強制終了後の復旧を強化。所有者を確認できない残留物は削除せず、保持してエラーを表示します。

### 画面と操作

- ファイルコピーとプロジェクト取り込みに、新しいカードレイアウト、入力元一覧、保存先、操作領域、タスク表示を追加。簡体字中国語、繁体字中国語、英語、日本語に対応しています。
- Finder からのドロップは、実際の位置に応じてプロジェクトカード、プロジェクト詳細、ファイルコピー画面へ入ります。カード間の隙間では誤って取り込みを開始しません。
- App 全体のセグメント選択、スイッチ、取り込みステップ表示で発生していた行き過ぎるアニメーションを修正。「検証なし」から「完全検証」へ直接切り替えても、スライダーが枠内に収まります。
- 読み込み失敗、ファイル選択の遅延応答、素早い連続操作、プロジェクト切り替え、再試行時の表示と重複実行防止を改善しました。

### 更新方法と対応範囲

Apple Silicon macOS 専用です。公開版 v0.1.19 は設定から更新を確認できます。取り込み、ファイルコピー、アーカイブの実行中には更新をインストールしません。重要な処理を終え、元のカードと別の信頼できるバックアップを保管してから更新してください。

このビルドは引き続き ad-hoc 署名で、Apple Developer ID 署名および Apple 公証はありません。初回起動時は **システム設定 → プライバシーとセキュリティ → そのまま開く** が必要な場合があります。本リリースでは、合成ファイル、分離データベース、Finder のネイティブドラッグ＆ドロップ、APFS ディスクイメージの強制切断を検証しています。すべての物理 USB 機器、NAS 障害、サードパーティ同期サービスへの対応を保証するものではありません。

</details>

---

**安装与文件：**本版仅提供 Apple Silicon macOS。DMG 用于手动安装；同页的 `Shiguang_aarch64.app.tar.gz`、`.sig` 和 `latest.json` 供应用内更新使用。本版为 ad-hoc 签名，未获 Apple Developer ID 签名或 Apple 公证。GitHub 自动生成的 Source code 归档只是公开资料，不含拾光 App 源码，也不是安装包。

重要素材请保留原始卡和另一份可靠备份，确认副本后再格式化。问题请提交至 [Issues](https://github.com/Sorasukiawa/shiguang/issues)，不要上传原始素材、客户资料或私密路径。
