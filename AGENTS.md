# Reusable process skills

Skills normalize capable agents' default approaches across projects. They do not teach expertise or improve the agent. Trust the agent's judgment; specify only the conventions that matter.

## Categories

- **Passive:** ongoing guidance within its stated scope once enabled, like an MTG static ability.
- **Activated:** a workflow deliberately requested by name or intent, like an MTG activated ability. It may be finite or explicitly continuous.

Store skills in `skills/<passive|activated>/<name>/SKILL.md`. Frontmatter requires `name`, a concise `description`, and `metadata.category`. Names are unique across categories. Activated Codex adapters set `policy.allow_implicit_invocation: false` in `agents/openai.yaml`; directory names alone do not enforce activation.

## Skill selection

Use the [request-term catalog](README.md#choose-what-to-read) and skill descriptions to choose what to read. Match the requested outcome, not a keyword alone. Load applicable passive conventions and the selected workflow; follow related links only when needed. Keep one shared goal record across transitions.

## Authoring

Use [design-and-refine-skill](skills/activated/design-and-refine-skill/SKILL.md) for requested creation or refinement.

- Keep only the intended outcome and critical choices where agent defaults should converge. Leave execution to the agent.
- Remove tutorials, micromanagement, repeated policy, obvious advice, and speculative edge cases. Every sentence costs attention.
- Prefer deletion or replacement to additional rules. Do not move unnecessary prose into references to make the entrypoint appear shorter.
- Keep skills portable and self-contained. Add supporting files only for necessary task-specific material.
- Check format and links; use behavioral evaluation when a consequential uncertainty warrants it.

## Scratch space

Use [scratch-space](skills/passive/scratch-space/SKILL.md) for durable, Git-versioned task notes in `./agents/scratch/`. Never ignore this directory; include relevant note updates when committing authorized work. Relevant skills read prior records and retain progress and evidence there; keep one record per goal rather than separate logs per skill. Read-only task scope still applies.

Use `./agents/tmp/` for disposable files. Always keep `/agents/tmp/` in the root `.gitignore`; never force-add its contents. Preserve evidence needed for future work outside this directory.

## Self-improvement

Self-improvement: enabled.

After a skill-assisted task exposes a reusable lesson, apply the [self-improvement hook](skills/activated/design-and-refine-skill/SKILL.md#self-improvement-hook) within the task's write scope. No evidence means no edit. Set the declaration above to `Self-improvement: disabled.` to turn off automatic refinement; explicit authoring requests still apply.

## Reference skill libraries

Use relevant examples as inspiration, not requirements. Favor this collection's minimalism over a reference library's complexity; check licenses before copying material.

| Library | Useful ideas to examine |
| --- | --- |
| [Anthropic skills](https://github.com/anthropics/skills) | Self-contained packaging, concise entrypoints, and supporting resources for substantial workflows. |
| [Obra Superpowers](https://github.com/obra/superpowers) | Composable development processes, explicit workflow transitions, and skill validation practices. Adapt individual ideas without importing the entire methodology. |
| [Vercel agent-skills](https://github.com/vercel-labs/agent-skills) | Clear use conditions, impact-based prioritization, and separation of collections into focused skills. Generalize relevant process ideas from stack-specific examples. |
| [Hermes Agent bundled skills](https://github.com/NousResearch/hermes-agent/tree/main/skills) | Default skill architecture, capability-focused discovery, progressive disclosure, and evidence-driven refinement. Inspect its [skill authoring procedure](https://github.com/NousResearch/hermes-agent/blob/main/skills/software-development/hermes-agent-skill-authoring/SKILL.md) and distinguish portable principles from Hermes-specific runtime policies. |

Use the [Agent Skills specification](https://agentskills.io/specification) for portable packaging. It is a format reference, not a skill library. Verify current content when relying on external conventions; avoid preserving star counts or treating popularity as evidence of effectiveness.
