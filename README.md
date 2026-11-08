# Handbook

My personal collection of reusable agent skills. The instructions focus on decisions and workflows that remain useful across projects and tools.

## Skills

| Skill | Purpose |
| --- | --- |
| [drdw](skills/drdw/SKILL.md) | Check existing solutions and weigh reuse against custom implementation. |
| [expert-designer](skills/expert-designer/SKILL.md) | Compare distinct static HTML interface prototypes outside the product repository, with a local server and links between attempts. |

## Use

Each folder under `skills/` is an independent skill with a `SKILL.md` entry point. Copy the whole folder into your harness's supported skills directory, or use its skill installer with this repository and the desired skill path. Cloning this repository alone does not install or activate the skills.

For example, with Codex's skill installer, request:

```text
Install drdw from megueutu/handbook at skills/drdw.
Install expert-designer from megueutu/handbook at skills/expert-designer.
```

Once installed in Codex, explicitly invoke `$drdw` or `$expert-designer`. Other harnesses may use different installation locations and invocation syntax. The skill descriptions also specify when an agent should consider them automatically, where supported.

The skills use tools already available in the environment and do not require a bundled MCP server, framework, or runtime. Prototype exploration needs a usable static HTTP server; browser inspection depends on the harness's available browser tools.

## License

[MIT](LICENSE).
