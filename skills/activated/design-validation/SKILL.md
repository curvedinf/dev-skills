---
name: design-validation
description: Design or revise validation for a change, user journey, or test suite when requested; execute the resulting checks when included in scope.
metadata:
  category: activated
---

# Design validation

Choose checks by the behavior they establish, not by test count or coverage percentage.

Use [testing-doctrine](../../passive/testing-doctrine/SKILL.md) when available to assign checks to iteration, handoff, staging rotation, or release obligations. Otherwise use the project's interval and evidence-reuse rules.

Consult project scratch space for existing evidence and coverage gaps; retain the claim-to-check mapping, candidate-specific results, and outstanding obligations there. Follow [scratch-space](../../passive/scratch-space/SKILL.md) when available; otherwise use `./agents/scratch/` with a small index and goal-specific notes.

1. Identify the acceptance claims, consequential failure modes, and existing evidence. Account for the requested test budget and project gates.
2. Map each claim to the smallest adequate check. Reuse existing tests and fixtures where suitable; include actual entrypoints, adverse conditions, and lifecycle boundaries when those are part of the claim.
3. Separate component proof from real integration and user-experience proof. Simulators can isolate a mechanism; they cannot establish unmodeled network, hardware, rendering, or external-service behavior.
4. Execute when authorized, retaining results and relevant candidate/configuration identity. A plan-only request produces the proposed checks and unresolved obligations instead.
5. Report which claims passed, failed, remain untested, or rely on substitute evidence. Repeat checks when a change invalidates them, not merely because another wrapper can run them again.

When reducing a suite, map each retired obligation to a demonstrated replacement or retained check. Preserve defect detection and fresh-state coverage; fewer test names alone are not savings. Skipped or empty selections are not passes.

Illustrative mapping: “Duplicate prevention: replay the same request in a component fixture. Interrupted delivery: exercise the production entrypoint with acknowledgment loss. Neither check establishes visual status accuracy.”
