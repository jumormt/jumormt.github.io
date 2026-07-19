# Plan: Rename Alumni and Simplify the Visitor Globe

**Epic:** E0: Site Maintenance Baseline

## Summary

Rename the former-supervisee group from Previous to Alumni and simplify the visitor footer to match the compact ClustrMaps globe treatment used by the supplied reference homepage. Preserve the existing visitor identity, Busuanzi history adjustment, and archived-map access while removing the decorative card treatment.

**Decisions locked in:**
- Use the conventional heading `Alumni`.
- Follow the reference site's 150×150 ClustrMaps `globe.js` approach.
- Keep the existing ClustrMaps data token unchanged.
- Retain a compact link to the preserved 23 February 2026 map snapshot when the live globe is unavailable.
- Keep the Busuanzi counter and historical `+20000` adjustment.

---

## Phase 1: Content and Globe Refresh

### [x] Task 1.1: Rename the supervision group
- [x] Change the Supervision subheading `Previous` to `Alumni`.
- [x] Preserve all five former-supervisee entries and their details.

### [x] Task 1.2: Replace the decorative visitor card
- [x] Remove the gradient, large card, and wide archived-map presentation.
- [x] Add a compact 150×150 globe area using `https://clustrmaps.com/globe.js` with the existing token.
- [x] Retain concise loading/error messaging and an archived snapshot link.
- [x] Keep the visit-count pill legible without relying on the third-party container's display style.

## Phase 2: Verify and Document

### [x] Task 2.1: Verify behavior and scope
- [x] Confirm the five Alumni entries are unchanged apart from the heading.
- [x] Confirm the globe loader uses the original token and no legacy map script remains.
- [x] Confirm Busuanzi markup and native offset logic remain intact.
- [x] Confirm local preview, JavaScript syntax, and `git diff --check` pass.

### [x] Task 2.2: Close the LDD session
- [x] Mark plan tasks complete.
- [x] Update `docs/PROGRESS.md` with status, tests, files, next steps, and blockers.

## Verification
- [x] Supervision uses `Alumni` and still contains five former-supervisee entries.
- [x] Visitor presentation is compact and centered around a 150×150 globe.
- [x] Existing visitor data token and historical snapshot access are preserved.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
