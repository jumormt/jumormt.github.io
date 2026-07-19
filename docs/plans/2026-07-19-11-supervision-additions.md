# Plan: Add Two Supervision Records

**Epic:** E0: Site Maintenance Baseline

## Summary

Extend the homepage Supervision section with one current summer research student and one undergraduate alumnus who is now pursuing a PhD at Monash University.

**Decisions locked in:**
- Add Thanakit Rattikanchalakorn to `Current` as a Summer Research Student.
- Add Jianing Wang to `Alumni` as an Undergraduate student, now PhD at Monash.
- Preserve the existing section structure, ordering style, and typography.

## Tasks

### [x] Task 1: Update Supervision content
- [x] Add both names and their supplied status details to the correct groups.
- [x] Keep the existing HTML structure and alternating section backgrounds unchanged.

### [x] Task 2: Verify and document
- [x] Confirm each new name appears exactly once in Supervision.
- [x] Confirm Current contains 12 entries and Alumni contains 6 entries.
- [x] Run local preview, JavaScript syntax, and `git diff --check` validation.
- [x] Update this plan and `docs/PROGRESS.md` with the result.

## Verification
- [x] Both additions are visible under the intended headings.
- [x] Existing supervision records remain unchanged.
- [x] `git diff --check` passes.
