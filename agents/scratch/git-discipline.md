# Git discipline

Created 2026-10-12 as passive guidance. Basis: user preferences recorded from prior merge and publication tasks, plus the current durable-scratch convention.

Key distinction: scoped editing preserves unrelated state; an unqualified “push your changes” includes the complete pending tree, subject to explicit exclusions. Preserve protected files byte-for-byte, avoid broad stashes, verify the remote ref, and distinguish publication from validation.

Reference inspected: Superpowers `finishing-a-development-branch`; retained state inspection and work preservation, omitted mandatory menus, broad test gates, and automatic cleanup. Actual branch names remain project-specific.

Validation: skill packaging, adapter metadata, catalog entry, local links, and whitespace checks. No commit, merge, or push was performed to test the instructions.

Branch model added from explicit user guidance: developer-owned features → persistent developer branches → regularly integrated staging → stabilized release candidate → main. Added stable source identities for automation, frozen candidate scope, exact-candidate promotion, and fix propagation. Reference: https://git-scm.com/docs/gitworkflows (topic ownership, published ancestry, and controlled propagation); its branch hierarchy is not substituted for the user’s model. No automation or branch changes were performed.

Task-completion defaults: direct work on main receives a local task-scoped commit; pushing main requires an explicit request. Work on persistent developer branches receives a task-scoped commit and push without renewed permission. Explicit broad push requests retain their complete-pending-tree meaning. Empty commits and implicit feature merges or release promotions are excluded.
