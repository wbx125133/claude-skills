# Obsidian 原子知识库助手

> 把对话 / 素材提炼为原子笔记写入 Obsidian vault，自动维护索引与操作日志。基于 Zettelkasten + LLM Wiki 模式。

**Skill name**: `obsidian-knowledge-saver`

---

## 安装方法

把整个目录复制到 `~/.claude/skills/`，重启 Claude Code 后即可通过自然语言触发：

```bash
cp -R obsidian-knowledge-saver ~/.claude/skills/
```

## 触发说明

以下为 `SKILL.md` frontmatter 中的原始 description（决定 Claude 何时自动激活此 skill）：

> Obsidian 知识库管理与原子笔记沉淀工具。将对话内容、原始素材提炼为可迭代的原子笔记，写入用户的 Obsidian vault，并自动维护索引和操作日志。当用户提到"帮我沉淀"、"沉淀到知识库"、"存到知识库"、"帮我整理到ob"、"写入obsidian"、"记到笔记里"、"帮我存下来"、"沉淀一下"、"这个对话帮我记一下"时立即触发。也适用于"帮我消化这篇文章"、"把这个整理成笔记"、"ingest这个"、"知识库健康检查"、"lint一下知识库"、"看看知识库有什么问题"等表达。即使用户只说"帮我记一下"或给了一篇文章说"帮我整理"，只要意图是将内容沉淀为结构化知识笔记，都应触发此skill。首次使用时会引导用户完成知识库初始化设置。

## 目录结构

```
obsidian-knowledge-saver/
├── SKILL.md
└── README.md
```

## License

MIT
