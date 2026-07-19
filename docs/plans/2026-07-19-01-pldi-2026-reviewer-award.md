# Plan: Add PLDI 2026 Reviewer Award to Homepage

**Epic:** E0: Site Maintenance Baseline

## Summary

Add the PLDI 2026 Distinguished Artifact Evaluation Reviewer Award to the homepage, with the announcement primarily shown in News. Synchronize the existing Grants & Awards entry so the award has one accurate name throughout the page.

**Decisions locked in:**
- Follow the News section's `MM/YYYY` date convention, with explicitly pinned items ahead of the remaining newest-first entries.
- Link the award text to the official PLDI 2026 research artifacts page.
- Preserve unrelated working-tree changes.

---

## Phase 1: Homepage Content Update

### [x] Task 1.1: Add the News announcement
- [x] In `index.html`, add a `06/2026` News item after the explicitly pinned entries.
- [x] Use `images/new.gif` and link the award name to the official PLDI 2026 award listing.

### [x] Task 1.2: Synchronize the Awards entry
- [x] In `index.html`, replace the inaccurate 2026 PLDI award wording with the official award name and link.

### [x] Task 1.3: Unpin the ICSE 2027 News item
- [x] In `index.html`, remove the pushpin marker from the existing `03/2026` ICSE 2027 service announcement while retaining the item and its `new.gif` marker.

### [x] Task 1.4: Add and pin the SIGSOFT school funding announcement
- [x] In `index.html`, add the `05/2026` proposal funding announcement as the first News item with a pushpin marker.
- [x] Link to the official ACM SIGSOFT list of funded 2026–2027 summer/winter schools.

## Phase 2: Verification and Documentation

### [x] Task 2.1: Verify the content
- [x] Confirm pinned News items appear first and the remaining entries stay newest-first.
- [x] Confirm only the ICSE 2027 item loses its pushpin marker.
- [x] Confirm the official PLDI link and award wording are consistent in both locations.
- [x] Inspect the diff for unintended changes.

### [x] Task 2.2: Complete LDD records
- [x] Mark plan tasks complete.
- [x] Update `docs/PROGRESS.md` with status, verification, changed files, next steps, and blockers.

## Verification

- [x] Relevant HTML structure and link targets inspected manually.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` updated with results.
