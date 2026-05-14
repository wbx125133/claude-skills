# MRD Writer · 市场需求文档生成器（writing 别名）

> 与 mrd 同源内容，命名差异用于不同的自然语言触发场景。

**Skill name**: `mrd-writing`

---

## 安装方法

把整个目录复制到 `~/.claude/skills/`，重启 Claude Code 后即可通过自然语言触发：

```bash
cp -R mrd-writing ~/.claude/skills/
```

## 触发说明

以下为 `SKILL.md` frontmatter 中的原始 description（决定 Claude 何时自动激活此 skill）：

> 市场需求文档（MRD）引导式生成器——在 BRD 确认方向后，深入分析市场需求。当用户提到"写MRD"、"市场需求文档"、"梳理市场需求"、"帮我分析用户数据"、"从用户反馈里提炼需求"时立即触发。也适用于"帮我看看这些用户原声"、"这批数据能提炼出什么"、"帮我做市场分析"等表达。即使用户只说"这些反馈帮我理一下"或给了一批用户数据说"帮我提炼"，只要意图是从用户数据中提炼市场需求、形成结构化的市场需求文档，都应触发此skill。注意：如果用户说"BRD"或"商业需求文档"，应触发 /brd 而非本 skill。

## 目录结构

```
mrd-writing/
├── SKILL.md
└── README.md
```

## License

MIT
