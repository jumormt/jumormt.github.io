# Plan: Hide the Homepage Tools Section

**Epic:** E0: Site Maintenance Baseline

## Summary

Temporarily hide the homepage Tools section without deleting its content. Comment out both the section and its navigation link, then shift downstream section backgrounds so the visible layout continues to alternate.

**Decisions locked in:**
- Preserve the Tools HTML inside comments for easy restoration.
- Do not leave a sidebar link pointing to a hidden anchor.
- Keep visible homepage sections alternating between white and light grey.

---

## Phase 1: Hide Tools

### [x] Task 1.1: Comment out Tools markup
- [x] In `index.html`, comment out the Tools sidebar navigation link.
- [x] Comment out the complete Tools content section without deleting it.

### [x] Task 1.2: Preserve visible section alternation
- [x] Shift the Education, Grants & Awards, and Misc background classes after hiding Tools.

## Phase 2: Verify and Document

### [x] Task 2.1: Verify the homepage
- [x] Confirm there is no active `#tools` navigation link or visible `id="tools"` section.
- [x] Confirm the Tools content remains recoverable in HTML comments.
- [x] Check local HTTP response and `git diff --check`.

### [x] Task 2.2: Close the LDD session
- [x] Mark tasks complete and update `docs/PROGRESS.md` with results.

## Verification
- [x] Tools is absent from the rendered navigation and page.
- [x] Tools source content remains commented in `index.html`.
- [x] Visible section backgrounds alternate correctly.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
