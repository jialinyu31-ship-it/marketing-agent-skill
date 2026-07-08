# Marketing Agent Skill

一个面向中文营销实战的 Codex skill，用于把行业资料、产品信息、创始人经历、用户洞察和零散营销笔记，转化为可执行的营销策略、短视频选题、口播脚本、私域运营 SOP 和内容质检标准。

> This repository contains a Codex skill for Chinese marketing strategy, content planning, short-video scripting, private-domain operations, and marketing content review.

## What It Does

`marketing-agent-skill` 不是单个提示词，而是一套可复用的营销 Agent 工作流。它把营销任务拆成几个稳定模块，按需加载对应参考文件，让 Codex 在处理营销问题时更像一个有方法论的策划、编导、运营和终审。

适合用于：

- 个人 IP 定位、创始人故事提炼、专家人设设计
- 行业分析、竞品分析、用户痛点和情绪洞察
- 抖音/小红书/视频号等短视频选题策划
- 情绪化观点选题、反常识选题、热点切入
- 口播脚本、黄金三秒、分镜头脚本、评论区引导
- 私域承接、线索筛选、转化 SOP、复盘指标
- 信息流广告策略、创意角度、落地页链路
- 去 AI 味改写、原创度检查、合规和版权风险审查

## Quick Start

### Install To Codex

macOS / Linux:

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/jialinyu31-ship-it/marketing-agent-skill.git ~/.codex/skills/marketing-agent-skill
```

Windows PowerShell:

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills"
git clone https://github.com/jialinyu31-ship-it/marketing-agent-skill.git "$env:USERPROFILE\.codex\skills\marketing-agent-skill"
```

安装后重新打开或刷新 Codex。你可以直接点名使用：

```text
Use $marketing-agent-skill to create a short-video marketing plan for my niche.
```

也可以用自然语言触发，例如：

```text
帮我为高端家政服务设计 30 天短视频选题、口播脚本和私域承接 SOP。
```

## Example Prompts

### 1. 行业分析与定位

```text
用 $marketing-agent-skill 分析我这个赛道：
行业：宠物营养品
产品：中高端猫犬肠胃调理补充剂
目标人群：一二线城市年轻宠物主人
目标：做小红书和抖音内容获客
请输出行业洞察、用户情绪、竞品差异化、内容支柱和转化路径。
```

### 2. 个人 IP 设计

```text
用 $marketing-agent-skill 帮我做个人 IP 定位。
我是一名做财税合规的创业者，服务中小企业老板。
请从人物底色、专业标签、反差标签、内容支柱、可讲故事和商业承接方式来设计。
```

### 3. 短视频选题和脚本

```text
用 $marketing-agent-skill 为装修建材行业生成 20 条短视频选题。
每条都要包含目标人群、情绪触发、冲突点、前三秒钩子、正文推进、信任证据和评论引导。
```

### 4. 内容终审

```text
用 $marketing-agent-skill 审查下面这条口播脚本：
[粘贴脚本]
请检查去 AI 味、原创度、合规风险、商业转化和发布前需要补充的证据，并给出改写版。
```

## Skill Structure

```text
marketing-agent-skill/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── research-and-ip.md
    ├── topic-and-script.md
    ├── private-domain-and-ops.md
    ├── quality-and-style.md
    ├── industry-playbooks.md
    ├── industries/
    │   ├── index.md
    │   ├── insurance.md
    │   ├── tax-accounting.md
    │   ├── renovation-materials.md
    │   └── ...
    └── source-map.md
```

### Core Files

