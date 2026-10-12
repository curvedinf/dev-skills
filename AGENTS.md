# Reusable process skills

Skills normalize capable agents' default approaches across projects. They do not teach expertise or improve the agent. Trust the agent's judgment; specify only the conventions that matter.

## Categories

- **Passive:** ongoing guidance within its stated scope once enabled, like an MTG static ability.
- **Activated:** a workflow deliberately requested by name or intent, like an MTG activated ability. It may be finite or explicitly continuous.

Store skills in `skills/<passive|activated>/<name>/SKILL.md`. Frontmatter requires `name`, a concise `description`, and `metadata.category`. Names are unique across categories. Activated Codex adapters set `policy.allow_implicit_invocation: false` in `agents/openai.yaml`; directory names alone do not enforce activation.

## Skill selection

Scan the request terms below or a skill’s frontmatter `description`. Load the workflow matching the requested outcome and only the passive conventions enabled for that work. A keyword is a routing hint, not permission to start another task.

- **Testing:** `testing-doctrine` decides when and how broadly to test; `design-validation` designs the checks; `diagnose-and-repair` investigates a failing behavior.
- **Improvement:** `run-experiment` answers a bounded comparison; `indefinite-loop` repeats experiment batches only when continuous work is requested.
- **Documentation:** `documentation-style` shapes ordinary edits; `polish-docs` redesigns the first-use experience.
- **Delivery:** `git-discipline` governs repository changes; `operate-workflow` handles external operations; `audit-and-resolve` assesses findings; `coordinate-work` manages assignments.

Switch workflows when the needed outcome changes, carrying the same goal record forward. Cross-links provide related guidance; they do not require loading the whole collection or invoking every linked workflow.

| Request terms | Read |
| --- | --- |
| claims, citations, uncertainty | [evidence-discipline](skills/passive/evidence-discipline/SKILL.md) |
| scope, requirements, ownership | [contract-discipline](skills/passive/contract-discipline/SKILL.md) |
| commit, push, merge, branches | [git-discipline](skills/passive/git-discipline/SKILL.md) |
| test cadence, nightly, release gates | [testing-doctrine](skills/passive/testing-doctrine/SKILL.md) |
| wording, terminology, examples | [documentation-style](skills/passive/documentation-style/SKILL.md) |
| checkpoint, resume, history | [scratch-space](skills/passive/scratch-space/SKILL.md) |
| create skill, refine, consolidate | [design-and-refine-skill](skills/activated/design-and-refine-skill/SKILL.md) |
| README, onboarding, quickstart | [polish-docs](skills/activated/polish-docs/SKILL.md) |
| debug, crash, regression | [diagnose-and-repair](skills/activated/diagnose-and-repair/SKILL.md) |
| test plan, acceptance, coverage gaps | [design-validation](skills/activated/design-validation/SKILL.md) |
| benchmark, compare, feasibility | [run-experiment](skills/activated/run-experiment/SKILL.md) |
| continuous optimization, metrics | [indefinite-loop](skills/activated/indefinite-loop/SKILL.md) |
| delegate, parallelize, handoff | [coordinate-work](skills/activated/coordinate-work/SKILL.md) |
| review, audit, PR findings | [audit-and-resolve](skills/activated/audit-and-resolve/SKILL.md) |
| deploy, migrate, resume job | [operate-workflow](skills/activated/operate-workflow/SKILL.md) |

## Authoring

Use [design-and-refine-skill](skills/activated/design-and-refine-skill/SKILL.md) for requested creation or refinement.

- `README.md` is for humans and is marketing-centric: communicate concrete value, credible proof, and a clear path to adoption. `AGENTS.md` is for computers and is utility-centric: provide precise routing, constraints, commands, and decision rules. Keep agent operating instructions out of the README and promotional prose out of AGENTS. Marketing remains evidence-driven, without exaggeration.
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
