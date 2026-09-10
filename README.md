# Content Publishing Suite

> Turn a fact-checked and compliance-approved final Markdown draft into multi-channel publishing assets — WeChat article, LinkedIn post, standalone responsive HTML, and an archive ledger. Orchestrates publishing and format conversion only; never auto-publishes.

[![ClawHub](https://img.shields.io/badge/ClawHub-content--publishing--suite--skill-blue)](https://clawhub.ai/haiyangchenbj/content-publishing-suite-skill)
[![GitHub](https://img.shields.io/badge/GitHub-haiyangchenbj-black)](https://github.com/haiyangchenbj/content-publishing-suite-skill)

---

## What it does

The publishing-orchestration layer. Converts a reviewed, approved final draft into WeChat / LinkedIn / standalone-HTML / archive assets and an archive ledger. It does **not** repeat fact-checking, originality review, or cross-material auditing (those are upstream skills), and it never performs any external publish action automatically.

## When to use

- You have a final draft that passed final check (`07-final.md` from `industry-deep-dive-pipeline`, or an equivalent Markdown explicitly marked "reviewed"), and want WeChat / LinkedIn / standalone HTML / archive assets.
- You ask to "publish this to multiple platforms", "generate a publish package", or "lay out and archive".

## When not to use

- Content not yet fact-checked or compliance-reviewed → run upstream skills first.
- Pure WeChat layout with an existing dedicated layout tool/platform flow → use that tool directly.
- Writing / rewriting body text → belongs to the writing stage.

## Hard rules (key)

- Input gate: must provide `final-check.json` (Gate B approved, red-line 0, credential/privacy P0 0) or an explicit "reviewed" marker with user confirmation.
- Zero leakage: no conversation traces, process meta, internal notes, or pen-names in any asset.
- WeChat: fully inline `<section>` HTML, ends with `<v2></v2>`; no `<style>`/`<script>`/outer `<div>`.
- External-action gate: any push / draft / Notion write defaults to `--dry-run`, needs listed targets + user confirmation, then readback.

## File structure

```
content-publishing-suite/
├── SKILL.md
├── SKILL_zh.md
├── README.md
├── README_zh.md
├── _meta.json
├── references/
│   ├── wechat-style.md
│   └── channel-contracts.md
├── scripts/
│   ├── build_publish_package.py
│   └── validate_publish_output.py
└── templates/
    ├── wechat-snippet.html
    ├── linkedin-post.md
    ├── standalone.html
    ├── archive-record.json
    └── notion-mapping.example.json
```

## License

MIT
