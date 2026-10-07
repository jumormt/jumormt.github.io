# Plan: Add ASE 2026 Distinguished Reviewer Award

**Epic:** E0: Site Maintenance Baseline

## Summary

Add the user-reported ASE 2026 Distinguished Reviewer Award to homepage News and Grants & Awards.

**Decisions locked in:**
- Preserve the user's award wording.
- Date the News announcement `10/2026`, the current announcement month, and place it after pinned entries before older unpinned news.
- Add the award as a separate 2026 list item at the top of Grants & Awards.
- No award URL was supplied; use plain text without a placeholder link.

## Phase 1: Homepage Update

- [x] Add the News item in `index.html` with `images/new.gif`.
- [x] Add the matching Grants & Awards item in `index.html`.

## Verification and Documentation

- [x] Inspect both entries, wording, dates, ordering, and HTML diff.
- [x] Run `git diff --check`.
- [x] Complete this plan and update `docs/PROGRESS.md` with verification, files, next steps, and blockers.
