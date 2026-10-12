---
name: testing-doctrine
description: Apply interval-appropriate validation during iteration, handoff, staging, and release, using compatible evidence and explicit coverage gaps.
metadata:
  category: passive
---

# Testing doctrine

Match testing to the decision being made. Use the project's runners and acceptance contracts; explicit test prohibitions and budgets take precedence. A skipped gate remains unverified, even when committing or publishing work is authorized.

## Intervals

| Interval | Required approach |
| --- | --- |
| During implementation | Run the smallest meaningful checks for the changed behavior, including a failing reproduction for repairs and the unchanged passing rerun. Use filtered tests and cheap syntax/build checks; expand when failures or uncertain impact warrant it. |
| Task completion or feature handoff | Run the routine gate: current-source build as applicable, ordinary unit/contract suites, and relevant language or configuration checks. Add acceptance scenarios triggered by the changed behavior. A quick filtered pass alone is not a routine-gate pass. |
| Scheduled staging integration | Validate the combined candidate on required platforms. Run routine coverage once, then use a bounded window to rotate complete expensive scenarios: changed behavior or reported defects first, maximum-age breaches next, then oldest-due coverage. Preserve time for rotation and cleanup; record displaced work for the next run. |
| Periodic capacity review | Compare upcoming coverage with available execution time. Set target and maximum evidence ages per scenario/platform using risk and measured cost. If the schedule cannot meet them, surface the conflict; do not silently extend validity. A weekly review is a useful starting cadence. |
| Release-candidate stabilization | Test the production build and packaged artifact, real startup and critical user paths, supported platforms, and every required release obligation. Fix defects and rerun affected checks. Routine success alone cannot certify the candidate. |
| Promotion to main or release | Verify that acceptance evidence covers the exact candidate being promoted. Reconcile intervening changes and revalidate affected obligations. Missing required coverage blocks certification unless the responsible owner explicitly accepts a recorded limitation. |

Task completion on a developer branch, or directly on `main`, uses the handoff interval. A commit or push does not itself require the entire release suite; release promotion does.

## Selection and evidence

- Keep a compact project catalog mapping expensive scenarios to change/symptom triggers, required platforms, target/maximum age, and release obligations. Expensive coverage runs when triggered or due; inexpensive checks remain routine. New tests must belong to a discoverable group.
- Reuse accessible passing evidence only when relevant source inputs, build flags, dependencies, environment, platform, scenario, and checker remain compatible and within maximum age. Record why intervening changes do not invalidate it. A matching commit alone is insufficient. Avoid duplicate execution through nested runners.
- Budget complete scenarios, including setup and cleanup. Use isolated parallel workers for independent checks; serialize shared-resource and timing-sensitive work. Never shorten a scenario or weaken assertions to fit the window.
- Match proof to the claim: use actual entrypoints, rendered behavior, real services or peers, and shipped artifacts where those properties matter. Component tests and simulations establish only what they exercise. Zero matches, skipped bodies, missing capabilities, and a process exit without completion assertions are not passes.
- Preserve first failures and counterevidence. Investigate with focused checks; a passing retry without an explanation does not erase the failure. Track unresolved defects and overdue coverage across intervals.

Read and update [scratch-space](../scratch-space/SKILL.md) with candidate identity, selected/reused/passed/failed/blocked/deferred checks, evidence links, limitations, and next due work. Standalone, use Git-versioned `./agents/scratch/` with an index and goal notes; disposable output belongs in ignored `./agents/tmp/`. Record retained evidence before cleanup. These conventions do not install a scheduler.
