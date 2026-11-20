<div align="center">

# Paul (hmj1026)

**Harness 工程架構 · 自主 Agent 系統開發 · 高韌性後端生態**

*打造可重現的 AI Agent 執行環境、具備驗證審查的知識建置管線，以及隱私優先的個人自動化系統。*

[![GitHub followers](https://img.shields.io/github/followers/hmj1026?style=flat-square&color=2563EB)](https://github.com/hmj1026)
[![GitHub stars](https://img.shields.io/github/stars/hmj1026?style=flat-square&color=F59E0B)](https://github.com/hmj1026?tab=repositories)
[![Packagist Version](https://img.shields.io/packagist/v/hmj1026/devkit?style=flat-square&color=10B981&label=devkit%20on%20packagist)](https://packagist.org/packages/hmj1026/devkit)
[![skills.sh](https://img.shields.io/badge/skills.sh-verified%20skills-6366f1?style=flat-square)](https://skills.sh/hmj1026)

[English](README.md) · [繁體中文](README.zh-TW.md)

</div>

---

### 💡 核心技術哲學

> **「以 Harness 環境架構為本，而非單純的提示詞調校 (Harness engineering over prompt engineering)。」**

面對新一代自主 AI Agent，與其不斷微調脆弱且難以重現的單次 Prompt，我的工程實踐專注於**為 Agent 構建具備嚴格約束與反饋機制的執行環境（Harness）**。透過執行時 Hook 攔截、多角色審查派發（Advisory Reviewer Dispatch）、有界技能流程（Bounded Skills）以及確定性的驗證閘門，讓 AI 模型在複雜的軟體工程生命週期中始終保持紀律與高精準度。

無論是設計跨編輯器的 Agent 插件、建構具備權威引用的結構化知識庫，或維護跨越 19 組版本矩陣的企業級 PHP/Laravel 生態，「**可重現性、零幻覺驗證、極致的架構韌性**」是我不變的研發基準。

---

### 🤖 AI Agent 架構與開發者基礎建設

> 將原始大語言模型轉化為專業、有紀律之生產力協作者的核心工具鏈。

| 專案 | 說明 | 技術棧 / 領域 |
| :--- | :--- | :--- |
| [**dhpk**](https://github.com/hmj1026/dhpk) | **Claude Code 專用開發 Harness 插件（Dev Harness Plugin Kit）。** 開箱即用的架構框架，內建 **33 位角色專用 Agent**、31 個可選技術棧模組（涵蓋 PHP、Yii、Laravel、Vue、React、Next.js、Python、Swift）、執行時 Wrapper 鉤子模型、顧問型審查派發、跨 Session 學習資料庫與 Codex CLI 投影映射。 | `JavaScript` `Claude Code Plugin` `Harness` |
| [**notebooklm-course-builder**](https://github.com/hmj1026/notebooklm-course-builder) ⭐ `13` | **Google NotebookLM 專業建課 Agent 技能。** 透過嚴謹的 **14 階段工作流**，將粗略課綱轉化為具備權威引用的完整教材。支援瀏覽器自動化與逐步嚮導保底機制，嚴格區隔研究提示詞與筆記來源，堅持「最小充分來源集」拒絕 SEO 農場文。已發布於 [skills.sh](https://skills.sh)。 | `JavaScript` `Agent Skill` `自動化` |
| [**claude-statusline**](https://github.com/hmj1026/claude-statusline) | **Claude Code 終端即時狀態列。** 在單行精簡介面中動態顯示當前模型與推論 Effort、上下文窗口消耗百分比（%）、5h / 7d 速率限制百分比與重設倒數、以及 Git 分支改動。透過獨立子進程外部執行，**完全不消耗 LLM Token**。 | `Shell` `Developer CLI` `Ergonomics` |
| [**bg-watch**](https://github.com/hmj1026/bg-watch) | **背景作業與 Agent 執行監控工具。** 為長時運行的單元測試、編譯構建及並行背景 Subagent 提供精簡且不干擾視線的終端即時進度監控。 | `TypeScript` `Terminal UI` |
| [**bug-investigation**](https://github.com/hmj1026/bug-investigation) | 建立假設驅動（Hypothesis-driven）診斷循環的 Agent 技能，專注於排查隱晦錯誤、狀態破壞與效能回退。 | `Shell` `Agent Skill` |
| [**home-assistant-helpers**](https://github.com/hmj1026/home-assistant-helpers) | 智慧家庭 Claude Code 擴充外掛，提供分階段 Lovelace 儀表板設計與建構技能（`ha-dashboard-studio`）。 | `Shell` `IoT` `Home Assistant` |

---

### 🔒 隱私優先與個人自動化系統

> 敏感金融與個人資料完全於本機封閉運算，端到端自動化無外洩風險。

- [**ccas**](https://github.com/hmj1026/ccas) — **信用卡自動化帳務管理系統（Credit Card Automation System）**：
  - 透過 Gmail OAuth 定期拉取並自動解密**台灣 7 大主流銀行**（中信、玉山、台新、聯邦、國泰、永豐、富邦）的加密 PDF 電子帳單。
  - 自動剖析交易細項，以優先級 Regex 與 100ms 防當超時機制執行智慧分類，永不覆蓋手動覆寫項目。
  - 提供本機 **REST API、React 現代化儀表板與 Telegram 互動機器人**，具備每月/各卡/各類別預算警示（80%、100%）與繳款截止日提醒。
  - 完全由 Docker Compose 本機部屬；內建 HMAC 簽章 Session、防止撞庫之限速機制與敏感資訊過濾日誌。
- [**Line_Parser**](https://github.com/hmj1026/Line_Parser) & [**line_parser_py**](https://github.com/hmj1026/line_parser_py) — 高效能 LINE 群組聊天記錄剖析器，將非結構化對話紀錄自動解析為可檢索、結構化的數據流。
- [**line-bot**](https://github.com/hmj1026/line-bot) — 支援即時事件派發、通知提醒與查詢互動的 LINE 機器人服務。

---

### 🧱 企業級後端工具庫與高可用架構

> 專注於長期維護性、清晰代碼邊界與嚴謹的多版本相容性保證。

- [**devkit**](https://github.com/hmj1026/devkit) ([Packagist `hmj1026/devkit`](https://packagist.org/packages/hmj1026/devkit)) — **通用型 PHP / Laravel 開發工具包（v1.0.0 穩定發行）**：
  - 框架無關（Framework-agnostic）的底層架構，整合 14 項常用生產級功能：Elasticsearch 模組、統一 HTTP Gateway、SMS 發送、審計日誌（Audit Log）、檔案上傳與 Google Chat 異常日誌記錄。
  - 經過 **19 組 CI 矩陣單元測試**嚴格驗證，跨越 **PHP 7.3 → 8.4** 與 **Laravel 6.x → 11.x**。
- [**notifier**](https://github.com/hmj1026/notifier) — 高可靠性網站與 API 服務健康監控、心跳檢查與異常即時通報系統。
- [**docker_run**](https://github.com/hmj1026/docker_run) — 解決跨系統相容性難題的標準化、可重現 Docker 容器開發環境配置。

---

### 🧰 技術領域與工具棧

<div align="center">

```
AI 與 Agent 架構：   Claude Code Plugins  ·  Agent Skills (skills.sh)  ·  MCP  ·  Harness Engineering
主要程式語言：       TypeScript / Node.js  ·  PHP 7.3 ~ 8.4  ·  Python 3.10+  ·  Shell (Bash/Zsh)
框架與生態系統：     Laravel 6~11  ·  React  ·  Vue  ·  SwiftUI  ·  Yii Framework
資料存儲與基建：     Docker & Compose  ·  Elasticsearch  ·  DuckDB  ·  MySQL  ·  Redis
工程品質與安全：     確定性驗證  ·  OAuth 2.0  ·  HMAC Auth  ·  19-Cell CI 測試矩陣
```

</div>

---

<div align="center">

<sub>Crafted with Architectural Rigor by Paul (hmj1026) · Taiwan</sub>

</div>
