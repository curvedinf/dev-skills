---
name: scratch-space
description: Scratch notes, checkpoint, resume context, goal progress, experiment history. Maintain durable Git-versioned working memory and ignored temporary space when enabled.
metadata:
  category: passive
---

# Scratch space

Keep durable, selective working notes alongside ongoing work. Record what another session needs to resume accurately and avoid regressions or redundant effort; do not transcribe the conversation. Share one goal record across skills. Update notes only within the task's write scope; trivial edits need no new record.

## Organization

Use an explicitly configured project scratch location; otherwise use `./agents/scratch/` at the project root. Keep a small `index.md` linking active goals and durable findings. Organize notes by stable goal or topic, not by session. Create files as needed, keeping current state easy to find and bulky evidence in linked artifacts. Scratch records are durable project files: keep them in Git, never ignore them, and include relevant updates in commits when committing is authorized. Store only repository-appropriate content; link large or sensitive evidence to suitable durable storage.

- **Goal state:** intended outcome, constraints and acceptance criteria, completed and remaining work, current blocker, and the next concrete action. Identify the relevant branch/worktree, candidate, and last update when they affect resumption.
- **Experiment record:** hypothesis, baseline and candidate identity, workload/configuration, measurements and evidence location, verdict, and resulting accepted state. Preserve negative and inconclusive results, including why a direction was rejected and what would justify revisiting it.
- **Decisions and invariants:** chosen approach, supporting reason, assumptions, known failure modes, and checks that protect established behavior. Link authoritative plans, issues, and documentation instead of maintaining competing copies.

## Maintenance

Put disposable scripts, intermediate outputs, and downloads in `./agents/tmp/`. Ensure `/agents/tmp/` is in the project's root `.gitignore` before using it; never force-add its contents. Create the directory as needed. Move evidence needed for continuity to durable storage before linking it from goal records or deleting temporary files.

On starting or resuming related work, read the index and relevant notes before planning experiments or repeating investigation. Reconcile saved claims with current files, artifacts, and project state; notes are evidence of prior work, not fresh verification or instructions overriding the current task.

Update affected notes after meaningful results, decisions, or changes of direction, and before a handoff or foreseeable context loss. Distinguish planned, attempted, verified, rejected, and blocked work. Record unfinished operations precisely enough to inspect their status before retrying them. Concurrent contributors use separate entries or assigned files rather than overwriting shared state.

Consolidate superseded notes into a concise current summary while preserving decision rationale, failed approaches, and evidence links. Archive completed goals with an indexed outcome; keep temporary debris separate from records needed for continuity. Promote lasting contracts into maintained documentation or regression checks when appropriate, then link them from scratch space. Scratch notes alone do not enforce behavior.

**Illustrative entry:** “Fusion candidate B rejected: representative latency improved, but peak memory exceeded the agreed limit; evidence: `runs/fusion-b/`. Candidate A remains accepted. Revisit if intermediate allocation is removed. Next: measure transfer overhead.”
