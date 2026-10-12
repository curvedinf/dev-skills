---
name: refine-skill
description: User corrections, repeated friction, workflow gaps, verified lessons, skill self-improvement. Apply evidence-driven skill maintenance before task completion when project-enabled; explicit refinement requests also apply.
metadata:
  category: passive
---

# Refine a skill

Refine shared procedures from observed evidence, not the agent itself. As a cross-cutting metaskill, always read and consider this guidance regardless of the selected workflow. Notice user corrections, recurring friction, procedural gaps, and verified reusable lessons during work; perform the refinement pass at task end, before the final response, when enabled. No evidence means no edit.

1. **Distill the lesson.** Identify the condition and required behavior; add rationale only where it changes decisions. Capture a reusable convention, not an incident transcript. Skip one-off details and rules already covered.
2. **Patch the owner.** Read the affected skill and replace the passage responsible for the divergence. Preserve prior requirements; avoid recency-driven overcorrection and accumulating exceptions. Consolidate overlapping guidance while preserving resources and callers. Use [design-skill](../../activated/design-skill/SKILL.md) for a genuinely distinct new process; otherwise keep the change local.
3. **Verify and finish.** Keep edits recoverable and within the task's write scope. Check packaging, links, and the affected decision; use behavioral evaluation for consequential uncertainty. For read-only or externally owned skills, report a proposed correction instead. Include edits in the authorized task commit and briefly report the refinement and its evidence; do not add routine no-op reports. This skill may refine itself, but maintenance does not trigger another pass.

Read and update [scratch records](../scratch-space/SKILL.md) in `agents/scratch/` with evidence, the owning skill, and any deferred correction. Keep session history out of runtime instructions.

## Enablement

The consuming project's applicable `AGENTS.md` controls automatic refinement: `Self-improvement: enabled.` enables it; disabled or absent leaves it off. Explicit refinement requests still apply. Installation must not inherit the library's opt-in or expand write scope to global skills.

Beside an enabled declaration, link this skill and include: “Always read and consider refine-skill. At the end of each task, before the final response, apply one evidence-backed refinement pass when self-improvement is enabled.” The host must load that instruction; a passive category or discovery adapter alone does not enforce it. This is an agent-followed completion obligation, not a runtime callback or background service.
