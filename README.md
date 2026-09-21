<div align="center">

<img src="docs/assets/banner.png" width="880" alt="Jev Radar — the world's most comprehensive tracker of the Jev ecosystem" />

# Jev Radar 📡

### 全网最全的 Jev 生态独立白皮书与实时监控
### The world's most comprehensive independent field report & live monitor of the Jev ecosystem

**全网最全,没有之一 · The Most Complete — if it was built with Jev, it's in this radar.**

[![status](https://img.shields.io/badge/monitor-active-brightgreen)]() [![cases](https://img.shields.io/badge/casebook-220%2B_cases-blue)]() [![registry](https://img.shields.io/badge/registry-255_graded_entries-9cf)]() [![cadence](https://img.shields.io/badge/scan_cadence-every_3_hours-important)]() [![verified](https://img.shields.io/badge/evidence_graded-A%2FB%2FC-purple)]() [![guide](https://img.shields.io/badge/API_access_guide-included-success)]()

**[English](#english) · [中文](#中文)**

</div>

---

## English

### What is Jev?

Jev is TypeSafe AI's first *System One* model, released on **September 15, 2026**. It never writes a single sentence. Instead, you send it some unstructured state plus a set of typed questions, and it returns decisions your code can branch on directly:

| Primitive | Question it answers | What you get back |
|---|---|---|
| **Noul** | Is this true? | A calibrated 0–1 probability |
| **Choice** | Which option fits? | Full distribution + confidence |
| **Score** | How good, on your rubric? | Probability-weighted rating |

The pitch that took over developer Twitter: **70–500 ms** end-to-end latency, **$0.042 per million input tokens, output free** — roughly 20–200× faster and 40–400× cheaper than routing the same judgments through a frontier LLM.

### What this repository is

Four days after launch, the Jev ecosystem crossed **1,000 repositories** within five days (21,600+ stars at day 4). Jev Radar is an independent attempt to answer one question with evidence: **what is the world actually building with this thing?**

Every case here was verified against a primary source — a repository we opened, a live demo we hit, or the author's original post. No hearsay, no listicle padding. And the work doesn't stop: an automated sweep (GitHub · X/Twitter · five community directories) re-runs **every three hours**, and anything new gets verified, graded, and committed.

### 🎁 Free Jev API keys for stargazers

**Star this repo ⭐, then email [hello@everyinfra.com](mailto:hello@everyinfra.com) with your GitHub username → we verify the star and reply with a free Jev API key.** 5,000 keys this round, one per person, while supplies last; keys are issued manually after verification (not automatic). Nothing is made public — the only address we publish is hello@everyinfra.com. Keys come from the maintainer's own quota and are not affiliated with TypeSafe AI. Details: [Discussion #1](https://github.com/everyinfra/jev-radar/discussions/1).

### Why you can trust it

Each of the 108 structured registry entries carries a `verification` block assigned during research:

| Tier | Confidence | How it's earned |
|---|---|---|
| **A** | 0.90 | We inspected the artifact: read the repo README, fetched the live page, read the full original post, or called the API ourselves |
| **B** | 0.75 | Primary source on record (repo or original post), inspected at description level |
| **C** | 0.60 | Directory-indexed only — promoted on the next scan once opened |

Current distribution: **38 × A · 70 × B · 0 × C**. Numbers inside entries are **as reported by their authors** unless marked reproduced. We also document what *doesn't* work: confidence ≠ correctness, ordering sensitivity, and a circulating wave of sped-up fake demos — with guidance on which repos carry real traces.

### What people are building (by density)

1. **Agent safety & supervision** — a Jev "second pair of eyes" on every tool call. Flagship: [`pi-warden`](https://github.com/DevMortimer/pi-warden), self-graded on 17,000 real calls (88% of holds correct)
2. **Context compaction** — score every tool result, keep what matters. [`fast-jev-compaction`](https://github.com/tamaratran/fast-jev-compaction) leads at 2.7k★
3. **Model routing** — 10+ implementations; [`jev-codex-router`](https://github.com/0xNatoshi/jev-codex-router) measured **−60% cost** on a 237-turn backtest
4. **Real-time decision layers** — browser (7.1s flight booking), voice (~300ms per phrase), games (Pokémon, StarCraft, Tetris at superhuman speed)
5. **Content scoring & growth** — 61 questions per draft post at $0.0004; 724 competitor ads torn down for $0.09
6. **Trading** — one decision per 300ms blockchain block ([`jev-trader`](https://github.com/jarrodwatts/jev-trader)); first honest paper-trading numbers published
7. **Jev as a systems primitive** — Postgres/DuckDB predicates, pandas layers, zsh history, Neovim, Emacs
8. **Verticals arriving** — tax forms (100% strict accuracy on 261 IRS forms), legal ruling prediction, PubMed screening, GTM workflows

### Field-tested lessons

- **Feed it narrow, mechanical questions** — "LLMs survive junk input; Jev doesn't"
- **Big option lists collapse** — a 12-way Choice scored 0.40 on real bookkeeping data
- **Confidence is not a halo** — rows with confidence ≥ 0.9 were only 72.2% accurate in one large independent eval
- **Order and phrasing matter** — evidence order flips 5.8% of one verifier's rulings
- **The cost story is real** — $1.43 per 34.1M tokens; $0.00003 per routed turn; $0.0002 per voice decision

### Repository contents

| Path | What it is |
|---|---|
| [`CASEBOOK.md`](./CASEBOOK.md) | The full casebook — 14 sections, per-case sources & tweet links, 10 documented deep-scan logs |
| [`data/projects.json`](./data/projects.json) | Machine-readable registry: uniform schema incl. `verification {tier, method, confidence}` |
| [`docs/jev-api-access-guide.zh.md`](./docs/jev-api-access-guide.zh.md) | **Jev API access guide** — waitlist walkthrough, the expedite-email trick, and no-wait alternatives (OpenRouter / Netlify / OpenJev / free playgrounds) |
| [`skills/jev-radar-briefing/SKILL.md`](./skills/jev-radar-briefing/SKILL.md) | **One-file quickstart + daily-briefing skill** — drop into any SKILL.md-compatible agent for scheduled pulls and auto-generated digests; includes a no-agent shell script |

**Cadence:** automated scan every 3 hours; the repo receives a commit on every scan that finds new evidence.
**Sources swept:** awesome-typesafe · awesomejev.com (488 entries) · madewithjev.com (178 builds) · risetive.com/jev (98) · jevable.com · typesafeai.app · GitHub Search · X · Reddit · HN · V2EX/linux.do/Bilibili · YouTube · LinkedIn.

### Contributing

Missed a project? Open an issue or PR with: **project URL + original post URL (if any) + primitives used + any measured numbers.** Submissions without primary sources are not accepted.

### License & disclaimer

Content: **CC BY 4.0** · Data: **CC0**. Independent community research — **not affiliated with TypeSafe AI**. Metrics are as reported by their authors; star counts are point-in-time snapshots (2026-09-19).

### About EveryInfra (maintainer disclosure)

Jev Radar is initiated and maintained by [EveryInfra](https://everyinfra.com) — public-data, web-search and CAPTCHA infrastructure for AI products, one API across 88 platforms. An independent report earns trust by disclosing its maintainer: editorial criteria, confidence grading and scan logs are all public in this repo, and this project is not affiliated with TypeSafe AI. If your Jev project needs live data as decision input, start at [everyinfra.com/docs](https://everyinfra.com/docs).

---

## 中文

### Jev 是什么?

Jev 是 TypeSafe AI 于 **2026-09-15** 发布的首个 *System One* 模型。它一个字都不写:你给它一段非结构化状态、一组带类型的问题,它直接返回代码可以拿去分支的判断——

| 原语 | 回答什么问题 | 返回什么 |
|---|---|---|
| **Noul** | 这句话成立吗? | 校准过的 0–1 概率 |
| **Choice** | 哪个选项合适? | 完整概率分布 + 置信度 |
| **Score** | 按你的量规打几分? | 概率加权分值 |

让它刷屏开发者圈的理由:**端到端 70–500 毫秒,输入 $0.042/百万 token、输出免费**——同样的判断走前沿 LLM 要慢 20–200 倍、贵 40–400 倍。

### 这个仓库是什么

发布 6 天,Jev 生态已突破 **1700 个仓库**。Jev Radar 想用证据回答一个问题:**大家到底在用它做什么?**

这里收录的每个案例都核对过一手出处——我们打开过的仓库、访问过的线上 demo、或作者原帖。不收传闻,不凑数。而且这件事没有终点:一套自动化巡检(GitHub · X · 五个社区目录站)**每 3 小时重跑一次**,新东西先检验、再定级、然后提交进仓库。

### 🎁 给仓库点 Star,免费领 Jev API key

**点 Star ⭐,然后给 [hello@everyinfra.com](mailto:hello@everyinfra.com) 发邮件(正文附 GitHub 用户名)→ 核对后免费 Key 回复到你的邮箱。**本轮共 **5,000 个**,每人限领 1 个,发完即止;Key 为人工核对后逐一发放(非自动即时)。全程不公开任何邮箱,对外只公布 hello@everyinfra.com;Key 来源自维护方自有配额,与 TypeSafe AI 无关联。详见 [Discussion #1](https://github.com/everyinfra/jev-radar/discussions/1)。

### 为什么可信

108 条结构化注册记录,每条都带研究时打上的 `verification` 块:

| 层级 | 置信度 | 怎么挣来的 |
|---|---|---|
| **A** | 0.90 | 我们亲手检验过工件:读过仓库 README、抓过线上页、读过原帖全文、或实测过 API |
| **B** | 0.75 | 一手源(仓库/原帖)在档,做过描述级核查 |
| **C** | 0.60 | 暂仅目录收录——下次扫描打开后升级 |

当前分布:**38 × A · 70 × B · 0 × C**。条目里的数字均为**作者自报**,复现过的会单独标注。我们同样记录不好用的部分:置信度 ≠ 正确性、对输入顺序敏感、以及市面上流通的加速假 demo——并告诉你哪些仓库带真实 trace。

### 大家在做什么(按密度排序)

1. **Agent 安全与监督**——给每次工具调用配"第二双眼睛"。旗舰:[`pi-warden`](https://github.com/DevMortimer/pi-warden),在 17,000 次真实调用上自评(拦截 88% 拦得对)
2. **上下文压缩**——逐条给工具输出打分、只留有用的。[`fast-jev-compaction`](https://github.com/tamaratran/fast-jev-compaction) 以 2.7k★ 领跑
3. **模型路由**——10+ 个实现;[`jev-codex-router`](https://github.com/0xNatoshi/jev-codex-router) 在 237 轮回测中实测**省 60% 成本**
4. **实时决策层**——浏览器(7.1 秒订好机票)、语音(每句 ~300ms)、游戏(宝可梦/星际/俄罗斯方块,超人类速度)
5. **内容评分与增长**——每条草稿帖 61 个问题只要 $0.0004;724 条竞品广告 $0.09 全拆完
6. **交易**——每 300ms 一个区块链区块决策一次([`jev-trader`](https://github.com/jarrodwatts/jev-trader));第一批诚实的模拟盘战绩已公开
7. **当系统原语用**——Postgres/DuckDB 谓词、pandas 语义层、zsh 历史、Neovim、Emacs
8. **垂直行业进场**——税单分类(261 份 IRS 表单 100% 严格准确)、司法裁定预测、PubMed 文献筛查、销售工作流

### 实战教训

- **问题要窄、要机械**——"LLM 吃垃圾输入也能凑合,Jev 不行"
- **选项一多就崩**——真实记账数据上,12 选 1 的 Choice 只打出 0.40
- **置信度不是免死金牌**——一项大型独立评测里,置信度 ≥ 0.9 的行只有 72.2% 是对的
- **顺序和措辞都敏感**——证据顺序能翻转某验证器 5.8% 的判决
- **成本优势是真的**——34.1M token 花 $1.43;每轮路由 $0.00003;每句语音 $0.0002

### 仓库内容

| 路径 | 是什么 |
|---|---|
| [`CASEBOOK.md`](./CASEBOOK.md) | 完整案例集——14 个章节、逐案例出处与推文链接、10 次深扫日志 |
| [`data/projects.json`](./data/projects.json) | 机器可读注册表:统一 schema,含 `verification {tier, method, confidence}` |
| [`docs/jev-api-access-guide.zh.md`](./docs/jev-api-access-guide.zh.md) | **Jev API 申请攻略**——waitlist 全流程(含官网按钮 bug 与加急邮件技巧)、OpenRouter / Netlify / OpenJev 免排队通道、免费 Playground |
| [`skills/jev-radar-briefing/SKILL.md`](./skills/jev-radar-briefing/SKILL.md) | **单文件接入 + 每日简报 Skill**——装进任意支持 SKILL.md 的 agent 即可定时拉取、自动生成日报;附不开 agent 的纯脚本版 |

**节奏:**每 3 小时自动扫描一次;只要扫到新东西,仓库就会多一个 commit。
**覆盖来源:** awesome-typesafe · awesomejev.com(488 条)· madewithjev.com(178 个 build)· risetive.com/jev(98)· jevable.com · typesafeai.app · GitHub 搜索 · X · Reddit · HN · V2EX/linux.do/B站 · YouTube · LinkedIn。

### 参与贡献

发现了我们漏掉的项目?开 issue 或 PR,附:**项目地址 + 原帖地址(如有)+ 用的原语 + 实测数字**。没有一手出处的提交不收。

### 许可与免责

内容 **CC BY 4.0** · 数据 **CC0**。独立社区研究,**与 TypeSafe AI 无关联**。指标均为作者自报;星数为 2026-09-19 时点快照。
### 关于 EveryInfra(维护方披露)

Jev Radar 由 [EveryInfra](https://everyinfra.com) 发起并维护——面向 AI 产品的公开数据、网页搜索与验证码基础设施,一个 API 覆盖 88 个平台。独立报告的公信力来自维护方披露:编辑标准、置信度分级与扫描日志全部公开于本仓,本项目与 TypeSafe AI 无关联。若你的 Jev 项目需要实时数据作为决策输入,可从 [everyinfra.com/docs](https://everyinfra.com/docs) 开始。
