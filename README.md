# Jev Radar 📡

### **The world's most comprehensive tracker of the Jev ecosystem** — independent whitepaper · live monitor · scanned every 3 hours

> **全网最全,没有之一 · The Most Complete.** If it was built with Jev, it's in this radar — 220+ documented cases, 108 confidence-graded registry entries, swept from 8 source classes including every major community directory.

> **Jev** is TypeSafe AI's first *System One* model (released **2026-09-15**): it never generates text. You send it unstructured state plus typed questions — **Noul** (yes/no probability), **Choice** (option distribution + confidence), **Score** (rubric rating) — and it returns calibrated, machine-consumable decisions in **70–500 ms** at **$0.042/M input tokens, output free**.

This repository tracks **what the world actually built with Jev** — every case verified against a primary source (repo, live demo, or embedded original tweet), organized, quantified, and kept current by automated monitoring plus manual deep scans.

> ### 🔬 Every project in this registry is verified, scanned, and carries a confidence score
> - **Scanned every 3 hours** — automated sweep of GitHub, X/Twitter and five community directories; changes are committed to this repo on every scan that finds something new
> - **Evidence-graded** — each entry carries a verification tier with a confidence value (see below)
> - **No hearsay** — claims without a primary source are rejected; author-reported numbers are labeled as such
> - 🧭 New to Jev? Start with the **[API 申请攻略 / Access Guide](./docs/jev-api-access-guide.zh.md)** — waitlist, expedite trick, and no-wait alternatives (OpenRouter / Netlify / OpenJev)

![status](https://img.shields.io/badge/monitor-active-brightgreen) ![cases](https://img.shields.io/badge/curated_cases-220%2B-blue) ![repos tracked](https://img.shields.io/badge/ecosystem_repos-500%2B-orange) ![cadence](https://img.shields.io/badge/scan_cadence-every_3_hours-blue) ![verified](https://img.shields.io/badge/evidence_graded-A%2FB%2FC_置信度-purple) ![guide](https://img.shields.io/badge/API_access_guide-included-success) ![license](https://img.shields.io/badge/CC_BY_4.0-content-green)

---

## 📊 The ecosystem, 4 days after launch

| Signal | Number |
|---|---|
| GitHub repos in the ecosystem | **~500** (539 → 718 search-count growth in 24h on day 4) |
| Total stars across ecosystem | **21,600+** |
| Cases documented in the casebook (with primary sources) | **220+** |
| Structured, confidence-graded registry entries | **108** (38 × A · 70 × B) |
| Star leaders | browser-use/jev-ultrafast (~6.0k★) · vercel/eve ships Jev as default eval model (5.3k★) · fast-jev-compaction (2.7k★) · SemIf open replica (1.6k★) |
| Open replicas / clones | **13+** (OpenJev, SemIf, jevlike, NanoJev, openjev-sglang, jeff, Kev…) |
| Aggregator directories born in 4 days | **8** (madewithjev.com, awesomejev.com, typesafeai.app, jevable.com, risetive.com/jev, …) |
| Community SDKs | **40+** languages/frameworks (Rust, Swift, Kotlin, Java, PHP, .NET, Elixir, Scala/ZIO, Haskell, Zig, Laravel, Rails, n8n…) |
| Platform adoptions | Vercel eve (default eval model), LanceDB reranker, LiteLLM pass-through, Pydantic AI model, Netlify + Vercel gateways, OpenRouter |

## 🔥 What people are actually using Jev for (ranked by density)

1. **Agent safety / supervision** (25+ projects) — a Jev "second pair of eyes" judging every tool call: irreversible? matches intent? reward-hacking? (`pi-warden` self-graded on 17k real calls: 88% of holds correct)
2. **Context compaction** — score every tool result, drop what's irrelevant (`winnow`'s recoverable stubs, `jev-pruner`, 2.7k★ `fast-jev-compaction`)
3. **Model routing** (10+ implementations) — `jev-codex-router` measured **−60% cost** on a 237-turn backtest
4. **Real-time browser / voice / game decision layers** — 7.1s flight search (`jev-ultrafast`), ~300ms/phrase voice control (`jev-voice-browser`), Pokémon/StarCraft/Tetris/Subway Surfers
5. **Content scoring & growth analytics** — SuperX virality scoring (61 questions/post, $0.0004), 724 ad teardown ($0.09), Every's editorial gate (<$0.01/1,709 judgments)
6. **Trading** — one decision per 300ms Monad block (`jev-trader`, 900+★); honest paper-trading data now public (375 trades, 41.1% win)
7. **Jev as SQL / system primitive** — pg-jev, vgi-typesafe (DuckDB), jevframe (pandas/Polars), zsh history, Neovim, Emacs
8. **Verticals arriving** — IRS tax forms (100% strict accuracy, 261 forms), federal MTD ruling prediction, PubMed screening, systematic-review extraction, Clay GTM workflows

## 🧪 Field-tested lessons (recurring, multi-source)

