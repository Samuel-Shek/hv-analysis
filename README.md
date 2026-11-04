# hv-analysis · 横纵分析法

> **English:** A research skill for AI agents that studies a product, company, technology, concept or person along two axes: the vertical axis explains how it got here (origins, turning points, path dependence), the horizontal axis compares it with peers at the same point in time, and the cross analysis links historical choices to today's strengths, weaknesses and constraints. Depth, length and file export follow the request; facts, inferences and opinions are kept apart with sources and dates. Optional Markdown → PDF export. Adapted from [KKKKhazix/khazix-skills](https://github.com/KKKKhazix/khazix-skills) (MIT). Chinese-language skill.

## 它做什么

- **纵向**：诞生时的需求与条件、关键转折、决策条件和路径依赖——按因果组织，不堆年表。
- **横向**：说明为什么选这些比较对象，按统一口径比较能力、短板、场景和成本；没有直接同类就分析替代方案，不凑竞品。
- **交叉**：把历史选择与当前差异连起来；未来路径写明依据、成立条件、可观察信号和失效条件，不凭空给概率。
- **证据纪律**：明确研究截止时间，关键事实标来源和日期，事实 / 推断 / 观点分开，转载不算独立印证。
- **深度随需求**：快速了解给核心判断；明确要深度研究才读取长篇参考模板；要 PDF 才导出。

不触发：简单名词解释、纯润色、公众号创作。

## 安装

这是一个 Agent Skill（一份写给 AI 读的工作说明，入口是 `SKILL.md`），可用于 Claude Code、Codex 等支持 skills 目录的工具。不需要额外的 API key 或后台服务；PDF 导出另需 Python 包 `markdown` 和 `weasyprint`。

把整个仓库放进你的 skills 目录，目录名保持 `hv-analysis`：

```bash
# Claude Code（个人级）
git clone https://github.com/Samuel-Shek/hv-analysis.git ~/.claude/skills/hv-analysis

# Codex
git clone https://github.com/Samuel-Shek/hv-analysis.git ~/.codex/skills/hv-analysis
```

其他工具放进各自的 skills 目录即可。装好后重开会话，说“用横纵分析法研究一下 XX”即可。

## 导出 PDF（可选）

```bash
python <skill-dir>/scripts/md_to_pdf.py input.md output.pdf --title "研究对象名称"
# 需要署名时再加 --author "作者名称"
```

## 目录

| 文件 | 用途 |
|---|---|
| `SKILL.md` | 主说明：深度选择、证据规则、双轴与交叉分析 |
| `references/deep-research.md` | 深度研究的细化维度与长篇模板 |
| `references/schema.json` | 结构化资料参考 |
| `references/export.md` | PDF 导出说明 |
| `scripts/md_to_pdf.py` | Markdown → PDF 转换 |

## 来源与致谢

横纵分析法由**数字生命卡兹克**提出并分享，本项目改编自 [KKKKhazix/khazix-skills](https://github.com/KKKKhazix/khazix-skills) 的 `hv-analysis`（MIT），正文重写为 v2.0.0，`schema.json` 和 `md_to_pdf.py` 在原版基础上修改。详见 [NOTICE](NOTICE)。

## 许可证

[MIT](LICENSE)，保留原作者数字生命卡兹克的版权声明。
