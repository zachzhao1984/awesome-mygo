<div align="center">

# Awesome MyGo

**A curated list of cross-platform desktop apps built with the [MyGo](https://github.com/egoist/mygo) framework**

[English](README.md) · [简体中文](README-ZH.md)

MyGo is a pure-Go desktop framework by [egoist](https://github.com/egoist): one window can host a system
WebView page (WKWebView / WebView2 / WebKitGTK) or be drawn entirely as native UI by Go code on the GPU.
No Electron, no cgo — the output is a single binary of a few MB, and one command produces the macOS app
bundle, the Windows installer and Linux packages, with signing, notarization and delta auto-updates.

**228 projects** · **208 desktop apps** (**75** of them ship all three platforms) · **20 libraries & templates**

_Data collected 2026-10-26. All 226 open-source entries are verified to actually depend on `github.com/egoist/mygo` in `go.mod`; the closed-source app is documented from its official site._

</div>

## Contents

- [Getting Started](#getting-started)
- [Open-source Apps by the Author](#open-source-apps-by-the-author)
- [Closed-source Apps by the Author](#closed-source-apps-by-the-author)
- [Desktop Apps](#desktop-apps)
  - [✍️ Editors · Notes · Writing](#editors-notes-writing)
  - [🤖 AI · Agents · LLM Clients](#ai-agents-llm-clients)
  - [🛠 Developer Tools](#developer-tools)
  - [🌐 Network · Proxy · Remote](#network-proxy-remote)
  - [🗂 Storage · Files · Sync](#storage-files-sync)
  - [🎵 Media · Players · Download](#media-players-download)
  - [⚡ Productivity · Menu Bar · Launchers](#productivity-menu-bar-launchers)
  - [📊 System · Monitoring · Hardware](#system-monitoring-hardware)
  - [🎮 Games · Fun](#games-fun)
- [Component Libraries · Templates · Framework Add-ons](#component-libraries-templates-framework-add-ons)
- [Legend](#legend)
- [Contributing](#contributing)

## Getting Started

A MyGo app with a web frontend (requires Go 1.27.3+ and Bun):

```sh
bunx mygo-cli init my-app      # or: npx mygo-cli init my-app
cd my-app
bun run dev
```

A pure-Go native-UI app needs only Go:

```sh
go run github.com/egoist/mygo/cmd/mygo@latest init -template native my-app
cd my-app
go tool mygo dev
```

Full docs at [egoist/mygo/docs](https://github.com/egoist/mygo/blob/main/docs/README.md); website [mygo.egoist.dev](https://mygo.egoist.dev).

## Open-source Apps by the Author

> The framework author's own MyGo apps — all open source, and verified to depend on `github.com/egoist/mygo`.

- [egoist/kero](https://github.com/egoist/kero) — A native terminal for coding agents: sessions run in the `kerod` daemon and survive quitting; the sidebar shows which one needs you and ⌘J jumps there; `kero new / split / send / wait / read` lets agents drive panes themselves; libghostty rendering with SSH / Tailscale / WSL remote hosts. 🍎 🪟 🐧 `1219★` · MIT [Website](https://kero.sh/)
- [egoist/gorex](https://github.com/egoist/gorex) — Rex terminal clone in MyGo native UI 🍎 🪟 🐧 `143★`
- [egoist/godiff](https://github.com/egoist/godiff) — Fast native diff viewer 🍎 🪟 🐧 `123★`
- [egoist/mygo-cloudmusic](https://github.com/egoist/mygo-cloudmusic) — A third-party NetEase Cloud Music client with native UI and no WebView: QR-code login, daily recommendations, private FM and heart-beat mode, per-syllable lyrics with a "rhythm" view; lossless and Hi-Res progressive playback, local caching, a notch mini-player, volume normalization and crossfade, light/dark themes. 🍎 🪟 🐧 · AGPL-3.0 [Website](https://music.egoist.dev/)
- [egoist/2048](https://github.com/egoist/2048) — 2048 game in MyGo native! ❓ [Website](https://2048.egoist.dev)

## Closed-source Apps by the Author

> A closed-source freeware app by the framework author, also written with MyGo. Information from its official site; not verifiable via `go.mod`.

- [Pulse](https://pulse.egoist.dev/) — [@egoist](https://github.com/egoist)（closed-source · free · Apple Silicon Mac）。"Everything your computer is doing, in one calm window": per-core CPU, memory pressure, GPU engines, disk and network traffic, battery and temperatures; every process with its icon, parent/children and history; menu-bar glance items. The site states "Built with MyGo" — GPU-drawn, no web view. 🍎 🪟 🐧

## Desktop Apps

Grouped by purpose; within a group, sorted by stars then name. Entries marked 🕸 explicitly use MyGo's WebView mode (Go backend + web frontend); unmarked entries are mostly pure-Go native UI.

## ✍️ Editors · Notes · Writing

- [sorrycc/Mayoi](https://github.com/sorrycc/Mayoi) — A small, fast code editor written in Go, with a native GPU-drawn UI (no webview, no Electron) 🍎 🪟 🐧 `256★` · MIT
- [mu-zi-lee/Tangentry](https://github.com/mu-zi-lee/Tangentry) — Follow your curiosity — a local-first, multi-platform content aggregation, reading and notes app. 🍎 🪟 `146★` · MIT
- [godwit-email/godwit](https://github.com/godwit-email/godwit) — Open-source, hackable AI email client 🍎 🪟 🐧 · Apache-2.0 [Website](https://godwit.email)
- [oneo-me/locus](https://github.com/oneo-me/locus) — A local-first Markdown notebook for macOS. Notes stay ordinary files you can edit anywhere, with HTML canvases, read-only MCP for Agents, and a built-in terminal. 🍎 🪟 🐧 🕸 · MIT [Website](https://oneo-me.github.io/locus/)
- [kiwiflydream/yunji-uml](https://github.com/kiwiflydream/yunji-uml) — Native macOS editor for PlantUML, Mermaid, and Flowchart.js 🍎 🪟 🐧 · MIT
- [sorrycc/Deckle](https://github.com/sorrycc/Deckle) — A fast, native Markdown editor for macOS 🍎 🪟 🐧 · MIT
- [RSK21X/GoRss](https://github.com/RSK21X/GoRss) — Native RSS and Atom reader for Apple Silicon Macs, built with MyGo and Onevra 🍎
- [alvyn16/GOsidian](https://github.com/alvyn16/GOsidian) — High-performance, local-first Obsidian clone built with MyGo (pure Go desktop runtime) and TypeScript. 🪟 · MIT
- [logdns/imyemail-cloud](https://github.com/logdns/imyemail-cloud) — Two open-source email editions: platform-native clients and Pulse-inspired Go/MyGo desktop 🍎 🪟 🐧 · MIT [Website](https://imy.email)
- [everpcpc/mica](https://github.com/everpcpc/mica) — A focused, native Gmail client for macOS. 🍎
- [xinde/Mote](https://github.com/xinde/Mote) — A macOS menu-bar app for quick Markdown notes and quick focus timers. 🍎
- [LZD121/my-gotion](https://github.com/LZD121/my-gotion) — A local-first Notion clone: block documents + database views, plain JSON files as the only data source, WebDAV / GitHub incremental sync. Go + mygo + React + TipTap. 🍎 🪟 🐧 · MIT
- [yangflow/oriel](https://github.com/yangflow/oriel) — Personal mixed-timeline reader for RSS and RSSHub, in pure Go with native UI (MyGo). Desktop app and headless server in one program. 🍎 🪟 🐧 · MIT


## 🤖 AI · Agents · LLM Clients

- [Licoy/Quosparr](https://github.com/Licoy/Quosparr) — A menu-bar/tray app tracking Codex, Claude Code and Grok quotas, resets, API-equivalent cost and local sessions, with multi-account and relay switching. 🍎 🪟 🐧 `300★` · AGPL-3.0 [Website](https://quosparr.com)
- [AstraFoundry/Arion](https://github.com/AstraFoundry/Arion) — Local-first voice dictation and Pinyin input method: hold-to-talk (right ⌥ on macOS, right Alt on Windows) to speak Mandarin, English or mixed technical terms in any focused editor, with recognition, full-Pinyin typing, correction learning and contextual polishing all on-device; Qwen3-ASR 1.7B runs locally (MLX on macOS, speech.cpp on Windows), with optional two-stage polishing that adapts wording to the visible app and cursor context; ships native system IME hosts (ArionInput.app / ArionTSF.dll), lives in the menu bar, keeps partial drafts in its floating pill until release, plus zero-knowledge sync and signed updates. 🍎 🪟 `51★` · AGPL-3.0 [Website](https://arion.astrafoundry.si)
- [hehehai/AudioSmith](https://github.com/hehehai/AudioSmith) — Speech, voices, stories, audiobooks, dubbing and transcription, made on your Mac. Free and open source. 🍎 `47★` · AGPL-3.0 [Website](https://actnow.dev/audiosmith)
- [kkkk2323/droi](https://github.com/kkkk2323/droi) — Native Mac, Windows and iPhone app for Factory Droid: your droid Sessions in one window and on your phone, built with Go (MyGo) and Expo 🍎 🪟 · MIT
- [nerv-base/mytoken](https://github.com/nerv-base/mytoken) — Where did all your tokens go? Local token & cost tracker for AI coding harnesses — Claude Code, Codex, Gemini CLI, opencode, Cline and more. 🍎 🪟 🐧 · MIT
- [enowx/enowx](https://github.com/enowx/enowx) — Run Claude Code, Codex and 43 other coding agents in parallel, each on its own branch in its own git worktree, on your machine or your own server. Watch, compare and merge them fro 🍎 🪟 🐧 · MIT
- [sorrycc/CCGuanjia](https://github.com/sorrycc/CCGuanjia) — A Mac app that looks after Claude Code: profiles of your own accounts, install, usage and cleanup 🍎 · MIT
- [oysterhyd/AgentMeter](https://github.com/oysterhyd/AgentMeter) — Windows desktop monitor for Codex quota, token usage, estimated costs and runtime metrics. 🪟
- [yeshan333/tingsub](https://github.com/yeshan333/tingsub) — Local bilingual live captions for English/Japanese browser audio; Apple Silicon + MLX, with a Chrome extension. 🍎 · MIT [Website](https://shansan.top/tingsub/)
- [tk103331/ChatGo](https://github.com/tk103331/ChatGo) — A simple cross-platform AI chat client built with Go and MyGo, with multi-provider models, Agents, tools, MCP, ACP and a built-in terminal. 🍎 🪟 🐧 · MIT
- [horizon0514/ds-search](https://github.com/horizon0514/ds-search) — A minimal macOS menu-bar search powered by the DeepSeek Search API, in MyGo native UI. 🍎 · MIT
- [YuanZhe-99/Kyokai](https://github.com/YuanZhe-99/Kyokai) — Kyokai is a cross-platform Computer Use application that enables people and AI agents to interact 🍎 🪟 · AGPL-3.0
- [bunnywaffle/llama-manager](https://github.com/bunnywaffle/llama-manager) — Lightweight, high-performance desktop llama.cpp manager built with MyGo, featuring branching chat, multi-model router, and automated diagnostics 🪟 🐧
- [HycJack/mygo-agent](https://github.com/HycJack/mygo-agent) — A Codex-style desktop AI coding agent built with MyGo — native GPU UI, built-in agent loop, skills and MCP 🍎 🪟 🐧
- [yaffalhakim1/opencode-gui](https://github.com/yaffalhakim1/opencode-gui) — Native desktop GUI for OpenCode, built with MyGo (Go), with a WebSocket daemon for phone access over Tailscale 🪟
- [minifish-org/pith-desk](https://github.com/minifish-org/pith-desk) — A thin local desktop agent powered by Pith, with workspace tools, MCP connections, and a TypeScript interface. 🍎 🐧 · AGPL-3.0
- [Beeta/voxi](https://github.com/Beeta/voxi) — Meeting-recording transcription and summarization app on MyGo native UI. 🍎 · MIT
- [hoanglong2311/AI-limit](https://github.com/hoanglong2311/AI-limit) — macOS menu bar app to view AI subscription usage 🍎
- [ixxxxoooo/ai-usage](https://github.com/ixxxxoooo/ai-usage) — A macOS menu-bar AI billing helper: Cursor request usage and DeepSeek balance, credentials kept in Keychain. 🍎 · MIT
- [gvenusleo/Atlas](https://github.com/gvenusleo/Atlas) — A general-purpose agent built in Go. 🍎 🪟 🐧 · MIT
- [hehehai/Auralink](https://github.com/hehehai/Auralink) — Voice input for macOS on remote models: speak in any app and the text lands at your cursor. Transcribe, translate and rewrite, with your own API keys. 🍎 · AGPL-3.0 [Website](https://actnow.dev/auralink)
- [lexleizou/byop](https://github.com/lexleizou/byop) — Native MyGo multi-plugin workbench for an external Pi CLI 🍎 · MIT
- [foyoodo/Cove](https://github.com/foyoodo/Cove) — Cove is a native macOS chat client. It draws its interface with MyGo's `ui` package, not a web view, and it talks to OpenAI-compatible Chat Completions endpoints (`POST {baseURL}/c 🍎
- [xinde/deepseek-harness-mygo](https://github.com/xinde/deepseek-harness-mygo) — Lightweight MyGO desktop launcher for a local DeepSeek Harness checkout 🍎 🕸 · MIT
- [meimingqi222/devin-usage-metrics](https://github.com/meimingqi222/devin-usage-metrics) — Local coding-agent analytics, now implemented in **Go + MyGo native UI**. No Rust compilation, WebView, JavaScript runtime, or cgo is required to build the desktop application. 🍎 🪟
- [M2tHane/Distill](https://github.com/M2tHane/Distill) — Distill local coding agent sessions (Claude Code, Codex, Pi) into skills, rules and AGENTS.md/CLAUDE.md 🍎
- [Maidang1/herdr-ui](https://github.com/Maidang1/herdr-ui) — Native desktop client for Herdr: workspaces, worktrees, agent status and a built-in terminal with tabs, splits and prefix mode. 🍎
- [ArnoChenFx/kura](https://github.com/ArnoChenFx/kura) — Desktop skills manager built with MyGo 🍎 🪟 🐧
- [Helix-lyh/leeway](https://github.com/Helix-lyh/leeway) — A CLI probe for AI coding providers' usage, quota and reset times. 🍎 🪟 🐧 · MIT
- [dhx007/mygo-dsh](https://github.com/dhx007/mygo-dsh) — A recreation of the first-generation DeepSeek Harness desktop app in MyGo native UI: sessions, trajectory, four modes, tool approvals, PTC — pure Go, no WebView. ❓ · MIT
- [pararchy/para-term](https://github.com/pararchy/para-term) — A personal terminal that runs Para CLI in a real pseudo-terminal inside a GPU-native window. 🪟
- [Clearzero22/pi-web-desktop](https://github.com/Clearzero22/pi-web-desktop) — Pi Web Desktop - MyGo shell for pi-web with isolated Node 🪟 🕸
- [javatoai/repodock](https://github.com/javatoai/repodock) — Native Go and MyGo GitHub project launcher for Codex 🍎 🪟 · MIT
- [Riablo/skills-hub](https://github.com/Riablo/skills-hub) — A desktop app to manage agent skills in one place and install them globally or per project, locally or over SSH. Built with MyGo. 🍎
- [songlairui/skills-reader](https://github.com/songlairui/skills-reader) — A MyGo desktop reader for agent skills in ~/.agents/skills — grouped, nicely typeset, with lock-file based update checks 🍎 🐧 🕸
- [zackzhou-work/spark-go](https://github.com/zackzhou-work/spark-go) — A small macOS window that shows the live status of every session in the Code tab of Claude Desktop. Built with Go and the native UI of mygo. 🍎 · MIT
- [nggalek-co/titen](https://github.com/nggalek-co/titen) — Titen is a native desktop meeting transcription application for macOS and Windows built with MyGo native GPU widgets, Go, and platform-specific native capture helpers. It captures 🍎 🪟
- [tviber/voice-morph](https://github.com/tviber/voice-morph) — A MorphVOX Pro-style real-time voice changer: Go DSP engine + web frontend + MyGo desktop shell. 🍎 🪟 🐧
- [xxww0098/xbs](https://github.com/xxww0098/xbs) — A cross-platform batch image-to-image tool supporting Doubao and Qwen, in Go + MyGo. 🍎 🪟 🐧 · MIT
- [ijry/YoYoCode](https://github.com/ijry/YoYoCode) — An native go verison codeg - Collaborative multi-agent AI coding workspace: aggregate sessions from Claude Code, Codex, OpenCode, Pi, Grok Build, etc. Desktop app. ❓
- [skeleton1231/zcode-my-go](https://github.com/skeleton1231/zcode-my-go) — Zgo — open-source desktop coding agent in pure Go (mygo native UI · ZCode-translated runtime · multi-provider) 🪟 🐧 · MIT


## 🛠 Developer Tools

- [hyoban/peek](https://github.com/hyoban/peek) — A native Git diff viewer: a Changes mode stacking diffs with the history, and a Files mode reading any file as the commit has it; changed files grouped into code, tests, docs and generated files and marked viewed, syntax-highlighted diffs in unified or side-by-side layout, step-through of every change, copy line references or GitHub links, comment from the gutter and copy the comments as an agent prompt, with Codex review findings shown under the lines they concern; several repositories in one window, plus branch switching and PR checkout via the GitHub CLI. 🍎 `55★` · MIT
- [Binaryify/MyGit](https://github.com/Binaryify/MyGit) — Check your agent's changes, fast. A light, native git client for macOS, Windows and Linux, built with MyGo. 🍎 🪟 🐧 · MIT [Website](https://binaryify.com/mygit/)
- [younland/apigo](https://github.com/younland/apigo) — A Hoppscotch-shaped API debugger: no frontend toolchain, no WebView — the UI and logic are all Go, one file, fully offline. 🍎 🪟 🐧 · MIT
- [fachrihawari/omaterm](https://github.com/fachrihawari/omaterm) — Oh My Terminal: a terminal workspace for running coding agents side by side. 🍎 🪟 🐧 · MIT [Website](https://fachrihawari.github.io/omaterm/)
- [saanuregh/dgopher](https://github.com/saanuregh/dgopher) — Fast, native database GUI: a SQL client for PostgreSQL, MySQL, ClickHouse, SQLite and DuckDB, and a Redis client. One Go binary, no Electron. Linux, macOS and Windows. 🍎 🪟 🐧 · Apache-2.0
- [cainiao524/hd2-font-maker-go](https://github.com/cainiao524/hd2-font-maker-go) — A Windows tool that generates Helldivers 2 font-replacement mods from your own fonts, in 14 UI languages. 🪟 · MIT
- [laojianzi/aster](https://github.com/laojianzi/aster) — A native Kubernetes workbench built with Go and MyGo Native UI. 🪟 · Apache-2.0
- [CarlOpenLab/Gloss](https://github.com/CarlOpenLab/Gloss) — Git client built for reviewing diffs: inline risk scan, topology graph, AI commit messages. Pure Go, GPU-rendered, zero WebView. macOS · Windows · Linux. 🍎 🪟 🐧 · MIT [Website](https://carlopenlab.github.io/Gloss/)
- [preceeder/gui-redis](https://github.com/preceeder/gui-redis) — redis cli support mac, windows 🍎 🪟
- [blyrin/java-ide](https://github.com/blyrin/java-ide) — A Java IDE with the MyGo native UI: project management, editor, build and run. ❓
- [hunghg255/mycode](https://github.com/hunghg255/mycode) — A small, fast code editor written in Go. It draws a native UI on the GPU with 🍎 🪟 🐧 · MIT [Website](https://docs-mu-roan.vercel.app)
- [smallnest/nutty](https://github.com/smallnest/nutty) — A native macOS terminal: a Go + MyGo recreation of otty.sh, built on the uix and onevra component libraries. 🍎 · Apache-2.0
- [tiramission/oci-sync](https://github.com/tiramission/oci-sync) — Sync local files or directories to OCI-compatible image registries 🍎 🪟 🐧 · MIT [Website](https://tiramission.github.io/oci-sync/)
- [oshell-desktop/oshell-desktop](https://github.com/oshell-desktop/oshell-desktop) — OShell Desktop — shared Go core and native desktop UI 🪟 🐧 · GPL-3.0
- [pteich/repo-hopper](https://github.com/pteich/repo-hopper) — Quickly navigate and open your recently changed Git repos with a native app. 🍎 🪟 🐧 · MIT
- [javatoai/silverwing](https://github.com/javatoai/silverwing) — A compact native multi-repo dev workbench in Go + MyGo (no WebView, no Electron), ~18 MB installer. 🍎 🪟 · MIT
- [version-fox/vfox-plus](https://github.com/version-fox/vfox-plus) — Experimental Web UI and cross-platform desktop application for the vfox CLI. 🐧 · Apache-2.0
- [tacshi/Yeek](https://github.com/tacshi/Yeek) — A native, cross-platform API client for HTTP, GraphQL, gRPC and WebSocket, written entirely in Go. 🍎 🪟 · MIT
- [CairnPack/Codei18nDesktop](https://github.com/CairnPack/Codei18nDesktop) — Codei18n's graphical user interface window, based on mygo 🪟 · MIT
- [congthien2003/dbl](https://github.com/congthien2003/dbl) — SBDb brings connection management, database exploration, table inspection, and data editing into a focused desktop workspace. Built with Go and MyGo Native UI, it follows a simple 🍎 🪟 🐧
- [my3rs/GoShell](https://github.com/my3rs/GoShell) — A lightweight cross-platform desktop SSH terminal and host manager in Go + MyGo. 🍎 🪟 🐧
- [zty012/guart](https://github.com/zty012/guart) — A Go serial-port tool in MyGo native UI + MujicaUI; no WebView, no cgo. 🪟 [Website](guart.2y.nz)
- [shenjing023/KLineChart-go](https://github.com/shenjing023/KLineChart-go) — KLineChart for go ❓ · MIT
- [ftech-vn/kubedesk](https://github.com/ftech-vn/kubedesk) — A fast, light Kubernetes desktop client for people who juggle many clusters: live resources, logs, shells, a watchlist with notifications, a timeline of changes and production guardrails. 🍎 · MIT [Website](https://kubedesk.cloud/)
- [zhengchalei/MQTT-Desktop](https://github.com/zhengchalei/MQTT-Desktop) — A lightweight MQTT desktop client: multiple connections, MQTT 3.1.1/5.0, subscribe/publish and history. 🪟
- [ca-x/nvflasher](https://github.com/ca-x/nvflasher) — nvflasher: a MyGo desktop app for flashing and provisioning NVIDIA Jetson devices (Linux flashing backend). 🐧 🕸 · MIT
- [nyakang/nyadb](https://github.com/nyakang/nyadb) — NyaDB: a cross-platform native database workbench for organizing connections and working with SQL. 🍎 🪟 🐧
- [flowprog/png2ico](https://github.com/flowprog/png2ico) — A PNG-to-ICO converter built with MyGo native, with GUI and command-line versions. The entire interface is written in Go. 🪟 · MIT
- [a8b7/Rubick](https://github.com/a8b7/Rubick) — Docker container management platform with Web UI 🍎
- [bernylinville/seismic](https://github.com/bernylinville/seismic) — A native macOS Elasticsearch client — a ground-up native rewrite of elasticvue with feature parity (13 modules), pure Go, no cgo, no WebView. 🍎
- [jinghaihan/sift](https://github.com/jinghaihan/sift) — Review complete feature branches without unrelated integration changes. 🍎 🪟 🐧 · MIT
- [Moonvy/UPX-Installer-GO](https://github.com/Moonvy/UPX-Installer-GO) — Adobe UPX/CEP Extension Installer, Windows/macOS app. 🍎 🪟 🐧
- [gantrol/YouRun](https://github.com/gantrol/YouRun) — Manage local project commands from a desktop app or CLI. Built with Go, MyGo and React. 🍎 🪟 🕸 · Apache-2.0 [Website](https://apps.microsoft.com/store/detail/9MWXXGC8H67D?cid=DevShareMCLPCS)


## 🌐 Network · Proxy · Remote

- [AstraFoundry/KumoApp](https://github.com/AstraFoundry/KumoApp) — A calm, native macOS client for the Mihomo proxy core, built with SwiftUI and a shared agent-friendly CLI. 🍎 🕸 `295★` · AGPL-3.0 [Website](https://usekumo.app)
- [lufficc/clash-traffic](https://github.com/lufficc/clash-traffic) — See where your Clash Verge traffic goes — by app, site, proxy node, subscription and device. 🍎 🪟 `42★`
- [Licoy/CPA-Bar](https://github.com/Licoy/CPA-Bar) — Keep an eye on your CLIProxyAPI servers from the menu bar. 🍎 🪟 🐧 · AGPL-3.0
- [xiaomai1011/GZIST-NetKeeper](https://github.com/xiaomai1011/GZIST-NetKeeper) — Campus-network auto-login keeper for GZIST: adapts to the new Dr.COM/eportal portal, auto-reconnects, autostarts, runs in background. 🍎 🪟 🐧 [Website](https://xiaomai1011.github.io/GZIST-NetKeeper/)
- [hygkui/v5vpn-rea-client](https://github.com/hygkui/v5vpn-rea-client) — Unofficial Go + MyGo desktop client for LeadSec V5VPN SSL VPN portals (protocol v2.0) 🍎 🪟 🐧 · Apache-2.0
- [xiaomai1011/GZIST-DormSignin-Baiyun](https://github.com/xiaomai1011/GZIST-DormSignin-Baiyun) — Dorm sign-in client for GZIST Baiyun campus; Go + MyGo, Windows x64. 🪟
- [marukolibro/Hop](https://github.com/marukolibro/Hop) — A native macOS and Windows proxy client for mihomo (Clash.Meta). Built in Go with MyGo, no webview. 🍎 🪟 · GPL-3.0 [Website](https://marukolibro.github.io/Hop/)
- [si-mods/MyVNC](https://github.com/si-mods/MyVNC) — Pure Go VNC viewer for Windows built with MyGo, ported from TigerVNC 🪟 · GPL-2.0
- [RedwindA/gotify-desktop](https://github.com/RedwindA/gotify-desktop) — A receive-only desktop client for Gotify. Works on macOS, Windows and Linux 🍎 🪟 🐧 · GPL-3.0
- [xiaomai1011/GZIST-Hotspot](https://github.com/xiaomai1011/GZIST-Hotspot) — Turns campus wired network into a hotspot: one-click toggle, auto anti-disconnect, NIC adaptation. 🪟 · MIT
- [moxuun/sing-box-drover-go](https://github.com/moxuun/sing-box-drover-go) — A tray controller for sing-box — the Go rewrite of sing-box-dover, supporting ref1nd-style providers. 🍎 🪟 🐧 · MIT
- [Sakurasan/ClashX-Go](https://github.com/Sakurasan/ClashX-Go) — A macOS menu bar proxy client modeled closely on ClashX 🍎 · AGPL-3.0
- [Binaryify/proxy-bridge](https://github.com/Binaryify/proxy-bridge) — A macOS menu-bar tool that routes all or per-app traffic into HTTP/HTTPS/SOCKS5 proxies over TUN. 🍎 · GPL-3.0
- [jiqing112/frpcclient](https://github.com/jiqing112/frpcclient) — A graphical frp client manager for Windows 10/11: edit frpc TOML visually and start/stop the process. 🪟
- [Fan-chou/magpie-native-routing](https://github.com/Fan-chou/magpie-native-routing) — A standalone native client for observing Magpie's real routing behavior. 🍎 🪟
- [jnnbimo/RayDock](https://github.com/jnnbimo/RayDock) — A Windows Xray client in Go + MyGo: native glass UI, TUN, proxy chains and dedicated ports. 🪟 · MIT
- [logdns/Win-XinAi-De-Tools](https://github.com/logdns/Win-XinAi-De-Tools) — A native Windows network toolbox: firewall, network config, SMB, WSL and a temporary HTTP server; bilingual, light/dark themes. 🪟 · MIT


## 🗂 Storage · Files · Sync

- [pteich/us3ui](https://github.com/pteich/us3ui) — 🗂️ Universal Cross-Platform native s3 Object Storage GUI and FileManager 🍎 🪟 🐧 `36★` · MIT [Website](https://us3ui.pteich.de)
- [DejavuMoe/Pail](https://github.com/DejavuMoe/Pail) — Cross-platform desktop manager for S3-compatible object storage: Amazon S3, MinIO, Cloudflare R2, VersityGW, Wasabi and other services that speak the S3 API. 🍎 🪟 🐧 `30★` · MIT [Website](https://pail.download)
- [Nigh/ReSoBackup](https://github.com/Nigh/ReSoBackup) — Reed-Solomon erasure-coding backup with AES-256 encryption, in both GUI and CLI. 🍎 🪟 🐧 · LGPL-2.1
- [vfasky/mygo-vaultwarden](https://github.com/vfasky/mygo-vaultwarden) — Your Vaultwarden, native on your Mac 🍎 [Website](https://mygo-vault.vfasky.com)
- [echoVic/cleanzo](https://github.com/echoVic/cleanzo) — A safety-first macOS cleaner: junk rules, space analysis, large files, similar photos and app uninstalling. 🍎 🪟 🕸 · MIT [Website](https://cleanzo.echovic.com/)
- [younland/RcloneDrive](https://github.com/younland/RcloneDrive) — Mounts 70+ rclone storage backends as local drives in MyGo native UI: single binary, no WebView, tray, auto-update — an open-source RaiDrive alternative. 🍎 🪟 🐧 · MIT
- [Magnetkopf/aim](https://github.com/Magnetkopf/aim) — Love ur AppImage. 🐧 · GPL-3.0 [Website](https://aim.magnetkopf.com)
- [DiiKhanh/burrow](https://github.com/DiiKhanh/burrow) — Burrow is a free, open-source macOS app (Apple Silicon) that frees disk space and shows the live health of your Mac. 🍎 · GPL-3.0
- [michaelmjhhhh/Chaos](https://github.com/michaelmjhhhh/Chaos) — handling macOS screenshots 🍎 · MIT
- [ychuo/copiggy](https://github.com/ychuo/copiggy) — Copiggy is a native clipboard companion for macOS. Browse what you copied, keep useful clips, and prepare content before pasting. 🍎
- [aouyitanaka/Fsearch-Mygo-GUI](https://github.com/aouyitanaka/Fsearch-Mygo-GUI) — A native desktop front end for fsearch, 🍎
- [lfcypo/pickphoto](https://github.com/lfcypo/pickphoto) — Quick photo sorting and organizing. 🍎 🪟 · MIT
- [Eurekaimer/TOUKO](https://github.com/Eurekaimer/TOUKO) — TOUKO treats image management as tree-oriented repository operations instead of individual file uploads. 🍎 🪟 🐧 🕸 · MIT
- [zachzhao1984/bucketeer](https://github.com/zachzhao1984/bucketeer) — A native macOS client for Cloudflare R2 and S3-compatible storage, built with Go and MyGo. 🍎 🪟
- [1e4DouWine/clipboard_go](https://github.com/1e4DouWine/clipboard_go) — A simple clipboard tool written in Go with MyGo native UI. ❓
- [viewhang/go_paste](https://github.com/viewhang/go_paste) — A clipboard manager for macOS and Windows, built with Go and MyGo. 🍎 🪟 · MIT
- [HycJack/mygo-tendedero](https://github.com/HycJack/mygo-tendedero) — Tendedero screenshot-line app, ported from SwiftUI/AppKit to MyGo (Go) 🍎 🪟 🐧
- [logdns/newtofile](https://github.com/logdns/newtofile) — Native macOS Finder file creation utility built with Go/MyGo and Swift 🍎 · MIT
- [ZeroDevi1/nomo-mygo](https://github.com/ZeroDevi1/nomo-mygo) — Nomo rewritten on MyGo (Go desktop shell) 🍎 🪟 🐧 · AGPL-3.0
- [Prit36/quarry-disk-analyzer](https://github.com/Prit36/quarry-disk-analyzer) — Quarry: a fast, native Windows disk space analyzer in Go. Direct NTFS MFT reading, Explorer-style tree, powerful search, synchronized treemap. 🪟 · MIT
- [thedavidweng/rainforest](https://github.com/thedavidweng/rainforest) — Rainforest — Unofficial cross-platform desktop backup and transfer client for Amazon Photos 🍎 🪟 🐧 · AGPL-3.0 [Website](http://rainforest.blahaj.uk/)
- [huynhkinhao1910/scan-image](https://github.com/huynhkinhao1910/scan-image) — Finder và Spotlight tìm rất chậm trên ổ mạng SMB, vì mỗi lần tìm lại phải hỏi server. Scan Image quét cây thư mục một lần, giữ index trong RAM và lưu trên máy, rồi chỉ quét lại nhữ 🍎
- [zachzhao1984/twintrail](https://github.com/zachzhao1984/twintrail) — A native dual-pane macOS file manager built with Go and myGO. 🍎
- [mcxen/WinExplorer](https://github.com/mcxen/WinExplorer) — A pure-native file manager visually aligned with the Windows 11 Explorer; icons and thumbnails drawn on the GPU by Go. 🍎 🪟 🐧


## 🎵 Media · Players · Download

- [fzn0x/mixmusic](https://github.com/fzn0x/mixmusic) — MixMusic: Spotify and YouTube Music in one player. Open-source desktop music player for macOS, Windows & Linux: one search, one queue, mixed playlists, synced lyrics, and equalizer with community them 🍎 🪟 🐧 `110★` · MIT [Website](https://fzn0x.github.io/mixmusic/)
- [vst93/bili-fm](https://github.com/vst93/bili-fm) — Listen to Bilibili as audio — a player or study tool built natively in Go + mygo for Windows, macOS and Linux. 🍎 🪟 🐧 `66★` · Apache-2.0
- [missuo/motrix-mygo](https://github.com/missuo/motrix-mygo) — Motrix with a native Go UI on MyGo, driving the aria2 engine Motrix ships. No Electron, no webview. 🍎 🪟 `55★`
- [elianiva/meiro](https://github.com/elianiva/meiro) — Lightweight Youtube Music client in MyGo!!!!! 🍎 🪟 🐧 `35★` · GPL-3.0
- [j4ckxyz/Aurelia](https://github.com/j4ckxyz/Aurelia) — A fast, native music player for Jellyfin (macOS, Windows, Linux), built with MyGo 🍎 🪟 🐧 · MIT
- [hackerlengyue/binggan](https://github.com/hackerlengyue/binggan) — A local video toolkit: key extraction and management, course playback scheduling, batch decryption and asset management (MyGo + Vue). 🍎 🪟 🕸 · GPL-3.0
- [owocc/bowerbird](https://github.com/owocc/bowerbird) — Bowerbird is a cross-platform desktop digital asset manager built with **mygo (Go)** in webview mode and **React 19 + TypeScript + Tailwind CSS v4**. The desktop shell migrated fro 🍎 🪟 🐧 🕸
- [xptea/curb](https://github.com/xptea/curb) — A minimal native video and audio downloader. Paste a link, choose video or MP3 audio and a quality, then save the file locally. No WebView No Electron 🍎 🪟 🐧 · MIT [Website](https://curb.seths.app)
- [biaobiaobiao108/fnmovie](https://github.com/biaobiaobiao108/fnmovie) — Brings your fnOS movie library to the Windows desktop. 🪟 [Website](https://biaobiaobiao108.github.io/fnmovie/)
- [freelxs/jstv-player](https://github.com/freelxs/jstv-player) — A macOS player for the JSTV / CatPawOpen streaming protocol. 🍎 🪟 🐧 🕸 · MIT
- [ZypherChan/MusicComments](https://github.com/ZypherChan/MusicComments) — Desktop app for random NetEase Cloud Music hot comments; Windows x64 and Linux x64 builds. 🪟 🐧
- [rzh0504/Qmdr](https://github.com/rzh0504/Qmdr) — 🎵 QQmusic/Playlist Downloader 🍎 🪟 🐧 · GPL-3.0
- [Team-Quaver/quaver-astra](https://github.com/Team-Quaver/quaver-astra) — A lightweight, cross-platform Quaver Music client with a native-like experience. built by MyGO 🍎 🪟 🐧 · AGPL-3.0
- [fazi-gondal/video-downloader-mygo](https://github.com/fazi-gondal/video-downloader-mygo) — Native desktop video downloader built with Go, MyGo, yt-dlp, and FFmpeg. The application analyzes videos and playlists, lets users choose quality, audio, subtitles, and containers, manages downloads i 🍎 🪟 🐧 · MIT
- [myoula/ape-player](https://github.com/myoula/ape-player) — emby player on omarchy 🐧
- [steampixel007/Dipper](https://github.com/steampixel007/Dipper) — A native anime-following desktop app built on MyGo Native UI + Go: Mikan catalog, RSS and a built-in BT downloader. 🍎 🪟 🐧
- [XueJie1/godrome](https://github.com/XueJie1/godrome) — A lightweight native desktop music player for your own Navidrome / Subsonic library. 🍎 🪟 🐧 · MIT
- [jyuuroku16/mediago](https://github.com/jyuuroku16/mediago) — A native, high-performance macOS media sniffer and downloader written in Go with MyGo's native UI 🍎
- [HycJack/mujicacut](https://github.com/HycJack/mujicacut) — CapCut-style desktop video editor, GPU-drawn with MyGo + MujicaUI — no WebView, no HTML/JS ❓
- [yaffalhakim1/playlist](https://github.com/yaffalhakim1/playlist) — A native desktop player for YouTube playlists. MyGo, Onevra, Inter. No webview. 🍎 🪟 🐧 [Website](https://yaffalhakim1.github.io/playlist/)
- [fazi-gondal/video](https://github.com/fazi-gondal/video) — A feature-rich video player built with the MyGo 🪟
- [Shirolin/videopress](https://github.com/Shirolin/videopress) — A good-looking Windows video compressor, GUI + CLI. 🪟 · MIT
- [Alpenl/wallpaper](https://github.com/Alpenl/wallpaper) — Cross-platform live wallpaper MVP: native transcoding and per-app rules on macOS; Windows/Linux take a compatibility route. 🍎 🪟 🐧


## ⚡ Productivity · Menu Bar · Launchers

- [henryyu333/shelf](https://github.com/henryyu333/shelf) — A native macOS app built entirely in Go with the MyGo framework 🍎 `51★` · MIT
- [egoist/uma](https://github.com/egoist/uma) — A native menubar app for Umami.is 🍎 🪟 🐧 `41★`
- [eziq1/golauncher](https://github.com/eziq1/golauncher) — A Raycast-style launcher for Windows and macOS, written in Go with the MyGo native UI toolkit 🍎 🪟 · MIT
- [iwangjie/xiangzhuan](https://github.com/iwangjie/xiangzhuan) — A menu-bar break reminder: when time is up, a stick of incense burns fullscreen; when it burns out, back to work. 🍎 🪟 · MIT
- [tacshi/Unscan](https://github.com/tacshi/Unscan) — Make scanned PDFs searchable, or retype them into clean text PDFs, entirely on your own machine. A macOS app and CLI in Go, without cgo, using PaddleOCR's PP-OCRv6. 🍎 · MIT
- [0froq/snip](https://github.com/0froq/snip) — Minimal macOS clipboard manager prototype built with MyGo **native UI** (`ui` package, no webview). Each new plain-text copy spawns a small floating card. Global shortcuts show/hid 🍎 · MIT
- [ychuo/tavu](https://github.com/ychuo/tavu) — Tavu is a native macOS workspace for running your tools, editing files, and reviewing changes in one place. Written in Go with MyGo. 🍎
- [zyition/voke](https://github.com/zyition/voke) — Voke — a Windows launcher. 🪟 · MIT
- [gomeen/Zakki](https://github.com/gomeen/Zakki) — A macOS / Windows scratchpad: several colored tags each holding a snippet of Markdown. 🍎 🪟 · MIT
- [diver80/avono-timebooking](https://github.com/diver80/avono-timebooking) — Zeitplanung und Achievo-Buchung für macOS – Woche/Tag/Monat, Jira-Tickets im Funnel, Kalender, Menüleiste (Go + MyGo) 🍎
- [soidaken/ClipRecorder](https://github.com/soidaken/ClipRecorder) — Native Windows screenshot / screen-record / selection-translate tool: local OCR + DeepSeek, no WebView. 🪟 · MIT
- [Star-Trails/countdowner](https://github.com/Star-Trails/countdowner) — A native Windows desktop countdown widget built with Go and MyGo. 🪟
- [zephyr-qu/kanso](https://github.com/zephyr-qu/kanso) — A small personal kanban board: Go backend + React frontend + SQLite, single-port. 🪟 🕸
- [308K/my-doubtful-go](https://github.com/308K/my-doubtful-go) — SmartAR Desktop: accounts-receivable aging analysis and bad-debt early warning (MyGo + React 19 + Shadcn UI + an Excelize dynamic formula engine). 🍎 🪟 🐧 🕸 · MPL-2.0
- [feiniao233/MyCast](https://github.com/feiniao233/MyCast) — Windows launcher built with Go/MyGo 🪟
- [cecil-su/mygo-browser](https://github.com/cecil-su/mygo-browser) — Windows browser prototype with Go-native UI, MyGo and WebView2 🍎 🪟
- [m3hu1/mygo-todo](https://github.com/m3hu1/mygo-todo) — Personal todo plus notes macos menubar app built using mygo. 🍎
- [nerv-base/MyToolbox](https://github.com/nerv-base/MyToolbox) — A local, native, modular desktop toolbox that keeps daily chores light. 🍎 🪟 🐧 · AGPL-3.0
- [yinshuwei/mytools](https://github.com/yinshuwei/mytools) — A developer toolbox built with mygo UI. 🍎 🪟 🐧 · MIT
- [mintonight/pomodoro](https://github.com/mintonight/pomodoro) — A minimal desktop Pomodoro timer: focus timing, overtime-cancel, stats heatmap, system tray and local SQLite storage. 🍎 🪟 🐧
- [azzliang6/pomodoro-mygo](https://github.com/azzliang6/pomodoro-mygo) — A Pomodoro timer built with the pure-Go desktop framework MyGo. 🪟 · MIT
- [HanlunWang/simple-toggle](https://github.com/HanlunWang/simple-toggle) — Turn any script into a managed menu bar switch on macOS 🍎 · MIT
- [javatoai/sleepdock](https://github.com/javatoai/sleepdock) — Native Go and MyGo sleep timer with tray controls 🍎 🪟 🐧 · MIT
- [dandibbert/textrouter](https://github.com/dandibbert/textrouter) — TextSoap redesigned: one-click clipboard cleanup, readable find-and-replace, tabular batch replacement and visual action chains. 🍎
- [ctzcs/Timer](https://github.com/ctzcs/Timer) — An always-on-top desktop timer widget styled after physical visual timers: a 30-segment bar plus a seven-segment LCD. 🪟
- [m3hu1/tuck](https://github.com/m3hu1/tuck) — Personal todos and markdown notes in a tiny 3.8 MB package. Native macOS menu bar app: fast, light on resources, built with MyGo. 🍎


## 📊 System · Monitoring · Hardware

- [Binaryify/MonitorBar](https://github.com/Binaryify/MonitorBar) — Monitor management from the macOS menu bar / Windows tray: switches inputs and adjusts volume over the Xiaomi HyperOS LAN API, no DDC/CI needed. 🍎 🪟 `162★` · MIT
- [xbenduan/vitals](https://github.com/xbenduan/vitals) — A tiny macOS app that does exactly one thing well. 🍎
- [oneo-me/neohm](https://github.com/oneo-me/neohm) — macOS menu bar app for controlling Home Assistant devices, with full air conditioner controls. Built in Go with MyGo and Onevra. 🍎 🪟 🐧 [Website](https://oneo-me.github.io/neohm/)
- [qzz0518/Moniflip](https://github.com/qzz0518/Moniflip) — Flip a monitor to another computer over DDC/CI, from the macOS status bar / Windows tray. 🍎 🪟 · MIT
- [rayorole/orole-os-desktop](https://github.com/rayorole/orole-os-desktop) — Orole OS - your personal operating environment (Windows-native, MyGo + Go daemon + React) 🪟 🕸 · MIT
- [e1roy/stage-manager-for-windows](https://github.com/e1roy/stage-manager-for-windows) — macOS-style Stage Manager for Windows 10/11: keep the current app on stage and group the rest into a sidebar, one per monitor. Pure Go, no cgo, no WebView. 🪟 · MIT
- [wan-kong/apex-helper](https://github.com/wan-kong/apex-helper) — Disables the keys that ruin your aim — yes Apex, that's you. 🪟
- [VeinsureLee/BYR-Client](https://github.com/VeinsureLee/BYR-Client) — A local desktop client for the BYR BBS forum; Go logic + MyGo native UI, Windows first. 🪟
- [villatothesea/DumpingGround](https://github.com/villatothesea/DumpingGround) — Windows-native maintenance utility — process viewer, disk-usage analyzer, safe cleanup with recycle-bin and backup guarantees 🪟 · MIT
- [sugarbearr/gogo-explorer](https://github.com/sugarbearr/gogo-explorer) — gogo-explorer is a from-scratch, opinionated take on the Windows Task Manager. There is no sidebar and no tab bar: the process table **is** the main screen. Select a row and a deta 🪟 · MIT
- [oscs1024-pixel/MiJia](https://github.com/oscs1024-pixel/MiJia) — A cross-platform Mijia smart-home control center rebuilt from scratch with MyGo GPU native UI; macOS menu-bar flyout, no HTML/WebView. 🍎 🪟 🐧
- [fondoger/mouse-mapper](https://github.com/fondoger/mouse-mapper) — A quiet mouse side-button remapper for Windows and macOS, built entirely with MyGo Native UI. 🍎 🪟 · MIT
- [17130239-coder/Pulse](https://github.com/17130239-coder/Pulse) — ⚡ Pulse — Native macOS System & Hardware Activity Monitor in Pure Go (via MyGo framework with GPU Metal rendering) 🍎
- [lesenelir/stock-float-mygo-native](https://github.com/lesenelir/stock-float-mygo-native) — A tiny always-on-top macOS panel for live stock prices, in pure Go with MyGo native UI (no webview) 🍎 · MIT


## 🎮 Games · Fun

- [zrcoder/ndor](https://github.com/zrcoder/ndor) — Draw with codes, for kids and coders~ ❓ · MIT [Website](https://ndor.netlify.app)
- [CBR0/calc](https://github.com/CBR0/calc) — A Windows 11-style desktop calculator written in pure Go and drawn natively 🪟 🐧 · MIT
- [zhengchalei/LeagueAkari-MyGo](https://github.com/zhengchalei/LeagueAkari-MyGo) — A lightweight CN-server LoL match & draft helper ported from LeagueAkari; MyGo + WebView2, optimized memory, on-demand queries. 🪟 · MIT
- [zrcoder/ttoy](https://github.com/zrcoder/ttoy) — Dev toys on the terminal 🍎 · MIT
- [li-yifei/bdon-mygo](https://github.com/li-yifei/bdon-mygo) — A desktop accelerator for BanG Dream! Our Notes deck building: native multithreaded solving plus one-tap ADB save import. 🍎 · MIT [Website](https://bdon.moe/tools/deck)
- [tortoise10h/calculus](https://github.com/tortoise10h/calculus) — A calculator built with Golang MyGo Native 🍎 🪟 🐧
- [ZeroDevi1/gamesave-manager](https://github.com/ZeroDevi1/gamesave-manager) — A MyGo-based game-save manager: back up, restore and organize local saves. 🪟 🕸
- [Eslzzyl/krkrgo](https://github.com/Eslzzyl/krkrgo) — Modern krkrz emulator in pure Go (WIP) 🍎 🪟 🐧
- [Yurbin/mygo-snake](https://github.com/Yurbin/mygo-snake) — Desktop Snake game in MyGo native UI; portable, no install, tested on Kylin V10 SP1. 🐧
- [BabyLy233/MyLock](https://github.com/BabyLy233/MyLock) — A mod manager for the game Deadlock, as a native Go + MyGo desktop app. 🍎 🪟 🐧 · MIT
- [ch1y1z1/xiangqi_go](https://github.com/ch1y1z1/xiangqi_go) — Desktop Chinese-chess endgame explorer: local setup, branch study and offline Pikafish AI. 🍎 🪟 🐧 · GPL-3.0

## Component Libraries · Templates · Framework Add-ons

> Not apps themselves: component libraries, theme packs and app templates built on MyGo — all pure-Go source packages.

- [egoist/mygo](https://github.com/egoist/mygo) — The MyGo framework itself: desktop apps in Go, mixing Go-drawn native UI and system WebView pages in one window; pure Go without cgo, one command ships macOS/Windows/Linux installers. 🍎 🪟 🐧 `2852★` · MIT [Website](https://mygo.egoist.dev)
- [oneo-me/onevra](https://github.com/oneo-me/onevra) — Native desktop components on MyGo: themed controls, window shells, Lucide icons, plus chat, Markdown, code highlighting, charts and a command palette — with a standalone tri-platform packager. 🍎 🪟 🐧 `252★` · MIT [Website](https://oneo-me.github.io/onevra/)
- [smallnest/uix](https://github.com/smallnest/uix) — A shadcn/ui-style component library for MyGo's native UI toolkit — import a component as a normal Go package. 🍎 🪟 🐧 · MIT
- [ELY-Open-Source/CrychicUI](https://github.com/ELY-Open-Source/CrychicUI) — 1500 components for MyGo native UI in MyGo's own look, with motion and sound. 🍎 🪟 🐧 · MIT
- [ELY-Open-Source/MujicaUI](https://github.com/ELY-Open-Source/MujicaUI) — Court-gothic components for MyGo native UI. 🍎 🪟 🐧 · MIT
- [ELY-Open-Source/8bitMyGoUI](https://github.com/ELY-Open-Source/8bitMyGoUI) — 16-bit pixel-art components for MyGo native Go UI; the showcase runs the same Go in the browser via WASM. 🍎 🪟 🐧 · MIT
- [firede/mygo-platinum](https://github.com/firede/mygo-platinum) — Classic desktop controls for MyGo. 🍎 🪟 🐧 · MIT [Website](https://mygo-platinum.firede.com)
- [mcxen/GodGo](https://github.com/mcxen/GodGo) — A MyGo app shell: sidebar, settings, workflows and signed auto-updates. 🍎 🪟 🐧
- [LoTwT/lucia](https://github.com/LoTwT/lucia) — A desktop app foundation on MyGo native UI: local dev, packaging, GitHub releases and signed auto-updates all wired up. 🍎 🪟 🐧
- [harukizmoe/mayu](https://github.com/harukizmoe/mayu) — A Material Design 3 (Material You) component library for MyGo's native GPU UI, in pure Go. 🍎 🪟 🐧 · MIT
- [HycJack/MintUI](https://github.com/HycJack/MintUI) — A native component library and gallery built on MyGo: 22 packages, no WebView, pure Go without cgo. 🍎 🪟 🐧
- [addidotlol/mycn](https://github.com/addidotlol/mycn) — shadcn/ui-style components for MyGo Native UI; call `mycn.Use` each frame to theme. 🍎 🪟 🐧
- [yldm-tech/mygo-breeze-ui](https://github.com/yldm-tech/mygo-breeze-ui) — Tailwind-inspired typed native UI components, utilities, CLI and MCP tools for MyGo. 🍎 🪟 🐧 · MIT [Website](https://yldm-tech.github.io/mygo-breeze-ui/)
- [HyperGrapher/mygo-desktop-webgl-app](https://github.com/HyperGrapher/mygo-desktop-webgl-app) — An experimental MyGo WebView + WebGL app template. 🍎 🪟 🐧
- [auron-labs/mygo-framework](https://github.com/auron-labs/mygo-framework) — A source-first framework and reference app for local-first MyGo apps: app layout, SQLite/GORM, Goose migrations, validation, explicit DI, structured logging, typed settings, OS secrets, generators and optional MCP tools. 🍎 🪟 🐧 🕸
- [xingkaixin/mygo-native-ui](https://github.com/xingkaixin/mygo-native-ui) — Native UI components for MyGo. 🍎 🪟 🐧 · MIT
- [baoziv587/mygo-template](https://github.com/baoziv587/mygo-template) — A MyGo app starter template (bilingual). 🍎 🪟 🐧
- [Cyenoch/mygoicons](https://github.com/Cyenoch/mygoicons) — Typed Iconify collections and a generator for MyGo native UI: lazy SVG caching and linker removal of unused icons. 🍎 🪟 🐧 · MIT
- [Cyenoch/mygoui](https://github.com/Cyenoch/mygoui) — Native Go UI components for MyGo with a shadcn-inspired style. 🍎 🪟 🐧 · MIT
- [ydongy/template-mygo-app](https://github.com/ydongy/template-mygo-app) — A pure-Go native desktop app template with initialization, localization, tests and packaging. 🍎 🪟 🐧 · MIT

## Legend

| Mark | Meaning |
| --- | --- |
| 🍎 | macOS build available (per GitHub Releases assets or README) |
| 🪟 | Windows build available |
| 🐧 | Linux build available |
| ❓ | No clear platform signal found; build from source |
| 🕸 | WebView mode: Go backend + web frontend |
| (no 🕸) | Mostly pure-Go native UI, GPU-drawn by MyGo (a few unconfirmed) |

Platform marks come from recent Release asset names and README statements (official sites for closed-source apps) and may not perfectly match reality — corrections welcome via Issues or PRs.

## Contributing

- New entries must actually depend on `github.com/egoist/mygo` in `go.mod` (or reference `github.com/egoist/mygo/cmd/mygo` as a `tool`); forks and mirrors are not listed separately.
- Closed-source apps are limited to the framework author's or officially endorsed projects, with their official site noted.
- One-line descriptions should say *what it is* — ideally with a well-known tool to compare against — not a list of technologies.
- Fill platform marks from Releases assets or official README statements; single-platform apps are welcome too.
- Follow the [awesome](https://github.com/sindresorhus/awesome) contribution guidelines: only public, runnable projects with a source repository (see above for closed-source).

## License

[![CC0](https://licensebuttons.net/p/zero/80x15.png)](https://creativecommons.org/publicdomain/zero/1.0/)

This list is released under CC0 — to the extent legally possible, all copyright and related rights are waived. Each app keeps its own license, noted per entry.
