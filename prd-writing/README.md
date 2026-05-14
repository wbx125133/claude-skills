# Vibe PRD Writer · 完整项目规范生成器

> 把一个产品想法转化为可直接喂给 Claude Code / Cursor 的 10 模块完整 PRD。

**Skill name**: `prd-writing`

---

## 安装方法

把整个目录复制到 `~/.claude/skills/`，重启 Claude Code 后即可通过自然语言触发：

```bash
cp -R prd-writing ~/.claude/skills/
```

## 触发说明

以下为 `SKILL.md` frontmatter 中的原始 description（决定 Claude 何时自动激活此 skill）：

> 完整项目规范（PRD）生成器——把一个产品想法转化成可直接喂给 Claude Code / Cursor 的 10 模块完整规范文档。自动检测并继承 BRD.md / MRD.md 的交接区数据，避免重复提问。当用户提到"帮我写个PRD"、"我想做一个XX"、"帮我梳理需求"、"我要vibe code一个产品"、"帮我写项目规范"、"coding spec"时立即触发。也适用于"帮我把这个想法变成可执行的文档"、"我想vibe code一个产品出来"、"帮我理一下做什么"等表达。即使用户只说"我想做个XX"或"帮我想想这个怎么做"，只要最终目的是产出一份可供 AI 编程 Agent 执行的 PRD，都应触发此 skill。与 ai-agent-prd-writer 的区分：ai-agent-prd-writer 是工作场景的正式 PRD（给开发团队看），本 skill 是给 AI 编程 Agent 看的项目规范（用户直接拿去 vibe coding）。

## 目录结构

```
prd-writing/
├── SKILL.md
├── references/
└── README.md
```

## License

MIT
