# Plan: Make Supervision Collapsible

**Epic:** E0: Site Maintenance Baseline

## Summary

Make the Current and Alumni supervision groups independently collapsible so the homepage remains compact while keeping every student entry accessible.

**Decisions locked in:**
- Use native HTML `<details>` and `<summary>` controls for accessible, dependency-free behavior.
- Show entry counts in both group labels.
- Keep Current expanded by default and Alumni collapsed by default.

---

## Phase 1: Add Collapsible Groups

### [x] Task 1.1: Add disclosure markup
- [x] In `index.html`, wrap the Current list in an open disclosure labelled `Current (13)`.
- [x] Wrap the Alumni list in a closed disclosure labelled `Alumni (6)`.

### [x] Task 1.2: Style the controls
- [x] Add compact summary and disclosure spacing consistent with the existing site typography.
- [x] Keep the controls keyboard-accessible and understandable without JavaScript.

## Phase 2: Verify and Document

### [x] Task 2.1: Verify behavior and content
- [x] Confirm both groups use valid native disclosure markup with the intended default states.
- [x] Confirm Current and Alumni retain 13 and 6 entries respectively.
- [x] Check inline JavaScript syntax and `git diff --check`.

### [x] Task 2.2: Close the LDD session
- [x] Mark tasks complete and update `docs/PROGRESS.md` with results.

## Verification
- [x] Current is expanded by default and Alumni is collapsed by default.
- [x] Both groups can be toggled without JavaScript.
- [x] All student entries and ordering are preserved.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
