# Product Insight Miner · 三平台产品灵感挖掘

> 从小红书 / X (Twitter) / Reddit 采集真实用户声音，聚类分析后一键生成 HTML 可视化洞察报告。

**Skill name**: `product-insight-miner`

---

## 安装方法

把整个目录复制到 `~/.claude/skills/`，重启 Claude Code 后即可通过自然语言触发：

```bash
cp -R product-insight-miner ~/.claude/skills/
```

## 触发说明

以下为 `SKILL.md` frontmatter 中的原始 description（决定 Claude 何时自动激活此 skill）：

> AI产品灵感挖掘引擎——从小红书、X(Twitter)、Reddit三平台采集用户痛点和需求信号，聚类分析后生成可视化HTML洞察报告。当用户提到"挖掘产品灵感"、"看看用户在抱怨什么"、"痛点挖掘"、"需求发现"、"市场调研"、"产品灵感"、"去三个平台看看"、"帮我搜一下用户反馈"时立即触发。也适用于用户说"这个方向有没有人做"、"看看这个品类的用户痛点"、"帮我调研一下"、"找找产品机会"、"有什么值得做的"、"搜一下大家在吐槽什么"等表达。即使用户只说"帮我看看XX的用户反馈"或给了一个产品方向说"帮我挖掘一下"，只要涉及从社交平台采集用户声音、发现产品机会的场景，都应触发此skill。支持两种工作模式：自动搜索采集模式和手动素材投喂模式，可混合使用，最终一键生成HTML可视化报告。注意：此skill专注于AI产品/工具领域的灵感挖掘，但也可灵活适配其他品类。

## 目录结构

```
product-insight-miner/
├── SKILL.md
├── references/
└── README.md
```

## License

MIT
