# Dev skills

**Carry your working conventions from project to project.**

Concise, stack-independent skills for how agents investigate, experiment, document, and retain progress. They normalize capable agents' default approaches while leaving implementation choices to their expertise.

[Install](#install) · [Try a skill](#try-a-skill) · [Browse the collection](#the-collection) · [Create your own](#create-and-refine-skills)

## Install

Choose where your conventions should live:

| Scope | Installer | Result |
| --- | --- | --- |
| One project | [project-install-dev-skills](skills/activated/project-install-dev-skills/SKILL.md) | Skills copied into your project, with applicable guidance merged into its `AGENTS.md`. |
| Across projects | [agent-install-dev-skills](skills/activated/agent-install-dev-skills/SKILL.md) | Skills in your agent's user-wide library, with shared guidance integrated into conventions skills. |

Give your agent the installer link and your destination. For example:

```text
Use https://github.com/curvedinf/dev-skills/blob/main/skills/activated/project-install-dev-skills/SKILL.md
to install dev-skills in this project and merge its applicable AGENTS.md guidance.
```

For agent-wide installation, use the `agent-install-dev-skills` link above and name your agent host. Both workflows preserve existing customizations and record the installed revision. Self-improvement keeps the destination project's opt-in setting.

## Try a skill

Clone this collection somewhere your agent can read:

```sh
git clone https://github.com/curvedinf/dev-skills.git
```

From that checkout, give your agent a task with an explicit skill path:

```text
Use skills/activated/polish-docs/SKILL.md to polish this project's README.
Lead with its concrete value and give newcomers a working first-use example.
```

For another project, point to the skill's absolute path in your checkout and name the target project. The skill guides the process; the target project supplies its requirements and implementation details.

Each skill is readable Markdown with its supporting files alongside it. To install selected skills, copy their complete folders to your agent host's skill directory. Installation and discovery depend on the host. Keep the collection's relative layout when using it by path; copy `scratch-space` alongside workflows that need durable progress.

## The collection

Two kinds of skills, modeled after abilities in *Magic: The Gathering*:

| Passive · ongoing conventions | Activated · requested workflows |
| --- | --- |
| Apply within their scope once enabled, like static abilities. | Start when deliberately requested, like activated abilities. |
| Example: preserve evidence and constraints throughout work. | Example: run a controlled experiment or polish a README. |

### Passive skills

Enable selected skills in the consuming project's `AGENTS.md` by linking them and stating their scope. For example, when this checkout is a sibling named `dev-skills`:

```markdown
During project work, follow
[contract-discipline](../dev-skills/skills/passive/contract-discipline/SKILL.md)
and [scratch-space](../dev-skills/skills/passive/scratch-space/SKILL.md).
```

| Skill | Convention |
| --- | --- |
| [evidence-discipline](skills/passive/evidence-discipline/SKILL.md) | Keep claims proportional to the evidence. |
| [contract-discipline](skills/passive/contract-discipline/SKILL.md) | Preserve agreed outcomes, constraints, and ownership. |
| [git-discipline](skills/passive/git-discipline/SKILL.md) | Preserve working state and verify the full authorized publication. |
| [testing-doctrine](skills/passive/testing-doctrine/SKILL.md) | Match testing and evidence reuse to iteration, integration, and release. |
| [documentation-style](skills/passive/documentation-style/SKILL.md) | Write concrete, reader-oriented documentation. |
| [scratch-space](skills/passive/scratch-space/SKILL.md) | Preserve goal progress, experiment outcomes, and decisions across sessions. |

### Activated skills

Request these by file path, or by name when installed and supported by your host. Their included Codex adapters disable implicit invocation; passive adapters allow it. Directory names alone do not enforce either behavior.

| Skill | Outcome |
| --- | --- |
| [project-install-dev-skills](skills/activated/project-install-dev-skills/SKILL.md) | Project-local skills and merged project guidance. |
| [agent-install-dev-skills](skills/activated/agent-install-dev-skills/SKILL.md) | Agent-wide skills and discoverable shared conventions. |
| [design-and-refine-skill](skills/activated/design-and-refine-skill/SKILL.md) | A minimal reusable process or an evidence-backed refinement. |
| [polish-docs](skills/activated/polish-docs/SKILL.md) | A credible, visually polished path to first use. |
| [diagnose-and-repair](skills/activated/diagnose-and-repair/SKILL.md) | An established failure mechanism and verified correction. |
| [design-validation](skills/activated/design-validation/SKILL.md) | Checks matched to acceptance claims and their limits. |
| [run-experiment](skills/activated/run-experiment/SKILL.md) | A reproducible comparison and supported conclusion. |
| [indefinite-loop](skills/activated/indefinite-loop/SKILL.md) | Continuous batches of substantive experiments, retaining measured improvements. |
| [coordinate-work](skills/activated/coordinate-work/SKILL.md) | Bounded assignments and verified integration. |
| [audit-and-resolve](skills/activated/audit-and-resolve/SKILL.md) | Substantiated findings and explicit dispositions. |
| [operate-workflow](skills/activated/operate-workflow/SKILL.md) | Verified operational progress and safe continuation. |

## Keep progress across sessions

Skills consult and update shared goal records so later work can recover decisions, inspect results, and see which approaches were already rejected.

```text
agents/
├── scratch/           Durable notes included in Git
│   ├── index.md       Active goals and retained findings
│   └── <goal>.md      Progress, evidence, decisions, next action
└── tmp/               Disposable files, always Git-ignored
```

The [scratch-space convention](skills/passive/scratch-space/SKILL.md) keeps shared goal records in Git and disposable files out of it.

The [indefinite-loop workflow](skills/activated/indefinite-loop/SKILL.md), for example, records its baseline, sequential experiment results, rejected directions, and accepted candidate here. It favors distinct structural hypotheses over repeated parameter tweaks. Continued execution still depends on the agent runtime; saved notes provide a resumption point.

## Create and refine skills

Use [design-and-refine-skill](skills/activated/design-and-refine-skill/SKILL.md) to capture the few decisions that should stay consistent across projects. Activated skills describe a process; passive skills establish ongoing conventions. Keep both concise, concrete, and grounded in observed needs.

Self-improvement refines these procedures from user corrections and demonstrated lessons. It is enabled for this repository. To opt in elsewhere, add this to the consuming project's `AGENTS.md`, adjusting the link to your checkout:

```markdown
Self-improvement: enabled.

After skill-assisted work exposes a reusable lesson, apply the
[self-improvement hook](../dev-skills/skills/activated/design-and-refine-skill/SKILL.md#self-improvement-hook)
within the task's write scope.
```

No declaration, or `Self-improvement: disabled.`, leaves automatic refinement off. This is an instruction for the working agent, not a background service.

See [authoring conventions and reference libraries](AGENTS.md), [per-skill research notes](docs/skill-research.md), and the [license](LICENSE).
