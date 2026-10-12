# Dev skills

**A library of reusable workflow skills for coding agents.**

Different coding agents make different choices about when to test, what to commit, how to investigate failures, and what to remember. Dev Skills puts those decisions into reusable Markdown instructions, so you can establish your working conventions once instead of explaining them again in every project and session.

## Install

Dev Skills is designed to be installed in your project or agent. Copy this prompt into your coding agent; it will ask where to install and whether you want skill self-improvement enabled.

```text
Use https://github.com/curvedinf/dev-skills/blob/main/skills/activated/install-dev-skills/SKILL.md to install dev-skills.
```

## Conventions your agent follows throughout work

Routine work should not require repeated reminders about scope, testing, commits, or lost context. Passive skills keep those expectations available throughout a task, giving your agent a shared basis for recurring decisions.

| Skill | What it guides |
| --- | --- |
| [evidence-discipline](skills/passive/evidence-discipline/SKILL.md) | Support claims with evidence and state what remains unverified. |
| [contract-discipline](skills/passive/contract-discipline/SKILL.md) | Keep work aligned with your requirements and scope. |
| [git-discipline](skills/passive/git-discipline/SKILL.md) | Preserve local work and follow branch, commit, and push conventions. |
| [testing-doctrine](skills/passive/testing-doctrine/SKILL.md) | Select checks for development, integration, and release. |
| [documentation-style](skills/passive/documentation-style/SKILL.md) | Explain the product and reader context before giving instructions. |
| [refine-skill](skills/passive/refine-skill/SKILL.md) | Turn corrections and workflow lessons into skill updates when enabled. |
| [scratch-space](skills/passive/scratch-space/SKILL.md) | Save progress, decisions, and failed experiments for later sessions. |

## Workflows you ask your agent to run

Some jobs need a deliberate process: a bug needs a reproduction, an experiment needs a baseline, and an interrupted deployment needs its state checked before retrying. Activated skills capture those processes so you can request the job without writing the procedure each time. Ask your agent to use a skill by name and describe the result you want.

| Skill | What it does |
| --- | --- |
| [install-dev-skills](skills/activated/install-dev-skills/SKILL.md) | Install the library in a project or agent-wide and merge its guidance. |
| [design-skill](skills/activated/design-skill/SKILL.md) | Create reusable process skills. |
| [polish-docs](skills/activated/polish-docs/SKILL.md) | Rewrite and style documentation so newcomers understand the project and can start using it. |
| [diagnose-and-repair](skills/activated/diagnose-and-repair/SKILL.md) | Reproduce a bug, identify its cause, and verify the fix. |
| [design-validation](skills/activated/design-validation/SKILL.md) | Design tests that establish whether requirements are met. |
| [run-experiment](skills/activated/run-experiment/SKILL.md) | Compare alternatives under controlled conditions. |
| [indefinite-loop](skills/activated/indefinite-loop/SKILL.md) | Research and run successive experiment batches, keeping measured improvements. |
| [coordinate-work](skills/activated/coordinate-work/SKILL.md) | Divide work among contributors and verify the combined result. |
| [audit-and-resolve](skills/activated/audit-and-resolve/SKILL.md) | Review work, verify findings, and resolve authorized corrections. |
| [operate-workflow](skills/activated/operate-workflow/SKILL.md) | Carry out deployments, migrations, and other operations, reconciling partial results before retrying. |

[Skill design and references](AGENTS.md) · [Research notes](docs/skill-research.md) · [MIT license](LICENSE)
