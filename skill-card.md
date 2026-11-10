## Description:

Converts a fact-checked and compliance-approved Markdown draft into WeChat, LinkedIn, responsive HTML, and archive assets without repeating fact-checking or automatically publishing.

This skill is ready for commercial/non-commercial use.

## Publisher:

[haiyangchenbj](https://clawhub.ai/user/haiyangchenbj)

### License/Terms of Use:

MIT-0

## Use Case:

Developers and content teams use this skill to turn an already reviewed Markdown draft into channel-specific publishing assets and an archive record. It keeps external publishing behind a separate confirmation step.

### Deployment Geography for Use:

Global

## Known Risks and Mitigations:

Risk: The helper may overwrite files outside its promised output folder.

Mitigation: Use an isolated output folder, back up existing project files and ledgers, and require approval for additional destinations and overwrites.

Risk: External publishing may act on an unintended target.

Mitigation: Confirm targets and require approval before any external publishing.

Risk: The publishing workflow relies on a separate checker dependency.

Mitigation: Review the checker dependency and confirm its targets before relying on checks or publishing externally.

## Reference(s):

- [Channel contracts](artifact/references/channel-contracts.md)
- [WeChat styling guide](artifact/references/wechat-style.md)
- [WeChat layout baseline](artifact/references/wechat_layout_baseline.json)
- [Content Publishing Suite on ClawHub](https://clawhub.ai/haiyangchenbj/skills/content-publishing-suite-skill)

## Skill Output:

**Output Type(s):** [Files, Markdown, HTML, JSON, Images, Publishing guidance]

**Output Format:** [Markdown, inline HTML, JSON, and image assets]

**Output Parameters:** [1D]

**Other Properties Related to Output:** [Transforms an approved draft into selected channel assets; external publishing is not automatic.]

## Skill Version(s):

1.1.14 (source: server-resolved release metadata)

## Ethical Considerations:

Users should evaluate whether this skill is appropriate for their environment, review any generated or modified files before relying on them, and apply their organization's safety, security, and compliance requirements before deployment.
