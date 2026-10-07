# Plan: Add NEUROSYMLAND to Selected and Full Publications

**Epic:** E0: Site Maintenance Baseline

## Summary

Add the user-supplied IROS 2026 paper as `[C20]` at the start of the 2026 Selected and Full Publication lists, with CORE-A and Best Paper Candidate badges.

**Decisions locked in:**
- Use the supplied title, author order, conference, ranking, and candidate status.
- Capitalize Sebastian Schroder's surname consistently with the other names; bold Xiao Cheng and mark only Xi Zheng with `<sup>*</sup>`.
- No PDF, DOI, or BibTeX link was supplied; add no placeholder links.
- Match existing badge and publication spacing conventions.

## Phase 1: Publication Entries

- [x] Add matching `[C20]` entries to `index.html` and `html/publications.html`.
- [x] Preserve spacing before the previously first entries.

## Verification and Documentation

- [x] Inspect affected HTML and confirm identical metadata, author order, annotation, badges, year, and unique numbering.
- [x] Run `git diff --check`.
- [x] Update `docs/PROGRESS.md` with completion, verification, changed files, next steps, and blockers; archive older session logs while preserving history.
