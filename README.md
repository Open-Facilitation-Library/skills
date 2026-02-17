# OFL Skills

Executable agent skills for AI-assisted facilitation, following the [Agent Skills specification](https://agentskills.io/specification).

Part of the [Open Facilitation Library](https://github.com/Open-Facilitation-Library).

## What Are Skills?

Skills are structured instructions that AI agents can discover and invoke to facilitate group processes. Each skill is a directory with a `SKILL.md` file containing frontmatter (name, description, metadata) and markdown instructions that tell an agent how to perform a specific facilitation task.

Unlike abstract facilitation patterns (described in the [synthesis](https://github.com/Open-Facilitation-Library/synthesis) knowledge base), skills are **executable** — they can be loaded by agent platforms like [Claude Code](https://claude.ai/code), [Harmonica](https://harmonica.chat), or [OpenClaw](https://github.com/openclaw) to actively facilitate conversations.

```
skill-name/
├── SKILL.md              # Required: frontmatter + instructions
├── scripts/              # Optional: executable code
├── references/           # Optional: detailed reference material
└── assets/               # Optional: templates, schemas, data files
```

## Current Content

### Facilitation Patterns (legacy format)

The `patterns/` directory contains facilitation methodologies in a custom Why-How-Who YAML schema. These document **what** each methodology does and how to apply it, but are not yet in the Agent Skills format.

| Pattern | Category | AI Suitability |
|---------|----------|----------------|
| [Cross-Pollination](patterns/deliberative/cross-pollination.yaml) | Deliberative | High |
| [Delphi Method](patterns/deliberative/delphi-method.yaml) | Deliberative | High |
| [Six Thinking Hats](patterns/generative/six-thinking-hats.yaml) | Generative | Medium |
| [Retrospective](patterns/generative/retrospective.yaml) | Generative | Medium |

The [pattern schema](patterns/schema/pattern-schema.yaml) (Why-How-Who) captures purpose, process mechanics, participant dynamics, and AI suitability. This content will inform the executable skills as they're developed.

### Resources

- [Facilitation Self-Assessment](docs/facilitation-self-assessment.md) — Competency checklist for during-session evaluation (Lucy Chambers)

## Adding Skills

To add a new skill following the [Agent Skills specification](https://agentskills.io/specification):

1. Create a directory named after your skill (lowercase, hyphens only)
2. Add a `SKILL.md` with required frontmatter (`name`, `description`) and instructions
3. Keep `SKILL.md` under 500 lines — move detailed reference material to `references/`
4. Add `scripts/` for any executable code the agent should run
5. Validate with `skills-ref validate ./your-skill`

## Relationship to OFL

Three complementary layers:
- **Patterns** (`synthesis/` knowledge base) — abstract facilitation methodologies
- **Skills** (this repo) — executable agent skills per the [Agent Skills spec](https://agentskills.io/specification)
- **Workflows** (`workflows/` repo) — how real platforms orchestrate agents into complete facilitation systems

## Related Repos

- [synthesis](https://github.com/Open-Facilitation-Library/synthesis) — Knowledge base, research monitoring, evaluation frameworks
- [workflows](https://github.com/Open-Facilitation-Library/workflows) — Agent workflow definitions for AI facilitation platforms
- [cross-pollination](https://github.com/Open-Facilitation-Library/cross-pollination) — Opinion exposure algorithms
- [evals](https://github.com/Open-Facilitation-Library/evals) — Evaluation frameworks (Why-How-Who conversation signatures)

## Stay Connected

- **[Subscribe on Substack](https://openfac.substack.com)** — Updates on OFL research and community
- **[Support on Giveth](https://giveth.io/project/open-facilitation-library)** — Help fund open facilitation standards

## License

MIT License
