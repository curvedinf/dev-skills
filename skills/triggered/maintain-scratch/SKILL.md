---
name: maintain-scratch
description: Fresh project session, weekly scratch compaction, archive completed goals. On initial project-context load, compact durable notes if the shared seven-day timer is due.
metadata:
  category: triggered
---

# Maintain scratch space

**Event:** first project-context load after the initial user prompt of a fresh agent session. Check once per project per session, before substantive work; follow-up tasks, rereading instructions, and context-window compaction do not retrigger it.

**Timer:** `maintain-scratch` in `agents/scratch/timers.json`, default `interval_days: 7`. Use the [shared timer contract](../../activated/design-time-triggered-skill/references/timer-contract.md). This trigger is independent of skill self-improvement enablement.

When due:

1. Read the index and goal records. Consolidate superseded entries into current summaries, preserving constraints, accepted state, decision rationale, rejected approaches and revisit criteria, unresolved work, and evidence links.
2. Move completed or superseded detail worth retaining into `archive/`, preserving indexed outcomes and repairing links. Keep active records resumable. Promote lasting contracts to canonical documentation where appropriate; never discard sole copies of needed evidence or sweep unrelated temporary files.
3. Verify the index, links, and retained context, then stamp only this timer's completion. A completed review finding nothing to compact still counts. Include maintenance in the next authorized commit.

Coordinate with active writers. Read-only, interrupted, or unsafe concurrent work leaves the timer unchanged; report the deferral. [scratch-space](../../passive/scratch-space/SKILL.md) governs ordinary note upkeep between passes, which does not reset this timer.

The host must load the startup instruction. No fresh session means no periodic check; this skill does not install a scheduler.
