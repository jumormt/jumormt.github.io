# Plan: Remove the False Live Visitor Marker

**Epic:** E0: Site Maintenance Baseline

## Summary

Correct the merged visitor map so MapMyVisitors' fixed `unknown location` placeholder is not presented as a real-time visitor in North America. Keep polling for genuinely geolocated visits, but describe the third-party data as recently recorded locations rather than current online visitors.

**Decisions locked in:**
- Preserve the archived historical map and existing MapMyVisitors dataset.
- Reject provider markers explicitly labelled `unknown location` instead of filtering by coordinates alone.
- Keep periodic refresh for valid new coordinates and retain graceful failure behavior.

---

## Phase 1: Correct Marker Semantics

### [x] Task 1.1: Filter provider placeholders
- [x] In `index.html`, parse complete marker objects so their provider labels remain available.
- [x] Exclude markers whose label identifies them as an unknown location.

### [x] Task 1.2: Make the status and legend accurate
- [x] Replace the misleading `Live` legend with wording for provider-recorded, geolocated visits.
- [x] Show a clear no-geolocated-visits state when the provider only returns placeholders.
- [x] Continue refreshing without presenting a provider placeholder as a real visitor.

## Phase 2: Verify and Document

### [x] Task 2.1: Verify the correction
- [x] Test the parser against the current provider payload containing `{latLng: [28, -68], name: "12 visits from unknown location"}`.
- [x] Test valid-coordinate rendering and no-location behavior in a DOM simulation.
- [x] Check inline JavaScript syntax, local HTTP response, and `git diff --check`.

### [x] Task 2.2: Close the LDD session
- [x] Mark plan tasks complete and update `docs/PROGRESS.md` with outcome, verification, files, and blockers.

## Verification
- [x] The `[28, -68]` unknown-location placeholder is not rendered.
- [x] Valid geolocated markers still render and refresh.
- [x] The page no longer implies that accumulated provider markers are currently online.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
