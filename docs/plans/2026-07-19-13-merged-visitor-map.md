# Plan: Merge Historical and Live Visitors into One Map

**Epic:** E0: Site Maintenance Baseline

## Summary

Replace the awkward two-map footer with one layered visitor map. Keep the archived ClustrMaps image as the historical base and draw current MapMyVisitors coordinates as green markers over it, while preserving honest date and data-source labeling.

**Decisions locked in:**
- This is a presentation-layer merge because the retired ClustrMaps dataset cannot be imported into MapMyVisitors.
- Preserve the archived red/yellow historical dots through 23 February 2026.
- Read live coordinates from the public MapMyVisitors JSONP callbacks and render them locally as green markers.
- Keep the archived image visible when JavaScript or the live provider is unavailable.
- Retain the existing host-aware Busuanzi total count unchanged.

---

## Phase 1: Build the Unified Map

### [x] Task 1.1: Replace the two-card layout
- [x] In `index.html`, replace the historical/live grid with one responsive map surface.
- [x] Add a compact historical/live marker legend and truthful date-range text.

### [x] Task 1.2: Overlay live coordinates
- [x] Register the MapMyVisitors widget through its public bootstrap callback.
- [x] Request the provider's public map JSONP data and parse its `latLng` marker coordinates without evaluating returned code.
- [x] Project coordinates onto the archived world-map image and refresh the live layer periodically.
- [x] Fail gracefully with the historical map still visible.

## Phase 2: Verify and Document

### [x] Task 2.1: Verify integration
- [x] Confirm the provider bootstrap and marker endpoints return valid callbacks and coordinates.
- [x] Confirm only one visible map exists and the archived map remains the base layer.
- [x] Confirm inline JavaScript syntax, local HTTP response, responsive CSS, and `git diff --check`.

### [x] Task 2.2: Close the LDD session
- [x] Update this plan, `docs/PROGRESS.md`, and the visitor-map summary with final behavior and limitations.

## Verification
- [x] One combined visitor map is displayed.
- [x] Historical visitor dots remain visible.
- [x] Live positions render as a distinct green layer.
- [x] Provider failures do not remove the historical map.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
