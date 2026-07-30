# Plan: Upload Three Publication PDFs

**Epic:** E0: Site Maintenance Baseline

## Summary

Publish the user-supplied PDFs for Jiahao Zhang's JSS 2026 paper, Jiawei Yang's ISSTA 2026 paper, and the ISSTA 2026 MalTotal paper. Add local PDF links wherever the corresponding publication is presented, while preserving the current Selected/Full List scope and all existing metadata.

**Decisions locked in:**
- Store the files as `data/jss26_fspta.pdf`, `data/issta26_mosps.pdf`, and `data/issta26_maltotal.pdf`.
- Keep `[J5]` and `[C17]` out of Selected Publications; add a PDF button only to their Full List entries.
- Add the `[C16]` PDF button to both Selected Publications and the Full List.
- Retarget the relevant Research Directions links to the new local PDFs.
- Preserve existing DOI, Page, Slides, and BibTeX buttons where present.

---

## Phase 1: Publish PDF Assets

### [x] Task 1.1: Add the three PDFs
- [x] Copy Jiahao Zhang's supplied PDF to `data/jss26_fspta.pdf`.
- [x] Copy Jiawei Yang's supplied ISSTA PDF to `data/issta26_mosps.pdf`.
- [x] Copy the supplied MalTotal PDF to `data/issta26_maltotal.pdf`.
- [x] Confirm the copied files match the source checksums and remain readable.

## Phase 2: Connect Publication Links

### [x] Task 2.1: Update homepage links
- [x] In `index.html`, link the `[J5]`, `[C16]`, and `[C17]` Research Directions references to their local PDFs.
- [x] Add the `[C16]` PDF button to Selected Publications without changing the selected-paper scope.

### [x] Task 2.2: Update Full List links
- [x] In `html/publications.html`, add local PDF buttons to `[J5]`, `[C16]`, and `[C17]`.
- [x] Preserve all existing publication metadata and supporting buttons.

## Phase 3: Verification and Documentation

### [x] Task 3.1: Verify assets and links
- [x] Confirm PDF titles, page counts, first-page rendering, and source/destination checksums.
- [x] Confirm every new relative URL resolves through a local HTTP preview.
- [x] Manually inspect affected HTML and run `git diff --check`.

### [x] Task 3.2: Complete LDD records
- [x] Mark plan tasks complete.
- [x] Update `docs/PROGRESS.md` with status, verification, changed files, next steps, and blockers.

## Verification

- [x] Three local PDF assets are readable and match their supplied source files.
- [x] `[C16]` has PDF buttons in Selected and Full Lists.
- [x] `[J5]` and `[C17]` have PDF buttons in the Full List only.
- [x] Relevant Research Directions links target the matching local PDFs.
- [x] Existing DOI, Page, Slides, and BibTeX links remain intact.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
