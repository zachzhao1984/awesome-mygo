<div align="center">

# Awesome MyGo

**用 [MyGo](https://github.com/egoist/mygo) 框架开发的跨平台桌面应用大全**

[English](README.md) · 简体中文

MyGo 是 [egoist](https://github.com/egoist) 出品的纯 Go 桌面应用框架：同一扇窗口可以挂系统
WebView 页面（WKWebView / WebView2 / WebKitGTK），也可以完全由 Go 代码在 GPU 上自绘原生 UI。
没有 Electron、没有 cgo，产物是一个几兆到几十兆的单二进制；一条命令产出 macOS 应用包、
Windows 安装器与 Linux 包，支持签名、公证与差量自动更新。

**229 个项目** · **209 个桌面应用**（其中 **75 个**提供三端构建） · **20 个组件库与模板**

_数据抓取于 2026-10-26；226 个开源条目均已核验 `go.mod` 实际依赖 `github.com/egoist/mygo`，另附闭源应用取自官网。_

</div>

## 目录

- [快速上手](#快速上手)
- [作者的开源应用](#作者的开源应用)
- [作者的闭源应用](#作者的闭源应用)
- [桌面应用](#桌面应用)
  - [🖋 编辑器 · 笔记 · 写作](#编辑器-笔记-写作)
  - [🤖 AI · Agent · LLM 客户端](#ai-agent-llm-客户端)
  - [🛠 开发者工具](#开发者工具)
  - [🌐 网络 · 代理 · 远程](#网络-代理-远程)
  - [🗂 存储 · 文件 · 同步](#存储-文件-同步)
  - [🎵 媒体 · 播放器 · 下载](#媒体-播放器-下载)
  - [⚡ 效率 · 菜单栏 · 启动器](#效率-菜单栏-启动器)
  - [📊 系统 · 监控 · 硬件](#系统-监控-硬件)
  - [🎮 游戏 · 娱乐 · 其他](#游戏-娱乐-其他)
- [组件库 · 模板 · 框架周边](#组件库-模板-框架周边)
- [图例](#图例)
- [贡献指南](#贡献指南)

## 快速上手

带 Web 前端的 MyGo 应用（需要 Go 1.27.3+ 与 Bun）：

```sh
bunx mygo-cli init my-app      # 或 npx mygo-cli init my-app
cd my-app
bun run dev
```

纯 Go 原生 UI 应用只需要 Go：

```sh
go run github.com/egoist/mygo/cmd/mygo@latest init -template native my-app
cd my-app
go tool mygo dev
```

完整文档见 [egoist/mygo/docs](https://github.com/egoist/mygo/blob/main/docs/README.md)，官网 [mygo.egoist.dev](https://mygo.egoist.dev)。

## 作者的开源应用

> 框架作者自己的 MyGo 应用，全部开源，且均已核验依赖 `github.com/egoist/mygo`。

- [egoist/kero](https://github.com/egoist/kero) — 面向编码 Agent 的原生终端：会话跑在 `kerod` 守护进程里，关掉窗口仍在继续；侧栏标出哪个会话在等你，⌘J 直达；`kero new / split / send / wait / read` 让 Agent 自己开分屏、递任务、读屏幕；libghostty 渲染，支持 SSH / Tailscale / WSL 远程主机。 🍎 🪟 🐧 `1219★` · MIT [官网](https://kero.sh/)
- [egoist/gorex](https://github.com/egoist/gorex) — Rex 终端的 MyGo 原生 UI 复刻。 🍎 🪟 🐧 `143★`
- [egoist/godiff](https://github.com/egoist/godiff) — 轻快原生的 Git diff 查看器。 🍎 🪟 🐧 `123★`
- [egoist/mygo-cloudmusic](https://github.com/egoist/mygo-cloudmusic) — 原生界面的第三方网易云音乐客户端，无 WebView：扫码登录、每日推荐、私人 FM 与心动模式、逐字歌词与「律动」视图；支持无损 / Hi-Res 边下边播、本地缓存、刘海迷你播放器、音量均衡与淡入淡出，深浅色跟随系统。 🍎 🪟 🐧 · AGPL-3.0 [官网](https://music.egoist.dev/)
- [egoist/2048](https://github.com/egoist/2048) — 经典 2048 的 MyGo 原生桌面版。 ❓ [官网](https://2048.egoist.dev)

## 作者的闭源应用

> 框架作者自己的闭源免费应用，同样用 MyGo 写成；信息来自官网，无法用 go.mod 核验。

- [Pulse](https://pulse.egoist.dev/) — [@egoist](https://github.com/egoist)（闭源 · 免费 · Apple Silicon Mac）。「你的电脑正在做什么，一窗看尽」：CPU 逐核负载、内存压力、GPU 引擎、磁盘与网络流量、电池与温度，每个进程带图标、可查父子关系与历史，菜单栏速览各项指标。官网注明 Built with MyGo，纯 GPU 自绘、无 WebView。 🍎 🪟 🐧

## 桌面应用

应用按用途分类；同一分类内先按 star 数、再按名称排序。标记 🕸 的条目明确使用了 MyGo 的 WebView 模式（Go 后端 + Web 前端），未标记的条目大多为纯 Go 原生 UI。

## 🖋 编辑器 · 笔记 · 写作

- [sorrycc/Mayoi](https://github.com/sorrycc/Mayoi) — 小而快的代码编辑器，界面完全由 Go 在 GPU 上绘制，无 WebView、无 Electron，打包后约 18 MB，含 Vim 模式。 🍎 🪟 🐧 `256★` · MIT
- [mu-zi-lee/Tangentry](https://github.com/mu-zi-lee/Tangentry) — 沿着好奇心继续发现——本地优先的多平台内容聚合、阅读与笔记工具。 🍎 🪟 `146★` · MIT
- [godwit-email/godwit](https://github.com/godwit-email/godwit) — 开源、可随意拆解改造的 AI 邮件客户端。 🍎 🪟 🐧 · Apache-2.0 [官网](https://godwit.email)
- [oneo-me/locus](https://github.com/oneo-me/locus) — 本地优先的 Markdown 笔记本：笔记就是普通文件，支持 HTML 画布与只读 MCP。 🍎 🪟 🐧 🕸 · MIT [官网](https://oneo-me.github.io/locus/)
- [kiwiflydream/yunji-uml](https://github.com/kiwiflydream/yunji-uml) — PlantUML / Mermaid / Flowchart.js 的原生 macOS 编辑器。 🍎 🪟 🐧 · MIT
- [sorrycc/Deckle](https://github.com/sorrycc/Deckle) — 快速原生的 macOS Markdown 编辑器。 🍎 🪟 🐧 · MIT
- [RSK21X/GoRss](https://github.com/RSK21X/GoRss) — Apple Silicon Mac 上的原生 RSS / Atom 阅读器，MyGo + Onevra。 🍎
- [alvyn16/GOsidian](https://github.com/alvyn16/GOsidian) — 高性能、本地优先的 Obsidian 复刻。 🪟 · MIT
- [logdns/imyemail-cloud](https://github.com/logdns/imyemail-cloud) — 开源邮件套件的桌面端：平台原生客户端与 Pulse 风格的 Go/MyGo 桌面版。 🍎 🪟 🐧 · MIT [官网](https://imy.email)
- [everpcpc/mica](https://github.com/everpcpc/mica) — 专注的 macOS 原生 Gmail 客户端。 🍎
- [xinde/Mote](https://github.com/xinde/Mote) — macOS 菜单栏工具：随手写 Markdown，也随手开一段专注计时。 🍎
- [LZD121/my-gotion](https://github.com/LZD121/my-gotion) — 纯本地优先的 Notion 克隆：块级文档 + 多维表格，JSON 文件是唯一数据源，WebDAV / GitHub 增量同步。 🍎 🪟 🐧 · MIT
- [yangflow/oriel](https://github.com/yangflow/oriel) — RSS / RSSHub 个人混合时间线阅读器：纯 Go 原生 UI，桌面应用与无头服务端是同一个程序。 🍎 🪟 🐧 · MIT


## 🤖 AI · Agent · LLM 客户端

- [Licoy/Quosparr](https://github.com/Licoy/Quosparr) — 菜单栏 / 托盘额度管家，统一查看 Codex、Claude Code、Grok 的额度、重置、API 等价成本与本机会话，支持多账号与中转切换。 🍎 🪟 🐧 `300★` · AGPL-3.0 [官网](https://quosparr.com)
- [AstraFoundry/Arion](https://github.com/AstraFoundry/Arion) — 本地优先的语音听写与拼音输入法：按住说话（macOS 右 ⌥ / Windows 右 Alt）在任意编辑器里说中英混说，识别、拼音打字、纠错学习与上下文润色全部在本机完成；Qwen3-ASR 1.7B 本地推理（macOS 走 MLX，Windows 走 speech.cpp），可选两阶段润色按当前应用与光标上下文调整措辞；自带系统输入法宿主（macOS ArionInput.app / Windows ArionTSF.dll），菜单栏常驻，草稿只在松键时提交，零知识同步与签名自动更新。 🍎 🪟 `51★` · AGPL-3.0 [官网](https://arion.astrafoundry.si)
- [hehehai/AudioSmith](https://github.com/hehehai/AudioSmith) — Mac 上的语音、配音、有声书、朗读与转写工作台，免费开源。 🍎 `47★` · AGPL-3.0 [官网](https://actnow.dev/audiosmith)
- [lbr77/lody-mygo](https://github.com/lbr77/lody-mygo) — Lody 的原生桌面客户端：界面由 MyGo 的 `ui` 包直接画在 GPU 上，无 WebView；浏览器设备流登录（凭据存 macOS 钥匙串），会话按机器与项目分组并带工作/等待/未读标记，支持置顶、归档与分叉；会话内是流式 Markdown、代码高亮、数学公式与 Mermaid，工具调用、思考、计划、diff 与子 Agent 一应俱全，`@` 引用文件与 issue、`$` 技能、`/` 快捷指令，另有定时任务，以及来自本机 Lody daemon 的终端、文件浏览器与 Git 工作树；可切换「仅连接本机」离线使用，中英文界面。 🍎 · AGPL-3.0
- [kkkk2323/droi](https://github.com/kkkk2323/droi) — Factory Droid 的原生 Mac / Windows / iPhone 应用：所有 droid 会话收进一个窗口，也能带在手机上。 🍎 🪟 · MIT
- [nerv-base/mytoken](https://github.com/nerv-base/mytoken) — 本地 token 与成本账本：统计 Claude Code、Codex、Gemini CLI、opencode、Cline 等的花名册。 🍎 🪟 🐧 · MIT
- [enowx/enowx](https://github.com/enowx/enowx) — 让 Claude Code、Codex 等 40+ 编码 Agent 各占一个 git worktree 并行跑，在一个原生应用里观察、对比、合并，无云端无账号。 🍎 🪟 🐧 · MIT
- [sorrycc/CCGuanjia](https://github.com/sorrycc/CCGuanjia) — 照看 Claude Code 的 Mac 应用：账号 Profile、安装、用量与清理。 🍎 · MIT
- [oysterhyd/AgentMeter](https://github.com/oysterhyd/AgentMeter) — Windows 桌面的 Codex 额度、token 用量、成本与运行时指标监视器。 🪟
- [yeshan333/tingsub](https://github.com/yeshan333/tingsub) — 浏览器音频的本地双语实时字幕（英/日），Apple Silicon + MLX，附 Chrome 扩展。 🍎 · MIT [官网](https://shansan.top/tingsub/)
- [tk103331/ChatGo](https://github.com/tk103331/ChatGo) — 面向学习的简单 AI 聊天客户端：多模型、Agent、工具、MCP、ACP 与内置终端。 🍎 🪟 🐧 · MIT
- [horizon0514/ds-search](https://github.com/horizon0514/ds-search) — macOS 菜单栏极简搜索，基于 DeepSeek Search API，MyGo 原生界面。 🍎 · MIT
- [YuanZhe-99/Kyokai](https://github.com/YuanZhe-99/Kyokai) — 跨设备的 AI Computer Use：P2P 连接、人工直接操控与主机侧 AI 执行合为一体。 🍎 🪟 · AGPL-3.0
- [bunnywaffle/llama-manager](https://github.com/bunnywaffle/llama-manager) — llama.cpp 桌面管理器：下载、更新、运行后端与 .gguf 模型，分支聊天与多模型路由。 🪟 🐧
- [HycJack/mygo-agent](https://github.com/HycJack/mygo-agent) — Codex 风格的桌面 AI 编码 Agent：原生 GPU UI、内置 Agent 循环、Skills 与 MCP。 🍎 🪟 🐧
- [yaffalhakim1/opencode-gui](https://github.com/yaffalhakim1/opencode-gui) — OpenCode 的原生桌面 GUI，附 WebSocket 守护进程，可经 Tailscale 用手机访问。 🪟
- [minifish-org/pith-desk](https://github.com/minifish-org/pith-desk) — Pith 驱动的轻量本地桌面 Agent：工作区工具、MCP 连接与 TypeScript 接口。 🍎 🐧 · AGPL-3.0
- [Beeta/voxi](https://github.com/Beeta/voxi) — 会议录音转写与摘要应用，MyGo 原生 UI。 🍎 · MIT
- [hoanglong2311/AI-limit](https://github.com/hoanglong2311/AI-limit) — 查看 AI 订阅用量的 macOS 菜单栏应用。 🍎
- [ixxxxoooo/ai-usage](https://github.com/ixxxxoooo/ai-usage) — macOS 菜单栏 AI 账单助手：查看 Cursor 请求用量与 DeepSeek 余额，凭据进钥匙串。 🍎 · MIT
- [gvenusleo/Atlas](https://github.com/gvenusleo/Atlas) — 用 Go 构建的通用 Agent。 🍎 🪟 🐧 · MIT
- [hehehai/Auralink](https://github.com/hehehai/Auralink) — 基于远端模型的 macOS 语音输入：在任何应用里说话，文字直接落在光标处，支持转写、翻译与改写。 🍎 · AGPL-3.0 [官网](https://actnow.dev/auralink)
- [lexleizou/byop](https://github.com/lexleizou/byop) — 通过 JSONL RPC 调用外部 Pi CLI 的多插件原生工作台（Build You Own Pi）。 🍎 · MIT
- [foyoodo/Cove](https://github.com/foyoodo/Cove) — macOS 原生聊天客户端：界面用 MyGo 的 `ui` 包绘制，对接 OpenAI 兼容 Chat Completions。 🍎
- [xinde/deepseek-harness-mygo](https://github.com/xinde/deepseek-harness-mygo) — 本地 DeepSeek Harness 代码库的轻量 MyGo 桌面启动器。 🍎 🕸 · MIT
- [meimingqi222/devin-usage-metrics](https://github.com/meimingqi222/devin-usage-metrics) — Devin 用量与成本指标看板桌面版。 🍎 🪟
- [M2tHane/Distill](https://github.com/M2tHane/Distill) — 把本地编码 Agent 会话（Claude Code、Codex、Pi）蒸馏成 Skills、Rules 与 AGENTS.md / CLAUDE.md。 🍎
- [Maidang1/herdr-ui](https://github.com/Maidang1/herdr-ui) — Herdr 原生桌面客户端：工作区、工作树、Agent 状态与内置终端，支持标签、分屏与 prefix 模式。 🍎
- [ArnoChenFx/kura](https://github.com/ArnoChenFx/kura) — 桌面 Skills 管理器：在一处浏览、检查与安装 Agent Skills。 🍎 🪟 🐧
- [Helix-lyh/leeway](https://github.com/Helix-lyh/leeway) — AI 编程服务商的用量 / 额度 / 重置时间探测工具。 🍎 🪟 🐧 · MIT
- [dhx007/mygo-dsh](https://github.com/dhx007/mygo-dsh) — 初代 DeepSeek Harness 的复刻：会话、轨迹、四种模式、工具审批、PTC，纯 Go 自绘无 WebView。 ❓ · MIT
- [pararchy/para-term](https://github.com/pararchy/para-term) — 在 GPU 原生窗口里用真实伪终端跑 Para CLI 的个人终端。 🪟
- [Clearzero22/pi-web-desktop](https://github.com/Clearzero22/pi-web-desktop) — Pi Web Desktop：MyGo 只做窗口 / 菜单 / 生命周期外壳，内部自带 Node 拉起 pi-web 侧车。 🪟 🕸
- [javatoai/repodock](https://github.com/javatoai/repodock) — Codex 用的 GitHub 项目启动器：一键把仓库开成原生窗口。 🍎 🪟 · MIT
- [Riablo/skills-hub](https://github.com/Riablo/skills-hub) — 统一管理 Agent Skills 的桌面应用，支持全局 / 按项目、本地 / SSH 安装。 🍎
- [songlairui/skills-reader](https://github.com/songlairui/skills-reader) — 阅读 `~/.agents/skills` 里 Agent Skills 的 MyGo 桌面浏览器：分组、排版、基于锁文件的更新检查。 🍎 🐧 🕸
- [zackzhou-work/spark-go](https://github.com/zackzhou-work/spark-go) — 实时显示 Claude Desktop「Code」标签页中各会话状态的小窗。 🍎 · MIT
- [nggalek-co/titen](https://github.com/nggalek-co/titen) — macOS / Windows 原生会议转写：MyGo GPU 控件 + 平台原生音频采集。 🍎 🪟
- [tviber/voice-morph](https://github.com/tviber/voice-morph) — MorphVOX Pro 风格的实时变声工坊：Go DSP 引擎 + Web 前端 + MyGo 桌面壳。 🍎 🪟 🐧
- [xxww0098/xbs](https://github.com/xxww0098/xbs) — 跨平台批量图生图桌面工具，支持豆包与千问。 🍎 🪟 🐧 · MIT
- [ijry/YoYoCode](https://github.com/ijry/YoYoCode) — 多 Agent 协作编码工作台：聚合 Claude Code、Codex、OpenCode、Pi、Grok Build 等会话于一个原生窗口。 ❓
- [skeleton1231/zcode-my-go](https://github.com/skeleton1231/zcode-my-go) — 开源桌面编码 Agent：纯 Go 原生 UI，多模型提供方。 🪟 🐧 · MIT


## 🛠 开发者工具

- [hyoban/peek](https://github.com/hyoban/peek) — 原生 Git diff 查看器：Changes 模式并排看改动与历史，Files 模式读某个提交下的任意文件；改动按代码/测试/文档/锁文件分组并标记已读，语法高亮、单栏或并排、逐变更跳转；可选中行号复制引用或 GitHub 链接，从行号槽写评论并一键导出成发给 Agent 的提示词，Codex 评审结论直接标在对应行下；多仓库同窗口切换，并可用 GitHub CLI 切分支或检出 PR。 🍎 `55★` · MIT
- [Binaryify/MyGit](https://github.com/Binaryify/MyGit) — 轻量原生 Git 客户端，专注快速检查 AI Agent 对仓库做了哪些改动，三端可用。 🍎 🪟 🐧 · MIT [官网](https://binaryify.com/mygit/)
- [younland/apigo](https://github.com/younland/apigo) — 对标 Hoppscotch 的接口调试工具：无前端构建链、无 WebView，界面与逻辑全是 Go，单文件分发、完全离线。 🍎 🪟 🐧 · MIT
- [fachrihawari/omaterm](https://github.com/fachrihawari/omaterm) — Oh My Terminal——并排运行多个编码 Agent 的终端工作区。 🍎 🪟 🐧 · MIT [官网](https://fachrihawari.github.io/omaterm/)
- [saanuregh/dgopher](https://github.com/saanuregh/dgopher) — 快速原生数据库 GUI：PostgreSQL / MySQL / ClickHouse / SQLite / DuckDB 与 Redis，一个 Go 二进制，无 Electron。 🍎 🪟 🐧 · Apache-2.0
- [cainiao524/hd2-font-maker-go](https://github.com/cainiao524/hd2-font-maker-go) — 用自己的字体生成 Helldivers 2 字体替换 Mod 的 Windows 工具，内置 14 种界面语言。 🪟 · MIT
- [laojianzi/aster](https://github.com/laojianzi/aster) — 原生 Kubernetes 工作台，不依赖浏览器 UI 或内嵌 Dashboard。 🪟 · Apache-2.0
- [CarlOpenLab/Gloss](https://github.com/CarlOpenLab/Gloss) — 为「看 diff」而生的 Git 客户端：内联风险扫描、拓扑图、AI 提交信息，GPU 自绘、零 WebView。 🍎 🪟 🐧 · MIT [官网](https://carlopenlab.github.io/Gloss/)
- [preceeder/gui-redis](https://github.com/preceeder/gui-redis) — 带图形界面的 Redis 客户端，支持 macOS 与 Windows。 🍎 🪟
- [blyrin/java-ide](https://github.com/blyrin/java-ide) — MyGo 原生 UI 实现的 Java IDE：项目管理、编辑器、构建与运行一条龙。 ❓
- [hunghg255/mycode](https://github.com/hunghg255/mycode) — MyGo 写的编码工作区。 🍎 🪟 🐧 · MIT [官网](https://docs-mu-roan.vercel.app)
- [smallnest/nutty](https://github.com/smallnest/nutty) — macOS 原生终端：otty.sh 的 Go + MyGo 复刻，基于 uix 与 onevra 组件。 🍎 · Apache-2.0
- [tiramission/oci-sync](https://github.com/tiramission/oci-sync) — 把本地文件与目录同步到 OCI 兼容镜像仓库。 🍎 🪟 🐧 · MIT [官网](https://tiramission.github.io/oci-sync/)
- [oshell-desktop/oshell-desktop](https://github.com/oshell-desktop/oshell-desktop) — 共享 Go 内核 + 原生桌面 UI 的终端工作台。 🪟 🐧 · GPL-3.0
- [pteich/repo-hopper](https://github.com/pteich/repo-hopper) — 快速跳转并打开最近改动的 Git 仓库的原生小应用。 🍎 🪟 🐧 · MIT
- [javatoai/silverwing](https://github.com/javatoai/silverwing) — 小巧的原生多仓库研发工作台，无 WebView / Electron，安装包约 18 MB。 🍎 🪟 · MIT
- [version-fox/vfox-plus](https://github.com/version-fox/vfox-plus) — vfox 版本管理器的图形前端：Material 3 Expressive 设计语言，MyGo 原生 UI 自绘。 🐧 · Apache-2.0
- [tacshi/Yeek](https://github.com/tacshi/Yeek) — HTTP / GraphQL / gRPC / WebSocket 的原生跨平台 API 客户端，完全用 Go 写成。 🍎 🪟 · MIT
- [CairnPack/Codei18nDesktop](https://github.com/CairnPack/Codei18nDesktop) — Codei18n 的图形界面窗口。 🪟 · MIT
- [congthien2003/dbl](https://github.com/congthien2003/dbl) — SBDb：轻量原生数据库客户端，PostgreSQL 优先，运行时约 50 MB 内存。 🍎 🪟 🐧
- [my3rs/GoShell](https://github.com/my3rs/GoShell) — 轻量跨平台桌面 SSH 终端与主机管理工具。 🍎 🪟 🐧
- [zty012/guart](https://github.com/zty012/guart) — Go 串口工具：MyGo 原生 UI + MujicaUI，不用 WebView / HTML / JS，无需 CGO。 🪟 [官网](guart.2y.nz)
- [shenjing023/KLineChart-go](https://github.com/shenjing023/KLineChart-go) — 用 MyGo 原生 UI 画的迷你 K 线图，默认遵循 A 股约定（红涨绿跌、交易时段标签）。 ❓ · MIT
- [ftech-vn/kubedesk](https://github.com/ftech-vn/kubedesk) — 轻快的 Kubernetes 桌面客户端：实时资源、日志、shell，适合同时管多个集群。 🍎 · MIT [官网](https://kubedesk.cloud/)
- [zhengchalei/MQTT-Desktop](https://github.com/zhengchalei/MQTT-Desktop) — 轻量 MQTT 桌面客户端：多连接、3.1.1 / 5.0、订阅、发布与历史记录。 🪟
- [ca-x/nvflasher](https://github.com/ca-x/nvflasher) — 刷写与初始化 NVIDIA Jetson 设备的 MyGo 桌面应用（Linux 刷写后端）。 🐧 🕸 · MIT
- [nyakang/nyadb](https://github.com/nyakang/nyadb) — NyaDB：跨平台原生数据库工作台，管理连接并直接写 SQL。 🍎 🪟 🐧
- [flowprog/png2ico](https://github.com/flowprog/png2ico) — PNG 转 ICO 转换器，GUI 与 CLI 双版本，界面全部用 MyGo 原生写成。 🪟 · MIT
- [a8b7/Rubick](https://github.com/a8b7/Rubick) — 带 Web UI 的 Docker 容器管理平台。 🍎
- [bernylinville/seismic](https://github.com/bernylinville/seismic) — macOS 原生 Elasticsearch 客户端：elasticvue 的原生重写，13 个模块功能对等，纯 Go 自绘、无 cgo、无 WebView。 🍎
- [jinghaihan/sift](https://github.com/jinghaihan/sift) — 只审阅完整特性分支、过滤掉无关集成改动的评审工具。 🍎 🪟 🐧 · MIT
- [Moonvy/UPX-Installer-GO](https://github.com/Moonvy/UPX-Installer-GO) — Adobe UPX / CEP 扩展安装器，Windows / macOS 可用。 🍎 🪟 🐧
- [gantrol/YouRun](https://github.com/gantrol/YouRun) — 在一个桌面应用或 CLI 里统一管理本地项目命令。 🍎 🪟 🕸 · Apache-2.0 [官网](https://apps.microsoft.com/store/detail/9MWXXGC8H67D?cid=DevShareMCLPCS)


## 🌐 网络 · 代理 · 远程

- [AstraFoundry/KumoApp](https://github.com/AstraFoundry/KumoApp) — Mihomo (Clash.Meta) 内核的 macOS 客户端：Go + MyGo 外壳、React 界面，附带对 Agent 友好的 CLI。 🍎 🕸 `295★` · AGPL-3.0 [官网](https://usekumo.app)
- [lufficc/clash-traffic](https://github.com/lufficc/clash-traffic) — 看清 Clash Verge 的流量去向：按应用、站点、代理节点、订阅与设备聚合统计。 🍎 🪟 `42★`
- [Licoy/CPA-Bar](https://github.com/Licoy/CPA-Bar) — 在菜单栏随时掌握你的 CLIProxyAPI 服务状态。 🍎 🪟 🐧 · AGPL-3.0
- [xiaomai1011/GZIST-NetKeeper](https://github.com/xiaomai1011/GZIST-NetKeeper) — 校园网自动登录保活：适配新版 Dr.COM / eportal 接口，掉线重连、开机自启、后台常驻。 🍎 🪟 🐧 [官网](https://xiaomai1011.github.io/GZIST-NetKeeper/)
- [hygkui/v5vpn-rea-client](https://github.com/hygkui/v5vpn-rea-client) — LeadSec V5VPN SSL VPN 门户的非官方 Go + MyGo 客户端（协议 v2.0）。 🍎 🪟 🐧 · Apache-2.0
- [xiaomai1011/GZIST-DormSignin-Baiyun](https://github.com/xiaomai1011/GZIST-DormSignin-Baiyun) — 宿舍签到客户端，Go + MyGo，Windows x64。 🪟
- [marukolibro/Hop](https://github.com/marukolibro/Hop) — macOS 与 Windows 原生 mihomo (Clash.Meta) 代理客户端，无 WebView。 🍎 🪟 · GPL-3.0 [官网](https://marukolibro.github.io/Hop/)
- [si-mods/MyVNC](https://github.com/si-mods/MyVNC) — 从 TigerVNC 移植的纯 Go VNC 查看器。 🪟 · GPL-2.0
- [RedwindA/gotify-desktop](https://github.com/RedwindA/gotify-desktop) — 只收不发的 Gotify 桌面客户端，三端可用。 🍎 🪟 🐧 · GPL-3.0
- [xiaomai1011/GZIST-Hotspot](https://github.com/xiaomai1011/GZIST-Hotspot) — 校园网有线转热点：一键开关、自动防断网、网卡自适应。 🪟 · MIT
- [moxuun/sing-box-drover-go](https://github.com/moxuun/sing-box-drover-go) — sing-box 托盘控制器，sing-box-dover 的 Go 重写，支持 ref1nd 内核的 provider 写法。 🍎 🪟 🐧 · MIT
- [Sakurasan/ClashX-Go](https://github.com/Sakurasan/ClashX-Go) — ClashX 的 Go + MyGo 重写。 🍎 · AGPL-3.0
- [Binaryify/proxy-bridge](https://github.com/Binaryify/proxy-bridge) — macOS 菜单栏工具：用 TUN 把全部或选中应用的流量送进 HTTP/HTTPS/SOCKS5 代理。 🍎 · GPL-3.0
- [jiqing112/frpcclient](https://github.com/jiqing112/frpcclient) — Windows 10/11 的 frp 客户端图形管理工具：可视化编辑 TOML、启停 frpc 进程。 🪟
- [Fan-chou/magpie-native-routing](https://github.com/Fan-chou/magpie-native-routing) — 用于观察 Magpie 真实路由行为的独立原生客户端。 🍎 🪟
- [jnnbimo/RayDock](https://github.com/jnnbimo/RayDock) — Windows Xray 客户端：原生玻璃界面、TUN、代理链与专用端口。 🪟 · MIT
- [logdns/Win-XinAi-De-Tools](https://github.com/logdns/Win-XinAi-De-Tools) — 原生 Windows 网络工具箱：防火墙、网络配置、SMB、WSL 与临时 HTTP 服务，中英文、深浅色主题。 🪟 · MIT


## 🗂 存储 · 文件 · 同步

- [pteich/us3ui](https://github.com/pteich/us3ui) — 通用的跨平台 S3 对象存储图形界面与文件管理器。 🍎 🪟 🐧 `36★` · MIT [官网](https://us3ui.pteich.de)
- [DejavuMoe/Pail](https://github.com/DejavuMoe/Pail) — 跨平台 S3 兼容对象存储管理器，支持 Amazon S3、MinIO、Cloudflare R2、VersityGW、Wasabi 等。 🍎 🪟 🐧 `30★` · MIT [官网](https://pail.download)
- [Nigh/ReSoBackup](https://github.com/Nigh/ReSoBackup) — Reed-Solomon 纠删码加密备份工具，AES-256 加密，GUI 与 CLI 双形态。 🍎 🪟 🐧 · LGPL-2.1
- [vfasky/mygo-vaultwarden](https://github.com/vfasky/mygo-vaultwarden) — Vaultwarden 的 Mac 原生客户端。 🍎 [官网](https://mygo-vault.vfasky.com)
- [echoVic/cleanzo](https://github.com/echoVic/cleanzo) — 稳妥优先的 macOS 深度清理：垃圾规则、空间分析、大文件、相似照片与应用卸载。 🍎 🪟 🕸 · MIT [官网](https://cleanzo.echovic.com/)
- [younland/RcloneDrive](https://github.com/younland/RcloneDrive) — 把 rclone 的 70+ 存储后端变成本地磁盘：MyGo 原生界面、单二进制、托盘常驻、自动更新，RaiDrive 的开源替代。 🍎 🪟 🐧 · MIT
- [Magnetkopf/aim](https://github.com/Magnetkopf/aim) — 「Love ur AppImage」——Linux 上的 AppImage 管理小工具。 🐧 · GPL-3.0 [官网](https://aim.magnetkopf.com)
- [DiiKhanh/burrow](https://github.com/DiiKhanh/burrow) — 释放磁盘空间并实时展示 Mac 健康状况的开源 macOS 应用（Apple Silicon）。 🍎 · GPL-3.0
- [michaelmjhhhh/Chaos](https://github.com/michaelmjhhhh/Chaos) — macOS 截图整理工具。 🍎 · MIT
- [ychuo/copiggy](https://github.com/ychuo/copiggy) — macOS 剪贴板伴侣：浏览历史、留存常用片段、粘贴前预处理。 🍎
- [aouyitanaka/Fsearch-Mygo-GUI](https://github.com/aouyitanaka/Fsearch-Mygo-GUI) — fsearch 全盘文件搜索的原生桌面前端：模糊容错、内容检索、可排序表格。 🍎
- [lfcypo/pickphoto](https://github.com/lfcypo/pickphoto) — 快捷照片分类整理工具。 🍎 🪟 · MIT
- [Eurekaimer/TOUKO](https://github.com/Eurekaimer/TOUKO) — 把图片管理当作面向树的仓库操作，而不是逐个文件上传。 🍎 🪟 🐧 🕸 · MIT
- [zachzhao1984/bucketeer](https://github.com/zachzhao1984/bucketeer) — Cloudflare R2 与 S3 兼容存储的原生客户端。 🍎 🪟
- [1e4DouWine/clipboard_go](https://github.com/1e4DouWine/clipboard_go) — 简单剪贴板工具，Go 编写 + MyGo 原生 UI。 ❓
- [viewhang/go_paste](https://github.com/viewhang/go_paste) — 跨平台剪贴板历史工具。 🍎 🪟 · MIT
- [HycJack/mygo-tendedero](https://github.com/HycJack/mygo-tendedero) — 截图晾衣绳应用 Tendedero 的 MyGo 移植：截图挂在屏幕上方，指针一靠就滑下来。 🍎 🪟 🐧
- [logdns/newtofile](https://github.com/logdns/newtofile) — macOS Finder 新建文件工具，Go / MyGo + Swift。 🍎 · MIT
- [ZeroDevi1/nomo-mygo](https://github.com/ZeroDevi1/nomo-mygo) — Nomo 的 MyGo 重写版。 🍎 🪟 🐧 · AGPL-3.0
- [Prit36/quarry-disk-analyzer](https://github.com/Prit36/quarry-disk-analyzer) — Windows 原生磁盘空间分析器：直读 NTFS MFT，资源管理器式树、强搜索与同步 treemap。 🪟 · MIT
- [thedavidweng/rainforest](https://github.com/thedavidweng/rainforest) — 非官方跨平台 Amazon Photos 桌面备份与传输客户端。 🍎 🪟 🐧 · AGPL-3.0 [官网](http://rainforest.blahaj.uk/)
- [huynhkinhao1910/scan-image](https://github.com/huynhkinhao1910/scan-image) — 在 macOS 上像 Everything 一样秒搜 NAS：索引常驻本地，穿过 VPN 也能用。 🍎
- [zachzhao1984/twintrail](https://github.com/zachzhao1984/twintrail) — 原生双栏 macOS 文件管理器。 🍎
- [mcxen/WinExplorer](https://github.com/mcxen/WinExplorer) — 对齐 Windows 11 资源管理器观感的纯原生文件管理器：图标与缩略图全部由 Go 在 GPU 上自绘。 🍎 🪟 🐧


## 🎵 媒体 · 播放器 · 下载

- [elianiva/meiro](https://github.com/elianiva/meiro) — 轻量级 YouTube Music 桌面播放器：界面原生而非浏览器套壳，内存占用约 100 MB，不加载 YouTube Music 网页即可播放，支持 Last.fm 记录、同步歌词与随歌曲变化的配色。 🍎 🪟 🐧 `268★` · GPL-3.0
- [fzn0x/mixmusic](https://github.com/fzn0x/mixmusic) — Spotify 与 YouTube Music 合一的跨平台播放器：一次搜索、一个队列、混合歌单、同步歌词与均衡器。 🍎 🪟 🐧 `110★` · MIT [官网](https://fzn0x.github.io/mixmusic/)
- [vst93/bili-fm](https://github.com/vst93/bili-fm) — 用音频「听」B 站节目，可当音乐播放器或学习工具，Go + MyGo 原生开发，三端可用。 🍎 🪟 🐧 `74★` · Apache-2.0
- [missuo/motrix-mygo](https://github.com/missuo/motrix-mygo) — Motrix 的 MyGo 原生重写，继续驱动 aria2 下载引擎，无 Electron、无 WebView。 🍎 🪟 `55★`
- [j4ckxyz/Aurelia](https://github.com/j4ckxyz/Aurelia) — Jellyfin 的快速原生音乐播放器，三端可用。 🍎 🪟 🐧 · MIT
- [hackerlengyue/binggan](https://github.com/hackerlengyue/binggan) — 饼干大小姐：本地视频密钥提取与管理、课程播放编排、批量解密与资源管理（MyGo + Vue）。 🍎 🪟 🕸 · GPL-3.0
- [owocc/bowerbird](https://github.com/owocc/bowerbird) — 本地素材与设计库管理器：MyGo WebView 模式 + React 19 / TypeScript / Tailwind v4，另有实验性原生渲染分支。 🍎 🪟 🐧 🕸
- [xptea/curb](https://github.com/xptea/curb) — 极简原生音视频下载器：粘链接、选画质或 MP3、本地保存，无 WebView、无 Electron。 🍎 🪟 🐧 · MIT [官网](https://curb.seths.app)
- [biaobiaobiao108/fnmovie](https://github.com/biaobiaobiao108/fnmovie) — 把家里的飞牛影视片库带到 Windows 桌面。 🪟 [官网](https://biaobiaobiao108.github.io/fnmovie/)
- [freelxs/jstv-player](https://github.com/freelxs/jstv-player) — JSTV / CatPawOpen 猫源协议的 macOS 播放器。 🍎 🪟 🐧 🕸 · MIT
- [ZypherChan/MusicComments](https://github.com/ZypherChan/MusicComments) — 网易云随机热评桌面应用，提供 Windows x64 与 Linux x64 构建。 🪟 🐧
- [rzh0504/Qmdr](https://github.com/rzh0504/Qmdr) — QQ 音乐 / 歌单下载器。 🍎 🪟 🐧 · GPL-3.0
- [Team-Quaver/quaver-astra](https://github.com/Team-Quaver/quaver-astra) — 轻量的跨平台 Quaver 音游客户端，接近原生的体验。 🍎 🪟 🐧 · AGPL-3.0
- [fazi-gondal/video-downloader-mygo](https://github.com/fazi-gondal/video-downloader-mygo) — 基于 yt-dlp + FFmpeg 的原生下载器：分析视频与歌单，选画质、音轨、字幕与容器，带队列与历史。 🍎 🪟 🐧 · MIT
- [myoula/ape-player](https://github.com/myoula/ape-player) — Omarchy 上的 Emby 播放器。 🐧
- [steampixel007/Dipper](https://github.com/steampixel007/Dipper) — 原生追番桌面应用：Mikan 目录、RSS 与内置 BT 下载。 🍎 🪟 🐧
- [XueJie1/godrome](https://github.com/XueJie1/godrome) — 连接自建 Navidrome / Subsonic 曲库的轻量原生桌面音乐播放器。 🍎 🪟 🐧 · MIT
- [jyuuroku16/mediago](https://github.com/jyuuroku16/mediago) — 高性能 macOS 媒体嗅探与下载器，MyGo 原生 UI。 🍎
- [HycJack/mujicacut](https://github.com/HycJack/mujicacut) — 剪映风格的桌面视频编辑器：MyGo + MujicaUI 全程 GPU 绘制，无 WebView / HTML / JS。 ❓
- [yaffalhakim1/playlist](https://github.com/yaffalhakim1/playlist) — YouTube 歌单原生桌面播放器：MyGo + Onevra，无 WebView。 🍎 🪟 🐧 [官网](https://yaffalhakim1.github.io/playlist/)
- [fazi-gondal/video](https://github.com/fazi-gondal/video) — 功能丰富的原生视频播放器，MyGo UI + MujicaUI，后台音频流播放。 🪟
- [Shirolin/videopress](https://github.com/Shirolin/videopress) — 高颜值 Windows 视频压缩工具，GUI + CLI。 🪟 · MIT
- [Alpenl/wallpaper](https://github.com/Alpenl/wallpaper) — 跨平台动态壁纸 MVP：macOS 原生转码与规则管理，Linux 走 mpv + X11 兼容路线。 🍎 🪟 🐧


## ⚡ 效率 · 菜单栏 · 启动器

- [henryyu333/shelf](https://github.com/henryyu333/shelf) — macOS 原生效率货架：剪贴板历史、截图、拖放暂存，全部用 Go 写成。 🍎 `51★` · MIT
- [egoist/uma](https://github.com/egoist/uma) — Umami.is 网站统计的 macOS 菜单栏原生客户端。 🍎 🪟 🐧 `41★`
- [eziq1/golauncher](https://github.com/eziq1/golauncher) — Raycast 风格的 Windows / macOS 快捷启动器，基于 MyGo 原生 UI 工具包。 🍎 🪟 · MIT
- [iwangjie/xiangzhuan](https://github.com/iwangjie/xiangzhuan) — 菜单栏休息提醒：工作到点全屏燃香，一炷香尽回到案前。 🍎 🪟 · MIT
- [tacshi/Unscan](https://github.com/tacshi/Unscan) — 完全在本机把扫描版 PDF 变可搜索，或重排成干净文本 PDF：Go 无 cgo + PaddleOCR PP-OCRv6。 🍎 · MIT
- [0froq/snip](https://github.com/0froq/snip) — macOS 剪贴板管理器雏形：每次复制弹出一张小浮卡。 🍎 · MIT
- [ychuo/tavu](https://github.com/ychuo/tavu) — macOS 原生工作区：运行工具、编辑文件、审阅改动都在一个窗口里。 🍎
- [zyition/voke](https://github.com/zyition/voke) — Voke——Windows 启动器。 🪟 · MIT
- [gomeen/Zakki](https://github.com/gomeen/Zakki) — macOS / Windows 速记：多个彩色标签各存一段 Markdown，⌘ 与 Ctrl 自动切换。 🍎 🪟 · MIT
- [diver80/avono-timebooking](https://github.com/diver80/avono-timebooking) — macOS 工时计划与 Achievo 报工：周 / 日 / 月视图、Jira 票漏斗、日历与菜单栏入口。 🍎
- [soidaken/ClipRecorder](https://github.com/soidaken/ClipRecorder) — Windows 原生截图 / 录屏 / 框选翻译：本机 OCR + DeepSeek，无 WebView。 🪟 · MIT
- [Star-Trails/countdowner](https://github.com/Star-Trails/countdowner) — Windows 原生桌面倒计时小组件。 🪟
- [zephyr-qu/kanso](https://github.com/zephyr-qu/kanso) — 个人看板项目管理小工具：Go 后端 + React 前端 + SQLite 单机存储，单端口运行。 🪟 🕸
- [308K/my-doubtful-go](https://github.com/308K/my-doubtful-go) — SmartAR：智能应收账款账龄分析与坏账预警桌面系统（MyGo + React 19 + Shadcn UI + Excelize 公式引擎）。 🍎 🪟 🐧 🕸 · MPL-2.0
- [feiniao233/MyCast](https://github.com/feiniao233/MyCast) — Windows 启动器。 🪟
- [cecil-su/mygo-browser](https://github.com/cecil-su/mygo-browser) — Windows 浏览器原型：Go 原生 UI + WebView2。 🍎 🪟
- [m3hu1/mygo-todo](https://github.com/m3hu1/mygo-todo) — macOS 菜单栏的待办 + 笔记应用。 🍎
- [nerv-base/MyToolbox](https://github.com/nerv-base/MyToolbox) — 「让日常，轻一点」——本地、原生、模块化的桌面工具箱。 🍎 🪟 🐧 · AGPL-3.0
- [yinshuwei/mytools](https://github.com/yinshuwei/mytools) — AI 时代的开发者工具箱。 🍎 🪟 🐧 · MIT
- [mintonight/pomodoro](https://github.com/mintonight/pomodoro) — 极简桌面番茄钟：专注计时、暂停超时取消、统计热力图、系统托盘、SQLite 本地存储。 🍎 🪟 🐧
- [azzliang6/pomodoro-mygo](https://github.com/azzliang6/pomodoro-mygo) — 番茄钟，基于纯 Go 桌面框架 MyGo 实现。 🪟 · MIT
- [HanlunWang/simple-toggle](https://github.com/HanlunWang/simple-toggle) — 把任意脚本变成 macOS 菜单栏上的一个开关。 🍎 · MIT
- [javatoai/sleepdock](https://github.com/javatoai/sleepdock) — 带托盘控制的原生睡眠定时器。 🍎 🪟 🐧 · MIT
- [dandibbert/textrouter](https://github.com/dandibbert/textrouter) — 重新设计的 TextSoap：剪贴板一键清理、看得懂的查找替换、表格式批量替换、可视化动作链。 🍎
- [ctzcs/Timer](https://github.com/ctzcs/Timer) — 置顶桌面倒计时小挂件：仿实体可视化计时器，30 段进度条 + 七段数码管。 🪟
- [m3hu1/tuck](https://github.com/m3hu1/tuck) — 3.8 MB 的 macOS 菜单栏待办与 Markdown 笔记，快且省资源。 🍎


## 📊 系统 · 监控 · 硬件

- [Binaryify/MonitorBar](https://github.com/Binaryify/MonitorBar) — macOS 菜单栏 / Windows 托盘的显示器管理工具：不依赖 DDC/CI，可通过澎湃 OS 局域网接口切换输入源、调音量。 🍎 🪟 `162★` · MIT
- [xbenduan/vitals](https://github.com/xbenduan/vitals) — 只做一件事的 macOS 系统状态小面板，主打体验而非功能堆叠。 🍎
- [oneo-me/neohm](https://github.com/oneo-me/neohm) — 控制 Home Assistant 设备的 macOS 菜单栏应用，带完整空调控制。 🍎 🪟 🐧 [官网](https://oneo-me.github.io/neohm/)
- [qzz0518/Moniflip](https://github.com/qzz0518/Moniflip) — 经 DDC/CI 一键把显示器切到另一台电脑：macOS 状态栏 / Windows 托盘。 🍎 🪟 · MIT
- [rayorole/orole-os-desktop](https://github.com/rayorole/orole-os-desktop) — 个人操作环境：Windows 原生，MyGo + Go 守护进程 + React。 🪟 🕸 · MIT
- [e1roy/stage-manager-for-windows](https://github.com/e1roy/stage-manager-for-windows) — 把 macOS 舞台管理器带上 Windows 10/11：当前应用留在台上，其余按显示器归入侧栏。 🪟 · MIT
- [wan-kong/apex-helper](https://github.com/wan-kong/apex-helper) — 禁用影响 Apex 英雄操作的游戏按键。 🪟
- [VeinsureLee/BYR-Client](https://github.com/VeinsureLee/BYR-Client) — 北邮人论坛本地桌面客户端：Go 业务逻辑 + MyGo 原生 UI，Windows 优先。 🪟
- [villatothesea/DumpingGround](https://github.com/villatothesea/DumpingGround) — Windows 原生维护工具：进程查看、磁盘占用分析、带回收站的安全清理。 🪟 · MIT
- [sugarbearr/gogo-explorer](https://github.com/sugarbearr/gogo-explorer) — Windows 原生任务管理器重写：实时进程表、系统性能条与「为什么在跑」血缘树。 🪟 · MIT
- [oscs1024-pixel/MiJia](https://github.com/oscs1024-pixel/MiJia) — 从零重构的跨平台米家智能家居控制中心：MyGo GPU 原生 UI，macOS 菜单栏 Flyout，不用 HTML / WebView。 🍎 🪟 🐧
- [fondoger/mouse-mapper](https://github.com/fondoger/mouse-mapper) — 安静的小工具：重映射鼠标侧键，Windows 与 macOS 全用 MyGo 原生 UI 写成。 🍎 🪟 · MIT
- [17130239-coder/Pulse](https://github.com/17130239-coder/Pulse) — macOS 原生系统与硬件活动监视器：Go + MyGo，经 Metal 直接 GPU 绘制，无 CGO、无 WebView。 🍎
- [lesenelir/stock-float-mygo-native](https://github.com/lesenelir/stock-float-mygo-native) — 常驻最前层的 macOS 实时股价浮窗：纯 Go + MyGo 原生 UI，无 WebView。 🍎 · MIT


## 🎮 游戏 · 娱乐 · 其他

- [zrcoder/ndor](https://github.com/zrcoder/ndor) — 用代码画画，给孩子和程序员~（GUI 版基于 MyGo，另附 CLI） ❓ · MIT [官网](https://ndor.netlify.app)
- [CBR0/calc](https://github.com/CBR0/calc) — Windows 11 风格桌面计算器，纯 Go 原生绘制。 🪟 🐧 · MIT
- [zhengchalei/LeagueAkari-MyGo](https://github.com/zhengchalei/LeagueAkari-MyGo) — 国服 LOL 战绩与选人助手（LeagueAkari 移植），MyGo + WebView2，优化内存与按需查询。 🪟 · MIT
- [zrcoder/ttoy](https://github.com/zrcoder/ttoy) — 开发者的桌面小玩具与迷你游戏合集。 🍎 · MIT
- [li-yifei/bdon-mygo](https://github.com/li-yifei/bdon-mygo) — BanG Dream! Our Notes 组卡加速器：原生多线程计算 + ADB 一键把存档导入卡池。 🍎 · MIT [官网](https://bdon.moe/tools/deck)
- [tortoise10h/calculus](https://github.com/tortoise10h/calculus) — MyGo 原生 UI 版计算器。 🍎 🪟 🐧
- [ZeroDevi1/gamesave-manager](https://github.com/ZeroDevi1/gamesave-manager) — 基于 MyGo 的游戏存档备份管理器：快速备份、恢复与整理本地存档。 🪟 🕸
- [Eslzzyl/krkrgo](https://github.com/Eslzzyl/krkrgo) — 纯 Go 的现代 krkrz 视觉小说模拟器（开发中）。 🍎 🪟 🐧
- [Yurbin/mygo-snake](https://github.com/Yurbin/mygo-snake) — 贪吃蛇桌面游戏，MyGo 原生 UI，麒麟 V10 SP1 绿色免安装。 🐧
- [BabyLy233/MyLock](https://github.com/BabyLy233/MyLock) — Deadlock（Deadlock 对战游戏）的模组管理器，Go + MyGo 原生桌面应用。 🍎 🪟 🐧 · MIT
- [ch1y1z1/xiangqi_go](https://github.com/ch1y1z1/xiangqi_go) — 象棋残局桌面端：本地摆棋、分支研究、离线 Pikafish AI。 🍎 🪟 🐧 · GPL-3.0

## 组件库 · 模板 · 框架周边

> 这些项目不是应用，而是构建在 MyGo 之上的组件库、主题包与应用模板；均为纯 Go 源码包，随 MyGo 本身支持 macOS / Windows / Linux。

- [egoist/mygo](https://github.com/egoist/mygo) — MyGo 框架本体：用 Go 写桌面应用，同一窗口可混用 Go 自绘的原生 UI 与系统 WebView 页面，纯 Go 无 cgo，一条命令产出 macOS / Windows / Linux 安装包。 🍎 🪟 🐧 `2852★` · MIT [官网](https://mygo.egoist.dev)
- [oneo-me/onevra](https://github.com/oneo-me/onevra) — 基于 MyGo 的原生桌面组件库：主题控件、窗口外壳、Lucide 图标，内置聊天、Markdown、代码高亮、图表与命令面板，另附三端打包工具。 🍎 🪟 🐧 `252★` · MIT [官网](https://oneo-me.github.io/onevra/)
- [smallnest/uix](https://github.com/smallnest/uix) — MyGo 原生 UI 的 shadcn/ui 风格组件库，按需 import 包名即可用 Go 调用。 🍎 🪟 🐧 · MIT
- [ELY-Open-Source/CrychicUI](https://github.com/ELY-Open-Source/CrychicUI) — 1500 个 MyGo 原生 UI 组件，沿用 MyGo 自身观感，带动效与音效。 🍎 🪟 🐧 · MIT
- [ELY-Open-Source/MujicaUI](https://github.com/ELY-Open-Source/MujicaUI) — 宫廷哥特（Court-gothic）风格的 MyGo 原生 UI 组件库。 🍎 🪟 🐧 · MIT
- [ELY-Open-Source/8bitMyGoUI](https://github.com/ELY-Open-Source/8bitMyGoUI) — 16-bit 像素风 MyGo 原生 UI 组件库：同一份 Go 代码还能经 WASM 在浏览器里跑展示。 🍎 🪟 🐧 · MIT
- [firede/mygo-platinum](https://github.com/firede/mygo-platinum) — 为 MyGo 补齐经典桌面控件（Windows 风格）的组件库。 🍎 🪟 🐧 · MIT [官网](https://mygo-platinum.firede.com)
- [mcxen/GodGo](https://github.com/mcxen/GodGo) — MyGo 应用的技术外壳：侧栏、设置、工作流与签名自动更新。 🍎 🪟 🐧
- [LoTwT/lucia](https://github.com/LoTwT/lucia) — MyGo 原生 UI 的桌面应用底座：本地开发、打包、GitHub 发布与签名自动更新已全部接通。 🍎 🪟 🐧
- [harukizmoe/mayu](https://github.com/harukizmoe/mayu) — 为 MyGo 原生 GPU UI 打造的 Material Design 3（Material You）纯 Go 组件库。 🍎 🪟 🐧 · MIT
- [HycJack/MintUI](https://github.com/HycJack/MintUI) — 构建在 MyGo 之上的原生组件库与组件画廊：22 个包，无 WebView，纯 Go 无 cgo。 🍎 🪟 🐧
- [addidotlol/mycn](https://github.com/addidotlol/mycn) — MyGo 原生 UI 的 shadcn/ui 风格组件库，每帧调用 `mycn.Use` 即可换肤。 🍎 🪟 🐧
- [yldm-tech/mygo-breeze-ui](https://github.com/yldm-tech/mygo-breeze-ui) — 受 Tailwind 启发的 MyGo 类型化原生 UI 组件、工具函数、CLI 与 MCP 工具。 🍎 🪟 🐧 · MIT [官网](https://yldm-tech.github.io/mygo-breeze-ui/)
- [HyperGrapher/mygo-desktop-webgl-app](https://github.com/HyperGrapher/mygo-desktop-webgl-app) — MyGo WebView + WebGL 的实验性应用模板。 🍎 🪟 🐧
- [auron-labs/mygo-framework](https://github.com/auron-labs/mygo-framework) — MyGo 的源码优先应用框架与参考实现：固定布局、SQLite/GORM、Goose 迁移、校验、显式 DI、结构化日志、类型化设置、系统密钥、代码生成器与可选 MCP。 🍎 🪟 🐧 🕸
- [xingkaixin/mygo-native-ui](https://github.com/xingkaixin/mygo-native-ui) — MyGo 原生 UI 组件集合。 🍎 🪟 🐧 · MIT
- [baoziv587/mygo-template](https://github.com/baoziv587/mygo-template) — MyGo 应用起步模板（中英双语）。 🍎 🪟 🐧
- [Cyenoch/mygoicons](https://github.com/Cyenoch/mygoicons) — 面向 MyGo 原生 UI 的类型化 Iconify 图标集合与生成器：懒加载 SVG 缓存，链接期剔除未用图标。 🍎 🪟 🐧 · MIT
- [Cyenoch/mygoui](https://github.com/Cyenoch/mygoui) — MyGo 原生 UI 的 shadcn 风格 Go 组件库。 🍎 🪟 🐧 · MIT
- [ydongy/template-mygo-app](https://github.com/ydongy/template-mygo-app) — 纯 Go 原生桌面应用模板：初始化、本地化、测试与打包齐全。 🍎 🪟 🐧 · MIT

## 图例

| 标记 | 含义 |
| --- | --- |
| 🍎 | 提供 macOS 构建（依据 GitHub Releases 产物或 README 声明） |
| 🪟 | 提供 Windows 构建 |
| 🐧 | 提供 Linux 构建 |
| ❓ | 未找到明确平台线索，需从源码自行构建 |
| 🕸 | 明确采用 WebView 模式：Go 后端 + Web 前端 |
| （无 🕸） | 大多为纯 Go 原生 UI（由 MyGo 在 GPU 上绘制），个别未能从 README 确认 |

平台标记来自各项目最新若干条 Release 的资源文件名与 README 声明（闭源应用取自官网），可能与真实支持范围不完全一致；发现错误欢迎提 Issue 或 PR。

## 贡献指南

- 新增条目请保证仓库的 `go.mod` 真的依赖 `github.com/egoist/mygo`（或以 `tool` 形式引用 `github.com/egoist/mygo/cmd/mygo`）；fork 与镜像不单列。
- 闭源应用需为框架作者或官方认可的项目，并注明官网来源。
- 一行描述说清「它是什么」，尽量给出对标的知名工具，而不是罗列技术栈。
- 平台标记按 Releases 产物或 README 的官方声明填写；仅支持单平台的应用同样欢迎收录。
- 遵循 [awesome](https://github.com/sindresorhus/awesome) 的贡献规范：只收录公开、可运行、有源码仓库的项目（闭源应用见上）。

## 许可证

[![CC0](https://licensebuttons.net/p/zero/80x15.png)](https://creativecommons.org/publicdomain/zero/1.0/)

本列表以 CC0 发布，在法律允许的最大限度内放弃所有版权与相关权利。各应用保留自己的原始许可证，条目中已标注。
