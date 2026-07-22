# Plan: Remove the 4.7 Feedback Highlight

**Epic:** E0: Site Maintenance Baseline

## Summary

Remove the Constructive Guidance 4.7/5 card and all public mention of that score from the COMP3050 feedback highlights page. Retain the three selected teaching indicators that each received 4.8/5.

**Decisions locked in:**
- Remove the entire Constructive Guidance card rather than merely hiding its number.
- Keep the privacy/method note concise and state only that the displayed indicator groups received 4.8/5.
- Preserve the remaining ratings, response rate, and paraphrased positive themes.

---

## Phase 1: Refine the Feedback Page

### [x] Task 1.1: Remove the lower rating
- [x] In `html/comp3050-feedback-2026s1.html`, remove the Constructive Guidance card.
- [x] Remove every public occurrence of `4.7` and update the method note for the three displayed 4.8 groups.

## Phase 2: Verify and Document

### [x] Task 2.1: Verify the page
- [x] Confirm the page contains three rating cards, each displaying 4.8/5.
- [x] Confirm neither `4.7` nor `Constructive guidance` remains in the public page.
- [x] Check local HTML response and `git diff --check`.

### [x] Task 2.2: Close the LDD session
- [x] Mark tasks complete and update `docs/PROGRESS.md` with results.

## Verification
- [x] Only three 4.8/5 teaching indicators are shown.
- [x] No public mention of the 4.7 score remains.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
