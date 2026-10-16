# Claude Skills 个人合集

> 我在日常 AI 产品 / 内容 / 学习工作流中积累的 Claude Code Skill 合集。包含 15 个面向 AI PM、内容创作、学习沉淀、产品拆解的 skill，全部可独立拷贝到本地 `~/.claude/skills/` 使用。

## 这个仓库是什么

Claude Code 的 [Skills](https://docs.claude.com/en/docs/claude-code/skills) 是一种把"在什么场景下我要做什么"封装成可复用模块的能力。每个 skill 是一个目录，包含 `SKILL.md`（带 frontmatter 的系统提示）以及可选的模板、参考资料、子文档。当用户说话命中触发条件，Claude Code 会自动加载对应 skill 接管对话。

这个仓库收录的全部是我自己在用的中文场景 skill，覆盖三类场景：

1. **产品工作流** — BRD → MRD → PRD 全链路、AI 产品逆向拆解、产品灵感挖掘
2. **求职 / 面试** — AI 产品经理简历撰写、面试诊断与备战
3. **学习 / 内容沉淀** — 48 小时领域加速学习、Bloom 2 Sigma 一对一学习、Obsidian 原子笔记、长文共创

## 完整目录

| Skill | 中文标题 | 用途一句话 |
|---|---|---|
| [`48h-accelerated-learning`](./48h-accelerated-learning) | 48 小时领域加速学习引擎 | 短时间内建立任意领域的认知全景图，达到能与专家对话的水平 |
| [`ai-agent-prd-writer`](./ai-agent-prd-writer) | AI Agent 产品 PRD 撰写专家 | 面向开发团队的正式 PRD 全流程撰写 |
| [`ai-pm-interview-diagnosis`](./ai-pm-interview-diagnosis) | AI 产品经理面试诊断 | 对面试录音/转写做诊断复盘 + JD 对齐备战 |
| [`ai-pm-resume-writer`](./ai-pm-resume-writer) | AI 产品经理简历撰写 | 覆盖 15-40k 全薪资段的简历撰写 / 优化 / JD 适配 |
| [`ai-product-teardown`](./ai-product-teardown) | AI 产品逆向工程拆解 | 按六层框架引导用户自己拆解 AI 产品 |
| [`brd`](./brd) / [`brd-writing`](./brd-writing) | 商业需求文档生成器 | 在投入时间之前判断一个方向值不值得做 |
| [`mrd`](./mrd) / [`mrd-writing`](./mrd-writing) | 市场需求文档生成器 | 从用户原声数据中提炼市场信号 |
| [`prd-writing`](./prd-writing) / [`vibe-prd-writer`](./vibe-prd-writer) | Vibe PRD Writer | 可直接喂给 Claude Code / Cursor 的 10 模块 PRD |
| [`interactive-learning`](./interactive-learning) | 一对一自适应学习 | 基于 Bloom 2 Sigma 的苏格拉底式教学 |
| [`obsidian-knowledge-saver`](./obsidian-knowledge-saver) | Obsidian 原子知识库 | 对话 / 素材提炼为原子笔记写入 vault |
| [`product-insight-miner`](./product-insight-miner) | 三平台产品灵感挖掘 | 小红书 / X / Reddit 用户痛点采集 + HTML 报告 |
| [`simin-article-cowriter`](./simin-article-cowriter) | AI / 产品长文共创助手 | 分步共创干货长文，输出到 Obsidian |

> 关于 `brd` / `brd-writing`、`mrd` / `mrd-writing`、`prd-writing` / `vibe-prd-writer` 这三对：内容相同，命名差异是为了对应不同自然语言触发命令（如 `/brd` 和 "帮我写 brd"），需要的话保留一个即可。

## 相关仓库

- [`codex-skills`](https://github.com/wbx125133/codex-skills) — 面向 Codex 的产品、设计与内容技能合集。
- [`AIPM-Vibecoding-Skill`](https://github.com/wbx125133/AIPM-Vibecoding-Skill) — `vibe-coding-prd` skill 单独发布在这个仓库（5 模块 + 17 项自查清单的 AI 可执行 PRD），未收录在本合集以避免重复。

## 按任务选择

| 当前任务 | 建议入口 |
|---|---|
| 判断方向值不值得做 | `brd-writing` |
| 从用户反馈中提炼市场需求 | `mrd-writing` |
| 给开发团队写正式需求 | `ai-agent-prd-writer` |
| 写 AI 编程助手执行的项目规范 | `prd-writing`，或独立仓库中的 `vibe-coding-prd` |
| 拆解产品、寻找产品机会 | `ai-product-teardown` / `product-insight-miner` |
| 求职、学习与知识沉淀 | 面试 / 简历、学习、Obsidian 与长文共创技能 |

## 安装

`brd` / `brd-writing`、`mrd` / `mrd-writing`、`prd-writing` / `vibe-prd-writer` 各组选一个即可，避免重复安装。同名技能已存在时先比较和备份。

### 全量安装

```bash
git clone https://github.com/wbx125133/claude-skills.git
cd claude-skills
mkdir -p "$HOME/.claude/skills"
for source in */; do
  [ -f "${source}SKILL.md" ] || continue
  skill_name="${source%/}"
  case "$skill_name" in brd|mrd|vibe-prd-writer) continue ;; esac
  if [ -e "$HOME/.claude/skills/$skill_name" ] || [ -L "$HOME/.claude/skills/$skill_name" ]; then
    printf '跳过已存在的 Skill：%s\n' "$skill_name"
    continue
  fi
  cp -R "$source" "$HOME/.claude/skills/$skill_name"
done
```

### 单个安装

```bash
git clone https://github.com/wbx125133/claude-skills.git
mkdir -p "$HOME/.claude/skills"
if [ ! -e "$HOME/.claude/skills/brd-writing" ] && [ ! -L "$HOME/.claude/skills/brd-writing" ]; then
  cp -R claude-skills/brd-writing "$HOME/.claude/skills/brd-writing"
fi
```

单个安装以 `brd-writing` 为例，选择其他技能时替换目录名。

重启 Claude Code（或新开会话）后，skill 会根据 `SKILL.md` frontmatter 里的 `description` 自动判断何时触发，也可以用 `/<skill-name>` 显式调用。

## 自定义建议

每个 skill 目录的 `SKILL.md` 是核心入口，可以直接改：

- **改触发条件**：调整 `description` 里的触发词列表
- **改语气 / 身份设定**：改 frontmatter 后面的提示主体
- **加模板 / 参考**：放进同目录其它文件，在 `SKILL.md` 里引用

特别是 `simin-article-cowriter` 含我个人化称呼，使用前请把"思敏"改成你自己的名字。

## License

MIT — 个人 skill 收藏，欢迎参考改造，不保证持续维护。
