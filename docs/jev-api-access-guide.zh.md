> 本攻略是 [jev-radar](https://github.com/everyinfra/jev-radar) 仓库的一部分:全网最全的 Jev 生态独立白皮书与实时监控。结构化项目数据见 [data/projects.json](../data/projects.json)。

# Jev API 完整申请攻略

> 更新时间:2026-09-18 · 信息来源:TypeSafe 官网/官方文档/官方博客 + Reddit 真实用户交叉确认

Jev 是 TypeSafe AI(创始人 Diogo Almeida,InstructGPT 共同作者)2026-09-15 发布的首个 "System One 模型":不生成文本,输入非结构化状态 + 一组带类型的问题,返回结构化决策(Choice 选择 / Score 打分 / Noul 是非概率),主打 40–200 倍速度、极低成本、数学上不会幻觉。

---

## 路线 A:官方通道(waitlist 制,拿正式 key)

### 第 1 步:加入等待名单

打开 [console.typesafe.ai](https://console.typesafe.ai),两种登录方式任选:

- **Continue with Google**
- 输入邮箱后点 **"Email me a code instead"** 收验证码登录

登录即自动进入 waitlist。

> ⚠️ 注意:官网首页的 "Join Waitlist" 按钮目前有 bug,实际链接指向他们的招聘页(jobs.ashbyhq.com),**别从那个按钮进,直接走 console 登录**。

### 第 2 步:收到确认邮件

加入后会收到一封确认你已在等待名单的邮件。有用户反映没收到这封——不影响,以实际权限为准。

### 第 3 步:等待批准

时长不定:发布公告当天加入的人几小时就通过了,现在普遍 **24 小时以上**,Reddit 上还有人排队中。官方说法是"尽快把开发者从 waitlist 里放出来"。

> 💡 **重要**:有用户批准了但**没收到任何通知邮件**——所以隔天记得重新登录 console 看看有没有权限,别干等邮件。

### 第 4 步:生成 API Key

批准后进入 [console.typesafe.ai/settings/keys](https://console.typesafe.ai/settings/keys) 创建 key(`jev_` 开头)。

### 第 5 步:调用

端点和认证(官方 API 文档确认):

```bash
curl -X POST https://api.typesafe.ai/v1/systemone \
  -H "Authorization: Bearer $TYPESAFE_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "state": "Help! My payouts have been failing for 3 days.",
    "model": "jev-latest",
    "questions": {
      "is_urgent": { "type": "noul", "instructions": "Does this convey urgency?" },
      "department": {
        "type": "choice",
        "instructions": "Which team should handle this?",
        "criteria": { "billing": "Payments, invoicing, refunds", "technical": "Bugs, outages, integrations" }
      }
    }
  }'
```

Python 官方 SDK(官方 quickstart 原样):

```python
# pip install typesafe-sdk  (需 Python ≥3.10,key 放环境变量 TYPESAFE_API_KEY)
from typesafe_sdk import Choice, Noul, Score, TypeSafeClient

client = TypeSafeClient()
response = client.system_one(
    state="Hi, I've been trying to connect my Stripe account for 3 days...",
    questions={
        "department": Choice(instructions="Which team should handle this",
                             criteria={"billing": "Payment or subscription issues",
                                       "technical": "Bugs or integration problems"}),
        "is_urgent": Noul(instructions="The message conveys urgency"),
    },
)
print(response.answers["department"].choice)
```

三种问题类型:

| 类型 | 作用 | 返回 |
|---|---|---|
| `noul` | 是非判断 | 0–1 概率 |
| `choice` | 从你定义的选项里选一个 | 选中项 + 全选项概率分布 + confidence |
| `score` | 按你给的等级量规打分 | 概率加权分值(可落在两档之间)+ legend |

**计费**:输入 $0.042/百万 token,输出免费,延迟 70–500ms。

### 加急技巧

官方博客明确说想听开发者"要自动化什么决策"——发邮件到 **hello@typesafe.ai**,写清你的用例和规模,社区反馈这有助于提前放行。这就是"要发邮件申请"传闻的来源。

---

## 路线 B:不想排队,今天就能用

| 通道 | 怎么用 |
|---|---|
| **[OpenRouter](https://openrouter.ai/typesafe/jev-1.13)** | 最省事。模型名 `typesafe/jev-1.13`,用现有的 OpenRouter key 直接调,价格同官方($0.042/M 输入)。Reddit 已有人等不及全程用这个 |
| **[Netlify AI Gateway](https://www.netlify.com/changelog/typesafe-jev-ai-gateway/)** | 装 `@typesafe-ai/sdk`,零配置走 Netlify 网关 |
| **[OpenJev](https://www.reddit.com/r/LocalLLaMA/comments/1wjlyzr/still_on_the_jev_waitlist_i_hosted_openjev_its/)** | 社区架的免费开源兼容版,官方 SDK 改个 base URL 就能用,适合先开发再换正式 key |

**完全不想注册**:[console.typesafe.ai/playground](https://console.typesafe.ai/playground) 或社区站 [jevai.org/playground](https://jevai.org/playground) 免 key 试玩。

---

## 建议

双线并行——现在就登录 console 排队 + 发一封用例说明邮件到 hello@typesafe.ai,同时用 OpenRouter 的 key 先把代码跑通,等正式 key 下来只改一行环境变量。

---

- 
