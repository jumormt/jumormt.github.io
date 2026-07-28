# Plan: Add Two ASE 2026 Publications and News

**Epic:** E0: Site Maintenance Baseline

## Summary

Add the two newly accepted ASE 2026 main-track papers to the standalone Full Publication List and announce both acceptances in the homepage News section. Preserve the supplied author orders and corresponding-author annotations while matching the site's existing 2026 publication and news conventions.

**Decisions locked in:**
- Add the papers only to `html/publications.html`; do not add them to Selected Publications.
- Assign `[C18]` to “RamFuzz” and `[C19]` to “Harnessing Uncertainty in Code Language Models”, following the order supplied by the user.
- Mark Xiao Cheng and Siqi Ma as corresponding authors on `[C18]`.
- Mark only Xiao Cheng as corresponding author on `[C19]`.
- Use the existing ASE 2026 research-track page while paper-specific PDF and BibTeX links are not available.
- Add separate `07/2026` News items immediately after the older pinned announcements.

---

## Phase 1: Full Publication List

### [x] Task 1.1: Add the ASE 2026 papers
- [x] Add `[C18]` and `[C19]` at the top of the 2026 list in `html/publications.html`.
- [x] Preserve the supplied titles and author orders.
- [x] Bold Xiao Cheng and apply `<sup>*</sup>` to each supplied corresponding author.
- [x] Match the existing `CORE-A*`, `CCF-A`, venue, and Page-link presentation.

## Phase 2: Homepage News

### [x] Task 2.1: Announce both acceptances
- [x] Add two `07/2026` items to `#news` in `index.html`.
- [x] Prefix both with `images/new.gif` and link ASE 2026 to the research-track page.
- [x] Keep pinned items first and preserve newest-first chronological ordering for unpinned news.

## Phase 3: Verification and Documentation

### [x] Task 3.1: Verify content and scope
- [x] Confirm each new publication occurs exactly once and only in the Full List.
- [x] Confirm titles, author orders, numbering, annotations, labels, and News ordering.
- [x] Confirm the ASE page link and affected local pages respond successfully.
- [x] Run `git diff --check` and inspect the final diff.

### [x] Task 3.2: Complete LDD records
- [x] Mark plan tasks complete.
- [x] Update `docs/PROGRESS.md` with status, verification, changed files, next steps, and blockers.

## Verification

- [x] Full-list and News HTML inspected manually.
- [x] New publication identifiers and scope checked.
- [x] Local page/link checks pass.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` updated with results.
