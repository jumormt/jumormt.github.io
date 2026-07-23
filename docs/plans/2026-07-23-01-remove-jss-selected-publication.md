# Plan: Remove JSS Paper from Selected Publications

**Epic:** E0: Site Maintenance Baseline

## Summary

Remove the Jiahao Zhang-led JSS 2026 paper `[J5]` from the homepage Selected Publications list while preserving its full-list record and supporting metadata.

**Decisions locked in:**
- Remove `[J5]` only from Selected Publications in `index.html`.
- Keep `[J5]` in `html/publications.html`, the Research Directions link, and `bibs/fspta.html` unchanged.
- Make the following `[C16]` item the first 2026 selected publication without an unnecessary top margin.

---

## Phase 1: Update Selected Publications

### [x] Task 1.1: Remove the JSS selected entry
- [x] Delete the `[J5]` list item from the 2026 Selected Publications list in `index.html`.
- [x] Normalize the first remaining 2026 list item's spacing.

## Phase 2: Verify and Document

### [x] Task 2.1: Verify scope
- [x] Confirm `[J5]` is absent from active Selected Publications.
- [x] Confirm `[J5]` remains in the Full Publications list, Research Directions, and BibTeX.
- [x] Run HTML/JavaScript sanity checks and `git diff --check`.

### [x] Task 2.2: Close the LDD session
- [x] Mark all plan tasks complete.
- [x] Update `docs/PROGRESS.md` with status, verification, changed files, next steps, and blockers.

## Verification
- [x] The active Selected Publications block contains no `[J5]` entry.
- [x] The full publication record and supporting metadata remain unchanged.
- [x] The first remaining 2026 selected item has correct spacing.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
