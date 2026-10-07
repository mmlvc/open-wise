# Project learning notes

Maintain only these files under the selected project's .open-wise/. Preserve existing content; do not replace it with a template on resume. If writes fail, report it and continue conversationally.

## profile.md
Keep a compact snapshot:
- Learning mode: active or paused
- Onboarding: complete or incomplete, with unanswered fields
- Project purpose and situation
- Programming and stack familiarity: supplied answer or unspecified
- Learning goal: supplied answer or understanding the project as built (explicit default)
- Frequency: normal; question style: open-ended; implementation: AI writes
- Concepts demonstrated / developing / revisit, backed by reasoning evidence

## progress.md
For each topic distinguish:
- Requirements from user
- Concepts explained by Codex
- Reasoning demonstrated by learner
- Agent-supplied proposals and skipped reasoning
- Pending question: exact question, stage, discussed coding scope and authorization
- Chosen design
- Implementation and actual verification result
Remove resolved pending entries; consolidate repetition. A yes is authorization where applicable, not evidence of understanding.

## project-map.md
Maintain:
- Purpose and requirements
- Components and verified source paths
- Main data flow
- Data ownership, storage and trust boundaries
- Verified build/test commands
- Unknowns
Label each new design item proposed, chosen or implemented; never describe a proposal as existing code.
Recommend excluding .open-wise/ from version control, but edit .gitignore only if requested.

## Reset
On an explicit reset request, back up profile.md, progress.md and project-map.md before rewriting. Use a new timestamped backup directory without overwriting a prior one.
Keep all operations inside the project state directory; never follow symlinks. Do not read old backups to reconstruct reset preferences.

