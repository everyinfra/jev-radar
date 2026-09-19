---
name: jev-radar-briefing
description: 拉取 everyinfra/jev-radar 仓库的最新更新并生成 Jev 生态每日简报。当用户说"Jev 简报"、"拉取 Jev Radar 更新"、"今天有什么新 Jev 项目"、"扫一下 Jev 生态"时使用。
---

# Jev Radar · 接入指南 + 每日简报 Skill(单文件版)

> **一个文件 = 人类指南 + 可安装的 agent skill。**
> 下载这一个文件,你就接入了全网最全的 Jev(TypeSafe AI System One)生态监控:
> 220+ 实证案例、108 条置信度分级数据、每 3 小时自动扫描更新。

**仓库主址**:[github.com/everyinfra/jev-radar](https://github.com/everyinfra/jev-radar)

---

## 一、给人的说明:这个仓库能给你什么

| 你想要 | 去哪里 |
|---|---|
| 看全部案例(中文,14 章节 + 扫描日志) | 仓库根目录 `CASEBOOK.md` |
| 机器可读的项目注册表(108 条,含置信度分级) | `data/projects.json` |
| Jev API 申请攻略(waitlist/加急技巧/免排队通道) | `docs/jev-api-access-guide.zh.md` |
| 置信度规则(A=0.90 工件直检 / B=0.75 一手源 / C=0.60 目录收录) | `README.md` 的 Verification 一节 |

不需要 API key 就能读以上所有内容。要真正调用 Jev,按攻略申请(输入 $0.042/M token,输出免费)。

---

## 二、怎么做到"每天定点拉取更新 + 生成简报"

### 方式 A:把本文件装成 agent skill(推荐)

任何支持 SKILL.md 约定的 agent(Claude Code、Codex、其他兼容 agent)都适用:

```bash
# Claude Code:
mkdir -p ~/.claude/skills/jev-radar-briefing
# 把本文件保存为:
#   ~/.claude/skills/jev-radar-briefing/SKILL.md
```

装好后对 agent 说一句:

> "每天早上 9 点拉取 jev-radar 更新,给我一份简报。"

支持定时任务的 agent 会自动建好调度;不支持的,你每天手动说"Jev 简报"即可。

### 方式 B:系统定时 + 手动触发

把这句加进 `crontab -e`(每天 09:00 提醒 agent 干活):

```
0 9 * * *  echo "运行 jev-radar-briefing skill:拉取 everyinfra/jev-radar 更新并生成今日简报"
```

### 方式 C:不开 agent,纯脚本(见第五节附录)

---

## 三、给 Agent 的指令(skill 本体,装好后自动生效)

当用户要求 Jev 简报 / 拉取 Jev Radar 更新时,按以下流程执行:

### 第 1 步:同步仓库(二选一)

**已 clone**(推荐,可增量):
```bash
cd <本地jev-radar克隆目录>
git fetch origin main
git log --oneline HEAD..origin/main     # 看 commit 摘要
git diff HEAD..origin/main -- data/projects.json | head -200
git merge --ff-only origin/main
```

**未 clone**(免 git,走 API):
```bash
# 最近 24h 的提交
curl -s "https://api.github.com/repos/everyinfra/jev-radar/commits?since=$(date -u -v-1d +%Y-%m-%dT%H:%M:%SZ 2>/dev/null || date -u -d '1 day ago' +%Y-%m-%dT%H:%M:%SZ)Z" | python3 -c "import json,sys;[print(c['commit']['committer']['date'][:16], c['commit']['message'].split(chr(10))[0][:90]) for c in json.load(sys.stdin)]"
```

### 第 2 步:提取增量

- 新项目:对比 `data/projects.json` 的 `projects` 数组(以 `name` 为键),新出现的条目就是今日新增;注意读每条的 `verification.tier / confidence / stars / metrics`。
- 动态:CASEBOOK.md 末尾"十三、监控日志"的最新小节。
- 若仓库无新 commit,简报写明"过去 24h 无新增"即可,不要编造。

### 第 3 步:生成简报(固定模板)

保存为 `briefings/YYYY-MM-DD.md` 并在对话中输出:

```markdown
# Jev 生态日报 · YYYY-MM-DD

## 今日新增(N 个)
| 项目 | 作者 | 一句话 | 置信度 | 地址 |
|---|---|---|---|---|
(来自 projects.json 新条目;A/B/C 分级照抄)

## 值得注意
(星数异动、新场景类别、平台采用、翻车/打假记录,各 1-2 条,注明出处链接)

## 一句话总结
(今日生态一句话)

数据源:github.com/everyinfra/jev-radar(每 3 小时自动扫描)
```

### 第 4 步:调度(若宿主支持)

- 若运行环境有定时任务能力(如 cron 类工具),建议以"每日 09:00"触发本 skill;**用户明确说过时间就以用户为准**。
- 无定时能力时,提示用户每天手动说"Jev 简报"。

### 红线

- 只报告仓库里实际存在的内容,链接一律取自 `projects.json` 的 `url` / `tweet` 字段,**不要自己编 URL**;
- 排除同名干扰:Journal of Extracellular Vesicles(期刊)、JEV 股票;
- OpenJev / SemIf 等克隆项目需注明"非官方"。

---

## 四、简报示例(第一天接入时会得到这样一份)

> **Jev 生态日报 · 2026-09-19**
> 今日新增 5 个:xxx(router,A 级)…;值得注意:jev-ultrafast 星数破 6k;Vercel eve 将 Jev 设为默认 eval 模型;X 上出现加速假 demo,已标记。数据源:everyinfra/jev-radar。

---

## 五、附录:无 agent 的纯脚本(保存为 `pull-and-brief.sh`,配合 cron 每天 09:00 跑)

```bash
#!/usr/bin/env bash
# Jev Radar 每日简报(纯脚本版):依赖 git + curl + python3
set -euo pipefail
DIR="${1:-$HOME/jev-radar}"
OUT="$DIR/briefings/$(date +%F).md"
FIRST=0

if [ ! -d "$DIR/.git" ]; then
  FIRST=1
  git clone -q https://github.com/everyinfra/jev-radar.git "$DIR"
fi
mkdir -p "$DIR/briefings"
cd "$DIR" && git fetch -q origin main

BEFORE=$(git rev-parse HEAD)
git merge -q --ff-only origin/main
AFTER=$(git rev-parse HEAD)

{
  echo "# Jev 生态日报 · $(date +%F)"
  echo
  if [ "$BEFORE" = "$AFTER" ] && [ "$FIRST" = "1" ]; then
    echo "首次接入成功:基线已建立,从明天起开始报告每日增量。"
  elif [ "$BEFORE" = "$AFTER" ]; then
    echo "过去 24h 无新增(仓库每 3 小时自动扫描,无变化即静默)。"
  else
    echo "## 新提交"; git log --oneline "$BEFORE".."$AFTER"
    echo; echo "## 新增项目"
    git diff "$BEFORE".."$AFTER" -- data/projects.json | grep -E '^\+\s+\{"name"' || echo "(见提交差异)"
  fi
  echo; echo "数据源: github.com/everyinfra/jev-radar"
} > "$OUT"
echo "简报已生成: $OUT"
```

cron:`0 9 * * * /bin/bash /path/to/pull-and-brief.sh`

---

## 六、出处与许可

- 数据与内容来自 [everyinfra/jev-radar](https://github.com/everyinfra/jev-radar),内容 CC BY 4.0、数据 CC0,独立社区研究,与 TypeSafe AI 无关联。
- 本 skill 文件本身可自由分发,请保留仓库链接。
- 维护方:[EveryInfra](https://everyinfra.com) · [文档](https://everyinfra.com/docs)。
