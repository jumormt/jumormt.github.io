# Plan: Repair and Refresh the Visitor Map Footer

**Epic:** E0: Site Maintenance Baseline

## Summary

Repair the broken ClustrMaps visitor map at the bottom of the homepage and present the visitor statistics in a cleaner, responsive footer card. Preserve the existing ClustrMaps data identity so the historical visitor dataset continues rather than starting over.

**Decisions locked in:**
- Keep the existing ClustrMaps data token `HA1rasF4Ps-g80mwIHPsyroDFlKH7oDfpAJDT-R0J8U` unchanged.
- Use explicit HTTPS URLs so the widget works on GitHub Pages and when `index.html` is opened directly.
- Keep the existing Busuanzi page-view counter and its historical offset behavior.

---

## Phase 1: Diagnose and Preserve State

### [x] Task 1.1: Inspect the existing footer integration
- [x] Locate the visitor-map and page-view integrations in `index.html`.
- [x] Confirm the legacy protocol-relative image endpoint and record the existing data token.

### [x] Task 1.2: Identify a compatible replacement
- [x] Check the current ClustrMaps embed pattern.
- [x] Select the dynamic HTTPS widget while retaining the original data token.

## Phase 2: Implement the Footer Refresh

### [x] Task 2.1: Replace the broken map embed
- [x] In `index.html`, replace the legacy static image with the current dynamic widget.
- [x] Add accessible loading/failure messaging and a dated archived snapshot without substituting or resetting visitor data.

### [x] Task 2.2: Improve presentation
- [x] Add scoped responsive styles for a compact visitor card and footer metadata.
- [x] Keep the layout legible on desktop and mobile without adding new dependencies.

## Phase 3: Verification and Documentation

### [x] Task 3.1: Verify the implementation
- [x] Confirm the live widget and archived snapshot use the same original ClustrMaps data token.
- [x] Confirm explicit HTTPS is used for both visitor-statistics services.
- [x] Inspect the rendered homepage at desktop and mobile widths where browser tooling permits.
- [x] Run HTML parsing checks and `git diff --check`.

### [x] Task 3.2: Close the LDD session
- [x] Mark completed plan tasks and record any third-party availability limitation.
- [x] Update `docs/PROGRESS.md` with status, verification, changed files, next steps, and blockers.

## Verification
- [x] Existing visitor-map data token is unchanged across the live widget and preserved snapshot.
- [x] Existing Busuanzi counter markup and offset are preserved.
- [x] Footer remains usable when the third-party map service is temporarily unavailable.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.

## Notes

- ClustrMaps was not accepting HTTPS connections during verification. The live loader is non-blocking and retains the original token; the 23 February 2026 Wayback snapshot remains visible until the live widget renders.
- Busuanzi and the archived map both returned HTTP 200. JavaScript syntax and diff checks passed. The installed Snap Firefox failed to capture even `about:blank`, so no automated browser screenshots were available.
