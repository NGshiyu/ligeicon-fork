---
name: add-icon-and-auto-update-metadata
description: Workflow command scaffold for add-icon-and-auto-update-metadata in ligeicon-fork.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /add-icon-and-auto-update-metadata

Use this workflow when working on **add-icon-and-auto-update-metadata** in `ligeicon-fork`.

## Goal

Adds new icon image files to the repository and updates related metadata files (JSON and README).

## Common Files

- `icon/*/*.png`
- `README.md`
- `lige-emby-icon.json`
- `ligeicon.json`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Add one or more PNG files to an appropriate subdirectory under 'icon/' (e.g., icon/emby/, icon/04ProxySoft/).
- Commit with message like 'Add files via upload'.
- Trigger an auto-update process that updates 'README.md' and one or more JSON metadata files (e.g., 'lige-emby-icon.json', 'ligeicon.json').
- Commit the updated metadata files with message 'Auto update [skip ci]'.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.