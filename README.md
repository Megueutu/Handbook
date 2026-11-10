# Handbook

My personal collection of reusable agent skills. The instructions focus on decisions and workflows that remain useful across projects and tools.

## Skills

| Skill | Purpose |
| --- | --- |
| [drdw](skills/drdw/SKILL.md) | Check existing solutions and weigh reuse against custom implementation. |
| [expert-designer](skills/expert-designer/SKILL.md) | Compare distinct static HTML interface prototypes outside the product repository, with a local server and links between attempts. |
| [ill-sleep](skills/ill-sleep/SKILL.md) | Complete authorized work without routine confirmation checkpoints, with subagent coordination, verification, and honest blocker reporting. |
| [mock-me](skills/mock-me/SKILL.md) | Discover project conventions, persist an evidence-based Markdown profile, and match them in the requested work. |
| [review-allergy](skills/review-allergy/SKILL.md) | Keep one coherent delivery in one evolving PR, avoiding duplicates and repetitive review churn. |

## Use

Each folder under `skills/` is an independent skill with a `SKILL.md` entry point. Copy the whole folder into your harness's supported skills directory, or use its skill installer with this repository and the desired skill path. Cloning this repository alone does not install or activate the skills.

For example, with Codex's skill installer, request:

```text
Install drdw from megueutu/handbook at skills/drdw.
Install expert-designer from megueutu/handbook at skills/expert-designer.
Install ill-sleep from megueutu/handbook at skills/ill-sleep.
Install mock-me from megueutu/handbook at skills/mock-me.
Install review-allergy from megueutu/handbook at skills/review-allergy.
```

Once installed in Codex, explicitly invoke `$drdw`, `$expert-designer`, `$ill-sleep`, `$mock-me`, or `$review-allergy`. Other harnesses may use different installation locations and invocation syntax. The skill descriptions also specify when an agent should consider them automatically, where supported.

For example: `Use $ill-sleep to implement the agreed plan, run the relevant checks, and finish all authorized steps while I am away.` This removes routine confirmation checkpoints; it does not change permissions, guarantee an overnight runtime, or authorize extra external actions. Subagents are used when available and useful, with sequential execution as a fallback.

The skills use tools already available in the environment and do not require a bundled MCP server, framework, or runtime. Prototype exploration needs a usable static HTTP server; browser inspection depends on the harness's available browser tools.

## License

[MIT](LICENSE).
