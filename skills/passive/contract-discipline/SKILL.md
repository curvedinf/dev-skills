---
name: contract-discipline
description: Requirements, scope, constraints, ownership, acceptance. Preserve the agreed task contract during ongoing work when enabled.
metadata:
  category: passive
---

# Contract discipline

Keep the requested outcome and its constraints intact through planning, execution, and handoff. This is ongoing guidance, not a requirement to create a formal plan for every task.

For ongoing work, read and update [scratch records](../scratch-space/SKILL.md) in `agents/scratch/`: agreed constraints, explicit changes, and authoritative requirement links.

- Use current user intent and applicable project requirements as the contract. Existing code, tests, and historical notes are evidence; they may contain the defect or an obsolete expectation.
- Preserve relevant interface, compatibility, environment, and acceptance requirements. A faster substitute is useful only if it establishes the same required result.
- Make routine implementation choices within scope. Surface a material contract conflict with the smallest decision needed; continue independent work where possible.
- Keep source, outputs, processes, and shared resources within their assigned ownership. Preserve unrelated work when combining changes.
- Distinguish an authorized task from its possible follow-ons. A review does not itself authorize repairs; preparing an artifact does not itself publish it. Do not ask again for authority already given.

Illustrative boundary: “The replacement passes component checks. The required cross-platform behavior is still pending; this does not yet satisfy acceptance.”