| File | Purpose |
| --- | --- |
| `SKILL.md` | Codex skill 入口，定义触发条件、工作流和输出标准 |
| `agents/openai.yaml` | Codex UI 展示元数据 |
| `references/research-and-ip.md` | 行业洞察、竞品分析、个人 IP 和商业 IP 工作流 |
| `references/topic-and-script.md` | 选题、钩子、口播脚本、热点切入和分镜脚本 |
| `references/private-domain-and-ops.md` | 评论区运营、私域承接、信息流和转化 SOP |
| `references/quality-and-style.md` | 去 AI 味、原创度、风格提取、合规和终审 |
| `references/industry-playbooks.md` | 多个垂类的情绪张力、信任障碍和内容角度 |
| `references/industries/index.md` | 按 C 列 Agent 拆出的 46 个行业/人群模块索引 |
| `references/industries/*.md` | 单行业 playbook，包含人群、情绪张力、选题簇、脚本框架、私域和合规 |
| `references/source-map.md` | 来源范围、整理原则和版权边界说明 |

## Industry Modules

The skill now includes 46 C-column industry/group playbooks. When a user names a vertical, Codex should load `references/industries/index.md` and then the matching file.

Examples:

| Vertical | File |
| --- | --- |
| 保险 | `references/industries/insurance.md` |
| 财税 | `references/industries/tax-accounting.md` |
| 餐饮 | `references/industries/catering.md` |
| 房产 | `references/industries/real-estate.md` |
| 装修建材 | `references/industries/renovation-materials.md` |
| 宠物 | `references/industries/pets.md` |
| 医疗 | `references/industries/medical.md` |
| 债务优化 | `references/industries/debt-optimization.md` |
| 财富管理 | `references/industries/wealth-management.md` |
| 高净值人群 | `references/industries/high-net-worth.md` |

## Output Standards

这个 skill 倾向于输出能直接执行的交付物，而不是泛泛的建议。

### 选题策划

每条选题通常包含：

| Field | Meaning |
| --- | --- |
| 选题 | 可发布的内容主题 |
| 目标人群 | 谁会关心这条内容 |
| 情绪触发 | 焦虑、愤怒、后悔、好奇、身份认同等 |
| 反常识/冲突 | 为什么值得点开 |
| 开头钩子 | 前 3 秒口播或标题 |
| 正文推进 | 内容展开逻辑 |
| 证据/案例 | 支撑观点的案例、流程、对比或经验 |
| CTA | 评论、私信、保存、咨询或转化动作 |
| 风险备注 | 合规、夸大、误导或平台风险 |

### 脚本创作

脚本通常包含：

- 标题
- 黄金三秒
- 镜头/画面建议
- 口播正文
- 转折和冲突
- 信任证据
- 评论区引导
- 备选标题

### IP 定位

IP 输出通常包含：

- 人物底色
- 专业标签
- 反差标签
- 内容支柱
- 可讲故事
- 禁区
- 商业承接方式

### 私域和投放

运营方案通常包含：

- 流量入口
- 筛选问题
- 评论区和私信承接
- 私域标签体系
- 转化动作
- 复盘指标
- 合规风险

## Design Principles

- **先诊断，再创作**：先明确用户、场景、痛点、信任障碍和成交链路，再写选题或脚本。
- **情绪和事实并重**：内容要有情绪张力，但不能脱离真实产品、服务和证据。
- **从内容走向成交**：每个内容建议都要能连接评论、私信、私域、咨询或购买。
- **垂类优先**：同一个营销框架必须根据行业、平台、用户成熟度和合规要求改写。
- **质检前置**：在发布前检查原创度、去 AI 味、夸大承诺、敏感行业风险和版权边界。

## Safety And Rights

这个仓库只包含整理后的营销工作流、方法结构和原创说明文本，不包含原始附件、完整来源提示词或导出的私有数据。

使用时请注意：

- 不复制第三方原始提示词、脚本或案例全文
- 不对金融、医疗、法律、教育、保险、债务等敏感领域做保证性承诺
- 不编造客户案例、平台数据、行业报告或资质
- 不利用用户的脆弱处境做过度恐吓式营销
- 对需要专业资质的建议保留边界和合规提醒

## Validation

本 skill 已通过 Codex skill 校验：

```text
Skill is valid!
```

## Repository

GitHub:

```text
https://github.com/jialinyu31-ship-it/marketing-agent-skill
```
