# Plan: Remove Direct Accept Badges

**Epic:** E0: Site Maintenance Baseline

## Summary

Remove the `Direct Accept` badges from the two ICSE 2027 papers, retaining the existing direct acceptance rate under each author list as requested.

## Scope

- Remove the badge from `[C21]` in Selected and Full Publications and `[C22]` in Full Publications only.
- Keep `ICSE '27 (direct acceptance rate: 119/2375=5.01%)`, authors, links, news, and selection unchanged.
- Continue the existing commit/push authorization for this publication correction.

## Tasks

- [x] Remove exactly three badge spans in `index.html` and `html/publications.html`.
- [x] Verify the diff contains only these HTML removals, all three rates remain, and `[C22]` remains outside Selected; run `git diff --check` and obtain an independent review.
- [x] Update `docs/PROGRESS.md` and prepare the verified correction for commit/push.

Verification: exact HTML comparison and independent review confirm only the three badge removals. All rate lines and other content remain unchanged; `git diff --check` passed.
