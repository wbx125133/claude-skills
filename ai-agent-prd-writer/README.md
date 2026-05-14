# AI Agent 产品 PRD 撰写专家

> 面向开发团队的正式 PRD 全流程撰写工具，覆盖工具型 / Agent 型 / 对话型 / 平台型 AI 产品。

**Skill name**: `ai-agent-prd-writer`

---

## 安装方法

把整个目录复制到 `~/.claude/skills/`，重启 Claude Code 后即可通过自然语言触发：

```bash
cp -R ai-agent-prd-writer ~/.claude/skills/
```

## 触发说明

以下为 `SKILL.md` frontmatter 中的原始 description（决定 Claude 何时自动激活此 skill）：

> AI Agent 产品 PRD 全流程撰写工具。当用户提到"帮我写PRD"、"写需求文档"、"梳理产品需求"、"PRD"、"产品需求文档"、"功能设计文档"、"帮我做产品设计"、"需求梳理"时立即触发。覆盖所有类型的 AI 产品 PRD（工具型、Agent型、对话型、平台型），支持从需求模糊到需求清晰的全场景。无论用户说"帮我理一下这个需求"还是"直接帮我输出PRD"，都应触发此 skill。即使用户只提到"功能设计"或"需求分析"，只要涉及 AI 产品，也应触发。

## 目录结构

```
ai-agent-prd-writer/
├── SKILL.md
├── references/
└── README.md
```

## License

MIT
