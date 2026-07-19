# Plan: Add the Supervision Section

**Epic:** E0: Site Maintenance Baseline

## Summary

Add a dedicated Supervision section to the homepage and sidebar navigation. Present the user-supplied students in distinct Current and Previous groups while preserving the existing alternating section backgrounds.

**Decisions locked in:**
- Use the supplied names, degrees, institutions, and current-position note as written.
- Place Supervision between Teaching Experience and Tools.
- Use a white section so the existing white/grey alternation continues.

---

## Phase 1: Add Content and Navigation

### [x] Task 1.1: Add the navigation entry
- [x] Add a `#supervision` sidebar link after Teaching.
- [x] Confirm the link targets a unique section anchor.

### [x] Task 1.2: Add the supervision lists
- [x] Add all 11 current students under `Current`.
- [x] Add all 5 former students under `Previous`.
- [x] Preserve the supplied degree and institution labels.

## Phase 2: Verify and Document

### [x] Task 2.1: Verify content
- [x] Confirm all 16 names appear exactly once in the Supervision section.
- [x] Confirm group counts, anchor, ordering, and alternating backgrounds.
- [x] Run JavaScript syntax validation and `git diff --check`.

### [x] Task 2.2: Close the LDD session
- [x] Mark plan tasks complete.
- [x] Update `docs/PROGRESS.md` with status, tests, files, next steps, and blockers.

## Verification
- [x] Sidebar contains a working Supervision anchor.
- [x] Current contains 11 entries and Previous contains 5 entries.
- [x] No supplied supervision detail is omitted.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
