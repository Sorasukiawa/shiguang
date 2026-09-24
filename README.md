[简体中文](./README.md) · [繁體中文](./README.zh-TW.md) · [English](./README.en.md) · [日本語](./README.ja.md)

<p align="center"><img src="./shiguang-icon.png" width="96" height="96" alt="拾光 App 图标"></p>
<h1 align="center">拾光 Shiguang</h1>
<p align="center"><strong>把拍摄素材，妥帖带回。</strong></p>
<p align="center">为摄影师与影像团队准备的 Mac 素材工作台：从相机卡、文件与文件夹收取素材，写入多个目的地，校验副本，留下可查阅的项目与任务报告。</p>
<p align="center"><a href="https://github.com/Sorasukiawa/shiguang/releases/download/v0.2.1/Shiguang_0.2.1_aarch64.dmg"><strong>下载 v0.2.1 · Apple Silicon Mac</strong></a> · <a href="https://getshiguang.pages.dev/guides/">使用指南</a> · <a href="https://github.com/Sorasukiawa/shiguang/releases/tag/v0.2.1">本次更新</a></p>
<p align="center">免费内测 · 简体中文 / 繁體中文 / English / 日本語 · 浅色与深色主题</p>

![拾光项目工作台，展示合成的摄影项目与备份状态；深色主题](./projects-v0.2.1-dark.png)

*示例项目与数据；画面由拾光界面在隔离浏览器环境渲染，不代表原生文件操作验收。*

## 一条清楚的素材工作流

| 从哪里开始 | 拾光会做什么 | 最后可确认什么 |
| --- | --- | --- |
| **相机卡拷卡** | 识别照片、视频和音频，按项目、拍摄日与机位整理；一次读取来源，同时写入工作盘和第二备份盘 | 每个目标的拷贝与校验结果、卡片记录及补拷状态 |
| **文件与文件夹拷贝** | 从 Finder 拖入或选择来源，保留目录层级，写入一个或多个目的地 | 来源清单、空间预检、传输结果与失败副本的重试入口 |
| **项目素材导入** | 把已有素材加入指定项目，按照片、视频、音频、工程文件等类别映射目录 | 导入位置、项目记录与任务结果 |
| **项目归档** | 将项目归档到本地或网络目标，保留原项目记录；归档不会自动删除本地素材 | 归档任务、可得的校验结果与报告 |

拾光坚持**不覆盖已有文件**。多目标任务分别记录结果；中断或目标掉线后，先重新确认目标身份和空间，再补齐未完成的副本。

### 文件拷贝

![拾光文件拷贝界面演示：来源、目的地与校验选项](./file-copy-v0.2.0-demo.png)

*v0.2.0 起提供的界面流程演示，路径与文件均为示例。*

### 任务报告

任务结果可按项目、日期、类型与状态查找，并导出离线 HTML 或多页 PDF。旧记录缺失的字段会标为“未记录”，不会推定成功。

<img src="./report-v0.2.1-synthetic.png" width="480" alt="拾光 v0.2.1 PDF 任务报告示例，使用合成数据并展示中断与失败状态">

*v0.2.1 报告示例；全部内容为合成数据。*

## 开始使用

1. 在上方下载 **Apple Silicon Mac** 版 DMG；Intel Mac 与 Windows 暂无公开安装包。可在 ** → 关于本机** 查看芯片。
2. 打开 DMG，将“拾光”拖入“应用程序”。若首次启动被 macOS 拦截，前往 **系统设置 → 隐私与安全性**，核对应用后选择“仍要打开”。无需关闭 Gatekeeper。
3. 添加来源、项目和目标盘，检查空间与校验方式后再开始。重要素材请保留原卡及另一份可靠备份，确认副本后再格式化卡片。

当前为 **免费内测版**，采用 ad-hoc 签名，尚无 Apple Developer ID 签名或 Apple 公证。请只从[本仓库 Releases](https://github.com/Sorasukiawa/shiguang/releases)下载。正在运行的拷卡、文件拷贝或归档任务会阻止更新安装。

## 当前版本 · v0.2.1

- 快速校验完整回读每份目标文件并比较 XXH64；完整校验还会独立重读来源。设备无法绕开系统缓存时，结果会如实标明。
- 拷卡、文件拷贝、项目导入及归档任务可筛选、查阅与导出报告；中断记录不再显示成成功。
- 等待慢速存储设备预检时，其他页面不再被共用数据库连接占住。

[阅读完整发布说明](https://github.com/Sorasukiawa/shiguang/releases/tag/v0.2.1) · [浏览所有版本](./VERSIONS.md)

<details>
<summary>校验、存储盘与网络目录</summary>

- **不校验**只依据写入过程是否报错，不适合重要素材。**快速校验**重读每份目标文件，计算 XXH64 与写入时的来源哈希比对。**完整校验**再独立重读全部来源文件。XXH64 用于检测内容差异，不是加密签名；通过后仍应人工抽查关键素材。
- 工作盘、第二备份盘和归档目标推荐 APFS。ExFAT 可作为目标盘，但必须先通过拾光的安全能力检查；无法证明安全时会在写入前拒绝。ExFAT 相机卡可作为只读来源。拾光不会要求格式化已有介质。
- 素材扫描、拷贝、校验和项目记录默认在本机完成，不会上传到拾光服务器。若选择 NAS 或第三方同步文件夹，后续网络传输或同步由对应系统与服务处理。网络盘断连和同步服务的行为仍需按实际环境核对。

</details>

## 帮助与反馈

[官网](https://getshiguang.pages.dev/) · [使用指南](https://getshiguang.pages.dev/guides/) · [提交问题或建议](https://github.com/Sorasukiawa/shiguang/issues)

反馈时请提供版本、macOS 与芯片型号、来源和目标格式、复现步骤及错误文字；截图请遮挡项目名和路径，**不要上传原始素材或客户资料**。

本仓库用于发布安装包、说明、版本记录与反馈。**仓库不包含拾光 App 源代码，未提供开源许可证或再分发授权。** GitHub 自动生成的 Source code 压缩包只是本仓库公开资料，不能安装为拾光。
