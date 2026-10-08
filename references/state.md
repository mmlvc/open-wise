# Project learning notes and templates

Keep these three notes under the selected project's `.open-wise/`, using the directory selected by SKILL.md. Create missing files from the templates and actual evidence; preserve existing content on resume. Fill bracketed fields with known facts or “Not specified,” in the learner's language. The status values active/paused and complete/incomplete remain explicit. Do not copy sample decisions into a real project's history. If writes fail, report it and continue conversationally.

## profile.md

Maintain a compact current snapshot. Update preferences and understanding in place; put learning-event history in progress.md. Mark onboarding complete when needed setup is answered or explicitly skipped; list unanswered setup only while incomplete. Defaults are normal frequency, open-ended questions, AI-written code and understanding the project as built, unless the user specified otherwise. Experience is self-reported, not evidence of understanding.

```markdown
# Learner profile

Learning mode: active
Onboarding: incomplete

## Project
Purpose: [Project purpose or Not specified]
Situation: [New / Existing / Known / Not specified]
Codebase familiarity: [Supplied answer or Not specified]
Learning scope: [Supplied answer or Not specified]

## Experience
Programming: [Supplied answer or Not specified]
Stack familiarity: [Per-technology answers or Not specified]

## Learning goal
[Supplied goal, or understanding the project as built — default]

## Preferences
Checkpoint frequency: normal
Question style: open-ended
Implementation: AI writes code

## Remaining onboarding
[Needed unanswered setup; remove this section when complete]

## Demonstrated concepts
No reasoning evidence recorded yet.

## Developing concepts
None recorded yet.

## Revisit
None recorded yet.
```

## progress.md

Start with an empty history:

```markdown
# Learning progress

No learning events recorded yet.
```

As topics arise, use the following structure where relevant. Keep topics independently readable and consolidate repetition. Record reasoning evidence rather than whole exchanges. A yes may authorize the presented scope; it is not evidence of understanding. Remove the empty-history sentence after the first event.

```markdown
## [Topic name]

Requirements: [User's requested behavior and constraints]
Explained by Codex: [Concepts taught, or none]
Learner reasoning: [Observed reasoning, or none recorded]
Codex proposals / skipped reasoning: [Agent-supplied choices, or none]
Chosen design: [Only confirmed choices, or undecided]
Implementation: [Actual source paths and changes, or not implemented]
Verification: [Checks actually run and results, or not run]
Needs reinforcement: [Evidence-based gaps, or none recorded]
```

Before waiting at a checkpoint, save a short pending section. Include its decision name and stage so another chat can resume at the same point. Use stages awaiting reasoning, awaiting design confirmation or awaiting implementation authorization. Keep proposals separate from confirmed choices, and record any existing authorization for the exact scope. If the coding scope is unknown, say undecided rather than inventing it.

```markdown
## Pending decision: [Decision name]

Checkpoint: [Build / Design / Implementation]
Stage: [Awaiting reasoning / Awaiting design confirmation / Awaiting implementation authorization]
Question / awaited reply: [Exact question or the confirmation being awaited]
Learner's confirmed choices: [Only actual choices, or none]
Codex proposals: [Unconfirmed suggestions, or none]
Coding scope: [Presented scope, or undecided]
Authorization: [Existing instruction covering that scope, or not yet given]
```

Refresh the pending section during discussion. Once resolved, move the actual decision and evidence into its topic and the project map, then remove the pending section. Confirming a design does not mark it implemented. Do not add unmentioned fields, behaviors, rationale or rejected alternatives to the chosen design.

## project-map.md

Reflect the learner's model refined together or verified existing code. Keep source paths and build/test commands evidence-based. Label design items proposed, chosen or implemented. Unknown relationships stay unknown; a system diagram must not silently fill in a design.

```markdown
# Project map

## Purpose
[What this software does]

## Requirements
[User needs and constraints; these do not automatically settle technical choices]

## Components
[Responsibilities and verified source paths; label proposed, chosen or implemented]

## Main flow
[Concrete user action → components → data / storage; label links and mark unknowns]

## Data and trust boundaries
[Ownership, storage, access rules and external services; unknown when unverified]

## Build and verification
[Commands and supporting configuration paths verified in the repository]

## Unknowns
[Unresolved choices and what needs inspection]
```

Tell the learner where the notes are saved when first creating them. Update pending decisions before waiting, chosen designs after confirmation, and implementation/verification after coding. A System check uses and refreshes the project map. Mention note paths when showing progress or when useful to inspect the recorded decision. Recommend excluding `.open-wise/` from version control, but edit .gitignore only if requested.

## Reset

On an explicit reset request, back up profile.md, progress.md and project-map.md before rewriting. Use a new timestamped directory under `.open-wise/backups/` without overwriting a prior backup. Keep operations inside the project state directory; never follow symlinks. Do not read old backups to reconstruct reset preferences.
