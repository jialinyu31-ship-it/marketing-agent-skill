---
name: marketing-agent-skill
description: "Use this skill for Chinese marketing strategy and AI-agent workflows: personal IP positioning, industry research, emotional POV topic planning, short-video scripts, content style review, comment/private-domain conversion, information-flow campaign planning, and vertical-specific marketing playbooks. Trigger when the user asks to turn marketing materials, prompts, notes, niches, products, C-column Agent names, industry categories, or audience insights into executable marketing playbooks or content prompts."
---

# Marketing Agent Skill

## Source And Rights

This skill is a synthesized working method distilled from the local Feishu Base export and its attachments. The source attachments include copyright and non-commercial notices from the original rights holder. Do not reproduce the original attachment text, full prompts, or proprietary examples verbatim. Use this skill to generate new strategy, prompts, checklists, and content based on the user's current business context.

## Workflow

1. Identify the user's task type and load only the matching reference files:
   - Industry, audience, competitor, IP biography, IP concept, or commercial IP positioning: `references/research-and-ip.md`.
   - Emotional POV topics, short-video hooks, scripts, story fragments, hot-topic entry, shot plans, or content formats: `references/topic-and-script.md`.
   - Comment operation, private-domain conversion, lead nurturing, information-flow ads, or funnel design: `references/private-domain-and-ops.md`.
   - Anti-AI rewriting, style extraction, originality review, risk review, or final content audit: `references/quality-and-style.md`.
   - Vertical-specific topic angles and trust barriers: `references/industry-playbooks.md`.
   - C-column industry/group Agent modules such as insurance, tax, catering, real estate, pets, medical, debt, or high-net-worth: first load `references/industry-module-framework.md`, then `references/industries/index.md`, then the matching `references/industries/*.md` file.
   - Source coverage, licensing notes, and extraction scope: `references/source-map.md`.
2. If product, audience, platform, offer, region, conversion goal, or brand tone is missing, state concise assumptions and proceed. Ask only when the missing detail can change the core strategy.
3. Build the answer in this order:
   - `输入复述`: product/niche, audience, goal, platform, constraints.
   - `诊断`: user pain, trust barrier, emotional tension, content gap, conversion bottleneck.
   - `策略`: positioning, angle clusters, channel role, offer or CTA logic.
   - `执行件`: topic list, scripts, prompts, operation SOP, or campaign plan.
   - `质检`: originality, factual risk, platform fit, sales pressure, anti-AI style.
4. Prefer practical outputs: tables, numbered steps, prompt packs, review rubrics, and ready-to-use content drafts. Keep reasoning visible enough for the user to edit.

## Output Standards

For topic planning, produce at least: `选题`, `目标人群`, `情绪触发`, `反常识/冲突`, `开头钩子`, `正文推进`, `证据/案例`, `CTA`, `风险备注`.

For scripts, produce at least: `标题`, `黄金三秒`, `镜头/画面`, `口播`, `转折`, `信任证据`, `评论引导`, `备选标题`.

For IP positioning, produce at least: `人物底色`, `专业标签`, `反差标签`, `内容支柱`, `可讲故事`, `禁区`, `商业承接方式`.

For private-domain or ads, produce at least: `流量入口`, `筛选问题`, `承接话术`, `内容节奏`, `转化动作`, `复盘指标`, `合规风险`.

## Guardrails

- Do not claim that a strategy is proven unless the user provides results or credible evidence.
- Do not invent book, course, client, or platform data. Mark unknowns as assumptions.
- Do not copy source prompts. Convert them into new, compact operating procedures.
- Avoid manipulative tactics that exploit sensitive personal attributes, medical vulnerability, debt distress, or illegal financial claims.
- For regulated verticals such as finance, healthcare, law, education, insurance, and debt services, include compliance review notes and avoid guaranteed outcomes.
