# Dev Skills

**A library of reusable workflow skills for coding agents.**

Different coding agents make different choices about when to test, what to commit, how to investigate failures, and what to remember. Dev Skills normalizes those decisions into reusable Markdown instructions, so you can establish your working conventions once instead of explaining them again in every project and session.

## Install

Dev Skills is designed to be installed in your project or agent. Copy this prompt into your coding agent; it will ask where to install and whether you want skill self-improvement enabled.

```text
Use https://github.com/curvedinf/dev-skills/blob/main/skills/activated/install-dev-skills/SKILL.md to install dev-skills.
```

## Opinionated Structure

Dev Skills adapts established conventions for organizing agent work. These references explain the ideas behind the library’s defaults.

| Convention | How Dev Skills applies it |
| --- | --- |
| [Agent Skills format](https://agentskills.io/specification) | Portable Markdown skill packages with metadata, instructions, and supporting resources. |
| [Progressive disclosure](https://agentskills.io/specification#progressive-disclosure) | Request terms identify relevant skills before an agent loads their full instructions. |
| [Separate human and agent documentation](https://agents.md/#why-agents-md) | README explains the product and its value; AGENTS contains operational instructions. |
| [Diátaxis](https://diataxis.fr/) | Documentation distinguishes tutorials, how-to guides, reference, and explanation by the reader’s need. |
| [Persistent agent progress](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents) | Git-versioned goal and experiment records carry context across sessions. This project keeps them in `agents/scratch/`. |
| [Topic and integration branches](https://git-scm.com/docs/gitworkflows) | Our adaptation promotes developer-owned features through developer branches, staging, a release candidate, and main. |
| [The practical test pyramid](https://martinfowler.com/articles/practical-test-pyramid.html) | Focused checks provide early feedback; broader integration and release checks establish behavior across boundaries. Our testing doctrine adds cadence and evidence-reuse rules. |
| [Hermes skill maintenance](https://hermes-agent.nousresearch.com/docs/user-guide/features/skills) | Our opt-in refinement pass captures corrections and reusable lessons in skills after skill use. |

## Conventions your agent follows throughout work

Routine work should not require repeated reminders about scope, testing, commits, or lost context. Passive skills keep those expectations available throughout a task, giving your agent a shared basis for recurring decisions.

| Skill | What it guides |
| --- | --- |
| [evidence-discipline](skills/passive/evidence-discipline/SKILL.md) | Support claims with evidence and state what remains unverified. |
| [contract-discipline](skills/passive/contract-discipline/SKILL.md) | Keep work aligned with your requirements and scope. |
| [git-discipline](skills/passive/git-discipline/SKILL.md) | Preserve local work and follow branch, commit, and push conventions. |
| [testing-doctrine](skills/passive/testing-doctrine/SKILL.md) | Select checks for development, integration, and release. |
| [documentation-style](skills/passive/documentation-style/SKILL.md) | Explain the product and reader context before giving instructions. |
| [scratch-space](skills/passive/scratch-space/SKILL.md) | Save progress, decisions, and failed experiments for later sessions. |

## Maintenance triggered by project events

Some upkeep should happen without another request. Triggered skills run when a defined event occurs and their conditions are met; weekly scratch maintenance, for example, is checked when a fresh agent session first loads the project.

| Skill | What triggers it |
| --- | --- |
| [security-hygiene-check](skills/triggered/security-hygiene-check/SKILL.md) | Before a commit; check for personal data and secrets, and ask how to handle findings. |
| [refine-skill](skills/triggered/refine-skill/SKILL.md) | Completed skill use; apply lessons when self-improvement is enabled. |
| [maintain-scratch](skills/triggered/maintain-scratch/SKILL.md) | Fresh project session with weekly compaction due in the shared timer file. |

## Workflows you ask your agent to run

Some jobs need a deliberate process: a bug needs a reproduction, an experiment needs a baseline, and an interrupted deployment needs its state checked before retrying. Activated skills capture those processes so you can request the job without writing the procedure each time. Ask your agent to use a skill by name and describe the result you want.

| Skill | What it does |
| --- | --- |
| [install-dev-skills](skills/activated/install-dev-skills/SKILL.md) | Install Dev Skills in your project or agent’s personal skill directory and integrate its instructions. |
| [design-time-triggered-skill](skills/activated/design-time-triggered-skill/SKILL.md) | Define periodic workflows with shared timers and explicit event triggers. |
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
