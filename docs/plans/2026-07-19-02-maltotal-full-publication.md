# Plan: Add New Papers to the Full Publication List

**Epic:** E0: Site Maintenance Baseline

## Summary

Add the accepted ISSTA 2026 paper “MalTotal”, the 2026 TOSEM paper identified by DOI `10.1145/3807456`, and the 2026 JSS paper identified by ScienceDirect PII `S0164121226002608` to the standalone Full List only. Preserve the verified author orders and user-specified equal-contribution/corresponding-author annotations while following the existing 2026 publication formatting.

**Decisions locked in:**
- Edit only `html/publications.html`; do not add these papers to Selected Publications or research-topic links on the homepage.
- Assign the next conference-paper identifier, `[C17]`.
- Assign the next journal-paper identifier, `[J4]`.
- Assign the subsequent journal-paper identifier, `[J5]`, to the JSS paper.
- Do not display author email addresses.
- Mark Xiao Cheng and Haoyu Wang as corresponding authors on `[J4]`, per the user's correction.
- Mark Jiahao Zhang and Xiao Cheng as equal contributors on `[J5]`, per the user's instruction.
- Link the venue to the official ISSTA 2026 research-papers page; do not invent PDF or BibTeX metadata that is not yet available.
- Do not show an acceptance rate on the new MalTotal `[C17]` entry.
- Link the TOSEM paper to the ACM DOI supplied by the user.

---

## Phase 1: Full-List Publication Entry

### [x] Task 1.1: Add the ISSTA 2026 paper
- [x] In `html/publications.html`, add `[C17]` at the top of the 2026 list.
- [x] Include the verified title and author order, with only Xiao Cheng bolded and no `<sup>*</sup>` annotation.
- [x] Match the existing ISSTA 2026 venue labels while omitting the acceptance rate as requested.

### [x] Task 1.2: Add the 2026 TOSEM paper
- [x] In `html/publications.html`, add `[J4]` to the 2026 list using the Crossref-verified title and author order.
- [x] Bold Xiao Cheng, mark Xiao Cheng and Haoyu Wang with `<sup>*</sup>`, and link the entry to DOI `10.1145/3807456`.
- [x] Match the existing TOSEM venue and ranking-label format.

### [x] Task 1.3: Add the 2026 JSS paper
- [x] In `html/publications.html`, add `[J5]` using the Crossref-verified title, author order, venue, and DOI.
- [x] Mark Jiahao Zhang and bolded Xiao Cheng with `<sup>#</sup>`; do not add unrequested corresponding-author annotations.
- [x] Match the existing journal publication and ranking-label format.

## Phase 2: Verification and Documentation

### [x] Task 2.1: Verify scope and content
- [x] Confirm `[C17]`, `[J4]`, and `[J5]` each appear once and only in `html/publications.html`.
- [x] Confirm all titles, author orders, venues, labels, and user-specified author annotations.
- [x] Confirm the official ISSTA link resolves and lists the paper.
- [x] Confirm the ACM DOI and Crossref metadata resolve for the TOSEM paper.
- [x] Confirm the supplied ScienceDirect link is used and Crossref metadata resolves for the JSS paper.
- [x] Inspect the diff and run `git diff --check`.

### [x] Task 2.2: Complete LDD records
- [x] Mark plan tasks complete.
- [x] Update `docs/PROGRESS.md` with status, verification, changed files, next steps, and blockers.

## Verification

- [x] Full-list HTML entries inspected manually.
- [x] Official ISSTA page and Crossref DOI metadata checked for titles and author orders.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` updated with results.
