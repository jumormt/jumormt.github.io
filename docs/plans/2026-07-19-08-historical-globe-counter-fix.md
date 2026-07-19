# Plan: Restore the Historical Globe and Correct Visitor Counts

**Epic:** E0: Site Maintenance Baseline

## Summary

Replace the nonfunctional ClustrMaps live globe with an animated globe derived from the site's preserved visitor-map snapshot, and stop displaying misleading local/offset visit counts. Keep the historical visitor dots accessible while clearly distinguishing archived geography from the live production page-view count.

**Decisions locked in:**
- Treat ClustrMaps as unavailable: its HTTPS service refuses connections and HTTP serves a domain-parking page.
- Animate the preserved 23 February 2026 same-token map as a compact CSS globe; do not label archived geography as live.
- Continue linking the full preserved snapshot.
- Load Busuanzi only on non-local hosts and display its unmodified `site_pv` value.
- Remove the artificial `+20000` offset because the deployed page's missing jQuery meant it never affected the visible count.
- On localhost or direct-file previews, show an explanatory note instead of Busuanzi's shared localhost count.

---

## Phase 1: Repair Visitor Presentation

### [x] Task 1.1: Replace the dead live widget
- [x] Remove the `globe.js` loader and widget host from `index.html`.
- [x] Use the verified archived map image as a repeating animated globe texture.
- [x] Retain accessible full-snapshot navigation and clearly date the globe.

### [x] Task 1.2: Correct page-view counting
- [x] Remove the unconditional Busuanzi script and `+20000` adjustment.
- [x] Load Busuanzi dynamically only on published hosts.
- [x] Show a nonnumeric preview note on localhost and `file:` URLs.

## Phase 2: Verify and Document

### [x] Task 2.1: Verify behavior and data honesty
- [x] Confirm the globe uses the preserved map URL and no dead ClustrMaps JavaScript remains.
- [x] Confirm local preview does not expose the shared localhost count.
- [x] Confirm the production Busuanzi endpoint returns a plausible raw value for `jumormt.github.io`.
- [x] Confirm local preview, JavaScript syntax, and `git diff --check` pass.

### [x] Task 2.2: Close the LDD session
- [x] Mark plan tasks complete.
- [x] Update `docs/PROGRESS.md` with status, tests, files, next steps, and blockers.

## Verification
- [x] Historical globe visibly rotates and links to the full preserved snapshot.
- [x] Visitor geography is labeled with its 23 February 2026 snapshot date.
- [x] Local preview displays no misleading numeric count.
- [x] Published hosts use raw Busuanzi `site_pv` without an artificial offset.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
