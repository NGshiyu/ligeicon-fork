---
name: update-rule-list
description: Workflow command scaffold for update-rule-list in ligeicon-fork.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-rule-list

Use this workflow when working on **update-rule-list** in `ligeicon-fork`.

## Goal

Updates a rule list file (such as proxylist or openai list) in the 'rule/' directory.

## Common Files

- `rule/proxylist.list`
- `rule/openai.list`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit the relevant list file in 'rule/' (e.g., 'proxylist.list', 'openai.list').
- Commit the change with a message like 'Update proxylist.list' or 'Update openai.list'.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.