# Plan: Add MajorDomo Catalyst Grant

**Epic:** E0: Site Maintenance Baseline

## Summary

Add the user-supplied Macquarie University internal teaching Catalyst Grant as a separate Grants & Awards entry. Do not update News.

**Decisions locked in:**
- Preserve the title: MajorDomo at Scale: Making AI-Assisted Continuous Formative Feedback Portable and Sustainable.
- List Ansgar Fehnker as primary contact, followed by Nader Hanna, Xiao Cheng, and Gunjan Chamania in the supplied order.
- Identify the School of Computing and Macquarie University College affiliations and bold Xiao Cheng.
- Omit email addresses, form instructions, and page labels from the public entry.
- Add no unsupported funding amount or link. Ask the user for the award year; omit the year if not confirmed rather than inventing one.
- Preserve the existing 2025 formative-feedback grant as a separate record.

## Implementation

- [x] Resolve the year presentation and add the entry in `index.html` under Grants & Awards only.

## Verification and Completion

- [x] Inspect title, team order, primary-contact role, affiliations, and bold name.
- [x] Confirm News and all HTML outside the award insertion are unchanged; run `git diff --check`.
- [x] Update `docs/PROGRESS.md`, commit, and push under the established session workflow.

## Outcome

Added an undated entry while the requested award-year clarification remains unanswered. Verified the exact title, four members in order, primary-contact role, affiliations, and bold self-name. Removing the single added line reproduces the prior HTML exactly, proving News and the 2025 grant are unchanged. No links or assets added; `git diff --check` passes. No browser visual check performed.

## Follow-up: Confirmed Award Year and Funding Inquiry

The user confirmed receiving the award notification today, 2026-10-07.

- [x] Prefix the existing award entry with `2026`; keep News unchanged.
- [x] Investigate public Catalyst funding information, distinguishing scheme amounts from this project's actual approved budget.
- [x] Verify the year-only HTML change and update the progress record, commit, and push.

Follow-up outcome: added the confirmed 2026 year. The official 2025 iViva Catalyst award records AUD $25,000 (https://researchers.mq.edu.au/en/prizes/winner-2025-innovation-in-education-grant-catalyst-award-25000/), but no public record established the actual 2026 MajorDomo allocation. No funding amount added to the homepage. Verified that the only HTML change is the year prefix; `git diff --check` passed.
