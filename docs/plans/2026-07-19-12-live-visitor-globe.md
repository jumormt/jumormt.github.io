# Plan: Restore a Live Visitor Map with a New Widget

**Epic:** E0: Site Maintenance Baseline

## Summary

Use the user-provided MapMyVisitors widget ID to restore live geographic visitor markers in the homepage footer. Present the provider's responsive flat map alongside the archived ClustrMaps image so the historical record remains visibly present instead of appearing only after a widget failure.

**Decisions locked in:**
- Use the validated public widget ID `ba8ZCxZKmuHUCpBMf2Y1mosAeUVIBTMwWYnc3MyshcA` over explicit HTTPS.
- Use the user-supplied `map.js` widget with `w=a`, constrained by a responsive 320px container.
- Remove the live globe layer and custom Canvas animation.
- Preserve the 23 February 2026 archived map as a permanently visible historical record and link.
- Label the live and historical datasets honestly; the new live dataset starts fresh.
- Keep Busuanzi's host-aware raw page-view behavior unchanged.

**Validation history:**
- The first supplied widget ID was rejected because its tracking image reported `Error: Incorrect map code!` and its live callback returned HTML.
- The replacement `map.js` widget ID was validated through its map image and JSONP callback. It also works with `globe.js`, but the final user preference is the flat map.
- The legacy ClustrMaps token was tested against MapMyVisitors and returns `Error: Incorrect map code!`; the providers cannot merge the old and new datasets.

---

## Phase 1: Integrate the Live Map

### [x] Task 1.1: Add the responsive live map
- [x] Replace the uncommitted live globe embed with the supplied MapMyVisitors map embed in `index.html`.
- [x] Constrain the auto-width widget to a clean 320px responsive footprint.
- [x] Use the archived map image as the visual fallback.

### [x] Task 1.2: Simplify the previous globe implementation
- [x] Remove live-globe, historical-globe, and Canvas-specific CSS/JavaScript.
- [x] Label the primary display as a live visitor map.
- [x] Keep a separate link to the dated 23 February 2026 historical visitor map.
- [x] Update visitor-map documentation and the known-issue note.

### [x] Task 1.3: Keep visitor history visible
- [x] Replace the hidden fallback behavior with two clearly labelled map cards.
- [x] Show the archived visitor map through 23 February 2026 beside the live map beginning 19 July 2026.
- [x] Keep both maps responsive and visually restrained on desktop and mobile.

## Phase 2: Verify and Document

### [x] Task 2.1: Verify integration
- [x] Confirm the map endpoint and tracking image are valid for the replacement widget ID.
- [x] Confirm the new widget ID appears once and the old archived token remains only in fallback/history URLs.
- [x] Confirm no globe/Canvas renderer remains.
- [x] Confirm the historical link, Busuanzi behavior, JavaScript syntax, local HTTP response, and `git diff --check` remain valid.
- [x] Confirm both historical and live maps are visible at the same time.

### [x] Task 2.2: Close the LDD session
- [x] Mark plan tasks complete.
- [x] Update `docs/PROGRESS.md` with status, tests, files, next steps, and blockers.

## Verification
- [x] Responsive live and historical maps are both visible.
- [x] New visitor markers come from the validated live dataset.
- [x] Historical visitor data remains visible, accessible, and is not discarded.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
