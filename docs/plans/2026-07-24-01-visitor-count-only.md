# Plan: Show Visitor Count Only

**Epic:** E0: Site Maintenance Baseline

## Summary

Hide the unreliable visitor map and keep the footer focused on the total visit count. Preserve the map markup and integration code as comments so the history remains recoverable, while ensuring no map image or MapMyVisitors request runs on the page.

**Decisions locked in:**
- Keep the existing host-aware Busuanzi visit counter unchanged.
- Comment out, rather than delete, the visitor-map markup and JavaScript.
- Leave the map invisible and stop all MapMyVisitors network activity.

---

## Phase 1: Disable the Map

### [x] Task 1.1: Comment out the visible map
- [x] In `index.html`, comment out the map heading, archived image, legend, and map status.
- [x] Keep the visit counter as the only visitor element in the footer.

### [x] Task 1.2: Disable map requests
- [x] Comment out the merged-map JavaScript integration in `index.html`.
- [x] Confirm the Busuanzi counter still loads on the published host and retains its local-preview message.

## Phase 2: Verify and Document

### [x] Task 2.1: Verify the simplified footer
- [x] Confirm no active map image, map status, MapMyVisitors URL, callback, or refresh timer remains.
- [x] Confirm the inline JavaScript parses, the homepage serves locally, and `git diff --check` passes.

### [x] Task 2.2: Close the LDD session
- [x] Mark this plan complete and update `docs/PROGRESS.md` with results, files, tests, and blockers.

## Verification
- [x] Only the visit count is visible in the visitor footer.
- [x] MapMyVisitors is not requested.
- [x] Local preview behavior remains accurate.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
