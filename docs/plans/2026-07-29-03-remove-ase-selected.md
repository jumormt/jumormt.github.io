# Plan: Remove ASE Papers from Selected Publications

**Epic:** E0: Site Maintenance Baseline

## Summary

Remove `[C18]` RamFuzz and `[C19]` Harnessing Uncertainty from the homepage Selected Publications list while retaining both papers in the Full Publication List, News, Research Directions, and the updated biography. Retarget the Research Directions references to the ASE 2026 research-track page because the papers will no longer have entries in the homepage Publications section.

**Decisions locked in:**
- Remove only the two Selected Publication entries from `index.html`.
- Restore `[C16]` as the first 2026 Selected Publication without extra top margin.
- Keep the Full Publication List, News, and biography unchanged.
- Keep `[C18]` under Memory safety and Dynamic testing and `[C19]` under Vulnerability detection.
- Replace the three `#publications` links for `[C18]`/`[C19]` with the ASE 2026 research-track URL.

## Phase 1: Selected Publications and Research Links

### [x] Task 1.1: Remove the two Selected entries
- [x] Delete the complete `[C18]` and `[C19]` list items from the 2026 Selected Publications list in `index.html`.
- [x] Remove `style="margin-top:8px"` from `[C16]` so it becomes the correctly spaced first item.

### [x] Task 1.2: Retarget Research Directions
- [x] Change both `[C18]` Research Directions links from `#publications` to `https://conf.researchr.org/track/ase-2026/ase-2026-research-track`.
- [x] Change the `[C19]` Research Directions link to the same ASE page.
- [x] Preserve the existing topic mappings and venue labels.

## Phase 2: Verification and Documentation

### [x] Task 2.1: Verify scope and page behavior
- [x] Confirm `[C18]` and `[C19]` are absent from Selected Publications and retained once each in `html/publications.html`.
- [x] Confirm Research Directions retains two `[C18]` references and one `[C19]` reference, all linked to ASE.
- [x] Confirm the biography and News remain unchanged.
- [x] Confirm the local homepage returns HTTP 200 and run `git diff --check`.

### [x] Task 2.2: Complete LDD records
- [x] Mark plan tasks complete.
- [x] Update `docs/PROGRESS.md` with status, verification, changed files, next steps, and blockers.

## Verification

- [x] Selected Publications scope inspected.
- [x] Full List, News, biography, and Research Directions checked.
- [x] Local homepage HTTP check passes.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` updated.
