# AI 产品逆向工程拆解引擎

> 按六层框架（市场 → 商业 → 用户 → 技术 → 模型 → 基础）引导用户自己拆解 AI 产品，适合竞品分析与面试准备。

**Skill name**: `ai-product-teardown`

---

## 安装方法

把整个目录复制到 `~/.claude/skills/`，重启 Claude Code 后即可通过自然语言触发：

```bash
cp -R ai-product-teardown ~/.claude/skills/
```

## 触发说明

以下为 `SKILL.md` frontmatter 中的原始 description（决定 Claude 何时自动激活此 skill）：

> AI产品逆向工程拆解引擎。当用户提到"拆解XX产品"、"分析XX产品"、"XX产品怎么做的"、"帮我拆一下XX"、"逆向工程"、"竞品分析"、"产品拆解"、"看看这个产品"时立即触发。也适用于用户说"我想了解XX产品的架构"、"XX是怎么实现的"、"帮我分析一下竞品"、"面试要聊XX产品"、"我想复刻一个类似的产品"等表达。即使用户只说"看看这个AI产品"或"这个产品挺有意思的"，只要涉及AI产品的深度拆解、竞品分析、架构还原、面试准备场景，都应触发此skill。覆盖从市场分析到基础数据层的六层逆向拆解全流程，支持按需裁剪深度。注意：如果用户只是简单问"XX产品好不好用"这种一句话评价，不需要触发，直接回答即可。此skill专为需要系统性深度拆解AI产品的场景设计。

## 目录结构

```
ai-product-teardown/
├── SKILL.md
├── references/
├── scripts/
├── templates/
└── README.md
```

## License

MIT