- **Input quality decides everything** — Jev needs narrow, mechanical questions ("LLMs survive junk input; Jev doesn't")
- **Too many options collapse accuracy** — a 12-way Choice scored 0.40 on real bookkeeping data
- **Confidence is not a halo** — rows with confidence ≥0.9 were only 72.2% accurate (agentjournal); Attest deleted a constant 0.95–0.99 confidence field entirely
- **Ordering & phrasing sensitivity** — evidence order flips 5.8% of Attest verdicts
- **Cost advantage is real and universally reported** — $1.43 / 34.1M tokens; $0.00003 per routed turn; $0.0002 per voice decision
- ⚠️ **Fake demo alert** — viral "superhuman speed" videos with sped-up footage are circulating; trust repos with methodology/trace (`jev-ultrafast`, `tsai-sc`, `WindTunnel`)

## 🔬 Verification & confidence scoring

Every entry in [`data/projects.json`](./data/projects.json) carries a `verification` block, assigned during research and re-checked on each scan:

| Tier | Confidence | Meaning | How it is earned |
|---|---|---|---|
| **A** | **0.90** | Artifact inspected | Repo README fetched & read · live page accessed · full original post read · official docs read · API call made |
| **B** | 0.75 | Primary source on record | Project URL (repo or original post) verified to exist; inspected at description level |
| **C** | 0.60 | Secondary index only | Aggregated from community directories; original not opened yet — promoted on the next scan |

Current distribution: **38 × A · 70 × B · 0 × C** (108 curated). Metrics inside entries are **as reported by their authors** unless independently reproduced (reproduced numbers are marked). Known ecosystem-level caveats are documented in the casebook: confidence≠correctness, ordering sensitivity, and the circulating fake-demo warning.

## 📁 Repository contents

| File | What it is |
|---|---|
| [`CASEBOOK.md`](./CASEBOOK.md) | **The full casebook (中文)** — 14 sections, 10 documented deep-scan logs, per-case primary sources + tweet addresses |
| [`data/projects.json`](./data/projects.json) | Structured, machine-readable registry of curated projects — uniform schema incl. `verification: {tier, method, confidence}` |
| [`docs/jev-api-access-guide.zh.md`](./docs/jev-api-access-guide.zh.md) | **Jev API 申请攻略** — waitlist walkthrough (incl. the homepage-button bug & expedite email), official SDK quickstart, and no-wait alternatives: OpenRouter / Netlify AI Gateway / OpenJev / free playgrounds |

Update cadence: **automated scan every 3 hours** (GitHub × X/Twitter × five directories) — the casebook's monitoring log grows in place, and this repo receives a commit on every scan that finds new evidence; plus manual deep scans on demand.

## 🗂 Sources swept

awesome-typesafe · awesomejev.com (488 entries) · madewithjev.com (178 builds, 76 embedded tweets) · risetive.com/jev (98) · jevable.com · typesafeai.app (evidence-graded) · GitHub Search API · X/Twitter · Reddit (r/PiCodingAgent, r/LocalLLaMA, r/SideProject, r/singularity) · Hacker News (Algolia) · V2EX / linux.do / Bilibili / Zhihu KOLs · YouTube · LinkedIn.

## 📮 Contributing

Found a Jev project we missed? Open an issue or PR with: **project URL + tweet/post URL (if any) + which primitives it uses + any measured numbers**. Claims without primary sources are not accepted.

## ⚖️ License & disclaimer

Content: **CC BY 4.0**. Data (`data/`): **CC0**.

Independent community research. **Not affiliated with, endorsed by, or sponsored by TypeSafe AI.** "Jev" and "TypeSafe" belong to their owners. Metrics are as reported by their authors unless marked otherwise; star counts are point-in-time snapshots (2026-09-19).

---

## 中文版块

**Jev Radar——全网最全的 Jev 生态独立白皮书与实时监控。**

Jev 是 TypeSafe AI 于 2026-09-15 发布的首个 System One 决策模型(不生成文本,只输出 Noul/Choice/Score 三类带校准概率的判断,70-500ms,输入 $0.042/M token、输出免费)。本仓库追踪**全世界真正用 Jev 做出来的东西**:每个案例均有原始出处(仓库/线上 demo/作者原推文),按场景分类、带实测数据,并由**每日定时监控 + 人工深扫**持续更新。

- 发布 4 天,生态已达 **~500 仓库 / 21,600+ 星**;案例集收录 **220+ 案例**,结构化注册表 **108 条**(A/B 置信度分级)
- 八大场景密度排名:agent 安全 → 上下文压缩 → 模型路由 → 实时决策层(浏览器/语音/游戏)→ 内容评分 → 交易 → SQL/系统原语 → 垂直业务
- **每 3 小时自动扫描与更新**(GitHub × X × 五大目录站),有新发现即提交到本仓库;**所有项目经过检验并给出置信度评分**(A=工件直检 0.90 / B=一手源在档 0.75 / C=仅目录收录 0.60,见 [data/projects.json](./data/projects.json) 的 verification 字段)
- 完整内容见 [CASEBOOK.md](./CASEBOOK.md)(14 个章节 + 10 次扫描日志);结构化数据见 [data/projects.json](./data/projects.json)
- **想上手 Jev?看 [API 申请攻略](./docs/jev-api-access-guide.zh.md)**:waitlist 全流程(含官网按钮 bug 与加急邮件技巧)、官方 SDK quickstart、以及 OpenRouter / Netlify / OpenJev 免排队替代通道
- 独立研究,与 TypeSafe AI 无关联;引用数据均来自公开原始出处
