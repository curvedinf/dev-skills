---
name: documentation-style
description: Documentation, prose, wording, terminology, examples. Apply concise evidence-driven writing conventions when enabled; use polish-docs for an onboarding redesign.
metadata:
  category: passive
---

# Documentation style

Apply these defaults to the documentation being written or edited. Preserve page purpose and canonical terminology.

`README.md` serves humans: make it marketing-centric, leading with concrete value, credible proof, and a clear next action. `AGENTS.md` serves computers: make it utility-centric, prioritizing precise instructions, routing, constraints, and decision rules. Keep promotional prose out of AGENTS and agent operating procedures out of the README; neither audience benefits from unsupported claims.

For ongoing work, read and update [scratch records](../scratch-space/SKILL.md) in `agents/scratch/`: terminology, voice decisions, claim sources, and open questions.

- Lead with what the reader needs to understand or accomplish. Use direct address and active verbs; put prerequisites before actions and recognizable results after them.
- Give each page a clear job. Tutorials teach through a result, how-to guides support a task, references specify behavior, and explanations develop understanding. Cross-link these page types; avoid mixing their purposes.
- State concrete capabilities and limits. No hand-waving, empty superlatives, exaggerated benefits, or unsupported claims of ease. Label illustrative data and distinguish roadmap from shipped behavior.
- Use descriptive sentence-case headings, short connected paragraphs, numbered sequences, and bullets for parallel choices. Use consistent names and units.
- Make examples usable: label code blocks, distinguish input from output, and explain substitutions. Use descriptive links to canonical detail rather than duplicating it.

Illustrative copy: “Export records as CSV. The export includes the active filters and excludes archived records.” A task heading could be “Export filtered records.”

Apply conventions locally; a local edit does not authorize a documentation overhaul.
