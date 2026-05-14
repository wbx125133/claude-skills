# 交互式一对一学习引擎

> 基于 Bloom 2 Sigma 的掌握学习模型，通过苏格拉底式提问做自适应教学。

**Skill name**: `interactive-learning`

---

## 安装方法

把整个目录复制到 `~/.claude/skills/`，重启 Claude Code 后即可通过自然语言触发：

```bash
cp -R interactive-learning ~/.claude/skills/
```

## 触发说明

以下为 `SKILL.md` frontmatter 中的原始 description（决定 Claude 何时自动激活此 skill）：

> 基于 Bloom 2 Sigma 理论的一对一自适应学习引擎。当用户提到"我想学X"、"我想了解X"、"给我讲解一下X"、"帮我理解X"、"X是什么"、"教我X"、"学习X"时立即触发。也适用于用户说"这个概念我不太懂"、"能帮我搞清楚X吗"、"我对X很感兴趣想深入了解"等表达。即使用户只是说"聊聊X"或"讲讲X"，只要意图是学习和理解某个知识领域，都应触发此 skill。注意：如果用户只是在问一个简单的事实性问题（如"Python的列表怎么排序"），不需要触发此 skill，直接回答即可。此 skill 专为需要深度理解、系统学习的场景设计。

## 目录结构

```
interactive-learning/
├── SKILL.md
└── README.md
```

## License

MIT
