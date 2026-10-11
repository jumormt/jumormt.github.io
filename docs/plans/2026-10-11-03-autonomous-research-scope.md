# Plan: Broaden the autonomous-systems research topics

**Epic:** E0: Site Maintenance Baseline

## Scope

- Remove the opening Research Directions summary sentence as requested.
- Retain the heading “Verification and Safety of Autonomous Systems” and the existing system-level verification topic.
- Broaden C15's topic to “Safety testing of autonomous systems”.
- Broaden C20's topic to “Neuro-symbolic reasoning for autonomous systems”, removing the specific UAV landing-site task and project name from this overview.
- Retain both paper references and their targets; preserve the biography, other research groups, and publication lists.

## Tasks

- [x] Review current content and the preceding research plan.
- [x] Remove the summary and broaden the two topic labels.
- [x] Inspect the scoped diff and verify retained links.
- [x] Record completion and verification in PROGRESS.md.

## Verification

- Manual diff review and exact comparison confirm only the introductory sentence and two topic labels changed.
- All links remain unchanged; the C15 PDF and C20 anchor exist.
- `git diff --check` passed. No browser visual inspection performed.
- User approved the revision and authorized commit and push to `main`.
