# Dev skills

**A library of reusable workflow skills for coding agents.**

Dev Skills packages development processes as Markdown instructions for coding agents. Its skills cover debugging, testing, Git, documentation, experiments, and progress tracking, with conventions you can reuse across projects and stacks.

## Install

To install Dev skills, copy and paste either prompt below into your coding agent.

**Project-wide — for this repository**

Copies the skills into your project and merges their guidance into its `AGENTS.md`, so the setup lives with the code and can be shared with collaborators.

```text
Use https://github.com/curvedinf/dev-skills/blob/main/skills/activated/project-install-dev-skills/SKILL.md to install dev-skills in this project and merge applicable guidance into its AGENTS.md.
```

**Agent-wide — across your projects**

Installs the skills in your agent’s personal skill directory and integrates shared guidance there, making them available across projects without copying the library into each repository.

```text
Use https://github.com/curvedinf/dev-skills/blob/main/skills/activated/agent-install-dev-skills/SKILL.md to install dev-skills in your agent-wide skills directory and integrate its AGENTS.md guidance into your shared conventions skills.
```

## Conventions your agent follows throughout work

Passive skills define how your agent handles recurring decisions—what to test, when to commit, and what to remember. Once enabled, they guide relevant work without a separate request each time.

| Skill | What it guides |
| --- | --- |
| [evidence-discipline](skills/passive/evidence-discipline/SKILL.md) | Support claims with evidence and state what remains unverified. |
| [contract-discipline](skills/passive/contract-discipline/SKILL.md) | Keep work aligned with your requirements and scope. |
| [git-discipline](skills/passive/git-discipline/SKILL.md) | Preserve local work and follow branch, commit, and push conventions. |
| [testing-doctrine](skills/passive/testing-doctrine/SKILL.md) | Select checks for development, integration, and release. |
| [documentation-style](skills/passive/documentation-style/SKILL.md) | Explain the product and reader context before giving instructions. |
| [scratch-space](skills/passive/scratch-space/SKILL.md) | Save progress, decisions, and failed experiments for later sessions. |

## Workflows you ask your agent to run

Activated skills define a process for a specific job. Ask your agent to use one by name—for example, “Use polish-docs to rewrite this README”—and describe the result you want.

| Skill | What it does |
| --- | --- |
| [project-install-dev-skills](skills/activated/project-install-dev-skills/SKILL.md) | Install the library in a project and merge its agent instructions. |
| [agent-install-dev-skills](skills/activated/agent-install-dev-skills/SKILL.md) | Install the library for your agent to use across projects. |
| [design-and-refine-skill](skills/activated/design-and-refine-skill/SKILL.md) | Create reusable skills or refine them from observed problems. |
| [polish-docs](skills/activated/polish-docs/SKILL.md) | Rewrite and style documentation so newcomers understand the project and can start using it. |
| [diagnose-and-repair](skills/activated/diagnose-and-repair/SKILL.md) | Reproduce a bug, identify its cause, and verify the fix. |
| [design-validation](skills/activated/design-validation/SKILL.md) | Design tests that establish whether requirements are met. |
| [run-experiment](skills/activated/run-experiment/SKILL.md) | Compare alternatives under controlled conditions. |
| [indefinite-loop](skills/activated/indefinite-loop/SKILL.md) | Research and run successive experiment batches, keeping measured improvements. |
| [coordinate-work](skills/activated/coordinate-work/SKILL.md) | Divide work among contributors and verify the combined result. |
| [audit-and-resolve](skills/activated/audit-and-resolve/SKILL.md) | Review work, verify findings, and resolve authorized corrections. |
| [operate-workflow](skills/activated/operate-workflow/SKILL.md) | Carry out deployments, migrations, and other operations, reconciling partial results before retrying. |

[Skill design and references](AGENTS.md) · [Research notes](docs/skill-research.md) · [MIT license](LICENSE)
