# 内容发布套件（Content Publishing Suite）

> 将一篇已审核定稿稳定转换为多平台发布物料——微信文章、LinkedIn 帖子、独立响应式 HTML、入库台账。只做发布编排与格式转换，绝不自动发布。

[![ClawHub](https://img.shields.io/badge/ClawHub-content--publishing--suite--skill-blue)](https://clawhub.ai/haiyangchenbj/content-publishing-suite-skill)
[![GitHub](https://img.shields.io/badge/GitHub-haiyangchenbj-black)](https://github.com/haiyangchenbj/content-publishing-suite-skill)

---

## 它做什么

发布编排层。将一篇已审核定稿转换为微信 / LinkedIn / 独立 HTML / 入库四类物料并生成入库台账。它**不**重复事实核验、原创性复核或跨材料审计（那些是上游 Skill），也绝不自动执行任何发布动作。

## 何时使用

- 你有一篇通过终检的定稿（`industry-deep-dive-pipeline` 的 `07-final.md`，或显式标记「已审核」的等价 Markdown），需要微信 / LinkedIn / 独立 HTML / 入库物料。
- 你要求「发到多个平台」「生成发布包」「排版并归档」。

## 何时不使用

- 内容尚未完成事实核验或合规审核 → 先走上游 Skill。
- 单纯微信排版且已有专门排版工具/平台流程 → 直接用该工具。
- 新写正文 / 改写 → 属于写作环节。

## 关键硬规则

- 输入门禁：须提供 `final-check.json`（Gate B approved、红线 0、凭据/隐私 P0 0）或显式「已审核」标记且用户确认。
- 零泄漏：发布物料中零对话痕迹、零流程元信息、零内部备注 / 笔名。
- 微信：全内联 `<section>` HTML，文末 `<v2></v2>`；禁 `<style>`/`<script>`/外层 `<div>`。
- 外部动作门禁：任何推送 / 建草稿 / 写 Notion 默认 `--dry-run`，须列目标并取得用户确认，写后回读。

## 目录结构

```
content-publishing-suite/
├── SKILL.md
├── SKILL_zh.md
├── README.md
├── README_zh.md
├── _meta.json
├── references/   # 微信样式、渠道格式合约
├── scripts/      # 打包、格式校验
└── templates/    # 微信片段、LinkedIn、独立 HTML、台账、Notion 映射样例
```

## 许可证

MIT
