---
name: polish-docs
description: Polish README, onboarding, quickstart, documentation redesign. Improve first-use structure, persuasive evidence, and visual presentation; documentation-style covers ordinary prose edits.
metadata:
  category: activated
---

# Polish docs

Make the project's value and first-use path clear. Default to the README and directly related getting-started material.

Treat `README.md` as human-facing, marketing-centric documentation: earn adoption through concrete benefits and evidence. Put computer-facing, utility-centric routing and operating instructions in `AGENTS.md`; do not turn it into marketing copy.

For ongoing work, read and update [scratch records](../../passive/scratch-space/SKILL.md) in `agents/scratch/`: audience decisions, claim sources, visual conventions, and remaining onboarding friction.

Use concrete, evidence-driven copy: no hand-waving, empty superlatives, or unsupported claims.

1. Review the current documentation and project. Identify the intended newcomer, the concrete value offered, and onboarding friction.
2. Compare introductions from successful projects with similar audiences. Choose relevant patterns to adapt; [reference examples](references/patterns.md) provide starting points.
3. Identify the product category, what it does, and how the reader uses it before relying on an abstract benefit or slogan. Build the opening around a desirable outcome: a benefit-led headline, a positioning sentence identifying the project and its audience-specific benefit, concrete proof, and one primary next action.
4. Follow the reader's adoption sequence: “Is this for me?” → “Why this?” → “Can I trust it?” → “How do I start?” Use a relevant example or demo as proof, address adoption barriers beside the call to action, then lead through a quickstart to a useful result. Link deeper reference and contributor material afterward.
5. Apply a coherent visual treatment using the conventions below and the existing documentation platform.
6. Walk through the revised experience as a newcomer, checking claims, instructions, and rendered presentation as the task permits. Resolve remaining friction before handing it back.

Use direct, reader-centered voice and the audience's terminology. Put proof beside each benefit; replace evaluative adjectives with observable behavior. Use descriptive benefit or task headings, avoiding generic labels such as “The collection”; and name the primary action by its payoff. Prefer one copyable example with labeled input, output, and substitutions. Keep deeper detail behind descriptive links. Once installation provides a complete first-use path, omit redundant setup walkthroughs. For ongoing prose work, use [documentation-style](../../passive/documentation-style/SKILL.md).

## Visual conventions

Visual polish should make identity, behavior, and evidence easier to recognize and inspect.

- **Opening:** compose a compact wordmark, concrete value proposition, primary action, and real example or product image. Restrained gradients or illustration can establish identity without competing with the content.
- **Visual proof:** use crisp screenshots, annotated diagrams, or short demonstrations of supported behavior. Use consistent framing and evidence-specific captions; do not imply functionality with invented product imagery.
- **Consistency:** use a small palette, one recognizable icon style, and consistent spacing and borders. Keep reading surfaces quiet, with clear hierarchy and accessible contrast; reserve expressive decoration for the opening and transitions.
- **Useful components:** use icon cards for distinct routes, labeled code panels with copy controls where supported, and selective line highlighting. Keep commands and results distinct; use motion only to explain behavior or acknowledge interaction.
- **Trust signals:** place supported versions near installation, methodology beside benchmarks, and release status beside downloads. Link the license, changelog, and relevant limitations. Use a few meaningful badges, not a wall of implied endorsements.

For a GitHub README, favor a compact branded header, one useful visual, clean examples, and deliberate spacing. For a documentation site, add navigation cards, code controls, and theme support where the platform allows. Preserve readable text alternatives and narrow-screen usability.

## Examples

Illustrative opening for a fictional tool; assume the stated capabilities are supported:

> **Find added, removed, and changed records in CSV exports.**
>
> Rowdiff compares recurring data exports by customer ID. Reordering rows does not count as a record change.
>
> **Review record changes**
>
> The report includes changed records and omits unchanged ones. Comparison runs locally; no upload or account required.
>
> **Compare your first exports**
>
> Try the included sample files, then compare your own.

The example immediately following that invitation, after installation:

```sh
rowdiff previous.csv current.csv --key customer_id
```

Example output:

```text
Added: 3 records
Removed: 1 record
Changed: 7 records
```
