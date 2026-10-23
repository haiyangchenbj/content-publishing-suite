## Description:

Turns a fact-checked and compliance-approved final Markdown draft into local multi-channel publishing assets for WeChat, LinkedIn, standalone HTML, and archive records without repeating fact-checking or auto-publishing.

This skill is ready for commercial/non-commercial use.

## Publisher:

[haiyangchenbj](https://clawhub.ai/user/haiyangchenbj)

### License/Terms of Use:

MIT-0

## Use Case:

Content and publishing teams use this skill to convert an already reviewed Markdown article into channel-ready local assets for WeChat, LinkedIn, standalone HTML, and archive ledgers. It is intended for publishing orchestration and format validation, not upstream fact-checking, content rewriting, or automatic posting.

### Deployment Geography for Use:

Global

## Known Risks and Mitigations:

Risk: Unreviewed or non-final drafts could be packaged as publishable assets.

Mitigation: Require an approved final-check file or explicit reviewed marker before generation, and stop when the input gate is not satisfied.

Risk: Generated assets could be posted before a human catches formatting, factual-boundary, or channel-specific issues.

Mitigation: Review generated files before posting, run the bundled validation gates, and keep external actions in dry-run mode until the user explicitly approves the target action.

Risk: Credentials, internal notes, or conversation traces could leak into publishing files.

Mitigation: Use environment variables for credentials, avoid hardcoded secrets, and run the output validator that checks for credential prefixes, internal markers, and conversation traces.

Risk: WeChat formatting or summary-card requirements could drift from the intended layout contract.

Mitigation: Use the bundled WeChat baseline and deterministic layout validators before delivery, especially when enforcing the visual chain for cover and summary-card assets.

## Reference(s):

- [Channel output contracts](artifact/references/channel-contracts.md)
- [WeChat 135 inline style guide](artifact/references/wechat-style.md)
- [WeChat layout baseline](artifact/references/wechat_layout_baseline.json)
- [Build publish package script](artifact/scripts/build_publish_package.py)
- [Publish output validator](artifact/scripts/validate_publish_output.py)
- [WeChat layout validator](artifact/scripts/validate_wechat_layout.py)

## Skill Output:

**Output Type(s):** [text, markdown, html, json, shell commands, configuration, guidance]

**Output Format:** [Local publishing package files plus validation reports and archive ledger JSON]

**Output Parameters:** [1D]

**Other Properties Related to Output:** [Produces channel-specific local assets such as WeChat snippets and previews, LinkedIn copy, standalone HTML, archive-ledger entries, package manifests, and gate reports; external posting remains gated by user confirmation.]

## Skill Version(s):

1.1.13 (source: frontmatter and release evidence)

## Ethical Considerations:

Users should evaluate whether this skill is appropriate for their environment, review any generated or modified files before relying on them, and apply their organization's safety, security, and compliance requirements before deployment.
