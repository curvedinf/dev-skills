---
name: design-and-refine-skill
description: Create a skill, refine a skill, consolidate skills, skill self-improvement. Design minimal process instructions; automatic refinement requires project opt-in.
metadata:
  category: activated
---

# Design and refine a skill

Skills normalize different agents' default approaches; they do not improve the agent or teach expertise. Capture the critical conventions needed for a shared outcome and trust the agent to execute.

For ongoing work, read and update [scratch records](../../passive/scratch-space/SKILL.md) in `agents/scratch/`: user corrections, reference findings, design decisions, and validation gaps.

1. Identify the desired outcome and which defaults should converge. Read the existing skill before refining it; extend an existing owner when the purpose matches.
2. Inspect relevant peer skills or exemplary outputs. Extract specific conventions worth adopting, not their entire methodology. [Architecture references](references/architecture.md) provide starting points.
3. Choose passive guidance or an activated workflow. For activated skills, write a short sequence from initial assessment through delivery and verification; continuous workflows instead define the repeat cycle and resumable interruption conditions. A list of principles alone is not a process. For passive skills, state the ongoing convention and its scope.
4. Front-load the description with likely request terms, the outcome, and the nearest routing boundary. Keywords select candidates; user intent determines activation. Keep agent routing in `AGENTS.md` and skill descriptions; reserve the README for human discovery and setup. Give each shared convention one owner and link it only where needed. Specify the important choices and add compact finished examples where they clarify the intended result. Leave execution mechanics to the agent.
5. Cut anything that does not establish a necessary convention. Preserve the process and distinguishing details, then check packaging, references, and any meaningful behavioral uncertainty.

## Writing conventions

- **Minimal, not vague:** replace “use best practices” or “make it polished” with the few concrete choices that define the requested standard. Conciseness must not erase the process.
- **Specific, not prescriptive:** normalize voice, structure, evidence, or decision criteria as relevant. Avoid tutorials, tool-by-tool instructions, arbitrary quotas, and repeated policy.
- **Examples show the target:** use finished examples, not before/after comparisons by default. Demonstrate the distinguishing qualities together; an example of brevity alone does not demonstrate persuasive, evidence-driven writing. Label fictional examples and assumptions.
- **Every sentence costs attention:** remove hand-waving, empty superlatives, speculative exceptions, and redundant explanations. Supporting files must earn their place, not conceal verbosity.
- **Refinement follows evidence:** use user feedback or observed divergence to replace the relevant passage. Preserve previously established requirements rather than overcorrecting toward the latest comment. No evidence means no edit.

Check that representative requests select the intended skill from descriptions alone, especially adjacent skills. Packaging checks do not establish execution behavior; exercise tasks when consequential uncertainty warrants it.

Use `skills/<passive|activated>/<name>/SKILL.md`, with frontmatter `name`, `description`, and `metadata.category`. Keep host-specific invocation settings in adapters.

## Self-improvement hook

When enabled by the host project, a user correction, a discovered procedural gap, or a verified reusable workflow triggers a refinement pass after the current task. Apply this to skills created with this procedure through one host-level instruction, not repeated hooks in every skill. Self-improvement means refining the shared procedure, not improving the agent.

1. Distill the evidence into a reusable convention: condition, action, and a brief reason where needed. Capture lessons, not session logs; skip one-off details and already-covered guidance.
2. Read the current owning skill and patch the relevant step. Prefer an existing owner; create a skill only for a distinct reusable process. Extend topic references in place rather than adding one file per incident.
3. Keep the change recoverable, preserve prior requirements, and check the affected behavior and packaging proportionately. Briefly report the correction and its basis. Respect the task's write scope; for read-only or externally owned skills, return the proposed correction instead.

This pass may refine this skill too. Finish after the evidence-backed correction; do not trigger another pass from the maintenance itself. Consolidation must preserve supporting files and callers. Background scheduling and library-wide archival are separate runtime features, not part of this hook.

Enablement lives in the consuming project's applicable `AGENTS.md`: `Self-improvement: enabled.` enables this hook; `Self-improvement: disabled.` or no declaration leaves automatic refinement off. Link this procedure beside the declaration so agents can load it. Follow the task's instructions and applicable project scope; the skill library's own setting does not enable maintenance in other projects. Explicit skill-authoring requests work regardless of this setting.

This is an instruction followed by the agent, not a background service or runtime callback. No separate configuration file is needed.
