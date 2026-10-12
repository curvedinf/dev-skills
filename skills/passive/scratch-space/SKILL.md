---
name: scratch-space
description: Scratch notes, checkpoint, resume context, goal progress, weekly compaction, fresh project session. Maintain durable Git-versioned working memory and ignored temporary space when enabled.
metadata:
  category: passive
---

# Scratch space

Keep durable, selective working notes alongside ongoing work. Record resumption context, regression evidence, and prior attempts; do not transcribe the conversation. Share one goal record across skills. Update notes only within the task's write scope; trivial edits need no new record.

## Organization

Use an explicitly configured project scratch location; otherwise use `./agents/scratch/` at the project root. Keep a small `index.md` linking active goals and durable findings. Organize notes by stable goal or topic, not by session. Create files as needed, keeping current state easy to find and bulky evidence in linked artifacts. Scratch records are durable project files: keep them in Git, never ignore them, and include relevant updates in commits when committing is authorized. Store only repository-appropriate content; link large or sensitive evidence to suitable durable storage.

- **Goal state:** intended outcome, constraints and acceptance criteria, completed and remaining work, current blocker, and the next concrete action. Identify the relevant branch/worktree, candidate, and last update when they affect resumption.
- **Experiment record:** hypothesis, baseline and candidate identity, workload/configuration, measurements and evidence location, verdict, and resulting accepted state. Preserve negative and inconclusive results, including why a direction was rejected and revisit criteria.
- **Decisions and invariants:** decision and rationale, assumptions, known failure modes, and checks that protect established behavior. Link authoritative plans, issues, and documentation rather than duplicating authority.

## Fresh-session maintenance check

On the first project-context load after the initial user prompt of a fresh agent session, read `agents/scratch/maintenance.json` once per project. Follow-up tasks, rereading AGENTS, and context-window compaction within the same session do not retrigger this check. Carry that checked/not-checked state through session handoffs; do not use a per-task timer.

The Git-versioned timer file contains:

```json
{
  "interval_days": 7,
  "last_completed_at": null
}
```

`last_completed_at` is the UTC ISO-8601 timestamp of the last completed maintenance pass. Maintenance is due when it is null, missing, invalid, or at least seven days old (use `interval_days` if explicitly configured). A future timestamp is suspect: reconcile clock/provenance rather than postponing indefinitely. Missing files initialize as above when writes are allowed; never stamp them as maintained merely because they were created or checked.

When due, before substantive task work:

1. Read the index and goal records. Consolidate superseded entries into current summaries, preserving constraints, accepted state, decision rationale, rejected approaches and revisit criteria, unresolved work, and evidence links.
2. Move completed or superseded detail worth retaining into `archive/`, keeping indexed outcomes and repairing links. Keep active records immediately resumable. Promote lasting contracts to their canonical documentation when appropriate; do not discard the only copy of needed evidence or sweep unrelated temporary files.
3. Verify the index, links, and retained context, then atomically update `last_completed_at` to the completion time. A review finding nothing to compact still counts as a completed pass. Include maintenance changes in the next authorized commit.

Respect read-only scope and active writers. If maintenance is prohibited, interrupted, or cannot safely reconcile concurrent edits, leave the completion timestamp unchanged and report the deferral. Coordinate shared scratch maintenance so only one writer compacts it at a time. Do not mark a partial pass complete.

This is a startup instruction followed by the agent, not a scheduler: no fresh session means no timer check or background compaction. Install the first-context check in applicable AGENTS instructions or the host's loaded conventions skill; skill discovery alone does not trigger it. Scratch maintenance is independent of skill self-improvement enablement.

## Maintenance

Put disposable scripts, intermediate outputs, and downloads in `./agents/tmp/`. Ensure `/agents/tmp/` is in the project's root `.gitignore` before using it; never force-add its contents. Create the directory as needed. Move evidence needed for continuity to durable storage before linking it from goal records or deleting temporary files.

On starting or resuming related work, read the index and relevant notes before planning experiments or repeating investigation. Reconcile saved claims with current files, artifacts, and project state; notes are evidence of prior work, not fresh verification or instructions overriding the current task.

Update affected notes after meaningful results, decisions, or changes of direction, and before a handoff or foreseeable context loss. Distinguish planned, attempted, verified, rejected, and blocked work. Record unfinished operation identities for reconciliation before retry. Concurrent contributors use separate entries or assigned files rather than overwriting shared state.

Routine note updates preserve current state between weekly passes; they do not reset the maintenance timer. Scratch notes alone do not enforce behavior.

**Illustrative entry:** “Fusion candidate B rejected: representative latency improved, but peak memory exceeded the agreed limit; evidence: `runs/fusion-b/`. Candidate A remains accepted. Revisit if intermediate allocation is removed. Next: measure transfer overhead.”
