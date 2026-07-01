---
name: update-documentation-and-integrations
description: Workflow command scaffold for update-documentation-and-integrations in community.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-documentation-and-integrations

Use this workflow when working on **update-documentation-and-integrations** in `community`.

## Goal

Updates documentation and the integrations registry, typically to add or clarify features or connectors.

## Common Files

- `README.md`
- `integrations.json`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit README.md to add or clarify documentation.
- Update integrations.json to reflect the new or changed integration.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.