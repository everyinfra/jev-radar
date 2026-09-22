# Jev Radar · Casebook — Jev(TypeSafe AI)项目案例集

> **生成时间**:2026-09-19(首版基于 2026-09-15 ~ 09-19 的全网检索)
> **对象**:TypeSafe AI 于 2026-09-15 发布的 System One 模型 Jev(Noul 是非判断 / Choice 选项分布 / Score 量规打分;70-500ms;$0.042/M 输入 token,输出免费)。
> **收录标准**:有可点击原始出处、能确认真实存在(已上线/开源/带实测数据)或明确标注为想法的项目。已排除 Journal of Extracellular Vesicles 期刊、JEV 股票(Jericho Energy Ventures)等同名干扰项;OpenJev 等兼容克隆单独归类并明确标注"非官方"。
> **主要索引来源**:[awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe)、GitHub Search API、Reddit / HN / X 直接检索。

---

## 一、总览表

> 链接规则:每个项目均给出**项目地址**;**推文地址**仅当存在时给出——"—"表示截至 2026-09-19 未发现发布推文(作者以 GitHub/Reddit 发布为主);标注"收录页"的,推文内嵌在 [madewithjev.com](https://madewithjev.com/) 对应 build 页(含成本/延迟数据)。

| 案例 | 平台/作者 | 用的原语 | 状态 | 项目地址 | 推文地址 |
|---|---|---|---|---|---|
| pi-warden | Reddit u/95-cosmo-changer | Noul(不可逆/符不符意图) | ✅ 已上线 v0.12.0 | [GitHub](https://github.com/DevMortimer/pi-warden) | [中文解读推](https://x.com/AISuperDomain/status/2100536937664938408) |
| Foreman | GitHub thruwire(280★) | Noul(完工/卡住/需验证) | ✅ 开源实验 | [GitHub](https://github.com/thruwire/foreman) | — |
| peepo_comfy 安全层 | Reddit u/peepo_comfy | Score(工具调用安全分) | 🔨 原型进行中 | [Reddit 帖](https://www.reddit.com/r/PiCodingAgent/comments/1whsav6/) | — |
| jev-guard (specpi) | Reddit u/fingerthief | Score(命令安全分) | ✅ 可玩 demo | [Demo](https://tannermidd.github.io/specpi-jev-guard/) | — |
| is-malicious | Reddit u/lu4p_ | Noul(逐文件恶意判断) | ✅ 开源 CLI | [GitHub](https://github.com/luantak/is-malicious) | — |
| Supercov | Reddit u/Nedomas | Score(单文件代码质量) | ✅ 开源(Rust) | [GitHub](https://github.com/supercorp-ai/supercov) | — |
| killmyidea | Reddit u/stemonte | Score(0-4 量规×10) | ✅ 线上应用 | [App](http://killmyidea.stemonte.io) / [源码](https://github.com/monteduro/killmyidea) | — |
| Jev Ultrafast | browser-use 团队 | Choice(操作+目标元素) | ✅ 开源+实测 | [GitHub](https://github.com/browser-use/jev-ultrafast) | [推文](https://x.com/gregpr07/status/2100411066966749359) |
| jev-voice-browser | GitHub moritzkremb | Choice+Noul(意图/目标/说完没) | ✅ 开源 | [GitHub](https://github.com/moritzkremb/jev-voice-browser) | [推文](https://x.com/moritzkremb/status/2100577979021832365) |
| Jev+Stagehand 浏览器操作 | X @kylejeong | Choice(下一步动作) | ✅ 演示($0.001/任务) | [收录页](https://madewithjev.com/builds/stagehand-remote-browser) | [收录页内嵌](https://madewithjev.com/builds/stagehand-remote-browser) |
| 无截图 computer use | X @milindlabs | Choice(UI 元素概率) | ✅ 演示(~90ms/决策) | [收录页](https://madewithjev.com/builds/computer-use-without-screenshots) | [收录页内嵌](https://madewithjev.com/builds/computer-use-without-screenshots) |
| Pociot X 过滤扩展 | X @marcelpociot | Noul/Choice(该不该折叠) | ✅ 已做出+演示 | 推文内演示(无独立仓库) | [推文](https://x.com/marcelpociot/status/2100520134481735729) |
| typesafe-adblock | GitHub realZachi(48★) | Noul(这是广告吗) | ✅ Chrome 扩展 | [GitHub](https://github.com/realZachi/typesafe-adblock) | — |
| x-scanner | GitHub oso95(7★) | 6×类型化(行为标签) | ✅ Chrome 扩展 | [GitHub](https://github.com/oso95/x-scanner) | — |
| Attest 声明核查 | quorumtech.ch | Choice(判决枚举) | ✅ 线上 API+MCP | [官网](https://quorumtech.ch/attest) | — |
| Crowdcheck | vercel.app | Noul 批量(万人格) | ✅ 线上 demo | [App](https://crowdcheck-ai.vercel.app/) | — |
| HA-Jev | GitHub AboveColin | 三原语(实体→传感器) | ✅ HA 集成 | [GitHub](https://github.com/AboveColin/HA-Jev) | — |
| pg-jev | GitHub realZachi(145★) | SQL 谓词(自然语言问表) | ✅ Postgres 扩展 | [GitHub](https://github.com/realZachi/pg-jev) | — |
| vgi-typesafe | GitHub Query-farm | SQL 表函数(三原语) | ✅ DuckDB 扩展 | [GitHub](https://github.com/Query-farm/vgi-typesafe) | — |
| jev-codex-router | GitHub 0xNatoshi(29★) | Choice+Score(选模型/深度) | ✅ 开源+回测 | [GitHub](https://github.com/0xNatoshi/jev-codex-router) | — |
| jev-shell-history | GitHub mrnugget(33★) | Choice(正在敲哪条) | ✅ zsh 插件 | [GitHub](https://github.com/mrnugget/jev-shell-history) | — |
| winnow | GitHub GhalebDweikat(17★) | Noul×N(这块需要吗) | ✅ Claude Code 插件 | [GitHub](https://github.com/GhalebDweikat/winnow) | — |
| jev-pruner | GitHub tamaratran(12★) | Noul×N(有行要留吗) | ✅ Claude Code 插件 | [GitHub](https://github.com/tamaratran/jev-pruner) | — |
| rh-guard | GitHub 24601 | 规则+Noul(在改评分器吗) | ✅ 开源+录制 demo | [GitHub](https://github.com/24601/rh-guard) | — |
| SuperX 病毒度评分 | X @robj3d3 | Score×61(单帖) | ✅ 免费工具 | [收录页](https://madewithjev.com/builds/superx-post-scoring) | [推文](https://x.com/robj3d3/status/2100722975645598191) |
| 724 广告拆解 | X @TheMattBerman | 混合(hook/格式/CTA…) | ✅ 集成进 stealads+MCP | [收录页](https://madewithjev.com/builds/competitor-ad-teardown) | [收录页内嵌](https://madewithjev.com/builds/competitor-ad-teardown) |
| 3282 自帖增长分析 | X @iannuttall | Score×8(话题/hook/语气) | ✅ 一次性分析 | [收录页](https://madewithjev.com/builds/x-post-analysis) | [收录页内嵌](https://madewithjev.com/builds/x-post-analysis) |
| 700 线索外联评分 | X @romanbuildsaas | Score(消息表现预测) | 🔨 即将上线 GojiberryAI | [收录页](https://madewithjev.com/builds/lead-outreach-scoring) | [收录页内嵌](https://madewithjev.com/builds/lead-outreach-scoring) |
| WebMCP 基准(WindTunnel) | nekuda-ai(@0xidanlevin) | Choice(选工具) | ✅ 开源可复现 | [GitHub](https://github.com/nekuda-ai/WindTunnel) | [收录页内嵌](https://madewithjev.com/builds/webmcp-benchmark) |
| jev-trader 实盘交易 | X @jarrodwatts(895★) | Choice(买/卖) | ✅ 开源+实盘 | [GitHub](https://github.com/jarrodwatts/jev-trader) / [Demo](https://jev-trader.vercel.app) | [推文](https://x.com/jarrodwatts/status/2100356151468585346) |
| $10,000 交给 Jev 交易 | X @abolbuild | Choice(买/卖) | ✅ 演示 | [收录页](https://madewithjev.com/builds/10k-trading) | [收录页内嵌](https://madewithjev.com/builds/10k-trading) |
| jevocks 股票终端 | Prosper Otemuyiwa | Noul/Score(状态判定) | ✅ 开源 | [收录页](https://madewithjev.com/builds/jevocks) | [收录页内嵌](https://madewithjev.com/builds/jevocks) |
| YouTube 跳赞助扩展 | X @tdinh_me(Tony Dinh) | Noul(是否赞助段) | ✅ 开源原型 ~$0.005/视频 | [收录页](https://madewithjev.com/builds/youtube-sponsor-skipper) | [收录页内嵌](https://madewithjev.com/builds/youtube-sponsor-skipper) |
| 欺诈检测级联 Jev→Kimi K3 | X @nutlope | Noul+置信路由 | ✅ 96/100、$0.07 | [收录页](https://madewithjev.com/builds/fraud-detection-jev-kimi) | [收录页内嵌](https://madewithjev.com/builds/fraud-detection-jev-kimi) |
| 1kpapers 论文主题分类 | X @nutlope | Choice×24(主题) | ✅ 1018 篇/$0.08/中位 256ms | [收录页](https://madewithjev.com/builds/1kpapers) | [收录页内嵌](https://madewithjev.com/builds/1kpapers) |
| keep.md 语义搜索+打标 | X @iannuttall | Score/rerank | ✅ 生产环境,快 7-50× | [收录页](https://madewithjev.com/categories/research-and-data) | [收录页内嵌](https://madewithjev.com/categories/research-and-data) |
| dabit3 三连(启动器/表格/Gmail) | X @dabit3(Nader Dabit) | Choice/Score | ✅ 演示 ~100ms/键 | [收录页](https://madewithjev.com/builds/predictive-launcher) | [收录页内嵌](https://madewithjev.com/builds/predictive-launcher) |
| Every 编辑部 vibe check | X @danshipper | Score(编辑判断) | ✅ 生产:1709 判断<$0.01 | [收录页](https://madewithjev.com/categories/content-and-growth) | [收录页内嵌](https://madewithjev.com/categories/content-and-growth) |
| DiffJury PR 裁判 | X @raihankhan_rk | Noul(能合吗) | ✅ 线上 | [Demo](https://diffjury.up.railway.app) | [收录页内嵌](https://madewithjev.com/builds/diffjury) |
| Mac 应用离线支持 agent | X @malekoo | Choice(哪篇文章) | ✅ 生产,42/42 留出集 | [收录页](https://madewithjev.com/categories/triage-and-routing) | [收录页内嵌](https://madewithjev.com/categories/triage-and-routing) |
| jevmeter | GitHub ChetasLua(53★) | Score(逐句可信度) | ✅ 开源 | [GitHub](https://github.com/ChetasLua/jevmeter) | [推文](https://x.com/chetaslua/status/2100473581251748216) |
| skillranker | GitHub Dicklesworthstone(44★) | Score/Choice(技能排序) | ✅ Rust CLI | [GitHub](https://github.com/Dicklesworthstone/skillranker) | — |
| Jev Plays Pokémon | GitHub anxkhn | Choice(战斗动作) | ✅ 开源 | [GitHub](https://github.com/anxkhn/JevPlaysPokemon) | — |
| Jev Plays StarCraft | GitHub phyous | Choice(指令) | ✅ verified run | [GitHub](https://github.com/phyous/tsai-sc) | — |
| TypeSafe Mario | GitHub fhshaik(260★) | Choice(合法动作) | ✅ 开源实验 | [GitHub](https://github.com/fhshaik/typesafe-mario) | [收录页内嵌](https://madewithjev.com/builds/jev-plays-mario) |
| 杀戮尖塔 2 超人类速通 | X @coolish(paulwei,中文) | Choice(卡牌动作) | ✅ 实测 0.7s/步 | [收录页](https://madewithjev.com/builds/slay-the-spire-2) | [收录页内嵌](https://madewithjev.com/builds/slay-the-spire-2) |
| Subway Surfers 同时 50 局 | X @_MaxBlade | Choice(动作) | ✅ <$0.01/局 | [收录页](https://madewithjev.com/builds/subway-surfers) | [收录页内嵌](https://madewithjev.com/builds/subway-surfers) |
| Smash Bros 四角色自搏 | X @maubaron | Choice(动作) | ✅ 22M token/几美分 | [收录页](https://madewithjev.com/builds/smash-bros) | [收录页内嵌](https://madewithjev.com/builds/smash-bros) |
| Tetris 超难模式 | X @AlanDaitch | Choice(落点) | ✅ 134 行/2 分钟 | [收录页](https://madewithjev.com/builds/jev-plays-tetris) | [收录页内嵌](https://madewithjev.com/builds/jev-plays-tetris) |
| 实时关卡生成 | X @HugoDuprez | Choice(关卡组件) | ✅ 演示 | [收录页](https://madewithjev.com/builds/realtime-game-levels) | [收录页内嵌](https://madewithjev.com/builds/realtime-game-levels) |
| jev-piano / 音乐即兴 | Paul / Stephen Wu | Choice(音符/乐句) | ✅ 开源 | [收录页](https://madewithjev.com/builds/jev-piano) | [收录页内嵌](https://madewithjev.com/builds/jev-piano) |
| HEIST//ONE | GitHub AbdelStark | 批量混合(六守卫) | ✅ 开源游戏 | [GitHub](https://github.com/AbdelStark/heist-one) | — |
| Jev Drone | GitHub RomanSlack(58★) | 混合(战术判断) | ✅ MuJoCo | [GitHub](https://github.com/RomanSlack/jev-drone) | — |
| Jev Search | superagents-lab(49★) | Choice+Noul(选源/排序) | ✅ 开源 demo | [GitHub](https://github.com/superagents-lab/jev-search) | — |
| TypeSafe Typewriter | Steve Krouse(Val Town) | 16 个实时判断 | ✅ 线上可玩 | [Demo](https://typesafe-demo.val.run/) | [推文](https://x.com/stevekrouse/status/2100287368221659289) |
| jev-cli (jevctl) | GitHub Nasrullah-AL | 全三种(verify/route/rerank…) | ✅ npm 已发布 | [GitHub](https://github.com/Nasrallah-AL/jev-cli) | — |
| kamchatka(assisted-shell) | GitHub ljedrz | Score(命令安全分) | ✅ 开源 | [GitHub](https://github.com/ljedrz/nachalnik) | — |
| jev-axi / pi-heed / pi-jev / Bicameral / jev-mobile / jev-browser 等 | 多作者 | 混合 | ✅ 开源/实验 | 见 [awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe) | — |
| Godot 测试 / GBC 导航 / 路由器构想 / CV 重排 | Reddit 众(u/MichettGodot 等) | 混合 | 🔨 原型 / 💭 想法 | [帖1](https://www.reddit.com/r/PiCodingAgent/comments/1wjibh5/anyone_here_using_jev/) / [帖2](https://www.reddit.com/r/PiCodingAgent/comments/1whsav6/) | — |
| 复刻生态:OpenJev / SemIf / jevlike / vLLM PR | razorback16 / TheoLeeCJ / vinnylarouge / Matt Mastracci | — | ✅ 均开源 | 见 §九 | [mmastrac 评测推](https://x.com/mmastrac/status/2100626193943052784) |
| 独立评测:Janus / agentjournal / Rerank Bench / Benchmark | 多作者 | 全三种 | ✅ 带数据 | 见 §八 | [iammrduncan 推](https://x.com/iamMrDuncan/status/2100467548298899918) |

---

## 二、AI Agent 安全 / 监督类(最密集,发布 72 小时内冒出 10+ 个)

### 1. pi-warden — 目前最完整的实战案例
- **作者**:u/95-cosmo-changer(GitHub: DevMortimer),2026-09-17
- **做了什么**:Pi 编码 agent 的"第二双眼睛"。Jev(~250ms)读取用户 prompt、agent 最后的陈述、即将执行的工具调用,以 Noul 判断"是否不可逆""是否与 agent 说的相符""影响是否超出工作区",结果注入 agent 上下文;还检查代码是否符合项目规则文件、检测循环、"说做完了但没跑测试"、压缩超大工具输出。
- **状态**:✅ 已上线([GitHub](https://github.com/DevMortimer/pi-warden)、[pi.dev 包页](https://pi.dev/packages/pi-warden)),作者已在工作中日常使用。
- **亮点/数据**:在 17,000 次历史调用上回放自评:仅 hold 42 次、~88% 拦得对;抱怨率 ~2%、无一例数据丢失;off-task 拦截因评测落败被自动降级为 steer。实测拦下过数据库迁移和死循环 bash。
- **出处**:[reddit.com/r/PiCodingAgent/comments/1wimfhg/](https://www.reddit.com/r/PiCodingAgent/comments/1wimfhg/)(77 赞)

### 2. Foreman — "软件工厂监工"(09-19 补充,280★)
- **作者**:GitHub [thruwire](https://github.com/thruwire/foreman),2026-09-17
- **做了什么**:Codex CLI 当工人干活,Foreman 用 Jev 在旁边独立监督:并行问 `implementation_complete / tests_sufficient / requirements_satisfied / worker_stuck / needs_verification / meaningful_progress` 等一组 Noul 问题,Python 策略层决定 continue/stop/retry/verify/finish。双 asyncio 循环,工人不停工、监督不阻塞。
- **状态**:✅ 开源实验(作者自称"architectural experiment, not a claim")。
- **亮点**:把 Jev 用成"高频语义监督层"——监督问题比生成问题窄得多,恰好是 Jev 的形状;README 附理论文档(semantic supervision / why-jev)。

### 3. peepo_comfy 的安全层 + 路由器构想
- 2026-09-16:安全层(扫描所有工具调用打安全分)**正在做**;自动模型路由器是下一步想法。经验之谈:"问题构造必须显式,但官方 TypeSafe skill 能教 LLM 写问题;分层/链式提问是正路"。
- **出处**:[reddit.com/r/PiCodingAgent/comments/1whsav6/](https://www.reddit.com/r/PiCodingAgent/comments/1whsav6/)(98 赞,评论区是 Jev 生态最肥的矿脉)

### 4. jev-guard(基于 OpenRouter)— u/fingerthief
- 2026-09-18:"OpenRouter 上了之后当天开做 command guard",附初始测试截图,称结果"相当惊艳"。Demo 页:[tannermidd.github.io/specpi-jev-guard](https://tannermidd.github.io/specpi-jev-guard/)。✅ 原型可玩。**出处**:[1whsav6 评论区](https://www.reddit.com/r/PiCodingAgent/comments/1whsav6/) 与 [1wjibh5 评论区](https://www.reddit.com/r/PiCodingAgent/comments/1wjibh5/anyone_here_using_jev/)。

### 5. is-malicious — u/lu4p_
扫仓库源码/CI/配置文件判断是否恶意,输出文件+行号指针。[GitHub: luantak/is-malicious](https://github.com/luantak/is-malicious)。✅ 开源 CLI。

### 6. 同型开源项目(细节见各自仓库)
- [pi-heed](https://github.com/Nyarlathoteppppp/pi-heed) — 从用户中英文消息提取约束、拦截副作用工具调用;09-18 已升级为"policy engine + benchmark + experiment log"。
- [pi-jev](https://github.com/y0usaf/pi-jev)(65★) — 影子模式工具门 + 输出裁判 + 通用 `jev_ask` 工具,门控效果有实测。
- [Bicameral](https://github.com/AbdelStark/bicameral) — LLM 写代码 + Jev 当"条件反射"层(策略/循环检测/评审)。
- [kamchatka --assisted-shell](https://github.com/ljedrz/nachalnik) — 给 shell 命令打红绿灯安全分;另有 Jev 内容感知压缩示例。
- [jev-axi](https://github.com/shiftynick/jev-axi) — 拦危险调用+筛查抓取内容的 prompt 注入+构建日志分诊+风险 diff;自带基准:agent 读文件更少但成本持平。
- [jev-mobile](https://github.com/Friedjof/jev-mobile) — 安卓 agent 每步在有界 UI 动作里做 Choice,PoC,主要对 Android Settings 测试过。
- [jev-browser](https://github.com/jkudish/jev-browser)(81★)、[jev-mcp](https://github.com/jkudish/jev-mcp)(71★)、[Jev MCP](https://github.com/blakestone-x/jev-mcp)、[TypeSafe MCP](https://github.com/itsmostafa/typesafe-mcp)(62★)、[ask-jev-skill](https://github.com/shantanugoel/ask-jev-skill)。

### 09-19 晚间新增(第二波)
- **rh-guard — reward-hack 雷达**:[24601/rh-guard](https://github.com/24601/rh-guard)。专拦编码 agent"篡改评分器/偷看隐藏测试/操纵评测过程"的行为:结构化硬规则 + Jev System One sidecar 判剩余灰区,挂进 Claude Code/Cursor/Codex/Grok Build/Pi 等 hook,附录制 demo(拦下对断言的 sed、放行无害 echo)。README 还点名三个兄弟项目:[JevLint](https://github.com/huntedman/JevLint)(Noul 语义约定的 write→check→fix lint 循环)、[jevgate](https://github.com/thevibeworks/jevgate)(白名单硬边界,Jev 只判白名单外,fail-open 永不单独一票否决)、[Augustus](https://github.com/24601/Augustus)(判断"该不该用 Jev"的设计层)。新子类:**反 reward-hacking**。
- [jevons](https://github.com/LilDojd/jevons) — Pi 的有界执行监督者:决策、恢复、评审。
- [clear-head](https://github.com/VladyslavHontar/clear-head) — Claude Code Stop hook:agent 声称读过的东西和它实际读到的对账(Noul 核查声明)。

### 09-19 午后第三波(守门类已成红海,细分差异化开始)
- [hermes-jev-approvals](https://github.com/anpicasso/hermes-jev-approvals)(4★) — Hermes Agent 智能命令审批的 Jev 审查员,**实测 8.7× 更快、4× 更便宜**——守门类少数带对比数字的。
- [toolgate](https://github.com/RiskAverseTech/toolgate) — "开源版 auto mode":校准型工具调用防火墙,影子模式默认。
- [noulgate](https://github.com/dhava-gautama/noulgate) — 给 agent 的昂贵步骤设闸,离线优先。
- [construct-auto-classifier](https://github.com/godspede/construct-auto-classifier) — 按副作用分级的 shell 命令安全闸(OpenCode/Antigravity)。
- [omp-typesafe](https://github.com/siddicky/omp-typesafe) / [omp-jev-decision](https://github.com/iAziz786/omp-jev-decision) — omp 编码 agent 的对抗性审查员 + 类型化 decision 工具。
- [codex-jev-assistant](https://github.com/2023Anita/codex-jev-assistant) — Codex 插件:风险审查/证据核查/上下文筛查。
- [jev-lens](https://github.com/rashedInt32/jev-lens) — "Claude Code 刚做的事我需要看吗?"每个 Stop 一个校准判决。
- [cmdc-auto-mode](https://github.com/mja00/cmdc-auto-mode) / [bouncer](https://github.com/clownware/bouncer) — Command Code 自动权限模式;"别再为 if 语句付推理价"(bouncer)。
- [jev-crawlers](https://github.com/russfranky/jev-crawlers)(09-20 02 时,A 级)—— **递归找 bug 管道**:seed|expand|judge|verify|report 五段 Unix 式组合;expand 纯机械(调用者/git 共变文件/配置引用),judge 每节点一次 Jev 调用($0.00008/节点,输出 expand/report/prune/escalate),verify 单独构造可证伪工件——"判断便宜到可以逐节点判,而不是每次扫描判一次"。
- [dsh-jev-guard](https://github.com/7starsseeker/dsh-jev-guard)(09-20 17 时,A 级,中文)—— DeepSeek Harness 的**强制执行前安全阀**:L0 离线静态规则→Jev 语义判定(~300ms)→allow/revise(附降级模板)/block/escalate 四态;挂 DSH 原生 `tools/pre-execute` 钩子,"是拦截,不是提醒模型自觉";**114 例校准、中文直送 90.4%**。
- [shipit-gate](https://github.com/thecoderpanda/shipit-gate)(09-20 20 时,A 级)—— **发布门**:"问 Jev 现在能不能 ship——在你 push 之前"。收集部署信号(时间/分支/diff 规模/风险区域/测试),~200ms 出裁决,阈值全在代码里(confidence<0.50、rollback_risk>0.70、blast_radius),支持显式 override,免 key 可看 demo(周五傍晚 + migration = 拦截)。
- [whoa](https://github.com/PaulChen79/whoa)(09-20 08 时,A 级)—— **编码 agent 的"止损器"**:数循环、判漂移;信号面全部枚举在 README 里,脱敏规则极其详尽(找不到密钥结尾就整体降级为只记 argv[0]——"几步的判决变差是代价,泄露密钥不是")。

---

## 三、浏览器 Agent / 扩展类

### 7. Jev Ultrafast — Browser Use 官方团队,性能数据最硬
- **作者**:browser-use 组织(Gregor Zunic [@gregpr07](https://x.com/gregpr07/status/2100411066966749359)),2026-09-16,口号 "i. am. speed."
- **做法**:DOM 转带索引元素表,**一次 Jev 请求同时决策操作和目标元素**(Choice,推测式多头),仅 TYPE_TEXT 时调一个小 LLM 生成文字;模型输出永远不变成选择器/JS。
- **数据**:苏黎世→伦敦机票搜索 **7.1 秒**;6 次交替运行中位 9.45s→7.09s(-25%),浏览器协议调用 1,092→101;维基百科任务 2.8s、酒店筛选 1.9s。作者诚实标注:3×1 任务、单浏览器 profile,非普适基准。
- **链接**:[github.com/browser-use/jev-ultrafast](https://github.com/browser-use/jev-ultrafast);第三方实测视频 [YouTube](https://www.youtube.com/watch?v=SNJ3yuJ_QwY)([B站搬运](https://www.bilibili.com/video/BV1yrey6QEHu/))。
- **推文**:[@gregpr07 发布推](https://x.com/gregpr07/status/2100411066966749359)(1× 速度视频,"7 秒、$0.0039")。

### 8. jev-voice-browser — 语音实时控浏览器(09-19 补充)
- **作者**:GitHub [moritzkremb](https://github.com/moritzkremb/jev-voice-browser)(42★,2026-09-17;疑与 YouTube 频道 "Moritz | AI Systems" 同人,其[教程视频](https://www.youtube.com/watch?v=Nq_lu5QT-fI) ~6 分钟处演示的"近即时语音 agent"即此项目,Reddit 用户曾[转述](https://www.reddit.com/r/PiCodingAgent/comments/1wjibh5/anyone_here_using_jev/))
- **做法**:语音流式转写,每个 partial transcript 发**一次 Jev 请求带 9-11 个问题**(意图/目标元素/站点/命令说完了吗/是在对我说话吗/是否破坏性),~250-350ms 回来,代码决定 act/wait/ask/ignore。Jev 不生成文字——搜索词和 URL 由代码抽成候选 span,Jev 只负责"挑一个"逐字复制。
- **成本**:每次调用约 $0.0002。✅ 开源可跑。
- **推文**:[发布推](https://x.com/moritzkremb/status/2100577979021832365);[全教程推](https://x.com/moritzkremb/status/2100715237267660873)(YouTube 教程出处)。

### 9. Marcel Pociot 的 X 帖子过滤器
- [@marcelpociot](https://x.com/marcelpociot/status/2100520134481735729),2026-09-17:"I built a browser extension with Jev that can hide/collapse posts on X based on natural language."✅ 已做出并推文演示。"一句自然语言当过滤器"的最小惊艳示例。

### 10. typesafe-adblock — "这是广告吗"(09-19 补充)
- [realZachi/typesafe-adblock](https://github.com/realZachi/typesafe-adblock)(48★):Chrome 扩展,对每个 DOM 元素问 Jev 一个 Noul("is this an ad?")。作者自标 "Fun project"。同作者还有 [pg-jev](https://github.com/realZachi/pg-jev)(见 §七)。

### x-scanner — X 时间线行为标签 + 精确花费角标(09-19 晚补充)
- [oso95/x-scanner](https://github.com/oso95/x-scanner)(7★):Chrome 扩展,帖子进入视口 800px 内即发**一次 Jev 请求带 6 个类型化问题**(5 个行为维度 + 1 个话题检查),~150ms 回数字,帖子还没滚到就打好标签:`✓ clean` 或 `⚑ engagement bait 97%`;点击可见每维度概率条、token 数、该次调用成本与延迟。右下角面板显示本 session "80 posts, $0.0027"——**美元数是精确值**(从返回的 usage 计算,不是估算)。API key 只存本地。✅ 开源可装。

### 09-19 深夜新增(来自 madewithjev.com 收录的 X 演示)
- **Jev + Stagehand** — [@kylejeong](https://madewithjev.com/builds/stagehand-remote-browser)(推文内嵌收录页):远程浏览器近即时操作——观察页面,a11y 树当 state、动作当 questions,Jev 决定下一步、Stagehand 执行。**$0.001/任务**。
- **无截图 computer use** — [@milindlabs](https://madewithjev.com/builds/computer-use-without-screenshots)(推文内嵌收录页):本地 CoreML 分割屏幕 UI 元素 + 端上 OCR 读标签,文本就是 Jev 得到的全部;Jev 返回各元素概率并点击,循环至目标完成。**~90ms/决策,无截图、无像素出机器**。同作者另有"Jev 当 bot 总参谋"的 [OpenMausBot 路由演示](https://madewithjev.com/builds/bot-chief-of-staff)。
- **rocky——语音控制整台电脑(09-21 05 时,A 级)** — [BenjisCollector/rocky](https://github.com/BenjisCollector/rocky):macOS 唤醒词 "watermelon" 即指挥;**路由一次 Jev 请求并行问 13 个问题**(类型/是否对你说的/是否复合/要屏幕吗/哪个 app/哪个站点/引擎…),目标循环三问合一、只读命中的头;**感知只走 a11y 树,零截图进模型**;默认干跑、`--act` 才真点(实测 "open photo booth" 置信 1.00)。把我们案例集里的全部最佳实践(批量问题/有界动作/干跑默认)打包成一个产品。
- **typesafe-computer-use** — Andrew Levin([收录页](https://madewithjev.com/builds/typesafe-computer-use)):macOS computer use,每步一个 Jev 决策,~$0.0002/步。
- 更多 X 演示( [@rileybrown](https://madewithjev.com/builds/agent-model-router) 的模型路由 agent、@YazanO_0、@SigGravi 的实时驾驶模拟器等)见 [madewithjev.com](https://madewithjev.com/) 分类页,共 178 个 build / 76 条 X 帖。

### 浏览器扩展 X 新浪潮(09-19 深夜三扫)
- **MacWork——住进你 Mac 的 worker(09-21 08 时,A 级)** — [gklab/MacWork](https://github.com/gklab/MacWork)([macwork.org](https://macwork.org)):只通过**原生接口**(菜单/a11y 树/快捷指令/Services/App Intents)操作,"不认识任何 app 的名字,因为你无法知道用户装了什么";架构=调用方经 MCP(mac_do/observe/act/resume)→ Python 引擎(观察→一次 Jev 请求→安全底线→执行→等 UI 稳定)→ **持权限的签名 Swift 助手**;不可逆先问、用户碰键盘即交还。
- **jev-browser-chrome——驱动已登录的真实 Chrome(09-20 17 时,A 级)** — [kofanlabs/jev-browser-chrome](https://github.com/kofanlabs/jev-browser-chrome):基于 jev-ultrafast 的分支,经**本地扩展桥**直接操作你**现有已登录的 Chrome 标签页**——绕开无头浏览器的登录/验证码/反爬难题,演示仍是 1× 速度的真实航班搜索并附核验时间戳。
- **YouTube 跳赞助** — [@tdinh_me (Tony Dinh,知名独立开发者)](https://madewithjev.com/builds/youtube-sponsor-skipper) 的推文;开源仓库:[trungdq88/youtube-sponsor-detection](https://github.com/trungdq88/youtube-sponsor-detection)(57★,BYOK):实时听 YouTube 音频,Jev 判"到赞助段了吗"即跳,**~$0.005/视频**。
- **LinkedIn 去 slop** — [sushrutb17/linkedin-noslop-extension](https://github.com/sushrutb17/linkedin-noslop-extension)(开源)+ [Walid Boulanouar 双层版](https://www.linkedin.com/posts/walid-boulanouar_i-built-a-browser-extension-that-removes-activity-7506661817759383553-mAdD)(免费模式扫描层 + Jev 层)。
- **X 帖过滤家族再添成员**:[x-post-firewall](https://madewithjev.com/builds/x-post-firewall)(Pociot)、[实时广告拦截](https://madewithjev.com/builds/realtime-ad-blocker)(@iam_zachi,即 typesafe-adblock 的推文出处)、[reply-guy 评论过滤](https://madewithjev.com/categories/content-and-growth)(@iannuttall,~5 分钟配好)、[Jev Detector](https://madewithjev.com/categories/content-and-growth)(@jozef_gherman,2 秒扫 1 万词,免费)、[Jev Calc 万物计算器](https://madewithjev.com/builds/jev-calc)(@thekitze)、[手势+语音画布](https://madewithjev.com/builds/gesture-canvas)(@jackcheng)。
- **生产环境迁移实例** — [@illyism (ILIAS ISM)](https://madewithjev.com/builds/regex-to-jev)(推文内嵌):把 aiseotracker.com / linkdr.com / genppt.com 里 vibe coding 出来的"正则 slop"整体迁到 Jev,"快 10 倍、省 50%"——**目前最大胆的生产迁移公开案例**。

---

## 四、内容审核 / 评分 / 业务决策类

### 11. killmyidea — 传播最广的社区应用(209 赞)
- **作者** u/stemonte,2026-09-17。✅ 线上可玩:[killmyidea.stemonte.io](http://killmyidea.stemonte.io),[开源](https://github.com/monteduro/killmyidea)(问题定义见 [questions.ts](https://github.com/monteduro/killmyidea/blob/main/src/lib/questions.ts))。
- **做法**:创业点子 → 10 个 0-4 分量规(Score)并行打分,代码加权出总分。"以前要 LLM 推理 30-60 秒,Jev 几分之一秒全并行出分。"
- **翻车点**:u/zerocukor287 实测同一 idea 去掉 "open source" 三个字各项分数大幅漂移("更不可 buildable 了?");u/blu3n0va 指出对法规门槛判断过于乐观。作者承认是 POC:"consistent gut check, not an oracle"。
- **出处**:[reddit.com/r/SideProject/comments/1wiw6tk/](https://www.reddit.com/r/SideProject/comments/1wiw6tk/)

### 12. Attest 声明/索赔核查 API — quorumtech.ch
- 团队账号 2026-09-18 确认正在用 Jev 改进其线上产品 [quorumtech.ch/attest](https://quorumtech.ch/attest)(含 MCP server)。✅ 已上线。
- **做法**:对"声明 vs 提供的证据文档"给 SUPPORTED/PARTIALLY_SUPPORTED/DISPUTED/INSUFFICIENT_EVIDENCE(Choice),判决引用证据中的具体句子 span。
- **关键数据**:190 个标注样本 **95.9% 判决准确率、1.6% overclaim**;**删掉了置信度字段**——24 次真实检查 22 次落在 0.95-0.99,"永远是同一个数的数字不是信息";**证据顺序翻转 5.8% 判决**(公开承认的缺陷);"六种架构、副本、投票、更高推理档都没打赢一次精心设计的单次 grounding 调用"。evals 将发布在 /research。
- **出处**:[1whsav6 评论区](https://www.reddit.com/r/PiCodingAgent/comments/1whsav6/)

### 13. Crowdcheck
[crowdcheck-ai.vercel.app](https://crowdcheck-ai.vercel.app/):144 字帖子测 10,000 个持久化合成人格的 read/like/agree/repost/follow/block 概率(Noul 批量、按组批处理)。✅ 线上(经 Vercel AI Gateway)。

### 14. HA-Jev — Home Assistant 集成
[AboveColin/HA-Jev](https://github.com/AboveColin/HA-Jev):对实体状态的类型化问题变成传感器和自动化动作,带 token 预算熔断。✅

### 15. Supercov — 代码质量评分
u/Nedomas,[supercorp-ai/supercov](https://github.com/supercorp-ai/supercov),Rust,8 小时做的。Jev 给每个源文件打质量分,告诉 agent 先修哪个。**被广泛引用的教训**:"LLM 吃垃圾输入也能凑合,**Jev 必须喂好输入**。扔整个文件问'质量'很差;只问机械性问题(duplicated_code、deep_nesting)追平 CodeRabbit、便宜 100 倍。"([出处](https://www.reddit.com/r/PiCodingAgent/comments/1wjibh5/anyone_here_using_jev/))

### 16. 同型
[Every](https://github.com/sufianetaouil/every)(语义代码搜索:对每个函数问是非题按概率排序)、[Jev Review](https://github.com/devagrawal09/jev-review)(253★,分阶段代码评审+仪表盘)、[Jev Spam Eval](https://github.com/bitnovus/jev-spam-eval)(零样本垃圾邮件 vs TF-IDF)、[jev-search](https://github.com/superagents-lab/jev-search)(Choice+Noul 挑搜索源/查询词再重排)。

### 17. jevmeter — 视频逐句"胡说仪表"(09-19 补充)
[ChetasLua/jevmeter](https://github.com/ChetasLua/jevmeter)(53★):给任意视频加实时 Jev 仪表——每句话打一个 Score,渲染成 16:9 可剪辑画面。即 X 上流传的 "Realtime debate BS meter" 一类 demo 的开源对应物。**推文**:[@chetaslua 发布推](https://x.com/chetaslua/status/2100473581251748216)。

### 垂直业务应用首现(09-19 晚补充)
发布第 4 天,业务场景项目开始取代玩具 demo:
- [jev-loan-triage](https://github.com/ravikadam/jev-loan-triage) — 语音贷款电话分诊:意图、信息充分性、放贷决策。
- [typesafe-screening-mcp](https://github.com/masa-med-ai/typesafe-screening-mcp) — 医学文献:按临床问题筛 PubMed 标题/摘要的 MCP server。
- [jev-reviewer](https://github.com/choxos/jev-reviewer) — 系统综述(systematic review)数据抽取,答案带论文原文引用。
- [grokbot-jev-jobs](https://github.com/mcgalleg/grokbot-jev-jobs) — 公开职位贴 × 个人简历评分(经 Vercel AI Gateway)。
- [explore-typesafe-ai](https://github.com/si618/explore-typesafe-ai) — 合成 FHIR 临床场景上评测 Jev(以 Claude 为参照)。
- [immanuelsavio/jev-experiment](https://github.com/immanuelsavio/jev-experiment) — 工单路由基准:Jev vs 通用 LLM。

### 交易/金融类(09-19 深夜二扫,X 独有场景)
- **jev-trader** — [@jarrodwatts](https://x.com/jarrodwatts/status/2100356151468585346)([开源推](https://x.com/jarrodwatts/status/2100405097029148890)):**895★,两天上 GitHub trending**。Jev 看资产对价格流,Choice 决定 buy/sell,经 [Monad](https://github.com/jarrodwatts/jev-trader) 链上订单簿 Kuru **每 300ms 一个区块执行一次真实交易**(MON-USDC)。Demo:[jev-trader.vercel.app](https://jev-trader.vercel.app)。✅ 开源+实盘。
- **$10,000 交给 Jev** — [@abolbuild](https://madewithjev.com/builds/10k-trading)(推文内嵌收录页):"I gave Jev $10,000 and let it trade"。✅ 演示。
- **jevocks 股票终端** — Prosper Otemuyiwa([收录页](https://madewithjev.com/builds/jevocks)):"Valyu 带证据,Jev 给状态"——每只股票的实时状态判定。✅ 开源。
- **[moomoo-jev-trader](https://github.com/maxlibin/moomoo-jev-trader)(09-20 14 时,A 级)——富途/Moomoo 实盘仪表盘**:真实 OpenD 行情+分钟 K,确定性七因子,每 5 秒一次 Jev 类型化市场点评,置信度门控后才执行;README 顶格警告"先 SIMULATE+shadow,任何模型概率都不构成盈利边际"(受 jev-trader 启发,声明独立)。中文券商生态首例。
- **QuantDinger——全生态星数第二(09-21 23 时,B 级,11,904★)** — [OpenByteInc/QuantDinger](https://github.com/OpenByteInc/QuantDinger):开源 AI 交易 OS + agent trading + vibe trading,含 Jev System One 集成;总量仅次于 jev-ultrafast。另:tiptour-macos(630★,本地 computer use)、phi(481★,编码 agent+RPC+子 agent)。
- **交易实盘数据(09-19 夜,X)** — [@BrendanPlayford](https://x.com/BrendanPlayford/status/2100614031845539975):Jev+微调模型的交易引擎前瞻纸面结果:**375 笔模拟交易、41.1% 胜率**——罕见的诚实数据(未吹嘘),推文自称"this blew up";另有 [Kalshi 预测市场实测视频](https://www.youtube.com/watch?v=Od4j4osz4JY)(用 Jev 评估切尔西伤情新闻/比特币对事件市场价格的影警)。

### 邮件分诊 / 办公生产力 / 研究数据(09-19 深夜三扫,X 实测带数据)
- **欺诈检测级联** — [@nutlope (Hassan)](https://madewithjev.com/builds/fraud-detection-jev-kimi)(推文内嵌):Jev 分类 100 封邮件 **1.42 秒**,<95% 置信度的 31 封路由给 Kimi K3 复核,整条流水线 **96/100 正确、总耗时 16s、$0.07**(Jev 仅 $0.003)——"快速窄模型打头阵、大模型兜底"级联模式的教科书示范。✅
- **1kpapers** — 同作者 @nutlope([收录页](https://madewithjev.com/builds/1kpapers)):1,018 篇论文每篇 24 个主题 Choice,总花费 **$0.08**、中位延迟 256ms;对照:同样的事让摘要模型做要 $3.99。
- **[jev-issue-radar](https://github.com/Patrick-SCH03/jev-issue-radar)(09-20 23 时,A 级)——GitHub 重复 issue 分诊**:检索候选对→Jev 判关系→**并排展示证据段落让人做最终裁量**;只读、从不自动关闭/打标/评论;诚实标注"实验性 MVP,真实仓库质量未立,合成冒烟测试 2/4 命中"。
- **[rspamd-jev](https://github.com/rioriost/rspamd-jev)(09-20 11 时,A 级)——首个生产邮件服务器集成**——Rspamd 的影子评估插件:默认禁用、零分值、不改投递决策、不进 Bayes 学习,Jev 观察与 Ollama/OpenAI/gpt 模块仅作对照基线;README 对数据外发审批/allowlist/合规的要求写得像企业采购清单。社区工程纪律的标杆。
- **邮件分诊实测潮** — [@rileybrown](https://madewithjev.com/builds/500-emails-3-cents):500 封 3.5 美分;[@ryanvogel (vogel)](https://madewithjev.com/builds/inbox-triage-1500-emails):自己 1500 封实测"blown away"(其 [YouTube](https://www.youtube.com/watch?v=9oWxrsRo4d8) 出处);[@iagolast](https://madewithjev.com/categories/triage-and-routing)(西语推):全公司发票秒级会计分类。
- **dabit3 系列** — [@dabit3 (Nader Dabit)](https://madewithjev.com/builds/predictive-launcher):①[键击预言启动器](https://madewithjev.com/builds/predictive-launcher)("the pdf I just downloaded"→最新 PDF 置顶,~100ms/键);②[预测表格](https://x.com/dabit3/status/2100780008193020049)(列头写 "Urgency" 即逐行打分,推文直链);③[Gmail 意图搜索](https://madewithjev.com/builds/gmail-intent-search);实验合集仓库 [dabit3/jev-experiments](https://github.com/dabit3/jev-experiments)(254★)。
- **keep.md 生产迁移** — [@iannuttall](https://madewithjev.com/categories/research-and-data):自家产品 keep.md 的搜索重排快 7×、打标快 50×(对照 GLM 4.7 Flash,零失败),跑在 Cloudflare Workers 上。**又两例正牌生产落地**(另一例见 @illysim 下方)。
- **Mac 应用离线支持 agent** — [@malekoo](https://madewithjev.com/categories/triage-and-routing)(推文内嵌):模型未加载时的安装/排障问答,Jev 拿"用户问题+整个内置手册"当 state,概率判定哪篇文章能答——"app 用自己的文档回答,无模型也不编造",留出集 **42/42**。
- **jev-palette——语义命令面板(09-19 23 时,A 级)** — [amycardoso/jev-palette](https://github.com/amycardoso/jev-palette):⌘K 面板每次击键**一次 Choice 问 77 个命令**,~100ms、约 $0.00004/击键,完整概率分布本身就是排序——无嵌入、无向量库;葡/英意图直配("jogar fora essa mensagem"→Delete message),旁边放着诚实失败的 fuzzy 基线做对照。
- **400 公司×候选人** — [@sarvagya_kul](https://madewithjev.com/builds/job-match-prediction):12 秒 $0.0005 预测录用概率+错配检测,将上 @textbackdoor。🔨
- **研究/数据工具** — [@albicodes](https://madewithjev.com/categories/research-and-data):每提示 100 张图的视觉参考检索(Cosmos/NASA/Met);另有 Obsidian 离线搜索+Jev 重排(jj1373)、英冰词典 Jev 重排(Jökull Sólberg)。

### 长尾场景雷达(09-19 傍晚,来自 jevable / risetive / GitHub 星搜)
一批此前未见过的有趣场景,按新奇度排列:
- **法律预测** — [LegalForecast-MTD](https://risetive.com/jev)(johnhughes3):预测美国联邦法院"驳回动议"裁定,用 micro-Brier 指标评分——Jev 进入司法预测这一严肃场景。
- **真实机械臂** — [robo-harness](https://risetive.com/jev)(grmkris):**SO-101 硬件机械臂**工作台,在有界关节步进和预算约束下选动作;另有 MuJoCo 机械臂实时控制(Dmytro Hrybov,纯文本几何/接触信息)和 MOSS 捡垃圾机器人模拟(metr0x)。
- **税务合规** — [tax-doc-classifier](https://github.com/kyotofin/tax-doc-classifier)(153★):税单页级分类,**261 份 IRS 表单 100% 严格准确**——合规场景的硬数字。
- **逐像素并行作画** — [@anshuc](https://jevable.com/):并行预测每个像素来画图——把"并行输出"特性推向图像合成的实验。
- **毫秒级生成式 UI** — Chris Tate(@ctatedev):经 json-render 毫秒级渲染设计系统组件。
- **3D 虚拟形象表情** — Joao Bortotti:每条消息编排 ~10 个面部/身体决策,合成连贯实时反应。
- **日文地址规范化** — smasato:歧义日文地址对本地地址母库消歧。
- **屏幕共享隐私** — [MrSecret](https://risetive.com/jev)(vkpdeveloper):屏幕共享时自动模糊隐私字段。
- **HTTP 200 里的错误** — [Jev Resilience](https://risetive.com/jev)(vicente-md):检测"状态码成功但内容像报错"的响应。
- **曼哈顿寻路** — Shivam Chauhan:Jev vs Dijkstra/A* 对比测试。
- **学术引用核查** — [citation-verifier](https://risetive.com/jev)(MarissaFamularo):检查被引论文是否真支持引用句。
- **3000 份儿童零食评分** — @nikunj:28 秒 $0.11 多准则打分。
- **SEO 内链审计** — borja:586 页 45 秒 $0.21(同时间 Claude Opus 只处理了 21 页)。
- **GTM/销售自动化(09-19 晚)** — [@outboundphd](https://www.linkedin.com/posts/outboundphd_so-jev-does-in-fact-work-for-building-clay-activity-7506771976632451072-co-4):实测 Jev **即时构建 Clay 工作流**(Clay 是主流 GTM 外呼编排工具)——Jev 进军销售运营场景;同场还有 Michael Tefula 的[1 秒组装 UI](https://www.linkedin.com/posts/michaeltefula_ive-been-testing-jev-a-new-ai-model-from-activity-7506620679417442304-QTlm)(LinkedIn)。
- **电车难题(官方玩梗,病毒传播)** — 出处竟是 [@CompleteSkeptic](https://x.com/CompleteSkeptic)(CEO Diogo 本人):让 Jev 在牺牲几人的选项间做 Choice,经 [Instagram reel](https://www.instagram.com/reel/DdbhDqCt-kF/) 等二次传播成为伦理梗 demo。
- **长尾第二波(09-19 夜,来自 awesomejev 488 条目录)**:[snifftest](https://github.com/DanRWilloughby/snifftest)(**AI 文风检测 linter**——检测"AI 写作痕迹");[riff](https://github.com/scale-venture-partners/riff)(**Scale Venture Partners 出品**的 ruff 式散文 linter);[commit-miner](https://github.com/devanshbatham/commit-miner)(Rust,提交分类+CVE/CWE 关联,安全研究向);[pkg-gate](https://github.com/hemanth/pkg-gate)(hemanth:**npm 生命周期脚本安全门**);西班牙官方公报 [BOE 每日筛查](https://typesafeai.app/)(gov-tech);[jev-tree](https://github.com/nicobailon/jev-tree)(**递归 Choice 突破 255 选项上限**——官方能力边界的社区补丁);vibecheck(发帖前 X 氛围检查)、dmx.to(智能规则的 X 客户端)、smart-switch(macOS 窗口切换预测)、jev-rerank(单次 30 文档)、qualm("把不确定性做成类型")。
- **长尾第十二波(09-22 11 时,A 级×3)**:[JohnRSandoval/meaning-assert](https://github.com/JohnRSandoval/meaning-assert)——**语义断言库**:"测输出的含义,不是字面匹配"——用自然语言写断言,Jev 判断实际输出是否满足;换措辞可以过,改事实就 fail,证据不足返回 inconclusive;附在线回放+录制 API 响应。[1104480426-hash/jev-qq-assist](https://github.com/1104480426-hash/jev-qq-assist)(中文)——**手机 QQ 聊天参谋**:读当前聊天窗口→判断"对方在等你回吗/想要什么/情绪多强/随便回会不会搞砸/该用哪种策略";本地量化 ONNX 或远程真 Jev,**只给判决不替你打字**,消息永不上传,APK 直接装。[wotai-dev/typesafe-jev-tools](https://github.com/wotai-dev/typesafe-jev-tools)——**"这个决策到底需要模型吗?"的 Claude Code 钩子**:写代码含 LLM 调用时自动注入三问测试——正则能答?前沿模型?还是"正常人一秒能答"的 System One 带?"这个钩子存在的目的就是防止第一带的陷阱:用判断模型去测正则就能产生的标签,得到一个自信但无意义的数字"。
- **长尾第十一波(09-22 08 时,A 级×2)**:[nadyth/jev-crash-course](https://github.com/nadyth/jev-crash-course)——**11 关 Jev 通关教程**(Level 0-10,~65 分钟):从零到实战,每关都有可运行示例(LLM 半用 LiteLLM 任意 provider 供_KEY,含免费选项);uv 管理,pytest 测试,进度独立可跳。[leonininder/remember-me](https://github.com/remember-me)——**agent 记忆"该水合哪些"**:本地召回找候选→Jev 在**脱敏后**的数据上做门控(include/stub/skip/promote);核心原则"**Jev 从不排序,只做准入**";离线默认(FakeJev),在线模式可批量多候选一次 POST。
- **长尾第十波(09-22 05 时,A 级×3)**:[eriestra/blockly-jev](https://github.com/eriestra/blockly-jev)——**Blockly 积木块里嵌入 Jev 判断**:Noul→Boolean/Choice→String/Score→Number,六种积木块(jev_if/jev_switch/jev_choice…),任何原生 Blockly 积木都能被 Jev 驱动——**"语义编程"进入可视化编程教育工具**;[gavansmyth-arch/jev-chrome-extension](https://github.com/gavansmyth-arch/jev-chrome-extension)——**Chrome 侧边栏 agent**:输入目标→Jev 依次点击/填写/滚动当前标签页直到完成;也可选中文本→右键→问 Jev 是非/选一/评分问题;Alt+J 全局唤起,两分钟装好。[vishalbitit/jev-prior-auth-triage](https://github.com/vishalbitit/jev-prior-auth-triage)——**医保预授权分诊(垂直行业 POC)**:Jev 判断"这个 PA 请求该去哪个审批通道"而非"批不批";合成数据+完整免责声明+在线结果看板。
- **长尾第九波(09-22 02 时,A 级×2)**:[rishhavv/tabjev](https://github.com/rishhavv/tabjev)——**每个新 Chrome 标签页自动归入正确分组**(~150ms,约一分钱/月):URL+标题→一次 Choice→返回分组名;与 LLM 方案对比清晰("2-30 秒+一分钱/次,所以别人的 AI 标签整理器要按按钮,这个在每个标签页上跑");冷调用 1133ms(TLS+service worker),热调用远低于此,设置页实时显示两个数字让你验证。[CompleteDotTech/jev-factorio-agent](https://github.com/CompleteDotTech/jev-factorio-agent)——**Factorio 游戏代理**:Jev 做宏观决策(目标/下一步/卡住检测),确定性代码管游戏规则和执行;"Jev 选 what,代码管 how";支持 mock 后端完全离线跑。
- **长尾第八波(09-21 23 时例行,A 级×2)**:[RiwRiwara/jev-computer](https://github.com/RiwRiwara/jev-computer)(泰文+英文)——**用 Jev 的一个是非问题造出 8 位计算机**:问 "a 和 b 都是 1 吗?"→四种输入即 NAND 真值表→2,102 个 NAND 搭出 8 位 CPU+16 字节 RAM;7×6=42 用了 59 个时钟周期/124,018 次门求值/124 次 Jev 调用/$0.000019。程序是纯 JSON。[Anmol-Srv/jev-video-search](https://github.com/Anmol-Srv/jev-video-search)——**语义视频场景搜索**:嵌入检索 50 候选(~30ms)→Jev 逐个判断"真的匹配吗";核心洞察:"嵌入永远返回 k 个,没有拒答能力";Jev 在不可回答的查询上保持 0.55-0.57 边际,且能处理嵌入丢掉的关系("车**里**的笔记本电脑"≠"桌上笔记本电脑+旁边停着车")。
- **长尾第七波(09-21 14 时,A 级)——"番茄炒蛋问题"**:[fancyboi999/ockev](https://github.com/fancyboi999/ockev):"Ship the result, not the conversation"——专治 agent 交付物里的**否认式废话**(apophasis:"实现了 JWT 认证(注:没用水印,没做镜像,没做下拉刷新,没做骨架屏)");35ms 本地判别式决策引擎(Apple Silicon MLX/CUDA),自建 **TomatoEggBench-120** 标 95.8% 准确率。写作质量工具线再添干将。
- **长尾第六波(09-21 11 时,A 级×2)**:[1aifanatic/jev-uipath-coded-agent](https://github.com/1aifanatic/jev-uipath-coded-agent)——**UiPath 编码 agent × 反洗钱(AML)警报分诊**(金融业 FINS 演示):LLM 网关读信/抽实体/做算术/写理由,**Jev 做全部决策**(5 红旗+风险级+处置),~400ms/次——**企业级 RPA 集成首例**;[fruitymcdoo/JevChat](https://github.com/fruitymcdoo/JevChat)——把文本生成反向重建:回复的**每个词都是 17000 词字典上的一次类型化决策**,另一个 Jev 当裁判决定"够不够格发送"(实测 87-94% 通过),UI 流式上词并展示每次决策;关键发现:"Jev 看得到完整句子时选词很强,选项脱离语境就弱"。
- **长尾第五波(09-21 08 时,A 级)——语义前端首例**:[etweisberg/jev-ui](https://github.com/etweisberg/jev-ui) 给 React 装上概率 UI:`<JevSwitch>`(Choice+无匹配兜底,选渲染哪个子树)、`<JevList>`(Choice 或逐项 Score,排序/过滤/截断)、`<JevReveal>`(Noul,条件成立才浮现)+ `useScore`;环境变量驱动,**record/replay 夹具让 UI 测试不花钱**,key 只在服务端。
- **长尾第四波(09-21 05 时,A 级×2)**:[watfile](https://github.com/jexp/watfile)(jexp,Neo4j)——文件语义归档:标题/摘要级抽取→一次 Choice→文件自动进对应文件夹,Classifier 抽象可插本地 MLX/laya 后端;[semantic-microscope](https://github.com/abhishekmishragithub/semantic-microscope)——逐句校准标注显微镜:每句一次请求 5-6 问,多泳道视图读整份文档,**3000 句 ≈ $0.08/3.5 分钟**,RFC 9110 演示,全程无 LLM。
- **长尾第三波(09-19 深夜,X/LinkedIn)**:[taratt 的零样本机器人操作](https://www.linkedin.com/posts/taratt_zero-shot-robot-tasks-with-the-new-typesafe-activity-7506600373059588096-FlJN)(视频:口头指令→零样本操作方块);[harshil1712 的 Cloudflare Workers 语音 agent](https://www.linkedin.com/posts/harshil1712_i-got-access-to-jev-a-new-model-from-typesafe-activity-7506395781399080961-4bKA)(即 slidepilot 作者);**"Jev 当弱标注器"模式**(r/singularity 评论区):用 Jev 批量合成训练数据→训一个传统分类器部署——把单价再压一个数量级的两段式架构。
- **翻译级失败案例(可贵)** — @hanz 的空战 AI 自述 "it kinda sucks";@Mnimiy 的草稿质量门出现"agent 沉默需第二个 agent 解救"的元失败——**少见的诚实翻车记录**。

### 内容增长/营销分析类(09-19 深夜新增,X 上的主力玩法)
- **SuperX 病毒度评分** — [@robj3d3 (Rob Hallam)](https://x.com/robj3d3/status/2100722975645598191)([构建过程推](https://x.com/robj3d3/status/2100631889585606959)):每条草稿帖过 **61 个 Jev 问题、~1s、$0.0004**;在 207 位创作者的 9,481 条真实帖子上拟合,"3 次里 2 次选中病毒帖,从不奖励回复诱饵"。免费无注册。✅
- **724 条竞品广告拆解** — [@TheMattBerman](https://madewithjev.com/builds/competitor-ad-teardown)(推文内嵌收录页):40 秒拆完 37 个品牌 724 条在投广告——每条的 hook/格式/offer/CTA/认知阶段/落地页错配,共 **$0.09**;将集成进 stealads + MCP。✅
- **自有账号增长复盘** — [@iannuttall (Ian Nuttall)](https://madewithjev.com/builds/x-post-analysis)(推文内嵌收录页):3,282 条 X 帖(累计 1 亿曝光)每条 8 个问题,全量 4.25M token、8 分 34 秒、**$0.1282**;结论如"how-to 类中位点赞 150 vs 均值 44""AI+编程是 1.9× 话题乘数,SEO 仅 1.0×"。✅ 一次性分析。
- **700 条线索外联评分** — [@romanbuildsaas](https://madewithjev.com/builds/lead-outreach-scoring)(推文内嵌收录页):预测每条个性化外联消息表现 + 置信度 + 线索-消息错配,$0.09/700 条;将进 GojiberryAI+MCP。🔨 即将上线。

---

## 五、路由 / 调度 / 上下文管理类

### 18. jev-codex-router — 第一个带回测数据的模型路由器(09-19 补充)
- **作者**:GitHub [0xNatoshi](https://github.com/0xNatoshi/jev-codex-router)(29★),2026-09-17。
- **做法**:Codex 每一轮先过 Jev 分类,选最便宜的能扛的模型 + 合适的思考深度(luna/sol/astra 三档),决策成本 ≈$0.00003、≈0.6s/轮;置信度低于 0.5 不降级只回中档;fail-open + kill switch。
- **数据**:**7 天 237 个真实 turn 回放,省 ≈60% 成本**;回测还发现"低置信回退到旗舰模型会吃掉 ~80% 节省"。
- **意义**:把社区喊得最响的"模型路由"想法真正落地并给了可复算的协议(BACKTEST.md)。

### 19. 上下文压缩/compaction 系
[kamchatka 的 Jev 压缩示例](https://github.com/ljedrz/nachalnik/blob/master/kamchatka/examples/jev_assisted_compaction.rs)、[jev-cli 的 compact/rerank/verify 子命令](https://github.com/Nasrallah-AL/jev-cli)、[fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction)(**2,735★——按 awesomejev 统计为社区工具类星数第一**,09-19 修正:此前低估)、pi-warden 的大输出压缩、o_sht_hi 的"实时剪枝工具输出"构想([出处](https://www.reddit.com/r/PiCodingAgent/comments/1wjibh5/anyone_here_using_jev/))。

**09-19 晚第二波(该场景一夜之间成为红海)**:
- **winnow** — [GhalebDweikat/winnow](https://github.com/GhalebDweikat/winnow)(17★,升星最快):Claude Code 的"校准上下文筛"。每个大 Read/Bash/Grep 结果切成 ~25 行块,**一次 Jev 调用并行问 N 个 Noul**("这个块当前任务需要吗");高置信不需要的块替换为三行 stub(隐藏了什么 + 廉价模型一段摘要 + 恢复 key),`winnow_recall(key)` 可随时取回全文——"什么都没丢,只是先不花 token"。还设计了用官方 system-one-adapter(Haiku 4.5 充当未校准 judge)的降级路径。带测试。
- **jev-pruner** — [tamaratran/jev-pruner](https://github.com/tamaratran/jev-pruner)(12★):Claude Code 插件,Bash 输出**跑完之后、送回模型之前**剪枝。≤10k 估算 token 直通;错误/JSON/diff/二进制/整文命令(cat/jq/git diff)不动;逐块 Noul"这块里有需要留的行吗",一条需要即保整块;请求批处理压在 30k token 内,历史与输出共享预算、按序分片不截断字段。
- **pi-jev-context** — [Nyarlathoteppppp/pi-jev-context](https://github.com/Nyarlathoteppppp/pi-jev-context):pi 的 cache 中立上下文裁剪(pi-heed 作者的第三个 Jev 项目)。

### 20. skillranker — 技能路由(09-19 补充)
[Dicklesworthstone/skillranker](https://github.com/Dicklesworthstone/skillranker)(44★):Rust CLI,用 Jev 按当前会话状态给 agent 技能排序,挑下一步该用哪个。

- **dynamic-context-engine——段落记忆(09-20 20 时,A 级)** — [rohanarun/dynamic-context-engine](https://github.com/rohanarun/dynamic-context-engine):项目笔记/偏好/文档存 **SQLite**,请求时 Jev 逐段判相关性,拼成**有界、带来源标签**的上下文——**无嵌入、无向量库、无生成式改写**,tiktoken 显式预算;[在线 playground](https://getsupers.com/demos/context-engine/)。记忆检索被压缩场景之外又开出一条新路。
- **jevusher——上下文门童(09-20 11 时,A 级)** — [cvsgireesh/jevusher](https://github.com/cvsgireesh/jevusher):"引座员不决定演出,只决定谁进门、坐哪里"——J1 路由(哪个模型配这一轮)/J2 技能门(200 个技能选 1)/J3 记忆筛选/J4 工具输出过滤/J7 抓取内容筛查/J6 早停/J5 压缩,七关卡一图流;**"便宜模型读一切,贵模型只读幸存者"**(号称比 Opus 直读便宜 ~350×)。压缩/路由/门控三大场景的集大成文档。
- **jev-labeler-action(09-21 20 时,A 级,yamadashy)** — 零配置 AI issue 打标:对每个仓库标签(用 GitHub 里已有的标签描述)问一个 Noul,≥0.8 才贴;Job Summary 列出全部概率,dry-run 可先看。**本轮最佳安全表述**:"恶意 issue 最多骗到一个错误标签——没有可劫持的评论、没有可调用的工具"——对不可信输入为什么用 Jev 而不用 LLM 的一句话论证。
- **记忆系统成为新赛道(09-21 23 时,B 级)** — 继压缩之后,Jev 做记忆检索正在分叉成独立方向:[hippo-memory](https://github.com/kitfunso/hippo-memory)(750★,生物启发式:衰减/检索增强/整合)、[agent-beacon](https://github.com/Asymptote-Labs/agent-beacon)(606★,跨 harness 自进化记忆层)、[reticle](https://github.com/reticlehq/reticle)(796★,"agent 能写代码但难以理解自己写的")、[distill](https://github.com/samuelfaj/distill)(682★,更少 token 干更多事)。
- **jevcache——"要不要调用模型"的本地缓存层(09-19 20 时,A 级)** — [kushals256/jevcache](https://github.com/kushals256/jevcache):OpenAI 兼容本地代理,用 Jev 做**校准的 same-intent 判定**(而非余弦相似度),同一问题换个说法即缓存命中、跳过昂贵的 LLM 调用;Jev 出错则 fail-open 照常调模型。README 实测:MISS ~3.2s → HIT ~0.4s。npm(`@kushalicious/jevcache`)+Docker,30 秒可试。口号精准:"Routers pick a model. jevcache decides whether to call one."——与路由器场景互补的新基建位。
- **stanley-code——会自进化的 Jev-first 编码 agent(09-19 23 时,A 级,12★)** — [devagrawal09/stanley-code](https://github.com/devagrawal09/stanley-code)(即 jev-review 作者,前身为 jev-code):Jev 把请求路由到确定性工作流(内置/插件/**它自己给自己写的**);没工作流可走时落到 Pi agent 兜底,随后台自动生成新工作流、校验、暂存,人工晋升后同类请求再也不用开 agent。npm 已发布。
### 21. 仍处"想法"阶段
- u/o_sht_hi:自然语言路由到 250-300 个 API(未拿到 access,代码打包中)。
- u/getpodapp:把 ArtificialAnalysis 模型分数喂给 Jev 做路由,绕开低额度账号。
- u/lovelace6329:CV↔职位匹配,先用 Jev 重排 top-20(内部已有匹配引擎)。
- **路由器又落地两个(09-19 午后)**:[pi-jev-model-router](https://github.com/da-vinci-noob/pi-jev-model-router)(按任务难度把 Pi 的 prompt 路由到合适模型档位,带预算控制)、[opencode-plugin-jev-auto-model-router](https://github.com/purplesmoke05/opencode-plugin-jev-auto-model-router)(OpenCode 侧,可配置模型白名单)。加上此前的 jev-codex-router、@ephraimduncan、@rileybrown、milindlabs 的 OpenMausBot,**"Jev 当模型路由器"已至少 6 个实现**。
- **路由器再+3(09-19 傍晚,该场景实现已 10+)**:[jev-router](https://github.com/gargpratyush/jev-router)(154★,Claude Code 最便宜模型路由)、[vexjoy-agent](https://github.com/notque/vexjoy-agent)(420★,"/do"把英文请求路由到正确技能)、[agent-router](https://github.com/nidhi-singh02/agent-router)(33★,CLI 选 Cursor/Claude Code/Codex/OpenCode+模型+力度);risetive 目录里还有 prismhq(LiteLLM 逐请求选模型)、pi-jev-router、jcm-router、jev-agent-skill-router、Higgsfield 按提示词选视频/图像生成模型。
- ⚠️ 对照 [Janus](https://github.com/FirasSX914/Janus) 的发现:路由阈值**不可跨数据集迁移**,此类系统需逐场景校准。

---

## 六、数据管道 / 基础设施 / 语言生态

- **pg-jev** — [realZachi/pg-jev](https://github.com/realZachi/pg-jev)(145★,09-19 补充):PostgreSQL 扩展,用自然语言问自己的表。
- **vgi-typesafe** — [Query-farm](https://github.com/Query-farm/vgi-typesafe):DuckDB 扩展,Noul/Choice/Score 变 SQL 表函数,`LATERAL JOIN` 逐行判、`is_true()` 进 WHERE。
- **jev-cli (jevctl)** — [Nasrallah-AL](https://github.com/Nasrallah-AL/jev-cli):`npm i -g jevctl`,Jev 判断变管道友好的退出码 shell 命令;兼容 TypeSafe/OpenRouter/Cloudflare Workers AI;Claude Code 插件。
- **jev-shell-history** — [mrnugget/jev-shell-history](https://github.com/mrnugget/jev-shell-history)(33★,09-19 补充):Fish 风格 zsh 补全建议,由 Jev 从最近 100 条历史里挑"你最可能正在敲的那条"(一次请求两个问题,异步不阻塞);前缀模式命中则零请求直出。
- **jevframe**(09-19 深夜三扫)— [ktaletsk/jevframe](https://github.com/ktaletsk/jevframe):pandas/Polars 的语义层——对 DataFrame 行做分类/情感/打分,数据科学侧第一个集成。
- **jev-connector** — [juanlentino/jev-connector](https://github.com/juanlentino/jev-connector):WordPress 连接器(CMS 侧第一个)。
- **目录再+1**:[jevable.com](https://jevable.com/)(09-19 上线的第三个聚合站,与 madewithjev、risetive 并立)。
- **jev-semgrep(09-19 23 时,A 级,42★)** — [uehaj/jev-semgrep](https://github.com/uehaj/jev-semgrep):**按语义跨语言 grep**——英文含义 "customer is angry" 能直接搜出日文行;每行一个 Noul、30 行合一请求、8 并发,210 行文件 <1 秒;语义与文本可在任意语言组合,零依赖单文件。
- **"语义 if"进入语言本体(09-20 05 时,A 级)** — [carldaws/hunch](https://github.com/carldaws/hunch)(Ruby gem):`if Hunch.almost_certainly?("this order is fraudulent", given: order)`——possibly?/likely?/probably?/almost_certainly?/definitely? 映射到可配置阈值,`chance/pick/rate` 即三原语的 Ruby 方法化;[doublerobust/rjif](https://github.com/doublerobust/rjif) 把同样的"校准 if 语句"带进 **R 语言**。继 Haskell DSL、MoonBit 之后,语义控制流正从库走向语言惯用法。
- **jev-browser-qa(09-20 05 时,A 级)** — [jonymusky/jev-browser-qa](https://github.com/jonymusky/jev-browser-qa):**Playwright 负责开车和拍片,Jev 负责裁判**——自然语言断言、自愈定位器、目标驱动点击循环,带仪表盘,判断全程 <400ms 且零生成 token;测试里"机械导航 + 语义判断"的分工范本。
- [maayanlevy/mysql-ailike](https://github.com/maayanlevy/mysql-ailike)(B)——MySQL 自然语言行过滤,数据库家族第三员(Postgres/DuckDB 之后)。
- **平台级采用(09-19 傍晚确认,09-19 夜修正星数)**:**Vercel [eve](https://github.com/vercel/eve)(**5,253★**)把 Jev 设为默认 evaluation model**;Vercel [ai-cli](https://github.com/vercel-labs/ai-cli)(796★)内置 Jev evaluate;[LanceDB 官方 TypeSafe Reranker](https://risetive.com/jev)(向量/全文/混合搜索重排);[LiteLLM 官方 pass-through 文档](https://risetive.com/jev);[Pydantic AI 的 TypeSafe Model](https://risetive.com/jev);Composio 工具 schema 编译、Braintrust 追踪、Neon Functions 代理([typesafe-on-neon](https://risetive.com/jev));**[n8n 节点 n8n-nodes-typesafe-ai](https://github.com/DomMonte/n8n-nodes-typesafe-ai)**(低代码工作流接入);日本出行应用 TrainLCD 通过 PR 接入 Jev 重排(生产 PR 级采用);[typesafe-ui](https://github.com/BunsDev/typesafe-ui)(shadcn 风格组件)。**Jev 正在成为 eval/路由基础设施的默认选项**。SDK 长尾再扩:Kotlin SDK(09-19 入 awesome-typesafe)、官方目录版 Go SDK、zod-jev、jev-dsl(Haskell!)、typesafe.zig(Zig)、jev-java。
- **09-19 午后新工具波**:[socai](https://github.com/socai-io/socai)(192★,"真正会读社交媒体的 Browser Use agent",快而深——本批最热)、[git-judge-jev](https://github.com/davidrydberg/git-judge-jev)(GitHub Action:给 agent 写的 PR 自动评论"它到底做了什么/改了哪些行为面")、[testedok](https://github.com/shashisp/testedok)(iOS 应用快速测试:a11y 树+Jev)、[intelliprompter](https://github.com/finetuningsingh/intelliprompter)(提词器:讲到哪条自动勾掉哪条)、[stanley](https://github.com/armansra-hub/stanley)(NetSuite 销售的领地情报:Jev 解读公司证据)、[invalidate](https://github.com/chopratejas/invalidate)("AI 记忆的失效层:每条事实有租约,新证据终止它"——概念创新)、[jury.nvim](https://github.com/rashedInt32/jury.nvim)(Neovim 校准选择)、[jgrep](https://github.com/kyu1204/jgrep)("按代码做什么搜,不按它叫什么")、[jev.el](https://github.com/wakamenod/jev.el)(**Emacs 包**)、[jev-chess](https://github.com/hemanth/jev-chess)(知名 JS 开发者 hemanth:走子/局面评估/人格化对手/对局分类)、[JevOnly](https://github.com/buluoray/JevOnly)("纯 Jev 也能'打字'并推进任务")、[jev-desktop](https://github.com/yikangy873-gif/jev-desktop)(Codex Computer Use 内的动作选择)、[jev-capability-atlas](https://github.com/Zaious/jev-capability-atlas)(7★,证据优先的"何时行/何时崩"能力地图)。
- **网关**:官方 API 之外,已可经 [Vercel AI Gateway](https://vercel.com/ai-gateway/models/jev) 与 [Netlify AI Gateway](https://www.netlify.com/changelog/typesafe-jev-ai-gateway)(09-19 补充,changelog 确认 `jev-1.13.0`、~32k token 状态+问题预算)调用。
- **语言 SDK**(发布 3 天内 10+):[Rust×2](https://github.com/AbdelStark/typesafe-rs)、[Swift](https://github.com/alterhq/typesafe-sdk-swift)、[Java](https://github.com/Premo-Cloud/typesafe-sdk-java)、[PHP](https://github.com/Fox-Islam/typesafe-sdk-php)、[.NET](https://github.com/Hawxy/TypeSafeAI.Net)(带 Microsoft.Extensions.AI 适配器)、[Elixir](https://github.com/nshkrdotcom/typesafe_sdk)、[Ruby×2](https://github.com/joshmn/typesafe-sdk)、[Rails](https://github.com/GenieRobot/typesafe-ai-rails)、[Advocaat TS](https://github.com/pithings/advocaat)(67★)、[LlamaIndex Jev 集成](https://github.com/AbdelStark/awesome-typesafe)(09-18 入册)、[RubyLLM TypeSafe](https://github.com/kieranklaassen/ruby_llm-typesafe)([作者推文](https://x.com/kieranklaassen/status/2100088928271585527))。
- **jevcal** — [abhixhek](https://github.com/abhixhek/jevcal):用自己的标注数据拟合每题置信度阈值并在 CI 复检——把"confidence 当架构旋钮"工程化。
- **building-with-jev-skill** — [dbreunig](https://github.com/dbreunig/building-with-jev-skill)(86★,09-19 补充):教 agent 写好 Jev 调用程序的技能包。
- **目录/索引**:[awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe)(214★)、[awesomejev.com](https://awesomejev.com/)、[typesafeai.app](https://typesafeai.app/)(带证据等级)、[madewithjev.com](https://madewithjev.com/)(**09-19 深夜新发现:178 个 build/76 条 X 帖/78 个 GitHub 项目的分类目录,每条带成本与延迟;配套清单 [kraayenjon/awesome-jev](https://github.com/kraayenjon/awesome-jev)**;另有 [risetive.com/jev](https://risetive.com/jev)),另有 5 个新 awesome-jev 目录:[yibie](https://github.com/yibie/awesome-jev)(123★)、[cobanov](https://github.com/cobanov/awesome-jev)(82★)、[fatwang2](https://github.com/fatwang2/awesome-jev)(69★)、[AnotiaWang](https://github.com/AnotiaWang/awesome-jev)(56★)、[hellogumbo](https://github.com/hellogumbo/awesome-jev)(29★)。⚠️ 另有 [Anil-matcha/awesome-jev-by-typesafe](https://github.com/Anil-matcha/awesome-jev-by-typesafe)(498★)系 2023 年老仓库改名转用,内容时效需自行甄别。

---

## 七、游戏 / 具身智能类(官方 Doom demo 的直接余波)

| 项目 | 内容 | 状态/链接 |
|---|---|---|
| [Jev Plays Pokémon](https://github.com/anxkhn/JevPlaysPokemon) | GBA 模拟器,按血量/状态/招式做战斗决策 | ✅ 开源 |
| [Jev Plays StarCraft](https://github.com/phyous/tsai-sc) | 初代 StarCraft 战役,结构化状态 harness + verified run + 概率轨迹 | ✅ 开源 |
| [TypeSafe Mario](https://github.com/fhshaik/typesafe-mario) | NES,模拟器遥测→结构化状态→选合法动作 | ✅ 实验(260★) |
| [HEIST//ONE](https://github.com/AbdelStark/heist-one) | 浏览器潜入游戏,Jev 当 6 个守卫;含一次"文档记录的 live sandbox 逃逸" | ✅ 开源 |
| [Jev Drone](https://github.com/RomanSlack/jev-drone) | MuJoCo 四旋翼,控制和安全在代码,Jev 2.5Hz 做战术判断 | ✅ 开源 |
| Godot 游戏测试 | u/MichettGodot:Jev 盯着玩、找游戏状态异常 | 🔨 早期"already pretty promising"([出处](https://www.reddit.com/r/PiCodingAgent/comments/1wjibh5/anyone_here_using_jev/)) |
| GBC 游戏翻译导航 | u/porkyminch:垄断类 GBC 游戏,想让 Jev 做界面导航(异步步进不卡帧) | 💭 想法([出处](https://www.reddit.com/r/PiCodingAgent/comments/1whsav6/)) |
| NPC 行为 | u/oxygen_addiction 等:LLM 生成选项、Jev 按人格/玩家输入打分 | 💭 想法(同上) |
| [jev-poker](https://github.com/meetr1912/jev-poker) | 单挑德州扑克,旁边实时显示每个决策的概率分布(09-19 晚) | ✅ 开源 |
| [jevtrafficsim](https://github.com/skcache/jevtrafficsim) | Jev 接管整座城市的交通(09-19 晚) | ✅ 开源实验 |
| [werewolf](https://github.com/asfarsadewa/werewolf) | 狼人杀:7 个村民的怀疑度=Jev 校准概率(09-19 晚) | ✅ 开源 |
| [mcts-agent](https://github.com/lhemerly/mcts-agent) | 判别式 MCTS:Jev 原语 × Gemini(09-19 晚) | ✅ 开源实验 |
| [jev_vampire_survivors](https://github.com/oldmoldycake/jev_vampire_survivors) | **Steam 商业游戏实机**:Vampire Survivors 的 BepInEx 插件 + Python 决策脑(09-19 午后) | ✅ 开源 |
| [JevBall](https://github.com/atarikcaliskan/jevball) | **22 个 Jev 踢一场 3D 足球**:每球员一次 Choice(≤14 个本地预算好的候选),整队合成一个请求;球权者 0.30s 决策一次,可按 J 接管任一球员(09-19 17 时) | ✅ 开源 |
| [jevdash](https://github.com/Sunwood-ai-labs/jevdash) | **100% 净室、无版权争议的 2D 平台跳跃基准**(60FPS 确定性物理,双语文档)——对"假 demo/版权"质疑的正面回应(09-20 14 时) | ✅ 开源 |
| [jev-board-game](https://github.com/KeWang0622/jev-board-game) | **"信念作为原语"**:谁是卧底/狼人杀/阿瓦隆,每个玩家=独立 Jev agent,怀疑度是可记录可打分的校准分布;上帝视角看台(怀疑箭头/信念条/完整决策日志)(09-21 08 时) | ✅ 开源 |
| Roulette Wars 整局自玩 | [@NicoSaraintaris](https://x.com/NicoSaraintaris/status/2100745151622664392):让 Jev 把他自己的游戏从头玩到尾,零人工输入(09-19 夜) | ✅ 演示 |
| [jevpilot](https://github.com/standardagents/jevpilot)(77★) | Three.js 驾驶模拟器 + Jev 自动驾驶(09-19 傍晚) | ✅ 开源 |
| [TypeSafe Snake](https://risetive.com/jev)(sorrycc) | 贪吃蛇:sorrycc(知名前端/ArcoDesign 作者)在确定性状态上选合法移动 | ✅ 开源 |
| [Jev Gomoku (MoonBit)](https://risetive.com/jev)(mizchi) | 五子棋双 Jev 对弈,mizchi 用 MoonBit 写 | ✅ 开源 |
| [Talos](https://risetive.com/jev) | Minecraft:选技能/目标/探索方向 | ✅ 开源 |
| 空战实验(@hanz,jevable) | 空战格斗 AI——作者自评"it kinda sucks",珍贵的失败样本 | 🔨 实验 |
| 杀戮尖塔 2(X 演示) | [@coolish/paulwei](https://madewithjev.com/builds/slay-the-spire-2):0.7s/步超人类速度,"画面没看清它就操作完了"(中文推);底层靠 STS2 mod 生态([STS2MCP](https://github.com/Gennadiyev/STS2MCP) 494★ 等) | ✅ 实测 |
| Subway Surfers(X 演示) | [@_MaxBlade](https://madewithjev.com/builds/subway-surfers):超人类速度,**同时打 50 局**,单局 <$0.01 | ✅ 演示 |
| Smash Bros 自搏(X 演示) | [@maubaron](https://madewithjev.com/builds/smash-bros):Jev 同时操控 4 个角色互博,22M token 只花几美分 | ✅ 演示 |
| Tetris(X 演示) | [@AlanDaitch](https://madewithjev.com/builds/jev-plays-tetris):超难模式 0.3s/步,2 分钟 357 块 134 行 | ✅ 演示 |
| 实时关卡生成(X 演示) | [@HugoDuprez](https://madewithjev.com/builds/realtime-game-levels):Jev 在 Choice 里逐组件实时生成游戏关卡——"生成"场景的新解法 | ✅ 演示 |
| [Beat Jev](https://madewithjev.com/builds/beat-jev) | 点球大战对抗 Jev(Render Workflows + Postgres,Ojus M Save) | ✅ 开源 |
| [TypeEvacSafe](https://madewithjev.com/builds/type-evac-safe) | 火灾疏散模拟:每个逃生者一个 Jev 式决策(Meteor Simulation) | ✅ 开源 |
| [jev-piano](https://madewithjev.com/builds/jev-piano) / [音乐操场](https://madewithjev.com/builds/jev-music-playground) | "Jev 写不出一个音符,但问对了问题它就能即兴钢琴"——Jev 选乐句,代码渲染曲谱/音频/MIDI | ✅ 开源 |

官方侧:[Doom bot](https://typesafe.ai/blog/introducing-system-one-models-and-jev)(文本化游戏状态,~10 次/秒,~$7/小时)、wiki racing、[smart-home demo](https://docs.typesafe.ai/demos/smart-home)。

---

## 八、独立评测类(有人真金白银跑过数字)

- **agentjournal.dev:一次法官调用 vs 12-14 维打分**([原文](https://agentjournal.dev/blog/llm-judge-vs-feature-extraction/))——最扎实的一篇。3 任务、5,477 测试行、34.1M token 共 **$1.43**。①简单任务直问 100%,拆维反而丢分;②难任务(日文 NLI)拆维 0.837→0.908;③**12 选 1 的 Choice 在真实记账数据上只有 0.3998**——"理解了单词但选不出 12 选 1,瓶颈是决策格式";与 n-gram 堆叠后 0.9695;④guardrail 场景:直问在 339 条"良性但提及攻击手法"文本上误报仅 1.5%,拆 12 维误报 37.2%(差 25 倍),四次修复全败;⑤**confidence≥0.9 的行上准确率只有 72.2%**。
- **Janus** — [FirasSX914](https://github.com/FirasSX914/Janus):Banking77 + Web of Science 测校准,协议先冻结;最优阈值、模型差符号、"路由是否回本"在两数据集间全部翻转——**路由参数不可迁移**。已打包 `pip install janus-decide`。
- **TypeSafe AI Benchmark** — [iammrduncan](https://github.com/iammrduncan/typesafe-ai-benchmark)(31★):Jev vs Cerebras 上的 Qwen 结构化输出,含成本核算([配套视频](https://x.com/iamMrDuncan/status/2100467548298899918))。
- **Jev Rerank Bench** — [anessbelbati](https://github.com/anessbelbati/jev-rerank-bench):重排对比,保留原始响应与不确定性区间。
- **JevNoiseGate** — 09-18 新入 awesome-typesafe Showcases(噪声门控类工具,[提交记录](https://github.com/AbdelStark/awesome-typesafe/commits/main) 可溯)。
- **20 臂分类基准·探针数据(09-20 05 时,A 级)** — [jev-classification-benchmark](https://github.com/rachit-srivastava-devx/jev-classification-benchmark)(规范已冻结、实现进行中,探针已实测):同一批工单、5 个标签,Jev-1.13 对 15 个聊天模型配置。已确认:**Jev 单次分类 $0.0000166**(395 输入 token,输出计零);"贵的是推理不是模型"——gemini-3.8-flash 为 5 token 的答案默认烧 171 个 reasoning token($0.000693),压到最小推理后 $0.0000518,差 **13×**;且各家关推理的方式互不兼容(gemini 强制 400、gpt-5.3-codex 可关)。
- **提示词技术移植到 Jev(09-19 17 时,A 级)** — [leepokai/llm-prompt-techniques-on-jev](https://github.com/leepokai/llm-prompt-techniques-on-jev):把 refine/chain/choose/rerank 翻译给不生成文本的模型——**把 Jev 的类型化答案渲染回 state 再问一轮,等于用代码补上"草稿纸"**。BIG-Bench Hard/LegalBench/MMLU-Pro/CLERC 全条目实测(约 $9,响应已缓存),npm 包零依赖。直接回应了"Jev 不能多步推理"的已知短板。
- **置信度换算器(09-19 17 时,A 级)** — [adarc8/how-sure-is-jev](https://github.com/adarc8/how-sure-is-jev):`pip install jev-confidence`,把 Jev 概率分布折算成一个 0-1 数 + 人话判词(CERTAIN/CONFIDENT/LEANING/TORN/CLUELESS),六种公式可取共识——"置信度三件套"之后的第四件,解决"0.67 到底能不能自动执行"的落地问题。
- **jevassert——给 Jev 集成做回归测试(09-19 20 时,A 级)** — [dtduc-git/jevassert](https://github.com/dtduc-git/jevassert):对"问题包"断言**准确率、校准度、成本**三件事;record→JSONL→CI 里离线确定性回放(不调 API、不限流),`compare` 对比模型版本升级前后的漂移;还能经官方 system-one-adapter 给普通 LLM 后端跑同一套基准。填补了"Jev 集成缺少 QA 工具链"的空白。
- **jev-prompt-optimization——给 Jev "调 prompt"的元工具(09-21 20 时,A 级)** — [j341nono](https://github.com/j341nono/jev-prompt-optimization)(日文/英文双语):从标注数据自动优化 Choice 的 `instructions` 与各 criteria 描述(标签名固定),进化式搜索用 GPT 当变异算子(EvoPrompt/GEPA),**适应度=Jev 概率分布上的归一化 Brier 分数**,带 Web UI。与 jev-reliability(测量)、jevcheck(契约)合拢成"**测量→优化→回归**"完整工具链。
- **lgtm——证明你的测试真的在测东西(09-21 02 时,A 级)** — [stardeckai/lgtm](https://github.com/stardeckai/lgtm):读每个测试块+其实现,揪出"全绿但什么都没证明"的无效测试;**16,000+ 测试块、347 个对照实现人工标注、阈值在真实代码上拟合**,留出集数字公开;CLI/CI 可跑,还带 `/lgtm` 和 `/actually-test` 两个 agent skill(先写测试证红、再实现)。
- **日文销售电话判定验证(09-20 17 时,A 级)** — [tsekino62/jev-sales-call](https://github.com/tsekino62/jev-sales-call):60 通虚构销售电话、每通 5 问(Choice 结果/Noul×3/Score 回访优先级),jev-1.13.0 实测 **outcome 60/60、Noul Brier 0.012、中位 250ms/p95 511ms**;弱点探针诚实:数"发言人次数"≈随机(37/60)。附逐通结果查看器。作者自注:LLM 生成的干净日志,真实 ASR 文本会更差。
- **可重复性实验·迄今最佳数据(09-20 14 时,A 级)** — [krsna-smnt/jev-moral-dilemmas](https://github.com/krsna-smnt/jev-moral-dilemmas):①1000 次同输入工单调用——类别决策 **100% 确定**,但 Score/Noul 的置信度在输入不变时最多漂移 **14 个点**;②52 个道德难题 × 200 次(共 10,400 次)——48 题完全确定,4 个翻转题的 Choice 置信度全部 **<17%**,高于该阈值连器官摘取/死刑案都从不翻转。**给"翻车区"划出实用阈值,也量化了置信度不稳定这个老 caveat**。
- **bias-bench——首个公平性/偏见基准(09-20 11 时,A 级)** — [natemoo-re/bias-bench](https://github.com/natemoo-re/bias-bench)(Astro 核心开发者):简历筛选偏见基准,方法论照简历审计经典文献(Bertrand & Mullainathan 2004 系)重做;并逐条批驳了此前 Bluesky 病毒式偏见测试的五个缺陷(单份简历混淆、无判断边际、76 个名字挤一个请求不独立、无统计功效、提示词太弱)。**公平性审计成为独立评测新维度**。
- **jevcheck——"pytest for Jev"(09-20 08 时,A 级)** — [sathariels/jevcheck](https://github.com/sathariels/jevcheck):**行为契约测试**——钉住生产契约(模型版本+fixtures+期望答案),候选模型对着 fixture 评,答案翻转或置信下滑即升级失败;默认拒绝 `jev-latest` 浮动别名(需 `--allow-unpinned`)。⚠️ 附带情报:其引用的 2026-09-19 官方模型列表中已出现 **jev-1.14 与 jev-preview 别名**——版本升级在即,正是此类工具的用武之地。
- **jev-reliability——问题级"起飞前检查"(09-20 02 时,A 级)** — [vcjdeboer/jev-reliability](https://github.com/vcjdeboer/jev-reliability):把"这个 Jev 问题能不能拿来当 if 用"变成四维测量——**重复性**(同问两次答案一致吗)、**措辞敏感**(改写引起的变化是否超过噪声)、**分辨率**(量表能否区分条目还是饱和成平局)、**可答性**(是否在对无从评价的东西自信打分);三原语全支持,swamp 框架扩展。把本案例集记录的"顺序/措辞敏感"类翻车点变成了可执行的门禁。
- **置信度校准审计(09-19 午后)** — [does-jev-confidence-mean-anything](https://github.com/Adilmp/does-jev-confidence-mean-anything):专门审计"Jev 自报的 confidence 到底意味着什么"——与 agentjournal(≥0.9 置度仅 72.2% 正确)、Attest(删掉恒 0.95-0.99 的置信度)构成三件套,置信度问题是社区反复回归的主题。
- **⚠️ 假 demo 警示(09-19 晚,元信号)** — [steve8708 公开点名](https://www.linkedin.com/posts/steve8708_jev-is-awesome-but-for-the-love-of-god-please-activity-7506883009443303424-IrBJ):X 上病毒传播的 Jev demo 里混有**加速/伪造**内容("this viral JEV demo you may have seen is fake. This demo too, very fake...")。阅读任何"超人类速度"类 demo 时应保持怀疑,以带 methodology/trace 的仓库(如 jev-ultrafast、tsai-sc、WindTunnel)为准。
- **基准/指标补充(09-19 夜)**:[browser-use-olympics](https://github.com/eriestra/almond-fastloop)(浏览器 agent 基准);jev-shield 自报"94% 拦截召回、0 误报"(作者口径);[jev-orderby-bench](https://github.com/yodablocks/jev-orderby-bench)(09-19 入 awesome-typesafe:"按 Jev 概率 ORDER BY 得到的排序站得住吗");typesafeai.app 的 30 条用例全部达到"E2 工件验证"级(编辑复现),含官方"监管简报 12.2× 降本"用例。
- **WebMCP 基准(nekuda-ai)** — [@0xidanlevin](https://madewithjev.com/builds/webmcp-benchmark)(推文内嵌收录页),开源可复现:[github.com/nekuda-ai/WindTunnel](https://github.com/nekuda-ai/WindTunnel)。Jev+Mercury 2.5+WebMCP 在 49 项网页任务 **49/49 全解,模型成本比 GPT-6 Astra computer use 低 ~112×**(比截图版低 245×);裸 Jev(改装 Ultrafast harness)只有 **25/49**——"选对合法按钮 ≠ 选对下一步",WebMCP 把点击序列压缩为单次工具调用后 Jev 才起飞。分工:Jev 选工具、Mercury 生成参数。**发布 4 天里最重要的基准发现**。
- **负面实测**:u/mpkrass7 发现[官方 quickstart 示例](https://github.com/typesafe-ai/typesafe-sdk-python/issues/2)注释写 `technical`,实际跑 100 次稳定判 `billing`(0.67)([出处](https://www.reddit.com/r/PiCodingAgent/comments/1whsav6/))。
- **轶事**:[@identityTorn](https://x.com/identityTorn/status/2100475121324728615) 称 Jev 早期精度已追平其私有微调 Qwen 分类器(作者自报,不可复现)。

---

## 九、复刻 / Open 替代生态(⚠️ 均非官方 Jev,注意区分)

- **OpenJev(托管版)** — u/Every-Comment5473 / razorback16,2026-09-18,[github.com/razorback16/openjev](https://github.com/razorback16/openjev) + 免费托管 [codiv.ai](https://codiv.ai)(每账号 100M token)。基于 **Matt Mastracci** 的 [vLLM PR #57250](https://github.com/vllm-project/vllm/pull/57250)(DiffusionGemma 单步去噪填"选择题答题卡"),API 兼容官方 SDK。[mmastrac 评测](https://x.com/mmastrac/status/2100626193943052784):DiffusionGemma-as-Jev 198/201 vs Jev 191/201(8 评测集);codiv.ai p50 ~170ms。⚠️ 命名混淆与 ToS 争议见[原帖评论区](https://www.reddit.com/r/LocalLLaMA/comments/1wjlyzr/)。
- **SemIf** — [TheoLeeCJ/SemIf](https://github.com/TheoLeeCJ/SemIf)(**1647★**,09-19 午后已从首日 1510★ 继续上涨,即原 TheoLeeCJ/openjev 改名):"Semantic ifs from open models, on a 3090 at home"——家用 3090 上跑的开源语义 if 层,目前星数最高的复刻。独立、非官方。
- **jevlike** — [vinnylarouge/jevlike](https://github.com/vinnylarouge/jevlike)(905★,2026-09-16,首日 674★):"逆向了一个 jev-like 架构"——选项变 query 向量做注意力、点积一次前向出全概率,比小 decoder 快 ~100 倍;同一打分头还能从图像 patch 给 Doom 按钮/象棋走子打分。收录于 [HF Jev Reproductions Tracker](https://huggingface.co/spaces/multimodalart/jev-reproductions-tracker)。
- **复刻再+4(09-19 深夜三扫)**:[openjev-sglang](https://madewithjev.com/categories/research-and-data) — @ekzhang1 (Eric Zhang):Jev 兼容 API 跑 Qwen3.6-35B-A3B + SGLang radix cache,64 任务 <1s;[jeff](https://github.com/logan-markewich/jeff)(logan-markewich,LangChain JS 维护者)— 自托管 Jev 替代,底座 GliFormer;"[openjev on Qwen 4B](https://madewithjev.com/categories/research-and-data)"(@justALEXWORTEGA,Qwen 4B 上训 MLP 头);r/LocalLLaMA 又出现[自称带 RLCD 训练的开源克隆](https://www.reddit.com/r/LocalLLaMA/comments/1wjieap/)。另有日文 [@wmoto_ai 的本地 Jev 尝试](https://madewithjev.com/categories/research-and-data)。
- **复刻五国杀(09-21 23 时)**:[jaredpalmer/kev](https://github.com/jaredpalmer/kev)(**1,879★**,Qwen3.5 底座的 Jev 族模型,可本地训练和运行——增量极快)和 [wfzyx/von](https://github.com/wfzyx/von)(320★,"开源 System One,<15ms,本地直替")加入战场;SemIf(2,898★)+ kev(1,879★)+ NanoJev(1,735★)+ jevlike(1,152★)+ von(320★)合计 **7,984★**。非官方。
- **Verdict——克隆生态首次"叫板官方"(09-20 23 时,A 级,148★)** — [openJev-verdict-2.0](https://github.com/Heman10x-NGU/openJev-verdict-2.0)(+[Verdict-open-jev](https://github.com/Heman10x-NGU/Verdict-open-jev) 33★):151M 非自回归决策引擎(ModernBERT/GLiClass),作者自报 **Top-1 77.10%、ECE 1.44%、~20-25ms/次、浏览器 WebGPU 零云端可跑**,称在 LocalLLaMA typed-decisions 基准上胜过 Jev 与 Laya;两模型分工(JevBench 通用版 + 工作流特化 2.0 版)。⚠️ 均为作者自评,Apache-2.0。非官方。
- [laya-jev-compatible-server](https://github.com/exfly/laya-jev-compatible-server)(09-20 23 时,A 级)—— 给开源 **Laya 多语模型**套官方兼容层:POST /v1/systemone + /v1/models,typesafe-sdk 改 base_url 即用;开源模型侧的"平替基建"正式成型(中文 README)。非官方。
- **复刻再+5(09-19 傍晚,高星)**:[NanoJev](https://github.com/TianyuCodings/NanoJev)(451★,并行决策+动态候选+**端到端训练管线**,教学向)、[simple-jev](https://github.com/featherless-ai/simple-jev)(99★,Featherless 出品:任意开源模型一键变 Jev 端点)、[jev-visual](https://github.com/hr98w/jev-visual)(112★,Apple Silicon 上的可视化推理教学实验)、[decider](https://risetive.com/jev)(Qwen3.5-2B 微调出校准概率)、Parallel Constrained Decoding(RLCD 训练的 Qwen2.5-1B,替代路线探索)。**克隆生态总星数已超 4000**。
- **2 小时克隆**:HN 用户贴出 [@harshagundal](https://x.com/harshagundal/status/2100044305536889015) 推文称 2 小时拼出等价物(仅推文为证,未验证)。r/LocalLLaMA 用户 No_Incident_6009 在[同帖](https://www.reddit.com/r/PiCodingAgent/comments/1whsav6/)贴了 BERT-mask 式完整方案,自称"跑了一阵就停了"。

---

## 十、官方示范(单独归类)

[docs.typesafe.ai](https://docs.typesafe.ai/):[cookbooks](https://docs.typesafe.ai/cookbooks/parallel_questions)(并行问题/重排/语义搜索/guardrails/抽取/分类)、[模式库](https://docs.typesafe.ai/patterns)(speculative fan-out、置信度门控路由、组合打分、意图路由)、Doom / wiki-racing / [smart-home demo](https://docs.typesafe.ai/demos/smart-home)、Playground 三教学用例(简历筛选/客服审计/工单路由,见 [flaviocopes 深潜](https://flaviocopes.com/jev))。第三方教程:[LangChain 指南](https://www.langchain.com/blog/building-a-harness-with-jev)、[DataCamp](https://www.datacamp.com/blog/system-one-models-jev)、YouTube([wtf is jev?](https://www.youtube.com/watch?v=QbYBRjOaGOo)、[Moritz 全教程](https://www.youtube.com/watch?v=Nq_lu5QT-fI)、[构建编码 agent harness 直播](https://www.youtube.com/watch?v=5Lx4DLLYafM))。知名背书(持续追加):Chrome DevRel 的 Adam Argyle([nerdy.dev/jev](https://nerdy.dev/jev));**Hasura 联创 Tanmai Gopal**([LinkedIn](https://www.linkedin.com/posts/tanmaig_tried-out-a-workflow-on-jev-better-accuracy-activity-7506498916549410816-MZgB):"准确率超 Sol、便宜 100 倍、快 5 倍,This is MASSIVE");**沃顿经济学教授 Kevin A. Bryan(@Afinetheorem)**([推文](https://x.com/Afinetheorem/status/2099988282520072479):"概率输出型首过判断是极常见的用例,LLM 本来就不是对的模型")。

## 十一、中文社区现状(截至 2026-09-19 晚)

讨论之外,**09-19 出现首批中文/日文落地项目**:
- [qingliu(清流)](https://github.com/pjrpjr/qingliu) — X 时间线清洁工(FeedSieve 衍生,MIT):AI 判定层**带实测标定——误杀率 0.7%,比词库过滤多抓 47% 词库认不出的内容**。目前唯一报出校准数据的中文项目。
- [jevcode](https://github.com/miounet11/jevcode)([jevcode.ai](https://www.jevcode.ai)) — 中文技术方案与最佳实践站。
- [jev-fedspeech](https://github.com/TurboGuo/jev-fedspeech) — 美联储发布会实时鹰/鸽判读,Jev vs 对话模型对照(中文作者)。
- **[@coolish/paulwei 的中文推](https://madewithjev.com/builds/slay-the-spire-2)** — "我刚实测用 Jev 打(杀戮尖塔 2),行动思考只需 0.7 秒,画面我都没看清它就操作完了……这超人类游戏速度,着实又让我震惊瘫坐了😅"(此前用 GPT-6 Astra 代打,能力强但速度慢)。目前传播最广的中文 Jev 实测推。
- **中文 KOL 实测(09-19 深夜三扫)**:[@nicekate8888](https://x.com/nicekate8888)(nicekate):亲自调用 **279 次**实测并出[中文案例盘点视频](https://www.youtube.com/watch?v=FQFKZiDOYAM)(浏览器自动化/邮件分类/上下文压缩/打游戏/复原魔方);[@vista8](https://x.com/vista8)(向阳乔木):"Waitlist 很快通过,Codex 调用成功……Jev 是一个非常强的、高性价比的决策层";[@pirrer](https://x.com/pirrer)(fox hsiao,繁中长推)。中文聚合站:[jev-hub](https://github.com/mizzlelover/jev-hub)(保留原链与作者的 X 演示聚合)。媒体:网易([Pociot 插件详解](https://www.163.com/dy/article/L73I8B8T055627NS.html))、[36氪](https://m.36kr.com/p/3988716815242885)、[technews](https://technews.tw/2026/09/18/typesafe-ai-introduces-system-one-models-and-jev/)。
- **[work-with-jev](https://github.com/Adkid-Zephyr/work-with-jev)(09-21 02 时,A 级)——飞书/企业微信消息四分类**:告诉它"你是谁、负责什么",工作群消息分进 紧急处理/我的待办/值得一看/暂时略过,汇总成**跨群待办看板**;本地运行、演示免 key、分类可人工纠正、原文保留;README 诚实标注"场景示意,不是准确率评测"。中文生产力场景首个完整产品。
- **[听写纸 semantic-live-caption](https://github.com/limboinf/semantic-live-caption)(09-21 02 时,A 级)——语义标注实时字幕**:网易有道开源流式 ASR(Confucius4-R2T2)+ Jev 逐句实时判断——重点加粗波浪线/情绪楷体浮注上色/意图句尾盖〔问〕〔行动〕章;**意图判定四道门**(choice 命中+置信≥0.55+领先幅度≥0.12+Noul 复核,高误伤类目复核线 0.70),标签体系可自定义且能经 DeepSeek 自动生长;零构建单 HTML,key 只存 localStorage。**置信度门控工程的中文教科书**。
- **[rag-jev](https://github.com/Nixz0824/rag-jev)(09-21 14 时,A 级)——中文项目方法论新标杆**:《英雄联盟》国服公告 RAG 问答;数字只来自公告的结构化抽取+模板渲染(**不经生成模型**),解析用确定性正则(48/48 盲测、零延迟),Jev 只做重排与自检(**$0.0001/次**);**78 题独立盲测(出题人被禁止读语料)+48 条解析盲测+18 条陷阱题**,同源与盲测分开记账;拒答靠黑名单+覆盖边界+回退(盲测 10/10);**负面结论全写进报告**(三种排序过滤后打平、门槛测量后不采用、Jev 曾把答案挤到 @2 已加置信闸门);93 项单测+CI。30 个版本/4995 chunks。
- **[twitter-jev-guard](https://github.com/qs-lll/twitter-jev-guard)(09-21 11 时,A 级)——X 时间线水印卫士**:低质帖不隐藏、**打红色半透明旋转 STOP 印章**(阈值 75% 可调),广告帖盖琥珀 AD 章;两问并行(值得提醒吗/什么类型:垃圾诈骗/推广/诱导/疑似误导/有价值),扩展后台直调 Jev 无需本地代理,限并发;免责声明完整("个人浏览辅助,非事实核查")。
- **中文枢纽站 [awesome-jev-zh](https://github.com/yzfly/awesome-jev-zh)(09-20 20 时,A 级,26★)** — yzfly(awesome-chatgpt-prompts-zh 维护者)出品:中文精选列表 + 中文上手指南 + [图解说明](https://code.jiangshu.ai/awesome-jev-zh/) + **每日自动收录 GitHub 热门项目**。开篇即金句:"我们今天写的很多 LLM 调用,本质上只是在做选择题";专设"冷静看待"一节收录批判数据(193×为厂商自评上限;独立评测钓鱼任务直问 62.6%、两行正则 91.8%)。CC0。
- **X 时间线意图标注器 [xtags](https://github.com/manifoldor/xtags)(09-20 08 时,A 级,8★)** — 每帖四问:`intent`(告知/说服/挑拨/推销/娱乐)+ 挑拨愤怒/批量生成感/未披露推广三个阈值信号;**标签=一个词+一个数**,意图常显、警示按阈值亮;扩展与油猴脚本双形态。README 的免责与合规声明是中文项目里最完整的(明确"仅供个人本地浏览辅助"、与 X Corp 无关联、需自证辖区合规)。
- **知乎过滤器(09-19 午后)** — [yink12138/zhihu-ai-filter](https://github.com/yink12138/zhihu-ai-filter):Edge 扩展,用 Jev 过滤知乎信息流,"保留与 AI 有实质关联的内容"——**中文平台侧第一个原生过滤器**(此前中文项目都是用 Jev 做,这个是给中文平台做的)。
- **韩文区首个项目**:[maeum-on-attendance-care](https://github.com/kijung4290/maeum-on-attendance-care) — 老人项目出勤风险监控仪表盘(韩文)。另有韩文 X 解读 [@kimmonismus](https://x.com/kimmonismus/status/2100222673385312617) 与 Facebook 视频科普——韩文社区以解读为主、项目尚少。
- 日文区:[jev-technical-term](https://github.com/Zogrus/jev-technical-term) — 听 YouTube 讲座/Zoom 会议时实时判定并显示技术术语的一句话解说。

讨论层不变:[V2EX 三帖](https://www.v2ex.com/t/1242402)([有人用么](https://v2ex.com/t/1242707)、[不如小参数开源模型?](https://www.v2ex.com/t/1242839))、[linux.do 转贴](https://linux.do/t/topic/2916166)、B站搬运;台湾 [INSIDE 报道](https://www.inside.com.tw/article/42416-typesafe-jev-decision-model-agentic-ai)。pi-heed 支持中文约束提取。

---

## 十二、高频模式总结(大家实际在用 Jev 干什么)

1. **给 agent 配安全副驾驶是第一大场景**(pi-warden、Foreman、jev-guard、is-malicious、pi-heed、pi-jev、jev-axi、kamchatka、Bicameral…)。共同形态:Noul 问"可逆吗/符合意图吗/卡住了吗",Score 打危险分,低置信就拦或 steer。70-500ms 延迟让它**塞得进 agent 循环每一步**,这是 3-30 秒的 LLM judge 做不到的。
2. **上下文压缩/compaction 第二大场景**:判断每条工具输出/历史条目"要不要留"(kamchatka、jev-cli、fast-jev-compaction、pi-warden)。
3. **路由与重排从想法进入落地**:jev-codex-router 用回测证明省 60%;但 Janus 证明路由阈值不可跨数据集迁移——逐场景校准是必需品(jevcal 应运而生)。
4. **浏览器/语音/游戏的"实时决策层"**:共同架构是"代码管感知和执行,Jev 只在有界动作空间里做 Choice"(Jev Ultrafast 7.1s 机票、voice-browser 300ms/句、Pokémon/StarCraft/Mario/无人机)。
5. **"把 Jev 当 SQL 谓词/系统工具"的基建化**:pg-jev、vgi-typesafe、jev-cli、10+ 语言 SDK、双网关(Vercel/Netlify)——发布 4 天就被当基础设施铺。
6. **反复出现的实战教训**:
   - **输入质量决定一切**(Supercov:"Jev 需要好的输入",问题要窄、要机械);
   - **一次给太多选项会崩**(agentjournal:12 选 1 只有 0.40);
   - **confidence 不是免死金牌**(agentjournal:≥0.9 置度只有 72.2% 正确;Attest 删掉恒 0.95-0.99 的置信度字段);
   - **对输入顺序和措辞敏感**(Attest 5.8% 顺序翻转;killmyidea 措辞漂移;官方 quickstart 自己翻车);
   - **成本优势是真的**:34.1M token=$1.43、路由决策 $0.00003/轮、语音控制 $0.0002/句——几乎所有作者都主动报成本。

---

## 十三、监控日志(定时任务追加区)

> 本节由每日监控任务(X/Twitter + GitHub)追加,记录新发现的项目与动态。

- **2026-09-19(首版建档)**:基线如上。待观察:quorumtech.ch/research 的 Jev evals、jev-voice-browser 与 Moritz YouTube 的联动传播、SemIf(1510★)能否长出本地生态、官方 waitlist 放开后的一波新案例。
- **2026-09-19(晚,第二次扫描)**:GitHub 仓库总数 539→645(+106),一夜新增约 30 个实质项目(awesome-typesafe 当日 0 新提交,以下为本文档早期索引)。要点:
  - **安全/监督新子类——反 reward-hacking**:[rh-guard](https://github.com/24601/rh-guard)(结构规则+Jev sidecar 拦"篡改评分器/偷看测试",附录制 demo;README 揭示兄弟项目 [JevLint](https://github.com/huntedman/JevLint)、[jevgate](https://github.com/thevibeworks/jevgate)、[Augustus](https://github.com/24601/Augustus));另见 [jevons](https://github.com/LilDojd/jevons)(Pi 执行监督)、[clear-head](https://github.com/VladyslavHontar/clear-head)(Stop hook 声明对账)。
  - **上下文压缩第二波**:[winnow](https://github.com/GhalebDweikat/winnow)(17★,可恢复 stub 设计)、[jev-pruner](https://github.com/tamaratran/jev-pruner)(12★)、[pi-jev-context](https://github.com/Nyarlathoteppppp/pi-jev-context)。该场景一夜成红海。
  - **浏览器扩展**:[x-scanner](https://github.com/oso95/x-scanner)(7★,X 每帖 6 问题打行为标签,精确花费角标"80 posts, $0.0027")。
  - **垂直业务首现**:贷款语音分诊 [jev-loan-triage](https://github.com/ravikadam/jev-loan-triage)、PubMed 筛查 MCP [typesafe-screening-mcp](https://github.com/masa-med-ai/typesafe-screening-mcp)、系统综述抽取 [jev-reviewer](https://github.com/choxos/jev-reviewer)、职位评分 [grokbot-jev-jobs](https://github.com/mcgalleg/grokbot-jev-jobs)、FHIR 评测 [explore-typesafe-ai](https://github.com/si618/explore-typesafe-ai)、工单路由基准 [jev-experiment](https://github.com/immanuelsavio/jev-experiment)。
  - **游戏**:[jev-poker](https://github.com/meetr1912/jev-poker)(德扑+概率可视化)、[jevtrafficsim](https://github.com/skcache/jevtrafficsim)(整城交通)、[werewolf](https://github.com/asfarsadewa/werewolf)(狼人杀)、[mcts-agent](https://github.com/lhemerly/mcts-agent)(Jev×MCTS)。
  - **生态**:Pydantic 文档新增 [Jev 页](https://pydantic.dev/docs/ai/models/typesafe/);[Langfuse](https://langfuse.com/blog/2026-09-18-using-typesafes-jev-for-evals)、[Braintrust](https://www.braintrust.dev/blog/evaluate-agent-responses-with-jev) 接入 Jev 做 eval;Go SDK [typesafe-sdk-go](https://github.com/dwisiswant0/typesafe-sdk-go)(知名安全研究员 dwisiswant0 出品);provider 无关 TS SDK [typedecide](https://github.com/shkumbinhasani/typedecide);YouTube 盘点视频 [8 Wild Things People Already Built](https://www.youtube.com/watch?v=BOn4OMC8O9c)(基于社区清单制作)。
  - **中文/日文首批落地**:[qingliu](https://github.com/pjrpjr/qingliu)(误杀 0.7%、多抓 47% 的实测标定)、[jevcode.ai](https://github.com/miounet11/jevcode)、[jev-fedspeech](https://github.com/TurboGuo/jev-fedspeech)、日文 [jev-technical-term](https://github.com/Zogrus/jev-technical-term)。另:Telegram 反垃圾 [jev_antispam_bot](https://github.com/backmeupplz/jev_antispam_bot)、Discord 真话计 [jev-bot](https://github.com/parzivale/jev-bot)、提问墙 [ask-jev-ai](https://github.com/waynesutton/ask-jev-ai)、可复现性实验 [jev-lab](https://github.com/danielhirt/jev-lab)、语义代码搜索 [jevgrep](https://github.com/Bentlybro/jevgrep)(无索引无嵌入,CLI+MCP)。
- **2026-09-19(深夜,第四次扫描:专扫 X)**:翻完 madewithjev 剩余分类,新增一批 X 独有项目(均已补项目地址+推文地址):
  - **交易类全新出现**:[jev-trader](https://github.com/jarrodwatts/jev-trader)(@jarrodwatts,**895★、GitHub trending**,Choice 买/卖,Monad 链上订单簿 300ms/块真实下单,[推文](https://x.com/jarrodwatts/status/2100356151468585346))、[$10,000 交给 Jev](https://madewithjev.com/builds/10k-trading)(@abolbuild)、[jevocks 股票终端](https://madewithjev.com/builds/jevocks)(Prosper Otemuyiwa)。
  - **游戏类 X 演示潮**:[杀戮尖塔 2](https://madewithjev.com/builds/slay-the-spire-2)(@coolish/paulwei **中文推**,0.7s/步)、[Subway Surfers 同时 50 局](https://madewithjev.com/builds/subway-surfers)(@_MaxBlade,<$0.01/局)、[Smash Bros 四角色自搏](https://madewithjev.com/builds/smash-bros)(@maubaron,22M token/几美分)、[Tetris 超难](https://madewithjev.com/builds/jev-plays-tetris)(@AlanDaitch,134 行/2 分钟)、[实时关卡生成](https://madewithjev.com/builds/realtime-game-levels)(@HugoDuprez)、[Beat Jev](https://madewithjev.com/builds/beat-jev)、[TypeEvacSafe 疏散模拟](https://madewithjev.com/builds/type-evac-safe)、[jev-piano 即兴钢琴](https://madewithjev.com/builds/jev-piano)/[音乐操场](https://madewithjev.com/builds/jev-music-playground)("Jev 写不出音符,但能即兴")。
  - **其他**:YouTube 创作者 vogel 的 [千封邮件批量分诊实测](https://www.youtube.com/watch?v=9oWxrsRo4d8)(100→1000 封,~200ms/封,含类目/优先级/垃圾/回复预测);dev.to 出现 [valyuai 实战指南](https://dev.to/valyuai/how-to-use-jev-a-practical-guide-to-typesafes-system-one-model-g5e)(明确指出官方 eval 的共识标签=GPT-6 Astra+Fable 5.1 平均、自跑无独立复现);Elixir SDK 在 [ElixirForum](https://elixirforum.com/t/typesafe-sdk-jev-the-first-system-one-model-from-typesafe/76700) 发布。
  - **模式新增**:①"Jev 当交易员"(300ms 决策窗口恰好匹配区块链出块节奏);②"用 Choice 做生成"(关卡/音乐:在预定义组件库里选,绕开"Jev 不能生成"的限制)。
- **2026-09-19(深夜,第五次扫描:X 专项深挖)**:翻完 madewithjev 全部 8 个分类(178 build)+ X/中文直接搜索,新增约 25 个项目(均已带双地址):
  - **邮件分诊/级联实测潮**:[欺诈检测 Jev→Kimi K3](https://madewithjev.com/builds/fraud-detection-jev-kimi)(@nutlope,96/100、$0.07,<95% 置信路由大模型——级联模式教科书)、[1kpapers](https://madewithjev.com/builds/1kpapers)(同作者,1018 篇论文 $0.08)、500 封邮件 3.5 美分(@rileybrown)、1500 封自测(@ryanvogel/vogel)。
  - **生产环境落地+2**:[keep.md](https://madewithjev.com/categories/research-and-data)(@iannuttall,重排快 7×/打标快 50×,Cloudflare Workers)、[@illyism 三站正则迁移 Jev](https://madewithjev.com/builds/regex-to-jev)("快 10 倍省 50%");另有 Every 编辑部(@danshipper,1709 判断<$0.01)、Mac 应用离线支持(@malekoo,42/42)。
  - **浏览器扩展新浪潮**:[YouTube 跳赞助](https://madewithjev.com/builds/youtube-sponsor-skipper)(@tdinh_me/Tony Dinh,$0.005/视频)、[LinkedIn 去 slop](https://github.com/sushrutb17/linkedin-noslop-extension)(+Walid Boulanouar 双层版)、reply-guy 过滤(@iannuttall)、Jev Detector(@jozef_gherman)。
  - **生产力**:dabit3 三连(键击预言启动器/预测表格/Gmail 意图搜索,~100ms/键)、Jev Calc(@thekitze)、手势语音画布(@jackcheng)、[DiffJury](https://diffjury.up.railway.app)(PR 能不能合,@raihankhan_rk)、400 公司×候选人(@sarvagya_kul)。
  - **复刻+4**:openjev-sglang(@ekzhang1,Qwen3.6-35B+SGLang,64 任务<1s)、jeff(logan-markewich/LangChain,GliFormer)、Qwen 4B+MLP(@justALEXWORTEGA)、r/LocalLLaMA RLCD 克隆。
  - **生态**:pandas/Polars 语义层 [jevframe](https://github.com/ktaletsk/jevframe)、WordPress 连接器 jev-connector、第三个聚合站 [jevable.com](https://jevable.com/)。
  - **中文圈实测**:nicekate 279 次调用+[中文盘点视频](https://www.youtube.com/watch?v=FQFKZiDOYAM)、向阳乔木 @vista8、fox hsiao @pirrer 长推、聚合站 jev-hub;韩文首个项目(养老出勤监控)。
- **2026-09-19(午后,第六次扫描)**:GitHub 仓库总数 645→**718**,新增约 30 个;星数动量(数小时差):**jev-ultrafast ~5955★**(此前约 2.9k)、SemIf 1510→1647★、jevlike 674→905★、jev-trader 895→929★、foreman 280→309★、pg-jev 145→175★、awesome-typesafe 214→252★。主流媒体进场:[TechCrunch 报道](https://techcrunch.com/2026/09/18/a-new-kind-of-ai-model-from-a-chatgpt-inventor-is-thrilling-developers/)。新增要点:
  - **守门类第三波(9 个)**:hermes-jev-approvals(**8.7× 快 / 4× 便宜**,少数带对比数字)、toolgate("开源 auto mode")、noulgate、construct-auto-classifier、omp-typesafe/omp-jev-decision、codex-jev-assistant、jev-lens("Claude 刚做的事我需要看吗")、cmdc-auto-mode、bouncer。
  - **模型路由器 +2**:pi-jev-model-router、opencode-plugin-jev-auto-model-router——该场景实现数已 ≥6。
  - **工具/编辑器**:[socai](https://github.com/socai-io/socai)(192★,会读社交媒体的 Browser Use agent)、[git-judge-jev](https://github.com/davidrydberg/git-judge-jev)(GH Action:给 agent 写的 PR 自动写"它真做了什么")、[invalidate](https://github.com/chopratejas/invalidate)(AI 记忆失效层,概念创新)、[jury.nvim](https://github.com/rashedInt32/jury.nvim)(Neovim)、[jev.el](https://github.com/wakamenod/jev.el)(Emacs)、[jev-chess](https://github.com/hemanth/jev-chess)(hemanth)、testedok(iOS 测试)、intelliprompter(提词器)、stanley(NetSuite 销售)、jgrep(语义 grep)、JevOnly(纯 Jev 打字推进任务)、jev-desktop、jev-capability-atlas。
  - **游戏**:Vampire Survivors(BepInEx 插件在 **Steam 商业游戏实机**上跑,超越模拟器阶段)。
  - **评测**:does-jev-confidence-mean-anything(置信度校准专项审计——与 agentjournal、Attest 构成"置信度三件套")。
  - **中文**:zhihu-ai-filter(知乎信息流 Edge 扩展过滤,**中文平台侧第一个**)。
  - **观察**:守门/压缩/路由三大场景进入同质化竞争(单场景 10+ 实现),差异化转向细分宿主(omp/CommandCode/OpenCode/Neovim/Emacs/GH Actions)与新概念(记忆失效层、置信度审计)。
- **2026-09-19(傍晚,第七次扫描:长尾场景专项)**:三个新矿脉(jevable.com 36 条、risetive.com/jev **98 条带作者的目录**、GitHub 按 star 宽搜),新增 40+ 项目,最有趣的新场景:
  - **法律**:LegalForecast-MTD——预测联邦法院驳回动议裁定(micro-Brier 评分)。
  - **真实硬件**:robo-harness(SO-101 机械臂)、MuJoCo 机械臂实时控制、MOSS 捡垃圾机器人。
  - **税务合规**:[tax-doc-classifier](https://github.com/kyotofin/tax-doc-classifier)(153★)——**261 份 IRS 表单 100% 严格准确**。
  - **生成侧新解法**:逐像素并行作画(@anshuc)、毫秒级生成式 UI(Chris Tate)、每条消息 ~10 个决策的 3D 虚拟表情(Joao Bortotti)。
  - **杂项惊喜**:日文地址消歧、屏幕共享隐私模糊(MrSecret)、HTTP 200 里的错误检测、曼哈顿寻路 vs Dijkstra/A*、学术引用核查、3000 份儿童零食 28 秒 $0.11、586 页 SEO 内链审计 45 秒 $0.21(同时间 Opus 仅 21 页);两个诚实失败案例(空战 AI"it kinda sucks"、草稿门 agent 卡死)。
  - **平台级采用**:**Vercel eve 把 Jev 设为默认 evaluation model**、LanceDB 官方 reranker、LiteLLM pass-through、Pydantic AI TypeSafe Model、Composio/Braintrust/Neon 集成——Jev 成为 eval 基础设施默认选项的趋势明确。
  - **高星新面孔**:[NanoJev](https://github.com/TianyuCodings/NanoJev) 451★(端到端训练管线)、[vexjoy-agent](https://github.com/notque/vexjoy-agent) 420★、[dabit3/jev-experiments](https://github.com/dabit3/jev-experiments) 254★、[quackd](https://github.com/rokbenko/quackd) 211★(多机器人编排)、kitze 双作(skillbox 163★/unclutter 107★)、jev-browser-use 131★(EZCollegeApp 生产)、jevpilot 77★、Tony Dinh 仓库确认为 [trungdq88/youtube-sponsor-detection](https://github.com/trungdq88/youtube-sponsor-detection)(已修正地址)。
  - **知名开发者继续入场**:sorrycc(贪吃蛇)、mizchi(MoonBit 五子棋)、jamesward(Scala ZIO)、hemanth(象棋)、featherless-ai(simple-jev)。
- **2026-09-19(晚,第八次扫描:X 热门场景+可信度)**:
  - **热门新场景**:GTM/销售——实测 Jev 即时构建 [Clay 工作流](https://www.linkedin.com/posts/outboundphd_so-jev-does-in-fact-work-for-building-clay-activity-7506771976632451072-co-4)(@outboundphd);1 秒组装 UI(@michaeltefula);[Medium 热文](https://ezzekielnjuguna.medium.com/jev-ai-explained-the-new-model-that-finished-a-3-minute-web-task-in-7-seconds-2fdb199e5588)盘点"3 分钟任务 7 秒完成"。
  - **病毒梗**:电车难题 demo 出处为 CEO @CompleteSkeptic 本人,经 Instagram 二次扩散。
  - **⚠️ 可信度警报**:[steve8708 打假](https://www.linkedin.com/posts/steve8708_jev-is-awesome-but-for-the-love-of-god-please-activity-7506883009443303424-IrBJ)——病毒 demo 中混有加速/伪造内容,已写入 §八 提醒读者以带 trace 的仓库为准。
  - @typesafeai 官方时间线暂无法经搜索引擎索引(需登录),后续监控经 Discord Show and Tell 或 X 关键词间接覆盖。
- **2026-09-19(夜,第九次扫描:三大目录全文 + HN 增量)**:
  - **规模修正**:[awesomejev.com](https://awesomejev.com/) 实为**收录 488 条、总星 21,644** 的最大目录(09-18 刷新)——本案例集此前仅采其局部;[typesafeai.app](https://typesafeai.app/) 30 条用例全部为"E2 工件验证"级;awesome-typesafe 当日终于更新 6 条(jgrep/Kotlin SDK/Go SDK/jev-orderby-bench/pi-jev-context/wakegate)。
  - **星数重要修正**:fast-jev-compaction 实为 **2,735★**(社区工具类第一,此前被低估);vercel/eve **5,253★**(全场最大的采用信号);jev-ultrafast 目录计数 4,799★。
  - **jev-review 有两个同名项目**:devagrawal09(247★)与 NiazMorshed2007(113★,即 @niazmorshed_ 的 MCP 版)。
  - **新场景**:AI 文风检测(snifftest)、Scale VP 的散文 linter(riff)、提交-CVE 关联(commit-miner)、npm 安全门(pkg-gate)、西班牙官报 BOE 筛查、**jev-tree 递归 Choice 突破 255 选项上限**。
  - **克隆+1**:Kev(HN,DiffusionGemma on Cloudflare Workers AI)。
  - **总规模**:全生态(含 SDK 长尾)已达 **~500 仓库/21,600+ 星**;发布第 4 天结束时的分层:官方(~10)→ 平台集成(eve/LanceDB/LiteLLM/Pydantic 等 ~15)→ 独立应用(~50)→ agent 工具(~90)→ SDK/长尾(~300)。
- **2026-09-19(深夜,第十次扫描:X 三轮场景关键词)**:
  - **交易硬数据**:[@BrendanPlayford 交易引擎](https://x.com/BrendanPlayford/status/2100614031845539975)——Jev+微调,**375 笔模拟交易、41.1% 胜率**(诚实的未-filtered 数据);[Kalshi 预测市场实测视频](https://www.youtube.com/watch?v=Od4j4osz4JY)(体育伤情/比特币事件市场)。
  - **新场景**:零样本机器人操作(@taratt,LinkedIn 视频)、Cloudflare Workers 语音 agent(@harshil1712/slidepilot)、Roulette Wars 整局自玩([@NicoSaraintaris](https://x.com/NicoSaraintaris/status/2100745151622664392))、**"Jev 当弱标注器"**(Jev 合成训练数据→训传统分类器,r/singularity 评论区浮出的两段式省钱架构)。
  - **背书升级**:Hasura 联创 Tanmai Gopal("准确率超 Sol、便宜 100 倍")、沃顿教授 @Afinetheorem("LLM 本来就不是干这个的对的模型")。
  - **韩文区**:以解读为主(kimmonismus 推文 + FB 视频),项目仍少。
  - **修正**:dabit3 预测表格补推文直链;harshil1712 即 slidepilot 作者(awesomejev 收录)。
- **2026-09-19 17:00**:新增 3 个 A 级项目:[llm-prompt-techniques-on-jev](https://github.com/leepokai/llm-prompt-techniques-on-jev)(CoT/self-refinement 移植到 Jev,四大基准)、[JevBall](https://github.com/atarikcaliskan/jevball)(22 个 Jev 踢 3D 足球)、[how-sure-is-jev](https://github.com/adarc8/how-sure-is-jev)(概率分布→一个数+判词);B 级补充:[sift](https://github.com/bohutang/sift)(X 帖五维打标)、[clean-code-review](https://github.com/frostney/clean-code-review)(Uncle Bob 规则)、[dinostomp](https://github.com/collapseindex/dinostomp)(评测工具的验证层);awesome 目录再+2([valentynkit](https://github.com/valentynkit/awesome-jev-typesafe) 14★、[SeeAPI](https://github.com/SeeAPI/awesome-jev-use-cases),全生态已 11 个);GitHub 总数 718→**781**;X 无新重大项目(以教程/视频为主)。
- **2026-09-19 20:00**:新增 6 个:[jevcache](https://github.com/kushals256/jevcache)(A,校准 same-intent 缓存代理,跳过重复 LLM 调用)、[jevassert](https://github.com/dtduc-git/jevassert)(A,Jev 问题包的 CI 回归测试:准确率/校准/成本)、[jev-bench](https://github.com/kamo-shika/jev-bench)(B,**日文公开数据独立基准**,Jev vs 开源模型直读概率)、[jev-mail-classifier](https://github.com/parth-kp/jev-mail-classifier)(B,5★,收件箱分类:打标/移动/标记/通知)、[JevPilot](https://github.com/InfamousCube/JevPilot)(B,德文:PC/浏览器/游戏/安卓统一 prompt 操控)、[gg-friggin-ez](https://github.com/ItisShikhar/gg-friggin-ez)(B,Node 脏话毒性秒筛)。awesome-typesafe 再收 7 条(JevDroid 安卓端、jev.nvim、jev-belay、jev-commit、jev-skip、pi-verdict、pokemon-red);GitHub 总数 781→**824**;X 无新项目(媒体讨论为主,新出现 Tildes 长帖)。
- **2026-09-19 23:00**:新增 7 个(A×3):[jev-semgrep](https://github.com/uehaj/jev-semgrep)(42★,按语义跨语言 grep,英文含义可搜出日文行)、[stanley-code](https://github.com/devagrawal09/stanley-code)(12★,自进化编码 agent:Jev 路由到确定性工作流,缺口自动生成新工作流)、[jev-palette](https://github.com/amycardoso/jev-palette)(一次 Choice 排 77 命令,$0.00004/击键);(B×4):[jev-ptbr-bench](https://github.com/amycardoso/jev-ptbr-bench)(**巴西葡语基准**,非英语独立基准第二个)、[jev-bonsai-2-27B](https://github.com/cyberumut/jev-bonsai-2-27B)(Apple Silicon 本地复刻再+1)、[jev-gmail-spam-filter](https://github.com/ilyamk/jev-gmail-ai-spam-filter-and-labeling)(Gmail 自托管分类)、[jev-storyboard-lab](https://github.com/jimmyliao/jev-storyboard-lab)(Google ADK vs Microsoft Agent Framework 对照)。生态:GitHub 824→**877**;awesome-typesafe +3(jev-social、JevBrowserExt、jev-agent-browser);[jevai.org](https://www.jevai.org/) 社区站正式上线(含 Playground);Theo Browne 等主播跟进报道。
- **2026-09-20 02:00**:新增 7 个(A×2):[jev-reliability](https://github.com/vcjdeboer/jev-reliability)(问题级可靠性四维测量:重复性/措辞/分辨率/可答性,swamp 扩展)、[jev-crawlers](https://github.com/russfranky/jev-crawlers)(递归找 bug 管道,$0.00008/节点);(B×5):[jevdevice](https://github.com/Xopher00/jevdevice)(MCP 操控真实安卓手机)、[JevPip](https://github.com/yo4e/JevPip)(日文 FX/BTC 本地交易终端:实盘图/纸面交易/回测/安全监督)、[jev-for-chrome](https://github.com/chy4pro/jev-for-chrome)(驱动当前标签页)、[Essentiel-Jev](https://github.com/JacquesGariepy/Essentiel-Jev)(邮件/日历/任务/文档套件)、[jev-kit](https://github.com/jonathanavis96/jev-kit)(Claude Code 全家桶:守门+分层保障)。另:jev-city(第三个城市交通模拟,带基准)、apa-agent-harness(置信度门控生产 harness)、awesome-typesafe 收录 QuantDinger 金融交易集成;GitHub 总量 877→**949**(+72,夜间加速);X:假 demo 打假话题出圈(Instagram 病毒视频),HN 首发帖确认 **1420 分**,Andrea Volpini(WordLift 创始人)入场做 demo。
- **2026-09-20 05:00**:新增 7 个(A×3):[hunch](https://github.com/carldaws/hunch)(Ruby 概率控制流:`Hunch.almost_certainly?`,阈值命名极优雅)、[jev-browser-qa](https://github.com/jonymusky/jev-browser-qa)(Playwright 开车拍片+Jev 裁判,<400ms)、[jev-classification-benchmark](https://github.com/rachit-srivastava-devx/jev-classification-benchmark)(20 臂基准探针:Jev $0.0000166/次;reasoning token 是成本大头,最小化后差 13×);(B×4):[rjif](https://github.com/doublerobust/rjif)(R 语言校准 if)、[mysql-ailike](https://github.com/maayanlevy/mysql-ailike)(MySQL NL 过滤,数据库第三员)、[pi-jev-sentinel](https://github.com/harshwasan/pi-jev-sentinel)(6★,Pi 三位一体检查:调用/输出/回复)、[jev_playground](https://github.com/JYeswak/jev_playground)("建之前先测")。生态:GitHub 949→**994**(破千在即);Dart SDK(jev_dart)出现;媒体层:r/LLMDevs 出现"我审了 287 个 Jev 项目选 20 个"元综述、hermes-ai.net 202 用例清单、Medium 信任度分析文。
- **2026-09-20 08:00**:🌐 **生态破千**(994→**1031**)。新增 7 个(A×3):[jevcheck](https://github.com/sathariels/jevcheck)("pytest for Jev"行为契约:钉模型版本+fixtures,答案翻转即升级失败;⚠️ 情报:官方模型列表已现 **jev-1.14 / jev-preview** 别名)、[whoa](https://github.com/PaulChen79/whoa)(编码 agent 止损器:数循环判漂移,脱敏规则极详)、[xtags](https://github.com/manifoldor/xtags)(中文 X 时间线意图标注,免责声明最完整);(B×4):[jev-town](https://github.com/CeciliaW888/jev-town)(3D 小镇 50 个 AI 市民并行反应你的广播)、[jev-builder](https://github.com/collapseindex/jev-builder)(Jev 请求可视化表单构建器)、[whatitdid](https://github.com/YukunHe304/whatitdid)(看 agent 每一步实际做了什么)、[jev-hft](https://github.com/cristiancolon/jev-hft)(Jev 判新闻做高频研究管线)。
- **2026-09-20 11:00**:新增 7 个(A×3):[bias-bench](https://github.com/natemoo-re/bias-bench)(首个偏见/公平性基准,按简历审计文献方法论重做并批驳病毒式旧测试)、[rspamd-jev](https://github.com/rioriost/rspamd-jev)(生产邮件服务器 Rspamd 影子评估插件,零分值不动投递)、[jevusher](https://github.com/cvsgireesh/jevusher)(上下文门童:J1-J7 七关卡,"便宜读一切,贵读幸存者");(B×4):[kojev](https://github.com/ItisNoMatter/kojev)(Kotlin Multiplatform,返回你自己的 enum/sealed 类型)、[jev-oas-sentinel](https://github.com/ShuhanSun/jev-oas-sentinel)(OpenAPI 兼容性检查)、[moongate](https://github.com/brickfrog/moongate)(语义 CI 门)、[jev-vs-open-decision-models](https://github.com/elcronos/jev-vs-open-decision-models)(Jev vs 开源非生成决策模型零样本对比)。生态:GitHub 1031→**1077**;**OpenRouter 官方 LinkedIn**:Ori Eval 中 Jev 比最快 LLM 快 5×且精度不降;另有 agentic 基准点评"最不饱和,但轮次越多结果越差"。
- **2026-09-20 14:00**:新增 7 个(A×3):[jev-moral-dilemmas](https://github.com/krsna-smnt/jev-moral-dilemmas)(可重复性黄金数据:决策 100% 确定但置信度漂移可达 14 点;翻转全部发生在置信度<17% 区间)、[moomoo-jev-trader](https://github.com/maxlibin/moomoo-jev-trader)(富途实盘+Jev 影子评估,每 5 秒点评,置信门控执行)、[jevdash](https://github.com/Sunwood-ai-labs/jevdash)(净室无版权 2D 平台跳跃基准,60FPS 确定性物理);(B×4):[slop-filter](https://github.com/adamnroman/slop-filter)(X+LinkedIn 双平台隐藏 AI 生成帖)、[grevi](https://github.com/tpellet/grevi)(语义 grep:万行日志找错误/按描述找提交)、[jev-cordhub](https://github.com/rmwahid/jev-cordhub)(自然语言问 Discord 频道里的 GitHub 收藏堆)、[laya-jev-lab](https://github.com/yibie/laya-jev-lab)(Jev vs 开源 Laya 独立对比)。生态:GitHub 1077→**1129**;X:Peter Wang 扩展演示、requesty 技术解析、"12 个真实用例诚实评测"等媒体内容持续。
- **2026-09-20 17:00**:新增 7 个(A×3):[jev-browser-chrome](https://github.com/kofanlabs/jev-browser-chrome)(驱动已登录真实 Chrome 标签页,本地扩展桥,解决登录/反爬)、[dsh-jev-guard](https://github.com/7starsseeker/dsh-jev-guard)(中文,DSH 强制执行阀,114 例校准中文 90.4%,四态 allow/revise/block/escalate)、[jev-sales-call](https://github.com/tsekino62/jev-sales-call)(日文,60 通销售电话 5 问:60/60、Brier 0.012、250ms 中位,含弱点探针);(B×4):[jev-architect](https://github.com/karanb192/jev-architect)(设计/评估 Jev 决策环路的元工具)、[jeffrey](https://github.com/thomasbrueggemann/jeffrey)(Jev/Laya 决策下一步的编码 CLI)、[diff-risk-sentinel](https://github.com/heliowap/diff-risk-sentinel)(大 diff 风险分诊 CRAP+Jev)、[n8n-nodes-jev-systemone](https://github.com/withabdul/n8n-nodes-jev-systemone)(第二个 n8n 节点)。生态:GitHub 1129→**1198**;awesome-typesafe +9(含 **Luce**:带与 Jev 对比数字的开源配方、poorjev);**jev-radar 自身 4→7★**(Key 发放开始生效)。
- **2026-09-20 20:00**:新增 7 个(A×3):[awesome-jev-zh](https://github.com/yzfly/awesome-jev-zh)(26★,中文枢纽:精选+指南+图解+每日自动收录,含"冷静看待"批判数据节)、[shipit-gate](https://github.com/thecoderpanda/shipit-gate)(发布门:~200ms 判"能不能 ship",阈值在代码)、[dynamic-context-engine](https://github.com/rohanarun/dynamic-context-engine)(SQLite 段落记忆,无嵌入无向量库,Jev 逐段判相关);(B×4):[jev-resume-match](https://github.com/hamidfarmani/jev-resume-match)(简历×JD 打分 Next.js)、[Dual-Spectrum-Phishing-Guardian](https://github.com/YuyaForest/Dual-Spectrum-Phishing-Guardian)(钓鱼/欺诈双谱卫士)、[jev-typesafe-real-financial-use-cases](https://github.com/IslamBaraka90/jev-typesafe-real-financial-use-cases)(50 个金融实战用例集)、[openclaw-tool-prefilter](https://github.com/MertBasar0/openclaw-tool-prefilter)(两段式技能/工具预筛)。生态:GitHub 1198→**1245**;awesome-typesafe +4(hush、PlayJev、Jev Trade)。
- **2026-09-20 23:00**:新增 7 个(A×3):[openJev-verdict-2.0](https://github.com/Heman10x-NGU/openJev-verdict-2.0)(148★,151M 非自回归引擎:自报 77.10% Top-1/ECE 1.44%/20-25ms/WebGPU 浏览器可跑,称胜 Jev 与 Laya——作者自评口径)、[laya-jev-compatible-server](https://github.com/exfly/laya-jev-compatible-server)(Laya 开源模型的官方 SDK 兼容层)、[jev-issue-radar](https://github.com/Patrick-SCH03/jev-issue-radar)(重复 issue 证据分诊,只读+诚实标注);(B×4):[Jev-Playing-Flappy-Birds](https://github.com/Vidit-Ostwal/Jev-Playing-Flipping-Birds)(Flappy Bird+WebSocket 观战)、[jev-outlook-organizer](https://github.com/Taveren7/jev-outlook-organizer)(自托管 Outlook 整理)、[jev-comment-analysis](https://github.com/juanlentino/jev-comment-analysis)(WordPress 评论审核)、[systemone-lite](https://github.com/fritzprix/systemone-lite)(玩具级本地 Jev 形 API)。生态:GitHub 1245→**1293**;开源决策模型三国杀格局成型(Jev 官方 / Laya / Verdict)。
- **2026-09-21 02:00**:新增 7 个(A×3):[work-with-jev](https://github.com/Adkid-Zephyr/work-with-jev)(中文,飞书/企微消息四分类+跨群待办,演示免 key)、[听写纸](https://github.com/limboinf/semantic-live-caption)(中文,流式 ASR+Jev 逐句实时标注,意图四道门:置信≥0.55+领先≥0.12+Noul 复核)、[lgtm](https://github.com/stardeckai/lgtm)(证明测试真的在测:16k 测试块/347 人工标注/阈值拟合);(B×4):[jev-adrank](https://github.com/leepokai/jev-adrank)(实时广告排序+创意审查,一次调用给广告定价)、[jev-android](https://github.com/dougsong/jev-android)(Kotlin 安卓 UI 自动化 SDK+a11y 运行时)、[jev-proxy](https://github.com/Santiago-j-s/jev-proxy)(本地可观测代理+playground)、[TheFishGame](https://github.com/muratcanberber/JEV-TheFishGame)(多人小鱼游戏,每个 AI 决策一次 Jev 调用)。生态:GitHub 1293→**1352**;awesome-typesafe +2(jev-fit、slop-grader)。
- **2026-09-21 05:00**:新增 7 个(A×3):[rocky](https://github.com/BenjisCollector/rocky)(语音控电脑:一次请求 13 问、a11y 树零截图、默认干跑)、[watfile](https://github.com/jexp/watfile)(jexp/Neo4j 出品的文件语义归档,可插本地后端)、[semantic-microscope](https://github.com/abhishekmishragithub/semantic-microscope)(逐句校准标注,3000 句≈$0.08/3.5 分钟,泳道视图);(B×4):[survey-qc-with-jev](https://github.com/stephotee/survey-qc-with-jev)(问卷受访者质检:规则+语义)、[aithyrion-director](https://github.com/psychodissection-ship-it/aithyrion-director)(AI 音乐视频导演,节拍同步)、[jev-atlas](https://github.com/ZeroX-01/jev-atlas)(**第 12 个**目录/索引站)、[before-the-fall-jev](https://github.com/muhammadaq1/before-the-fall-jev)(电影感 2D 救援游戏)。生态:GitHub 1352→**1393**。
- **2026-09-21 08:00**:🎉 **注册表破 200**(197→**204**)。新增 7 个(A×3):[jev-ui](https://github.com/etweisberg/jev-ui)(概率 UI React 组件:选子树/排列表/条件浮现,record/replay 测试——语义前端首例)、[jev-board-game](https://github.com/KeWang0622/jev-board-game)(信念作为原语:谁是卧底/狼人杀/阿瓦隆,每个玩家独立 Jev agent,怀疑度=校准分布+上帝视角看台)、[MacWork](https://github.com/gklab/MacWork)(住进 Mac 的原生接口 worker,签名 Swift 权限助手+MCP);(B×4):[jev-tree-memory](https://github.com/Pizzawookiee/jev-tree-memory)(n 叉记忆树+Jev 路由检索)、[jevtriage](https://github.com/sathariels/jevtriage)(PR 三态分诊 GH Action)、[DriftLab](https://github.com/asmirrr/DriftLab)(动量策略量化研究 CLI)、[python-jev-if](https://github.com/YosAwed/python-jev-if)(Python 语义 if)。生态:GitHub 1393→**1433**。
- **2026-09-21 11:00**:新增 7 个(A×3):[jev-uipath-coded-agent](https://github.com/1aifanatic/jev-uipath-coded-agent)(**UiPath 编码 agent 做 AML 反洗钱分诊**,企业 RPA 首例:LLM 读写算、Jev 全决策)、[JevChat](https://github.com/fruitymcdoo/JevChat)(每个词=17000 词字典上一次类型化决策+Jev 裁判把关)、[twitter-jev-guard](https://github.com/qs-lll/twitter-jev-guard)(中文,STOP 水印而非隐藏);(B×4):[jev-debtgate](https://github.com/smlayero/jev-debtgate)(技术债门)、[jevseo](https://github.com/epergaboni/jevseo)(类型化 SEO/AEO/GEO)、[jev-subagent-router](https://github.com/DefensiveSniper/jev-subagent-router)(选子代理模型+推理力度)、[jev-laya-free](https://github.com/Sharkelot/jev-laya-free)(规则/Laya 兜底的免费本地兼容层)。生态:GitHub 1433→**1488**。
- **2026-09-21 14:00**:新增 7 个(A×2):[rag-jev](https://github.com/Nixz0824/rag-jev)(中文,LOL 公告 RAG:数字不经生成模型、78 题独立盲测+18 陷阱题、负面结论全公开——中文项目方法论新标杆)、[ockev](https://github.com/fancyboi999/ockev)(35ms 本地判别引擎,专治 agent 否认式废话"番茄炒蛋问题",TomatoEggBench-120 95.8%);(B×5):[squint](https://github.com/valsecchi75/squint)(Claude 只读大文件里回答问题的那部分)、[exact-paste](https://github.com/goodnight000/exact-paste)(表单要什么就粘什么)、[approval-judge-bridge](https://github.com/oppih/approval-judge-bridge)(OpenAI 兼容的审批裁判端点)、[Jcua](https://github.com/1deat0r/Jcua)(跨平台自进化 computer-use)、[jev-mcp-spring](https://github.com/Ashfaqbs/jev-mcp-spring)(Java/Spring MCP server)。生态:GitHub 1488→**1528**;awesome-typesafe +2。
- **2026-09-21 20:00**:新增 7 个(A×2):[jev-prompt-optimization](https://github.com/j341nono/jev-prompt-optimization)(进化式自动优化 Choice 指令与判据,GPT 当变异算子/Brier 当适应度——补齐"测量→优化→回归"工具链)、[jev-labeler-action](https://github.com/yamadashy/jev-labeler-action)(知名 OSS 作者 yamadashy,零配置 issue 打标,"恶意 issue 最多骗到错误标签");(B×5):[jevcraft](https://github.com/Ege-BULUT/jevcraft)(Jev 全天候玩 VoxeLibre 带录像)、[jev-no-en](https://github.com/patryckalves/jev-no-en)(巴西 ENEM 高考基准,非英语评测再+1)、[arxiv-for-chat-users](https://github.com/SalomonOli/arxiv-for-chat-users)(Jev 筛"对普通人真有用的 arXiv 论文")、[jev-screen-mcp/jev-review-mcp](https://github.com/jiawei686/jev-screen-mcp)(单用途 MCP 门:内容审核/代码评审,"one tool one job")、[jev-stock-decision-maker](https://github.com/0xZee/jev-stock-decision-maker)(实时行情→结构化决策)。生态:GitHub 1528→**1647**;awesome-typesafe 仓库疑似迁移(API 301)。
- **2026-09-21 23:00**:🔥 深度排查轮(非例行)。生态总量 1,708 仓库;发现多个高星未收录项目:[QuantDinger](https://github.com/OpenByteInc/QuantDinger)(11,904★,AI 交易 OS+Jev,全生态第二)、[kev](https://github.com/jaredpalmer/kev)(1,879★,Qwen3.5 可训复刻)、[reticle](https://github.com/reticlehq/reticle)(796★)、[hippo-memory](https://github.com/kitfunso/hippo-memory)(750★,生物启发记忆)、[distill](https://github.com/samuelfaj/distill)(682★)、[tiptour-macos](https://github.com/milind-soni/tiptour-macos)(630★)、[agent-beacon](https://github.com/Asymptote-Labs/agent-beacon)(606★)、[phi](https://github.com/pulseaiclub/phi)(481★)、[von](https://github.com/wfzyx/von)(320★,<15ms 本地直替)。**关键信号**:①量化交易类总量可能已超守门类;②记忆系统从压缩分叉成独立赛道;③复刻五国杀合计近 8,000★;④Spring AI 官方发文集成;⑤Cloudflare rita kozlov 公开喊话想接入;⑥**TypeSafe API 首次公开出现稳定性问题**(@dotpem:"we are working to restore");⑦"jevops"作为术语开始在 X 上流通。
- **2026-09-21 23:01(例行)**:新增 7 个(A×2):[jev-computer](https://github.com/RiwRiwara/jev-computer)(用 Jev 的 NAND 真值表搭出 8 位 CPU+RAM,2,102 门;7×6=42 花 $0.000019)、[jev-video-search](https://github.com/Anmol-Srv/jev-video-search)(嵌入检索+Jev 判真假;Jev 能拒答、能理解关系,嵌入不能);(B×5):[jev-edge](https://github.com/kiwi0719/jev-edge)(边缘网关三层提示注入防护)、[jev-oasis](https://github.com/badgerbees/jev-oasis)(超低成本社会模拟引擎)、[ticket-triage](https://github.com/jackkfan0305/ticket-triage)(工单分诊)、[Jev.Sdk](https://github.com/nothingmn/Jev.Sdk)(又一个 .NET 客户端)、[jev-arm-lab](https://github.com/Vankleben/jev-arm-lab)(模拟机械臂任务决策)。生态:GitHub 1,708→**1,713**。
- **2026-09-22 02:00**:新增 7 个(A×2):[tabjev](https://github.com/rishhavv/tabjev)(每个新标签页自动分组 ~150ms/$0.00001/次,"一月开一千个标签约一分钱";热/冷延迟在设置页可见)、[jev-factorio-agent](https://github.com/RiwRiwara/jev-computer)(Factorio 游戏代理:Jev 选 what 代码管 how,mock 后端可离线跑);(B×5):[jev-superpowers](https://github.com/AkashPriyadarshii/jev-superpowers)(13★,系统化 AI 编码框架+Jev)、[jev-curate](https://github.com/AkashPriyadarshii/jev-curate)(13★,高通量数据集筛选)、[shunt-jev](https://github.com/moelahmady/shunt-jev)(按需拦截全文件 Read)、[Footwork](https://github.com/Tom-R-Main/Footwork)(双过程浏览器代理)、[jev-foundation-models](https://github.com/peterfriese/jev-foundation-models)(Swift 6 原生桥)。另:awesome-typesafe 一口气 +15 提交(社区提交指南+分类页+视觉画廊+原生分享);awesome-jev-live(11★)第 **13 个**目录站出现。生态:GitHub 1,713→**1,772**。
- **2026-09-22 05:00**:新增 7 个(A×3):[blockly-jev](https://github.com/eriestra/blockly-jev)(Blockly 积木块嵌 Jev:Noul→Boolean/Choice→String,可视化编程里的"语义 if")、[jev-chrome-extension](https://github.com/gavansmyth-arch/jev-chrome-extension)(Chrome 侧栏:输入目标自动操作当前页,或选中文本问 Jev)、[jev-prior-auth-triage](https://github.com/vishalbitit/jev-prior-auth-triage)(医保预授权分诊 POC:Jev 判"该去哪个通道"而非"批不批",免责声明完整);(B×4):[feedlens](https://github.com/Klikwork/feedlens)(LinkedIn 信息流标签+广告变暗)、[anti-dead-internet](https://github.com/koz/anti-dead-internet)(X 时间线 AI 生成帖分类+移除)、[moviejev](https://github.com/SebasPinto/moviejev)(电影推荐,Jev 做校准重排)、[jev-harness](https://github.com/linksawakening/jev-harness)(自托管项目 harness)。生态:GitHub 1,772→**1,825**;awesome-typesafe +10 提交(视觉画廊+分类页+移动端优化);发布第 7 天。
- **2026-09-22 08:00**:新增 7 个(A×2):[jev-crash-course](https://github.com/nadyth/jev-crash-course)(11 关通关教程,~65 分钟,可运行示例+pytest)、[remember-me](https://github.com/leonininder/remember-me)(agent 记忆门控:本地召回→脱敏→Jev include/stub/skip,"Jev 从不排序只做准入");(B×5):[jevgram](https://github.com/sksq96/jevgram)("Jev 能做 Pangram 做的吗?"7,139 条文本 AI 检测评测)、[deslop](https://github.com/yoichiojima-2/deslop)(网页广告/slop/SEO 评分)、[judgevet](https://github.com/Alberto-Codes/judgevet)(类型化客户端+CLI+MCP)、[sabr-jev](https://github.com/harlanljones/sabr-jev)(棒球赛季评分)、[readwise-jev-classifier](https://github.com/osrim/readwise-jev-classifier)(Readwise 文章自动打标)。生态:GitHub 1,825→**1,859**;awesome-typesafe +10(含收录 Jevals 独立基准和 Beacon/Distill)。
- **2026-09-22 11:00**:新增 7 个(A×3):[meaning-assert](https://github.com/JohnRSandoval/meaning-assert)(语义断言:换措辞过/改事实挂/证据不足 inconclusive,附在线回放)、[jev-qq-assist](https://github.com/1104480426-hash/jev-qq-assist)(中文,手机QQ聊天参谋:只给判决不替你打字,APK直接装,本地ONNX或远程Jev)、[typesafe-jev-tools](https://github.com/wotai-dev/typesafe-jev-tools)(Claude Code钩子:写LLM调用时自动注入"这个决策需要模型吗"三问测试);(B×4):[athena-jev](https://github.com/MartinesEmanuel/athena-jev)(认知控制层)、[commander-oracle](https://github.com/kitapplegate/commander-oracle)(万智牌新卡买卖建议)、[dgui-hypermem](https://github.com/ctaxnagomi/dgui-hypermem)(自托管混合记忆MCP)、[tri-emails-jev](https://github.com/ColinDargent/tri-emails-jev)(法文,4套邮件分诊模板)。生态:GitHub 1,859→**1,897**。
