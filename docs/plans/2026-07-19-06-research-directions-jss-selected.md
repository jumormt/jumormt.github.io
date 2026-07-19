# Plan: Refresh Research Directions and Select the JSS Paper

**Epic:** E0: Site Maintenance Baseline

## Summary

Synchronize the homepage Research Directions with the three papers most recently added to the Full List, and promote the JSS flow-sensitive pointer-analysis paper to Selected Publications. Replace its preprint BibTeX with the verified journal metadata and keep the selected/full entries aligned.

**Decisions locked in:**
- Add `[J5]` to Pointer analysis, `[J4]` to Vulnerability detection, and `[C17]` to Malware detection.
- Add only `[J5]` to Selected Publications; do not automatically select `[J4]` or `[C17]`.
- Keep the existing `[J5]` identifier, equal-contribution annotations, CORE-A and CCF-B labels.
- Use DOI `10.1016/j.jss.2026.113027` and the existing `bibs/fspta.html` link; do not invent a PDF or slides link.
- Update `bibs/fspta.html` from the arXiv record to verified JSS volume/article metadata.

---

## Phase 1: Synchronize Research and Publication Content

### [x] Task 1.1: Refresh Research Directions
- [x] Add `[J5]: JSS '26` to Pointer analysis and specification inference.
- [x] Add `[J4]: TOSEM '26` to Vulnerability detection.
- [x] Add `[C17]: ISSTA '26` to Malware detection.

### [x] Task 1.2: Add JSS to Selected Publications
- [x] Add `[J5]` to the 2026 Selected Publications list in `index.html`.
- [x] Preserve the verified author order, equal-contribution markers, and journal rankings.
- [x] Link the DOI and matching BibTeX without placeholder PDF or slides buttons.

### [x] Task 1.3: Synchronize Full List and BibTeX
- [x] Use the canonical DOI and expose the BibTeX link in `html/publications.html`.
- [x] Update `bibs/fspta.html` to the verified Journal of Systems and Software record.

## Phase 2: Verify and Document

### [x] Task 2.1: Verify metadata and duplication
- [x] Confirm the three new research-direction references target the intended papers.
- [x] Confirm `[J5]` metadata and annotations match across selected and full lists.
- [x] Confirm DOI and BibTeX links resolve and no placeholder assets were added.
- [x] Run JavaScript syntax validation and `git diff --check`.

### [x] Task 2.2: Close the LDD session
- [x] Mark plan tasks complete.
- [x] Update `docs/PROGRESS.md` with status, tests, files, next steps, and blockers.

## Verification
- [x] Research Directions includes `[J5]`, `[J4]`, and `[C17]` in the correct topics.
- [x] Selected Publications contains one `[J5]` entry under 2026.
- [x] Full and selected `[J5]` entries agree on title, authors, annotations, venue, and labels.
- [x] BibTeX contains the journal DOI, volume 242, and article number 113027.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
