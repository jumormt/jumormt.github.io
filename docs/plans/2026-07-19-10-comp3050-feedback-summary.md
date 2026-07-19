# Plan: Publish a Privacy-Safe COMP3050 Feedback Summary

**Epic:** E0: Site Maintenance Baseline

## Summary

Create a public-facing summary page for the 2026 S1 COMP3050 student feedback without publishing the internal PDF. Present only anonymous aggregate ratings, response context, and carefully paraphrased positive themes, then link the page from the corresponding Teaching Experience entry.

**Decisions locked in:**
- Do not copy the source PDF into the repository or expose it through any link.
- Omit demographics, institutional reference identifiers, and response-level comments.
- Do not use verbatim student quotations.
- State that the page contains selected aggregate highlights and paraphrased themes, not the full report.
- Include the 44.4% response rate for transparency, while omitting the response count from the public page.
- Use four concise aggregate categories based directly on the reported 4.7–4.8/5 teaching dimensions.

---

## Phase 1: Create and Link the Summary

### [x] Task 1.1: Create the feedback page
- [x] Add `html/comp3050-feedback-2026s1.html` using the existing supporting-page structure.
- [x] Present aggregate rating cards, response context, and paraphrased feedback themes.
- [x] Add a clear privacy/method note and homepage navigation.

### [x] Task 1.2: Link from Teaching Experience
- [x] Add a `Student Feedback Highlights` link to the 2026 S1 COMP3050 entry in `index.html`.
- [x] Confirm the relative path resolves in local preview.

## Phase 2: Verify and Document

### [x] Task 2.1: Verify privacy and accuracy
- [x] Confirm the source PDF was not copied into the repository.
- [x] Confirm the summary contains no demographic details, identifiers, emails, or verbatim comments.
- [x] Confirm ratings and the published response rate match the source report.
- [x] Confirm local links, HTML structure, JavaScript syntax, and `git diff --check` pass.

### [x] Task 2.2: Close the LDD session
- [x] Mark plan tasks complete.
- [x] Update `docs/PROGRESS.md` with status, tests, files, next steps, and blockers.

## Verification
- [x] Public summary is aggregate and paraphrased only.
- [x] Internal PDF remains outside the repository.
- [x] COMP3050 Teaching Experience entry links to the summary.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
