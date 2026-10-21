# Plan: Annotate ICSE 2027 Direct Acceptances

**Epic:** E0: Site Maintenance Baseline

## Summary

Annotate both ICSE 2027 papers with the user-supplied Direct Accept outcome and direct acceptance count of 119 out of 2375 (5.01%, rounded to two decimal places).

**Decisions locked in:**
- Add a `Direct Accept` badge and `direct acceptance rate: 119/2375=5.01%` to `[C21]` in Selected and Full Publications and `[C22]` in Full Publications only.
- Label the fraction specifically as the direct acceptance rate; do not describe it as the overall conference acceptance rate.
- Update both acceptance news items to say “has been directly accepted”.
- Preserve titles, author order, author-role annotations, links, and the user's Full-List-only preference for `[C22]`.
- Continue the user's explicit commit/push authorization for this follow-up to the same publication update.

## Tasks and Verification

- [x] Update the three publication entries and two news items in `index.html` and `html/publications.html`.
- [x] Verify arithmetic, exact update counts, preserved author roles/selection, matching `[C21]` metadata, and unrelated content preservation; run `git diff --check` and obtain independent review.
- [x] Update `docs/PROGRESS.md` and prepare the verified follow-up for the authorized commit/push to `main`.

## Outcome

All three publication entries now show `Direct Accept` and `direct acceptance rate: 119/2375=5.01%`; both news items say “directly accepted”. Decimal arithmetic, exact counts, matching C21 metadata, preserved author roles, C22 Full-List-only scope, and exact preservation of all unrelated HTML passed. Independent review found no issues; `git diff --check` passed. Remote main was fetched and matched local HEAD before this change. No browser visual inspection performed; no links or assets changed.
